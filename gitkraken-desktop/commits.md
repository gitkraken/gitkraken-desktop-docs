---
title: Committing Changes
description: Learn how to commit changes in GitKraken Desktop, including staging files, co-authoring, templates, amending commits, and resetting or reverting history.
product: GitKraken Desktop
feature: Commits
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
tags: [commits, amend, revert, reset, co-authors]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to create commits, stage files, add co-authors, work with commit templates, amend recent history, and undo or revert changes in GitKraken Desktop. Basic local commit workflows are available in the app, while actions that rewrite pushed history require extra care because they may require a force push.

**Key constraints**
- Commit scope: This page covers local commit workflows in GitKraken Desktop
- History rewrite warning: Amending a commit that has already been pushed requires a force push to update the remote branch
- Hook behavior: Selecting **Skip Git hooks** bypasses all configured Git hooks for that commit
- Commit templates: Repository-local commit templates take precedence over global templates
- Undo vs. revert: Use Undo for local history changes you have not shared yet; use Revert when you need to preserve published history with a new reversing commit

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8a6fYPkBDbY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## Quick Start

Create a commit in GitKraken Desktop by staging your changes and entering a commit message.

1. Save changes to your files. The **WIP** (Work in Progress) node appears at the top of the Commit Graph.
2. Click the WIP node to open the Commit Panel and view changed files.
3. Click a file to review its diff, then click the checkbox or the file name to stage it. To stage all files, press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd>.
4. Enter a commit message in the message field.
5. Click **Commit**, or press <kbd>Cmd</kbd>/<kbd>Enter</kbd> (macOS) or <kbd>Ctrl</kbd>/<kbd>Enter</kbd> (Windows/Linux).

To commit and push in one step, enable the **Push after committing** option before clicking **Commit**.

To amend the most recent commit, stage any additional changes, then check **Amend the previous commit** in the Commit Panel. To update only the message, click the most recent commit in the graph and edit the message field directly, then click **Update Message**.

To undo a commit, press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>Z</kbd> or click the **Undo** button in the toolbar.

***

<a id="making-a-commit"></a>

## How to create a commit

To create a commit, select your _Work in Progress_ (WIP) node to view file changes in the Commit Panel.

<div class='callout callout--basic'>
    <p><strong>Use this workflow when:</strong> you are recording a logical set of local changes that belong together in one commit. <strong>Don't use it when:</strong> your changes should be split into multiple commits first, or when you need to preserve published history without rewriting it.</p>
</div>

<figure class='figure center'>
    <img src='/wp-content/uploads/select-WIP-2025.png' class="help-center-img img-bordered" alt="WIP node displayed at the top of the GitKraken Commit Graph with a file listed as modified but unstaged." />
    <figcaption style="text-align: center; color: #888;">The WIP node appears at the top of the Commit Graph when you save file changes.</figcaption>
</figure>

Select files to stage by clicking them individually or reviewing diffs. To stage all files:
- **Mac:** <kbd>&#8984;</kbd><kbd>Shift</kbd><kbd>S</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>S</kbd>

Type your commit message, then click **Commit**, or use the shortcut:
- **Mac:** <kbd>&#8984;</kbd> + <kbd>Enter</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd> + <kbd>Enter</kbd>

<a id="commit-and-push"></a>

### How to commit and push in one step

To commit and immediately push changes, stage files and enter a message. Then select the **Commit and Push** option.

<figure class='figure center'>
    <img src='/wp-content/uploads/push-after-commit-2025.png' class="help-center-img img-bordered" alt="Commit panel in GitKraken showing a commit message, the 'Push after committing' checkbox enabled, and a green button labeled 'Commit Changes to 2 Files and Push'." />
    <figcaption style="text-align: center; color: #888;">Enable this option to commit and push changes in one step.</figcaption>
</figure>

The graph updates with your commit. If needed, undo it with:
- **Mac:** <kbd>&#8984;</kbd> + <kbd>Z</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd> + <kbd>Z</kbd>

<a id="committing-with-co-authors"></a>

### How to add co-authors to a commit

To credit co-authors in a commit, add lines to the commit message using the following format:

```
Co-authored-by: Name One <email1@example.com>
Co-authored-by: Name Two <email2@example.com>
```

<figure class='figure center'>
    <img src='/wp-content/uploads/co-author@2x.png' class="help-center-img img-bordered" alt="GitKraken commit panel showing a commit message with a co-author attribution line using the format 'Co-authored-by: Name <email>'." />
    <figcaption style="text-align: center; color: #888;">Use this syntax to attribute co-authors in a commit.</figcaption>
</figure>

Co-authors appear in the Commit Panel history:

<figure class='figure center'>
    <img src='/wp-content/uploads/co-author-history@2x.png' class="help-center-img img-bordered" alt="Commit details in GitKraken showing a co-authored commit with the primary author and a listed co-author under the commit message." />
    <figcaption style="text-align: center; color: #888;">Co-authors are listed with the primary author in the commit history.</figcaption>
</figure>

### How to bypass Git hooks for one commit

To skip Git hooks for a specific commit, enable the **Skip Git hooks** checkbox in the Commit Panel.

<div class='callout callout--warning'>
    <p><strong>Warning:</strong> Skipping this will bypass all configured Git hooks for the commit action.</p>
</div>

<figure class='figure center'>
    <img src='/wp-content/uploads/skip-commits-2025.png' class="help-center-img img-bordered" alt="GitKraken commit panel with 'Skip Git hooks' option enabled, showing a commit message and the commit button labeled to reflect skipping hooks." />
    <figcaption style="text-align: center; color: #888;">Enable this option to bypass Git commit hooks.</figcaption>
</figure>

***

<a id="commit-templates"></a>

## How commit templates work

<a id="reading-the-commit-template"></a>

### How GitKraken Desktop chooses a commit template

When you open a repository, GitKraken Desktop checks for a commit template in this order:

1. The repository’s local `.git/config` file
2. Your global `.gitconfig`
3. If neither contains a `commit.template` setting, GitKraken Desktop does not load a template

<a id="creating-and-updating-the-commit-template"></a>

### How to create or update a commit template

To create or update a commit template, navigate to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> Commit</em>.

<figure class='figure center'>
    <img src='/wp-content/uploads/commit-template-setting-2025.png' class="help-center-img img-bordered" alt="GitKraken Commit Preferences showing Commit Template settings with summary and description fields for prefilled commit messages." />
    <figcaption style="text-align: center; color: #888;">Set an initial commit message in Preferences &gt; Commit.</figcaption>
</figure>

If a template is loaded from your local config, GitKraken Desktop saves changes to that file. If no template exists, your changes are saved to a new `gkcommittemplate.txt` file in your repo’s `.git/` directory. GitKraken Desktop also updates the `commit.template` path in the local config.

This setup lets you maintain a local template without altering your global Git configuration.

#### Commit Template Options

- **Apply this template to commit messages**: Automatically inserts the template in the message editor.
- **Remove comments from commit messages**: Omits lines starting with `#` when applying the template.

### How to configure commit templates

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

## How to amend the most recent commit

GitKraken Desktop lets you modify the last commit by updating the message, adding new changes, or both.

<div class='callout callout--basic'>
    <p><strong>Use amend when:</strong> you need to fix the most recent commit before others depend on it. <strong>Don't use amend when:</strong> the commit is already shared and you want to avoid rewriting remote history for collaborators.</p>
</div>

<div class='callout callout--warning'>
    <p><strong>Warning:</strong> If you have already pushed the commit, amending it changes history and requires a force push to update the remote branch.</p>
</div>

To include new changes:
1. Modify files in your working directory.
2. Stage the changes.
3. Select **Amend the previous commit** in the Commit Panel.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-commit-2025.png' class="help-center-img img-bordered" alt="GitKraken Commit panel with 'Amend previous commit' checkbox selected, showing an updated commit message and the 'Amend Previous Commit' button." />
    <figcaption style="text-align: center; color: #888;">Select this option to append changes to the most recent commit.</figcaption>
</figure>

To update only the message:
1. Select the most recent commit in the graph.
2. Click into the message box and revise the text.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-message-2025.png' class="help-center-img img-bordered" alt="GitKraken commit details panel with the commit message shown and a tooltip indicating the option to amend the commit message." />
    <figcaption style="text-align: center; color: #888;">Edit your previous commit message directly in the message field.</figcaption>
</figure>

To resize the commit message field, drag the bottom edge of the editor.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-box-2025.png' class="help-center-img img-bordered" alt="Commit amend view in GitKraken with message editing field and buttons to update or cancel the commit message." />
    <figcaption style="text-align: center; color: #888;">Resize the commit message box as needed.</figcaption>
</figure>

Use the **Update Message** button to save changes, or **Cancel Amend** to discard them.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> If you’ve already pushed a commit, amending it will require a force push to update the remote history.</p>
</div>

***

<a id="resetting-commits"></a>

## How to reset commits

Git uses a pointer called <code>HEAD</code> to track your current commit. Resetting updates <code>HEAD</code> to point to a specific commit in your history. GitKraken Desktop offers three reset types:

<div class='callout callout--basic'>
    <p><strong>Use reset when:</strong> you need to move local history to another commit and you understand whether you want to keep staged or working directory changes. <strong>Don't use reset when:</strong> you need a safe, shareable reversal of changes that are already published to a remote branch.</p>
</div>

- **Soft** — Moves <code>HEAD</code> to the selected commit and retains staged and working directory changes.
- **Mixed** — Moves <code>HEAD</code>, unstages files, but retains working directory changes.
- **Hard** — Moves <code>HEAD</code>, unstages files, and discards all changes in your working directory.

<figure class='figure center'>
    <img src='/wp-content/uploads/reset-commit-2025.png' class="help-center-img img-bordered" alt="GitKraken context menu showing 'Reset main to this commit' with soft, mixed, and hard reset options." />
    <figcaption style="text-align: center; color: #888;">Right-click a commit or branch to access reset options.</figcaption>
</figure>

You can also drag and drop a branch onto another to initiate a reset, or use the left panel for local repository actions.

***

<a id="reverting-changes"></a>

## How to undo local changes before pushing

GitKraken Desktop provides an **Undo** button to reverse recent actions that haven’t been pushed.

<div class='callout callout--basic'>
    <p><strong>Use Undo when:</strong> you want to reverse a recent local action that has not been pushed yet. <strong>Use Revert Commit when:</strong> the commit is already part of shared history and you need a new commit that reverses it safely.</p>
</div>

<figure class='figure center'>
    <img src='/wp-content/uploads/undo-undo-2025.png' class="help-center-img img-bordered" alt="GitKraken interface showing Undo button highlighted with tooltip 'Undo Commit amend Updates the GitKraken commit documentation to reflect UI'." />
    <figcaption style="text-align: center; color: #888;">Click Undo to revert local actions before they are pushed.</figcaption>
</figure>

You can also use the Undo shortcut:
- **Mac:** <kbd>&#8984;</kbd> + <kbd>Z</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd> + <kbd>Z</kbd>

<a id="reverting-commits"></a>

### How to revert a commit that is already in history

If Undo is not available, you can still reverse changes by creating a **revert commit**.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/U_axv67W1Ik?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

Right-click any commit node in the graph and choose **Revert Commit**. GitKraken Desktop will create a new commit that undoes the changes from the selected commit.

<figure class='figure center'>
    <img src='/wp-content/uploads/revert-commit-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken showing the 'Revert commit' option highlighted." />
    <figcaption style="text-align: center; color: #888;">Use the revert option to create a new commit that undoes a previous one.</figcaption>
</figure>

## How to restore files from a commit

GitKraken Desktop lets you restore any file to its state at a specific commit and place it directly into your working directory (WIP). This is useful when you want to retrieve an older version of a file, resurrect a deleted file, or selectively reverse changes without affecting the rest of your working directory.

To restore a file from a commit:
1. Select a commit in the Commit Graph to open it in the Commit Panel.
2. Right-click any file listed in the Commit Panel.
3. Select **Restore file from this commit**.

The file is placed into your working directory as a staged change, ready to include in your next commit.

<figure class=’figure center’>
    <img src=’/wp-content/uploads/restore-files.png’ class="help-center-img img-bordered" alt="GitKraken Desktop Commit Panel showing multiple files selected from a commit’s file list, with a right-click context menu displaying the ‘Restore selected files from this commit’ option highlighted" />
    <figcaption style="text-align: center; color: #888;">Right-click a file in the Commit Panel to restore it to your working directory.</figcaption>
</figure>

To restore multiple files at once, hold <kbd>Shift</kbd> or <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> to multi-select files in the Commit Panel, then right-click and select **Restore selected files from this commit**.

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
