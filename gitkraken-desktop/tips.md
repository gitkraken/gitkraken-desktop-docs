---
title: GitKraken Desktop Tips | Productivity Shortcuts & Power Features
description: GitKraken Desktop tips for Profiles, the Command Palette, keyboard shortcuts, coding agents, cherry pick, integrations, and the Commit Graph.
product: GitKraken Desktop
feature: Tips and Power Features
content_type: overview
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps, generic]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps]
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [tips, productivity, shortcuts, integrations, advanced]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-start-here"
    nav_label: "Tips"
    nav_order: 100
    nav_parent: "desktop-start-here"
    page_type: "content"
    card_icon: "bulb"
    card_color: "purple"
    card_description: "Shortcuts and power features worth knowing"
---
<kbd>Last updated: November 2026</kbd>

Use these tips to speed up everyday Git work in GitKraken Desktop. You can set up Profiles, navigate with the Command Palette and keyboard shortcuts, run coding agents in parallel worktrees, connect integrations, and control what the Commit Graph shows.

**Requirements and limits**
- Each tip is a summary. For full steps and edge cases, open the linked feature page.
- Some tips use paid features, including multiple Profiles and some integrations.
- Integration capabilities vary by Git provider and plan, especially for Azure DevOps and self-hosted services.
- Shortcuts, Command Palette actions, and other UI behavior can differ by operating system and by repository.

***

## How to set up profiles

Use [Profiles](/start-here/profiles) to keep work and personal repositories separate, or to manage multiple accounts.

<figure class='figure center'>
  <img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered" alt="GitKraken Desktop showing a different GitHub account linked to each profile.">
  <figcaption style="text-align: center; color: #888;">Each profile can save a unique integration connection.</figcaption>
</figure>

Each profile keeps its own Git config, preferences, and open tabs.

> **Note:** Access to multiple profiles requires a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.

***

## How to use the Command Palette

Use the [Command Palette](/start-here/command-palette) to find and run GitKraken Desktop actions from the keyboard.

<figure class='figure center'>
  <img src="/wp-content/uploads/command-palette-2025.gif" class="help-center-img img-bordered" alt="The GitKraken Desktop Command Palette filtering its commands as open and then create are typed, showing matches such as Open in VS Code, Open Repo, Create File, and Create Branch.">
  <figcaption style="text-align: center; color: #888;">Use the Command Palette to launch repositories, open editors, and more.</figcaption>
</figure>

Common Command Palette actions include:

- **Undo** and **Redo**
- File actions: **Create File**, **Delete File**, **Open File**, **Edit File**, and **View File**
- Change actions: **Discard all changes**, **Stage all changes**, and **Unstage all changes**

***

## How to use keyboard shortcuts

Use [keyboard shortcuts](/start-here/keyboard-shortcuts) to run common actions without the mouse. To see the full list in GitKraken Desktop, use this shortcut:

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

## How to use the Agents view for parallel work

Use the Agents view to start and monitor coding agent sessions in parallel. In the Left Panel, use the `List | Agents` toggle to switch between List view and the Agents view. For setup and session steps, see [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

The Agents view uses the same underlying worktrees as List view, but organizes them around coding agent sessions, status, and quick actions. For general worktree management, see [Manage Git Worktrees in GitKraken Desktop](/gitkraken-desktop/worktrees/).

***

## How to cherry pick multiple commits

Select multiple commits using <kbd>Cmd/Ctrl</kbd> or <kbd>Shift</kbd>, then right-click and select <kbd>Cherry pick X commits</kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/multi-cherry-pick-menu.png' class="help-center-img img-bordered" alt="GitKraken Desktop context menu showing 'Cherry pick 5 commits' after selecting multiple commits from the commit graph.">
  <figcaption style="text-align: center; color: #888;">Select multiple commits from the graph to cherry pick them together.</figcaption>
</figure>

Before GitKraken Desktop applies the commits, you can reorder, squash, reword, or drop them. Learn more in [Interactive Cherry Pick](/gitkraken-desktop/cherrypick/).

***

## How to integrate with Git services

Connect GitKraken Desktop to [GitHub, GitLab, Bitbucket, and Azure DevOps](/gitkraken-desktop/integrations/) to work with your hosted repositories and pull requests.

<figure class='figure center'>
  <img src="/wp-content/uploads/connect-azure-devops-2025-v3@2x.png" class="help-center-img img-bordered" alt="Preferences > Integrations > Azure DevOps in GitKraken Desktop: the Azure DevOps card reads Not Connected with a Connect to Azure DevOps button, a Manage Integrations button sits at the top right, and below &quot;or&quot; are Host Domain and Personal Access Token fields with a Connect button.">
  <figcaption style="text-align: center; color: #888;">Connect your Git provider to speed up repository access.</figcaption>
</figure>

With an integration connected, you can:
- Create repositories and add a `.gitignore` or license file
- Clone from a list of your remote repositories
- Manage remotes and pull requests

Integration access depends on your plan:
- Community users can use public repositories on GitHub, GitLab, and Bitbucket only.
- Azure DevOps integration requires a GitKraken subscription.
- Self-hosted services require a paid plan that supports self-hosted integrations.

***

## How to hide and solo branches

Control the Commit Graph display with [Hide and Solo](/gitkraken-desktop/hiding-and-soloing/) options.

<div class="flex-wrap" style="align-items: flex-start">
  <div class="flex-item">
    <figure>
      <img src="/wp-content/uploads/gk-hide-icon-green.svg" class='img-responsive' style="width: 70px; height: 70px" alt="Hide branch icon">
      <figcaption style="text-align: center; color: #888">Hide branch icon.</figcaption>
    </figure>
  </div>
  <div class="flex-item">
    <h3>Hide</h3>
    <p>To hide a branch, click the eye <i class='fa fa-eye icon-green'></i> icon next to it in the Left Panel, or right-click it and select <kbd>Hide</kbd>. Hidden branches show a gray <i class='fa fa-eye-slash'></i> icon.</p>
  </div>
</div>

<div class="flex-wrap" style="align-items: flex-start">
  <div class="flex-item">
    <figure>
      <img src="/wp-content/uploads/gk-solo-icon-orange.svg" class='img-responsive' style="width: 70px; height: 70px" alt="Solo branch icon">
      <figcaption style="text-align: center; color: #888">Solo branch icon.</figcaption>
    </figure>
  </div>
  <div class="flex-item">
    <h3>Solo</h3>
    <p>Right-click a branch and select <kbd>Solo</kbd> to show only that branch. Soloed branches show an orange <i class='fa fa-dot-circle-o icon-orange'></i> icon. To solo or unsolo other branches, click the solo icon next to each branch name in the Left Panel.</p>
  </div>
</div>

***

## How to view file history and blame

To [view file history and blame](/gitkraken-desktop/diff/#how-to-view-file-blame-and-history), click a commit and right-click a file.

<figure class='figure center'>
  <img src='/wp-content/uploads/file-history-content-menu-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the options to view file history and blame.">
  <figcaption style="text-align: center; color: #888;">Right-click a file to view its history or blame.</figcaption>
</figure>

<figure class='figure center'>
  <img src='/wp-content/uploads/file-diff-2025.png' class="help-center-img img-bordered" alt="File history panel next to a line-by-line commit diff in GitKraken Desktop.">
  <figcaption style="text-align: center; color: #888;">Switch between commit diff and file view with blame.</figcaption>
</figure>

***

## How to open the GitKraken Desktop terminal

Run Git commands in the [GitKraken Terminal](/gitkraken-desktop/terminal/). To open it, click the Terminal <i class="fa fa-terminal"></i> button in the toolbar.

You can also use the embedded terminal to run coding agents by hand in a repository or worktree, including agents that GitKraken Desktop does not integrate with.

To choose the terminal that <kbd>Alt/Opt + T</kbd> opens, set a default terminal in <kbd>Preferences > External Tools</kbd>. For terminal sessions that follow your active worktree, see [GitKraken Terminal Guide](/gitkraken-desktop/terminal/).

***

## How to resize the Commit Graph

To resize the Commit Graph, hover over the graph's colored lines and drag.

<figure class='figure center'>
  <img src='/wp-content/uploads/graph-drag-2025.gif' class='help-center-img img-bordered' alt='The GitKraken Desktop Commit Graph being resized horizontally by dragging.'>
  <figcaption style="text-align: center; color: #888;">Adjust the graph view to focus on the information you need.</figcaption>
</figure>
