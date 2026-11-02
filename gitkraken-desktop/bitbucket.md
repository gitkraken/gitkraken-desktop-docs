---
title: Bitbucket Integration with GitKraken Desktop
description: Connect GitKraken Desktop with Bitbucket to clone repositories, manage pull requests, and configure SSH authentication.
product: GitKraken Desktop
feature: Bitbucket Integration
content_type: how-to
audience: developer
plan_required: Pro
os_support: [Windows, macOS, Linux]
git_hosts: [Bitbucket]
integrations: [Bitbucket]
hosted_variant: cloud
status: GA
last_verified: 2026-11
llms_include: true
tags: [bitbucket, integration, oauth, ssh, pull-requests]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to connect GitKraken Desktop to Bitbucket.org for repository discovery, SSH setup, clone and remote workflows, and pull request activity. To use more than 1 Bitbucket account, you use profiles, and you see pull request reviewers only with the right repository permissions.

**Requirements and limits**
- Integration covered here: Bitbucket.org
- Authentication: Browser-based Bitbucket connection through your GitKraken account (sign in to GitKraken Desktop first)
- Account limit: 1 Bitbucket account per profile; multiple accounts require multiple profiles and a GitKraken Pro subscription
- SSH behavior: GitKraken Desktop uses the key in <kbd>Preferences &gt; SSH</kbd> unless you configure a Bitbucket-specific key or use your system SSH Agent
- Reviewers: Pull request reviewer visibility depends on having Project Admin permissions on the repository

| Workflow | Supported | Notes |
|----------|-----------|-------|
| Connect Bitbucket account | Yes | Browser-based connection through your GitKraken account |
| Clone and browse repositories | Yes | Uses the integrated repository list |
| SSH key generation and upload | Yes | Uses GitKraken SSH settings unless overridden |
| Create and view pull requests | Yes | Supported directly in GitKraken Desktop |
| Add reviewers to pull requests | Partial | Reviewer visibility depends on Project Admin permissions |
| Multiple Bitbucket accounts | Yes | Requires separate profiles and a Pro subscription |

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Select **Bitbucket** and click **Connect to Bitbucket**. If you are signed out of your GitKraken account, sign in first.
3. Finish connecting in your browser at gitkraken.dev. If asked, log in to Bitbucket.

To configure SSH access after connecting:
1. In <kbd>Preferences > Integrations</kbd>, click **Generate SSH key and copy to clipboard**.
2. Paste the key into your Bitbucket account SSH settings.

After you connect, GitKraken Desktop shows your Bitbucket repositories when you clone, lists forks when you add remotes, and lets you create and view pull requests. To manage more than 1 Bitbucket account, use multiple [profiles](/gitkraken-desktop/profiles/) with a GitKraken Pro plan.

### What the Bitbucket integration lets you do

- Create new repositories on your Bitbucket account with .gitignore and license templates.
- Generate and copy an SSH key pair for Bitbucket.
- Save authentication in reusable [profiles](/gitkraken-desktop/profiles/).
- Clone from a personalized Bitbucket repository list.
- Add and manage remotes from Bitbucket.
- Create and view pull requests in GitKraken Desktop.

<div class='embed-container embed-container--16-9'>
  <iframe width='560' height='315' src='https://www.youtube.com/embed/sQ4ouJpAeR8?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## How to connect Bitbucket

<div class='callout callout--basic'>
  <p><strong>Before you start:</strong> sign in to your GitKraken account. Bitbucket connects through your GitKraken account, so you can also use the connection on your other computers and profiles. See <a href="/gitkraken-desktop/integrations/#how-integrations-connect-through-your-gitkraken-account">How integrations connect through your GitKraken account</a>.</p>
</div>

To authenticate with Bitbucket:

1. Go to <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> in the upper-right corner.

<figure>
  <img alt="Open Preferences to configure integrations" src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Open Preferences to configure integrations</figcaption>
</figure>

2. Select <strong>Bitbucket</strong> and click <button class='button button--success button--ui button--nolink'>Connect to Bitbucket</button>.

<figure>
  <img alt="Preferences > Integrations > Bitbucket in GitKraken Desktop: the Bitbucket card reads Not Connected with a Connect to Bitbucket button, and a Manage Integrations button sits at the top right of the pane." src="/wp-content/uploads/connect-bitbucket-2025-v2@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Click to authenticate via Bitbucket</figcaption>
</figure>

3. Your default browser opens gitkraken.dev. Log in to Bitbucket if asked, then follow the prompts to return to GitKraken Desktop. The Bitbucket card then reads **Connected to your Bitbucket integration**.

<figure>
  <img alt="Login success prompt from Bitbucket" src="/wp-content/uploads/bitbucket-success-1@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Login success prompt from Bitbucket</figcaption>
</figure>

***

## How to generate SSH keys for Bitbucket

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken Desktop uses your SSH key from <kbd>Preferences > SSH</kbd> unless you configure a Bitbucket-specific key or enable your system SSH Agent.</p>
</div>

After you connect Bitbucket:

1. Go to <kbd>Preferences > Integrations</kbd>.
2. Click <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</button>.
3. Paste the key into your Bitbucket account settings.

<figure>
  <img alt="Copy and add your new SSH key to Bitbucket" class="img-bordered center aligncenter" decoding="async" src='/wp-content/uploads/ssh-bitbucket-2025@2x.png' class="img-bordered" class="help-center" style="display:inline-block;">
  <figcaption style="color:#888; text-align:center">Copy and add your new SSH key to Bitbucket</figcaption>
</figure>

***

## What Bitbucket OAuth enables in GitKraken Desktop

<div class='callout callout--basic'>
  <p><strong>Use the Bitbucket integration when:</strong> you want repo discovery, remotes, and pull request workflows tied to Bitbucket.org inside GitKraken Desktop. <strong>For self-hosted Bitbucket:</strong> see <a href="/gitkraken-desktop/bitbucket-data-center/">Bitbucket Data Center</a>.</p>
</div>

With Bitbucket connected, GitKraken Desktop shows:

- A searchable list of Bitbucket repositories when cloning:

<figure>
  <img alt="Cloning from your Bitbucket repositories" src="/wp-content/uploads/clone@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Cloning from your Bitbucket repositories</figcaption>
</figure>

- A list of forks when adding remotes:

<figure>
  <img alt="Forks available for remote setup" src="/wp-content/uploads/remote@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Forks available for remote setup</figcaption>
</figure>

You can still enter repository URLs manually.

***

## How to connect multiple Bitbucket accounts

GitKraken Desktop supports 1 Bitbucket account per profile. With GitKraken Pro, use multiple [profiles](/start-here/profiles) to manage several Bitbucket identities.

<div class='callout callout--basic'>
  <p><strong>Use multiple profiles when:</strong> you need separate Bitbucket identities or workspaces in the same GitKraken Desktop install. <strong>Do not use multiple profiles when:</strong> one Bitbucket account already covers the repositories you work with.</p>
</div>

## How Bitbucket pull request reviewers work

Bitbucket supports pull request reviewers. If you have Project Admin permissions on the repository, GitKraken Desktop shows reviewer details.
