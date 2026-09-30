# Slice 与 Array

## 是什么

Array 是固定长度数组，长度属于类型的一部分；Slice 是对底层数组的一段视图，是 Go 中更常用的序列类型。

```go
var a [3]int
s := []int{1, 2, 3}
```

## Python 对照

Python `list` 更接近 Go 的 `slice`，但 Go slice 有明确元素类型，并包含 pointer / len / cap 三个核心概念。

## 常用操作

```go
len(s)
cap(s)
s[i]
s = append(s, 4)
copy(dst, src)
```

`append` 必须接住返回值，因为扩容后可能指向新的底层数组：

```go
s = append(s, value)
```

## 注意

- slice 传参时 header 是值传递，但通常仍指向同一底层数组。
- 修改 `s[i]` 往往会影响调用方看到的数据。
- `append` 可能扩容，因此不能假设 append 前后底层数组一定相同。
- 空 slice 可以是 `var s []int`、`[]int{}`、`make([]int, 0)`。