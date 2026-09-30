# 文件与 IO

常用包：`os`、`io`、`bufio`。

```go
data, err := os.ReadFile(path)
err = os.WriteFile(path, data, 0644)
```

流式读取时会接触 `io.Reader` / `io.Writer`。

Python 对照：`open/read/write`；Go 更强调接口与显式错误。

注意：
- 打开资源后及时 defer Close。
- 明确处理文件不存在、权限、部分读取等错误。
