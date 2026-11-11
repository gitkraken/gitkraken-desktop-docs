---
title: Azure DevOps Integration with GitKraken Desktop
description: Connect GitKraken Desktop to Azure DevOps to manage repositories, SSH keys, and pull requests using OAuth or Personal Access Tokens.
product: GitKraken Desktop
feature: Azure DevOps Integration
content_type: how-to
audience: developer
plan_required: Pro
os_support: [Windows, macOS, Linux]
git_hosts: [Azure DevOps]
integrations: [Azure DevOps]
hosted_variant: cloud
status: GA
last_verified: 2026-11
llms_include: true
tags: [azure-devops, integration, oauth, pat, ssh]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "integrations-with-git-providers"
    nav_label: "Azure DevOps"
    nav_order: 70
    nav_parent: "integrations-with-git-providers"
    page_type: "content"
    card_icon: "brand-azure"
    card_color: "blue"
    card_description: "Connect Azure DevOps with OAuth or a personal access token"
---
<kbd>Last updated: November 2026</kbd>

Use this page to connect GitKraken Desktop to Azure DevOps for repository access, pull request work, and SSH setup by using OAuth or a personal access token. The integration requires a Pro subscription or higher, and PAT authentication is the fallback when an Azure DevOps organization blocks third-party OAuth access.

**Requirements and limits**
- Integration covered here: Azure DevOps
- Plan: Pro subscription tier or higher
- Authentication options: OAuth or Personal Access Token (PAT)
- OAuth constraint: If the Azure DevOps organization disables third-party OAuth access, use a PAT instead
- Account limit: 1 Azure DevOps account per profile; multiple profiles require a paid Pro, Teams, or Enterprise plan
- SSH behavior: GitKraken Desktop uses the key in <kbd>Preferences &gt; SSH</kbd> unless you configure a service-specific key or system SSH Agent

| Method | When to use | Requires | Limitation |
|--------|-------------|----------|------------|
| OAuth | Standard Azure DevOps browser-based connection | Pro subscription and third-party OAuth access | Not available if the organization blocks third-party OAuth |
| Personal Access Token | OAuth is blocked or policy requires token-based access | Pro subscription, host domain, PAT | Manual token generation and paste flow |
| SSH key setup | You want SSH-based Git operations after connecting | Existing integration connection and SSH key upload | Uses GitKraken SSH settings unless overridden |

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> in GitKraken Desktop.
2. Select **Azure DevOps** and click **Connect to Azure DevOps**.
3. Finish connecting in your browser at gitkraken.dev. If asked, log in with your Azure DevOps credentials.
4. If your Azure DevOps account has more than 1 organization, choose one from the **Azure Organization** list on the Azure DevOps card.

You must be signed in to your GitKraken account to connect with OAuth. The connection belongs to your GitKraken account, so you can also use it on your other computers and profiles. See [How integrations connect through your GitKraken account](/gitkraken-desktop/integrations/#how-integrations-connect-through-your-gitkraken-account).

If OAuth is not available, for example because your organization has disabled third-party access, use a Personal Access Token (PAT) instead:
1. In <kbd>Preferences > Integrations</kbd>, enter your host domain.
2. Click **Generate a token on Azure DevOps** to open the token creation page.
3. Copy the token and paste it into GitKraken Desktop, then click **Connect**.

After connecting, GitKraken Desktop can browse your Azure DevOps repositories when cloning, display fork options when adding remotes, and show pull request details. To use SSH, go to <kbd>Preferences > Integrations</kbd>, click **Generate SSH key and copy to clipboard**, and add it to your Azure DevOps SSH settings.

### What the Azure DevOps integration lets you do

- Create new repositories on your Azure DevOps account with optional .gitignore and license files.
- Generate an SSH key and copy it to your clipboard for Azure DevOps.
- Clone directly from your Azure DevOps repository list.
- Identify Azure DevOps repositories by remote avatars on the Commit Graph.
- Add remotes for Azure DevOps repositories.
- Create and view pull requests, and add reviewers.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> The Azure DevOps integration requires a <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">Pro subscription</a> tier or higher.</p>
</div>

***

## How to authenticate with Azure DevOps

<div class='callout callout--basic'>
  <p><strong>Use OAuth when:</strong> your Azure DevOps organization allows third-party application access and you want the simplest browser-based setup. <strong>Use a PAT when:</strong> OAuth is blocked by policy or you need token-based access that matches your organization's security controls.</p>
</div>

To authenticate with Azure DevOps:

1. Open <kbd><i class="fas fa-cog"></i> Preferences > Integrations</kbd> in the top-right corner.

<figure>
  <img alt="Accessing integrations via Preferences" src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Accessing integrations via Preferences</figcaption>
</figure>

2. Choose **Azure DevOps** and click <button class='button button--success button--ui button--nolink'>Connect to Azure DevOps</button>.

<figure>
  <img alt="Preferences > Integrations > Azure DevOps in GitKraken Desktop: the Azure DevOps card reads Not Connected with a Connect to Azure DevOps button, a Manage Integrations button sits at the top right, and below &quot;or&quot; are Host Domain and Personal Access Token fields with a Connect button." src="/wp-content/uploads/connect-azure-devops-2025-v3@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Connecting to Azure DevOps from GitKraken</figcaption>
</figure>

3. Finish connecting in your browser at gitkraken.dev. If asked, log in with your Azure DevOps credentials.
4. If your Azure DevOps account has more than 1 organization, the card reads **Select an organization to finish connecting Azure DevOps**. Choose your organization from the **Azure Organization** list.

<figure>
  <img alt="Select your Azure DevOps organization" src="/wp-content/uploads/select-azure-organization-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Select your Azure DevOps organization</figcaption>
</figure>

### How to choose an organization after you sign in

If Azure DevOps is linked to your GitKraken account, GitKraken Desktop can connect it when you sign in. When your Azure DevOps account has more than 1 organization, GitKraken Desktop shows **Choose an Azure DevOps organization**, either as a step during setup or in a window after you sign in again. With 1 organization, GitKraken Desktop selects it for you.

1. Select an organization from the list.
2. Click **Continue**.

To decide later, click **Skip this step**. Azure DevOps stays partly connected until you choose an organization in <kbd>Preferences > Integrations > Azure DevOps</kbd>. You can change the organization there at any time.

You can also connect using a Personal Access Token (PAT):

1. Enter your host domain and click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Generate a token on Azure DevOps</span></button>.

<figure>
  <img alt="Generate a Personal Access Token (PAT)" src="/wp-content/uploads/generate-token-azure-devops-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Generate a Personal Access Token (PAT)</figcaption>
</figure>

2. Log in to Azure DevOps and generate a token.

<figure>
  <img alt="Define scopes for your PAT" src="/wp-content/uploads/azure-PAT-scopes-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Define scopes for your PAT</figcaption>
</figure>

3. Copy the token and paste it into GitKraken Desktop, then click <button class='button button--success button--ui button--nolink'>Connect</button>. Azure DevOps shows the token only once.

<figure>
  <img alt="PAT added and connected in GitKraken" src="/wp-content/uploads/PAT-azure-added-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">PAT added and connected in GitKraken</figcaption>
</figure>

## How to generate an SSH key for Azure DevOps

GitKraken Desktop uses your default SSH configuration from <kbd>Preferences > SSH</kbd> unless you configure a specific key for Azure DevOps or enable your system SSH agent.

After you connect, generate a new SSH key:

<figure>
  <img alt="Generate and copy your SSH key for Azure DevOps" src="/wp-content/uploads/gkc-ssh-azure-devops@2x.png" class="img-responsive center img-bordered">
  <figcaption style="color:#888; text-align:center">Generate and copy your SSH key for Azure DevOps</figcaption>
</figure>

1. Click <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</button>.
2. Paste the key into your Azure DevOps SSH settings.

***

## What Azure DevOps OAuth enables in GitKraken Desktop

<div class='callout callout--basic'>
  <p><strong>Use the Azure DevOps integration when:</strong> you want repository discovery, remotes, and pull request workflows directly in GitKraken Desktop. <strong>Do not rely on it alone when:</strong> your Azure DevOps setup requires organization-specific workflows outside the features surfaced here.</p>
</div>

When you are authenticated, GitKraken Desktop lets you:

- Browse your Azure DevOps repositories while cloning:

<figure>
  <img alt="Browse Azure DevOps repos during cloning" src="/wp-content/uploads/gkc-azure-integration-clone@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Browse Azure DevOps repos during cloning</figcaption>
</figure>

- View fork options when adding remotes:

<figure>
  <img alt="Fork options displayed when adding remotes" src="/wp-content/uploads/gkc-azure-add-remote@2x.png" class="help-center-img img-bordered">
  <figcaption style="color:#888; text-align:center">Fork options displayed when adding remotes</figcaption>
</figure>

You can still enter a remote URL manually.

***

## How to connect multiple Azure DevOps accounts

GitKraken Desktop supports 1 Azure DevOps account per profile. With a paid Pro, Teams, or Enterprise plan, use multiple [profiles](/start-here/profiles) to switch between accounts.

<div class='callout callout--basic'>
  <p><strong>Use multiple profiles when:</strong> you need to switch cleanly between separate Azure DevOps identities or organizations. <strong>Do not use multiple profiles when:</strong> one account already covers the repos you need and profile switching would only add overhead.</p>
</div>

***

## How to enable Azure DevOps OAuth for GitKraken Desktop

To connect via OAuth, Azure DevOps must allow third-party applications:

<figure style="text-align:center;">
  <img alt="OAuth access error message in GitKraken" class="img-bordered center aligncenter" decoding="async" src="/wp-content/uploads/gkd-ado-oauth-error.png" class="img-bordered" style="display:inline-block;">
  <figcaption style="color:#888; text-align:center">OAuth access error message in GitKraken</figcaption>
</figure>

1. In Azure DevOps, go to <kbd>Organization Settings > Policies</kbd>.
2. Enable <strong>Third-party application access via OAuth</strong>.

For details, see the Microsoft documentation: [Change application connection & security policies for your organization](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).

If you cannot enable this setting, connect using a Personal Access Token (PAT) instead.

***

## Azure DevOps troubleshooting

Use these fixes when an Azure DevOps feature does not appear as expected.

### How to fix a missing Azure DevOps pull request form

If your Azure DevOps pull request does not appear in GitKraken Desktop:

1. In the Left Panel, right-click the remote (typically `origin`) and select <kbd>Edit</kbd>.
2. Make sure the URL uses the format `dev.azure.com/[organization]` and matches the domain of your integration:
   - If you use a PAT, the URL must match the Host Domain URL in <kbd>Preferences > Integrations</kbd>.
   - If you use OAuth, the URL must match the connected domain.
3. Do not use the deprecated VSTS format, `[organization].visualstudio.com`.
4. Click <kbd>Edit Remote</kbd> to save changes.
