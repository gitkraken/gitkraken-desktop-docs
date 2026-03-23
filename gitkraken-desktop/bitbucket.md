---
title: Bitbucket Integration with GitKraken Desktop
description: Connect GitKraken Desktop with Bitbucket to clone repositories, manage pull requests, and configure SSH authentication with OAuth or token-based access.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to Bitbucket.org for repository discovery, SSH setup, clone and remote workflows, and pull request activity. It also covers multi-account usage through profiles and the reviewer visibility requirement for Bitbucket pull requests.

**Requirements and limits**
- Integration covered here: Bitbucket.org
- Authentication options: Browser-based Bitbucket connection or manual OAuth token entry
- Account limit: One Bitbucket account per profile; multiple accounts require multiple profiles and a GitKraken Pro subscription
- SSH behavior: GitKraken uses the key in <kbd>Preferences &gt; SSH</kbd> unless you configure a Bitbucket-specific key or use your system SSH Agent
- Pull request reviewer visibility depends on having Project Admin permissions on the repository

***

## Quick Start

Connect GitKraken Desktop to Bitbucket.org to clone repositories, manage remotes, and work with pull requests from your Bitbucket account.

1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Select **Bitbucket.org** and click **Connect to Bitbucket**.
3. Log in to your Bitbucket account in the browser window that opens.
4. Select **Open GitKraken** to complete the connection.

To configure SSH access after connecting:
1. In <kbd>Preferences > Integrations</kbd>, click **Generate SSH key and copy to clipboard**.
2. Paste the key into your Bitbucket account SSH settings.

Once connected, GitKraken Desktop displays your Bitbucket repositories when cloning, lists forks when adding remotes, and supports creating and viewing pull requests within the application. If you need to manage more than one Bitbucket account, use multiple [profiles](/gitkraken-desktop/profiles/) with a GitKraken Pro plan.

### What the Bitbucket integration lets you do

- Create new repositories on your Bitbucket account with .gitignore and license templates.
- Easily generate and copy an SSH key pair for Bitbucket.
- Save authentication in reusable [profiles](/gitkraken-desktop/profiles/).
- Clone from a personalized Bitbucket repository list.
- Add and manage remotes from Bitbucket.
- Create and view pull requests within GitKraken.

<div class='embed-container embed-container--16-9'>
  <iframe width='560' height='315' src='https://www.youtube.com/embed/sQ4ouJpAeR8?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## How to connect Bitbucket

To authenticate with Bitbucket:

1. Navigate to <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> in the upper-right corner.

<figure>
  <img src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Open Preferences to configure integrations</figcaption>
</figure>

2. Select <strong>Bitbucket.org</strong> and click <button class='button button--success button--ui button--nolink'>Connect to Bitbucket</button>.

<figure>
  <img src="/wp-content/uploads/connect-bitbucket-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Click to authenticate via Bitbucket</figcaption>
</figure>

4. A browser window opens prompting you to log in. Upon success, confirm by selecting <kbd>Open GitKraken</kbd>.

<figure>
  <img src="/wp-content/uploads/bitbucket-success-1@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Login success prompt from Bitbucket</figcaption>
</figure>

Alternatively, you may authenticate manually using an OAuth token:

<figure style="text-align:center;">
  <img src="/wp-content/uploads/bitbucket-oauth-token.png" class="img-bordered" style="display:inline-block;">
  <figcaption style="color:#888; text-align:center">Manual OAuth token entry for Bitbucket</figcaption>
</figure>

***

## How to generate SSH keys for Bitbucket

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken uses your SSH key from <kbd>Preferences > SSH</kbd> unless a Bitbucket-specific key is configured or your system SSH Agent is enabled.</p>
</div>

After connecting Bitbucket:

1. Go to <kbd>Preferences > Integrations</kbd>.
2. Click <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</button>.
3. Paste the key into your Bitbucket account settings.

<figure>
  <img class="img-bordered center aligncenter" decoding="async" src='/wp-content/uploads/ssh-bitbucket-2025@2x.png' class="img-bordered" class="help-center" style="display:inline-block;">
  <figcaption style="color:#888; text-align:center">Copy and add your new SSH key to Bitbucket</figcaption>
</figure>

***

## What Bitbucket OAuth enables in GitKraken Desktop

GitKraken enhances your workflow with:

- A searchable list of Bitbucket repositories when cloning:

<figure>
  <img src="/wp-content/uploads/clone@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Cloning from your Bitbucket repositories</figcaption>
</figure>

- A list of forks when adding remotes:

<figure>
  <img src="/wp-content/uploads/remote@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Forks available for remote setup</figcaption>
</figure>

Manual repo URLs are still supported.

***

## How to connect multiple Bitbucket accounts

GitKraken supports one Bitbucket account per profile. With GitKraken Pro, use multiple [profiles](/start-here/profiles) to manage several Bitbucket identities.

## How Bitbucket pull request reviewers work

Bitbucket supports pull request reviewers. GitKraken will show reviewer details if you have Project Admin permissions on the repository.
