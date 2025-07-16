---
title: GitKraken Desktop & Jira Issues Integration
description: Learn how to connect and manage Jira Issues in GitKraken Desktop. Preview, edit, and create issues, filter with JQL, and sync changes with Jira Cloud or Data Center.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: June 2025</kbd>

GitKraken Desktop makes it easy to integrate with Jira Cloud and Jira Data Center.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/On83cso-w3U" frameborder="0" allowfullscreen></iframe>
</div>

<div class='callout callout--basic'>
    <p>The Jira integration is view-only for Community users. To unlock full functionality, consider upgrading to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken subscription</a>.</p>
</div>

---

## Connect Jira Integration

Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>. If you do not see the ISSUES section, right-click on any Left Panel header and enable it from the context menu.

<img src="/wp-content/uploads/connect-jira-issues-2025.png" srcset="/wp-content/uploads/connect-jira-issues-2025@2x.png" class="help-center-img img-bordered" alt="Connecting Jira integration in GitKraken">

You will be redirected to an Atlassian page to authorize the connection. Click <em>Accept</em> to proceed.

<img src="/wp-content/uploads/connect-atlassian-2025.png" srcset="/wp-content/uploads/connect-atlassian-2025@2x.png" class="help-center-img img-bordered" alt="Atlassian OAuth prompt for Jira integration">

Alternatively, you may copy the token from the _Success_ page and paste it into the Jira Cloud integration screen in GitKraken Desktop.

---

## Preview Jira Issues

Once connected, your Jira issues will appear in the Left Panel. By default, the app displays issues assigned to you under the _My Issues_ filter.

<img src="/wp-content/uploads/preview-jira-issues-2025.png" srcset="/wp-content/uploads/preview-jira-issues-2025@2x.png" class="help-center-img img-bordered" alt="Preview of Jira issues in the Left Panel">

Hover over any issue to preview key details including Title, Description, Status, Assignee, and Reporter.

<img src="/wp-content/uploads/hover-issue-2025.png" srcset="/wp-content/uploads/hover-issue-2025@2x.png" class="help-center-img img-bordered" alt="Issue preview tooltip in GitKraken">

---

## View Jira Issue Details

Click an issue to open its detail view.

<img src="/wp-content/uploads/jira-issue-view.png" srcset="/wp-content/uploads/jira-issue-view@2x.png" class="help-center-img img-bordered" alt="Jira issue detail view">

You can:

- Edit Title and Description
- Change Status
- Assign or reassign
- Add comments

These changes will sync with your Jira board.

---

## Create a New Jira Issue

From the Left Panel, click the <code>+</code> icon to add a new Jira issue.

<img src="/wp-content/uploads/create-jira-issue-2025.png" srcset="/wp-content/uploads/create-jira-issue-2025@2x.png" class="help-center-img img-bordered" alt="Create new Jira issue from GitKraken">

The issue will sync directly with your connected Jira project.

---

## Create Filters

You can create filters to show specific issues. The integration supports Atlassian’s JQL (Jira Query Language) and provides auto-complete for filter fields.

<img src="/wp-content/uploads/create-jira-filter-2025.png" srcset="/wp-content/uploads/create-jira-filter-2025@2x.png" class="help-center-img img-bordered" alt="Creating a JQL filter in GitKraken">

For advanced filtering tips, see Atlassian’s [JQL guide](https://www.atlassian.com/software/jira/guides/expand-jira/jql#visualize-results).

---

## Create Branches from Issues

You can create branches tied to Jira issues directly from the issue detail view.

<img src="/wp-content/uploads/create-branch-jira-integration.gif" class="help-center-img img-bordered" alt="Creating a branch from Jira issue view">

The branch name is prefilled based on the issue title. After creation, branches linked to Jira issues display the Jira icon.

---

## Copy Issue Link or View in Jira

Click the <kbd><i class="fa fa-ellipsis-v"></i></kbd> icon on an issue card to copy the issue link or open it directly in Jira.

<img src="/wp-content/uploads/view-jira-issue-2025.png" srcset="/wp-content/uploads/view-jira-issue-2025@2x.png" class="help-center-img img-bordered" alt="Options to copy or view Jira issue">

---

## More Integration Options

For more powerful features between GitKraken and Jira, check out <a href="/integrations/git-integration-for-jira">Git Integration for Jira</a>.
