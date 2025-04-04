---

title: Worktrees
description: How to use Git Worktrees in GitKraken Desktop
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

Learn more about Git Worktrees in GitKraken Desktop and how to use them.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/grAsFn5yvjA?si=5U8cIbu_m_41yGxR?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## Worktrees

A Git worktree is a linked working copy of your Git repository that allows you to work on multiple branches simultaneously. Unlike branches which share the same working directory, each worktree has its own working directory with its own set of files. This means you can have different branches checked out in different locations on your filesystem at the same time.

Worktrees are particularly useful when you need to:

+ Work on multiple features or bug fixes in parallel without switching branches
+ Build and test different versions of your code simultaneously  
+ Keep a clean main branch while working on experimental changes
+ Review pull requests while continuing development on another branch

Each worktree maintains its own index and working tree state, but shares the same Git history and objects with the main repository. Changes made in one worktree can be seen from other worktrees once committed.

***

## Worktrees in GitKraken Desktop

Since version 10.5.0, GitKraken Desktop supports worktrees, allowing you to create, switch, delete, and lock or unlock them directly from the left panel. By hovering over a worktree, you can view its full path in your filesystem

## Creating a Worktree

To create a worktree, right click on a branch in the Repository View and select `Create worktree`.

<img src="/wp-content/uploads/gkd-10-5-create-worktree.png" class="help-center-img img-bordered">

***

## Switching Worktrees

To switch to a different worktree, right click on the worktree in the left panel and select `Open this worktree`.

<img src="/wp-content/uploads/gkd-10-5-worktrees-actions.png" class="help-center-img img-bordered">

Or check out the branch you want to switch to in the Repository View to switch to that worktree.

***

## Deleting a Worktree

To delete a worktree, right click on the worktree in the left panel and select `Remove this Worktree`.


## Locking/Unlocking a Worktree

To lock or unlock a worktree, right click on the worktree in the left panel and select `Lock this worktree` or `Unlock this worktree`.


