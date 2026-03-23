---
title: Cherry Pick Commits in GitKraken Desktop
description: Learn how to cherry pick single or multiple commits across branches in GitKraken Desktop, including using the interactive cherry-pick tool.
product: GitKraken Desktop
feature: Cherry Pick
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
tags: [cherry-pick, commits, branches, interactive, history]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to cherry pick one or more commits onto your current branch in GitKraken Desktop when you need selected changes without merging an entire branch. It covers single-commit cherry picks, multi-commit interactive cherry pick, and the reorder, squash, reword, and drop actions available before applying changes.

***

## Quick Start


**To cherry pick a single commit:**
1. Check out the branch where you want to apply the commit.
2. Right-click the commit in the Commit Graph.
3. Select **Cherry pick commit**.

**To cherry pick multiple commits:**
1. Hold <kbd>Cmd</kbd> (Mac) or <kbd>Ctrl</kbd> (Windows/Linux), or use <kbd>Shift</kbd>, to select multiple commits in the graph.
2. Right-click one of the selected commits.
3. Select **Cherry pick X commits**.

The interactive cherry-pick tool opens, where you can reorder commits by dragging, squash child commits into parents, reword commit messages, or drop commits before applying. Use keyboard shortcuts in the interactive view: <kbd>P</kbd> to pick, <kbd>S</kbd> to squash, <kbd>R</kbd> to reword, and <kbd>D</kbd> to drop. Click **Reset** to abandon the session without applying changes.

***

## How to cherry pick a single commit

1. Check out the branch where you want to apply the commit.
2. Right-click the commit in the graph.
3. Select **Cherry pick commit**.

<figure class='figure center'>
    <img src='/wp-content/uploads/cherrypick@2x.png' class="help-center-img img-bordered" alt="Right-click context menu in GitKraken showing option to cherry pick a commit.">
    <figcaption style="text-align: center; color: #888;">Check out the target branch, then right-click a commit to cherry pick it.</figcaption>
</figure>

You can also cherry pick the HEAD commit of a branch by right-clicking a branch name under the **Local** section of the Left Panel.

<figure class='figure center'>
  <img src='/wp-content/uploads/cherrypick-left-panel@2x.png' class="help-center-img img-bordered" alt="Context menu in GitKraken showing option to cherry pick the HEAD commit of a selected branch from the Left Panel.">
  <figcaption style="text-align: center; color: #888;">Right-click a branch in the Left Panel to cherry pick its HEAD commit.</figcaption>
</figure>

***

## How to cherry pick multiple commits

1. Hold <kbd>Cmd</kbd> (Mac) or <kbd>Ctrl</kbd> (Windows/Linux) or <kbd>Shift</kbd> and click multiple commits.
2. Right-click one of the selected commits.
3. Choose **Cherry pick X commits**.

<figure class='figure center'>
  <img src='/wp-content/uploads/multi-cherry-pick-menu.png' class="help-center-img img-bordered" alt="GitKraken Desktop context menu showing 'Cherry pick 5 commits' after selecting multiple commits from the commit graph.">
  <figcaption style="text-align: center; color: #888;">Select a range of commits with Shift or Cmd/Ctrl and right-click to cherry pick.</figcaption>
</figure>

This opens the interactive cherry pick tool where you can:

- **Reorder** commits with drag-and-drop
- **Squash** commits
- **Reword** commit messages
- **Drop** a commit

<figure class='figure center'>
  <img src='/wp-content/uploads/interactive-cherry-pick.png' class="help-center-img img-bordered" alt="GitKraken Interactive Cherry Pick panel showing selected commits with a Reword option and an editable commit message field.">
  <figcaption style="text-align: center; color: #888;">Use the interactive tool to modify selected commits before applying them.</figcaption>
</figure>

***

## What the interactive cherry-pick actions do

- **Pick**: Apply the commit as-is to the target branch.
- **Reword**: Edit the commit summary and description.
- **Squash**: Combine a child commit into its parent (requires a parent-child relationship).
- **Drop**: Remove a commit from the list.

Use keyboard shortcuts to manage commits in the interactive view:

<kbd>P</kbd> = Pick <kbd>S</kbd> = Squash <kbd>R</kbd> = Reword <kbd>D</kbd> = Drop

To abandon the cherry-pick session, click: <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Reset</span></button>

***

## Learn more about cherry pick

<p class="small">
    <a href="https://gitkraken.com/learn/git/tutorials/cherry-pick?product=gitkraken&source=help_center" target="_blank">Cherry Pick Tutorial</a> | <a href="https://gitkraken.com/learn/git/cherry-pick?product=gitkraken&source=help_center" target="_blank">Learn Git: What is Cherry Pick?</a>
</p>
