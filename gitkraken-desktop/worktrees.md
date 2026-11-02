---
title: Manage Git Worktrees in GitKraken Desktop
description: Create, switch, and manage Git worktrees in GitKraken Desktop to work on several branches in parallel, including branches where coding agents run.
product: GitKraken Desktop
feature: Worktrees
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
tags: [worktrees, branches, parallel-work, repositories, checkout]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to create, switch, lock, and remove Git worktrees in GitKraken Desktop when you need multiple branches checked out at the same time. Worktrees keep separate working directories while sharing the same repository history, which makes them useful for parallel feature work, testing, review workflows, and coding agent sessions.

If you use coding agents in GitKraken Desktop, the Agents view works with the same worktrees. See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/) for agent-specific setup, session management, and status details.

**Requirements and limits**
- GitKraken Desktop version: Worktrees are supported in version 10.5.0 and later
- Worktree model: Each worktree has its own working directory and index but shares repository history with the main repo
- Change visibility: Once committed, changes made in one worktree become visible in other worktrees
- Lock behavior: Locking a worktree prevents accidental changes while you work elsewhere
- Removal behavior: Removing a worktree from the Left Panel detaches that working directory from the repository
- Best fit: Use worktrees when you need multiple branches checked out simultaneously instead of repeatedly switching one working directory

| Action | What it does | Affects shared history | Notes |
|--------|--------------|------------------------|-------|
| Create worktree | Creates another working directory for a branch | No | Requires GitKraken Desktop 10.5.0 or later. New worktrees inherit hidden refs, hidden remotes, soloed refs and remotes, and collapsed folders and remotes from the source repository |
| Open worktree | Switches you into that working directory | No | Available from the Left Panel |
| Lock worktree | Prevents accidental changes to that worktree | No | Useful when working elsewhere temporarily |
| Remove worktree | Detaches that working directory from the repository | No | Removes the worktree entry, not shared history |
| Remove worktree and delete branch | Removes the worktree and deletes its associated branch in one step | No | Available from the worktree context menu in the Left Panel and from the branch's context menu. If the branch has an upstream, **Remove worktree and delete branch (local & remote)** also deletes the remote branch |
| View worktrees through the Agents view | Shows the same worktrees in an agent-focused interface | No | Adds coding agent session context, quick actions, and a merged PR pill when the branch has a merged pull request on GitHub, GitLab, Azure DevOps, Bitbucket, or Bitbucket Data Center |
| Commit in a worktree | Records history from that worktree | Yes | Committed changes become visible across all worktrees |

***

## Quick Start


**To create a worktree:**
1. Right-click a branch in the Repository View.
2. Select **Create worktree from** followed by the branch name.

**To switch between worktrees:** Right-click a worktree in the Left Panel and choose **Open this worktree**, or check out the corresponding branch from the Repository View. To open the worktree in a separate tab instead, choose **Open worktree in new tab**. Tabs for a repository and its worktrees are grouped together in the tab bar. See [Worktree tab groups](/gitkraken-desktop/interface/#worktree-tab-groups).

**To remove a worktree:** Right-click it in the Left Panel and select **Remove this worktree**. To remove the worktree and delete its associated branch in one step, choose **Remove worktree and delete branch**.

**To lock or unlock a worktree:** Right-click the worktree and choose **Lock this worktree** or **Unlock this worktree**. Locking prevents accidental changes while you work in another worktree.

Worktrees share Git history with the main repository, so changes committed in one worktree are visible in the others. When the worktree folder name differs from its checked-out branch, GitKraken Desktop shows the folder name below the branch in the Left Panel and the Agents view. Search in either list matches both names. To see the full file path of a worktree, hover over it in the Left Panel.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/grAsFn5yvjA?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## What Git worktrees are

A Git worktree is a linked working copy of your repository. Each worktree:

- Has its own working directory and index
- Shares Git history with the main repository
- Lets you keep different branches checked out simultaneously

Worktrees are useful when you want to:

- Work on multiple features or fixes without switching branches
- Build or test alternate versions of your code
- Experiment safely while keeping your main branch clean
- Review pull requests without halting other work

Once committed, changes in one worktree become visible in others.

<div class='callout callout--basic'>
  <p><strong>Using coding agents?</strong> The Agents view in GitKraken Desktop runs each agent session in its own Git worktree. If you want to run Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI, or OpenCode in GitKraken Desktop, see <a href="/gitkraken-desktop/agents/">Coding Agents in GitKraken Desktop</a>.</p>
</div>

***

## How to use worktrees in GitKraken Desktop

In the Left Panel, you can work with worktrees in 2 views:

- **List view** for general branch and worktree management
- **Agents view** for coding agent sessions that run in worktrees

Both views show the same worktrees:

- Use **List view** when you want to create, switch, lock, or remove worktrees directly
- Use the **Agents view** when you want to create, monitor, and manage coding agent sessions in worktrees

From the Left Panel, you can:

- Create and switch between worktrees
- Remove or lock/unlock worktrees
- See the folder name below the branch when the names differ, and search by either name
- Hover over a worktree to see its full file path

See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/) if you want to:

- Install and use a supported coding agent CLI
- Start a coding agent session in a new worktree
- Monitor agent status such as **Waiting for input**
- Manage agent sessions from the Agents view

### How to create a worktree

To create a worktree:
1. Right-click a branch in the Repository View.
2. Select <kbd>Create worktree from</kbd> followed by the branch name.

New worktrees inherit view settings from the source repository, including hidden refs, hidden remotes, soloed refs and remotes, and collapsed folders and remotes, so you do not need to hide branches or remotes again.

<figure>
  <img src="/wp-content/uploads/gkd-10-5-create-worktree.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop context menu showing the option to create a worktree from the branch updates-10-4, with the branch 10-5-updates currently checked out.">
  <figcaption style="text-align:center; color:#888">
    Create a new worktree from any branch
  </figcaption>
</figure>

### How to switch worktrees

To switch to another worktree:
- Right-click the desired worktree in the Left Panel and choose <kbd>Open this worktree</kbd>
- If the worktree has a WIP row in the Commit Graph, select that row and click **Open Worktree**, or double-click the row. Each worktree WIP row shows the branch the worktree is on, such as *on feature/login-form*, or the commit SHA if the worktree is on a detached HEAD

  <figure>
    <img src="/wp-content/uploads/gkd-open-worktree-from-wip-01-v2@2x.png" 
         class="help-center-img img-bordered" 
         alt="Commit Graph rows with three worktree WIP rows, labeled &quot;on feature/login-form&quot;, &quot;on fix/readme-typo&quot; and &quot;on 4d9484&quot;, each showing its change counts. The selected feature/login-form row shows the Open Worktree button.">
    <figcaption style="text-align:center; color:#888">
      Opening a worktree from its WIP node in the commit graph
    </figcaption>
  </figure>

- Right-click the desired worktree in the Left Panel and choose <kbd>Open worktree in new tab</kbd> to open it in a separate tab instead of replacing the current one
- Or check out the corresponding branch from the Repository View

<figure>
  <img src="/wp-content/uploads/gkd-10-5-worktrees-actions.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop worktree context menu with options to open, remove, or lock the selected worktree named 10-4-1-updates.">
  <figcaption style="text-align:center; color:#888">
    Switch between worktrees from the Left Panel
  </figcaption>
</figure>

### How to remove a worktree

To remove a worktree:
1. Right-click it in the Left Panel.
2. Select <kbd>Remove this worktree</kbd>.

To remove a worktree and delete its associated branch in a single step:
1. Right-click the worktree in the Left Panel.
2. Select <kbd>Remove worktree and delete branch</kbd>.

Use this option when you are done with the worktree and no longer need its branch, for example after merging a feature or finishing a coding agent session. It deletes the local branch even if its commits are not merged, and you cannot undo it.

If the branch has an upstream, the worktree context menu also offers <kbd>Remove worktree and delete branch (local & remote)</kbd>, which deletes the remote branch as well. GitKraken Desktop asks you to confirm, then removes the worktree first. If the worktree cannot be removed, no branch is deleted.

You can also start from the branch. A branch checked out in a worktree has no **Delete** option in its context menu in the Commit Graph or Left Panel. Instead, right-click the branch and select <kbd>Remove this worktree</kbd> or <kbd>Remove worktree and delete branch</kbd>.

### How to lock or unlock a worktree

To change lock status:
- Right-click the worktree and choose <kbd>Lock this worktree</kbd> or <kbd>Unlock this worktree</kbd>

Locking a worktree prevents accidental changes while you work elsewhere.

<div class='callout callout--basic'>
  <p><strong>Tip:</strong> A merged PR pill on a worktree card in the Agents view means the branch has a merged pull request on GitHub, GitLab, Azure DevOps, Bitbucket, or Bitbucket Data Center. Use this as a signal that it is safe to remove the worktree and delete the branch. See <a href="/gitkraken-desktop/clean-up-agent-worktrees/">Clean Up AI Coding Agent Worktrees and Branches</a>.</p>
</div>

## Multiple WIP nodes for multiple worktrees

The Commit Graph shows a separate WIP row for every other worktree that has uncommitted changes or an active coding agent session. Each row appears just above the commit that worktree is on and shows the branch it is on.

- A row without an agent shows **// WIP** and the worktree's change counts.
- A row with an active agent session shows the agent's logo and a status pill, such as **Running**, **Thinking**, or **Using Tool**.

These rows only open the worktree. Selecting one does not open the Commit Panel, and the row has no context menu. To stage, commit, or review the files, select the row and click **Open Worktree**, or double-click the row.

To hide these rows, open <kbd>Preferences</kbd>, select **Agents** under **Repo-Specific Preferences**, and clear **Show worktree WIP nodes in the graph**. The setting is on by default.

<figure>
  <img src="/wp-content/uploads/multiple-WIP-nodes.png" 
       class="help-center-img img-bordered" 
       alt="Commit graph showing a separate WIP node for each of several worktrees with pending changes.">
  <figcaption style="text-align:center; color:#888">
    Each worktree gets its own WIP node in the commit graph
  </figcaption>
</figure>

When you start a coding agent session from the [Agents view](/gitkraken-desktop/agents/), GitKraken Desktop creates the branch and worktree for you, so each agent's pending changes appear in their own WIP row. To review or undo them, see [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/).
