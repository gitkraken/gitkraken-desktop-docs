---
title: GitKraken Desktop Preferences | Customize Settings & Workflow
description: Find where each GitKraken Desktop setting lives in Preferences, including themes, integrations, profiles, commit signing, notifications, and terminal settings.
product: GitKraken Desktop
feature: Preferences
content_type: reference
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [preferences, settings, ssh, integrations, profiles]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to find where a setting lives in GitKraken Desktop Preferences and what each Preferences section controls, before you change your workflow or environment.

**Requirements and limits**
- Scope: Preferences overview for app-wide, profile-specific, and repository-specific settings
- Access point: Gear icon in the top-right corner of GitKraken Desktop
- Profile behavior: Preferences are stored per profile, so switching profiles changes integrations and UI configuration
- Repo-specific settings: Some settings apply only to the currently open repository
- Plan-gated sections: Organization settings, GitKraken AI, and some notification controls depend on plan level
- Detailed workflows: Follow the linked feature pages for the steps and limits of each feature

***

## Quick Start


- **General**: Set auto-fetch intervals, conflict detection behavior, Commit Graph limits, and tab retention.
- **Profiles**: Create and switch between profiles to separate Git identities, integrations, and tab sets.
- **SSH and Integrations**: Connect to GitHub, GitLab, Bitbucket, Azure DevOps, Jira, Trello, and more.
- **GitKraken AI**: Enable AI-assisted commit messages and PR descriptions (Pro plan and above).
- **External Tools**: Set your preferred editor, diff tool, merge tool, external terminal, and custom coding agent commands.
- **UI Customization**: Change themes, date formats, avatar display, and Commit Graph metadata.
- **Commit Signing**: Enable GPG signing for verified commits.
- **Experimental**: Try preview features such as Git Executable and Cloud Patches.
- **Repo-Specific Preferences**: Configure encoding, Gitflow, hooks, LFS, issues, Team View, and agent setup commands per repository.

Each profile has its own preferences, so switching profiles switches integrations and UI options to that profile's configuration.

<figure>
  <img src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop window with the gear icon that opens Preferences highlighted.">
  <figcaption style="text-align:center; color:#888">Access Preferences from the gear icon in the top right corner</figcaption>
</figure>

***

## How organization settings work

This section is labeled with your organization's name and shows its members and teams. Owners and Admins can:
- Manage member roles
- Invite users and assign licenses
- Create and manage teams

<div class='callout callout--warning'>
  <p><strong>Note:</strong> Organization settings are available on the <strong>Pro</strong> plan and above.</p>
</div>

***

## How General preferences work

Configure app-wide behavior such as auto-fetch, conflict detection, and Commit Graph settings.

| Setting | What it controls |
| --- | --- |
| **Auto-Fetch Interval** | Sets how often GitKraken Desktop fetches, from 0 to 60 minutes. 0 turns off auto-fetch. |
| **Auto-Prune** | Removes stale remote-tracking references. |
| **Enable proactive conflict detection with target branch** | GitKraken Desktop checks for conflicts with the base branch. |
| **Keep submodules up to date** | Updates submodules automatically after Git actions. |
| **Default Branch Name** | Sets the branch name for new repositories (default is `main`). |
| **Delete ".orig" files after merging** | Controls cleanup of merge backup files. |
| **Show All Commits in Graph** | Shows every commit in the graph. This can slow GitKraken Desktop down on large repositories. |
| **Initial Commits in Graph** | Sets the number of commits the graph shows at first (minimum 500). |
| **Lazy Load Commits in Graph** | Loads more commits only as needed. |
| **Remember tabs** | Saves open tabs and profile context between sessions. |
| **Longpaths** and **AutoCRLF** | Windows-only settings tied to your global `.gitconfig`. |
| **Use extended logging in activity log** | Records more detailed activity logs, which you can get from <kbd>Help > Support Logs</kbd>. |
| **Forget all Usernames and Passwords** | Clears stored usernames and passwords. |
| **Share my current branch status with my team** | Shares your work in progress with teammates in [Team View](/gitkraken-desktop/team-view/). |

On Windows, if your global `.gitconfig` has no `core.autocrlf` value, GitKraken Desktop's bundled Git uses the line-ending setting of your installed Git for Windows. If Git for Windows is not installed, it uses `core.autocrlf=true`. The Activity Log shows which setting applies. To override it, change **AutoCRLF**: this sets the global value, which takes precedence.

***

## How profile preferences work

Each profile keeps its own settings, tabs, and integrations, so you can keep separate setups when you work with more than one account.

See [how to create and switch profiles](/start-here/profiles).

***

## How SSH and integration preferences work

Control access and connections to remote repositories:

- [SSH settings](/gitkraken-desktop/authentication/#ssh)
- Git hosting integrations such as GitHub, GitLab, Bitbucket, and Azure DevOps
- Issue tracker integrations such as Jira and Trello

***

## How GitKraken AI preferences work

<div class='callout callout--warning'>
  <p>This feature is available for <strong>Pro</strong> plans or higher.</p>
</div>

Use [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai) to automate repetitive Git tasks.

The **Usage Details** card shows how many AI credits you have used this week and when your credits reset. Below it, the **Shared Organization Pool** meter shows your organization's credits this week, split into **Your usage**, **Rest of organization**, and **Remaining**.

When you reach your weekly credit limit, the card shows **You've reached your weekly credit limit**. GitKraken AI then draws from your organization's shared credit pool, so you can keep working. Every member of the organization can use the shared pool, and it resets weekly along with your personal limit.

- Organization Owners and Admins on a paid plan can click **Get more AI credits** to add credits.
- Users on a trial can click **Upgrade to get more credits**.

<div class='callout callout--basic'>
  <p>See the <a href="https://help.gitkraken.com/general/gitkraken-ai-faq/">GitKraken AI FAQ</a> for common questions.</p>
</div>

***

## How external tool preferences work

Configure your preferred editors, terminals, coding agent commands, and diff/merge tools.

- **External Merge Tool**: [View supported tools](/working-with-repositories/branching-and-merging/#external-merge-tools)
- **External Diff Tool**: [View supported tools](/working-with-commits/diff/#external-diff-tools)
- **External Editor**: Choose from VS Code, Atom, Sublime, IntelliJ, or custom path
- **External Terminal**: The terminal that opens from <kbd>File > Open External Terminal</kbd> or <kbd>Alt</kbd>/<kbd>Option</kbd> + <kbd>T</kbd>. For a custom terminal, set **Terminal Executable** and **Terminal Arguments**
- **Coding Agent**: Configure custom commands or arguments used when GitKraken Desktop starts a coding agent session. GitKraken Desktop detects the supported coding agent CLIs installed on your machine, such as Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI, and OpenCode. You choose the coding agent for a session in the **Start an Agent Session** modal. In on-premises environments, available options depend on what your organization allows and can reach. See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).
- **Agent Status Integrations**: Install, reinstall, or uninstall the plugins that let Claude Code, Codex CLI, Copilot CLI, and OpenCode report live session status in the Agents view. See [How to manage agent status plugins and hooks](/gitkraken-desktop/agents/#how-to-manage-agent-status-plugins-and-hooks).

<div class='callout callout--warning'>
  <p><strong>macOS Note:</strong> Use the executable file, not the .app, when selecting a custom editor.</p>
</div>

***

## How notification preferences work

Control product and marketing messages:
- **Enable Desktop Notifications**
- **Receive Marketing Notifications**

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Only Pro, Advanced, Business, and Enterprise users can turn off marketing notifications.</p>
</div>

***

## How UI customization preferences work

Change the theme and how the Commit Graph looks:
- [Themes](/start-here/themes)
- Notification location
- Date/time locale and formatting
- Author initials or avatars
- Graph metadata, such as branches, tags, author, commit message, and SHA
- **Hide Launchpad in status bar**
- **Show Agents view in left panel**. See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).
- **Automatically group worktree tabs together**: On by default. Groups the tabs of a repository and its worktrees in the tab bar. See [Worktree tab groups](/gitkraken-desktop/interface/#worktree-tab-groups).

To switch between the standard Left Panel and the Agents view, go to <kbd>Preferences > UI Customization</kbd> and enable **Show Agents view in left panel**.

<figure>
  <img src="/wp-content/uploads/toggle-agents-view-preferences.png" class="help-center-img img-bordered" alt="GitKraken Desktop Preferences highlighting the Show Agents view in left panel setting that controls whether the List and Agents toggle appears in the Left Panel.">
  <figcaption style="text-align:center; color:#888">Enable <code>Show Agents view in left panel</code> to display the <code>List | Agents</code> toggle</figcaption>
</figure>

***

## How commit signing preferences work

Enable and configure [GPG signing](/git-workflows-and-extensions/commit-signing-with-gpg/#configure-gpg-in-gitkraken) for commit verification.

***

## How editor preferences work

Customize the code editor and diff viewer:
- Font, size, tab spacing
- EOL characters
- Syntax highlighting
- Line numbers and word wrap

***

## How in-app terminal preferences work

Adjust the appearance and behavior of the in-app terminal:
- Font, size, line height, cursor
- **Dim terminal when unfocused**: On by default. Fades the terminal output while you work elsewhere in the app
- Autocomplete behavior
- **Default In-App Terminal** on Windows

For worktree-specific terminal sessions and manual coding agent workflows, see [GitKraken Terminal Guide](/gitkraken-desktop/terminal/).

***

## How experimental preferences work

Preview [Experimental Features](/gitkraken-desktop/experimental-features):
- **Use Git Executable**: Run Git operations with a Git executable instead of the NodeGit library
- Cloud Patches

***

## How repo-specific preferences work

These settings apply only to the open repository, so you can configure each repository differently:

- [Encoding](/gitkraken-desktop/editing-files/#encoding)
- [Gitflow](/gitkraken-desktop/git-flow/)
- [Git Hooks](/gitkraken-desktop/githooks/)
- [LFS](/gitkraken-desktop/git-lfs/)
- [Commit settings](/working-with-commits/commits/)
- [Issues](/gitkraken-desktop/jira/)
- [Team View](/gitkraken-desktop/team-view/)
- [Submodules](/gitkraken-desktop/submodules/#keep-submodules-up-to-date)
- [Agents](/gitkraken-desktop/agents/#how-to-configure-setup-commands):
  - **Show worktree WIP nodes in the graph** (on by default) shows a WIP row in the Commit Graph for every other worktree with uncommitted changes or an active agent session
  - **Setup commands**, such as install scripts or build steps, run when a new agent session starts in a worktree
