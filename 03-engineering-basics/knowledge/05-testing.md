# Testing 与 Table-Driven Tests

测试文件：`*_test.go`

```go
func TestAdd(t *testing.T) { ... }
```

Table-driven：

```go
tests := []struct{
    name string
    in int
    want int
}{...}
```

Python 对照：pytest 参数化测试。

常用：

```bash
go test ./...
go test -v ./...
go test -cover ./...
```

注意：测试边界、错误路径、空输入，不只测 happy path。
