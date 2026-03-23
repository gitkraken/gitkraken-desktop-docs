---
title: GitKraken Desktop & Jira Data Center Issues Integration
description: Learn how to connect Jira Data Center with GitKraken Desktop. Use Personal Access Tokens to manage, preview, create, and sync Jira issues from within your Git workflow.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to Jira Data Center so you can preview, create, and manage Jira issues from the Left Panel. This integration requires an Advanced subscription tier or higher, supports Jira Data Center 8.4 or newer, and uses a Personal Access Token instead of the Jira Cloud authorization flow.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/On83cso-w3U" frameborder="0" allowfullscreen></iframe>
</div>

---

## Requirements

<div class='callout callout--warning'>
    <p>This integration is only available for <a href="https://www.gitkraken.com/pricing" target="_blank">Advanced subscription tiers</a> or higher.</p>
</div>

<div class='callout callout--basic'>
    <p>The Jira Data Center integration requires Jira version 8.4 or newer. Some SSO (single sign-on) configurations are not supported.</p>
</div>

---

## Quick Start

Connect GitKraken Desktop to Jira Data Center to view and manage issues from your Git workflow.

1. Go to <kbd>Preferences > Integrations</kbd> or open the **ISSUES** section in the Left Panel.
2. Enter your Jira Data Center host domain and a Personal Access Token from your Jira instance.
3. Once connected, preview issues, open issue details, create issues, and create issue-based branches using the same workflows documented for Jira.

---

## How to connect Jira Data Center

Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>. If you don't see the ISSUES section, right-click any header in the Left Panel and enable it from the context menu.

<img src="/wp-content/uploads/connect-jira-dc-issues-2025@2x.png" class="help-center-img img-bordered" alt="Open Jira Data Center integration settings">

Enter your Host Domain URL and a Personal Access Token generated in your Jira Data Center instance.

<img src="/wp-content/uploads/connect-jira-dc-2025@2x.png" class="help-center-img img-bordered" alt="Enter domain and access token for Jira Data Center">

Once connected, GitKraken Desktop will confirm the integration.

<img src="/wp-content/uploads/connected-jira-dc-2025@2x.png" class="help-center-img img-bordered" alt="Successful Jira Data Center connection">

---

## What the Jira Data Center integration supports

The Jira Data Center integration includes the same functionality as the Jira Cloud integration:

- [Preview Jira Issues](/integrations/jira/#preview-jira-issues)
- [View Jira Issue Details](/integrations/jira/#view-jira-issue-details)
- [Create New Jira Issue](/integrations/jira/#create-new-jira-issue)
- [Create Filters](/integrations/jira/#create-filters)
- [Create Branch from Issue](/integrations/jira/#create-branches-from-issue)
- [Copy Issue link or View in Jira](/integrations/jira/#copy-issue-link-or-view-in-jira)

For more information on each feature, refer to the [Jira Cloud integration guide](/integrations/jira).
