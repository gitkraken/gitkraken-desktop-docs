---
title: Improve GitKraken Desktop Performance
description: Troubleshoot and fix performance issues in GitKraken Desktop with maintenance tips and optimization settings.
product: GitKraken Desktop
feature: Performance Troubleshooting
content_type: troubleshooting
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-03
llms_include: true
tags: [performance, troubleshooting, optimization, maintenance, large-repos]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to diagnose slow or unresponsive behavior in GitKraken Desktop, especially in large or complex repositories. It focuses on practical fixes such as repository maintenance, graph-size limits, auto-fetch changes, branch cleanup, LFS cleanup, and build verification for macOS systems.

**Requirements and limits**
- Scope: Troubleshooting performance problems in GitKraken Desktop repositories and UI rendering
- Common trigger: Large repositories with many references or heavy graph rendering
- Primary fixes: Repo maintenance, graph-size reduction, auto-fetch changes, branch cleanup, and LFS cleanup
- macOS-specific note: Version 11.5.1 performance can be affected by using the wrong Intel vs Apple Silicon build
- Escalation path: Contact GitKraken Support if maintenance and configuration fixes do not help

***

## Quick Start


**Common fixes:**
- Run **Perform Repo Maintenance** from the Command Palette. This executes `git maintenance run` to optimize the repository’s internal data structures.
- Set the Auto-fetch interval to `0` in <kbd>Preferences > General</kbd> to disable automatic background fetches.
- Lower the **Max Commits in Graph** value in <kbd>Preferences > General</kbd> to reduce the number of commits rendered.
- Delete unnecessary local branches to reduce reference overhead.
- If Git LFS is in use, run an LFS prune to clean up unreferenced objects.
- Clone a fresh copy of the repository to a clean directory if the local copy has accumulated issues.

**macOS users on version 11.5.1:** Confirm the installed build matches your chip type (Apple Silicon or Intel) by checking the GitKraken menu. Download the correct version from gitkraken.com if there is a mismatch.

If problems persist after these steps, contact GitKraken support.

***

## How to improve performance

Performance issues are commonly linked to large repositories with many references. Try these steps to improve responsiveness:

### Repository-level actions

- Use the <kbd>Perform Repo Maintenance</kbd> command from the [Command Palette](/start-here/command-palette). This runs `git maintenance run`, which may take several minutes on large repos.
- Run [`git gc`](https://git-scm.com/docs/git-gc) in your local repository.
- Clone a fresh copy of the repository to a new directory.

### Interface optimization

- Disable auto-fetch by setting the [Auto-fetch interval](/gitkraken-desktop/preferences/#auto-fetch) to `0`.
- Reduce the number of commits shown in the graph by setting a lower [Max Commits value](/gitkraken-desktop/preferences/#max-commits-in-graph).
- [Solo or Hide](/gitkraken-desktop/hiding-and-soloing/) branches and tags to reduce visual complexity.

### Cleanup and maintenance

- [Delete unnecessary local branches](/gitkraken-desktop/branching-and-merging/#delete-a-branch).
- If using Git LFS, perform an [LFS prune](/gitkraken-desktop/git-lfs/).
- Run [`git status`](https://git-scm.com/docs/git-status) to check for unexpected working directory states.
- Restart GitKraken Desktop daily to clear any accumulated memory or cache usage.


### How to verify your GitKraken Desktop build on macOS

Some Mac users have noticed that GitKraken Desktop **11.5.1** may feel less responsive. In most cases, the Mac installed the wrong build for the machine’s chip (Intel vs. Apple Silicon).

It’s an easy check:

1. **Open GitKraken.** Navigate to the **GitKraken** menu from the top left of your machine.

   <figure>
     <img src="/wp-content/uploads/arm2.png" class="help-center-img img-bordered" alt="Check your version number and build (arm64 64-bit)" />
     <figcaption style="text-align: center; color: #888">Check your version from the GitKraken menu.</figcaption>
   </figure>

2. **Confirm the build matches your Mac’s chip** (Apple Silicon/arm64 vs. Intel/x64).

3. **If it doesn’t match,** [download the correct version](https://www.gitkraken.com/download) and reinstall.



<div class='callout callout--basic'>
    <p><strong>Note:</strong> Performance issues may also be impacted by file system speed, antivirus scanning, or external integrations. If the above steps don’t help, reach out to <a href="https://help.gitkraken.com/gitkraken-desktop/contact-support/">GitKraken support</a>.</p>
</div>
