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
last_verified: 2026-03
llms_include: true
tags: [stash, pop, apply, work-in-progress, partial-stash]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to stash, apply, pop, rename, and partially restore uncommitted changes in GitKraken Desktop when you need to switch context without creating a commit. It covers both full stashes and partial file-based stashes, along with the graph and Left Panel workflows for managing them.

**Requirements and limits**
- Workflow scope: Uncommitted local changes only
- Apply vs. pop: **Apply Stash** keeps the stash; **Pop Stash** applies it and removes it
- Partial stash behavior: Applying a single file from a partial stash does not remove the stash
- Naming option: Name the stash before creating it by editing the `// WIP` field or stash summary field
- GitKraken AI note: AI-generated stash messages require GitKraken AI to be enabled
- Stash visibility: Stashes can be hidden from the graph without being deleted

***

## Quick Start

Stash and restore uncommitted changes in GitKraken Desktop using the toolbar or Commit Panel.

**To stash all changes:** Click the **Stash** icon in the top toolbar. Your stash appears in the Commit Graph.

**To manage a stash:** Right-click the stash node in the graph to apply, pop, delete, or hide it. Right-click a stash in the Left Panel for the same options.

**To pop the latest stash:** Click the **Pop Stash** button in the toolbar to apply changes and delete the stash in one step.

**To name a stash:** Type a name into the `// WIP` field at the top of the graph before clicking Stash.

**To stash specific files (partial stash):** Stage your files in the Commit Panel, then right-click a file in the Staged Files section and select **Stash file**.

**To apply a partial stash file by file:** Select the stash in the graph, then right-click a file in the Commit Panel and choose to apply it. Applying a single file does not remove the stash.

***

<a name="stashing-files"></a>

## How to stash changes from the top toolbar

Click the **Stash** icon in the top toolbar to create a new stash.

<figure>
  <img src='/wp-content/uploads/stash@2x.png' class="help-center-img img-bordered" alt="GitKraken top toolbar with Stash button highlighted">
  <figcaption style="text-align:center; color:#888">Create a stash from the top toolbar.</figcaption>
</figure>

Your stash will appear in the Commit Graph. Right-click on the stash node to see available options:

* **Apply Stash**: Apply changes to your working directory and keep the stash.
* **Pop Stash**: Apply changes and remove the stash.
* **Delete Stash**: Permanently remove the stash.
* **Hide**: Hide the stash from the graph.
* **Hide all stashes**: Hide all stashes from the graph.
* **Show all stashes**: Display all hidden stashes.

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

You can stash changes from the Commit Panel. Stage your files and click the Stash icon (instead of Commit).

<figure>
  <img src='/wp-content/uploads/stash-commit-panel-2025.png' class="help-center-img img-bordered" alt="Commit Panel's stash tab with input for name and description, and a Stash Changes button">
  <figcaption style="text-align:center; color:#888">Stage files and click the Stash icon to save changes.</figcaption>
</figure>

If you use [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai/), click the sparkle icon to auto-generate a stash message based on your staged changes.

<figure>
  <img src="/wp-content/uploads/stash-ai-message@2x.png" class="help-center-img img-bordered" alt="GitKraken Stash panel (inside Commit Panel) with tooltip pointing to the AI icon for generating a stash message">
  <figcaption style="text-align:center; color:#888">Use GitKraken AI to generate a stash description.</figcaption>
</figure>

## How to view and manage stashes from the Left Panel

All your stashes are listed in the Left Panel. Right-click to Apply, Pop, Delete, Hide, or Show them.

<figure>
  <img src='/wp-content/uploads/stash-left-2025.png' class="help-center-img img-bordered" alt="Stash management menu in GitKraken's Left Panel showing options like Apply, Pop, Delete, and Share stash">
  <figcaption style="text-align:center; color:#888">Review and manage your stashes from the Left Panel.</figcaption>
</figure>

<a name="naming-a-stash"></a>

## How to name a stash

To give a stash a name, type into the `// WIP` field at the top of the graph before stashing.

<figure>
  <img src='/wp-content/uploads/custom-stash-wip@2x.png' class="help-center-img img-bordered" alt="User typing a custom stash name in the GitKraken commit graph WIP node">
  <figcaption style="text-align:center; color:#888">Enter a custom stash name before saving.</figcaption>
</figure>

Named stashes are easier to recognize in the Left Panel and commit graph.

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

Stash specific files by right-clicking them in the **Staged Files** panel and selecting **Stash file**. This clears their changes and saves them to a partial stash.

<figure>
  <img src='/wp-content/uploads/partial-stash.png' 
       class="help-center-img img-bordered" 
       alt="Context menu showing the option to stash two selected unstaged files from the Commit Panel.">
  <figcaption style="text-align:center; color:#888">Select individual files to stash partially.</figcaption>
</figure>

You can also apply changes from a partial stash one file at a time. Right-click a file in the Commit Panel while a stash is selected.

<figure>
  <img src='/wp-content/uploads/partial-stash-apply.png' 
       class="help-center-img img-bordered" 
       alt="Commit Panel showing context menu option to apply two selected files from stash.">
  <figcaption style="text-align:center; color:#888">Apply part of a stash by selecting specific files.</figcaption>
</figure>

### Tips for partial stashes

* Name a partial stash via the `// WIP` node or summary field before stashing.
* Hold **Shift** or **Ctrl** to select multiple files.
* Applying a file from a stash doesn’t remove it from the stash.
