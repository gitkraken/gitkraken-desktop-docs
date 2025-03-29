---

title: Launchpad
description: Launchpad presents an overview of your Pull Requests, Issues and WIPs.
taxonomy:
    category: gitkraken-desktop

---

<kbd>Last Updated: March 2025</kbd>

Start your day with Launchpad! The Launchpad displays all of your Pull Requests, Issues, and Works In Progress (WIPs) relevant to you for a selected filters. 

The Launchpad is also available for GitKraken On-Premise customers, with some variations in features. 

### Getting started with the Launchpad

The Launchpad tab can be found in the top-left corner. By default, it displays a list of your Pull Requests, WIPs and Issues for the selected Workspace directly from your Hosting Service and Issue Tracker.

***

#### Connect Integrations

Integrate your repositories, issues, and pull requests with the Launchpad to consolidate your workflow.

You can easily connect your integrations at <kbd>Preferences > Integrations</kbd>

<img src="/wp-content/uploads/gkc-launchpad-hosting-service-10-0-0.png" class="help-center-img img-bordered">

#### Set up Workspaces and Integrations

Create a [Workspace](/gitkraken-desktop/workspaces/) with the relevant integration. Once created, you will be able to filter and focus on WIPs for specific repositories, issues, and pull requests.


<img src="/wp-content/uploads/gkc-launchpad-10-0-0.gif" class="help-center-img img-bordered">

<div class='callout callout--warning'>
    <p>To respect security requirements, Cloud Workspaces are not available for GitKaken On-Premise and will therefore not show in the Launchpad in those clients.</p>
</div>

* PULL REQUESTS: Shows all open pull requests for the repositories in selected Workspace.
* ISSUES: Shows all issues for the repositories in selected Workspace.
* WIPS: Shows all uncommitted changes for the repositories in selected Workspace.
* ALL: Shows all pull requests, issues, and WIPs for the repositories in selected Workspace.


Pull Requests and Issues can be pinned (and unpinned) by selecting the <i class="fa-solid fa-thumbtack"></i> icon to move them to the top of the list. Additionally, you have the option to Snooze PRs either indefinitely or for a specific duration by clicking the <i class="fa-solid fa-snooze"></i> icon, which will relocate them to the 'Snoozed' section. To retrieve these PRs, simply visit the 'Snoozed' section and remove them from the snooze state."

<img src="/wp-content/uploads/gkc-launchpad-pinsnooze-10-0-0.gif" class="help-center-img img-bordered">

***

### Personal or Team view

<img src="/wp-content/uploads/gkc-launchpad-personal-team-10.0.0.png" class="help-center-img img-bordered">

The Launchpad can be viewed in Personal or Team mode. Personal mode displays only the items where you are involved (created by you, assigned to you or created by you), while Team mode shows all pull requests and issues for the repositories in your Workspace - giving you a high level view of your team's coding efforts. You can toggle between these views by selecting the corresponding icon in the top right corner of the Launchpad.

<div class='callout callout--warning'>
    <p>Because Team View depends on Cloud Workspaces, Team View is not available for GitKaken On-Premise and will not show in the Launchpad for those clients. The Team View is available for Advanced users and higher.</p>
</div>

Note that Personal mode allows to see all items where you are involved in the remote hosting service, without limiting to a selected Workspace (select None in the Workspace dropdown). But Team mode requires a Workspace to be selected.

In Team View you can filter items by users, giving you a more focused view of specific team members' work.

<img src="/wp-content/uploads/gkd-launchpad-teamview-filter-10.3.0.png" class="help-center-img img-bordered">

***

### Saved Views

You can save your Launchpad views by clicking the <i class="fa-solid fa-plus"></i> Save View icon in the Launchpad tab bar.
Custom Launchpad views are only visible when the corresponding Team or Personal mode they were created in is selected.

<img src="/wp-content/uploads/gkd-10-5-launchpad-save-view.gif" class="help-center-img img-bordered">

<div class='callout callout--basic'>
    <p>Saved Views is only available on GitKraken Cloud clients.</p>
</div>

***

### Pull Requests

From the Launchpad, you can take action quickly on items such as:
- Merge pull request
- Close pull request
- Update issue status
- Mark issue as closed
- Open pull request/issue in the browser

<img src="/wp-content/uploads/gkc-launchpad-actions-10-0-0.png" class="help-center-img img-bordered">

Pull Requests section has the following columns:

* Last Updated 
* Status
  * Pull Request status. Shows status for "Open", “Draft” or “At Risk” pull requests
  * Pending Review or Changes Requested
  * Build status
* PR title with link to open the pull request in the hosting provider
  * Lines added/removed
  * Code Suggestions
* People 
* Repository and branch
* Actions
  * Open Repository
  * Open Repository in browser
  * Open Code Suggestions
  * Review Pull Request (GitHub only)
  * Close Pull Request

#### Github Pull Requests

If you are working with a GitHub.com Workspace, you may select a pull request to work with the <a href="/working-with-repositories/pull-requests/#github-pull-request-view">GitHub pull request view</a>.


### Issues

You can switch the Issue Tracker provider from the Issues section. The Issue Tracker provider can be set up in the <kbd>Preferences > Integrations</kbd> tab. 
Issues can be filtered by created, assigned or mentioned, and labels.

<img src="/wp-content/uploads/gkc-launchpad-issues-10-3-0.png" class="help-center-img img-bordered">

#### WIPs

The WIPs section displays all uncommitted changes for the repositories in the selected Workspace. You can quickly open the repository in a repository tab by clicking on <button class="button button--success button--ui button--nolink">View Repo</button>.

#### All

The ALL section displays all pull requests, issues, and WIPs for the repositories in the selected Workspace.

#### Snoozed

The SNOOZED section displays all snoozed pull requests and issues. You can unsnooze them by clicking on the <i class="fa-solid fa-snooze"></i> icon.

<div class='callout callout--basic'>
    <p>Snoozing is only available for GitKraken Pro clients.</p>
</div>

***

### Filtering by Jira Fix Versions and Sprints or GitHub and GitLab Milestones

You can now filter the Launchpad by Jira Fix Versions and Sprints or GitHub and GitLab Milestones.

<img src="/wp-content/uploads/gkd-10-4-launchpad-jira-sprint-filter.gif" class="help-center-img img-bordered">

### Launchpad Summary

The Launchpad summary in the status bar displays your most critical pull request. To view a detailed summary of your pull requests categorized by status (e.g., ready to merge, blocked, needs review), click on the indicator in the status bar. This action will open the Launchpad tab with the relevant status group expanded, allowing you to see more details and take appropriate actions on the pull requests.

The pull requests shown in the Launchpad summary are determined by the filters applied in the Launchpad tab.

<img src="/wp-content/uploads/gkd-launchpad-summary.gif" class="help-center-img img-bordered">

### On-Premise vs. Cloud Launchpad

Since GitKraken On-Premise is designed to function without sending data outside your network, we’ve right-sized Launchpad to fit this use case. Here’s what’s changed:

- ❌ No Cloud Workspaces – In the cloud version, workspaces help teams organize repositories across providers. The on-premise version focuses solely on your personal repositories and activity from your connected Git provider.
- ❌ No Snoozing or Pinning – Since these features require cloud storage, they’ve been removed from the on-prem version.
- ❌ No Team Launchpad – Because Cloud Workspaces are not available, Team Launchpad remains cloud-only.
- ✅ Filtering Still Works – You can still filter issues and PRs by assignment, mention, and status, just like in the cloud version.
- ✅ View Settings – While you can’t save Views, you can still toggle view settings and the app will remember your preferences.  

<img src="/wp-content/uploads/launchpad-prs.png" class="help-center-img img-bordered">

Since this is a fully local experience, no data leaves your network, making it ideal for teams with strict security and compliance requirements.