# Go Learning Roadmap

> 面向有 Python 开发经验的 Go 学习路线：从语法基础逐步走到并发、Web、数据库、工程化和完整项目。

## 学习方式

这个仓库采用 **Learn → Practice → Review → Project**。

每个阶段都按下面顺序：

1. 先进入该阶段的 `knowledge/` 目录学习知识点
2. 看 Go 语法、Python 对照、常见坑和最小示例
3. 再开始对应 Issue
4. 完成后做 Code Review、边界测试和复杂度分析
5. 阶段结束后进入阶段项目

原则：**Issue 不应该是第一次看到一个概念的地方。**

如果 Issue 中出现了 `knowledge/` 没解释过的概念，先补知识文档，再继续做题。

## 目录结构

```text
01-go-basics/
  README.md
  knowledge/
    README.md
    01-xxx.md
    02-xxx.md

02-go-core/
  README.md
  knowledge/
...
```

Stage README 只负责：
- 阶段目标
- 学习顺序
- Issue / 项目
- 验收标准

`knowledge/` 负责：
- 概念是什么
- 为什么需要
- Go 如何使用
- Python 对应方法/心智模型
- 常见坑
- 最小示例

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

开始位置：**01-go-basics/knowledge/README.md**。
