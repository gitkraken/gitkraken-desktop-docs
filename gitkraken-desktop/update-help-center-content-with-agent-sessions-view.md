# Update Help Center content with Agent Sessions View

<kbd>Last updated: April 2026</kbd>

Use this example to review and update repository documentation with a coding agent in GitKraken Desktop. Agent Sessions View is useful for documentation maintenance because it keeps the worktree, agent session, WIP changes, and pull request status together in one place.

## Before you start

Make sure you have the following:

- GitKraken Desktop installed and updated to a version that includes Agent Sessions View
- Access to a Git repository on GitHub that includes markdown documentation
- A coding agent configured in GitKraken Desktop, using Codex in this example
- GitHub integration connected so you can create a pull request from GitKraken Desktop

## Open the Help Center repo in GitKraken Desktop

Many codebases include markdown files for setup instructions, contributor guidance, architecture notes, changelogs, or internal documentation. This example uses a repository that includes markdown docs you want to review and update so they match the current codebase.

1. Open GitKraken Desktop.
2. Click the plus icon in the top left and choose **Open**.
3. Select the repository you want to review.
4. Confirm that the default worktree opens and that you can see the commit graph.

## Create a new agent session worktree

Agent Sessions View organizes worktrees around coding agent sessions. List view shows the same underlying worktrees, but focuses on general branch and worktree management.

1. Open the **Agents** left panel and switch to **Agent Sessions View**.
2. Click **New agent session**.
3. Name the branch something like `token-to-credit-renaming`.
4. Choose **Codex** as the coding agent for this session.
5. Click **Start** to create a new worktree and agent session.
6. Confirm that:
   - A new worktree appears in the left panel.
   - The branch is checked out in the new worktree.
   - The agent session is ready for instructions.

## Ask the agent to update Gemini references

You can describe the task to the agent in plain language. In this example, start with the Gemini naming update.

```text
Search all .md files in this repo for mentions of
"Google Gemini Flash" or "Google Gemini 2.x Flash"
and rename them to "Google Gemini models".
```

The agent scans markdown files in the repository and proposes or applies edits, depending on your configuration. Before you let the agent run, validate the target phrasing so you are sure that `Google Gemini Flash` should become `Google Gemini models`.

## Ask the agent to update token references

Next, update billing and usage wording more carefully. In this case, you only want to rename `tokens` where the text clearly refers to GitKraken AI usage or billing.

```text
Search all .md files in this repo for mentions of "tokens"
and change them to "credits" only in the context of
GitKraken AI usage or billing. Do not change unrelated uses
of the word "token".
```

The agent may touch multiple pages, including release notes and common issues pages. Review those edits closely because `token` can also appear in unrelated technical contexts.

## Update date stamps for modified pages

Some GitKraken Help Center pages include a `Last updated` date near the top of the page. You can use the agent to keep those dates consistent for any files it changed.

```text
For any pages you modified that include a date stamp
at the top, update the date to "April 2026".
```

The agent updates the date line for each affected file. You can verify those changes in the diff view before you commit anything.

## Review agent changes in WIP

Agent Sessions View surfaces uncommitted edits for the current worktree in a **Work in progress (WIP)** node at the top of the graph. This makes it easy to review the full set of documentation changes produced by you or the agent.

1. In **Agent Sessions View**, select the current session.
2. Click the **WIP** node at the top of the graph.
3. Use the right-side file list to open each modified markdown file.
4. Confirm that:
   - `Google Gemini Flash` references are now `Google Gemini models`.
   - `tokens` to `credits` changes only appear in GitKraken AI contexts.
   - Date stamps at the top of modified pages are set to `April 2026`.

## Stage changes and generate commits with GitKraken AI

Once the edits look correct, stage the documentation changes and use GitKraken AI to help prepare commits.

1. Click **Stage all changes**.
2. Use the **Generate commit message** magic wand button to create a single commit message from the staged changes, or
3. Click **Compose commits with AI** to have GitKraken AI group the changes into multiple topic-based commits.
4. Review the suggested commits and optionally squash, drop, or reword them before confirming.

Multiple topic-based commits can help reviewers. For example, you might keep Gemini wording updates separate from `tokens` to `credits` updates and separate both from date-only edits.

## Open a pull request from GitKraken Desktop

After you commit the changes, open a pull request from the same worktree. Agent Sessions View keeps this workflow together so you can move from editing to review without leaving the context of the session.

1. Push the branch to your fork or `origin` if it does not exist on the remote yet.
2. Drag and drop the feature branch onto `main` in the graph to start a pull request, or use the pull request action from the right panel.
3. Use the GitHub integration to:
   - Select the repository and base branch.
   - Apply the existing pull request template.
   - Use GitKraken AI to generate a pull request title and description from the template and your changes.
4. Add reviewers and assignees if needed.
5. Create the pull request.

Once the pull request exists, GitKraken Desktop shows an active PR chip in the worktree and displays pull request details in the top-right panel.

## Merge the pull request and verify

If you have permission, you can merge the pull request directly from GitKraken Desktop. You can also open the pull request in GitHub in your browser if your team prefers to merge there.

1. Merge the pull request after review and approval.
2. Pull the latest changes into your local `main`.
3. Confirm that `Google Gemini models` and `AI credits` appear correctly in the updated documentation.
4. If your Help Center publishing flow requires a CMS publish step, complete that process so the changes appear live.

## Clean up the agent worktree

Agent Sessions View and List view both point to the same worktrees. When the work is complete, remove the temporary worktree from List view.

1. Switch from **Agents** to **List view** in the left panel.
2. Make sure **Worktrees** is visible. If it is not, right-click a left-panel header and enable **Worktrees**.
3. Hover over the worktree you used for the agent session.
4. Right-click and select **Remove worktree**.
5. Verify that:
   - The worktree disappears from the left panel.
   - It is no longer available in the branch or worktree selector at the top of GitKraken Desktop.

## Example prompts you can reuse

Use prompts like these when you want to understand a repository before making changes, or when you want to apply the same workflow to a different set of documentation files.

```text
Scan this repository and tell me which markdown files are most relevant
to terminology updates or documentation maintenance. Summarize what you
find before making any changes.
```

```text
Search markdown files for references to "Google Gemini Flash" or
"Google Gemini 2.x Flash". Show me which files would need to change
to use "Google Gemini models", then make the edits after I confirm.
```

```text
Search markdown files for references to "tokens" and identify which
uses appear to describe product billing, usage, or entitlements.
Change only those references to "credits" and leave unrelated uses
of "token" unchanged.
```

```text
For any documentation files you modified, check whether they include a
"Last updated" line near the top. Update that date consistently and
show me the affected files in the diff.
```

```text
Summarize the changes you made, group them into logical commit topics,
and suggest commit messages I can use for a pull request.
```

Reuse this workflow whenever you need to safely review, refactor, or standardize wording across multiple documentation pages with coding agents in GitKraken Desktop. Agent Sessions View helps you keep the worktree, edits, review flow, and pull request connected so the process stays repeatable.
