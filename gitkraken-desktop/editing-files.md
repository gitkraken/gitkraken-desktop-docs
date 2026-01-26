---
title: Edit and Save Files in GitKraken Desktop
description: Learn how to open, edit, save, discard, and stage file changes using GitKraken Desktop’s built-in code editor. Includes shortcuts and encoding options.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: January 2026</kbd>

Learn how to edit, save, and manage files using GitKraken Desktop’s built-in editor.

***

## Enter Edit Mode Automatically

If you [create a new file](/working-with-files/adding-and-removing#adding-a-file), GitKraken Desktop opens the file immediately in edit mode so you can begin editing right away.

***

## Ways to Edit an Existing File

### 1. Use the Context Menu

Right-click a file (from a previous commit or via **View all files**) and select <kbd>Edit file</kbd>.

<figure class='figure center'>
    <img src='/wp-content/uploads/edit-file-menu-2025.png' class="help-center-img img-bordered" alt="Right-click context menu showing the Edit file option for a selected file in GitKraken Desktop">
    <figcaption style="text-align: center; color: #888;">Right-click any file and select Edit file.</figcaption>
</figure>

### 2. Use the Command Palette

1. Press <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>P</kbd>
2. Type `Edit File` and press <kbd>Enter</kbd>
3. Type the filename and press <kbd>Enter</kbd>

<figure class='figure center'>
    <img src='/wp-content/uploads/edit-file-fuzzy.gif' class="help-center-img img-bordered" alt="Using the Command Palette in GitKraken Desktop to search for and select a file to edit">
    <figcaption style="text-align: center; color: #888;">Find and open files using the Command Palette.</figcaption>
</figure>

### 3. Use the Diff or File View

Click the <button class='button button--primary button--ui button--nolink'>Edit this file</button> button from a file diff.

<figure class='figure center'>
    <img src='/wp-content/uploads/edit-file-diff-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop UI showing the Edit This File button enabled from Diff view">
    <figcaption style="text-align: center; color: #888;">Click Edit this file from the Diff/File view panel.</figcaption>
</figure>

<div class='callout callout--success'>
<p><strong>Note:</strong> If viewing a file on a different branch, the button will read <kbd>Edit in working directory</kbd>. It opens the file version from your current branch.</p>
</div>

***

## File Edit Indicators

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

## Save or Discard Changes

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

## Stage Your File Edits

After editing, click <button class='button button--success button--ui button--nolink'>Stage File</button> to commit your changes. Options include:

- <kbd>Save and stage</kbd>
- <kbd>Stage saved changes only</kbd>

<figure class='figure center'>
    <img src='/wp-content/uploads/save-and-stage-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop prompt asking to save and stage changes or only stage saved content when clicking Stage File">
    <figcaption style="text-align: center; color: #888;">Save and stage or stage only saved changes.</figcaption>
</figure>

***

## File Encoding

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

## Markdown Preview

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

