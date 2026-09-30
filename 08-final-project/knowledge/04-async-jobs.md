# Async Jobs

异步适合邮件、通知、慢任务、可重试任务。

需要设计：
- job payload
- retry
- idempotency
- failure handling
- shutdown 时如何停止 worker

先用 goroutine/channel 理解模型，再考虑外部队列。