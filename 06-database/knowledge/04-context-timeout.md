# Context 与数据库超时

```go
ctx, cancel := context.WithTimeout(parent, 2*time.Second)
defer cancel()
row := db.QueryRowContext(ctx, query)
```

让请求取消/超时传播到 DB 层。

Repository 优先接收调用方 ctx，不要随意改成 Background。