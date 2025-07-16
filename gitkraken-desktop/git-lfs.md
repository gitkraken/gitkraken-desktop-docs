---
title: Using Git LFS in GitKraken Desktop
description: Learn how to manage large files with Git LFS in GitKraken Desktop. Covers installation, initialization, configuration, and common troubleshooting.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: June 2025</kbd>

## What is Git LFS?

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/S03EEusFxoI?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

Git Large File Storage (Git LFS) is a Git extension that helps you manage large binary files. Git LFS stores the actual binary content separately, while Git tracks metadata about these files.

> 💡 Fun fact: Git LFS jokingly stands for "Legendary Fabled Squid" in the GitKraken universe.

### How it works

- Git LFS tracks specific files or file types based on defined patterns.
- When viewing diffs for LFS-tracked files, you’ll see metadata: a URL, a SHA hash, and file size.
- The actual binary content is stored in `.git/lfs/objects` or hosted on GitHub, GitLab, Bitbucket, or a custom server.
- Git LFS uses Git hooks and filters to manage file commits and retrieval.

<img src='/wp-content/uploads/lfs-ref-2025.png' srcset='/wp-content/uploads/lfs-ref-2025@2x.png 2x' class="help-center-img img-bordered" alt="LFS file metadata in GitKraken Desktop" />

To learn more, visit the [Git LFS documentation](https://github.com/git-lfs/git-lfs).

***

## Git LFS Requirements

Make sure the following are installed:

- Git version `2.39.3+`
- Git LFS version `3.0.0+`
- GitKraken Desktop version `7.0.0+`

<div class='callout callout--success'>
    <p><strong>Note:</strong> GitKraken Desktop usually does not require <a href="https://git-scm.com/">Git</a>. However, to use Git LFS, Git must be installed.</p>
</div>

### Verify Installation

Run these commands in a terminal or CMD:

```bash
git --version
git lfs version
```

You should see output like:

```bash
git version 2.39.3
git-lfs/3.0.0 (GitHub; windows 386; go 1.8.1; git bd2c9987)
```

To verify paths:

- macOS/Linux:
  ```bash
  which git
  which git-lfs
  ```
- Windows:
  ```cmd
  where git
  where git-lfs
  ```

If versions are missing or outdated, visit:

- [git-scm.com](https://git-scm.com/)
- [git-lfs.github.com](https://git-lfs.github.com/)

### Updating PATH on Windows

1. Search `Env` in the Start Menu.
2. Open <kbd>Environmental Variables</kbd>.
3. Edit the **Path** variable.
4. Click `New` to add paths to Git and Git LFS.

<img src="/wp-content/uploads/lfs-AddPathVariable-0.png" class="help-center-img img-bordered" alt="Windows environment variable dialog">

<img src="/wp-content/uploads/lfs-add-env-variable-image1-2025.png" srcset="/wp-content/uploads/lfs-add-env-variable-image1-2025@2x.png 2x" class="help-center-img img-bordered" alt="Add Path Environment Variable Step 1">

<img src="/wp-content/uploads/lfs-add-env-variable-image2-2025.png" srcset="/wp-content/uploads/lfs-add-env-variable-image2-2025@2x.png 2x" class="help-center-img img-bordered" alt="Add Path Environment Variable Step 2">

<img src="/wp-content/uploads/lfs-add-env-variable-image3-2025.png" srcset="/wp-content/uploads/lfs-add-env-variable-image3-2025@2x.png 2x" class="help-center-img img-bordered" alt="Add Path Environment Variable Step 3">

***

## Initializing Git LFS

### On an Existing Repository

1. Open the repo in GitKraken Desktop.
2. Go to <kbd>Preferences > LFS</kbd> and click **Initialize LFS**.

<img src='/wp-content/uploads/lfs-preferences-2025.png' srcset='/wp-content/uploads/lfs-preferences-2025@2x.png 2x' class="help-center-img img-bordered" alt="LFS tab in Preferences">  

3. Commit the change to the `.gitattributes` file.
4. Untrack and re-add existing files to apply the LFS tracking.

<img src='/wp-content/uploads/lfs-gitattributes-2025.png' srcset='/wp-content/uploads/lfs-gitattributes-2025@2x.png 2x' class="help-center-img img-bordered" alt="Modified .gitattributes file">  

### On a New Repository

You can initialize Git LFS during repository creation by selecting _Initialize with LFS_.

<img src='/wp-content/uploads/init-with-lfs-2025.png' srcset='/wp-content/uploads/init-with-lfs-2025@2x.png 2x' class="help-center-img img-bordered" alt="New repo dialog with LFS checkbox">  

***

## Configuring Git LFS

Add file tracking patterns to the `.gitattributes` file. You can do this via:

- <kbd>Preferences > LFS</kbd>
- Unstage pane in the Commit Panel
- Directly editing `.gitattributes`

<img src='/wp-content/uploads/lfs-tracking-patterns-2025.png' srcset='/wp-content/uploads/lfs-tracking-patterns-2025@2x.png 2x' class="help-center-img img-bordered" alt="Tracking pattern dialog">  

To track a file:

1. Right-click it under WIP.
2. Select **LFS > Track file pattern**.

<img src='/wp-content/uploads/add-tracked-file-lfs-2025.png' srcset='/wp-content/uploads/add-tracked-file-lfs-2025@2x.png 2x' class="help-center-img img-bordered" alt="LFS file tracking menu">  

<div class='callout callout--success'>
    <p><strong>Note:</strong> GitKraken Desktop runs an LFS pull automatically after clone or submodule init.</p>
</div>

Files tracked by LFS will show an LFS tag in the Commit Panel:

<img src='/wp-content/uploads/lfs-tags-2025.png' srcset='/wp-content/uploads/lfs-tags-2025@2x.png 2x' class="help-center-img img-bordered" alt="LFS tag in commit panel">

Clicking on the file shows the LFS reference information:

<img src='/wp-content/uploads/lfs-ref-2025.png' srcset='/wp-content/uploads/lfs-ref-2025@2x.png 2x' class="help-center-img img-bordered" alt="LFS reference information">

Use the LFS menu in the toolbar to run commands:

<img src='/wp-content/uploads/lfs-actions-2025.png' srcset='/wp-content/uploads/lfs-actions-2025@2x.png 2x' class="help-center-img img-bordered" alt="LFS toolbar menu">  

> ⚠️ Prune is destructive. Use with caution. See the [Git LFS prune docs](https://github.com/git-lfs/git-lfs/blob/main/docs/man/git-lfs-prune.adoc).

***

## FAQs and Troubleshooting

### LFS not showing in Preferences?
Check if your PATH includes Git and Git LFS. See [Verify Installation](#verify-installation).

### LFS button disappeared?
You may have switched to a repo without LFS. Use the menu: <kbd>Hamburger > LFS > Initialize</kbd>.

### Tracking pattern not working?
Only new files match new patterns. Remove and re-add existing files.

### LFS prompts for credentials?
Enter credentials for your LFS server or Git host.

### SSH issues with LFS?
SSH must be configured in both GitKraken and your CLI. [GitHub SSH Agent guide](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

### Homebrew on macOS not in path?
Run:
```bash
sudo launchctl config user path "/opt/homebrew/bin:$PATH"
```
More at [Homebrew FAQ](https://docs.brew.sh/FAQ#my-mac-apps-dont-find-usrlocalbin-utilities).

---

## Summary

To use Git LFS in GitKraken Desktop:

1. Install Git, Git LFS, and GitKraken Desktop.
2. Initialize LFS via Preferences or during repo creation.
3. Add file tracking patterns.
4. Commit and push as usual.

Need more? Visit the [Git LFS GitHub](https://github.com/git-lfs/git-lfs).
