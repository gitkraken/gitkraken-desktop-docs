---
title: GitLab Integration with GitKraken Desktop
description: Connect GitKraken Desktop with GitLab to clone repositories, manage SSH keys, create pull requests, and streamline development with OAuth.
product: GitKraken Desktop
feature: GitLab Integration
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitLab]
integrations: [GitLab]
hosted_variant: cloud
status: GA
last_verified: 2026-11
llms_include: true
tags: [gitlab, integration, oauth, ssh, pull-requests]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-integrations-with-git-providers"
    nav_label: "GitLab"
    nav_order: 30
    nav_parent: "desktop-integrations-with-git-providers"
    page_type: "content"
    card_icon: "brand-gitlab"
    card_color: "blue"
    card_description: "Clone repositories, manage SSH keys and create pull requests with GitLab.com"
---
<kbd>Last updated: November 2026</kbd>

Use this page to connect GitKraken Desktop to GitLab.com for repository access, SSH setup, clone and remote workflows, and pull request activity. On the Community plan, GitLab access is limited to public repositories, and you use profiles to work with more than 1 GitLab account.

**Requirements and limits**
- Integration covered here: GitLab.com
- Community plan limit: Public repositories only
- Authentication: Browser-based GitLab connection through your GitKraken account (sign in to GitKraken Desktop first)
- Account limit: 1 GitLab account per profile; multiple accounts require multiple profiles and a GitKraken Pro subscription
- SSH behavior: GitKraken Desktop uses the key in <kbd>Preferences &gt; SSH</kbd> unless you configure a GitLab-specific key or enable your local SSH Agent

| Workflow | Supported | Community limit | Notes |
|----------|-----------|-----------------|-------|
| Connect GitLab.com account | Yes | None | Browser-based connection through your GitKraken account |
| Clone and browse repositories | Yes | Public repositories only | Private repository access requires a paid plan |
| SSH key generation and upload | Yes | Public repositories only | Uses GitKraken SSH settings unless overridden |
| Create and manage pull requests | Yes | Public repositories only | Supported directly in GitKraken Desktop |
| Multiple GitLab accounts | Yes | Not included | Requires separate profiles and a Pro plan |

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Select **GitLab** and click **Connect to GitLab**. If you are signed out of your GitKraken account, sign in first.
3. Finish connecting in your browser at gitkraken.dev. If asked, log in to GitLab.

To configure SSH access after connecting, do one of the following in <kbd>Preferences > Integrations</kbd>:
- Click **Generate SSH key and add to GitLab** to generate and upload a key automatically.
- Click **Add key to GitLab** to upload your existing default SSH key.

After you connect, GitKraken Desktop shows your GitLab repositories when you clone, shows forks when you add remotes, and lets you create and manage pull requests. To manage more than one GitLab account, use multiple [profiles](/start-here/profiles) with a GitKraken Pro plan.

### What the GitLab integration lets you do

- Create new repositories on your GitLab account with optional .gitignore and license templates.
- Automatically generate and upload an SSH key pair to GitLab.
- Clone repositories directly from your GitLab repo list.
- Identify GitLab repositories by remote avatars on the Commit Graph.
- Add remotes to GitLab repositories.
- Create and manage pull requests in GitKraken Desktop.
- Work with [GitLab Issues](/integrations/gitlab-issues/) alongside your code.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> The <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">GitKraken Community plan</a> only supports public repositories.</p>
</div>

***

## How to connect the GitLab integration

<div class='callout callout--basic'>
  <p><strong>Before you start:</strong> sign in to your GitKraken account. GitLab connects through your GitKraken account, so you can also use the connection on your other computers and profiles. See <a href="/gitkraken-desktop/integrations/#how-integrations-connect-through-your-gitkraken-account">How integrations connect through your GitKraken account</a>.</p>
</div>

To authenticate with GitLab:

1. Open <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> from the upper-right corner.

<figure>
  <img alt="Access GitLab integration from Preferences" src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Access GitLab integration from Preferences</figcaption>
</figure>

2. Select **GitLab** and click <button class='button button--success button--ui button--nolink'>Connect to GitLab</button>.

<figure>
  <img alt="Preferences > Integrations > GitLab in GitKraken Desktop: the GitLab card reads Not Connected with a Connect to GitLab button, and a Manage Integrations button sits at the top right of the pane." src="/wp-content/uploads/connect-gitlab-2025-v3@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Click to authenticate GitLab account</figcaption>
</figure>

3. Your default browser opens gitkraken.dev. Log in to GitLab if asked, then follow the prompts to return to GitKraken Desktop. The GitLab card then reads **Connected to your GitLab integration**.

<figure>
  <img alt="Sign in to GitLab" src="/wp-content/uploads/gitlab-sign-in-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Sign in to GitLab</figcaption>
</figure>

<figure>
  <img alt="Authentication successful — return to GitKraken" src="/wp-content/uploads/auth-success-gitlab-1@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Authentication successful — return to GitKraken</figcaption>
</figure>

## How to generate an SSH key for GitLab

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken Desktop uses the SSH key listed in <kbd>Preferences > SSH</kbd> unless you configure a GitLab-specific key or enable your local SSH Agent.</p>
</div>

After you connect GitLab, generate a new SSH key or upload an existing one:

<figure>
  <img alt="Options to add an SSH key to GitLab" src="/wp-content/uploads/add-key-to-gitlab-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Options to add an SSH key to GitLab</figcaption>
</figure>

- Click <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitLab</button> to generate a key and add it to GitLab.
- Click <button class='button button--uiorange button--ui button--nolink'>Add key to GitLab</button> to add your existing default SSH key.
- Click **Add existing SSH key** to upload your own key manually.

***

## What GitLab OAuth enables in GitKraken Desktop

<div class='callout callout--basic'>
  <p><strong>Use the GitLab integration when:</strong> you want cloning, remotes, pull requests, and issue workflows tied directly to GitLab.com inside GitKraken Desktop. <strong>For self-managed GitLab:</strong> see <a href="/gitkraken-desktop/gitlab-self-hosted/">GitLab Self-Managed</a>.</p>
</div>

With GitLab connected, you can:

- Browse your GitLab repositories while cloning:

<figure>
  <img alt="Browse GitLab repositories while cloning" src="/wp-content/uploads/clone-gitlab@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Browse GitLab repositories while cloning</figcaption>
</figure>

- View forks when adding remotes:

<figure>
  <img alt="Forks shown when adding GitLab remotes" src="/wp-content/uploads/remote-gitlab@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Forks shown when adding GitLab remotes</figcaption>
</figure>

You can still enter repository URLs manually.

***

## How to connect multiple GitLab accounts

GitKraken Desktop supports 1 GitLab account per profile. With [profiles](/start-here/profiles) in GitKraken Pro, you can switch between multiple GitLab accounts.

<div class='callout callout--basic'>
  <p><strong>Use multiple profiles when:</strong> you need to switch between separate GitLab identities or organizations cleanly. <strong>Do not use multiple profiles when:</strong> one GitLab account already covers the repositories you need and profile switching would add unnecessary overhead.</p>
</div>
