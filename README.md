# **Awesome AI Agent Orchestrators**

_A curated list of awesome tools for orchestrating AI coding agents._

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

AI coding is moving from **one agent in one terminal** to **fleets of agents working in parallel**. This list focuses on tools that help developers run, isolate, supervise, review, and merge work from Claude Code, Codex, OpenCode, Gemini CLI, Cursor, Pi, and other coding agents.

> [!NOTE]
> The closest alternatives to [Conductor](https://www.conductor.build/) are listed first. Companion tools are kept separate so this does not become a generic AI-tools directory.

## **Table of Contents**

1. [Conductor-like Orchestrators](#conductor-like-orchestrators)
2. [Terminal & TUI Orchestrators](#terminal--tui-orchestrators)
3. [Kanban & Workflow Orchestrators](#kanban--workflow-orchestrators)
4. [Companion Tools](#companion-tools)
   - [Agent Launchers & Providers](#agent-launchers--providers)
   - [Review & Diff](#review--diff)
   - [Context, Memory & Code Intelligence](#context-memory--code-intelligence)
   - [Coding Agents](#coding-agents)
5. [Related Awesome Lists](#related-awesome-lists)
6. [Contributions](#contributions)
7. [Author](#author)
8. [Support](#support)

## **1. Conductor-like Orchestrators**

These are the closest matches to Conductor's model: parallel coding-agent sessions, isolated workspaces/worktrees, supervision, and review.

- [get-bb/bb](https://github.com/get-bb/bb) - Open-source agentic IDE with desktop, web, CLI, and HTTP API surfaces. Runs agent work in steerable threads and supports managed Git worktrees.
- [stablyai/orca](https://github.com/stablyai/orca) - Open-source Agent Development Environment for running fleets of coding agents in parallel using your own subscriptions, with desktop, mobile, and remote runtime support.
- [generalaction/emdash](https://github.com/generalaction/emdash) - Open-source agentic development environment for running multiple coding agents in parallel with any model provider.
- [superset-sh/superset](https://github.com/superset-sh/superset) - Agentic IDE designed to orchestrate large numbers of coding agents in parallel using your existing subscriptions.
- [pingdotgg/t3code](https://github.com/pingdotgg/t3code) - Open-source control surface for running coding-agent sessions across web, desktop, and mobile.
- [nimbalyst/nimbalyst](https://github.com/nimbalyst/nimbalyst) - Visual workspace for Claude Code, Codex, and OpenCode with parallel worktrees, task tracking, visual editing, and mobile companions.
- [coollabsio/jean](https://github.com/coollabsio/jean) - Development environment for AI agents across projects and Git worktrees.
- [johannesjo/parallel-code](https://github.com/johannesjo/parallel-code) - Desktop app for running Claude Code, Codex, and Gemini CLI side by side in isolated Git worktrees.
- [intentic/intentic](https://github.com/intentic/intentic) - Self-hosted workspace for coding agents with persistent Docker sandboxes, Git worktrees, browser/mobile access, and review workflows.
- [getpaseo/paseo](https://github.com/getpaseo/paseo) - Self-hosted multi-agent environment controllable from desktop, mobile, web, and CLI.
- [simion/termic](https://github.com/simion/termic) - Open-source Conductor alternative that runs real agent CLIs in PTYs with parallel worktrees, multi-repo tasks, and sandboxing.
- [stravu/crystal](https://github.com/stravu/crystal) - Desktop multi-session manager for running Claude Code and Codex in parallel Git worktrees.
- [BloopAI/vibe-kanban](https://github.com/BloopAI/vibe-kanban) - Kanban-based workspace for planning, running, reviewing, and merging coding-agent work. The upstream project is sunsetting, but remains an important open-source reference.
- [Conductor](https://www.conductor.build/) - The reference product for this category: parallel coding agents in isolated workspaces, local and cloud execution, review, and automation. Proprietary; included as the baseline.

## **2. Terminal & TUI Orchestrators**

For developers who prefer a terminal-native workflow.

- [herdrdev/herdr](https://github.com/herdrdev/herdr) - Agent-aware terminal runtime with persistent panes, agent status, remote machines, CLI/socket APIs, and agent-to-agent orchestration.
- [smtg-ai/claude-squad](https://github.com/smtg-ai/claude-squad) - TUI for managing multiple Claude Code, Codex, OpenCode, Amp, Gemini, and other agent sessions with tmux and Git worktrees.
- [dmux](https://github.com/standardagents/dmux) - Developer-agent multiplexer pairing coding agents with Git worktrees and tmux.
- [Worktrunk](https://github.com/max-sixty/worktrunk) - CLI for fast Git worktree management; useful as the workspace layer underneath parallel coding-agent setups.
- [StructuPath/herdr-swarm](https://github.com/StructuPath/herdr-swarm) - Herdr plugin for parallel worktree-per-agent fan-out with live change visibility and review-first harvesting.
- [StructuPath/herdr-conductor](https://github.com/StructuPath/herdr-conductor) - Attended feature-delivery orchestration for task-bound producer and gate roles inside Herdr.

## **3. Kanban & Workflow Orchestrators**

Tools that organize agent work around tasks, boards, or structured execution rather than only terminals.

- [BloopAI/vibe-kanban](https://github.com/BloopAI/vibe-kanban) - Kanban planning plus isolated agent workspaces, diff review, previews, PR creation, and merge.
- [automaker](https://github.com/AutoMaker-Org/automaker) - Feature-oriented agent workflow with Kanban-style planning and isolated worktrees.
- [agent-kanban](https://github.com/eyaltoledano/agent-kanban) - Leader/worker task-board approach to coordinating coding agents.
- [bb Orchestra](https://github.com/dbrekelmans/bb-orchestra) - Plugin that turns a bb thread into a live orchestrator which delegates work to subagents with independent providers, models, reasoning levels, and worktrees.
- [bbonductor](https://github.com/gmemmanuel/bbonductor) - Conductor-style workspace and issue-to-merge workflow plugin for bb.

## **4. Companion Tools**

These are not necessarily Conductor replacements. They make a parallel-agent setup substantially better and are included because they complement the orchestrators above.

This section is seeded from the tools used in [jellydn/my-ai-tools](https://github.com/jellydn/my-ai-tools).

### Agent Launchers & Providers

- [Delta](https://delta.dev/) - Collaborative agent workspace from the `my-ai-tools` stack for isolated checkouts, agent threads, review, and syncing changes back to a repository.
- [nkzw-tech/codiff](https://github.com/nkzw-tech/codiff) - Agent-aware code review/diff tool used in `my-ai-tools`, with configurable agent backends and review-comment workflows.
- [ctx](https://ctx.rs/) - Open-source local index and search layer for past coding-agent sessions, with SQLite-backed history and MCP access.
- [jellydn/ai-launcher](https://github.com/jellydn/ai-launcher) - Fast cross-platform launcher for switching among AI coding CLIs with fuzzy search, aliases, templates, and automatic detection.
- [Ike-li/ccs](https://github.com/Ike-li/ccs) - Claude Code provider switcher for Anthropic-compatible providers.
- [vercel-labs/fx](https://github.com/vercel-labs/fx) - Tiny, open, embeddable native coding agent with ACP, MCP, skills, and subagents.

### Review & Diff

- [modem-dev/hunk](https://github.com/modem-dev/hunk) - Review-first terminal diff viewer designed for agent-authored changes, including live sessions and inline agent annotations.
- [spencermarx/open-code-review](https://github.com/spencermarx/open-code-review) - Multi-agent code-review system with customizable reviewer teams and reviewer discourse.
- [qiankunli/open-codereview](https://github.com/qiankunli/open-codereview) - Open-source AI code-review CLI combining deterministic analysis and LLM-agent review with line-level comments.
- [dandavison/delta](https://github.com/dandavison/delta) - Syntax-highlighting pager for Git, diff, grep, and blame output; useful for agent-heavy terminal workflows.
- [Wilfred/difftastic](https://github.com/Wilfred/difftastic) - Structural diff tool that compares syntax rather than only lines.

### Context, Memory & Code Intelligence

- [tobi/qmd](https://github.com/tobi/qmd) - Local-first Markdown search and retrieval that can serve project knowledge to agents.
- [modelcontextprotocol/servers](https://github.com/modelcontextprotocol/servers) - Reference MCP servers and examples for extending agent tool access.
- [upstash/context7](https://github.com/upstash/context7) - Up-to-date library documentation/context for coding agents through MCP.
- [jellydn/my-ai-tools](https://github.com/jellydn/my-ai-tools) - Portable, source-controlled configuration for coding agents, skills, hooks, MCP servers, and companion tools.

### Coding Agents

Orchestrators need agents to run. Common open-source or CLI-based companions include:

- [anthropics/claude-code](https://github.com/anthropics/claude-code) - Claude Code.
- [openai/codex](https://github.com/openai/codex) - OpenAI Codex CLI.
- [sst/opencode](https://github.com/sst/opencode) - Open-source coding agent.
- [google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli) - Gemini CLI.
- [paul-gauthier/aider](https://github.com/Aider-AI/aider) - AI pair-programming CLI.
- [block/goose](https://github.com/block/goose) - Extensible open-source AI agent from Block.
- [badlogic/pi-mono](https://github.com/badlogic/pi-mono) - Pi coding-agent ecosystem.

## **5. Related Awesome Lists**

- [andyrewlee/awesome-agent-orchestrators](https://github.com/andyrewlee/awesome-agent-orchestrators) - Broad directory covering terminal, desktop/web, swarm, autonomous, and infrastructure orchestrators.
- [jellydn/my-ai-tools](https://github.com/jellydn/my-ai-tools) - Dung's working AI coding-tool stack and configurations.
- [jellydn/awesome-typesafe](https://github.com/jellydn/awesome-typesafe) - Formatting and curation inspiration for this repository.

## **6. Contributions**

Contributions are welcome. Please keep additions focused on tools that **orchestrate, supervise, isolate, review, route, or materially support coding-agent workflows**.

Before submitting a project:

1. Prefer an open-source repository or clearly identify source-available/proprietary software.
2. Link to the canonical upstream repository.
3. Use one short factual sentence; avoid marketing copy.
4. Put the project in the narrowest relevant section.
5. Do not add generic chatbots or model APIs unless they provide a concrete companion capability for agent orchestration.

See [CONTRIBUTING.md](CONTRIBUTING.md).

## **7. Author**

**Dung Huynh**

- Website: [productsway.com](https://productsway.com/)
- YouTube: [IT Man Channel](https://www.youtube.com/@it-man)
- X: [@jellydn](https://twitter.com/jellydn)
- GitHub: [@jellydn](https://github.com/jellydn)

## **8. Support**

Give this project a ⭐️ if it helps you discover a better way to run coding agents.

[![Ko-fi](https://img.shields.io/badge/Ko--fi-Support-ff5e5b?logo=ko-fi&logoColor=white)](https://ko-fi.com/dunghd)
[![PayPal](https://img.shields.io/badge/PayPal-Support-00457C?logo=paypal&logoColor=white)](https://paypal.me/dunghd)
[![Buy Me a Coffee](https://img.shields.io/badge/Buy_Me_a_Coffee-Support-FFDD00?logo=buymeacoffee&logoColor=000000)](https://www.buymeacoffee.com/dunghd)
