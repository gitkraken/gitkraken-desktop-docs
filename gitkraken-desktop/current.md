---

title: GitKraken Desktop Release Notes
description: View a history of the new features and fixes in GitKraken Desktop's Version 11.
og_image: /img/GitKrakenClient-Hero.png
taxonomy:
    category: gitkraken-desktop

---

Behold the evolution of GitKraken Desktop! Find out what&rsquo;s new, what&rsquo;s fixed, or just take a trip down memory lane with a nostalgic swagger, remembering those bugs of yesterday.

<a href="https://www.gitkraken.com/download?product=gitkraken&source=help_center" target="_blank" class="button button--basic ">Download Current Version Now</a>

Check out our [GitKraken Roadmap](https://www.gitkraken.com/git-client/roadmap?product=gitkraken&source=help_center) to see what we’re working on.

***
<a id="v11-8-0"></a>
## Version 11.8.0

<kbd>Wednesday, January 14th, 2026</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Q9CpplgRhEE?si=B6SfWfzFOj4SLln5" frameborder="0" allowfullscreen></iframe>
</div>


_"GitKraken Desktop is ARM'd with new performance improvements!"_


### New ✨
 - **ARM for Linux & Windows**
  - Linux and Windows users on ARM should visit (https://gitkraken.com/download) to ensure the correct build for their chip architecture.
 - **Shallow Clones**
  - Shallow Clones can now be created directly from GitKraken Desktop as part of the clone workflow instead of requiring manual creation outside the app.

### Bug Fixes 🐛
 - Fixed inconsistent code block styling in issue and pull request views.
 - AI context menu items (such as "Explain working changes" and "Explain branch changes") will no longer appear when AI is disabled in settings or when the organization does not allow AI.
 - Users who provide their own OpenAI API key will no longer get an error when resolving conflicts with GPT-5 models.
 - Switching providers in the AI preferences will no longer confuse GitKraken Desktop about which provider's AI models to show in the dropdowns.
 - Fixed excessive whitespace in Jira automation comments and improved visual distinction of status badges.

### Modernization Notice 🎨
 - **Custom Themes:** Custom themes have been disabled in 11.8.0 as we modernize the UI for better performance and maintainability. Our new architecture requires rebuilding theme support from the ground up. Light, dark, and high-contrast themes will remain available during the transition.
   - _We plan to restore custom theme support once the modernization is complete._

***
<a id="v11-7-0"></a>
## Version 11.7.0

<kbd>Tuesday, December 9th, 2025</kbd>

_"Re-rebase (verb): To undo a rebase, only to redo it again."_


### New ✨
 - **Markdown File Preview:**
   - You can now preview markdown files directly in the file viewer! Toggle between Code and Preview modes using the new buttons in the file header.
 - **Undo/Redo for Rebase Operations:**
   - Added support for undoing and redoing rebase operations, including Interactive Rebase, Multi-Commit Cherry Pick, dropping and rewording commits, and AI Commit Composer (Recompose with AI).
 - **GitKraken AI:**
   - **Explain Branch Changes:** Right-click any branch to get a clear summary of what changed and why.

### Bug Fixes 🐛
 - Fixed AI Commit Composer failing when composing commits that include empty new files, binary files, deleted or renamed files, or files with identical hunk headers.
 - F11 now toggles fullscreen on Windows and Linux, matching platform conventions.
 - "Revert Hunk" will no longer appear on working directory changes ("WIP"). "Discard Hunks" is still available for WIP changes.
 - Fixed blank UI when selecting too many options in Launchpad filters for Jira issues.
 - Fixed an issue where commit hook changes did not appear in the unstaged area.
 - Fixed an issue where Git commit options ("skip hooks" and "push after commit") were not being honored when using the commit keyboard shortcut: <kbd>Shift/Cmd + Enter</kbd>.

### Modernization Notice 🎨
 - **Custom Themes:** Custom themes will be sunset in 11.8.0 as we modernize the UI for better performance and maintainability. Our new architecture requires rebuilding theme support from the ground up. Light, dark, and high-contrast themes will remain available during the transition.
   - _We plan to restore custom theme support once the modernization is complete._

***
<a id="v11-6-0"></a>
## Version 11.6.0

<kbd>Tuesday, November 11th, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ySD7E_S1qDA?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>

_"Shallow repos. It's not that deep."_


### New ✨
  - **Experimental Feature - Git Executable:**
    - Shallow repo support is now in preview! If you have a shallowly-cloned repository, you can now open it inside of GitKraken Desktop, and most features will work as normal. If you run into any problems, please let us know!
  - **GitKraken AI:**
    - Explain Working Changes: Select your unstaged edits and get a clear summary of what changed and why.

### Improvements 🙌
 - **Merge Conflict Improvements**
   - AI conflict resolution is now synced to the exact code line so you can review and apply changes faster.
 
 - **GitKraken AI:**
   - Added support for custom OpenAI, Anthropic & Gemini endpoint URLs. 
   - Added the ability to cancel the Commit Composer while the AI is still composing.
   - Added preset instruction choices to custom instructions in preferences.
 
 - **Experimental Feature – Git Executable**:
   - Bumped Bundled Git to v2.51.1.
 - Upgraded Electron to v38.
 - GitHub pull request templates now support organization-level templates.
 - Added a left-panel context menu option to checkout a tag’s commit directly.
 - Added HTML syntax highlighting for `.vue` files.
 - When the graph is focused, using the **Select First** keybind (`Ctrl+Home`/`⌘+↑`) will now select the WIP/conflict when present, instead of the most recent commit/stash.

### Bug Fixes 🐛
 - Commit/Stash message generation no longer errors with `Cannot read properties of undefined (reading ‘requestIdleCallback')`.
 - `Skip Hooks` now appears when committing from Git worktrees.
 - GitHub issues using `<ul>` and `<li>` now format correctly.
 - GitHub issues with descriptions will once again display tooltips on hover.
  - **Submodules**
	  - Fixed failure when cloning unreachable submodules that could leave repos unstable.
	  - Fixed warnings in the Diff View that misattributed changes to uninitialized submodules, when the changes actually belonged to the parent repo.
 - Git notes no longer appear as commits in the graph.
 - Ambiguous branches, tags, and remotes no longer block branch deletion or cause other issues in the graph.
 - Prefetch and other non-standard branches are no longer displayed in the graph.
 - With Git Executable enabled, submodules in the left panel are now alphabetized.

### Modernization Notice 🎨
 - **Custom Themes**
   - As part of our UI modernization efforts, we will be sunsetting custom themes supported starting in 11.7. Light, dark, and high-contrast themes will remain available.


***
<a id="v11-5-1"></a>
## Version 11.5.1

<kbd>Tuesday, October 14th, 2025</kbd>

_"Hey I finished fixing those bugs... Wait, we released already?"_
 
### Improvements 🙌
 - Upgraded Electron to v36 to address performance issues on MacOS Tahoe.

### Bug Fixes 🐛
 - Fixed an issue where submodules that contain dots in their path could not be loaded.
 - Fixed an issue where we could fail to write log entries or Git Hooks executions.
 - Fixed an issue where some repositories with unexpected branches or tags would fail to load.


***
<a id="v11-5-0"></a>
## Version 11.5.0

<kbd>Tuesday, October 7th, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/YorNwlXEFHc?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>

_"It was bothering us too."_

### Performance ⚡️
In 11.5, GitKraken Desktop got faster across the board: large repo load times, stash refreshes, branch and tag updates, and even memory usage have all improved. More perf improvements to come in future releases!      

 - Faster commits and checkouts! We saw **>100%** speed-up on both in the VS Code repository!
   - This is thanks to faster branch and tag refreshes (up to 98% faster!), massively speeding up graph updates on repos with thousands of branches/tags.
 - Up to **480%** faster opening of large repositories! We now perform git maintenance in the background on your open repository. After this completes, future opens will be dramatically faster.
 - Up to **100x** faster loading of stashes, further improving repo open speeds on repositories with many local stashes.
 - Up to 20% less RAM use

### New ✨
 - **GitKraken AI:** 
   - Users can now choose their preferred model from any provided by GitKraken AI, including our newly-added OpenAI GPT-5 models.
   - GPT-5 is now available for those bringing their own OpenAI API key.
   - Added a usage gauge in the profile menu for easy reference of your GitKraken AI token usage.
 - Added organization suggestions in _Preferences > Members_ to help users discover and join relevant teams.
 
### Improvements 🙌
 - When creating a pull request, if only one PR template is available, it will be automatically selected.
 - Hovering an annotated tag in the left panel now shows its annotation.
 - Experimental Feature - Git Executable:
   - Users who have opted out of the Git Executable (in the Experimental settings) should note that most of the performance gains in this release are only available with the Git Executable enabled. 
   - Added support for `Reset branch (hard/mixed/soft) to commit`.
   - Added support for `Undo checkout`.
   - Added support for submodules.

### Bug Fixes 🐛
 - Fixed an issue where the Commit Detail panel was not refreshing after discarding unstaged renamed files or added staged files.
 - Fixed issue where undoing a checkout to a branch with submodules did not update the submodules, even with `Keep submodules up to date` enabled.
 - Fixed a visual issue in dropdowns where the selected content was misaligned in the Create Jira Issue panel.

***
<a id="v11-4-0"></a>
## Version 11.4.0

<kbd>Wednesday, September 3rd, 2025</kbd>

_"No prob-llama: Ollama setup just got easier."_

### Improvements 🙌
 - Added a new Ollama option to the GitKraken AI preferences, which works the same as `<Custom URL>`. This provides a clearer path for users wanting to connect their local Ollama server, making the setup process more intuitive.

### Bug Fixes 🐛
 - Fixed an issue where custom instructions were not enabled when `GitKraken AI` was set as the only configured provider on `gitkraken.dev`.
 - On Jira Cloud issue search, fixed "The requested API has been removed" errors.
 - Fixed an issue where some integrations could not connect when using certain proxy configurations (such as those requesting optional client certificates).


***

<a id="v11-3-0"></a>
## Version 11.3.0

<kbd>Tuesday, August 5th, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/5_e_OBP20Do?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>


_"Compose commits that hit the right note, every time."_

### New ✨
- **AI-powered Commit Composer (Preview):** Use AI to help organize your Git commits into clear, logical stories by breaking up uncommitted changes into meaningful commits or recomposing previous commits. _It's ideal for cleaning things up before a pull request or when you've just been… coding a little too fast._

- **Launchpad:** Team mode is graduating from preview! Users will require an Advanced license (or higher) to continue using Team mode.

### Improvements 🙌
 - ⚠️ **Important:** Ubuntu 18 support has been discontinued. Users running Ubuntu 18 should not update to this version of GitKraken as it will no longer function properly. Please upgrade your operating system to a supported version of Ubuntu to continue receiving GitKraken updates.
 - Experimental Feature - Git Executable:
   - Bumped Bundled Git to v2.50.1
 - <kbd>Cmd/Ctrl+O</kbd> will now open a system dialog to browse for a repo.
 - <kbd>Cmd+Option+O / Ctrl+Alt+O</kbd> will now open the Repo Management Tabs
 - **GitKraken AI** now follows your custom instructions more accurately

### Bug Fixes 🐛
 - Conflict detection button finally has a reserved parking spot on the toolbar, other buttons will not shift around. 
 - Fixed issue where feedback form causes commit options to move off screen

***

<a id="v11-2-1"></a>
## Version 11.2.1

<kbd>Monday, July 7th, 2025</kbd>

_"Tabsolutely better: smarter start, sharper avatars, speedier search."_

### Improvements 🙌
- Revamped New Tab Experience:
   - View more of your recent or favorite repositories and use search to quickly find and open any repo from the list.
- Bitbucket Data Center avatars now show in the Commit Graph and Commit Details Panel.
- Improved coverage for GitLab avatars in the Commit Graph.

### Bug Fixes 🐛
 - Fixed an issue where AI-generated PR titles and descriptions were not working correctly with some GitLab repositories.
 - GitHub Student Pack users will no longer get "missing org header" errors when using GitKraken AI features.
 - Fixed an issue where auto-resolving a conflict with AI did not work with a conflict generated from a cherry-pick or a stash.

***

<a id="v11-2-0"></a>
## Version 11.2.0

<kbd>Tuesday, June 17th, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/fQ23CWMoNCk?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>

_"Because sometimes, even your conflicts need a mediator."_

### New ✨
- **AI-powered Merge Conflict Resolution (Preview):** Quickly handle conflicts by having AI suggest a resolution.
   - When viewing a conflicted file, click `Auto-resolve with AI` to generate a suggested resolution in the Output panel.
   - An explanation is provided for each conflict in the file with a confidence level so you can review with ease.
- **Revert Individual Hunks from the Diff View**
   - You can now revert specific hunks while viewing a diff in Hunk View mode. Selecting `Revert Hunk` will apply the inverse of that hunk’s changes to your working directory as unstaged changes.

### Improvements 🙌
 - The Commit Graph and Commit Details Panel now use provider avatars for GitLab, BitBucket, and Azure repos.
 - Conflict Prevention menus now show the provider avatar of the user you have a potential conflict with.
 - GitKraken AI:
   - Added a cache of the last 5 AI explanations to prevent unnecessary token usage and give you quick access to explanations after navigating away from the Explain panel.
   - Buttons that activate GitKraken AI now have a unified look and feel.
   - GitKraken Desktop will now respect AI provider configurations and security controls enforced by your organization on [GitKraken.dev](https://gitkraken.dev)
 - Experimental Feature - Git Executable:
   - Fully support discard changes by also supporting cases for renamed file and multi-selection of added/renamed files.

### Bug Fixes 🐛
 - Fixed an issue when finishing a release or hotfix with Git Flow where changes did not merge into master after a conflict on develop.
 - Fixed a crash when pressing the Generate button in SSH settings on Windows.

<br>

> **GitKraken also introduced Model Context Protocol (MCP) support via the GitKraken CLI!**<br>Spin up a local MCP server and connect AI tools like GitHub Copilot, Cursor, or Windsurf to surface real‑time code insights (e.g. list PRs, clean old branches, find your code expert) directly from your GitKraken Workspace. [Learn more.](https://www.gitkraken.com/blog/introducing-gitkraken-mcp)

> **Heads up: Support for older Linux distros ending soon**<br>In an upcoming release, GitKraken Desktop will no longer support glibc versions older than 2.28. This affects users on older Linux distributions like Ubuntu 18, Debian 9, etc. If you're using one of these systems, please check these release notes before each update, and avoid updating GitKraken Desktop once support is dropped.

***

<a id="v11-1-1"></a>
## Version 11.1.1
<kbd>Tuesday, May 15th, 2025</kbd>

_"We fixed launching VS Code from GitKraken Desktop! Sorry it took so long; we were trying to figure out how to launch VS Code without GitKraken Desktop."_

### Bug Fixes 🐛
 - Fixed a regression in the last release where opening repositories/files in an external editor caused an "unknown error".
 - Experimental Feature - [Git Executable](/gitkraken-desktop/experimental-features/#git-executable):
    - When discarding all changes fails, error details will be provided in the error message.

***

<a id="v11-1-0"></a>
## Version 11.1.0
<kbd>Tuesday, May 6th, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/jg3n_dg4IjM?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>
 
_"More Jarvis. Less Skynet."_

### New ✨
 - **[GitKraken AI:](/gitkraken-desktop/gkd-gitkraken-ai/)** New AI-powered capabilities to accelerate your development workflow, with expanded support for additional providers and environments.
   - [Pull Request Title and Description Generation](/gitkraken-desktop/gkd-gitkraken-ai/#ai-generated-pull-request-title-and-description)
     - Generate titles and descriptions for Pull Requests based on the commits of the PR in just a click.
     - When creating a Pull Request, click `Generate title and description` to automatically populate the fields using GitKraken AI.
     - If you have a Pull Request template selected, GitKraken AI will attempt to generate content that adheres to the selected template.
   - [Stash Message Generation](/gitkraken-desktop/gkd-gitkraken-ai/#ai-generated-stash-messages)
     - Generate stash messages based on your code changes in just a click.
     - With a WIP selected, click on the sparkle icon in the stash message form to have GitKraken AI generate a stash message based on your staged changes.
   - [Amend Commit Message](/gitkraken-desktop/gkd-gitkraken-ai/#amend-commit-messages)
     - You can now also generate a new commit message when amending a previous commit message.
   - [Expanded provider support when using your own API key](/gitkraken-desktop/gkd-gitkraken-ai/#bring-your-own-key)
     - Added support for OpenAI GPT-4.1 models.
     - Removed the deprecated OpenAI o1-mini model.
     - Added Google Gemini as a provider.
     - Added Azure as a provider (private AI model providers such as Azure require GitKraken Advanced).
     - You can now configure a custom URL endpoint for an OpenAI compatible API to use with GitKraken AI, like a local or self-hosted AI server.


### Improvements 🙌
 - You can now [Hide All / Show All](/gitkraken-desktop/hiding-and-soloing/#hide-or-show-all-refs) items in the Local and Remote sections of the Left Panel from each section header's context menu.
    - The Hide All / Show All actions for Tags and Stashes have also been moved to their respective section headers.
 - GitHub user avatars will now display in the Commit Graph and Commit Details Panel for commits made on GitHub repositories.
 - Experimental Feature - [Git Executable](/gitkraken-desktop/experimental-features/#git-executable):
   - Respects `core.commentString` and `core.commentChar` values from your Git config.
   - Improved stability and performance for on-premise clients when authenticating with Git remotes.
 - [Conflict Prevention](/gitkraken-desktop/conflict-prevention/):
   - Potential conflict alerts with your teammates will now work when the current branch has no upstream.
   - You can now access the branches involved in a potential conflict directly from the menu, and each branch label matches the color of the branch in the Commit Graph.
 - Upgraded Electron to v34.

### Bug Fixes 🐛
 - The [Repository Management tab](/gitkraken-desktop/open-clone-init/#repository-management) now displays GitLab workspaces with more than 25 repos.
 - Fixed an issue in the Commit Graph where branch labels wouldn't render properly.
 - Fixed several styling issues across the application.
 - Experimental Feature - Git Executable:
   - Fixed an issue where Pull failed with files having the same name but different casing in a case-insensitive file system.


***
<a id="v11-0-0"></a>
## Version 11.0.0
<kbd>Monday, March 31st, 2025</kbd>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/sVLftA_jpak?si=87vB8ooSU5GAn5wk" frameborder="0" allowfullscreen></iframe>
</div>

_"Turn it up to 11! 🎸"_

### New ✨
 - **GitKraken AI:** A seamless extension of your development workflow, [GitKraken AI](https://help.gitkraken.com/gitkraken-desktop/gkd-gitkraken-ai/) automates tedious tasks to improve your efficiency and focus.
   - [Commit Message Generation](/gitkraken-desktop/gkd-gitkraken-ai/#ai-generated-commit-messages)
     - You'll now be able to generate clear, meaningful commit messages based on your code changes in just a click.
     - With a WIP selected, click on the sparkle icon in the commit message form to have GitKraken AI generate a commit message for you based on your staged changes.
   - [Explain Commits](/gitkraken-desktop/gkd-gitkraken-ai/#ai-powered-commit-explain)
     - You can now get detailed summaries of changes made in your repository without spending time diving through files and diffs.
     - With one or multiple commits selected in the Commit Graph, click on the `Explain` button in the top right of the Commit Panel to generate an explanation of changes made in the selected commits.
   - [Configure GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai/#bring-your-own-key) from _Preferences > GitKraken AI_
     - Use the `Custom Instructions` setting to provide additional details so GitKraken AI can better tailor commit messages and explanations for you.
     - With GitKraken AI enabled, you can also select to use your own API key to make requests directly to OpenAI or Anthropic. When one of those providers is selected, you can choose what model you'd like to use for each AI feature.
     - Note: The AI Commit Message Generation section has been removed from _Preferences > Experimental_.


### Improvements 🙌
 - We updated our plans to better align with how developers and teams use GitKraken, and your new plan is now reflected in the status bar.
 - Upgraded React to v17.
 - Updated Git to 2.49.0.

### Bug Fixes 🐛
 - [Launchpad](/gitkraken-desktop/gitkraken-launchpad/) now works with GitHub users set as Enterprise Managed Users.


