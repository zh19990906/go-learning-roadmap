# Handler / JSON / 状态码

Handler：

```go
func(w http.ResponseWriter, r *http.Request)
```

JSON：

```go
w.Header().Set("Content-Type", "application/json")
json.NewEncoder(w).Encode(v)
```

读取 body：

```go
json.NewDecoder(r.Body).Decode(&input)
```

常见状态码：200/201/204/400/401/403/404/409/500。不要所有错误都返回 500。