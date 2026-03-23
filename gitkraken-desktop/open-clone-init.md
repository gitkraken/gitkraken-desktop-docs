---
title: Open, Clone, or Initialize a Git Repository in GitKraken Desktop
description: Learn how to open, clone, or initialize repositories in GitKraken Desktop. Get started with repository management and project setup.
product: GitKraken Desktop
feature: Repository Management
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps, generic]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps]
hosted_variant: both
status: GA
last_verified: 2026-03
llms_include: true
tags: [open, clone, init, shallow-clone, sparse-checkout]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to open an existing local repository, clone a remote repository, or initialize a new repository in GitKraken Desktop. It also covers shallow clone, sparse checkout, and the Repository Management tab so you can choose the right setup path for a new or existing project.

**Requirements and limits**
- Entry points: Repository Management tab, New Tab, or <kbd>File &gt; Clone / Init / Open</kbd>
- Open workflow: Requires an existing local Git repository
- Clone workflow: Requires a remote repository URL or a connected integration
- Shallow clone: Supports branch, depth, since-date, and custom clone flags
- Sparse checkout: Root-level files are always checked out even when path rules are applied
- Initialize workflow: Creates a `.git` directory and can optionally add a `README.md`, `.gitignore`, and `LICENSE`

***

## Quick Start

Open, clone, or initialize repositories in GitKraken Desktop from the Repository Management tab.

**To open an existing local repository:**
1. Click the folder icon in the top-left corner or press <kbd>Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + O</kbd> (Mac).
2. Click **Browse** and select your repository folder.

**To clone a remote repository:**
1. Open the Repository Management tab and click **Clone**.
2. Enter the repository URL or select a repository from your connected integration.
3. Click **Clone the repo** to download it locally.

**To initialize a new repository:**
1. Click **Init** in the Repository Management tab.
2. Fill in the repository path and optional settings (`.gitignore`, license).
3. Click **Create Repository** to create the repo and open it.

Shallow clone is supported when cloning. Enable the **Shallow Clone** option in the Clone dialog to limit commit history by depth or date. Access all three options from the Repository Management tab, the New Tab, or <kbd>File > Clone / Init / Open</kbd>.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8uxrA56VJgY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***
## How to complete the initial setup
Complete these setup steps before managing repositories:

1. [Install GitKraken Desktop](/gitkraken-desktop/how-to-install)
2. Create an account and configure your [profile](/gitkraken-desktop/profiles)

***
## How Repository Management works

The **Repository Management** tab provides an overview of active repositories, Workspaces, and favorites. Open this tab by clicking the folder icon in the top-left or using:
- <kbd>Alt + O</kbd> (Windows/Linux)
- <kbd>Cmd + O</kbd> (Mac)

<figure>
  <img src='/wp-content/uploads/repo-mgmt-2025@2x.png' class="help-center-img img-bordered"   alt="Repository Management tab showing buttons for Browse, Clone, and Init, with open, favorite, and recent repositories listed by group.">
  <figcaption style="text-align:center; color:#888">Repository Management tab in GitKraken Desktop</figcaption>
</figure>

From here, you can:
- **Browse**: Open a local Git repository.
- **Clone**: Copy a remote Git repository to your machine.
- **Init**: Initialize a new Git repository or reinitialize an existing one.

This tab also includes Workspaces and repository actions:
- Open in VS Code
- View repository details (README.md panel)
- Open/Close repo tab

***
### How to open an existing project

To open an existing repo:

1. From Repository Management, select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Browse</span></button>
2. Use the file explorer to locate your repo

<figure>
  <img src='/wp-content/uploads/open-repo-2025@2x.png'  class="help-center-img img-bordered" alt="Repository Management screen with the Browse button highlighted to open an existing repository">
  <figcaption style="text-align:center; color:#888">Select an existing repository to open</figcaption>
</figure>

You can also access this via the <strong>New Tab</strong> by clicking the + icon.


#### How to open shallow-cloned repositories

GitKraken Desktop supports opening shallow cloned repositories.

No special setup is required. Just navigate to the shallow clone’s location and open it as you would any other repository (see above).

***
### How to clone a project

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OA9o09Bq5M8?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

To clone a remote repo:

1. In Repository Management, select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Clone</span></button>

<figure>
  <img src='/wp-content/uploads/clone-repo-mgmt-2025@2x.png' class="help-center-img img-bordered" alt="Repository Management tab with the Clone button highlighted in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Clone from Repository Management tab</figcaption>
</figure>

2. You can also access clone options via <kbd><strong>File > Clone</strong></kbd> or the New Tab.

<figure>
  <img src='/wp-content/uploads/clone-url@2x.png' class="help-center-img img-bordered" alt="Clone a Repo dialog with URL input and provider options in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Enter the clone URL to start</figcaption>
</figure>

#### How shallow clone works

GitKraken Desktop supports **shallow cloning** when cloning a repository. Shallow clones let you limit the commit history that is downloaded, which can significantly reduce clone time and disk usage for large repositories.

To perform a shallow clone:

1. Open the **Clone** dialog from **Repository Management**, the **New Tab**, or <kbd><strong>File > Clone</strong></kbd>.
2. Select the repository you want to clone.
3. Enable the **Shallow Clone** option.

<figure>
  <img src="/wp-content/uploads/perform-shallow-clone@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop shallow clone options, including branch to clone, depth, since date, and custom flags">
  <figcaption style="text-align: center; color: #888">Shallow Clone option in the Clone dialog</figcaption>
</figure>

When **Shallow Clone** is selected, additional options become available:

- **Branch to clone**: Specify the branch to clone. By default, GitKraken Desktop uses the repository’s default branch.
- **Depth**: Set how many commits deep to clone from the selected branch.
- **Since date**: Limit the clone to commits newer than a specific date.
- **Custom flags**: Provide any additional flags you typically pass to the `git clone` command. Enter these exactly as you would in the command-line interface.

4. Click <button class='button button--success button--ui button--nolink'>Clone the repo!</button> to complete the shallow clone.

After cloning, the repository opens automatically in GitKraken Desktop.

#### How sparse checkout works

Sparse checkout lets you check out only a subset of files from a repository, keeping your working directory smaller and improving performance on large repositories such as monorepos.

To perform a sparse checkout when cloning:

1. Open the **Clone** dialog from **Repository Management**, the **New Tab**, or <kbd><strong>File > Clone</strong></kbd>.
2. Select the repository you want to clone.
3. Enable the **Sparse Checkout** option.
4. In the **Paths to include** field, enter one path per line (for example, `src/`, `docs/`, `README.md`). If no paths are provided, only root-level files will be checked out.

<figure>
  <img src="/wp-content/uploads/sparse-checkout.png" class="help-center-img img-bordered" alt="GitKraken Desktop Clone dialog with Sparse Checkout enabled, showing a Blobless clone option and a Paths to include text field with example paths such as src/, docs/, and README.md">
  <figcaption style="text-align: center; color: #888">Enable Sparse Checkout in the Clone dialog and specify which paths to include.</figcaption>
</figure>

5. Click <button class='button button--success button--ui button--nolink'>Clone the repo!</button> to complete the clone.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Files at the root of the repository are always checked out regardless of the paths you specify.</p>
</div>

**Configuring sparse checkout on an existing repository**

To enable or update sparse checkout rules on a repository you have already opened, go to <kbd>Preferences > Sparse Checkout</kbd> for that repository.

<figure>
  <img src="/wp-content/uploads/sparse-checkout-preferences.png" class="help-center-img img-bordered" alt="GitKraken Desktop Repo-Specific Preferences panel open to the Sparse Checkout section, showing a Paths to include text field and three action buttons: Enable sparse checkout, Disable sparse checkout, and Reapply sparse checkout">
  <figcaption style="text-align: center; color: #888">Configure sparse checkout paths and actions under Repo-Specific Preferences.</figcaption>
</figure>

From this panel you can:
- **Enable sparse checkout** — activates sparse checkout using the paths you have entered.
- **Disable sparse checkout** — turns off sparse checkout and restores the full working directory.
- **Reapply sparse checkout** — re-applies the current path rules, useful after pulling in new files or resolving inconsistencies.

When a repository has sparse checkout active, a **Sparse** button appears in the toolbar. Click it to quickly edit your sparse checkout paths, disable sparse checkout, or reapply the current rules without opening Preferences.

<figure>
  <img src="/wp-content/uploads/toolbar-action-for-sparse-checkout-repos.png" class="help-center-img img-bordered" alt="GitKraken Desktop toolbar showing the Sparse button expanded, with a dropdown menu listing Sparse Checkout Commands: Edit sparse checkout paths, Disable sparse checkout, and Reapply sparse checkout">
  <figcaption style="text-align: center; color: #888">The Sparse toolbar button provides quick access to sparse checkout commands on active repos.</figcaption>
</figure>


***
### How to initialize a new project

To start a new repo:

1. Select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Init</span></button> in Repository Management.

<figure>
  <img src='/wp-content/uploads/init-2025@2x.png' class="help-center-img img-bordered" alt="Initialize a Repository dialog in GitKraken Desktop showing local and remote provider options, with fields for repo name, location, and additional settings">
  <figcaption style="text-align:center; color:#888">Repository initialization options</figcaption>
</figure>

2. Fill in:
   - Repository path
   - `.gitignore` template (optional)
   - License (optional)

3. Click <button class='button button--success button--ui button--nolink'>Create Repository</span></button>

Also accessible via <kbd><strong>File > Init</strong></kbd> or New Tab.

**Initialization result:**
- `.git` directory created
- Repo opens in GitKraken Desktop
- Includes `README.md`, and optionally `.gitignore` and `LICENSE`

<div class='callout callout--success'>
    <p>You can also initialize a repository directly to GitHub, Bitbucket, or other remote providers.</p>
</div>

***
### How to customize Repository Management

- Drag and drop group headers to reorder
- Change colors via <kbd>Change color</kbd> in the repo group menu
- Set default colors in <kbd>Preferences > UI Customization</kbd>

<figure>
  <img src='/wp-content/uploads/gkd-repo-mgm-tab-customize1.gif' class="help-center-img img-bordered" alt="User interacting with GitKraken Desktop Repository Management tab to change the color of a repo group via the group menu">
  <figcaption style="text-align:center; color:#888">Customize repo group layout and colors</figcaption>
</figure>
