---
title: GitKraken Desktop + GitLab Issues Integration
description: Connect GitKraken with GitLab to view, filter, and manage issues directly from your local Git interface.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to GitLab Issues so you can preview, create, edit, filter, and branch from issues without leaving your Git workflow. GitLab Issues uses the same GitLab integration connection, and Community users are limited to public repositories.

**Requirements and limits**
- Integration covered here: GitLab Issues through the shared GitLab.com connection
- Connection model: GitLab Issues uses the same authentication as the GitLab integration
- Community plan limit: Public repositories only
- Branch creation, editing, and issue management depend on the connected GitLab repository and account permissions
- Custom filters use GitLab issue filter syntax

<div class='callout callout--basic'>
    <p>The GitLab Issues integration is restricted to public repositories for Community users. To unlock all features, consider upgrading to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken license</a>.</p>
</div>

***

## Quick Start

Connect GitKraken Desktop to GitLab Issues to view, create, and manage issues alongside your repository workflow.

1. Go to <kbd>Preferences > Integrations</kbd> and select **GitLab.com**, or click the ISSUES section in the Left Panel.
2. Click **Connect to GitLab** and authorize the connection in the browser.
3. Once connected, your GitLab issues appear in the Left Panel under default filters such as _My Issues_ and _All Issues_.

**To view issue details:** Click any issue to open its detail view. Changes sync with GitLab.

**To create a new issue:** Click the **+** icon in the Left Panel, fill in the required fields, and submit. The issue syncs directly to GitLab.

**To create a branch from an issue:** Open the issue detail view and click **Create a branch for this issue**. The branch name is pre-filled from the issue title.

**To create custom filters:** Use GitLab's issue filter syntax in the Left Panel to narrow your view by label, milestone, assignee, or status.

To open an issue in GitLab or copy its link, use the ellipsis menu or the external link icon in the issue detail view.

---

## How to connect the GitLab Issues integration

The GitLab and GitLab Issues integrations share the same connection. Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>.

<img src="/wp-content/uploads/connect-gitlab-issues-2025@2x.png" class="help-center-img img-bordered" alt="Connect GitLab Issues integration">

From the Integrations window, select <em>GitLab.com</em> and click <strong>Connect to GitLab</strong>.

<img src="/wp-content/uploads/connect-gitlab-2025@2x.png" class="help-center-img img-bordered" alt="Connect to GitLab prompt">

A browser window will open to authorize the connection. Log in with your GitLab credentials and click <strong>Continue authorization</strong>.

<img src="/wp-content/uploads/authorize-gitlab@2x.png" class="help-center-img img-bordered" alt="GitLab authorization dialog">

<img src="/wp-content/uploads/gitlab-sign-in@2x.png" class="help-center-img img-bordered" alt="GitLab sign-in screen">

Once authorized, GitKraken will display a success message.

<img src="/wp-content/uploads/auth-success-gitlab-1@2x.png" class="help-center-img img-bordered" alt="Successful GitLab integration">

---

## How to preview GitLab issues

After connecting, your GitLab issues will appear in the Left Panel. Default filters include _My Issues_ and _All Issues_.

<img src="/wp-content/uploads/gitlab-issues-list-2025@2x.png" class="help-center-img img-bordered" alt="GitLab Issues in Left Panel">

Hover over an issue to preview the title, description, labels, milestones, and assignee.

<img src="/wp-content/uploads/gitlab-issue-hover-2025@2x.png" class="help-center-img img-bordered" alt="GitLab issue preview tooltip">

---

## How to view and edit GitLab issue details

Click an issue to view its details.

<img src="/wp-content/uploads/github-issue-view-click-2025@2x.png" class="help-center-img img-bordered" alt="View GitLab issue details">

Edits made here will sync with your GitLab issue tracker.

---

## How to create a new GitLab issue

Click the <code>+</code> icon from the Left Panel to add a new issue.

<img src="/wp-content/uploads/gitlab-issue-create-2025@2x.png" class="help-center-img img-bordered" alt="Create new GitLab issue">

Required fields are marked with <code>*</code>. The issue will sync automatically to your GitLab repository.

---

## How to create GitLab issue filters

Use GitLab’s issue syntax to create filters and narrow your view.

<img src="/wp-content/uploads/gitlab-filter-create-2025@2x.png" class="help-center-img img-bordered" alt="Create GitLab filter">

Refer to GitLab’s [issue filtering guide](https://docs.gitlab.com/ee/user/search/index.html#filtering-issue-and-merge-request-lists) for examples.

---

## How to create branches from GitLab issues

From the issue detail view, click <strong>Create a branch for this issue</strong>. You can also right-click the issue or use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu.

<img src="/wp-content/uploads/gitlab-issue-create-branch-2025@2x.png" class="help-center-img img-bordered" alt="Create branch from GitLab issue">

The branch name is auto-filled based on the issue title. These branches show the GitLab icon to indicate the connection.

---

## How to copy an issue link or open it in GitLab

Use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu or <i class="fa fa-external-link" aria-hidden="true"></i> icon to open the issue in GitLab or copy the link.

<img src="/wp-content/uploads/gitlab-issue-copy-link-2025@2x.png" class="help-center-img img-bordered" alt="View GitLab issue on web">
