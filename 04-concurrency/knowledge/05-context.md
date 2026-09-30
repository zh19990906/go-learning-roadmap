# Context

`context.Context` 用于传播：
- 取消
- 超时/截止时间
- request-scoped value（谨慎）

```go
ctx, cancel := context.WithTimeout(parent, time.Second)
defer cancel()
```

监听：

```go
select {
case <-ctx.Done():
    return ctx.Err()
}
```

Web/DB 调用常传 ctx。不要把可选业务参数塞进 context。
