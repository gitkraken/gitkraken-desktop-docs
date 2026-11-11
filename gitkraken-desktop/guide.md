---
title: Learn Git with GitKraken Desktop | Beginner Guide & Workflow
description: New to Git? Get started with GitKraken Desktop using this beginner-friendly guide. Learn cloning, branching, staging, committing, and merging with tutorials and videos.
product: GitKraken Desktop
feature: Beginner Guide
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
tags: [git, beginner, guide, workflow]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "gitkraken-desktop-start-here"
    nav_label: "Beginner Guide & Workflow"
    nav_order: 70
    nav_parent: "gitkraken-desktop-start-here"
    page_type: "content"
    card_icon: "school"
    card_color: "purple"
    card_description: "Clone, branch, stage, commit and merge, step by step"
---
<kbd>Last updated: November 2026</kbd>

<div style="display:flex; flex-wrap:wrap; align-items:center; gap:8px 32px; margin-bottom:24px;">
  <p style="flex:1 1 300px; margin:0;">Learn a basic GitKraken Desktop workflow: clone a repository, create a branch, make and stage changes, commit them, push the branch, and merge the work back. These steps are for new Git users who want a practical first path through GitKraken Desktop.</p>
  <img src="/wp-content/uploads/GitKraken_Keif_student.png" alt="" width="800" height="900" loading="lazy" style="flex:0 0 auto; max-height:200px; width:auto; height:auto; max-width:100%; margin:0 auto; transform:scaleX(-1);">
</div>

**Requirements and limits**
- The steps cover a basic workflow, not every GitKraken Desktop option or edge case.
- You need access to a Git repository you can clone, change, commit to, and push from GitKraken Desktop.
- Whether you can push and merge depends on your remote permissions and repository policy.
- Resolving merge conflicts is outside these steps. See [Branching and Merging](/working-with-repositories/branching-and-merging).

***

## Quick Start


1. **Clone a repository**: Go to <kbd>File > Clone Repo</kbd>, paste a repository URL or browse your connected Git hosting service, and click **Clone the repo!**.
2. **Create a branch**: Right-click any commit in the graph and select **Create branch here**. Name it and press <kbd>Enter</kbd>.
3. **Make changes**: Edit files in your working directory. Saved changes appear under the WIP node in the Commit Graph.
4. **Stage changes**: Click the WIP node to open the Commit Panel. Click files to stage them, or press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd> to stage all.
5. **Commit**: Enter a commit message and press <kbd>Cmd</kbd> + <kbd>Enter</kbd> (macOS) or <kbd>Ctrl</kbd> + <kbd>Enter</kbd> (Windows/Linux).
6. **Push**: Click **Push** in the toolbar to upload your branch to the remote.
7. **Merge**: When your work is ready, check out the target branch, right-click your feature branch, and select **Merge *[feature branch]* into *[target branch]***.

If the merge has conflicts, GitKraken Desktop opens the Merge Tool, where you can select lines from each side and commit the resolution.

***

## How to learn Git with GitKraken

This video series teaches Git concepts and how to apply them in GitKraken Desktop.

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Git tutorial series for beginners.</figcaption>
</figure>

To see how version control fits into a DevOps workflow, read the GitKraken [DevOps Tools Report](https://www.gitkraken.com/resources/devops-report-2020).

***

## GitKraken tutorials

Watch these video tutorials to learn the GitKraken Desktop interface.

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV78WqGmGSq8JPnafR3lAa55n" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Video tutorials for using GitKraken Desktop.</figcaption>
</figure>

***

## How local repositories work

Most Git actions in GitKraken Desktop run in your local repository, on your machine. In the Commit Graph, the <i class="fa fa-laptop"></i> icon marks local branches.

Git is fast because it makes changes locally, not over a network. If a remote server fails, each copy of the repository on your team still has the full project history.

### What the `.git` folder does

The `.git` folder holds your repository's metadata and commit history. If you delete it, Git operations such as switching branches or pulling from remotes do not work.

### What the working directory does

The working directory holds the files you are working on. When you switch branches or pull updates, Git changes the files in your working directory to match the checked-out branch.

Learn more about [Git repositories](https://www.gitkraken.com/learn/git/tutorials/what-is-a-git-repository).

***

## How the example workflow works

Follow this workflow to make your first commit in GitKraken Desktop.

### How to create a branch

Right-click `main` in the Commit Graph and choose <kbd>Create branch here</kbd>. Name it `develop`, a branch for ongoing development.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-new-branch-2025.png' class='help-center-img img-bordered' alt='Right-clicking the main branch in GitKraken Desktop to create a new branch at that commit.'>
  <figcaption style="text-align:center; color:#888">Right-click main to create a new branch.</figcaption>
</figure>

### How to modify a file

Edit `README.md` to reflect your project. You can open this file directly from the Commit Graph.

<figure class='figure center'>
  <img src='/wp-content/uploads/open-file-2025.png' class='help-center-img img-bordered' alt='Clicking a file name in the GitKraken Desktop Commit Panel to open it for editing.'>
  <figcaption style="text-align:center; color:#888">Click a filename to access the Edit button.</figcaption>
</figure>

### How to stage and commit changes

After editing, select the <kbd>//WIP</kbd> node to view unstaged changes. To stage all of them, click the green <button class='button button--success button--ui button--nolink'>Stage All Changes</button> button.

<figure class='figure center'>
  <img src='/wp-content/uploads/unstage-2025.png' class='help-center-img img-bordered' alt='Unstaged file changes for the WIP node in GitKraken Desktop.'>
  <figcaption style="text-align:center; color:#888">Click the WIP node to view and stage changes.</figcaption>
</figure>

Then enter a commit message and click <button class='button button--success button--ui button--nolink'>Commit Changes to 1 File</button>.

Learn more about [staging](/working-with-commits/staging) and [committing](/working-with-commits/commits).

### How to merge back to main

When `develop` is ahead of `main`, you can merge:

<figure class='figure center'>
  <img src='/wp-content/uploads/graph-commit-2025.png' class='help-center-img img-bordered' alt='Commit Graph in GitKraken Desktop showing the develop branch 1 commit ahead of main.'>
  <figcaption style="text-align:center; color:#888">Develop is ahead by 1 commit.</figcaption>
</figure>

To merge, drag `develop` onto `main` in the Commit Graph and select <kbd>Merge develop into main</kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/drag-and-drop-2025.png' class='help-center-img img-bordered' alt='Dragging the develop branch onto main in GitKraken Desktop to show the merge options.'>
  <figcaption style="text-align:center; color:#888">Drag develop onto main to merge branches.</figcaption>
</figure>

Learn more in [Branching and Merging](/working-with-repositories/branching-and-merging).

***

## Getting started summary

This basic workflow sets the foundation for more advanced topics like [pushing and pulling](/working-with-repositories/pushing-and-pulling) and [GitFlow](/git-workflows-and-extensions/git-flow).

When you are ready to go further, continue with:

- [GitKraken Desktop Interface Guide](/gitkraken-desktop/interface/) to learn how the Left Panel, Commit Graph, and Commit Panel fit together
- [Manage Git Worktrees in GitKraken Desktop](/gitkraken-desktop/worktrees/) to work on multiple branches in parallel
- [GitKraken Terminal Guide](/gitkraken-desktop/terminal/) to use the embedded terminal
- [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/) to use the Agents view and coding agent workflows

Watch how to make a commit in GitKraken Desktop:

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8a6fYPkBDbY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Walkthrough of creating a commit in GitKraken Desktop.</figcaption>
</figure>
