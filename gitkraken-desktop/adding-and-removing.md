---
title: Add, Delete, and Filter Files in GitKraken Desktop
description: Learn how to create, delete, and manage files and folders in GitKraken Desktop using the Command Palette, context menu, and file filter. This page covers file and folder operations only — for adding or removing remotes, see the Remotes documentation.
product: GitKraken Desktop
feature: File Management
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
tags: [files, folders, create, delete, filter]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

<div class="callout callout--note">
<p><strong>Note:</strong> This page covers creating, deleting, and filtering files inside a repository. To add or remove a remote repository, see <a href="/gitkraken-desktop/pushing-and-pulling/">Remote Repositories and Pushing/Pulling</a>.</p>
</div>

Use this page to create files, create folders, delete files, and filter repository contents from inside GitKraken Desktop. It covers both Command Palette and context-menu workflows, plus the `View all files` mode you need when you want to delete or locate files outside the current staged or changed set.

**Requirements and limits**
- Workflow scope: File and folder creation, deletion, and filtering inside an existing repository
- Create-file access: Command Palette or Commit Panel context menu
- Folder creation behavior: Include `/` in the new filename to create a folder and file at the same time
- Delete-file limitation: To delete arbitrary repository files, enable `View all files` first
- Filter behavior: The `Filter Files` bar appears only when `View all files` is enabled

***

## Quick Start


**To create a file:**
1. Press <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>P</kbd> to open the Command Palette.
2. Type `Create File` and press <kbd>Enter</kbd>.
3. Enter a filename and press <kbd>Enter</kbd>. To create a folder at the same time, include a `/` in the name (e.g., `src/utils.js`).

**To create a file using the context menu:**
1. Right-click the empty space in the Commit Panel.
2. Select `Create File`.

**To delete a file:**
1. Right-click the file in the Commit Panel.
2. Select `Delete file`.

To delete any file in the repository (not just staged files), first enable `View all files` in the Commit Panel. Once enabled, right-click any file and select `Delete file`. A **Filter Files** bar also appears when `View all files` is on, letting you type a filename or extension to locate files quickly.

***

## How to add a file using the Command Palette

1. Press <kbd>Ctrl</kbd>/<kbd>Cmd</kbd> + <kbd>P</kbd> to open the Command Palette.
2. Type `Create File` and press <kbd>Enter</kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-file-command-palette-2025.png' class="help-center-img img-bordered" alt="Using GitKraken Desktop's Command Palette to create a new file directly from the keyboard, demonstrating how the palette streamlines file creation workflows without navigating away from the commit graph.">
  <figcaption style="text-align: center; color: #888;">Create a new file from the Command Palette.</figcaption>
</figure>

3. Type the desired filename and press <kbd>Enter</kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-file-2025-gif.gif' class="help-center-img img-bordered" alt="Using GitKraken Desktop's Command Palette to create and name a new file, demonstrating how developers can generate project files without leaving the keyboard or switching UI contexts.">
  <figcaption style="text-align: center; color: #888;">Watch how to name and create a file.</figcaption>
</figure>

To create a folder and a file at once, include a forward slash (/) in the file name:

<figure class='figure center'>
  <img src='/wp-content/uploads/create-folder@2x.png' class="help-center-img img-bordered" alt="Creating a new folder by including a slash in the file name, demonstrating how GitKraken Desktop auto-generates nested directory structures during file creation.">
  <figcaption style="text-align: center; color: #888;">This creates a folder called &quot;folder-name&quot; that contains &quot;file-name.txt.&quot;</figcaption>
</figure>

***

## How to add a file using the context menu

You can also add files via the Commit Panel:

1. Right-click the empty space in the Commit Panel.
2. Select `Create File` from the context menu.

***

## How to delete a file from the Commit Panel

1. In the Commit Panel, right-click the file you want to delete.
2. Select `Delete file` from the context menu.

<figure class='figure center'>
  <img src='/wp-content/uploads/delete-file@2x.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing file actions, including the option to delete a file from the Commit Panel.">
  <figcaption style="text-align: center; color: #888;">Use the context menu to delete a file from the Commit Panel.</figcaption>
</figure>

***

## How to delete any file in the repository

1. Enable the `View all files` option.
2. Right-click the file you want to remove.
3. Select `Delete file` from the context menu.

<figure class='figure center'>
  <img src='/wp-content/uploads/delete-any-file@2x.png' class="help-center-img img-bordered" alt="Right-click context menu with file deletion option after enabling 'View all files' in GitKraken Desktop.">
  <figcaption style="text-align: center; color: #888;">Check the 'View all files' option to find a file, and then delete it from the context menu.</figcaption>
</figure>

***

## How to filter files

When `View all files` is enabled, a <kbd>Filter Files</kbd> bar appears.

- Type a filename or extension to quickly find and jump to specific files.

<figure class='figure center'>
  <img src='/wp-content/uploads/filter-files.gif' class="help-center-img img-bordered" alt="Filtering visible files in GitKraken Desktop by typing a file extension in the Tree View filter bar.">
  <figcaption style="text-align: center; color: #888;">Type a file name or extension to filter the list of files in your repository.</figcaption>
</figure>
