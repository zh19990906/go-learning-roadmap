# select 与 timeout

```go
select {
case v := <-ch:
    _ = v
case <-time.After(time.Second):
}
```

`select` 在多个 channel 操作间等待。

可用于：
- timeout
- 多路复用
- 取消信号
- 非阻塞尝试（default）

注意：频繁循环里直接创建 `time.After` 可能产生额外定时器，应理解生命周期。