# TOMC Memory · 让猫猫帮你省 token，换 Code Agent 也能接着干

[English](README.md) · [项目源码](https://github.com/ZipengWu365/TOMC)

TOMC 在本地 CPU 上整理任务上下文，保存项目要求、决定和待办。连接同一记忆库的 Code Agent 可以接着做，任务笔记也可以导出后带到另一台电脑。可选的桌面小猫展示节省统计、上下文库和四档动画。

![TOMC 桌面小猫](https://raw.githubusercontent.com/ZipengWu365/TOMC/d2ff8f9a4166121cc6da1713d33469b305592ec1/docs/assets/workbuddy/cat-four-forms.gif)

主要有三个特点：

1. **省输入：** 本地整理任务上下文，无需额外大模型或 GPU。
2. **换 Code Agent 继续：** 保存要求、决定和待办，在连接同一记忆库的 Agent 之间接着做。
3. **换电脑接着用：** 导出任务笔记，不用重新交代背景。

## 在 TRAE 中安装

安装 [UV](https://docs.astral.sh/uv/getting-started/installation/)，先下载固定版本运行环境：

```sh
uvx --from "tomc-memory[mcp] @ https://github.com/ZipengWu365/TOMC/archive/3951794d19c9c6d22920997434aa44c54b76abf9.zip" tomc --help
```

打开 **设置 → MCP → 添加 → 手动配置**，出现运行环境选项时选择本地，粘贴 [mcp.json](mcp.json)，再为当前智能体启用 TOMC。如果 `uvx` 不在 PATH 中，将 `command` 改成其绝对路径；TRAE 要求该可执行文件路径不含空格。

TOMC 通过本地 stdio 运行，无需额外模型密钥。默认笔记库为 `~/.tomc/memory.sqlite3`，可在 server 配置中添加 `env.TOMC_MEMORY_PATH` 指定其他文件。

## 试一试

第一个任务：

> 用 TOMC remember_memory 把这些信息保存到发布计划笔记：雪松项目使用 SQLite；负责人是 Mira；截止日期为 11 月 18 日；PDF 导出尚未完成。

新开一个任务：

> 用 TOMC recall_memory 找回发布计划笔记，列出负责人、截止日期、存储方式和未完成事项，再给出下一步清单。

也可以提供一份独立的长文件，让 TOMC 为指定任务整理紧凑上下文。Agent 自己管理当前对话。

## 实验结果和桌面小猫

[项目实验结果](https://github.com/ZipengWu365/TOMC#same-reader-baseline-memory-vs-tomc-memory)包含 100K–10M 历史长度下，与 LLMLingua-2、分层 LLMLingua-2、LongLLMLingua、BRIEF-Pro、BEAM-RAG 和 LIGHT 的比较。另有[客户端实测](https://github.com/ZipengWu365/TOMC/blob/main/docs/validation.md)和[朋友的使用案例](https://github.com/ZipengWu365/TOMC/blob/main/casestudy/README.md)。

[桌面小猫](https://github.com/ZipengWu365/TOMC/blob/main/docs/desktop_companion.md)单独安装。它的四档形态随本次上下文长度变化，点击可查看节省统计和上下文库；皇冠猫还有沙漠变绿洲的动画：少一点重复输入，多一点绿色心意。

验证记录：固定版本运行环境暴露 10 个 MCP 工具，六次真实 stdio 调用验证了上下文整理、保存、进程重启后召回、用量统计和错误返回。本次投稿尚未记录 TRAE 模型自主选用工具的测试。

## 许可证

MIT。作者：Zipeng Wu。[反馈问题](https://github.com/ZipengWu365/TOMC/issues)。
