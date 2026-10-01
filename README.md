# **Awesome AI Agent Orchestrators**

_A curated list of awesome AI coding-agent orchestrators and the companion tools that make multi-agent development practical._

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

AI coding is moving from **one agent in one terminal** to **orchestrated teams of agents**. This list focuses on software that coordinates coding agents: spawning and supervising parallel sessions, isolating work, routing tasks, enabling agent-to-agent or human-to-agent coordination, reviewing changes, and integrating results.

**Orchestrator** is intentionally broad here. It includes desktop Agent Development Environments (ADEs), terminal/TUI multiplexers, task and Kanban systems, and programmable multi-agent workflow engines. A tool does not need to resemble Conductor to qualify.

> [!NOTE]
> Companion tools are kept separate so this remains an orchestrator list rather than a generic AI-tools directory.

## **Table of Contents**

1. [Desktop & GUI Orchestrators](#desktop--gui-orchestrators)
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

## **1. Desktop & GUI Orchestrators**

Visual environments for coordinating coding agents. These range from parallel-session workspaces to full ADEs with worktree isolation, task management, review, remote control, and multi-agent coordination.

### Quick Comparison

> Pricing is the **orchestrator price**, not the cost of Claude, Codex, Gemini, model APIs, cloud VMs, or other agent/provider subscriptions. **BYO** means the orchestrator uses credentials/subscriptions you provide. Pricing changes frequently; verify the linked project before purchasing.

| Orchestrator | License | Plan | Published price | Agent cost | Interface | Isolation | Remote |
| --- | --- | --- | --- | --- | --- | --- | :---: |
| [bb](https://github.com/get-bb/bb) | MIT | Free / self-hosted | $0 | BYO | Desktop / Web / CLI / API | Worktrees | Web |
| [Orca](https://github.com/stablyai/orca) | MIT | Free / self-hosted | $0 | BYO | Desktop / Mobile / CLI | Worktrees / SSH | ✅ |
| [Superset](https://github.com/superset-sh/superset) | ELv2 source-available | Free + Pro | Free; Pro $20/seat/mo | BYO | Desktop / Mobile / CLI / SDK | Worktrees | Pro |
| [Emdash](https://github.com/generalaction/emdash) | Open source | Free / self-hosted | $0 | BYO | Desktop | Isolated workspaces | — |
| [OpenChamber](https://github.com/openchamber/openchamber) | Open source | Free / self-hosted | $0 | BYO | Desktop / Web / Editor / Mobile | Worktrees | ✅ |
| [Vicoa](https://github.com/vicoa-ai/vicoa) | Open source | Free / self-hosted | $0 | BYO | Desktop / Web / Mobile | Worktrees | ✅ |
| [Tempest](https://github.com/tempestai-dev/tempest) | Open source | Free / self-hosted | $0 | BYO | Desktop | Worktrees | — |
| [Nimbalyst](https://github.com/nimbalyst/nimbalyst) | MIT | Free / self-hosted | $0 | BYO | Desktop | Worktrees | Mobile companion |
| [Parallel Code](https://github.com/johannesjo/parallel-code) | MIT | Free | $0 | BYO | Desktop | Worktrees | — |
| [intentic](https://github.com/intentic/intentic) | MIT | Free / self-hosted | $0 | BYO | Web | Docker / worktrees | Web |
| [Paseo](https://github.com/getpaseo/paseo) | Open source | Free / self-hosted | $0 | BYO | Desktop / Web / CLI | Agent workspaces | ✅ |
| [Termic](https://github.com/simion/termic) | AGPL-3.0 | Free / self-hosted | $0 | BYO | Desktop | Worktrees / sandbox | — |
| [Crystal](https://github.com/stravu/crystal) | Open source | Free / self-hosted | $0 | BYO | Desktop | Worktrees | — |
| [Vibe Kanban](https://github.com/BloopAI/vibe-kanban) | Open source | Free / self-hosted | $0 | BYO | Web / Desktop | Workspaces | Web |
| [Conductor](https://www.conductor.build/) | Proprietary | Free + Pro + Teams | Free; Pro $50/mo; Teams $60/user/mo* | BYO locally | Desktop | Worktrees / cloud sandboxes | Cloud |

\* Published pricing can change. Entries with paid plans should be checked against the vendor's current pricing page.

### Pricing Labels

- **Free** — no orchestrator subscription fee.
- **Free / self-hosted** — the software itself can be run without a paid orchestrator plan; infrastructure may still cost money.
- **Free + Pro** — usable free tier plus optional paid functionality.
- **Paid** — requires a paid orchestrator plan for normal use.
- **BYO** — bring your own coding-agent subscription, API key, or model provider; those costs are separate.
- **Custom / Enterprise** — vendor does not publish a fixed public price.

For projects without a commercial service, the list uses **$0 + BYO** rather than calling the complete AI workflow free. Running five free orchestrator sessions against five paid model subscriptions can still be expensive.

The table emphasizes orchestration mechanics rather than declaring a single tool the reference implementation.

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
- [Conductor](https://www.conductor.build/) - Proprietary desktop orchestrator for parallel coding agents in isolated workspaces with local/cloud execution, review, and automation.

- [vivy-company/aizen](https://github.com/vivy-company/aizen) - macOS workspace for organizing Git worktrees, environments, and coding-agent sessions per project.
- [mrmans0n/alas](https://github.com/mrmans0n/alas) - Native macOS agent workspace with worktree terminals, native chat panes, comment-based review, merge workflows, SSH, and phone pickup.
- [Kc1t/alethe-agents](https://github.com/Kc1t/alethe-agents) - Local-first desktop workspace with persistent real PTYs, split panes, custom grids, and support for Claude Code, Codex, and OpenCode.
- [AndyMik90/Aperant](https://github.com/AndyMik90/Aperant) - Parallel agent workspace supporting up to 12 agent terminals, self-validating QA, and conflict-aware merging.
- [clawnify/ateam](https://github.com/clawnify/ateam) - macOS and iPhone workspace for Claude Code, OpenCode, and Codex crews isolated in Git worktrees.
- [block/berd](https://github.com/block/berd) - Block's open-source desktop agent workspace built around Goose, project chats, worktrees, skills, connections, and shareable agents.
- [hardbeat920/monocode](https://github.com/hardbeat920/monocode) - Cross-platform Tauri desktop UI for running many coding-agent CLIs in parallel tabs using existing subscriptions.
- [ShreyPaharia/octomux](https://github.com/ShreyPaharia/octomux) - Local agent dashboard with a Kanban fleet view, unified permission inbox, and in-app diff review.
- [BennyKok/omg.dev](https://github.com/BennyKok/omg.dev) - Open-source parallel-agent harness for local or hosted execution with web and mobile control.
- [openchamber/openchamber](https://github.com/openchamber/openchamber) - Open-source workspace for parallel coding-agent runs across desktop, browser, editor, and mobile with per-run worktrees and review.
- [tellahq/opensession](https://github.com/tellahq/opensession) - Self-hosted server for coding sessions in worktrees or sandboxes with web UI, external task intake, diff/PR review, and multiple agent subscriptions.
- [ouijit/ouijit](https://github.com/ouijit/ouijit) - Kanban-plus-terminal workspace with lifecycle hooks, per-task worktrees, optional VM sandboxing, and support for Claude Code, Codex, Pi, and OpenCode.
- [madeinorbit/podium](https://github.com/madeinorbit/podium) - Open-source Agent Development Environment with a shared task system for coordinating coding agents from idea through implementation.
- [yicheng47/runner](https://github.com/yicheng47/runner) - Native macOS and Windows app that runs CLI agents side by side and can organize them as a lead-and-crew team.
- [supabitapp/supacode](https://github.com/supabitapp/supacode) - Native macOS command center for worktree-per-agent development.
- [tempestai-dev/tempest](https://github.com/tempestai-dev/tempest) - Tauri desktop ADE for parallel agents in isolated worktrees with shared local code knowledge, live status, and built-in diff/PR review.
- [sahithvibudhi/vibe-tree](https://github.com/sahithvibudhi/vibe-tree) - Desktop, web, and CLI environment using one Git worktree per coding agent.
- [vicoa-ai/vicoa](https://github.com/vicoa-ai/vicoa) - Desktop, web, and mobile agentic IDE with real-time sync, parallel worktrees, and broad coding-agent support.
- [egoist/waku](https://github.com/egoist/waku) - Native macOS desktop workspace for local coding-agent projects, sessions, and transcripts.
- [coder/xum](https://github.com/coder/xum) - Desktop application for isolated parallel agentic development.
- [zeronsh/zeron](https://github.com/zeronsh/zeron) - Cross-device coding-agent control plane with an always-on daemon and synchronized sessions across machines.
- [swarajbachu/zuse](https://github.com/swarajbachu/zuse) - Chat-first macOS/Linux desktop app wrapping multiple coding-agent CLIs in persistent sessions.

## **2. Terminal & TUI Orchestrators**

For developers who prefer a terminal-native workflow.

- [herdrdev/herdr](https://github.com/herdrdev/herdr) - Agent-aware terminal runtime with persistent panes, agent status, remote machines, CLI/socket APIs, and agent-to-agent orchestration.
- [smtg-ai/claude-squad](https://github.com/smtg-ai/claude-squad) - TUI for managing multiple Claude Code, Codex, OpenCode, Amp, Gemini, and other agent sessions with tmux and Git worktrees.
- [dmux](https://github.com/standardagents/dmux) - Developer-agent multiplexer pairing coding agents with Git worktrees and tmux.
- [Worktrunk](https://github.com/max-sixty/worktrunk) - CLI for fast Git worktree management; useful as the workspace layer underneath parallel coding-agent setups.
- [StructuPath/herdr-swarm](https://github.com/StructuPath/herdr-swarm) - Herdr plugin for parallel worktree-per-agent fan-out with live change visibility and review-first harvesting.
- [StructuPath/herdr-conductor](https://github.com/StructuPath/herdr-conductor) - Attended feature-delivery orchestration for task-bound producer and gate roles inside Herdr.

- [asheshgoplani/agent-deck](https://github.com/asheshgoplani/agent-deck) - TUI for live status and session resume across Claude Code, Codex, Gemini, and OpenCode.
- [YoanWai/agent-manager](https://github.com/YoanWai/agent-manager) - tmux TUI with live agent status, detached prompting, and in-terminal diff review.
- [izll/agent-session-manager](https://github.com/izll/agent-session-manager) - tmux session manager with groups, resume/fork, diff review, and mobile notifications.
- [agent-of-empires/agent-of-empires](https://github.com/agent-of-empires/agent-of-empires) - TUI plus web view for supervising the same coding-agent sessions locally or from a phone.
- [madarco/agentbox](https://github.com/madarco/agentbox) - Runs agents in isolated local or cloud VMs with fast checkpoint-based startup.
- [umputun/agterm](https://github.com/umputun/agterm) - Native macOS terminal with named agent workspaces, attention states, dashboard, and control API.
- [andyrewlee/amux](https://github.com/andyrewlee/amux) - Minimal terminal UI for spawning parallel coding agents in Git worktrees.
- [yuuichieguchi/Calyx](https://github.com/yuuichieguchi/Calyx) - Native macOS terminal with agent attention states, approval inbox, and in-terminal diff review.
- [manaflow-ai/cmux](https://github.com/manaflow-ai/cmux) - Ghostty-based macOS terminal designed for supervising many concurrent coding-agent sessions.
- [onevcat/Prowl](https://github.com/onevcat/Prowl) - Native macOS command center with vertical agent tabs, live canvas, and command palette.
- [AliHamzaAzam/repomon](https://github.com/AliHamzaAzam/repomon) - Rust TUI for supervising durable agent sessions across multiple repositories.
- [thinkany-ai/termany](https://github.com/thinkany-ai/termany) - Agent-focused terminal with worktrees, diffs, status, remote hosts, port management, and token-cost visibility.
- [Thurbeen/thurbox](https://github.com/Thurbeen/thurbox) - TUI orchestrator with SSH sessions, inter-session messaging, and native code review.
- [butterlatte-zhang/vigil](https://github.com/butterlatte-zhang/vigil) - Native macOS terminal where manager agents can spawn hierarchical worker trees while preserving each agent's native TUI.

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

Contributions are welcome. The primary list is for tools that **coordinate multiple coding agents, sessions, tasks, or execution environments**. Companion tools may supervise, isolate, review, route, provide context, or otherwise materially support those orchestrated workflows.

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
