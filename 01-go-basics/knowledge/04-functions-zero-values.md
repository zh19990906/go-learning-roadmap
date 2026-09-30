# 函数、多返回值与零值

## 函数

```go
func add(a, b int) int {
    return a + b
}
```

Go 不支持函数重载。

## 多返回值

```go
func find(...) (int, bool)
```

非常常见的模式是：

```text
value, ok
```

Python 常见用 None / exception 表达“没有结果”；Go 经常显式返回 bool 或 error。

## 零值

未显式初始化时：

```text
int    -> 0
bool   -> false
string -> ""
pointer/slice/map/function/channel -> nil
```

零值是 Go 设计的重要部分，很多代码会利用零值简化逻辑，例如：

```go
count[x]++
```

## 注意

- int 不能和 nil 比较。
- 一个声明没有返回值的函数不能 `return value`。
- 调用多返回值函数时，要接收匹配数量的返回值，或用 `_` 忽略。