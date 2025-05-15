---

title: Gitflow
description: Gitflow is a list of rules to keep a repo’s history organized, and is used to make the release process, bug fixes, and feature creation easier.
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

Gitflow is a list of rules to keep a repo’s history organized, and is used to make the release process, bug fixes, and feature creation easier.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/eTOgjQ9o4vQ?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

***
## Configuration
First initialize Gitflow in <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> Gitflow</em> and change the default branch names if desired.

<img src="/wp-content/uploads/gitflow-preferences-2025.png" srcset="/wp-content/uploads/gitflow-preferences-2025.png" class="help-center-img img-bordered">

Once initialized, two branches will always be present: `main` (The version in production) and `develop` (The version currently in development for the next release).

Changes are merged into these branches.  If you do not currently have these branches in your local repository, GitKraken Desktop will create them when Gitflow is initialized.

***
## Usage
With Gitflow initialized in your repo, you will get an additional menu in the left panel.  Start or finish any of your Gitflow branches here.

<img src="/wp-content/uploads/giflow-panel-2025.png" srcset="/wp-content/uploads/giflow-panel-2025@2x.png" class="help-center-img img-bordered">

Create new Gitflow branches by clicking the green button on the Gitflow menu on the left.

Or whenever you add a branch, include the prefix for the Gitflow branch type i.e.
`release/branch-name`.  Any branches that do not have the prefix, will be displayed in the local
repository section, but not in the Gitflow menu.

<img src="/wp-content/uploads/prefix-example-2025.png" srcset="/wp-content/uploads/prefix-example-2025@2x.png" class="help-center-img img-bordered">

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Gitflow has the benefit of adding all features, hot-fixes, and release branches in different folders.</p>
</div>

Gitflow branches can be pushed to a remote which is the same as '_Publishing_' the Gitflow object in the command line.

### Feature
Feature branches are used for new features or bug fixes.  They typically exist only in local repos and aren't shared with others.

When finishing a feature branch, GitKraken Desktop will merge the feature branch into `develop`, and delete the feature branch from the local repository.

<img src="/wp-content/uploads//finish-feature.gif" class="help-center-img img-bordered">

You also have the option to rebase the `feature` branch on top of `develop`.

### Release
Releases are major and minor versions of your product.  They're often shared with other collaborators working on the same version.

When finishing a release, the release branch is merged into both `main` and `develop` branches. 

<img src="/wp-content/uploads/finish-release-context-menu-2025.png" srcset="/wp-content/uploads/finish-release-context-menu-2025@2x.png" class="help-center-img img-bordered">

This creates a tag with the release name for future reference.

<img src="/wp-content/uploads/finish-release-2025.png" srcset="/wp-content/uploads/finish-release-2025@2x.png" class="help-center-img img-bordered">

### Hotfix
Hotfixes are the same as Releases in Gitflow, except hotfix branches are created on top of `main`, while release branches are created on top of `develop`.

Hotfixes are for quickly pushing out a change to your production branch.  Common examples of hotfixes are fixing typos, and bugs that need to be pushed out as soon as possible to production.

<img src="/wp-content/uploads/finish-hotfix-2025.png" srcset="/wp-content/uploads/finish-hotfix-2025@2x.png" class="help-center-img img-bordered">

When finishing a hotfix, GitKraken Desktop will merge the changes into both `main` and `develop`.


### Tag

Tags are used to mark a specific point in the repository's history.  They are often used to mark a release.

Tags can be created from the Gitflow menu, or from the command line. When creating a tag from the Gitflow menu, GitKraken Desktop will create a tag with the same name as the branch. For example, if you create a tag from a `release/1.0.0` branch, GitKraken Desktop will create a tag named `1.0.0`. Additionally, you can add a tag message when finishing a branch. This message will be added to the tag.

<img src="/wp-content/uploads//finish-release-tag.gif" class="help-center-img img-bordered">

<br>
<br>
<img src="/wp-content/uploads//tag-message.png" class="help-center-img img-bordered">

In `Preferences > Gitflow`, you can set a tag prefix.  This prefix will be added to the tag name when creating a tag from the Gitflow menu.  For example, if you set the tag prefix to `v`, and create a tag from a `release/1.0.0` branch, GitKraken Desktop will create a tag named `v1.0.0`.

<img src="/wp-content/uploads/tag-prefix-2025.png" srcset="/wp-content/uploads/tag-prefix-2025.png" class="help-center-img img-bordered">

