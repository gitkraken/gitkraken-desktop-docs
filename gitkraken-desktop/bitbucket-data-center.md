---

title: Bitbucket Data Center Integration
description: Integrate GitKraken Desktop with your Bitbucket Data Center repository by following these steps.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

GitKraken Desktop allows you to authenticate with Bitbucket Data Center, which will help you find repos on Bitbucket Data Center when cloning or adding your remotes.

**Benefits**

* Create repositories on Bitbucket Data Center including .gitignore and license
* Easily generate an SSH key pair and copy to clipboard to add to Bitbucket Data Center
* Save authentication into [profiles](/gitkraken-desktop/profiles/)
* Clone from Bitbucket Data Center repo list
* Add remotes for Bitbucket Data Center repos
* Create and view Pull Requests

<div class='callout callout--warning'>
    <p>Note: All Self-Hosted server integrations, including Bitbucket Data Center, require an <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">Advanced subscription</a> tier or higher.</p>
</div>

***

## Connecting to Bitbucket Data Center

<div class='callout callout'>
    <p>Note 📝 - GitKraken Desktop supports any version of Bitbucket Data Center released within one year.</p>
</div>

To authenticate with Bitbucket Data Center, navigate to the upper right corner to access <kbd><i> <i class="fas fa-cog"></i> Preferences    <i class='fa fa-caret-right'></i>     Integrations</i></kbd>

<img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered">

Or alternatively if you are in the <kbd>New Tab</kbd> view, click on <kbd>See all the integrations</kbd> under <strong>Integrations</strong>.

<img src="/wp-content/uploads/see-all-integrations-2025.png" srcset="/wp-content/uploads/see-all-integrations-2025@2x.png" class="help-center-img img-bordered">

From the Integrations window, select **Bitbucket Data Center**. Enter your host domain URL and then click the Generate a token on Bitbucket Data Center button. Note the permissions that need to be assigned to the token on your Bitbucket Self-Hosted server.

<img src="/wp-content/uploads/connecting-bb-data-center-2025.png" srcset="/wp-content/uploads/connecting-bb-data-center-2025@2x.png 2x" class="help-center-img img-bordered">

This opens a web browser where you will log in with your Bitbucket Data Center credentials and create an access token.

<img src='/wp-content/uploads/BitbucketServerPAT.png' class="help-center-img img-bordered">

Copy the token and paste it into GitKraken Desktop, then click the <button class='button button--success button--ui button--nolink'>Connect</span></button> button.


***
## Generating SSH keys for Bitbucket Data Center.
<div class='callout callout'>
    <p>Note 📝 - GitKraken Desktop uses your SSH key defined in <kbd><i>Preferences  <i class='fa fa-caret-right'></i>  SSH</i></kbd> for git operations unless you set up a BitBucket-specific SSH key, or enable your local SSH Agent.</p>
</div>

Once your Bitbucket Data Center account has been connected to your GitKraken Desktop, you may then generate an SSH key and add it to your Bitbucket Data Center account from <em class='context-menu'>Preferences     <i class='fa fa-caret-right'></i>    Integrations</em>

<img src="/wp-content/uploads/ssh-bb-data-center-2025.png" srcset="/wp-content/uploads/ssh-bb-data-center-2025@2x.png 2x" class="help-center-img img-bordered">

Click <button class='button button--success button--ui button--nolink'>Generate SSH key and copy to clipboard</span></button> and follow the toast prompt to add the key to your Bitbucket Data Center account. If you miss the toast pop-up or need to copy the public key later, you can use the link as well.

In your Bitbucket Data Center SSH keys page, click <button class='button button--primary button--ui button--nolink'>Add Key</span></button>.

<img src='/wp-content/uploads/bitbucket-server-add-key.png' class="help-center-img img-bordered">

Paste your key and click <button class='button button--primary button--ui button--nolink'>Add Key</span></button>.

<img src="/wp-content/uploads/bitbucket-server-SSHkey-add.png" srcset="/wp-content/uploads/bitbucket-server-SSHkey-add@2x.png 2x" class="help-center-img img-bordered">

***
## OAuth integration with Bitbucket Data Center
GitKraken's integration with Bitbucket Data Center provides handy information about your repositories.

First, you may search through your existing repositories when cloning:

<img src="/wp-content/uploads/bb-data-center-clone.png" srcset="/wp-content/uploads/bb-data-center-clone@2x.png 2x" class="help-center-img img-bordered">

Next, GitKraken Desktop presents a list of forks of the current repository when adding remotes:

<img src="/wp-content/uploads/add-remote-bb-dc-2025.png" srcset="/wp-content/uploads/add-remote-bb-dc-2025@2x.png 2x" class="help-center-img img-bordered">

Of course, you still have the option of manually entering repo URLs.

***

## Connecting to multiple Bitbucket Data Center accounts

GitKraken connects to one Bitbucket Data Center account at a time. However, with GitKraken Pro's multiple <a href="/start-here/profiles">profile</a> support, you can easily switch between profiles that each have their own associated Bitbucket Data Center accounts.

## Bitbucket Data Center Pull Request Reviewers

Bitbucket Data Center supports pull request reviewers. GitKraken Desktop will display the list of reviewers for a pull request. In order to view the list of reviewers, you must have Project Admin permissions and connect using a token with Project Admin and Repository Admin scopes.
