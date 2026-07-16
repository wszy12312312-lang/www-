# 贡献指南

感谢你对 **www 多人格协作智能体** 的关注！以下是参与贡献的方式和规范。

## 如何贡献

### 报告问题

- 在 [Issues](https://github.com/wszy12312312-lang/www-/issues) 页面提交问题
- 请包含：问题描述、复现步骤、运行环境（Windows 版本、Ollama 版本、模型名称）

### 提交改进

1. Fork 本仓库
2. 创建功能分支：`git checkout -b feature/your-feature`
3. 提交修改：`git commit -m "描述你的改动"`
4. 推送到 Fork：`git push origin feature/your-feature`
5. 提交 [Pull Request](https://github.com/wszy12312312-lang/www-/pulls)

### 重点需求

当前最需要帮助的方向：

- **HOST 自主增删人格**：让 HOST 能动态创建和删除人格（当前为静态配置）
- **全自动化运行**：减少人工干预，实现系统完全自主运行
- **跨平台支持**：当前仅支持 Windows，欢迎贡献 macOS/Linux 支持
- **评分体系优化**：改进四维评分标准或激励联动机制
- **通信协议扩展**：新增消息类型或优化现有协议格式

## 开发规范

### 文件命名

- 人格定义：`skills/S{n}_名称/SKILL.md`
- 注册管理：`www_personas_registry.json`
- 记忆文件：`memory/S{n}_名称/`
- 经验条目：`EXP-{YYYYMMDD}-{NNN}`

### 通信协议

人格间交互必须遵循 11 种标准化消息类型，详见 README.md 中的"通信协议"章节。

### 确认协议

所有需要确认的操作使用 CFM 格式：`CFM-{日期}-{时间}-{序列号}`

### 记忆管理底线

- **仅检查与恢复，不删除**——这是所有记忆操作的底线原则
- 每个人格的记忆独立，互不共享

## 代码风格

- Markdown 文件使用一致的 YAML frontmatter 格式
- JSON 文件保持 2 空格缩进
- 中文注释和文档为主，技术术语保留英文原文

## 许可证

所有贡献内容将基于 MIT License 发布。
