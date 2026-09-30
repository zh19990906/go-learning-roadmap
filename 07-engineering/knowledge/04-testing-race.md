# Test / Mock / Race

测试包含单元测试、集成测试、少量端到端测试。

Mock/Fake 用来控制依赖，但不要过度 mock 实现细节。

常用：

```bash
go test ./...
go test -race ./...
go test -cover ./...
```

race detector 是 Go 并发项目的重要工具。