# Interface 与组合

## Interface
Go interface 描述“需要哪些方法”，实现是隐式的：

```go
type Storage interface {
    Save(Student) error
    Find(id int) (Student, error)
}
```

类型只要实现这些方法，就满足接口，不需要 `implements`。

Python 对照：接近 duck typing / Protocol，但 Go 在编译期检查方法集合。

## Embedding
Go 常用嵌入实现组合：

```go
type Service struct {
    Storage
}
```

注意：优先定义小接口，让接口靠近使用方，而不是为了抽象而抽象。
