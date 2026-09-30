# Transaction

```go
tx, err := db.BeginTx(ctx, nil)
```

典型流程：开始事务 → 多步操作 → 任一步失败回滚 → 全部成功提交。

注意：事务尽量短，不要在事务中做慢网络调用。