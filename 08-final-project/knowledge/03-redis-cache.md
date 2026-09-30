# Redis Cache

常见模式：cache-aside。

流程：读缓存 → miss 查 DB → 写缓存。

写操作后要考虑失效/更新缓存。

注意：
- 缓存不是数据库真相来源
- TTL
- key 设计
- stampede
- stale data