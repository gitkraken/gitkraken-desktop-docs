---
title: Set Up GitKraken Self-Hosted Server (On-Premise)
description: Learn how to install and configure GitKraken On-Premise Self-Hosted Server, including system requirements, supported OS versions, and benefits for secure environments.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

## Overview

**GitKraken On-Premise Self-Hosted Server** is a version of GitKraken Desktop that operates entirely within your internal network. Also referred to as *GitKraken Enterprise Self-Hosted*, *Enterprise On-Premise Server*, or *Self-Hosted*, this option allows users to authenticate and work without external internet access.

### Key Benefits

- Operates without internet connectivity (ideal for air-gapped or secure environments)
- Supports email-based and LDAP authentication
- Full control over version management

<figure class='figure center'>
  <img src='/wp-content/uploads/manage-users.png' srcset='/wp-content/uploads/manage-users@2x.png 2x' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Manage users and settings within your private GitKraken instance.</figcaption>
</figure>

<div class='callout callout--warning'>
  <p><strong>Note:</strong> GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately from standard subscriptions. To purchase, visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing?_gl=1*vtr4xk*_up*MQ..*_gs*MQ..&gclid=Cj0KCQjwqIm_BhDnARIsAKBYcmv98H0EKgytPnuCPuTqdL2vy4GQaCsizBMO9m8mz2n1hMMXO3AAw7YaAiyKEALw_wcB?source=help_center&product=gitkraken'>On-Premise Pricing</a> page.</p>
</div>

## System Requirements

GitKraken Self-Hosted Server runs on a lightweight Linux server or virtual machine using Docker containers.

### Supported OS
- CentOS 7 (64-bit)
- Ubuntu (Zesty 17.04, Xenial 16.04 LTS, Trusty 14.04 LTS)
- Red Hat Enterprise Linux 7 (RHEL7)

### Minimum Specifications
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
