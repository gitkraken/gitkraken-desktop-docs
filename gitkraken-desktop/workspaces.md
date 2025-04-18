---

title: Workspaces
description: Workspaces allow you to create groups of repositories.
taxonomy:
    category: gitkraken-desktop

---

GitKraken Workspaces allow you to create easily accessible groups of repositories, take action across multiple repos, view details about their state at a glance, and share them with your team.

***

## Access Workspaces

Workspaces are listed in the Repo Management Tab. To access the Repo Management tab, either click on the folder icon located at the top left or utilize the keyboard shortcut <kbd>Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + O</kbd> (Mac).
<img src='/wp-content/uploads/gkc-repo-mngmt-tab.png' class='img-bordered img-responsive center'>

***

## Cloud Workspaces

Cloud Workspaces will be available for you to work with on any machine and the selected [teams](/start-here/teams/) within your organization. This helps ensure that everyone is up-to-date on the same set of repositories by offering [multi-repository actions](/gitkraken-desktop/workspaces/#cloud-multi-repository-actions) and the ability to [work with all pull requests](/gitkraken-desktop/workspaces/#pull-requests) from these repositories. 

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OIQVsNRqg1M?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

### Create a Cloud Workspace

To create a Cloud Workspace, select <button class="button button--success button--ui button--nolink">+ New Workspace</button>.

Then, select "Cloud Workspace”, name your Workspace, selecting the hosting service, and then select repositories to add. Optionally, you can also provide an icon, description and select teams or individual users to share with.

<img src="/wp-content/uploads/gkc-10-create-cloud-workspace.gif" class="help-center-img img-bordered">

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
            The integration for the desired service must be connected under <kbd>Preferences > Integrations</kbd> to create a Cloud Workspace.
    </p>
</div>

### Cloud multi-repository actions

Actions can be performed on multiple repositories within the Workspace at once, making it easy to get a new member of your team onboarded quickly or keep repository information up-to-date. To perform an action on multiple repositories, select the check box next to the repository name and then select the desired action from the options at the top.

<img src="/wp-content/uploads/gkc-10-cloud-workspace-multi-action.png" class="help-center-img img-bordered">

<img src="/wp-content/uploads/gkc-10-cloud-workspace-multi-action-2.png" class="help-center-img img-bordered">

The following multi-repository actions can be performed:
- Clone: clone all selected repositories. HTTPS will be used by default unless you have SSH configured in your [Integration settings](https://help.gitkraken.com/gitkraken-desktop/integrations/). This option is only available if the repositories are not already cloned locally. If one or more repositories are already cloned, you have to select the repositories that are not cloned and then select the clone option.
- Fetch: fetch all selected repositories.
- Pull: pull all selected repositories. You can change the behavior of the pull button by selecting the dropdown and selecting the radio button next to the desired option.
- Open in GitKraken Desktop or an external editor: open all selected repositories in GitKraken or in your [default editor](/start-here/preferences/#external-editor).
- Locate in filesystem: point to all selected repositories locally or update the local location of the repositories if they have changed. 
- Remove: remove all selected repositories from the Workspace.

### Pull requests

You can see all open pull requests for all repositories in [Launchpad](https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/) within the selected Workspace. Information shown here includes the pull request title, pull request number, CI status, complexity, the name of the branch being merged, and number of comments.

### Create a Local Workspace

To create a Local Workspace, select <button class="button button--success button--ui button--nolink">New Workspace</button>. Then, select “Local Workspace”, name your Workspace, and browse to select repositories to add to your Local Workspace. You may select individual repositories, a directory of repositories, or a VS Code Workspace (.code-workspace). Optionally, you can also provide an icon and description. 

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

<img src="/wp-content/uploads/gkc-10-local-to-cloud-workspace.png" class="help-center-img img-bordered">

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
            The integration for the desired service must be connected under <kbd>Preferences > Integrations</kbd> to create a Cloud Workspace.
    </p>
</div>

***

## Edit a Workspace

Edit a Workspace by selecting the ellipsis <i class="fas fa-ellipsis-v"></i> icon by the Workspace name.

<img src="/wp-content/uploads/gkd-10-2-edit-a-workspace.png" class="help-center-img img-bordered">

The available options are:

### Hide

You can hide a workspace to declutter your view, just as you can hide other groups in the Repo Management Tab (e.g., Recent Repositories or Favorites).

To show a hidden workspace or group, simply click the <i class="fa-solid fa-eye-slash"></i> icon to unhide.

<img src="/wp-content/uploads/gkd-10-2-hide-workspaces.png" class="help-center-img img-bordered">

### Select/Unselect

You can select or unselect repositories within a workspace. This functionality allows you to perform specific actions, such as fetching, pulling, or opening repositories in VS Code, on the selected repositories only.

### Open/Clone/Locate Repositories

Use this option to open, clone, or locate repositories. You can apply these actions to the selected repositories or to all repositories within the workspace.

<img src="/wp-content/uploads/gkd-10-2-open-clone-locate-workspaces.png" class="help-center-img img-bordered">

### Edit Workspace

Customize your workspace by editing its name, color in the Repo Management Tab, description, and the list of members with access to the workspace. This helps you keep your workspace organized and accessible to the right team members.

<img src="/wp-content/uploads/gkd-10-2-edit-workspace.png" class="help-center-img img-bordered">

### Change Color

Similar to what you can do with Edit Workspace, change the color of your Workspace (or group) by selecting `Change color` in the three-dot menu of any repo group. Use color to categorize Workspaces or highlight your most used groups of repositories.

***

## Insights

GitKraken Insights is a powerful tool that helps you visualize how pull requests are merged into your repositories. It provides a visual representation of your repository's history, allowing you to see how your codebase has evolved over time. You can use this information to make informed decisions about how to improve your workflow.

Insights is available for Github.com, Bitbucket.org, Gitlab.com, and Azure DevOps (Hosted).

To access GitKraken Insights for your Workspace, click on the Insights icon. This will open a new browser window, directing you to the Insights view for that specific Workspace on [GitKraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken
).

See [gitkraken.dev Insights](/gk-dev/gk-dev-insights/) for more information on working with Insights. 

<img src="/wp-content/uploads/gkd-10-4-insights-icon.png" class="help-center-img img-bordered">

***

## Requirement for Azure Workspaces and Insights

In order to work with Workspaces and [Insights](/gk-dev/gk-dev-insights/) for Azure, `Third-party application access via OAuth` will need to be enabled in Azure from `Organization Settings > Policies`. You can find more information on this setting [here](https://learn.microsoft.com/en-us/azure/devops/organizations/accounts/change-application-access-policies?view=azure-devops).