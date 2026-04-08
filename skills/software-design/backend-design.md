---
name: backend-design
description: 后端模块设计规范，涉及后端时使用
---

# 后端模块设计规范

设计文档需包含以下内容：

- API 设计：接口路径、方法、入参、出参、错误码
- 数据库设计：表结构、字段、索引、关联关系
- 业务逻辑：核心业务流程、异常处理
- 权限设计：角色、权限划分、鉴权方式

## 输出示例

```markdown
## API 设计
| 接口 | 方法 | 入参 | 出参 | 错误码 |
|------|------|------|------|--------|
| /api/users/login | POST | { email, password } | { token, user } | 401 认证失败 |
| /api/orders | GET | ?page&size&status | { list, total } | 403 无权限 |

## 数据库设计
### users 表
| 字段 | 类型 | 说明 |
|------|------|------|
| id | bigint | 主键 |
| email | varchar(255) | 唯一索引 |
| password_hash | varchar(255) | 密码哈希 |

## 权限设计
- admin：全部权限
- user：仅查看和操作自己的数据
```
