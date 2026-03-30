---
name: development
description: 编码阶段规范：按任务清单逐项开发，每项完成后执行 code review，通过后合并分支，再开发下一项
---

# 开发

## 目的
按任务清单逐项开发，每项经过 review 后才进入下一项。

## 输入
- 任务清单：`03-pre-development` 输出的功能任务清单

## 步骤

- 逐项开发（严禁多项并行），每项必须按以下步骤完成：
  - 创建分支：按 `base.git-workflow` 为当前任务创建功能分支
  - 开发：实现当前任务，遵守 `base.coding-standards`
    - 异步处理：所有异步操作必须有加载状态，不允许无反馈的等待
    - 错误处理：所有错误必须有明确处理，不允许静默失败或空 catch
  - 执行 review：开发完成后必须立即执行 review 本次代码，遵守 `code-review-process`
  - 合并分支：review 通过后 merge 到主分支，删除功能分支
  - 文档同步：若修改了公共模块，同步更新其使用文档和演示入口页面

## 输出
- 模块代码：通过 review 的各模块代码

## Review 检查清单
> 通用规则见 `base.review-base`，代码 review 细则见 `code-review-process`

- 模块完成：所有模块已完成 review，无堆积
- 文档同步：公共模块使用文档和演示入口页面与代码同步
- 分支管理：符合 `base.git-workflow`

## 阶段结束

下一阶段：`05-testing`

#[[file:base.stage-gate.md]]
