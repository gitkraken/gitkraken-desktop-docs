---
title: GitLab Integration with GitKraken Desktop
description: Connect GitKraken Desktop with GitLab to clone repositories, manage SSH keys, create pull requests, and streamline development with OAuth.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

GitKraken allows you to connect to [GitLab](https://gitlab.com), enabling streamlined access to your repositories for cloning, issue tracking, and pull request workflows.

### Benefits

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

## Connecting the GitLab integration

To authenticate with GitLab:

1. Open <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> from the upper-right corner.

<figure>
  <img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Access GitLab integration from Preferences</figcaption>
</figure>

2. In the integration window, select _GitLab.com_ and click <button class='button button--success button--ui button--nolink'>Connect to GitLab</button>.

<figure>
  <img src="/wp-content/uploads/connect-gitlab-2025.png" srcset="/wp-content/uploads/connect-gitlab-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Click to authenticate GitLab account</figcaption>
</figure>

4. Log in via your default browser. After successful authentication, click <kbd>Open GitKraken</kbd> to complete the connection.

<figure>
  <img src="/wp-content/uploads/gitlab-sign-in-2025.png" srcset="/wp-content/uploads/gitlab-sign-in-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Sign in to GitLab</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/auth-success-gitlab-1.png" srcset="/wp-content/uploads/auth-success-gitlab-1@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Authentication successful — return to GitKraken</figcaption>
</figure>

You may also connect manually using an OAuth token.

<figure>
  <img src="/wp-content/uploads/gitlab-oauth-token.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Enter an OAuth token to connect manually</figcaption>
</figure>

## Generating an SSH Key for GitLab

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken uses the SSH key listed in <kbd>Preferences > SSH</kbd> unless you configure a GitLab-specific key or enable your local SSH Agent.</p>
</div>

Once GitLab is connected, you can generate a new SSH key or upload an existing one:

<figure>
  <img src="/wp-content/uploads/add-key-to-gitlab-2025.png" srcset="/wp-content/uploads/add-key-to-gitlab-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Options to add an SSH key to GitLab</figcaption>
</figure>

- Click <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitLab</button> to automate the process.
- Use <button class='button button--uiorange button--ui button--nolink'>Add key to GitLab</button> to use an existing SSH Default.
- Use _Add existing SSH key_ to upload your own key manually.

***

## OAuth Integration with GitLab

With GitLab connected, GitKraken enhances your workflow with features such as:

- Browsing your GitLab repositories during cloning:

<figure>
  <img src="/wp-content/uploads/clone-gitlab.png" srcset="/wp-content/uploads/clone-gitlab@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Browse GitLab repositories while cloning</figcaption>
</figure>

- Viewing forks when adding remotes:

<figure>
  <img src="/wp-content/uploads/remote-gitlab.png" srcset="/wp-content/uploads/remote-gitlab@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Forks shown when adding GitLab remotes</figcaption>
</figure>

You can still manually enter repository URLs if preferred.

***

## Connecting to Multiple GitLab Accounts

GitKraken supports one GitLab account per profile. With [profile support](/start-here/profiles) in GitKraken Pro, you can switch between multiple GitLab accounts easily.
