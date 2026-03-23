---
title: Branch, Merge, and Rebase in GitKraken Desktop
description: Learn how to create branches, merge code, and rebase commits using GitKraken Desktop. Includes merge conflict resolution and external tool setup.
product: GitKraken Desktop
feature: Branching and Merging
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
tags: [branches, merge, rebase, conflicts, squash]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to create, rename, delete, merge, and rebase branches in GitKraken Desktop. It also covers merge conflict resolution, external merge tools, and the difference between merge-based and rebase-based workflows so you can choose the right history strategy for your branch.

**Key constraints**
- Merge strategy: Use merge to preserve branch history; use rebase to move commits onto a new base and keep history more linear
- Merge conflict editor: The in-app merge conflict output editor requires a paid GitKraken license
- Squash merge behavior: With **Squash** enabled, GitKraken Desktop stages the merge result but does not create the final commit automatically
- Branch deletion: Deleting a branch is permanent
- External merge tools: Review the supported and unsupported tool lists before relying on a third-party merge tool

| Action | Use when | Preserves branch history | Rewrites history | Notes |
|--------|----------|--------------------------|------------------|-------|
| Branch | You need isolated work for a feature, fix, or experiment | Yes | No | Can be renamed or deleted later |
| Merge | You want to combine branches and keep the branch structure visible | Yes | No | May create a merge commit |
| Rebase | You want a more linear history before sharing or merging | No | Yes | Replays commits onto a new base |
| Squash merge | You want one final commit from a branch's combined changes | Partial | Yes | Stages the result but does not create the final commit automatically |

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8-qRKyy-v7I?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

Looking for a quick summary? See [how GitKraken solves merge conflicts](https://www.gitkraken.com/developer-problems/merge-conflicts?product=gitkraken&source=help_center).

***

## Quick Start


**To create and check out a branch:**
1. Right-click any commit in the graph and select **Create branch here**.
2. Enter a branch name and press <kbd>Enter</kbd>.
3. Double-click the branch label in the graph or Left Panel to check it out.

**To merge a branch:**
1. Check out the branch you want to merge into.
2. Right-click the source branch in the Left Panel and select **Merge**, or drag and drop it onto the target branch.
3. If conflicts occur, click a conflicted file in the Commit Panel to open the Merge Tool. Select lines from each side, save the output, and commit.

**To rebase:**
1. Drag the source branch onto the target branch and select **Rebase**.
2. Resolve any conflicts if prompted, then confirm.

To delete a branch, first check out a different branch, then right-click the target branch and select **Delete**. Use <kbd>Shift</kbd> or <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> in the Left Panel to select and delete multiple branches at once.

***

## How to create and manage branches

Create a new branch when working on a feature or fix. Right-click any commit to open the context menu and create a branch.

<div class='callout callout--basic'>
  <p><strong>Use branches when:</strong> you want to isolate a feature, fix, or experiment from the main line of development. <strong>Don't keep branches around when:</strong> the work is complete and the branch can be merged or deleted to reduce graph clutter.</p>
</div>

<figure>
  <img src="/wp-content/uploads/add-branch@2x.png" class="help-center-img img-bordered" alt="Right-click menu in GitKraken Desktop showing option to create a new branch from a selected commit">
  <figcaption style="text-align:center; color:#888">Create a branch by right-clicking on a commit</figcaption>
</figure>

A branch is a pointer to a specific commit, allowing you to isolate changes from the main codebase. Consider adopting [GitFlow](/git-workflows-and-extensions/git-flow) for structured branching strategies.

### How to check out a branch

Branch checkout updates files in the working directory to reflect the version defined by that branch.

To update your working directory:
- Double-click a branch label from the Commit Graph or the Left Panel
- Right-click a branch from the Commit Graph or the Left Panel and select **Checkout**

<figure>
  <img src="/wp-content/uploads/add-branch-2025.gif" class="help-center-img img-bordered" alt="Animated view of creating and checking out a new branch in GitKraken Desktop from the right-click context menu on a commit">
  <figcaption style="text-align:center; color:#888">Creating and checking out a new branch</figcaption>
</figure>

If you’re on the wrong branch, [stash](/gitkraken-desktop/stashing) your changes, switch branches, and pop the stash.

If you only need a subset of files checked out, see [Sparse Checkout](/gitkraken-desktop/open-clone-init/#sparse-checkout).

### How to rename a branch

Right-click the branch label or use the Left Panel to rename the current branch.

<figure>
  <img src="/wp-content/uploads/rename-branch@2x.png" class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop with the Rename branch option selected for the branch 'branch-rename'">
  <figcaption style="text-align:center; color:#888">Rename a branch from the graph or Left Panel</figcaption>
</figure>

You can also rename using the Command Palette (Cmd+P / Ctrl+P):

<figure>
  <img src="/wp-content/uploads/rename-branch-command-palette@2x.png" class="help-center-img img-bordered" alt="Command Palette in GitKraken Desktop showing filtered results for 'Rename Branch'">
  <figcaption style="text-align:center; color:#888">Search for "Rename Branch" in Command Palette</figcaption>
</figure>

### How to delete a branch

To delete a branch:
1. Switch to another branch
2. Right-click the branch you wish to delete

Use multi-select in the Left Panel to delete several branches at once:
- <kbd>Shift</kbd> to select a range
- <kbd>&#8984;</kbd> / <kbd>Ctrl</kbd> to select specific branches

<figure>
  <img src="/wp-content/uploads/multi-delete-branches.gif" class="help-center-img img-bordered" alt="Confirmation prompt for deleting multiple local branches in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Select and delete multiple branches</figcaption>
</figure>

<div class='callout callout--warning'>
  <p><strong>Caution:</strong> Deleting a branch is permanent.</p>
</div>

### How to pin a branch to the left

Pinning a branch fixes it to the left side of the Commit Graph so that its direct commit history always appears on the left. This is particularly useful for long-lived branches like `main` or a production branch, where you want a stable reference point to see how other branches merge into it.

To pin a branch:
1. Right-click a branch label in the Commit Graph or the Left Panel.
2. Select **Pin to left**.

<figure>
  <img src="/wp-content/uploads/pin-to-left.png" class="help-center-img img-bordered" alt="Right-click context menu on a branch in the GitKraken Desktop Commit Graph with the 'Pin to Left' option visible at the bottom of the menu">
  <figcaption style="text-align:center; color:#888">Select "Pin to Left" from the branch context menu</figcaption>
</figure>

To unpin a branch, right-click the branch label again and select **Unpin from left**.

### When to use Smart Branch Visibility

Smart Branch Visibility reduces visual noise in the Commit Graph by displaying only the branches most relevant to your current work. When enabled, the graph shows only your checked-out branch, its target branch, and their respective upstream branches — hiding all others.

This is especially useful in repositories with a large number of branches where the full graph can be difficult to navigate.

To enable Smart Branch Visibility:
1. Click the gear icon in the top-right corner of the Commit Graph header.
2. Select **Smart Branch Visibility**.

<figure>
  <img src="/wp-content/uploads/smart-visibility.png" class="help-center-img img-bordered" alt="GitKraken Desktop Commit Graph with Smart Branch Visibility enabled, showing a filtered branch list in the Left Panel and the column settings dropdown with the Smart Branch Visibility option checked">
  <figcaption style="text-align:center; color:#888">Enable Smart Branch Visibility from the Commit Graph column settings</figcaption>
</figure>

Smart Branch Visibility activates on your currently checked-out branch. To disable it, follow the same steps and deselect **Smart Branch Visibility**.
***

## How to merge branches

Merging combines changes from one branch into another. To merge:
- Drag and drop one branch onto your target branch
- Or right-click the source branch and choose **Merge**

<div class='callout callout--basic'>
  <p><strong>Use merge when:</strong> you want to preserve the full branch history. <strong>Use rebase when:</strong> you want to move commits onto a new base and keep the history more linear before sharing or merging.</p>
</div>

<div class='callout callout--basic'>
  <p><strong>Don't use merge when:</strong> your team expects a rebased, linear branch before review or integration. <strong>Don't use rebase when:</strong> collaborators are already building on the commits you plan to rewrite.</p>
</div>

<figure>
  <img src="/wp-content/uploads/merge-right@2x.png" class="help-center-img img-bordered" alt="Context menu showing option to merge dev branch into production branch in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Merge via drag-and-drop or right-click</figcaption>
</figure>

If no conflicts exist, changes will be merged automatically.

<div class='callout callout--warning'>
  <p>The in-app merge conflict output editor is available with a <a href="https://gitkraken.com/pricing?product=gitkraken&source=help_center" target="_blank">Paid</a> license.</p>
</div>

### When to use squash merges

When you enable the **Squash** setting, GitKraken Desktop stages all changes from the source branch locally without creating a merge commit automatically. You then commit the squashed result manually, which produces a single, clean commit on the target branch.

<div class='callout callout--basic'>
  <p><strong>Use squash merges when:</strong> you want one clean commit on the target branch and do not need to preserve each feature-branch commit. <strong>Don't use squash when:</strong> the individual commits matter for auditing, review context, or future debugging.</p>
</div>

This is useful when you want to maintain a linear history on your main branch without preserving the individual commits from a feature branch.

To enable squash merges:
1. Go to **Preferences** > **Commit**.
2. Enable the **Squash** toggle.

<figure>
  <img src="/wp-content/uploads/squash-merge.png" class="help-center-img img-bordered" alt="GitKraken Desktop Preferences panel open to the Commit section, with the Merge Behavior area highlighted showing the Squash checkbox and its description: 'When enabled, merging branches locally will stage all changes without creating a merge commit automatically. You will need to commit manually.'">
  <figcaption style="text-align:center; color:#888">Enable the Squash toggle under Preferences > Commit > Merge Behavior</figcaption>
</figure>

After merging with squash enabled, review the staged changes in the Commit Panel and commit them manually.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> With squash enabled, GitKraken Desktop stages all changes but does not create the merge commit for you. You must commit manually to complete the merge.</p>
</div>

### How to resolve conflicts in the Merge Conflict Editor

When conflicts occur, the Commit Panel shows the conflicted files. Click a file to open the Merge Tool.

<figure>
  <img src="/wp-content/uploads/merge-conflict@2x.png" class="help-center-img img-bordered" alt="GitKraken merge conflict interface showing conflicting file test.txt when merging origin/test-merge-pr into multi-conflict-left">
  <figcaption style="text-align:center; color:#888">Conflicted files shown in Commit Panel</figcaption>
</figure>

The Merge Tool shows:
- Current branch on the left
- Target branch on the right
- Output at the bottom

<figure>
  <img src="/wp-content/uploads/merge-tool2@2x.png" class="help-center-img img-bordered" alt="Screenshot of GitKraken's merge conflict tool showing side-by-side comparison of conflicting lines in glo/calendar.md">
  <figcaption style="text-align:center; color:#888">Review and resolve conflicts in the Merge Tool</figcaption>
</figure>

Use checkboxes or click <button class='button button--success button--ui button--nolink'>+</button> to select lines. Use arrow keys to navigate conflicts.

<figure>
  <img src="/wp-content/uploads/merge-tool-toggle.gif" class="help-center-img img-bordered" alt="GIF showing GitKraken's merge tool with the ability to select specific changes from each side to resolve merge conflicts.">
  <figcaption style="text-align:center; color:#888">Select specific lines or edit output directly</figcaption>
</figure>

After resolving, save and commit the output.

<div class='callout callout--basic'>
  <p><strong>Tip:</strong> Use <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>F</kbd> to search inside the Merge Tool.</p>
</div>

<figure>
  <img src="/wp-content/uploads/merge-tool-gif.gif" class="help-center-img img-bordered" alt="GIF showing animated merge conflict resolution process in GitKraken, selecting changes from both sides.">
  <figcaption style="text-align:center; color:#888">Animated merge resolution process</figcaption>
</figure>

### How to use an external merge tool

Set your preferred merge tool under <em>Preferences > General</em>.

<div class='callout callout--basic'>
  <p><strong>Use the built-in merge tool when:</strong> you want to stay inside GitKraken Desktop and the supported editor meets your needs. <strong>Use an external merge tool when:</strong> your team already relies on a supported third-party tool or you need a workflow GitKraken does not provide directly.</p>
</div>

Supported tools:
- Beyond Compare
- FileMerge
- Kaleidoscope
- KDiff
- Araxis
- P4Merge

<figure>
  <img src="/wp-content/uploads/configureExternalTool@2x.png" class="help-center-img img-bordered" alt="Preferences panel showing merge tool selection dropdown with Kaleidoscope selected.">
  <figcaption style="text-align:center; color:#888">Select a merge tool in Preferences</figcaption>
</figure>

If not appearing, ensure command line tools are installed:

<figure>
  <img src="/wp-content/uploads/beyond-compare@2x.png" class="help-center-img img-bordered" alt="Beyond Compare application menu showing the Install Command Line Tools option.">
  <figcaption style="text-align:center; color:#888">Sample view of configured merge tool</figcaption>
</figure>

Unsupported tools include:
- Meld
- SemanticMerge
- TortoiseMerge
- WinMerge

For compatibility details, visit [Git Config merge tools](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#_external_merge_tools).

### How to resolve conflicts with Take Current or Take Incoming

Right-click a conflicted file and select:
- `Take current (branch)` – Use your current branch’s changes
- `Take incoming (branch)` – Use changes from the incoming branch

<figure>
  <img src="/wp-content/uploads/current-incoming.png" class="help-center-img img-bordered" alt="Merge conflict resolution menu with options to take the current branch (branch-2) or the incoming branch (branch-1).">
  <figcaption style="text-align:center; color:#888">Quick resolve using current or incoming options</figcaption>
</figure>

***

## How Conflict Prevention works

GitKraken Desktop’s **Conflict Prevention** helps identify potential issues before a merge.

[Learn more →](/gitkraken-desktop/conflict-prevention/)

<div class='callout callout--warning'>
  <p>Available to users on the Advanced tier or higher.</p>
</div>

***

## How to rebase commits

Rebasing moves commits from one branch onto another for a cleaner history.

<div class='embed-container embed-container--16-9'>
<iframe width="560" height="315" src="https://www.youtube.com/embed/xot40u-_1FI" frameborder="0" allowfullscreen></iframe>
</div>

To rebase:
- Drag and drop the source branch onto the target branch
- Select <kbd>Rebase</kbd> from the menu

<figure>
  <img src="/wp-content/uploads/select-rebase@2x.png" class="help-center-img img-bordered" alt="Rebase menu with the option to rebase the testfill2 branch onto origin/develop.">
  <figcaption style="text-align:center; color:#888">Rebase one branch onto another</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/select-rebase-sidebar@2x.png" class="help-center-img img-bordered" alt="Sidebar context menu showing options to fast-forward, merge, or rebase the testfill2 branch onto master.">
  <figcaption style="text-align:center; color:#888">Sidebar shows rebase confirmation</figcaption>
</figure>

Rebasing rewrites history but results in a more linear and readable commit tree.

### How to rebase a range of commits onto another branch

You can rebase a specific range of commits onto another branch without performing a full interactive rebase. This is useful when you want to move only a subset of commits from your current branch onto a target branch.

GitKraken Desktop provides two ways to do this:

**Option 1: Multi-select a range of commits**
1. Check out the target branch.
2. In the Commit Graph, hold <kbd>Shift</kbd> and click to select a range of commits on the source branch.
3. Right-click the base branch and select **Rebase X commits onto [branch]**.

<figure>
  <img src="/wp-content/uploads/rebase-N-commits.png" class="help-center-img img-bordered" alt="GitKraken Desktop Commit Graph showing a right-click context menu on a branch with the 'Rebase 4 commits onto gitkraken/main' option highlighted, after a range of commits has been selected">
  <figcaption style="text-align:center; color:#888">Right-click the target branch after selecting a commit range to rebase</figcaption>
</figure>

**Option 2: Select a single pivot commit**
1. Select one commit in the middle of your current branch. No merge commits should exist between the selected commit and the head of the branch.
2. Right-click the target branch.
3. Select **Rebase N commits onto [branch]**.

GitKraken Desktop rebases the selected commit and all subsequent commits up to the branch head onto the target branch.
