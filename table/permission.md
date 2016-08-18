# permission

权限管理

## 结构

| key | 类型 | 说明 | 备注 | 例子 |
| --- | --- | --- | --- | --- |
| type | int | 权限类型 | [详细说明](#type) |  0 |
| status | int | 权限 | [详细说明](#status) | 0 |
| domains | array | 限定的邮箱域名 | status=2 时有效 | [greedlab.com] |

### type

unequal

| value | 说明 |
| --- | --- |
| 0 | register（默认） |
| 1 | login |

### status

| value | 说明 |
| --- | --- |
| 0 | 所有可用（默认） |
| 1 | 所有禁用 |
| 2 | 限制邮箱可用 |