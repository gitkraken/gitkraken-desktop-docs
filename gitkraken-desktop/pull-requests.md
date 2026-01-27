---
title: Pull Requests in GitKraken Desktop
description: Create, manage, and review pull requests in GitKraken Desktop. Supports GitHub, GitLab, Bitbucket, Azure DevOps, and includes templates, comments, and suggestions.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

A pull request (sometimes called merge requests) is a review workflow that lets you propose changes in one branch before merging it into another. GitKraken Desktop supports creating, managing, and reviewing pull requests with integrated Git services like GitHub, GitLab, Bitbucket, and Azure DevOps.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/2VX1ISk9XH8?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## Creating a Pull Request

To create a pull request:
- Drag one branch onto another and select <em class='context-menu'>Start a pull request</em>
- Or right-click the target branch and choose the same option
- Or click the <button class='button button--success button--ui button--nolink'>+</button> icon in the Left Panel PULL REQUESTS section

<figure>
  <img src="/wp-content/uploads/create-pull-request-drag-and-drop-2025.gif" alt="User initiates a pull request in GitKraken Desktop by dragging a local branch (PM-34-docs-review-pr-page) onto the remote origin/main. The Create Pull Request dialog then appears, pre-filled with repository and branch information, ready for title, description, and assignee input." class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Start a pull request by dragging a branch</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/create-pr-2025.png" 
       srcset="/wp-content/uploads/create-pr-2025@2x.png" 
       alt="User clicks the plus button in the Pull Requests section of GitKraken Desktop’s Left Panel to open the Create Pull Request interface. The dialog appears with fields to select repositories, branches, title, description, and other PR options." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Create a pull request from the Left Panel</figcaption>
</figure>

<div class='callout callout'>
  <p><strong>Note:</strong> If the Azure DevOps PR form isn’t populating, see <a href="https://help.gitkraken.com/gitkraken-desktop/azure-devops/#azure-devops-pull-requests-form-not-populating-in-gitkraken-desktop">Azure DevOps Integration</a>.</p>
</div>

***

## Pull Request Templates

GitKraken Desktop supports PR templates on GitHub, GitLab, and Azure DevOps. When committed to the remote, the template appears during PR creation.

<figure>
  <img src="/wp-content/uploads/pr-template-2025.png" 
       srcset="/wp-content/uploads/pr-template-2025@2x.png" 
       alt="GitKraken Desktop interface displaying the Create Pull Request dialog with a dropdown field for selecting a pull request template. The template 'pull_request_template.md' is highlighted." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Pull request template field shown during creation</figcaption>
</figure>

Tips:
- Follow your provider's documentation for file location
- Ensure the template is on the currently checked out branch

Resources:
- [GitHub PR templates](https://help.github.com/articles/creating-a-pull-request-template-for-your-repository/)
- [GitLab merge request templates](https://docs.gitlab.com/ee/user/project/description_templates.html)
- [Azure DevOps PR templates](https://docs.microsoft.com/en-us/azure/devops/repos/git/pull-request-templates?view=azure-devops)

***

## Assignees, Labels, Reviewers

Some integrations allow adding:
- Assignees
- Reviewers
- Labels

<figure>
  <img src='/wp-content/uploads/add-reviewers-assignees-labels-2025.png' 
       srcset='/wp-content/uploads/add-reviewers-assignees-labels-2025@2x.png' 
       alt="GitKraken Desktop pull request creation screen showing fields for assigning reviewers, assignees, and labels. Two reviewers, two assignees, and two labels are selected." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Assign reviewers and labels during PR creation</figcaption>
</figure>

Conflict warnings appear if your source and target branches differ:

<figure>
  <img src='/wp-content/uploads/pr-merge-conflict-warning-2025.png' 
       srcset='/wp-content/uploads/pr-merge-conflict-warning-2025@2x.png' 
       alt="GitKraken Create Pull Request screen displaying a warning banner indicating a merge conflict between the source and target branches." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Merge conflict warning in PR modal</figcaption>
</figure>

<div class='callout callout--basic'>
  <p><strong>Reminder:</strong> Push your branch before creating a pull request.</p>
</div>

***

## Draft Pull Requests (GitHub)

With the GitHub integration, select the draft checkbox to mark the pull request as a draft.

<figure>
  <img src='/wp-content/uploads/create-draft-pr-2025.png' 
       srcset='/wp-content/uploads/create-draft-pr-2025@2x.png' 
       alt="GitKraken interface showing the Create Pull Request form with the 'Submit as draft' checkbox enabled." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Enable draft pull request in GitHub</figcaption>
</figure>

***

## GitHub Pull Request View

Enable the GitHub integration to access GitHub PR view:
- Select a PR in the Left Panel
- Or click the PR icon in the Launchpad

<figure>
  <img src='/wp-content/uploads/github-pr-view-2025.png' 
       srcset='/wp-content/uploads/github-pr-view-2025@2x.png' 
       alt="GitKraken Desktop displaying the GitHub pull request view for PR #1993, which adds Arm64 support for Windows and Linux." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitHub pull request view in the repo tab</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/launchpad-open-pr-panel-2025.png' 
       srcset='/wp-content/uploads/launchpad-open-pr-panel-2025@2x.png' 
       alt="Launchpad view in GitKraken Desktop showing a list of pull requests with an option highlighted to open the pull request panel." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Access PRs from the Launchpad</figcaption>
</figure>

From this view, GitHub users can edit:
- Title
- Description
- Reviewers
- Assignees
- Milestones
- Labels

Click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Review Code and Suggest Changes</span></button> to review changes.

***

## Suggest Changes

When you click to <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Review Code and Suggest Changes</span></button>, this will allow you to write the code suggestion directly in GitKraken Desktop's editor or [gitkraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken).

<figure>
  <img src='/wp-content/uploads/gkd-10-2-0-pr-suggest-code-changes.gif' 
       alt="User suggesting code changes within a pull request using GitKraken Desktop's review interface" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Suggest code changes inside a pull request</figcaption>
</figure>

All code suggestions are posted a comments in the GitHub pull request conversation with a link to review the code suggestion inside of gitkraken.dev or GitKraken Desktop. 

***

## Accept or Reject Suggestions

Code suggestions display in the PR view under the “Code Suggestions” label:

<figure>
  <img src='/wp-content/uploads/code-suggestion-2025.png' 
       srcset='/wp-content/uploads/code-suggestion-2025@2x.png' 
       alt="Code suggestion label displayed in the PR list and detailed panel in GitKraken Desktop" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Label for PRs containing code suggestions</figcaption>
</figure>

You can apply or reject each suggestion in the Commit Panel:

<figure>
  <img src='/wp-content/uploads/gkc-pr-code-suggestions-apply.gif' 
       alt="User applying a code suggestion to the main branch from a pull request in GitKraken Desktop" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Review and apply suggestions</figcaption>
</figure>

***

## Commenting and Quoting

Comment on pull requests, refresh the comments feed, or quote replies:

<figure>
  <img src='/wp-content/uploads/refresh-comments-2025.png' 
       srcset='/wp-content/uploads/refresh-comments-2025@2x.png' 
       alt="GitHub Pull Request view in GitKraken Desktop showing reviewers, code diff, and a highlighted refresh comments button" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Refresh and quote comments</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/quote-reply-2025.png' 
       srcset='/wp-content/uploads/quote-reply-2025@2x.png' 
       alt="Highlighted UI option for quoting a reply in a pull request comment thread, with 'Merging is blocked' status below" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Reply with quotes</figcaption>
</figure>

***

## Branch Actions and Build Status

Double-click a branch in the PR view to check it out. Click build status to open in browser.

<figure>
  <img src='/wp-content/uploads/build-status-2025.png' 
       srcset='/wp-content/uploads/build-status-2025@2x.png' 
       alt="Build status section showing a successful Jenkins check completed 15 minutes ago with tooltip 'View Jenkins's latest build'" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Check out branches and monitor CI</figcaption>
</figure>

If the remote isn’t added yet, GitKraken will prompt you to add it.

***

## Merge in GitHub PR View

Click <button class='button button--success button--ui button--nolink'>Merge pull request</button> to merge.

<figure>
  <img src='/wp-content/uploads//merge-options.png' 
       srcset='/wp-content/uploads//merge-options@2x.png' 
       alt="Merge pull request dropdown showing three GitHub merge strategies: Create a merge commit, Squash and merge, and Rebase and merge" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Merge using GitHub PR view options</figcaption>
</figure>

Choose:
- <kbd>Create a merge commit</kbd>
- <kbd>Squash and merge</kbd>
- <kbd>Rebase and merge</kbd>

<div class='callout callout--basic'>
  <p>If data appears out of sync, refresh GitKraken Desktop.</p>
</div>

***

## Active Pull Requests Panel

Active PRs appear with this icon <em class='context-menu'><img style='height:1.5em;' src='/wp-content/uploads/gk-pull-request-icon.svg'></em> and are listed in the PULL REQUESTS section of the Left Panel.

<figure>
  <img src='/wp-content/uploads/pull-request-icon-and-panel-2025.png' 
       srcset='/wp-content/uploads/pull-request-icon-and-panel-2025@2x.png' 
       alt="GitKraken Desktop interface showing the Pull Requests panel expanded with filters and PR list from the origin remote" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Pull request panel and filters</figcaption>
</figure>

Use predefined filters like *My pull requests* or <i>All pull requests</i>, or [create custom filters](/working-with-repositories/pull-requests-filter-syntax/).

Tooltips show branch, author, status, and more:

<figure>
  <img src='/wp-content/uploads//tooltip-general.png' 
       srcset='/wp-content/uploads//tooltip-general@2x.png' 
       alt="Tooltip showing details of a pull request in GitKraken Desktop, including source and target branches, author, and timestamps" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">General tooltip details</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads//tooltip-gitlab.png' 
       srcset='/wp-content/uploads//tooltip-gitlab@2x.png' 
       alt="GitLab tooltip in GitKraken Desktop showing pull request details including branches, author, assignee, and timestamps" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitLab tooltip with an assignee</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads//tooltip-github.png' 
       srcset='/wp-content/uploads//tooltip-github@2x.png' 
       alt="GitHub tooltip in GitKraken Desktop showing pull request details including title, branches, build status, reviewers, assignees, labels, and timestamps" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitHub tooltip with reviewers and build status</figcaption>
</figure>

Pull request icons:
- <i class='fa fa-check' style="color:green"></i> = CI passed and approved
- <i class='fa fa-circle' style="color:orange"></i> = CI passed/pending or reviews pending
- <i class='fa fa-times' style="color:red"></i> = Failing CI or changes requested
