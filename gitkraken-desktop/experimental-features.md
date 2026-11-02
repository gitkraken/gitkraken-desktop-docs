---
title: GitKraken Desktop Experimental Features | Cloud Patch & Git Executable
description: Enable and use the experimental GitKraken Desktop features Git Executable and Cloud Patches, including how to share, apply, and self-host Cloud Patches.
product: GitKraken Desktop
feature: Experimental Features
content_type: overview
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: preview
last_verified: 2026-11
llms_include: true
tags: [experimental, cloud-patch, git-executable, preview, features]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to enable and evaluate the GitKraken Desktop experimental features Git Executable and Cloud Patches. Experimental features are optional previews: you can turn each one on or off, see what it does, and find the workflows that depend on it.

**Requirements and limits**
- Scope: Optional preview features in GitKraken Desktop
- Settings location: <kbd>Preferences &gt; Experimental</kbd>
- Stability note: You can enable or disable experimental features at any time. Their behavior can change between releases
- Git Executable scope: Uses a Git executable instead of NodeGit for supported operations
- Cloud Patch dependency: Cloud Patches require Git Executable to be enabled
- Cloud Patch sharing modes: **Anyone with the link**, **Members of my Org with the link**, or **Only collaborators**
- Self-hosting note: Cloud Patch data can be self-hosted on AWS S3 instead of GitKraken servers

***

## Quick Start


**To enable experimental features:**
- Go to <kbd>Preferences > Experimental</kbd> and toggle the features you want to use.

**To use the Git Executable:**
- Enable **Use Git Executable** under <kbd>Preferences > Experimental</kbd>. GitKraken Desktop then runs core operations with a Git executable instead of the built-in NodeGit library.

**To create a Cloud Patch:**
1. Stage files in the Commit Panel.
2. Click the Cloud Patch icon to create the patch.
3. Copy the generated link and share it with your team.

**To apply a Cloud Patch:**
1. Open the link in GitKraken Desktop, or find the patch in the Left Panel.
2. Select a target branch and apply the patch.

**To share a commit as a Cloud Patch:**
- Right-click any commit in the graph and select **Share commit as Cloud Patch**.

GitKraken stores Cloud Patches securely. You can share a patch with anyone who has the link, with members of your GitKraken organization, or with selected collaborators. To delete a patch, right-click it in the Left Panel and choose **Delete Cloud Patch**.

---

## How to access experimental features

To access experimental settings:

- Go to <i class="fas fa-cog"></i> <kbd><strong>Preferences</strong> <i class='fa fa-caret-right'></i> Experimental</kbd>

Experimental features are optional, and you can enable or disable them at any time. If you experience issues or have feedback, [contact support](https://help.gitkraken.com/gitkraken-desktop/contact-support/?issue_category__customer_facing_field_=Experimental+feedback&subject=GitKraken+Client+Experimental+feedback).

---

## How Git Executable works

The **Use Git Executable** setting makes GitKraken Desktop run core Git operations with a Git executable instead of NodeGit. It can improve compatibility and performance with some projects and development environments.

**Enable it from:** <kbd>Preferences > Experimental > Use Git Executable</kbd>

GitKraken Desktop includes a bundled Git, or you can select a system Git path in **Git Executable**.

### Which features use Git Executable

These Git actions use the Git executable when **Use Git Executable** is enabled:

- Commit, fetch, push, pull
- Branch rename/delete, merge base
- Tag creation/deletion, revert commits
- Cherry-pick, rebase, checkout, clone
- Shallow repositories and shallow clone settings
- Staging, unstaging, stash support
- SSH signing, Git Credential Manager
- Discard changes, undo/redo, hooks output
- Reset to commit (mixed, hard, soft)
- Undo checkout
- Submodules
- Squash merge setting in Commit preferences
- File history and blame
- Adding, removing, renaming, and editing remotes
- Creating and applying patches
- Opening files in your external diff and merge tools

See the changes in each release in the [GitKraken Desktop release notes](/gitkraken-desktop/current/).

---

## How Cloud Patches work

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/kKZKoKVQYKY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch how to create and apply Cloud Patches in GitKraken Desktop.</figcaption>
</figure>

### What Cloud Patches are

A Cloud Patch is a Git patch that GitKraken securely stores so you can share it across GitKraken Desktop, GitLens, and GitKraken CLI. Use Cloud Patches to:
- Share work-in-progress with teammates before a pull request
- Apply changes across machines or collaborators securely

### How to enable Cloud Patches

Cloud Patches require the **Git Executable** to be enabled (it is by default).

### How to create a Cloud Patch

1. Stage files in the Commit Panel.
2. Click the Cloud Patch icon.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-cloud-patch-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop Cloud Patch creation panel for sharing staged changes as a patch without pushing to a remote.">
  <figcaption style="text-align: center; color: #888;">Create a Cloud Patch from staged changes.</figcaption>
</figure>

You can also right-click any commit in the graph and select <kbd>Share commit as Cloud Patch</kbd>.

### How to share and apply Cloud Patches

After you create a Cloud Patch, copy its link from the notification or the Left Panel. Choose who can open the patch:

- **Anyone with the link**
- **Members of my Org with the link** (requires a GitKraken login)
- **Only collaborators** (requires a GitKraken login)

Recipients can open the patch and apply it to a selected branch.

<figure class='figure center'>
  <img src='/wp-content/uploads/gkc-apply-cloud-patch-example.gif' class="help-center-img img-bordered" alt="GitKraken Desktop opening a shared Cloud Patch and applying its changes without switching branches or pulling from a remote.">
  <figcaption style="text-align: center; color: #888;">Apply Cloud Patch to a target branch in GitKraken Desktop.</figcaption>
</figure>

### How to manage Cloud Patches

To delete a patch, right-click it in the Left Panel and choose <kbd>Delete Cloud Patch</kbd>.

<figure class='figure center'>
  <img src="/wp-content/uploads/gkc-delete-cloud-patch.png" class="help-center-img img-bordered" alt="GitKraken Desktop Left Panel with the context menu for a Cloud Patch, showing options to open, copy, or delete it.">
  <figcaption style="text-align: center; color: #888;">Manage Cloud Patches via context menu.</figcaption>
</figure>

### How to self-host Cloud Patches

You can self-host Cloud Patch data on an AWS S3 instance instead of GitKraken servers. See [Security Controls](/gk-dev/gk-dev-security-controls/#self-hosted) for setup instructions.
