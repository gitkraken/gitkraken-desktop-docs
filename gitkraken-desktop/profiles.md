---
title: Profiles
description: Create multiple profiles in GitKraken Desktop to quickly switch between repository preferences. Manage different gitconfig settings, repositories, and more!
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZgYjeaJDbX8?rel=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
</div>

***

GitKraken Desktop uses profiles to manage app preferences, [Tabs](/start-here/interface/#tabs), and Git config settings. You can create and switch between profiles for different projects and environments.

<figure>
  <img src="/wp-content/uploads/profiles@2x.png" class="help-center-img img-bordered" alt="Profile settings showing avatar preview">
  <figcaption style="text-align:center; color:#888">Set your email address to view your Gravatar preview.</figcaption>
</figure>

<div class='callout callout--success'>
    <p>Create and switch between multiple profiles with a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.</p>
</div>

***

## Manage Profiles

<figure>
  <img src="/wp-content/uploads/profiles-preferences@2x.png" class="help-center-img img-bordered" alt="Profiles tab in Preferences">
  <figcaption style="text-align:center; color:#888">Access profiles from <kbd>Preferences > Profiles</kbd>.</figcaption>
</figure>

Enable <em>Keep my .gitconfig updated with my profile info</em> to sync your name and email with Git’s global `.gitconfig`.

### What Does a Profile Store?

Each profile retains settings under:
- <kbd>Preferences > General</kbd>
- <kbd>Preferences > Integrations</kbd>
- <kbd>Preferences > UI Preferences</kbd>

[Tabs](/start-here/interface/#tabs) are also profile-specific. When you create a new profile, GitKraken Desktop will duplicate the tabs open in your current one.

<figure>
  <img src='/wp-content/uploads/profile-tabs-2025.gif' class="help-center-img img-bordered" alt="Switching profiles changes tabs">
  <figcaption style="text-align:center; color:#888">Each profile maintains its own set of tabs.</figcaption>
</figure>

Profiles support unique integration connections. For example, use separate profiles to connect different GitHub accounts.

<figure>
  <img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered" alt="Different profiles connected to different integrations">
  <figcaption style="text-align:center; color:#888">Profiles can connect to different remote hosting accounts.</figcaption>
</figure>

### Change Profile Avatars

If connected to [GitHub](/gitkraken-desktop/github-gitkraken-desktop/), your avatar will match your GitHub profile. Otherwise, GitKraken Desktop uses the [Gravatar](https://gravatar.com) linked to your profile’s email address.

To change your profile avatar:
1. Click the profile icon in the top-right corner.
2. Select <kbd>Manage Profiles <i class='fa fa-caret-right'></i> <i class="fa fa-ellipsis-v" aria-hidden="true"></i></kbd>

<figure>
  <img src="/wp-content/uploads/edit-profile-1-2025.png" class="help-center-img img-bordered" alt="Manage Profiles menu option">
  <figcaption style="text-align:center; color:#888">Start from the profile image menu.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/edit-profile-2-2025.png" class="help-center-img img-bordered" alt="Edit profile details">
  <figcaption style="text-align:center; color:#888">Edit your profile details here.</figcaption>
</figure>

Choose an icon or change the email address to use a different Gravatar image.

<figure>
  <img src="/wp-content/uploads/gravatar-2025.png" class="help-center-img img-bordered" alt="Gravatar image preview in profile settings">
  <figcaption style="text-align:center; color:#888">Set a different author email to change the profile Gravatar.</figcaption>
</figure>

### Author Initials in the Graph

Instead of avatars, display commit author initials in the commit graph:

<figure>
  <img src="/wp-content/uploads/author-initials-2025.png" class="help-center-img img-bordered" alt="Commit graph showing author initials">
  <figcaption style="text-align:center; color:#888">Display author initials instead of profile avatars.</figcaption>
</figure>

To enable, go to <kbd><strong>Preferences > UI Preferences > Display author initials and generic remote icons instead of avatars</strong></kbd>.

#### Which Initials Are Used?

GitKraken Desktop uses initials based on the commit’s author name:
- Commits made in GitKraken use profile name initials.
- Commits from the CLI use initials from `.git/config` or `.gitconfig`.

### Can Profiles Use Different Avatars?

Yes—if each profile has a unique email address linked to a different Gravatar. GitKraken currently does not support custom image uploads.
