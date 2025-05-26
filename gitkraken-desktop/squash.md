---
title: Squash Commits in GitKraken Desktop
description: Learn how to squash commits to simplify your Git history.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: May 2025</kbd>

Squashing lets you combine multiple commits into one to clean up your Git history. This is helpful before pushing to a shared branch or finalizing a feature branch.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/cr1N8VTRmfM?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

## Squash Requirements

You can squash commits if they meet all the following conditions:

- More than one commit is selected
- Commits are in a straight line (ancestor-descendant)
- Commits are in chronological order
- The oldest selected commit has a parent

To select multiple commits, hold <kbd>Shift</kbd> or <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> and click the commits.

<figure class='figure center'>
    <img src='/wp-content/uploads/squash.gif' srcset='/wp-content/uploads/squash@2x.gif' class="help-center-img img-bordered" alt="Selecting and squashing multiple commits">
    <figcaption style="text-align: center; color: #888;">Select a commit range and right-click to squash.</figcaption>
</figure>

After squashing, the new commit appears in the Commit Panel. You can click the commit message to amend and consolidate the messages from the squashed commits.

<figure class='figure center'>
    <img src='/wp-content/uploads/amend-commitmsg.png' srcset='/wp-content/uploads/amend-commitmsg@2x.png' class="help-center-img img-bordered" alt="Amending a squashed commit message">
    <figcaption style="text-align: center; color: #888;">Click the commit message to edit after squashing.</figcaption>
</figure>

***

## Push a Squashed Commit

Avoid pushing commits to your remote that you intend to squash. If you've already pushed them, and then squash locally, your local and remote branches will differ.

<figure class='figure center'>
    <img src='/wp-content/uploads/squashed-remote.png' srcset='/wp-content/uploads/squashed-remote@2x.png' class="help-center-img img-bordered" alt="Local branch has squashed commit while remote shows all commits">
    <figcaption style="text-align: center; color: #888;">After squashing, your local branch no longer matches the remote.</figcaption>
</figure>

When you push, GitKraken shows a warning that your local branch is behind the remote. This is expected, because the squashed commit rewrites history.

<figure class='figure center'>
    <img src='/wp-content/uploads/squash-pushremote.png' srcset='/wp-content/uploads/squash-pushremote@2x.png' class="help-center-img img-bordered" alt="Warning about diverging history when pushing squashed commits">
    <figcaption style="text-align: center; color: #888;">A warning appears because your branch history changed.</figcaption>
</figure>

To resolve this:

- Click <button class='button button--danger button--ui button--nolink'>Force Push</button> to overwrite the remote branch with your squashed history

<figure class='figure center'>
    <img src='/wp-content/uploads/force-push.png' srcset='/wp-content/uploads/force-push@2x.png' class="help-center-img img-bordered" alt="Force Push button and warning in GitKraken">
    <figcaption style="text-align: center; color: #888;">Use Force Push to push squashed commits and rewrite remote history.</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Warning:</strong> Force pushing is a destructive action. It replaces remote history and can disrupt teammates working on the same branch. Use with caution.</p>
</div>
