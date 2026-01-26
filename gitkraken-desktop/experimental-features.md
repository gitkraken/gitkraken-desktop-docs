---
title: GitKraken Desktop Experimental Features | Cloud Patch & Git Executable
description: Explore experimental GitKraken Desktop features like Git Executable integration and Cloud Patches. Learn how to enable, use, and self-host these in-development tools.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

GitKraken Desktop includes experimental features, which are early previews of in-development functionality. These features may change or be removed in future releases.

---

## Access Experimental Features

To access experimental settings:

- Go to <i class="fas fa-cog"></i> <kbd><strong>Preferences</strong> <i class='fa fa-caret-right'></i> Experimental</kbd>

Experimental features are optional and can be enabled or disabled at any time. If you experience issues or have feedback, [contact support](https://help.gitkraken.com/gitkraken-desktop/contact-support/?issue_category__customer_facing_field_=Experimental+feedback&subject=GitKraken+Client+Experimental+feedback).

---

## Git Executable

This setting allows GitKraken Desktop to use your system’s Git executable instead of NodeGit for core Git operations. It can enhance compatibility and performance.

**Enable it from:** <kbd>Preferences > Experimental > Use Git Executable</kbd>

GitKraken ships with Git built-in, or you can select a system Git path.

### Features Using Git Executable

Git actions that currently use the Git executable (by version):

**v9.4.0–11.6.0:**
- Commit, fetch, push, pull
- Branch rename/delete, merge base
- Tag creation/deletion, revert commits
- Cherry-pick, rebase, checkout, clone
- Staging, unstaging, stash support
- SSH signing, Git Credential Manager
- Discard changes, undo/redo, hooks output
- Reset to commit (mixed, hard, soft)
- Undo checkout
- Submodules

See full details per release in the [GitKraken Desktop release notes](/gitkraken-desktop/current/).

---

## Cloud Patches

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/kKZKoKVQYKY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch how to create and apply Cloud Patches in GitKraken.</figcaption>
</figure>

### What Are Cloud Patches?

A Cloud Patch is a Git patch that GitKraken securely stores so you can share it across GitKraken Desktop, GitLens, and CLI. Use them to:
- Share work-in-progress with teammates before a pull request
- Apply changes across machines or collaborators securely

### How to Enable

Cloud Patches require the **Git Executable** to be enabled (it is by default).

### Create a Cloud Patch

1. Stage files in the Commit Panel.
2. Click the Cloud Patch icon.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-cloud-patch-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing the Cloud Patch creation panel, illustrating how users can package and share staged changes as a lightweight patch, enabling quick peer review or collaboration without needing to push to a remote.">
  <figcaption style="text-align: center; color: #888;">Create a Cloud Patch from staged changes.</figcaption>
</figure>

You can also right-click any commit in the graph and select <kbd>Share commit as Cloud Patch</kbd>.

### Share and Apply Cloud Patches

- Copy the link from the toast or Left Panel
- Options:
  - Anyone with the link
  - Anyone in my org (requires GitKraken login)
  - Only selected collaborators (requires login)

Recipients can open the patch and apply it to a selected branch.

<figure class='figure center'>
  <img src='/wp-content/uploads/gkc-apply-cloud-patch-example.gif' class="help-center-img img-bordered" alt="Applying a Cloud Patch in GitKraken Desktop, demonstrating how users can instantly review and merge shared patches without switching branches or pulling from a remote. This accelerates cross-branch collaboration and simplifies patch-based workflows.">
  <figcaption style="text-align: center; color: #888;">Apply Cloud Patch to a target branch in GitKraken Desktop.</figcaption>
</figure>

### Manage Cloud Patches

To delete a patch, right-click it in the Left Panel and choose <kbd>Delete Cloud Patch</kbd>.

<figure class='figure center'>
  <img src="/wp-content/uploads/gkc-delete-cloud-patch.png" class="help-center-img img-bordered" alt="GitKraken Desktop showing how users can manage Cloud Patches from the left panel, including the ability to open, copy, or delete patches, reinforcing that Cloud Patches are lightweight and user-controlled artifacts rather than permanent Git history.">
  <figcaption style="text-align: center; color: #888;">Manage Cloud Patches via context menu.</figcaption>
</figure>

### Self-Hosting Cloud Patches

You can self-host Cloud Patch data on an AWS S3 instance instead of GitKraken servers. See [Security Controls](/gk-dev/gk-dev-security-controls/#self-hosted) for setup instructions.
