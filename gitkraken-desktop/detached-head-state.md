---
title: Detached HEAD in GitKraken Desktop
description: Learn how to safely enter, work in, and exit detached HEAD state in GitKraken Desktop. Includes recovery tips and commit preservation.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: January 2026</kbd>

Detached HEAD state lets you check out any commit in GitKraken Desktop without creating a branch. This is useful for reviewing or experimenting with past changes without affecting your active branches.

***

## Enter Detached HEAD State

1. Right-click the commit you want to inspect.
2. Select <kbd><strong>Checkout this commit</strong></kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/checkout-commit-2025.png' class="help-center-img img-bordered" alt="Context menu showing 'Checkout this commit' option in GitKraken Desktop after right-clicking a specific commit in the graph view">
  <figcaption style="text-align: center; color: #888;">Check out any past commit without creating a new branch.</figcaption>
</figure>

The checked-out commit will display a `HEAD` label, indicating you’re in detached HEAD state.

<figure class='figure center'>
  <img src='/wp-content/uploads/HEAD-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing HEAD label attached to a specific commit in the graph, indicating the currently checked-out commit">
  <figcaption style="text-align: center; color: #888;">GitKraken tags the commit with HEAD.</figcaption>
</figure>

You can now review the full history and diffs, or create a branch from this state.

***

## Commit in Detached HEAD State

You can make changes and commit them while in this state. However, these commits won’t belong to any branch.

<figure class='figure center'>
  <img src='/wp-content/uploads/editing-detachedly-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing a warning banner that says 'You are in a detached HEAD state' above the commit panel with unstaged changes listed">
  <figcaption style="text-align: center; color: #888;">GitKraken shows a warning when you commit in detached HEAD state.</figcaption>
</figure>

To preserve your work, create a branch from the current commit:

1. Right-click the commit tagged as HEAD.
2. Select <kbd><strong>Create branch here</strong></kbd>.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-branch-from-HEAD-2025.png' class="help-center-img img-bordered" alt="Context menu in GitKraken Desktop showing the option 'Create branch here' when right-clicking a commit labeled HEAD">
  <figcaption style="text-align: center; color: #888;">Start a branch from your current detached commit to keep your changes.</figcaption>
</figure>

***

## Exit Detached HEAD State

To exit detached HEAD state:

- Check out any local branch.

This will remove the `HEAD` label and discard any unpreserved commits.

<figure class='figure center'>
  <img src='/wp-content/uploads/discard-commits.gif' class="help-center-img img-bordered" alt="Animation showing how unbranched commits in GitKraken Desktop are removed from view after switching branches from a detached HEAD state">
  <figcaption style="text-align: center; color: #888;">Unbranched commits are removed when you check out another branch.</figcaption>
</figure>

<div class='callout callout--danger'>
  <p><strong>Important:</strong> Commits made in detached HEAD state will be lost unless you create a branch. You may be able to <a href='https://help.gitkraken.com/gitkraken-desktop/detached-head-state/#recovering-lost-commits'>recover them manually</a>.</p>
</div>

***

## Recover Lost Commits

If you accidentally switch branches before saving your changes:

- Click <a href="https://support.gitkraken.com/working-with-commits/undo-and-redo/">Undo</a> in GitKraken if available.
- Use the CLI and run [`git reflog`](https://git-scm.com/docs/git-reflog) to find the lost commit SHA.
- Then use [`git checkout <SHA>`](https://git-scm.com/docs/git-checkout) to re-enter that state.
