# Module / Package / Import

初始化项目：

```bash
go mod init example.com/project
```

`go.mod` 管依赖与 module path。

一个目录通常对应一个 package；导出的标识符首字母大写。

Python 对照：
- module/package 的组织思想相近
- Go import path 与 module path 强绑定
- Go 不允许未使用 import

常用：

```bash
go mod tidy
go list ./...
go test ./...
```
