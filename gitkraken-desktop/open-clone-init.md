---
title: Open, Clone, or Initialize a Git Repository in GitKraken Desktop
description: Learn how to open, clone, or initialize repositories in GitKraken Desktop. Get started with repository management and project setup.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2025</kbd>

Each user will need to open, clone, or initialize a repository in GitKraken Desktop. This guide explains how.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8uxrA56VJgY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***
## Setup
Complete these setup steps before managing repositories:

1. [Install GitKraken Desktop](/gitkraken-desktop/how-to-install)
2. Create an account and configure your [profile](/gitkraken-desktop/profiles)

***
## Repository Management

The **Repository Management** tab provides an overview of active repositories, Workspaces, and favorites. Open this tab by clicking the folder icon in the top-left or using:
- <kbd>Alt + O</kbd> (Windows/Linux)
- <kbd>Cmd + O</kbd> (Mac)

<figure>
  <img src='/wp-content/uploads/repo-mgmt-2025.png' srcset="/wp-content/uploads/repo-mgmt-2025@2x.png" class="help-center-img img-bordered">
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
### Open an Existing Project

To open an existing repo:

1. From Repository Management, select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Browse</span></button>
2. Use the file explorer to locate your repo

<figure>
  <img src='/wp-content/uploads/open-repo-2025.png' srcset="/wp-content/uploads/open-repo-2025@2x.png"  class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Select an existing repository to open</figcaption>
</figure>

You can also access this via the <strong>New Tab</strong> by clicking the + icon.

<figure>
  <img src='/wp-content/uploads/open-new-tab-2025.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">New tab view with Browse option</figcaption>
</figure>

#### Open Shallow Cloned Repos

GitKraken Desktop supports opening shallow cloned repositories.

No special setup is required. Just navigate to the shallow clone’s location and open it as you would any other repository (see above).

***
### Clone a Project

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OA9o09Bq5M8?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

To clone a remote repo:

1. In Repository Management, select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Clone</span></button>

<figure>
  <img src='/wp-content/uploads/clone-repo-mgmt-2025.png' srcset="/wp-content/uploads/clone-repo-mgmt-2025@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Clone from Repository Management tab</figcaption>
</figure>

2. You can also access clone options via <kbd><strong>File > Clone</strong></kbd> or the New Tab.

<figure>
  <img src='/wp-content/uploads/clone-url.png' srcset='/wp-content/uploads/clone-url@2x.png 2x' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Enter the clone URL to start</figcaption>
</figure>

#### Shallow Clone Repositories

You can create a shallow clone by enabling the <kbd>Shallow clone</kbd> option in the clone dialog. By default, this option fetches the latest 50 commits, but you can customize this number or choose to fetch from a specific date.

<figure>
  <img src='/wp-content/uploads/shallow-clone-2025.png' srcset="/wp-content/uploads/shallow-clone-2025@2x.png 2x" class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Shallow clone options in the clone dialog</figcaption>
</figure>

***
### Initialize a New Project

To start a new repo:

1. Select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Init</span></button> in Repository Management.

<figure>
  <img src='/wp-content/uploads/init-2025.png' srcset="/wp-content/uploads/init-2025@2x.png" class="help-center-img img-bordered">
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
### Customize Repository Management

- Drag and drop group headers to reorder
- Change colors via <kbd>Change color</kbd> in the repo group menu
- Set default colors in <kbd>Preferences > UI Customization</kbd>

<figure>
  <img src='/wp-content/uploads/gkd-repo-mgm-tab-customize1.gif' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Customize repo group layout and colors</figcaption>
</figure>
