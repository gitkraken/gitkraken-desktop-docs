---

title: Cherry Pick
description: Learn how to get changes from one commit to add it to your current branch.
taxonomy:
    category: gitkraken-desktop

---

Sometimes you commit to one branch, when you meant to commit to another. Here's how to grab the changes you need.

***
To cherry pick a commit, right click on a commit node and select the Cherrypick Commit option:

<img src='/wp-content/uploads/cherrypick.png' srcset='/wp-content/uploads/cherrypick@2x.png 2x' class="help-center-img img-bordered">

The cherry pick action is also available from _Local_ on the left panel.

Here, cherry pick grabs the changes from the commit referenced by the HEAD of that branch, and places them onto the branch currently checked out.

<img src='/wp-content/uploads/cherrypick-left-panel.png' srcset='/wp-content/uploads/cherrypick-left-panel@2x.png 2x' class="help-center-img img-bordered">

### Cherry Pick Multiple Commits

To cherry pick multiple commits, you can select multiple commits by holding down the kbd>Cmd/Ctrl</kbd> or <kbd>Shift</kbd> key and clicking on the desired commits. Then, right-click on one of the selected commits and choose the Cherry Pick Commits option.
Selecting the option to cherry pick multiple commits opens an interactive cherry pick tool that allows you to reorder, squash, reword, or drop any of the commits selected.

***
### Additional Learning Git Resources:

<p class="small">
	<a href="https://gitkraken.com/learn/git/tutorials/cherry-pick" target="_blank">Cherry Pick Tutorial</a> | <a href="https://gitkraken.com/learn/git/cherry-pick" target="_blank">Learn Git: What is Cherry Pick?</a></a>
</p>