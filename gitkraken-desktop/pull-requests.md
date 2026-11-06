---
title: Pull Requests in GitKraken Desktop
description: Create, manage, and review pull requests in GitKraken Desktop. Supports GitHub, GitLab, Bitbucket, Azure DevOps, and includes templates, comments, and suggestions.
product: GitKraken Desktop
feature: Pull Requests
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps]
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [pull-requests, review, templates, suggestions, merge]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "working-with-repositories"
    nav_label: "Pull Requests"
    nav_order: 120
    nav_parent: "working-with-repositories"
    page_type: "content"
---
<kbd>Last updated: November 2026</kbd>

Use this page to create, review, filter, comment on, and merge pull requests (PRs) in GitKraken Desktop on GitHub, GitLab, Bitbucket, and Azure DevOps. On GitHub, you also get GitHub Pull Request View, stacked pull requests, code suggestions, and in-app merge options. To review a pull request, you open it in GitKraken Code Review on GitKraken.dev.

**Requirements and limits**
- Supported providers on this page: GitHub, GitLab, Bitbucket, and Azure DevOps
- Precondition: Push your branch to the remote before creating a pull request
- GitHub-only features: GitHub Pull Request View, stacked pull requests on GitHub.com, code suggestions, and in-app merge options
- Pull request review: **Review on GitKraken.dev** opens GitHub, GitLab, and Azure DevOps pull requests in GitKraken Code Review in your browser; it is not available in GitKraken On-Premise (Self-Hosted Server and Serverless)
- Template support: Pull request templates are supported for GitHub, GitLab, and Azure DevOps
- Azure DevOps note: If the PR form does not populate, check the remote URL and integration domain on the Azure DevOps integration page

| Provider | Create PR or MR | View PR or MR | Merge in app | Notes |
|----------|------------------|---------------|--------------|-------|
| GitHub | Yes | Yes | Yes | GitHub Pull Request View and stacked pull requests are GitHub-only |
| GitLab | Yes | Yes | Yes | Uses merge request terminology |
| Bitbucket | Yes | Yes | Yes | Some reviewer workflows depend on permissions |
| Azure DevOps | Yes | Yes | Yes | Verify remote URL and integration domain if the form does not populate |

***

## Quick Start


**To create a pull request:** Push your branch to the remote, then use one of these:
- Drag one branch onto another in the graph and select **Start a pull request**.
- Right-click the target branch and choose the same option.
- Click the **+** icon in the PULL REQUESTS section of the Left Panel.

**To review a pull request:** Right-click the pull request in the Left Panel and select **Review on GitKraken.dev**. The pull request opens in [GitKraken Code Review](https://gitkraken.dev?source=help_center&product=gitkraken) in your browser, where you can review the changes, use AI-generated suggestions, and approve or comment. Review is available for GitHub, GitLab, and Azure DevOps pull requests. For other places to start a review, see [How to review pull requests with GitKraken Code Review](#how-to-review-pull-requests-with-gitkraken-code-review).

**To view a GitHub pull request's changes in the graph:** Right-click the pull request in the Left Panel and select **View changes in #N**, where #N is the pull request number.

**To merge a pull request:** Click **Merge Pull Request** in GitHub Pull Request View and select a merge strategy (merge commit, squash, or rebase).

**To create a stacked pull request on GitHub.com:** Create a pull request from a branch whose target already has an open pull request. In the Create Pull Request panel, select **Start a pull request stack** or **Add this pull request to an existing stack**. GitKraken Desktop shows which pull requests the new one will stack on.

**To filter pull requests:** Use a predefined filter such as **My Pull Requests**, or create custom filters in the Left Panel. PR icons show CI status and review state.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/2VX1ISk9XH8?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***

## How to create a pull request

Push your branch to the remote first. Then use one of these:
- Drag one branch onto another and select <em class='context-menu'>Start a pull request</em>
- Right-click the target branch and choose the same option
- Click the <button class='button button--success button--ui button--nolink'>+</button> icon in the Left Panel PULL REQUESTS section

<div class='callout callout--basic'>
  <p><strong>Use GitKraken Desktop PR creation when:</strong> your branch is already pushed and you want to open or manage the PR without leaving the app. <strong>Do not start the PR yet when:</strong> the branch is not pushed, the target branch is still unclear, or you need provider-specific options not exposed in GitKraken Desktop.</p>
</div>

<figure>
  <img src="/wp-content/uploads/create-pull-request-drag-and-drop-2025.gif" alt="User initiates a pull request in GitKraken Desktop by dragging a local branch (PM-34-docs-review-pr-page) onto the remote origin/main. The Create Pull Request dialog then appears, pre-filled with repository and branch information, ready for title, description, and assignee input." class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Start a pull request by dragging a branch</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/create-pr-2025@2x.png" 
       alt="User clicks the plus button in the Pull Requests section of GitKraken Desktop's Left Panel to open the Create Pull Request interface. The dialog appears with fields to select repositories, branches, title, description, and other PR options." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Create a pull request from the Left Panel</figcaption>
</figure>

<div class='callout callout'>
  <p><strong>Note:</strong> If the Azure DevOps PR form is not populating, see <a href="https://help.gitkraken.com/gitkraken-desktop/azure-devops/#azure-devops-pull-requests-form-not-populating-in-gitkraken-desktop">Azure DevOps Integration</a>.</p>
</div>

***

## How stacked pull requests work on GitHub.com

A stacked pull request targets the branch of another open pull request. Use a stack to split related work into smaller pull requests while keeping the branch relationship visible.

To create or extend a stack:

1. Create a pull request from a branch whose target branch has an open pull request in the same repository. Pull requests from forks cannot be stacked.
2. In the Create Pull Request panel, select the stacking option:
   - **Start a pull request stack** appears when the target pull request is not in a stack yet.
   - **Add this pull request to an existing stack** appears when the target pull request is already in a stack.
3. Confirm the pull requests listed below the option, such as **This pull request will be stacked with #103**. Click a pull request number to open it in your browser.
4. Click **Create Pull Request**.

If you change the target branch, GitKraken Desktop clears the stacking option. If GitKraken Desktop creates the pull request but cannot add it to the stack, you see **Pull request created, but it could not be stacked**.

<figure>
  <img src='/wp-content/uploads/gkd-12-6-stacked-pr-create.png' 
       alt="Bottom of the Create Pull Request panel in GitKraken Desktop with the Add this pull request to an existing stack checkbox selected and the message This pull request will be stacked with #104 and #103, above the Cancel and Create Pull Request buttons." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Add a new pull request to an existing stack</figcaption>
</figure>

GitKraken Desktop shows a pull request's place in its stack in GitHub Pull Request View, the Commit Panel, the graph, and the Left Panel, so you can move between related pull requests.

In GitHub Pull Request View, the header shows the pull request's position in the stack, such as **2/2**. Use the arrows next to it to move between the open pull requests in the stack. Above **Merge Pull Request**, GitKraken Desktop lists each pull request in the stack down to the base branch, with a status for each one: **Ready**, **Not ready**, **Draft**, **Merged**, **Closed**, or **Blocked downstack**.

<figure>
  <img src='/wp-content/uploads/gkd-12-6-stacked-pr-view.png' 
       alt="GitHub Pull Request View in GitKraken Desktop for pull request #104, showing its stack position 2/2 with previous and next arrows in the header, and a list of the stacked pull requests #104 and #103 above the main base branch and the Merge Pull Request button." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">View and navigate a pull request stack in GitHub Pull Request View</figcaption>
</figure>

When you select a commit that has a stacked pull request, the Commit Panel shows the stack position, such as **1/2**, next to the pull request. Hover over the position to see every pull request in the stack, its status, and its branch, down to the base branch of the stack:

- Click an open pull request to open it in GitHub Pull Request View.
- Click a branch to select it in the graph.
- Double-click a branch to check it out.

In the graph, hover over a pull request icon on a branch to see the pull request's position in its stack. The pull request tooltip in the Left Panel also shows the position.

<figure>
  <img src='/wp-content/uploads/gkd-12-6-stacked-pr-graph.png' 
       alt="GitKraken Desktop graph showing the kepler/update-docs-12-6 branch with a tooltip reading #103 (1 of 2): Documents GitKraken Desktop v12.6.0 features." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">See a pull request's stack position from the graph</figcaption>
</figure>

***

## How pull request templates work

GitKraken Desktop supports PR templates on GitHub, GitLab, and Azure DevOps. After you commit a template to the remote, you can select it in the **Template** field when you create a pull request.

<figure>
  <img src="/wp-content/uploads/pr-template-2025@2x.png" 
       alt="GitKraken Desktop interface displaying the Create Pull Request dialog with a dropdown field for selecting a pull request template. The template 'pull_request_template.md' is highlighted." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Pull request template field shown during creation</figcaption>
</figure>

Tips:
- Store the template where your provider's documentation says
- Make sure the template is on the branch you have checked out

Resources:
- [GitHub PR templates](https://help.github.com/articles/creating-a-pull-request-template-for-your-repository/)
- [GitLab merge request templates](https://docs.gitlab.com/ee/user/project/description_templates.html)
- [Azure DevOps PR templates](https://docs.microsoft.com/en-us/azure/devops/repos/git/pull-request-templates?view=azure-devops)

***

## How assignees, labels, and reviewers work

Depending on the integration, you can add these when you create a pull request:
- Assignees
- Reviewers
- Labels

<figure>
  <img src='/wp-content/uploads/add-reviewers-assignees-labels-2025@2x.png' 
       alt="GitKraken Desktop pull request creation screen showing fields for assigning reviewers, assignees, and labels. Two reviewers, two assignees, and two labels are selected." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Assign reviewers and labels during PR creation</figcaption>
</figure>

If the source and target branches have a merge conflict, the panel shows **Merge conflict detected**:

<figure>
  <img src='/wp-content/uploads/pr-merge-conflict-warning-2025@2x.png' 
       alt="GitKraken Desktop Create Pull Request screen displaying a warning banner indicating a merge conflict between the source and target branches." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Merge conflict warning in PR modal</figcaption>
</figure>

***

## How draft pull requests work on GitHub

With the GitHub integration, select **Submit as draft** to create the pull request as a draft.

<div class='callout callout--basic'>
  <p><strong>Use a draft pull request when:</strong> you want early visibility or feedback before the branch is ready to merge. <strong>Do not mark it ready too early when:</strong> the implementation still needs major changes and you are not ready for formal review.</p>
</div>

<figure>
  <img src='/wp-content/uploads/create-draft-pr-2025@2x.png' 
       alt="GitKraken Desktop showing the Create Pull Request form with the 'Submit as draft' checkbox enabled." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Enable draft pull request in GitHub</figcaption>
</figure>

***

## How GitHub Pull Request View works

With the GitHub integration connected, open GitHub Pull Request View in either of these ways:
- Select a PR in the Left Panel
- Click the PR icon in Launchpad

<div class='callout callout--basic'>
  <p><strong>Use GitHub Pull Request View when:</strong> you want to update PR metadata, check build status, or merge inside GitKraken Desktop. <strong>Do not rely on it for every review workflow when:</strong> your team depends on deeper provider-native review features outside the app.</p>
</div>

<figure>
  <img src='/wp-content/uploads/github-pr-view-2025@2x.png' 
       alt="GitKraken Desktop displaying the GitHub pull request view for PR #1993, which adds Arm64 support for Windows and Linux." 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitHub pull request view in the repo tab</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/launchpad-open-pr-panel-2025@2x.png' 
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

To review the changes, click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Review on GitKraken.dev</span></button> below the number of changed files. See [How to review pull requests with GitKraken Code Review](#how-to-review-pull-requests-with-gitkraken-code-review).

***

## How to review pull requests with GitKraken Code Review

Pull requests open for review in [GitKraken Code Review](https://gitkraken.dev?source=help_center&product=gitkraken) on GitKraken.dev, in your browser. Review works for GitHub, GitLab, and Azure DevOps pull requests.

To start a review, use any of these:

- In GitHub Pull Request View, click <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Review on GitKraken.dev</span></button>.
- In the PULL REQUESTS section of the Left Panel, right-click a pull request and select **Review on GitKraken.dev**.
- In the graph or the Left Panel, right-click a branch that has a pull request and select **Review on GitKraken.dev**.
- In Launchpad, select **Review Pull Request** in the pull request's actions.

<div class='callout callout--warning'>
  <p><strong>GitKraken On-Premise users:</strong> <strong>Review on GitKraken.dev</strong> and <strong>Review Pull Request</strong> are not available in Self-Hosted Server or Serverless deployments.</p>
</div>

In GitKraken Code Review, you can:
- Read the pull request's diffs
- Get AI-generated review suggestions
- Chat with the rest of your team
- Approve and comment as you would on your hosting service

<figure>
  <img src='/wp-content/uploads/code-review-actions.png' 
       alt="List of actions available through GitKraken.dev Code Review" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">List of actions available through GitKraken.dev Code Review</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/code-review-AI-panel.png' 
       alt="AI-assisted code review summary in GitKraken.dev" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">AI-assisted code review summary in GitKraken.dev</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/code-review-comment.png' 
       alt="Commenting on a pull request in GitKraken.dev Code Review" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Commenting on a pull request in GitKraken.dev Code Review</figcaption>
</figure>

***

## How to accept or reject suggestions

GitHub Pull Request View lists a pull request's code suggestions under **Code Suggestions**:

<figure>
  <img src='/wp-content/uploads/code-suggestion-2025@2x.png' 
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

## How commenting and quoting work

Comment on pull requests, refresh the comments feed, or quote replies:

<figure>
  <img src='/wp-content/uploads/refresh-comments-2025@2x.png' 
       alt="GitHub Pull Request view in GitKraken Desktop showing reviewers, code diff, and a highlighted refresh comments button" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Refresh and quote comments</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/quote-reply-2025@2x.png' 
       alt="Highlighted UI option for quoting a reply in a pull request comment thread, with 'Merging is blocked' status below" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Reply with quotes</figcaption>
</figure>

***

## How branch actions and build status work

In GitHub Pull Request View, double-click a branch to check it out. Click the build status to open the latest build in your browser.

<figure>
  <img src='/wp-content/uploads/build-status-2025@2x.png' 
       alt="Build status section showing a successful Jenkins check completed 15 minutes ago with tooltip 'View Jenkins's latest build'" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Check out branches and monitor CI</figcaption>
</figure>

If the branch's remote is not in your repository yet, GitKraken Desktop prompts you to add it.

***

## How to merge in GitHub PR View

Click <button class='button button--success button--ui button--nolink'>Merge Pull Request</button> to merge.

<figure>
  <img src='/wp-content/uploads/merge-options@2x.png' 
       alt="Merge pull request dropdown showing three GitHub merge strategies: Create a merge commit, Squash and merge, and Rebase and merge" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Merge using GitHub PR view options</figcaption>
</figure>

Choose a merge strategy:
- <kbd>Create a merge commit</kbd>
- <kbd>Squash and merge</kbd>
- <kbd>Rebase and merge</kbd>

<div class='callout callout--basic'>
  <p>If data appears out of sync, refresh GitKraken Desktop.</p>
</div>

***

## How the active pull requests panel works

Active PRs appear with this icon <em class='context-menu'><img alt="" style='height:1.5em;' src='/wp-content/uploads/gk-pull-request-icon.svg'></em> and are listed in the PULL REQUESTS section of the Left Panel.

<figure>
  <img src='/wp-content/uploads/pull-request-icon-and-panel-2025@2x.png' 
       alt="GitKraken Desktop interface showing the Pull Requests panel expanded with filters and PR list from the origin remote" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Pull request panel and filters</figcaption>
</figure>

Use the predefined filters **My Pull Requests** or **All Pull Requests**, or [create custom filters](/working-with-repositories/pull-requests-filter-syntax/).

Tooltips show branch, author, status, and more:

<figure>
  <img src='/wp-content/uploads/tooltip-general@2x.png' 
       alt="Tooltip showing details of a pull request in GitKraken Desktop, including source and target branches, author, and timestamps" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">General tooltip details</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/tooltip-gitlab@2x.png' 
       alt="GitLab tooltip in GitKraken Desktop showing pull request details including branches, author, assignee, and timestamps" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitLab tooltip with an assignee</figcaption>
</figure>

<figure>
  <img src='/wp-content/uploads/tooltip-github@2x.png' 
       alt="GitHub tooltip in GitKraken Desktop showing pull request details including title, branches, build status, reviewers, assignees, labels, and timestamps" 
       class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">GitHub tooltip with reviewers and build status</figcaption>
</figure>

Pull request icons:
- <i class='fa fa-check' style="color:green"></i> = CI passed and approved
- <i class='fa fa-circle' style="color:orange"></i> = CI passed/pending or reviews pending
- <i class='fa fa-times' style="color:red"></i> = Failing CI or changes requested

### How to view a pull request's changes in the graph

For GitHub and GitHub Enterprise pull requests, you can see all of a pull request's changes in one diff:

1. Right-click the pull request in the PULL REQUESTS section of the Left Panel, or right-click a branch that has a pull request in the graph.
2. Select **View changes in #N**, where #N is the pull request number.

GitKraken Desktop selects the pull request's base and head commits in the graph, and the Commit Panel shows the full diff of the pull request.

- If the pull request's branch comes from a remote that is not in your repository, GitKraken Desktop asks whether to add it, for example **Do you want to add "fork-owner" as a remote to view "feature-branch"?** Accept to add the remote and continue.
- If the base or head commit is not loaded in the graph, a message tells you how old the commit is. Scroll down the graph, or increase **Initial Commits in Graph** in <kbd>Preferences > General</kbd>, then try again.

***

## How merged pull request status appears in the interface

When a pull request is merged, GitKraken Desktop shows a merged PR status pill in 3 places for the branch. The pill appears for GitHub, GitLab, Bitbucket, and Azure DevOps, including GitHub Enterprise, GitLab Self-Managed, and Bitbucket Data Center.

| Location | When it appears |
|----------|-----------------|
| **Toolbar** | When the branch with a merged PR is checked out |
| **Commit Panel** | When you select a commit on the branch with a merged PR |
| **Worktree cards** (Agents view) | On the card for the branch with a merged PR |

Use the merged PR pill to confirm that a branch's work has shipped before you delete the branch or remove its worktree.
