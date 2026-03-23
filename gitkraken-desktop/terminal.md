---
title: GitKraken Terminal Guide
description: Learn how to use GitKraken’s in-app terminal to run Git commands, use auto-complete, and customize shell preferences.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to run Git CLI commands from the GitKraken Desktop terminal while staying in the context of the open repository and commit graph. It covers how to open the terminal, how command and flag auto-complete works, and where to change shell and terminal appearance settings.

To get started, open a repository and click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar, or search for "terminal" using the <a href="/working-with-repositories/command-palette">Command Palette</a>.

***

## Quick Start

Use the GitKraken Desktop terminal to run Git commands alongside the visual commit graph.

**To open the terminal:** Click the Terminal icon in the toolbar or search for "terminal" in the Command Palette.

**To run commands:** Type any Git command such as `git status`, `git commit -m "message"`, or `git log --oneline`. Auto-complete suggestions appear as you type, including flag suggestions for each command.

**To customize terminal appearance:** Go to <kbd>Preferences > In-App Terminal</kbd> to change font, size, line height, cursor style, and autocomplete behavior.

**To set your default shell:**
- **macOS/Linux**: Set ZSH or Bash as the default shell in your OS settings and restart your machine.
- **Windows**: Open <kbd>Preferences > Terminal</kbd> and select PowerShell or Bash.

The terminal shares context with the open repository, so commands run against the correct working directory automatically.

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

## Common Git commands to try

Use the terminal to quickly execute common Git operations:

- `git status` – View working directory and staging status
- `git commit -m "message"` – Commit changes with a message
- `git log --oneline` – View a condensed commit history

These commands complement GitKraken’s visual graph for a comprehensive Git experience.
