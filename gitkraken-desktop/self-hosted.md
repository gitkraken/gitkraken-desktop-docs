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
last_verified: 2026-03
llms_include: true
tags: [self-hosted, on-premise, setup, enterprise, server]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: April 2026</kbd>

Use this page to understand what GitKraken On-Premise Self-Hosted Server is, when to choose it, and what infrastructure it requires before installation. It summarizes the offline deployment model, supported operating systems, minimum server specs, and the distinction between Self-Hosted and Serverless on-premise offerings.

**Requirements and limits**
- Product scope: GitKraken On-Premise Self-Hosted Server
- Environment fit: Internal-network, offline, or air-gapped deployments
- Infrastructure model: Lightweight Linux server or VM running Docker containers
- Minimum specs: 2 CPU cores, 4 GB RAM, 5 GB disk space
- Supported OS families on this page: CentOS 7, selected Ubuntu versions, and RHEL 7
- Commercial note: Self-Hosted and Serverless on-premise offerings are sold separately from standard subscriptions and from each other

## Overview

**GitKraken On-Premise Self-Hosted Server** is a version of GitKraken Desktop that operates entirely within your internal network. Also referred to as *GitKraken Enterprise Self-Hosted*, *Enterprise On-Premise Server*, or *Self-Hosted*, this option allows users to authenticate and work without external internet access.

### Key benefits

- Operates without internet connectivity (ideal for air-gapped or secure environments)
- Supports email-based and LDAP authentication
- Full control over version management

<figure class='figure center'>
  <img src='/wp-content/uploads/manage-users@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Manage users and settings within your private GitKraken instance.</figcaption>
</figure>

<div class='callout callout--warning'>
  <p><strong>Note:</strong> GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately from standard subscriptions. To purchase, visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing?_gl=1*vtr4xk*_up*MQ..*_gs*MQ..&gclid=Cj0KCQjwqIm_BhDnARIsAKBYcmv98H0EKgytPnuCPuTqdL2vy4GQaCsizBMO9m8mz2n1hMMXO3AAw7YaAiyKEALw_wcB?source=help_center&product=gitkraken'>On-Premise Pricing</a> page.</p>
</div>

## Feature support

GitKraken On-Premise Self-Hosted Server uses the same Desktop client as GitKraken On-Premise Serverless. The Desktop client feature set is identical between the two variants. The difference between Self-Hosted and Serverless is the deployment and license model, not the feature set.

In Self-Hosted, a central server inside your network handles authentication and license management. This gives your organization control over which client version is deployed to users and how users authenticate. Features that require connectivity to GitKraken cloud services are not available in either on-premises variant.

### What is included

The following feature categories are fully supported:

**Core Git client**: All standard Git operations, including commits, branches, merges, rebases, diffs, stashing, tagging, interactive rebase, cherry pick (including multi-commit interactive cherry pick), worktrees, shallow clone, and undo or redo of rebase and cherry pick operations.

**Launchpad**: Track pull requests and issues in a single view and filter by repository, branch, milestone, or sprint. Launchpad works with the following on-premises integrations: GitHub Enterprise Server, GitLab Self-Managed, Bitbucket Server and Data Center, Azure DevOps Server, and Jira Data Center. For a description of the differences between cloud and on-premises Launchpad, see [How On-Premise Launchpad differs from Cloud Launchpad](/gitkraken-desktop/gitkraken-launchpad/#how-on-premise-launchpad-differs-from-cloud-launchpad).

**Local Workspaces**: Organize multiple local Git repositories in one view. You can see the branch status of each repository and run multi-repository actions, such as fetch and pull, from a single place. Cloud Workspaces are not available.

**Conflict detection**: GitKraken detects potential conflicts with your target branch before you reach the merge step and alerts you when your checked-out branch has diverged from its pull request target.

**GitKraken AI (bring your own key)**: All GitKraken AI features are available when you configure a Custom URL that points to a private or internal AI endpoint. For setup instructions, see [GitKraken AI in Self-Hosted Server](#gitkraken-ai-in-self-hosted-server).

**ARM builds**: A native ARM installer is available for machines with ARM architecture.

**Centralized version management**: Because the Desktop client connects to your internal server, your admin controls which client version is served to users. This lets you test and roll out updates on your own schedule.

**Authentication**: Users authenticate through your Self-Hosted Server using email-based or LDAP authentication. No external GitKraken cloud account is required.

**On-premises integrations**: GitKraken Self-Hosted supports integrations with self-hosted Git hosting services and issue trackers. For the full list, see [Supported on-premises integrations](#supported-on-premises-integrations).

### What is not available

The following features require connectivity to GitKraken cloud services (`gitkraken.dev`) or to external cloud hosting providers and are not available in Self-Hosted Server:

- Cloud Workspaces and features that depend on them, including Team Launchpad, Launchpad Saved Views, and Launchpad snooze and pin
- GitKraken Insights
- GitKraken AI using the default GitKraken-hosted provider
- Cloud Patch sharing
- Org Member conflict detection
- Integrations with cloud-hosted services: GitHub.com, GitLab.com, Bitbucket.org, Azure DevOps cloud, Jira Cloud, and Trello

### Feature support table

| Feature | Supported | Notes |
|---|---|---|
| Core Git client (commits, branches, merges, rebase, diff, stash) | Yes | |
| Interactive Rebase | Yes | |
| Multi-commit Cherry Pick | Yes | |
| Worktrees | Yes | Requires client version 10.5.0 or later |
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
| GitKraken AI (default hosted provider, no key required) | No | Calls GitKraken cloud endpoint |
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

### GitKraken AI in Self-Hosted Server

GitKraken AI is available in Self-Hosted Server when individual users configure a Custom URL that directs AI requests to a private or internal service. The default GitKraken-hosted AI provider is not accessible in network-isolated environments.

**To enable GitKraken AI:**

1. Go to <kbd>Preferences > GitKraken AI</kbd>.
2. Select **Custom URL** as the provider.
3. Enter the endpoint URL for your internal AI service.
4. If your endpoint requires authentication, enter an API key.

This is an opt-in, per-user setting. GitKraken does not validate or support the configuration of third-party or self-hosted AI endpoints.

When you configure a Custom URL, the following AI features are available:

- Commit message generation
- Commit Composer (Preview)
- Explain commits
- Explain branch changes
- Pull request title and description generation (requires a configured on-premises integration)
- Auto-resolve merge conflicts (Preview)
- Stash message generation

To configure organization-wide AI controls, see [GitKraken Dev Security Controls](https://help.gitkraken.com/gk-dev/gk-dev-security-controls/).

### Supported on-premises integrations

GitKraken Self-Hosted supports the following self-hosted integrations. These integrations communicate only within your network and do not require outbound internet access:

- GitHub Enterprise Server
- GitLab Self-Managed
- Bitbucket Server and Data Center
- Azure DevOps Server
- Jira Data Center

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

<div class='callout callout--neutral'>
  <p>Prefer to skip installation and maintenance? Explore our <a href="/gitkraken-desktop/stand-alone/">Serverless option</a>.</p>
</div>
