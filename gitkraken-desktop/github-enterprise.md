---
title: GitHub Enterprise Integration with GitKraken Desktop
description: Connect GitKraken Desktop with your GitHub Enterprise Server to manage repos, pull requests, SSH keys, and profiles using OAuth or access tokens.
product: GitKraken Desktop
feature: GitHub Enterprise Server Integration
content_type: how-to
audience: developer
plan_required: [Advanced, Business, Enterprise]
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub Enterprise Server]
integrations: [GitHub Enterprise Server]
hosted_variant: self-hosted
status: GA
last_verified: 2026-03
llms_include: true
tags: [github-enterprise-server, self-hosted, token, ssh, pull-requests]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

This page explains how to connect GitKraken Desktop to GitHub Enterprise Server so you can authenticate, browse repositories, manage remotes, upload SSH keys, and work with pull requests from one interface. Use it when setting up a self-hosted GitHub Enterprise Server connection or switching between enterprise accounts with profiles.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitHub Enterprise Server integration is available on Advanced, Business, and Enterprise plans.</p>
</div>

**Requirements and limits**
- Integration covered here: GitHub Enterprise Server
- Plan: Advanced, Business, or Enterprise
- Supported server versions: GitHub Enterprise Server releases from the past year
- Authentication: Personal access token required to connect
- Account limit: One GitHub Enterprise Server account per profile
- SSH behavior: GitKraken uses the key set in <kbd>Preferences &gt; SSH</kbd> unless a GitHub-specific key or system SSH Agent is configured

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Enter your GitHub Enterprise Server host domain and click the link to generate an access token.
3. Log in to your GitHub Enterprise Server, generate the token, and copy it.
4. Paste the token into GitKraken Desktop and click **Connect**.

To configure SSH access after connecting:
- In <kbd>Preferences > Integrations</kbd>, click **Generate SSH key and add to GitHub Enterprise Server** to generate and upload a new key automatically.
- Or click **Add key to GitHub Enterprise Server** to upload your existing SSH default.

Once connected, you can browse repositories when cloning, add remotes, and create and view pull requests from within GitKraken Desktop. GitKraken Desktop supports one GitHub Enterprise Server account per profile. Use multiple [profiles](/start-here/profiles) to work with more than one account.

### What you can do after connecting

- Create new repositories on GitHub Enterprise Server with options to add a .gitignore and license file.
- Automatically generate and upload an SSH key to GitHub Enterprise Server.
- [Fork repositories](/working-with-repositories/fork/) directly from GitKraken.
- Save GitHub Enterprise Server authentication into [profiles](/gitkraken-desktop/profiles/).
- Clone repositories using the integrated repo list.
- Add remotes from GitHub Enterprise Server.
- Create and view pull requests within GitKraken.

***

## How to connect GitHub Enterprise Server

<div class='callout callout'>
    <p><strong>Note:</strong> GitKraken supports any GitHub Enterprise Server version released within the past year.</p>
</div>

<div class='callout callout--basic'>
    <p><strong>Use GitHub Enterprise Server integration when:</strong> your repositories live on a self-hosted GitHub Enterprise Server instance and require token-based access. <strong>Don't use the GitHub.com integration when:</strong> your environment depends on enterprise host domains, self-hosted server compatibility, or enterprise-specific credentials.</p>
</div>

To authenticate with GitHub Enterprise Server:

1. Go to <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> in the upper-right corner.

<figure>
  <img src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Accessing Preferences and Integrations</figcaption>
</figure>

2. Enter your GitHub Enterprise Server host domain and follow the link to generate an access token.

<figure>
  <img src="/wp-content/uploads/gkc-github-enterprise-server-integration.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Enter host and generate access token</figcaption>
</figure>

4. Log in using your GitHub Enterprise Server credentials and copy the token. Paste it into GitKraken and click <button class='button button--success button--ui button--nolink'>Connect</button>.

<figure>
  <img src='/wp-content/uploads/accesstoken-github-enterprise.png' class='center img-bordered'>
  <figcaption style="color:#888; text-align:center">Generate and copy your GitHub Enterprise access token</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/gkc-github-enterprise-server-integration-2.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Paste token into GitKraken and connect</figcaption>
</figure>

## How to generate or upload an SSH key for GitHub Enterprise Server

<div class='callout callout'>
    <p><strong>Note:</strong> GitKraken uses the SSH key set in <kbd>Preferences > SSH</kbd> unless you configure a GitHub-specific key or enable your system’s SSH Agent.</p>
</div>

After connecting your GitHub Enterprise Server account, you can generate a new SSH key and upload it directly:

<figure>
  <img src='/wp-content/uploads/gkc-github-enterprise-server-add-key.png' class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Generate SSH key and upload to GitHub Enterprise</figcaption>
</figure>

You can:

- Click <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitHub Enterprise Server</button>.
- Use <button class='button button--uiorange button--ui button--nolink'>Add key to GitHub Enterprise Server</button> to upload your SSH default.
- Use _Add existing SSH key_ if you have a saved key pair.

***

## How to use multiple GitHub Enterprise Server accounts

GitKraken supports one GitHub Enterprise Server account per profile. Use [multiple profiles](/start-here/profiles) to switch between accounts.

<div class='callout callout--basic'>
    <p><strong>Use multiple profiles when:</strong> you need to switch between separate enterprise servers or distinct enterprise identities. <strong>Don't use multiple profiles when:</strong> one enterprise account already covers the repositories you work with.</p>
</div>
