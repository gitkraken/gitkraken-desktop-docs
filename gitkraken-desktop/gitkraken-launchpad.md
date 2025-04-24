---

title: Launchpad
description: Launchpad presents an overview of your Pull Requests, Issues and WIPs.
taxonomy:
    category: gitkraken-desktop

---

<kbd>Last Updated: April 2025</kbd>

Start your day with Launchpad! The Launchpad displays all of your Pull Requests, Issues, and Works In Progress (WIPs) relevant to you for a selected filters. 

<img src="/wp-content/uploads/launchpad-highlight-2025.png" srcset="/wp-content/uploads/launchpad-highlight-2025@2x.png" class="help-center-img img-bordered">

The Launchpad is also [available for GitKraken On-Premise](https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/#elementor-toc__heading-anchor-13) customers, with some variations in features. 

***

### Getting started with the Launchpad

The Launchpad tab can be found in the top-left corner. 

<img src="/wp-content/uploads/open-launchpad-2025.png" srcset="/wp-content/uploads/open-launchpad-2025@2x.png" class="help-center-img img-bordered">

By default, it displays a list of your Pull Requests, WIPs and Issues for the selected Workspace directly from your hosting service and issue tracker. You can easily connect your integrations at <kbd>Preferences > Integrations</kbd> or follow the shortcuts to connect a given integration.

<img src="/wp-content/uploads/connect-integration-launchpad-2025.png" srcset="/wp-content/uploads/connect-integration-launchpad-2025@2x.png" class="help-center-img img-bordered">

#### Set up Workspaces and Integrations

Launchpad works best with at least 1 Workspace.

If this is your first time learning about Workspaces, take a moment to first [create a Cloud Workspace](https://help.gitkraken.com/gitkraken-desktop/workspaces/#cloud-workspaces/) and then return to this page.

With your Workspace(s) created, you will be able to filter and focus on WIPs for specific repositories, issues, and pull requests.


<img src="/wp-content/uploads/select-workspace-launchpad-2025.png" srcset="/wp-content/uploads/select-workspace-launchpad-2025@2x.png" class="help-center-img img-bordered">

* PULL REQUESTS: Shows all open pull requests for the repositories in selected Workspace.
* ISSUES: Shows all issues for the repositories in selected Workspace.
* WIPS: Shows all uncommitted changes for the repositories in selected Workspace.
* ALL: Shows all pull requests, issues, and WIPs for the repositories in selected Workspace.

<div class='callout callout--warning'>
    <p>To respect security requirements, Cloud Workspaces are not available for GitKaken On-Premise and will therefore not show in the Launchpad in those clients. <a href="https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/#elementor-toc__heading-anchor-13">Learn more.</a></p>
</div>

Pull Requests and Issues can be pinned (and unpinned) by selecting the <i class="fa-solid fa-thumbtack"></i> icon to move them to the top of the list. 

<img src="/wp-content/uploads/pin-launchpad-2025.png" srcset="/wp-content/uploads/pin-launchpad-2025@2x.png" class="help-center-img img-bordered">

Additionally, you have the option to Snooze PRs either indefinitely or for a specific duration by clicking the <i class="fa-solid fa-snooze"></i> icon, which will relocate them to the <kbd>Snoozed</kbd> section. To retrieve these PRs, simply visit the <kbd>Snoozed</kbd> section and remove them from the snooze state."

<img src="/wp-content/uploads/snooze-tab-launchpad-2025.png" srcset="/wp-content/uploads/snooze-tab-launchpad-2025@2x.png" class="help-center-img img-bordered">

***

### Personal View

The Launchpad can be viewed in Personal or Team View. Personal displays only the pull requests and issues where you are involved in the following ways:

- Created by you
- Assigned to you
- You are the reviewer
- Mentions you

<img src="/wp-content/uploads/gkc-launchpad-personal-team-10.0.0.png" class="help-center-img img-bordered">

Additionally when you select "None" in the Workspace dropdown, Personal view shows all items where you are involved in the remote hosting service, without limiting to a selected Workspace.


<div class='callout callout--warning'>
    <p>Because Team View depends on Cloud Workspaces, Team View is not available for GitKaken On-Premise and will not show in the Launchpad for those clients. The Team View is available for Advanced users and higher.</p>
</div>

### Team View

You can toggle between Personal and Team Views from the top right corner of the Launchpad.

<img src="/wp-content/uploads/team-view-launchpad-2025.png" srcset="/wp-content/uploads/team-view-launchpad-2025@2x.png" class="help-center-img img-bordered">

Team mode requires a Workspace to be selected, and will display all pull requests and issues associated to everyone but you. 

- Created by someone else
- Assigned to someone else
- Reviewer(s) set 
- Mentions others

In Team View you can filter items by users, giving you a more focused view of specific team members' work.

<img src="/wp-content/uploads/filter-team-member-2025.png" srcset="/wp-content/uploads/filter-team-member-2025@2x.png" class="help-center-img img-bordered">

Team mode shows all pull requests and issues for the repositories in your Workspace - giving you a high level view of your team's coding efforts.


***

### Saved Views

Like your filter selections? You can save your Launchpad views by clicking the <i class="fa-solid fa-plus"></i> Save View icon in the Launchpad tab bar.

<img src="/wp-content/uploads/gkd-10-5-launchpad-save-view.gif" class="help-center-img img-bordered">

Any Saved View can be deleted by selecting the View, and then navigating to <kbd>View Settings > Delete this view</kbd> Custom Launchpad views are only visible when the corresponding Team or Personal mode they were created in is selected.

<div class='callout callout--basic'>
    <p>Saved Views is not available for GitKraken On-Premise clients.</p>
</div>

***

### Pull Requests

From the Launchpad, you can take action quickly on items such as:
- Open pull request in the browser
- View Repo
- Open Code Suggestion (if applicable)
- Review Pull Request (GitHub only)
- Checkout PR branch
- Close PR
- Checkout in New Worktree

<img src="/wp-content/uploads/pr-actions-launchpad-2025.png" srcset="/wp-content/uploads/pr-actions-launchpad-2025@2x.png" class="help-center-img img-bordered">

Pull Requests section has the following columns:

<table>
  <thead>
    <tr>
      <th>Column</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Last Updated</td>
      <td>Timestamp of the last activity on the pull request.</td>
    </tr>
    <tr>
      <td>Status</td>
      <td>PR status (Open, Draft, At Risk), pending review, changes requested, and build status.</td>
    </tr>
    <tr>
      <td>PR Title</td>
      <td>Title with link to hosting provider, lines added/removed, and code suggestions if available.</td>
    </tr>
    <tr>
      <td>Author(s)</td>
      <td>Creator(s) of the pull request.</td>
    </tr>
    <tr>
      <td>Repository and Branch</td>
      <td>Name of the repository and the associated branch.</td>
    </tr>
    <tr>
      <td>Actions</td>
      <td>Open repository, open in browser, open code suggestions, review PR (GitHub only), or close PR.</td>
    </tr>
  </tbody>
</table>



#### GitHub Pull Requests

If you are working with a GitHub.com Workspace, you may open the <a href="/working-with-repositories/pull-requests/#github-pull-request-view">GitHub pull request view</a> directly in the Launchpad.

<img src="/wp-content/uploads/github-pr-view-launchpad.png" class="help-center-img img-bordered">


### Issues

Launchpad is here to show you all issues you or your team is working on. Whether you are using Jira, GitHub Issues, Azure DevOps, or Trello, you can switch the Issue Tracker provider from the Issues section. 

<img src="/wp-content/uploads/issues-tab-launchpad-2025.png" srcset="/wp-content/uploads/issues-tab-launchpad-2025@2x.png" class="help-center-img img-bordered">

The Issue Tracker provider can be set up in the <kbd>Preferences > Integrations</kbd> tab. And similar to the Pull Request section, issues can be filtered by created, assigned or mentioned, and labels.

<img src="/wp-content/uploads/issue-filters-launchpad-2025.png" srcset="/wp-content/uploads/issue-filters-launchpad-2025@2x.png" class="help-center-img img-bordered">

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