 ---

title: Experimental Features
description: Learn about experimental features that are being worked on for possible future inclusion into GitKraken Desktop.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

Coming from the icy depths of the Git ocean are GitKraken Desktop experimental features! These are ideas we are trying out that are still being worked on, but we want to share with the world sooner 🧪

---

## Experimental Features

Navigate to <i class="fas fa-cog"></i><kbd><strong>Preferences</strong> <i class='fa fa-caret-right'></i> <strong>Experimental</strong></i></kbd> to access the experimental features menu.

Experimental features are still under development - treat these as an early sneak peek at some of the new functionality we're working on at GitKraken. Experimental features may not work as intended and could be changed or removed in the future. These settings are entirely optional and can be turned off at any time.

If you do experience issues, or have any other feedback, please reach out to us [Contact Support](https://help.gitkraken.com/gitkraken-desktop/contact-support/?issue_category__customer_facing_field_=Experimental+feedback&subject=GitKraken+Client+Experimental+feedback).

---

### Git Executable

When this setting is enabled, GitKraken Desktop will utilize the Git Executable instead of the NodeGit library for certain Git actions including fetching and committing. This may provide increased performance and compatibility with certain projects and development environments. This is a partial implementation and will only affect some aspects of Git within GitKraken Desktop - the amount of Git commands using the Git executable will increase with each release.

**Use Git Executable:** <i class="fa-regular fa-square-check"></i> turn on this experimental feature! Check the box to immediately apply the setting.

**Git Executable:** We automatically include Git with GitKraken Desktop. You can select other from other versions that are installed on your system. 

##### Features using the Git Executable

Find below a list of features using the Git binary if the Git Executable experimental setting is enabled. Anything not listed is still using LibGit2/NodeGit paths.

**Added in 9.4.0:**
- refresh commits (some of the commit info displayed in the graph)
- verify commit gpg signature
- commit
- fetch
- branch ahead/behind count (e.g. from pull request panel)
- merge base calculation (e.g. from right clicking a local branch in the Left Panel)
- branch rename
- branch delete (local branch only)

**Added in 9.5.0:**
- remote branch delete
- tag delete (local and remote)

**Added in 9.6.0:**
- support for SSH commit signing (configured from your gitconfig)
    - actions that do not currently use the Git Executable (like rebasing) will still use GPG for signing
- support for SSH strict host key checking

**Added in 9.6.1:**
- push
- support for streaming Git hooks output

**Added in 9.7.0:**
- Signing tags with SSH

**Added in 9.9.0:**
- Added revert commit support
- Added pageant ssh agent support

**Added in 9.10.0:**
- Added Pull (fast-forward if possible) and Pull (fast-forward only) support
- Added cherry-pick support

**Added in 9.11.0:**
- Added merge support
- Add pull support when the selected branch is not active
- Added new log level `GIT_SILLY` to get extra info about `git` and `ssh` commands in logs

**Added in 9.12.0:**
- Added clone support

**Added in 9.13.0:**
- Added rebase support
- Added pull (rebase) support
- Added checkout suppport
- LFS improvements by calling git-lfs directly

**Added in 10.0:**
- Added stage files support
- Added unstage files support
- Added stash support
- Added support for Git Credential Manager on SSH settings

**Added in 10.0.2:**
- Added push tag support

**Added in 10.2.0:**
- Added git status support

**Added in 10.4.1:**
- Added support for amending and rewording the latest (HEAD) commit, providing full support for SSH commit signing

**Added in 10.7.0:**
- Added support for 'Discard all changes' and connected Undo/Redo actions
- Added partial support for 'Discard changes' of unstaged files
- Interactive rebase now replays all rebased commits instead of fast-forwarding over the unchanged ones

**Added in 10.8.0:**
- Allow commit hooks when amending the latest commit message in the current branch
- Added partial support for 'Discard changes' of unstaged files (renames)
- Added partial support for 'Unstage and delete file' (new file)
- Support squashing latest commits in the current branch

---

### Cloud Patches

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/kKZKoKVQYKY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

#### What are Cloud Patches and why would you want to use them

A Cloud Patch is a Git patch that GitKraken securely stores for you so it can be easily shared with others across GitKraken Desktop, GitLens, and the GitKraken CLI. The patch is directly transferred from your machine into secure storage. 

Cloud Patches allow the ability to engage early with your team before a pull request. They can be created as soon as you have a work in progress. This can help with collaborating on changes prior to a pull request and minimize the delay of pull request reviews. 

#### How to setup Cloud Patches

`Preferences > Experimental > Use Git Executable` must be checked in order to work with Cloud Patches. This is enabled by default.

#### How to work with Cloud Patches

To create a Cloud Patch, stage the changes you want to include in the Cloud Patch and click on the Cloud Patch icon. You can also create a Cloud Patch from a commit by right-clicking on a commit in the Commit Graph and selecting `Share commit as Cloud Patch`. 

<img src='/wp-content/uploads/create-cloud-patch-2025.png' class="help-center-img img-bordered">

Once created, you can select `Copy Cloud Patch link` from the toast or by right-clicking a Cloud Patch in the Left Panel where all your Cloud Patches will be listed.

When creating a Cloud Patch, you have the following sharing options:

- `Anyone with the link`: Anyone that has access to the public link will be able to work with the Cloud Patch.

- `Anyone in my org`: Anyone in the GitKraken Organization will be able to work with the Cloud Patch. They will be required to authenticate with a GitKraken account to access it.

- `Only collaborators`: Only users in the GitKraken Organization who have been selected when sharing will be able to work with the Cloud Patch. They will be required to authenticate with a GitKraken account to access it.

Cloud Patches shared with you can be viewed in the Cloud Patches Left Panel section under `Shared with Me`.


Cloud Patch links can be shared with users to open the Cloud Patch in GitKraken Desktop or GitLens. When a Cloud Patch link is opened, the user will be prompted to open the client, clone or open the repository if not known to GitKraken Desktop, and then select the base branch to apply the patch to. From here, they can simply select `apply patch to <branch>`. 

<img src='/wp-content/uploads/gkc-apply-cloud-patch-example.gif' class="help-center-img img-bordered">

To delete a cloud path, right-click it and select `Delete Cloud Patch`.

<img src="/wp-content/uploads/gkc-delete-cloud-patch.png" class="help-center-img img-bordered">

#### Self-Hosting Cloud Patches

If you do not want your Cloud Patch data stored on GitKraken Servers, we offer the ability for you to host Cloud Patches on your own AWS S3 storage instance. For more information on configuring this, see our [security documentation](/gk-dev/gk-dev-security-controls/#self-hosted).
