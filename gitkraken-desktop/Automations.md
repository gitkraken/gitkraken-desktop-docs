---

title: Automations
description: Automations for automating repository actions like pull requests and issue management
taxonomy:
    category: gitkraken-desktop

---

GitKraken Automations makes it easier to manage your team’s workflows by codifying best practices, automating repetitive tasks, and proactively highlighting potential issues for you.



## Auotmation Examples

These are just a few ways teams are already using Automations to reduce manual effort, enforce best practice standards, and create more scalable, repeatable workflows.
- Safe Deployments: Add a checklist for database migrations to ensure smooth rollouts.
- Critical Code Reviews: Assign the right engineers to review high-impact areas of the codebase, such as a payment service.
- Security Checks: Flag changes to sensitive areas like authentication and ensure a security review is completed.
- Refactoring Guardrails: Prevent conflicting changes during refactors and follow up with post-refactor maintenance tasks.
- SOC 2 Compliance: Automate checklists for encryption, security scans, and documentation to meet regulatory standards.
- DevOps Enhancements: Simplify deployment pipelines, enforce pre-deployment quality checks, and manage infrastructure-as-code changes with Automation workflows tailored to your processes.

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
           Currently, Automations supports GitHub and GitLab repositories.
    </p>
</div>


## Get Started with Automations

To get started with Automations simply login to [gitkraken.dev](https://gitkraken.dev/automations/list?product=gitkraken&source=help_center) and select Automations on the left side menu. If this is your first automation you will be directed to our get started landing page, from here you can create a new automation or select a template from the suggestion list. 

<img src="/wp-content/uploads/Createautomations-scaled.jpeg" class="help-center-img img-bordered">


### Create a Automation

To create a Automation, select <button class="button button--success button--ui button--nolink">+ Create Automation</button>.

Then, create a name for your automation. Next, using the Provider drop down select either GitHub or GitLab as your hosting provider. And finally locate the repository you wish to apply the automation to in the Repository drop down. If you wish for the Automation to also apply to draft pull requests please select the checkbox. 

<img src="/wp-content/uploads/Createautomations2.png" class="help-center-img img-bordered">

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
            A webhook will be set up on the selected repository in order to trigger when saving the automation.
    </p>
</div>


## Conditions

Next up, you will set up conditions, which are a list of criteria that determine when a Trigger should execute. We currently support 3 types of conditions: "File location", "File contents", and "Pull Request"

<img src="/wp-content/uploads/Createautomations3.png" class="help-center-img img-bordered">

### Boolean logic

You can choose whether all or any of the conditions you set up apply to your Trigger:

<img src="/wp-content/uploads/Createautomations4.png" class="help-center-img img-bordered">

### File Location  

The Following File Location trigger options can be selected: 
- File name condition: This condition matches the name of files in your repository.
- File path condition: This condition matches the path of files in your repository.
- File added in folder condition: This condition matches when files are added to a specific folder in a pull request. For example, the filter "File added in folder" with the operator "folder path equals" with the value "src/components/icons" would match any file that was added in that icons folder (or subfolders).

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
           A file path is different from a file name. For example: *src/app/index.ts* is a file path, while *index.ts* is a file name.
    </p>
</div>


### File Contents

The Following File Contet trigger options can be selected: 
- Old Code condition: Matches against modified lines of code from before your code change: the red on the left-hand side of a split view diff.
- New Code condition: Matches against modified lines of code from after your code change: the green on the right-hand side of a split view diff.
- New and Old Code condition: Matches both sides of the diff view

### Pull Request

The Following Pull Request trigger options can be selected: 
- Number of changed files condition: This condition matches when the number of files that are part of this pull request satisfy the inequality. 
- PR Author condition: This condition matches the author of the pull request. This automation will only run if the author matches this condition.
- Labels on the PR condition: This condition matches the GitHub Labels specified.


## Actions

Five kinds of actions are currently supported: posting a comment, adding a checklist item, assigning a pull request, and assigning a reviewer.

- Add Comment: When this action is executed, GitKraken will post the comment on the matching pull request
- Add to Checklist: When this action is executed, GitKraken will add a new checklist item to the PR description. You can add as many checklist items as you need by adding an action for each item.
- Add Assignee: When this action is executed, GitKraken will assign the pull request to the user of your choice. If you'd like to assign multiple users, you can create multiple instances of this action on the same Trigger. If you supply an optional message to explain why this user is being assigned, GitKraken will post a comment notifying that user and explaining why they were assigned.
- Add Label: When this action is executed, GitKraken will assign the selected GitHub label to the pull request. If you'd like to add multiple labels, you can create multiple instances of this action on the same Trigger.
- Add Reviewer: When this action is executed, GitKraken will assign the person or team of your choice as a reviewer on the PR. If you'd like to add multiple reviewers, you can create multiple instances of this action on the same Trigger. If you supply an optional message to explain why this user is being assigned as a reviewer, GitKraken will post a comment notifying that user and explaining why they were assigned as a reviewer.

<div class='callout callout--warning'>
    <p>
        <strong>Note:</strong>
           A pull request can never have the author of the pull request as a reviewer. If an action would cause the author to be a reviewer on their own pull request, GitKraken will skip over that action, but still perform all other actions on the trigger.
    </p>
</div>


## Managing Saved Automations

After creating your first automation you will now see a list of all your saved automations on [GitKraken.dev](https://gitkraken.dev/automations/list?product=gitkraken&source=help_center). From this screen you can add additional automations, disable/enable, delete, sort, edit and duplicate your saved automations. 

<img src="/wp-content/uploads/Createautomations5.png" class="help-center-img img-bordered">


### Edit / Delete / Duplicate an Automation

Edit / Delete / Duplicate a Automation by selecting the ellipsis <i class="fas fa-ellipsis-v"></i> icon by the Automation name.

<img src="/wp-content/uploads/Createautomations6.png" class="help-center-img img-bordered">


### Sort Automations

GitKraken Automations has two options for sorting, Status and Action. Status is if the Automation is Enabled or Disabled. Actions allows you to sort by the triggered action of your automation. 

<img src="/wp-content/uploads/Createautomations7.png" class="help-center-img img-bordered">


### Add Additional Automations

To create an additional Automation, select <button class="button button--success button--ui button--nolink">+ Create Automation</button>.


