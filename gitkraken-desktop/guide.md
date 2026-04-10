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
last_verified: 2026-03
llms_include: true
tags: [git, beginner, guide, workflow]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this getting started guide to learn a basic GitKraken Desktop workflow: clone a repository, create a branch, make and stage changes, commit them, push the branch, and merge the work back. It is aimed at new Git users who need a practical first path through the product rather than a reference page.

**Requirements and limits**
- This page is a beginner workflow guide, not a full reference for every GitKraken Desktop option or edge case.
- You need access to a Git repository you can clone, change, commit to, and push from GitKraken Desktop.
- Merging and pushing steps depend on your remote permissions and repository policy.
- If merge conflicts occur, you may need separate merge-conflict guidance beyond this introductory walkthrough.

***

## Quick Start


1. **Clone a repository**: Go to <kbd>File > Clone Repo</kbd>, paste a repository URL or browse your connected Git hosting service, and click **Clone the repo**.
2. **Create a branch**: Right-click any commit in the graph and select **Create branch here**. Name it and press <kbd>Enter</kbd>.
3. **Make changes**: Edit files in your working directory. Saved changes appear under the WIP node in the Commit Graph.
4. **Stage changes**: Click the WIP node to open the Commit Panel. Click files to stage them, or press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>Shift</kbd> + <kbd>S</kbd> to stage all.
5. **Commit**: Enter a commit message and press <kbd>Cmd</kbd>/<kbd>Enter</kbd> (macOS) or <kbd>Ctrl</kbd>/<kbd>Enter</kbd> (Windows/Linux).
6. **Push**: Click **Push** in the toolbar to upload your branch to the remote.
7. **Merge**: When your work is ready, check out the target branch and right-click your feature branch to select **Merge**.

If merge conflicts occur, GitKraken Desktop opens the Merge Tool, where you can select lines from each side and commit the resolution.

***

## How to learn Git with GitKraken

GitKraken offers two ways to learn Git: a free structured certification course for guided study and a YouTube playlist for casual learning and quick refreshers.

### Foundations of Git course

If you want a structured path for learning Git, take the free [Foundations of Git certification course](https://learn.gitkraken.com/courses/git-foundations). The course is self-paced and designed for people who want practical Git training without relying on dense reference material or scattered tutorials.

<figure class='figure center'>
  <img src='/wp-content/uploads/foundations-of-git-certification-course.png' class='help-center-img img-bordered' alt='Course card for the Foundations of Git certification course showing the Git logo, the course title, and a five-star rating.'>
  <figcaption style="text-align:center; color:#888">Foundations of Git certification course.</figcaption>
</figure>

The course helps you:

- Learn at your own pace with a curated curriculum that supports everyday version control work.
- Understand Git concepts through motion graphics and visual examples.
- Validate what you learned with the Foundations of Git Certification Exam at the end of the course.

### Learn Git with GitKraken

If you want a lighter way to build Git knowledge, watch the GitKraken YouTube playlist. Some topics overlap with the certification course, but the playlist is a good option for casual learning and quick refreshers on key Git concepts.

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV7-_41SpakZoTIYCgX4aMTdU" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch our Git tutorial series for beginners.</figcaption>
</figure>

Explore how version control fits into a DevOps workflow by reading our [DevOps Tools Report](https://www.gitkraken.com/resources/devops-report-2020).

***

## GitKraken tutorials

Need help getting started with the product interface? Watch these video tutorials.

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/playlist?list=PLe6EXFvnTV78WqGmGSq8JPnafR3lAa55n" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Video tutorials for using GitKraken Desktop.</figcaption>
</figure>

***

## How local repositories work

Most Git actions in GitKraken Desktop occur in the local repository, meaning changes are made on your machine.

Local branches are indicated in the graph with the <i class="fa fa-laptop"></i> icon.

Git is fast because all changes occur locally, not over a network. Even if a remote server fails, your team retains full copies of the project.

### What the `.git` folder does

This folder contains all the metadata and commit history. If deleted, Git operations like switching branches or pulling remotes won’t work.

### What the working directory does

This is your active file state. When switching branches or pulling updates, Git modifies your working directory to match the current branch.

Learn more about [Git repositories](https://www.gitkraken.com/learn/git/tutorials/what-is-a-git-repository).

***

## How the example workflow works

Follow this workflow to make your first commit in GitKraken Desktop.

### How to create a branch

Right-click `main` in the Commit Graph and choose <kbd>Create branch here</kbd>. Name it `develop`—a branch for ongoing development.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-new-branch-2025.png' class='help-center-img img-bordered' alt='Right-clicking the main branch in GitKraken Desktop to create a new branch at a specific commit, reinforcing how Git branching can point to any commit.'>
  <figcaption style="text-align:center; color:#888">Right-click main to create a new branch.</figcaption>
</figure>

### How to modify a file

Edit `README.md` to reflect your project. You can open this file directly from the Commit Graph.

<figure class='figure center'>
  <img src='/wp-content/uploads/open-file-2025.png' class='help-center-img img-bordered' alt='Clicking a file name in the GitKraken Desktop commit panel to open it for editing, illustrating how Git users can inspect or modify historical files directly from any commit.'>
  <figcaption style="text-align:center; color:#888">Click a filename to access the Edit button.</figcaption>
</figure>

### How to stage and commit changes

After editing, select the <kbd>//WIP</kbd> node to view unstaged changes. Stage all with the green <button class='button button--success button--ui button--nolink'>Stage all changes</button> button.

<figure class='figure center'>
  <img src='/wp-content/uploads/unstage-2025.png' class='help-center-img img-bordered' alt='Viewing unstaged file changes from the WIP node in GitKraken Desktop, illustrating how users can access and stage modified files directly from the commit graph for efficient commit preparation.'>
  <figcaption style="text-align:center; color:#888">Click the WIP node to view and stage changes.</figcaption>
</figure>

Then enter a commit message and click <button class='button button--success button--ui button--nolink'>Commit</button>.

Learn more about [staging](/working-with-commits/staging) and [committing](/working-with-commits/commits).

### How to merge back to main

When `develop` is ahead of `main`, you can merge:

<figure class='figure center'>
  <img src='/wp-content/uploads/graph-commit-2025.png' class='help-center-img img-bordered' alt='Commit graph showing the develop branch with one additional commit compared to main, visualizing how GitKraken Desktop helps users understand branch divergence and progress at a glance.'>
  <figcaption style="text-align:center; color:#888">Develop is ahead by 1 commit.</figcaption>
</figure>

To merge, drag `develop` onto `main` in the graph and choose <kbd>Merge</kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/drag-and-drop-2025.png' class='help-center-img img-bordered' alt='Dragging the develop branch onto main in GitKraken Desktop to trigger merge options, illustrating how visual interactions simplify common Git operations like branch merges.'>
  <figcaption style="text-align:center; color:#888">Drag develop onto main to merge branches.</figcaption>
</figure>

Learn more in [Branching and Merging](/working-with-repositories/branching-and-merging).

***

## Getting started summary

This basic workflow sets the foundation for more advanced topics like [pushing and pulling](/working-with-repositories/pushing-and-pulling) and [GitFlow](/git-workflows-and-extensions/git-flow).

Watch how a commit is made using GitKraken Desktop:

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8a6fYPkBDbY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Walkthrough of creating a commit in GitKraken Desktop.</figcaption>
</figure>
