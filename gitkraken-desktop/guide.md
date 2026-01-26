---
title: Learn Git with GitKraken Desktop | Beginner Guide & Workflow
description: New to Git? Get started with GitKraken Desktop using this beginner-friendly guide. Learn cloning, branching, staging, committing, and merging with tutorials and videos.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

This Getting Started Guide introduces GitKraken Desktop with a basic workflow—cloning a repository, making changes, and merging them.

***

## Learn Git with GitKraken

In this series, you'll learn Git concepts and how to apply them using GitKraken Desktop.

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch our Git tutorial series for beginners.</figcaption>
</figure>

Explore how version control fits into a DevOps workflow by reading our [DevOps Tools Report](https://www.gitkraken.com/resources/devops-report-2020).

***

## GitKraken Tutorials

Need help getting started with the product interface? Watch these video tutorials.

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV78WqGmGSq8JPnafR3lAa55n" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Video tutorials for using GitKraken Desktop.</figcaption>
</figure>

***

## Understanding Local Repositories

Most Git actions in GitKraken Desktop occur in the local repository, meaning changes are made on your machine.

Local branches are indicated in the graph with the <i class="fa fa-laptop"></i> icon.

Git is fast because all changes occur locally, not over a network. Even if a remote server fails, your team retains full copies of the project.

### .git Folder

This folder contains all the metadata and commit history. If deleted, Git operations like switching branches or pulling remotes won’t work.

### Working Directory

This is your active file state. When switching branches or pulling updates, Git modifies your working directory to match the current branch.

Learn more about [Git repositories](https://www.gitkraken.com/learn/git/tutorials/what-is-a-git-repository).

***

## Example Workflow

Follow this workflow to make your first commit in GitKraken Desktop.

### Create a Branch

Right-click `main` in the Commit Graph and choose <kbd>Create branch here</kbd>. Name it `develop`—a branch for ongoing development.

<figure>
  <img src='/wp-content/uploads/create-new-branch-2025.png' class='img-bordered img-responsive center' alt='Create new branch from main'>
  <figcaption style="text-align:center; color:#888">Right-click main to create a new branch.</figcaption>
</figure>

### Modify a File

Edit `README.md` to reflect your project. You can open this file directly from the Commit Graph.

<figure>
  <img src='/wp-content/uploads/open-file-2025.png' class='img-bordered img-responsive center' alt='Open file from commit panel'>
  <figcaption style="text-align:center; color:#888">Click a filename to access the Edit button.</figcaption>
</figure>

### Stage and Commit

After editing, select the <kbd>//WIP</kbd> node to view unstaged changes. Stage all with the green <button class='button button--success button--ui button--nolink'>Stage all changes</button> button.

<figure>
  <img src='/wp-content/uploads/unstage-2025.png' class='img-bordered img-responsive center' alt='Pending file changes in staging area'>
  <figcaption style="text-align:center; color:#888">Click the WIP node to view and stage changes.</figcaption>
</figure>

Then enter a commit message and click <button class='button button--success button--ui button--nolink'>Commit</button>.

Learn more about [staging](/working-with-commits/staging) and [committing](/working-with-commits/commits).

### Merge to Main

When `develop` is ahead of `main`, you can merge:

<figure>
  <img src='/wp-content/uploads/graph-commit-2025.png' class='img-bordered img-responsive center' alt='Commit graph showing develop ahead of main'>
  <figcaption style="text-align:center; color:#888">Develop is ahead by 1 commit.</figcaption>
</figure>

To merge, drag `develop` onto `main` in the graph and choose <kbd>Merge</kbd>.

<figure>
  <img src='/wp-content/uploads/drag-and-drop-2025.png' class='img-bordered img-responsive center' alt='Drag develop branch onto main to merge'>
  <figcaption style="text-align:center; color:#888">Drag develop onto main to merge branches.</figcaption>
</figure>

Learn more in [Branching and Merging](/working-with-repositories/branching-and-merging).

***

## Summary

This basic workflow sets the foundation for more advanced topics like [pushing and pulling](/working-with-repositories/pushing-and-pulling) and [GitFlow](/git-workflows-and-extensions/git-flow).

Watch how a commit is made using GitKraken Desktop:

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8a6fYPkBDbY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Walkthrough of creating a commit in GitKraken Desktop.</figcaption>
</figure>
