---
title: Committing Changes
description: Commit to save your work with GitKraken Desktop easily when changing files. Learn how to squash, amend, and save work when committing.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

GitKraken Desktop simplifies the Git commit process by helping you stage, commit, and push your work—all from a visual interface.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8a6fYPkBDbY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

<a id="making-a-commit"></a>

## Making a commit

To create a commit, select your _Work in Progress_ (WIP) node to view file changes in the Commit Panel.

<figure class='figure center'>
    <img src='/wp-content/uploads/select-WIP-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">The WIP node appears at the top of the Commit Graph when you save file changes.</figcaption>
</figure>

Select files to stage by clicking them individually or reviewing diffs. To stage all files:
- **Mac:** <kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>S</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>S</kbd>

Type your commit message, then click **Commit**, or use the shortcut:
- **Mac:** <kbd>&#8984;</kbd> + <kbd>Enter</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd> + <kbd>Enter</kbd>

<a id="commit-and-push"></a>

### Commit and push

To commit and immediately push changes, stage files and enter a message. Then select the **Commit and Push** option.

<figure class='figure center'>
    <img src='/wp-content/uploads/push-after-commit-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Enable this option to commit and push changes in one step.</figcaption>
</figure>

The graph updates with your commit. If needed, undo it with:
- **Mac:** <kbd>&#8984;</kbd> + <kbd>Z</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd> + <kbd>Z</kbd>

<a id="committing-with-co-authors"></a>

### Committing with Co-Authors

To credit co-authors in a commit, add lines to the commit message using the following format:

```
Co-authored-by: Name One <email1@example.com>
Co-authored-by: Name Two <email2@example.com>
```

<figure class='figure center'>
    <img src='/wp-content/uploads/co-author.png' srcset='/wp-content/uploads/co-author@2x.png 2x' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Use this syntax to attribute co-authors in a commit.</figcaption>
</figure>

Co-authors appear in the Commit Panel history:

<figure class='figure center'>
    <img src='/wp-content/uploads/co-author-history.png' srcset='/wp-content/uploads/co-author-history@2x.png 2x' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Co-authors are listed with the primary author in the commit history.</figcaption>
</figure>

### Bypass Git hooks

To skip Git hooks for a specific commit, enable the **Skip Git hooks** checkbox in the Commit Panel.

<div class='callout callout--warning'>
    <p><strong>Warning:</strong> Skipping this will bypass all configured Git hooks for the commit action.</p>
</div>

<figure class='figure center'>
    <img src='/wp-content/uploads/skip-commits-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Enable this option to bypass Git commit hooks.</figcaption>
</figure>

***

<a id="amending-commits"></a>

## Amending commits

GitKraken Desktop allows you to amend a commit message, add additional changes, or both.

To add more changes to the previous commit, first make the code changes in your working directory. Then when you stage changes in GitKraken Desktop, select the option to _"Amend the previous commit."_

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-commit-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Check this option to add changes to the previous commit.</figcaption>
</figure>

To only update the commit message, select the most recent commit in the graph and then click in the message box to amend the message.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-message-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">You can edit your most recent commit message from the Commit Panel.</figcaption>
</figure>

To accommodate viewing a longer commit description, click on the bar at the the bottom of the message box and drag downwards to dynamically resize the text field.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-box-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Drag and drop this bar to resize the commit message box.</figcaption>
</figure>

Select <button class='button button--success button--ui button--nolink'>Update Message</button> to save your changes or <button class='button button--danger button--ui button--nolink'>Cancel Amend</button> to discard.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Amending commits which are already pushed to a remote are more difficult to apply and would require a force push for the rewrite.</p>
</div>

***

<a id="resetting-commits"></a>

## Resetting commits
Git keeps track of your current commit in a file called the HEAD.  When resetting a commit, you update the HEAD of your repo to point to the selected commit.  GitKraken Desktop offers the following reset options:

* **Soft** - resets the HEAD to the selected commit, but keeps your changes staged and in your WIP directory
* **Mixed** - resets the HEAD to the selected commit, unstages your changes, but keeps them in your WIP directory
* **Hard** - resets the HEAD to the selected commit, unstages your changes, and deletes your WIP files

<figure class='figure center'>
    <img src='/wp-content/uploads/reset-commit-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Perform a reset by right-clicking a branch or commit.</figcaption>
</figure>


You may also drag and drop a branch onto another to select from the three reset options above or access the reset options from your local repos in the left panel.

***

<a id="reverting-changes"></a>

## Reverting changes

Undo, undo, undo. You can undo many of your actions in GitKraken Desktop with the Undo icon.

<figure class='figure center'>
    <img src='/wp-content/uploads/undo-undo-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">If you haven't pushed it, you can probably undo it.</figcaption>
</figure>

If you're a keyboard fan, you may also enjoy using the keyboard shortcut
<kbd>&#8984;</kbd> + <kbd>z</kbd> for Mac or <kbd>Ctrl</kbd> + <kbd>Z</kbd> for not-Mac.

<a id="reverting-commits"></a>

### Reverting commits

Reverting commits is trivial thanks to GitKraken Desktop.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/U_axv67W1Ik?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

If you wish to revert a commit (perhaps Undo is not available), the option is available when right-clicking on a commit node.  This will create a new commit to reverse your previous changes.

<figure class='figure center'>
    <img src='/wp-content/uploads/revert-commit-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Right-click any commit to revert it.</figcaption>
</figure>
