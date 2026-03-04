# TRAE MCPs

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**TRAE MCPs** 是一个由社区维护的 [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) 服务器集合，专为 **TRAE** 编辑器打造。

通过集成 MCP 服务器，TRAE 可以突破单纯的文本交互限制，连接到本地文件系统、数据库、浏览器以及各种第三方服务，成为功能强大的全能开发助手。

> **💡 提示**：本项目主要托管 **MCP 服务器 (Tools)**。如果您正在寻找 TRAE 的 **技能 (Skills/SOPs)**，请查看 [TRAE Agent Skills](./README-skills.md)。

---

## 📖 什么是 MCP？

**Model Context Protocol (MCP)** 是由 Anthropic 推出的一个开放标准协议，旨在标准化 AI 模型与外部系统的连接方式。

如果说 AI 模型是“大脑”，那么 MCP 就是它的“感官”和“手脚”。它赋予了 AI 以下能力：
- **🔧 操作工具**：执行命令行、发送消息、管理代码仓库等。
- **📂 读取数据**：访问本地文件、查询数据库、读取文档等。
- **🌐 连接服务**：与 Slack、GitHub、Google Drive 等外部平台无缝交互。

在 TRAE 中，配置好的 MCP 服务器会作为可调用的**工具 (Tools)** 提供给智能体，智能体可根据任务需求自动选择并执行这些工具。

## 🚀 功能特性

- **开箱即用**：提供经过测试、适配 TRAE 环境的 MCP 服务器。
- **社区驱动**：汇聚社区开发者的智慧，持续扩充工具库。
- **标准统一**：遵循 MCP 标准协议，确保兼容性和稳定性。

## 📦 MCP 服务器列表

| MCP 名称 | 描述 | 状态 | 文档 |
| :--- | :--- | :--- | :--- |
| (待添加) | 更多 MCP 服务器正在开发中... | 🚧 | - |

*(目前仓库正在初始化中，欢迎提交 PR 贡献您推荐的 MCP！)*

## 🛠️ 如何使用

要在 TRAE 中使用本仓库提供的 MCP 服务器，请按照以下步骤操作：

1. **打开 TRAE 的MCP设置**
   - 打开 TRAE 。
   - 导航到 `Settings` > `MCP`。

2. **配置 MCP 的config**
   点击添加-手动添加，添加服务器配置：
   ```json
   {
     "mcpServers": {
       "your-mcp-name": {
         "command": "node",
         "args": ["/absolute/path/to/trae-mcp/mcp/your-mcp-name/build/index.js"],
         "env": {
           "API_KEY": "your-api-key"
         }
       }
     }
   }
   ```
   *(注：具体配置请参考每个 MCP 目录下的 README 说明)*

3. **在对话框中使用**
   保存配置，回到 TRAE 的对话框，使用Builder with mcp或自定义智能体。现在，您可以在对话中要求 AI 使用新添加的MCP了！

## 🤝 如何贡献

我们非常欢迎并感谢社区的贡献！如果您开发了一个新的 MCP 服务器，请按以下步骤提交：

1. 阅读 [贡献指南](./CONTRIBUTING.md)。
2. Fork 本仓库并创建一个新的分支。
3. README 中【## 📦 MCP 服务器列表】板块添加您推荐的 MCP 服务器信息。
4. 确保包含详细的 描述、状态、文档 说明。
5. 提交 Pull Request。

## 📚 更多MCP学习资源

- [Model Context Protocol 官方文档](https://modelcontextprotocol.io/)
- [Anthropic MCP 发布公告](https://www.anthropic.com/news/model-context-protocol)
- [MCP 编程极速入门指南](https://github.com/liaokongVFX/MCP-Chinese-Getting-Started-Guide)

## 📄 许可证

本项目采用 [MIT 许可证](LICENSE)。

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=trae-community/trae-mcp&type=Date)](https://www.star-history.com/#trae-community/trae-mcp&Date)

## 免责声明

本仓库中的技能为社区/学习用途提供。请在你自己的环境中审阅并充分测试后再用于生产或安全敏感场景。

## 链接

- TRAE 官网：https://www.trae.cn/
- TRAE 技能文档：https://docs.trae.ai/ide/model-context-protocol?_lang=zh