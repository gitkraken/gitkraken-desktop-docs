---
title: GitLab Self-Managed Integration with GitKraken Desktop
description: Connect GitKraken Desktop with your GitLab Self-Managed server to manage repositories, SSH keys, and pull requests using personal access tokens.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

<div class='embed-container embed-container--16-9'>
  <iframe width="560" height="315" src="https://www.youtube.com/embed/BhIX7fGSM8k?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

GitKraken allows you to connect to GitLab Self-Managed (CE or EE), enabling repository discovery, pull request creation, and SSH key management within your self-hosted GitLab environment.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> All self-hosted server integrations, including GitLab Self-Managed, require an <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">Advanced subscription</a> tier or higher.</p>
</div>

### Benefits

- Create new repositories with optional .gitignore and license files.
- Automatically generate an SSH key and upload it to GitLab Self-Managed.
- Save authentication credentials using [profiles](/gitkraken-desktop/profiles/).
- Clone from your GitLab Self-Managed repository list.
- Add and manage remotes for GitLab Self-Managed.
- Create and view pull requests.
- Manage [GitLab Self-Managed Issues](/integrations/gitlab-self-managed-issues/).

***

## GitLab Self-Managed Authentication

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken supports any version of GitLab Self-Managed released within the past year.</p>
</div>

To authenticate:

1. Navigate to <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> in the upper-right corner.

<figure>
  <img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Open Preferences to access Integrations</figcaption>
</figure>

2. Choose **Gitlab Self-Managed**. Enter your GitLab Self-Managed host domain. Click <button class='button button--success button--ui button--nolink'>Generate a token on GitLab</button> and follow the link.

<figure>
  <img src="/wp-content/uploads/connect-gitlab-self-managed-2025.png" srcset="/wp-content/uploads/connect-gitlab-self-managed-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Connect to GitLab Self-Managed</figcaption>
</figure>

4. In your browser, log in and generate a token. Required scopes: `api` and `read_user`. Leave expiration blank.

<figure>
  <img src="/wp-content/uploads/access-token-gitlab-self-managed.png" srcset="/wp-content/uploads/access-token-gitlab-self-managed@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Create a personal access token for GitLab</figcaption>
</figure>

5. Copy and paste the token into GitKraken, then click <button class='button button--success button--ui button--nolink'>Connect</button>.

<figure>
  <img src="/wp-content/uploads/connect-gitlab-self-managed-PAT-2025.png" srcset="/wp-content/uploads/connect-gitlab-self-managed-PAT-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Token successfully connected in GitKraken</figcaption>
</figure>

***

## Generating an SSH Key for GitLab Self-Managed

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken uses the SSH key from <kbd>Preferences > SSH</kbd> unless overridden with a GitLab-specific key or a system SSH Agent.</p>
</div>

1. Open <kbd>Preferences > Integrations</kbd>.
2. Click <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitLab</button>.

<figure>
  <img src="/wp-content/uploads/add-key-gitlab-self-managed-2025.png" srcset="/wp-content/uploads/add-key-gitlab-self-managed-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Generate and upload SSH key to GitLab Self-Managed</figcaption>
</figure>

You can also:

- Use <button class='button button--uiorange button--ui button--nolink'>Add key to GitLab</button> for an existing SSH Default.
- Use _Add existing SSH key_ to upload a saved key manually.

***

## Connecting to Multiple GitLab Self-Managed Accounts

GitKraken supports one GitLab Self-Managed account per profile. Use multiple [profiles](/start-here/profiles) with GitKraken Pro to manage separate accounts.