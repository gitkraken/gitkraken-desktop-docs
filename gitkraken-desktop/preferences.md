---
title: GitKraken Desktop Preferences | Customize Settings & Workflow
description: Explore GitKraken Desktop’s Preferences to control themes, integrations, profiles, commit signing, notifications, terminal settings, and more.
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
last_verified: 2026-03
llms_include: true
tags: [preferences, settings, ssh, integrations, profiles]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to understand what each major Preferences section controls in GitKraken Desktop, including profiles, integrations, AI settings, external tools, commit signing, terminal behavior, and repository-specific options. Start here when you need to know where a setting lives before changing your workflow or environment.

**Requirements and limits**
- Scope: Preferences overview for app-wide, profile-specific, and repository-specific settings
- Access point: Gear icon in the top-right corner of GitKraken Desktop
- Profile behavior: Preferences are stored per profile, so switching profiles changes integrations and UI configuration
- Repo-specific settings: Some settings apply only to the currently open repository
- Plan-gated sections: Organization settings, GitKraken AI, and some notification controls depend on plan level
- Use this page for setting location and scope; follow linked feature pages for detailed workflow constraints

***

## Quick Start


- **General**: Set auto-fetch intervals, conflict detection behavior, commit graph limits, and tab retention.
- **Profiles**: Create and switch between profiles to separate Git identities, integrations, and tab sets.
- **SSH and Integrations**: Connect to GitHub, GitLab, Bitbucket, Azure DevOps, Jira, Trello, and more.
- **GitKraken AI**: Enable AI-assisted commit messages and PR descriptions (Pro plan and above).
- **External Tools**: Set your preferred editor, diff tool, merge tool, and default terminal.
- **UI Customization**: Change themes, date formats, avatar display, and commit graph metadata.
- **Commit Signing**: Enable GPG signing for verified commits.
- **Experimental**: Try preview features such as the Git binary executor.
- **Repo-Specific Preferences**: Configure encoding, Gitflow, hooks, LFS, issues, and Team View per repository.

Preferences are stored per profile, so switching profiles resets integrations and UI options to that profile's configuration.

<figure>
  <img src="/wp-content/uploads/preferences@2x.png" class="help-center-img img-bordered" alt="Highlighting the gear icon in GitKraken Desktop to explain where users access Preferences, enabling customization of integrations, UI and more.">
  <figcaption style="text-align:center; color:#888">Access Preferences from the gear icon in the top right corner</figcaption>
</figure>

***

## How organization settings work

This section is labeled with your organization's name. It shows members and teams, and allows Owners and Admins to:
- Manage member roles
- Invite users and assign licenses
- Create and manage teams

<div class='callout callout--warning'>
  <p><strong>Note:</strong> Organization settings are available on the <strong>Pro</strong> plan and above.</p>
</div>

***

## How General preferences work

Configure app-wide behavior like auto-fetch, conflict detection, and commit graph settings.

| Setting | What it controls |
| --- | --- |
| **Auto-Fetch** | Set an interval (0–60 minutes); 0 disables auto-fetch. |
| **Auto-Prune** | Removes stale remote-tracking references. |
| **Automatic Conflict Detection** | GitKraken monitors for base branch conflicts. |
| **Keep Submodules Up to Date** | Auto-update submodules after Git actions. |
| **Default Branch Name** | Used when initializing new repos (default is `main`). |
| **Delete ".orig" Files** | Control cleanup of merge backup files. |
| **Show All Commits in Graph** | May affect performance on large repos. |
| **Initial Commits in Graph** | Define max visible commits (minimum: 500). |
| **Lazy Load Commits** | Loads more commits only as needed. |
| **Remember Tabs** | Saves open tabs and profile context between sessions. |
| **Longpaths / AutoCRLF** | Windows-only settings tied to global `.gitconfig`. |
| **Extended Logging** | Toggle detailed activity logs from <kbd>Help > Support Logs</kbd>. |
| **Forget All Credentials** | Clears stored usernames and passwords. |
| **Share Work-in-Progress** | Enables visibility for teammates via the [Team View](/gitkraken-desktop/team-view/). |

***

## How profile preferences work

Store unique settings, tabs, and integrations per context. Useful for multi-account workflows.

[Learn more about Profiles](/start-here/profiles)

***

## How SSH and integration preferences work

Control access and connections to remote repositories:

- [SSH settings](/gitkraken-desktop/authentication/#ssh)
- Git hosting integrations for GitHub, GitLab, Bitbucket, Azure DevOps, etc.
- Issue tracker integrations like Jira and Trello

***

## How GitKraken AI preferences work

<div class='callout callout--warning'>
  <p>This feature is available for <strong>Pro</strong> plans or higher.</p>
</div>

Let [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai) automate repetitive Git tasks to improve your efficiency.

<div class='callout callout--basic'>
  <p>See the <a href="https://help.gitkraken.com/general/gitkraken-ai-faq/">GitKraken AI FAQ</a> for common questions.</p>
</div>

***

## How external tool preferences work

Configure your preferred editors, terminals, and diff/merge tools.

- **External Merge Tool**: [View supported tools](/working-with-repositories/branching-and-merging/#external-merge-tools)
- **External Diff Tool**: [View supported tools](/working-with-commits/diff/#external-diff-tools)
- **External Editor**: Choose from VS Code, Atom, Sublime, IntelliJ, or custom path
- **Default Terminal**: Launch from <kbd>File > Open Terminal</kbd> or <kbd>Alt</kbd>/<kbd>Option</kbd> + <kbd>T</kbd>
- **Use Custom Terminal Command**: Example for PowerShell: `start "" "C:\Program Files\PowerShell\7\pwsh.exe" -noexit -command "cd %d"`

<div class='callout callout--warning'>
  <p><strong>macOS Note:</strong> Use the executable file, not the .app, when selecting a custom editor.</p>
</div>

***

## How notification preferences work

Control product and marketing messages:
- Enable Desktop Notifications
- Receive Marketing and Help Notifications

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Marketing notifications can be disabled only by Pro, Advanced, Business, and Enterprise users.</p>
</div>

***

## How UI customization preferences work

Visual preferences for theming and commit graph display:
- [Themes](/start-here/themes)
- Notification location
- Date/time locale and formatting
- Author initials vs. avatars
- Graph metadata: branches, tags, author, commit message, SHA, etc.
- Hide Launchpad from the status bar

***

## How commit signing preferences work

Enable and configure [GPG signing](/git-workflows-and-extensions/commit-signing-with-gpg/#configure-gpg-in-gitkraken) for commit verification.

***

## How editor preferences work

Customize code and diff viewer:
- Font, size, tab spacing
- EOL characters
- Syntax highlighting
- Line numbers and word wrap

***

## How in-app terminal preferences work

Adjust the appearance and behavior of GitKraken’s terminal:
- Font, size, line height, cursor
- Autocomplete behavior
- Default terminal for Windows

***

## How experimental preferences work

Preview [Experimental Features](/gitkraken-desktop/experimental-features):
- Switch from NodeGit to Git binary (limited support)
- AI commit message generation

***

## How repo-specific preferences work

These apply only to the open repository:

- [Encoding](/gitkraken-desktop/editing-files/#encoding)
- [Gitflow](/gitkraken-desktop/git-flow/)
- [Git Hooks](/gitkraken-desktop/githooks/)
- [LFS](/gitkraken-desktop/git-lfs/)
- [Commit settings](/working-with-commits/commits/)
- [Issues](/gitkraken-desktop/jira/)
- [Team View](/gitkraken-desktop/team-view/)
- [Submodules](/gitkraken-desktop/submodules/#keep-submodules-up-to-date)

You can configure these uniquely per repository.
