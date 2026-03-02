---
title: Create and Manage GitHub Actions Workflows in GitKraken Desktop
description: Learn how to automate tasks with GitHub Actions in GitKraken Desktop. Covers creating, editing, and deleting workflow files directly in your repository.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: February 2026</kbd>

[GitHub Actions](https://github.com/features/actions) is a service from GitHub that lets you automate tasks in your repository using workflow files. These workflows are written in YAML and stored in the `.github/workflows` directory of your repository.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/qr3vwIvXUfc?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## Quick Start

Create, edit, and delete GitHub Actions workflow files from within GitKraken Desktop without leaving the application.

**To create a workflow:**
1. Open a GitHub-hosted repository in GitKraken Desktop. The **GitHub Actions** section appears in the Left Panel.
2. Hover over **GitHub Actions** and click the **+** button to open the Create Workflow panel.
3. Choose a workflow template or start with a blank file.
4. The workflow is saved automatically in the `.github/workflows` directory.

**To edit an existing workflow:**
- Double-click the workflow file in the Left Panel under **GitHub Actions** to open and modify it.

**To delete a workflow:**
- Right-click the workflow file and select **Delete Workflow**.

The **GitHub Actions** section is only visible when working with a GitHub-hosted repository that has the GitHub integration connected. For workflow syntax, triggers, and advanced configuration options, refer to the [GitHub Actions Documentation](https://docs.github.com/en/actions).

---

## Managing Workflows in GitKraken Desktop

GitKraken Desktop provides basic tools for creating, editing, and deleting GitHub Action workflows directly within your repository.

<div class='callout callout--success'>
    <p><strong>Note:</strong> The <strong>GitHub Actions</strong> section appears only when you're working in a GitHub-hosted repository.</p>
</div>

### Create a Workflow

1. In the Left Panel, hover over <strong>GitHub Actions</strong>.
2. Click the <code>+</code> button to open the <strong>Create Workflow</strong> panel.
3. Choose from available workflow templates or start with a blank workflow.
4. The workflow file will be saved in the `.github/workflows` directory (created automatically if it doesn’t exist).

<img src='/wp-content/uploads/create-github-action-2025@2x.png' class="help-center-img img-bordered" alt="Creating GitHub Action workflow from GitKraken Desktop">

### Edit a Workflow

Double-click any existing workflow file to open it. You can view, modify, and save changes directly.

<img src='/wp-content/uploads/github-actions-edit@2x.png' class="help-center-img img-bordered" alt="Editing a GitHub Action workflow in GitKraken Desktop">

### Delete a Workflow

Right-click a workflow file and select <strong>Delete Workflow</strong> to remove it.

<img src='/wp-content/uploads/delete-github-action-2025@2x.png' class="help-center-img img-bordered" alt="Deleting a GitHub Action workflow in GitKraken Desktop">

---

## Learn More

For workflow syntax, best practices, and advanced automation examples, visit the [GitHub Actions Documentation](https://docs.github.com/en/actions).
