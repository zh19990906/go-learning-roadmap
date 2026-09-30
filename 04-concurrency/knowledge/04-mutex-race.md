# Mutex 与 Race

共享内存写入需要同步：

```go
mu.Lock()
defer mu.Unlock()
```

读多写少可了解 `sync.RWMutex`。

Race detector：

```bash
go test -race ./...
```

Python 的 GIL 不能类比成“Go 自动安全”；Go 多 goroutine 访问共享数据依然会数据竞争。

原则：
- 数据所有权清晰
- channel 适合传递所有权/事件
- mutex 适合保护共享状态
