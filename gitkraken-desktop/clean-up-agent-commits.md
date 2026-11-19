---
title: Clean Up AI Coding Agent Commits Before Review in GitKraken Desktop
description: Turn a Claude Code or Codex agent's one giant commit, or a run of "fix stuff" commits, into a history a reviewer can follow in GitKraken Desktop. Use Commit Composer to regroup the changes with AI, or interactive rebase to squash, reorder and reword the commits by hand on every plan.
product: GitKraken Desktop
feature: Clean Up Agent Commits
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: preview
last_verified: 2026-11
llms_include: true
tags: [agents, coding-agents, ai, claude-code, codex, commit-composer, recompose, interactive-rebase, squash, commits, history, pull-requests]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-agent-workflows"
    nav_label: "Clean Up Agent Commits"
    nav_order: 30
    nav_parent: "desktop-agent-workflows"
    page_type: "content"
    card_icon: "git-commit"
    card_color: "purple"
    card_description: "Turn an agent's commits into a reviewable history"
---
<kbd>Last updated: November 2026</kbd>

To clean up the commits that Claude Code, Codex or another AI coding agent left on a branch, open the branch in GitKraken Desktop and use Commit Composer or interactive rebase. Commit Composer uses AI to split 1 giant commit, or regroup 15 "fix stuff" commits, into logical commits with clear messages, and it never changes the code itself. Interactive rebase lets you squash, reorder and reword the agent's commits by hand, with no AI and on every plan. With either one, you review the new history before anything on your branch changes, so a reviewer can follow the work one commit at a time.

## Requirements and limits

- Scope: Regrouping an agent's uncommitted changes or existing commits into a reviewable history before you open a pull request
- Prerequisite: Interactive rebase works on every plan and does not use AI.
- Prerequisite: Commit Composer requires a [paid GitKraken subscription](https://www.gitkraken.com/pricing?source=help_center&product=gitkraken) with GitKraken AI enabled. On-premises deployments need a custom AI endpoint (see [GitKraken AI](/gitkraken-desktop/gkd-gitkraken-ai/)).
- AI usage: Commit Composer uses your GitKraken AI credits, or your own AI provider if you set one up.
- Limits: Commit Composer is in Preview.
- Limits: To recompose existing commits, they must be contiguous, on the current branch, and have no merge commits between the branch head and the oldest selected commit.
- Limits: Interactive rebase has the same limits: the commits must be on the branch you have checked out, with no merge commits between the branch head and the agent's first commit.
- Limits: Recomposing or rebasing commits you already pushed rewrites shared history.

***

## Quick Start

Before you start, open the agent's worktree: in the Agents view, right-click the session card and select **Open this worktree**. Then pick the row that matches what the agent left you.

| Where the changes are | What to use | How | Notes |
|---|---|---|---|
| Uncommitted, in the agent's worktree | **Compose commits with AI** | Stage the changes, then click **Compose commits with AI** in the Commit Panel | |
| Committed on the agent's branch, not pushed | **Recompose commits with AI** | <kbd>Shift</kbd> + click the agent's first and last commits, right-click, and select **Recompose *[number]* commits with AI (Preview)** | The commits must be next to each other, with no merge commits in between |
| Committed and pushed | **Recompose commits with AI**, then force push | Recompose as above, then force push the branch | Only if nobody else has pulled or built on the branch |
| Committed, and you want to clean up by hand | **Interactive Rebase** | Right-click the commit just below the agent's first commit and select **Interactive Rebase *[number]* children of *[commit]***. Set each commit to **Pick**, **Reword**, **Squash**, or **Drop**, drag commits to reorder them, then click **Start Rebase** | No AI, works on every plan. If you already pushed the branch, force push it afterward |

With Commit Composer, GitKraken Desktop shows the proposed commits first, and your branch does not change until you click **Create Commits**. With interactive rebase, your branch does not change until you click **Start Rebase**.

***

## Which AI credits Commit Composer uses

Commit Composer runs on GitKraken AI. By default, it uses your GitKraken AI credits. If you add your own provider and API key, such as OpenAI, Anthropic, Azure, Google Gemini, or a custom URL, Commit Composer uses that provider instead.

You can choose which set of credits a cleanup spends. For example, if your agent work is already running through one provider, you can compose commits with the other. To set your provider, go to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> GitKraken AI</em>. See [How to use your own AI provider key](/gitkraken-desktop/gkd-gitkraken-ai/) for setup.

***

## How to split an agent's uncommitted changes into commits

Use this when the agent changed files but did not commit anything.

1. Open the agent's worktree, then select its WIP node and stage the changes you want to commit. Selecting the agent's WIP row from another worktree does not open its files in the Commit Panel. Click **Open Worktree** on that row first.
2. In the Commit Panel, click **Compose commits with AI**.
3. Review the proposed commits. Reorder them, squash related ones together, or edit the messages.
4. Click **Create Commits** to apply them. If you want to start over, click **Reset** to go back to the proposal as it was before your edits. To leave without changing anything, click **Cancel**.

<figure>
  <img src="/wp-content/uploads/compose-WIP@2x.png" class="help-center-img img-bordered" alt="Selected WIP node in GitKraken Desktop with an arrow pointing to the Compose commits with AI button in the Commit Panel.">
  <figcaption style="text-align:center; color:#888">Compose commits from the agent's uncommitted changes.</figcaption>
</figure>

***

## How to recompose commits the agent already made

Use this when the agent committed everything at once, or in many small steps that do not tell a clear story.

1. In the Commit Graph, hold <kbd>Shift</kbd> and click the agent's first and last commits to select the range.
2. Right-click the selection and select **Recompose *[number]* commits with AI (Preview)**, or click **Recompose commits with AI** in the Commit Panel.
3. Review the proposed structure. Reorder, squash, or edit messages until each commit does one thing and its message says what and why.
4. Click **Create Commits**. You can also click **Reset** to start over from the original proposal, or **Cancel** to leave without changing anything.

<figure>
  <img src="/wp-content/uploads/compose-existing-commits@2x.png" class="help-center-img img-bordered" alt="Commit Graph context menu in GitKraken Desktop with the option to recompose a range of commits with AI.">
  <figcaption style="text-align:center; color:#888">Recompose a range of the agent's commits.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/commit-composer-UI@2x.png" class="help-center-img img-bordered" alt="Commit Composer window in GitKraken Desktop with options to pick, squash, or reword each proposed commit.">
  <figcaption style="text-align:center; color:#888">Adjust the proposed commits before you apply them.</figcaption>
</figure>

Recomposing keeps the original commit authors and adds co-authors when a new commit combines work from several people.

***

## How to check the new commits

Commit Composer does not change any code, so the final state of your branch is the same before and after. What changes is how the work is split up and described. Check that part before you share it:

1. **Read each new commit.** Click each commit and read its diff and message. A reviewer should be able to follow the change one commit at a time.
2. **Test each commit if your team needs every commit to build.** The newest commit has the same code as before, so this check is about the commits in between. Right-click each new commit, select **Checkout this commit**, and run your tests from the [embedded terminal](/gitkraken-desktop/terminal/). Check out the agent's branch again when you're done. Your CI may also run this check for you.

If you do not like the result, click **Undo** in the toolbar right away. Undo reverses a Compose or Recompose action as long as you have not pushed the branch. The Undo tooltip lists the action as a rebase, because that is how GitKraken Desktop applies the new commits.

<figure>
  <img src="/wp-content/uploads/gkd-commit-composer-undo.png" class="help-center-img img-bordered" alt="GitKraken Desktop toolbar with the Undo button hovered after composing commits with AI. The tooltip reads Undo Rebase followed by a commit SHA.">
  <figcaption style="text-align:center; color:#888">Click Undo to reverse a commit composition. The tooltip lists it as a rebase.</figcaption>
</figure>

***

## How to share the cleaned-up branch

- **If you never pushed the branch,** push it as usual and [open a pull request](/gitkraken-desktop/pull-requests/).
- **If you already pushed it,** recomposing or rebasing rewrote commits that are on the remote, so a normal push is rejected. GitKraken Desktop tells you the branch is behind the remote and offers **Pull**, **Force Push**, and **Cancel**. Select **Force Push**, then confirm. GitKraken Desktop uses a safe force push (force-with-lease), which stops if someone pushed to the branch since your last fetch. Use it only if nobody else has pulled or built on the branch. See [Push, Pull, and Fetch](/gitkraken-desktop/pushing-and-pulling/).

To write the pull request description, click the AI icon in the description field when you create the pull request to generate a draft, or right-click the branch and select **Explain Branch Changes** for a summary to start from. Edit either one so it says what you checked and what you did not.

***

## Common questions

Answers to frequent questions about cleaning up agent commits.

### Does Commit Composer change my code?

No. It only reorganizes the changes into new commits and rewrites their messages. The final code on your branch is the same before and after.

### Can I recompose commits from more than one agent session?

Not across a merge. Recompose only works on commits that are next to each other on the branch you have checked out, with no merge commits in the range. Clean up each agent's branch on its own first, then combine them. See [Resolve Merge Conflicts Between AI Agent Branches](/gitkraken-desktop/agent-merge-conflicts/).

### Can I clean up commits without AI?

Yes. [Interactive rebase](/gitkraken-desktop/interactive-rebase/) works on every plan and does not use AI. Use it to squash an agent's "fix stuff" commits into the commits they fix, put the commits in a logical order, and rewrite their messages:

1. Open the agent's worktree so its branch is checked out.
2. In the Commit Graph, right-click the commit just below the agent's first commit and select **Interactive Rebase *[number]* children of *[commit]***.
3. In the list next to each commit, choose what to do with it:
   - **Pick**: keep the commit as it is.
   - **Reword**: write a new message. You can also double-click the commit.
   - **Squash**: combine the commit into the older commit below it.
   - **Drop**: remove the commit and its changes.
4. Drag commits up or down to reorder them, or right-click a commit and select **Move commit up** or **Move commit down**.
5. Click **Start Rebase**. To go back to the original list, click **Reset**. To leave without changing anything, click **Cancel Rebase**.

<figure>
  <img src="/wp-content/uploads/squash.png" class="help-center-img img-bordered" alt="Interactive rebase in GitKraken Desktop showing Squash selected for two commits, which will combine into a single commit">
  <figcaption style="text-align:center; color:#888">Squash small agent commits into the commit they belong to.</figcaption>
</figure>

If you already pushed the branch, force push it afterward, as described in [How to share the cleaned-up branch](#how-to-share-the-cleaned-up-branch).

### How do I see what the agent changed before I clean it up?

See [Review and Undo AI Coding Agent Changes](/gitkraken-desktop/review-and-undo-agent-changes/).

***

## Related pages

- [GitKraken AI Features Overview](/gitkraken-desktop/gkd-gitkraken-ai/)
- [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/)
- [Interactive Rebase](/gitkraken-desktop/interactive-rebase/)
- [Pull Requests](/gitkraken-desktop/pull-requests/)
- [Resolve Merge Conflicts Between AI Agent Branches](/gitkraken-desktop/agent-merge-conflicts/)
- [Undo and Redo](/gitkraken-desktop/undo-and-redo/)
