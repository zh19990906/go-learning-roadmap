# Worker Pool 与常见坑

Worker Pool = 固定数量 worker + jobs channel + results。

目标：限制并发，避免无限开 goroutine。

常见坑：
- goroutine 泄漏
- channel 无人接收导致阻塞
- close 时机错误
- WaitGroup Add/Done 不匹配
- 捕获循环变量（新 Go 版本语义已改善，但仍应理解作用域）

设计时先画清楚：谁生产、谁消费、谁关闭、谁取消。
