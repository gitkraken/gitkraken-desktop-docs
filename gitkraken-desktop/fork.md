---
title: Fork GitHub Repositories from GitKraken Desktop
description: Learn how to fork public or private GitHub repositories directly from GitKraken Desktop and manage them as remotes.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

Forking allows you to create your own copy of a repository. You can use forks to propose changes, contribute to upstream projects, or maintain your own version of a project.

With the [GitHub integration](/gitkraken-desktop/github-gitkraken-desktop/) or [GitHub Enterprise Server integration](/integrations/github-enterprise/), you can fork repositories directly from GitKraken Desktop.

***

## Fork a Repository

1. [Open the repository](/working-with/open-clone-init/#opening-an-existing-project) you want to fork.
2. In the Left Panel, hover over <em class='context-menu'><img src='/wp-content/uploads/gk-remote-icon.svg' style='height:1em;'> Remote</em> and click the <button class='button button--success button--ui button--nolink'>+</button> icon.
3. Select the <kbd>GitHub.com</kbd> or <kbd>GitHub Enterprise Server</kbd> tab.

<figure>
  <img src="/wp-content/uploads/add-remote.png" srcset="/wp-content/uploads/add-remote@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Add a remote using the + icon in the Left Panel</figcaption>
</figure>

If no fork is currently linked, GitKraken Desktop offers to fork the repo and add it as a remote.

<figure>
  <img src="/wp-content/uploads/fork-github-2025.png" srcset="/wp-content/uploads/fork-github-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitKraken detects the repo is not yet forked</figcaption>
</figure>

Click <button class='button button--success button--ui button--nolink'>Fork and Add Remote</button> to fork the repository and link it.

<figure>
  <img src="/wp-content/uploads/add-fork-2025.png" srcset="/wp-content/uploads/add-fork-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Fork is added as a remote in the Left Panel</figcaption>
</figure>

***

## Add an Existing Fork

If you've already forked the repo on GitHub:

1. Click the <button class='button button--success button--ui button--nolink'>+</button> icon next to <em class='context-menu'><img src='/wp-content/uploads/gk-remote-icon.svg' style='height:1em;'> Remote</em>
2. Select the <kbd>GitHub.com</kbd> or <kbd>GitHub Enterprise Server</kbd> tab

GitKraken Desktop will detect the existing fork and offer to add it.

<figure>
  <img src="/wp-content/uploads/detect-fork.png" srcset="/wp-content/uploads/detect-fork@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Add an existing fork as a remote</figcaption>
</figure>

Click <button class='button button--success button--ui button--nolink'>Add this Remote</button> to link your fork.

You can also [add any remote](/working-with/pushing-and-pulling/#adding-remotes) manually using an HTTPS or SSH URL.
