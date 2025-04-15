---

title: Cherry Pick
description: Learn how to get changes from one commit to add it to your current branch.
taxonomy:
    category: gitkraken-desktop

---

<kbd>Last updated: April 2025</kbd>

Sometimes you commit to one branch, when you meant to commit to another. Here's how to grab the changes you need.

***
To cherry pick a commit, right click on a commit node and select the "Cherrypick commit" option:

<img src='/wp-content/uploads/cherrypick.png' srcset='/wp-content/uploads/cherrypick@2x.png 2x' class="help-center-img img-bordered">

The cherry pick action is also available when interacting with branches from _Local_ in the Left Panel.

Here, cherry pick grabs the changes from the commit referenced by the HEAD of that branch, and places them onto the branch currently checked out.

<img src='/wp-content/uploads/cherrypick-left-panel.png' srcset='/wp-content/uploads/cherrypick-left-panel@2x.png 2x' class="help-center-img img-bordered">

### Cherry Pick Multiple Commits

To cherry pick multiple commits, you can select multiple commits by holding down the <kbd>Cmd/Ctrl</kbd> or <kbd>Shift</kbd> key and clicking on the desired commits. Then, right-click on one of the selected commits and choose the "Cherry pick X commits" option.

<img src='/wp-content/uploads/multi-cherry-pick-menu.png' class="help-center-img img-bordered">

Selecting the option to cherry pick multiple commits opens an interactive cherry pick tool that allows you to reorder (with drag and drop of mouse), squash, reword, or drop any of the commits selected.

<img src='/wp-content/uploads/interactive-cherry-pick.png' class="help-center-img img-bordered">

## Commit Actions

### Pick
Pick takes the commits from one branch and places them onto the last commit of another branch.


### Reword
When selecting reword you will see the <em class='context-menu'>Reword commit message</em> modal open. Here you can edit the summary and description of your commit.

### Squash
When you squash you are taking the child commit and in turn writing that commit to the parent commit. In order for squash to be an option there will have to be a parent child relationship.

### Drop commit
Drop removes the commit from the branch, completes rebase and rewrites the commit graph.


---

### Keyboard Shortcuts and Reset
Use keyboard shortcuts <kbd>P</kbd>ick, <kbd>S</kbd>quash, <kbd>R</kbd>eword and <kbd>D</kbd>rop to perform commit actions. If you wish to start over, click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Reset</span></button>.

***
### Additional Learning Git Resources:

<p class="small">
	<a href="https://gitkraken.com/learn/git/tutorials/cherry-pick?product=gitkraken&source=help_center" target="_blank">Cherry Pick Tutorial</a> | <a href="https://gitkraken.com/learn/git/cherry-pick?product=gitkraken&source=help_center" target="_blank">Learn Git: What is Cherry Pick?</a></a>
</p>