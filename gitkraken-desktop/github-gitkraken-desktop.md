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
last_verified: 2026-11
llms_include: true
tags: [github, integration, oauth, ssh, pull-requests]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "integrations-with-git-providers"
    nav_label: "GitHub"
    nav_order: 10
    nav_parent: "integrations-with-git-providers"
    page_type: "content"
---
<kbd>Last updated: November 2026</kbd>

Use this page to connect GitKraken Desktop to GitHub for sign-in, repository access, SSH setup, pull request work, and account management on GitHub.com. If repositories or remotes are missing after you connect, see [How to fix missing repositories or remotes](#how-to-fix-missing-repositories-or-remotes).

**Requirements and limits**
- Integration covered here: GitHub.com
- Community plan: Public repositories only
- Multiple GitHub accounts: Each profile uses one GitHub account at a time; you can switch a profile between connected accounts, and multiple profiles require a Pro plan
- SSH behavior: GitKraken Desktop uses the key set in <kbd>Preferences &gt; SSH</kbd> unless a GitHub-specific key or local SSH Agent is configured
- Pull request review: **Review on GitKraken.dev** opens a pull request in GitKraken Code Review in your browser

| Workflow | GitHub.com support | Community limits | Notes |
|----------|--------------------|------------------|-------|
| Sign in and connect account | Yes | None | Browser-based sign-in and connection through GitKraken.dev |
| Clone and browse repositories | Yes | Public repositories only | Private repo access requires a paid plan |
| SSH key generation and upload | Yes | Public repositories only | Uses GitKraken Desktop SSH settings unless overridden |
| Create and view pull requests | Yes | Public repositories only | Supported directly in GitKraken Desktop |
| Review pull requests | Yes | Public repositories only | Opens in GitKraken Code Review on GitKraken.dev |
| Multiple GitHub accounts | Yes | Not included | One account per profile; multiple profiles require a Pro plan |

***

## Quick Start


**To sign in with GitHub:**
1. Click the profile icon in the top-right corner of GitKraken Desktop and select **Sign in**.
2. In the browser window that opens on GitKraken.dev, choose GitHub and log in with your GitHub credentials. The sign-in completes automatically.

**To connect manually or add SSH:**
1. Go to <kbd>Preferences > Integrations</kbd> and select **GitHub**.
2. Click **Connect to GitHub** and log in in the browser.
3. To add an SSH key, click **Generate SSH key and add to GitHub** in the same panel.

**To create a pull request:**
1. Push your branch to GitHub.
2. Select the branch in the Left Panel, then click **Start a pull request** or use the Command Palette.
3. Fill in the title, description, reviewers, and labels, then submit.

**To review a pull request:** Right-click the pull request in the Left Panel and select **Review on GitKraken.dev**. The pull request opens in GitKraken Code Review in your browser.

To use multiple GitHub accounts, [connect another GitHub account](#how-to-connect-multiple-github-accounts) and switch between them, or create separate [profiles](/start-here/profiles) in GitKraken Desktop (Pro plan required).

With the GitHub integration, you can:

* Sign in to GitKraken Desktop with your GitHub account
* Create repositories on GitHub with `.gitignore` and license options
* Generate an SSH key pair and add it to GitHub
* [Fork repositories](/working-with-repositories/fork/) from GitKraken Desktop
* Save authentication into profiles
* Clone from your list of GitHub repositories
* Add remotes for GitHub repositories
* Create and work with [pull requests](/working-with-repositories/pull-requests/#how-assignees-labels-and-reviewers-work)

<div class='callout callout--warning'>
    <p>Note: The <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">GitKraken Community plan</a> only supports public repositories.</p>
</div>

***

## How to sign in with GitHub

GitKraken Desktop signs you in through your browser on GitKraken.dev.

<div class='callout callout--basic'>
    <p><strong>Use GitHub sign-in when:</strong> you want GitHub to be your primary GitKraken Desktop identity and login path. <strong>Do not use sign-in as your only setup step when:</strong> you also need repository-level integration settings such as SSH key management or multiple profiles.</p>
</div>

To sign in with your GitHub account:

1. Click the profile icon in the top-right corner of GitKraken Desktop and select **Sign in**. During first-time setup, select GitHub as your provider instead. GitKraken Desktop shows the **Sign In to GitKraken** dialog and opens GitKraken.dev in your browser.
2. On GitKraken.dev, choose GitHub and log in with your GitHub credentials.

The sign-in completes automatically and connects your GitHub account to GitKraken Desktop.

<figure>
    <img alt="The Sign In to GitKraken dialog in GitKraken Desktop, reading Sign in from your browser to continue, with links to open it manually or copy the URL if the browser did not open, and a Manually enter authentication code link." src='/wp-content/uploads/sign-in-github-2025-v2@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">The Sign In to GitKraken dialog</figcaption>
</figure>

If your browser does not open, click **open it manually** or **copy the URL** in the dialog. If GitKraken.dev gives you an authentication code, click **Manually enter authentication code**, paste the code, and click **Save**.

***

## How to connect GitKraken Desktop to GitHub

To connect your GitHub account manually, first sign in to your GitKraken account. GitHub connections belong to your GitKraken account, so a connection you make is also available on your other devices and profiles.

1. Navigate to <kbd><i>Preferences</i> <i class='fa fa-caret-right'></i> <i>Integrations</i></kbd> in the upper right corner.

<figure>
    <img alt="The gear icon in the GitKraken Desktop toolbar highlighted, with its Preferences tooltip." src="/wp-content/uploads/preferences-menu-gear-2025.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Open Preferences from the gear icon.</figcaption>
</figure>

2. From the Integrations window, select **GitHub**.
3. Click <kbd>Connect to GitHub</kbd>. GitKraken Desktop opens your browser to authenticate with GitHub.

<figure>
    <img alt="Preferences > Integrations > GitHub in GitKraken Desktop: the GitHub card reads Not Connected with a Connect to GitHub button, and a Manage Integrations button sits at the top right of the pane." src="/wp-content/uploads/connect-github-2025-v3@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">GitHub integration screen</figcaption>
</figure>

4. Log in with your GitHub credentials. When the confirmation message appears, select **Open GitKraken** to finish.

<figure>
    <img alt="Successful GitHub authentication confirmation" src="/wp-content/uploads/github-success-1@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Successful GitHub authentication confirmation</figcaption>
</figure>

When the connection is complete, the GitHub card shows **Connected to your GitHub integration** and your GitHub user name.

- Click **Manage Integrations** to manage your connected integrations on GitKraken.dev.
- Click **Disconnect from this profile** to remove the GitHub connection from the current profile. The connection stays available to your other devices and profiles.

### How to generate an SSH key for GitHub

<div class='callout callout'>
    <p>Note 📝 GitKraken Desktop uses your SSH key defined in <kbd><i>Preferences <i class='fa fa-caret-right'></i> SSH</i></kbd> unless a GitHub-specific SSH key or your local SSH Agent is configured.</p>
</div>

To generate and add an SSH key to your GitHub account:

1. Go to <kbd><i>Preferences <i class='fa fa-caret-right'></i> Integrations</i></kbd>.
2. Click <kbd>Generate SSH key and add to GitHub</kbd> to complete the process automatically.

You can also:

- Use <kbd>Add key to GitHub</kbd> from _SSH Defaults_.
- Add an existing key with <kbd>Add existing SSH key</kbd>.

<figure>
    <img alt="Options for adding an SSH key in GitKraken Desktop" src="/wp-content/uploads/add-ssh-key-2025@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Options for adding an SSH key in GitKraken Desktop</figcaption>
</figure>


***
## What GitHub OAuth enables in GitKraken Desktop

<div class='callout callout--basic'>
    <p><strong>Use the GitHub integration when:</strong> you want repository discovery, PR creation, and GitHub-aware workflows directly inside GitKraken Desktop. <strong>Use GitKraken Code Review when:</strong> you need to review a pull request's code. Click <strong>Review on GitKraken.dev</strong> to open it in your browser.</p>
</div>

With GitHub connected, you can:

- See a list of your GitHub repositories when you clone.

<figure>
    <img alt="GitHub repositories available for cloning" src="/wp-content/uploads/clone@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">GitHub repositories available for cloning</figcaption>
</figure>

- See a list of repository forks when you add a remote.

<figure>
    <img alt="Fork list when adding a GitHub remote" src="/wp-content/uploads/remote@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Fork list when adding a GitHub remote</figcaption>
</figure>

### How to create pull requests from GitKraken Desktop

Create and manage [pull requests](/working-with-repositories/pull-requests/#how-assignees-labels-and-reviewers-work) in GitKraken Desktop. When you create one, you can:

- Add reviewers
- Assign teammates
- Apply labels

<figure>
    <img alt="Creating a pull request in GitKraken Desktop" src="/wp-content/uploads/pull-request-create@2x.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Creating a pull request in GitKraken Desktop</figcaption>
</figure>


### How to use GitHub Pull Request View

<figure>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/MZIPpyQDQ_U?rel=0&vq=hd1080' frameborder='0' allowfullscreen style="display: block; margin: 0 auto;"></iframe>
    <figcaption style="text-align:center;color:#888">Overview of GitHub Pull Request View</figcaption>
</figure>

On GitHub.com repositories, use **Pull Request View** in GitKraken Desktop to view and edit pull requests.

<div class='callout callout--basic'>
    <p><strong>Use Pull Request View when:</strong> you want to edit PR metadata, check build status, or merge without leaving GitKraken Desktop. <strong>Use GitKraken Code Review when:</strong> you want to review the code in the pull request.</p>
</div>

To open Pull Request View:

1. Make sure the [GitHub integration](#how-to-connect-gitkraken-desktop-to-github) is connected.
2. Open a GitHub repository in GitKraken Desktop.
3. Select a pull request from the Left Panel, or check out the source branch to reveal a PR icon with the pull request number.

<figure>
    <img alt="Accessing Pull Request View via the Left Panel" src='/wp-content/uploads/github-pr-view-2025@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Accessing Pull Request View via the Left Panel</figcaption>
</figure>

You can also open it from Launchpad: click the **Open Pull Request Panel** icon in the pull request's row.

<figure>
    <img alt="Opening Pull Request View from the Launchpad" src='/wp-content/uploads/github-pr-view-launchpad.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Opening Pull Request View from the Launchpad</figcaption>
</figure>

In Pull Request View, you can edit:

- Title
- Description
- Reviewers
- Assignees
- Milestones
- Labels

To review the files affected by a pull request, click <kbd>Review on GitKraken.dev</kbd> below the number of changed files. The pull request opens in GitKraken Code Review in your browser. For other ways to start a review, see [How to review pull requests with GitKraken Code Review](/working-with-repositories/pull-requests/#how-to-review-pull-requests-with-gitkraken-code-review).

If the pull request is part of a stack, the Pull Request View header shows its position in the stack, with arrows to move between the pull requests in the stack. For details, see [stacked pull requests](/working-with-repositories/pull-requests/).

### How to accept or reject code suggestions

In Pull Request View, code suggestions from teammates appear under <em class='context-menu'>Code Suggestions</em>.

<figure>
    <img alt="Label showing code suggestions" src='/wp-content/uploads/code-suggestion-2025@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Label showing code suggestions</figcaption>
</figure>

Click a suggestion to open its diff, then apply or reject the change.

<figure>
    <img alt="Applying code suggestions" src='/wp-content/uploads/gkc-pr-code-suggestions-apply.gif' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Applying code suggestions</figcaption>
</figure>

### How to check out branches, review build status, and add remotes

- **Double-click a branch name** in Pull Request View to check it out and view its graph.
- **Click the build status** to open the latest build in your browser.

<figure>
    <img alt="Build status with link to CI/CD pipeline" src='/wp-content/uploads/build-status@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Build status with link to CI/CD pipeline</figcaption>
</figure>

If the branch's remote is not in your repository yet, GitKraken Desktop prompts you to add it.

### How to merge pull requests

To merge a pull request:

1. In Pull Request View, click <kbd>Merge Pull Request</kbd>.
2. Choose a merge method:
   - <kbd>Create a merge commit</kbd> (default)
   - <kbd>Squash and merge</kbd>
   - <kbd>Rebase and merge</kbd>

<figure>
    <img alt="Merge options in GitKraken Desktop" src='/wp-content/uploads/merge-options@2x.png' class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Merge options in GitKraken Desktop</figcaption>
</figure>

<div class='callout callout--basic'>
  <p>If Pull Request View does not show recent updates, refresh GitKraken Desktop.</p>
</div>

### How to fix missing repositories or remotes

If remotes or repositories are missing in the Add Remote or Clone menus:

1. Check that GitKraken has access in your [GitHub Applications](https://github.com/settings/connections/applications/a7557949433b7d282a76).
2. Ask your organization to allow [Organization Approval](https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/).
3. If the repo is owned by another individual, they must also [install GitKraken](/gitkraken-client/how-to-install/) and authorize it.
4. Read GitHub's guide to [third-party application restrictions](https://help.github.com/articles/about-third-party-application-restrictions/).


## How to connect multiple GitHub accounts

Each GitKraken Desktop profile uses one GitHub account at a time. You can connect more than one GitHub account and choose which one the current profile uses:

1. Go to <kbd>Preferences > Integrations</kbd> and select **GitHub**.
2. To add an account, click **Connect another GitHub account** and log in with that account in your browser.
3. To switch accounts, click **Use a different GitHub account for this profile** and choose the account.

With a Pro plan, you can also use <a href="/start-here/profiles">multiple profiles</a>. You can associate each profile with a different GitHub account, then switch accounts by switching profiles.
