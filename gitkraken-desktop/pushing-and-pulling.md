---
title: Push, Pull, and Fetch in GitKraken Desktop
description: Learn how to push, pull, and fetch changes with GitKraken Desktop. Understand upstream branches, default pull behavior, and drag-and-drop actions.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

Push, pull, and fetch operations are essential for synchronizing local work with remote repositories in GitKraken Desktop.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/EZFyiSLr-Bc?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## Add a Remote

To add a remote:
1. Hover over <em class='context-menu'><img src='/wp-content/uploads/gk-remote-icon.svg' style='height:1em;'> Remote</em> in the Left Panel.
2. Click the <button class='button button--success button--ui button--nolink'>+</button> icon.
3. Enter the remote URL or choose from integration-based dropdowns (GitHub, GitLab, Bitbucket).

<figure>
  <img src="/wp-content/uploads/add-remote.png" 
       srcset="/wp-content/uploads/add-remote@2x.png 2x"
       class="help-center-img img-bordered"
       alt="Add Remote dialog in GitKraken Desktop with GitHub selected">
  <figcaption style="text-align:center; color:#888">
    Add a remote from the Left Panel
  </figcaption>
</figure>

<div class='callout callout--warning'>
  <p><strong>Note:</strong> Integration dropdowns show forks only. For non-fork remotes, use the URL option.</p>
</div>

Remote icons in the Commit Graph:
- <i class="fab fa-github"></i> GitHub
- <i class="fab fa-bitbucket"></i> Bitbucket
- <i class="fab fa-gitlab"></i> GitLab
- <i class="fab fa-windows"></i> Azure DevOps
- <i class="fa fa-globe"></i> Other

***

## Push Changes <img src='/wp-content/uploads/gk-push-icon.svg' style='height:1em;'>

To push local commits to a remote branch:
- Click <kbd>Push</kbd> in the main toolbar
- Or right-click a branch and select <em class='context-menu'>Push</em>

<figure>
  <img src="/wp-content/uploads//push.png" 
       srcset="/wp-content/uploads//push@2x.png" 
       class="help-center-img img-bordered"
       alt="Push button in GitKraken Desktop toolbar">
  <figcaption style="text-align:center; color:#888">Push a local branch to its upstream</figcaption>
</figure>

If a remote branch doesn’t exist yet, GitKraken will prompt you to name and create it.

<div class='callout callout--warning'>
  <p><strong>Caution:</strong> If fast-forwarding fails, GitKraken may offer a <kbd>Force Push</kbd> option. Use with care.</p>
</div>

### Drag and Drop Push
Drag a branch onto a remote branch (in the graph or Left Panel) to trigger a push.

<figure>
  <img src="/wp-content/uploads/push-branch-2025-HD.gif" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop showing drag-and-drop to push main branch to origin">
  <figcaption style="text-align:center; color:#888">Drag to push a branch to a remote</figcaption>
</figure>

***

## Fetch

Fetching retrieves updates from remotes but doesn’t change your working directory.

<figure>
  <img src="/wp-content/uploads/fetch-menu-2025.png" 
       srcset="/wp-content/uploads/fetch-menu-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop pull dropdown menu showing fetch and pull options, with the fetch option highlighted.">
  <figcaption style="text-align:center; color:#888">Fetch from the pull dropdown menu</figcaption>
</figure>

### Fetch All
Shows how far ahead/behind your branches are compared to the remote.

<figure>
  <img src="/wp-content/uploads/branch-behind-2025.png" 
       srcset="/wp-content/uploads/branch-behind-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop Left Panel showing branch main is 1 commit behind">
  <figcaption style="text-align:center; color:#888">Ahead/behind indicators in the Left Panel</figcaption>
</figure>

Fetching runs automatically every minute. Adjust the interval in <kbd>Preferences > General</kbd>.

***

## Pull Options <img src='/wp-content/uploads/gk-pull-icon.svg' style='height:1em;'>

Pulling performs a fetch and then updates your local branch.

### Pull (fast-forward if possible)
Fast-forwards your branch if there are no conflicting commits; otherwise, merges.

<figure>
  <img src='/wp-content/uploads/pull-ff-ex-2025.png' 
       srcset="/wp-content/uploads/pull-ff-ex-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop commit graph showing fallback to merge when fast-forward pull is not possible">
  <figcaption style="text-align:center; color:#888">Example: Merge fallback when fast-forward not possible</figcaption>
</figure>

### Pull (fast-forward only)
Attempts to fast-forward. If not possible, no action is taken.

### Pull (rebase)
Temporarily stashes your commits, pulls from remote, and replays your changes on top.

<figure>
  <img src='/wp-content/uploads/pull-rebase-2025.png' 
       srcset="/wp-content/uploads/pull-rebase-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop commit graph demonstrating linear history using pull-rebase">
  <figcaption style="text-align:center; color:#888">Rebase keeps commit history linear</figcaption>
</figure>

### Set Pull Behavior
Select a default pull method via the dropdown menu.

<figure>
  <img src="/wp-content/uploads/set-default.png" 
       srcset="/wp-content/uploads/set-default@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop pull menu with option to set default pull behavior">
  <figcaption style="text-align:center; color:#888">Choose a default pull behavior</figcaption>
</figure>

***

## Set Upstream Branch

The upstream defines the remote branch a local branch tracks.

- Right-click a branch to set its upstream
- Or click the <kbd><i class="fa fa-ellipsis-v"></i></kbd> button

<figure>
  <img src="/wp-content/uploads/upstream.png" 
       srcset="/wp-content/uploads/upstream@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop context menu with 'Set Upstream' option selected">
  <figcaption style="text-align:center; color:#888">Set the upstream branch</figcaption>
</figure>

You can also drag and drop to push instead of explicitly setting the upstream:

<figure>
  <img src="/wp-content/uploads/drag-and-drop-push-2025.gif" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop interface showing a user pushing a branch to origin/main using drag-and-drop">
  <figcaption style="text-align:center; color:#888">Push without setting upstream via drag-and-drop</figcaption>
</figure>
