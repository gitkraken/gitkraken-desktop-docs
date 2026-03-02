---
title: Deep Linking in GitKraken Desktop
description: Learn how to share and open deep links to specific branches, commits, tags, and repositories in GitKraken Desktop for faster collaboration.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: February 2026</kbd>

Use deep links in GitKraken Desktop to share or open specific remote repositories, commits, branches, or tags. This allows your team to quickly access relevant project context with a single click.

***

## Quick Start

Use deep links in GitKraken Desktop to share direct access to branches, commits, tags, or repositories with teammates.

**To copy a deep link:**
- Right-click a branch, commit, tag, or repository in the Commit Graph or Left Panel and select the copy link option.
- Paste the copied link into tools like Jira, GitHub, Slack, or Microsoft Teams.

**When a teammate clicks your link:**
- If the repository is already open, GitKraken Desktop navigates directly to the referenced item.
- If the repository is not open, GitKraken Desktop attempts to open it automatically.
- If the repository is not cloned, a clone dialog appears with the URL pre-filled.
- If multiple local copies exist, you will be prompted to select which copy to use.

Deep links are available for any hosted remote repository that is connected through a GitKraken integration. No additional configuration is required beyond having the repository accessible locally.

***

## Copy a Link from GitKraken Desktop

Right-click on a branch, commit, tag, or repository to copy a deep link.

<figure>
  <img src="/wp-content/uploads/link_context_menu_options.gif"
       class="help-center-img img-bordered"
       alt="GitKraken Desktop context menu showing 'Copy link to this commit' options">
  <figcaption style="text-align:center; color:#888">
    Copy link from context menu options
  </figcaption>
</figure>

These links can be pasted into tools like Jira, GitHub, Slack, or Microsoft Teams.

***

## Open a Deep Link

If someone sends you a GitKraken Desktop link:
- Click the link
- GitKraken Desktop will open and navigate to the specified item

<figure>
  <img src="/wp-content/uploads/click_link_slack.gif" 
       class="help-center-img img-bordered"
       alt="User clicking a GitKraken deep link in Slack, opening the commit in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">
    Opening a GitKraken deep link from Slack
  </figcaption>
</figure>

***

## What Happens When...

GitKraken Desktop handles links dynamically depending on your local setup:

- **Repository is not open**: The app will try to open it automatically.
- **Repository is not cloned**: You'll be prompted to clone and the modal will be pre-filled.
- **Multiple copies of the repo**: You'll be prompted to choose which local copy to use.

Deep links streamline collaboration by ensuring you and your teammates view the same Git objects instantly, even across different environments.
