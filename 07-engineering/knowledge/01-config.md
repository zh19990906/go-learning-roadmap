# 配置管理

配置常来自环境变量、配置文件、命令行参数。

原则：
- 不把密码/token 写死进仓库
- 启动时校验必要配置
- 配置结构化到 struct
- 区分开发/测试/生产

Python 对照：settings / dotenv / pydantic-settings 等职责。