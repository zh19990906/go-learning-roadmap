# Stage 04 · 并发编程

## 目标
掌握 Go 最核心的并发模型。

## 学习前先读
进入 [knowledge/README.md](./knowledge/README.md)。

知识目录包含：
- goroutine / WaitGroup
- channel
- select / timeout
- Mutex / race detector
- context
- worker pool / goroutine 泄漏等常见坑

## 阶段项目
实现一个并发任务执行器 / 下载器模拟器，支持并发限制、超时取消、结果统计。

## 阶段验收
能避免常见 goroutine 泄漏与数据竞争，并能判断应该使用 channel 还是 mutex。
