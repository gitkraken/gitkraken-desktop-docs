---
title: Manage Git Tags in GitKraken Desktop
description: Learn how to create, annotate, move, and share Git tags in GitKraken Desktop to mark releases and key commits.
product: GitKraken Desktop
feature: Tags
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
tags: [tags, releases, annotate, git, versions]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to create, annotate, push, move, delete, and filter Git tags in GitKraken Desktop. Tags are useful when you want to mark releases, deployment points, or other important commits and then share or inspect those references from the commit graph or Left Panel.

**Requirements and limits**
- Scope: Local and remote Git tag management in GitKraken Desktop
- Creation points: Commit Graph or Left Panel tag actions
- Checkout limitation: Tags cannot be checked out directly as branches
- Rename limitation: Tags cannot be renamed directly; delete and recreate them instead
- Move limitation: Moving a tag works only when fast-forwarding is possible; otherwise delete and recreate it
- Deletion warning: Deleting a tag locally or remotely is permanent
- Visibility control: The Tags pane can be filtered, shown, or hidden from the Left Panel

***

## Quick Start


**To create a tag:** Right-click a commit in the graph and select **Create tag here**. Enter the tag name and press Enter.

**To create an annotated tag:** Right-click a commit and select **Create annotated tag here**. Annotation messages appear as tooltips in the graph and Left Panel.

**To push a tag to a remote:** Right-click the tag in the Left Panel or graph and select **Push tag**.

**To create a branch from a tag:** Right-click the tag and select **Create branch here**.

**To delete a tag:** Right-click the tag and choose to delete it locally, from the remote, or both. Deletion is permanent.

**To rename a tag:** Tags cannot be renamed directly. Delete the existing tag locally and from the remote, then recreate it with the desired name on the same commit.

**To filter tags:** Use the filter bar at the top of the Tags section in the Left Panel. Toggle the Tags pane by right-clicking any Left Panel header.

***

## How to add a tag

To create a new tag:
1. Right-click a commit.
2. Select <kbd>Create tag here</kbd>.

<figure>
  <img src="/wp-content/uploads/create-tag-2025@2x.png" 
       alt="GitKraken Desktop context menu on a commit with options to create tag or annotated tag" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Create a tag from a commit's context menu</figcaption>
</figure>

To share a tag with collaborators, right-click it and choose <kbd>Push tag</kbd>.

<figure>
  <img src="/wp-content/uploads/push-tag-2025@2x.png" 
       alt="GitKraken Desktop tag context menu showing push, merge, rebase, and delete options" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Push a local tag to a remote</figcaption>
</figure>

Double-click a tag in the Left Panel to jump to that commit in the graph. You can also hide or solo tags via the context menu.

<figure>
  <img src="/wp-content/uploads/tag-right@2x.png" 
       alt="GitKraken Desktop context menu for a tag with options to push, merge, rebase, create branch, and delete" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Access tag options from the Left Panel</figcaption>
</figure>

***

## How to create a branch from a tag

While you can't check out a tag directly, you can branch from it:
1. Right-click the tag.
2. Select <kbd>Create branch here</kbd>.

<figure>
  <img src="/wp-content/uploads/tag-branch@2x.png" 
       alt="GitKraken Desktop tag context menu showing options to push, merge, rebase, create branch, and more. The `create a branch` option is selected." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Create a branch from a tag</figcaption>
</figure>

Alternatively, use the [detached HEAD state](/working-with-commits/detached-head-state/) to inspect a tagged commit.

***

## How to move a tag

To move a tag to a new commit:
1. Check out the new branch.
2. Right-click the tag.
3. Choose <kbd>Fast-forward</kbd>.

If fast-forwarding is not possible, delete the tag locally and remotely, then recreate it on the new commit.

***

## How to annotate a tag

To add a message to a tag:
- Right-click a commit and choose <kbd>Create annotated tag here</kbd>.
- Or right-click an existing tag and select <kbd>Annotate tag</kbd>.

Annotated messages appear in the graph and Left Panel on hover.

<figure>
  <img src="/wp-content/uploads/tag-annotation.png"
       alt="GitKraken Desktop interface showing a hover tooltip for the annotated Git tag v1.9.0 in the Commit Graph"
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Hover to preview an annotated tag</figcaption>
</figure>

***

## How to delete a tag

To delete a tag locally:

1. Right-click the tag in the Left Panel or Commit Graph.
2. Select <kbd>Delete [tag name] locally</kbd>.
3. Confirm by clicking <kbd>Delete</kbd>.

To delete a tag from the remote:

1. Right-click the tag in the Left Panel or Commit Graph.
2. Select <kbd>Delete [tag name] from [remote]</kbd>.
3. Confirm by clicking <kbd>Delete</kbd>

> Deleting a tag is permanent and cannot be undone.

<figure>
  <img src="/wp-content/uploads/delete-tag-context-menu-2025@2x.png" 
       alt="GitKraken Desktop context menu showing options to delete a Git tag locally or from the origin remote" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Right-click a tag to delete it locally or from a remote.</figcaption>
</figure>

***

## How to rename a tag

GitKraken Desktop does not support renaming tags directly. To rename a tag, delete the existing one and create a new tag with the desired name.

1. Right-click the tag in the Left Panel or Commit Graph.
2. Select <kbd>Delete [tag name] locally</kbd>.
3. If the tag also exists on a remote, right-click it again and select <kbd>Delete [tag name] from [remote]</kbd>.
4. Right-click the commit where you want to place the tag.
5. Select <kbd>Create tag here</kbd> and enter the new name.

> This workaround reflects Git’s limitations—Git tags are immutable once created.

***

## How to search or filter tags

Use the filter bar in the Left Panel to search for tags.

<figure>
  <img src="/wp-content/uploads/filter-tags@2x.png" 
       alt="GitKraken Desktop interface showing filtered Git tags matching '20160' under the 'translation' category in the left panel" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Search for tags from the Left Panel</figcaption>
</figure>

***

## How to show or hide the Tags panel

To toggle visibility of the Tags section:
- Right-click any header in the Left Panel.
- Check or uncheck <kbd>Tags</kbd>.

<figure>
  <img src="/wp-content/uploads/toggle-panes-2025@2x.png" 
       alt="GitKraken Desktop interface with a dropdown menu showing toggles for Left Panel sections such as Remote, Pull Requests, Tags, and GitHub Actions" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Show or hide the Tags pane in the Left Panel</figcaption>
</figure>
