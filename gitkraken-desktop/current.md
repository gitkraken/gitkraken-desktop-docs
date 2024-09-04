---

title: GitKraken Desktop Release Notes
description: View a history of the new features and fixes in GitKraken Desktop's Version 10.
og_image: /img/GitKrakenClient-Hero.png
taxonomy:
    category: gitkraken-desktop

---

Behold the evolution of GitKraken Desktop! Find out what&rsquo;s new, what&rsquo;s fixed, or just take a trip down memory lane with a nostalgic swagger, remembering those bugs of yesterday.

<a href="https://www.gitkraken.com/download" target="_blank" class="button button--basic ">Download Current Version Now</a>

Check out our [GitKraken Roadmap](https://www.gitkraken.com/git-client/roadmap) to see what we’re working on.


***
<a id="v10-3-0"></a>
## Version 10.3.0

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/U0BNklVfZQg" frameborder="0" allowfullscreen></iframe>
</div>

_“Label the maple table with sable staples.”_

### Wednesday, September 4th, 2024

### New ✨
 - **Customize Launchpad to create the ultimate hub for you and your team's work**
   - Launchpad can now be filtered by PR and Issue labels.
   - The Team Launchpad can now be filtered by users, giving you a more focused view of specific team members' work.


### Improvements 🙌
 - Commit Graph:
   - Added support for having no commit selected in the graph by left-clicking the selected commit. This is an easy way to hide the Commit Details Panel and give the graph more screen space. You can still hide the Commit Details Panel manually with <kbd>cmd/ctrl+K</kbd> or from the `View` app menu.
   - The author filter in the Commit Graph now groups emails for organization members so you can more easily filter by people instead of selecting all emails associated with a person.

### Bug Fixes 🐛
 - Experimental Feature - Git Executable:
   - Fixed an issue with renamed branches where pulling could overwrite local commits.
   - Fixed an issue where the WIP was not autostashed when dropping the latest commit(s).
   - Fixed an issue where interactive rebase failed when executed within a submodule.
   - Fixed an issue on Windows where updating preferences (like long path) was failing when only the bundled Git version was installed.
 - Fixed an issue where Cloud Patches couldn't be created from commits due to input validation.
 - GitKraken will now correctly detect Beyond-Compare 5 installations on Windows.
 - Improved the message in the Launchpad summary to explain when an integration is not connected or not selected.
 - Fixed an issue where certain repositories were not displayed in the Repository Management tab.
 - Fixed an issue where transparent branch/tag avatars were displayed with a black background. 
 - Fixed an issue where repository aliases were not showing in the Repo Management tab.  

***

<a id="v10-2-0"></a>
## Version 10.2.0

_“We kept tabs on that Cloud Patch button you all loved.”_

### Thursday, August 8th, 2024

### New ✨
 - **New Commit Panel changes**
   - Added a tabbed form for committing, stashing, creating Cloud Patches, and creating Code Suggestions.
   - Use the staging area to choose which changes you want to stash. This now allows you to easily stash specific files and adds support for stashing specific hunks.
 - **Team Launchpad is even more actionable with PR groupings by status**
   - Visit the Launchpad tab and toggle the view from `Personal` to `Team` to see all PRs and Issues for the repositories in a Cloud Workspace.
   - The Team Launchpad (preview) now groups pull requests by status like the Personal Launchpad.


### Improvements 🙌
 - Improved the flow of opening a repo from a new tab:
   - Added a button to open the Repository Management tab.
   - Added a button to browse and open a repository.
 - Repository Management tab:
   - Added an option to hide/unhide groups.
   - Added an option to set a group's color to default color set in *Preferences > UI Customization*.
 - Launchpad:
   - Improved the UX of filtering.
   - Added 'None' options for Launchpad pull request and issue filters.
 - Experimental Feature - Git Executable:
   - Added support for git status.
 - Updated Electron to v31.
 - Updated Git to 2.45.2.


### Bug Fixes 🐛
 - Fixed an issue where Cloud Workspace repositories were not loading after connecting the integration in the Repository Management tab.
 - Fixed an issue where the dropdown menu would not close when clicking one of its options in the Repository Management tab.
 - Fixed an issue where the author filter in the Commit Graph was selecting and deselecting teams/members that you had not clicked on.
 - Fixed an issue where the open repository dialog did not remember the last opened repository and always showed the home directory.
 - Fixed an issue where interactive rebase editor showed context menu options not matching the drop-down menu options.
 - Fixed an issue where the Commit Graph was not sorting checked items to the top when re-opening the author filter.
 - Fixed issues where the build status of a pull request in Launchpad would be incorrect.
 - Fixed an issue where the Commit Graph would display an unaesthetic continuous line when the avatar image had a transparent background.
 - It is now possible to filter by files with spaces in the right panel.
 - Fixed issues where performing organization actions (such as inviting new members) could fail silently or show a false success message after failing.
 - Fixed duplicate base branch options that showed when creating a branch in the Launchpad issue view panel.

***

<a id="v10-1-1"></a>
## Version 10.1.1

### Wednesday, July 17th, 2024

### Improvements 🙌
 - Updated the look & feel of the Repository Management tab.
 - Updated the look & feel of the Launchpad summary in the status bar.

### Bug Fixes 🐛
 - Fixed a bug where cloning from the Repository Management tab could result in being unable to switch tabs (even after cloning was finished).

***
<a id="v10-1-0"></a>
## Version 10.1.0

_“It's a bird, it's a plane... it's your Launchpad summary in the status bar!”_

### Tuesday, July 9th, 2024

### New ✨
 - **Keep an eye on your most important PRs with the Launchpad summary in the status bar**
   - The Launchpad summary indicates your most critical pull request in the status bar.
   - Click on the indicator in the status bar to open a summary of your pull requests grouped by status, such as ready to merge, blocked, and needs your review.
   - Clicking on a pull request status group will open the Launchpad tab with the relevant group expanded so you can see more info and take action on the pull requests.
   - The Launchpad summary contains pull requests based on the filters set in the Launchpad tab. 
 - **Customize your Repository Management tab**
   - Reorder repository groups by dragging and dropping the header to create a more organized list that fits your workflow.
   - Change the color of a group by selecting `Change color` in the three-dot menu of any repo group. Use color to categorize Workspaces or highlight your most used groups of repositories.
   - Set a default color for Workspaces and other groups in *Preferences > UI Customization*
 - **Commit search with multi-language support**
   - The commit search now supports searching for UTF-8 characters

### Improvements 🙌
 - Launchpad:
   - Added an 'Author' column for pull requests and issues
   - Added a pull request action to checkout the branch if a local repository is found.
   - Added a pull request action to clone the repository if it is not found locally.
   - Added the ability to clone or locate the repository from the pull request panel.
 - Repository Management tab:
   - Added a new repo group to display recently opened repositories.
   - Added a button to open a Cloud Workspace in the Launchpad tab so you can see all PRs for the repositories in that Workspace.
   - Improved loading speeds when there are a large number of repositories.
 - Experimental Feature - Git Executable:
   - Added interactive rebase support
     - Includes support for interactive rebase actions `edit commit message`, `drop commit(s)`, `move commit(s) up / down`, and `squash commits`
   - Added create/rename branch support.
   - Added load stashes support.
   - Added support for the Fetch All and Pull All actions in the Repository Management tab.
   - Added support for applying a Cloud Patch with cherry-pick.
 - Upgraded to Electron 30.

### Bug Fixes 🐛
 - Fixed an issue where hiding and showing folders in the left panel wasn't working.
 - Fixed an issue where Cloud Patches could not be created after resolving a merge conflict.
 - Lowered minimum window dimensions to fix maximizing on GNOME-based desktop environments at lower resolutions.
 - Fixed an issue where submodules were not synced when doing a fast-forward.
 - Experimental Feature - Git Executable:
   - Fixed an issue where branches couldn't be fast-forwarded to HEAD using the context menu when HEAD is checked out at a specific commit.
   - Fixed an issue where authentication was not prompted once credentials expired.
 - Fixed an issue where repositories could not be added to an Azure Workspace with manually added repositories.
 - Removed the unused 'People' column from the WIPS-only view in Launchpad.
 - Fixed cases when Azure DevOps issues would not load within Launchpad.
 - Fixed <kbd>Ctrl+Tab</kbd> skipping over a tab when on the Repo Management or Launchpad tab.
 - Fixed <kbd>Ctrl+Tab</kbd> / <kbd>Ctrl+Shift+Tab</kbd> not being able to enter an expanded Launchpad tab.

***

<a id="v10-0-2"></a>
## Version 10.0.2

### Tuesday, June 4th, 2024

### Improvements 🙌
 - Repository Management tab:
   - The search bar will be automatically focused when accessing the Repository Management tab.
   - Custom Workspace icons will now show in the collapsible section header.
   - Your scroll position will be saved when returning to the Repository Management tab.
   - After creating a new Workspace, the Workspace will be expanded and scrolled to automatically.
   - User avatars will show in the section header of any shared Cloud Workspace.
 - Experimental Feature - Git Executable:
   - Added push tag support.

### Bug Fixes 🐛
 - Experimental Feature - Git Executable:
   - Fixed an issue where continuing a rebase would fail after a conflict if the current commit message started with `#`.
 - Fixed an issue where the client would fail to load Bitbucket Server users.

 ***

<a id="v10-0-1"></a>
## Version 10.0.1

_“To err is human; to forgive, divine”_

### Monday, May 20th, 2024

### Improvements ✨
 - Updated Git to 2.44.1.
 - Improved the layout of filtering controls in Launchpad.

### Bug Fixes 🐛
 - Fixed an issue where pull requests from archived repositories would appear in Launchpad.
 - Fixed an issue where GitLab Self-Managed Workspaces would not show any repositories.

***

<a id="v10-0-0"></a>
## Version 10.0.0

_“How many arms does Keif have? Ten-tacles.”_

### Tuesday, May 14th, 2024

### New ✨
 - GitKraken Client is now called GitKraken Desktop
 - Focus View is now called Launchpad

### Improvements 🙌
 - Completely re-built our in-app informational/error message pop-ups ("toasts") to give them a fresh look.
 - Added loading icon to Launchpad issue and pull request panel
 - Show provider icon for Launchpad workspace dropdown. Hide hosting service dropdown when a workspace is selected rather than disabling it
 - Default the Launchpad to open in the pull request sub tab
 - Experimental Feature - Git Executable:
   - Added stage files support
   - Added unstage files support
   - Added stash support
   - Added support for Git Credential Manager on SSH settings
 - The Launchpad sub tab will be remembered when going between different tabs and when the client is restarted
 - The Launchpad search text will be remembered when going between different tabs
 - Now able to search Launchpad items using pull request and issue number
 - Updated Git to 2.44.0 and 2.44.0-windows
 - Update git-lfs to 3.5.1
 - Renamed the Jira Server integration to Jira Data Center as Jira Server has reached end of support
 - Use gpg from bundle if gpg executable is not found on Windows
 - Add ability to suggest changes to Pull Requests via Cloud Patches
 - Show Suggested Changes for a Pull Request in the Pull Request view
 - Add a new Team view within Launchpad that shows all PR's and issues for an integration
 - Organize pullrequests within the Launchpad view into different groups. This is only for Launchpad personal view
 - Add action button to open code suggestions for PR's in Launchpad

### Bug Fixes 🐛
 - Interacting with an expired notification now clears that notification instead of leaving it unread forever
 - Fixed an issue where the Launchpad issue and pull request panel did not span to the top of the page
 - Fixed an issue where the diff editor not showing images when switching between files
 - Fixed an issue where LFS detection was failing with LFS repos having custom LFS hooks
 - Fixed getting "Invalid Version: undefined" when creating a workspace
 - Fixed an issue on windows where closing a terminal would close all terminals in the app
 - Fixed an issue where the Launchpad refresh button would disappear for a moment when selected a workspace to filter by
 - Fixed an issue with cloning LFS repositories with hundreds of LFS files.
 - Experimental Feature - Git Executable:
   - Fixed an issue were commits could be made using the user name and email specified in the global git config file instead of the profile values when they were different
   - Fixed fast-forwarding tags
