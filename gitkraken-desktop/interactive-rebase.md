---

title: Interactive Rebase
description: Learn about interactive rebase in GitKraken Desktop.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

Learn how to rewrite your commit history with interactive rebase in GitKraken Desktop.

***

## Initiating Interactive Rebase
To initiate interactive rebase, drag and drop one branch onto another branch or right-click the target branch and select <em class='context-menu'>Interactive Rebase</em>.

<img src='/wp-content/uploads/interactive-rebase-init.gif' class="help-center-img img-bordered" />

Right-click on any parent commit to see the interactive rebase option. However, please note that interactive rebase is not available for merge commits.

### Interactive rebase requirements

The drag and drop option will only show the interactive rebase option if:

- No merge commits are present on the branch you’re rebasing
- The 2 branches share a common ancestor
- Neither branch has the repo’s initial commit
- You are not attempting to rebase a parent branch onto a child (like main into a feature branch)

<div class='callout callout--note'>
    <p><strong>Note:</strong> If you start the interactive rebase with GitKraken Desktop you must finish the rebase with GitKraken Desktop.</p>
</div>

---

## Commit Actions

### Pick
Pick takes the commits from one branch and places them onto the last commit of another branch.

<img src='/wp-content/uploads/pick.gif' class="help-center-img img-bordered" />

### Reword
When selecting reword you will see the <em class='context-menu'>Reword commit message</em> modal open. Here you can edit the summary and description of your commit.

<img src='/wp-content/uploads/reword.png' class="help-center-img img-bordered" />

### Squash
When you squash you are taking the child commit and in turn writing that commit to the parent commit. In order for squash to be an option there will have to be a parent child relationship.

<img src='/wp-content/uploads/squash.png' class="help-center-img img-bordered" />

### Drop commit
Drop removes the commit from the branch, completes rebase and rewrites the Commit Graph.

<img src='/wp-content/uploads/drop.gif' class="help-center-img img-bordered" />

---

### Keyboard Shortcuts and Reset
Use keyboard shortcuts <kbd>P</kbd>ick, <kbd>S</kbd>quash, <kbd>R</kbd>eword and <kbd>D</kbd>rop to perform commit actions. If you wish to start over, click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Reset</span></button>.

<img src='/wp-content/uploads/keyboard-shortcut-reset.gif' class="help-center-img img-bordered" />