---
title: GitKraken Desktop Profiles | Manage Git Configs & Accounts
description: Learn how to use GitKraken Desktop profiles to manage Git settings, integrations, avatars, and multiple accounts across different projects. Manage different gitconfig settings, repositories, and more!
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZgYjeaJDbX8?rel=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
</div>

***

GitKraken Desktop uses profiles to manage app preferences, [Tabs](/start-here/interface/#tabs), and Git config settings. You can create and switch between profiles for different projects and environments.

<figure>
  <img src="/wp-content/uploads/profiles@2x.png" class="help-center-img img-bordered" alt="Add Profile dialog in GitKraken showing selected avatar, profile name, author name, and email fields." />
  <figcaption style="text-align:center; color:#888">Set your email address to view your Gravatar preview.</figcaption>
</figure>

<div class='callout callout--success'>
    <p>Create and switch between multiple profiles with a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.</p>
</div>

***

## Manage Profiles

<figure>
  <img src="/wp-content/uploads/profiles-preferences@2x.png" class="help-center-img img-bordered" alt="GitKraken Preferences showing Profiles tab with profile details including name, author info, and organization." />
  <figcaption style="text-align:center; color:#888">Access profiles from <kbd>Preferences &gt; Profiles</kbd>.</figcaption>
</figure>

Enable <em>Keep my .gitconfig updated with my profile info</em> to sync your name and email with Git’s global `.gitconfig`.

### What Does a Profile Store?

Each profile retains settings under:
- <kbd>Preferences > General</kbd>
- <kbd>Preferences > Integrations</kbd>
- <kbd>Preferences > UI Preferences</kbd>

[Tabs](/start-here/interface/#tabs) are also profile-specific. When you create a new profile, GitKraken Desktop will duplicate the tabs open in your current one.

<figure>
  <img src='/wp-content/uploads/profile-tabs-2025.gif' class="help-center-img img-bordered" alt="User switching between GitKraken profiles, showing that each profile has its own independent set of tabs open." />
  <figcaption style="text-align:center; color:#888">Each profile maintains its own set of tabs.</figcaption>
</figure>

Profiles support unique integration connections. For example, use separate profiles to connect different GitHub accounts.

<figure>
  <img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered" alt="List of three GitKraken profiles showing author names and emails, with notes indicating connection to different GitHub accounts for work and personal use.">
  <figcaption style="text-align:center; color:#888">Profiles can connect to different remote hosting accounts.</figcaption>
</figure>

### Change Profile Avatars

If connected to [GitHub](/gitkraken-desktop/github-gitkraken-desktop/), [GitHub Enterprise Server](/gitkraken-desktop/github-enterprise/),[GitLab](/gitkraken-desktop/gitlab-gitkraken-desktop/), [GitLab Self-Managed](/gitkraken-desktop/gitlab-self-hosted/), [Azure DevOps](/gitkraken-desktop/azure-devops/), or [Bitbucket](/gitkraken-desktop/bitbucket/) your avatar will match your GitHub profile. Otherwise, GitKraken Desktop uses the [Gravatar](https://gravatar.com) linked to your profile’s email address.

To change your profile avatar:
1. Click the profile icon in the top-right corner.
2. Select <kbd>Manage Profiles <i class='fa fa-caret-right'></i> <i class="fa fa-ellipsis-v" aria-hidden="true"></i></kbd>

<figure>
  <img src="/wp-content/uploads/edit-profile-1-2025.png" class="help-center-img img-bordered" alt="Profile dropdown open in GitKraken with arrow pointing to 'Manage profiles' option.">
  <figcaption style="text-align:center; color:#888">Start from the profile image menu.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/edit-profile-2-2025.png" class="help-center-img img-bordered" alt="GitKraken Profiles Preferences with arrow pointing to 'Edit Profile' option for Default Profile.">
  <figcaption style="text-align:center; color:#888">Edit your profile details here.</figcaption>
</figure>

Choose an icon or change the email address to use a different Gravatar image.

<figure>
  <img src="/wp-content/uploads/gravatar-2025.png" class="help-center-img img-bordered" alt="GitKraken profile editing screen showing the selected gravatar image and highlighted author email used to display it.">
  <figcaption style="text-align:center; color:#888">Set a different author email to change the profile Gravatar.</figcaption>
</figure>

### Author Initials in the Graph

Instead of avatars, display commit author initials in the commit graph:

<figure>
  <img src="/wp-content/uploads/author-initials-2025.png" class="help-center-img img-bordered" alt="GitKraken commit graph view showing commits with author initials instead of profile pictures">
  <figcaption style="text-align:center; color:#888">Display author initials instead of profile avatars.</figcaption>
</figure>

To enable, go to <kbd><strong>Preferences > UI Preferences > Display author initials and generic remote icons instead of avatars</strong></kbd>.

#### Which Initials Are Used?

GitKraken Desktop uses initials based on the commit’s author name:
- Commits made in GitKraken use profile name initials.
- Commits from the CLI use initials from `.git/config` or `.gitconfig`.

### Can Profiles Use Different Avatars?

Yes it can, if each profile has a unique email address linked to a different Gravatar. GitKraken currently does not support custom image uploads.
