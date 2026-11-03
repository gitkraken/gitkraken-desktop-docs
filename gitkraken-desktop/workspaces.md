---
title: Workspaces in GitKraken Desktop
description: Learn how to create, manage, and share Cloud or Local Workspaces in GitKraken Desktop to organize and collaborate across repositories.
product: GitKraken Desktop
feature: Workspaces
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps]
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [workspaces, cloud-workspaces, local-workspaces, multi-repo, launchpad]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to create Local or Cloud Workspaces in GitKraken Desktop so you can organize repositories, run multi-repository actions, review pull requests across a group of repos, and share workspace context with a team. Cloud Workspaces require connected integrations, while Local Workspaces stay on your machine until you convert them.

**Requirements and limits**
- Workspace types: Local Workspace or Cloud Workspace
- Cloud Workspace requirement: The relevant hosting service integration must be connected in <kbd>Preferences &gt; Integrations</kbd>
- Local Workspace scope: Stored on your machine until you convert it
- Cloud Workspace scope: Accessible across machines and shareable with teams or users
- Multi-repository actions: Clone, Fetch, Pull, Open, Locate, and Remove are available from the Workspace toolbar
- Conversion path: Local Workspaces can be converted to Cloud Workspaces after connecting a supported integration

| Workspace type | Stored where | Shareable | Requires integration | Cross-device access |
|----------------|-------------|-----------|----------------------|---------------------|
| Local Workspace | On your machine | No | No | No |
| Cloud Workspace | In your GitKraken account and connected service context | Yes | Yes | Yes |

***

<div class='callout callout--warning'>
  <p><strong>GitKraken On-Premise users:</strong> Cloud Workspaces are not available in Serverless or Self-Hosted Server deployments. Use <a href="#how-local-workspaces-work">Local Workspaces</a> to organize repositories in those environments. Features that depend on Cloud Workspaces, including Workspace Insights and Launchpad Team View, are also not available.</p>
</div>

## Quick Start


**To open the Workspaces view:** Click the **Repo Management** folder icon in the tab bar, or press <kbd>Ctrl + Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + Option + O</kbd> (Mac).

**To create a Cloud Workspace:**
1. Click **+ New Workspace** and select **Cloud Workspace**.
2. Name the Workspace, select a hosting service, and choose repositories.
3. Optionally share with teams or users and add an icon and description.

**To create a Local Workspace:** Click **New Workspace**, select **Local Workspace**, name it, and browse to select repositories or a directory.

**To act across multiple repositories:** Select the checkboxes next to repositories, then use the toolbar to Fetch, Pull, Clone, Open, or Remove them in bulk.

**To view pull requests for all repos:** Open a Cloud Workspace and click the Launchpad icon to see PRs across the entire Workspace.

**To convert a Local Workspace to Cloud:** Open the Workspace and click **Create Cloud Workspace**. You need a connected integration in <kbd>Preferences > Integrations</kbd>.

Workspaces are in the Repo Management tab.

<figure>
  <img src="/wp-content/uploads/workspaces-tab-2025@2x.png"
       class="help-center-img img-bordered"
       alt="GitKraken Desktop showing multiple cloud Workspaces, each grouping related repositories with options to clone, locate, or manage them.">
  <figcaption style="color:#888; text-align:center">
    Group your repos into a Workspace
  </figcaption>
</figure>

***

## How to access your Workspaces

To open the Repo Management tab, do one of the following:

- Click the **Repo Management** folder icon in the tab bar.
- Press <kbd>Ctrl + Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + Option + O</kbd> (Mac).

<figure>
  <img src="/wp-content/uploads/open-workspaces-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface highlighting the folder icon used to access Workspaces from the Repo Management tab.">
  <figcaption style="color:#888; text-align:center">
    Opening Workspaces from the Repo Management tab
  </figcaption>
</figure>

***

## How Cloud Workspaces work

Cloud Workspaces are available from any machine, and you can share them with selected [teams](/start-here/teams/) in your organization. Use them to run [multi-repository actions](#how-to-run-multi-repository-actions-in-a-cloud-workspace) and manage pull requests for all their repositories in one place.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> Cloud Workspaces are not available in GitKraken On-Premise Serverless or Self-Hosted Server deployments. See <a href="#how-local-workspaces-work">How Local Workspaces work</a> for the supported alternative in those environments.</p>
</div>

<div class='callout callout--basic'>
    <p><strong>Use a Cloud Workspace when:</strong> you need to share repository groups across machines or with teammates. <strong>Do not use a Cloud Workspace when:</strong> the repo list is only for your local machine and does not need shared or synced workspace context.</p>
</div>

<p>Watch the overview:</p>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OIQVsNRqg1M?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

### How to create a Cloud Workspace

1. Click <button class="button button--success button--ui button--nolink">+ New Workspace</button>.
2. Select **Cloud Workspace**.
3. Name your Workspace and select the hosting service.
4. Choose repositories to add.
5. (Optional) Add an icon and description, and share the Workspace with teams or users.

<figure>
  <img src="/wp-content/uploads/add-new-workspace-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Highlighted 'New Workspace' button in the Repository Management view of GitKraken Desktop.">
  <figcaption style="color:#888; text-align:center">
    Add a new Cloud Workspace
  </figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/config-cloud-workspace-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Cloud Workspace creation form in GitKraken Desktop, showing workspace name, color selection, provider, and repository fields.">
  <figcaption style="color:#888; text-align:center">
    Configuring Cloud Workspace settings
  </figcaption>
</figure>

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        Connect the hosting service's integration in <kbd>Preferences > Integrations</kbd> first.
    </p>
</div>

### How to run multi-repository actions in a Cloud Workspace

To take action across multiple repositories:

1. Select the checkboxes next to the desired repositories.
2. Choose an action from the toolbar at the top.

<figure>
  <img src="/wp-content/uploads/multi-fetch-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing multiple selected repositories in a workspace and the 'Fetch 3 repositories' button highlighted.">
  <figcaption style="color:#888; text-align:center">Multi-repo fetch operation</figcaption>
</figure>

Find more actions in the ellipsis menu.

<figure>
  <img src="/wp-content/uploads/more-multi-repo-actions-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop showing a dropdown menu with bulk workspace options, including Select All, Open repositories, and Remove repositories.">
  <figcaption style="color:#888; text-align:center">Accessing more multi-repo actions</figcaption>
</figure>

These multi-repository actions are available:

<table style="font-size: 14px; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="text-align: left; padding: 4px;">Action</th>
      <th style="text-align: left; padding: 4px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 4px;"><strong>Clone</strong> <img alt="" src="/wp-content/uploads/gk-remote-icon.svg" style="height:1em;"></td>
      <td style="padding: 4px;">Clone all selected repositories. GitKraken Desktop uses HTTPS unless <a href="https://help.gitkraken.com/gitkraken-desktop/integrations/">SSH is configured in your settings</a>. Only available if repositories are not already cloned.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Fetch</strong></td>
      <td style="padding: 4px;">Fetch all selected repositories.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Pull</strong> <img alt="" src="/wp-content/uploads/gk-pull-icon.svg" style="height:1em;"></td>
      <td style="padding: 4px;">Pull all selected repositories. Customize pull behavior from the dropdown menu.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Open in GitKraken Desktop or an external editor</strong></td>
      <td style="padding: 4px;">Open all selected repositories in GitKraken Desktop or your <a href="https://help.gitkraken.com/start-here/preferences/#external-editor">default editor</a>.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Locate in filesystem</strong></td>
      <td style="padding: 4px;">Reveal local paths of selected repositories or update their location.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Remove</strong></td>
      <td style="padding: 4px;">Remove selected repositories from the Workspace.</td>
    </tr>
  </tbody>
</table>

### How to view Workspace pull requests in Launchpad

See open pull requests for all repositories in a Workspace in [Launchpad](https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/).

<figure>
  <img src="/wp-content/uploads/open-ws-in-lp-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing the rocket icon to open the workspace in Launchpad.">
  <figcaption style="color:#888; text-align:center">Viewing a Workspace in Launchpad</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/launchpad-team-view-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Launchpad showing categorized pull requests with author, collaborators, repo, and branch information listed and actions like Open in GitHub, View Repo and open code suggestion available as a dropdown.">
  <figcaption style="color:#888; text-align:center">
    Launchpad showing team-wide pull request details
  </figcaption>
</figure>


## How Local Workspaces work

<div class='callout callout--basic'>
    <p><strong>Use a Local Workspace when:</strong> you want a private repository grouping stored only on your machine. <strong>Convert to a Cloud Workspace when:</strong> you need cross-device access, sharing, or integration-backed workspace features.</p>
</div>

### How to create a Local Workspace

To create a Local Workspace:

1. Click <button class="button button--success button--ui button--nolink">New Workspace</button>.
2. Select **Local Workspace**.
3. Name your Workspace.
4. Browse to select one or more repositories. You can choose:
   - Individual repositories
   - A directory of repositories
   - A VS Code Workspace file (`.code-workspace`)
5. (Optional) Add an icon and description.

<figure>
  <img src="/wp-content/uploads/create-local-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Dialog for creating a Local Workspace in GitKraken Desktop with workspace name, color, and repository options.">
  <figcaption style="color:#888; text-align:center">
    Creating a Local Workspace in GitKraken Desktop
  </figcaption>
</figure>

To automatically add all repositories in a selected folder, enable the <strong>Sync with local directory</strong> option.

### How to run multi-repository actions in a Local Workspace

You can take actions across multiple repositories within a Local Workspace:

1. Select the checkboxes next to the repositories.
2. Use the action toolbar at the top to:
   - **Fetch**: Update all selected repositories.
   - **Pull**: Sync selected repositories with the latest changes. Use the dropdown to customize pull behavior.
   - **Open**: Open selected repositories in GitKraken Desktop or your [default external editor](/start-here/preferences/#external-editor).
   - **Remove**: Remove selected repositories from the Workspace.

### How to convert a Local Workspace to a Cloud Workspace

To share a Local Workspace or use it on other machines, convert it to a Cloud Workspace:

1. Open your Local Workspace.
2. Click <strong>Create Cloud Workspace</strong>.
3. Choose a provider and select repositories to include.
4. (Optional) Add more repositories from the same provider.

<figure>
  <img src="/wp-content/uploads/local-to-cloud-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Workspace menu in GitKraken Desktop with the Create Cloud Workspace option highlighted.">
  <figcaption style="color:#888; text-align:center">
    Converting a Local Workspace to a Cloud Workspace
  </figcaption>
</figure>

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        Connect the provider integration in <kbd>Preferences > Integrations</kbd> before you create a Cloud Workspace.
    </p>
</div>

***

## How to edit a Workspace

To edit a Workspace, click the ellipsis <i class="fas fa-ellipsis-v"></i> next to the Workspace name.

<figure>
  <img src="/wp-content/uploads/multi-actions-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Dropdown menu in GitKraken Desktop showing workspace-level actions such as open, clone, locate, edit, change color, delete, and leave workspace.">
  <figcaption style="color:#888; text-align:center">
    Workspace actions menu
  </figcaption>
</figure>

### How to hide a Workspace

Hide a Workspace to reduce clutter. To show a hidden group again, such as Recents or Favorites, click the <i class="fa-solid fa-eye-slash"></i> icon.

<figure>
  <img src="/wp-content/uploads/unhide-group-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop interface showing the option to unhide a group from the workspace list via the visibility settings menu.">
  <figcaption style="color:#888; text-align:center">
    Unhiding a group from the Repo Management tab
  </figcaption>
</figure>

### How to select or unselect repositories

Select repositories to run multi-repository actions, such as Fetch or Pull, on only those repositories.

### How to open, clone, or locate repositories

Open repositories in GitKraken Desktop or your preferred editor. You can also clone or locate repositories within the file system.

<figure>
  <img src="/wp-content/uploads/clone-or-locate-ws-repos-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop interface showing options to clone or locate selected repositories within a workspace using the context menu.">
  <figcaption style="color:#888; text-align:center">
    Cloning or locating repositories
  </figcaption>
</figure>

### How to edit Workspace details

Customize your Workspace's name, color, description, and access permissions.

<figure>
  <img src="/wp-content/uploads/gkd-10-2-edit-workspace.png" 
       class="help-center-img img-bordered" 
       alt="Edit Workspace modal in GitKraken Desktop with fields to update workspace name, color, description, and team sharing settings.">
  <figcaption style="color:#888; text-align:center">
    Editing Workspace properties
  </figcaption>
</figure>

### How to change Workspace color

Use color to visually organize and prioritize Workspaces. Select **Change color** from the ellipsis menu.

***

## How to reorder Workspaces

Drag Workspaces to put them in the order you want.

<figure>
  <img src="/wp-content/uploads/reorder-workspaces-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing a hand cursor dragging a workspace section to reorder its position.">
  <figcaption style="color:#888; text-align:center">
    Reordering Workspaces
  </figcaption>
</figure>

***

## How to use Insights to visualize pull request history

<div class='callout callout--warning'>
  <p><strong>Note:</strong> GitKraken Insights is not available in GitKraken On-Premise Serverless or Self-Hosted Server deployments. Insights requires a connection to <a href="https://gitkraken.dev">gitkraken.dev</a>.</p>
</div>

GitKraken Insights shows how pull requests are merged into your repositories. Insights supports GitHub.com, Bitbucket.org, GitLab.com, and Azure DevOps (Hosted), and gives you:

- A visual history of your repository's development
- Pull request trends and team workflows

<figure>
  <img src="/wp-content/uploads/insights-gkdev-2026@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken.dev Insights dashboard for the GitLens Team, showing metrics like copy/paste vs moved code, change lead time, deployment frequency, duplicated code, number of PR reviews, cycle time, and active users over a 90-day period.">
  <figcaption style="color:#888; text-align:center">
    Insights metrics view in GitKraken.dev > Insights > Dashboards
  </figcaption>
</figure>

Insights runs on GitKraken.dev. To view it, open <a href="https://gitkraken.dev?source=help_center&product=gitkraken">GitKraken.dev</a> in your browser.

For more details, visit the [GitKraken.dev Insights documentation](/gk-dev/gk-dev-insights/).


***

## Azure DevOps requirements for Workspace Insights

To use Workspaces and [Insights](/gk-dev/gk-dev-insights/) with Azure DevOps, turn on third-party application access in Azure DevOps:

1. In your Azure DevOps dashboard, go to <kbd>Organization Settings > Policies</kbd>.
2. Enable **Third-party application access via OAuth**.

For details, see Microsoft's guide: [Change application connection & security policies for your organization](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).
