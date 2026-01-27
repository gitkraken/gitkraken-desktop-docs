---
title: Branch, Merge, and Rebase in GitKraken Desktop
description: Learn how to create branches, merge code, and rebase commits using GitKraken Desktop. Includes merge conflict resolution and external tool setup.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

Learn how to branch, merge, and rebase in GitKraken Desktop.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8-qRKyy-v7I?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

Looking for a quick summary? See [how GitKraken solves merge conflicts](https://www.gitkraken.com/developer-problems/merge-conflicts?product=gitkraken&source=help_center).

***

## Branches

Create a new branch when working on a feature or fix. Right-click any commit to open the context menu and create a branch.

<figure>
  <img src="/wp-content/uploads/add-branch-2025.png" srcset="/wp-content/uploads/add-branch@2x.png 2x" class="help-center-img img-bordered" alt="Right-click menu in GitKraken Desktop showing option to create a new branch from a selected commit">
  <figcaption style="text-align:center; color:#888">Create a branch by right-clicking on a commit</figcaption>
</figure>

A branch is a pointer to a specific commit, allowing you to isolate changes from the main codebase. Consider adopting [GitFlow](/git-workflows-and-extensions/git-flow) for structured branching strategies.

### Checkout a Branch

Branch checkout updates files in the working directory to reflect the version defined by that branch.

To update your working directory:
- Double-click a branch label from the Commit Graph or the Left Panel
- Right-click a branch from the Commit Graph or the Left Panel and select **Checkout**

<figure>
  <img src="/wp-content/uploads/add-branch-2025.gif" class="help-center-img img-bordered" alt="Animated view of creating and checking out a new branch in GitKraken Desktop from the right-click context menu on a commit">
  <figcaption style="text-align:center; color:#888">Creating and checking out a new branch</figcaption>
</figure>

If you’re on the wrong branch, [stash](/gitkraken-desktop/stashing) your changes, switch branches, and pop the stash.

### Rename a Branch

Right-click the branch label or use the Left Panel to rename the current branch.

<figure>
  <img src="/wp-content/uploads/rename-branch.png" srcset="/wp-content/uploads/rename-branch@2x.png 2x" class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop with the Rename branch option selected for the branch 'branch-rename'">
  <figcaption style="text-align:center; color:#888">Rename a branch from the graph or Left Panel</figcaption>
</figure>

You can also rename using the Command Palette (Cmd+P / Ctrl+P):

<figure>
  <img src="/wp-content/uploads/rename-branch-command-palette.png" srcset="/wp-content/uploads/rename-branch-command-palette@2x.png 2x" class="help-center-img img-bordered" alt="Command Palette in GitKraken Desktop showing filtered results for 'Rename Branch'">
  <figcaption style="text-align:center; color:#888">Search for "Rename Branch" in Command Palette</figcaption>
</figure>

### Delete a Branch

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

***

## Merging

Merging combines changes from one branch into another. To merge:
- Drag and drop one branch onto your target branch
- Or right-click the source branch and choose **Merge**

<figure>
  <img src="/wp-content/uploads/merge-right.png" srcset="/wp-content/uploads/merge-right@2x.png" class="help-center-img img-bordered" alt="Context menu showing option to merge dev branch into production branch in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Merge via drag-and-drop or right-click</figcaption>
</figure>

If no conflicts exist, changes will be merged automatically.

<div class='callout callout--warning'>
  <p>The in-app merge conflict output editor is available with a <a href="https://gitkraken.com/pricing?product=gitkraken&source=help_center" target="_blank">Paid</a> license.</p>
</div>

### Merge Conflict Editor

When conflicts occur, the Commit Panel shows the conflicted files. Click a file to open the Merge Tool.

<figure>
  <img src="/wp-content/uploads/merge-conflict.png" srcset="/wp-content/uploads/merge-conflict@2x.png" class="help-center-img img-bordered" alt="GitKraken merge conflict interface showing conflicting file test.txt when merging origin/test-merge-pr into multi-conflict-left">
  <figcaption style="text-align:center; color:#888">Conflicted files shown in Commit Panel</figcaption>
</figure>

The Merge Tool shows:
- Current branch on the left
- Target branch on the right
- Output at the bottom

<figure>
  <img src="/wp-content/uploads/merge-tool2.png" srcset="/wp-content/uploads/merge-tool2@2x.png" class="help-center-img img-bordered" alt="Screenshot of GitKraken's merge conflict tool showing side-by-side comparison of conflicting lines in glo/calendar.md">
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

### Use an External Merge Tool

Set your preferred merge tool under <em>Preferences > General</em>.

Supported tools:
- Beyond Compare
- FileMerge
- Kaleidoscope
- KDiff
- Araxis
- P4Merge

<figure>
  <img src="/wp-content/uploads/configureExternalTool.png" srcset="/wp-content/uploads/configureExternalTool@2x.png" class="help-center-img img-bordered" alt="Preferences panel showing merge tool selection dropdown with Kaleidoscope selected.">
  <figcaption style="text-align:center; color:#888">Select a merge tool in Preferences</figcaption>
</figure>

If not appearing, ensure command line tools are installed:

<figure>
  <img src="/wp-content/uploads/beyond-compare.png" srcset="/wp-content/uploads/beyond-compare@2x.png 2x" class="help-center-img img-bordered" alt="Beyond Compare application menu showing the Install Command Line Tools option.">
  <figcaption style="text-align:center; color:#888">Sample view of configured merge tool</figcaption>
</figure>

Unsupported tools include:
- Meld
- SemanticMerge
- TortoiseMerge
- WinMerge

For compatibility details, visit [Git Config merge tools](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#_external_merge_tools).

### Resolve with Take Current/Incoming

Right-click a conflicted file and select:
- `Take current (branch)` – Use your current branch’s changes
- `Take incoming (branch)` – Use changes from the incoming branch

<figure>
  <img src="/wp-content/uploads/current-incoming.png" class="help-center-img img-bordered" alt="Merge conflict resolution menu with options to take the current branch (branch-2) or the incoming branch (branch-1).">
  <figcaption style="text-align:center; color:#888">Quick resolve using current or incoming options</figcaption>
</figure>

***

## Conflict Prevention

GitKraken Desktop’s **Conflict Prevention** helps identify potential issues before a merge.

[Learn more →](/gitkraken-desktop/conflict-prevention/)

<div class='callout callout--warning'>
  <p>Available to users on the Advanced tier or higher.</p>
</div>

***

## Rebasing

Rebasing moves commits from one branch onto another for a cleaner history.

<div class='embed-container embed-container--16-9'>
<iframe width="560" height="315" src="https://www.youtube.com/embed/xot40u-_1FI" frameborder="0" allowfullscreen></iframe>
</div>

To rebase:
- Drag and drop the source branch onto the target branch
- Select <kbd>Rebase</kbd> from the menu

<figure>
  <img src="/wp-content/uploads/select-rebase.png" srcset="/wp-content/uploads/select-rebase@2x.png" class="help-center-img img-bordered" alt="Rebase menu with the option to rebase the testfill2 branch onto origin/develop.">
  <figcaption style="text-align:center; color:#888">Rebase one branch onto another</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/select-rebase-sidebar.png" srcset="/wp-content/uploads/select-rebase-sidebar@2x.png" class="help-center-img img-bordered" alt="Sidebar context menu showing options to fast-forward, merge, or rebase the testfill2 branch onto master.">
  <figcaption style="text-align:center; color:#888">Sidebar shows rebase confirmation</figcaption>
</figure>

Rebasing rewrites history but results in a more linear and readable commit tree.
