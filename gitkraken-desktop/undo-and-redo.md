---
title: How to Undo and Redo Git Actions in GitKraken Desktop
description: Learn how to quickly undo or redo Git actions like commits, discards, and checkouts in GitKraken Desktop using buttons, shortcuts, or the Command Palette.
product: GitKraken Desktop
feature: Undo and Redo
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
tags: [undo, redo, history, shortcuts, command-palette]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Have you ever made a Git change and immediately wished you could take it back? Whether it’s an accidental commit, a discarded change, or a deleted branch, GitKraken Desktop lets you undo many actions quickly and safely.

You can undo many common actions with a single click of the **Undo** button. If you undo something by mistake, you can also **redo** it just as easily.

**Requirements and limits**
- Undo scope: The most recent supported action only
- Redo scope: Only actions that were just undone
- Supported actions include checkout, commit, discard, delete branch, remove remote, reset branch, and several rebase-related operations
- Access methods: Toolbar buttons or keyboard shortcuts
- Availability depends on whether the last action is one GitKraken Desktop can safely track and reverse

***

## Quick Start


**To undo an action:** Click the **Undo** button in the toolbar, or press <kbd>Cmd + Z</kbd> (Mac) or <kbd>Ctrl + Z</kbd> (Windows/Linux).

**To redo an undone action:** Press <kbd>Cmd + Y</kbd> or <kbd>Cmd + Shift + Z</kbd> (Mac), or <kbd>Ctrl + Y</kbd> or <kbd>Ctrl + Shift + Z</kbd> (Windows/Linux).

**Supported undo actions include:** Checkout, Commit, Discard, Delete branch, Remove remote, Reset branch to a commit, and rebase operations including Interactive Rebase, Multi-Commit Cherry Pick, dropping and rewording commits, and AI Commit Compose.

Undo is available for the most recent supported action. Redo is available for any action that was just undone.

<figure>
    <img src=’/wp-content/uploads/undo-undo-2025.png’
         class=”help-center-img img-bordered”
         alt=”GitKraken Desktop showing the Undo button with tooltip: ‘Undo Commit amend “Updates the GitKraken commit documentation to reflect UI”’.”>
    <figcaption style=”color: #888; text-align: center;”>Click the Undo button to revert supported Git actions.</figcaption>
</figure>

## Supported undo actions

You can undo the following actions in GitKraken Desktop:

+ Checkout
+ Commit
+ Discard
+ Delete branch
+ Remove remote
+ Reset branch to a commit
+ Rebase operations, including Interactive Rebase, Multi-Commit Cherry Pick, dropping and rewording commits, and AI Commit Compose (Recompose with AI).

These undo actions can help you recover from common missteps without going to the command line.

## How redo works

If you undo something accidentally, use the **Redo** function to restore it. Redo is available for any action you've just undone.

## Keyboard shortcuts

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
            <td>Undo</td>
            <td><kbd>&#8984;</kbd><kbd>Z</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Z</kbd></td>
        </tr>
        <tr>
            <td>Redo</td>
            <td><kbd>&#8984;</kbd><kbd>Y</kbd><br><kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>Z</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>Y</kbd><br><kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>Z</kbd></td>
        </tr>
    </tbody>
</table>

Use these shortcuts to move faster and stay in your flow while working in GitKraken Desktop.
