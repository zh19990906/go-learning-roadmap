# Error 处理

Go 用返回值表达错误：

```go
v, err := load()
if err != nil {
    return err
}
```

Python 常用 exception；Go 常用显式 `error` 流程。

包装错误：

```go
fmt.Errorf("load student: %w", err)
```

判断：

```go
errors.Is(err, target)
errors.As(err, &targetType)
```

注意：
- 不要只比较错误字符串。
- 错误信息应补充上下文。
- 能处理就在当前层处理，不能处理就返回上层。
