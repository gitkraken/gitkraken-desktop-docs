---
title: Coding Agents in GitKraken Desktop
description: Use Agent Sessions View in GitKraken Desktop to configure coding agent CLIs, create agent sessions, monitor progress, and manage parallel worktrees.
product: GitKraken Desktop
feature: Agents
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-04
llms_include: true
tags: [agents, worktrees, coding-agents, parallel-work, ai, terminal]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: April 2026</kbd>

Use this page to learn how coding agents work in GitKraken Desktop and how to use **Agent Sessions View** to create, monitor, and manage coding agent sessions. Read this page if you want to use external coding agent CLIs such as Claude Code, Codex CLI, Copilot CLI, Gemini CLI, or OpenCode from inside GitKraken Desktop.

<img src='/wp-content/uploads/gkd-agents-panel-overview-20260414.png' class="help-center-img img-bordered" alt="GitKraken Desktop with Agent Sessions View open in the Left Panel. The view shows multiple agent session cards with status indicators alongside the commit graph and an active terminal session running a coding agent.">

A **coding agent** is an external CLI that can work on code in a terminal session. In GitKraken Desktop, each **agent session** runs that CLI in its own [**worktree**](/gitkraken-desktop/worktrees/). **Agent Sessions View** shows those worktrees as agent-focused cards so you can start parallel work, monitor progress, and switch back when an agent needs attention.

GitKraken Desktop explicitly integrates with a set of supported coding agent CLIs. You can also run other coding agents manually in the embedded terminal, even if they do not appear in the coding agent configuration.

This page also helps answer common questions such as:
- How do I use Claude Code with GitKraken Desktop?
- How do I run Copilot CLI as a coding agent in GitKraken?
- How do I use Codex CLI, Gemini CLI, or OpenCode in GitKraken Desktop?
- Can I run multiple coding agent sessions at the same time?

**Requirements and limits**
- Product: GitKraken Desktop with Agent Sessions View enabled
- Coding agent CLI: Install and configure a supported coding agent CLI in <kbd>Preferences > External Tools > Coding Agent</kbd>
- Session model: Each agent session runs in its own Git worktree and working directory
- Repository setup: Setup commands are configured per repository in <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>
- Status support: Agent status indicators are available for Claude Code as of version 12.0.0
- Other agents: You can still run other coding agents manually in the embedded terminal, even if GitKraken does not explicitly integrate with or detect them

| What you want to do | Supported | Where in GitKraken Desktop | Notes |
|---------------------|-----------|-----------------------------|-------|
| Start a coding agent session | Yes | Agent Sessions View | Creates a worktree, runs setup commands, and launches the coding agent CLI |
| Start multiple coding agent sessions at the same time | Yes | Agent Sessions View | Each session runs in a separate worktree |
| Choose a different base branch for a new session | Yes | New Agent Session form | Default base branch is `HEAD` |
| Choose a coding agent CLI for a session | Yes | New Agent Session form | Falls back to the coding agent set in Preferences |
| Monitor agent progress | Yes | Agent Sessions View card | Cards show WIP changes, ahead/behind, and agent status |
| Respond when an agent is waiting for input | Yes | Agent Sessions View and embedded terminal | Claude Code can show a **Waiting for input** status in the card |
| Configure coding agent CLIs | Yes | <kbd>Preferences > External Tools > Coding Agent</kbd> | GitKraken auto-detects installed CLIs |
| Configure setup commands for a repository | Yes | <kbd>Preferences > Repo-Specific Preferences > Agents</kbd> | Commands run before the agent launches |

***

## Quick start for coding agents in GitKraken Desktop

**To open Agent Sessions View:**
Click **Agents** in the `List | Agents` segmented control at the top of the Left Panel.

**To start a coding agent session:**
1. Click **+ New Agent Session** at the top of Agent Sessions View.
2. Enter a branch name.
3. Optional: choose a base branch, choose a coding agent CLI, or click **Configure setup commands**.
4. Click **Start**.

**To monitor an agent session:**
Review the card for branch name, WIP changes, ahead/behind counts, and agent status.

**To respond when an agent is waiting for input:**
Open that worktree or switch to its terminal session and respond there.

**To configure coding agent CLIs:**
Go to <kbd>Preferences > External Tools > Coding Agent</kbd>.

**To configure setup commands for the current repository:**
Go to <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>.

***

## What coding agents, agent sessions, and Agent Sessions View mean

Use these terms consistently when working with Agent Sessions View:

| Term | What it means |
|------|---------------|
| **Coding agent** | An external coding agent CLI such as Claude Code, Codex CLI, Copilot CLI, Gemini CLI, or OpenCode |
| **Coding agent session** | A running session of a coding agent CLI started from GitKraken Desktop |
| **Worktree** | A separate Git working directory used for that agent session |
| **Agent Sessions View** | The Left Panel view that shows worktrees as agent session cards |
| **List view** | The standard Left Panel view for worktrees and branches |

Agent Sessions View and List view use the same underlying worktrees. The difference is how GitKraken Desktop presents them:

- Use **List view** when you want a branch-focused view.
- Use **Agent Sessions View** when you want an agent-focused view with status and quick actions.

<div class='callout callout--basic'>
      <p><strong>Why use Agent Sessions View instead of only List view?</strong> Agent Sessions View shows the same worktrees you already use in GitKraken Desktop, but it organizes them around agent activity such as progress, status, and actions. You can switch between <strong>List</strong> and <strong>Agents</strong> at any time without losing work.</p>
</div>

***

## When to use coding agents in GitKraken Desktop

Use coding agents when you want to:
- Work on multiple tasks in parallel without leaving GitKraken Desktop
- Start a task on a new branch and let a coding agent work in a separate worktree
- Monitor agent progress while you continue working in another worktree
- Review and act on agent-generated changes when the session finishes

Coding agents are usually not the best choice when you:
- Need to make a small manual change in your current worktree
- Do not want to create another worktree
- Need behavior that depends on a CLI that is not installed or configured

***

## How to configure coding agent CLIs (Claude Code, Copilot CLI, Codex CLI, Gemini CLI, OpenCode)

Go to <kbd>Preferences > External Tools > Coding Agent</kbd> to choose which coding agent CLI GitKraken Desktop launches for new sessions.

GitKraken Desktop explicitly integrates with these supported coding agent CLIs:
- [Claude Code](https://code.claude.com/docs/en/quickstart)
- [Codex CLI](https://developers.openai.com/codex/quickstart)
- [Copilot CLI](https://github.com/features/copilot/cli)
- [Gemini CLI](https://geminicli.com/docs/)
- [OpenCode](https://opencode.ai/download)

GitKraken auto-detects installed CLIs. You can also add custom CLI arguments that GitKraken passes when it starts a coding agent session.

If you use a different coding agent, you can still open a session worktree and run that agent manually in the embedded terminal. The agent does not need to appear in the coding agent configuration for you to use that terminal workflow.

If you are asking:
- "How do I use Claude Code with GitKraken Desktop?"
- "How do I run Copilot CLI as a coding agent in GitKraken?"
- "How do I use Codex CLI, Gemini CLI, or OpenCode in GitKraken Desktop?"

The setup path is the same: install the CLI on your system, then configure it in <kbd>Preferences > External Tools > Coding Agent</kbd>.

***

## How to configure setup commands for coding agent sessions

Setup commands run in sequence in the new worktree before the coding agent launches. Use setup commands to prepare the repository for the session, for example:

- `npm install`
- `pnpm install`
- `pnpm build`

Put each command on its own line.

Go to <kbd>Preferences > Repo-Specific Preferences > Agents</kbd> to define setup commands for the current repository.

Because these settings are under Repo-Specific Preferences, setup commands apply only to the repository you configure them in.

<img src='/wp-content/uploads/gkd-agents-setup-commands-preferences-20260413.png' class="help-center-img img-bordered" alt="The Agents pane under Repo-Specific Preferences in GitKraken Desktop, showing a Setup commands text area with example commands, one per line, and helper text explaining that commands run in sequence when a new agent session starts.">

***

## How to create a new coding agent session

1. Open **Agent Sessions View** by clicking **Agents** in the Left Panel.
2. Click **+ New Agent Session**.

   <img src='/wp-content/uploads/gkd-agents-new-session-button-20260414.png' class="help-center-img img-bordered" alt="Agent Sessions View in GitKraken Desktop showing the New Agent Session form expanded at the top with a branch name input, Options section with Base branch and Coding agent dropdowns, and a Configure setup commands link.">

3. Enter a branch name.
4. Optional: review the session options.

   | Option | Use it to | Default |
   |--------|-----------|---------|
   | **Base branch** | Create the new worktree from a different branch | `HEAD` |
   | **Coding agent** | Launch a specific coding agent CLI for this session | Coding agent set in Preferences |

   To update repository setup, click **Configure setup commands** to open <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>.

   <img src='/wp-content/uploads/gkd-agents-new-session-form-20260414.png' class="help-center-img img-bordered" alt="The expanded New Agent Session form showing the Coding agent dropdown open with available options including Claude Code, Codex CLI, Open Code, and Gemini CLI.">

5. Click **Start**.

GitKraken Desktop creates a new worktree from the selected base branch, runs any configured setup commands, and launches the selected coding agent in the embedded terminal.

***

## How to monitor coding agent progress and session status

Each card in Agent Sessions View represents one worktree and one coding agent session.

| Card element | What it shows |
|--------------|---------------|
| **Branch name** | The branch checked out in that worktree |
| **WIP change summary** | The count of uncommitted file changes |
| **Ahead / behind** | Commit counts relative to the remote |
| **Agent status** | Whether the agent is running, waiting for input, or done |

The status bar at the bottom of each card shows the current session state. Status indicators are available for Claude Code as of version 12.0.0.

When an agent needs attention, the card can show a bell icon and a **Waiting for input** label. This lets you see that the session needs a response without switching to the terminal first.

<img src='/wp-content/uploads/gkd-agents-monitoring-status-20260414.png' class="help-center-img img-bordered" alt="Agent Sessions View showing multiple worktree cards with WIP change counts, ahead-behind indicators, and agent status bars displaying various states including Waiting for input.">

You can keep working in another worktree while monitoring these cards. When a session finishes, switch to that worktree to review the results.

***

## How to monitor and respond to coding agent prompts

Use this workflow when a coding agent pauses and waits for input.

1. Watch the card in **Agent Sessions View** for a bell icon or a **Waiting for input** status.
2. Open that worktree from the card.
3. Switch to the embedded terminal for that agent session.
4. Review the prompt from the coding agent CLI.
5. Respond in the terminal to continue the session.

This workflow is especially useful when you run multiple coding agent sessions at the same time and need to see which session needs attention first.

***

## How to open, review, and manage a coding agent worktree

For general worktree tasks outside coding agents, see [Manage Git Worktrees in GitKraken Desktop](/gitkraken-desktop/worktrees/).

Right-click any card in Agent Sessions View to manage that worktree:

| What you want to do | Action in the card menu | Result |
|---------------------|-------------------------|--------|
| Open the session worktree | **Open this worktree** | Switches to that worktree |
| Open the session in another tab | **Open worktree in a new tab** | Opens the worktree in a new GitKraken tab |
| Prevent the worktree from being pruned, moved, or deleted | **Lock this worktree** | Locks the worktree |
| Re-enable normal worktree management | **Unlock this worktree** | Unlocks the worktree |
| Remove the session worktree | **Remove this worktree** | Deletes the worktree and its working directory |

Use these actions after the agent finishes so you can review changes, push the branch, create a pull request, or clean up the worktree.

***

## Typical workflow for coding agents and worktrees

1. You are working on a feature in your current worktree.
2. A second task comes in, such as a bug fix or a small refactor.
3. You open **Agent Sessions View** and start a new coding agent session on a new branch such as `fix/login-crash`.
4. GitKraken Desktop creates a worktree, runs setup commands, and launches the coding agent CLI.
5. You continue working in your original worktree while monitoring the new agent session card.
6. If the card shows **Waiting for input**, you switch to that session and respond in the terminal.
7. When the agent finishes, you open the worktree, review the diff, and push or open a pull request.
8. After the work is merged or no longer needed, you remove the worktree.

***

## Common questions about coding agents in GitKraken Desktop

### Can I run multiple coding agent sessions at the same time?

Yes. Each coding agent session runs in its own worktree and working directory, so you can run parallel sessions in the same repository.

### What happens when I start a coding agent session?

GitKraken Desktop creates a worktree, checks out the new branch, runs any configured setup commands, and then launches the selected coding agent CLI in the embedded terminal.

### Do Agent Sessions View and List view show different worktrees?

No. They show the same underlying worktrees. The difference is the presentation: List view is branch-focused, and Agent Sessions View is agent-focused.

### Where do I choose Claude Code, Copilot CLI, Codex CLI, Gemini CLI, or OpenCode?

Go to <kbd>Preferences > External Tools > Coding Agent</kbd>. You can also choose a different coding agent in the New Agent Session form for a single session.

### Can I use a coding agent that GitKraken Desktop does not explicitly integrate with?

Yes. GitKraken Desktop explicitly integrates with supported coding agent CLIs such as Claude Code, Codex CLI, Copilot CLI, Gemini CLI, and OpenCode, but you can still run other coding agents manually in the embedded terminal. The agent does not need to appear in the coding agent configuration for you to use that terminal workflow.

### Where do I configure repository setup before the agent starts?

Go to <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>. Setup commands run in sequence in the new worktree before the coding agent launches.
