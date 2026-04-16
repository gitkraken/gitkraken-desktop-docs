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
last_verified: 2026-04
llms_include: true
tags: [terminal, shell, git, commands, auto-complete]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: April 2026</kbd>

Use this page to use the GitKraken Desktop terminal while staying in the context of the open repository, commit graph, and active worktree. It covers how to open the terminal, how command and flag auto-complete works, how terminal sessions behave across worktrees, how to run coding agents manually, and where to change shell and terminal appearance settings.

**Requirements and limits**
- Scope: In-app terminal for the currently open repository context
- Repository context: Commands run in the active repository or worktree working directory automatically
- Supported shell note: macOS and Linux use the OS default shell; Windows supports PowerShell and Bash via Preferences
- Auto-complete limitation: Conflicting third-party auto-complete tools can disable GitKraken suggestions
- Settings location: <kbd>Preferences &gt; In-App Terminal</kbd> for appearance and autocomplete behavior
- Coding agents: You can run supported or unsupported coding agent CLIs manually in the embedded terminal

To get started, open a repository and click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar, or search for "terminal" using the <a href="/working-with-repositories/command-palette">Command Palette</a>.

***

## Quick Start


**To open the terminal:** Click the Terminal icon in the toolbar or search for "terminal" in the Command Palette.

**To run commands:** Type any Git command such as `git status`, `git commit -m "message"`, or `git log --oneline`. Auto-complete suggestions appear as you type, including flag suggestions for each command.

**To run a coding agent manually:** Open the terminal in the worktree you want to use, then start your coding agent CLI there.

**To customize terminal appearance:** Go to <kbd>Preferences > In-App Terminal</kbd> to change font, size, line height, cursor style, and autocomplete behavior.

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

## How multi-session support works

The embedded terminal supports independent sessions per worktree in a single tab. GitKraken Desktop uses the same underlying worktrees in both List view and [Agent Sessions View](/gitkraken-desktop/agents/).

When you switch to another worktree, the terminal view refreshes to that worktree's session and opens in its working directory. For example, you might switch worktrees from List view or by clicking an agent session card in Agent Sessions View.

Each session runs independently, so long-running commands in one worktree keep running when you switch away and come back.

This is also how manual coding agent workflows work. If a coding agent is not explicitly integrated with GitKraken Desktop, you can still open the terminal for a worktree and run that agent there.

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
