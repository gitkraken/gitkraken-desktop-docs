---
title: How to Undo and Redo Git Actions in GitKraken Desktop
description: Undo or redo Git actions like commits, discards, and checkouts in GitKraken Desktop, including cleanup after a coding agent, with buttons or shortcuts.
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
last_verified: 2026-11
llms_include: true
tags: [undo, redo, history, shortcuts, command-palette]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-working-with-commits"
    nav_label: "Undo and Redo Git Actions"
    nav_order: 50
    nav_parent: "desktop-working-with-commits"
    page_type: "content"
    card_icon: "arrow-back-up"
    card_color: "green"
    card_description: "Undo or redo commits, discards and checkouts"
---

<kbd>Last updated: November 2026</kbd>

Use this page to undo or redo Git actions in GitKraken Desktop, such as an accidental commit, a discarded change, or a deleted branch.

To undo a supported action, click the **Undo** button. If you undo something by mistake, you can **redo** it.

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
    <img src="/wp-content/uploads/undo-undo-2025.png"
         class="help-center-img img-bordered"
         alt="GitKraken Desktop showing the Undo button with tooltip: 'Undo Commit amend &quot;Updates the GitKraken commit documentation to reflect UI&quot;'." />
    <figcaption style="color: #888; text-align: center;">Click the Undo button to revert supported Git actions.</figcaption>
</figure>

## Supported undo actions

You can undo the following actions in GitKraken Desktop:

+ Checkout
+ Commit
+ Discard
+ Delete branch
+ Remove remote
+ Reset branch to a commit
+ Rebase operations, including Interactive Rebase, Multi-Commit Cherry Pick, dropping and rewording commits, and AI Commit Compose (Recompose with AI)

If you have uncommitted changes when you undo or redo a reset (such as dropping the latest commit) or a rebase, GitKraken Desktop asks you to stash them first. Click **Yes, Stash Changes** to stash your changes and continue, or **Cancel** to leave everything as it is.

Undo lets you recover from common mistakes without using the command line. To reverse changes a coding agent made, see [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/).

## How redo works

If you undo something accidentally, use **Redo** to restore it. Redo is available for any action you've just undone.

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
