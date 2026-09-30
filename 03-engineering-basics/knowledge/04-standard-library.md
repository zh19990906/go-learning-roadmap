# strings / strconv / time

## strings
`Contains / Split / Join / TrimSpace / ToLower`

Python 对照：`in / split / join / strip / lower`

## strconv
字符串与数字/布尔转换：

```go
n, err := strconv.Atoi("123")
s := strconv.Itoa(123)
```

## time
时间：

```go
time.Now()
time.Parse(layout, value)
time.Since(start)
```

Go 时间格式 layout 用固定参考时间 `2006-01-02 15:04:05`，这是常见坑。
