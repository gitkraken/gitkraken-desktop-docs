---
title: Create and Manage GitHub Actions Workflows in GitKraken Desktop
description: Learn how to automate tasks with GitHub Actions in GitKraken Desktop. Covers creating, editing, and deleting workflow files directly in your repository.
product: GitKraken Desktop
feature: GitHub Actions
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub]
integrations: [GitHub]
hosted_variant: cloud
status: GA
last_verified: 2026-03
llms_include: true
tags: [github-actions, workflows, yaml, automation, github]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

GitHub Actions workflows in GitKraken Desktop are managed by editing the YAML files stored in your repository's `.github/workflows` directory. As of GitKraken Desktop 11.10, workflow management is no longer available from the Left Panel, so use this page when you need the current file-based workflow for creating, editing, or deleting Actions definitions.

**Requirements and limits**
- GitKraken Desktop 11.10 and later manages workflows by editing files in your repository instead of using a Left Panel Actions view.
- Store workflow definitions in the repository's `.github/workflows` directory.
- Creating, editing, and deleting workflows requires staging and committing the YAML file changes.
- Existing GitHub Actions workflows continue to run after the Left Panel deprecation; only the management workflow changed.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/qr3vwIvXUfc?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

<div class='callout callout--warning'>
  <p><strong>Deprecation notice 🧟 — GitKraken Desktop 11.10:</strong> GitHub Actions has been removed from the Left Panel to simplify navigation. Existing workflows will continue to run normally. To update workflow files, edit and commit them directly within your repository.</p>
</div>


## Quick Start

Create and edit GitHub Actions workflow files directly in your repository from within GitKraken Desktop.

**To create a workflow:**
1. In your repository, create a `.github/workflows` directory if one does not already exist.
2. Add a new YAML workflow file to that directory.
3. Stage and commit the file. GitHub Actions detects and registers the workflow automatically.

**To edit an existing workflow:**
1. Open the workflow file from your repository's `.github/workflows` directory.
2. Make your changes, then stage and commit them.

**To delete a workflow:**
1. Delete the workflow YAML file from your repository's `.github/workflows` directory.
2. Stage and commit the deletion. GitHub Actions stops running the deleted workflow.

For workflow syntax, triggers, and advanced configuration options, refer to the [GitHub Actions Documentation](https://docs.github.com/en/actions).

---

## How to manage GitHub Actions workflows in GitKraken Desktop

As of version 11.10, GitHub Actions workflow management is handled by editing YAML files directly in your repository’s `.github/workflows` directory.

### How to create a workflow

1. Navigate to your repository’s `.github/workflows` directory. Create it if it does not already exist.
2. Add a new YAML file for your workflow.
3. Stage and commit the file. GitHub Actions automatically detects and registers the new workflow.

### How to edit a workflow

1. Open the workflow file from your repository’s `.github/workflows` directory.
2. Make your changes.
3. Stage and commit the updated file.

### How to delete a workflow

1. Delete the workflow YAML file from your repository’s `.github/workflows` directory.
2. Stage and commit the deletion. GitHub Actions stops running the deleted workflow.

---

## Where to learn more about GitHub Actions syntax

For workflow syntax, best practices, and advanced automation examples, visit the [GitHub Actions Documentation](https://docs.github.com/en/actions).
