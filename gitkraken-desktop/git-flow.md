---
title: Gitflow in GitKraken Desktop
description: Learn how to use Gitflow in GitKraken Desktop to manage features, releases, and hotfixes with organized branching workflows.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to configure and run Gitflow in GitKraken Desktop when your team organizes work into feature, release, and hotfix branches. It covers the initial Gitflow setup, how the Gitflow panel works, and what happens when each Gitflow branch type is finished.

**Requirements and limits**
- Workflow scope: Gitflow-style branching with feature, release, and hotfix branches
- Setup location: <kbd>Preferences &gt; Gitflow</kbd>
- Initialization behavior: GitKraken Desktop creates `main` and `develop` locally if they do not exist
- Panel behavior: Only branches with Gitflow prefixes appear in the Gitflow panel
- Finish behavior: Features merge into `develop`; releases merge into `main` and `develop` and create a tag; hotfixes merge into `main` and `develop`
- Publishing behavior: Publishing a Gitflow branch works the same as pushing any other Git branch

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/eTOgjQ9o4vQ?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

## Quick Start

Set up and use Gitflow in GitKraken Desktop to manage features, releases, and hotfixes with structured branches.

1. Go to <kbd>Preferences > Gitflow</kbd> and initialize Gitflow for the repository. Optionally adjust default branch names.
2. GitKraken Desktop creates `main` and `develop` branches if they do not exist.
3. A **Gitflow** panel appears in the Left Panel. Click the green button to start a branch, or create a branch manually using a Gitflow prefix (e.g., `feature/my-feature`, `release/1.0.0`).

**To finish a branch type:**
- **Feature**: Merges into `develop` and deletes the branch locally.
- **Release**: Merges into both `main` and `develop`, and creates a tag.
- **Hotfix**: Merges into both `main` and `develop`.

Right-click a Gitflow branch in the Left Panel and select **Finish** to complete it. To set a tag prefix (e.g., `v`), configure it under <kbd>Preferences > Gitflow</kbd>. Publishing a Gitflow branch to a remote works the same as pushing any other branch.

***
## How Gitflow configuration works

To configure Gitflow in GitKraken Desktop:

1. Navigate to <code>Preferences > Gitflow</code>.
2. Optionally, change the default branch names.

<img src="/wp-content/uploads/gitflow-preferences-2025@2x.png" class="help-center-img img-bordered" alt="Gitflow Preferences menu with default branch names">

Once initialized, two branches will always be present:

- <code>main</code>: the version in production.
- <code>develop</code>: the current development version for the next release.

If these branches don't exist locally, GitKraken Desktop will create them when Gitflow is initialized.

***
## How to use Gitflow

After initializing Gitflow, a Gitflow panel appears in the left sidebar. Use it to start or finish Gitflow branches.

<img src="/wp-content/uploads/giflow-panel-2025@2x.png" class="help-center-img img-bordered" alt="Gitflow panel in left sidebar">

To create a Gitflow branch:

- Click the green button in the Gitflow panel.
- Or name a branch with a Gitflow prefix (e.g., <code>release/branch-name</code>).

Branches with a Gitflow prefix appear in the Gitflow panel. Others appear in the local repository section only.

<img src="/wp-content/uploads/prefix-example-2025@2x.png" class="help-center-img img-bordered" alt="Branch name prefixes">

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Gitflow organizes features, hotfixes, and releases into separate folders.</p>
</div>

Publishing a Gitflow branch (i.e., pushing it to a remote) works the same as with regular Git branches.

### How feature branches work

Feature branches are for new features or bug fixes. They're typically local and not shared.

When you finish a feature branch:

- It's merged into <code>develop</code>.
- It's deleted from the local repository.

<img src="/wp-content/uploads//finish-feature.gif" class="help-center-img img-bordered" alt="Finishing a feature branch">

Optionally, rebase the feature branch onto <code>develop</code> before finishing.

### How release branches work

Release branches represent versions shared with collaborators.

When you finish a release branch:

- It's merged into both <code>main</code> and <code>develop</code>.
- A tag is created with the release name.

<img src="/wp-content/uploads/finish-release-context-menu-2025@2x.png" class="help-center-img img-bordered" alt="Context menu for finishing a release">

<img src="/wp-content/uploads/finish-release-2025@2x.png" class="help-center-img img-bordered" alt="Finish release process">

### How hotfix branches work

Hotfix branches are similar to releases but created from <code>main</code>. Use them for urgent production fixes.

Examples include bug fixes or typos that must go live immediately.

<img src="/wp-content/uploads/finish-hotfix-2025@2x.png" class="help-center-img img-bordered" alt="Finish hotfix process">

When you finish a hotfix:

- It's merged into both <code>main</code> and <code>develop</code>.

### How Gitflow tags work

Tags mark specific points in your repository's history, such as releases.

Create tags from the Gitflow panel or the command line. When tagging from the Gitflow panel:

- The tag name matches the branch name (e.g., <code>release/1.0.0</code> → <code>1.0.0</code>).
- You can add a message to the tag.

<img src="/wp-content/uploads//finish-release-tag.gif" class="help-center-img img-bordered" alt="Tagging during release">

<br>
<br>
<img src="/wp-content/uploads//tag-message.png" class="help-center-img img-bordered" alt="Tag message dialog">

In <code>Preferences > Gitflow</code>, set a tag prefix (e.g., <code>v</code>). This prefix is added to tags (e.g., <code>v1.0.0</code>).

<img src="/wp-content/uploads/tag-prefix-2025@2x.png" class="help-center-img img-bordered" alt="Setting tag prefix">
