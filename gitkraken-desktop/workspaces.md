---
title: Workspaces in GitKraken Desktop
description: Learn how to create, manage, and share Cloud or Local Workspaces in GitKraken Desktop to organize and collaborate across repositories.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

GitKraken Workspaces allow you to create easily accessible groups of repositories, take action across multiple repos, view details about their state at a glance, and share them with your team.

<figure>
  <img src="/wp-content/uploads/workspaces-tab-2025.png" 
       srcset="/wp-content/uploads/workspaces-tab-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop showing multiple cloud Workspaces, each grouping related repositories with options to clone, locate, or manage them.">
  <figcaption style="color:#888; text-align:center">
    Group your repos into a Workspace
  </figcaption>
</figure>

***

## Access Your Workspaces

To access the Repo Management tab:

1. Click on the folder icon at the top left.
2. Or use the keyboard shortcut <kbd>Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + O</kbd> (Mac).

<figure>
  <img src="/wp-content/uploads/open-workspaces-2025.png" 
       srcset="/wp-content/uploads/open-workspaces-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface highlighting the folder icon used to access Workspaces from the Repo Management tab.">
  <figcaption style="color:#888; text-align:center">
    Opening Workspaces from the Repo Management tab
  </figcaption>
</figure>

***

## Cloud Workspaces

Cloud Workspaces are accessible from any machine and can be shared with selected [teams](/start-here/teams/) in your organization. They allow for [multi-repository actions](/gitkraken-desktop/workspaces/#cloud-multi-repository-actions) and centralized pull request management.

<p>Watch the overview:</p>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OIQVsNRqg1M?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

### Create a Cloud Workspace

1. Click <button class="button button--success button--ui button--nolink">+ New Workspace</button>.
2. Select "Cloud Workspace".
3. Name your Workspace and select the hosting service.
4. Choose repositories to add.
5. (Optional) Add an icon, description, and share with teams or users.

<figure>
  <img src="/wp-content/uploads/add-new-workspace-2025.png" 
       srcset="/wp-content/uploads/add-new-workspace-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Highlighted 'New Workspace' button in the Repository Management view of GitKraken Desktop.">
  <figcaption style="color:#888; text-align:center">
    Add a new Cloud Workspace
  </figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/config-cloud-workspace-2025.png" 
       srcset="/wp-content/uploads/config-cloud-workspace-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Cloud Workspace creation form in GitKraken Desktop, showing workspace name, color selection, provider, and repository fields.">
  <figcaption style="color:#888; text-align:center">
    Configuring Cloud Workspace settings
  </figcaption>
</figure>

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        The integration for the desired service must be connected under <kbd>Preferences > Integrations</kbd>.
    </p>
</div>

### Perform Multi-repository Actions

To take action across multiple repositories:

1. Select the checkboxes next to the desired repositories.
2. Choose an action from the toolbar at the top.

<figure>
  <img src="/wp-content/uploads/multi-fetch-ws-2025.png" 
       srcset="/wp-content/uploads/multi-fetch-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing multiple selected repositories in a workspace and the 'Fetch 3 repositories' button highlighted.">
  <figcaption style="color:#888; text-align:center">Multi-repo fetch operation</figcaption>
</figure>

More options are available via the ellipsis menu.

<figure>
  <img src="/wp-content/uploads/more-multi-repo-actions-2025.png" 
       srcset="/wp-content/uploads/more-multi-repo-actions-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop showing a dropdown menu with bulk workspace options, including Select All, Open repositories, and Remove repositories.">
  <figcaption style="color:#888; text-align:center">Accessing more multi-repo actions</figcaption>
</figure>


<table style="font-size: 14px; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="text-align: left; padding: 4px;">Action</th>
      <th style="text-align: left; padding: 4px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 4px;"><strong>Clone</strong> <img src="/wp-content/uploads/gk-remote-icon.svg" style="height:1em;"></td>
      <td style="padding: 4px;">Clone all selected repositories. HTTPS is used by default unless <a href="https://help.gitkraken.com/gitkraken-desktop/integrations/">SSH is configured in your settings</a>. Only available if repositories aren't already cloned.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Fetch</strong></td>
      <td style="padding: 4px;">Fetch all selected repositories.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Pull</strong> <img src="/wp-content/uploads/gk-pull-icon.svg" style="height:1em;"></td>
      <td style="padding: 4px;">Pull all selected repositories. Customize pull behavior from the dropdown menu.</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><strong>Open in GitKraken Desktop or an external editor</strong></td>
      <td style="padding: 4px;">Open all selected repositories in GitKraken or your <a href="https://help.gitkraken.com/start-here/preferences/#external-editor">default editor</a>.</td>
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

### View Pull Requests in Launchpad

Access open pull requests for all repositories in a Workspace directly from [Launchpad](https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/).

<figure>
  <img src="/wp-content/uploads/open-ws-in-lp-2025.png" 
       srcset="/wp-content/uploads/open-ws-in-lp-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing the rocket icon to open the workspace in Launchpad.">
  <figcaption style="color:#888; text-align:center">Viewing a Workspace in Launchpad</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/launchpad-team-view-2025.png" 
       srcset="/wp-content/uploads/launchpad-team-view-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Launchpad showing categorized pull requests with author, collaborators, repo, and branch information listed and actions like Open in GitHub, View Repo and open code suggestion available as a dropdown.">
  <figcaption style="color:#888; text-align:center">
    Launchpad showing team-wide pull request details
  </figcaption>
</figure>


## Local Workspaces

### Create a Local Workspace

To create a Local Workspace:

1. Click <button class="button button--success button--ui button--nolink">New Workspace</button>.
2. Select “Local Workspace.”
3. Name your Workspace.
4. Browse to select one or more repositories. You can choose:
   - Individual repositories
   - A directory of repositories
   - A VS Code Workspace file (`.code-workspace`)
5. (Optional) Add an icon and description.

<figure>
  <img src="/wp-content/uploads/create-local-ws-2025.png" 
       srcset="/wp-content/uploads/create-local-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Dialog for creating a Local Workspace in GitKraken Desktop with workspace name, color, and repository options.">
  <figcaption style="color:#888; text-align:center">
    Creating a Local Workspace in GitKraken Desktop
  </figcaption>
</figure>

To automatically add all repositories in a selected folder, enable the <strong>Sync with local directory</strong> option.

### Perform Multi-repository Actions

You can take actions across multiple repositories within a Local Workspace:

1. Select the checkboxes next to the repositories.
2. Use the action toolbar at the top to:
   - **Fetch**: Update all selected repositories.
   - **Pull**: Sync selected repositories with the latest changes. Use the dropdown to customize pull behavior.
   - **Open**: Launch selected repositories in GitKraken or your [default external editor](/start-here/preferences/#external-editor).
   - **Remove**: Delete selected repositories from the Workspace.

### Convert a Local Workspace to a Cloud Workspace

To enable sharing and enhanced visibility:

1. Open your Local Workspace.
2. Click <strong>Create cloud workspace</strong>.
3. Choose a provider and select repositories to include.
4. (Optional) Add additional repositories from the same provider.

<figure>
  <img src="/wp-content/uploads/local-to-cloud-ws-2025.png" 
       srcset="/wp-content/uploads/local-to-cloud-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Context menu in GitKraken showing the option to convert a Local Workspace to a Cloud Workspace.">
  <figcaption style="color:#888; text-align:center">
    Converting a Local Workspace to a Cloud Workspace
  </figcaption>
</figure>

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        Ensure the provider integration is connected under <kbd>Preferences > Integrations</kbd> before creating a Cloud Workspace.
    </p>
</div>

***

## Edit a Workspace

To edit a Workspace, click the ellipsis <i class="fas fa-ellipsis-v"></i> next to the Workspace name.

<figure>
  <img src="/wp-content/uploads/multi-actions-ws-2025.png" 
       srcset="/wp-content/uploads/multi-actions-ws-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="Dropdown menu in GitKraken showing workspace-level actions such as open, clone, locate, edit, change color, delete, and leave workspace.">
  <figcaption style="color:#888; text-align:center">
    Workspace actions menu
  </figcaption>
</figure>

### Hide a Workspace

Hide a Workspace to reduce clutter. Hidden groups (e.g., Recents, Favorites) can be shown again using the <i class="fa-solid fa-eye-slash"></i> icon.

<figure>
  <img src="/wp-content/uploads/unhide-group-2025.png" 
       srcset="/wp-content/uploads/unhide-group-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop interface showing the option to unhide a group from the workspace list via the visibility settings menu.">
  <figcaption style="color:#888; text-align:center">
    Unhiding a group from the Repo Management tab
  </figcaption>
</figure>

### Select/Unselect Repositories

Manually select repositories for targeted multi-repo actions like Fetch or Pull.

### Open/Clone/Locate Repositories

Open repositories in GitKraken Desktop or your preferred editor. You can also clone or locate repositories within the file system.

<figure>
  <img src="/wp-content/uploads/clone-or-locate-ws-repos-2025.png" 
       srcset="/wp-content/uploads/clone-or-locate-ws-repos-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop interface showing options to clone or locate selected repositories within a workspace using the context menu.">
  <figcaption style="color:#888; text-align:center">
    Cloning or locating repositories
  </figcaption>
</figure>

### Edit Workspace Details

Customize your Workspace’s name, color, description, and access permissions.

<figure>
  <img src="/wp-content/uploads/gkd-10-2-edit-workspace.png" 
       class="help-center-img img-bordered" 
       alt="Edit Workspace modal in GitKraken Desktop with fields to update workspace name, color, description, and team sharing settings.">
  <figcaption style="color:#888; text-align:center">
    Editing Workspace properties
  </figcaption>
</figure>

### Change Workspace Color

Use color to visually organize and prioritize Workspaces. Select `Change color` from the three-dot menu.

***

## Reorder Workspaces

Drag and drop Workspaces to arrange them in the desired order.

<figure>
  <img src="/wp-content/uploads/reorder-workspaces-2025.png" 
       srcset="/wp-content/uploads/reorder-workspaces-2025@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken Desktop interface showing a hand cursor dragging a workspace section to reorder its position.">
  <figcaption style="color:#888; text-align:center">
    Reordering Workspaces
  </figcaption>
</figure>

***

## Use Insights to Visualize Pull Request History

GitKraken Insights helps you understand how pull requests are merged into your repositories. It provides:

- A visual history of your repository’s development
- Insight into pull request trends and team workflows
- Support for GitHub.com, Bitbucket.org, GitLab.com, and Azure DevOps (Hosted)

<figure>
  <img src="/wp-content/uploads/insights-gkdev-2026.png" 
       srcset="/wp-content/uploads/insights-gkdev-2026@2x.png" 
       class="help-center-img img-bordered"
       alt="GitKraken.dev Insights dashboard for the GitLens Team, showing metrics like copy/paste vs moved code, change lead time, deployment frequency, duplicated code, number of PR reviews, cycle time, and active users over a 90-day period.">
  <figcaption style="color:#888; text-align:center">
    Insights metrics view in GitKraken.dev > Insights > Dashboards
  </figcaption>
</figure>

To launch GitKraken Insights:

1. Open a Cloud Workspace.
2. Click the <strong>Insights</strong> icon in the upper-right of the Workspace header.

<figure>
  <img src="/wp-content/uploads/insights-icon-ws-2025.png" 
       srcset="/wp-content/uploads/insights-icon-ws-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="Insights icon highlighted in the Workspace header of GitKraken Desktop, showing how to open Insights for the selected Workspace.">
  <figcaption style="color:#888; text-align:center">
    Accessing GitKraken Insights from a Workspace
  </figcaption>
</figure>

This will open a new browser tab showing insights for that Workspace on <a href="https://gitkraken.dev?source=help_center&product=gitkraken">GitKraken.dev</a>.

For more details, visit the [GitKraken.dev Insights documentation](/gk-dev/gk-dev-insights/).


***

## Azure DevOps Requirements for Insights

To use Workspaces and [Insights](/gk-dev/gk-dev-insights/) with Azure DevOps:

- You must enable **Third-party application access via OAuth** in Azure.
- Navigate to <kbd>Organization Settings > Policies</kbd> in your Azure DevOps dashboard.

Learn more from Microsoft’s official guidance: [Change application connection & security policies for your organization](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).


***

## Workspace Changelog

Take a trip down memory lane, and see how Workspaces have evolved over time.

<table style="font-size: 14px; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="text-align: left; padding: 4px;">Version</th>
      <th style="text-align: left; padding: 4px;">Highlight</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-4-0">10.4</a></td>
      <td style="padding: 4px;">Insights now on <a href="https://gitkraken.dev?source=help_center&product=gitkraken">gitkraken.dev</a></td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-3-0">10.3</a></td>
      <td style="padding: 4px;">New look for Repo Management tab</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-1-0">10.1</a></td>
      <td style="padding: 4px;">Customize your Repository Management tab</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-0-2">10.0.2</a></td>
      <td style="padding: 4px;">Workspaces merge with Repository Management</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-0-0">10.0</a></td>
      <td style="padding: 4px;">Focus View becomes Launchpad</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-5-0">9.5</a></td>
      <td style="padding: 4px;">Multi-pull + Share Workspace</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-2-0">9.2</a></td>
      <td style="padding: 4px;">Issue View added (now in Launchpad)</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-1-0">9.1</a></td>
      <td style="padding: 4px;">Insights for Azure DevOps</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-0-0">9.0</a></td>
      <td style="padding: 4px;">Local & Cloud Workspaces + Insights</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-9-0">8.9</a></td>
      <td style="padding: 4px;">Team Overview added</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-8-0">8.8</a></td>
      <td style="padding: 4px;">Workspace Overview added</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-6-0">8.6</a></td>
      <td style="padding: 4px;">Bitbucket support added</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-5-0">8.5</a></td>
      <td style="padding: 4px;">Azure DevOps support added</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-4-0">8.4</a></td>
      <td style="padding: 4px;">Workspace pull requests added</td>
    </tr>
    <tr>
      <td style="padding: 4px;"><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-2-0">8.2</a></td>
      <td style="padding: 4px;">Workspaces introduced</td>
    </tr>
  </tbody>
</table>

