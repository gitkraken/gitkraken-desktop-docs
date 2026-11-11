---
title: GitKraken Terminal Guide
description: Use the GitKraken Desktop in-app terminal to run Git commands in the open repository or worktree, manage terminal tabs, run coding agents manually, and customize shell preferences.
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
last_verified: 2026-11
llms_include: true
tags: [terminal, shell, git, commands, auto-complete]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "working-with-repositories"
    nav_label: "Terminal"
    nav_order: 170
    nav_parent: "working-with-repositories"
    page_type: "content"
    card_icon: "terminal-2"
    card_color: "amber"
    card_description: "Run Git commands and coding agents in the in-app terminal"
---
<kbd>Last updated: November 2026</kbd>

Use this page to run commands in the open repository or worktree from the GitKraken Desktop in-app terminal. You can open several terminal tabs, use command and flag autocomplete, keep separate terminals for each worktree, run coding agents manually, and change the shell and terminal appearance.

**Requirements and limits**
- Scope: In-app terminal for the currently open repository or worktree
- Repository context: Commands run in the working directory of the active repository or worktree
- Supported shell note: macOS and Linux use the OS default shell. On Windows, choose PowerShell or Bash in Preferences
- Autocomplete limitation: Conflicting third-party autocomplete tools can disable GitKraken Desktop suggestions
- Settings location: <kbd>Preferences &gt; In-App Terminal</kbd> for appearance and autocomplete behavior
- Terminal tabs: Each repository or worktree keeps its own terminal tabs. Starting an agent session in a worktree with an open terminal starts the agent in a separate tab
- Panel behavior: The embedded terminal resizes when surrounding panels change. You can minimize it and keep the terminal panel header visible. The **Kill All Terminals** trash icon in the panel header ends every terminal for the current repository or worktree
- Focus: The terminal output dims while you work elsewhere in the app. Turn this off with **Dim terminal when unfocused** in <kbd>Preferences &gt; In-App Terminal</kbd>
- Coding agents: You can run supported or unsupported coding agent CLIs manually in the embedded terminal

To get started, open a repository and click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar, or search for "terminal" using the <a href="/working-with-repositories/command-palette">Command Palette</a>.

***

## Quick Start


**To open the terminal:** Click the Terminal icon in the toolbar or search for "terminal" in the Command Palette.

**To run commands:** Type any Git command such as `git status`, `git commit -m "message"`, or `git log --oneline`. Autocomplete suggestions appear as you type, including flag suggestions for each command.

**To open another terminal:** Click the **+** button in the terminal tab bar, or press <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>N</kbd> (<kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>N</kbd> on macOS). Select a tab to switch terminals, or close a tab you no longer need. See [How terminal tabs work](#how-terminal-tabs-work) for all terminal tab shortcuts.

**To run a coding agent manually:** Open the terminal in the worktree you want to use, then start your coding agent CLI there.

**To customize terminal appearance:** Go to <kbd>Preferences > In-App Terminal</kbd> to change font, size, line height, cursor style, whether the terminal dims when unfocused, and autocomplete behavior.

**To minimize the terminal panel:** Click **Minimize Terminal** in the terminal panel header. The panel header stays visible so you can expand the terminal again when you need it.

**To kill all terminals:** Click the **Kill All Terminals** trash icon in the terminal panel header. GitKraken Desktop ends every terminal tab for the current repository or worktree and closes the panel. If 2 or more terminals are open, GitKraken Desktop asks you to confirm first, because any running processes stop. To end a single terminal, close its tab instead.

**To set your default shell:**
- **macOS/Linux**: Set ZSH or Bash as the default shell in your OS settings and restart your machine.
- **Windows**: Open <kbd>Preferences > In-App Terminal</kbd> and select PowerShell or Bash in **Default In-App Terminal**.

The terminal shares context with the open repository or worktree, so commands run against the correct working directory automatically.

<figure>
  <img src="/wp-content/uploads/terminal-button-2025@2x.png"
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing the Terminal button in the top toolbar and an open terminal panel running the git status command.">
  <figcaption style="text-align:center; color:#888">Launch the terminal from the toolbar</figcaption>
</figure>

---

## How Git commands and auto-complete work

Run <a href="https://git-scm.com/" target="_blank">Git</a> commands in the terminal as you would in any shell. Start typing `git` to see autocomplete suggestions for commands.

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
  <figcaption style="text-align:center; color:#888">Flag suggestions for a Git command</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Other autocomplete programs can conflict with the terminal and disable its suggestions. If suggestions do not appear, uninstall or disable those programs.</p>
</div>

---

## How to customize terminal preferences

Open <kbd><strong>Preferences > In-App Terminal</strong></kbd> to change your terminal settings.

**Dim terminal when unfocused** is on by default: the terminal output fades while you work elsewhere in GitKraken Desktop and returns to full brightness when you click back into the terminal. The panel header and tabs stay at full brightness. Clear the checkbox to keep the terminal output at full brightness at all times.

<figure>
  <img src="/wp-content/uploads/terminal-preferences-2025-v2@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop Preferences with In-App Terminal selected, showing Font, Font Size, Line Height, Cursor Style, the Dim terminal when unfocused checkbox highlighted, and the Autocomplete options.">
  <figcaption style="text-align:center; color:#888">Access terminal settings under Preferences</figcaption>
</figure>

### How the default terminal works on macOS and Linux

GitKraken Desktop supports ZSH and Bash. To switch shells:
1. Set the preferred shell as default in your OS settings.
2. Restart your machine to apply changes.

### How the default terminal works on Windows

GitKraken Desktop supports PowerShell and Bash. To change the shell:
1. Open <kbd>Preferences > In-App Terminal</kbd>.
2. Set **Default In-App Terminal** to your desired shell.

---

## How terminal tabs work

The terminal panel supports multiple terminal tabs. Click **+** in the tab bar to open another terminal, then select a tab to switch to it. Each repository or worktree keeps its own set of terminals.

Each tab is named after the app running in it, such as `claude` or `node`, or after the shell when no app is running. Drag a tab to change the order of the tabs. GitKraken Desktop keeps that order for the repository or worktree until you close the app. When you close the last tab, the terminal panel closes.

Use these shortcuts while the terminal panel is open. They are also in the <kbd>View > Terminal Tabs</kbd> menu (<kbd>Window > Terminal Tabs</kbd> on macOS).

| Action | Windows and Linux | macOS |
|---|---|---|
| Open a new terminal tab | <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>N</kbd> | <kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>N</kbd> |
| Close the current terminal tab | <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>W</kbd> | <kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>W</kbd> |
| Select the next terminal tab | <kbd>Ctrl</kbd> + <kbd>Page Down</kbd> | <kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>Right Arrow</kbd> |
| Select the previous terminal tab | <kbd>Ctrl</kbd> + <kbd>Page Up</kbd> | <kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>Left Arrow</kbd> |
| Select terminal tab 1 to 9 | <kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>1</kbd> to <kbd>9</kbd> | <kbd>Cmd</kbd> + <kbd>Option</kbd> + <kbd>1</kbd> to <kbd>9</kbd> |

The next and previous tab shortcuts wrap around: from the last tab, the next tab is the first one.

<figure>
  <img src="/wp-content/uploads/gkd-12-6-terminal-tabs.png"
       class="help-center-img img-bordered"
       alt="GitKraken Desktop terminal panel with three terminal tabs named zsh, zsh, and node, the selected tab showing a close button, and a plus button for opening another terminal.">
  <figcaption style="text-align:center; color:#888">Open, switch between, and close terminal tabs</figcaption>
</figure>

When you switch worktrees, GitKraken Desktop shows that worktree's terminal tabs. Each terminal runs in its worktree's working directory, and long-running commands continue while you switch to another worktree.

When you start a coding agent in a worktree that already has a terminal open, GitKraken Desktop starts the agent in a new tab instead of replacing the existing terminal.

GitKraken Desktop uses the same worktrees in both List view and the [Agents view](/gitkraken-desktop/agents/). You can open a worktree from either view and use its terminal tabs.

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

Drag a file from your OS file manager or from the Commit Panel into the terminal to insert the file's full path at the cursor. You can also drag text into the terminal to insert it at the cursor. Use drag and drop to add a path or snippet to a command without retyping it.

---

## Common Git commands to try

Use the terminal to run common Git operations:

- `git status` - View working directory and staging status
- `git commit -m "message"` - Commit changes with a message
- `git log --oneline` - View a condensed commit history
