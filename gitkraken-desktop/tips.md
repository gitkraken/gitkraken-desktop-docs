---

title: Tips
description: Find out all the things users should know to boost their GitKraken Desktop experience.
taxonomy:
    category: gitkraken-desktop

---
<kbd>>Last updated: April 2025</kbd>
Here's the TLDR of the best features in GitKraken Desktop.

***

### 1. Set up Profiles

If you have personal projects you wish to separate from work repos–or if you need to connect to multiple instances of GitHub, GitLab, Bitbucket, etc.–then set up [Profiles](/start-here/profiles).

<img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered">

Each profile stores different app preferences and Git config information, which makes it easier to switch context.

<div class='callout callout--success'>
    <p>Note, access to multiple profiles requires a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.</p>
</div>

***

### 2. Use the Command Palette

Work like the pros, and use the [Command Palette](/start-here/command-palette) to quickly access GitKraken Desktop actions.

<img src="/wp-content/uploads/command-palette-2025.gif" srcset="/wp-content/uploads/command-palette-2025.gif" class="help-center-img img-bordered">

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

<img src='/wp-content/uploads/multi-cherry-pick-menu.png' class="help-center-img img-bordered">

From here, you can decide to reorder, squash, drop, or rename commits before completing the cherry pick. Learn more about [Interactive Cherry Pick](/gitkraken-desktop/cherrypick/)

***

### 6. Integrate with GitHub, GitLab, Bitbucket, and Azure DevOps

GitKraken Desktop allows you to authenticate with GitHub, GitLab, Bitbucket, and Azure DevOps (previously VSTS), which will help you find repos when cloning or adding your remotes.

<img src="/wp-content/uploads/authentication.png" srcset="/wp-content/uploads/authentication@2x.png" class="img-bordered img-responsive center">

Availability of Integrations can vary based on your Gitkraken plan.
- Community Plan users are limited to public repos only for Github.com, Gitlab.com, and Bitbucket cloud.
- Azure DevOps cloud availability is restricted to Pro users.
- All Self-Hosted server integrations require an Advanced subscription tiers or higher

#### Benefits

- Create repositories on GitHub/GitLab/Bitbucket/Azure DevOps including .gitignore and license
- Save authentication into profiles
- Clone from remote repo list
- Add remotes 
- Create and view pull requests

***

### 7. Build Status, Assignees, and Reviewers in PRs

If you are using the GitLab or GitHub integration, you may also add a pull request assignee and label(s) to your pull request. GitKraken Desktop will then pass these values onto GitLab or GitHub when the pull request is created. 

<img src='/wp-content/uploads/gitlab-assignee.png' srcset='/wp-content/uploads/gitlab-assignee@2x.png' class='img-bordered img-responsive center'>

If you are using the GitHub integration, you may also add reviewers and multiple assignees to a pull request. 

<img src='/wp-content/uploads/github-assignee.png' srcset='/wp-content/uploads/github-assignee@2x.png' class='img-bordered img-responsive center'>

Additionally for GitHub pull requests, this tooltip will show assignees, labels, reviewers, and build status.

<img src='/wp-content/uploads/tooltip-github.png' srcset='/wp-content/uploads/tooltip-github@2x.png' class='img-bordered img-responsive center'>

Learn more about [pull requests](/working-with-repositories/pull-requests).

***

### 8. File History and File Blame

File History and File Blame information display in the same view.

To access either option, first click on a commit in the graph. Then right click a file to access File History or File Blame.

<img src='/wp-content/uploads/file-history.png' srcset='/wp-content/uploads/file-history@2x.png 2x' class='img-bordered img-responsive center'>

File History shows that file's commit history on the left.

<img src='/wp-content/uploads/file-diff.png' srcset='/wp-content/uploads/file-diff.png 2x' class='img-bordered img-responsive center'>

Use the top toggle button to switch between Diff View, which shows the selected commit's changes to the file, and the File View, which shows the file's state at that commit, including the blame info.

***

### 9. Gitkraken Desktop Terminal

The GitKraken Desktop terminal is a fully-featured terminal emulator that allows you to run Git commands directly from the app.
Click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar.

To open the current repo folder in an external terminal, go to <em class="context-menu">File <i class='fa fa-caret-right'></i> Open Terminal</em> or use the keyboard shortcuts <kbd>opt</kbd> + <kbd>T</kbd> (Mac) / <kbd>alt</kbd> + <kbd>T</kbd> (Windows + Linux). 

You can set your default terminal from <em class="context-menu">Preferences <i class='fa fa-caret-right'></i> External Tools</em>.


***

### 10. Resize the Graph

It's simple, but easy to miss. Hover over any of the colored lines to drag and drop the graph.

<img src='/wp-content/uploads/graph-gif.gif' class='figure img-floated img-floated--right'>


Resize and marvel at the colors of the rainbow.



