---

title: Workspaces
description: Workspaces allow you to create groups of repositories.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

GitKraken Workspaces allow you to create easily accessible groups of repositories, take action across multiple repos, view details about their state at a glance, and share them with your team.

<img src="/wp-content/uploads/workspaces-tab-2025.png" srcset="/wp-content/uploads/workspaces-tab-2025@2x.png" class="help-center-img img-bordered">

***

## Access Workspaces

Workspaces are listed in the Repo Management Tab. To access the Repo Management tab, either click on the folder icon located at the top left or utilize the keyboard shortcut <kbd>Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + O</kbd> (Mac).
<img src='/wp-content/uploads/open-workspaces-2025.png' srcset="/wp-content/uploads/open-workspaces-2025@2x.png" class='img-bordered img-responsive center'>

***

## Cloud Workspaces

Cloud Workspaces will be available for you to work with on any machine and the selected [teams](/start-here/teams/) within your organization. This helps ensure that everyone is up-to-date on the same set of repositories by offering [multi-repository actions](/gitkraken-desktop/workspaces/#cloud-multi-repository-actions) and the ability to [work with all pull requests](/gitkraken-desktop/workspaces/#pull-requests) from these repositories. 

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OIQVsNRqg1M?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

### Create a Cloud Workspace

To create a Cloud Workspace, select <button class="button button--success button--ui button--nolink">+ New Workspace</button>.

<img src="/wp-content/uploads/add-new-workspace-2025.png" srcset="/wp-content/uploads/add-new-workspace-2025@2x.png" class="help-center-img img-bordered">

Then, select "Cloud Workspace”, name your Workspace, selecting the hosting service, and then select repositories to add. Optionally, you can also provide an icon, description and select teams or individual users to share with.

<img src="/wp-content/uploads/config-cloud-workspace-2025.png" srcset="/wp-content/uploads/config-cloud-workspace-2025@2x.png" class="help-center-img img-bordered">

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
            The integration for the desired service must be connected under <kbd>Preferences > Integrations</kbd> to create a Cloud Workspace.
    </p>
</div>

### Cloud multi-repository actions

Perform an action on multiple repositories within the Workspace at once, making it easy to get a new member of your team onboarded quickly or keep repository information up-to-date. To perform an action on multiple repositories, select the check box next to the repository name and then select the desired action from the options at the top.

<img src="/wp-content/uploads/multi-fetch-ws-2025.png" srcset="/wp-content/uploads/multi-fetch-ws-2025@2x.png" class="help-center-img img-bordered">

There are more multi-repo actions available from the ellipsis menu in the corner of each Workspace, in addition to general Workspace actions. 

<img src="/wp-content/uploads/more-multi-repo-actions-2025.png" srcset="/wp-content/uploads/more-multi-repo-actions-2025@2x.png" class="help-center-img img-bordered">

<table style="font-size: 14px; border-collapse: collapse;">
  <thead>
    <tr>
      <th style="text-align: left; padding: 4px;">Action</th>
      <th style="text-align: left; padding: 4px;">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding: 4px;">
        <strong>Clone</strong> <img src="/wp-content/uploads/gk-remote-icon.svg" style="height:1em;">
      </td>
      <td style="padding: 4px;">
        Clone all selected repositories. HTTPS will be used by default unless you have 
        <a href="https://help.gitkraken.com/gitkraken-desktop/integrations/">SSH configured in your Integration settings</a>. 
        This option is only available if the repositories are not already cloned locally. 
        If one or more repositories are already cloned, you have to select the repositories 
        that are not cloned and then select the clone option.
      </td>
    </tr>
    <tr>
      <td style="padding: 4px;">
        <strong>Fetch</strong> <img src="/wp-content/uploads/gk-fetch-pull-icon.svg" style="height:1em;">
      </td>
      <td style="padding: 4px;">
        Fetch all selected repositories.
      </td>
    </tr>
    <tr>
      <td style="padding: 4px;">
        <strong>Pull</strong> <img src="/wp-content/uploads/gk-pull-icon.svg" style="height:1em;">
      </td>
      <td style="padding: 4px;">
        Pull all selected repositories. You can change the behavior of the pull button 
        by selecting the dropdown and selecting the radio button next to the desired option.
      </td>
    </tr>
    <tr>
      <td style="padding: 4px;">
        <strong>Open in GitKraken Desktop or an external editor</strong>
      </td>
      <td style="padding: 4px;">
        Open all selected repositories in GitKraken or in your 
        <a href="https://help.gitkraken.com/start-here/preferences/#external-editor">default editor</a>.
      </td>
    </tr>
    <tr>
      <td style="padding: 4px;">
        <strong>Locate in filesystem</strong>
      </td>
      <td style="padding: 4px;">
        Point to all selected repositories locally or update the local location of 
        the repositories if they have changed.
      </td>
    </tr>
    <tr>
      <td style="padding: 4px;">
        <strong>Remove</strong>
      </td>
      <td style="padding: 4px;">
        Remove all selected repositories from the Workspace.
      </td>
    </tr>
  </tbody>
</table>


### Pull requests

You can see all open pull requests for all repositories in [Launchpad](https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/) within the selected Workspace. 

<img src="/wp-content/uploads/open-ws-in-lp-2025.png" srcset="/wp-content/uploads/open-ws-in-lp-2025@2x.png" class="help-center-img img-bordered">

Information shown here includes the pull request title, pull request number, CI status, complexity, the name of the branch being merged, and number of comments.

<img src="/wp-content/uploads/launchpad-team-view-2025.png" srcset="/wp-content/uploads/launchpad-team-view-2025@2x.png" class="help-center-img img-bordered">

## Local Workspaces

### Create a Local Workspace

To create a Local Workspace, select <button class="button button--success button--ui button--nolink">New Workspace</button>. Then, select “Local Workspace”, name your Workspace, and browse to select repositories to add to your Local Workspace. You may select individual repositories, a directory of repositories, or a VS Code Workspace (.code-workspace). Optionally, you can also provide an icon and description. 

<img src="/wp-content/uploads/create-local-ws-2025.png" srcset="/wp-content/uploads/create-local-ws-2025@2x.png" class="help-center-img img-bordered">

The option "Sync with local directory" will allow you to sync the Workspace with a local directory. This will automatically add any repositories in the selected directory to the Workspace.

### Local multi-repository actions

Actions can be performed on multiple repositories within the Workspace at once. To perform an action on multiple repositories, select the check box next to the repository name and then select the desired action from the options at the top.

The following multi-repository actions can be performed:
- Fetch: fetch all selected repositories.
- Pull: pull all selected repositories. You can change the behavior of the pull button by selecting the dropdown and selecting the radio button next to the desired option.
- Open in GitKraken Desktop or an external editor: open all selected repositories in GitKraken or in your [default editor](/start-here/preferences/#external-editor).
- Remove: remove all selected repositories from the Workspace.

### Create a Cloud Workspace from a Local Workspace

You can create a Cloud Workspace from a Local Workspace which will enable more visibility into your pull requests, issues, and share your Workspace with teams.

To do this, select your local Workspace to open it and then select `Create cloud workspace`. From here, you will need to select the provider for your new Cloud Workspace, select the repositories you would like added, and you can even add more repositories to this Workspace from the selected provider.

<img src="/wp-content/uploads/local-to-cloud-ws-2025.png" srcset="/wp-content/uploads/local-to-cloud-ws-2025@2x.png" class="help-center-img img-bordered">

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
            The integration for the desired service must be connected under <kbd>Preferences > Integrations</kbd> to create a Cloud Workspace.
    </p>
</div>

***

## Edit a Workspace

Edit a Workspace by selecting the ellipsis <i class="fas fa-ellipsis-v"></i> icon by the Workspace name.

<img src="/wp-content/uploads/multi-actions-ws-2025.png" srcset="/wp-content/uploads/multi-actions-ws-2025@2x.png" class="help-center-img img-bordered">

The available options are:

### Hide

You can hide a workspace to declutter your view, just as you can hide other groups in the Repo Management Tab (e.g., Recent Repositories or Favorites).

To show a hidden workspace or group, simply click the <i class="fa-solid fa-eye-slash"></i> icon to unhide.

<img src="/wp-content/uploads/unhide-group-2025.png" srcset="/wp-content/uploads/unhide-group-2025@2x.png" class="help-center-img img-bordered">

### Select/Unselect

You can select or unselect repositories within a workspace. This functionality allows you to perform specific actions, such as fetching, pulling, or opening repositories in VS Code, on the selected repositories only.

### Open/Clone/Locate Repositories

Use this option to open, clone, or locate repositories. You can apply these actions to the selected repositories or to all repositories within the workspace.

<img src="/wp-content/uploads/clone-or-locate-ws-repos-2025.png" srcset="/wp-content/uploads/clone-or-locate-ws-repos-2025@2x.png" class="help-center-img img-bordered">

### Edit Workspace

Customize your workspace by editing its name, color in the Repo Management Tab, description, and the list of members with access to the workspace. This helps you keep your workspace organized and accessible to the right team members.

<img src="/wp-content/uploads/gkd-10-2-edit-workspace.png" class="help-center-img img-bordered">

### Change Color

Similar to what you can do with Edit Workspace, change the color of your Workspace (or group) by selecting `Change color` in the three-dot menu of any repo group. Use color to categorize Workspaces or highlight your most used groups of repositories.

***
## Reorder Workspaces

Drag and drop your Workspaces to reorder the list. 

<img src="/wp-content/uploads/reorder-workspaces-2025.png" srcset="/wp-content/uploads/reorder-workspaces-2025@2x.png" class="help-center-img img-bordered">

Don't forget that you can [Hide Workspaces](/gitkraken-desktop/workspaces/#elementor-toc__heading-anchor-9) that you prefer not to see. 

***
## Insights

GitKraken Insights is a powerful tool that helps you visualize how pull requests are merged into your repositories. It provides a visual representation of your repository's history, allowing you to see how your codebase has evolved over time. You can use this information to make informed decisions about how to improve your workflow.

<img src="/wp-content/uploads/insights-gkdev-2025.png" srcset="/wp-content/uploads/insights-gkdev-2025@2x.png" class="help-center-img img-bordered">

Insights is available for GitHub.com, Bitbucket.org, GitLab.com, and Azure DevOps (Hosted). To access GitKraken Insights for your Workspace, click on the Insights icon. 

<img src="/wp-content/uploads/insights-icon-ws-2025.png" srcset="/wp-content/uploads/insights-icon-ws-2025@2x.png" class="help-center-img img-bordered">

This will open a new browser window, directing you to the Insights view for that specific Workspace on [GitKraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken
).

See [gitkraken.dev Insights](/gk-dev/gk-dev-insights/) for more information on working with Insights. 

***

## Requirement for Azure Workspaces and Insights

In order to work with Workspaces and [Insights](/gk-dev/gk-dev-insights/) for Azure, `Third-party application access via OAuth` will need to be enabled in Azure from `Organization Settings > Policies`. 

You can find more information on this setting from Microsoft's [Change application connection & security policies for your organization](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops) article.


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

