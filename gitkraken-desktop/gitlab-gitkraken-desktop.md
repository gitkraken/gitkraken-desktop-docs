---
title: GitLab Integration with GitKraken Desktop
description: Connect GitKraken Desktop with GitLab to clone repositories, manage SSH keys, create pull requests, and streamline development with OAuth.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to GitLab.com for repository access, SSH setup, clone and remote workflows, and pull request activity. It also explains the public-repository limitation on the Community plan and how multiple GitLab accounts are handled through profiles.

**Requirements and limits**
- Integration covered here: GitLab.com
- Community plan limit: Public repositories only
- Authentication options: Browser-based GitLab connection or manual OAuth token entry
- Account limit: One GitLab account per profile; multiple accounts require multiple profiles and a GitKraken Pro subscription
- SSH behavior: GitKraken uses the key in <kbd>Preferences &gt; SSH</kbd> unless you configure a GitLab-specific key or enable your local SSH Agent

***

## Quick Start

Connect GitKraken Desktop to GitLab.com to clone repositories, manage remotes, and create pull requests from your GitLab account.

1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Select **GitLab.com** and click **Connect to GitLab**.
3. Log in to GitLab in the browser window that opens, then click **Open GitKraken** to complete the connection.

To configure SSH access after connecting:
- In <kbd>Preferences > Integrations</kbd>, click **Generate SSH key and add to GitLab** to generate and upload a key automatically.
- Or click **Add key to GitLab** to upload your existing SSH default.

Once connected, GitKraken Desktop displays your GitLab repositories when cloning, shows forks when adding remotes, and supports creating and managing pull requests from within the application. To manage more than one GitLab account, use multiple [profiles](/start-here/profiles) with a GitKraken Pro plan.

### What the GitLab integration lets you do

- Create new repositories on your GitLab account with optional .gitignore and license templates.
- Automatically generate and upload an SSH key pair to GitLab.
- Clone repositories directly from your GitLab repo list.
- Easily identify GitLab repos via remote avatars on the graph.
- Add remotes to GitLab repositories.
- Create and manage pull requests from within GitKraken.
- Work with [GitLab Issues](/integrations/gitlab-issues/) alongside your code.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> The <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">GitKraken Community plan</a> only supports public repositories.</p>
</div>

***

## How to connect the GitLab integration

To authenticate with GitLab:

1. Open <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> from the upper-right corner.

<figure>
  <img src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Access GitLab integration from Preferences</figcaption>
</figure>

2. In the integration window, select _GitLab.com_ and click <button class='button button--success button--ui button--nolink'>Connect to GitLab</button>.

<figure>
  <img src="/wp-content/uploads/connect-gitlab-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Click to authenticate GitLab account</figcaption>
</figure>

4. Log in via your default browser. After successful authentication, click <kbd>Open GitKraken</kbd> to complete the connection.

<figure>
  <img src="/wp-content/uploads/gitlab-sign-in-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Sign in to GitLab</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/auth-success-gitlab-1@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Authentication successful — return to GitKraken</figcaption>
</figure>

You may also connect manually using an OAuth token.

<figure>
  <img src="/wp-content/uploads/gitlab-oauth-token.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Enter an OAuth token to connect manually</figcaption>
</figure>

## How to generate an SSH key for GitLab

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken uses the SSH key listed in <kbd>Preferences > SSH</kbd> unless you configure a GitLab-specific key or enable your local SSH Agent.</p>
</div>

Once GitLab is connected, you can generate a new SSH key or upload an existing one:

<figure>
  <img src="/wp-content/uploads/add-key-to-gitlab-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Options to add an SSH key to GitLab</figcaption>
</figure>

- Click <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitLab</button> to automate the process.
- Use <button class='button button--uiorange button--ui button--nolink'>Add key to GitLab</button> to use an existing SSH Default.
- Use _Add existing SSH key_ to upload your own key manually.

***

## What GitLab OAuth enables in GitKraken Desktop

With GitLab connected, GitKraken enhances your workflow with features such as:

- Browsing your GitLab repositories during cloning:

<figure>
  <img src="/wp-content/uploads/clone-gitlab@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Browse GitLab repositories while cloning</figcaption>
</figure>

- Viewing forks when adding remotes:

<figure>
  <img src="/wp-content/uploads/remote-gitlab@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Forks shown when adding GitLab remotes</figcaption>
</figure>

You can still manually enter repository URLs if preferred.

***

## How to connect multiple GitLab accounts

GitKraken supports one GitLab account per profile. With [profile support](/start-here/profiles) in GitKraken Pro, you can switch between multiple GitLab accounts easily.
