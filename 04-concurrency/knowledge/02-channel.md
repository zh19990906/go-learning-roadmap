# Channel

Channel 用于 goroutine 间传值/同步：

```go
ch := make(chan int)
ch <- 1
v := <-ch
```

缓冲：

```go
ch := make(chan int, 10)
```

Python 对照：某些场景类似 queue。

只传信号常用：

```go
chan struct{}
```

注意：
- 谁发送谁通常负责 close。
- 向已关闭 channel 发送会 panic。
- 从已关闭 channel 可继续读到零值，配合 `v, ok := <-ch` 判断。
