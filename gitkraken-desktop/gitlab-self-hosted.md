---
title: GitLab Self-Managed Integration with GitKraken Desktop
description: Connect GitKraken Desktop with your GitLab Self-Managed server to manage repositories, SSH keys, and pull requests using personal access tokens.
product: GitKraken Desktop
feature: GitLab Self-Managed Integration
content_type: how-to
audience: developer
plan_required: Enterprise
os_support: [Windows, macOS, Linux]
git_hosts: [GitLab Self-Managed]
integrations: [GitLab Self-Managed]
hosted_variant: self-hosted
status: GA
last_verified: 2026-03
llms_include: true
tags: [gitlab-self-managed, self-hosted, pat, ssh, pull-requests]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to a GitLab Self-Managed server so you can authenticate with a personal access token, manage SSH keys, discover repositories, and work with pull requests in your self-hosted GitLab environment. This integration requires an Advanced subscription tier or higher.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> All self-hosted server integrations, including GitLab Self-Managed, require an <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">Advanced subscription</a> tier or higher.</p>
</div>

**Requirements and limits**
- Integration covered here: GitLab Self-Managed
- Plan: Advanced subscription tier or higher
- Supported server versions: GitLab Self-Managed releases from the past year
- Authentication: Personal access token with `api` and `read_user` scopes
- Token setup note: Leave token expiration blank when following this workflow
- Account limit: One GitLab Self-Managed account per profile; use Profiles for multiple accounts
- SSH behavior: GitKraken uses the key in <kbd>Preferences &gt; SSH</kbd> unless you configure a GitLab-specific key or system SSH Agent

<div class='embed-container embed-container--16-9'>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/BhIX7fGSM8k?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

## Quick Start

Connect GitKraken Desktop to a GitLab Self-Managed server to clone repositories, manage remotes, and create pull requests.

1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Select **GitLab Self-Managed**, enter your host domain, and click **Generate a token on GitLab**.
3. Log in to your GitLab instance, generate a Personal Access Token with the `api` and `read_user` scopes (leave expiration blank), and copy the token.
4. Paste the token into GitKraken Desktop and click **Connect**.

To configure SSH access after connecting:
- In <kbd>Preferences > Integrations</kbd>, click **Generate SSH key and add to GitLab** to generate and upload a key automatically.
- Or click **Add key to GitLab** to upload your existing SSH default.

Once connected, GitKraken Desktop lets you clone from your self-hosted repository list, add remotes, and create or view pull requests. To manage more than one GitLab Self-Managed account, use multiple [profiles](/start-here/profiles) with a GitKraken Pro plan.

### What the GitLab Self-Managed integration lets you do

- Create new repositories with optional .gitignore and license files.
- Automatically generate an SSH key and upload it to GitLab Self-Managed.
- Save authentication credentials using [profiles](/gitkraken-desktop/profiles/).
- Clone from your GitLab Self-Managed repository list.
- Add and manage remotes for GitLab Self-Managed.
- Create and view pull requests.
- Manage [GitLab Self-Managed Issues](/integrations/gitlab-self-managed-issues/).

***

## How to authenticate with GitLab Self-Managed

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken supports any version of GitLab Self-Managed released within the past year.</p>
</div>

<div class='callout callout--basic'>
  <p><strong>Use GitLab Self-Managed integration when:</strong> your repositories live on a self-hosted GitLab server and you need PAT-based access. <strong>Don't use the GitLab.com page when:</strong> your environment requires self-managed host domains, self-hosted auth, or server-version compatibility checks.</p>
</div>

To authenticate:

1. Navigate to <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> in the upper-right corner.

<figure>
  <img src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Open Preferences to access Integrations</figcaption>
</figure>

2. Choose **Gitlab Self-Managed**. Enter your GitLab Self-Managed host domain. Click <button class='button button--success button--ui button--nolink'>Generate a token on GitLab</button> and follow the link.

<figure>
  <img src="/wp-content/uploads/connect-gitlab-self-managed-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Connect to GitLab Self-Managed</figcaption>
</figure>

4. In your browser, log in and generate a token. Required scopes: `api` and `read_user`. Leave expiration blank.

<figure>
  <img src="/wp-content/uploads/access-token-gitlab-self-managed@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Create a personal access token for GitLab</figcaption>
</figure>

5. Copy and paste the token into GitKraken, then click <button class='button button--success button--ui button--nolink'>Connect</button>.

<figure>
  <img src="/wp-content/uploads/connect-gitlab-self-managed-PAT-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Token successfully connected in GitKraken</figcaption>
</figure>

***

## How to generate an SSH key for GitLab Self-Managed

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken uses the SSH key from <kbd>Preferences > SSH</kbd> unless overridden with a GitLab-specific key or a system SSH Agent.</p>
</div>

1. Open <kbd>Preferences > Integrations</kbd>.
2. Click <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitLab</button>.

<figure>
  <img src="/wp-content/uploads/add-key-gitlab-self-managed-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Generate and upload SSH key to GitLab Self-Managed</figcaption>
</figure>

You can also:

- Use <button class='button button--uiorange button--ui button--nolink'>Add key to GitLab</button> for an existing SSH Default.
- Use _Add existing SSH key_ to upload a saved key manually.

***

## How to connect multiple GitLab Self-Managed accounts

GitKraken supports one GitLab Self-Managed account per profile. Use multiple [profiles](/start-here/profiles) with GitKraken Pro to manage separate accounts.

<div class='callout callout--basic'>
  <p><strong>Use multiple profiles when:</strong> you need to switch between separate GitLab Self-Managed servers or identities. <strong>Don't use multiple profiles when:</strong> one self-hosted account already covers the repositories you need to manage.</p>
</div>
