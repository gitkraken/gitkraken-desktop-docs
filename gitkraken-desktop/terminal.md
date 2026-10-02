---
title: GitKraken Terminal Guide
description: Learn how to use GitKraken’s in-app terminal to run Git commands, work in repository and worktree context, run coding agents manually, and customize shell preferences.
product: GitKraken Desktop
feature: Terminal
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-09
llms_include: true
tags: [terminal, shell, git, commands, auto-complete]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: September 2026</kbd>

Use this page to run commands in the context of the open repository and worktree. It covers how to open and manage terminal tabs, how command and flag auto-complete works, how terminal sessions behave across worktrees, how to run coding agents manually, and where to change shell and terminal appearance settings.

**Requirements and limits**
- Scope: In-app terminal for the currently open repository context
- Repository context: Commands run in the active repository or worktree working directory automatically
- Supported shell note: macOS and Linux use the OS default shell; Windows supports PowerShell and Bash via Preferences
- Auto-complete limitation: Conflicting third-party auto-complete tools can disable GitKraken suggestions
- Settings location: <kbd>Preferences &gt; In-App Terminal</kbd> for appearance and autocomplete behavior
- Terminal tabs: Each repository or worktree keeps its own terminal tabs. Starting an agent session in a worktree with an open terminal starts the agent in a separate tab
- Panel behavior: The embedded terminal resizes smoothly when surrounding panels change, can be minimized to keep the terminal panel header visible, and exposes a trash icon in the panel header to kill terminal sessions
- Coding agents: You can run supported or unsupported coding agent CLIs manually in the embedded terminal

To get started, open a repository and click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar, or search for "terminal" using the <a href="/working-with-repositories/command-palette">Command Palette</a>.

***

## Quick Start


**To open the terminal:** Click the Terminal icon in the toolbar or search for "terminal" in the Command Palette.

**To run commands:** Type any Git command such as `git status`, `git commit -m "message"`, or `git log --oneline`. Auto-complete suggestions appear as you type, including flag suggestions for each command.

**To open another terminal:** Click the **+** button in the terminal tab bar. Select a tab to switch terminals, or close a tab you no longer need.

**To run a coding agent manually:** Open the terminal in the worktree you want to use, then start your coding agent CLI there.

**To customize terminal appearance:** Go to <kbd>Preferences > In-App Terminal</kbd> to change font, size, line height, cursor style, and autocomplete behavior.

**To minimize the terminal panel:** Use the minimize control in the terminal panel header. The panel header stays visible so you can restore the terminal when you need it.

**To kill a terminal session:** Click the trash icon in the terminal panel header. This ends the current terminal session for that worktree.

**To set your default shell:**
- **macOS/Linux**: Set ZSH or Bash as the default shell in your OS settings and restart your machine.
- **Windows**: Open <kbd>Preferences > Terminal</kbd> and select PowerShell or Bash.

The terminal shares context with the open repository or worktree, so commands run against the correct working directory automatically.

<figure>
  <img src="/wp-content/uploads/terminal-button-2025@2x.png"
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing the Terminal button in the top toolbar and an open terminal panel running the git status command.">
  <figcaption style="text-align:center; color:#888">Launch the terminal from the GitKraken toolbar</figcaption>
</figure>

---

## How Git commands and auto-complete work

The GitKraken Terminal supports most <a href="https://git-scm.com/" target="_blank">Git</a> commands. Start typing `git` to see command suggestions via auto-complete.

<figure>
  <img src="/wp-content/uploads/autocomplete-suggestions.png" 
       class="help-center-img img-bordered" 
       alt="Autocomplete dropdown in GitKraken Desktop terminal suggesting Git commands after typing 'git'. Suggestions include commit, config, rebase, add, and others.">
  <figcaption style="text-align:center; color:#888">Git commands appear in auto-complete suggestions</figcaption>
</figure>

Flag suggestions are also supported:

<figure>
  <img src="/wp-content/uploads/autocomplete-suggestions-flags.png" 
       class="help-center-img img-bordered" 
       alt="Autocomplete dropdown in the GitKraken Desktop terminal showing flag suggestions for the 'git status' command. Flags include --verbose, --branch, --show-stash, and others.">
  <figcaption style="text-align:center; color:#888">Flag suggestions enhance Git command efficiency</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Conflicting auto-complete programs may disable suggestions. You may need to uninstall or disable such programs for GitKraken's suggestions to work correctly.</p>
</div>

---

## How to customize terminal preferences

Visit <kbd><strong>Preferences > In-app Terminal</strong></kbd> to modify your terminal settings.

<figure>
  <img src="/wp-content/uploads/terminal-preferences-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop Preferences window with In-App Terminal settings selected. Options visible include font selection, font size, line height, cursor style, and autocomplete behavior.">
  <figcaption style="text-align:center; color:#888">Access terminal settings under Preferences</figcaption>
</figure>

### How the default terminal works on macOS and Linux

GitKraken supports ZSH and Bash. To switch shells:
1. Set the preferred shell as default in your OS settings.
2. Restart your machine to apply changes.

### How the default terminal works on Windows

PowerShell and Bash are currently supported. To change the shell:
1. Open <kbd>Preferences > Terminal</kbd>.
2. Set the _Default Terminal_ to your desired shell.

---

## How terminal tabs work

The terminal panel supports multiple terminal tabs. Click **+** in the tab bar to open another terminal, then select a tab to switch to it. Each repository or worktree keeps its own set of terminals.

<figure>
  <img src="/wp-content/uploads/gkd-12-6-terminal-tabs.png"
       class="help-center-img img-bordered"
       alt="GitKraken Desktop terminal panel with three terminal tabs named zsh, zsh, and node, the selected tab showing a close button, and a plus button for opening another terminal.">
  <figcaption style="text-align:center; color:#888">Open, switch between, and close terminal tabs</figcaption>
</figure>

When you switch worktrees, GitKraken shows that worktree's terminal tabs. Each terminal runs in its worktree's working directory, and long-running commands continue while you switch to another worktree.

When you start a coding agent in a worktree that already has a terminal open, GitKraken starts the agent in a new tab instead of replacing the existing terminal.

GitKraken Desktop uses the same worktrees in both List view and [Agent Sessions View](/gitkraken-desktop/agents/). You can open a worktree from either view and use its terminal tabs.

---

## How to run a coding agent manually in the terminal

Use this workflow when you want to run a coding agent CLI that GitKraken Desktop does not explicitly integrate with, or when you prefer to start the agent yourself.

1. Open the repository or worktree you want to use.
2. Open the terminal from the toolbar or Command Palette.
3. Confirm that the terminal is running in the correct working directory.
4. Start your coding agent CLI in the terminal.
5. Continue working in GitKraken Desktop while the terminal session stays attached to that worktree.

If you want GitKraken Desktop to create and manage coding agent sessions for explicitly supported agents, see [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

---

## How to drag and drop files into the terminal

You can drag a file from your OS file manager or from the Commit Panel into the terminal to insert the file's full path at the cursor. You can also drag text into the terminal to insert it at the cursor. This is useful when you want to paste a path or snippet into a command without retyping it.

---

## Common Git commands to try

Use the terminal to quickly execute common Git operations:

- `git status` - View working directory and staging status
- `git commit -m "message"` - Commit changes with a message
- `git log --oneline` - View a condensed commit history

These commands complement GitKraken’s visual graph for a comprehensive Git experience.
