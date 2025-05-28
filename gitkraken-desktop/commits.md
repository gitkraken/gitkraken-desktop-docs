---
title: Committing Changes
description: Commit to save your work with GitKraken Desktop easily when changing files. Learn how to squash, amend, and save work when committing.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

GitKraken Desktop simplifies the Git commit process by helping you stage, commit, and push your work from a visual interface.

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

<a id="commit-templates"></a>

## Commit Templates

<a id="reading-the-commit-template"></a>

### Reading the Commit Template

When you open a repository, GitKraken Desktop checks for a commit template in this order:

1. The repository’s local `.git/config` file
2. Your global `.gitconfig`
3. If neither contains a `commit.template` setting, GitKraken Desktop does not load a template

<a id="creating-and-updating-the-commit-template"></a>

### Creating and Updating the Commit Template

To create or update a commit template, navigate to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> Commit</em>.

<figure class='figure center'>
    <img src='/wp-content/uploads/commit-template-setting-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Set an initial commit message in Preferences > Commit.</figcaption>
</figure>

If a template is loaded from your local config, GitKraken Desktop saves changes to that file. If no template exists, your changes are saved to a new `gkcommittemplate.txt` file in your repo’s `.git/` directory. GitKraken Desktop also updates the `commit.template` path in the local config.

This setup lets you maintain a local template without altering your global Git configuration.

#### Commit Template Options

- **Apply this template to commit messages**: Automatically inserts the template in the message editor.
- **Remove comments from commit messages**: Omits lines starting with `#` when applying the template.

### Configuring Commit Templates

There are three ways to configure commit templates:

* **Create in GitKraken Desktop** — Saves to `.git/gkcommittemplate.txt`
* **Set a repo-specific template** — Use:
  ```bash
  git config commit.template <path_to_template>
  ```
* **Set a global template** — Use:
  ```bash
  git config --global commit.template <path_to_template>
  ```

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Editing a global template within GitKraken Desktop causes it to create `gkcommittemplate.txt` locally and point your repository’s config to that file.</p>
</div>

***

<a id="amending-commits"></a>

## Amending Commits

GitKraken Desktop lets you modify the last commit by updating the message, adding new changes, or both.

To include new changes:
1. Modify files in your working directory.
2. Stage the changes.
3. Select **Amend the previous commit** in the Commit Panel.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-commit-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Select this option to append changes to the most recent commit.</figcaption>
</figure>

To update only the message:
1. Select the most recent commit in the graph.
2. Click into the message box and revise the text.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-message-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Edit your previous commit message directly in the message field.</figcaption>
</figure>

To resize the commit message field, drag the bottom edge of the editor.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-box-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Resize the commit message box as needed.</figcaption>
</figure>

Use the **Update Message** button to save changes, or **Cancel Amend** to discard them.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> If you’ve already pushed a commit, amending it will require a force push to update the remote history.</p>
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
