# Go Learning Roadmap

> 面向有 Python 开发经验的 Go 学习路线：从语法基础逐步走到并发、Web、数据库、工程化和完整项目。

## 学习方式

这个仓库不是单纯的教程，而是一套 **Learn → Practice → Review → Project** 的训练计划。

建议每天 1～2 小时：

1. 20 分钟学习一个知识点
2. 40 分钟完成对应练习
3. 30～60 分钟推进阶段项目
4. 10 分钟复盘错误和 Go / Python 思维差异

原则：**先自己写，再看提示；先标准库，再框架；每个知识点必须通过代码验证。**

## 8 个阶段

| 阶段 | 主题 | 目标 |
|---|---|---|
| 01 | Go 基础强化 | 熟练 slice、map、string、函数、指针基础 |
| 02 | Go 核心抽象 | 掌握 struct、method、interface、error |
| 03 | 工程基础 | 掌握 package、module、文件、JSON、测试 |
| 04 | 并发编程 | 掌握 goroutine、channel、select、mutex、context |
| 05 | Web 开发 | 使用 net/http 与 Gin 构建 REST API |
| 06 | 数据库 | 使用 PostgreSQL/MySQL、事务、连接池、Repository |
| 07 | 工程化 | 测试、日志、配置、Docker、Graceful Shutdown |
| 08 | 综合项目 | 完成可部署的 Go 任务管理系统 |

## 目录

```text
01-go-basics/
02-go-core/
03-engineering-basics/
04-concurrency/
05-web-development/
06-database/
07-engineering/
08-final-project/
```

每个目录都有自己的 README，说明：

- 学习目标
- 核心知识点
- 练习顺序
- 阶段项目
- 验收标准

## Issue 使用方式

仓库中的练习会拆成独立 Issue。建议：

- 一次只处理 1～2 个 Issue
- 完成后提交代码并关闭对应 Issue
- 如果卡住，先记录你尝试过什么，再查资料
- 每完成一个阶段，再进入下一阶段

## Python 开发者重点转换

| Python | Go |
|---|---|
| class | struct + method |
| exception | error |
| list | slice |
| dict | map |
| duck typing | interface |
| thread / asyncio | goroutine |
| queue | channel |
| try/finally | defer |

重点不是把 Python 写法翻译成 Go，而是逐步理解 Go 的显式错误处理、接口组合、值/指针语义和并发模型。

## 最终目标

完成本仓库后，你应该能够：

- 独立编写中小型 Go 程序
- 理解并正确使用 goroutine / channel / context
- 构建 REST API
- 使用数据库和事务
- 编写可测试、可维护的 Go 工程
- 使用 Docker 部署完整后端服务
- 阅读并参与常见 Go 项目

开始位置：**01-go-basics**。
