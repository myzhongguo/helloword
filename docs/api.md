T# API 文档

## 用户相关接口

### 用户登录
- 请求方法：POST
- 请求路径：/api/login
- 请求参数：
  - username: 用户名
  - password: 密码
- 响应示例：
```json
{
  "token": "jwt_token",
  "userInfo": {
    "username": "testuser",
    "role": "admin"
  }
}
```

### 获取用户信息
- 请求方法：GET
- 请求路径：/api/user
- 请求头：
  - Authorization: Bearer {token}
- 响应示例：
```json
{
  "username": "testuser",
  "email": "test@example.com",
  "avatar": "https://example.com/avatar.png"
}
```

## 数据相关接口

### 获取数据列表
- 请求方法：GET
- 请求路径：/api/data
- 请求参数：
  - page: 页码
  - pageSize: 每页数量
- 响应示例：
```json
{
  "total": 100,
  "list": [
    {
      "id": 1,
      "name": "数据1"
    }
  ]
}
