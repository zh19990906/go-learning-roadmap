# HTTP 与 net/http

最小服务：

```go
http.HandleFunc("/", func(w http.ResponseWriter, r *http.Request) {
    w.Write([]byte("hello"))
})
http.ListenAndServe(":8080", nil)
```

需要理解 method / path / header / body / status code。

Python 对照：Flask/FastAPI 隐藏了很多 HTTP 细节；Go 建议先学标准库 `net/http`。