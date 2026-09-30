# 项目结构与工程注意点

Go 没有唯一官方目录模板，先按职责拆分，避免过早复杂化。

常见：

```text
cmd/
internal/
migrations/
config/
```

原则：
- package 名表达职责
- 避免循环依赖
- interface 靠近使用方
- 不建立无业务价值的层层转发
