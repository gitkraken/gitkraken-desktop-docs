---

title: Profiles
description: Create multiple profiles in GitKraken Desktop to quickly switch between repository preferences. Manage different gitconfig settings, repositories, and more!
taxonomy:
    category: gitkraken-desktop

---

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZgYjeaJDbX8?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***

GitKraken Desktop uses profiles to store your app preferences, current [Tabs](/start-here/interface/#tabs), and Git config information.


<img src="/wp-content/uploads/profiles@2x.png" class="help-center-img img-bordered">

<div class='callout callout--success'>
    <p>Create and quickly switch between additional profiles for your different projects and work environments. This requires <a href="https://www.gitkraken.com/pricing" target="_blank">GitKraken Pro</a> subscription or higher.</p>
</div>

***
## Profiles


<img src="/wp-content/uploads/profiles-preferences@2x.png" class="help-center-img img-bordered">

The _Keep my .gitconfig updated with my profile info_ option updates your global `.gitconfig` file with the name and email address of your current profile.


### What's saved in each profile?

The _General_, _Integrations_, and _UI Preferences_ settings configured under your <kbd>Preferences</kbd> are profile-specific.  

[Tabs](/start-here/interface/#tabs) are unique to each profile. When creating a new profile, GitKraken Desktop will use the same tabs that are open in your current profile.

<img src='/wp-content/uploads/profile-tabs-2025.gif' class="help-center-img img-bordered">

Integrations are unique to each profile. If you need to connect to a second remote hosting account, create a second profile and connect the other account from the <kbd>Integrations</kbd> tab. You can do this for any of the integrations.

<img src="/wp-content/uploads/profile-example@2x.png" class="help-center-img img-bordered">

### Changing Avatars
Your commit avatar is either a generated identicon, or the active [Gravatar](https://gravatar.com) image linked to your <code>.gitconfig</code> email address. If you change your Gravatar, your GitKraken Desktop avatar will update itself.

To change the image, click the profile icon in the top right corner then <kbd>Manage Profiles <i class='fa fa-caret-right'></i> <i class="fa fa-ellipsis-v" aria-hidden="true"></i></kbd>.

<img src="/wp-content/uploads/edit-profile@2x.png" class="help-center-img img-bordered">

<img src="/wp-content/uploads/edit-profile-2@2x.png" class="help-center-img img-bordered">

You can choose from the list of icons available on the left then click <button class='button button--success button--ui button--nolink'>Save changes</span></button>. Alternatively, you can set a different email address for this profile if the email address has a different Gravatar image associated to it.

<img src="/wp-content/uploads/gravatar.png" class="help-center-img img-bordered">

### Author initials in graph

GitKraken Desktop lets you replace all commit nodes with the commit author's initials. 

<img src="/wp-content/uploads/author-initials@2x.png" class="help-center-img img-bordered">

Navigate to <kbd><strong>Preferences > UI Preferences</strong></kbd> to enable the setting.

#### What initials does GitKraken Desktop use?

If you have enabled this UI setting, GitKraken Desktop will reference the original name associated with the commit.

If a commit was made in GitKraken Desktop, the app will list initials from the GitKraken user profile. If a commit was made in the CLI, the app will list initials from the user's `.git/config` or global `.gitconfig`.

### Do profiles allow different identity pictures?</p>

As long you have different email addresses with the profiles associated with Gravatar images, then yes! GitKraken Desktop at this time does not allow selection of custom images.

