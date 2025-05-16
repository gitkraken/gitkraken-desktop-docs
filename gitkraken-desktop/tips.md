---

title: Tips
description: Find out all the things users should know to boost their GitKraken Desktop experience.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

Here's the TLDR of the best features in GitKraken Desktop.

***

### 1. Set up Profiles

If you have personal projects you wish to separate from work repos–or if you need to connect to multiple instances of GitHub, GitLab, Bitbucket, etc.–then set up [Profiles](/start-here/profiles).

<figure class='figure center'>
    <img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Each profile can save a unique integration connection.</figcaption>
</figure>

Each profile stores different app preferences and Git config information, which makes it easier to switch context.

<div class='callout callout--success'>
    <p>Note, access to multiple profiles requires a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.</p>
</div>

***

### 2. Use the Command Palette

Work like the pros, and use the [Command Palette](/start-here/command-palette) to quickly access GitKraken Desktop actions.

<figure class='figure center'>
    <img src="/wp-content/uploads/command-palette-2025.gif" srcset="/wp-content/uploads/command-palette-2025.gif" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Use the Command Palette to open the current repo in VS Code and more.</figcaption>
</figure>

As you type, the Command Palette will find the most relevant commands, allowing you to perform many actions without clicking. Here are a few examples:

<h3>Core:</h3>

 * `Redo`
 * `Undo`

<h3>File:</h3>

* `Create File` + `filename`
* `Delete File` + `filename`
* `Open File` + `filename`
* `View File` + `filename`
* `Edit File` + `filename`
* `Discard all changes`
* `Stage all changes`
* `Unstage all changes`



***

### 3. Keyboard Shortcuts

For fast fingers, check out our [keyboard shortcuts](/start-here/keyboard-shortcuts). These will help you blitz through the app.

<table class='table table--bordered table--shortcuts'>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Open keyboard shortcuts</td>
            <td><kbd>&#8984;</kbd><kbd>/</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>/</kbd></td>
        </tr>
    </tbody>
</table>

***

### 4. Cherry Pick Multiple Commits

To cherry pick multiple commits, you can select multiple commits by holding down the <kbd>Cmd/Ctrl</kbd> or <kbd>Shift</kbd> key and clicking on the desired commits. Then, right-click on one of the selected commits and choose the "Cherry pick X commits" option.

<figure class='figure center'>
    <img src='/wp-content/uploads/multi-cherry-pick-menu.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Select multiple commits from the Commit Graph to access multi-cherry pick.</figcaption>
</figure>

From here, you can decide to reorder, squash, drop, or rename commits before completing the cherry pick. Learn more about [Interactive Cherry Pick](/gitkraken-desktop/cherrypick/)

***

### 6. Integrate with GitHub, GitLab, Bitbucket, and Azure DevOps

GitKraken Desktop allows you to authenticate with [GitHub, GitLab, Bitbucket, and Azure DevOps](/gitkraken-desktop/integrations/) (previously VSTS), which will help you find repos when cloning or adding your remotes.

<figure class='figure center'>
    <img src="/wp-content/uploads/connect-azure-devops-2025.png" srcset="/wp-content/uploads/connect-azure-devops-2025@2x.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Connect your remote hosting service to get more bang for your buck.</figcaption>
</figure>

Availability of integrations can vary based on your GitKraken subscription.
- Community plan users are limited to public repos only for GitHub.com, GitLab.com, and Bitbucket Cloud
- Azure DevOps Cloud integration requires a GitKraken subscription
- All Self-Hosted server integrations require an Advanced subscription tiers or higher

#### Benefits

- Create repositories on GitHub/GitLab/Bitbucket/Azure DevOps including .gitignore and license
- Save authentication into profiles
- Clone from remote repo list
- Add remotes 
- Create and view pull requests

***

### 7. Hide and Solo branches

Tailor the Commit Graph to display the branches you need with [Hiding and Soloing](/gitkraken-desktop/hiding-and-soloing/). Hide branches temporarily, or solo 1 branch focus it in the app.

<div class="flex-wrap" style="align-items: flex-start">
    <div class="flex-item">
        <img src="/wp-content/uploads/gk-hide-icon-green.svg" class='img-responsive' style="width: 70px; height: 70px">
    </div>
    <div class="flex-item">
        <h3>Hide</h3>
        <p>Hides the selected branch from the graph.</p>
        <p>To hide a branch, mouse over that branch, and you will see the eye <i class='fa fa-eye icon-green'></i> icon appear to the left of the branch name; click this to hide. Or perform this task by right-clicking the branch and selecting `Hide`.</p>
        <p>Hidden branches will now have a gray eye <i class='fa fa-eye-slash'></i> icon. Clicking this will restore that repo to the graph.</p>
    </div>
</div>

 <div class="flex-wrap" style="align-items: flex-start">
    <div class="flex-item">
        <img src="/wp-content/uploads/gk-solo-icon-orange.svg" class='img-responsive' style="width: 70px; height: 70px">
    </div>
    <div class="flex-item">
        <h3>Solo</h3>
        <p>Soloing a branch will hide all other branches which have not been soloed, showing <i>only</i> soloed branches.</p>
        <p>To solo a branch, right-click the branch and select `Solo`. This initiates Solo Mode, with soloed branches highlighted in orange and with a solid orange <i class='fa fa-dot-circle-o icon-orange'></i> icon to the left of the branch name.</p>
        <p>Solo/unsolo additional branches by clicking on the semi-opaque icon to the left of that branch's name.</p>
        <p>Consider hiding/soloing entire remotes if you only need about two remotes, and then hiding everything else.</p>
    </div>
</div>
***

### 8. File History and File Blame

[File History and File Blame](/gitkraken-desktop/diff/#file-blame-and-history) information display in the same view.

To access either option, first click on a commit in the graph. Then right click a file to access File History or File Blame.

<figure class='figure center'>
    <img src='/wp-content/uploads/file-history-content-menu-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Right-click a file to get access to its History or Blame.</figcaption>
</figure>


File History shows that file's commit history on the left.

<figure class='figure center'>
    <img src='/wp-content/uploads/file-diff-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Review the list and diffs of all commits made to this file.</figcaption>
</figure>

Use the top toggle button to switch between Diff View, which shows the selected commit's changes to the file, and the File View, which shows the file's state at that commit, including the blame info.

***

### 9. GitKraken Desktop Terminal

The [GitKraken Desktop terminal](/gitkraken-desktop/terminal/) is a fully-featured terminal emulator that allows you to run Git commands directly from the app.
Click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar.

To open the current repo folder in an external terminal, go to <em class="context-menu">File <i class='fa fa-caret-right'></i> Open Terminal</em> or use the keyboard shortcuts <kbd>opt</kbd> + <kbd>T</kbd> (Mac) / <kbd>alt</kbd> + <kbd>T</kbd> (Windows + Linux). 

You can set your default terminal from <em class="context-menu">Preferences <i class='fa fa-caret-right'></i> External Tools</em>.


***

### 10. Resize the Graph

It's simple, but easy to miss. Hover over any of the colored lines to drag and drop the graph.

<figure class='figure center'>
    <img src='/wp-content/uploads/graph-drag-2025.gif' class='figure img-floated img-floated--right'>
    <figcaption style="text-align: center; color: #888;">Resize the graph to your liking.</figcaption>
</figure>


Resize and marvel at the colors of the rainbow.



