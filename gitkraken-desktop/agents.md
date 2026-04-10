---
title: Coding Agents in GitKraken Desktop
description: Use the Agents panel in GitKraken Desktop to create, monitor, and manage parallel coding agent sessions across Git worktrees without leaving the app.
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

Use this page to create and monitor coding agent sessions in GitKraken Desktop. The Agents panel lets you spin up a new agent session on any branch, track its progress while you keep working, and act on the results — all from the left panel without switching context.

**Requirements and limits**
- A coding agent CLI must be installed and configured in <kbd>Preferences > External Tools > Coding Agent</kbd>
- Agent sessions each run in their own Git worktree and working directory
- Setup commands (install scripts, build steps) are configured per repository in <kbd>Preferences > Agents</kbd>
- Agent status indicators are available for Claude Code as of version 12.0.0

| Workflow | Supported | Notes |
|----------|-----------|-------|
| Open Agents panel | Yes | Toggle with `List \| Agents` at the top of the left panel |
| Create a new agent session | Yes | Creates a worktree, runs setup commands, and launches the agent |
| Choose base branch per session | Yes | Defaults to HEAD |
| Choose coding agent per session | Yes | Falls back to the agent set in Preferences |
| Monitor session status | Yes | Each card shows WIP changes, ahead/behind, and agent status |
| Configure setup commands | Yes | Per repository in <kbd>Preferences > Agents</kbd> |

***

## Quick Start

**To open the Agents panel:** Click **Agents** in the `List | Agents` segmented control at the top of the left panel.

**To start a new agent session:**
1. Click the dashed **New Agent Session** card at the top of the list.
2. Type a branch name.
3. Optionally set a base branch, choose a coding agent, or click **Configure setup commands**.
4. Click **Start**.

**To monitor sessions:** Each card shows the branch name, WIP change count, ahead/behind status, and agent status. The status bar at the bottom of each card reflects whether the agent is running, waiting for input, or done.

**To act on a session:** Right-click any card to open, push, create a pull request, lock, or remove the worktree.

**To configure the coding agent:** Go to <kbd>Preferences > External Tools > Coding Agent</kbd>.

***

## How the Agents panel works

The Agents panel is toggled by the `List | Agents` segmented control at the top of the left panel. When active, it shows all agents and worktrees for the current repository as cards. The List view and Agents view share the same underlying worktrees — you can switch between them at any time.

<div class='callout callout--basic'>                                                                                                           
      <p><strong>Why Agents instead of worktrees?</strong> The Agents panel surfaces the same underlying Git worktrees as the List view, but organizes them around agent activity — status, progress, and quick actions — rather than branch references. You can switch between views at any time without losing your work.</p>
                                                                                                                  
</div>  

***

## How to start a new agent session

1. In the Agents panel, click the dashed **New Agent Session** card at the top of the list.

   The card expands into an inline creation form with the branch name input focused.

2. Type a branch name.

3. Optionally configure the inline settings:

   | Setting | What it does | Default |
   |---------|-------------|---------|
   | **Base branch** | Which branch to create the new worktree from | HEAD |
   | **Coding agent** | Which agent CLI to launch in the session | Set in Preferences |

   To configure setup commands, click **Configure setup commands** to open <kbd>Preferences > Agents</kbd>.

4. Click **Start**.

GitKraken creates a new worktree from the selected base branch, runs any configured setup commands, and launches the selected coding agent in the embedded terminal. 

***

## How to monitor active sessions

Each card in the Agents panel represents a worktree and shows:

| Card element | What it shows |
|--------------|--------------|
| **Branch name** | The branch checked out in that worktree |
| **WIP change summary** | Count of uncommitted file changes |
| **Ahead / behind** | Commits ahead of and behind the remote |
| **Agent status** | Running, waiting for input, or done |

The status bar at the bottom of each card describes the agent's current status. Status indicators are available for Claude Code as of version 12.0.0.

You can continue working in any other worktree while monitoring agent cards. When a card turns green, switch to it to review the agent's output.

***

## How to act on a session

Right-click any card in the Agents panel to access actions for that worktree:

| Action | What it does |
|--------|-------------|
| **Open this worktree** | Switches to the worktree |
| **Open worktree in a new tab** | Opens the worktree in a new GitKraken tab |
| **Lock this worktree** | Prevents the worktree from being pruned, moved, or deleted |
| **Remove this worktree** | Deletes the worktree and its working directory |

***

## How to configure the coding agent

Go to <kbd>Preferences > External Tools > Coding Agent</kbd> to choose which agent CLI GitKraken launches when starting a new session.

Supported coding agents:
- Claude Code
- Codex CLI
- Copilot CLI
- Gemini CLI
- OpenCode

GitKraken auto-detects installed CLIs. You can also provide custom CLI arguments to pass when starting an agent session.

***

## How to configure setup commands

Setup commands run in the new worktree before the coding agent launches. Use them for steps like installing dependencies or running a build.

Go to <kbd>Preferences > Agents</kbd> to define setup commands per repository.

***

## Typical workflow

1. You are working on a feature in your current worktree (highlighted card in the Agents panel).
2. A bug report comes in. You click **New Agent Session**, type `fix/login-crash`, and press <kbd>Enter</kbd>.
3. A new card appears. GitKraken sets up the worktree and the agent starts.
4. You continue working on your feature. A few minutes later, you glance at the left panel and see the agent has finished its work.
5. You switch to the `fix/login-crash` worktree, review the changes in the diff view, and open a pull request.
6. After the pull request is merged, you right-click the card and remove the worktree.
