# Struct 与 Method

## struct 是什么
Go 没有 Python 那种 class 体系，常用 struct 表达数据结构：

```go
type Student struct {
    Name string
    Age  int
}
```

方法通过 receiver 绑定：

```go
func (s Student) DisplayName() string {
    return s.Name
}
```

Python 对照：`class` 的“数据 + 方法”在 Go 中通常拆成 `struct + method`。

## 注意
- 字段首字母大写表示可导出。
- Go 更强调组合，而不是复杂继承层级。
