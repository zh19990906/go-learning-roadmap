# REST 与参数校验

REST 常见映射：
- GET：列表/详情
- POST：创建
- PUT/PATCH：更新
- DELETE：删除

输入必须校验 path/query/body、必填字段、长度/范围和业务冲突。

Python FastAPI 常自动做 schema 校验；Go 标准库通常更显式。