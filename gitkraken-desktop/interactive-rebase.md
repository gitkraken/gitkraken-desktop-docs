---
title: Interactive Rebase in GitKraken Desktop
description: Step-by-step guide to using interactive rebase in GitKraken Desktop to clean up your Git commit history by picking, squashing, rewording, or dropping commits.
product: GitKraken Desktop
feature: Interactive Rebase
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
tags: [interactive-rebase, history, squash, reword, drop]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to run interactive rebase in GitKraken Desktop when you need to reorder, combine, rename, or drop commits before sharing or merging a branch. It explains how to start the rebase, what the available actions do, and which branch and history conditions must be met before the workflow is available.

**Requirements and limits**
- Workflow scope: Rewrite local branch history before sharing or merging
- Required branch condition: Branches must share a common ancestor
- Rebase limitation: Interactive rebase is not available for merge commits
- Source-branch limitation: No merge commits may exist on the source branch
- Initial-commit limitation: Neither branch may include the repository’s initial commit for this workflow
- Tooling limitation: If you start the rebase in GitKraken Desktop, you must complete it there

***

## Quick Start


**To start interactive rebase:**
- Drag and drop a branch onto a target branch and select **Interactive Rebase**.
- Or right-click a target branch in the Left Panel and choose **Interactive Rebase**.
- Or right-click any parent commit in the graph and select the option.

**Available commit actions:**
- **Pick**: Keep the commit as-is.
- **Reword**: Edit the commit message.
- **Squash**: Combine the commit into its parent commit.
- **Drop**: Remove the commit from history entirely.

Keyboard shortcuts in the rebase view: <kbd>P</kbd> = Pick, <kbd>S</kbd> = Squash, <kbd>R</kbd> = Reword, <kbd>D</kbd> = Drop.

To undo all changes before confirming, click **Reset**. Interactive rebase requires that branches share a common ancestor and that no merge commits exist on the source branch. If you start the rebase in GitKraken Desktop, you must complete it there.

***

## How to start an interactive rebase

To begin:
- Drag and drop one branch onto another
- Or right-click a target branch and select <em class='context-menu'>Interactive Rebase</em>

<figure>
  <img src='/wp-content/uploads/interactive-rebase-init.gif'
       class="help-center-img img-bordered"
       alt="Interactive rebase initiated in GitKraken Desktop by dragging one branch onto another, revealing options including 'Interactive Rebase'">
  <figcaption style="text-align:center; color:#888">
    Start interactive rebase via drag-and-drop or right-click
  </figcaption>
</figure>

You can also right-click any parent commit to access the option. Note: Interactive rebase is not available for merge commits.

### Interactive rebase requirements
Interactive rebase is available only if:
- The branches share a common ancestor
- No merge commits exist on the source branch
- Neither branch includes the repo’s initial commit
- You’re not trying to rebase a parent onto a child (e.g., `main` onto `feature`)

<div class='callout callout--note'>
  <p><strong>Note:</strong> If you start the rebase in GitKraken Desktop, you must complete it there.</p>
</div>

***

## What the interactive rebase actions do

### How Pick works
Moves the commit onto the target branch as-is.

<figure>
  <img src='/wp-content/uploads/pick.gif'
       class="help-center-img img-bordered"
       alt="Interactive rebase in GitKraken Desktop using the 'Pick' action to include each commit as-is">
  <figcaption style="text-align:center; color:#888">
    Pick applies the commit without modifications
  </figcaption>
</figure>

### How Reword works
Opens a modal to edit the commit summary and description.

<figure>
  <img src='/wp-content/uploads/reword.png'
       class="help-center-img img-bordered"
       alt="Interactive rebase in GitKraken Desktop showing the reword option and message editor for updating a commit message">
  <figcaption style="text-align:center; color:#888">
    Reword lets you update the commit message
  </figcaption>
</figure>

### How Squash works
Combines the selected commit into its parent.

<figure>
  <img src='/wp-content/uploads/squash.png'
       class="help-center-img img-bordered"
       alt="Interactive rebase in GitKraken Desktop showing Squash selected for two commits, which will combine into a single commit">
  <figcaption style="text-align:center; color:#888">
    Squash merges the commit into the one above
  </figcaption>
</figure>

### How Drop works
Removes the commit entirely and rewrites the graph.

<figure>
  <img src='/wp-content/uploads/drop.gif'
       class="help-center-img img-bordered"
       alt="Interactive rebase in GitKraken Desktop with one commit marked as Drop, which will remove it from history">
  <figcaption style="text-align:center; color:#888">
    Drop deletes the commit from history
  </figcaption>
</figure>

***

## How shortcuts and Reset work

Use these keyboard shortcuts during rebase:
- <kbd>P</kbd>: Pick
- <kbd>S</kbd>: Squash
- <kbd>R</kbd>: Reword
- <kbd>D</kbd>: Drop

To undo all changes during setup, click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Reset</span></button>.

<figure>
  <img src='/wp-content/uploads/keyboard-shortcut-reset.gif'
       class="help-center-img img-bordered"
       alt="Interactive rebase in GitKraken Desktop showing a user clicking the Reset button to undo changes and restart the rebase process">
  <figcaption style="text-align:center; color:#888">
    Use Reset to cancel changes and start over
  </figcaption>
</figure>
