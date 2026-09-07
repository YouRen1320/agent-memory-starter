# Agent Memory Starter

中文 | English

一个面向 `Codex`、`Claude Code`、`Antigravity` 的开源模板，用来统一项目级规则、长期记忆和每日记录，并让不同工具尽量通过原生入口自动加载。

An open-source starter for `Codex`, `Claude Code`, and `Antigravity` that organizes project rules, durable memory, and daily logs while keeping native startup entrypoints for each tool.

## 与 Agent Project Kit 的区别

- 本仓库是轻量的“规则与记忆”起步模板，适合只想统一 `AGENTS.md`、工具桥接文件和每日记录的项目。
- [agent-project-kit](https://github.com/YouRen1320/agent-project-kit) 是更完整的项目治理模板，包含需求、架构、测试、发布、安全与交接资料，以及对应的自动验证。
- 两者不需要同时安装：只需要记忆骨架时选本仓库；希望建立完整工程协作基线时选 `agent-project-kit`。

## Why This Exists

### 中文

- 把共享规则集中在项目根 `AGENTS.md`
- 用 `CLAUDE.md`、`GEMINI.md` 做薄桥接，避免多份重复规则
- 把长期记忆和每日记录分层，避免启动入口越来越臃肿
- 给“用户明确指定、未经允许不要改”的内容留保护区块

### English

- Keep shared rules in the project-root `AGENTS.md`
- Use thin bridge files such as `CLAUDE.md` and `GEMINI.md` instead of duplicating rules
- Separate durable memory from daily logs so startup files stay lean
- Protect explicit user policy with sections that should not be edited without approval

## Supported Tools

### 中文

- `Codex`: 原生读取 `AGENTS.md`
- `Claude Code`: 通过 `CLAUDE.md` 薄桥接到 `AGENTS.md` 与 `MEMORY.md`
- `Antigravity`: 通过 `GEMINI.md` 加载工具专属补充，同时把共享规则留在 `AGENTS.md`

### English

- `Codex`: reads `AGENTS.md` natively
- `Claude Code`: uses `CLAUDE.md` as a thin bridge into `AGENTS.md` and `MEMORY.md`
- `Antigravity`: uses `GEMINI.md` for tool-specific additions while keeping shared rules in `AGENTS.md`

## Repository Layout

```text
agent-memory-starter/
├── README.md
├── AGENTS.md
├── CLAUDE.md
├── GEMINI.md
├── MEMORY.md
├── memory/
│   └── DATE_TEMPLATE.md
├── docs/
│   └── adoption-checklist.md
└── examples/
    ├── global/
    │   ├── .codex/
    │   │   └── AGENTS.md
    │   └── .claude/
    │       └── CLAUDE.md
    └── private-project-gitignore.txt
```

## Design Principles

### 中文

1. `AGENTS.md` 是共享宪法，不是流水账。
2. `MEMORY.md` 放长期有效的项目事实、偏好、约束，不承担所有启动上下文。
3. `memory/` 里放日期日志，定期提炼回 `MEMORY.md`。
4. `CLAUDE.md`、`GEMINI.md` 只放桥接和工具专属内容，不复制整套规则。
5. 对“必须得到用户确认”的规则，用保护区块包裹。

### English

1. `AGENTS.md` is the shared constitution, not a running diary.
2. `MEMORY.md` stores durable facts, preferences, and constraints without becoming a bloated startup file.
3. `memory/` stores dated notes that can later be distilled into `MEMORY.md`.
4. `CLAUDE.md` and `GEMINI.md` stay thin and tool-specific instead of duplicating the full rule set.
5. Wrap policy that must not be changed casually in protected blocks.

## Quick Start

### 中文

1. 复制这个目录作为你的新项目模板。
2. 在项目根修改 `AGENTS.md` 中的共享规则与偏好摘要。
3. 在 `MEMORY.md` 填入项目的长期事实、架构约束、已确认决策。
4. 用 `memory/DATE_TEMPLATE.md` 新建每日记录。
5. 如果你还想配全局层，参考 `examples/global/`。

### English

1. Copy this directory as the starting point for your project.
2. Edit the shared rules and preference summary in `AGENTS.md`.
3. Add durable project facts, architecture constraints, and confirmed decisions to `MEMORY.md`.
4. Use `memory/DATE_TEMPLATE.md` to create dated daily notes.
5. If you also want global files, use `examples/global/` as a reference.

## Recommended Workflow

### 中文

1. 把项目通用规则写进 `AGENTS.md`
2. 把项目长期记忆写进 `MEMORY.md`
3. 每次会话把过程性内容写到 `memory/YYYY-MM-DD.md`
4. 定期把稳定结论从每日记录提炼回 `MEMORY.md`
5. 避免把每日细节直接塞进 `AGENTS.md`

### English

1. Put project-wide rules in `AGENTS.md`
2. Put durable project memory in `MEMORY.md`
3. Store session details in `memory/YYYY-MM-DD.md`
4. Regularly promote stable conclusions from daily logs into `MEMORY.md`
5. Avoid stuffing daily details directly into `AGENTS.md`

## Optional Private Mode

### 中文

如果你不想把这些文件提交到仓库，可以参考 `examples/private-project-gitignore.txt` 里的忽略规则。

### English

If you do not want to commit these files, use the ignore snippet in `examples/private-project-gitignore.txt`.

## Publishing Notes

### 中文

- 开源前请自行选择许可证，本模板故意不预设 `LICENSE`
- 如果你要面向更多工具，可以在此结构上继续加桥接文件
- 如果某个工具的全局配置路径不确定，不要在文档里编造路径

### English

- Choose your own license before publishing; this starter intentionally does not assume one
- If you support more tools later, add bridge files on top of this structure
- If a tool's global config path is uncertain, document that uncertainty instead of inventing paths

## Non-Goals

### 中文

- 不试图把所有工具的所有私有机制抽象成一种格式
- 不把 `MEMORY.md` 当作所有工具都会原生启动加载的唯一入口
- 不预设你必须把这些文件提交到 Git

### English

- It does not attempt to abstract every private memory mechanism into one universal format
- It does not assume `MEMORY.md` is the single native startup entrypoint for every tool
- It does not force you to commit these files to Git
