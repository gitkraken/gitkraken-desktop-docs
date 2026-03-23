---
title: GitHub Integration with GitKraken Desktop
description: Learn how to connect GitKraken Desktop with GitHub to sign in, clone repos, create pull requests, manage SSH keys, and use OAuth features.
product: GitKraken Desktop
feature: GitHub Integration
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
tags: [github, integration, oauth, ssh, pull-requests]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to GitHub for sign-in, repository access, SSH setup, pull request work, and account management. It covers GitHub.com workflows inside GitKraken Desktop, highlights plan-related limits such as multiple profiles and Community plan restrictions, and points to troubleshooting steps when authentication or repo discovery fails.

**Requirements and limits**
- Integration covered here: GitHub.com
- Community plan: Public repositories only
- Multiple GitHub accounts: Use separate profiles in GitKraken Desktop; Pro plan required
- SSH behavior: GitKraken uses the key set in <kbd>Preferences &gt; SSH</kbd> unless a GitHub-specific key or local SSH Agent is configured
- Pull request review limit: GitKraken Desktop can view pull requests and suggest changes, but full in-app code review and commenting are not available

***

## Quick Start

Connect GitKraken Desktop to GitHub to authenticate, clone repositories, and manage pull requests from your GitHub account.

**To sign in with GitHub:**
1. Open GitKraken Desktop and click **Sign in with GitHub**.
2. Log in with your GitHub credentials in the browser. The connection completes automatically.

**To connect manually or add SSH:**
1. Go to <kbd>Preferences > Integrations</kbd> and select **GitHub**.
2. Click **Connect to GitHub** and log in in the browser.
3. To add an SSH key, click **Generate SSH key and add to GitHub** in the same panel.

**To create a pull request:**
1. Push your branch to GitHub.
2. Select the branch in the Left Panel, then click **Start a pull request** or use the Command Palette.
3. Fill in the title, description, reviewers, and labels, then submit.

**To review a pull request:**
1. Select a pull request from the Left Panel.
2. Click **Review Code and Suggest Changes** to edit files and propose modifications.
3. Click **Suggest X file change to PR** to submit your suggestions.

To use multiple GitHub accounts, create separate [profiles](/start-here/profiles) in GitKraken Desktop (Pro plan required).

**Benefits**

* Login to GitKraken using your GitHub account
* Create repositories on GitHub with `.gitignore` and license options
* Automatically generate an SSH key pair and add it to GitHub
* [Fork repositories](/working-with-repositories/fork/) from GitKraken
* Save authentication into profiles
* Clone from GitHub repo list
* Add remotes for GitHub repos
* Create and work with [Pull Requests](/working-with-repositories/pull-requests/#assignee-labels-and-reviewers)

<div class='callout callout--warning'>
    <p>Note: The <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">GitKraken Community plan</a> only supports public repositories.</p>
</div>

***

## How to sign in with GitHub

To sign in to GitKraken using your GitHub account:

<div class='callout callout--basic'>
    <p><strong>Use GitHub sign-in when:</strong> you want GitHub to be your primary GitKraken Desktop identity and login path. <strong>Don't use sign-in as your only setup step when:</strong> you also need repository-level integration settings such as SSH key management or multiple profiles.</p>
</div>

1. Open GitKraken.
2. Click <kbd>Sign in with GitHub</kbd>.
3. Log in using your GitHub credentials.

This connects your GitHub account to GitKraken automatically.

<figure>
    <img src='/wp-content/uploads/sign-in-github-2025.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">GitKraken login interface with GitHub option</figcaption>
</figure>

***

## How to connect GitKraken Desktop to GitHub

To connect your GitHub account manually:

<div class='callout callout--basic'>
    <p><strong>Use the browser-based GitHub connection when:</strong> standard OAuth access is available and you want the simplest setup. <strong>Use a manual token when:</strong> your environment requires token-based access or you need tighter control over the credentials you provide.</p>
</div>

1. Navigate to <kbd><i>Preferences</i> <i class='fa fa-caret-right'></i> <i>Integrations</i></kbd> in the upper right corner.

<figure>
    <img src="/wp-content/uploads/preferences-menu-gear-2025.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Preferences menu in GitKraken</figcaption>
</figure>

2. From the Integrations window, select **GitHub**.
4. Click <kbd>Connect to GitHub</kbd>. This will open your browser to authenticate GitKraken with GitHub.

<figure>
    <img src="/wp-content/uploads/connect-github-2025@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">GitHub integration screen</figcaption>
</figure>

5. Log in with your GitHub credentials. A confirmation message will appear. Select `Open GitKraken` to finish.

<figure>
    <img src="/wp-content/uploads/github-success-1@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Successful GitHub authentication confirmation</figcaption>
</figure>

Alternatively, you can connect by manually pasting an OAuth token:

<figure>
    <img src="/wp-content/uploads/github-oauth-token.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Manual OAuth token entry</figcaption>
</figure>

### How to generate an SSH key for GitHub

<div class='callout callout'>
    <p>Note 📝 GitKraken uses your SSH key defined in <kbd><i>Preferences <i class='fa fa-caret-right'></i> SSH</i></kbd> unless a GitHub-specific SSH key or your local SSH Agent is configured.</p>
</div>

To generate and add an SSH key to your GitHub account:

1. Go to <kbd><i>Preferences <i class='fa fa-caret-right'></i> Integrations</i></kbd>.
2. Click <kbd>Generate SSH key and add to GitHub</kbd> to complete the process automatically.

You may also:

- Use <kbd>Add key to GitHub</kbd> from _SSH Defaults_.
- Add an existing key via _Add existing SSH key_.

<figure>
    <img src="/wp-content/uploads/add-ssh-key-2025@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Options for adding SSH key in GitKraken</figcaption>
</figure>


***
## What GitHub OAuth enables in GitKraken Desktop

GitKraken's OAuth integration enhances how you interact with your repositories:

<div class='callout callout--basic'>
    <p><strong>Use the GitHub integration when:</strong> you want repository discovery, PR creation, and GitHub-aware workflows directly inside GitKraken Desktop. <strong>Don't rely on it alone when:</strong> you need full GitHub code review and commenting capabilities that still require GitHub's native review experience.</p>
</div>

- View a list of your GitHub repositories to simplify cloning.

<figure>
    <img src="/wp-content/uploads/clone@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">GitHub repositories available for cloning</figcaption>
</figure>

- View a list of repository forks when adding remotes.

<figure>
    <img src="/wp-content/uploads/remote@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Fork list when adding a GitHub remote</figcaption>
</figure>

### How to create pull requests from GitKraken Desktop

Create and manage [Pull Requests](/working-with-repositories/pull-requests/#assignee-labels-and-reviewers) directly in GitKraken. You can:

- Add reviewers
- Assign teammates
- Apply labels

<figure>
    <img src="/wp-content/uploads/pull-request-create@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Creating a pull request in GitKraken</figcaption>
</figure>


### How to use GitHub Pull Request View

<figure>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/MZIPpyQDQ_U?rel=0&vq=hd1080' frameborder='0' allowfullscreen style="display: block; margin: 0 auto;"></iframe>
    <figcaption style="text-align:center;color:#888">Overview of GitHub Pull Request View</figcaption>
</figure>

GitHub.com users can use the **Pull Request View** feature in GitKraken Desktop to review and edit pull requests.

<div class='callout callout--basic'>
    <p><strong>Use Pull Request View when:</strong> you want to inspect files, edit PR metadata, and suggest changes without leaving GitKraken Desktop. <strong>Don't use it as a full replacement for GitHub review when:</strong> you need the full in-browser code review and commenting feature set.</p>
</div>

To access this view:

1. Ensure the [GitHub integration](/gitkraken-desktop/github-gitkraken-desktop/) is connected.
2. Open a GitHub repository in GitKraken Desktop.
3. Select a pull request from the Left Panel, or check out the source branch to reveal a PR icon with the pull request number.

<figure>
    <img src='/wp-content/uploads/github-pr-view-2025@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Accessing Pull Request View via the Left Panel</figcaption>
</figure>

Alternatively, launch the view from the **Launchpad** by clicking the pull request icon on the right.

<figure>
    <img src='/wp-content/uploads/github-pr-view-launchpad.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Opening Pull Request View from the Launchpad</figcaption>
</figure>

Within the Pull Request View, you can edit the following:

- Title
- Description
- Reviewers
- Assignees
- Milestones
- Labels

To review the files affected by a pull request, click the <kbd>Review Code and Suggest Changes</kbd> button in the top-right corner.

<figure>
    <img src='/wp-content/uploads/github-pr-review-2025@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Reviewing files within a pull request</figcaption>
</figure>

<div class='callout callout--basic'>
    <p>Note: While you can view and suggest changes, full code review and commenting features are not yet available within GitKraken Desktop.</p>
</div>

### How to review code and suggest changes

In GitKraken Desktop, the **Review Code and Suggest Changes** feature lets you propose modifications across the entire project—not just to lines that were changed. This is useful when reviewing a Pull Request:

1. Open the Pull Request.
2. Click <kbd>Edit to Suggest Changes to PR #XX</kbd>.
3. Make your edits and save.
4. Click <kbd>Suggest X file change to PR #XX</kbd>.

<figure>
    <img src='/wp-content/uploads/gkc-pr-suggest-code-changes.gif' class="help-center-img img-bordered" style="max-width: 75%;"><figcaption style="text-align:center;color:#888">Suggesting code changes in a pull request</figcaption>
</figure>

### How to accept or reject code suggestions

In the Pull Request panel, suggestions from teammates are labeled with <em class='context-menu'>Code Suggestions</em>.

<figure>
    <img src='/wp-content/uploads/code-suggestion-2025@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Label showing code suggestions</figcaption>
</figure>

Clicking a suggestion opens the diff view, where you can choose to apply or reject the change.

<figure>
    <img src='/wp-content/uploads/gkc-pr-code-suggestions-apply.gif' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Applying code suggestions</figcaption>
</figure>

### How to check out branches, review build status, and add remotes

- **Double-click a branch name** in the PR view to check it out and view its graph.
- **Click the build status** to open the related URL in your browser.

<figure>
    <img src='/wp-content/uploads/build-status@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Build status with link to CI/CD pipeline</figcaption>
</figure>

If the remote is not already added, GitKraken prompts you to add it for local review.

### How to merge pull requests

To merge a pull request:

1. Click <kbd>Merge pull request</kbd>.
2. Choose a merge method:
   - <kbd>Create a merge commit</kbd> (default)
   - <kbd>Squash and merge</kbd>
   - <kbd>Rebase and merge</kbd>

<figure>
    <img src='/wp-content/uploads/merge-options@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Merge options in GitKraken</figcaption>
</figure>

<div class='callout callout--basic'>
  <p>Not seeing updates in the pull request view? Try refreshing GitKraken Desktop.</p>
</div>

### How to fix missing repositories or remotes

If remotes or repositories are missing in the Add Remote or Clone menus:

1. Check if GitKraken has access via your [GitHub Applications](https://github.com/settings/connections/applications/a7557949433b7d282a76).
2. Ask your organization to allow [Organization Approval](https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/).
3. If the repo is owned by another individual, they must also [install GitKraken](/gitkraken-client/how-to-install/) and authorize it.
4. Learn more in [Third-party apps list](https://help.github.com/articles/about-third-party-application-restrictions/).


## How to connect multiple GitHub accounts

GitKraken connects to one GitHub account at a time. However, if you're using the Pro version of GitKraken, you can take advantage of <a href="/start-here/profiles">multiple profiles</a>.

Each profile can be associated with a different GitHub account, allowing you to switch between accounts without needing to disconnect and reconnect each time.
