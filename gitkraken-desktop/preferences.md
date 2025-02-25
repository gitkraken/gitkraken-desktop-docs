---

title: Preferences
description: Customize your GitKraken Desktop experience to match your tastes!
taxonomy:
    category: gitkraken-desktop

---

Navigate to <i class="fas fa-cog"></i> <kbd><strong>Preferences</strong></kbd> to customize your GitKraken Desktop experience. Here are what each of the major sections do.


<img src="/wp-content/uploads/preferences.png" srcset="/wp-content/uploads/preferences@2x.png 2x" class="img-responsive center img-bordered">

*** 

## Organization

This section will actually be labeled with your organization name rather than "Organization".  It shows the members and teams within your organization. Click `switch organization` to swap to another organization.

The Owner and any Admins are able to:

- Change role of members within the organization
- Invite members to the organization and purchase licenses
- Create and manage teams


<div class='callout callout--warning'>
    <p><strong>Note:</strong> the Organization section is only available to users who have a Pro or Enterprise license.
</p>
</div>

## General

### Auto-Fetch

Set the number of minutes between auto-fetches. This value must be between 0 and 60 minutes, and it will fetch all visible remotes for the repository. Setting the value to 0 minutes will disable auto-fetch.

If you’re experiencing issues with performance, consider setting your auto-fetch value to 0 and restarting the application. 
 
### Auto-Prune

Removes any remote-tracking references that no longer exist on the remote.

### Automatic Conflict Detection

GitKraken will monitor your base branch for conflicts and alert you with an icon in the toolbar when conflicts are detected, providing options to resolve your conflicts sooner rather than later.
Unchecking this option will disable the automatic conflict detection feature for all repositories. You can disable this feature on a per-repo basis by going to the repo preferences and unchecking the box for automatic conflict detection.
More information on [Automatic Conflict Detection](https://help.gitkraken.com/gitkraken-desktop/branching-and-merging/#automatic-conflict-detection-preview)

### Keep Submodules Up to Date

When enabled, GitKraken Desktop will automatically update all submodules after performing a Git action. This setting can be configured on a per-repo basis.

### Default Branch Name

Set the default name when initializing a new repo. The app defaults to `main`.


### Delete ".orig" files

GitKraken Desktop will make .orig files during a merge. If turned off, these before and after files will not be automatically deleted. 

### Show All Commits in Graph

Enabling this option will force GitKraken Desktop to always show all commits in repo. This setting may cause performance issues with large repositories.

### Initial Commits in Graph

Set the max number of commits GitKraken Desktop will show in the graph. Lower counts may help improve performance, and the minimum value is 500 commits.

### Lazy Load Commits

When enabled, GitKraken Desktop will only load additional commits if you reach the earliest commit in the Graph. This setting may cause performance issues with large repositories.

### Remember tabs

This will remember open tabs when you quit GitKraken Desktop. This option will also remember what tabs you have open for each profile. 

### Longpaths (Windows Only)

For Windows users, GitKraken Desktop will respect the `core.longpaths` setting in the global .gitconfig. Adjusting this setting will change `core.longpaths` in your .gitconfig. `core.longpaths` only applies to the files in the working directory, not in the .git directory, to maintain compatibility with Git for Windows.

### AutoCRLF (Windows Only)

For Windows users, GitKraken Desktop will respect the `core.autocrlf` setting in the global .gitconfig. Adjusting this setting will change `core.autocrlf` in your .gitconfig. Enabling this option auto-converts CRLF line endings into LF when adding a file to index, and vice versa when checking out code onto your file system. For more information check out this [git documentation](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration#_core_autocrlf)


### Use extended logging in activity log

Provides more information for the activity log. You may access the activity log from <kbd><strong>Help > Support Logs > Activity Logs</strong></kbd>.

### Forget all Usernames and Passwords

Removes credentials that currently stored by GitKraken Desktop.

### Share work-in-progress status with my team

Allows other users in your team to see your local work in progress files. This is directly related to the [Teams](/working-with-repositories/teams) feature.

## Profiles

GitKraken Desktop uses profiles to store your app preferences, current [Tabs](/start-here/interface/#tabs), and Git config information.

[Learn more about Profiles](/start-here/profiles)

## SSH & Integrations

GitKraken Desktop supports HTTPS and SSH authentication, and provides useful integrations with many Git hosting services. Here's how to get started.

- [General SSH settings](/gitkraken-desktop/authentication/#ssh)
- [GitHub Integration](/gitkraken-desktop/github-gitkraken-desktop/)
- [GitHub Enterprise Server Integration](/gitkraken-desktop/github-enterprise/)
- [GitLab Integration](/gitkraken-desktop/gitlab/)
- [GitLab Self-Managed Integration](/gitkraken-desktop/gitlab-self-hosted/)
- [Bitbucket Integration](/gitkraken-desktop/bitbucket/)
- [Bitbucket Data Center Integration](/gitkraken-desktop/bitbucket-server/)
- [Azure DevOps Integration](/gitkraken-desktop/azure-devops/)
- [TFS, AWS CodeCommit, custom service, etc](/gitkraken-desktop/authentication/)
- [Jira Cloud Integration](/gitkraken-desktop/jira/)
- [Jira Data Center Integration](/gitkraken-desktop/jira-data-center/)

## External Tools

### External Merge Tool
This is where you may set your preferred external merge tool. 

- [Supported Merge Tools](/working-with-repositories/branching-and-merging/#external-merge-tools)
 
### External Diff Tool

There is where you may set your preferred external diff tool.

- [Supported Diff Tools](/working-with-commits/diff/#external-diff-tools)

### External Editor

You may open a repo in your preferred external editor program using the [Command Palette](/start-here/command-palette/). Supported editors include:

- VS Code
- Atom
- Sublime
- IntelliJ

You may also set your preferred external editor selecting `<Custom>` and entering the path for the editor you want to use. If needed, you can configure the arguments to pass when opening repos or files in your selected editor.


### Default Terminal

You may open the current repo folder in terminal by navigating to  <kbd><strong>File > Open Terminal</strong></kbd> or use the keyboard shortcuts <kbd><strong>opt</strong></kbd> + <kbd><strong>T</strong></kbd> (Mac) / <kbd><strong>alt</strong></kbd> + <kbd><strong>T</strong></kbd> (Windows + Linux). 

Set your preferred terminal from this preference option for this action.
 
### Use Custom Terminal Command

Enables the option to specify a custom command to open a terminal window. 

For example, to set up GitKraken Desktop to open Powershell 7, use the command `start "" "C:\Program Files\PowerShell\7\pwsh.exe" -noexit -command "cd %d"`



## Notifications

GitKraken Desktop's notification system is designed to tell you about updates, bug fixes, product tips, and more. The following preferences are available:

- Enable Desktop Notifications
- Receive Marketing Notifications
- Receive Help Notifications

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Marketing notifications can only be disabled by Pro users.
</p>
</div>


## UI Customization

The following UI preferences are available:

- [Theme](/start-here/themes)
- Notification location
- Date/Time Locale
- Date/Time Short Format
- Default Workspace Color
- Default color for default groups
- Show toolbar icon labels
- Enable spell checking
- Display author initials instead of avatars (Gravatar) and generic remote icons instead of avatars
- Show ghost branch/tag when hovering over or selecting a commit
- Highlight associated rows when hovering over a branch
- Show branches and tags in graph
- Show commit author in graph
- Show commit date/time in graph
- Show commit message in graph
- Show commit description in graph
- Show commit sha in graph
- Show commit tree in graph
- Hide Launchpad in status bar

### Date/Time Locale and Short Format

Date and Time Locale can be set from the UI Customization to match your system or you can set a custom locale. The Date/Time Short Format will match the Date/Time Locale. However, you can define a custom format as well.

See all formatting options that can be used <a href="https://momentjs.com/docs/#/displaying/format/">here</a>. 

## Commit Signing

Learn more about how to [configure GPG signing](/git-workflows-and-extensions/commit-signing-with-gpg/#configure-gpg-in-gitkraken) in GitKraken Desktop.

## Editor Preferences

Customize the following settings for your GitKraken Desktop editor and diff:

- Font
- Font size
- Tab size
- End of line character
- Syntax highlighting
- Show line numbers
- Word wrap

## In-App Terminal

These settings only effect to the in-app `Terminal`.

- Font
- Font Size
- Line Height
- Cursor Style
- Autocomplete behavior
- Default Terminal (Windows only)
 
## Experimental

Activate [Experimental Features](/gitkraken-desktop/experimental-features.md) and try out ideas that are still being worked on.

- Git Binary: Use Git executable instead of NodeGit Git actions (partially, not all git actions are implemented to Git executable)
- AI Commit Message Generation

## Repo-Specific Preferences

Repo-Specific preferences only apply to the repo currently open in GitKraken Desktop. The following preferences are repo-specific:

- [Encoding](/gitkraken-desktop/editing-files/#encoding)
- [Gitflow](/gitkraken-desktop/git-flow/)
- [Git Hooks](/gitkraken-desktop/githooks/)
- [Commit](/working-with-commits/commits/)
- [LFS](/gitkraken-desktop/git-lfs/)
- [Issues](/gitkraken-desktop/jira/)
- [Team](/gitkraken-desktop/team-view/)
- [Submodules](/gitkraken-desktop/submodules/#keep-submodules-up-to-date)

You may configure unique repo-specific settings for each repo.

