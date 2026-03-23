---
title: GitKraken Desktop & Jira Issues Integration
description: Learn how to connect and manage Jira Issues in GitKraken Desktop. Preview, edit, and create issues, filter with JQL, and sync changes with Jira Cloud or Data Center.
product: GitKraken Desktop
feature: Jira Issues Integration
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [Jira Cloud, Jira Data Center]
integrations: [Jira Cloud, Jira Data Center]
hosted_variant: both
status: GA
last_verified: 2026-03
llms_include: true
tags: [jira, issues, jql, branching, integration]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to Jira Cloud or Jira Data Center so you can preview, create, edit, filter, and branch from Jira issues alongside your repository work. Jira is view-only for Community users, while paid GitKraken subscriptions unlock the full issue management workflow.

**Requirements and limits**
- Integrations covered here: Jira Cloud and Jira Data Center
- Community plan: View-only access
- Full issue workflows: Paid GitKraken subscription required for create, edit, and branch workflows
- Filter syntax: Uses JQL for custom Jira issue filters
- Data Center note: Jira Data Center uses a Personal Access Token flow instead of the Jira Cloud authorization flow

| Variant | Auth flow | Community access | Full edit support | Filter syntax |
|---------|-----------|------------------|-------------------|---------------|
| Jira Cloud | Atlassian browser authorization flow | View-only | Paid GitKraken subscription required | JQL |
| Jira Data Center | Personal Access Token | View-only | Paid GitKraken subscription required | JQL |

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/On83cso-w3U" frameborder="0" allowfullscreen></iframe>
</div>

<div class='callout callout--basic'>
    <p>The Jira integration is view-only for Community users. To unlock full functionality, consider upgrading to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken subscription</a>.</p>
</div>

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> or click the ISSUES section in the Left Panel. If the ISSUES section is not visible, right-click any Left Panel header and enable it.
2. Select **Jira Cloud** or **Jira Data Center** and click to authorize. Complete the authorization in the Atlassian browser page that opens.
3. Once connected, your Jira issues appear in the Left Panel under the _My Issues_ filter by default.

**To view and edit issue details:** Click any issue to open its detail view. You can edit the title, description, status, and assignee. Changes sync with your Jira board.

**To create a new issue:** Click the **+** icon in the Left Panel, fill in the required fields, and submit. The issue syncs to Jira automatically.

**To create a branch from an issue:** Open the issue detail view and click **Create a branch for this issue**. The branch name is pre-filled from the issue title.

**To use JQL filters:** Use the filter syntax in the Left Panel to narrow issues by project, label, sprint, or status.

---

## How to connect the Jira integration

Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>. If you do not see the ISSUES section, right-click on any Left Panel header and enable it from the context menu.

<div class='callout callout--basic'>
    <p><strong>Use Jira Cloud on this page when:</strong> your organization uses Atlassian's hosted Jira authorization flow. <strong>Use Jira Data Center instead when:</strong> your team runs self-hosted Jira and needs PAT-based setup with Data Center-specific compatibility.</p>
</div>

<img src="/wp-content/uploads/connect-jira-issues-2025@2x.png" class="help-center-img img-bordered" alt="Connecting Jira integration in GitKraken">

You will be redirected to an Atlassian page to authorize the connection. Click <em>Accept</em> to proceed.

<img src="/wp-content/uploads/connect-atlassian-2025@2x.png" class="help-center-img img-bordered" alt="Atlassian OAuth prompt for Jira integration">

Alternatively, you may copy the token from the _Success_ page and paste it into the Jira Cloud integration screen in GitKraken Desktop.

---

## How to preview Jira issues

Once connected, your Jira issues will appear in the Left Panel. By default, the app displays issues assigned to you under the _My Issues_ filter.

<img src="/wp-content/uploads/preview-jira-issues-2025@2x.png" class="help-center-img img-bordered" alt="Preview of Jira issues in the Left Panel">

Hover over any issue to preview key details including Title, Description, Status, Assignee, and Reporter.

<img src="/wp-content/uploads/hover-issue-2025@2x.png" class="help-center-img img-bordered" alt="Issue preview tooltip in GitKraken">

---

## How to view Jira issue details

Click an issue to open its detail view.

<img src="/wp-content/uploads/jira-issue-view@2x.png" class="help-center-img img-bordered" alt="Jira issue detail view">

You can:

- Edit Title and Description
- Change Status
- Assign or reassign
- Add comments

These changes will sync with your Jira board.

---

## How to create a new Jira issue

From the Left Panel, click the <code>+</code> icon to add a new Jira issue.

<img src="/wp-content/uploads/create-jira-issue-2025@2x.png" class="help-center-img img-bordered" alt="Create new Jira issue from GitKraken">

The issue will sync directly with your connected Jira project.

---

## How to create Jira filters

You can create filters to show specific issues. The integration supports Atlassian’s JQL (Jira Query Language) and provides auto-complete for filter fields.

<div class='callout callout--basic'>
    <p><strong>Use JQL filters when:</strong> you need focused issue queues by project, sprint, assignee, or status. <strong>Don't rely only on the default My Issues view when:</strong> your workflow depends on a more specific slice of Jira work.</p>
</div>

<img src="/wp-content/uploads/create-jira-filter-2025@2x.png" class="help-center-img img-bordered" alt="Creating a JQL filter in GitKraken">

For advanced filtering tips, see Atlassian’s [JQL guide](https://www.atlassian.com/software/jira/guides/expand-jira/jql#visualize-results).

---

## How to create branches from Jira issues

You can create branches tied to Jira issues directly from the issue detail view.

<div class='callout callout--basic'>
    <p><strong>Use issue-based branch creation when:</strong> one branch should map directly to one Jira issue. <strong>Don't use it when:</strong> the branch spans several tickets or the auto-filled issue-based name is not the branch structure you need.</p>
</div>

<img src="/wp-content/uploads/create-branch-jira-integration.gif" class="help-center-img img-bordered" alt="Creating a branch from Jira issue view">

The branch name is prefilled based on the issue title. After creation, branches linked to Jira issues display the Jira icon.

---

## How to copy an issue link or open it in Jira

Click the <kbd><i class="fa fa-ellipsis-v"></i></kbd> icon on an issue card to copy the issue link or open it directly in Jira.

<img src="/wp-content/uploads/view-jira-issue-2025@2x.png" class="help-center-img img-bordered" alt="Options to copy or view Jira issue">

---

## More Jira integration options

For more powerful features between GitKraken and Jira, check out <a href="/integrations/git-integration-for-jira">Git Integration for Jira</a>.
