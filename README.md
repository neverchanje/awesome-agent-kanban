# Awesome Agent Kanban

A curated directory of tools that put agents to work on tasks — organized by **what you want to hand over**, not by how the tool is built.

**Agent kanban**, as this directory uses the term, is a work system that organizes agents around tasks to manage a project, run the work, or coordinate it. A **kanban agent** is an agent that can take a task from an existing board or issue tracker, do the work, and report the result back there. This is a working definition for navigating the directory, not a claim of industry consensus.

Entries verified 2026-09-13.

## Which category do you need?

| What you want | Category |
| --- | --- |
| I have a goal and want an agent to drive it to delivery. | [AI Project Managers](#ai-project-managers) |
| The tasks are already defined and I want agents to finish them. | [Agent Orchestration](#agent-orchestration) |
| I already use agents and want them to share tasks and continue each other's work. | [Agent Coordination & Memory](#agent-coordination--memory) |

## AI Project Managers

Start from a goal, not a task list. These tools clarify the requirement, break it into tasks, order and assign them, then coordinate implementation and follow the work through to delivery. You supply the goal, make the key trade-offs, and accept the result.

- [Agent Kanban](https://github.com/saltbo/agent-kanban) — `ak-plan` splits a project into tasks with owners and dependencies, confirms the whole plan with you, then keeps coordinating execution, review, and rework until the project is finished. Execution runs through a separate runner service.
- [AI4Kanban](https://github.com/ai4kanban/ai4kanban) — breaks a vague goal into cards, clarifies it over rounds of questions, orders dependencies and priorities, calls in specialist agents such as `ui-designer`, and drives implementation, verification, and delivery. You make the key trade-offs and accept the result.

## Agent Orchestration

The work is already defined. These tools organize agents to execute it — managing runs, parallel work, and review of what comes back. You define the tasks and review the results.

- [Agent Kanban](https://github.com/saltbo/agent-kanban) — dispatches planned tasks to agents and tracks execution, review, and rework against the board. The runs themselves are carried out by a separate runner service.
- [Agentic Kanban](https://github.com/p-wegner/agentic-kanban) — start a coding agent in an isolated workspace from a card, follow its output, review the diff, and merge.
- [AI4Kanban](https://github.com/ai4kanban/ai4kanban) — runs a defined card end to end: an agent works it in its own git worktree and returns the change for review before it lands.
- [Automaker](https://github.com/AutoMaker-Org/automaker) — you give a feature request and approve an optional breakdown and plan; agents then run in separate worktrees, in parallel, and submit results for review.
- [Cursor (Linear integration)](https://cursor.com/product/linear) — delegate a Linear issue to Cursor or mention it on one; a cloud agent does the work while you track progress and review the resulting PR from the issue.
- [Devin (Linear integration)](https://docs.devin.ai/integrations/linear) — trigger work on a Linear issue by assignment, label, or command; Devin posts its plan, activity, and PR on the issue for you to follow and review.
- [GitHub Copilot cloud agent (GitHub Issues)](https://docs.github.com/en/issues/tracking-your-work-with-issues/using-issues/assigning-issues-and-pull-requests-to-other-github-users) — assign an issue to Copilot; the agent implements it on its own and opens a pull request for review.
- [Tale](https://github.com/tale-project/tale) — assign tasks to reusable project agents, start coding harnesses in persistent sandboxes, and review the reports and deliverables they return to the project.
- [Task Master](https://github.com/eyaltoledano/claude-task-master) — turns a requirements document into tasks and dependencies; once you approve the execution plan it can run a [cluster of agents](https://docs.task-master.dev/capabilities/clusters) in parallel, including a [TDD workflow](https://docs.task-master.dev/tdd-workflow/quickstart).
- [Vibe Kanban](https://github.com/BloopAI/vibe-kanban) — run tasks through coding-agent workspaces, inspect diffs, and review results. Now community maintained: [bloop has shut down](https://www.vibekanban.com/blog/shutdown) and remote services were withdrawn; local workspaces continue to work, and this entry covers those.

## Agent Coordination & Memory

You already work with agents and want them on one shared task list. These tools keep tasks, dependencies, ownership, and durable context so a different agent — or a later session — can continue where the last one stopped. You drive the workflow.

- [Agent Kanban](https://github.com/saltbo/agent-kanban) — agents claim tasks from a shared board, and status and work records persist so another agent or session can pick one up.
- [AgentKanban](https://docs.agentkanban.io/introducing-agentkanban) — pick a task inside the coding tool you already use, restore its context, and move it through stages; conversations, TODOs, and board memory are kept, and a PLAN / TODO / IMPLEMENT flow guides the agent through clarifying, splitting, and implementing.
- [AI4Kanban](https://github.com/ai4kanban/ai4kanban) — cards and per-module memory hold the decisions and context a task settled, so a later session or a different agent continues from them rather than from scratch.
- [Backlog.md](https://github.com/MrLesk/Backlog.md) — Markdown tasks carry acceptance criteria, milestones, dependencies, plans, and decisions for the next agent to read. Its documented flow also guides an agent from idea to tasks, research, and implementation, with you advancing and reviewing each task.
- [Beads](https://github.com/gastownhall/beads) — agents query unblocked issues, claim, update, and close them against a shared dependency graph and persistent memory. You or an external agent workflow start and drive the execution.
- [Task Master](https://github.com/eyaltoledano/claude-task-master) — the task graph, statuses, and checkpoints can be used on their own to organize agents you already run.

## How entries are classified

- **Categories describe responsibilities, not form factors.** Whether a tool is a UI, a CLI, or an MCP server is not a category. Deployment details — issue-tracker integration, local or cloud, CLI or UI — are noted inside an entry only when they change your choice.
- **A category is earned by a complete workflow.** Splitting tasks, running code, or storing memory, on its own, does not demonstrate project management.
- **A product may appear in more than one category** when it ships a complete, independently usable workflow for each — at most once per category, and each entry describes only that category's workflow. This is not a capability ranking, and absence from a category does not mean a product cannot do that work.
- **Entries are sorted by name** within each category. There is no ranking and no promotional wording.

## What belongs here

- The agent must actually do task work, or read and write tasks, plans, and progress through a workflow the product itself provides.
- Open source and commercial products are treated the same. Coordination and memory tools do not need a visual board.
- Every claim must be backed by official documentation, source code, or a reproducible workflow. A capability the vendor does not document is treated as unverified and left out until it is checked.
- **Not included:** general kanban tools such as Trello and Jira, and products whose only AI feature is summarizing or drafting text.

## Contributing

Open a pull request that adds one entry:

- Name the category and say why the product's full workflow delivers that category's responsibility.
- Link the official doc, source, or reproducible workflow that backs the claim.
- Keep it to one line — the product link and one verifiable sentence. No ranking, no marketing copy.

Corrections are welcome, including to how a product is classified here. Classifications are this directory's editorial judgment based on publicly documented workflows.

This directory is maintained by the [AI4Kanban](https://github.com/ai4kanban/ai4kanban) project. AI4Kanban is listed under the same criteria as every other entry, with no placement, badge, or wording of its own.

## License

[CC0 1.0](LICENSE) — no rights reserved.
