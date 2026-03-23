---
title: GitKraken Desktop + GitLab Self-Managed Issues Integration
description: Connect GitKraken with GitLab Self-Managed to preview, manage, and filter issues directly from your Git workflow.
product: GitKraken Desktop
feature: GitLab Self-Managed Issues Integration
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitLab Self-Managed]
integrations: [GitLab Self-Managed]
hosted_variant: self-hosted
status: GA
last_verified: 2026-03
llms_include: true
tags: [gitlab-self-managed, issues, self-hosted, filters, branching]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to GitLab Self-Managed Issues so you can preview, manage, filter, and branch from issues alongside your repository work. This integration shares the GitLab Self-Managed connection, requires GitLab Self-Managed 13.1 or newer, and is view-only for Community users.

<div class='callout callout--basic'>
    <p>The GitLab Self-Managed Issues integration is view-only for Community users. To unlock all features, consider upgrading to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken license</a>.</p>
</div>

**Requirements and limits**
- Integration covered here: GitLab Self-Managed Issues
- Server version: GitLab Self-Managed 13.1 or newer
- Connection model: Shares the same connection as the GitLab Self-Managed integration
- Community plan: View-only access
- Full issue workflows: Paid GitKraken license required for editing, branching, and full issue management

---

## Requirements

<div class='callout callout--warning'>
    <p>This integration requires GitLab Self-Managed version 13.1 or newer.</p>
</div>

---

## Quick Start

Connect GitKraken Desktop to GitLab Self-Managed Issues to preview and manage issues from the Left Panel.

1. Connect your GitLab Self-Managed instance from <kbd>Preferences > Integrations</kbd> by following the GitLab Self-Managed authentication flow.
2. Open the **ISSUES** section in the Left Panel to load issues from the connected instance.
3. Preview, filter, and open issue details directly in GitKraken Desktop.

To edit issues, create issue-based branches, or open issues in GitLab Self-Managed, use the same workflows documented for [GitLab Issues](/integrations/gitlab-issues/).

---

## How to connect the GitLab Self-Managed Issues integration

The GitLab Self-Managed and GitLab Self-Managed Issues integrations share the same connection.

<div class='callout callout--basic'>
    <p><strong>Use GitLab Self-Managed Issues in GitKraken Desktop when:</strong> you already have the self-managed GitLab integration connected and want issue workflows next to your repository work. <strong>Don't use this page when:</strong> you still need to configure the underlying self-managed GitLab connection first.</p>
</div>

Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>.

Follow these [GitLab Self-Managed authentication steps](/integrations/gitlab-self-hosted/#gitlab-self-managed-authentication) to connect your instance.

---

## What the GitLab Self-Managed Issues integration supports

Once connected, the GitLab Self-Managed Issues integration provides the same functionality as the GitLab Issues integration:

<div class='callout callout--basic'>
    <p><strong>Use the in-app issue workflow when:</strong> you want issue context, filtering, and branching without leaving GitKraken Desktop. <strong>Don't rely on it alone when:</strong> you need broader project-management features outside the issue workflows documented here.</p>
</div>

- [Preview GitLab Issues](/integrations/gitlab-issues/#preview-gitlab-issues)
- [View and Edit GitLab Issue Details](/integrations/gitlab-issues/#view-and-edit-gitlab-issue-details)
- [Create GitLab Issues](/integrations/gitlab-issues/#create-new-gitlab-issue)
- [Create GitLab Filters](/integrations/gitlab-issues/#create-filters)
- [Create Branch from Issue](/integrations/gitlab-issues/#create-branches-from-issue)
- [Shortcuts to view Issues in GitLab](/integrations/gitlab-issues/#copy-issue-link-or-view-in-gitlab)
