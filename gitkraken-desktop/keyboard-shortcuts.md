---
title: GitKraken Desktop Keyboard Shortcuts | Speed Up Your Git Workflow
description: Keyboard shortcuts for GitKraken Desktop on macOS, Windows, and Linux, for staging, committing, navigating the Commit Graph, and managing tabs and terminal tabs.
product: GitKraken Desktop
feature: Keyboard Shortcuts
content_type: reference
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [keyboard-shortcuts, shortcuts, navigation, command-palette, tabs]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use these keyboard shortcuts to work in GitKraken Desktop on macOS, Windows, and Linux without leaving the keyboard. They cover staging, committing, navigating the Commit Graph, opening the Command Palette, managing tabs, toggling interface panels, and opening the terminal.

**Requirements and limits**
- Shortcuts differ between macOS and Windows/Linux, so check the column for your platform before using a shortcut.
- A shortcut works only when its view or repository is open.

<blockquote><strong>Note:</strong> The <kbd>&#8984;</kbd> symbol refers to the <strong>Command</strong> key on macOS.</blockquote>

***

## How to open the keyboard shortcuts list

<table class='table table--bordered table--shortcuts'>
  <colgroup>
    <col style="width: 44%;">
    <col style="width: 28%;">
    <col style="width: 28%;">
  </colgroup>
  <thead>
    <tr>
      <th scope="col">Action</th>
      <th scope="col">Mac</th>
      <th scope="col">Windows/Linux</th>
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

## Keyboard shortcuts for repo actions
<table class='table table--bordered table--shortcuts'>
    <colgroup>
        <col style="width: 44%;">
        <col style="width: 28%;">
        <col style="width: 28%;">
    </colgroup>
    <thead>
        <tr>
            <th>Action</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Create branch</td>
            <td><kbd>&#8984;</kbd><kbd>B</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>B</kbd></td>
        </tr>
        <tr>
            <td>Fetch all</td>
            <td><kbd>&#8984;</kbd><kbd>L</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>L</kbd></td>
        </tr>
        <tr>
            <td>Stage the current file</td>
            <td><kbd>S</kbd></td>
            <td><kbd>S</kbd></td>
        </tr>
        <tr>
            <td>Stage all files</td>
            <td><kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>S</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>S</kbd></td>
        </tr>
        <tr>
            <td>Unstage the current file</td>
            <td><kbd>U</kbd></td>
            <td><kbd>U</kbd></td>
        </tr>
        <tr>
            <td>Unstage all files</td>
            <td><kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>U</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>U</kbd></td>
        </tr>
        <tr>
            <td>Commit staged files with current message</td>
            <td><kbd>&#8984;</kbd><kbd>Enter</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Enter</kbd></td>
        </tr>
        <tr>
            <td>Stage all files and commit with current message</td>
            <td><kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>Enter</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>Enter</kbd></td>
        </tr>
        <tr>
            <td>Focus commit message box</td>
            <td><kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>M</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>M</kbd></td>
        </tr>
    </tbody>
</table>

### Keyboard shortcuts for navigation
<table class='table table--bordered table--shortcuts'>
    <colgroup>
        <col style="width: 44%;">
        <col style="width: 28%;">
        <col style="width: 28%;">
    </colgroup>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Select previous item</td>
            <td><kbd>K</kbd> or <kbd>&uarr;</kbd></td>
            <td><kbd>K</kbd> or <kbd>&uarr;</kbd></td>
        </tr>
        <tr>
            <td>Select next item</td>
            <td><kbd>J</kbd> or <kbd>&darr;</kbd></td>
            <td><kbd>J</kbd> or <kbd>&darr;</kbd></td>
        </tr>
        <tr>
            <td>Select the item to the right</td>
            <td><kbd>L</kbd> or <kbd>&rarr;</kbd></td>
            <td><kbd>L</kbd> or <kbd>&rarr;</kbd></td>
        </tr>
        <tr>
            <td>Select the item to the left</td>
            <td><kbd>H</kbd> or <kbd>&larr;</kbd></td>
            <td><kbd>H</kbd> or <kbd>&larr;</kbd></td>
        </tr>
        <tr>
            <td>Select next item in branch</td>
            <td><kbd>Shift</kbd><kbd>&darr;</kbd><br>
            <kbd>Shift</kbd><kbd>J</kbd></td>
            <td><kbd>Shift</kbd><kbd>&darr;</kbd><br>
            <kbd>Shift</kbd><kbd>J</kbd></td>
        </tr>
        <tr>
            <td>Select previous item in branch</td>
            <td><kbd>Shift</kbd><kbd>&uarr;</kbd><br>
            <kbd>Shift</kbd><kbd>K</kbd></td>
            <td><kbd>Shift</kbd><kbd>&uarr;</kbd><br>
            <kbd>Shift</kbd><kbd>K</kbd></td>
        </tr>
        <tr>
            <td>Select first commit in graph</td>
            <td><kbd>&#8984;</kbd><kbd>&uarr;</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>HOME</kbd></td>
        </tr>
        <tr>
            <td>Select last commit in graph</td>
            <td><kbd>&#8984;</kbd><kbd>&darr;</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>END</kbd></td>
        </tr>
        <tr>
            <td>Undo</td>
            <td><kbd>&#8984;</kbd><kbd>Z</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Z</kbd></td>
        </tr>
        <tr>
            <td>Redo</td>
            <td><kbd>&#8984;</kbd><kbd>Y</kbd><br>
            <kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>Z</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Y</kbd><br>
            <kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>Z</kbd></td>
        </tr>
    </tbody>
</table>

### Keyboard shortcuts for the Command Palette
<table class='table table--bordered table--shortcuts'>
    <colgroup>
        <col style="width: 44%;">
        <col style="width: 28%;">
        <col style="width: 28%;">
    </colgroup>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
         <tr>
            <td>Toggle Command Palette</td>
            <td><kbd>&#8984;</kbd><kbd>P</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>P</kbd></td>
        </tr>
        <tr>
            <td>Search commits</td>
            <td><kbd>&#8984;</kbd><kbd>F</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>F</kbd></td>
        </tr>
        <tr>
            <td>Open repo via Command Palette</td>
            <td><kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>O</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>O</kbd></td>
        </tr>
        <tr>
            <td>Search file to view history and blame</td>
            <td><kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>H</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>H</kbd></td>
        </tr>
        <tr>
            <td>Focus the Left Panel filter bar</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>F</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Alt</kbd><kbd>F</kbd></td>
        </tr>
        <tr>
            <td>Open current repo in default terminal</td>
            <td><kbd>Option</kbd><kbd>T</kbd></td>
            <td><kbd>Alt</kbd><kbd>T</kbd></td>
        </tr>
        <tr>
            <td>Open current repo in File Manager</td>
            <td><kbd>Option</kbd><kbd>O</kbd></td>
            <td><kbd>Alt</kbd><kbd>O</kbd></td>
        </tr>
        <tr>
            <td>Open diff or merge tool</td>
            <td><kbd>&#8984;</kbd><kbd>D</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>D</kbd></td>
        </tr>
        <tr>
            <td>Close current repo</td>
            <td><kbd>&#8984;</kbd><kbd>W</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>W</kbd></td>
        </tr>
        <tr>
            <td>Search within file (if file content has focus)</td>
            <td><kbd>&#8984;</kbd><kbd>F</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>F</kbd></td>
        </tr>
    </tbody>
</table>

**Open current repo in default terminal** opens the current repository in your external terminal. To run commands or manual coding agent workflows in the in-app terminal for the current repository or worktree, see [GitKraken Terminal Guide](/gitkraken-desktop/terminal/).

### Keyboard shortcuts for the interface
<table class='table table--bordered table--shortcuts'>
    <colgroup>
        <col style="width: 44%;">
        <col style="width: 28%;">
        <col style="width: 28%;">
    </colgroup>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Toggle Full Screen</td>
            <td><kbd>Control</kbd><kbd>&#8984;</kbd><kbd>F</kbd></td>
            <td><kbd>F11</kbd></td>
        </tr>
        <tr>
            <td>Increase Zoom</td>
            <td><kbd>&#8984;</kbd><kbd>&equals;</kbd><br>
            <kbd>&#8984;</kbd><kbd>&plus;</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>&equals;</kbd><br>
            <kbd>Ctrl</kbd><kbd>&plus;</kbd></td>
        </tr>
        <tr>
            <td>Decrease Zoom</td>
            <td><kbd>&#8984;</kbd><kbd>&minus;</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>&minus;</kbd></td>
        </tr>
        <tr>
            <td>Reset Zoom</td>
            <td><kbd>&#8984;</kbd><kbd>0</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>0</kbd></td>
        </tr>
        <tr>
            <td>Toggle the Left Panel</td>
            <td><kbd>&#8984;</kbd><kbd>J</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>J</kbd></td>
        </tr>
        <tr>
            <td>Toggle the Commit Detail panel</td>
            <td><kbd>&#8984;</kbd><kbd>K</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>K</kbd></td>
        </tr>
        <tr>
            <td>Focus the search bar</td>
            <td><kbd>&#8984;</kbd><kbd>F</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>F</kbd></td>
        </tr>
        <tr>
            <td>Focus the Left Panel filter bar</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>F</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Alt</kbd><kbd>F</kbd></td>
        </tr>
        <tr>
            <td>Close the current panel (if one is open)</td>
            <td><kbd>Esc</kbd></td>
            <td><kbd>Esc</kbd></td>
        </tr>
    </tbody>
</table>

### Keyboard shortcuts for tabs
<table class='table table--bordered table--shortcuts'>
    <colgroup>
        <col style="width: 44%;">
        <col style="width: 28%;">
        <col style="width: 28%;">
    </colgroup>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>New Tab</td>
            <td><kbd>&#8984;</kbd><kbd>T</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>T</kbd></td>
        </tr>
        <tr>
            <td>Close Tab</td>
            <td><kbd>&#8984;</kbd><kbd>W</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>W</kbd></td>
        </tr>
        <tr>
            <td>Switch to tab 1-9</td>
            <td><kbd>&#8984;</kbd><kbd>#1-9</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>#1-9</kbd></td>
        </tr>
        <tr>
            <td>Jump to next open tab</td>
            <td><kbd>Control</kbd><kbd>Tab</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Tab</kbd></td>
        </tr>
        <tr>
            <td>Jump to previous open tab</td>
            <td><kbd>Control</kbd><kbd>Shift</kbd><kbd>Tab</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>Tab</kbd></td>
        </tr>
        <tr>
            <td>Focus the repository search on a New Tab</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>F</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Alt</kbd><kbd>F</kbd></td>
        </tr>
    </tbody>
</table>

On a New Tab, the repository search box shows this shortcut in its placeholder text.

### Keyboard shortcuts for terminal tabs
<table class='table table--bordered table--shortcuts'>
    <colgroup>
        <col style="width: 44%;">
        <col style="width: 28%;">
        <col style="width: 28%;">
    </colgroup>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>New terminal tab</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>N</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>N</kbd></td>
        </tr>
        <tr>
            <td>Close terminal tab</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>W</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>W</kbd></td>
        </tr>
        <tr>
            <td>Jump to the next terminal tab</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>&rarr;</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Page Down</kbd></td>
        </tr>
        <tr>
            <td>Jump to the previous terminal tab</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>&larr;</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Page Up</kbd></td>
        </tr>
        <tr>
            <td>Jump to terminal tab 1-9</td>
            <td><kbd>&#8984;</kbd><kbd>Option</kbd><kbd>#1-9</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>#1-9</kbd></td>
        </tr>
    </tbody>
</table>

Terminal tab shortcuts work while the terminal panel is open. The same actions are in the <kbd>View > Terminal Tabs</kbd> menu on Windows and Linux, and in <kbd>Window > Terminal Tabs</kbd> on macOS. For more information, see [How terminal tabs work](/gitkraken-desktop/terminal/#how-terminal-tabs-work).
