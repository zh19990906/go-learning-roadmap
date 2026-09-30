# Value Receiver 与 Pointer Receiver

```go
func (s Student) Name() string
func (s *Student) SetName(name string)
```

值接收者拿到副本；指针接收者可修改原对象，并避免复制较大 struct。

Python 对象方法默认操作对象引用；Go 需要你显式选择值语义还是指针语义。

经验：
- 方法需要修改 receiver：用指针。
- 大 struct：通常倾向指针。
- 小且不可变语义：值接收者很自然。
- 同一个类型的方法集合尽量保持一致风格。
