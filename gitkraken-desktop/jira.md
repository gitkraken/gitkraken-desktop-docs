---

title: GitKraken Desktop and Jira Issues Integration
description: Learn how to access Jira Issues from GitKraken Desktop
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

GitKraken Desktop makes it easy to integrate with Jira Cloud and Jira Data Center.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/On83cso-w3U" frameborder="0" allowfullscreen></iframe>
</div>

<div class='callout callout--basic'>
    <p>The Jira integration is view-only for Community users. To unlock all features for the Jira integration, consider upgrading to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken subscription</a>.</p>
</div>
***

### Connect Jira Integration

Set up the integration from the ISSUES pane in the Left Panel or from <kbd><i>Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>. If you do not see the ISSUES pane, right-click on any Left Panel header to access the context menu and check the option for Issues.

<img src="/wp-content/uploads/connect-jira-issues-2025.png" srcset="/wp-content/uploads/connect-jira-issues-2025@2x.png" class="help-center-img img-bordered">

You will then be prompted by an Atlassian page to allow GitKraken Desktop to connect to your Jira account. Hit <em>Accept</em> to proceed.

<img src="/wp-content/uploads/connect-atlassian-2025.png" srcset="/wp-content/uploads/connect-atlassian-2025@2x.png" class="help-center-img img-bordered">

Alternatively, you may copy the token from the _Success_ page and paste it into the Jira Cloud integration page inside GitKraken Desktop.

***

### Preview Jira Issues

Once connected, your Jira issues will start to appear in the Left Panel. The app will default to a _My Issues_ filter which will show issues assigned to you.

<img src="/wp-content/uploads/preview-jira-issues-2025.png" srcset="/wp-content/uploads/preview-jira-issues-2025@2x.png" class="help-center-img img-bordered">

Hover over any issue to get a preview of the issue Title, Description, Status, Assignee, and Reporter.

<img src="/wp-content/uploads/hover-issue-2025.png" srcset="/wp-content/uploads/hover-issue-2025@2x.png" class="help-center-img img-bordered">

***

### View Jira Issue Details

Click to select an issue to view the issue details.

<img src="/wp-content/uploads/jira-issue-view.png" srcset="/wp-content/uploads/jira-issue-view@2x.png" class="help-center-img img-bordered">

Here you may view and edit:

 - Title and Description
 - Status
 - Assignee
 - Add comments

Any changes made here will be reflected in your Jira board.

***

### Create New Jira Issue

From the Left Panel, click the <button class='button button--success button--ui button--nolink'>+</button> icon to add a new Jira issue.

<img src="/wp-content/uploads/create-jira-issue-2025.png" srcset="/wp-content/uploads/create-jira-issue-2025@2x.png" class="help-center-img img-bordered">

Your new issue will automatically sync with your Jira project.

***

### Create Filters

You may create filters to view the issues you need. Atlassian uses JQL syntax for filters, and the integration will help you auto-complete your filter fields.

<img src="/wp-content/uploads/create-jira-filter-2025.png" srcset="/wp-content/uploads/create-jira-filter-2025@2x.png" class="help-center-img img-bordered">

However for more details about how to write your JQL filters, please refer to the [Get started with Advanced Search and JQL](https://www.atlassian.com/software/jira/guides/expand-jira/jql#visualize-results) guide by Atlassian.

***

### Create Branches from Issue

You may create a branches tied to an issue from the issue details view.

<img src="/wp-content/uploads/create-branch-jira-integration.gif" class="help-center-img img-bordered">

The branch name will automatically prefill based on the issue name. After the branch is created, these branches will be denoted with the Jira icon to reflect its link to a Jira issue.

From here, it should be possible to configure triggers on the Jira side for changes made to this branch.

***

### Copy Issue link or View in Jira

Click the <kbd> <i class="fa fa-ellipsis-v"></i> </kbd> icon to copy the issue link or view the item directly in Jira.

<img src="/wp-content/uploads/view-jira-issue-2025.png" srcset="/wp-content/uploads/view-jira-issue-2025@2x.png" class="help-center-img img-bordered">

### Git Integration for Jira

For even more goodness between GitKraken and Jira, check out our additional integration features with <a href="/integrations/git-integration-for-jira">Git Integration for Jira</a>.
