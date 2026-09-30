# Stage 08 · 综合项目

## 项目
完成一个可部署的 Go 任务管理系统。

## 推荐技术栈
- Go
- Gin
- PostgreSQL
- Redis
- JWT
- Docker Compose

## 核心功能
- 注册 / 登录
- JWT 鉴权
- Task CRUD
- 分页与搜索
- 状态与优先级
- 截止时间
- PostgreSQL Repository
- Redis 缓存
- 异步任务
- 日志
- 测试
- Graceful Shutdown
- Docker Compose

## 推荐结构
```text
cmd/server/
internal/handler/
internal/service/
internal/repository/
internal/model/
internal/middleware/
config/
migrations/
```

## 最终验收
能从零启动服务、运行测试、连接数据库与 Redis，并通过 README 让其他开发者在本地运行项目。
