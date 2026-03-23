---
title: GitKraken Desktop Profiles | Manage Git Configs & Accounts
description: Learn how to use GitKraken Desktop profiles to manage Git settings, integrations, avatars, and multiple accounts across different projects. Manage different gitconfig settings, repositories, and more!
product: GitKraken Desktop
feature: Profiles
content_type: reference
audience: developer
plan_required: Pro
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitHub Enterprise Server, GitLab, GitLab Self-Managed, Bitbucket, Azure DevOps]
integrations: [GitHub, GitHub Enterprise Server, GitLab, GitLab Self-Managed, Bitbucket, Azure DevOps]
hosted_variant: both
status: GA
last_verified: 2026-03
llms_include: true
tags: [profiles, accounts, gitconfig, avatars, integrations]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZgYjeaJDbX8?rel=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
</div>

***

Use profiles in GitKraken Desktop to keep separate Git identities, integrations, app preferences, and tab sets for different projects or environments. This page explains how to create and switch profiles, what a profile stores, how avatar behavior works, and when a paid GitKraken subscription is required for multiple profiles.

**Requirements and limits**
- Purpose: Separate Git identities, integrations, preferences, and tab sets by work context
- Multiple profiles: Require a paid GitKraken subscription
- Profile data: General, Integrations, and UI Preferences are stored per profile
- Tab behavior: Open tabs are profile-specific; new profiles duplicate tabs from the active profile when created
- Git config option: You can sync profile name and email into the global `.gitconfig`
- Avatar behavior: Connected integrations use provider avatars; otherwise GitKraken Desktop uses the Gravatar tied to the profile email

***

## Quick Start


**To create a profile:**
1. Click the profile icon in the top-right corner.
2. Select **Manage Profiles**, then click the option to add a new profile.
3. Enter a profile name, author name, and email address.

**To switch profiles:**
- Click the profile icon and select the profile you want to use.

**What each profile stores:**
- Preferences from General, Integrations, and UI Preferences
- Open tabs (duplicated from the active profile when a new profile is created)
- Integration connections (for example, connect one profile to a personal GitHub account and another to a work account)

**To sync your profile email with Git's global config:** Enable the option "Keep my .gitconfig updated with my profile info" in <kbd>Preferences > Profiles</kbd>.

Multiple profiles require a paid GitKraken subscription. Profiles are accessible from <kbd>Preferences > Profiles</kbd>.

<figure>
  <img src="/wp-content/uploads/profiles@2x.png" class="help-center-img img-bordered" alt="Add Profile dialog in GitKraken showing selected avatar, profile name, author name, and email fields." />
  <figcaption style="text-align:center; color:#888">Set your email address to view your Gravatar preview.</figcaption>
</figure>

<div class='callout callout--success'>
    <p>Create and switch between multiple profiles with a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.</p>
</div>

***

## How to manage profiles

<div class='callout callout--basic'>
  <p><strong>Use profiles when:</strong> you need clean separation between work and personal Git identities, integrations, and tabs. <strong>Don't use multiple profiles when:</strong> one identity and one integration set already cover your workflow.</p>
</div>

<figure>
  <img src="/wp-content/uploads/profiles-preferences@2x.png" class="help-center-img img-bordered" alt="GitKraken Preferences showing Profiles tab with profile details including name, author info, and organization." />
  <figcaption style="text-align:center; color:#888">Access profiles from <kbd>Preferences &gt; Profiles</kbd>.</figcaption>
</figure>

Enable <em>Keep my .gitconfig updated with my profile info</em> to sync your name and email with Git’s global `.gitconfig`.

### What a profile stores

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

<div class='callout callout--basic'>
  <p><strong>Use separate profiles when:</strong> you want integrations, UI settings, and open tabs isolated by context. <strong>Don't expect profiles to be lightweight if:</strong> constantly duplicating and switching tabs would slow down your workflow more than it helps.</p>
</div>

<figure>
  <img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered" alt="List of three GitKraken profiles showing author names and emails, with notes indicating connection to different GitHub accounts for work and personal use.">
  <figcaption style="text-align:center; color:#888">Profiles can connect to different remote hosting accounts.</figcaption>
</figure>

### How to change profile avatars

If connected to [GitHub](/gitkraken-desktop/github-gitkraken-desktop/), [GitHub Enterprise Server](/gitkraken-desktop/github-enterprise/),[GitLab](/gitkraken-desktop/gitlab-gitkraken-desktop/), [GitLab Self-Managed](/gitkraken-desktop/gitlab-self-hosted/), [Azure DevOps](/gitkraken-desktop/azure-devops/), or [Bitbucket](/gitkraken-desktop/bitbucket/) your avatar will match your GitHub profile. Otherwise, GitKraken Desktop uses the [Gravatar](https://gravatar.com) linked to your profile’s email address.

<div class='callout callout--basic'>
  <p><strong>Use provider avatars when:</strong> the profile is connected to a supported integration and you want that service's identity reflected in GitKraken Desktop. <strong>Use separate Gravatar-backed emails when:</strong> you need profiles to display different non-provider avatars.</p>
</div>

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

### How to show author initials in the graph

Instead of avatars, display commit author initials in the commit graph:

<figure>
  <img src="/wp-content/uploads/author-initials-2025.png" class="help-center-img img-bordered" alt="GitKraken commit graph view showing commits with author initials instead of profile pictures">
  <figcaption style="text-align:center; color:#888">Display author initials instead of profile avatars.</figcaption>
</figure>

To enable, go to <kbd><strong>Preferences > UI Preferences > Display author initials and generic remote icons instead of avatars</strong></kbd>.

#### Which initials GitKraken Desktop uses

GitKraken Desktop uses initials based on the commit’s author name:
- Commits made in GitKraken use profile name initials.
- Commits from the CLI use initials from `.git/config` or `.gitconfig`.

### Can profiles use different avatars?

Yes it can, if each profile has a unique email address linked to a different Gravatar. GitKraken currently does not support custom image uploads.
