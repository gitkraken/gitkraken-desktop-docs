---
title: Committing Changes
description: Learn how to commit changes in GitKraken Desktop, including staging files, co-authoring, templates, amending commits, and resetting or reverting history.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: February 2026</kbd>

GitKraken Desktop simplifies the Git commit process by helping you stage, commit, and push your work from a visual interface.

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

## Making a commit

To create a commit, select your _Work in Progress_ (WIP) node to view file changes in the Commit Panel.

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

### Commit and push

To commit and immediately push changes, stage files and enter a message. Then select the **Commit and Push** option.

<figure class='figure center'>
    <img src='/wp-content/uploads/push-after-commit-2025.png' class="help-center-img img-bordered" alt="Commit panel in GitKraken showing a commit message, the 'Push after committing' checkbox enabled, and a green button labeled 'Commit Changes to 2 Files and Push'." />
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
    <img src='/wp-content/uploads/co-author@2x.png' class="help-center-img img-bordered" alt="GitKraken commit panel showing a commit message with a co-author attribution line using the format 'Co-authored-by: Name <email>'." />
    <figcaption style="text-align: center; color: #888;">Use this syntax to attribute co-authors in a commit.</figcaption>
</figure>

Co-authors appear in the Commit Panel history:

<figure class='figure center'>
    <img src='/wp-content/uploads/co-author-history@2x.png' class="help-center-img img-bordered" alt="Commit details in GitKraken showing a co-authored commit with the primary author and a listed co-author under the commit message." />
    <figcaption style="text-align: center; color: #888;">Co-authors are listed with the primary author in the commit history.</figcaption>
</figure>

### Bypass Git hooks

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
    <img src='/wp-content/uploads/commit-template-setting-2025.png' class="help-center-img img-bordered" alt="GitKraken Commit Preferences showing Commit Template settings with summary and description fields for prefilled commit messages." />
    <figcaption style="text-align: center; color: #888;">Set an initial commit message in Preferences &gt; Commit.</figcaption>
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

## Resetting Commits

Git uses a pointer called <code>HEAD</code> to track your current commit. Resetting updates <code>HEAD</code> to point to a specific commit in your history. GitKraken Desktop offers three reset types:

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

## Reverting Changes

GitKraken Desktop provides an **Undo** button to reverse recent actions that haven’t been pushed.

<figure class='figure center'>
    <img src='/wp-content/uploads/undo-undo-2025.png' class="help-center-img img-bordered" alt="GitKraken interface showing Undo button highlighted with tooltip 'Undo Commit amend Updates the GitKraken commit documentation to reflect UI'." />
    <figcaption style="text-align: center; color: #888;">Click Undo to revert local actions before they are pushed.</figcaption>
</figure>

You can also use the Undo shortcut:
- **Mac:** <kbd>&#8984;</kbd> + <kbd>Z</kbd>
- **Windows/Linux:** <kbd>Ctrl</kbd> + <kbd>Z</kbd>

<a id="reverting-commits"></a>

### Reverting Commits

If Undo is not available, you can still reverse changes by creating a **revert commit**.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/U_axv67W1Ik?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

Right-click any commit node in the graph and choose **Revert Commit**. GitKraken Desktop will create a new commit that undoes the changes from the selected commit.

<figure class='figure center'>
    <img src='/wp-content/uploads/revert-commit-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken showing the 'Revert commit' option highlighted." />
    <figcaption style="text-align: center; color: #888;">Use the revert option to create a new commit that undoes a previous one.</figcaption>
</figure>
<style>
pre{position:relative}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;width:28px;height:28px;padding:0;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2 2v1"></path></svg>',K='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p;cp(el.innerText.replace(/\n$/,'')).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
