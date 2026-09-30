# Docker / Makefile / CI

Docker 用于可重复构建与运行环境。Go 常用 multi-stage build 减小镜像。

Makefile/Taskfile 可统一：
- test
- lint
- run
- build
- migrate

CI 至少执行：格式/静态检查、测试、构建。