---
title: Clean Up AI Coding Agent Commits Before Review in GitKraken Desktop
description: Turn an AI coding agent's one giant commit or pile of "fix stuff" commits into a clean history a reviewer can follow, using Commit Composer in GitKraken Desktop.
product: GitKraken Desktop
feature: Clean Up Agent Commits
content_type: how-to
audience: developer
plan_required: Pro
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: preview
last_verified: 2026-10
llms_include: true
tags: [agents, coding-agents, ai, commit-composer, recompose, commits, history, pull-requests]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: October 2026</kbd>

Use this page when an AI coding agent leaves you with one giant commit, or with a long run of small "fix stuff" commits, and you need a history a reviewer can follow. Commit Composer in GitKraken Desktop groups the agent's changes into logical commits with clear messages. It only reorganizes the changes and never changes the code itself. You review and adjust the result before anything on your branch changes.

**Requirements and limits**
- Scope: Regrouping an agent's uncommitted changes or existing commits into a reviewable history before you open a pull request
- Prerequisite: A [paid GitKraken subscription](https://www.gitkraken.com/pricing?source=help_center&product=gitkraken) with GitKraken AI enabled. On-premises deployments need a custom AI endpoint (see [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai/)).
- Limits: Commit Composer is in Preview.
- Limits: To recompose existing commits, they must be contiguous, on the current branch, and have no merge commits between the branch head and the oldest selected commit.
- Limits: Recomposing commits you already pushed rewrites shared history.

***

## Quick Start

Before you start, open the agent's worktree: in Agent Sessions View, right-click the session card and select **Open this worktree**. Then pick the row that matches what the agent left you.

| What the agent left you | What to use | How |
|---|---|---|
| Changes it never committed | **Compose Commit with AI** | Stage the changes, then click **Compose Commit with AI** in the Commit Details Panel |
| One giant commit, or many small ones | **Recompose Commits with AI** | Select the agent's commits in the Commit Graph, right-click, and select **Recompose Commits with AI** |
| Commits you already pushed | **Recompose Commits with AI**, then force push | Only if nobody else has pulled or built on the branch |

In every case, GitKraken Desktop shows the proposed commits first. Your branch doesn't change until you click **Create commits**.

***

## How to split an agent's uncommitted changes into commits

Use this when the agent changed files but didn't commit anything.

1. Select the agent's WIP node and stage the changes you want to commit.
2. In the Commit Details Panel, click **Compose Commit with AI**.

<figure>
  <img src="/wp-content/uploads/compose-WIP@2x.png" class="help-center-img img-bordered" alt="Selected WIP node in GitKraken Desktop with an arrow pointing to the Compose commits with AI button in the Commit Details Panel.">
  <figcaption style="text-align:center; color:#888">Compose commits from the agent's uncommitted changes.</figcaption>
</figure>

3. Review the proposed commits. Reorder them, squash related ones together, or edit the messages.
4. Click **Create commits** to apply them, **Reset** to undo your edits to the proposal, or **Cancel** to stop without changing anything.

***

## How to recompose commits the agent already made

Use this when the agent committed everything at once, or in many small steps that don't tell a clear story.

1. In the Commit Graph, select the agent's commits. Hold <kbd>Shift</kbd> or <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> to select a contiguous range.
2. Right-click the selection and select **Recompose Commits with AI**, or click the button in the Commit Details Panel.

<figure>
  <img src="/wp-content/uploads/compose-existing-commits@2x.png" class="help-center-img img-bordered" alt="Commit Graph context menu in GitKraken Desktop with the option to recompose a range of commits with AI.">
  <figcaption style="text-align:center; color:#888">Recompose a range of the agent's commits.</figcaption>
</figure>

3. Review the proposed structure. Reorder, squash, or edit messages until each commit does one thing and its message says what and why.

<figure>
  <img src="/wp-content/uploads/commit-composer-UI@2x.png" class="help-center-img img-bordered" alt="Commit Composer window in GitKraken Desktop with options to pick, squash, or reword each proposed commit.">
  <figcaption style="text-align:center; color:#888">Adjust the proposed commits before you apply them.</figcaption>
</figure>

4. Click **Create commits**.

Recomposing keeps the original commit authors and adds co-authors when a new commit combines work from several people.

***

## How to check the new commits

Commit Composer doesn't change any code, so the final state of your branch is the same before and after. What changes is how the work is split up and described. Check that part before you share it:

1. **Read each new commit.** Click each commit and read its diff and message. A reviewer should be able to follow the change one commit at a time.
2. **Run your tests if your team needs every commit to build.** Run them from the [embedded terminal](/gitkraken-desktop/terminal/) in the agent's worktree.

If you don't like the result, click **Undo** in the toolbar right away. Undo reverses a Compose or Recompose action as long as you haven't pushed the branch.

***

## How to share the cleaned-up branch

- **If you never pushed the branch,** push it as usual and [open a pull request](/gitkraken-desktop/pull-requests/).
- **If you already pushed it,** recomposing rewrote commits that are on the remote, so a normal push fails. GitKraken Desktop may offer **Force Push**. Use it only if nobody else has pulled or built on the branch. See [Pushing and pulling](/gitkraken-desktop/pushing-and-pulling/).

To write the pull request description, you can generate a draft with GitKraken AI, or right-click the branch and select **Explain Branch Changes** for a summary to start from. Edit either one so it says what you checked and what you didn't.

***

## Common questions

### Does Commit Composer change my code?

No. It only reorganizes the changes into new commits and rewrites their messages. The final code on your branch is the same before and after.

### Can I recompose commits from more than one agent session?

Only if they're contiguous commits on the branch you have checked out, with no merge commits in the range. To combine work from separate agent branches, merge them first. See [Resolve Merge Conflicts Between AI Coding Agent Branches](/gitkraken-desktop/agent-merge-conflicts/).

### Can I clean up commits without AI?

Yes. Use [interactive rebase](/gitkraken-desktop/interactive-rebase/) to reorder, squash, and reword commits by hand.

### How do I see what the agent changed before I clean it up?

See [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/).

***

## Related pages

- [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai/)
- [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/)
- [Interactive Rebase](/gitkraken-desktop/interactive-rebase/)
- [Pull Requests](/gitkraken-desktop/pull-requests/)
- [Undo and Redo](/gitkraken-desktop/undo-and-redo/)
