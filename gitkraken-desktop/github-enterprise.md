---

title: GitKraken Desktop GitHub Enterprise Server Integration
description: Easily integrate GitKraken with you GitHub Enterprise Server repository. Learn how to link GitKraken and GitHub Enterprise Server by following these steps.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

GitKraken allows you to connect to GitHub Enterprise Server, which will help you find repos when cloning or adding your remotes.

<div class='callout callout--warning'>
    <p>Note: All Self-Hosted server integrations, including GitHub Enterprise, require an <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">Advanced subscription</a> tier or higher.</p>
</div>



**Benefits**

* Create repositories on GitHub Enterprise Server account including .gitignore and license
* Automatically generate an SSH key pair and add it to GitHub Enterprise Server
* [Fork repositories](/working-with-repositories/fork/) from GitKraken
* Save authentication into [profiles](/gitkraken-desktop/profiles/)
* Clone from GitHub Enterprise Server repo list
* Add remotes for GitHub Enterprise Server repos
* Create and view Pull Requests


***
## Connecting GitHub Enterprise Server

<div class='callout callout'>
    <p>Note 📝 - GitKraken supports any version of GitHub Enterprise Server released within one year.</p>
</div>

To authenticate with GitHub Enterprise Server, navigate to the upper right corner to access <kbd><i> <i class="fas fa-cog"></i> Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>

<img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">

Or alternatively if you are in the <kbd>New Tab</kbd> view, click on <kbd>See all the integrations</kbd> under <strong>Integrations</strong>.

<img src="/wp-content/uploads/see-all-integrations-2025.png" srcset="/wp-content/uploads/see-all-integrations-2025@2x.png" class="help-center-img img-bordered">

From the Integrations window, enter your _Host Domain_ then click the Generate an access token on _your URL_ link.

<img src="/wp-content/uploads/gkc-github-enterprise-server-integration.png" class="help-center-img img-bordered">

This opens a web browser where you next log in with your GitHub Enterprise Server credentials and generate an access token.

<img src='/wp-content/uploads/accesstoken-github-enterprise.png' class='center img-bordered'>

Copy your token to the clipboard as this is the only time you will see this token.  Paste the token into GitKraken and click on <button class='button button--success button--ui button--nolink'>Connect</button>.

<img src="/wp-content/uploads/gkc-github-enterprise-server-integration-2.png" class="help-center-img img-bordered">

### Generating an SSH Key for GitHub Enterprise Server
<div class='callout callout'>
    <p>Note 📝 - GitKraken uses your SSH key defined in <kbd><i>Preferences  <i class='fa fa-caret-right'></i>  SSH</i></kbd> for git operations unless you set up a GitHub-specific SSH key, or enable your local SSH Agent.</p>
</div>
Once your GitHub Enterprise Server account has been connected to GitKraken, you may easily generate an SSH key and add it to your GitHub Enterprise Server account from <kbd><i>Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>.

<img src='/wp-content/uploads/gkc-github-enterprise-server-add-key.png' class="help-center-img img-bordered">

Click the <button class='button button--success button--ui button--nolink'>Generate SSH key and add to GitHub Enterprise Server</button> button and watch the magic happen.

Alternatively add existing  _SSH Defaults_ with <button class='button button--uiorange button--ui button--nolink'>Add key to GitHub Enterprise Server</button> or an existing key pair through _Add existing SSH key_.

***

## Connecting to multiple GitHub Enterprise Server accounts

GitKraken connects to one GitHub Enterprise Server account at a time. However, with GitKraken Pro's multiple <a href="/start-here/profiles">profile</a> support, you can easily switch between profiles that each have their own associated GitHub Enterprise Server accounts.
