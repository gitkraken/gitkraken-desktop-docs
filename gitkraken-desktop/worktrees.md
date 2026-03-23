---
title: Manage Git Worktrees in GitKraken Desktop
description: Learn how to create, switch, and manage Git worktrees in GitKraken Desktop to work on multiple branches in parallel.
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
last_verified: 2026-03
llms_include: true
tags: [worktrees, branches, parallel-work, repositories, checkout]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to create, switch, lock, and remove Git worktrees in GitKraken Desktop when you need multiple branches checked out at the same time. Worktrees keep separate working directories while sharing the same repository history, which makes them useful for parallel feature work, testing, and review workflows.

**Requirements and limits**
- GitKraken Desktop version: Worktrees are supported in version 10.5.0 and later
- Worktree model: Each worktree has its own working directory and index but shares repository history with the main repo
- Change visibility: Once committed, changes made in one worktree become visible in other worktrees
- Lock behavior: Locking a worktree prevents accidental changes while you work elsewhere
- Removal behavior: Removing a worktree detaches that working directory from the repo via the Left Panel workflow
- Best fit: Use worktrees when you need multiple branches checked out simultaneously instead of repeatedly switching one working directory

***

## Quick Start

Create and manage Git worktrees in GitKraken Desktop to work on multiple branches simultaneously, each in its own working directory.

**To create a worktree:**
1. Right-click a branch in the Repository View.
2. Select **Create worktree**.

**To switch between worktrees:** Right-click a worktree in the Left Panel and choose **Open this worktree**, or check out the corresponding branch from the Repository View.

**To remove a worktree:** Right-click it in the Left Panel and select **Remove this worktree**.

**To lock or unlock a worktree:** Right-click the worktree and choose **Lock this worktree** or **Unlock this worktree**. Locking prevents accidental changes while you work in another worktree.

Worktrees share Git history with the main repository. Changes committed in one worktree are visible in others. Hover over a worktree in the Left Panel to see its full file path. Worktrees are supported in GitKraken Desktop 10.5.0 and later.

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

***

## How to use worktrees in GitKraken Desktop

GitKraken Desktop has supported worktrees since version **10.5.0**. From the Left Panel, you can:

- Create and switch between worktrees
- Remove or lock/unlock worktrees
- Hover over a worktree to see its full file path

### How to create a worktree

To create a worktree:
1. Right-click a branch in the Repository View
2. Select <kbd>Create worktree</kbd>

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
1. Right-click it in the Left Panel
2. Select <kbd>Remove this worktree</kbd>

### How to lock or unlock a worktree

To change lock status:
- Right-click the worktree and choose <kbd>Lock this worktree</kbd> or <kbd>Unlock this worktree</kbd>

Locking a worktree prevents accidental changes while you work elsewhere.
