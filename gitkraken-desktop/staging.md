---
title: Stage, Unstage, and Ignore Files in GitKraken Desktop
description: Learn how to stage, unstage, discard changes, and manage .gitignore rules when committing in GitKraken Desktop. Includes line-by-line diff staging.
product: GitKraken Desktop
feature: Staging
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
tags: [staging, unstage, gitignore, wip, diff]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-working-with-commits"
    nav_label: "Stage, Unstage, and Ignore Files"
    nav_order: 10
    nav_parent: "desktop-working-with-commits"
    page_type: "content"
    card_icon: "list-check"
    card_color: "green"
    card_description: "Stage, unstage, discard and ignore changes"
---

<kbd>Last updated: November 2026</kbd>

Use this page to stage, unstage, discard, and ignore files in GitKraken Desktop from the Commit Panel and diff view.

**Requirements and limits**
- Workflow scope: Working directory and staged file management from the Commit Panel and diff view
- Starting point: Select the `//WIP` node to work with current uncommitted changes
- Line-level actions: Stage, unstage, and discard selected lines or hunks from the diff view
- Ignore behavior: GitKraken Desktop writes ignore rules to the root-level `.gitignore`
- Ignore limitation: GitKraken Desktop does not read nested `.gitignore` files
- Tracked-file behavior: **Ignore and Stop Tracking** removes the file from the Git index in addition to adding the ignore rule

| Action | Scope | Where to do it | Notes |
|--------|-------|----------------|-------|
| Stage file | Whole file | Commit Panel | Moves the file into Staged Files |
| Unstage file | Whole file | Commit Panel | Returns the file to the working directory |
| Stage selected lines | Partial file | Diff view | Supports line or hunk-level staging |
| Discard changes | Whole file or selected hunk | Commit Panel or diff view | Permanently removes uncommitted changes |
| Ignore | File, extension, or directory | Context menu on unstaged files | Writes to the root-level `.gitignore` |
| Ignore and Stop Tracking | Already tracked file | Context menu on tracked files | Adds ignore rule and removes the file from the Git index |

***

## Quick Start


**To stage files:**
1. Select the **//WIP** node in the Commit Graph to open the Commit Panel.
2. Hover over a file and click **Stage File**, or click **Stage All Changes** to stage everything at once.
3. To stage specific lines, click a file to open its diff, highlight the lines, right-click, and select **Stage selected lines**.

**To unstage files:** Select a file under Staged Files and click **Unstage File**. Click **Unstage All Changes** to move all staged files back to the working directory.

**To discard changes:** Select the **//WIP** node and click the trash icon to discard all changes or the selected files. To discard individual hunks, click a file to open its diff and click **Discard Hunk**.

**To ignore a file:** Right-click any unstaged file and select **Ignore**. Choose to ignore by file name, extension, or directory. GitKraken Desktop adds the rule to the root-level `.gitignore`. For already-tracked files, select **Ignore and Stop Tracking** to also remove the file from the Git index.

***

## How to stage files and changes

Staging prepares your file changes for commit. To begin:

1. Select the <strong>//WIP</strong> node in the Commit Graph to open the Commit Panel.

<figure class='figure center'>
    <img src='/wp-content/uploads/select-WIP-2025.png' class="help-center-img img-bordered" alt="Working directory changes shown in GitKraken Desktop with the //WIP node selected in the commit graph">
    <figcaption style="text-align: center; color: #888;">Select the //WIP node to view your working changes.</figcaption>
</figure>

2. Hover over a file and click <button class='button button--success button--ui button--nolink'>Stage File</button> to stage it.

<figure class='figure center'>
    <img src='/wp-content/uploads/stage-file-2025@2x.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing unstaged files with the 'Stage File' button visible next to markdown.md">
    <figcaption style="text-align: center; color: #888;">Click Stage File on hover.</figcaption>
</figure>

You can also:

- Click <button class='button button--success button--ui button--nolink'>Stage All Changes</button> to stage all files at once
- Click a file to view its diff and selectively stage lines:
  - Highlight lines
  - Right-click and select <kbd>Stage selected lines</kbd>

<figure class='figure center'>
    <img src='/wp-content/uploads/stage-selected-lines-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing 'Stage selected lines' for staging specific changes from the diff view.">
    <figcaption style="text-align: center; color: #888;">Right-click to stage specific lines or hunks.</figcaption>
</figure>

> **Tip:** Use <a href="/gitkraken-desktop/keyboard-shortcuts/#repo-actions">keyboard shortcuts</a> to speed up staging actions.

***

## How to unstage files or lines

To unstage a file:

1. Select the file under the <strong>Staged Files</strong> section
2. Click <button class='button button--danger button--ui button--nolink'>Unstage File</button>

<figure class='figure center'>
    <img src='/wp-content/uploads/unstage-file-2025@2x.png' class="help-center-img img-bordered" alt="The staged files list in GitKraken Desktop showing the Unstage File button for a selected file.">
    <figcaption style="text-align: center; color: #888;">Click Unstage File to move it back to working changes.</figcaption>
</figure>

To unstage lines or hunks, click a staged file to view its diff, then right-click the lines or click **Unstage Hunk**.

<figure class='figure center'>
    <img src='/wp-content/uploads/unstage-hunk-2025.png' class="help-center-img img-bordered" alt="The file diff view in GitKraken Desktop showing the Unstage Hunk option with a pointer from the staged file list.">
    <figcaption style="text-align: center; color: #888;">Unstage specific hunks directly from the diff view.</figcaption>
</figure>

To unstage all files, click <button class='button button--danger button--ui button--nolink'>Unstage All Changes</button>.

***

## How to discard changes

To discard changes across your working directory:

1. Select the <strong>//WIP</strong> node
2. Click the <i class="fa fa-trash-o" aria-hidden="true"></i> trash icon (**Discard all changes**). If you selected files first, it discards only those files.

<figure class='figure center'>
    <img src='/wp-content/uploads/discard-all-changes-2025@2x.png' class="help-center-img img-bordered" alt="Discard all changes button highlighted above a list of unstaged files.">
    <figcaption style="text-align: center; color: #888;">Discard changes for all or multiple selected files.</figcaption>
</figure>

You can also:

- Select 1 or more files, right-click, and select <strong>Discard changes</strong>
- Discard lines or hunks from the file diff, for example with <strong>Discard Hunk</strong>

<figure class='figure center'>
    <img src='/wp-content/uploads/discard-hunk-ex-2025.png' class="help-center-img img-bordered" alt="Discard hunk button highlighted above a section of modified code.">
    <figcaption style="text-align: center; color: #888;">Discard selected hunks of code.</figcaption>
</figure>

***

## How to ignore files

To prevent Git from tracking certain files, add them to a `.gitignore` file.

Right-click a file and select <strong>Ignore</strong>:

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-file@2x.png' class="help-center-img img-bordered" alt="Context menu with Ignore options for a selected file in the Tree view">
    <figcaption style="text-align: center; color: #888;">Choose ignore rules based on file, extension, or folder.</figcaption>
</figure>

You can choose to:

- Ignore the selected file only
- Ignore all files with that extension
- Ignore all files in the directory

GitKraken Desktop adds the rule to the `.gitignore` file at the root of your repository.

> **Note:** GitKraken Desktop uses only the root-level <code>.gitignore</code> file. It does not read nested <code>.gitignore</code> files.

### How to ignore previously tracked files

If the file is already tracked, a prompt offers 2 ways to ignore it:

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-stop-tracking-2025.png' class="help-center-img img-bordered" alt="Dialog with options to ignore, ignore and stop tracking, or cancel for a selected tracked file">
    <figcaption style="text-align: center; color: #888;">Prompt showing options to ignore a file already tracked by Git.</figcaption>
</figure>

<strong>Ignore</strong> adds the entry to the `.gitignore` file, and Git continues to track the file.

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-only@2x.png' class="help-center-img img-bordered" alt="Untracked .gitignore and test.txt files displayed under the obj folder in the Unstaged Files section.">
    <figcaption style="text-align: center; color: #888;">Ignore file but keep it tracked by Git.</figcaption>
</figure>

<strong>Ignore and Stop Tracking</strong> adds the entry and removes the file from the Git index, so Git stops tracking it.

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-untrack@2x.png' class="help-center-img img-bordered" alt=".gitignore file shown as unstaged; test.txt under obj folder shown as staged for removal">
    <figcaption style="text-align: center; color: #888;">Ignore file and remove it from Git tracking.</figcaption>
</figure>

For a file with a merge conflict, the prompt offers only <strong>Ignore</strong>. The same applies when you ignore an extension or a folder that includes a conflicted file. To also stop tracking the file, resolve the conflict first.
