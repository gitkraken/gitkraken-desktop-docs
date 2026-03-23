---
title: Edit and Save Files in GitKraken Desktop
description: Learn how to open, edit, save, discard, and stage file changes using GitKraken Desktop’s built-in code editor. Includes shortcuts and encoding options.
product: GitKraken Desktop
feature: File Editing
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
tags: [editing, files, save, discard, encoding]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to open, edit, save, discard, stage, and preview files in GitKraken Desktop’s built-in editor. It covers the different ways to enter edit mode, what the editor indicators mean, how save-and-stage behaves, and how to review or override file encoding when UTF-8 is not enough.

**Requirements and limits**
- Workflow scope: Built-in file editing inside GitKraken Desktop
- Entry points: Context menu, Command Palette, or the file diff view
- Unsaved-change indicator: A blue dot marks unsaved edits in the editor
- Stage behavior: Choose between **Save and stage** or **Stage saved changes only**
- Branch-context limitation: `Edit in working directory` opens the version from your current branch, not the branch currently being inspected
- Encoding limitation: GitKraken Desktop can read and label encodings, but it does not convert file encodings on save
- Markdown preview: Available for `.md` files only

***

## Quick Start

Edit files directly in GitKraken Desktop without switching to an external editor.

**To open a file for editing:**
- Right-click any file in the Commit Panel or via **View all files** and select **Edit file**.
- Or open the Command Palette (<kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>P</kbd>), type `Edit File`, and enter the filename.
- Or click the **Edit this file** button from any file diff view.

**To save changes:**
- Press <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>S</kbd>. A blue dot in the editor indicates unsaved changes.

**To discard unsaved changes:**
- Hover over the blue dot in the editor tab and click the **X**, then confirm with **Don’t Save**.

**To stage your edits:**
- Click **Stage File** in the Commit Panel. Choose **Save and stage** to save and stage together, or **Stage saved changes only** to stage only what was already saved.

For `.md` files, click **Preview** in the editor toolbar to toggle a rendered Markdown preview alongside the editor. GitKraken Desktop expects UTF-8 encoding by default; adjust the encoding setting from the dropdown in the editor or under <kbd>Preferences > Encoding</kbd>.

***

## How edit mode starts automatically for new files

If you [create a new file](/working-with-files/adding-and-removing#adding-a-file), GitKraken Desktop opens the file immediately in edit mode so you can begin editing right away.

***

## How to edit an existing file

### How to edit a file from the context menu

Right-click a file (from a previous commit or via **View all files**) and select <kbd>Edit file</kbd>.

<figure class='figure center'>
    <img src='/wp-content/uploads/edit-file-menu-2025.png' class="help-center-img img-bordered" alt="Right-click context menu showing the Edit file option for a selected file in GitKraken Desktop">
    <figcaption style="text-align: center; color: #888;">Right-click any file and select Edit file.</figcaption>
</figure>

### How to edit a file from the Command Palette

1. Press <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>P</kbd>
2. Type `Edit File` and press <kbd>Enter</kbd>
3. Type the filename and press <kbd>Enter</kbd>

<figure class='figure center'>
    <img src='/wp-content/uploads/edit-file-fuzzy.gif' class="help-center-img img-bordered" alt="Using the Command Palette in GitKraken Desktop to search for and select a file to edit">
    <figcaption style="text-align: center; color: #888;">Find and open files using the Command Palette.</figcaption>
</figure>

### How to edit a file from Diff or File View

Click the <button class='button button--primary button--ui button--nolink'>Edit this file</button> button from a file diff.

<figure class='figure center'>
    <img src='/wp-content/uploads/edit-file-diff-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop UI showing the Edit This File button enabled from Diff view">
    <figcaption style="text-align: center; color: #888;">Click Edit this file from the Diff/File view panel.</figcaption>
</figure>

<div class='callout callout--success'>
<p><strong>Note:</strong> If viewing a file on a different branch, the button will read <kbd>Edit in working directory</kbd>. It opens the file version from your current branch.</p>
</div>

***

## What the file edit indicators mean

The upper-left corner of the file editor shows:

- <strong>editable</strong> tag: Indicates the file can be modified
- <strong>blue dot</strong>: Indicates unsaved changes

<figure class='figure center'>
    <img src='/wp-content/uploads/editable-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop file editor showing active editable mode with highlighted label">
    <figcaption style="text-align: center; color: #888;">The file editor shows editable state.</figcaption>
</figure>

<figure class='figure center'>
    <img src='/wp-content/uploads/save-changes-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing blue dot indicator for unsaved file edits">
    <figcaption style="text-align: center; color: #888;">Unsaved changes are indicated with a blue dot.</figcaption>
</figure>

***

## How to save or discard changes

- Press <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>S</kbd> to save
- To discard unsaved changes:
  1. Hover over the blue dot
  2. Click the <kbd>X</kbd>
  3. Select <kbd>Don't Save</kbd>

<figure class='figure center'>
    <img src='/wp-content/uploads/do-not-save-prompt-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop prompt asking whether to save or discard unsaved file changes">
    <figcaption style="text-align: center; color: #888;">Prompt to discard unsaved changes.</figcaption>
</figure>

***

## How to stage file edits

After editing, click <button class='button button--success button--ui button--nolink'>Stage File</button> to commit your changes. Options include:

- <kbd>Save and stage</kbd>
- <kbd>Stage saved changes only</kbd>

<figure class='figure center'>
    <img src='/wp-content/uploads/save-and-stage-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop prompt asking to save and stage changes or only stage saved content when clicking Stage File">
    <figcaption style="text-align: center; color: #888;">Save and stage or stage only saved changes.</figcaption>
</figure>

***

## How file encoding works

GitKraken Desktop expects most files to use `UTF-8` encoding. To review or adjust encoding:

- Use the dropdown at the top of the editor
- Visit <kbd>Preferences</kbd> > <kbd>Encoding</kbd>
- Or select <kbd>Guess Encoding</kbd> to let GitKraken match it automatically

<figure class='figure center'>
    <img src='/wp-content/uploads/file-encoding-diff2.png' class="help-center-img img-bordered" alt="File editor in GitKraken Desktop showing encoding options including UTF-8, UTF-16LE, and Windows-1252">
    <figcaption style="text-align: center; color: #888;">Encoding dropdown available from file editor.</figcaption>
</figure>

<div class='callout callout--warning'>
<p><strong>Note:</strong> GitKraken Desktop does not change a file’s encoding upon save. Use an external editor like VS Code if you need to convert encodings.</p>
</div>

<figure class='figure center'>
    <img src='/wp-content/uploads/preferences-encoding-select-2025.png' class="help-center-img img-bordered" alt="Preferences panel in GitKraken Desktop showing a dropdown list of available default encodings including UTF-8 and ISO-8859 variants">
    <figcaption style="text-align: center; color: #888;">Choose your default encoding from preferences.</figcaption>
</figure>

## How Markdown preview works

GitKraken Desktop includes a built-in markdown preview for `.md` files. To access the option, first click to edit a file in the upper left of the file diff.

<figure class='figure center'>
    <img src='/wp-content/uploads/edit-file-diff-2025.png' class="help-center-img img-bordered" alt="Diff view in GitKraken Desktop with the 'Edit This File' button highlighted in the top left panel">
    <figcaption style="text-align: center; color: #888;">Click Edit this file from the Diff/File view panel.</figcaption>
</figure>

From here, toggle the preview pane by clicking the <button class='button button--primary button--ui button--nolink'>Preview</button> button in the top of the editor. 

<figure class='figure center'>
    <img src='/wp-content/uploads/markdown-preview@2x.png' class="help-center-img img-bordered" alt="Markdown file open in GitKraken Desktop with the Preview tab selected to show rendered output">
    <figcaption style="text-align: center; color: #888;">Toggle the markdown preview when editing a file.</figcaption>
</figure>

You can switch between editing and previewing the markdown content.
