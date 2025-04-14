---

title: Open, Clone, and Init
description: Learn the basics of GitKraken Desktop, like initializing or cloning projects!
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

Whether you are a newborn or a wizened deep-ocean octopod, each user will need to open, clone, or initialize a repo in GitKraken Desktop.

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/8uxrA56VJgY?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
</div>

***
## Setup
The essential setup process includes:

1. [Installing](/gitkraken-desktop/how-to-install) GitKraken Desktop
2. Creating an account and setting up your [profile](/gitkraken-desktop/profiles)

Once this is complete, you are ready for your oceanic journey!

***
## Repository Management

The Repo Management tab provides an overview of your active repositories, Workspaces, and favorite repositories. To access the Repo Management tab, either click on the folder icon located at the top left or utilize the keyboard shortcut <kbd>Alt + O</kbd> (Windows/Linux) or <kbd>Cmd + O</kbd> (Mac).

<img src='/wp-content/uploads/repo-mgmt-2025.png' srcset="/wp-content/uploads/repo-mgmt-2025@2x.png" class="help-center-img img-bordered">

At the top left corner, you'll find three options for managing Git repositories within your projects:

1. **Browse** - Open a local Git repository already initialized and available locally.
2. **Clone** - Clone a remote Git repository already initialized.
3. **Init** - Create an empty Git repository or reinitialize an existing one.

Additionally, you can create a new Workspace and manage your integrations.

In the Repo Management tab you will find a list of your active repos (Open Repositories), your favorites (Favorites) and your [Workspaces](/gitkraken-desktop/workspaces/).

For each repo, you have three available actions:
* Open repository in VS Code.
* Open repository details (this toggles a panel with the README.md content)
* Open/Close repo tab.


***

### Opening an existing project
GitKraken Desktop allows you to load your existing repositories and pick up where you left off. It's also useful for visualizing past work done.  

From the Repository Management window, select <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Browse</span></button> to open a file explorer window and select the repository folder to open it in Gitkraken Desktop.

<img src='/wp-content/uploads/open-repo-2025.png' srcset="/wp-content/uploads/open-repo-2025@2x.png"  class="help-center-img img-bordered">

Alternatively, click the + icon to open a New Tab and access the <strong>Browse</strong> button from there.

<img src='/wp-content/uploads/open-new-tab-2025.png' class="help-center-img img-bordered">

***
### Cloning an existing project

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OA9o09Bq5M8?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

If your project is not on your local machine or you want a new copy, clone the project from the Repository Management window by selecting <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Clone</span></button>.

<img src='/wp-content/uploads/clone-repo-mgmt-2025.png' srcset="/wp-content/uploads/clone-repo-mgmt-2025@2x.png" class="help-center-img img-bordered">

Alternatively, you may also clone from <kbd><strong>File > Clone</strong></kbd> or from the New Tab view. No matter how you access the Clone option, you'll be prompted to open the newly copied project in GitKraken Desktop.

<img src='/wp-content/uploads/clone-url.png' srcset='/wp-content/uploads/clone-url@2x.png 2x' class="help-center-img img-bordered">



***
### Initialize a new project
There are a few ways to initialize a new repo.

From the Repository Management window, just hit the <button class='button button--primary button--ui button--nolink'><span style='color:#141422;'>Init</span></button> button. 

<img src='/wp-content/uploads/init-2025.png' srcset="/wp-content/uploads/init-2025@2x.png" class="help-center-img img-bordered">

All you need to do is fill out the fields and select <button class='button button--success button--ui button--nolink'>Create Repository</span></button> for the magic to begin.

You may also initialize a repo from <kbd><strong>File > Init</strong></kbd> or from the New Tab view. 

#### Input
* New repository path
* `.gitignore` template (**optional**)
 * Automatically creates a `.gitignore` file in your working copy.

* License (**optional**)
 * On init, GitKraken Desktop will create a `LICENSE` file in your repository.
 * Check out the [Open Source Initiative](https://opensource.org/licenses) or find out more about [Choosing a License](http://choosealicense.com/).

#### Output
* A new initialized Git project at the specified repository path by creating a `.git` folder.
* The project is opened in GitKraken Desktop
* An "Initial commit" on a `main` branch containing a blank `README.md` along with a `.gitignore` and `LICENSE.md` if applicable.

 <div class='callout callout--success'>
     <p>GitKraken Desktop also allows initializing a repository directly to a remote Git hosting provider such as GitHub and Bitbucket.</p>
 </div>

***

### Customize your Repository Management tab

* Reorder repository groups by dragging and dropping the header to create a more organized list.
* Change the color of a group by selecting <kbd>Change color</kbd> in the three-dot menu of any repo group. 
* Set a default color for Workspaces and other groups in <kbd>Preferences > UI Customization</kbd>.

<img src='/wp-content/uploads/gkd-repo-mgm-tab-customize1.gif' class="help-center-img img-bordered">

