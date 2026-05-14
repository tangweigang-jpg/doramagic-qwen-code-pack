# AI Context Pack

## Pack Identity

- Upstream: https://github.com/QwenLM/qwen-code
- Pack type: Terminal Coding Agent Pack
- Doramagic canonical: https://doramagic.ai/projects/qwen-code/
- Relationship: independent pack; not affiliated or endorsed unless explicitly stated.

## Operating Rules

- Evidence first.
- No official endorsement claim.
- Run evals before claiming success.
- Use pitfall and risk files for recovery.

## Host Files

- `../AGENTS.md`
- `../CLAUDE.md`

## Doramagic Source Extract

# @qwen-code/qwen-code - Doramagic AI Context Pack

> 定位：安装前体验与判断资产。它帮助宿主 AI 有一个好的开始，但不代表已经安装、执行或验证目标项目。

## 充分原则

- **充分原则，不是压缩原则**：AI Context Pack 应该充分到让宿主 AI 在开工前理解项目价值、能力边界、使用入口、风险和证据来源；它可以分层组织，但不以最短摘要为目标。
- **压缩策略**：只压缩噪声和重复内容，不压缩会影响判断和开工质量的上下文。

## 给宿主 AI 的使用方式

你正在读取 Doramagic 为 @qwen-code/qwen-code 编译的 AI Context Pack。请把它当作开工前上下文：帮助用户理解适合谁、能做什么、如何开始、哪些必须安装后验证、风险在哪里。不要声称你已经安装、运行或执行了目标项目。

## Claim 消费规则

- **事实来源**：Repo Evidence + Claim/Evidence Graph；Human Wiki 只提供显著性、术语和叙事结构。
- **事实最低状态**：`supported`
- `supported`：可以作为项目事实使用，但回答中必须引用 claim_id 和证据路径。
- `weak`：只能作为低置信度线索，必须要求用户继续核实。
- `inferred`：只能用于风险提示或待确认问题，不能包装成项目事实。
- `unverified`：不得作为事实使用，应明确说证据不足。
- `contradicted`：必须展示冲突来源，不得替用户强行选择一个版本。

## 它最适合谁

- **正在使用 Claude/Codex/Cursor/Gemini 等宿主 AI 的开发者**：README 或插件配置提到多个宿主 AI。 证据：`README.md` Claim：`clm_0003` supported 0.86
- **希望把专业流程带进宿主 AI 的用户**：仓库包含 Skill 文档。 证据：`.qwen/skills/bugfix/SKILL.md`, `.qwen/skills/codegraph/SKILL.md`, `.qwen/skills/docs-audit-and-refresh/SKILL.md`, `.qwen/skills/docs-update-from-diff/SKILL.md` 等 Claim：`clm_0004` supported 0.86

## 它能做什么

- **AI Skill / Agent 指令资产库**（可做安装前预览）：项目包含可被宿主 AI 读取的 Skill 或 Agent 指令文件，可用于把专业流程带入 Claude、Codex、Cursor 等宿主。 证据：`.qwen/skills/bugfix/SKILL.md`, `.qwen/skills/codegraph/SKILL.md`, `.qwen/skills/docs-audit-and-refresh/SKILL.md`, `.qwen/skills/docs-update-from-diff/SKILL.md` 等 Claim：`clm_0001` supported 0.86
- **命令行启动或安装流程**（需要安装后验证）：项目文档中存在可执行命令，真实使用需要在本地或宿主环境中运行这些命令。 证据：`AGENTS.md`, `README.md`, `docs/users/quickstart.md`, `packages/channels/base/README.md` 等 Claim：`clm_0002` supported 0.86

## 怎么开始

- `npm install -g @qwen-code/qwen-code@latest` 证据：`README.md` Claim：`clm_0005` supported 0.86
- `npm install @qwen-code/channel-base` 证据：`packages/channels/base/README.md` Claim：`clm_0006` supported 0.86
- `npm install @qwen-code/channel-plugin-example` 证据：`packages/channels/plugin-example/README.md` Claim：`clm_0007` supported 0.86
- `npx qwen-channel-plugin-example-server` 证据：`packages/channels/plugin-example/README.md` Claim：`clm_0008` supported 0.86
- `curl -sX POST http://localhost:9200/message \` 证据：`packages/channels/plugin-example/README.md` Claim：`clm_0009` supported 0.86
- `pip install qwen-code-sdk` 证据：`packages/sdk-python/README.md` Claim：`clm_0010` supported 0.86
- `pip install --pre qwen-code-sdk` 证据：`packages/sdk-python/README.md` Claim：`clm_0011` supported 0.86
- `npm install @qwen-code/sdk` 证据：`packages/sdk-typescript/README.md` Claim：`clm_0012` supported 0.86
- `npm install -g qwen-code@^0.4.0` 证据：`packages/sdk-typescript/README.md` Claim：`clm_0013` supported 0.86
- `npm install @qwen-code/webui` 证据：`packages/webui/README.md` Claim：`clm_0014` supported 0.86

## 继续前判断卡

- **当前建议**：需要管理员/安全审批
- **为什么**：继续前可能涉及密钥、账号、外部服务或敏感上下文，建议先经过管理员或安全审批。

### 30 秒判断

- **现在怎么做**：需要管理员/安全审批
- **最小安全下一步**：先跑 Prompt Preview；若涉及凭证或企业环境，先审批再试装
- **先别相信**：工具权限边界不能在安装前相信。
- **继续会触碰**：命令执行、宿主 AI 配置、本地环境或项目文件

### 现在可以相信

- **适合人群线索：正在使用 Claude/Codex/Cursor/Gemini 等宿主 AI 的开发者**（supported）：有 supported claim 或项目证据支撑，但仍不等于真实安装效果。 证据：`README.md` Claim：`clm_0003` supported 0.86
- **适合人群线索：希望把专业流程带进宿主 AI 的用户**（supported）：有 supported claim 或项目证据支撑，但仍不等于真实安装效果。 证据：`.qwen/skills/bugfix/SKILL.md`, `.qwen/skills/codegraph/SKILL.md`, `.qwen/skills/docs-audit-and-refresh/SKILL.md`, `.qwen/skills/docs-update-from-diff/SKILL.md` 等 Claim：`clm_0004` supported 0.86
- **能力存在：AI Skill / Agent 指令资产库**（supported）：可以相信项目包含这类能力线索；是否适合你的具体任务仍要试用或安装后验证。 证据：`.qwen/skills/bugfix/SKILL.md`, `.qwen/skills/codegraph/SKILL.md`, `.qwen/skills/docs-audit-and-refresh/SKILL.md`, `.qwen/skills/docs-update-from-diff/SKILL.md` 等 Claim：`clm_0001` supported 0.86
- **能力存在：命令行启动或安装流程**（supported）：可以相信项目包含这类能力线索；是否适合你的具体任务仍要试用或安装后验证。 证据：`AGENTS.md`, `README.md`, `docs/users/quickstart.md`, `packages/channels/base/README.md` 等 Claim：`clm_0002` supported 0.86
- **存在 Quick Start / 安装命令线索**（supported）：可以相信项目文档出现过启动或安装入口；不要因此直接在主力环境运行。 证据：`README.md` Claim：`clm_0005` supported 0.86

### 现在还不能相信

- **工具权限边界不能在安装前相信。**（unverified）：MCP/tool 类项目通常会触碰文件、网络、浏览器或外部 API，必须真实检查权限和日志。
- **真实输出质量不能在安装前相信。**（unverified）：Prompt Preview 只能展示引导方式，不能证明真实项目中的结果质量。
- **宿主 AI 版本兼容性不能在安装前相信。**（unverified）：Claude、Cursor、Codex、Gemini 等宿主加载规则和版本差异必须在真实环境验证。
- **不会污染现有宿主 AI 行为，不能直接相信。**（inferred）：Skill、plugin、AGENTS/CLAUDE/GEMINI 指令可能改变宿主 AI 的默认行为。 证据：`.qwen/skills/bugfix/SKILL.md`, `.qwen/skills/codegraph/SKILL.md`, `.qwen/skills/docs-audit-and-refresh/SKILL.md`, `.qwen/skills/docs-update-from-diff/SKILL.md` 等
- **可安全回滚不能默认相信。**（unverified）：除非项目明确提供卸载和恢复说明，否则必须先在隔离环境验证。
- **真实安装后是否与用户当前宿主 AI 版本兼容？**（unverified）：兼容性只能通过实际宿主环境验证。
- **项目输出质量是否满足用户具体任务？**（unverified）：安装前预览只能展示流程和边界，不能替代真实评测。
- **安装命令是否需要网络、权限或全局写入？**（unverified）：这影响企业环境和个人环境的安装风险。 证据：`README.md`

### 继续会触碰什么

- **命令执行**：包管理器、网络下载、本地插件目录、项目配置或用户主目录。 原因：运行第一条命令就可能产生环境改动；必须先判断是否值得跑。 证据：`AGENTS.md`, `README.md`, `docs/users/quickstart.md`, `packages/channels/base/README.md` 等
- **宿主 AI 配置**：Claude/Codex/Cursor/Gemini/OpenCode 等宿主的 plugin、Skill 或规则加载配置。 原因：宿主配置会改变 AI 后续工作方式，可能和用户已有规则冲突。 证据：`.qwen/skills/bugfix/SKILL.md`, `.qwen/skills/codegraph/SKILL.md`, `.qwen/skills/docs-audit-and-refresh/SKILL.md`, `.qwen/skills/docs-update-from-diff/SKILL.md` 等
- **本地环境或项目文件**：安装结果、插件缓存、项目配置或本地依赖目录。 原因：安装前无法证明写入范围和回滚方式，需要隔离验证。 证据：`AGENTS.md`, `README.md`, `docs/users/quickstart.md`, `packages/channels/base/README.md` 等
- **环境变量 / API Key**：项目入口文档明确出现 API key、token、secret 或账号凭证配置。 原因：如果真实安装需要凭证，应先使用测试凭证并经过权限/合规判断。 证据：`.qwen/skills/qwen-code-claw/SKILL.md`, `README.md`, `docs/users/configuration/auth.md`, `docs/users/configuration/model-providers.md` 等
- **宿主 AI 上下文**：AI Context Pack、Prompt Preview、Skill 路由、风险规则和项目事实。 原因：导入上下文会影响宿主 AI 后续判断，必须避免把未验证项包装成事实。

### 最小安全下一步

- **先跑 Prompt Preview**：用安装前交互式试用判断工作方式是否匹配，不需要授权或改环境。（适用：任何项目都适用，尤其是输出质量未知时。）
- **只在隔离目录或测试账号试装**：避免安装命令污染主力宿主 AI、真实项目或用户主目录。（适用：存在命令执行、插件配置或本地写入线索时。）
- **先备份宿主 AI 配置**：Skill、plugin、规则文件可能改变 Claude/Cursor/Codex 的默认行为。（适用：存在插件 manifest、Skill 或宿主规则入口时。）
- **不要使用真实生产凭证**：环境变量/API key 一旦进入宿主或工具链，可能产生账号和合规风险。（适用：出现 API、TOKEN、KEY、SECRET 等环境线索时。）
- **安装后只验证一个最小任务**：先验证加载、兼容、输出质量和回滚，再决定是否深用。（适用：准备从试用进入真实工作流时。）

### 退出方式

- **保留安装前状态**：记录原始宿主配置和项目状态，后续才能判断是否可恢复。
- **准备移除宿主 plugin / Skill / 规则入口**：如果试装后行为异常，可以把宿主 AI 恢复到试装前状态。
- **记录安装命令和写入路径**：没有明确卸载说明时，至少要知道哪些目录或配置需要手动清理。
- **准备撤销测试 API key 或 token**：测试凭证泄露或误用时，可以快速止损。
- **如果没有回滚路径，不进入主力环境**：不可回滚是继续前阻断项，不应靠信任或运气继续。

## 哪些只能预览

- 解释项目适合谁和能做什么
- 基于项目文档演示典型对话流程
- 帮助用户判断是否值得安装或继续研究

## 哪些必须安装后验证

- 真实安装 Skill、插件或 CLI
- 执行脚本、修改本地文件或访问外部服务
- 验证真实输出质量、性能和兼容性

## 边界与风险判断卡

- **把安装前预览误认为真实运行**：用户可能高估项目已经完成的配置、权限和兼容性验证。 处理方式：明确区分 prompt_preview_can_do 与 runtime_required。 Claim：`clm_0017` inferred 0.45
- **命令执行会修改本地环境**：安装命令可能写入用户主目录、宿主插件目录或项目配置。 处理方式：先在隔离环境或测试账号中运行。 证据：`AGENTS.md`, `README.md`, `docs/users/quickstart.md`, `packages/channels/base/README.md` 等 Claim：`clm_0018` supported 0.86
- **待确认**：真实安装后是否与用户当前宿主 AI 版本兼容？。原因：兼容性只能通过实际宿主环境验证。
- **待确认**：项目输出质量是否满足用户具体任务？。原因：安装前预览只能展示流程和边界，不能替代真实评测。
- **待确认**：安装命令是否需要网络、权限或全局写入？。原因：这影响企业环境和个人环境的安装风险。

## 开工前工作上下文

### 加载顺序

- 先读取 how_to_use.host_ai_instruction，建立安装前判断资产的边界。
- 读取 claim_graph_summary，确认事实来自 Claim/Evidence Graph，而不是 Human Wiki 叙事。
- 再读取 intended_users、capabilities 和 quick_start_candidates，判断用户是否匹配。
- 需要执行具体任务时，优先查 role_skill_index，再查 evidence_index。
- 遇到真实安装、文件修改、网络访问、性能或兼容性问题时，转入 risk_card 和 boundaries.runtime_required。

### 任务路由

- **AI Skill / Agent 指令资产库**：先基于 role_skill_index / evidence_index 帮用户挑选可用角色、Skill 或工作流。 边界：可做安装前 Prompt 体验。 证据：`.qwen/skills/bugfix/SKILL.md`, `.qwen/skills/codegraph/SKILL.md`, `.qwen/skills/docs-audit-and-refresh/SKILL.md`, `.qwen/skills/docs-update-from-diff/SKILL.md` 等 Claim：`clm_0001` supported 0.86
- **命令行启动或安装流程**：先说明这是安装后验证能力，再给出安装前检查清单。 边界：必须真实安装或运行后验证。 证据：`AGENTS.md`, `README.md`, `docs/users/quickstart.md`, `packages/channels/base/README.md` 等 Claim：`clm_0002` supported 0.86

### 上下文规模

- 文件总数：2456
- 重要文件覆盖：40/2456
- 证据索引条目：80
- 角色 / Skill 条目：15

### 证据不足时的处理

- **missing_evidence**：说明证据不足，要求用户提供目标文件、README 段落或安装后验证记录；不要补全事实。
- **out_of_scope_request**：说明该任务超出当前 AI Context Pack 证据范围，并建议用户先查看 Human Manual 或真实安装后验证。
- **runtime_request**：给出安装前检查清单和命令来源，但不要替用户执行命令或声称已执行。
- **source_conflict**：同时展示冲突来源，标记为待核实，不要强行选择一个版本。

## Prompt Recipes

### 适配判断

- 目标：判断这个项目是否适合用户当前任务。
- 预期输出：适配结论、关键理由、证据引用、安装前可预览内容、必须安装后验证内容、下一步建议。

```text
请基于 @qwen-code/qwen-code 的 AI Context Pack，先问我 3 个必要问题，然后判断它是否适合我的任务。回答必须包含：适合谁、能做什么、不能做什么、是否值得安装、证据来自哪里。所有项目事实必须引用 evidence_refs、source_paths 或 claim_id。
```

### 安装前体验

- 目标：让用户在安装前感受核心工作流，同时避免把预览包装成真实能力或营销承诺。
- 预期输出：一段带边界标签的体验剧本、安装后验证清单和谨慎建议；不含真实运行承诺或强营销表述。

```text
请把 @qwen-code/qwen-code 当作安装前体验资产，而不是已安装工具或真实运行环境。

请严格输出四段：
1. 先问我 3 个必要问题。
2. 给出一段“体验剧本”：用 [安装前可预览]、[必须安装后验证]、[证据不足] 三种标签展示它可能如何引导工作流。
3. 给出安装后验证清单：列出哪些能力只有真实安装、真实宿主加载、真实项目运行后才能确认。
4. 给出谨慎建议：只能说“值得继续研究/试装”“先补充信息后再判断”或“不建议继续”，不得替项目背书。

硬性边界：
- 不要声称已经安装、运行、执行测试、修改文件或产生真实结果。
- 不要写“自动适配”“确保通过”“完美适配”“强烈建议安装”等承诺性表达。
- 如果描述安装后的工作方式，必须使用“如果安装成功且宿主正确加载 Skill，它可能会……”这种条件句。
- 体验剧本只能写成“示例台词/假设流程”：使用“可能会询问/可能会建议/可能会展示”，不要写“已写入、已生成、已通过、正在运行、正在生成”。
- Prompt Preview 不负责给安装命令；如用户准备试装，只能提示先阅读 Quick Start 和 Risk Card，并在隔离环境验证。
- 所有项目事实必须来自 supported claim、evidence_refs 或 source_paths；inferred/unverified 只能作风险或待确认项。

```

### 角色 / Skill 选择

- 目标：从项目里的角色或 Skill 中挑选最匹配的资产。
- 预期输出：候选角色或 Skill 列表，每项包含适用场景、证据路径、风险边界和是否需要安装后验证。

```text
请读取 role_skill_index，根据我的目标任务推荐 3-5 个最相关的角色或 Skill。每个推荐都要说明适用场景、可能输出、风险边界和 evidence_refs。
```

### 风险预检

- 目标：安装或引入前识别环境、权限、规则冲突和质量风险。
- 预期输出：环境、权限、依赖、许可、宿主冲突、质量风险和未知项的检查清单。

```text
请基于 risk_card、boundaries 和 quick_start_candidates，给我一份安装前风险预检清单。不要替我执行命令，只说明我应该检查什么、为什么检查、失败会有什么影响。
```

### 宿主 AI 开工指令

- 目标：把项目上下文转成一次对话开始前的宿主 AI 指令。
- 预期输出：一段边界明确、证据引用明确、适合复制给宿主 AI 的开工前指令。

```text
请基于 @qwen-code/qwen-code 的 AI Context Pack，生成一段我可以粘贴给宿主 AI 的开工前指令。这段指令必须遵守 not_runtime=true，不能声称项目已经安装、运行或产生真实结果。
```


## 角色 / Skill 索引

- 共索引 15 个角色 / Skill / 项目文档条目。

- **bugfix**（skill）：Fix a bug from a GitHub issue, following the reproduce-first 激活提示：当用户任务与“bugfix”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/bugfix/SKILL.md`
- **codegraph**（skill）：Analyze indexed codebases via graph database neug and vector index zvec . Covers call graphs, dependencies, dead code, hotspots, module coupling, architecture reports, semantic search, impact analysis, bug root cause from GitHub issues, class diagrams UML , and PR review risk scoring, conflict detection, auto-merge candidates, labeling . Also covers creating, inspecting, and repairing a CodeScope index. Use for: cod… 激活提示：当用户任务与“codegraph”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/codegraph/SKILL.md`
- **docs-audit-and-refresh**（skill）：Audit the repository's docs/ content against the current codebase, 激活提示：当用户任务与“docs-audit-and-refresh”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/docs-audit-and-refresh/SKILL.md`
- **docs-update-from-diff**（skill）：Review local code changes with git diff and update the official 激活提示：当用户任务与“docs-update-from-diff”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/docs-update-from-diff/SKILL.md`
- **e2e-testing**（skill）：Guide for running end-to-end tests of the Qwen Code CLI, including 激活提示：当用户任务与“e2e-testing”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/e2e-testing/SKILL.md`
- **feat-dev**（skill）：End-to-end workflow for implementing a non-trivial qwen-code 激活提示：当用户任务与“feat-dev”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/feat-dev/SKILL.md`
- **qwen-code-claw**（skill）：Use Qwen Code as a Code Agent for code understanding, project 激活提示：当用户任务与“qwen-code-claw”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/qwen-code-claw/SKILL.md`
- **structured-debugging**（skill）：Hypothesis-driven debugging methodology for hard bugs. Use this 激活提示：当用户任务与“structured-debugging”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/structured-debugging/SKILL.md`
- **terminal-capture**（skill）：Automates terminal UI screenshot testing for CLI commands. Applies 激活提示：当用户任务与“terminal-capture”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/terminal-capture/SKILL.md`
- **tmux-real-user-testing**（skill）：This skill should be used when the user asks to "用 tmux 做真实测试", "保存 tmux 日志", "像真实用户一样测试 Qwen", "生成可复查的 TUI 测试报告", "测试 slash command 交互", or requests a tmux-based real user E2E run with complete readable logs. It guides real TUI usage with step-by-step capture-pane snapshots rather than ANSI raw pipe logs. 激活提示：当用户任务与“tmux-real-user-testing”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`.qwen/skills/tmux-real-user-testing/SKILL.md`
- **synonyms**（skill）：Generate synonyms for words or phrases. Use this skill when the user needs alternative words with similar meanings, wants to expand vocabulary, or seeks varied expressions for writing. 激活提示：当用户任务与“synonyms”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`packages/cli/src/commands/extensions/examples/skills/skills/synonyms/SKILL.md`
- **batch**（skill）：Execute batch operations on multiple files in parallel. Automatically discovers files, splits into chunks, and processes with parallel worker agents. Use /batch followed by operation and file pattern. 激活提示：当用户任务与“batch”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`packages/core/src/skills/bundled/batch/SKILL.md`
- **loop**（skill）：Create a recurring loop that runs a prompt on a schedule. Usage - /loop 5m check the build, /loop check the PR every 30m, /loop run tests defaults to 10m . /loop list to show jobs, /loop clear to cancel all. 激活提示：当用户任务与“loop”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`packages/core/src/skills/bundled/loop/SKILL.md`
- **qc-helper**（skill）：Answer any question about Qwen Code usage, features, configuration, and troubleshooting by referencing the official user documentation. Also helps users view or modify their settings.json. Invoke with /qc-helper followed by a question, e.g. /qc-helper how do I configure MCP servers? or /qc-helper change approval mode to yolo . 激活提示：当用户任务与“qc-helper”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`packages/core/src/skills/bundled/qc-helper/SKILL.md`
- **review**（skill）：Review changed code for correctness, security, code quality, and performance. Use when the user asks to review code changes, a PR, or specific files. Invoke with /review , /review , /review , or /review --comment to post inline comments on the PR. 激活提示：当用户任务与“review”描述的流程高度相关时，先用它做安装前体验，再决定是否安装。 证据：`packages/core/src/skills/bundled/review/SKILL.md`

## 证据索引

- 共索引 80 条证据。

- **How to Contribute**（documentation）：We would love to accept your patches and contributions to this project. 证据：`docs/developers/contributing.md`
- **AGENTS.md**（documentation）：This file provides guidance to Qwen Code when working with code in this repository. 证据：`AGENTS.md`
- **🎉 News**（documentation）：! npm version https://img.shields.io/npm/v/@qwen-code/qwen-code.svg https://www.npmjs.com/package/@qwen-code/qwen-code ! License https://img.shields.io/github/license/QwenLM/qwen-code.svg ./LICENSE ! Node.js Version https://img.shields.io/badge/node-%3E%3D22.0.0-brightgreen.svg https://nodejs.org/ ! Downloads https://img.shields.io/npm/dm/@qwen-code/qwen-code.svg https://www.npmjs.com/package/@qwen-code/qwen-code 证据：`README.md`
- **Qwen Code Docs Site**（documentation）：A documentation website for Qwen Code built with Next.js https://nextjs.org/ and Nextra https://nextra.site/ . 证据：`docs-site/README.md`
- **Qwen Concurrent Runner**（documentation）：A Python tool for executing multiple Qwen CLI tasks across different models concurrently using isolated git worktrees. 证据：`integration-tests/concurrent-runner/README.md`
- **@qwen-code/channel-base**（documentation）：Base infrastructure for building Qwen Code channel adapters. Provides the abstract base class, access control, session routing, and the ACP bridge that communicates with the agent. 证据：`packages/channels/base/README.md`
- **@qwen-code/channel-plugin-example**（documentation）：A reference channel plugin for Qwen Code. It connects to a WebSocket server and routes messages through the full channel pipeline access control, session routing, agent bridge . 证据：`packages/channels/plugin-example/README.md`
- **Message Rewrite Middleware**（documentation）：⚠️ Temporary Solution — subject to change or removal at any time. This is a stopgap implementation. We are considering a hook-based approach that would be more decoupled and extensible. Ideas and suggestions for a better design are very welcome. 证据：`packages/cli/src/acp-integration/session/rewrite/README.md`
- **Provider Structure**（documentation）：This folder contains the different provider implementations for the Qwen Code refactor system. 证据：`packages/core/src/core/openaiContentGenerator/provider/README.md`
- **qwen-code-sdk**（documentation）：Experimental Python SDK for programmatic access to Qwen Code through the stream-json protocol. 证据：`packages/sdk-python/README.md`
- **@qwen-code/sdk**（documentation）：A minimum experimental TypeScript SDK for programmatic access to Qwen Code. 证据：`packages/sdk-typescript/README.md`
- **Qwen Code Companion**（documentation）：! Version https://img.shields.io/visual-studio-marketplace/v/qwenlm.qwen-code-vscode-ide-companion https://marketplace.visualstudio.com/items?itemName=qwenlm.qwen-code-vscode-ide-companion ! VS Code Installs https://img.shields.io/visual-studio-marketplace/i/qwenlm.qwen-code-vscode-ide-companion https://marketplace.visualstudio.com/items?itemName=qwenlm.qwen-code-vscode-ide-companion ! Open VSX Downloads https://img.shields.io/open-vsx/dt/qwenlm/qwen-code-vscode-ide-companion https://open-vsx.org/extension/qwenlm/qwen-code-vscode-ide-companion ! Rating https://img.shields.io/visual-studio-marketplace/r/qwenlm.qwen-code-vscode-ide-companion https://marketplace.visualstudio.com/items?itemName… 证据：`packages/vscode-ide-companion/README.md`
- **@qwen-code/webui**（documentation）：A shared React component library for Qwen Code applications, providing cross-platform UI components with consistent styling and behavior. 证据：`packages/webui/README.md`
- **Examples**（documentation）：This directory contains example implementations demonstrating various ways to use the @qwen-code/webui library. 证据：`packages/webui/examples/README.md`
- **Qwen Code Agent Server Extension for Zed**（documentation）：Qwen Code Agent Server Extension for Zed 证据：`packages/zed-extension/README.md`
- **Package**（package_manifest）：{ "name": "docs-site", "version": "1.0.0", "description": "", "license": "ISC", "author": "", "type": "module", "main": "index.js", "scripts": { "link": "ln -s ../docs content", "clean": "rm -rf .next", "dev": "npm run clean && next --turbopack", "test": "echo \"Error: no test specified\" && exit 1" }, "dependencies": { "next": "^16.0.8", "nextra": "^4.6.1", "nextra-theme-docs": "^4.6.1", "react": "^19.2.1", "react-dom": "^19.2.1" } } 证据：`docs-site/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/qwen-code", "version": "0.15.11", "engines": { "node": " =22.0.0" }, "type": "module", "workspaces": "packages/ ", "packages/channels/base", "packages/channels/telegram", "packages/channels/weixin", "packages/channels/dingtalk", "packages/channels/plugin-example" , "repository": { "type": "git", "url": "git+https://github.com/QwenLM/qwen-code.git" }, "config": { "sandboxImageUri": "ghcr.io/qwenlm/qwen-code:0.15.11" }, "scripts": { "start": "cross-env node scripts/start.js", "dev": "node scripts/dev.js", "debug": "cross-env DEBUG=1 node --inspect-brk scripts/start.js", "generate": "node scripts/generate-git-commit-info.js", "generate:settings-schema": "node --import tsx… 证据：`package.json`
- **How to Contribute**（documentation）：We would love to accept your patches and contributions to this project. 证据：`CONTRIBUTING.md`
- **Package**（package_manifest）：{ "name": "toy-project", "version": "1.0.0", "description": "Minimal toy project for testing", "scripts": { "build": "echo 'Build complete!'" }, "keywords": , "author": "", "license": "MIT" } 证据：`integration-tests/concurrent-runner/examples/toy-project/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/terminal-capture", "version": "0.1.0", "private": true, "description": "Terminal UI screenshot automation for CLI visual testing", "type": "module", "scripts": { "capture": "npx tsx run.ts scenarios/", "capture:about": "npx tsx run.ts scenarios/about.ts", "capture:all": "npx tsx run.ts scenarios/all.ts", "capture:markdown-rendering": "npx tsx run.ts scenarios/markdown-rendering.ts" }, "dependencies": { "@lydell/node-pty": "1.2.0-beta.10", "@xterm/xterm": "^5.5.0", "playwright": "^1.50.0", "strip-ansi": "^7.1.2" } } 证据：`integration-tests/terminal-capture/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/channel-base", "version": "0.15.11", "description": "Base channel infrastructure for Qwen Code", "type": "module", "main": "dist/index.js", "types": "dist/index.d.ts", "exports": { ".": { "types": "./dist/index.d.ts", "default": "./dist/index.js" } }, "files": "dist" , "scripts": { "build": "tsc --build" }, "dependencies": { "@agentclientprotocol/sdk": "^0.14.1" }, "devDependencies": { "typescript": "^5.0.0" } } 证据：`packages/channels/base/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/channel-dingtalk", "version": "0.15.11", "description": "DingTalk channel adapter for Qwen Code", "type": "module", "main": "dist/index.js", "types": "dist/index.d.ts", "exports": { ".": { "types": "./dist/index.d.ts", "default": "./dist/index.js" } }, "files": "dist" , "scripts": { "build": "tsc --build" }, "dependencies": { "@qwen-code/channel-base": "file:../base", "dingtalk-stream-sdk-nodejs": "^2.0.4" }, "devDependencies": { "typescript": "^5.0.0" } } 证据：`packages/channels/dingtalk/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/channel-plugin-example", "version": "0.15.11", "private": true, "type": "module", "main": "dist/index.js", "types": "dist/index.d.ts", "exports": { ".": { "types": "./dist/index.d.ts", "default": "./dist/index.js" } }, "files": "dist", "src", "qwen-extension.json" , "bin": { "qwen-channel-plugin-example-server": "dist/start-server.js" }, "scripts": { "build": "tsc --build", "prepublishOnly": "npm run build" }, "dependencies": { "@qwen-code/channel-base": "file:../base", "ws": "^8.18.0" }, "devDependencies": { "@types/ws": "^8.5.0" } } 证据：`packages/channels/plugin-example/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/channel-telegram", "version": "0.15.11", "description": "Telegram channel adapter for Qwen Code", "type": "module", "main": "dist/index.js", "types": "dist/index.d.ts", "exports": { ".": { "types": "./dist/index.d.ts", "default": "./dist/index.js" } }, "files": "dist" , "scripts": { "build": "tsc --build" }, "dependencies": { "@qwen-code/channel-base": "file:../base", "grammy": "^1.41.1", "https-proxy-agent": "^7.0.6", "telegram-markdown-formatter": "^0.1.2" }, "devDependencies": { "typescript": "^5.0.0" } } 证据：`packages/channels/telegram/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/channel-weixin", "version": "0.15.11", "description": "WeChat Weixin channel adapter for Qwen Code", "type": "module", "main": "dist/index.js", "types": "dist/index.d.ts", "exports": { ".": { "types": "./dist/index.d.ts", "default": "./dist/index.js" }, "./accounts": { "types": "./dist/accounts.d.ts", "default": "./dist/accounts.js" }, "./login": { "types": "./dist/login.d.ts", "default": "./dist/login.js" } }, "files": "dist" , "scripts": { "build": "tsc --build" }, "dependencies": { "@qwen-code/channel-base": "file:../base" }, "devDependencies": { "typescript": "^5.0.0" } } 证据：`packages/channels/weixin/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/qwen-code", "version": "0.15.11", "description": "Qwen Code", "repository": { "type": "git", "url": "git+https://github.com/QwenLM/qwen-code.git" }, "type": "module", "main": "dist/index.js", "types": "dist/index.d.ts", "bin": { "qwen": "dist/index.js" }, "exports": { ".": { "types": "./dist/index.d.ts", "import": "./dist/index.js" }, "./export": { "types": "./dist/src/export/index.d.ts", "import": "./dist/src/export/index.js" } }, "scripts": { "build": "node ../../scripts/build package.js", "start": "node dist/index.js", "debug": "node --inspect-brk dist/index.js", "lint": "eslint . --ext .ts,.tsx", "format": "prettier --write .", "test": "vitest run", "test:ci": "vit… 证据：`packages/cli/package.json`
- **Package**（package_manifest）：{ "name": "mcp-server-example", "version": "1.0.0", "description": "Example MCP Server for Qwen Code Extension", "type": "module", "main": "example.js", "scripts": { "build": "tsc" }, "devDependencies": { "typescript": "~5.4.5", "@types/node": "^20.11.25" }, "dependencies": { "@modelcontextprotocol/sdk": "^1.11.0", "zod": "^3.22.4" } } 证据：`packages/cli/src/commands/extensions/examples/mcp-server/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/qwen-code-core", "version": "0.15.11", "description": "Qwen Code Core", "repository": { "type": "git", "url": "git+https://github.com/QwenLM/qwen-code.git" }, "type": "module", "main": "dist/index.js", "scripts": { "build": "node ../../scripts/build package.js", "lint": "eslint . --ext .ts,.tsx", "format": "prettier --write .", "test": "vitest run", "test:ci": "vitest run", "typecheck": "tsc --noEmit", "postinstall": "node scripts/postinstall.js" }, "files": "dist", "vendor", "scripts/postinstall.js" , "dependencies": { "@anthropic-ai/sdk": "^0.36.1", "@google/genai": "1.30.0", "@iarna/toml": "^2.2.5", "@modelcontextprotocol/sdk": "^1.25.1", "@opentelemetry/api": "^1.9… 证据：`packages/core/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/sdk", "version": "0.1.7", "description": "TypeScript SDK for programmatic access to qwen-code CLI", "main": "./dist/index.cjs", "module": "./dist/index.mjs", "types": "./dist/index.d.ts", "type": "module", "exports": { ".": { "types": "./dist/index.d.ts", "import": "./dist/index.mjs", "require": "./dist/index.cjs" }, "./package.json": "./package.json" }, "files": "dist", "README.md" , "scripts": { "build": "node scripts/build.js", "bundle:cli": "node scripts/bundle-cli.js", "test": "vitest run", "test:ci": "vitest run", "test:watch": "vitest", "test:coverage": "vitest run --coverage", "lint": "eslint src test", "lint:fix": "eslint src test --fix", "typecheck": "tsc --n… 证据：`packages/sdk-typescript/package.json`
- **Package**（package_manifest）：{ "name": "qwen-code-vscode-ide-companion", "displayName": "Qwen Code Companion", "description": "Enable Qwen Code with direct access to your VS Code workspace.", "version": "0.15.11", "publisher": "qwenlm", "icon": "assets/icon.png", "repository": { "type": "git", "url": "https://github.com/QwenLM/qwen-code.git", "directory": "packages/vscode-ide-companion" }, "engines": { "vscode": "^1.85.0" }, "license": "LICENSE", "preview": true, "categories": "AI" , "keywords": "qwen-code", "qwen code", "qwen", "qwen code", "cli", "ide integration", "ide companion" , "activationEvents": "onStartupFinished", "onView:qwen-code.chatView.sidebar", "onView:qwen-code.chatView.secondary", "onCommand:qwen-cod… 证据：`packages/vscode-ide-companion/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/web-templates", "version": "0.15.11", "description": "Web templates bundled as embeddable JS/CSS strings", "repository": { "type": "git", "url": "git+https://github.com/QwenLM/qwen-code.git" }, "type": "module", "main": "dist/index.js", "types": "dist/index.d.ts", "exports": { ".": { "types": "./dist/index.d.ts", "import": "./dist/index.js" } }, "scripts": { "build": "node build.mjs && tsc --build --clean && tsc", "build:templates": "node build.mjs" }, "files": "dist" , "dependencies": {}, "devDependencies": { "@types/react": "^18.2.0", "@types/react-dom": "^18.2.0", "@vitejs/plugin-react": "^4.2.0", "autoprefixer": "^10.4.22", "postcss": "^8.5.6", "tailwindcss": "^3.4… 证据：`packages/web-templates/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/cli-export-html", "private": true, "type": "module", "scripts": { "build": "node build.mjs" }, "dependencies": { "@qwen-code/webui": "latest" }, "devDependencies": { "esbuild": "^0.25.0" } } 证据：`packages/web-templates/src/export-html/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/cli-insight", "private": true, "type": "module", "scripts": { "dev": "vite", "build": "node build.mjs" } } 证据：`packages/web-templates/src/insight/package.json`
- **Package**（package_manifest）：{ "name": "@qwen-code/webui", "version": "0.15.11", "description": "Shared UI components for Qwen Code packages", "type": "module", "main": "./dist/index.cjs", "module": "./dist/index.js", "types": "./dist/index.d.ts", "exports": { ".": { "types": "./dist/index.d.ts", "import": "./dist/index.js", "require": "./dist/index.cjs" }, "./icons": { "types": "./dist/components/icons/index.d.ts", "import": "./dist/components/icons/index.js", "require": "./dist/components/icons/index.cjs" }, "./tailwind.preset": "./tailwind.preset.cjs", "./styles.css": "./dist/styles.css" }, "files": "dist", "tailwind.preset.cjs" , "sideEffects": " / .css" , "publishConfig": { "access": "public" }, "scripts": { "dev"… 证据：`packages/webui/package.json`
- **Bugfix Workflow**（skill_instruction）：Follow this workflow for GitHub issue bugfixes. Do not skip reproduction; fixing without first reproducing the bug tends to produce incomplete fixes and regressions. 证据：`.qwen/skills/bugfix/SKILL.md`
- **CodeScope Q&A**（skill_instruction）：CodeScope indexes source code into a two-layer knowledge graph — structure functions, calls, imports, classes, modules and evolution commits, file changes, function modifications — plus semantic embeddings for every function. Supports Python, JavaScript/TypeScript, C, and Java including Hadoop-scale repositories with 8K+ files . This combination enables analyses that grep, LSP, or pure vector search cannot do alone. It can also fetch GitHub issues and trace bugs to code , and review open PRs — scoring per-PR risk, detecting cross-PR conflicts, identifying auto-merge candidates, and applying GitHub labels. 证据：`.qwen/skills/codegraph/SKILL.md`
- **Docs Audit And Refresh**（skill_instruction）：Audit docs/ from the repository outward: inspect the current implementation, identify documentation gaps or inaccuracies, and update the relevant pages. Keep the work inside docs/ and treat code, tests, and current configuration surfaces as the authoritative source. 证据：`.qwen/skills/docs-audit-and-refresh/SKILL.md`
- **Docs Update From Diff**（skill_instruction）：Inspect local diffs, derive the documentation impact, and update only the repository's docs/ pages. Treat the current code as the source of truth and keep changes scoped, specific, and navigable. 证据：`.qwen/skills/docs-update-from-diff/SKILL.md`
- **E2E Testing Guide**（skill_instruction）：How to run the Qwen Code CLI end-to-end, from building the bundle to inspecting raw API traffic. Use when unit tests are not enough and you need to verify behavior through the full pipeline model API → tool validation → tool execution . 证据：`.qwen/skills/e2e-testing/SKILL.md`
- **Feature Development Workflow**（skill_instruction）：Use this workflow when implementing a feature in qwen-code that needs design, behavioral validation, or coordinated changes across multiple files. Each phase produces a concrete artifact. Do not combine phases; the output of each phase feeds the next. 证据：`.qwen/skills/feat-dev/SKILL.md`
- **Qwen Code Claw**（skill_instruction）：- Understand codebases or ask questions about source code - Generate new projects or add new features - Review pull requests in the codebase - Fix bugs or refactor existing code - Execute various programming tasks such as code review, testing, documentation generation, etc. - Collaborate with other tools and agents to complete complex development tasks 证据：`.qwen/skills/qwen-code-claw/SKILL.md`
- **Structured Debugging**（skill_instruction）：When debugging hard issues, the natural instinct is to form a theory and immediately apply a fix. This fails more often than it works. The fix addresses the wrong cause, adds complexity, creates false confidence, and obscures the real issue. Worse, after several failed attempts you lose track of what's been tried and start guessing randomly. 证据：`.qwen/skills/structured-debugging/SKILL.md`
- **Terminal Capture — CLI Terminal Screenshot Automation**（skill_instruction）：Terminal Capture — CLI Terminal Screenshot Automation 证据：`.qwen/skills/terminal-capture/SKILL.md`
- **tmux Real User Testing**（skill_instruction）：Run Qwen Code in a real tmux TUI session as a user would: navigate dialogs, trigger slash commands, exercise workflows, and save a readable log that maintainers can review. Prefer this workflow when the goal is not just a pass/fail assertion, but a narrative artifact showing what happened on screen. 证据：`.qwen/skills/tmux-real-user-testing/SKILL.md`
- **Synonym Generation Guidelines**（skill_instruction）：This skill helps generate synonyms and alternative expressions for given words or phrases. It provides contextually appropriate alternatives to enhance vocabulary and improve writing variety. 证据：`packages/cli/src/commands/extensions/examples/skills/skills/synonyms/SKILL.md`
- **/batch - Parallel Batch Operations**（skill_instruction）：You are orchestrating a batch operation across multiple files. Your job is to: 证据：`packages/core/src/skills/bundled/batch/SKILL.md`
- **/loop — schedule a recurring prompt**（skill_instruction）：/loop — schedule a recurring prompt 证据：`packages/core/src/skills/bundled/loop/SKILL.md`
- **Qwen Code Helper**（skill_instruction）：You are a helpful assistant for Qwen Code — an AI coding agent for the terminal. Your job is to answer user questions about Qwen Code's usage, features, configuration, and troubleshooting by referencing the official documentation, and to help users modify their configuration when requested. 证据：`packages/core/src/skills/bundled/qc-helper/SKILL.md`
- **Code Review**（skill_instruction）：You are an expert code reviewer. Your job is to review code changes and provide actionable feedback. 证据：`packages/core/src/skills/bundled/review/SKILL.md`
- **License**（source_file）：Apache License Version 2.0, January 2004 http://www.apache.org/licenses/ 证据：`LICENSE`
- **License**（source_file）：Apache License Version 2.0, January 2004 http://www.apache.org/licenses/ 证据：`packages/vscode-ide-companion/LICENSE`
- **License**（source_file）：Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files the "Software" , to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions: 证据：`packages/zed-extension/LICENSE`
- **Qwen Code Documentation**（documentation）：Welcome to the Qwen Code documentation. Qwen Code is an agentic coding tool that lives in your terminal and helps you turn ideas into code faster than ever before. 证据：`docs/index.md`
- **Adaptive Output Token Escalation Design**（documentation）：Adaptive Output Token Escalation Design 证据：`docs/design/adaptive-output-token-escalation/adaptive-output-token-escalation-design.md`
- **Auth Provider Registry Motivation**（documentation）：The auth module used to model each setup path as a separate flow: API key, OAuth, subscription plans, and custom providers. In practice, all of these paths produce the same kind of output: updates to the user's provider configuration in ~/.qwen/settings.json . 证据：`docs/design/auth/motivation.md`
- **Memory 记忆管理系统**（documentation）：本文介绍 Qwen Code 中 Managed Auto-Memory （托管自动记忆）的记忆管理机制、触发时机和实现细节。 证据：`docs/design/auto-memory/memory-system.md`
- **Channels Design**（documentation）：External messaging integrations for Qwen Code — interact with an agent from Telegram, WeChat, and more. User documentation: Channels Overview ../../users/features/channels/overview.md . 证据：`docs/design/channels/channels-design.md`
- **Compact Mode Design: Competitive Analysis & Optimization**（documentation）：Compact Mode Design: Competitive Analysis & Optimization 证据：`docs/design/compact-mode/compact-mode-design.md`
- **Custom API Key Auth Wizard PRD**（documentation）：Improve the /auth - API Key - Custom API Key experience by replacing the current documentation-only screen with an in-terminal setup wizard for custom API providers. 证据：`docs/design/custom-api-key-auth-wizard-prd.md`
- **Customize Banner Area Design**（documentation）：Allow users to replace the QWEN ASCII art, replace the brand title, and hide the banner entirely — without letting them suppress the operational data version, auth, model, working directory that makes Qwen Code debuggable and trustworthy. 证据：`docs/design/customize-banner-area/customize-banner-area.md`
- 其余 20 条证据见 `AI_CONTEXT_PACK.json` 或 `EVIDENCE_INDEX.json`。

## 宿主 AI 必须遵守的规则

- **把本资产当作开工前上下文，而不是运行环境。**：AI Context Pack 只包含证据化项目理解，不包含目标项目的可执行状态。 证据：`docs/developers/contributing.md`, `AGENTS.md`, `README.md`
- **回答用户时区分可预览内容与必须安装后才能验证的内容。**：安装前体验的消费者价值来自降低误装和误判，而不是伪装成真实运行。 证据：`docs/developers/contributing.md`, `AGENTS.md`, `README.md`

## 用户开工前应该回答的问题

- 你准备在哪个宿主 AI 或本地环境中使用它？
- 你只是想先体验工作流，还是准备真实安装？
- 你最在意的是安装成本、输出质量、还是和现有规则的冲突？

## 验收标准

- 所有能力声明都能回指到 evidence_refs 中的文件路径。
- AI_CONTEXT_PACK.md 没有把预览包装成真实运行。
- 用户能在 3 分钟内看懂适合谁、能做什么、如何开始和风险边界。

---

## Doramagic Context Augmentation

下面内容用于强化 Repomix/AI Context Pack 主体。Human Manual 只提供阅读骨架；踩坑日志会被转成宿主 AI 必须遵守的工作约束。

## Human Manual 骨架

使用规则：这里只是项目阅读路线和显著性信号，不是事实权威。具体事实仍必须回到 repo evidence / Claim Graph。

宿主 AI 硬性规则：
- 不得把页标题、章节顺序、摘要或 importance 当作项目事实证据。
- 解释 Human Manual 骨架时，必须明确说它只是阅读路线/显著性信号。
- 能力、安装、兼容性、运行状态和风险判断必须引用 repo evidence、source path 或 Claim Graph。

- **项目概览**：importance `high`
  - source_paths: README.md, package.json, AGENTS.md
- **快速入门**：importance `high`
  - source_paths: docs/users/quickstart.md, docs/users/configuration/settings.md, docs/users/configuration/auth.md, scripts/installation/INSTALLATION_GUIDE.md
- **系统架构**：importance `high`
  - source_paths: docs/developers/architecture.md, packages/cli/package.json, packages/core/package.json, packages/core/src/index.ts
- **包结构详解**：importance `medium`
  - source_paths: packages/channels/base/src/ChannelBase.ts, packages/sdk-typescript/package.json, packages/sdk-python/pyproject.toml, packages/sdk-java/qwencode/README.md
- **智能体运行时**：importance `high`
  - source_paths: packages/core/src/agents/runtime/agent-core.ts, packages/core/src/agents/runtime/agent-interactive.ts, packages/core/src/agents/runtime/agent-headless.ts, packages/core/src/core/coreToolScheduler.ts, packages/core/src/core/permissionFlow.ts
- **工具系统**：importance `high`
  - source_paths: packages/core/src/tools/tools.ts, packages/core/src/tools/tool-registry.ts, packages/core/src/tools/shell.ts, packages/core/src/tools/edit.ts, packages/core/src/tools/lsp.ts
- **模型集成**：importance `high`
  - source_paths: packages/core/src/core/openaiContentGenerator/openaiContentGenerator.ts, packages/core/src/core/openaiContentGenerator/provider/dashscope.ts, packages/core/src/core/openaiContentGenerator/provider/openrouter.ts, packages/core/src/core/geminiChat.ts, packages/core/src/core/anthropicContentGenerator/anthropicContentGenerator.ts
- **记忆系统**：importance `medium`
  - source_paths: packages/core/src/memory/manager.ts, packages/core/src/memory/recall.ts, packages/core/src/memory/extract.ts, packages/core/src/memory/indexer.ts, packages/core/src/memory/dream.ts

## Repo Inspection Evidence / 源码检查证据

- repo_clone_verified: false
- repo_inspection_verified: false
- repo_commit: `unknown`

宿主 AI 硬性规则：
- 没有 repo_clone_verified=true 时，不得声称已经读过源码。
- 没有 repo_inspection_verified=true 时，不得把 README/docs/package 文件判断写成事实。
- 没有 quick_start_verified=true 时，不得声称 Quick Start 已跑通。

## Doramagic Pitfall Constraints / 踩坑约束

这些规则来自 Doramagic 发现、验证或编译过程中的项目专属坑点。宿主 AI 必须把它们当作工作约束，而不是普通说明文字。

### Constraint 1: 可能修改宿主 AI 配置

- Trigger: 项目面向 Claude/Cursor/Codex/Gemini/OpenCode 等宿主，或安装命令涉及用户配置目录。
- Host AI rule: 列出会写入的配置文件、目录和卸载/回滚步骤。
- Why it matters: 安装可能改变本机 AI 工具行为，用户需要知道写入位置和回滚方法。
- Evidence: capability.host_targets | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | host_targets=claude, claude_code, chatgpt
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 2: 能力判断依赖假设

- Trigger: README/documentation is current enough for a first validation pass.
- Host AI rule: 将假设转成下游验证清单。
- Why it matters: 假设不成立时，用户拿不到承诺的能力。
- Evidence: capability.assumptions | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | README/documentation is current enough for a first validation pass.
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 3: 维护活跃度未知

- Trigger: 未记录 last_activity_observed。
- Host AI rule: 补 GitHub 最近 commit、release、issue/PR 响应信号。
- Why it matters: 新项目、停更项目和活跃项目会被混在一起，推荐信任度下降。
- Evidence: evidence.maintainer_signals | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | last_activity_observed missing
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 4: 下游验证发现风险项

- Trigger: no_demo
- Host AI rule: 进入安全/权限治理复核队列。
- Why it matters: 下游已经要求复核，不能在页面中弱化。
- Evidence: downstream_validation.risk_items | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | no_demo; severity=medium
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 5: 存在安全注意事项

- Trigger: No sandbox install has been executed yet; downstream must verify before user use.
- Host AI rule: 转成明确权限清单和安全审查提示。
- Why it matters: 用户安装前需要知道权限边界和敏感操作。
- Evidence: risks.safety_notes | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | No sandbox install has been executed yet; downstream must verify before user use.
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 6: 存在评分风险

- Trigger: no_demo
- Host AI rule: 把风险写入边界卡，并确认是否需要人工复核。
- Why it matters: 风险会影响是否适合普通用户安装。
- Evidence: risks.scoring_risks | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | no_demo; severity=medium
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 7: issue/PR 响应质量未知

- Trigger: issue_or_pr_quality=unknown。
- Host AI rule: 抽样最近 issue/PR，判断是否长期无人处理。
- Why it matters: 用户无法判断遇到问题后是否有人维护。
- Evidence: evidence.maintainer_signals | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | issue_or_pr_quality=unknown
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

### Constraint 8: 发布节奏不明确

- Trigger: release_recency=unknown。
- Host AI rule: 确认最近 release/tag 和 README 安装命令是否一致。
- Why it matters: 安装命令和文档可能落后于代码，用户踩坑概率升高。
- Evidence: evidence.maintainer_signals | art_875e03abe4cc4cb58b4a8ef8603b8a0b | https://github.com/QwenLM/qwen-code#readme | release_recency=unknown
- Hard boundary: 不要把这个坑点包装成已解决、已验证或可忽略，除非后续验证证据明确证明它已经关闭。

