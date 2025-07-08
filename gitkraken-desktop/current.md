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


