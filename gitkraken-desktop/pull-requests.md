---
title: Pull requests
description: Create pull requests directly from GitKraken Desktop and merge one branch into another.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

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
  <img src="/wp-content/uploads/create-pull-request-drag-and-drop-2025.gif" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Start a pull request by dragging a branch</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/create-pr-2025.png" srcset="/wp-content/uploads/create-pr-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Create a pull request from the Left Panel</figcaption>
</figure>

<div class='callout callout'>
  <p><strong>Note:</strong> If the Azure DevOps PR form isn’t populating, see <a href="https://help.gitkraken.com/gitkraken-desktop/azure-devops/#azure-devops-pull-requests-form-not-populating-in-gitkraken-desktop">Azure DevOps Integration</a>.</p>
</div>

***

## Pull Request Templates

GitKraken Desktop supports PR templates on GitHub, GitLab, and Azure DevOps. When committed to the remote, the template appears during PR creation.

<figure>
  <img src="/wp-content/uploads/pr-template-2025.png" srcset="/wp-content/uploads/pr-template-2025@2x.png" class="help-center-img img-bordered">
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
  <img src='/wp-content/uploads/add-reviewers-assignees-labels-2025.png' srcset='/wp-content/uploads/add-reviewers-assignees-labels-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Assign reviewers and labels during PR creation</figcaption>
</figure>

Conflict warnings appear if your source and target branches differ:

<figure>
  <img src='/wp-content/uploads/pr-merge-conflict-warning-2025.png' srcset='/wp-content/uploads/pr-merge-conflict-warning-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Merge conflict warning in PR modal</figcaption>
</figure>

<div class='callout callout--basic'>
  <p><strong>Reminder:</strong> Push your branch before creating a pull request.</p>
</div>

***

## Draft Pull Requests (GitHub)

With GitHub integration, select the draft checkbox to mark the pull request as a draft.

<figure>
  <img src='/wp-content/uploads/create-draft-pr-2025.png' srcset='/wp-content/uploads/create-draft-pr-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Enable draft pull request in GitHub</figcaption>
</figure>

***

## GitHub Pull Request View

Enable the GitHub integration to access GitHub PR view:
- Select a PR in the Left Panel
- Or click the PR icon in the Launchpad

<figure>
  <img src='/wp-content/uploads/github-pr-view-2025.png' srcset='/wp-content/uploads/github-pr-view-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitHub pull request view in the repo tab</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/launchpad-open-pr-panel-2025.png' srcset='/wp-content/uploads/launchpad-open-pr-panel-2025@2x.png' class="help-center-img img-bordered">
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

Suggest edits directly in GitKraken Desktop or [gitkraken.dev](https://gitkraken.dev?source=help_center&product=gitkraken).

<figure>
  <img src='/wp-content/uploads/gkd-10-2-0-pr-suggest-code-changes.gif' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Suggest code changes inside a pull request</figcaption>
</figure>

***

## Accept or Reject Suggestions

Code suggestions display in the PR view under the “Code Suggestions” label:

<figure>
  <img src='/wp-content/uploads/code-suggestion-2025.png' srcset='/wp-content/uploads/code-suggestion-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Label for PRs containing code suggestions</figcaption>
</figure>

You can apply or reject each suggestion in the Commit Panel:

<figure>
  <img src='/wp-content/uploads/gkc-pr-code-suggestions-apply.gif' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Review and apply suggestions</figcaption>
</figure>

***

## Commenting and Quoting

Comment on pull requests, refresh the comments feed, or quote replies:

<figure>
  <img src='/wp-content/uploads/refresh-comments-2025.png' srcset='/wp-content/uploads/refresh-comments-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Refresh and quote comments</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/quote-reply-2025.png' srcset='/wp-content/uploads/quote-reply-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Reply with quotes</figcaption>
</figure>

***

## Branch Actions and Build Status

Double-click a branch in the PR view to check it out. Click build status to open in browser.

<figure>
  <img src='/wp-content/uploads/build-status-2025.png' srcset='/wp-content/uploads/build-status-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Check out branches and monitor CI</figcaption>
</figure>

If the remote isn’t added yet, GitKraken will prompt you to add it.

***

## Merge in GitHub PR View

Click <button class='button button--success button--ui button--nolink'>Merge pull request</button> to merge.

<figure>
  <img src='/wp-content/uploads//merge-options.png' srcset='/wp-content/uploads//merge-options@2x.png' class="help-center-img img-bordered">
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
  <img src='/wp-content/uploads/pull-request-icon-and-panel-2025.png' srcset='/wp-content/uploads/pull-request-icon-and-panel-2025@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Pull request panel and filters</figcaption>
</figure>

Use predefined filters like *My pull requests* or <i>All pull requests</i>, or [create custom filters](/working-with-repositories/pull-requests-filter-syntax/).

Tooltips show branch, author, status, and more:

<figure>
  <img src='/wp-content/uploads//tooltip-general.png' srcset='/wp-content/uploads//tooltip-general@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">General tooltip details</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads//tooltip-gitlab.png' srcset='/wp-content/uploads//tooltip-gitlab@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitLab tooltip with labels and assignee</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads//tooltip-github.png' srcset='/wp-content/uploads//tooltip-github@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitHub tooltip with reviewers and build status</figcaption>
</figure>

Pull request icons:
- <i class='fa fa-check' style="color:green"></i> = CI passed and approved
- <i class='fa fa-circle' style="color:orange"></i> = CI passed/pending or reviews pending
- <i class='fa fa-times' style="color:red"></i> = Failing CI or changes requested
