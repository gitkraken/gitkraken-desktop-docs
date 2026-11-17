---
title: How to Stash Changes in GitKraken Desktop
description: Save and manage your uncommitted changes with stashing in GitKraken Desktop. Learn to stash, pop, name, edit, and apply partial stashes using the GUI.
product: GitKraken Desktop
feature: Stashing
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
tags: [stash, pop, apply, work-in-progress, partial-stash]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to stash, apply, pop, rename, and partially restore uncommitted changes in GitKraken Desktop when you need to switch context without creating a commit. You can stash all your changes or only selected files, and manage your stashes from the Commit Graph or the Left Panel.

**Requirements and limits**
- Workflow scope: Uncommitted local changes only
- Submodule limitation: Changes inside a submodule, a submodule checked out at another commit, and folders that hold their own Git repository are not stashed. Commit or stash those changes from the submodule itself
- Apply vs. pop: **Apply Stash** keeps the stash; **Pop Stash** applies it and removes it
- Partial stash behavior: Applying a single file from a partial stash does not remove the stash
- Naming option: Name the stash before creating it in the WIP node's `// WIP` field or the **Stash title** field in the Commit Panel
- GitKraken AI note: AI-generated stash messages require GitKraken AI to be enabled
- Stash visibility: Stashes can be hidden from the graph without being deleted

| Action | What it does | Keeps stash entry | Notes |
|--------|--------------|-------------------|-------|
| Stash | Saves current uncommitted changes | Yes | Creates a new stash entry |
| Apply Stash | Restores stashed changes | Yes | Keeps the stash for reuse |
| Pop Stash | Restores stashed changes | No | Applies and removes the stash |
| Partial stash | Saves selected files only | Yes | Created from staged or unstaged files in the Commit Panel |
| Apply partial stash file | Restores one file from a partial stash | Yes | Does not remove the stash |
| Hide stash | Removes stash from graph view only | Yes | Does not delete the stash |

***

## Quick Start


**To stash all changes:** Click the **Stash** icon in the top toolbar. Your stash appears in the Commit Graph.

**To manage a stash:** Right-click the stash node in the graph to apply, pop, delete, or hide it. Right-click a stash in the Left Panel for the same options.

**To pop the latest stash:** Click the **Pop Stash** button in the toolbar to apply changes and delete the stash in one step.

**To name a stash:** Type a name in the WIP node's `// WIP` field in the Commit Graph, then click **Stash**.

**To stash specific files (partial stash):** In the Commit Panel, right-click a staged or unstaged file and select **Stash file**.

**To apply a partial stash file by file:** Select the stash in the graph, then right-click a file in the Commit Panel and select **Apply stashed file**. Applying a single file does not remove the stash.

***

<a name="stashing-files"></a>

## How to stash changes from the top toolbar

Click the **Stash** icon in the top toolbar to create a new stash.

If your only changes are inside submodules or in folders that hold their own Git repository, GitKraken Desktop shows **Nothing to stash** and does not create a stash. Open the submodule to commit or stash its changes there.

<figure>
  <img src='/wp-content/uploads/stash@2x.png' class="help-center-img img-bordered" alt="GitKraken top toolbar with Stash button highlighted">
  <figcaption style="text-align:center; color:#888">Create a stash from the top toolbar.</figcaption>
</figure>

Your stash appears in the Commit Graph. Right-click the stash node to see these options:

* **Apply Stash**: Apply changes to your working directory and keep the stash.
* **Pop Stash**: Apply changes and remove the stash.
* **Delete Stash**: Permanently remove the stash.
* **Hide**: Hide the stash from the graph.

To hide or show every stash at once, right-click the **STASHES** header in the Left Panel and select **Hide all stashes** or **Show all stashes**.

<figure>
  <img src='/wp-content/uploads/stash-options@2x.png' class="help-center-img img-bordered" alt="Right-click stash options menu in GitKraken Desktop showing Apply, Pop, Delete, and visibility controls">
  <figcaption style="text-align:center; color:#888">Right-click a stash to manage it.</figcaption>
</figure>

To quickly pop the latest stash, use the **Pop Stash** button:

<figure>
  <img src='/wp-content/uploads/pop-stash@2x.png' class="help-center-img img-bordered" alt="Top toolbar in GitKraken Desktop with Pop Stash button highlighted">
  <figcaption style="text-align:center; color:#888">Use the Pop Stash button for one-click restore and delete.</figcaption>
</figure>

<a name="stashing-from-the-left-panel"></a>

## How to stash changes from the Commit Panel

To stash from the Commit Panel:

1. Click the **Stash** tab icon in the Commit Panel.
2. Stage the files you want to stash.
3. Type a **Stash title**.
4. Click **Stash Changes to *N* Files**.

<figure>
  <img src='/wp-content/uploads/stash-commit-panel-2025.png' class="help-center-img img-bordered" alt="Commit Panel's stash tab with input for name and description, and a Stash Changes button">
  <figcaption style="text-align:center; color:#888">Stage files and click the Stash icon to save changes.</figcaption>
</figure>

If you use [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai/), click the sparkle icon, **Generate a stash message with AI**, to write a stash message from your staged changes.

<figure>
  <img src="/wp-content/uploads/stash-ai-message@2x.png" class="help-center-img img-bordered" alt="GitKraken Stash panel (inside Commit Panel) with tooltip pointing to the AI icon for generating a stash message">
  <figcaption style="text-align:center; color:#888">Use GitKraken AI to generate a stash description.</figcaption>
</figure>

## How to view and manage stashes from the Left Panel

The Left Panel lists all your stashes. Right-click a stash to apply, pop, delete, hide, or show it.

<figure>
  <img src='/wp-content/uploads/stash-left-2025.png' class="help-center-img img-bordered" alt="Stash management menu in GitKraken's Left Panel showing options like Apply, Pop, Delete, and Share stash">
  <figcaption style="text-align:center; color:#888">Review and manage your stashes from the Left Panel.</figcaption>
</figure>

<a name="naming-a-stash"></a>

## How to name a stash

To name a stash, type the name in the WIP node's `// WIP` field in the Commit Graph before you stash.

<figure>
  <img src='/wp-content/uploads/custom-stash-wip@2x.png' class="help-center-img img-bordered" alt="User typing a custom stash name in the GitKraken commit graph WIP node">
  <figcaption style="text-align:center; color:#888">Enter a custom stash name before saving.</figcaption>
</figure>

The name identifies the stash in the Left Panel and the Commit Graph.

<figure>
  <img src='/wp-content/uploads/custom-stash-panel@2x.png' 
       class="help-center-img img-bordered" 
       alt="Custom-named stash labeled 'my-custom-stash-name' displayed under STASHES in the GitKraken Left Panel on the master branch">
  <figcaption style="text-align:center; color:#888">Named stash in the Left Panel.</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/custom-stash-graph@2x.png' 
       class="help-center-img img-bordered" 
       alt="Commit Graph showing a WIP stash labeled 'my-custom-stash-name' created on the master branch.">
  <figcaption style="text-align:center; color:#888">Named stash in the graph view.</figcaption>
</figure>

## How to edit a stash message

To update a stash description, right-click the stash in the graph or the Left Panel, then select **Edit stash message**.

<figure>
  <img src="/wp-content/uploads/amend-stash-graph2.png" 
       class="help-center-img img-bordered" 
       alt="Commit Graph showing a stash selected on the feature branch with the context menu open and 'Edit stash message' highlighted.">
  <figcaption style="text-align:center; color:#888">Edit a stash message from the context menu.</figcaption>
</figure>

## How to create and apply a partial stash

To stash specific files, right-click them in the Commit Panel, staged or unstaged, and select **Stash file** (or **Stash *N* files** for a multiple selection). GitKraken Desktop removes their changes from your working directory and saves them in a partial stash.

<figure>
  <img src='/wp-content/uploads/partial-stash.png' 
       class="help-center-img img-bordered" 
       alt="Context menu showing the option to stash two selected unstaged files from the Commit Panel.">
  <figcaption style="text-align:center; color:#888">Select individual files to stash partially.</figcaption>
</figure>

You can also apply changes from a stash one file at a time. Select the stash, right-click a file in the Commit Panel, and select **Apply stashed file** (or **Apply *N* files from stash**).

<figure>
  <img src='/wp-content/uploads/partial-stash-apply.png' 
       class="help-center-img img-bordered" 
       alt="Commit Panel showing context menu option to apply two selected files from stash.">
  <figcaption style="text-align:center; color:#888">Apply part of a stash by selecting specific files.</figcaption>
</figure>

### Tips for partial stashes

* Name a partial stash in the WIP node's `// WIP` field before stashing.
* Hold **Shift** or **Ctrl** to select multiple files.
* Applying a file from a stash does not remove the file from the stash.
