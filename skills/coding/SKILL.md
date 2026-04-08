---
name: coding
description: 编码阶段规范：按任务清单逐项开发，每项完成后执行 code review
---

# 编码

## 依赖规范
#[[file:../rules/git-workflow.md]]
#[[file:../rules/coding-standards.md]]
#[[file:../rules/review-base.md]]
#[[file:../rules/web-standards.md]]
#[[file:../code-review/SKILL.md]]

## 目的
按任务清单逐项开发，每项经过 review 后才进入下一项。

## 输入
- 任务清单：功能任务清单，或对话上下文

## 步骤

> 每个步骤先输出标题，再输出结果

- 逐项开发，每项必须按以下步骤完成：
  - 创建分支：按 `git-workflow` 为当前任务创建功能分支
  - 开发：实现当前任务，遵守 `coding-standards`；web 项目同时遵守 `web-standards`
  - 执行 review：开发完成后必须立即执行 review 本次代码，遵守 `code-review` skill
  - 合并分支：review 通过后 merge 到主分支
  - 文档同步：若修改了公共模块，同步更新其使用文档和演示入口页面

## 输出
- 模块代码：通过 review 的各模块代码

## Review 检查清单

- 模块完成：所有模块已完成 review，无堆积
- 文档同步：公共模块使用文档和演示入口页面与代码同步
- 分支管理：符合 `git-workflow`

## 阶段结束

下一阶段：`testing`

#[[file:../rules/stage-gate.md]]
