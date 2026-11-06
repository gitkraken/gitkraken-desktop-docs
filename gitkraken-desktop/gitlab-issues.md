---
title: GitKraken Desktop + GitLab Issues Integration
description: Connect GitKraken Desktop with GitLab to view, filter, and manage issues directly from your local Git interface.
product: GitKraken Desktop
feature: GitLab Issues Integration
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitLab]
integrations: [GitLab]
hosted_variant: cloud
status: GA
last_verified: 2026-11
llms_include: true
tags: [gitlab, issues, filters, branching, integration]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "integrations-with-issue-trackers"
    nav_label: "GitLab Issues"
    nav_order: 60
    nav_parent: "integrations-with-issue-trackers"
    page_type: "content"
---

<kbd>Last updated: November 2026</kbd>

Use this page to connect GitKraken Desktop to GitLab Issues so you can preview, create, edit, filter, and branch from issues without leaving your Git workflow. GitLab Issues uses the same GitLab integration connection, and Community users are limited to public repositories.

**Requirements and limits**
- Integration covered here: GitLab Issues through the shared GitLab.com connection
- Connection model: GitLab Issues uses the same authentication as the GitLab integration
- Community plan limit: Public repositories only
- Permissions: Branch creation, editing, and issue management depend on the connected GitLab repository and account permissions
- Filters: Custom filters use GitLab issue filter syntax

| Capability | Community | Paid plans | Notes |
|------------|-----------|------------|-------|
| Preview issues | Yes | Yes | Uses the shared GitLab integration connection |
| Create issues | Public repos only | Yes | Depends on repository and account permissions |
| Edit issue details | Public repos only | Yes | Depends on repository and account permissions |
| Create branches from issues | Public repos only | Yes | Depends on repository and account permissions |
| Filter issues | Yes | Yes | Uses GitLab issue filter syntax |

<div class='callout callout--basic'>
    <p>The GitLab Issues integration is restricted to public repositories for Community users. To use all features, upgrade to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken license</a>.</p>
</div>

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> and select **GitLab**, or click the ISSUES section in the Left Panel.
2. Click **Connect to GitLab**, then finish connecting in your browser at gitkraken.dev.
3. Find your GitLab issues in the Left Panel under the default filters, such as _My Issues_ and _All Issues_.

**To view issue details:** Click any issue to open its detail view. Changes sync with GitLab.

**To create a new issue:** Click the **+** icon in the Left Panel, fill in the required fields, and submit. The issue syncs directly to GitLab.

**To create a branch from an issue:** Open the issue detail view and click **Create a Branch for This Issue**. GitKraken Desktop pre-fills the branch name from the issue title.

**To create custom filters:** Use GitLab's issue filter syntax in the Left Panel to narrow your view by label, milestone, assignee, or status.

To open an issue in GitLab or copy its link, use the ellipsis menu or the external link icon in the issue detail view.

---

## How to connect the GitLab Issues integration

The GitLab and GitLab Issues integrations share the same connection. Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>.

<div class='callout callout--basic'>
    <p><strong>Use GitLab Issues in GitKraken Desktop when:</strong> you want issue context, issue editing, and branch creation close to your repository workflow. <strong>Do not use the in-app view alone when:</strong> you need broader GitLab project management outside the issue workflows covered here.</p>
</div>

<figure>
  <img src="/wp-content/uploads/connect-gitlab-issues-2025@2x.png" class="help-center-img img-bordered" alt="Connect GitLab Issues integration">
  <figcaption style="text-align: center; color: #888">Connect GitLab Issues integration.</figcaption>
</figure>

GitLab connects through your GitKraken account, so sign in to GitKraken Desktop first. In <kbd>Preferences > Integrations</kbd>, select <strong>GitLab</strong> and click <strong>Connect to GitLab</strong>.

<figure>
  <img src="/wp-content/uploads/connect-gitlab-2025-v3@2x.png" class="help-center-img img-bordered" alt="Preferences > Integrations > GitLab in GitKraken Desktop: the GitLab card reads Not Connected with a Connect to GitLab button, and a Manage Integrations button sits at the top right of the pane.">
  <figcaption style="text-align: center; color: #888">Connect to GitLab prompt.</figcaption>
</figure>

Your browser opens gitkraken.dev to finish the connection. Log in with your GitLab credentials and authorize the connection if GitLab asks. You can also use the connection on your other computers and profiles. See [How integrations connect through your GitKraken account](/gitkraken-desktop/integrations/#how-integrations-connect-through-your-gitkraken-account).

<figure>
  <img src="/wp-content/uploads/authorize-gitlab@2x.png" class="help-center-img img-bordered" alt="GitLab authorization dialog">
  <figcaption style="text-align: center; color: #888">GitLab authorization dialog.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/gitlab-sign-in@2x.png" class="help-center-img img-bordered" alt="GitLab sign-in screen">
  <figcaption style="text-align: center; color: #888">GitLab sign-in screen.</figcaption>
</figure>

After you authorize the connection, GitKraken Desktop shows a success message.

<figure>
  <img src="/wp-content/uploads/auth-success-gitlab-1@2x.png" class="help-center-img img-bordered" alt="Successful GitLab integration">
  <figcaption style="text-align: center; color: #888">Successful GitLab integration.</figcaption>
</figure>

---

## How to preview GitLab issues

After you connect, your GitLab issues appear in the Left Panel. Default filters include _My Issues_ and _All Issues_.

<figure>
  <img src="/wp-content/uploads/gitlab-issues-list-2025@2x.png" class="help-center-img img-bordered" alt="GitLab Issues in Left Panel">
  <figcaption style="text-align: center; color: #888">GitLab Issues in Left Panel.</figcaption>
</figure>

Hover over an issue to preview the title, description, labels, milestones, and assignee.

<figure>
  <img src="/wp-content/uploads/gitlab-issue-hover-2025@2x.png" class="help-center-img img-bordered" alt="GitLab issue preview tooltip">
  <figcaption style="text-align: center; color: #888">GitLab issue preview tooltip.</figcaption>
</figure>

---

## How to view and edit GitLab issue details

Click an issue to view its details.

<figure>
  <img src="/wp-content/uploads/github-issue-view-click-2025@2x.png" class="help-center-img img-bordered" alt="View GitLab issue details">
  <figcaption style="text-align: center; color: #888">View GitLab issue details.</figcaption>
</figure>

Your edits sync with your GitLab issue tracker.

---

## How to create a new GitLab issue

Click the <code>+</code> icon in the Left Panel to add a new issue.

<figure>
  <img src="/wp-content/uploads/gitlab-issue-create-2025@2x.png" class="help-center-img img-bordered" alt="Create new GitLab issue">
  <figcaption style="text-align: center; color: #888">Create new GitLab issue.</figcaption>
</figure>

Required fields are marked with <code>*</code>. GitKraken Desktop syncs the issue to your GitLab repository automatically.

---

## How to create GitLab issue filters

Use GitLab’s issue syntax to create filters and narrow your view.

<div class='callout callout--basic'>
    <p><strong>Use custom filters when:</strong> you need focused issue queues by label, assignee, milestone, or status. <strong>Do not rely on only the default filters when:</strong> your team needs a narrower view of active work.</p>
</div>

<figure>
  <img src="/wp-content/uploads/gitlab-filter-create-2025@2x.png" class="help-center-img img-bordered" alt="Create GitLab filter">
  <figcaption style="text-align: center; color: #888">Create GitLab filter.</figcaption>
</figure>

For examples, see GitLab’s [issue filtering guide](https://docs.gitlab.com/ee/user/search/index.html#filtering-issue-and-merge-request-lists).

---

## How to create branches from GitLab issues

From the issue detail view, click <strong>Create a Branch for This Issue</strong>. You can also right-click the issue or use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu.

<div class='callout callout--basic'>
    <p><strong>Use issue-based branch creation when:</strong> you want the branch tied clearly to a specific GitLab issue. <strong>Do not use it when:</strong> the work spans multiple issues or the branch name needs a different structure than the issue title provides.</p>
</div>

<figure>
  <img src="/wp-content/uploads/gitlab-issue-create-branch-2025@2x.png" class="help-center-img img-bordered" alt="Create branch from GitLab issue">
  <figcaption style="text-align: center; color: #888">Create branch from GitLab issue.</figcaption>
</figure>

GitKraken Desktop pre-fills the branch name from the issue title. Branches created from an issue show the GitLab icon.

---

## How to copy an issue link or open it in GitLab

Use the <kbd><i class="fa fa-ellipsis-v"></i></kbd> menu or <i class="fa fa-external-link" aria-hidden="true"></i> icon to open the issue in GitLab or copy the link.

<figure>
  <img src="/wp-content/uploads/gitlab-issue-copy-link-2025@2x.png" class="help-center-img img-bordered" alt="View GitLab issue on web">
  <figcaption style="text-align: center; color: #888">View GitLab issue on web.</figcaption>
</figure>
