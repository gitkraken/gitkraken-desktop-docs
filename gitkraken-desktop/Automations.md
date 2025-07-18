---
title: Automations
description: Automations for automating repository actions like pull requests and issue management
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: July 2025</kbd>

GitKraken Automations helps you streamline your team’s workflows by codifying best practices, eliminating repetitive tasks, and proactively flagging potential issues.

## Automation Examples

Teams use Automations to reduce manual effort, enforce standards, and build scalable, repeatable workflows. Here are some common use cases:

- **Safe Deployments**: Add a checklist for database migrations to ensure smooth rollouts.
- **Critical Code Reviews**: Automatically assign the right engineers to review high-impact areas of the codebase, such as a payment service.
- **Security Checks**: Flag changes to sensitive areas like authentication and ensure a security review is completed.
- **Refactoring Guardrails**: Prevent conflicting changes during refactors and trigger follow-up maintenance tasks.
- **SOC 2 Compliance**: Automate checklists for encryption, security scans, and documentation to meet regulatory standards.
- **DevOps Enhancements**: Streamline deployment pipelines, enforce pre-deployment quality checks, and manage infrastructure-as-code updates.

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        Currently, Automations supports GitHub and GitLab repositories.
    </p>
</div>

## Get Started with Automations

To begin, log in to [GitKraken Automations](https://gitkraken.dev/automations/list?product=gitkraken&source=help_center) and select <strong>Automations</strong> from the left-hand menu.

If this is your first time using Automations, you'll see a start page where you can either create a new automation or choose from a list of suggested templates.

<figure>
  <img src="/wp-content/uploads/Createautomations-scaled.jpeg" alt="Create Automations landing page" class="help-center-img img-bordered">
</figure>

### Create an Automation

To create an automation:

1. Click <button class="button button--success button--ui button--nolink">+ Create Automation</button>.
2. Enter a name for your automation.
3. From the **Provider** dropdown, select either `GitHub` or `GitLab`.
4. Use the **Repository** dropdown to choose the repository you want to apply the automation to.
5. (Optional) To include draft pull requests, check the corresponding box.

<figure>
  <img src="/wp-content/uploads/Createautomations2.png" alt="Automation creation screen" class="help-center-img img-bordered">
</figure>

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        A webhook will be set up on the selected repository to trigger events when the automation is saved.
    </p>
</div>

## Conditions

Conditions define when a trigger should execute. Automations currently support the following condition types:

- **File Location**
- **File Content**
- **Pull Request**

<figure>
  <img src="/wp-content/uploads/Createautomations3.png" alt="Set up conditions screenshot" class="help-center-img img-bordered">
</figure>

### Boolean Logic

Choose whether **all** conditions or **any** conditions must be met for the trigger to execute.

- **All conditions**: The trigger fires only if every condition is met.
- **Any condition**: The trigger fires if at least one condition is met.

<figure>
  <img src="/wp-content/uploads/Createautomations4.png" alt="Boolean logic selection" class="help-center-img img-bordered">
</figure>

### File Location Conditions

- **File name**: Matches filenames in the repository.
- **File path**: Matches full paths of files in the repository.
- **File added in folder**: Matches when files are added to a specified folder in a pull request. For example, using:
  - Filter: `File added in folder`
  - Operator: `Folder path equals`
  - Value: `src/components/icons`

  This would match any file added within the `icons` folder or its subfolders.

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        A file path includes the directory structure (e.g., <code>src/app/index.ts</code>), while a file name is just the filename (e.g., <code>index.ts</code>).
    </p>
</div>

### File Content Conditions

- **Old Code**: Matches modified lines *before* the code change (red in split diff view).
- **New Code**: Matches modified lines *after* the code change (green in split diff view).
- **New and Old Code**: Matches both sides of the split diff view.

### Pull Request Conditions

- **Number of changed files**: Matches based on how many files are changed in the pull request.
- **PR author**: Matches the author of the pull request.
- **Labels on the PR**: Matches if specific GitHub labels are present.

## Actions

The following actions can be executed when a trigger is matched:

- **Add Comment**: Posts a comment on the matching pull request.
- **Add to Checklist**: Inserts checklist items into the PR description. You can add multiple items by creating separate actions.
- **Add Assignee**: Assigns the pull request to a user. You can assign multiple users or include an optional comment explaining why they were assigned.
- **Add Label**: Adds the specified GitHub label to the pull request. Use multiple actions to assign multiple labels.
- **Add Reviewer**: Assigns a person or team as a reviewer. You can include an optional comment explaining the review request. Reviewers can be assigned in bulk using multiple actions.

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
        GitKraken will not assign the PR author as a reviewer. If such a match occurs, that action is skipped while other actions still run.
    </p>
</div>


## Managing Saved Automations

After creating your first automation, you'll see a list of all your saved automations on [GitKraken.dev](https://gitkraken.dev/automations/list?product=gitkraken&source=help_center). From this screen, you can add, disable/enable, delete, sort, edit, or duplicate automations.

<figure>
  <img src="/wp-content/uploads/Createautomations5.png" alt="Saved automations list" class="help-center-img img-bordered">
</figure>

### Edit, Delete, or Duplicate an Automation

To edit, delete, or duplicate an automation, click the ellipsis <i class="fas fa-ellipsis-v"></i> icon next to the automation name.

<figure>
  <img src="/wp-content/uploads/Createautomations6.png" alt="Ellipsis menu for automations" class="help-center-img img-bordered">
</figure>

### Sort Automations

You can sort automations by:

- **Status**: Enabled or Disabled
- **Action**: The type of action the automation executes

<figure>
  <img src="/wp-content/uploads/Createautomations7.png" alt="Sort automations options" class="help-center-img img-bordered">
</figure>

### Add Additional Automations

To create an additional automation, click <button class="button button--success button--ui button--nolink">+ Create Automation</button>.


