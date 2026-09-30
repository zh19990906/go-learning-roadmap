# Structured Logging

结构化日志记录字段，而不是拼接长字符串。

标准库可用 `log/slog`：

```go
slog.Info("request completed", "status", 200, "duration", d)
```

常见字段：request_id、method、path、status、duration、error。

不要记录密码、token 等敏感信息。