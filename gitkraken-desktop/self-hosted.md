---
title: Set Up GitKraken Self-Hosted Server (On-Premise)
description: Learn how to install and configure GitKraken On-Premise Self-Hosted Server, including system requirements, supported OS versions, and benefits for secure environments.
product: GitKraken Self-Hosted
feature: Self-Hosted Server Setup
content_type: overview
audience: enterprise-admin
plan_required: Enterprise
os_support: [server-linux]
git_hosts: [n/a]
integrations: []
hosted_variant: self-hosted
status: GA
last_verified: 2026-11
llms_include: true
tags: [self-hosted, on-premise, setup, enterprise, server]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "on-premise"
    nav_label: "On-Premise Self-Hosted Server"
    nav_order: 10
    nav_parent: "on-premise"
    page_type: "content"
---
<kbd>Last updated: November 2026</kbd>

Use this page to understand what GitKraken On-Premise Self-Hosted Server is, when to choose it, and what infrastructure it requires before installation.

**Requirements and limits**
- Product scope: GitKraken On-Premise Self-Hosted Server
- Environment fit: Internal-network, offline, or air-gapped deployments
- Infrastructure model: Lightweight Linux server or VM running Docker containers
- Minimum specs: 2 CPU cores, 4 GB RAM, 5 GB disk space
- Supported OS families: CentOS 7, selected Ubuntu versions, and RHEL 7
- Commercial note: Self-Hosted and Serverless on-premise offerings are sold separately from standard subscriptions and from each other

## Overview

**GitKraken On-Premise Self-Hosted Server** is a version of GitKraken Desktop that operates entirely within your internal network. Also referred to as *GitKraken Enterprise Self-Hosted*, *Enterprise On-Premise Server*, or *Self-Hosted*, it lets users authenticate and work without external internet access.

### Key benefits

- Operates without internet connectivity, for air-gapped or secure environments
- Supports email-based and LDAP authentication
- Full control over version management

<figure class='figure center'>
  <img alt="Manage users and settings within your private GitKraken instance" src='/wp-content/uploads/manage-users@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Manage users and settings within your private GitKraken instance.</figcaption>
</figure>

> **Note:** GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately from standard subscriptions. To purchase, see the <a href='https://www.gitkraken.com/git-client/on-premise-pricing?_gl=1*vtr4xk*_up*MQ..*_gs*MQ..&gclid=Cj0KCQjwqIm_BhDnARIsAKBYcmv98H0EKgytPnuCPuTqdL2vy4GQaCsizBMO9m8mz2n1hMMXO3AAw7YaAiyKEALw_wcB?source=help_center&product=gitkraken'>On-Premise Pricing</a> page.

## Feature support

GitKraken On-Premise Self-Hosted Server uses the same GitKraken Desktop client as GitKraken On-Premise Serverless, with the same features. The difference between Self-Hosted and Serverless is the deployment and license model, not the feature set.

In Self-Hosted, a central server inside your network handles authentication and license management, so your organization controls which client version users get and how they authenticate. Features that require connectivity to GitKraken cloud services are not available in either on-premises variant.

### What is included

The following feature categories are fully supported:

| Category | Included | Notes |
| --- | --- | --- |
| **Core Git client** | All standard Git operations, including commits, branches, merges, rebases, diffs, stashing, tagging, interactive rebase, cherry pick (including multi-commit interactive cherry pick), worktrees, shallow clone, and undo or redo of rebase and cherry pick operations. | |
| **Agents view and coding agent session workflows** | The Agents view and worktree-based coding agent session workflows are available in the on-premises GitKraken Desktop client. | Available coding agents depend on your security policy, internal approvals, client version, and local environment. OpenCode and Gemini CLI can run fully air-gapped against an internal model endpoint; Claude Code, Codex CLI, Copilot CLI, and Cursor CLI are supported when internally permitted and reachable. |
| **Embedded terminal for manual coding agent workflows** | You can run coding agents manually in the embedded terminal, including agents that GitKraken Desktop does not explicitly integrate with. | See [GitKraken Terminal Guide](/gitkraken-desktop/terminal/). |
| **Launchpad** | Track pull requests and issues in a single view and filter by repository, branch, milestone, or sprint. Launchpad works with the following on-premises integrations: GitHub Enterprise Server, GitLab Self-Managed, Bitbucket Server and Data Center, Azure DevOps Server, and Jira Data Center. | For a description of the differences between cloud and on-premises Launchpad, see [How On-Premise Launchpad differs from Cloud Launchpad](/gitkraken-desktop/gitkraken-launchpad/#how-on-premise-launchpad-differs-from-cloud-launchpad). |
| **Local Workspaces** | Organize multiple local Git repositories in one view. You can see the branch status of each repository and run multi-repository actions, such as fetch and pull, from a single place. | Cloud Workspaces are not available. |
| **Conflict detection** | GitKraken Desktop detects potential conflicts with your target branch before you reach the merge step and alerts you when your checked-out branch has diverged from its pull request target. | |
| **GitKraken AI (bring your own key)** | All GitKraken AI features are available when you configure a Custom URL that points to a private or internal AI endpoint. | For setup instructions, see [GitKraken AI in Self-Hosted Server](#gitkraken-ai-in-self-hosted-server). |
| **ARM builds** | A native ARM installer is available for machines with ARM architecture. | |
| **Centralized version management** | Because the GitKraken Desktop client connects to your internal server, your admin controls which client version users get, so you can test and roll out updates on your own schedule. | |
| **Authentication** | Users authenticate through your Self-Hosted Server using email-based or LDAP authentication. No external GitKraken cloud account is required. | |
| **On-premises integrations** | GitKraken Self-Hosted supports integrations with self-hosted Git hosting services and issue trackers. | For the full list, see [Supported on-premises integrations](#supported-on-premises-integrations). |

### What is not available

The following features require connectivity to GitKraken cloud services (`gitkraken.dev`) or to external cloud hosting providers and are not available in Self-Hosted Server:

- Cloud Workspaces and features that depend on them, including Launchpad Team View, Launchpad Saved Views, and Launchpad snooze and pin
- GitKraken Insights
- GitKraken Code Review, including the **Review on GitKraken.dev** and **Review Pull Request** actions for pull requests
- GitKraken AI using the default GitKraken-hosted provider
- Cloud Patch sharing
- Org Member conflict detection
- Integrations with cloud-hosted services: GitHub.com, GitLab.com, Bitbucket.org, Azure DevOps cloud, Jira Cloud, and Trello

Local GitKraken Desktop workflows such as worktrees, the Agents view, and terminal-based coding agent workflows remain available unless they depend on a cloud-only or otherwise unsupported external service. For coding agents, availability depends on what your organization approves and what services are reachable from the environment.

### Feature support table

| Feature | Supported | Notes |
|---|---|---|
| Core Git client (commits, branches, merges, rebase, diff, stash) | Yes | |
| Interactive Rebase | Yes | |
| Multi-commit Cherry Pick | Yes | |
| Worktrees | Yes | Requires client version 10.5.0 or later |
| Agents view and coding agent session workflows | Yes | Available in the on-premises GitKraken Desktop client; available coding agents depend on security policy, internal approvals, client version, and local environment |
| Embedded terminal for manual coding agent workflows | Yes | You can run coding agents manually in the embedded terminal |
| Shallow Clone | Yes | |
| Undo rebases, cherry picks, and AI Commit Compose | Yes | |
| Local Workspaces | Yes | Stored on-device only; not shareable across machines |
| Cloud Workspaces | No | Requires gitkraken.dev |
| Launchpad with on-premises integrations | Yes | See supported integrations list |
| Launchpad Cloud Workspace filtering | No | |
| Launchpad Team View | No | |
| Launchpad Saved Views | No | |
| Launchpad snooze and pin | No | |
| Conflict detection (target branch) | Yes | |
| Conflict detection (Org Member awareness) | No | Requires cloud GitKraken Org |
| Cloud Patch sharing | No | |
| GitKraken AI (default hosted provider, no key required) | No | Requires GitKraken cloud services |
| GitKraken AI (Custom URL or bring your own key) | Yes | Per-user opt-in; you provide the AI infrastructure |
| ARM builds | Yes | Separate ARM installer available |
| Centralized version management | Yes | Admin controls client version rollout via the server |
| LDAP authentication | Yes | Configured on the Self-Hosted Server |
| GitHub Enterprise Server integration | Yes | |
| GitLab Self-Managed integration | Yes | |
| Bitbucket Server and Data Center integration | Yes | |
| Azure DevOps Server integration | Yes | |
| Jira Data Center integration | Yes | |
| GitHub.com, GitLab.com, Bitbucket.org, Azure DevOps cloud, Jira Cloud | No | Require outbound internet access |
| GitKraken Insights | No | Requires gitkraken.dev |
| GitKraken Code Review (**Review on GitKraken.dev**) | No | Requires gitkraken.dev |

### GitKraken AI in Self-Hosted Server

GitKraken AI is available in Self-Hosted Server when individual users configure a Custom URL that directs AI requests to a private or internal service. The default GitKraken-hosted AI provider is not accessible in network-isolated environments.

**To enable GitKraken AI:**

1. Go to <kbd>Preferences > GitKraken AI</kbd>.
2. Select **Custom URL** as the provider.
3. Enter the endpoint URL for your internal AI service.
4. If your endpoint requires authentication, enter an API key.

Custom URL is an opt-in, per-user setting. GitKraken does not validate or support the configuration of third-party or self-hosted AI endpoints.

When you configure a Custom URL, the following AI features are available:

- Commit message generation
- Commit Composer (Preview)
- Explain commits
- Explain branch changes
- Pull request title and description generation (requires a configured on-premises integration)
- Auto-resolve merge conflicts (Preview)
- Stash message generation


### Supported on-premises integrations

GitKraken Self-Hosted supports the following self-hosted integrations. These integrations communicate only within your network and do not require outbound internet access:

- GitHub Enterprise Server
- GitLab Self-Managed
- Bitbucket Server and Data Center
- Azure DevOps Server
- Jira Data Center
- Any custom remote hosting service available over HTTPS or SSH authentication

The cloud-hosted counterparts of these services (GitHub.com, GitLab.com, Bitbucket.org, Azure DevOps cloud, and Jira Cloud) are not supported because they require outbound internet connectivity.

***

## System requirements

GitKraken Self-Hosted Server runs on a lightweight Linux server or virtual machine using Docker containers.

### Supported operating systems
- CentOS 7 (64-bit)
- Ubuntu (Zesty 17.04, Xenial 16.04 LTS, Trusty 14.04 LTS)
- Red Hat Enterprise Linux 7 (RHEL7)

### Minimum specifications
- 2 CPU cores
- 4 GB RAM
- 5 GB disk space

To install Docker CE, the host system must meet Docker's requirements:

#### [CentOS Requirements](https://docs.docker.com/engine/installation/linux/docker-ce/centos/)
- 64-bit CentOS 7 is required

#### [Ubuntu Requirements](https://docs.docker.com/engine/installation/linux/docker-ce/ubuntu/)
- 64-bit versions of:
  - Zesty 17.04
  - Xenial 16.04 (LTS)
  - Trusty 14.04 (LTS)

> **Note:** To skip server installation and maintenance, see the <a href="/gitkraken-desktop/stand-alone/">Serverless option</a>.
