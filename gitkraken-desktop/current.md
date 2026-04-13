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
last_verified: 2026-04
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
<a id="v12-0-0"></a>
## Version 12.0.0

<kbd>Tuesday, April 14th, 2026</kbd>

_TODO: add tagline._

### New ✨
 - **GitKraken AI:**
   - Added Claude Sonnet 4.6 and Claude Opus 4.6 models to Anthropic BYOK.
   - Added support for Google Gemini 3.1 Pro (Preview) when using your own API key.
 - **Repo Management:**
   - Added resizable columns for repo name, remote, and branch in the Repo Management tab. Column widths persist across app restarts.
 - **Worktrees:**
   - Added an Agent sessions view in the left panel for browsing worktrees with branch and status information.
   - Added associated pull request chip to worktree cards, allowing quick access to PRs directly from the Agent sessions view.
   - Added an option to open a worktree in a new tab from the worktree context menu.
   - Added an "Agents" section in the Preferences to configure setup commands for agent worktrees.
   - Added a "Coding Agent" setting in Preferences > External Tools, with support for Claude Code, Codex CLI, OpenCode, Copilot CLI, and Gemini CLI (auto-detected based on installation), and an option to pass custom CLI arguments when starting agent sessions.
   - Added a "New Agent Session" action in the Agent sessions panel that creates a worktree, switches to it, and launches the configured coding agent in the terminal.
 - **Terminal:**
   - Added multi-session support to the embedded terminal, allowing independent terminal sessions per worktree in a single tab.
   - Added drag-and-drop support for files and text into the terminal.
 - **Command Palette:**
   - Added all detected IDEs as "Open in…" options in the Command Palette (<kbd>Cmd/Ctrl + P</kbd>).

### Improvements 🙌
 - **GitKraken AI:**
   - Removed deprecated Claude 3.x models (Claude 3.7 Sonnet, Claude 3.5 Sonnet, Claude 3.5 Haiku, Claude 3 Haiku, Claude 3 Opus) from AI preferences. Users previously on these models will be automatically migrated to Claude 4.6 Sonnet.
 - **Left Panel:**
   - Added a preference to hide the Agent sessions toggle in the left panel.
 - **Terminal:**
   - Upgraded the terminal engine (xterm.js) from v4 to v6, bringing major improvements:
     - Significantly faster rendering with optimized WebGL and DOM renderers, reducing main-thread blocking during buffer resizing.
     - Improved glyph rendering with multi-page texture atlas support, removing the previous hard cap on glyph storage.
     - Better Unicode and emoji rendering, including fixes for clipped italic emoji and wide character handling.
     - Added support for ligatures, additional Powerline glyphs, and new underline styles (dashed, dotted, overline).
     - Synchronized output mode (DEC 2026) to prevent flicker during rapid terminal updates.
   - Updated default terminal color theme for improved readability and contrast.
 - **Shallow Clone Settings:**
   - You can now set shallow clone options when adding a remote to a repository which is shallow-cloned.

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
 - Fixed an issue where committed file diffs showed all lines as additions when color.ui = always was set in the git config.
