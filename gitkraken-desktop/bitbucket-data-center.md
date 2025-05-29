---
title: Bitbucket Data Center Integration
description: Integrate GitKraken Desktop with your Bitbucket Data Center repository by following these steps.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

GitKraken Desktop allows you to connect to Bitbucket Data Center, so you can find repositories, manage remotes, and create pull requests from a self-hosted environment.

### Benefits

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

## Connecting to Bitbucket Data Center

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken Desktop supports Bitbucket Data Center versions released within the past year.</p>
</div>

To authenticate:

1. Go to <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd>.

<figure>
  <img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Open Preferences to access Integrations</figcaption>
</figure>

2. From the <kbd>New Tab</kbd>, click <kbd>See all the integrations</kbd>.

<figure>
  <img src="/wp-content/uploads/see-all-integrations-2025.png" srcset="/wp-content/uploads/see-all-integrations-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Open all available integrations from New Tab</figcaption>
</figure>

3. Choose **Bitbucket Data Center**. Enter your host domain and click <button class='button button--success button--ui button--nolink'>Generate a token on Bitbucket Data Center</button>. Ensure the token has appropriate permissions.

<figure>
  <img src="/wp-content/uploads/connecting-bb-data-center-2025.png" srcset="/wp-content/uploads/connecting-bb-data-center-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Start connection to Bitbucket Data Center</figcaption>
</figure>

4. In the browser, log in to your Bitbucket Data Center account and create the token.

<figure>
  <img src="/wp-content/uploads/BitbucketServerPAT.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Create a Personal Access Token in Bitbucket Data Center</figcaption>
</figure>

5. Paste the token into GitKraken and click <button class='button button--success button--ui button--nolink'>Connect</button>.

***

## Generating SSH Keys for Bitbucket Data Center

<div class='callout callout'>
  <p><strong>Note:</strong> GitKraken uses the key in <kbd>Preferences > SSH</kbd> unless you configure a Bitbucket-specific SSH key or use your system SSH Agent.</p>
</div>

1. Open <kbd>Preferences > Integrations</kbd>.
2. Click <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</button>.
3. Follow the in-app toast or manual instructions to add the key.

<figure>
  <img src="/wp-content/uploads/ssh-bb-data-center-2025.png" srcset="/wp-content/uploads/ssh-bb-data-center-2025@2x.png" class="help-center-img img-bordered">
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
  <img src="/wp-content/uploads/bitbucket-server-SSHkey-add.png" srcset="/wp-content/uploads/bitbucket-server-SSHkey-add@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">SSH key successfully added</figcaption>
</figure>

***

## OAuth Integration with Bitbucket Data Center

GitKraken allows you to:

- Search your repositories when cloning:

<figure>
  <img src="/wp-content/uploads/bb-data-center-clone.png" srcset="/wp-content/uploads/bb-data-center-clone@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Clone repositories from Bitbucket Data Center</figcaption>
</figure>

- View forks when adding remotes:

<figure>
  <img src="/wp-content/uploads/add-remote-bb-dc-2025.png" srcset="/wp-content/uploads/add-remote-bb-dc-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Remotes list includes repository forks</figcaption>
</figure>

Manual entry of repository URLs is also supported.

***

## Connecting to Multiple Bitbucket Data Center Accounts

GitKraken supports one Bitbucket Data Center account per profile. Use multiple [profiles](/start-here/profiles) with GitKraken Pro to switch between accounts.

## Bitbucket Data Center Pull Request Reviewers

If your token includes Project Admin and Repository Admin scopes, and you have the correct permissions, GitKraken will display reviewer details for pull requests.
