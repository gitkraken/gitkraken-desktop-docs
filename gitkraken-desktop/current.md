---
title: GitKraken Desktop Release Notes
description: View the latest features, improvements, and fixes shipping in the current version of GitKraken Desktop.
product: GitKraken Desktop
feature: Release Notes
content_type: release-notes
audience: all
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-05
llms_include: true
tags: [release-notes, changelog, upgrades, version-history]
og_image: /img/GitKrakenClient-Hero.png
taxonomy:
    category: gitkraken-desktop
---

This release notes page tracks what's new and changing in the current version of GitKraken Desktop, including new features, improvements, bug fixes, and deprecations. Use it to see what shipped in the most recent release, confirm when a capability became available, or review changes before upgrading.

**Requirements and limits**
- This page covers the current major version of GitKraken Desktop. For earlier releases, see the archived version pages ([Version 11](/gitkraken-desktop/11x/), [Version 10](/gitkraken-desktop/10x/), [Version 9](/gitkraken-desktop/9x/), and earlier).
- Each entry applies only to the specific release listed under its version heading.
- Use the current feature documentation for step-by-step guidance and the release notes to confirm version timing.

<a href="https://www.gitkraken.com/download?product=gitkraken&source=help_center" target="_blank" class="button button--basic ">Download Current Version Now</a>

Check out our [GitKraken Roadmap](https://www.gitkraken.com/git-client/roadmap?product=gitkraken&source=help_center) to see what we’re working on.

***
<a id="v12-1-2"></a>
## Version 12.1.2

<kbd>Tuesday, May 19th, 2026</kbd>

### Improvements 🙌
 - **Agent Sessions view:**
   - Added sort and filter controls to the worktree list so you can quickly focus on the sessions that matter. Narrow down by status or branch to keep large groups of parallel agent sessions manageable at a glance.
 - **GitHub Pull Requests:**
   - Merged PRs now surface as a pill on the Toolbar, Commit Details panel, and worktree cards for their associated branches, giving you instant confirmation that a branch's work has shipped, so you know when it's safe to clean up local branches and worktrees.

### Bug Fixes 🐛
 - Fixed an issue where extensionless image files were not correctly identified in commit diffs, showing them as editable.
 - Fixed repeated "Staging paths failed" errors when rebasing across a file/directory name collision.
 - Fixed an issue where profile and repository management row menus could be visually cut off.

***
<a id="v12-1-1"></a>
## Version 12.1.1

<kbd>Thursday, May 7th, 2026</kbd>

### Improvements 🙌
 - **Worktrees:**
   - You can now remove the active worktree directly; GitKraken will switch back to the main worktree before removing it.

### Bug Fixes 🐛
 - Fixed an issue where GitKraken Desktop could get trapped on the splash screen and fail to start.

***
<a id="v12-1-0"></a>
## Version 12.1.0

<kbd>Tuesday, May 5th, 2026</kbd>

### Improvements 🙌
 - **Worktrees:**
   - New worktrees and agent sessions now inherit view settings (hidden refs, hidden remotes, soloed refs/remotes, and collapsed folders/remotes) from the source repository, so you no longer need to re-hide branches and remotes after creating a worktree.
   - Added a "Remove worktree and delete branch" action to the worktree context menu for one-step cleanup of worktrees and their associated branches.
 - **Agent Sessions view:**
   - Added a three-dot action menu to worktree cards in the Agents Left Panel view.
   - You can now start an agent session directly from an existing worktree's context menu.
   - Refined the New Agent Session form so options are always visible and the branch, coding agent, and Start Session controls are easier to use.
   - The base branch selector in the New Agent Session form is now searchable.
   - A new "Running" status appears when an agent session starts (Claude Code may show a different status if hooks are enabled).
   - Added visual feedback on worktrees in the Agents view to show a worktree deletion is in progress.
 - **Command Line:**
   - You can now open a repository by passing its path directly as an argument (e.g. `gitkraken .` or `gitkraken /path/to/repo`) without needing the `--path` flag.
 - **Review GitHub Pull Requests on GitKraken.dev:**
   - Added a "Review on GitKraken.dev" button in the GitHub Pull Request view to open a PR with GitKraken Code Review. Review PRs faster with cleaner diffs, AI-generated suggestions, and integrated chat — approve and comment just like on GitHub.
 - **Terminal:**
   - The embedded terminal now resizes smoothly when adjusting surrounding panels.
   - You can now minimize the integrated terminal, keeping the terminal panel header visible.
   - You can now kill terminal sessions directly from the trash icon in the terminal panel header.
 - Added zoom levels 140%, 150%, 175%, and 200% to the standard zoom options in the status bar.
 - Upgraded Electron to v41.

### Bug Fixes 🐛
 - Fixed an issue where Bitbucket Cloud repositories were not listed in the clone dialog due to a deprecated API endpoint removal.
 - Fixed an issue where active agent sessions could stop showing the "Needs response" status while waiting for user input.
 - Fixed an issue when selecting an old commit in the file history view that made the application crash.
 - Fixed an issue where the interactive rebase editor did not show a scrollbar when needed.
 - Fixed an issue where diffs were rendered with all lines shown as additions when `diff.noprefix = true` was set in the git config.

***
<a id="v12-0-1"></a>
## Version 12.0.1

<kbd>Saturday, April 18th, 2026</kbd>

### Improvements 🙌
 - You can now uninstall and reinstall Claude Code hooks used to display live agent status in the Agents Session View from *Preferences > External Tools*.

### Bug Fixes 🐛
 - GitKraken will no longer attempt to automatically install Claude Code hooks after they are removed.
 - Fixed an issue in 12.0.0 where GitKraken On-Premise and Standalone clients were attempting to send telemetry via the GitKraken CLI.

***
<a id="v12-0-0"></a>
## Version 12.0.0

<kbd>Tuesday, April 14th, 2026</kbd>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/iwVvE0PICqY?rel=0&vq=hd1080" frameborder="0" allowfullscreen></iframe>
</div>

_"A special agent with a license to commit."_

### New ✨
 - **Agent Sessions View - Manage, create, and monitor parallel AI agent sessions from a single panel:**
   - The new Agent Sessions View in the Left Panel gives you a unified dashboard for your worktrees and active agent sessions. Each worktree is represented as a card showing its branch, uncommited changes, ahead/behind state, and associated PRs so you can monitor multiple agents at a glance.
     - If using Claude Code, the associated agent's status will show in the card so you know when it's working, waiting for input, or errors.
   - The "New Agent Session" action creates a worktree, runs your configured setup commands, and launches your coding agent in one step — making it easy to start a parallel task in a new, isolated environment.
     - Add setup commands in *Preferences > Agents* to configure per-worktree setup commands (dependency installs, build steps, env file copies) so new agent environments are ready to go automatically.
     - Configure your preferred coding agent in the inline options menu when creating a new agent session, or go to *Preferences > External Tools* to set your agent and pass custom CLI arguments when starting agent sessions. This setting currently supports Claude Code, Codex CLI, OpenCode, Copilot CLI, and Gemini CLI (auto-detected based on installation).
   - Added a setting in *Preferences > UI Customization* to hide the Agent view toggle in the Left Panel.
 - **Terminal - An upgraded terminal that keeps your entire workflow in one window:**
   - Added multi-session support to the embedded terminal, allowing independent terminal sessions per worktree in a single tab. Switching worktrees will switch to the relevant terminal session automatically.
   - Added drag-and-drop support for files and text into the terminal.
   - Updated default terminal color theme for improved readability and contrast.
   - Upgraded the terminal engine (xterm.js) from v4 to v6, bringing a handful of major improvements:
     - Significantly faster rendering with optimized WebGL and DOM renderers, reducing main-thread blocking during buffer resizing.
     - Improved glyph rendering with multi-page texture atlas support, removing the previous hard cap on glyph storage.
     - Better Unicode and emoji rendering, including fixes for clipped italic emoji and wide character handling.
     - Added support for ligatures, additional Powerline glyphs, and new underline styles (dashed, dotted, overline).
     - Synchronized output to prevent flicker during rapid terminal updates.


### Improvements 🙌
 - **GitKraken AI:**
   - Added support for Claude Sonnet 4.6 and Claude Opus 4.6 when using your own API key.
   - Added support for Google Gemini 3.1 Pro (Preview) when using your own API key.
   - Removed deprecated Claude 3.x models (Claude 3.7 Sonnet, Claude 3.5 Sonnet, Claude 3.5 Haiku, Claude 3 Haiku, Claude 3 Opus) from AI preferences. Users previously on these models will be automatically migrated to Claude 4.6 Sonnet.
 - **Shallow Clone Settings:**
   - You can now set shallow clone options when adding a remote to a repository which is shallow-cloned.
 - **Repository Management Tab:**
   - Added resizable columns for repo name, remote, and branch in the Repo Management tab. Column widths persist across app restarts.
 - **Command Palette:**
   - Added all detected IDEs as "Open in…" options in the Command Palette (<kbd>Cmd/Ctrl + P</kbd>).
 - **Worktrees:** 
   - Added an option to open a worktree in a new tab from the worktree context menu and the post-creation prompt.


### Bug Fixes 🐛
 - Fixed visual issues with the terminal panel not properly resizing to fill the available space.
 - Fixed an issue where the content of stashes created from the command line with unstaged changes were not displayed in the right panel.
 - Fixed an issue where LFS file tags were not shown for files located in subdirectories.
 - Bitbucket users can once again assign multiple reviewers when creating a pull request.
 - Fixed an issue where commit diffs appeared empty when the commit contained only whitespace changes and "Ignore Leading/Trailing Whitespace" was enabled.
 - Fixed an issue where typechanged files were missing their diff icon and not appearing in the staged/unstaged area.
 - Fixed an issue where the terminal panel would jump to the top of the viewport when switching repositories or worktrees.
 - Added visual feedback and prevented duplicate actions when deleting a worktree from the left panel.
 - Fixed an issue where columns in the 'All Repositories' group on Repo Management were horizontally misaligned with other groups.
 - Fixed visual issues with the terminal panel styling and padding.
 - Fixed an issue where committed file diffs showed all lines as additions when `color.ui = always` was set in the git config.


### Known Issues
 - Users running GitKraken Desktop in WSL may experience issues when starting agent sessions. Windows-installed coding agents can take precedence over WSL-installed ones, causing the agent to fail to run.
 - When cloning Bitbucket repositories, the repository list may not appear in the Clone modal due to a Bitbucket API deprecation. As a workaround, you can clone the repository by pasting its URL directly, or browse and clone repositories from the Repository Management tab.

***
