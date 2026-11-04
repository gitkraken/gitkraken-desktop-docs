---
title: Gitflow in GitKraken Desktop
description: Learn how to use Gitflow in GitKraken Desktop to manage features, releases, and hotfixes with organized branching workflows.
product: GitKraken Desktop
feature: Gitflow
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [gitflow, branching, releases, hotfixes, workflow]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: November 2026</kbd>

Use this page to configure and run Gitflow in GitKraken Desktop when your team organizes work into feature, release, and hotfix branches.

**Requirements and limits**
- Workflow scope: Gitflow-style branching with feature, release, and hotfix branches
- Setup location: <kbd>Preferences &gt; Gitflow</kbd>
- Initialization behavior: `main` must already exist locally; GitKraken Desktop creates `develop` if it does not exist
- Panel behavior: Only branches with Gitflow prefixes appear in the **GITFLOW** section of the Left Panel
- Finish behavior: Features merge into `develop`; releases and hotfixes merge into `main` and `develop` and create a tag
- Publishing behavior: Publishing a Gitflow branch works the same as pushing any other Git branch

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/eTOgjQ9o4vQ?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

## Quick Start


1. Go to <kbd>Preferences > Gitflow</kbd>, optionally adjust the default branch names, and click **Initialize Gitflow**.
2. GitKraken Desktop creates `develop` if it does not exist. Your `main` branch must already exist locally.
3. A **GITFLOW** section appears in the Left Panel. To start a branch, click **Open Gitflow** on the section header, then under **Start** click **Feature**, **Release**, or **Hotfix**. You can also create a branch manually with a Gitflow prefix (for example, `feature/my-feature` or `release/1.0.0`).

**To finish a branch type:**
- **Feature**: Merges into `develop`.
- **Release**: Merges into both `main` and `develop`, and creates a tag.
- **Hotfix**: Merges into both `main` and `develop`, and creates a tag.

To finish a branch, right-click it in the Left Panel and select **Finish** followed by the branch name.

Each Finish form has a **Delete branch** checkbox, selected by default, that deletes the branch locally after it is merged. GitKraken Desktop remembers your choice separately for features, releases, and hotfixes.

To set a tag prefix (for example, `v`), go to <kbd>Preferences > Gitflow</kbd>.

***
## How Gitflow configuration works

To configure Gitflow in GitKraken Desktop:

1. Go to <kbd>Preferences > Gitflow</kbd>.
2. Optionally, change the default branch names.
3. Click **Initialize Gitflow**.

<figure>
  <img src="/wp-content/uploads/gitflow-preferences-2025@2x.png" class="help-center-img img-bordered" alt="Gitflow Preferences menu with default branch names">
  <figcaption style="text-align: center; color: #888">Gitflow Preferences menu with default branch names.</figcaption>
</figure>

After you initialize Gitflow, the repository always has these 2 branches:

- <code>main</code>: the version in production.
- <code>develop</code>: the current development version for the next release.

The <code>main</code> branch must already exist locally, or initializing fails with **Failed initializing Gitflow**. If <code>develop</code> does not exist, GitKraken Desktop creates it when Gitflow is initialized: from the remote <code>develop</code> branch if there is one, otherwise from <code>main</code>.

***
## How to use Gitflow

After you initialize Gitflow, a **GITFLOW** section appears in the Left Panel. Click **Open Gitflow** on its header to open the Gitflow panel, where you start and finish Gitflow branches.

<figure>
  <img src="/wp-content/uploads/giflow-panel-2025@2x.png" class="help-center-img img-bordered" alt="Gitflow panel in left sidebar">
  <figcaption style="text-align: center; color: #888">Gitflow panel in left sidebar.</figcaption>
</figure>

To create a Gitflow branch:

- In the Gitflow panel, under **Start**, click **Feature**, **Release**, or **Hotfix**.
- Or name a branch with a Gitflow prefix (for example, <code>release/branch-name</code>).

Branches with a Gitflow prefix appear in the **GITFLOW** section of the Left Panel. Other branches appear only in the **LOCAL** section.

<figure>
  <img src="/wp-content/uploads/prefix-example-2025@2x.png" class="help-center-img img-bordered" alt="Branch name prefixes">
  <figcaption style="text-align: center; color: #888">Branch name prefixes.</figcaption>
</figure>

<div class='callout callout--basic'>
    <p><strong>Note:</strong> The <strong>GITFLOW</strong> section groups feature, release, and hotfix branches into separate folders.</p>
</div>

To publish a Gitflow branch, push it to a remote the same way as any other branch.

### How feature branches work

Feature branches are for new features or bug fixes. They're typically local and not shared.

When you finish a feature branch:

- It's merged into <code>develop</code>.
- It's deleted from the local repository, unless you clear **Delete branch**.

<figure>
  <img src="/wp-content/uploads//finish-feature.gif" class="help-center-img img-bordered" alt="Finishing a feature branch">
  <figcaption style="text-align: center; color: #888">Finishing a feature branch.</figcaption>
</figure>

To rebase the feature branch onto <code>develop</code> before it merges, select **Rebase on develop** in the Finish form.

### How release branches work

Release branches represent versions shared with collaborators.

When you finish a release branch:

- It's merged into both <code>main</code> and <code>develop</code>.
- A tag is created with the release name.
- It's deleted from the local repository, unless you clear **Delete branch**.

If the finish stops on a merge conflict, resolve the conflict and commit the merge. GitKraken Desktop then completes the rest of the finish, including the tag.

<figure>
  <img src="/wp-content/uploads/finish-release-context-menu-2025@2x.png" class="help-center-img img-bordered" alt="Context menu for finishing a release">
  <figcaption style="text-align: center; color: #888">Context menu for finishing a release.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/finish-release-2025@2x.png" class="help-center-img img-bordered" alt="Finish release process">
  <figcaption style="text-align: center; color: #888">Finish release process.</figcaption>
</figure>

### How hotfix branches work

Hotfix branches are similar to releases but created from <code>main</code>. Use them for urgent production fixes, such as bug fixes or typos that must go live immediately.

<figure>
  <img src="/wp-content/uploads/finish-hotfix-2025@2x.png" class="help-center-img img-bordered" alt="Finish hotfix process">
  <figcaption style="text-align: center; color: #888">Finish hotfix process.</figcaption>
</figure>

When you finish a hotfix:

- It's merged into both <code>main</code> and <code>develop</code>.
- A tag is created with the hotfix name.
- It's deleted from the local repository, unless you clear **Delete branch**.

If the finish stops on a merge conflict, resolve the conflict and commit the merge. GitKraken Desktop then completes the rest of the finish, including the tag.

### How Gitflow tags work

Tags mark specific points in your repository's history, such as releases.

Create tags from the Gitflow panel or the command line. When you finish a release or hotfix from the Gitflow panel:

- The tag name is the branch name without its prefix (for example, <code>release/1.0.0</code> → <code>1.0.0</code>, <code>hotfix/1.0.1</code> → <code>1.0.1</code>).
- You can add a message to the tag.

<figure>
  <img src="/wp-content/uploads//finish-release-tag.gif" class="help-center-img img-bordered" alt="Tagging during release">
  <figcaption style="text-align: center; color: #888">Tagging during release.</figcaption>
</figure>

<br>
<br>
<figure>
  <img src="/wp-content/uploads//tag-message.png" class="help-center-img img-bordered" alt="Tag message dialog">
  <figcaption style="text-align: center; color: #888">Tag message dialog.</figcaption>
</figure>

To add a prefix to these tags, enter it in **Version Tag** under <kbd>Preferences > Gitflow</kbd>. For example, the prefix <code>v</code> produces the tag <code>v1.0.0</code>.

<figure>
  <img src="/wp-content/uploads/tag-prefix-2025@2x.png" class="help-center-img img-bordered" alt="Setting tag prefix">
  <figcaption style="text-align: center; color: #888">Setting tag prefix.</figcaption>
</figure>
