---
name: frontend-design
description: 前端模块设计规范，涉及前端时使用
---

# 前端模块设计规范

设计文档需包含以下内容：

- 页面结构：页面列表、层级关系
- 路由设计：路由路径、参数、嵌套关系
- 状态管理：全局状态、局部状态划分
- UI 交互流程：覆盖所有交互状态（空态、加载、错误、成功）
- 组件划分：可复用组件识别，组件职责和接口

## 输出示例

```markdown
## 页面结构
- /login — 登录页
- /dashboard — 首页
  - /dashboard/orders — 订单列表
  - /dashboard/orders/:id — 订单详情

## 状态管理
- 全局：用户信息、权限
- 局部：表单状态、列表筛选条件

## 组件划分
- SearchBar：搜索栏，接收 onSearch 回调
- OrderCard：订单卡片，接收 order 数据
```
