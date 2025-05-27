---
title: Terminal
description: A Git-enhanced terminal experience with GitKraken’s powerful visual Git commit graph
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

Open the Terminal to run Git CLI commands while viewing the Commit Graph.

To get started, open a repository and click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar, or search for "terminal" using the <a href="/working-with-repositories/command-palette">Command Palette</a>.

<figure>
  <img src="/wp-content/uploads/terminal-button-2025.png" srcset="/wp-content/uploads/terminal-button-2025@2x.png" class="help-center-img img-bordered" alt="Terminal button in GitKraken toolbar">
  <figcaption style="text-align:center; color:#888">Launch the terminal from the GitKraken toolbar</figcaption>
</figure>

---

## Git Commands and Auto-complete

The GitKraken Terminal supports most <a href="https://git-scm.com/" target="_blank">Git</a> commands. Start typing `git` to see command suggestions via auto-complete.

<figure>
  <img src="/wp-content/uploads/autocomplete-suggestions.png" class="help-center-img img-bordered" alt="Auto-complete suggestions for Git commands">
  <figcaption style="text-align:center; color:#888">Git commands appear in auto-complete suggestions</figcaption>
</figure>

Flag suggestions are also supported:

<figure>
  <img src="/wp-content/uploads/autocomplete-suggestions-flags.png" class="help-center-img img-bordered" alt="Auto-complete for Git command flags">
  <figcaption style="text-align:center; color:#888">Flag suggestions enhance Git command efficiency</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Conflicting auto-complete programs may disable suggestions. You may need to uninstall or disable such programs for GitKraken's suggestions to work correctly.</p>
</div>

---

## Customize Terminal Preferences

Visit <kbd><strong>Preferences > In-app Terminal</strong></kbd> to modify your terminal settings.

<figure>
  <img src="/wp-content/uploads/terminal-preferences-2025.png" srcset="/wp-content/uploads/terminal-preferences-2025@2x.png" class="help-center-img img-bordered" alt="Terminal preferences in GitKraken">
  <figcaption style="text-align:center; color:#888">Access terminal settings under Preferences</figcaption>
</figure>

### Default Terminal on macOS and Linux

GitKraken supports ZSH and Bash. To switch shells:
1. Set the preferred shell as default in your OS settings.
2. Restart your machine to apply changes.

### Default Terminal on Windows

PowerShell and Bash are currently supported. To change the shell:
1. Open <kbd>Preferences > Terminal</kbd>.
2. Set the _Default Terminal_ to your desired shell.

---

## Tip: Try Common Git Commands

Use the terminal to quickly execute common Git operations:

- `git status` – View working directory and staging status
- `git commit -m "message"` – Commit changes with a message
- `git log --oneline` – View a condensed commit history

These commands complement GitKraken’s visual graph for a comprehensive Git experience.
