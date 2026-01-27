---
title: Manage Git Submodules in GitKraken Desktop
description: Learn how to add, update, and manage Git submodules in GitKraken Desktop, including how to track commits and enable automatic updates.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

Submodules allow you to include another Git repository inside a parent repository. Use submodules to incorporate independent projects while maintaining separate commit histories.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/moC2KyxGb10?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## Enable the Submodules Pane

To toggle the Submodules pane:
1. Right-click any pane header in the Left Panel.
2. Check or uncheck “Submodules” to show or hide the pane.

<figure>
  <img src="/wp-content/uploads/toggle-panes-2025.png" 
       srcset="/wp-content/uploads/toggle-panes-2025@2x.png" 
       alt="GitKraken Desktop Left Panel showing the toggle pane menu with options to show or hide sections like Remote, Pull Requests, Tags, and Submodules" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Toggle the Submodules pane from the Left Panel</figcaption>
</figure>

***

## Add a Submodule

To add a submodule:
1. Hover over <em>Submodules</em> in the Left Panel.
2. Click the <button class='button button--success button--ui button--nolink'>+</button> icon.
3. Paste the HTTPS or SSH repository URL.
4. Enter the desired path.

<figure>
  <img src="/wp-content/uploads//add-submodule.png" 
       srcset="/wp-content/uploads//add-submodule@2x.png" 
       alt="GitKraken Desktop interface showing the Add Submodule modal with fields for Remote URL and Name/Path, and a green Add Submodule button" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Add a submodule using HTTPS or SSH URL</figcaption>
</figure>

Adding a submodule updates the `.gitmodules` file and references the submodule commit.

When cloning the parent repository, you’ll be prompted to initialize the submodule to fetch and checkout its commit.

***

## Update a Submodule

To update a submodule:
1. Open the Submodules pane.
2. Right-click the submodule.
3. Select <kbd>Update</kbd> to fetch the latest commit.

<figure>
  <img src="/wp-content/uploads//update-submodule.png" 
       srcset="/wp-content/uploads//update-submodule@2x.png" 
       alt="Context menu in GitKraken Desktop showing options to update, edit, open, or delete the submodule vendor/libgit2" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Update a submodule from the Left Panel</figcaption>
</figure>

When cloning a repository that includes submodules, GitKraken prompts you to initialize them.

***

## Change the Pointer Commit

To update the tracked commit:
1. Open the submodule in GitKraken Desktop.
2. Check out a new commit or branch.
3. Exit the submodule to return to the parent repo.

GitKraken Desktop will prompt you to save the updated pointer commit.

<figure>
  <img src="/wp-content/uploads//submodule-commit.png" 
       srcset="/wp-content/uploads//submodule-commit@2x.png" 
       alt="GitKraken Desktop interface showing submodule vendor/libgit2 out-of-sync, with options to commit or discard changes, and view or delete the submodule" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Update the pointer commit for a submodule</figcaption>
</figure>

***

## Submodule Statuses

Possible submodule states and how to resolve them:

- **Out of sync**: The pointer commit changed. Stash, commit, or discard changes.
- **Added but not initialized**: Right-click and select <kbd>Initialize</kbd>.
- **Added and initialized but not committed**: Commit the submodule folder and update `.gitmodules`.

***

## Keep Submodules Up to Date

Enable automatic submodule updates:
- Globally: <kbd>Preferences > General</kbd>
- Per repository: <kbd>Preferences > Submodules</kbd>

***

## Subtree Support

GitKraken Desktop does **not** support subtree workflows in-app.
