---
title: Manage Git Worktrees in GitKraken Desktop
description: Learn how to create, switch, and manage Git worktrees in GitKraken Desktop to work on multiple branches in parallel.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

Learn how to manage Git worktrees using GitKraken Desktop. Worktrees let you work on multiple branches at the same time, with each in its own working directory.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/grAsFn5yvjA?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## What Are Worktrees?

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

## Using Worktrees in GitKraken Desktop

GitKraken Desktop has supported worktrees since version **10.5.0**. From the Left Panel, you can:

- Create and switch between worktrees
- Remove or lock/unlock worktrees
- Hover over a worktree to see its full file path

### Create a Worktree

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

### Switch Worktrees

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

### Delete a Worktree

To remove a worktree:
1. Right-click it in the Left Panel
2. Select <kbd>Remove this worktree</kbd>

### Lock or Unlock a Worktree

To change lock status:
- Right-click the worktree and choose <kbd>Lock this worktree</kbd> or <kbd>Unlock this worktree</kbd>

Locking a worktree prevents accidental changes while you work elsewhere.
