# JSON 编解码

```go
type User struct {
    Name string `json:"name"`
    Age  int    `json:"age"`
}
```

编码：

```go
b, err := json.Marshal(v)
```

解码：

```go
err := json.Unmarshal(b, &v)
```

流式场景用 `json.NewEncoder/Decoder`。

Python 对照：`json.dumps / json.loads`。

注意：只有可导出字段（首字母大写）能被 encoding/json 正常处理。
