---

title: Submodules
description: Submodules allow you to include other Git repositories within another Git repository. Work with submodules in GitKraken Desktop.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

Submodules allow you to include other Git repositories within a Git repository and can be managed directly inside of GitKraken Desktop.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/moC2KyxGb10?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## Adding submodules

Add a submodule by clicking the <button class='button button--success button--ui button--nolink'>+</button> when hovering over <img src='/wp-content/uploads/icons/gk-new-submodules-icon.svg' style='height:1em;'> _Submodules_ in the left panel. Paste the HTTPS or SSH link to the repository, and then enter the path.

<img src="/wp-content/uploads//add-submodule.png" srcset="/wp-content/uploads//add-submodule@2x.png" class="help-center-img img-bordered">

Adding a submodule to the repository adds a link to the submodule's repository in the <code>.gitmodules</code> file.

When the parent repository is cloned, it includes the reference to any submodules and the submodules require initialization.

Your repository tracks the submodule's checked out commit.  If there are any updates to the submodule, the files will not automatically update your working directory.

***

## Updating submodules

To update submodules, navigate to the Submodule pane in the left panel and right click on the submodule.

<img src="/wp-content/uploads//update-submodule.png" srcset="/wp-content/uploads//update-submodule@2x.png" class="help-center-img img-bordered">

If you clone a repository that contains a submodule, you will be prompted to initialize the submodule.  This will clone the submodule's repository and check out the referenced commit.

***

## Changing pointer commit

To change the pointer commit, open the submodule in GitKraken Desktop and then check out the new commit. You may need to first create a branch on the target commit before you can check it out.

Then when you exit the submodule, GitKraken Desktop will detect the change and ask you if you wish to save the change.

<img src="/wp-content/uploads//submodule-commit.png" srcset="/wp-content/uploads//submodule-commit@2x.png" class="help-center-img img-bordered">

***

## Statuses

Below are possible statuses of your submodules and their remedies:

- _Out of sync_ -- The checked out commit of the submodule has changed.  There is a change to the submodule reference in your work in progress that should be stashed, committed or discarded.
- _Added but not initialized_ -- Right click and select initialize.
- _Added and initialized but not committed_ -- When adding a submodule, commit the submodule folder to the repository and insert the reference to the submodule in the <code>.gitmodules</code> file.

***

### Keep submodules up to date

There is a setting to automatically _Keep submodules up to date_ when performing Git actions. This can be enabled or disabled:

+ Globally - from <kbd>Preferences > General</kbd>
+ Per repository - from <kbd>Preferences > Submodules</kbd>

***

### GitKraken Desktop and subtree, not submodules

GitKraken Desktop does not currently support subtree in-app.
