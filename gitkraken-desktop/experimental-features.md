---
title: GitKraken Desktop Experimental Features | Cloud Patches
description: Find GitKraken Desktop's experimental features and use Cloud Patches, including how to create, share, apply, and self-host them.
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
tags: [experimental, cloud-patch, preview, features]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-start-here"
    nav_label: "Experimental Features"
    nav_order: 110
    nav_parent: "desktop-start-here"
    page_type: "content"
    card_icon: "flask"
    card_color: "purple"
    card_description: "Cloud Patches and other preview features"
---
<kbd>Last updated: November 2026</kbd>

Use this page to find GitKraken Desktop's experimental features and to create, share, and apply Cloud Patches. Experimental features are previews whose behavior can change between releases.

## Requirements and limits

- Scope: Preview features in GitKraken Desktop. Cloud Patches is the current experimental feature
- Settings location: <kbd>Preferences &gt; Experimental</kbd>. The self-hosted and standalone versions of GitKraken Desktop do not show this section
- Stability note: Experimental features can change between releases
- Git Executable: GitKraken Desktop runs every Git operation with a Git executable. To choose which one, see [General preferences](/gitkraken-desktop/preferences/#how-general-preferences-work)
- Cloud Patch sharing modes: **Anyone with the link**, **Members of my Org with the link**, or **Only collaborators**
- Self-hosting note: You can store Cloud Patch data on AWS S3 instead of GitKraken servers

***

## Quick Start


**To see the experimental features:**
- Go to <kbd>Preferences > Experimental</kbd>.

**To create a Cloud Patch:**
1. Stage files in the Commit Panel.
2. Click the Cloud Patch icon to create the patch.
3. Copy the generated link and share it with your team.

**To apply a Cloud Patch:**
1. Open the link in GitKraken Desktop, or find the patch in the Left Panel.
2. Select a target branch and apply the patch.

**To share a commit as a Cloud Patch:**
- Right-click any commit in the Commit Graph and select **Share commit as Cloud Patch**.

GitKraken stores Cloud Patches securely. You can share a patch with anyone who has the link, with members of your GitKraken organization, or with selected collaborators. To delete a patch, right-click it in the Left Panel and choose **Delete Cloud Patch**.

---

## How to access experimental features

To open the Experimental section:

- Go to <i class="fas fa-cog"></i> <kbd><strong>Preferences</strong> <i class='fa fa-caret-right'></i> Experimental</kbd>

The Experimental section describes each experimental feature. If you have issues or feedback, click **Provide Feedback on Experimental Features** there, or [contact support](https://help.gitkraken.com/gitkraken-desktop/contact-support/?issue_category__customer_facing_field_=Experimental+feedback&subject=GitKraken+Client+Experimental+feedback).

> **Note:** GitKraken Desktop runs every Git operation with a Git executable. To choose which one, go to <kbd>Preferences > General > Git Executable</kbd>.

---

## How Cloud Patches work

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/kKZKoKVQYKY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch how to create and apply Cloud Patches in GitKraken Desktop.</figcaption>
</figure>

### What Cloud Patches are

A Cloud Patch is a Git patch that GitKraken stores so you can share it across GitKraken Desktop, GitLens, and the GitKraken CLI. Use Cloud Patches to:
- Share work-in-progress with teammates before a pull request
- Apply changes across machines or collaborators securely

### How to create a Cloud Patch

1. Stage files in the Commit Panel.
2. Click the Cloud Patch icon.

<figure class='figure center'>
  <img src='/wp-content/uploads/create-cloud-patch-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop Commit Panel on the Cloud Patch tab, creating a Cloud Patch from main with one staged file, the Anyone with the link sharing option, and title and description fields.">
  <figcaption style="text-align: center; color: #888;">Create a Cloud Patch from staged changes.</figcaption>
</figure>

You can also right-click any commit in the Commit Graph and select <kbd>Share commit as Cloud Patch</kbd>.

### How to share and apply Cloud Patches

After you create a Cloud Patch, copy its link from the notification or the Left Panel. Choose who can open the patch:

- **Anyone with the link**
- **Members of my Org with the link** (requires a GitKraken login)
- **Only collaborators** (requires a GitKraken login)

Recipients can open the patch and apply it to a selected branch.

<figure class='figure center'>
  <img src='/wp-content/uploads/gkc-apply-cloud-patch-example.gif' class="help-center-img img-bordered" alt="Opening a shared Cloud Patch link in a browser, choosing GitKraken Client, and clicking Apply patch to main in GitKraken Desktop, then committing the patch to main.">
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
