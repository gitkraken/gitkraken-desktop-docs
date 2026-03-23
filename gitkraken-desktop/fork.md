---
title: Fork GitHub Repositories from GitKraken Desktop
description: Learn how to fork public or private GitHub repositories directly from GitKraken Desktop and manage them as remotes.
product: GitKraken Desktop
feature: Fork
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub]
integrations: [GitHub]
hosted_variant: cloud
status: GA
last_verified: 2026-03
llms_include: true
tags: [fork, github, remotes, repositories, integration]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to fork GitHub or GitHub Enterprise Server repositories from GitKraken Desktop and add the fork as a remote without leaving the app. Forking is useful when you need your own copy of a repository to contribute changes, open pull requests, or maintain a separate version of a project.

With the [GitHub integration](/gitkraken-desktop/github-gitkraken-desktop/) or [GitHub Enterprise Server integration](/integrations/github-enterprise/), you can fork repositories directly from GitKraken Desktop.

**Requirements and limits**
- Supported hosts on this page: GitHub.com and GitHub Enterprise Server
- Requirement: The repository must already be open in GitKraken Desktop
- Integration requirement: Use the GitHub or GitHub Enterprise Server integration tab in the Add Remote flow
- Existing fork behavior: GitKraken Desktop can detect an existing fork and offer to add it as a remote
- Manual fallback: If needed, add the fork manually with an HTTPS or SSH remote URL

***

## Quick Start


**To fork a repository and add it as a remote:**
1. Open the repository you want to fork in GitKraken Desktop.
2. In the Left Panel, hover over **Remote** and click the **+** icon.
3. Select the **GitHub.com** or **GitHub Enterprise Server** tab.
4. If no fork is linked, GitKraken Desktop offers to fork the repo. Click **Fork and Add Remote**.

**To add an existing fork as a remote:**
1. Click the **+** icon next to **Remote** in the Left Panel.
2. Select the **GitHub.com** or **GitHub Enterprise Server** tab.
3. GitKraken Desktop detects the existing fork and offers to add it. Click **Add this Remote**.

The fork appears in the Left Panel under **Remote** and is ready to use for pushing branches and creating pull requests. If you need to add a remote manually, use an HTTPS or SSH URL from the same panel.

***

## How to fork a repository

1. [Open the repository](/working-with/open-clone-init/#opening-an-existing-project) you want to fork.
2. In the Left Panel, hover over <em class='context-menu'><img src='/wp-content/uploads/gk-remote-icon.svg' style='height:1em;'> Remote</em> and click the <button class='button button--success button--ui button--nolink'>+</button> icon.
3. Select the <kbd>GitHub.com</kbd> or <kbd>GitHub Enterprise Server</kbd> tab.

<figure>
  <img src="/wp-content/uploads/add-remote@2x.png" class="help-center-img img-bordered" alt="GitKraken interface showing the Add Remote panel with a green plus icon on the REMOTE section and GitHub.com selected as the source.">
  <figcaption style="text-align:center; color:#888">Add a remote using the + icon in the Left Panel</figcaption>
</figure>

If no fork is currently linked, GitKraken Desktop offers to fork the repo and add it as a remote.

<figure>
  <img src="/wp-content/uploads/fork-github-2025@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop UI showing an alert that the user has not yet forked the DiceDB/dice repository on GitHub, with a button to 'Fork and Add Remote'.">
  <figcaption style="text-align:center; color:#888">GitKraken detects the repo is not yet forked</figcaption>
</figure>

Click <button class='button button--success button--ui button--nolink'>Fork and Add Remote</button> to fork the repository and link it.

<figure>
  <img src="/wp-content/uploads/add-fork-2025@2x.png" class="help-center-img img-bordered" alt="Fork remote named 'jjsilva4' shown in the Left Panel of GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Fork is added as a remote in the Left Panel</figcaption>
</figure>

***

## How to add an existing fork

If you've already forked the repo on GitHub:

1. Click the <button class='button button--success button--ui button--nolink'>+</button> icon next to <em class='context-menu'><img src='/wp-content/uploads/gk-remote-icon.svg' style='height:1em;'> Remote</em>
2. Select the <kbd>GitHub.com</kbd> or <kbd>GitHub Enterprise Server</kbd> tab

GitKraken Desktop will detect the existing fork and offer to add it.

<figure>
  <img src="/wp-content/uploads/detect-fork@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop detecting a fork from the Add Remote pane and prompting to add it as a remote">
  <figcaption style="text-align:center; color:#888">Add an existing fork as a remote</figcaption>
</figure>

Click <button class='button button--success button--ui button--nolink'>Add this Remote</button> to link your fork.

You can also [add any remote](/working-with/pushing-and-pulling/#adding-remotes) manually using an HTTPS or SSH URL.
