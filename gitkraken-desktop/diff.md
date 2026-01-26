---
title: View Diffs, File History, and Blame in GitKraken Desktop
description: Learn how to use GitKraken Desktop to compare changes with diffs, view file history and blame, configure external diff tools, and manage Git patches.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

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
  <img src='/wp-content/uploads/diff-full-screen-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing a full-screen side-by-side diff of a markdown file, with syntax-highlighted line changes and a file activity panel listing added images.">
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
  <img src='/wp-content/uploads/diff-2-commits-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop displaying a visual diff between two selected commits, with syntax-highlighted line changes and commit metadata shown in the right panel.">
  <figcaption style="text-align: center; color: #888;">Diff view comparing two selected commits.</figcaption>
</figure>

You can also select multiple commit rows using <kbd>Shift</kbd> + <kbd>Click</kbd> to show a combined diff:

<figure class='figure center'>
  <img src='/wp-content/uploads/combined-diff-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing a combined diff view summarizing file and line changes from multiple selected commits, with commit history and file modification list visible.">
  <figcaption style="text-align: center; color: #888;">Combined diff across multiple selected commits.</figcaption>
</figure>

### Hunk View

Displays only the changed blocks of a file.

<figure class='figure center'>
  <img src='/wp-content/uploads/hunk-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop displaying hunk view mode, focusing on a grouped block of code changes with syntax highlighting and minimal surrounding context.">
  <figcaption style="text-align: center; color: #888;">Hunk view highlights change blocks without full context.</figcaption>
</figure>

#### Revert Hunks

GitKraken offers a convenient option in the diff view: **Revert Hunks**.

In **Hunk View**, you can roll back a specific block of changes. Click the **Revert** button next to any hunk to apply an equal and opposite change to your working directory.

<figure>
  <img src="/wp-content/uploads/revert-hunk-2025.png" srcset="/wp-content/uploads/revert-hunk-2025@2x.png 2x" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken Desktop showing the Revert Hunk button in the diff view, with a tooltip explaining it will reverse the selected code changes in the working directory." />
  <figcaption style="text-align: center; color: #888">Click the Revert button to undo a specific hunk directly from the diff view.</figcaption>
</figure>

This lets you revert only what you need—no reset or manual edits required.

### Inline View

Displays changes within the full context of the file.

<figure class='figure center'>
  <img src='/wp-content/uploads/inline-annotated-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop displaying Inline View mode for file diffs, with added lines and a selected image insertion shown directly in context." />
  <figcaption style="text-align: center; color: #888;">Inline view shows changes inline with full file content.</figcaption>
</figure>

### Split View

Displays changes side-by-side, with the original file on the left and the updated version on the right.

<figure class='figure center'>
  <img src='/wp-content/uploads/split-2025.png' class="help-center-img img-bordered" alt="Split View mode in GitKraken Desktop comparing changes between two versions of a file, highlighting additions, deletions, and updated image references side-by-side." />
  <figcaption style="text-align: center; color: #888;">Split view compares before (left) and after (right) file states.</figcaption>
</figure>

***

## External Diff Tools

Configure an external diff tool in <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> External Tools</em>:

<figure class='figure center'>
  <img src="/wp-content/uploads/external-diff-2025.png" class="help-center-img img-bordered" alt="GitKraken Desktop External Tools preferences showing dropdown to select an external diff tool, with options like FileMerge and Git Config Default." />
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
  <img src='/wp-content/uploads/beyond-compare.png' srcset='/wp-content/uploads/beyond-compare@2x.png 2x' class='help-center-img img-bordered' alt="Beyond Compare application menu with Install Command Line Tools option highlighted, used to enable CLI integration." />
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

## Diff a WIP

To compare your Work in Progress (WIP) with another commit or branch:
- Use <kbd>Ctrl/Cmd</kbd> + click to select the WIP and another commit
- Or, right-click a commit or branch and select <kbd>Compare commit against working directory</kbd>

<figure class='figure center'>
  <img src='/wp-content/uploads/compare-WIP-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the option to compare a selected commit against the working directory from the commit graph." />
  <figcaption style="text-align: center; color: #888;">Compare WIP with a commit or branch from the graph.</figcaption>
</figure>

***

## File Blame and History

Access _File History_ and _File Blame_ from the file diff view. Options appear in the upper-right corner.

<figure class='figure center'>
  <img src='/wp-content/uploads/blame-history-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing Blame and History buttons in the file view toolbar for accessing file-level version history and author attributions." />
  <figcaption style="text-align: center; color: #888;">Use buttons in the top-right to view file history or blame.</figcaption>
</figure>

Alternatively, right-click a file after selecting a commit in the graph.

<figure class='figure center'>
  <img src='/wp-content/uploads/file-history-commit-selected-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing file history for a selected commit, with highlighted changes in the diff view panel." />
  <figcaption style="text-align: center; color: #888;">Access history or blame from the commit graph.</figcaption>
</figure>

_File Blame_ color-codes each line or hunk by author.

<figure class='figure center'>
  <img src='/wp-content/uploads/blame-2025.png' class="help-center-img img-bordered" alt="Blame view in GitKraken Desktop showing author and date annotations alongside each line of code." />
  <figcaption style="text-align: center; color: #888;">Blame view showing per-line author contributions.</figcaption>
</figure>

Use the toggle in the top-right to switch between <kbd>Diff View</kbd> (showing changes) and <kbd>File View</kbd> (showing the full file with blame).

***

## Patch

A patch (or patch file) records the differences between files. Patches allow users to share changes without pushing them to a remote repository.

### Create Patch from File(s)

To create a patch:
- Right-click a **commit** and choose <kbd>Create patch from commit</kbd>
- Right-click a **file** and choose <kbd>Create patch from file changes</kbd>

You will be prompted to name the patch file.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-patch-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the option to generate a patch file from a selected commit." />
  <figcaption style="text-align: center; color: #888;">Create a patch from a commit.</figcaption>
</figure>

<figure class='figure center'>
  <img src='/wp-content/uploads/patch-from-changes-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the option to generate a patch from unstaged file changes." />
  <figcaption style="text-align: center; color: #888;">Create a patch from file changes.</figcaption>
</figure>

You can also multi-select files or commits using <kbd>Shift</kbd> or <kbd>Cmd/Ctrl</kbd> + click, then right-click to create a patch.

<figure class='figure center'>
  <img src='/wp-content/uploads/patch-from-many-files-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop context menu showing the option to create a patch from changes across multiple unstaged files." />
  <figcaption style="text-align: center; color: #888;">Create a patch from multiple files or commits.</figcaption>
</figure>

### Create Patch from Command Palette

Launch the Command Palette from the toolbar or with <kbd>Cmd/Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>, then search for “Create Patch.”

<figure class='figure center'>
  <img src="/wp-content/uploads/create-patch-from-command-palette.png" class="help-center-img img-bordered" alt="Command Palette in GitKraken Desktop displaying the option to create a patch from all working directory changes." />
  <figcaption style="text-align: center; color: #888;">Create a patch using the Command Palette.</figcaption>
</figure>

### Apply Patch from Command Palette

To apply a patch:
1. Open the Command Palette (<kbd>Cmd/Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>P</kbd>)
2. Type “Apply Patch” and select the command
3. Choose your `.patch` file in the file explorer

<figure class='figure center'>
  <img src='/wp-content/uploads/apply-patch-2025.png' class="help-center-img img-bordered" alt="Command Palette in GitKraken Desktop showing the option to apply a patch from the file system." />
  <figcaption style="text-align: center; color: #888;">Apply a patch from the file system.</figcaption>
</figure>

<div class='callout callout--basic'>
    <p><strong>Note:</strong> GitKraken Desktop does not currently support generating patches from binary files. This is a preliminary release. For feedback, contact our <a href="https://www.gitkraken.com/git-client/contact-support?product=gitkraken&source=help_center">support team</a>.</p>
</div>
