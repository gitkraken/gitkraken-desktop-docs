---

title: Performance Issues
description: What to do if GitKraken Desktop is performing poorly
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: April 2025</kbd>

We're always on a quest to streamline the git experience as well as improve the performance of GitKraken Desktop. If you're experiencing slow performance, it can often be remedied using one of the troubleshooting steps below.

***

### Improving Performance

Perfomance issues in GitKraken Desktop are often related to a specific repository. Some large or complex repositories with many references may cause GitKraken Desktop to slow down. 

#### How to troubleshoot slow performance

- `Perform Repo Maintenance` from the [Command Palette](/start-here/command-palette). This command will execute `git maintenance run`, which may take several minutes on larger repositories.

- Perform a [git gc](https://git-scm.com/docs/git-gc) on the repository.  

- Take a fresh clone of the repository to a new local directory.

#### Additional troubleshooting steps

- Disable auto-fetch by setting the [Auto-fetch](/gitkraken-desktop/preferences/#auto-fetch) Interval to 0. 

- Perform a [git status](https://git-scm.com/docs/git-status) on the repository.

- [Delete local branches](branching-and-merging/#delete-a-branch) that are not needed. 

- [Soloing or Hiding](/gitkraken-desktop/hiding-and-soloing/) branches/tags.

- Set the Max Commits in Graph to [show fewer commits](/gitkraken-desktop/preferences/#max-commits-in-graph).

- If [working with an LFS repository](/gitkraken-desktop/git-lfs/), you can perfom an LFS prune.

- Restart GitKraken Desktop daily
