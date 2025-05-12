---
title: Azure DevOps Integration
description: Integrate GitKraken with your Azure DevOps (formerly VSTS) repository by following these steps.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

GitKraken allows you to connect to Azure DevOps (formerly VSTS), which will help you find repos on Azure DevOps when cloning.

**Benefits**

* Create repositories on Azure DevOps account including .gitignore and license
* Automatically generate an SSH key pair and copy it to Azure DevOps
* Clone from Azure DevOps repo list
* Identify Azure DevOps repos with remote avatars on the Commit Graph
* Add remotes for Azure DevOps repos
* Create and view Pull Requests, including the option to add Reviewers

<div class='callout callout--warning'>
    <p>The Azure DevOps integration requires a <a href="https://www.gitkraken.com/pricing" target="_blank">Pro subscription</a> tier or higher.</p>
</div>

***

## Azure DevOps Authentication

To authenticate with Azure DevOps, navigate to the upper right corner to access <kbd><i> <i class="fas fa-cog"></i> Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>

<img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">

Or alternatively if you are in the <kbd>New Tab</kbd> view, click on <kbd>See all the integrations</kbd> under <strong><i class="fa-solid fa-plug"></i> Integrations</strong>.

<img src="/wp-content/uploads/see-all-integrations-2025.png" srcset="/wp-content/uploads/see-all-integrations-2025@2x.png" class="help-center-img img-bordered">

From the Integrations window, select **Azure DevOps** and then hit the <button class='button button--success button--ui button--nolink'>Connect to Azure DevOps</button> button.

<img src="/wp-content/uploads/connect-azure-devops-2025.png" srcset="/wp-content/uploads/connect-azure-devops-2025@2x.png" class="help-center-img img-bordered">

This opens a web browser where you first log in with your Azure DevOps credentials to allow GitKraken access.

Upon login, a success message appears. Finish connecting by selecting `Open GitKraken`. Then, select the organization from your Azure DevOps account.

<img src="/wp-content/uploads/select-azure-organization-2025.png" srcset="/wp-content/uploads/select-azure-organization-2025@2x.png" class="help-center-img img-bordered">

You can connect using a Password Access Token too. Enter your _Host Domain_ then click the <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Generate a token on Azure DevOps</span></button>

<img src="/wp-content/uploads/generate-token-azure-devops-2025.png" srcset="/wp-content/uploads/generate-token-azure-devops-2025@2x.png" class="help-center-img img-bordered">

This opens a web browser where you next log in with your Azure DevOps credentials and generate an access token.

<img src="/wp-content/uploads/azure-PAT-scopes-2025.png" srcset="/wp-content/uploads/azure-PAT-scopes-2025@2x.png" class="help-center-img img-bordered">


Copy your token to the clipboard as this is the only time you will see this token.  Paste the token into GitKraken and click on <button class='button button--success button--ui button--nolink'>Connect</button>.

<img src="/wp-content/uploads/PAT-azure-added-2025.png" srcset="/wp-content/uploads/PAT-azure-added-2025@2x.png" class="help-center-img img-bordered">

### Generating an SSH Key for Azure DevOps
GitKraken uses your local SSH Config from _SSH Defaults_ to fetch and push unless you set up a Azure DevOps-specific SSH key, or enable your local SSH Agent.

Once your Azure DevOps account has been connected to GitKraken, you may easily generate an SSH key and add it to your Azure DevOps account from <kbd><i>Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>.

Click the magic <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</button> button and add the key to your Azure DevOps account.

<img src="/wp-content/uploads/gkc-ssh-azure-devops.png" srcset="/wp-content/uploads/gkc-ssh-azure-devops@2x.png" class="img-responsive center img-bordered">

***
## OAuth integration with Azure DevOps
GitKraken's integration with Azure DevOps provides handy information about your repositories.

First, you may search through your existing repositories when cloning:

<img src="/wp-content/uploads/gkc-azure-integration-clone.png" srcset="/wp-content/uploads/gkc-azure-integration-clone@2x.png" class="help-center-img img-bordered">

Next, GitKraken presents a list of forks of the current repository when adding remotes:

<img src="/wp-content/uploads/gkc-azure-add-remote.png" srcset="/wp-content/uploads/gkc-azure-add-remote@2x.png" class="help-center-img img-bordered">

Of course, you still have the option of manually entering repo URLs.

***

## Connecting to multiple Azure DevOps accounts

GitKraken connects to one Azure DevOps account at a time. However, with a paid GitKraken Pro/Teams/Enterprise plan, you can easily switch between multiple <a href="/start-here/profiles">profiles</a> that each have their own associated Azure DevOps accounts.

***

## Requirement for connecting to Azure DevOps using OAuth

<img src="/wp-content/uploads/gkd-ado-oauth-error.png" class="img-bordered center" style="display: block; margin-left: auto; margin-right: auto;" />

In order connect the Azure Devops integrations using OAuth, `Third-party application access via OAuth` will need to be enabled in Azure from `Organization Settings > Policies`. You can find more information on this setting on [Microsoft's Learn Resources](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

If enabling this setting is not possible, you can connect using a Password Access Token.
