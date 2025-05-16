---

title: Profiles
description: Create multiple profiles in GitKraken Desktop to quickly switch between repository preferences. Manage different gitconfig settings, repositories, and more!
taxonomy:
    category: gitkraken-desktop

---

<kbd>Last updated: May 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZgYjeaJDbX8?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

GitKraken Desktop uses profiles to store your app preferences, current [Tabs](/start-here/interface/#tabs), and Git config information.

<figure class='figure center'>
    <img src="/wp-content/uploads/profiles@2x.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Set your email address to call the Gravatar image preview.</figcaption>
</figure>

<div class='callout callout--success'>
    <p>Create and quickly switch between additional profiles for your different projects and work environments. Note, access to multiple profiles requires a <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken subscription</a>.</p>
</div>

***
## Profiles

<figure class='figure center'>
    <img src="/wp-content/uploads/profiles-preferences@2x.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Navigate to Preferences > Profiles to access this .gitconfig setting.</figcaption>
</figure>

The _Keep my .gitconfig updated with my profile info_ option updates your global `.gitconfig` file with the name and email address of your current profile.


### What's saved in each profile?

The _General_, _Integrations_, and _UI Preferences_ settings configured under your <kbd>Preferences</kbd> are profile-specific.  

[Tabs](/start-here/interface/#tabs) are unique to each profile. When creating a new profile, GitKraken Desktop will use the same tabs that are open in your current profile.

<figure class='figure center'>
    <img src='/wp-content/uploads/profile-tabs-2025.gif' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Note how the tabs change when switching to a different profile.</figcaption>
</figure>

Integrations are unique to each profile. If you need to connect to a second remote hosting account, create a second profile and connect the other account from the <kbd>Integrations</kbd> tab. You can do this for any of the integrations.

<figure class='figure center'>
    <img src="/wp-content/uploads/profile-example-2025.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Each profile can save a unique integration connection.</figcaption>
</figure>

### Changing Avatars
If you are connected to the [GitHub integration](/gitkraken-desktop/github-gitkraken-desktop/), your commit avatar will be the same as your GitHub profile avatar. Please note that even with the GitHub integration, your GitKraken profile image will still default to Gravatar. Support for additional integrations is planned for the future.

For all other cases, your commit avatar is either a generated identicon, or the active [Gravatar](https://gravatar.com) image linked to your <code>.gitconfig</code> email address. If you change your Gravatar, your GitKraken Desktop avatar will update itself.

To change the image, click the profile icon in the top right corner then <kbd>Manage Profiles <i class='fa fa-caret-right'></i> <i class="fa fa-ellipsis-v" aria-hidden="true"></i></kbd>.

<figure class='figure center'>
    <img src="/wp-content/uploads/edit-profile-1-2025.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">First click on your profile image in the upper right.</figcaption>
</figure>

<figure class='figure center'>
    <img src="/wp-content/uploads/edit-profile-2-2025.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Then click to edit the profile.</figcaption>
</figure>



You can choose from the list of icons available on the left then click <button class='button button--success button--ui button--nolink'>Save changes</span></button>. Alternatively, you can set a different email address for this profile if the email address has a different Gravatar image associated to it.

<figure class='figure center'>
    <img src="/wp-content/uploads/gravatar-2025.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Set the author email address to preview the Gravatar image.</figcaption>
</figure>

### Author initials in graph

GitKraken Desktop lets you replace all commit nodes with the commit author's initials. 

<figure class='figure center'>
    <img src="/wp-content/uploads/author-initials-2025.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Set commits to display author initials instead of profile avatars.</figcaption>
</figure>

Navigate to <kbd><strong>Preferences > UI Preferences > Display author initials and generic remote icons instead of avatars</strong></kbd> to enable the setting.

#### What initials does GitKraken Desktop use?

If you have enabled this UI setting, GitKraken Desktop will reference the original name associated with the commit.

If a commit was made in GitKraken Desktop, the app will list initials from the GitKraken user profile. If a commit was made in the CLI, the app will list initials from the user's `.git/config` or global `.gitconfig`.

### Do profiles allow different identity pictures?</p>

As long you have different email addresses with the profiles associated with Gravatar images, then yes! Otherwise, GitKraken Desktop does not currently allow selection of custom images.

