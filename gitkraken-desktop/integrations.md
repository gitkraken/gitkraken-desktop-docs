---
title: GitKraken Desktop Integrations | Connect Git & Issue Trackers
description: Learn how to integrate GitKraken Desktop with GitHub, GitLab, Bitbucket, Jira, Trello, and other tools to streamline repo access and issue tracking.
product: GitKraken Desktop
feature: Integrations
content_type: overview
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitHub Enterprise Server, GitLab, GitLab Self-Managed, Bitbucket, Bitbucket Data Center, Azure DevOps, Jira Cloud, Jira Data Center, Trello]
integrations: [GitHub, GitHub Enterprise Server, GitLab, GitLab Self-Managed, Bitbucket, Bitbucket Data Center, Azure DevOps, Jira Cloud, Jira Data Center, Trello]
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [integrations, git-hosting, issue-trackers, setup]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Integrations connect GitKraken Desktop to Git hosting services and issue trackers so you can clone repositories, manage remotes, review pull requests, and work with issues from one interface. Use this page to find the right integration for GitHub, GitLab, Bitbucket, Azure DevOps, Jira, Trello, and self-hosted services.

To set up external coding agent CLIs such as Claude Code, Codex CLI, Copilot CLI, Gemini CLI, and OpenCode, see [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

**Requirements and limits**
- Git hosting integrations: GitHub, GitHub Enterprise Server, GitLab, GitLab Self-Managed, Bitbucket, Bitbucket Data Center, and Azure DevOps
- Issue tracker integrations: Jira Cloud, Jira Data Center, Trello, GitLab Issues, GitLab Self-Managed Issues, GitHub Issues, and GitHub Enterprise Server Issues
- Community plan: Public GitHub and GitLab repositories only; some issue tracker integrations are view-only
- Self-hosted integrations: Require a paid plan; GitLab Self-Managed is available on Pro and up, while GitHub Enterprise and Bitbucket Data Center require Advanced
- Multiple profiles with separate integrations: Pro plan or higher
- Coding agent CLIs: Managed separately from Git hosting and issue tracker integrations

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/bR4pBzXPuIs?rel=0&vq=hd1080' frameborder='0' allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch an overview of how to connect integrations in GitKraken Desktop.</figcaption>
</figure>

***

## How to connect remote Git hosting integrations

GitKraken Desktop connects to these Git hosting services:

- [GitHub](/gitkraken-desktop/github-gitkraken-desktop/)
- [GitHub Enterprise Server](/gitkraken-desktop/github-enterprise/)
- [GitLab](/gitkraken-desktop/gitlab-gitkraken-desktop/)
- [GitLab Self-Managed](/gitkraken-desktop/gitlab-self-hosted/)
- [Bitbucket](/gitkraken-desktop/bitbucket)
- [Bitbucket Data Center](/gitkraken-desktop/bitbucket-data-center/)
- [Azure DevOps](/gitkraken-desktop/azure-devops/)

### How integrations connect through your GitKraken account

GitHub, GitLab, Bitbucket, Azure DevOps, Jira Cloud, and Trello connect through your GitKraken account. Sign in to GitKraken Desktop first. If you are signed out, the integration's pane in <kbd>Preferences > Integrations</kbd> asks you to sign in.

To connect one of these integrations:

1. Go to <kbd>Preferences > Integrations</kbd> and select the integration.
2. Click **Connect to** followed by the provider name, for example **Connect to GitHub**.
3. Finish connecting in your browser at gitkraken.dev.

When the integration is connected, its card reads **Connected to your GitHub integration** (or the name of your provider) and shows the account you connected. Because the connection belongs to your GitKraken account, you can also use it on your other computers and profiles. From the integration pane you can:

- Click **Manage Integrations** to see and manage your integrations on gitkraken.dev.
- Click **Disconnect from this profile** to disconnect the integration from the current profile only. It stays connected to your GitKraken account.
- Click **Connect another GitHub account** (or the name of your provider) to add a second account for the same provider.
- When you have more than 1 account for a provider, click **Use a different GitHub account for this profile** (or the name of your provider) to choose which account this profile uses.

An integration you connected with an earlier version of GitKraken Desktop keeps working and keeps its existing connection options until you disconnect it.

### What connects automatically when you sign in

When you sign in to your GitKraken account, GitKraken Desktop connects the Git hosting and issue tracker integrations already linked to that account on gitkraken.dev:

- **With 1 profile:** GitKraken Desktop connects every integration linked to your account.
- **With 2 or more profiles:** GitKraken Desktop connects only the provider you signed in with, so each profile keeps its own integrations.

GitKraken Desktop skips integrations that are already connected. On the Community plan, it does not automatically connect integrations that need a paid plan, such as Azure DevOps. While the connection runs, the **Connect to** buttons in <kbd>Preferences > Integrations</kbd> show a loading indicator.

<div class='callout callout--warning'>
  <p><strong>Note:</strong> Self-hosted server integrations require a paid plan. GitLab Self-Managed is available on Pro and up, while GitHub Enterprise and Bitbucket Data Center require Advanced.</p>
</div>

***

## How to connect issue tracker integrations

To track your development tasks, connect GitKraken Desktop to these issue trackers:

- [Jira Cloud](/gitkraken-desktop/jira/)
- [Jira Data Center](/gitkraken-desktop/jira-data-center/) <em>(Advanced plan and above)</em>
- [Trello](/gitkraken-desktop/trello/)
- [GitLab Issues](/gitkraken-desktop/gitlab-issues/)
- [GitLab Self-Managed Issues](/gitkraken-desktop/gitlab-self-managed-issues/)
- [GitHub Issues](/gitkraken-desktop/github-issues/)
- [GitHub Enterprise Server Issues](/gitkraken-desktop/github-enterprise-issues/)

<div class='callout callout--warning'>
  <p><strong>Community plan limits:</strong> You can access only public repositories on GitHub and GitLab. Jira Cloud, GitHub Enterprise, GitLab Self-Managed, and Trello are view-only.</p>
</div>

***

## What you can do with integrations

By connecting integrations, you can:

- Clone and open remote repositories
- View and update issues in GitKraken Desktop
- Access remote branches and pull requests
- Sync commits and metadata with issue trackers

***

## How plan requirements vary by integration

| Feature Type | Integration | Minimum Plan |
|--------------|-------------|----------------|
| Self-Hosted Git Servers | GitLab Self-Managed | Pro |
| Self-Hosted Git Servers | GitHub Enterprise, Bitbucket Data Center | Advanced |
| Issue Trackers with Write Access | Jira Cloud, Trello, etc. | Pro or Advanced |
| Multiple Profiles with Separate Integrations | All | Pro or higher |

For more details, see the [GitKraken pricing plans](https://www.gitkraken.com/pricing).
