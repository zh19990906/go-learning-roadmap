# Query / QueryRow / Exec

```go
db.ExecContext(ctx, ...)
db.QueryRowContext(ctx, ...)
db.QueryContext(ctx, ...)
```

`Query` 返回 rows，要 `defer rows.Close()`，遍历后检查 `rows.Err()`。

参数使用占位符，避免字符串拼接 SQL 注入。