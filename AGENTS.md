# AGENTS.md

## Purpose | 目的

- Shared source of truth for project-level collaboration rules, startup-friendly preferences, and workflow boundaries.
- 项目级共享真源：存放协作规则、启动友好的偏好摘要，以及工作边界。

## Protected Sections | 保护区块

- Content inside `<!-- BEGIN USER-SPECIFIED -->` and `<!-- END USER-SPECIFIED -->` is user-approved policy.
- Do not modify, remove, or contradict protected content without explicit user approval.
- `<!-- BEGIN USER-SPECIFIED -->` 与 `<!-- END USER-SPECIFIED -->` 包裹的内容视为用户明确指定。
- 未经用户明确同意，不要改动、删除，或与这些内容冲突。

## Shared Collaboration Rules | 共享协作规则

<!-- BEGIN USER-SPECIFIED -->
- Replace this block with the user's durable collaboration rules.
- 在这里替换成用户长期稳定的协作规则。

- Example: Before major changes, list viable options and decision dimensions before implementing.
- 示例：启动大改前，先列出可选方案和决策维度，再开始实施。

- Example: If best practice is requested, prefer mainstream industry structure over preserving legacy layout.
- 示例：如果用户要求最佳实践，优先行业主流做法，不被历史结构绑定。

- Example: Separate verified results from unverified assumptions in every final summary.
- 示例：最终总结时，已验证和未验证内容要分开写。
<!-- END USER-SPECIFIED -->

## Completion Criteria | 完成标准

<!-- BEGIN USER-SPECIFIED -->
- Define what counts as done before implementation starts.
- 在开始实施前，先定义什么算完成。

- Define what is explicitly out of scope.
- 明确什么内容不在本次范围内。
<!-- END USER-SPECIFIED -->

## Preference Summary | 偏好摘要

<!-- BEGIN USER-SPECIFIED -->
- Keep this section short enough to load comfortably at startup.
- 这一节应保持简短，方便作为启动入口被读取。

- Summarize only the most important standing preferences.
- 这里只总结最关键、最长期的偏好。
<!-- END USER-SPECIFIED -->

## Project-Specific Overrides | 项目特定覆盖

<!-- BEGIN USER-SPECIFIED -->
- Add rules that are unique to this repository and should apply across sessions.
- 在这里添加只对当前仓库生效、且应跨会话保留的规则。
<!-- END USER-SPECIFIED -->

## Related Files | 相关文件

- `MEMORY.md`: detailed durable context
- `memory/YYYY-MM-DD.md`: dated notes
- `CLAUDE.md`: Claude Code bridge
- `GEMINI.md`: Antigravity bridge

- `MEMORY.md`：详细长期上下文
- `memory/YYYY-MM-DD.md`：按日期记录
- `CLAUDE.md`：Claude Code 桥接文件
- `GEMINI.md`：Antigravity 桥接文件
