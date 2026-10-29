# TOMC Memory · A token-saving cat, with memory across code agents

[简体中文](README.zh-CN.md) · [Source](https://github.com/ZipengWu365/TOMC)

TOMC prepares compact context for a task on your CPU and saves reusable project notes. Switch between code agents connected to the same notebook database, or export notes and continue on another computer. The optional desktop cat shows context savings, saved contexts, and four animation forms.

![TOMC desktop cat](https://raw.githubusercontent.com/ZipengWu365/TOMC/d2ff8f9a4166121cc6da1713d33469b305592ec1/docs/assets/workbuddy/cat-four-forms.gif)

Three practical features:

1. **Reduce input:** prepare task context locally, without another LLM or GPU.
2. **Switch code agents:** carry requirements, decisions, and unfinished work between agents using the same notebook database.
3. **Switch computers:** export notes and continue without explaining the project again.

## Install in TRAE

Install [UV](https://docs.astral.sh/uv/getting-started/installation/), then prefetch the pinned runtime:

```sh
uvx --from "tomc-memory[mcp] @ https://github.com/ZipengWu365/TOMC/archive/3951794d19c9c6d22920997434aa44c54b76abf9.zip" tomc --help
```

Open **Settings → MCP → Add → Manual**, choose the local runtime if prompted, and paste [mcp.json](mcp.json). If `uvx` is not on PATH, use its absolute executable path in `command`. TRAE requires that executable path to contain no spaces. Enable the server for your agent.

TOMC uses a local stdio process and needs no extra model key. The notebook database defaults to `~/.tomc/memory.sqlite3`. Add `env.TOMC_MEMORY_PATH` to the server entry to choose a different file.

## Try it

First task:

> Use TOMC remember_memory to save this in release-plan: Project Cedar uses SQLite; Mira owns the release; the deadline is November 18; PDF export remains unfinished.

New task:

> Use TOMC recall_memory to recall release-plan. List the owner, deadline, storage choice, and unfinished work. Then write a short next-step checklist.

You can also ask TOMC to prepare a compact context from a separately supplied long file for a specific task. The agent keeps managing its own active conversation.

## Results and desktop cat

The [project results](https://github.com/ZipengWu365/TOMC#same-reader-baseline-memory-vs-tomc-memory) compare TOMC with LLMLingua-2, hierarchical LLMLingua-2, LongLLMLingua, BRIEF-Pro, BEAM-RAG, and LIGHT at 100K–10M history lengths. [Client test records](https://github.com/ZipengWu365/TOMC/blob/main/docs/validation.md) and [community cases](https://github.com/ZipengWu365/TOMC/blob/main/casestudy/README.md) are available separately.

Install the [desktop cat](https://github.com/ZipengWu365/TOMC/blob/main/docs/desktop_companion.md) separately. Its forms follow the current context length; clicking it shows savings and the context library. The crowned cat also has an oasis animation: less repeated input, a little more care for our planet.

Validation: the pinned runtime exposes 10 MCP tools. Six real stdio calls verified preparation, saving, recall after a server restart, usage statistics, and readable errors. TRAE model-selected calls are not yet recorded in this submission.

## License

MIT. Author: Zipeng Wu. [Report an issue](https://github.com/ZipengWu365/TOMC/issues).
