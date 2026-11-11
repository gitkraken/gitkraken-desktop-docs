---
title: View Diffs, File History, and Blame in GitKraken Desktop
description: View diffs, file history, and blame in GitKraken Desktop to see what changed, including changes from coding agents, and set up external diff tools and patches.
product: GitKraken Desktop
feature: Diff Viewer
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
tags: [diff, blame, history, patches, external-tools]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "working-with-files"
    nav_label: "View Diffs, File History, and Blame in GitKraken Desktop"
    nav_order: 50
    nav_parent: "working-with-files"
    page_type: "content"
    card_icon: "file-diff"
    card_color: "blue"
    card_description: "Diffs, file history, blame and external diff tools"
---
<kbd>Last updated: November 2026</kbd>

Use this page to compare uncommitted changes, inspect commit diffs, switch between diff views, review file history or blame, set up an external diff tool, and create or apply patches in GitKraken Desktop.

**Key constraints**
- Patch support: Patch creation and application are preliminary features
- Binary files: GitKraken Desktop does not generate patches from binary files
- External diff tools: Beyond Compare, FileMerge, Kaleidoscope, KDiff, Araxis, and P4Merge are supported directly
- Other tools: Use <kbd>Git Config Default</kbd> and your global `.gitconfig` if your preferred diff tool is not listed in Preferences

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/-0bn2H63axM?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

## Quick Start


**To view a diff:**
- Click a file in the staging area (WIP node) to see your uncommitted changes.
- Click a commit in the graph, then click any file in the Commit Panel to view that commit's changes.
- Select 2 commits with <kbd>Shift</kbd> + click to compare them directly.

**To switch diff view modes**, use the **Hunk**, **Inline**, or **Split** toggles in the diff viewer. To revert a specific block of changes, use the **Revert Hunk** button in Hunk view.

**To view file history or blame:**
- Open the diff for any file and click the **History** or **Blame** button in the upper-right corner.
- Or right-click a file after selecting a commit in the graph.

**To create or apply a patch:**
- Right-click a commit and select **Create patch from commit**.
- To apply a patch, open the Command Palette (<kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>P</kbd>), type `Apply patch`, and select your `.patch` file.

To use an external diff tool, go to <kbd>Preferences > External Tools</kbd> and select your preferred application.

To review what a coding agent changed across its commits and worktree, see [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/).

***

<a id="what-is-a-diff-in-gitkraken"></a>

## What Is a Diff in GitKraken Desktop?

A diff displays lines added and removed from a file:
- <span style='color: #d90171;'>Red</span> indicates removed lines.
- <span style='color: #7bd938;'>Green</span> indicates added lines.

<div class='callout callout--basic'>
  <p><strong>Use the built-in diff when:</strong> you want to inspect changes, compare commits, or review file history directly in GitKraken Desktop. <strong>Use an external diff tool when:</strong> you need a specialized comparison workflow that is not covered well by the built-in viewer.</p>
</div>

<figure class='figure center'>
  <img src='/wp-content/uploads/diff-full-screen-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing a full-screen side-by-side diff of a markdown file, with syntax-highlighted line changes and a file activity panel listing added images.">
  <figcaption style="text-align: center; color: #888;">Full-screen diff view with color-coded changes.</figcaption>
</figure>

The built-in diff viewer in GitKraken Desktop includes:

- Word diffing
- Syntax highlighting
- File mini-map
- Toggleable views: Hunk, Inline, Split
- Word wrap toggle
- Arrows to navigate between change sets

Use the <button class="button button--primary button--ui button--nolink"><span style="color:#141422;">Edit in Working Directory</span></button> button to edit the file directly. See [Editing Files](/working-with-files/editing-files).

***

## Where Can I Access the Diff?

You can view diffs from:

- **Staging area**: Click a file to open its diff
- **Commit node**: Select a commit and click any file
- **GitHub pull request**: Right-click a pull request in the Left Panel's **Pull Requests** section, or a branch that has a pull request, and select **View changes in #N**

Selecting 2 commits shows the differences between them.

**View changes in #N** is available for GitHub and GitHub Enterprise pull requests. It selects the pull request's base and head commits in the graph, and the Commit Panel shows every change in the pull request. If the pull request comes from a remote you have not added, such as a fork, GitKraken Desktop asks to add that remote first. If the base or head commit is not loaded in the graph, scroll down or increase **Initial Commits in Graph** in <kbd>Preferences > General</kbd>, then try again.

<figure class='figure center'>
  <img src='/wp-content/uploads/diff-2-commits-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop displaying a visual diff between two selected commits, with syntax-highlighted line changes and commit metadata shown in the right panel.">
  <figcaption style="text-align: center; color: #888;">Diff view comparing two selected commits.</figcaption>
</figure>

Select consecutive commits in the graph using <kbd>Shift</kbd> or <kbd>Cmd/Ctrl</kbd> + click to show their combined changes in the Commit Panel, titled **Viewing diff of N commits**. You can include the WIP if your selection reaches the latest commit. If you select more than 2 nonconsecutive items, GitKraken Desktop explains why it cannot show a combined diff, and the AI actions for the selection are hidden.

<figure class='figure center'>
  <img src='/wp-content/uploads/combined-diff-2025-v2@2x.png' class="help-center-img img-bordered" alt="The Commit Panel titled &quot;Viewing diff of 3 commits&quot;, listing three commits by Alex Lee with their dates and short SHAs, then 2 modified and 3 added files: docs/CONTRIBUTING.md, three files under docs/onboarding/ and README.md.">
  <figcaption style="text-align: center; color: #888;">Combined diff across multiple selected commits.</figcaption>
</figure>

### When to use Hunk View

Hunk View displays only the changed blocks of a file.

<div class='callout callout--basic'>
  <p><strong>Use Hunk View when:</strong> you want to focus only on changed blocks or revert a specific hunk quickly. <strong>Do not use it when:</strong> you need full-file context around the changes.</p>
</div>

<figure class='figure center'>
  <img src='/wp-content/uploads/hunk-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop displaying hunk view mode, focusing on a grouped block of code changes with syntax highlighting and minimal surrounding context.">
  <figcaption style="text-align: center; color: #888;">Hunk view highlights change blocks without full context.</figcaption>
</figure>

#### How to revert a hunk

In **Hunk View**, you can roll back a specific block of changes. Click the **Revert Hunk** button next to any hunk to apply an equal and opposite change to your working directory.

<figure>
  <img src="/wp-content/uploads/revert-hunk-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken Desktop showing the Revert Hunk button in the diff view, with a tooltip explaining it will reverse the selected code changes in the working directory." />
  <figcaption style="text-align: center; color: #888">Click the Revert button to undo a specific hunk directly from the diff view.</figcaption>
</figure>

You revert only the hunk you choose, without a reset or manual edits.

### When to use Inline View

Inline View displays changes within the full context of the file.

<div class='callout callout--basic'>
  <p><strong>Use Inline View when:</strong> you want to read edits in the flow of the full file. <strong>Do not use it when:</strong> side-by-side comparison is easier for the change you are reviewing.</p>
</div>

<figure class='figure center'>
  <img src='/wp-content/uploads/inline-annotated-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop displaying Inline View mode for file diffs, with added lines and a selected image insertion shown directly in context." />
  <figcaption style="text-align: center; color: #888;">Inline view shows changes inline with full file content.</figcaption>
</figure>

### When to use Split View

Split View displays changes side-by-side, with the original file on the left and the updated version on the right.

<div class='callout callout--basic'>
  <p><strong>Use Split View when:</strong> you want to compare old and new content line-by-line. <strong>Do not use it when:</strong> you want a more compact, single-column review for small changes.</p>
</div>

<figure class='figure center'>
  <img src='/wp-content/uploads/split-2025.png' class="help-center-img img-bordered" alt="Split View mode in GitKraken Desktop comparing changes between two versions of a file, highlighting additions, deletions, and updated image references side-by-side." />
  <figcaption style="text-align: center; color: #888;">Split view compares before (left) and after (right) file states.</figcaption>
</figure>

### How to use Word Wrap in the diff view

The Word Wrap toggle wraps long lines in the diff view so that the full content of each line is visible without horizontal scrolling. Use it to review files with long lines, such as Markdown documents, minified JavaScript, or LaTeX files.

To toggle word wrap, click the **Word Wrap** button in the toolbar of the diff view, file view, file history, or merge conflict resolution panel.

<figure class='figure center'>
  <img src='/wp-content/uploads/word-wrap.png' class="help-center-img img-bordered" alt="GitKraken Desktop file view toolbar with the Word Wrap button highlighted in the top-right corner, showing a file with long lines wrapped for easier reading." />
  <figcaption style="text-align: center; color: #888;">Click the Word Wrap button in the toolbar to toggle line wrapping.</figcaption>
</figure>

***

## How to use external diff tools

Configure an external diff tool in <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> External Tools</em>:

<div class='callout callout--basic'>
  <p><strong>Use an external diff tool when:</strong> you already rely on a supported third-party app or need its advanced comparison features. <strong>Do not use an external tool when:</strong> GitKraken Desktop's built-in diff already gives you the context and controls you need.</p>
</div>

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
  <img src='/wp-content/uploads/beyond-compare@2x.png' class='help-center-img img-bordered' alt="Beyond Compare application menu with Install Command Line Tools option highlighted, used to enable CLI integration." />
  <figcaption style="text-align: center; color: #888;">Example setup with Beyond Compare.</figcaption>
</figure>

To use a different diff tool, go to <em class="context-menu">Preferences <i class="fa fa-caret-right"></i> External Tools</em> and set <kbd>External Diff Tool</kbd> to _Git Config Default_. Then add the appropriate configuration in your global `.gitconfig`:

### macOS
```
[diff]
    tool = meld
[difftool "meld"]
    cmd = open -a Meld --args "$LOCAL" "$REMOTE"
```

### Linux
```
[diff]
    tool = meld
[difftool "meld"]
    cmd = meld "$LOCAL" "$REMOTE"
```

### Windows
```
[diff]
    tool = meld
[difftool]
    prompt = false
[difftool "meld"]
    cmd = meld "$LOCAL" "$REMOTE"
```

***

## How to compare a WIP against another commit or branch

To compare your Work in Progress (WIP) with another commit or branch:
- Use <kbd>Ctrl/Cmd</kbd> + click to select the WIP and another commit
- Or, right-click a commit or branch and select <kbd>Compare commit against working directory</kbd>

<figure class='figure center'>
  <img src='/wp-content/uploads/compare-WIP-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the option to compare a selected commit against the working directory from the commit graph." />
  <figcaption style="text-align: center; color: #888;">Compare WIP with a commit or branch from the graph.</figcaption>
</figure>

***

## How to view file blame and history

To view a file's history or blame, open its diff and click **History** or **Blame** in the upper-right corner.

<figure class='figure center'>
  <img src='/wp-content/uploads/blame-history-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing Blame and History buttons in the file view toolbar for accessing file-level version history and author attributions." />
  <figcaption style="text-align: center; color: #888;">Use buttons in the top-right to view file history or blame.</figcaption>
</figure>

Alternatively, right-click a file after selecting a commit in the graph.

<figure class='figure center'>
  <img src='/wp-content/uploads/file-history-commit-selected-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing file history for a selected commit, with highlighted changes in the diff view panel." />
  <figcaption style="text-align: center; color: #888;">Access history or blame from the commit graph.</figcaption>
</figure>

Blame view color-codes each line or hunk by author.

<figure class='figure center'>
  <img src='/wp-content/uploads/blame-2025.png' class="help-center-img img-bordered" alt="Blame view in GitKraken Desktop showing author and date annotations alongside each line of code." />
  <figcaption style="text-align: center; color: #888;">Blame view showing per-line author contributions.</figcaption>
</figure>

Use the toggle in the top-right to switch between <kbd>Diff View</kbd> (showing changes) and <kbd>File View</kbd> (showing the full file with blame).

***

## How patch files work in GitKraken Desktop

<div class='callout callout--basic'>
    <p><strong>Use patches when:</strong> you need to share changes without pushing them to a remote. <strong>Do not rely on patches for binary files:</strong> GitKraken Desktop does not generate patches from binary files.</p>
</div>

A patch (or patch file) records the differences between files. Use patches to share changes without pushing them to a remote repository.

### How to create a patch from files or commits

To create a patch:
- Right-click a **commit** and choose <kbd>Create patch from commit</kbd>
- Right-click a **file** and choose <kbd>Create patch from file changes</kbd>

GitKraken Desktop asks you to name the patch file.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-patch-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the option to generate a patch file from a selected commit." />
  <figcaption style="text-align: center; color: #888;">Create a patch from a commit.</figcaption>
</figure>

<figure class='figure center'>
  <img src='/wp-content/uploads/patch-from-changes-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the option to generate a patch from unstaged file changes." />
  <figcaption style="text-align: center; color: #888;">Create a patch from file changes.</figcaption>
</figure>

You can also multi-select files or commits using <kbd>Shift</kbd> or <kbd>Cmd/Ctrl</kbd> + click, then right-click to create a patch. For selected commits, the patch contains the same combined changes shown in the Commit Panel. If GitKraken Desktop cannot show a combined diff for the selection, the patch action is unavailable.

<figure class='figure center'>
  <img src='/wp-content/uploads/patch-from-many-files-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop context menu showing the option to create a patch from changes across multiple unstaged files." />
  <figcaption style="text-align: center; color: #888;">Create a patch from multiple files or commits.</figcaption>
</figure>

### How to create a patch from the Command Palette

Launch the Command Palette from the toolbar or with <kbd>Cmd/Ctrl</kbd> + <kbd>P</kbd>, then search for "Create patch".

<figure class='figure center'>
  <img src="/wp-content/uploads/create-patch-from-command-palette.png" class="help-center-img img-bordered" alt="Command Palette in GitKraken Desktop displaying the option to create a patch from all working directory changes." />
  <figcaption style="text-align: center; color: #888;">Create a patch using the Command Palette.</figcaption>
</figure>

### How to apply a patch from the Command Palette

To apply a patch:
1. Open the Command Palette (<kbd>Cmd/Ctrl</kbd> + <kbd>P</kbd>).
2. Type "Apply patch" and select the command.
3. Choose your `.patch` file in the file explorer.

<figure class='figure center'>
  <img src='/wp-content/uploads/apply-patch-2025.png' class="help-center-img img-bordered" alt="Command Palette in GitKraken Desktop showing the option to apply a patch from the file system." />
  <figcaption style="text-align: center; color: #888;">Apply a patch from the file system.</figcaption>
</figure>

<div class='callout callout--basic'>
    <p><strong>Note:</strong> GitKraken Desktop does not generate patches from binary files. Patch support is a preliminary feature. For feedback, contact the GitKraken <a href="https://www.gitkraken.com/git-client/contact-support?product=gitkraken&source=help_center">support team</a>.</p>
</div>

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
