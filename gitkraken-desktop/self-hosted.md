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
<kbd>Last updated: March 2026</kbd>

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
