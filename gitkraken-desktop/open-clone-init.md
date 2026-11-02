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
last_verified: 2026-11
llms_include: true
tags: [open, clone, init, shallow-clone, sparse-checkout, command-line]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

<div style="display:flex; flex-wrap:wrap; align-items:center; gap:8px 32px; margin-bottom:24px;">
  <p style="flex:1 1 300px; margin:0;">Use this page to open an existing local repository, clone a remote repository, or initialize a new repository in GitKraken Desktop. You can also use shallow clone, sparse checkout, and the Repository Management tab to set up a new or existing project.</p>
  <img src="/wp-content/uploads/GitKraken_Keif_clone.png" alt="" width="788" height="786" loading="lazy" style="flex:0 0 auto; max-height:200px; width:auto; height:auto; max-width:100%; margin:0 auto; transform:scaleX(-1);">
</div>

**Requirements and limits**
- Entry points: Repository Management tab, New Tab, <kbd>File &gt; Clone Repo / Init Repo / Open Repo</kbd>, or the `gitkraken` command line
- Open workflow: Requires an existing local Git repository
- Clone workflow: Requires a remote repository URL or a connected integration
- Shallow clone: Supports branch, depth, since-date, and custom clone flags
- Sparse checkout: Root-level files are always checked out even when path rules are applied
- Initialize workflow: Creates a `.git` directory and can optionally add a `README.md`, `.gitignore`, and `LICENSE`
- Command line: You can open a repository by passing its path as an argument (for example, `gitkraken .` or `gitkraken /path/to/repo`) without the `--path` flag

***

## Quick Start


**To open an existing local repository:**
1. Click the folder icon in the top-left corner or press <kbd>Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + O</kbd> (Mac).
2. Click **Browse** and select your repository folder.

**To open a repository from the command line:**
Pass the repository path directly as an argument, for example `gitkraken .` to open the current directory or `gitkraken /path/to/repo` to open a specific path. You do not need the `--path` flag.

**To clone a remote repository:**
1. Open the Repository Management tab and click **Clone**.
2. Enter the repository URL or select a repository from your connected integration.
3. Click **Clone the repo!** to download it locally.

**To initialize a new repository:**
1. Click **Init** in the Repository Management tab.
2. Fill in the repository path and optional settings (`.gitignore`, license).
3. Click **Create Repository** to create the repo and open it.

To limit commit history by depth or date when you clone, enable **Shallow Clone** in the Clone dialog. You can open, clone, and initialize repositories from the Repository Management tab, the New Tab, or <kbd>File > Clone Repo / Init Repo / Open Repo</kbd>.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8uxrA56VJgY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***
## How to complete the initial setup
Complete these setup steps before managing repositories:

1. [Install GitKraken Desktop](/gitkraken-desktop/how-to-install)
2. Create an account and configure your [profile](/gitkraken-desktop/profiles). GitKraken Desktop opens your browser to sign up or sign in at gitkraken.dev. If you choose a provider such as GitHub during setup, gitkraken.dev opens with that provider selected.

***
## How Repository Management works

The **Repository Management** tab shows your active repositories, Workspaces, and favorites. Open this tab by clicking the folder icon in the top-left or using:
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

1. From Repository Management, select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Browse</span></button>.
2. Use the file explorer to locate your repo.

<figure>
  <img src='/wp-content/uploads/open-repo-2025@2x.png'  class="help-center-img img-bordered" alt="Repository Management screen with the Browse button highlighted to open an existing repository">
  <figcaption style="text-align:center; color:#888">Select an existing repository to open</figcaption>
</figure>

You can also browse for a repository from the <strong>New Tab</strong>, which you open with the + icon.

#### How to open a repository from the command line

You can open a repository in GitKraken Desktop by running the `gitkraken` command and passing the repository path directly as an argument:

```bash
# Open the current directory
gitkraken .

# Open a specific repository path
gitkraken /path/to/repo
```

The `--path` flag is not required.

#### How to open shallow-cloned repositories

GitKraken Desktop opens shallow-cloned repositories with no special setup. Open the shallow clone’s folder as you would any other repository.

***
### How to clone a project

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OA9o09Bq5M8?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

To clone a remote repo:

1. In Repository Management, select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Clone</span></button>.

<figure>
  <img src='/wp-content/uploads/clone-repo-mgmt-2025@2x.png' class="help-center-img img-bordered" alt="Repository Management tab with the Clone button highlighted in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Clone from Repository Management tab</figcaption>
</figure>

2. Enter the clone URL, or select a repository from a connected integration. You can also open the clone options from <kbd><strong>File > Clone Repo</strong></kbd> or the New Tab.

<figure>
  <img src='/wp-content/uploads/clone-url@2x.png' class="help-center-img img-bordered" alt="Clone a Repo dialog with URL input and provider options in GitKraken Desktop">
  <figcaption style="text-align:center; color:#888">Enter the clone URL to start</figcaption>
</figure>

#### How shallow clone works

GitKraken Desktop supports **shallow cloning** when cloning a repository. Shallow clones let you limit the commit history that is downloaded, which can reduce clone time and disk usage for large repositories.

To perform a shallow clone:

1. Open the **Clone** dialog from **Repository Management**, the **New Tab**, or <kbd><strong>File > Clone Repo</strong></kbd>.
2. Select the repository you want to clone.
3. Enable the **Shallow Clone** option.

<figure>
  <img src="/wp-content/uploads/perform-shallow-clone@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop shallow clone options, including branch to clone, depth, since date, and custom flags">
  <figcaption style="text-align: center; color: #888">Shallow Clone option in the Clone dialog</figcaption>
</figure>

Selecting **Shallow Clone** shows these options:

- **Branch to clone**: Specify the branch to clone. By default, GitKraken Desktop uses the repository’s default branch.
- **Depth**: Set how many commits deep to clone from the selected branch.
- **Since date**: Limit the clone to commits newer than a specific date.
- **Custom flags**: Provide any additional flags you typically pass to the `git clone` command. Enter these exactly as you would in the command-line interface.

4. Click <button class='button button--success button--ui button--nolink'>Clone the repo!</button> to complete the shallow clone.

After cloning, the repository opens automatically in GitKraken Desktop.

#### How sparse checkout works

Sparse checkout lets you check out only a subset of files from a repository, keeping your working directory smaller and improving performance on large repositories such as monorepos.

To perform a sparse checkout when cloning:

1. Open the **Clone** dialog from **Repository Management**, the **New Tab**, or <kbd><strong>File > Clone Repo</strong></kbd>.
2. Select the repository you want to clone.
3. Enable the **Sparse Checkout** option.
4. In the **Paths to include** field, enter one path per line (for example, `src/`, `docs/`, `README.md`). If you enter no paths, GitKraken Desktop checks out only root-level files.

<figure>
  <img src="/wp-content/uploads/sparse-checkout.png" class="help-center-img img-bordered" alt="GitKraken Desktop Clone dialog with Sparse Checkout enabled, showing a Blobless clone option and a Paths to include text field with example paths such as src/, docs/, and README.md">
  <figcaption style="text-align: center; color: #888">Enable Sparse Checkout in the Clone dialog and specify which paths to include.</figcaption>
</figure>

5. Click <button class='button button--success button--ui button--nolink'>Clone the repo!</button> to complete the clone.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Files at the root of the repository are always checked out regardless of the paths you specify.</p>
</div>

#### How to configure sparse checkout on an existing repository

To enable or update sparse checkout rules on a repository you have already opened, go to <kbd>Preferences > Sparse Checkout</kbd> for that repository.

<figure>
  <img src="/wp-content/uploads/sparse-checkout-preferences.png" class="help-center-img img-bordered" alt="GitKraken Desktop Repo-Specific Preferences panel open to the Sparse Checkout section, showing a Paths to include text field and three action buttons: Enable sparse checkout, Disable sparse checkout, and Reapply sparse checkout">
  <figcaption style="text-align: center; color: #888">Configure sparse checkout paths and actions under Repo-Specific Preferences.</figcaption>
</figure>

From this panel you can:
- **Enable sparse checkout**: Turns on sparse checkout with the paths you have entered.
- **Disable sparse checkout**: Turns off sparse checkout and restores the full working directory.
- **Reapply sparse checkout**: Reapplies the current path rules. Use it after you pull in new files or resolve inconsistencies.

When a repository has sparse checkout active, a **Sparse** button appears in the toolbar. Click it to edit your sparse checkout paths, disable sparse checkout, or reapply the current rules without opening Preferences.

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

3. Click <button class='button button--success button--ui button--nolink'>Create Repository</button>.

You can also initialize a repository from <kbd><strong>File > Init Repo</strong></kbd> or the New Tab.

After initialization:
- GitKraken Desktop creates a `.git` directory.
- The repository opens in GitKraken Desktop.
- The repository includes `README.md`, and optionally `.gitignore` and `LICENSE`.

<div class='callout callout--success'>
    <p>You can also initialize a repository directly to GitHub, Bitbucket, or other remote providers.</p>
</div>

***
### How to customize Repository Management

You can customize the Repository Management tab:
- Drag group headers to reorder them.
- To change a group's color, select <kbd>Change color</kbd> in the repo group menu.
- To set default colors, go to <kbd>Preferences > UI Customization</kbd>.

<figure>
  <img src='/wp-content/uploads/gkd-repo-mgm-tab-customize1.gif' class="help-center-img img-bordered" alt="User interacting with GitKraken Desktop Repository Management tab to change the color of a repo group via the group menu">
  <figcaption style="text-align:center; color:#888">Customize repo group layout and colors</figcaption>
</figure>
