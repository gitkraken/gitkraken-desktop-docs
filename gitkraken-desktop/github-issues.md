---
title: GitKraken Desktop + GitHub Issues Integration
description: Learn how to connect GitKraken Desktop with GitHub Issues to manage, filter, preview, and create issues directly from your Git workflow.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to GitHub Issues so you can preview, create, edit, filter, and branch from issues alongside your repository work. GitHub Issues uses the same GitHub integration connection, and Community users are limited to public repositories.

<div class='callout callout--basic'>
    <p>The GitHub Issues integration is limited to public repositories for Community users. To unlock full access, consider upgrading to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken license</a>.</p>
</div>

**Requirements and limits**
- Integration covered here: GitHub Issues for GitHub.com
- Connection model: Shares the same connection as the GitHub integration
- Community plan: Public repositories only
- Issue workflows: Preview, create, edit, filter, and branch from issues after connecting GitHub
- Filter syntax: Uses GitHub issue filtering syntax for custom filters

***

## Quick Start

Connect GitKraken Desktop to GitHub Issues to view, create, and manage issues alongside your repository workflow.

1. Go to <kbd>Preferences > Integrations</kbd> and select **GitHub.com**, or click the ISSUES section in the Left Panel.
2. Click **Connect to GitHub** and complete authorization in the browser window that opens.
3. Once connected, your GitHub issues appear in the Left Panel under default filters such as _My Open Issues_ and _All Open Issues_.

**To view issue details:** Click any issue in the Left Panel to open its detail view. Changes made here sync with GitHub.

**To create a new issue:** Click the **+** icon in the Left Panel, fill in the required fields, and submit. The issue syncs directly to GitHub.

**To create a branch from an issue:** Open the issue detail view and click **Create a branch for this issue**. The branch name is pre-filled from the issue title.

**To create custom filters:** Use GitHub's issue filter syntax to build filters in the Left Panel and narrow your view to specific labels, statuses, or assignees.

To open an issue in GitHub or copy its link, use the ellipsis menu or the external link icon in the issue detail view.

---

## How to connect the GitHub Issues integration

The GitHub and GitHub Issues integrations share the same connection.

<div class='callout callout--basic'>
    <p><strong>Use GitHub Issues in GitKraken Desktop when:</strong> you want issue triage and branch creation directly beside your Git workflow. <strong>Don't use the in-app view alone when:</strong> you need broader GitHub project or issue-management features outside the issue flows covered here.</p>
</div>

You can set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>.

<img src="/wp-content/uploads/connect-github-issues-2025@2x.png" class="help-center-img img-bordered" alt="Connect GitHub Issues from Preferences">

From the Integrations window, select <em>GitHub.com</em> and click <strong>Connect to GitHub</strong>.

<img src="/wp-content/uploads/connect-github-2025@2x.png" class="help-center-img img-bordered" alt="Connect to GitHub prompt">

A browser window will open to complete authorization. Log in with your GitHub credentials and click <strong>Continue authorization</strong>.

Once successful, GitKraken will show a confirmation message and enable the integration.

<img src="/wp-content/uploads/github-success-1@2x.png" class="help-center-img img-bordered" alt="Successful GitHub integration">

---

## How to preview GitHub issues

After connecting, your GitHub issues will appear in the Left Panel. Default filters include _My Open Issues_ and _All Open Issues_. You can customize or remove these as needed.

<img src="/wp-content/uploads/github-issues-left-panel-2025@2x.png" class="help-center-img img-bordered" alt="GitHub Issues in Left Panel">

Hover over an issue to preview the title, description, status, labels, assignees, and reporter.

<img src="/wp-content/uploads/issues-preview-github-issues@2x.png" class="help-center-img img-bordered" alt="Issue preview tooltip">

---

## How to view and edit GitHub issue details

Click an issue to open the details view.

<img src="/wp-content/uploads/view-github-issue-2025@2x.png" class="help-center-img img-bordered" alt="GitHub Issue Details View">

Any changes made here will be synced with GitHub.

---

## How to create a new GitHub issue

To create a new issue, click the <code>+</code> icon from the Left Panel.

<img src="/wp-content/uploads/create-github-issue-2025@2x.png" class="help-center-img img-bordered" alt="Create new GitHub issue">

Required fields are marked with <code>*</code>. Your issue will sync directly to your GitHub repository.

---

## How to create GitHub issue filters

Create filters using GitHub's issue filter syntax. These help narrow your view to specific issue types, labels, or statuses.

<div class='callout callout--basic'>
    <p><strong>Use custom filters when:</strong> you need to focus on a subset of issues such as bugs, assigned work, or open review blockers. <strong>Don't rely only on default filters when:</strong> they leave you with too much issue noise.</p>
</div>

<img src="/wp-content/uploads/create-github-filter@2x.png" class="help-center-img img-bordered" alt="Create GitHub issue filter">

Refer to GitHub’s [issue filtering guide](https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests) for syntax examples.

---

## How to create branches from GitHub issues

From the issue details view, click <strong>Create a branch for this issue</strong>. You can also right-click an issue or use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu.

<div class='callout callout--basic'>
    <p><strong>Use issue-based branch creation when:</strong> you want a clear branch-to-issue link and an auto-filled branch name. <strong>Don't use it when:</strong> the branch should represent a larger initiative or combine work from multiple issues.</p>
</div>

<img src="/wp-content/uploads/create-branch-github-issue@2x.png" class="help-center-img img-bordered" alt="Create branch from GitHub issue">

Branch names auto-fill based on the issue title. Created branches will display the GitHub icon to reflect their link.

---

## How to copy an issue link or open it in GitHub

To open the issue in GitHub or copy its link, use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu or click the <i class="fa fa-external-link" aria-hidden="true"></i> icon in the top right.

<img src="/wp-content/uploads/view-github-issue-on-web-2025@2x.png" class="help-center-img img-bordered" alt="Open GitHub issue in browser">
