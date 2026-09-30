# 指针与 Slice 语义

## 指针

```go
x := 10
p := &x
*p = 20
```

`&x` 获取地址，`*p` 解引用。

Python 通常不让你显式操作这种指针语法。

## Go 是值传递

包括 slice 也是值传递，只是 slice header 内部保存了底层数组地址。

因此：

```go
func reverse(nums []int) {
    nums[0] = 99
}
```

调用后，调用方通常能看到底层数组被修改。

## 为什么很多 slice 操作不需要 *[]int

直接修改元素时：

```go
nums[i] = x
```

通常不需要传 `*[]int`。

但如果函数要让调用方拿到 append 后可能变化的 slice header，则应返回新 slice，或传 slice 指针（后者较少作为第一选择）。

## 注意

先理解值语义，再决定是否用指针；不要为了“像 C”而过度使用指针。