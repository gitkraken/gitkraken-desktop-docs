---
title: GitKraken Desktop + GitHub Issues Integration
description: Learn how to connect GitKraken Desktop with GitHub Issues to manage, filter, preview, and create issues directly from your Git workflow.
product: GitKraken Desktop
feature: GitHub Issues Integration
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub]
integrations: [GitHub]
hosted_variant: cloud
status: GA
last_verified: 2026-11
llms_include: true
tags: [github, issues, filters, branching, integration]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: November 2026</kbd>

Use this page to connect GitKraken Desktop to GitHub Issues so you can preview, create, edit, filter, and branch from issues alongside your repository work. GitHub Issues uses the same GitHub integration connection, and Community users are limited to public repositories.

<div class='callout callout--basic'>
    <p>The GitHub Issues integration is limited to public repositories for Community users. To use all features, upgrade to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken license</a>.</p>
</div>

**Requirements and limits**
- Integration covered here: GitHub Issues for GitHub.com
- Connection model: Shares the same connection as the GitHub integration
- Community plan: Public repositories only
- Issue workflows: Preview, create, edit, filter, and branch from issues after connecting GitHub
- Filter syntax: Uses GitHub issue filtering syntax for custom filters

| Capability | Community | Paid plans | Notes |
|------------|-----------|------------|-------|
| Preview issues | Yes | Yes | Uses the shared GitHub integration connection |
| Create issues | Public repositories only | Yes | Requires the connected GitHub repository and account permissions |
| Edit issue details | Public repositories only | Yes | Requires the connected GitHub repository and account permissions |
| Create branches from issues | Public repositories only | Yes | Requires the connected GitHub repository and account permissions |
| Filter issues | Yes | Yes | Uses GitHub issue filtering syntax |

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> and select **GitHub**, or click the ISSUES section in the Left Panel.
2. Click **Connect to GitHub**, then finish connecting in your browser at gitkraken.dev.
3. Find your GitHub issues in the Left Panel under the default filters, such as _My Open Issues_ and _All Open Issues_.

**To view issue details:** Click any issue in the Left Panel to open its detail view. Changes you make there sync with GitHub.

**To create a new issue:** Click the **+** icon in the Left Panel, fill in the required fields, and submit. The issue syncs directly to GitHub.

**To create a branch from an issue:** Open the issue detail view and click **Create a Branch for This Issue**. GitKraken Desktop pre-fills the branch name from the issue title.

**To create custom filters:** Use GitHub's issue filter syntax to build filters in the Left Panel and narrow your view to specific labels, statuses, or assignees.

To open an issue in GitHub or copy its link, use the ellipsis menu or the external link icon in the issue detail view.

---

## How to connect the GitHub Issues integration

The GitHub and GitHub Issues integrations share the same connection.

<div class='callout callout--basic'>
    <p><strong>Use GitHub Issues in GitKraken Desktop when:</strong> you want issue triage and branch creation directly beside your Git workflow. <strong>Do not use the in-app view alone when:</strong> you need broader GitHub project or issue-management features outside the issue flows covered here.</p>
</div>

You can set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>.

<figure>
  <img src="/wp-content/uploads/connect-github-issues-2025@2x.png" class="help-center-img img-bordered" alt="Connect GitHub Issues from Preferences">
  <figcaption style="text-align: center; color: #888">Connect GitHub Issues from Preferences.</figcaption>
</figure>

GitHub connects through your GitKraken account, so sign in to GitKraken Desktop first. In <kbd>Preferences > Integrations</kbd>, select <strong>GitHub</strong> and click <strong>Connect to GitHub</strong>.

<figure>
  <img src="/wp-content/uploads/connect-github-2025@2x.png" class="help-center-img img-bordered" alt="Preferences > Integrations > GitHub: the GitHub card reads Not Connected with a Connect to GitHub button, and Manage Integrations is at the top right of the pane.">
  <figcaption style="text-align: center; color: #888">Connect to GitHub prompt.</figcaption>
</figure>

Your browser opens gitkraken.dev to finish the connection. Log in with your GitHub credentials and authorize the connection if GitHub asks.

When the connection succeeds, the GitHub card in <kbd>Preferences > Integrations</kbd> reads <strong>Connected to your GitHub integration</strong>. You can also use the connection on your other computers and profiles. See [How integrations connect through your GitKraken account](/gitkraken-desktop/integrations/#how-integrations-connect-through-your-gitkraken-account).

<figure>
  <img src="/wp-content/uploads/github-success-1@2x.png" class="help-center-img img-bordered" alt="Successful GitHub integration">
  <figcaption style="text-align: center; color: #888">Successful GitHub integration.</figcaption>
</figure>

---

## How to preview GitHub issues

After you connect, your GitHub issues appear in the Left Panel. Default filters include _My Open Issues_ and _All Open Issues_. You can customize or remove these filters.

<figure>
  <img src="/wp-content/uploads/github-issues-left-panel-2025@2x.png" class="help-center-img img-bordered" alt="GitHub Issues in Left Panel">
  <figcaption style="text-align: center; color: #888">GitHub Issues in Left Panel.</figcaption>
</figure>

Hover over an issue to preview the title, description, status, labels, assignees, and reporter.

<figure>
  <img src="/wp-content/uploads/issues-preview-github-issues@2x.png" class="help-center-img img-bordered" alt="Issue preview tooltip">
  <figcaption style="text-align: center; color: #888">Issue preview tooltip.</figcaption>
</figure>

---

## How to view and edit GitHub issue details

Click an issue to open the details view.

<figure>
  <img src="/wp-content/uploads/view-github-issue-2025@2x.png" class="help-center-img img-bordered" alt="GitHub Issue Details View">
  <figcaption style="text-align: center; color: #888">GitHub Issue Details View.</figcaption>
</figure>

Your changes sync with GitHub.

---

## How to create a new GitHub issue

To create a new issue, click the <code>+</code> icon in the Left Panel.

<figure>
  <img src="/wp-content/uploads/create-github-issue-2025@2x.png" class="help-center-img img-bordered" alt="Create new GitHub issue">
  <figcaption style="text-align: center; color: #888">Create new GitHub issue.</figcaption>
</figure>

Required fields are marked with <code>*</code>. GitKraken Desktop syncs the issue to your GitHub repository.

---

## How to create GitHub issue filters

Create filters with GitHub's issue filter syntax to narrow your view to specific issue types, labels, or statuses.

<div class='callout callout--basic'>
    <p><strong>Use custom filters when:</strong> you need to focus on a subset of issues such as bugs, assigned work, or open review blockers. <strong>Do not rely only on default filters when:</strong> they leave you with too much issue noise.</p>
</div>

<figure>
  <img src="/wp-content/uploads/create-github-filter@2x.png" class="help-center-img img-bordered" alt="Create GitHub issue filter">
  <figcaption style="text-align: center; color: #888">Create GitHub issue filter.</figcaption>
</figure>

For syntax examples, see GitHub’s [issue filtering guide](https://docs.github.com/en/github/searching-for-information-on-github/searching-issues-and-pull-requests).

---

## How to create branches from GitHub issues

From the issue details view, click <strong>Create a Branch for This Issue</strong>. You can also right-click an issue or use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu.

<div class='callout callout--basic'>
    <p><strong>Use issue-based branch creation when:</strong> you want a clear branch-to-issue link and an auto-filled branch name. <strong>Do not use it when:</strong> the branch should represent a larger initiative or combine work from multiple issues.</p>
</div>

<figure>
  <img src="/wp-content/uploads/create-branch-github-issue@2x.png" class="help-center-img img-bordered" alt="Create branch from GitHub issue">
  <figcaption style="text-align: center; color: #888">Create branch from GitHub issue.</figcaption>
</figure>

GitKraken Desktop pre-fills the branch name from the issue title. Branches created from an issue show the GitHub icon.

---

## How to copy an issue link or open it in GitHub

To open the issue in GitHub or copy its link, use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu or click the <i class="fa fa-external-link" aria-hidden="true"></i> external link icon in the top right.

<figure>
  <img src="/wp-content/uploads/view-github-issue-on-web-2025@2x.png" class="help-center-img img-bordered" alt="Open GitHub issue in browser">
  <figcaption style="text-align: center; color: #888">Open GitHub issue in browser.</figcaption>
</figure>
