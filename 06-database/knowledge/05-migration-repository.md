# Migration 与 Repository

Migration 用版本化 SQL 管 schema 变更。

Repository 隔离数据访问：

```go
type TodoRepository interface {
    Create(ctx context.Context, todo Todo) error
}
```

Python 对照：接近 DAO / repository layer。不要为了“多一层”而创建无价值的转发层。