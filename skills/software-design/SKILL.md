---
name: software-design
description: 软件模块设计、UI 设计与分批确认流程
---

# 软件设计

## 依赖规范
#[[file:../rules/review-base.md]]
#[[file:../rules/git-workflow.md]]
#[[file:../rules/project-structure.md]]
#[[file:frontend-design.md]]
#[[file:backend-design.md]]

## 目的
将需求转化为可执行的模块设计方案，明确模块边界、接口和 UI 交互。

## 输入
- 需求文档：需求清单 + 范围边界说明，或对话上下文

## 步骤

> 每个步骤先输出标题，再输出结果

- 分批设计：设计拆成批次，每批次与开发者 review 确认，记录设计决策
- 文档拆分：根据项目架构，按 `frontend-design` 和 `backend-design` 规范分别输出对应的设计文档
- 模块依赖：所有模块设计完成后，标注模块间的依赖关系
- 写入文档：每个模块单独一个文件，创建入口文档引用所有设计文件（路径遵守 `project-structure` 文档存放规范）
- 执行 review：遵守 `review-base`，通过后才进入下一步
- 提交：review 通过后按 `git-workflow` 提交

## 输出
- 模块划分方案：职责、边界
- 模块依赖关系：标注模块间的依赖，无依赖的模块不需要列出
- 前端设计文档：按 `frontend-design` 规范输出（涉及前端时）
- 后端设计文档：按 `backend-design` 规范输出（涉及后端时）

## Review 检查清单

- 模块职责：单一，边界清晰，无职责重叠
- 前端设计：符合 `frontend-design` 规范（涉及前端时）
- 后端设计：符合 `backend-design` 规范（涉及后端时）
- 模块依赖：依赖关系已标注，无循环依赖
- 需求覆盖：覆盖所有已确认的需求，无遗漏
- 公共模块：已识别，无重复设计
- 敏感信息：设计文档中不包含真实密码、密钥、token 等敏感信息，使用占位符代替

## 阶段结束

下一阶段：`dev-planning`

#[[file:../rules/stage-gate.md]]
