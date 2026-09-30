# Goroutine 与 WaitGroup

启动：

```go
go work()
```

goroutine 是 Go 的轻量并发执行单元，不等同于 Python thread/asyncio task，但在使用层面可类比“并发任务”。

等待一组 goroutine：

```go
var wg sync.WaitGroup
wg.Add(1)
go func() {
    defer wg.Done()
}()
wg.Wait()
```

注意 Add/Done 数量必须匹配。