# database/sql 与连接池

`sql.DB` 不是“单条连接”，而是数据库连接池句柄。

```go
db, err := sql.Open(driver, dsn)
err = db.PingContext(ctx)
```

常配置：`SetMaxOpenConns / SetMaxIdleConns / SetConnMaxLifetime`。

Python 对照：类似 SQLAlchemy engine/pool 的部分职责。