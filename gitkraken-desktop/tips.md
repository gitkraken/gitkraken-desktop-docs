---
title: Tips
description: Find out all the things users should know to boost their GitKraken Desktop experience.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

Here's the TL;DR of GitKraken Desktop’s most powerful productivity features.

***

### 1. Set Up Profiles

Separate work and personal repositories—or manage multiple accounts with [Profiles](/start-here/profiles).

<figure class='figure center'>
  <img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered" alt="Example of unique integrations for each profile">
  <figcaption style="text-align: center; color: #888;">Each profile can save a unique integration connection.</figcaption>
</figure>

Each profile retains its own Git config, preferences, and open tabs.

<div class='callout callout--success'>
  <p>Note: Access to multiple profiles requires a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.</p>
</div>

***

### 2. Use the Command Palette

The [Command Palette](/start-here/command-palette) helps you navigate GitKraken quickly with keyboard-driven actions.

<figure class='figure center'>
  <img src="/wp-content/uploads/command-palette-2025.gif" class="help-center-img img-bordered" alt="Command Palette in use to open repo in VS Code">
  <figcaption style="text-align: center; color: #888;">Use the Command Palette to launch repositories, open editors, and more.</figcaption>
</figure>

Common actions:

**Core**
- `Undo`, `Redo`

**File**
- `Create File`, `Delete File`, `Open File`, `Edit File`, `View File`
- `Discard all changes`, `Stage all changes`, `Unstage all changes`

***

### 3. Keyboard Shortcuts

Speed through tasks with [keyboard shortcuts](/start-here/keyboard-shortcuts).

<table class='table table--bordered table--shortcuts'>
  <thead>
    <tr>
      <th>Action</th>
      <th>Mac</th>
      <th>Windows/Linux</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Open keyboard shortcuts</td>
      <td><kbd>&#8984;</kbd><kbd>/</kbd></td>
      <td><kbd>Ctrl</kbd><kbd>/</kbd></td>
    </tr>
  </tbody>
</table>

***

### 4. Cherry Pick Multiple Commits

Select multiple commits using <kbd>Cmd/Ctrl</kbd> or <kbd>Shift</kbd>, then right-click and select <kbd>Cherry pick X commits</kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/multi-cherry-pick-menu.png' class="help-center-img img-bordered" alt="Multi-commit cherry pick menu in GitKraken">
  <figcaption style="text-align: center; color: #888;">Select multiple commits from the graph to cherry pick them together.</figcaption>
</figure>

You can reorder, squash, drop, or rename commits before completing. Learn more in [Interactive Cherry Pick](/gitkraken-desktop/cherrypick/).

***

### 5. Integrate with Git Services

Connect GitKraken Desktop with [GitHub, GitLab, Bitbucket, and Azure DevOps](/gitkraken-desktop/integrations/) to streamline cloning, remotes, and PR workflows.

<figure class='figure center'>
  <img src="/wp-content/uploads/connect-azure-devops-2025.png" class="help-center-img img-bordered" alt="Git hosting integration settings">
  <figcaption style="text-align: center; color: #888;">Connect your Git provider to speed up repository access.</figcaption>
</figure>

**Note:**
- Community users are limited to public repositories on GitHub/GitLab/Bitbucket.
- Azure DevOps integration requires a GitKraken subscription.
- Self-Hosted services require an Advanced plan or higher.

**Benefits:**
- Create repos and configure `.gitignore` or license files
- Clone via remote repo list
- Manage remotes and pull requests

***

### 6. Hide and Solo Branches

Control the Commit Graph display with [Hide and Solo](/gitkraken-desktop/hiding-and-soloing/) options.

<div class="flex-wrap" style="align-items: flex-start">
  <div class="flex-item">
    <img src="/wp-content/uploads/gk-hide-icon-green.svg" class='img-responsive' style="width: 70px; height: 70px" alt="Hide branch icon">
  </div>
  <div class="flex-item">
    <h3>Hide</h3>
    <p>Click the eye <i class='fa fa-eye icon-green'></i> next to a branch or right-click to hide it. Hidden branches show a gray <i class='fa fa-eye-slash'></i> icon.</p>
  </div>
</div>

<div class="flex-wrap" style="align-items: flex-start">
  <div class="flex-item">
    <img src="/wp-content/uploads/gk-solo-icon-orange.svg" class='img-responsive' style="width: 70px; height: 70px" alt="Solo branch icon">
  </div>
  <div class="flex-item">
    <h3>Solo</h3>
    <p>Right-click a branch and select `Solo` to show only that branch. Repeat to solo/unsolo other branches using the orange <i class='fa fa-dot-circle-o icon-orange'></i> icon.</p>
  </div>
</div>

***

### 7. File History and Blame

[View file history and blame](/gitkraken-desktop/diff/#file-blame-and-history) by clicking a commit and right-clicking a file.

<figure class='figure center'>
  <img src='/wp-content/uploads/file-history-content-menu-2025.png' class="help-center-img img-bordered" alt="File history and blame menu">
  <figcaption style="text-align: center; color: #888;">Right-click a file to view its history or blame.</figcaption>
</figure>

<figure class='figure center'>
  <img src='/wp-content/uploads/file-diff-2025.png' class="help-center-img img-bordered" alt="File diff and commit history">
  <figcaption style="text-align: center; color: #888;">Switch between commit diff and file view with blame.</figcaption>
</figure>

***

### 8. GitKraken Desktop Terminal

Run Git commands with the [GitKraken Terminal](/gitkraken-desktop/terminal/). Click <i class="fa fa-terminal"></i> in the toolbar or use <kbd>Alt/Opt + T</kbd>.

Set a default terminal from <kbd>Preferences > External Tools</kbd>.

***

### 9. Resize the Commit Graph

Hover over the graph’s colored lines and drag to resize.

<figure class='figure center'>
  <img src='/wp-content/uploads/graph-drag-2025.gif' class='help-center-img img-bordered' alt='Resize GitKraken commit graph'>
  <figcaption style="text-align: center; color: #888;">Adjust the graph view to focus on the information you need.</figcaption>
</figure>
