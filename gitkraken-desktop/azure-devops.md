---
title: Azure DevOps Integration with GitKraken Desktop
description: Connect GitKraken Desktop to Azure DevOps to manage repositories, SSH keys, and pull requests using OAuth or Personal Access Tokens.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

GitKraken lets you connect to Azure DevOps (formerly VSTS), making it easier to find and manage repositories when cloning, working with remotes, or handling pull requests.

### Benefits

- Create new repositories on your Azure DevOps account with optional .gitignore and license files.
- Automatically generate and copy an SSH key to Azure DevOps.
- Clone directly from your Azure DevOps repository list.
- Identify Azure DevOps repositories by remote avatars on the Commit Graph.
- Add remotes for Azure DevOps repositories.
- Create and view pull requests, including the ability to add reviewers.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> The Azure DevOps integration requires a <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">Pro subscription</a> tier or higher.</p>
</div>

***

## Azure DevOps Authentication

To authenticate with Azure DevOps:

1. Open <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> in the top-right corner.

<figure>
  <img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Accessing integrations via Preferences</figcaption>
</figure>

2. Choose **Azure DevOps** and click <button class='button button--success button--ui button--nolink'>Connect to Azure DevOps</button>.

<figure>
  <img src="/wp-content/uploads/connect-azure-devops-2025.png" srcset="/wp-content/uploads/connect-azure-devops-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Connecting to Azure DevOps from GitKraken</figcaption>
</figure>

4. In the browser window that opens, log in with your Azure DevOps credentials. Once successful, select <kbd>Open GitKraken</kbd> and choose your organization.

<figure>
  <img src="/wp-content/uploads/select-azure-organization-2025.png" srcset="/wp-content/uploads/select-azure-organization-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Select your Azure DevOps organization</figcaption>
</figure>

You can also connect using a Personal Access Token (PAT):

- Enter your host domain and click the <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Generate a token on Azure DevOps</span></button> button.

<figure>
  <img src="/wp-content/uploads/generate-token-azure-devops-2025.png" srcset="/wp-content/uploads/generate-token-azure-devops-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Generate a Personal Access Token (PAT)</figcaption>
</figure>

- Log in to Azure DevOps and generate a token.

<figure>
  <img src="/wp-content/uploads/azure-PAT-scopes-2025.png" srcset="/wp-content/uploads/azure-PAT-scopes-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Define scopes for your PAT</figcaption>
</figure>

- Copy the token (you’ll only see it once) and paste it into GitKraken, then click <button class='button button--success button--ui button--nolink'>Connect</button>.

<figure>
  <img src="/wp-content/uploads/PAT-azure-added-2025.png" srcset="/wp-content/uploads/PAT-azure-added-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">PAT added and connected in GitKraken</figcaption>
</figure>

## Generating an SSH Key for Azure DevOps

GitKraken uses your default SSH configuration from <kbd>Preferences > SSH</kbd> unless you configure a specific key for Azure DevOps or enable your system SSH agent.

Once connected, you can generate a new SSH key:

<figure>
  <img src="/wp-content/uploads/gkc-ssh-azure-devops.png" srcset="/wp-content/uploads/gkc-ssh-azure-devops@2x.png" class="img-responsive center img-bordered">
  <figcaption style="color:#888; text-align:center">Generate and copy your SSH key for Azure DevOps</figcaption>
</figure>

- Click <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</button>.
- Paste the key into your Azure DevOps SSH settings.

***

## OAuth Integration with Azure DevOps

When authenticated, GitKraken enables:

- Browsing your Azure DevOps repositories while cloning:

<figure>
  <img src="/wp-content/uploads/gkc-azure-integration-clone.png" srcset="/wp-content/uploads/gkc-azure-integration-clone@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Browse Azure DevOps repos during cloning</figcaption>
</figure>

- Viewing fork options when adding remotes:

<figure>
  <img src="/wp-content/uploads/gkc-azure-add-remote.png" srcset="/wp-content/uploads/gkc-azure-add-remote@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Fork options displayed when adding remotes</figcaption>
</figure>

Manual URL entry is still available.

***

## Connecting to Multiple Azure DevOps Accounts

GitKraken supports one Azure DevOps account per profile. With a paid Pro, Teams, or Enterprise plan, use multiple [profiles](/start-here/profiles) to switch between accounts.

***

## Requirement for Connecting to Azure DevOps Using OAuth

To connect via OAuth, Azure DevOps must allow third-party applications:

<figure style="text-align:center;">
  <img class="img-bordered center aligncenter" decoding="async" src="/wp-content/uploads/gkd-ado-oauth-error.png" class="img-bordered" style="display:inline-block;">
  <figcaption style="color:#888; text-align:center">OAuth access error message in GitKraken</figcaption>
</figure>

- Navigate to <kbd>Organization Settings > Policies</kbd> in Azure DevOps.
- Enable <strong>Third-party application access via OAuth</strong>.

For details, refer to Microsoft documentation: [Change application connection & security policies for your organization](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

If this setting cannot be enabled, you can connect using a Personal Access Token (PAT) instead.

***

## Troubleshooting

### Azure DevOps Pull Request Form Not Showing in GitKraken

If your Azure DevOps pull request does not appear in GitKraken:

1. In the Left Panel, right-click the remote (typically `origin`) and select <kbd>Edit</kbd>.
2. Make sure the URL matches the domain used for your integration:
   - If using a PAT: should match the Host Domain URL from <kbd>Preferences > Integrations</kbd>.
   - If using OAuth: should match the connected domain.
3. The correct format is: `dev.azure.com/[organization]`
4. Avoid using the deprecated VSTS format: `[organization].visualstudio.com`
5. Click <kbd>Edit Remote</kbd> to save changes.
