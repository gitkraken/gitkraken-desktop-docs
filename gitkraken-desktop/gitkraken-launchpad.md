---
title: GitKraken Launchpad Overview
description: Learn how to track pull requests, issues, and WIPs using GitKraken Launchpad, including Personal and Team Views, integrations, filters, and saved views.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

Launchpad provides a unified overview of your Pull Requests, Issues, and Works In Progress (WIPs) for your selected Workspace or collaborators. Use it to monitor your personal tasks and your team’s contributions in one place.

<figure>
  <img src="/wp-content/uploads/launchpad-highlight-2025.png" 
       srcset="/wp-content/uploads/launchpad-highlight-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop Launchpad view showing a list of pull requests with unassigned reviewers on the left and detailed GitHub pull request panel open on the right.">
  <figcaption style="color:#888; text-align:center">
    Launchpad displaying a list of unassigned reviewers, with a PR open for more details
  </figcaption>
</figure>

The Launchpad is also <a href="https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/#elementor-toc__heading-anchor-13">available for GitKraken On-Premise</a> customers with some feature variations.

***

## Getting Started

To open Launchpad:

1. Click the <strong>Launchpad</strong> tab in the top-left corner of GitKraken Desktop.
2. Connect your integrations via <kbd>Preferences > Integrations</kbd>, or follow the in-app prompts for specific providers.

<figure>
  <img src="/wp-content/uploads/open-launchpad-2025.png" 
       srcset="/wp-content/uploads/open-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="User highlighting the rocket icon in GitKraken Desktop to open the Launchpad tab for managing pull requests and issues.">
  <figcaption style="color:#888; text-align:center">
    Accessing the Launchpad tab
  </figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/connect-integration-launchpad-2025.png" 
       srcset="/wp-content/uploads/connect-integration-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="No pull requests found in GitKraken Launchpad with options to connect a pull request hosting service like GitHub, GitLab, Bitbucket, or Azure DevOps.">
  <figcaption style="color:#888; text-align:center">
    Connecting your integrations for PRs and Issues
  </figcaption>
</figure>

### Set Up Workspaces and Integrations

Launchpad works best when connected to at least one Workspace. To set this up:

1. [Create a Cloud Workspace](https://help.gitkraken.com/gitkraken-desktop/workspaces/#cloud-workspaces/)
2. Return to the Launchpad to view filtered WIPs, Issues, and PRs across selected repositories.

<figure>
  <img src="/wp-content/uploads/select-workspace-launchpad-2025.png" 
       srcset="/wp-content/uploads/select-workspace-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="Dropdown menu in GitKraken Launchpad for selecting a Workspace to filter pull request and issue activity.">
  <figcaption style="color:#888; text-align:center">
    Selecting a Workspace to view associated activity
  </figcaption>
</figure>

You can filter by:

- **Pull Requests**: Displays open PRs in selected Workspace repositories.
- **Issues**: Shows active issues.
- **WIPs**: Lists repositories with uncommitted changes.
- **All**: Displays a unified view of all three above.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Cloud Workspaces are not available in GitKraken On-Premise. As a result, Launchpad will not show Cloud Workspace-related data in those environments. <a href="https://help.gitkraken.com/gitkraken-desktop/gitkraken-launchpad/#elementor-toc__heading-anchor-13">Learn more.</a></p>
</div>

Pinned and snoozed items help prioritize what you see first:

- Click the <i class="fa-solid fa-thumbtack"></i> icon to pin PRs or issues to the top.
- Click the <i class="fa-solid fa-snooze"></i> icon to snooze a PR. Snoozed items are moved to the <kbd>Snoozed</kbd> tab.

<figure>
  <img src="/wp-content/uploads/pin-launchpad-2025.png" 
       srcset="/wp-content/uploads/pin-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="User interface showing a pin icon in GitKraken Launchpad for marking pull requests under Suggested Changes.">
  <figcaption style="color:#888; text-align:center">
    Pin items to prioritize visibility
  </figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/snooze-tab-launchpad-2025.png" 
       srcset="/wp-content/uploads/snooze-tab-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="Interface showing snooze options in GitKraken Launchpad, allowing users to temporarily hide pull requests for 1 hour, 4 hours, or until the next day.">
  <figcaption style="color:#888; text-align:center">
    Manage snoozed pull requests and issues
  </figcaption>
</figure>


***

## Personal View

Personal View displays items where you're directly involved:

- PRs/issues created by you
- Assigned to you
- You're listed as a reviewer
- You are mentioned

<figure>
  <img src="/wp-content/uploads/gkc-launchpad-personal-team-10.0.0.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Launchpad interface showing a toggle between Personal and Team views for managing pull requests.">
  <figcaption style="color:#888; text-align:center">
    Toggle between Personal and Team View
  </figcaption>
</figure>

If you select "None" in the Workspace dropdown, you'll still see items related to your user identity across all connected services.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> Team View is not available for GitKraken On-Premise due to its dependency on Cloud Workspaces. Team View is available for Advanced plans and above.</p>
</div>

## Team View

Switch to Team View using the toggle in the top-right corner of Launchpad. Team View displays items not associated with your user account:

- Created by others
- Assigned to others
- Others are listed as reviewers or mentioned

<figure>
  <img src="/wp-content/uploads/team-view-launchpad-2025.png" 
       srcset="/wp-content/uploads/team-view-launchpad-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="GitKraken Launchpad interface with the Team view selected, showing team-wide PR and issue filters.">
  <figcaption style="color:#888; text-align:center">
    Viewing team pull requests and issues
  </figcaption>
</figure>

You can filter by user to focus on specific collaborators’ activity.

<figure>
  <img src="/wp-content/uploads/filter-team-member-2025.png" 
       srcset="/wp-content/uploads/filter-team-member-2025@2x.png" 
       class="help-center-img img-bordered" 
       alt="Launchpad filter menu showing GitKraken team members and external collaborators to narrow down pull request visibility.">
  <figcaption style="color:#888; text-align:center">
    Filter by contributor in Team View
  </figcaption>
</figure>

Team View provides a high-level look at your team's current efforts across all repositories in the selected Workspace.

***

## Saved Views

You can save customized views by clicking the <i class="fa-solid fa-plus"></i> Save View icon in the Launchpad tab bar.

<figure>
  <img src="/wp-content/uploads/gkd-10-5-launchpad-save-view.gif" class="help-center-img img-bordered" alt="Saving a Launchpad view by entering a custom name and clicking 'Create View' in the GitKraken Launchpad interface">
  <figcaption style="color:#888; text-align:center">Save frequently used filters as a custom view</figcaption>
</figure>

To delete a saved view:

1. Select the view.
2. Navigate to <kbd>View Settings > Delete this view</kbd>.

Note that saved views are only visible when you’re in the same mode (Team or Personal) in which they were created.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Saved Views are not available in GitKraken On-Premise clients.</p>
</div>


***

## Pull Requests

From Launchpad, you can quickly take action on pull requests:

- Open PR in the browser
- View the repository
- Open Code Suggestions (if available)
- Review pull request (GitHub only)
- Checkout PR branch
- Close PR
- Checkout in new worktree

<figure>
  <img src="/wp-content/uploads/pr-actions-launchpad-2025.png" srcset="/wp-content/uploads/pr-actions-launchpad-2025@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop Launchpad showing a pull request with dropdown menu options including 'Open in GitHub', 'Review Pull Request', 'Checkout Branch', and more.">
  <figcaption style="color:#888; text-align:center">Quick actions available for pull requests in Launchpad</figcaption>
</figure>

### Pull Request Table Columns

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
      <td>PR status (e.g., Open, Draft, At Risk), review state, and build status.</td>
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
      <td>Displays the repository and branch for the pull request.</td>
    </tr>
    <tr>
      <td>Actions</td>
      <td>Links to open the repo, view in browser, review PR, and more.</td>
    </tr>
  </tbody>
</table>

### GitHub Pull Requests

If your Workspace uses GitHub.com, you can view PRs directly in Launchpad’s GitHub pull request interface.

<figure>
  <img src="/wp-content/uploads/github-pr-view-launchpad.png" class="help-center-img img-bordered" alt="Launchpad Action column showing 'Open in GitHub' dropdown and icon button labeled 'Open Pull Request Panel'.">
  <figcaption style="color:#888; text-align:center">GitHub pull request details integrated in Launchpad</figcaption>
</figure>

## Issues

Launchpad supports multiple issue trackers including Jira, GitHub Issues, Azure DevOps, and Trello.

<figure>
  <img src="/wp-content/uploads/issues-tab-launchpad-2025.png" srcset="/wp-content/uploads/issues-tab-launchpad-2025@2x.png" class="help-center-img img-bordered" alt="Launchpad Issues tab with filters for workspace, issue source, project, labels, and fix versions, displaying a list of issues and associated actions.">
  <figcaption style="color:#888; text-align:center">View and filter issues from connected services</figcaption>
</figure>

To customize your view:

- Switch providers from the Issues section dropdown.
- Connect integrations under <kbd>Preferences > Integrations</kbd>.
- Filter issues by creator, assignee, mentions, and labels.

<figure>
  <img src="/wp-content/uploads/issue-filters-launchpad-2025.png" srcset="/wp-content/uploads/issue-filters-launchpad-2025@2x.png" class="help-center-img img-bordered" alt="Launchpad Issues tab with filters for team member, workspace, issue source, project, labels, and fix versions, showing a list of issues and branch creation actions.">
  <figcaption style="color:#888; text-align:center">Use filters to target relevant issues</figcaption>
</figure>

## WIPs

The WIPs section shows uncommitted changes in the repositories of your selected Workspace. 

To view a repository with changes:

- Click <button class="button button--success button--ui button--nolink">View Repo</button> next to the listing.

## All

The All tab combines Pull Requests, Issues, and WIPs for all repositories in the selected Workspace, giving a unified snapshot of ongoing work.

## Snoozed

The Snoozed tab lists all pull requests and issues you've chosen to hide temporarily.

- Click the <i class="fa-solid fa-snooze"></i> icon again to unsnooze an item.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Snoozing is available only with a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank" rel="noopener noreferrer">paid GitKraken subscription</a>.</p>
</div>

## Filter by Milestones and Sprints

Launchpad allows you to filter issues and pull requests by:

- Jira Fix Versions and Sprints
- GitHub and GitLab Milestones

<figure>
  <img src="/wp-content/uploads/gkd-10-4-launchpad-jira-sprint-filter.gif" class="help-center-img img-bordered" alt="Launchpad user selecting a specific milestone from a dropdown filter labeled 'All milestones', showing options like '10.6 release', 'October refactor', and '10.5 release'.">
  <figcaption style="color:#888; text-align:center">Filter Launchpad by Jira or GitHub milestones</figcaption>
</figure>

## Launchpad Summary

Your most important pull requests are summarized in the status bar.

- Click the summary indicator to open Launchpad with the matching status group expanded.
- Results reflect current filters set in the Launchpad tab.

<figure>
  <img src="/wp-content/uploads/gkd-launchpad-summary.gif" class="help-center-img img-bordered" alt="GitKraken Desktop UI showing the commit graph, terminal, and Launchpad status bar listing pull request states like ready to merge, no assigned reviewers, and merge conflicts.">
  <figcaption style="color:#888; text-align:center">Launchpad status bar shows actionable pull requests</figcaption>
</figure>

## On-Premise vs. Cloud Launchpad

GitKraken On-Premise respects network isolation, which limits certain cloud-based features.

| Feature | Cloud | On-Premise |
|--------|-------|------------|
| Cloud Workspaces | ✅ | ❌ |
| Snoozing/Pinning | ✅ | ❌ |
| Team Launchpad | ✅ | ❌ |
| Issue/PR Filtering | ✅ | ✅ |
| View Settings | ✅ | ✅ (unsaved only) |

<figure>
  <img src="/wp-content/uploads/launchpad-prs.png" class="help-center-img img-bordered" alt="GitKraken Desktop Launchpad showing a filtered view of 32 personal pull requests in an on-premise GitHub Enterprise Server environment, with options to clone or open each PR.">
  <figcaption style="color:#888; text-align:center">Launchpad in On-Premise with limited cloud features</figcaption>
</figure>

This local-only experience is ideal for teams requiring full network control.

***

## Launchpad Changelog

Stay up to date with recent enhancements.

<table style="border-collapse: collapse; width: 100%; font-size: 90%;">
  <thead>
    <tr>
      <th style="text-align: left; padding: 4px;">Version</th>
      <th style="text-align: left; padding: 4px;">Change</th>
    </tr>
  </thead>
  <tbody>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-5-0">10.5</a></td><td>Add Saved Views</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-4-0">10.4</a></td><td>Added time-based filters</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-3-0">10.3</a></td><td>Filter Launchpad by PR and Issue labels</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-2-0">10.2</a></td><td>Add Team Launchpad (Preview)</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/10x/#version-10-1-0">10.1</a></td><td>Added Launchpad Status Bar</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-12-0">10.0</a></td><td>Focus View renamed to Launchpad</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-12-0">9.12</a></td><td>Focus View gets its own tab</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-11-0">9.11</a></td><td>Add PR actions to Focus View</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-9-0">9.9</a></td><td>Add pin and snooze support</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-8-0">9.8</a></td><td>Redesigned Focus View</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-5-0">9.5</a></td><td>Invite others to Workspace</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-4-0">9.4</a></td><td>Support Azure projects</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-3-0">9.3</a></td><td>Support Azure Issues</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-2-0">9.2</a></td><td>Start branch from issue</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/9x/#version-9-0-0">9.0</a></td><td>Added Cloud and Local Workspaces, Rename Overview to Focus View</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#wednesday-september-7th-2022">8.9</a></td><td>Add Team Overview</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#workspace-updates-overview">8.8</a></td><td>Add Workspace Overview</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-6-0">8.6</a></td><td>Add support for Bitbucket Server</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#tuesday-may-17th-2022">8.5</a></td><td>Add Workspace support for Azure DevOps</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#version-8-4-0">8.4</a></td><td>Pull Request View added to Workspaces</td></tr>
    <tr><td><a href="https://help.gitkraken.com/gitkraken-desktop/8x/#monday-december-13th-2021">8.2</a></td><td>Workspaces introduced</td></tr>
  </tbody>
</table>
