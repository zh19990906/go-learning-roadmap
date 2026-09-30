# Gin 与 net/http

Gin 提供更方便的路由、参数绑定、中间件 API，但底层仍建立在 `net/http` 上。

学习顺序：
1. 先理解 Request / ResponseWriter / Handler
2. 再迁移 Gin

Python 对照：使用体验更接近 Flask/FastAPI，但 Go 的 error/context/类型系统仍不同。