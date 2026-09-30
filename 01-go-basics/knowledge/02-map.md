# Map 与 Set 思维

## 是什么

Map 是键值映射：

```go
m := make(map[string]int)
m["alice"] = 1
```

读取不存在的 key 会返回 value 类型的零值。

## 判断 key 是否存在

```go
v, ok := m[key]
if ok {
    _ = v
}
```

Python 对照：

```python
if key in d:
    ...
```

Go：

```go
if _, ok := m[key]; ok {
    ...
}
```

## 计数器

```go
count := map[int]int{}
count[x]++
```

因为不存在的 int value 默认是 0。

## 模拟 Set

直观版：

```go
seen := map[int]bool{}
```

Go 常见版：

```go
seen := map[int]struct{}{}
seen[x] = struct{}{}
```

`struct{}` 不承载业务数据，适合表达“只关心存在”。

## 注意

- 不要依赖 map 遍历顺序。
- 需要稳定顺序时，用 slice 保存顺序、map 负责查重。