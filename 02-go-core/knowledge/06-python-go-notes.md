# Python → Go 抽象差异

```text
Python class        -> Go struct + method
duck typing         -> interface
exception           -> error return
inheritance         -> composition / embedding
try/finally         -> defer
None                -> nil（仅部分类型）
```

重点：不要把 Python OOP 逐句翻译成 Go。Go 更偏向小接口、组合、显式错误和值/指针语义。