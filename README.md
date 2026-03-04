# TRAE MCPs

[![License: MIT](https://img.shields.io/badge/License-MIT-brightgreen.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

[中文](./README.zh-CN.md)

**TRAE MCPs** is a community-maintained collection of [Model Context Protocol (MCP)](https://modelcontextprotocol.io/) servers designed for the **TRAE** editor.

By integrating MCP servers, TRAE can break through the limitations of pure text interaction, connecting to local file systems, databases, browsers, and various third-party services, becoming a powerful all-around development assistant.

> **💡 Note**: This project primarily hosts **MCP Servers (Tools)**. If you are looking for **Skills (SOPs)** for TRAE, please check out [TRAE Agent Skills](./README-skills.md).

---

## 📖 What is MCP?

**Model Context Protocol (MCP)** is an open standard protocol introduced by Anthropic, designed to standardize how AI models connect with external systems.

If the AI model is the "brain", then MCP is its "senses" and "limbs". It empowers AI with the following capabilities:
- **🔧 Operate Tools**: Execute command lines, send messages, manage code repositories, etc.
- **📂 Read Data**: Access local files, query databases, read documents, etc.
- **🌐 Connect Services**: Seamlessly interact with external platforms like Slack, GitHub, Google Drive, etc.

In TRAE, configured MCP servers serve as callable **Tools** for the agent. The agent can automatically select and execute these tools based on task requirements.

## 🚀 Features

- **Out of the Box**: Provides MCP servers that are tested and adapted for the TRAE environment.
- **Community Driven**: Gathers wisdom from community developers to continuously expand the tool library.
- **Unified Standard**: Follows the MCP standard protocol to ensure compatibility and stability.

## 📦 MCP Server List

| MCP Name | Description | Status | Documentation |
| :--- | :--- | :--- | :--- |
| (To be added) | More MCP servers are under development... | 🚧 | - |

*(The repository is currently initializing. PRs to contribute your recommended MCPs are welcome!)*

## 🛠️ How to Use

To use the MCP servers provided in this repository in TRAE, please follow these steps:

1. **Open TRAE MCP Settings**
   - Open TRAE.
   - Navigate to `Settings` > `MCP`.

2. **Configure MCP Config**
   Click Add - Manually Add, and add the server configuration:
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
   *(Note: Please refer to the README in each MCP directory for specific configurations)*

3. **Use in Chat**
   Save the configuration and return to the TRAE chat interface. Use Builder with MCP or a custom agent. Now, you can ask the AI to use the newly added MCP in the conversation!

## 🤝 How to Contribute

We welcome and appreciate community contributions! If you have developed a new MCP server, please follow these steps to submit:

1. Read the [Contribution Guidelines](./CONTRIBUTING.md).
2. Fork this repository and create a new branch.
3. Add your recommended MCP server information to the **MCP Server List** section in `README.md`.
4. Ensure a detailed Description, Status, and Documentation are included.
5. Submit a Pull Request.

## 📚 More MCP Learning Resources

- [Model Context Protocol Official Documentation](https://modelcontextprotocol.io/)
- [Anthropic MCP Announcement](https://www.anthropic.com/news/model-context-protocol)
- [MCP Programming Quick Start Guide](https://github.com/liaokongVFX/MCP-Chinese-Getting-Started-Guide) (Chinese)

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## Star History

[![Star History Chart](https://api.star-history.com/svg?repos=trae-community/trae-mcp&type=Date)](https://www.star-history.com/#trae-community/trae-mcp&Date)

## Disclaimer

The skills in this repository are provided for community/learning purposes. Please review and fully test them in your own environment before using them in production or security-sensitive scenarios.

## Links

- TRAE Official Website: https://www.trae.ai/
- TRAE Skills Documentation: https://docs.trae.ai/ide/model-context-protocol
