---
title: Resolve Merge Conflicts Between AI Coding Agent Branches in GitKraken Desktop
description: Merge two AI coding agents' branches in GitKraken Desktop, resolve conflicts with the Merge Tool or Auto-resolve with AI, and test the combined result.
product: GitKraken Desktop
feature: Agent Merge Conflicts
content_type: how-to
audience: developer
plan_required: Pro
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-10
llms_include: true
tags: [agents, coding-agents, ai, merge, merge-conflicts, auto-resolve, worktrees, parallel-agents]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: October 2026</kbd>

Use this page when two AI coding agents worked in separate worktrees and their branches now conflict. You merge both branches into one integration branch, resolve each conflict in the Merge Tool, with or without Auto-resolve with AI, and then test the combined result before you open a pull request.

**Requirements and limits**
- Scope: Combining the work of two or more agent branches and resolving the conflicts between them
- Prerequisite: The in-app merge conflict output editor requires a [paid GitKraken license](https://www.gitkraken.com/pricing?source=help_center&product=gitkraken). Auto-resolve with AI also requires GitKraken AI to be enabled.
- Limits: Auto-resolve with AI is in Preview. It suggests a resolution for each conflicted hunk, and you decide whether to keep it.
- Limits: A merge with no conflicts doesn't prove the two agents' changes work together. Test the combined result.

***

## Quick Start

1. Create an integration branch from your target branch, such as `main`, and open it in its own worktree.
2. Merge the first agent's branch into it.
3. Merge the second agent's branch. GitKraken Desktop lists any conflicted files in the Commit Panel.
4. Click each conflicted file to open the Merge Tool. Resolve it by hand, or click **Auto-resolve with AI** and review the suggestion for each hunk.
5. Commit the merge, then run both agents' tests together.
6. Push the integration branch and open a pull request.

***

## Why merge in a separate integration branch

Merging into a new branch keeps both agent branches exactly as the agents left them. If the combined result isn't right, you can throw away the integration branch and start again without losing either agent's work.

To set one up:

1. In the Commit Graph, right-click the newest commit on your target branch, such as `main`, and select **Create branch here**. Name it something like `integrate/login-and-search`.
2. In the Left Panel, right-click the new branch and select **Create worktree**.
3. Open the new worktree.

Your own worktree and the agents' worktrees stay untouched.

***

## How to merge the agent branches

With the integration worktree open:

1. Right-click the first agent's branch and select **Merge**, or drag it onto the integration branch. If the agents only changed different files, the merge completes on its own.
2. Repeat for the second agent's branch.

<figure>
  <img src="/wp-content/uploads/merge-right@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop context menu showing the option to merge one branch into another.">
  <figcaption style="text-align:center; color:#888">Merge each agent's branch with drag and drop or the right-click menu.</figcaption>
</figure>

If both agents changed the same lines, GitKraken Desktop stops and lists the conflicted files in the Commit Panel.

<figure>
  <img src="/wp-content/uploads/merge-conflict@2x.png" class="help-center-img img-bordered" alt="GitKraken Desktop Commit Panel listing a conflicted file during a merge.">
  <figcaption style="text-align:center; color:#888">Conflicted files appear in the Commit Panel.</figcaption>
</figure>

***

## How to resolve each conflict

Click a conflicted file to open the Merge Tool. It shows the integration branch on the left, the incoming agent branch on the right, and the output at the bottom. You have four ways to resolve it.

### Use Auto-resolve with AI

1. In the Merge Tool, click **Auto-resolve with AI**.
2. Read the explanation and the confidence level for each conflicted hunk.
3. Accept, edit, or discard the suggestion. Look hardest at the hunks with low confidence.

<figure>
  <img src="/wp-content/uploads/Auto-resolve-with-AI-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken Desktop merge conflict view showing an AI-generated resolution with an explanation and a confidence level for each hunk.">
  <figcaption style="text-align:center; color:#888">Auto-resolve with AI explains each suggestion and rates its confidence.</figcaption>
</figure>

Treat the suggestion as a starting point. The AI sees the conflicting code, not what each agent was asked to do. To give it that context, add instructions in <kbd>Preferences > GitKraken AI > Conflict Resolution</kbd>, for example a sentence about what each task was meant to change.

### Choose lines by hand

Use the checkboxes or the **+** buttons to pick lines from each side, or type in the output directly. Use the arrow keys to move between conflicts.

### Take one side for the whole file

If one agent's version of a file should win completely, right-click the file in the Commit Panel and select **Take current** or **Take incoming**.

### Use an external merge tool

If your team uses a supported external tool, set it under <kbd>Preferences > General</kbd>. See [Branching and merging](/gitkraken-desktop/branching-and-merging/) for the supported tools.

When every file is resolved, save the output, stage the files, and commit the merge.

***

## How to check the combined result

Resolving every conflict means Git can combine the files. It doesn't mean the two agents' changes work together.

1. **Run the tests for both tasks** in the integration worktree, from the [embedded terminal](/gitkraken-desktop/terminal/). A change from one agent can break the other agent's feature without causing a conflict.
2. **Review the combined diff.** Click the newest commit on your target branch, then hold <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> and click the merge commit to see everything the integration branch adds. See [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/) for more ways to inspect the work.
3. **Push and open a pull request** from the integration branch. See [Pull Requests](/gitkraken-desktop/pull-requests/).

If the result isn't right, remove the integration worktree and its branch and start again. Both agent branches are unchanged.

***

## How to keep conflicts small next time

- **Merge each agent's branch as soon as it finishes,** instead of waiting for every agent. Smaller merges produce smaller conflicts.
- **Give agents tasks that touch different files** when you can. Parallel agents conflict most when they edit the same files.
- **Check for overlap early.** [Conflict Prevention](/gitkraken-desktop/conflict-prevention/) warns when your work overlaps with your target branch or with Org Members' work.

***

## Common questions

### Can GitKraken Desktop resolve the conflicts automatically?

It can suggest a resolution. Auto-resolve with AI proposes a fix for each conflicted hunk, with an explanation and a confidence level, and you accept, edit, or discard each one. Nothing is committed until you commit the merge.

### Does a merge with no conflicts mean the agents' work fits together?

No. Git only checks whether lines overlap. Run both agents' tests on the combined branch before you open a pull request.

### Should I rebase one agent branch onto the other instead?

You can. Rebase gives a straight-line history but rewrites the rebased branch's commits. See [Branching and merging](/gitkraken-desktop/branching-and-merging/) for when to use merge or rebase. If you rebase, you resolve the same conflicts one commit at a time.

### Does this work with any coding agent?

Yes. Merging works on Git branches, so it doesn't matter which agent made the changes. See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/) for the agents GitKraken Desktop integrates with.

***

## Related pages

- [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/)
- [Branching and merging](/gitkraken-desktop/branching-and-merging/)
- [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai/)
- [Manage Git Worktrees](/gitkraken-desktop/worktrees/)
- [Clean Up AI Coding Agent Commits Before Review](/gitkraken-desktop/clean-up-agent-commits/)
