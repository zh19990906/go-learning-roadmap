# 数据库测试与常见坑

关注：
- rows.Close / rows.Err
- transaction rollback
- context timeout
- 唯一键冲突
- NULL 扫描
- SQL 参数化
- integration test 数据隔离

集成测试最好使用独立测试库/容器，并保证可重复执行。