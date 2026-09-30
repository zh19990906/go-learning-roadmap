# httptest

标准库可直接测试 Handler：

```go
req := httptest.NewRequest(http.MethodGet, "/todos", nil)
rec := httptest.NewRecorder()
handler.ServeHTTP(rec, req)
```

断言状态码、header、JSON body。

优先测试 handler 行为，不必每次启动真实 TCP server。