# Stage 08 · 综合项目

## 学习前先读
进入 [knowledge/README.md](./knowledge/README.md)。

知识目录包含：
- Authentication / JWT
- Task CRUD / Pagination / Search
- Redis Cache
- Async Jobs
- Docker Compose / 部署
- Final Project Checklist

## 项目
完成一个可部署的 Go 任务管理系统。

## 推荐技术栈
- Go
- Gin
- PostgreSQL
- Redis
- JWT
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
