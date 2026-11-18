---
title: Manage Git Submodules in GitKraken Desktop
description: Learn how to add, update, and manage Git submodules in GitKraken Desktop, including how to track commits and enable automatic updates.
product: GitKraken Desktop
feature: Submodules
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
tags: [submodules, git, update, nested-repos, repositories]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to add, update, initialize, and manage Git submodules in GitKraken Desktop when one repository needs to reference another repository at a fixed commit. You can also change the commit the parent repository points to and turn on automatic submodule updates.

## Requirements and limits

- Workflow scope: Git submodules, not Git subtree workflows
- Pane access: Enable the Submodules pane from the Left Panel header menu
- Add workflow: Requires an HTTPS or SSH repository URL and a target path
- Clone behavior: GitKraken Desktop prompts you to initialize submodules when cloning a parent repository that includes them
- Pointer behavior: Changing the tracked commit changes the parent repository's pointer to the submodule commit, which you then commit in the parent repository
- Auto-update settings: Configure globally in <kbd>Preferences &gt; General</kbd> or per repository in <kbd>Preferences &gt; Submodules</kbd>
- Limitation: GitKraken Desktop does not support subtree workflows in-app

| Workflow | Supported in app | Notes |
|----------|------------------|-------|
| Show Submodules pane | Yes | Enable it from the Left Panel header menu |
| Add submodule | Yes | Requires repository URL and target path |
| Initialize submodules after clone | Yes | GitKraken Desktop prompts you when needed |
| Update submodule | Yes | Checks out the commit the parent repository records |
| Configure auto-update | Yes | Available globally or per repository |
| Git subtree workflow | No | Not supported in-app |

***

## Quick Start


**To show the Submodules pane:** Right-click any Left Panel header and check **Submodules**.

**To add a submodule:**
1. Hover over **Submodules** in the Left Panel and click the **+** icon.
2. Paste the HTTPS or SSH repository URL in **Remote URL** and enter the path in **Name/Path**.
3. Click **Add Submodule**. GitKraken Desktop updates `.gitmodules` and references the submodule commit.

**To update a submodule:** Open the Submodules pane, right-click the submodule, and select **Update *[submodule]*** to fetch and check out the commit the parent repository records.

**To change the tracked commit:** Open the submodule in GitKraken Desktop, check out a new commit or branch, then close the submodule. In the parent repository, right-click the submodule and select **Commit Changes** to save the updated pointer.

**To enable automatic updates:** Go to <kbd>Preferences > General</kbd> to update all repos globally, or <kbd>Preferences > Submodules</kbd> for per-repository settings.

When you clone a parent repository that includes submodules, GitKraken Desktop asks whether to initialize them.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/moC2KyxGb10?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## How to enable the Submodules pane

To toggle the Submodules pane:
1. Right-click any pane header in the Left Panel.
2. Check or uncheck **Submodules** to show or hide the pane.

<figure>
  <img src="/wp-content/uploads/toggle-panes-2025@2x.png" 
       alt="GitKraken Desktop Left Panel showing the toggle pane menu with options to show or hide sections like Remote, Pull Requests, Tags, and Submodules" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Toggle the Submodules pane from the Left Panel</figcaption>
</figure>

***

## How to add a submodule

To add a submodule:
1. Hover over <em>Submodules</em> in the Left Panel.
2. Click the <button class='button button--success button--ui button--nolink'>+</button> icon.
3. Paste the HTTPS or SSH repository URL in **Remote URL**.
4. Enter the path in **Name/Path**.
5. Click **Add Submodule**.

<figure>
  <img src="/wp-content/uploads/add-submodule@2x.png" 
       alt="GitKraken Desktop interface showing the Add Submodule modal with fields for Remote URL and Name/Path, and a green Add Submodule button" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Add a submodule using HTTPS or SSH URL</figcaption>
</figure>

Adding a submodule updates the `.gitmodules` file and references the submodule commit.

When you clone the parent repository, GitKraken Desktop asks whether to initialize its submodules, which fetches and checks out each submodule's commit.

***

## How to update a submodule

To update a submodule:
1. Open the Submodules pane.
2. Right-click the submodule.
3. Select <kbd>Update *[submodule]*</kbd>. GitKraken Desktop fetches the submodule if needed and checks out the commit the parent repository records.

<figure>
  <img src="/wp-content/uploads/update-submodule@2x.png" 
       alt="Context menu in GitKraken Desktop showing options to update, edit, open, or delete the submodule vendor/libgit2" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Update a submodule from the Left Panel</figcaption>
</figure>

***

## How to change the pointer commit

To update the tracked commit:
1. Open the submodule in GitKraken Desktop.
2. Check out a new commit or branch.
3. Click **Close Submodule** in the toolbar to return to the parent repository.
4. In the Submodules pane, double-click the submodule to see its out-of-sync status.
5. Click **Commit Changes** to save the updated pointer commit, or **Discard Submodule Changes** to go back to the recorded commit.

Both actions are also in the submodule's right-click menu.

<figure>
  <img src="/wp-content/uploads/submodule-commit@2x.png" 
       alt="GitKraken Desktop interface showing submodule vendor/libgit2 out-of-sync, with options to commit or discard changes, and view or delete the submodule" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Update the pointer commit for a submodule</figcaption>
</figure>

***

## What submodule statuses mean

Possible submodule states and how to resolve them:

- **Out of sync**: The pointer commit changed. Commit or discard the change. A stash does not save a submodule's pointer or the changes inside it.
- **Added but not initialized**: Right-click the submodule and select <kbd>Initialize *[submodule]*</kbd>.
- **Added and initialized but not committed**: Commit the submodule folder and update `.gitmodules`.

Before an action that can move or reset your submodules, such as a checkout, rebase, reset, or undo, GitKraken Desktop checks them and asks first:

- **A submodule is checked out at a commit that is not staged**: The action can move the submodule back to the commit the repository records, which leaves a commit made only in the submodule on no branch. Click **Stage and Continue** to stage the submodule's commit first, **Continue** to go on without staging, or **Cancel**. If the action would move the submodule back even after staging, only **Continue** and **Cancel** appear.
- **A submodule has changes that will be lost**: With **Keep submodules up to date** on, **Discard all changes**, a hard reset, and some undo and redo actions throw away edits inside a submodule. GitKraken Desktop names each affected submodule. Click **Continue** to go on or **Cancel** to keep the edits. Undo cannot bring them back.
- **A submodule has a merge conflict**: GitKraken Desktop cannot stash your changes and stops the action with **Error Creating Stash**. Resolve the conflict, then try again.

***

<a name="keep-submodules-up-to-date"></a>

## How to keep submodules up to date

Turn on **Keep submodules up to date** to update all submodules automatically after each Git action. You can set it in 2 places:
- Globally: <kbd>Preferences > General</kbd>
- Per repository: <kbd>Preferences > Submodules</kbd>, where you can also choose **Use global setting**

***

## Subtree support

GitKraken Desktop does **not** support subtree workflows in-app.
