---
title: Performance Issues
description: What to do if GitKraken Desktop is performing poorly
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

If GitKraken Desktop is running slowly, it’s often due to the size or complexity of the repository. Try the steps below to improve performance.

***

## Improving Performance

Performance issues are commonly linked to large repositories with many references. Try these steps to improve responsiveness:

### Repository-Level Actions

- Use the <kbd>Perform Repo Maintenance</kbd> command from the [Command Palette](/start-here/command-palette). This runs `git maintenance run`, which may take several minutes on large repos.
- Run [`git gc`](https://git-scm.com/docs/git-gc) in your local repository.
- Clone a fresh copy of the repository to a new directory.

### Interface Optimization

- Disable auto-fetch by setting the [Auto-fetch interval](/gitkraken-desktop/preferences/#auto-fetch) to `0`.
- Reduce the number of commits shown in the graph by setting a lower [Max Commits value](/gitkraken-desktop/preferences/#max-commits-in-graph).
- [Solo or Hide](/gitkraken-desktop/hiding-and-soloing/) branches and tags to reduce visual complexity.

### Cleanup and Maintenance

- [Delete unnecessary local branches](/gitkraken-desktop/branching-and-merging/#delete-a-branch).
- If using Git LFS, perform an [LFS prune](/gitkraken-desktop/git-lfs/).
- Run [`git status`](https://git-scm.com/docs/git-status) to check for unexpected working directory states.
- Restart GitKraken Desktop daily to clear any accumulated memory or cache usage.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> Performance issues may also be impacted by file system speed, antivirus scanning, or external integrations. If the above steps don’t help, reach out to <a href="https://help.gitkraken.com/gitkraken-desktop/contact-support/">GitKraken support</a>.</p>
</div>
