# Graceful Shutdown

收到 SIGTERM/SIGINT 后：
1. 停止接收新请求
2. 等待正在处理的请求
3. 关闭资源
4. 在超时时间内退出

HTTP server 常用：

```go
server.Shutdown(ctx)
```

配合 `signal.NotifyContext`。