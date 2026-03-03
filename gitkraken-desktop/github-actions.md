---
title: Create and Manage GitHub Actions Workflows in GitKraken Desktop
description: Learn how to automate tasks with GitHub Actions in GitKraken Desktop. Covers creating, editing, and deleting workflow files directly in your repository.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

[GitHub Actions](https://github.com/features/actions) is a service from GitHub that lets you automate tasks in your repository using workflow files. These workflows are written in YAML and stored in the `.github/workflows` directory of your repository.

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

## Managing Workflows in GitKraken Desktop

As of version 11.10, GitHub Actions workflow management is handled by editing YAML files directly in your repository’s `.github/workflows` directory.

### Create a Workflow

1. Navigate to your repository’s `.github/workflows` directory. Create it if it does not already exist.
2. Add a new YAML file for your workflow.
3. Stage and commit the file. GitHub Actions automatically detects and registers the new workflow.

### Edit a Workflow

1. Open the workflow file from your repository’s `.github/workflows` directory.
2. Make your changes.
3. Stage and commit the updated file.

### Delete a Workflow

1. Delete the workflow YAML file from your repository’s `.github/workflows` directory.
2. Stage and commit the deletion. GitHub Actions stops running the deleted workflow.

---

## Learn More

For workflow syntax, best practices, and advanced automation examples, visit the [GitHub Actions Documentation](https://docs.github.com/en/actions).
