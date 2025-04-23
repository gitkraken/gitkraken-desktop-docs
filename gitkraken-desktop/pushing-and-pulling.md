---

title: Pushing and Pulling
description: Pushing and Pulling data from Remote Repos.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

Pushing and pulling are the keys to collaboration 🤝

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/EZFyiSLr-Bc?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>


***
## Adding Remotes
To add a new remote, click the <button class='button button--success button--ui button--nolink'>+</button> icon when hovering over <em class='context-menu'><img src='/wp-content/uploads/gk-remote-icon.svg' style='height:1em;'> Remote</em> in the Left Panel, then fill in the remote URL.

<img src="/wp-content/uploads/add-remote.png" srcset="/wp-content/uploads/add-remote@2x.png" class="help-center-img img-bordered">

When using an integration like GitHub or Bitbucket, select the remotes from your collaborators in the dropdown box.  This makes viewing other forks of the same repository quick and easy.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> When using an integration, the drop-down box will only display <strong>Forks</strong> of this repository. If you would like to add a remote that is not a fork you can still do so via the URL option.</p>
</div>

You can identify remote branches in the Commit Graph through the following icons:

 + <em class='context-menu'><i class="fab fa-github"></i></em> &mdash; GitHub
 + <em class='context-menu'><i class="fab fa-bitbucket" aria-hidden="true"></i></em> &mdash; Bitbucket
 + <em class='context-menu'><i class="fab fa-gitlab" aria-hidden="true"></i></em> &mdash; GitLab
 + <em class='context-menu'><i class="fab fa-windows" aria-hidden="true"></i></em> &mdash; Azure DevOps
 + <em class='context-menu'><i class="fa fa-globe" aria-hidden="true"></i></em> &mdash; Other Remote Server

All remote branches are located in the Left Panel.

***

## Push <img src='/wp-content/uploads/gk-push-icon.svg' style='height:1em;'>
Pushing takes any local changes <em class='context-menu'><i class="fa fa-laptop" aria-hidden="true"></i></em>, and making them available on the remote <em class='context-menu'><i class="fa fa-globe" aria-hidden="true"></i></em>.

Push the currently checked out branch by clicking <kbd>Push <img src='/wp-content/uploads/gk-push-icon.svg' style='height:1em;'></kbd> in the main toolbar, or by right clicking on the branch, and selecting <em class='context-menu'>Push</em>.

<img src="/wp-content/uploads//push.png" srcset="/wp-content/uploads//push@2x.png" class="help-center-img img-bordered">

Pushing attempts to upload any new commits to the remote branch, then fast-forward the remote to bring it up to date with the local repo.

If the remote branch cannot be fast-forwarded, the push will be refused.  If this is the case, GitKraken Desktop will provide the option to _Pull (fast-forward if possible)_, or <button class='button button--danger button--ui button--nolink'>Force Push</button>.

<div class='callout callout--warning'>
    <p><strong>Caution:</strong> Forcing a push is considered destructive because it overwrites the remote branch by replacing it with the local branch.</p>
</div>

If the branch pushed does not exist on the remote, GitKraken Desktop will prompt you to name and create the new remote branch.  This is typically the fork name followed by a slash, and the branch name. i.e. `origin/my-branch`.

### Drag and drop to push

Drag and drop a branch to a remote to access the <kbd>Push</kbd> action. You may drag a branch to a remote branch on the Commit Graph, or to a remote branch listed in the Left Panel.

<img src="/wp-content/uploads/push-branch-2025-HD.gif" srcset="/wp-content/uploads/push-branch-2025-HD.gif" class="help-center-img img-bordered">

***
## Fetching
Pulling and fetching take updates from the remote and get them into our local repo. You can fetch by selecting the Pull dropdown. Additionally, you can select the radio button next to the desired option to change the behavior of this button.

<img src="/wp-content/uploads/fetch-menu-2025.png" srcset="/wp-content/uploads/fetch-menu-2025@2x.png" class="help-center-img img-bordered">

### Fetch All
Fetching gets updates from remote branches, but does not update any files in your working directory.

Updates will appear in the graph, and also update any branches on the left to show how many commits you are ahead or behind.

When you're behind the remote, it means that there are commits on the remote branch which have not been incorporated into the local repo. _Pull (fast-forward if possible)_ to get these changes on local.

<img src="/wp-content/uploads/branch-behind-2025.png" srcset="/wp-content/uploads/branch-behind-2025@2x.png" class="help-center-img img-bordered">

If you are ahead of the remote branch, there are local commits that have not yet been pushed to the remote.

It is possible to be both ahead of and behind a remote.  However if you are both ahead and behind a remote, you will not be able to perform a _Pull (fast-forward if possible)_ as the branches have diverged. Consider rebasing onto the remote first.

GitKraken Desktop automatically fetches updates from your remote repositories every minute by default.  You can change this setting from <kbd><strong>Preferences > General</strong></kbd> menu.

### Fast-forwarding
Fast forwarding moves the currently checked out commit to one that was added later, replaying all commits in between in the order which they happened.

<img src="/wp-content/uploads/pull-ff-2025.png" srcset="/wp-content/uploads/pull-ff-2025@2x.png" class="help-center-img img-bordered">

To fast-forward your currently checked out commit, you can right click on the branch with newer commits, and select the <em class='context-menu'>Fast-Forward</em> option from the menu.

<img src="/wp-content/uploads/pull-ff-left-panel.png" srcset="/wp-content/uploads/pull-ff-left-panel@2x.png" class="help-center-img img-bordered">

***
## Pulling <img src='/wp-content/uploads/gk-pull-icon.svg' style='height:1em;'>
Pulling first performs a fetch and then incorporates any commits in the remote repository into the local copy.

There are three pulling options. Let's demonstrate what each one does by starting with an example 2 commits made locally, and 2 that have been made on the remote.
<figure class='figure center'>
    <img src='/wp-content/uploads/remote-commit-2025.png' srcset="/wp-content/uploads/remote-commit-2025@2x.png">
    <figcaption>The remote commits display on the graph because they have been fetched,</br>but have not been incorporated into the local repo.</figcaption>
</figure>

### Pull (fast-forward if possible)
_Pull (fast-forward if possible)_ fetches any updates on the remote branch, then attempts to _fast-forward_ the local branch.  If a _fast-forward_ is not possible, a _merge_ will be performed.

This is the default option for new GitKraken Desktop users.

<figure class='figure center'>
    <img src='/wp-content/uploads/pull-ff-ex-2025.png' srcset="/wp-content/uploads/pull-ff-ex-2025@2x.png">
    <figcaption>A fast-forward was not possible, so the remote branch was merged into the local branch.</figcaption>
</figure>

### Pull (fast-forward only)
_Pull (fast-forward only)_ fetches any updates and then attempts a _fast-forward_.  If a fast-forward is not possible, GitKraken Desktop will not make any changes to the local repo.

In our 2-commit example, a fast-forward is not possible as there are new commits added to both branches.

### Pull (rebase)
_Pull (rebase)_ stashes all commits on this branch, pulls in new commits from the remote, and then replays your commits.  This has the added benefit of maintaining all commits in a single line, as opposed to creating branches which are then merged back together.

<figure class='figure center'>
    <img src='/wp-content/uploads/pull-rebase-2025.png' srcset="/wp-content/uploads/pull-rebase-2025@2x.png">
    <figcaption>The remote commits were pulled in, then the local commits were moved on top of them.</figcaption>
</figure>

### Setting a default pull option
Set the default pull option by clicking the down arrow to the right, and clicking on the circle button by each option.

<img src="/wp-content/uploads/set-default.png" srcset="/wp-content/uploads/set-default@2x.png" class="help-center-img img-bordered">

Our [interface](/start-here/interface) page covers this and more.


***
## Setting the upstream branch
Whenever pushing, pulling, or fetching, GitKraken Desktop gets updates from the _Upstream_ branch.

The _Upstream_ defaults to the remote branch where the local branch was checked out, but you may change the _Upstream_ to push, pull, or fetch from a different branch.

Right click on a branch to <a href="https://gitkraken.com/learn/git/problems/git-set-upstream-branch" target="_blank">set the upstream</a> or click the <kbd> <i class="fa fa-ellipsis-v"></i> </kbd> option.

<img src="/wp-content/uploads/upstream.png" srcset="/wp-content/uploads//upstream@2x.png" class="help-center-img img-bordered">

Alternatively, drag and drop a branch to push instead of setting upstream.

<img src="/wp-content/uploads/drag-and-drop-push-2025.gif" class="help-center-img img-bordered">
