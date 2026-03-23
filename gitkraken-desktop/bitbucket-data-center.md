---
title: Bitbucket Data Center Integration with GitKraken Desktop
description: Connect GitKraken Desktop to your Bitbucket Data Center server for repository access, SSH authentication, cloning, and pull request workflows.
product: GitKraken Desktop
feature: Bitbucket Data Center Integration
content_type: how-to
audience: developer
plan_required: Advanced
os_support: [Windows, macOS, Linux]
git_hosts: [Bitbucket Data Center]
integrations: [Bitbucket Data Center]
hosted_variant: self-hosted
status: GA
last_verified: 2026-03
llms_include: true
tags: [bitbucket-data-center, self-hosted, pat, ssh, pull-requests]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to Bitbucket Data Center in a self-hosted environment so you can authenticate with a personal access token, configure SSH, clone repositories, and work with pull requests. This integration requires an Advanced subscription tier or higher.

**Requirements and limits**
- Integration covered here: Bitbucket Data Center in a self-hosted environment
- Plan: Advanced subscription tier or higher for self-hosted integrations
- Authentication: Personal Access Token (PAT)
- Server support: Bitbucket Data Center versions released within the past year
- Account limit: One Bitbucket Data Center account per profile; multiple accounts require multiple profiles
- SSH behavior: GitKraken uses the key in <kbd>Preferences &gt; SSH</kbd> unless you configure a Bitbucket-specific key or use your system SSH Agent
- Pull request reviewer visibility depends on token scopes and repository permissions

***

## Quick Start

Connect GitKraken Desktop to a Bitbucket Data Center server to clone repositories and manage pull requests from your self-hosted environment.

1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Select **Bitbucket Data Center**, enter your host domain, and click **Generate a token on Bitbucket Data Center**.
3. Log in to your Bitbucket Data Center account in the browser and create a Personal Access Token with the appropriate permissions.
4. Copy the token, paste it into GitKraken Desktop, and click **Connect**.

To configure SSH access after connecting:
1. In <kbd>Preferences > Integrations</kbd>, click **Generate SSH key and copy to clipboard**.
2. Open your Bitbucket Data Center account settings and add the copied public key.

Once connected, you can clone repositories directly from your Bitbucket Data Center list, add remotes including forks, and create and view pull requests from within GitKraken Desktop. GitKraken Desktop supports one Bitbucket Data Center account per profile. Use multiple [profiles](/gitkraken-desktop/profiles/) to work with more than one account.

### What the Bitbucket Data Center integration lets you do

- Create repositories on Bitbucket Data Center with optional .gitignore and license files.
- Generate and copy an SSH key to use with Bitbucket Data Center.
- Save authentication in reusable [profiles](/gitkraken-desktop/profiles/).
- Clone from your Bitbucket Data Center repository list.
- Add remotes for Bitbucket Data Center repositories.
- Create and view pull requests.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> All self-hosted server integrations, including Bitbucket Data Center, require an <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">Advanced subscription</a> tier or higher.</p>
</div>

***

## How to connect Bitbucket Data Center

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken Desktop supports Bitbucket Data Center versions released within the past year.</p>
</div>

<div class='callout callout--basic'>
  <p><strong>Use Bitbucket Data Center integration when:</strong> your repositories live on a self-hosted Bitbucket Data Center server. <strong>Don't use the Bitbucket.org integration when:</strong> your environment requires self-hosted server access, PAT authentication, or Data Center-specific permissions.</p>
</div>

To authenticate:

1. Go to <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd>.

<figure>
  <img src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Open Preferences to access Integrations</figcaption>
</figure>

2. Choose **Bitbucket Data Center**. Enter your host domain and click <button class='button button--success button--ui button--nolink'>Generate a token on Bitbucket Data Center</button>. Ensure the token has appropriate permissions.

<figure>
  <img src="/wp-content/uploads/connecting-bb-data-center-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Start connection to Bitbucket Data Center</figcaption>
</figure>

4. In the browser, log in to your Bitbucket Data Center account and create the token.

<figure>
  <img src="/wp-content/uploads/BitbucketServerPAT.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Create a Personal Access Token in Bitbucket Data Center</figcaption>
</figure>

5. Paste the token into GitKraken and click <button class='button button--success button--ui button--nolink'>Connect</button>.

***

## How to generate SSH keys for Bitbucket Data Center

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken uses the key in <kbd>Preferences > SSH</kbd> unless you configure a Bitbucket-specific SSH key or use your system SSH Agent.</p>
</div>

1. Open <kbd>Preferences > Integrations</kbd>.
2. Click <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</button>.
3. Follow the in-app toast or manual instructions to add the key.

<figure>
  <img src="/wp-content/uploads/ssh-bb-data-center-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Generate and copy your SSH key</figcaption>
</figure>

4. In your Bitbucket Data Center account:
   - Click <button class='button button--primary button--ui button--nolink'>Add Key</button>.

<figure style="text-align:center;">
  <img src="/wp-content/uploads/bitbucket-server-add-key.png" class="help-center-img img-bordered" style="display:inline-block;">
  <figcaption style="color:#888; text-align:center">Add the SSH key to Bitbucket Data Center</figcaption>
</figure>

5. Paste your public key and click <button class='button button--primary button--ui button--nolink'>Add Key</button>.

<figure>
  <img src="/wp-content/uploads/bitbucket-server-SSHkey-add@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">SSH key successfully added</figcaption>
</figure>

***

## What Bitbucket Data Center authentication enables in GitKraken Desktop

GitKraken allows you to:

<div class='callout callout--basic'>
  <p><strong>Use this integration when:</strong> you want cloning, remotes, and pull request workflows against your self-hosted Bitbucket Data Center instance inside GitKraken Desktop. <strong>Don't use it when:</strong> your repositories are on Bitbucket.org rather than a self-hosted server.</p>
</div>

- Search your repositories when cloning:

<figure>
  <img src="/wp-content/uploads/bb-data-center-clone@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Clone repositories from Bitbucket Data Center</figcaption>
</figure>

- View forks when adding remotes:

<figure>
  <img src="/wp-content/uploads/add-remote-bb-dc-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Remotes list includes repository forks</figcaption>
</figure>

Manual entry of repository URLs is also supported.

***

## How to connect multiple Bitbucket Data Center accounts

GitKraken supports one Bitbucket Data Center account per profile. Use multiple [profiles](/start-here/profiles) with GitKraken Pro to switch between accounts.

<div class='callout callout--basic'>
  <p><strong>Use multiple profiles when:</strong> you need to switch between separate Data Center accounts or host domains. <strong>Don't use multiple profiles when:</strong> one profile already covers the single self-hosted account you use.</p>
</div>

## How Bitbucket Data Center pull request reviewers work

If your token includes Project Admin and Repository Admin scopes, and you have the correct permissions, GitKraken will display reviewer details for pull requests.
