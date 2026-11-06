---
title: GitKraken Launchpad Overview
description: Learn how to track pull requests, issues, and WIPs using GitKraken Launchpad, including Personal and Team Views, integrations, filters, and saved views.
product: GitKraken Launchpad
feature: Launchpad
content_type: overview
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps, Jira Cloud, Jira Data Center]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps, Jira Cloud, Jira Data Center]
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [launchpad, pull-requests, issues, wip, filters]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "gitkraken-launchpad"
    nav_label: "Launchpad"
    nav_order: 90
    nav_parent: ""
    page_type: "content"
---
<kbd>Last updated: November 2026</kbd>

Use GitKraken Launchpad to monitor pull requests, issues, and works in progress (WIPs) across a selected Workspace or team. Use this page to open Launchpad, connect integrations, switch between Personal and Team Views, save filtered views, and check which features differ between Cloud and On-Premise environments.

<figure>
  <img src="/wp-content/uploads/launchpad-highlight-2025@2x.png"
       class="help-center-img img-bordered"
       alt="GitKraken Desktop Launchpad view showing a list of pull requests with unassigned reviewers on the left and detailed GitHub pull request panel open on the right.">
  <figcaption style="color:#888; text-align:center">
    Launchpad displaying a list of unassigned reviewers, with a PR open for more details
  </figcaption>
</figure>

Launchpad is also available in GitKraken On-Premise, with some differences. See <a href="#how-on-premise-launchpad-differs-from-cloud-launchpad">How On-Premise Launchpad differs from Cloud Launchpad</a>.

***

<div class='callout callout--warning'>
  <p><strong>GitKraken On-Premise users:</strong> Step 3 below requires a Cloud Workspace, which is not available in Serverless or Self-Hosted Server deployments. Skip step 3 and connect your on-premises integrations (GitHub Enterprise Server, GitLab Self-Managed, Bitbucket Server, Azure DevOps Server, or Jira Data Center) in <kbd>Preferences &gt; Integrations</kbd> instead. For a full description of Launchpad feature differences in on-premises environments, see <a href="#how-on-premise-launchpad-differs-from-cloud-launchpad">How On-Premise Launchpad differs from Cloud Launchpad</a>.</p>
</div>

## Quick Start


1. Click the **Launchpad** tab in the top-left corner of GitKraken Desktop.
2. Connect your integrations via <kbd>Preferences > Integrations</kbd>, or follow the in-app prompts.
3. Select a Cloud Workspace from the dropdown to filter activity to specific repositories.
4. Use the **Pull Requests**, **Issues**, **WIPs**, or **All** tabs to view relevant items.
5. Toggle between **Personal View** (items assigned to or created by you) and **Team View** (items from others) using the toggle in the top-right.

To prioritize items:
- Click the pin icon to keep a PR or issue at the top of the list.
- Click the snooze icon to hide an item temporarily. Snoozed items appear in the **Snoozed** tab.

To save a filtered view for reuse, click the **+** Save View icon in the Launchpad tab bar and name it. Saved views are tied to the mode (Personal or Team) in which they were created.

***

## How to get started with Launchpad

To open Launchpad:

1. Click the <strong>Launchpad</strong> tab in the top-left corner of GitKraken Desktop.
2. Connect your integrations via <kbd>Preferences > Integrations</kbd>, or follow the in-app prompts for specific providers.

The **Pull Requests** and **Issues** tabs require you to sign in to your GitKraken account. If you are signed out, these tabs show **Sign In to Use Launchpad** with **Sign Up** and **Sign In** buttons. The **WIPs**, **All**, and **Snoozed** tabs work without signing in.

<figure>
  <img src="/wp-content/uploads/open-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="User highlighting the rocket icon in GitKraken Desktop to open the Launchpad tab for managing pull requests and issues.">
  <figcaption style="color:#888; text-align:center">
    Accessing the Launchpad tab
  </figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/connect-integration-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="No pull requests found in GitKraken Launchpad with options to connect a pull request hosting service like GitHub, GitLab, Bitbucket, or Azure DevOps.">
  <figcaption style="color:#888; text-align:center">
    Connecting your integrations for PRs and Issues
  </figcaption>
</figure>

### How to set up Workspaces and integrations

Select a Cloud Workspace in Launchpad to see WIPs, issues, and PRs for that Workspace's repositories:

1. [Create a Cloud Workspace](/gitkraken-desktop/workspaces/#how-to-create-a-cloud-workspace).
2. Return to Launchpad and select the Workspace from the dropdown.

<figure>
  <img src="/wp-content/uploads/select-workspace-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="Dropdown menu in GitKraken Launchpad for selecting a Workspace to filter pull request and issue activity.">
  <figcaption style="color:#888; text-align:center">
    Selecting a Workspace to view associated activity
  </figcaption>
</figure>

Use the Launchpad tabs to choose what you see:

- **Pull Requests**: Open PRs in the selected Workspace's repositories.
- **Issues**: Active issues.
- **WIPs**: Repositories with uncommitted changes.
- **All**: Pull requests, issues, and WIPs together.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Cloud Workspaces are not available in GitKraken On-Premise. As a result, Launchpad does not show Cloud Workspace data in those environments. See <a href="#how-on-premise-launchpad-differs-from-cloud-launchpad">How On-Premise Launchpad differs from Cloud Launchpad</a>.</p>
</div>

Pin or snooze items to control what you see first:

- Click the <i class="fa-solid fa-thumbtack"></i> icon to pin PRs or issues to the top.
- Click the <i class="fa-solid fa-snooze"></i> icon to snooze a PR. Launchpad moves snoozed items to the <kbd>Snoozed</kbd> tab.

<figure>
  <img src="/wp-content/uploads/pin-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="User interface showing a pin icon in GitKraken Launchpad for marking pull requests under Suggested Changes.">
  <figcaption style="color:#888; text-align:center">
    Pin items to prioritize visibility
  </figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/snooze-tab-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="Interface showing snooze options in GitKraken Launchpad, allowing users to temporarily hide pull requests for 1 hour, 4 hours, or until the next day.">
  <figcaption style="color:#888; text-align:center">
    Manage snoozed pull requests and issues
  </figcaption>
</figure>


***

## How Personal View works

Personal View shows pull requests and issues that:

- You created
- Are assigned to you
- List you as a reviewer
- Mention you

<figure>
  <img src="/wp-content/uploads/gkc-launchpad-personal-team-10.0.0.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Launchpad interface showing a toggle between Personal and Team views for managing pull requests.">
  <figcaption style="color:#888; text-align:center">
    Toggle between Personal and Team View
  </figcaption>
</figure>

If you select **None** in the Workspace dropdown, Personal View still shows your items from all connected services.

## How Team View works

<div class='callout callout--warning'>
  <p><strong>Note:</strong> Team View requires an Advanced plan or higher. Team View depends on Cloud Workspaces, so it is not available in GitKraken On-Premise.</p>
</div>

Switch to Team View with the toggle in the top-right corner of Launchpad. Team View shows pull requests and issues that involve other people:

- Created by others
- Assigned to others
- With others listed as reviewers or mentioned

<figure>
  <img src="/wp-content/uploads/team-view-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Launchpad interface with the Team view selected, showing team-wide PR and issue filters.">
  <figcaption style="color:#888; text-align:center">
    Viewing team pull requests and issues
  </figcaption>
</figure>

Filter by user to see specific collaborators' activity.

<figure>
  <img src="/wp-content/uploads/filter-team-member-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="Launchpad filter menu showing GitKraken team members and external collaborators to narrow down pull request visibility.">
  <figcaption style="color:#888; text-align:center">
    Filter by contributor in Team View
  </figcaption>
</figure>

Team View shows your team's work across all repositories in the selected Workspace.

***

## How to save and reuse Launchpad views

You can save customized views by clicking the <i class="fa-solid fa-plus"></i> Save View icon in the Launchpad tab bar.

<figure>
  <img src="/wp-content/uploads/gkd-10-5-launchpad-save-view.gif" class="help-center-img img-bordered" alt="Saving a Launchpad view by entering a custom name and clicking 'Create View' in the GitKraken Launchpad interface">
  <figcaption style="color:#888; text-align:center">Save frequently used filters as a custom view</figcaption>
</figure>

To delete a saved view:

1. Select the view.
2. Navigate to <kbd>View Settings > Delete this view</kbd>.

A saved view appears only in the mode (Team or Personal) where you created it.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Saved Views are not available in GitKraken On-Premise clients.</p>
</div>


***

## How to work with pull requests in Launchpad

From Launchpad, you can take these actions on pull requests:

- Open PR in the browser
- View the repository
- Open Code Suggestions (if available)
- Review Pull Request, which opens the pull request in GitKraken Code Review on GitKraken.dev (GitHub, GitLab, and Azure DevOps pull requests; not available in GitKraken On-Premise)
- Checkout PR branch
- Close PR
- Checkout in New Worktree

Use **Checkout in New Worktree** when you want to review or continue pull request work in a separate working directory. For more information, see [Manage Git Worktrees in GitKraken Desktop](/gitkraken-desktop/worktrees/). If you want to use coding agents in those worktrees, see [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

<figure>
  <img src="/wp-content/uploads/pr-actions-launchpad-2025@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop Launchpad showing a pull request with dropdown menu options including 'Open in GitHub', 'Review Pull Request', 'Checkout Branch', and more.">
  <figcaption style="color:#888; text-align:center">Quick actions available for pull requests in Launchpad</figcaption>
</figure>

### What the pull request table columns mean

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
      <td>Timestamp of the most recent activity on the pull request.</td>
    </tr>
    <tr>
      <td>Status</td>
      <td>PR status (such as Open, Draft, or At Risk), review state, and build status.</td>
    </tr>
    <tr>
      <td>PR Title</td>
      <td>Pull request title with a link to the host, line diffs, and code suggestion indicators.</td>
    </tr>
    <tr>
      <td>Author(s)</td>
      <td>PR creators.</td>
    </tr>
    <tr>
      <td>Collaborators</td>
      <td>Contributors working on the pull request.</td>
    </tr>
    <tr>
      <td>Repository and Branch</td>
      <td>The repository and branch for the pull request.</td>
    </tr>
    <tr>
      <td>Actions</td>
      <td>Links to open the repo, view in browser, review PR, and more.</td>
    </tr>
  </tbody>
</table>

### How GitHub pull requests work in Launchpad

If your Workspace uses GitHub.com, click the **Open Pull Request Panel** icon in a pull request's row to see its details in Launchpad.

<figure>
  <img src="/wp-content/uploads/github-pr-view-launchpad.png" class="help-center-img img-bordered" alt="Launchpad Action column showing 'Open in GitHub' dropdown and icon button labeled 'Open Pull Request Panel'.">
  <figcaption style="color:#888; text-align:center">GitHub pull request details integrated in Launchpad</figcaption>
</figure>

## How to work with issues in Launchpad

Launchpad supports multiple issue trackers including Jira, GitHub Issues, Azure DevOps, and Trello.

To start a coding agent on an issue that has no linked branch:

1. Click **Start an Agent Session** in the issue's actions.
2. In the dialog, review the **Repository**, **Branch name**, **Base branch**, and **Coding agent**.
3. Leave **Send issue context to start immediately** selected (the default) to give the agent the issue's details so it can start working right away.

For more information, see [How to start an agent session from a work item](/gitkraken-desktop/agents/#how-to-start-an-agent-session-from-a-work-item).

<figure>
  <img src="/wp-content/uploads/issues-tab-launchpad-2025@2x.png" class="help-center-img img-bordered" alt="Launchpad Issues tab with filters for workspace, issue source, project, labels, and fix versions, displaying a list of issues and associated actions.">
  <figcaption style="color:#888; text-align:center">View and filter issues from connected services</figcaption>
</figure>

To customize your view:

- Switch providers from the Issues section dropdown.
- Connect integrations under <kbd>Preferences > Integrations</kbd>.
- Filter issues by creator, assignee, mentions, and labels.

<figure>
  <img src="/wp-content/uploads/issue-filters-launchpad-2025@2x.png" class="help-center-img img-bordered" alt="Launchpad Issues tab with filters for team member, workspace, issue source, project, labels, and fix versions, showing a list of issues and branch creation actions.">
  <figcaption style="color:#888; text-align:center">Use filters to target relevant issues</figcaption>
</figure>

## How to view works in progress in Launchpad

The **WIPs** tab shows uncommitted changes in the repositories of your selected Workspace.

To open a repository with changes, click <button class="button button--success button--ui button--nolink">View Repo</button> next to it.

## How the All tab works

The **All** tab combines pull requests, issues, and WIPs for all repositories in the selected Workspace.

## How the Snoozed tab works

The **Snoozed** tab lists the pull requests and issues you have snoozed. To unsnooze an item, click the <i class="fa-solid fa-snooze"></i> icon again.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Snoozing is available only with a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank" rel="noopener noreferrer">paid GitKraken subscription</a>.</p>
</div>

## How to filter by milestones and sprints

You can filter Launchpad issues and pull requests by:

- Jira Fix Versions and Sprints
- GitHub and GitLab Milestones

<figure>
  <img src="/wp-content/uploads/gkd-10-4-launchpad-jira-sprint-filter.gif" class="help-center-img img-bordered" alt="Launchpad user selecting a specific milestone from a dropdown filter labeled 'All milestones', showing options like '10.6 release', 'October refactor', and '10.5 release'.">
  <figcaption style="color:#888; text-align:center">Filter Launchpad by Jira or GitHub milestones</figcaption>
</figure>

## Launchpad summary

The status bar shows a Launchpad summary of your pull requests, grouped by status.

- Click the summary indicator to open Launchpad with the matching status group expanded.
- The summary uses the filters set in the Launchpad tab.

<figure>
  <img src="/wp-content/uploads/gkd-launchpad-summary.gif" class="help-center-img img-bordered" alt="GitKraken Desktop UI showing the commit graph, terminal, and Launchpad status bar listing pull request states like ready to merge, no assigned reviewers, and merge conflicts.">
  <figcaption style="color:#888; text-align:center">Launchpad status bar shows actionable pull requests</figcaption>
</figure>

## How On-Premise Launchpad differs from Cloud Launchpad

GitKraken On-Premise runs in isolated networks, so some cloud-based Launchpad features are not available:

| Feature | Cloud | On-Premise |
|--------|-------|------------|
| Cloud Workspaces | ✅ | ❌ |
| Snoozing/Pinning | ✅ | ❌ |
| Team View | ✅ | ❌ |
| Issue/PR Filtering | ✅ | ✅ |
| View Settings | ✅ | ✅ (unsaved only) |

<figure>
  <img src="/wp-content/uploads/launchpad-prs.png" class="help-center-img img-bordered" alt="GitKraken Desktop Launchpad showing a filtered view of 32 personal pull requests in an on-premise GitHub Enterprise Server environment, with options to clone or open each PR.">
  <figcaption style="color:#888; text-align:center">Launchpad in On-Premise with limited cloud features</figcaption>
</figure>
