---
title: Coding Agents in GitKraken Desktop
description: Run Claude Code, Codex CLI, and other coding agents in parallel worktrees with GitKraken Desktop's Agents view, and approve their permission requests.
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
last_verified: 2026-11
llms_include: true
tags: [agents, worktrees, coding-agents, parallel-work, ai, terminal]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-agent-workflows"
    nav_label: "Coding Agents"
    nav_order: 10
    nav_parent: "desktop-agent-workflows"
    page_type: "content"
    card_icon: "robot"
    card_color: "purple"
    card_description: "Run Claude Code, Codex CLI and other agents in the Agents view"
---
<kbd>Last updated: November 2026</kbd>

In GitKraken Desktop, each coding agent session runs on its own branch in its own Git worktree. The agent's changes stay separate from yours and show up in the Commit Graph like any other branch, where you can review them and undo them.

<div style="display:flex; flex-direction:row-reverse; flex-wrap:wrap; align-items:center; gap:8px 32px; margin-bottom:24px;">
  <p style="flex:1 1 300px; margin:0;">Use this page to run external coding agent CLIs, such as Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI, or OpenCode, from inside GitKraken Desktop, and to create, monitor, and manage their sessions in the <strong>Agents view</strong>.</p>
  <img src="/wp-content/uploads/GitKraken_Keif_agents.png" alt="" width="794" height="803" loading="lazy" style="flex:0 0 auto; max-height:200px; width:auto; height:auto; max-width:100%; margin:0 auto;">
</div>

> **Note:** **On-premises note:** Which coding agents you can run depends on your security policy, network access, and the CLIs your organization allows. OpenCode and Gemini CLI can run in fully air-gapped environments when you point them to an internal model endpoint. Claude Code, Codex CLI, Copilot CLI, and Cursor CLI are also supported when your organization permits them and the required services are reachable from your environment.

<figure>
  <img src='/wp-content/uploads/gkd-agents-panel-overview-20260414.png' class="help-center-img img-bordered" alt="GitKraken Desktop with the Agents view open in the Left Panel, showing six worktree cards, two with a Waiting for input status, next to the Commit Graph and a terminal panel running Claude Code.">
  <figcaption style="text-align: center; color: #888">GitKraken Desktop with the Agents view open in the Left Panel, showing worktree cards next to the Commit Graph and a terminal running Claude Code.</figcaption>
</figure>

A **coding agent** is an external CLI that can work on code in a terminal session. In GitKraken Desktop, each **agent session** runs that CLI in its own [**worktree**](/gitkraken-desktop/worktrees/). The **Agents view** shows those worktrees as agent-focused cards so you can start parallel work, monitor progress, and switch back when an agent needs attention.

GitKraken Desktop explicitly integrates with a set of supported coding agent CLIs. You can also run other coding agents manually in the embedded terminal, even if they do not appear in the coding agent configuration.

**Requirements and limits**
- Product: GitKraken Desktop with the Agents view enabled
- Coding agent CLI: Install and configure a supported coding agent CLI in <kbd>Preferences > External Tools > Coding Agent</kbd>
- Session model: Each agent session runs in its own Git worktree and working directory
- Repository setup: Setup commands are configured per repository in <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>
- Live status: Claude Code, Codex CLI, Copilot CLI, and OpenCode can report live session status when you install their status integrations. Cursor CLI can launch sessions but does not report live status in the Agents view.
- View settings: New agent session worktrees inherit hidden refs, hidden remotes, soloed refs and remotes, and collapsed folders and remotes from the source repository
- Other agents: You can still run other coding agents manually in the embedded terminal, even if GitKraken Desktop does not explicitly integrate with or detect them
- On-premises environments: Available coding agents may be limited by your organization's security restrictions, internal approvals, or air-gapped network design

| What you want to do | Supported | Where in GitKraken Desktop | Notes |
|---------------------|-----------|-----------------------------|-------|
| Start a coding agent session | Yes | Agents view, a worktree card's menu, or an issue in Launchpad or the Left Panel | Creates a worktree (when starting a new session), runs setup commands, and launches the coding agent CLI |
| Start multiple coding agent sessions at the same time | Yes | Agents view | Each session runs in a separate worktree. You can also start another agent in a worktree where one is already running |
| Choose a different base branch for a new session | Yes | Start an Agent Session modal | Defaults to the branch you have checked out. The base branch selector is searchable |
| Choose a coding agent CLI for a session | Yes | Start an Agent Session modal | Defaults to the coding agent set in Preferences. Available options depend on the CLIs installed and allowed in your environment |
| Monitor agent progress | Yes | Agents view card | Cards show WIP changes, ahead/behind, and agent status |
| Respond when an agent is waiting for input | Yes | Agents view and embedded terminal | Claude Code, Codex CLI, and Copilot CLI can show permission requests with **Allow once** and **Deny** actions on the card |
| Manage a worktree from the Agents view | Yes | Three-dot action menu on each worktree card | Open, lock or unlock, remove, or remove and delete the local branch, or the local and remote branches |
| Configure coding agent CLIs | Yes | <kbd>Preferences > External Tools > Coding Agent</kbd> | GitKraken Desktop detects installed CLIs automatically. In on-premises environments, the usable CLIs depend on what your organization allows and can reach |
| Configure setup commands for a repository | Yes | <kbd>Preferences > Repo-Specific Preferences > Agents</kbd> | Commands run before the agent launches |
| Search, filter, and sort the worktree list | Yes | Search and **Sort & filter** buttons in the Agents view | Search by branch or folder name, or filter to the worktrees that need attention, have agent sessions, have changes, or have a PR |

***

## Quick start for coding agents in GitKraken Desktop

**To open the Agents view:**
Click **Agents** in the `List | Agents` toggle at the top of the Left Panel.

**To start a coding agent session:**
In the Agents view, click **+ Start *[coding agent]* Session** to choose a branch name, base branch, and coding agent before GitKraken Desktop creates the worktree. The button label shows your default coding agent, such as **Start Claude Code Session**. To start a session immediately with generated defaults, click the lightning-bolt button next to it, **Quick session**.

You can also start an agent session in an existing worktree. In the Agents view, right-click the worktree's card, select **Start Agent Session**, and choose a coding agent.

**To monitor an agent session:**
Review the card for branch name, WIP changes, ahead/behind counts, and agent status. In List view, a status icon on the **Agents** toggle shows the most urgent agent status in the repository.

**To search, filter, or sort agent sessions:**
Use the search and **Sort & filter** buttons at the top of the Agents view to narrow the list when you are running many parallel sessions.

**To respond when an agent is waiting for input:**
Open that worktree or switch to its terminal session and respond there.

**To configure coding agent CLIs:**
Go to <kbd>Preferences > External Tools > Coding Agent</kbd>.

**To configure setup commands for the current repository:**
Go to <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>.

***

## What coding agents, agent sessions, and the Agents view mean

GitKraken Desktop uses these terms for coding agents:

| Term | What it means |
|------|---------------|
| **Coding agent** | An external coding agent CLI such as Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI, or OpenCode |
| **Coding agent session** | A running session of a coding agent CLI started from GitKraken Desktop |
| **Worktree** | A separate Git working directory used for that agent session |
| **Agents view** | The Left Panel view that shows worktrees as agent session cards |
| **List view** | The standard Left Panel view for worktrees and branches |

The Agents view and List view use the same underlying worktrees. The difference is how GitKraken Desktop presents them:

- Use **List view** when you want a branch-focused view.
- Use the **Agents view** when you want an agent-focused view with status and quick actions.

> **Note:** **Why use the Agents view instead of only List view?** The Agents view shows the same worktrees you already use in GitKraken Desktop, but it organizes them around agent activity such as progress, status, and actions. You can switch between <strong>List</strong> and <strong>Agents</strong> at any time without losing work.

***

## How to toggle Agents view

To show or hide the `List | Agents` toggle at the top of the Left Panel, go to <kbd>Preferences > UI Customization</kbd> and toggle the **Show Agents view in left panel** setting.

<figure>
  <img src="/wp-content/uploads/toggle-agents-view-preferences.png" class="help-center-img img-bordered" alt="GitKraken Desktop Preferences showing the UI Customization section with the Show Agents view in left panel setting that controls whether the List and Agents toggle appears in the Left Panel.">
  <figcaption style="text-align:center; color:#888">Enable <code>Show Agents view in left panel</code> to display the <code>List | Agents</code> toggle</figcaption>
</figure>

***

## How to switch to an agent running outside GitKraken Desktop

When you start an agent outside GitKraken Desktop, such as in your own terminal, its session appears as a row on the worktree's card in the Agents view. To bring that agent's window to the front:

1. Switch to **Agents** view in the Left Panel.
2. Hover over the agent's session row.
3. Click the eye icon, **Focus agent application**.

If GitKraken Desktop cannot identify the agent's window, the icon is disabled and its tooltip reads **Cannot focus agent application**. If GitKraken Desktop cannot bring the window to the front, a **Couldn't focus the agent application** message appears. Click **Launch in terminal** in that message to start the same coding agent in the worktree's terminal in GitKraken Desktop instead.

On Linux, bringing a window to the front needs your desktop's window tool, such as `xdotool` on X11, `kdotool` on KDE Plasma (Wayland), or the built-in commands of Hyprland, Sway, or niri.

<figure>
  <img src="/wp-content/uploads/focus-agent-icon.png" class="help-center-img img-bordered" alt="Focusing on an agent from the Left Panel.">
  <figcaption style="text-align:center; color:#888">Focusing on an agent from the Left Panel</figcaption>
</figure>

***

## When to use coding agents in GitKraken Desktop

Use coding agents when you want to:
- Work on multiple tasks in parallel without leaving GitKraken Desktop
- Start a task on a new branch and let a coding agent work in a separate worktree
- Monitor agent progress while you continue working in another worktree
- Review and act on agent-generated changes when the session finishes

A coding agent session is not the best choice when you:
- Need to make a small manual change in your current worktree
- Do not want to create another worktree
- Need behavior that depends on a CLI that is not installed or configured

***

## How to configure coding agent CLIs (Claude Code, Copilot CLI, Cursor CLI, Codex CLI, Gemini CLI, OpenCode)

Go to <kbd>Preferences > External Tools > Coding Agent</kbd> to choose which coding agent CLI GitKraken Desktop launches for new sessions.

GitKraken Desktop explicitly integrates with these supported coding agent CLIs:
- [Claude Code](https://code.claude.com/docs/en/quickstart)
- [Codex CLI](https://developers.openai.com/codex/quickstart)
- [Copilot CLI](https://github.com/features/copilot/cli)
- Cursor CLI
- [Gemini CLI](https://geminicli.com/docs/)
- [OpenCode](https://opencode.ai/download)

GitKraken Desktop detects installed CLIs automatically. If you install `cursor-agent`, Cursor CLI appears in the Coding Agent settings and the agent picker when you start a session. You can also add custom CLI arguments that GitKraken Desktop passes when it starts a coding agent session.

In on-premises environments, do not assume every supported CLI will be available. The list in GitKraken Desktop depends on which CLIs are installed on the machine and which services your organization allows that machine to access.

If you need fully air-gapped agent workflows, OpenCode and Gemini CLI can run against an internal model endpoint. Claude Code, Codex CLI, Copilot CLI, and Cursor CLI are supported when your organization permits them and the required services are available inside your environment.

If you use a different coding agent, you can still open a session worktree and run that agent manually in the embedded terminal. The agent does not need to appear in the coding agent configuration for you to use that terminal workflow.

Setup is the same for every supported CLI: install the CLI on your system, then configure it in <kbd>Preferences > External Tools > Coding Agent</kbd>.

***

## How to configure setup commands for coding agent sessions

Setup commands run in sequence in the new worktree before the coding agent launches. They apply only to the repository you configure them in.

To define setup commands for the current repository, go to <kbd>Preferences > Repo-Specific Preferences > Agents</kbd> and enter each command on its own line. Use setup commands to prepare the repository for the session, for example:

- `npm install`
- `pnpm install`
- `pnpm build`

The same **Agents** pane has the **Show worktree WIP nodes in the graph** checkbox, which is selected by default. While it is selected, the Commit Graph shows a WIP row for every other worktree that has uncommitted changes or an active agent session. Rows with an agent show the agent's logo and current status. Select a row and click **Open Worktree**, or double-click the row, to open that worktree. Unlike the setup commands, this checkbox applies to every repository you open with your current profile.

<figure>
  <img src='/wp-content/uploads/gkd-agents-setup-commands-preferences-20260413-v2@2x.png' class="help-center-img img-bordered" alt="GitKraken Desktop repo-specific Preferences with Agents selected, showing the Show worktree WIP nodes in the graph checkbox and the Setup commands box containing npm install and pnpm build.">
  <figcaption style="text-align: center; color: #888">The Agents pane in Repo-Specific Preferences, with the worktree WIP nodes checkbox and setup commands.</figcaption>
</figure>

***

## How to create a new coding agent session

1. Open the **Agents view** by clicking **Agents** in the Left Panel.
2. Click **+ Start *[coding agent]* Session** to open the setup modal. The button label shows the default coding agent set in your Preferences, such as **Start Claude Code Session**. GitKraken Desktop generates a branch name and selects that coding agent.
3. Review or change the branch name, base branch, and coding agent, then click **Start an Agent Session**. The branch name updates when you change the base branch, and GitKraken Desktop checks it against existing branches and worktrees.

   <figure>
     <img src='/wp-content/uploads/gkd-12-6-agents-new-session-button.png' class="help-center-img img-bordered" alt="Agents view in GitKraken Desktop showing the Start Claude Code Session button with the adjacent lightning-bolt button, the plug icon in the Worktrees header, and two worktree cards, one waiting for input.">
     <figcaption style="text-align: center; color: #888">Open the setup modal or start with generated defaults.</figcaption>
   </figure>

   To start a session without opening the modal, click the lightning-bolt button, **Quick session**, next to **+ Start *[coding agent]* Session**. GitKraken Desktop uses the generated branch name and the coding agent selected in Preferences.

   | Option | Use it to | Default |
   |--------|-----------|---------|
   | **Branch name** | Set a specific branch name for the new worktree | Auto-generated |
   | **Base branch** | Create the new worktree from a different branch. The selector is searchable, so you can type to filter long branch lists | The branch you have checked out |
   | **Coding agent** | Launch a specific coding agent CLI for this session | Coding agent set in Preferences |

   To update repository setup, click **Configure setup commands** to open <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>.

   <figure>
     <img src='/wp-content/uploads/gkd-12-6-agents-start-session-modal.png' class="help-center-img img-bordered" alt="The Start an Agent Session modal in GitKraken Desktop showing a generated branch name, the Base branch selector set to main, and the Coding agent dropdown open with None, Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI, and OpenCode.">
     <figcaption style="text-align: center; color: #888">Set session options before starting an agent.</figcaption>
   </figure>

GitKraken Desktop creates a new worktree from the selected base branch, runs any configured setup commands, and launches the selected coding agent in the embedded terminal. The new worktree inherits hidden refs, hidden remotes, soloed refs and remotes, and collapsed folders and remotes from the source repository, so you do not need to re-hide branches or remotes after starting the session.

### How to start an agent session from a work item

Start an agent session from an issue to create a branch and worktree for that issue and give the agent the issue's details up front. **Start an Agent Session** appears for issues that have no linked branch yet, while the Agents view is turned on. In the Left Panel, it also needs a detected coding agent CLI.

The setup modal has these options:

- **Branch name**: generated from the issue.
- **Base branch**: the branch to create the worktree from.
- **Coding agent**: the CLI to launch.
- **Send issue context to start immediately**: selected by default. The agent starts working right away with the issue's title, status, link, author, assignees, labels, and description. Clear it to start the agent without the issue details. It is unavailable when **Coding agent** is set to **None**.

If a worktree for that branch already exists, GitKraken Desktop uses it. If an agent is already running in that worktree, GitKraken Desktop opens the worktree instead of starting a second agent.

#### Starting from Launchpad view

From Launchpad, go to your Issues view and click **Start an Agent Session**. For an issue with no linked branch, it is the default action button.

The modal shows the issue's **Repository** when Launchpad knows where you cloned it. Otherwise, choose one in **Select repository**. The **Configure setup commands** link does not appear when you start from Launchpad.

   <figure>
     <img src='/wp-content/uploads/GKD-Launching-Agent-Launchpad1.png' class="help-center-img img-bordered" alt="Start an Agent Session">
     <figcaption style="text-align: center; color: #888">Starting an Agent Session from the Launchpad view.</figcaption>
   </figure>

Review or set your **Branch name**, **Base branch**, and **Coding agent**, then click **Start an Agent Session**.

   <figure>
     <img src='/wp-content/uploads/GKD-Launching-Agent-Launchpad2.png' class="help-center-img img-bordered" alt="Session Options">
     <figcaption style="text-align: center; color: #888">Setting Session options.</figcaption>
   </figure>

#### Starting from the Left Panel

From the Left Panel, go to your Issues view, right-click the issue or click the three-dot menu next to it, and click **Start an Agent Session**. The repository you have open is selected by default. If it stays selected, the modal also shows the **Configure setup commands** link.

   <figure>
     <img src='/wp-content/uploads/GKD-Launching-Agent-Sidebar-view1.png' class="help-center-img img-bordered" alt="Start an Agent Session">
     <figcaption style="text-align: center; color: #888">Starting an Agent Session from the Left Panel.</figcaption>
   </figure>

Review or set your **Branch name**, **Base branch**, and **Coding agent**, then click **Start an Agent Session**.

   <figure>
     <img src='/wp-content/uploads/GKD-Launching-Agent-Sidebar-view2.png' class="help-center-img img-bordered" alt="Session Options">
     <figcaption style="text-align: center; color: #888">Setting Session options.</figcaption>
   </figure>

### How to start an agent session from an existing worktree

You can start a coding agent session in a worktree that already exists, without creating a new one:

1. In the Agents view, right-click the worktree's card, or click its three-dot menu.
2. Select **Start Agent Session**, then choose a coding agent.

GitKraken Desktop launches that coding agent in the worktree. If the worktree already has a terminal open, the agent opens in a new terminal tab.

You can start another agent in a worktree where an agent is already running. Each agent gets its own terminal tab and its own session row on the worktree's card.

***

## How to monitor coding agent progress and session status

Each card in the Agents view represents one worktree and lists each coding agent session running in it.

| Card element | What it shows |
|--------------|---------------|
| **Branch name** | The branch checked out in that worktree |
| **Folder name** | The worktree's folder, shown below the branch name only when it differs from the branch |
| **WIP change summary** | The count of uncommitted file changes |
| **Ahead / behind** | Commit counts relative to the remote |
| **Agent status** | One row per agent session, showing its state: **Running**, **Thinking**, **Using tool**, **Awaiting approval**, **Needs response**, **Error**, or **Waiting for input** |
| **Merged PR pill** | Whether the branch has a merged pull request on GitHub, GitLab, Azure DevOps, Bitbucket, or Bitbucket Data Center |

The status row on each card shows the current session state. Claude Code, Codex CLI, Copilot CLI, and OpenCode can report live status when you install their status integrations. If the branch has a merged pull request or merge request on GitHub, GitLab, Azure DevOps, Bitbucket, or Bitbucket Data Center, a merged PR pill appears on the card.

When you start a session, the card shows a **Running** status. If you install a status integration for a supported CLI, the card can show more specific status information.

When an agent needs attention, the card can show a bell icon and a **Waiting for input** label, so you can see that the session needs a response without switching to the terminal first.
<figure>
  <img src='/wp-content/uploads/agent-status.png' class="help-center-img img-bordered" alt="GitKraken Desktop Left Panel in List view, with the pointer over the Agents toggle and a tooltip reading 1 agent session waiting for input.">
  <figcaption style="text-align: center; color: #888">Hover over the Agents toggle to see how many agent sessions are waiting for input.</figcaption>
</figure>
If you remove a worktree from the card menu, the card shows that the removal is in progress until it finishes.

<figure>
  <img src='/wp-content/uploads/GKD-Remove-Session-and-Worktree.png' class="help-center-img img-bordered" alt="Card menu for a worktree in the Agents view showing the Remove this worktree and Remove worktree and delete branch options.">
  <figcaption style="text-align: center; color: #888">Removing a worktree from the card menu in the Agents view.</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/gkd-agents-monitoring-status-20260414.png' class="help-center-img img-bordered" alt="Agents view showing worktree cards with highlighted change counts (+97, a pencil with 91, and -91) and a PR #65 pill, and two cards with a Waiting for input status.">
  <figcaption style="text-align: center; color: #888">Worktree cards in the Agents view show change counts, pull request pills, and agent status.</figcaption>
</figure>

You can keep working in another worktree while monitoring these cards. When a session finishes, switch to that worktree to review the results.

### How to check agent status from List view

You do not need to switch to the Agents view to see whether an agent needs you. When the open repository or any of its worktrees has an agent session, the **Agents** option of the `List | Agents` toggle shows a status icon. The icon matches the most urgent state across those sessions, in this order: **Error**, **Awaiting approval**, **Needs response**, **Using tool**, **Thinking**, **Running**, **Waiting for input**.

Hover over the **Agents** option to see how many sessions are in that state, for example **2 agent sessions awaiting approval**. When there are no agent sessions, the toggle shows only the **Agents** label.

<a id="how-to-respond-to-agent-permission-requests"></a>

### How to approve Claude Code, Codex CLI, and Copilot CLI permission requests

When Claude Code, Codex CLI, or Copilot CLI requests approval for an action, its session row on the card in the Agents view shows the request and the tool the agent wants to use. Respond without switching to the session:

- Click the check mark, **Allow once**, to approve this request only.
- Click the X, **Deny**, to refuse it.
- To see the description and the exact command the agent wants to run, click the request or the chevron, **Toggle permission request details**.

Claude Code can also offer to always allow similar requests. When it offers one option, a double check mark appears next to **Allow once**. Hover over it to see the rule, such as **Always allow: *[rule]***, and click it to approve and save that rule. When Claude Code offers several options, click the ellipsis, **More allow options**, and choose one, such as **Allow all edits during this session**.

For other prompts, open the worktree and respond in the agent's terminal.

<figure>
  <img src='/wp-content/uploads/allow-deny.png' class="help-center-img img-bordered" alt="Agents view showing Agent permission request">
  <figcaption style="text-align: center; color: #888">The Agents view allows you to approve agent permission requests directly from the view without switching to the session.</figcaption>
</figure>

### How to search, filter, and sort agent sessions

Use the buttons in the **Worktrees** header of the Agents view to manage large groups of parallel sessions.

**To search:** Click the magnifier icon and type in **Search worktrees...**. The list shows worktrees whose branch name or folder name matches. If nothing matches, the list shows **No matching worktrees**.

**To filter or sort:** Click **Sort & filter** and choose from these options:

| Option | What it does |
|--------|--------------|
| **Sort** | Order the list by **None**, **Alphabetical**, **Status** (most urgent agent status first), or **Change size** (most changes first) |
| **Needs attention** | Show worktrees with an agent session that is in **Error**, **Awaiting approval**, or **Needs response** |
| **Has agent sessions** | Show worktrees with at least one agent session |
| **Has changes** | Show worktrees with uncommitted changes or commits ahead of or behind the remote |
| **Has PR** | Show worktrees whose branch has a pull request |
| **Current** | Show the worktree you have open |
| **Clear all** | Reset sorting and remove all filters |

When you select several filters, the list shows only worktrees that match all of them. While you search or filter, the count in the header shows the number of worktrees shown out of the total, such as `3 / 8`.

These controls affect only how sessions appear in the Agents view. They do not change the underlying worktrees or sessions.

***

## How to monitor and respond to coding agent prompts

Use this workflow when a coding agent pauses for input that you cannot answer from its card.

1. Watch the card in the **Agents view** for a bell icon or a **Waiting for input** status.
2. Open that worktree from the card.
3. Switch to the embedded terminal for that agent session.
4. Review the prompt from the coding agent CLI.
5. Respond in the terminal to continue the session.

***

## How to open, review, and manage a coding agent worktree

For general worktree tasks outside coding agents, see [Manage Git Worktrees in GitKraken Desktop](/gitkraken-desktop/worktrees/).

Each worktree card in the Agents view has a three-dot action menu so you can manage that worktree without leaving the Agents view. Right-click the card or open the three-dot menu to see the available actions:

| What you want to do | Action in the card menu | Result |
|---------------------|-------------------------|--------|
| Start a coding agent in the worktree | **Start Agent Session**, then a coding agent | Launches that agent in the worktree, even if another agent is already running there |
| Open the session worktree | **Open this worktree** | Switches to that worktree |
| Open the session in another tab | **Open worktree in new tab** | Opens the worktree in a new tab |
| Prevent the worktree from being pruned, moved, or deleted | **Lock this worktree** | Locks the worktree |
| Re-enable normal worktree management | **Unlock this worktree** | Unlocks the worktree |
| Remove the session worktree | **Remove this worktree** | Deletes the worktree and its working directory |
| Remove the worktree and delete its branch in one step | **Remove worktree and delete branch** | Deletes the worktree and its local branch |
| Remove the worktree and delete its branch on the remote too | **Remove worktree and delete branch (local & remote)** | Deletes the worktree, its local branch, and the remote branch. Appears only when the branch has a remote branch |

You can also reach the removal options from the branch itself. When you right-click a branch that is checked out in another worktree, in the Commit Graph or the Left Panel, the menu shows **Remove this worktree** and **Remove worktree and delete branch** instead of the delete option.

Use these actions after the agent finishes so you can review changes, push the branch, create a pull request, or clean up the worktree. For what each removal option deletes, see [Clean Up AI Coding Agent Worktrees and Branches](/gitkraken-desktop/clean-up-agent-worktrees/). To see exactly what the agent changed and undo any of it, see [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/).

***

## How to manage agent status plugins and hooks

GitKraken Desktop uses a status plugin for each supported agent to report live status in the Agents view. Installing a plugin changes that agent's configuration, so GitKraken Desktop installs it only when you request it. The plugins send only event metadata. Prompt content, agent output, and source code are never sent to GitKraken.

To check which agents can report live status or install an integration:

1. Open the **Agents view** in the Left Panel.
2. Hover over the plug icon in the panel header to see how many detected agents have status available. The icon appears only when GitKraken Desktop detects a supported agent CLI, and it is highlighted when a detected agent is not reporting status. Click the icon to open **Agent plugins**, which lists each detected agent as **Status available**, **Status not available**, or **Status unknown**.

   <figure>
     <img src='/wp-content/uploads/gkd-12-6-agents-status-plugin-tooltip.png' class="help-center-img img-bordered" alt="Agents view in GitKraken Desktop with the plug icon in the Worktrees header highlighted and its tooltip reading Agent plugins: 1 of 2 agents have status available.">
     <figcaption style="text-align: center; color: #888">Hover over the plug icon to see how many agents can report live status.</figcaption>
   </figure>

3. Select **Install** or **Reinstall** next to an agent, or click **Manage in Preferences** to open <kbd>Preferences > External Tools</kbd>. To uninstall a plugin, use <kbd>Preferences > External Tools</kbd>.

In <kbd>Preferences > External Tools</kbd>, the **Agent Status Integrations** section lists a plugin for each supported agent. The buttons next to each agent show whether its plugin is installed:

- **Install Plugin**: the plugin is not installed.
- **Reinstall Plugin** and **Uninstall Plugin**: the plugin is installed.
- **Install/Reinstall Plugin**, with the message **Unable to verify plugin status.**: GitKraken Desktop could not check whether the plugin is installed. You can still install or reinstall it.

<figure>
  <img src='/wp-content/uploads/gkd-12-6-preferences-agent-status-integrations.png' class="help-center-img img-bordered" alt="The External Tools tab in GitKraken Desktop Preferences showing the Coding Agent setting and the Agent Status Integrations section, with Reinstall Plugin and Uninstall Plugin buttons for the Claude Code, Codex, Copilot CLI, and OpenCode plugins.">
  <figcaption style="text-align: center; color: #888">Manage agent status plugins in Preferences > External Tools.</figcaption>
</figure>

GitKraken Desktop keeps installed plugins up to date when you update the app. You can uninstall them from <kbd>Preferences > External Tools</kbd>.

### Copilot CLI status plugin and permission requests

Install the **Copilot CLI Plugin** from <kbd>Preferences > External Tools</kbd> to show Copilot CLI session status and permission requests in the Agents view. You can also install or reinstall the plugin from the plug icon in the Agents view. To uninstall it, use <kbd>Preferences > External Tools</kbd>.

When Copilot CLI requests permission, select **Allow once** or **Deny** on its worktree card. If you dismiss the request without choosing either action, Copilot CLI asks you in its own prompt instead.

### Claude Code status hooks

The Claude Code plugin adds hooks to Claude Code so that the Agents view can show its status as the session starts and ends, uses tools, receives prompts, and requests permission.

#### Reinstalling or uninstalling the Claude Code plugin

1. Open **Preferences**.
2. Navigate to the **External Tools** tab.
3. In the **Agent Status Integrations** area, next to **Claude Code Plugin**, click **Reinstall Plugin** or **Uninstall Plugin**. If the plugin is not installed, click **Install Plugin**. If the area shows **Install/Reinstall Plugin**, GitKraken Desktop could not verify the plugin's status, and that button installs or reinstalls it.

### OpenCode status plugin

GitKraken Desktop uses an OpenCode plugin to report live agent status for OpenCode sessions.

Use the plug icon in the Agents view or open <kbd>Preferences > External Tools</kbd> to install or reinstall the OpenCode plugin. To uninstall it, use <kbd>Preferences > External Tools</kbd>.

***

## Typical workflow for coding agents and worktrees

Suppose you are working on a feature in your current worktree when a second task comes in, such as a bug fix or a small refactor:

1. Open the **Agents view** and start a new coding agent session on a new branch, such as `fix/login-crash`. GitKraken Desktop creates a worktree, runs setup commands, and launches the coding agent CLI.
2. Keep working in your original worktree while you monitor the new agent session card.
3. If the card shows **Waiting for input**, switch to that session and respond in the terminal.
4. When the agent finishes, open the worktree, review the diff, and push or open a pull request.
5. After the work is merged or no longer needed, remove the worktree.

***

## Common questions about coding agents in GitKraken Desktop

Answers to frequent questions about running coding agents in GitKraken Desktop.

### Can I run multiple coding agent sessions at the same time?

Yes. Each coding agent session runs in its own worktree and working directory, so you can run parallel sessions in the same repository.

### Can I approve Claude Code permission prompts without leaving my Git history?

Yes. Select **Allow once** or **Deny** on the agent's card in the Agents view, next to your Commit Graph, without switching to the agent's terminal. This also works for Codex CLI and Copilot CLI. See [How to approve permission requests](#how-to-respond-to-agent-permission-requests).

### How do I review, clean up, and combine work from several agents?

See [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/), [Clean Up AI Coding Agent Commits Before Review](/gitkraken-desktop/clean-up-agent-commits/), and [Resolve Merge Conflicts Between AI Agent Branches](/gitkraken-desktop/agent-merge-conflicts/). To remove the worktrees and branches afterward, see [Clean Up AI Coding Agent Worktrees and Branches](/gitkraken-desktop/clean-up-agent-worktrees/).

### What happens when I start a coding agent session?

GitKraken Desktop creates a worktree, checks out the new branch, runs any configured setup commands, and then launches the selected coding agent CLI in the embedded terminal.

### Do the Agents view and List view show different worktrees?

No. They show the same underlying worktrees. The difference is the presentation: List view is branch-focused, and the Agents view is agent-focused.

### Where do I choose Claude Code, Copilot CLI, Cursor CLI, Codex CLI, Gemini CLI, or OpenCode?

Go to <kbd>Preferences > External Tools > Coding Agent</kbd>. You can also choose a different coding agent for one session in the Start an Agent Session modal.

### Are all supported coding agents available in on-premises environments?

No. In on-premises environments, available coding agents depend on your organization's security policy, network restrictions, and approved tools.

OpenCode and Gemini CLI can run in fully air-gapped environments when they are configured to use an internal model endpoint. Claude Code, Codex CLI, Copilot CLI, and Cursor CLI are also supported when your organization permits them and the required services are reachable.

### Can I use a coding agent that GitKraken Desktop does not explicitly integrate with?

Yes. GitKraken Desktop explicitly integrates with supported coding agent CLIs such as Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI, and OpenCode, but you can still run other coding agents manually in the embedded terminal. The agent does not need to appear in the coding agent configuration for you to use that terminal workflow. In on-premises environments, use this manual path for internally approved tools that are not part of the built-in list.

### Where do I configure repository setup before the agent starts?

Go to <kbd>Preferences > Repo-Specific Preferences > Agents</kbd>. Setup commands run in sequence in the new worktree before the coding agent launches.

### Why does GitKraken install hooks or plugins for agent status?

GitKraken Desktop uses hooks or plugins to receive agent status events, such as when an agent starts, finishes, or changes state, and shows that status in the Agents view. GitKraken Desktop installs a plugin only when you request it and updates installed plugins when you update the app. The plugins send only status metadata. They do not send prompt content, agent responses, or source code.
