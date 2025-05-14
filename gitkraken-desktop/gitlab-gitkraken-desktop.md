---

title: GitKraken Desktop & GitLab Integration
description: Integrate GitKraken with your GitLab repository by following these steps.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

GitKraken allows you to connect to [GitLab](https://gitlab.com), which will help you find repos on GitLab when cloning.

**Benefits**

* Create repositories on GitLab account including .gitignore and license
* Automatically generate an SSH key pair and add it to GitLab
* Clone from GitLab repo list
* Identify GitLab repos with remote avatars on graph
* Add remotes for GitLab repos
* Create and view Pull Requests
* Work with [GitLab Issues](/integrations/gitlab-issues/)

<div class='callout callout--warning'>
    <p>Note: The <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">GitKraken Community plan</a> only supports public repositories.</p>
</div>

***

## Connecting the GitLab integration

To authenticate with GitLab, navigate to the upper right corner to access <kbd><i> <i class="fas fa-cog"></i> Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>

<img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">

Or alternatively if you are in the <kbd>New Tab</kbd> view, click on <kbd>GitLab</kbd> under <strong>Integrations</strong>.

<img src="/wp-content/uploads/see-all-integrations-2025.png" srcset="/wp-content/uploads/see-all-integrations-2025@2x.png" class="help-center-img img-bordered">

From the Integrations window, select _GitLab.com_ and then hit the <button class='button button--success button--ui button--nolink'>Connect to GitLab</button> button.

<img src="/wp-content/uploads/connect-gitlab-2025.png" srcset="/wp-content/uploads/connect-gitlab-2025@2x.png 2x" class="help-center-img img-bordered">

This will open your default web browser where you can log in with your GitLab credentials.

<img src="/wp-content/uploads/gitlab-sign-in-2025.png" srcset="/wp-content/uploads/gitlab-sign-in-2025@2x.png 2x" class="help-center-img img-bordered">

Upon login, a success message appears. Finish connecting by selecting `Open GitKraken`. 

<img src="/wp-content/uploads/auth-success-gitlab-1.png" srcset="/wp-content/uploads/auth-success-gitlab-1@2x.png 2x" class="help-center-img img-bordered">

Alternativley, you can connect the integration by copy and pasting the OAuth token manually. 
 
<img src="/wp-content/uploads/gitlab-oauth-token.png" class="help-center-img img-bordered"> 

### Generating an SSH Key for GitLab
<div class='callout callout'>
    <p>Note 📝 - GitKraken uses your SSH key defined in <kbd><i>Preferences  <i class='fa fa-caret-right'></i>  SSH</i></kbd> for git operations unless you set up a GitLab-specific SSH key, or enable your local SSH Agent.</p>
</div>

Once your GitLab account has been connected to GitKraken, you may easily generate an SSH key and add it to your GitLab account from <kbd><i>Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>.

Click the magic <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitLab</button> button and watch what used to be 8 steps be complete in one.

Alternatively add a key from  _SSH Defaults_ with <button class='button button--uiorange button--ui button--nolink'>Add key to GitLab</button> or an existing key pair through _Add existing SSH key_.

<img src="/wp-content/uploads/add-key-to-gitlab-2025.png" srcset="/wp-content/uploads/add-key-to-gitlab-2025@2x.png 2x" class="help-center-img img-bordered">

***
## OAuth integration with GitLab
GitKraken's integration with GitLab provides handy information about your repositories.

First, you may search through your existing repositories when cloning:

<img src="/wp-content/uploads/clone-gitlab.png" srcset="/wp-content/uploads/clone-gitlab@2x.png" class="help-center-img img-bordered">

Next, GitKraken presents a list of forks of the current repository when adding remotes:

<img src="/wp-content/uploads/remote-gitlab.png" srcset="/wp-content/uploads/remote-gitlab@2x.png" class="help-center-img img-bordered">

Of course, you still have the option of manually entering repo URLs.

***

## Connecting to multiple GitLab accounts

GitKraken connects to one GitLab account at a time. However, with GitKraken Pro's multiple <a href="/start-here/profiles">profile</a> support, you can easily switch between profiles that each have their own associated GitLab accounts.
