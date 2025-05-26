---
title: Staging Files and Changes
description: Learn how to stage, unstage, discard, and ignore files before committing in GitKraken Desktop.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: May 2025</kbd>

Learn how to stage files, review changes, and manage tracked content in GitKraken Desktop.

***

## Stage Files and Changes

Staging prepares your file changes for commit. To begin:

1. Select the <strong>//WIP</strong> node in the Commit Graph to open the Commit Panel.

<figure class='figure center'>
    <img src='/wp-content/uploads/select-WIP-2025.png' class="help-center-img img-bordered" alt="Select the WIP node to view changes">
    <figcaption style="text-align: center; color: #888;">Select the //WIP node to view your working changes.</figcaption>
</figure>

2. Hover over a file and click <button class='button button--success button--ui button--nolink'>Stage File</button> to stage it.

<figure class='figure center'>
    <img src='/wp-content/uploads/stage-file-2025.png' srcset="/wp-content/uploads/stage-file-2025@2x.png" class="help-center-img img-bordered" alt="Stage file button appears on hover">
    <figcaption style="text-align: center; color: #888;">Click Stage File on hover.</figcaption>
</figure>

You can also:

- Click <button class='button button--success button--ui button--nolink'>Stage all changes</button> to stage all at once
- Click a file to view its diff and selectively stage lines:
  - Highlight lines
  - Right-click and select <kbd>Stage selected lines</kbd>

<figure class='figure center'>
    <img src='/wp-content/uploads/stage-selected-lines-2025.png' class="help-center-img img-bordered" alt="Select lines to stage from diff view">
    <figcaption style="text-align: center; color: #888;">Right-click to stage specific lines or hunks.</figcaption>
</figure>

<div class='callout callout--success'>
<p><strong>Tip:</strong> Use <a href="/gitkraken-desktop/keyboard-shortcuts/#repo-actions">keyboard shortcuts</a> to speed up staging actions.</p>
</div>

***

## Unstage Files or Lines

To unstage a file:

1. Select the file under the <strong>Staged Files</strong> section
2. Click <button class='button button--danger button--ui button--nolink'>Unstage File</button>

<figure class='figure center'>
    <img src='/wp-content/uploads/unstage-file-2025.png' srcset="/wp-content/uploads/unstage-file-2025@2x.png" class="help-center-img img-bordered" alt="Unstage a file button">
    <figcaption style="text-align: center; color: #888;">Click Unstage File to move it back to working changes.</figcaption>
</figure>

To unstage lines or hunks, click a file to view its diff and right-click the content to unstage.

<figure class='figure center'>
    <img src='/wp-content/uploads/unstage-hunk-2025.png' class="help-center-img img-bordered" alt="Unstage hunk from file diff view">
    <figcaption style="text-align: center; color: #888;">Unstage specific hunks directly from the diff view.</figcaption>
</figure>

To unstage all:

- Click <button class='button button--danger button--ui button--nolink'>Unstage all changes</button>

***

## Discard Changes

To discard changes across your working directory:

1. Select the <strong>//WIP</strong> node
2. Click the <i class="fa fa-trash-o" aria-hidden="true"></i> trash icon to discard all or selected files

<figure class='figure center'>
    <img src='/wp-content/uploads/discard-all-changes-2025.png' srcset="/wp-content/uploads/discard-all-changes-2025@2x.png" class="help-center-img img-bordered" alt="Discard all changes from WIP">
    <figcaption style="text-align: center; color: #888;">Discard changes for all or multiple selected files.</figcaption>
</figure>

You can also:

- Multi-select files and right-click to <strong>Discard selected</strong>
- Discard lines/hunks from the file diff
- Right-click within the staging panel and choose <strong>Discard Changes</strong>

<figure class='figure center'>
    <img src='/wp-content/uploads/discard-hunk-ex-2025.png' class="help-center-img img-bordered" alt="Discard individual hunk from diff">
    <figcaption style="text-align: center; color: #888;">Discard selected hunks of code.</figcaption>
</figure>

***

## Ignore Files

To prevent Git from tracking certain files, add them to a `.gitignore` file.

Right-click a file and select <strong>Ignore</strong>:

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-file.png' srcset='/wp-content/uploads/ignore-file@2x.png 2x' class="help-center-img img-bordered" alt="Ignore option in file context menu">
    <figcaption style="text-align: center; color: #888;">Choose ignore rules based on file, extension, or folder.</figcaption>
</figure>

You can choose to:

- Ignore the selected file only
- Ignore all files with that extension
- Ignore all files in the directory

GitKraken Desktop will add the rule to a `.gitignore` file at the root of your repo. Nested `.gitignore` files are not parsed.

<div class='callout callout--note'>
<p><strong>Note:</strong> GitKraken Desktop only uses the root-level <code>.gitignore</code> file.</p>
</div>

### Ignore Previously Tracked Files

If a file is already tracked, you’ll see two options:

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-stop-tracking-2025.png' class="help-center-img img-bordered" alt="Prompt to ignore a tracked file">
</figure>

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-only.png' srcset='/wp-content/uploads/ignore-only@2x.png' class="help-center-img img-bordered" alt="Option to ignore but keep tracking">
</figure>

<figure class='figure center'>
    <img src='/wp-content/uploads/ignore-untrack.png' srcset='/wp-content/uploads/ignore-untrack@2x.png' class="help-center-img img-bordered" alt="Option to ignore and stop tracking">
</figure>

- <strong>Ignore</strong>: Adds to `.gitignore`, but Git will still track the file
- <strong>Ignore and Stop Tracking</strong>: Adds to `.gitignore` and removes from Git’s index
