---
title: GitKraken Desktop Command Palette | Fast Actions & Navigation
description: Discover how to use the Command Palette in GitKraken Desktop to quickly run commands, open files, switch repos, and customize settings with shortcuts.
product: GitKraken Desktop
feature: Command Palette
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
tags: [command-palette, shortcuts, navigation, search, actions]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: April 2026</kbd>

Use this page to run GitKraken Desktop actions from the Command Palette when you want a keyboard-first workflow for commands, files, repositories, worktrees, and settings. It explains how to open the palette, what command categories are available, and when it is faster than navigating the UI directly.

**Requirements and limits**
- Access methods: <kbd>Cmd/Ctrl + P</kbd>, the wand icon, or the Help menu
- Scope: Commands, files, repositories, branches, stashes, worktree-related navigation, settings, logs, and patches
- Search behavior: Results filter live as you type
- Execution model: Press <kbd>Enter</kbd> to run the selected item
- Command availability depends on the current repository state, open repo context, and configured integrations

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/lNsQesvuRj4?rel=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch how to use the Command Palette for faster workflows.</figcaption>
</figure>

***

## Quick Start


- Open with <kbd>Cmd</kbd> + <kbd>P</kbd> (macOS) or <kbd>Ctrl</kbd> + <kbd>P</kbd> (Windows/Linux), or click the wand icon in the top-right toolbar.
- Start typing to filter available commands. Results update as you type.
- Press <kbd>Enter</kbd> to run the selected command.

Common actions available through the Command Palette:
- **File management**: Create File, Delete File, Open File, Stage all changes, Discard all changes
- **Branch operations**: Create Branch, Rename Branch, Checkout, Push, Pull, Fetch All
- **Repository**: Open Repo, Clone, Init, Perform Repo Maintenance
- **Stash**: Create, Apply, Pop
- **View and settings**: Toggle Theme, Toggle Left Panel, Keyboard Shortcuts, Switch to Profile
- **Terminal and workflow**: Open in terminal for command-line tasks and manual coding agent workflows

The Command Palette is available at any time regardless of which panel or view is currently active in GitKraken Desktop.

***

## How to open the Command Palette

You can launch the Command Palette in three ways:

- Use the keyboard shortcut:
  - <kbd>Cmd</kbd> + <kbd>P</kbd> on macOS
  - <kbd>Ctrl</kbd> + <kbd>P</kbd> on Windows/Linux
- Click the <i class="fa fa-magic" style="transform: rotate(225deg)"></i> icon in the top-right toolbar
- Go to the Help menu → <strong>Open Command Palette</strong>

<figure>
  <img src="/wp-content/uploads/command-palette-example.gif" class="help-center-img img-bordered" alt="Using the GitKraken Command Palette to filter and select commands, files, and branches, demonstrating how it accelerates navigation and common Git workflows without leaving the keyboard.">
  <figcaption style="text-align:center; color:#888">Start typing to filter commands, files, repos, and more.</figcaption>
</figure>

***

## What command categories are available

Below is a list of supported commands grouped by category.

### Repo
- `Close Tab`
- `Open Repo`
- `Open in file manager`
- `Open in External Editor`
- `Open in External Diff/Merge Tool`
- `Open in terminal`
- `Repo Management: Clone`
- `Repo Management: Init`
- `Repo Management: Open`
- `Perform Repo Maintenance`

`Open in terminal` is especially useful when you want to start a command-line workflow in the current repository or worktree, including a manual coding agent workflow. For more information, see [GitKraken Terminal Guide](/gitkraken-desktop/terminal/) and [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

### Settings
- `Configure Git Flow`
- `Configure LFS`
- `Configure GPG Signing`
- `Initialize LFS on this repo`
- `Join the Light side` / `Join the Dark side`
- `Manage Account`
- `Settings`
- `Switch to Profile` + `profile name`

### View
- `Decrease Zoom`
- `Increase Zoom`
- `Keyboard Shortcuts`
- `Reset Zoom`
- `Toggle Left Panel`
- `Toggle Commit Detail Panel`
- `Toggle Syntax Highlighting`
- `Toggle Theme`

### History
- `Blame` + `filename`
- `History` + `filename`
- `Search Commits` + `message` / `sha` / `author`

### Core
- `Redo`
- `Undo`

### File
- `Create File` + `filename`
- `Delete File` + `filename`
- `Open File` + `filename`
- `View File` + `filename`
- `Edit File` + `filename`
- `Discard all changes`
- `Stage all changes`
- `Unstage all changes`

### Stash
- `Stash: Apply`
- `Stash: Create`
- `Stash: Pop`

### Branch
- `Create Branch`
- `Create Tag`
- `Create Annotated Tag`
- `Fetch All`
- `Pull`
- `Push`
- `Rename Branch`
- `Start Pull Request`
- `View Working Directory Changes`

### Checkout
- `Checkout` + `{branch name}`

### Patch
- `Create patch from all working directory changes`
- `Apply patch`

### Logs
- `Activity logs`
- `View Error Logs`
- `View Performance Logs`
- `View Release Notes`
