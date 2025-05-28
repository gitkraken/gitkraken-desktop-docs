---
title: Diff, Patch, Blame, and History
description: Compare your changes using diffs in GitKraken Desktop. Learn how to access diffs, view file history and blame, and configure external diff tools.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

Compare changes within GitKraken Desktop using _diffs_. Learn how to access them, view file history or file blame, and use external tools.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/-0bn2H63axM?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

<a id="what-is-a-diff-in-gitkraken"></a>

## What Is a Diff in GitKraken Desktop?

A diff displays lines added and removed from a file:
- <span style='color: #d90171;'>Red</span> indicates removed lines.
- <span style='color: #7bd938;'>Green</span> indicates added lines.

<figure class='figure center'>
  <img src='/wp-content/uploads/diff-full-screen-2025.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Full-screen diff view with color-coded changes.</figcaption>
</figure>

GitKraken Desktop’s built-in diff viewer includes:

- Word diffing
- Syntax highlighting
- File mini-map
- Toggleable views: Hunk, Inline, Split
- Arrows to navigate between change sets

Use the <button class="button button--primary button--ui button--nolink"><span style="color:#141422;">Edit in working directory</span></button> button to directly edit the file. Learn more in the [Editing Files](/working-with-files/editing-files) section.

***

## Where Can I Access the Diff?

You can view diffs from:

- **Staging area**: Click a file to open its diff
- **Commit node**: Select a commit and click any file

Selecting two commits shows the differences between them.

<figure class='figure center'>
  <img src='/wp-content/uploads/diff-2-commits-2025.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Diff view comparing two selected commits.</figcaption>
</figure>

You can also select multiple commit rows using <kbd>Shift</kbd> + <kbd>Click</kbd> to show a combined diff:

<figure class='figure center'>
  <img src='/wp-content/uploads/combined-diff-2025.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Combined diff across multiple selected commits.</figcaption>
</figure>

### Hunk View

Displays only the changed blocks of a file.

<figure class='figure center'>
  <img src='/wp-content/uploads/hunk-2025.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Hunk view highlights change blocks without full context.</figcaption>
</figure>

### Inline View

Displays changes within the full context of the file.

<figure class='figure center'>
  <img src='/wp-content/uploads/inline-annotated-2025.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Inline view shows changes inline with full file content.</figcaption>
</figure>

### Split View

Displays changes side-by-side, with the original file on the left and the updated version on the right.

<figure class='figure center'>
  <img src='/wp-content/uploads/split-2025.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Split view compares before (left) and after (right) file states.</figcaption>
</figure>

***

## External Diff Tools

Configure an external diff tool in <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> External Tools</em>:

<figure class='figure center'>
  <img src="/wp-content/uploads/external-diff-2025.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Configure your preferred diff tool from Preferences.</figcaption>
</figure>

Supported tools include:

- Beyond Compare
- FileMerge
- Kaleidoscope
- KDiff
- Araxis
- P4Merge

If a supported tool does not appear in the dropdown, verify that its command line tools are installed.

<figure class='figure center'>
  <img src='/wp-content/uploads/beyond-compare.png' srcset='/wp-content/uploads/beyond-compare@2x.png 2x' class='img-bordered'>
  <figcaption style="text-align: center; color: #888;">Example setup with Beyond Compare.</figcaption>
</figure>

To use a different diff tool, go to <em class="context-menu">Preferences <i class="fa fa-caret-right"></i> General</em> and set the <kbd>Diff Tool</kbd> to _Git Config Default_. Then add the appropriate configuration in your global `.gitconfig`:

#### macOS
```
[diff]
    tool = meld
[difftool "meld"]
    cmd = open -a Meld --args "$LOCAL" "$REMOTE"
```

#### Linux
```
[diff]
    tool = meld
[difftool "meld"]
    cmd = meld "$LOCAL" "$REMOTE"
```

#### Windows
```
[diff]
    tool = meld
[difftool]
    prompt = false
[difftool "meld"]
    cmd = meld "$LOCAL" "$REMOTE"
```

***

## Diff Multiple Commits

Use <kbd>Shift</kbd> or <kbd>Cmd/Ctrl</kbd> to select multiple commits in the Commit Graph.

<figure class='figure center'>
  <img src="/wp-content/uploads/select-commits-2025.gif" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Multi-select commits to generate a combined diff.</figcaption>
</figure>

This generates a combined diff showing all added, modified, renamed, or deleted files between the selected commits.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> To diff branches, use <kbd>Cmd/Ctrl</kbd> to select the head commits of each branch.</p>
</div>

***

## Diff a WIP

When you have a Work in Progress (WIP), you can diff this against any commit or branch by ctrl/command clicking the WIP and then the other desired commit. Alternativley, with your WIP sleected, you can right-click the desired commit or branch and select `Compare commit against working directory`.

<img src='/wp-content/uploads/compare-WIP-2025.png' class="help-center-img img-bordered">

***

## File Blame and History

_File History_ and _File Blame_ information display in the same view.

To access either option, click to view the file diff and the options will appear in the upper right.

<img src='/wp-content/uploads/blame-history-2025.png' class="help-center-img img-bordered">

You may also click on a commit in the graph and then right click a file to access _File History_ or _File Blame_. _File History_ shows that file's commit history on the left.

<img src='/wp-content/uploads/file-history-commit-selected-2025.png' class="help-center-img img-bordered">

_File Blame_ will color code the commit author of each line or hunk.

<img src='/wp-content/uploads/blame-2025.png' class="help-center-img img-bordered">

Use the top toggle button to switch between <kbd>Diff View</kbd>, which shows the selected commit's changes to the file, and the <kbd>File View</kbd>, which shows the file's state at that commit, including the blame info.

## Patch

A patch, or patchfile, is a file describing changes between 2 files. Patch files can be used to distribute changes that a given user would like to make to a particular revision without codifying it onto a git server. Patches can be created from either a commit(s) or a file(s).

### Create patch from file(s)

To create a patch from a commit, right-click a commit and select `Create patch from commit`. You will be prompted to name the patch after.

<img src='/wp-content/uploads/create-patch-2025.png' class="help-center-img img-bordered">

To create a patch from a file, right-click a file and select `Create patch from file changes`. You will be prompted to name the patch after.

<img src='/wp-content/uploads/patch-from-changes-2025.png' class="help-center-img img-bordered">

You can also multi-select files or commits by holding command/ctrl or shift and clicking. You can then right-click the selected files or commits to create a patch from the selected.

<img src='/wp-content/uploads/patch-from-many-files-2025.png' class="help-center-img img-bordered">

### Create patch from Command Palette

Click on the Command Palette icon on the toolbar, or use the keyboard shortcut <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd> to launch Command Palette.

<img src="/wp-content/uploads/create-patch-from-command-palette.png" class="help-center-img img-bordered">

### Apply patch from Command Palette

To apply a patch, use the keyboard shortcut `command/ctrl + Shift + P` or click the <i  class="fa fa-magic" style="transform: rotate(225deg)"></i> in the top right of the UI to bring up the Command Palette. Type “Apply Patch" to summon the “Apply Patch” command, and select it to open your file explorer. 

<img src='/wp-content/uploads/apply-patch-2025.png' class="help-center-img img-bordered">

Select your .patch file to then apply changes to your working directory. 


<div class='callout callout--basic'>
    <p>Note: GitKraken Desktop does not yet support generating patches from binary files. This is a preliminary release with better support coming, and if you have feedback please reach out to our <a href="https://www.gitkraken.com/git-client/contact-support?product=gitkraken&source=help_center">support team</a>. </p>
</div>