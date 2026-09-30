# defer

`defer` 会在当前函数返回前执行：

```go
f, err := os.Open(path)
if err != nil { return err }
defer f.Close()
```

Python 对照：接近 `try/finally` 或 context manager 的清理职责。

常见用途：
- Close 文件/连接
- Unlock mutex
- Recover（谨慎）
- 统计耗时

注意：defer 绑定在函数级，不是普通代码块级。
