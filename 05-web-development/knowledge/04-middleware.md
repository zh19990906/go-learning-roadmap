# Middleware

Middleware 包装 Handler：

```go
func logging(next http.Handler) http.Handler {
    return http.HandlerFunc(func(w http.ResponseWriter, r *http.Request) {
        next.ServeHTTP(w, r)
    })
}
```

常见用途：日志、鉴权、request id、recover、CORS、限流。

注意：不要把业务核心逻辑塞进 middleware。