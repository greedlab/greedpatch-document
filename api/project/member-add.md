# 工程添加成员

系统管理员或工程管理员可操作

## URI

```
/projects/:project/members
```

## 请求方式

```
POST
```

## 包头

```
Authorization: Bearer <token>
```

## 请求参数

| key | 类型 | 是否必须 | 说明 | 备注 | 例子 |
| --- | --- | --- | --- | --- | --- |
| :project | string | 是 | 工程 ID |  |  |
| email | string | 是 | 邮箱 |  |  |

## 成功

### 成功返回状态码

| 状态码 | 说明 | 备注 |
| --- | --- | --- |
| 204 | 添加成功 | 无返回数据 |

## 失败

### 失败返回状态码

| 状态码 | 说明 | 备注 |
| --- | --- | --- |
| 401 | token 失效 |  |
| 403 | 无权限访问工程/无权限添加成员 |  |
| 422 | 工程不存在/用户不存在/成员已添加 |  |
| 500 | 服务器内部错误 |  |

### 出错返回数据实例

```json
{
  "message": "用户不存在"
}
```

## example

```
curl -H "Accept: application/vnd.greedlab+json" -H "Content-Type: application/json" -H "Authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpYXQiOjE0NzIxODEyMzUxMzksImV4cCI6MTQ3NDc3MzIzNTEzOSwiaWQiOiI1N2JmOWJhMWNlODRjOTk5YTBlZmQ1YjciLCJzY29wZSI6ImRlZmF1bHQifQ.ESm0koiqDc8nfRTiHp4Uwo7PKNCtPRU5dfVfLT6MUSk" -X POST -d '{"email":"test1@greedlab.com"}' localhost:4002/projects/57bfebadd2dbc1cea6430f8b/members
```
