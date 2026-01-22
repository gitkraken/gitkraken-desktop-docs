---
title: GitKraken AI Features Overview
description: Use GitKraken AI to generate commit messages, PR descriptions, and explanations of code changes. Customize your AI provider and prompts to fit your workflow.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: January 2026</kbd>

Let the app handle the boring parts! GitKraken offers built-in AI features to fast-track your code contributions.

<div class='callout callout--warning'>
    <p>GitKraken AI requires a <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">paid GitKraken subscription</a>.</p>
</div>

***

## AI-powered Commit Composer (Preview)

Use AI to help organize your Git commits into clear, logical stories.

### What it does

The AI-powered Commit Composer can:

- Break up unstaged changes into meaningful commits.
- Recompose selected previous commits into a new structure.
- Reorder, squash, or edit commit messages before pushing.

<figure>
  <img src="/wp-content/uploads/before-after-commit-compose.png" srcset="/wp-content/uploads/before-after-commit-compose@2x.png" class="help-center-img img-bordered" alt="GitKraken interface showing a selected range of commits before and after being composed into a cleaner history." />
  <figcaption style="text-align: center; color: #888">AI Commit Composer button in the Commit Details Panel</figcaption>
</figure>

### How to use it

To generate commits with AI:

- **For uncommitted changes**:
  1. Stage your changes.
  2. In the Commit Details Panel, click **Compose Commit with AI**.
  3. GitKraken AI will take a moment to compose the new commits. A new window will appear with the results of the composition.
     - You can reorder, squash, or edit the commit messages.
     - The branch will not be updated until you click **Create commits**.
     - To cancel the process, click **Cancel**.
     - To undo any changes made during composition (such as reordering or squashing), click **Reset**.

<figure>
  <img src="/wp-content/uploads/compose-WIP.png" srcset="/wp-content/uploads/compose-WIP@2x.png" class="help-center-img img-bordered" alt="Selected WIP commits in GitKraken UI with arrow pointing to the 'Compose commits with AI' button in the commit panel." />
  <figcaption style="text-align: center; color: #888">Compose commits from your WIP.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/compose-WIP-UI.png" srcset="/wp-content/uploads/compose-WIP-UI@2x.png" class="help-center-img img-bordered" alt="Commit Composer interface showing a list of commits with dropdown options to pick, squash, or reword before composing." />
  <figcaption style="text-align: center; color: #888">Made adjustments, and confirm to create commits.</figcaption>
</figure>

- **For existing committed changes**:
  1. In the Commit Graph, select a contiguous range of commits using <kbd>Shift</kbd> or <kbd>Cmd</kbd>/<kbd>Ctrl</kbd>.
  2. Do one of the following:
     - Right-click the selection and choose **Recompose Commits with AI** from the context menu.
     - Click **Recompose Commits with AI** in the Commit Details Panel.
  3. GitKraken AI will take a moment to compose the new commits. A new window will appear with the results of the composition.
     - You can reorder, squash, or edit the commit messages.
     - The branch will not be updated until you click **Create commits**.
     - To cancel the process, click **Cancel**.
     - To undo any changes made during composition (such as reordering or squashing), click **Reset**.

<figure>
  <img src="/wp-content/uploads/compose-existing-commits.png" srcset="/wp-content/uploads/compose-existing-commits@2x.png" class="help-center-img img-bordered" alt="Context menu for a selected commit showing the option to recompose a series of commits with AI." />
  <figcaption style="text-align: center; color: #888">Recompose an existing range of commits.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/commit-composer-UI.png" srcset="/wp-content/uploads/commit-composer-UI@2x.png"  class="help-center-img img-bordered" alt="Commit Composer interface showing options to pick, squash, or reword each commit in a sequence." />
  <figcaption style="text-align: center; color: #888">Made adjustments, and confirm to create commits.</figcaption>
</figure>

### Rules for composing commits

- If composing from the WIP node, ensure it's selected and use the WIP panel (top right).
- If composing from existing commits:
  - Selected commits must be contiguous and part of the current branch.
  - There must be no merge commits between (and including) the branch head commit and the parent of the oldest selected commit.

> **Tip**: Need to reverse the composed commits? Use the **Undo** button in the toolbar to undo any AI Commit Compose or Recompose commits with AI action. 

***

## AI-Powered Commit Explain

GitKraken can generate natural language explanations of your commits directly from the UI.

### How to use Commit Explain

1. Open GitKraken Desktop and select one or more commits (Use <kbd>Shift</kbd> or <kbd>Ctrl/Cmd</kbd>).

<figure>
<img src="/wp-content/uploads/gkd-11-Select-Commits.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Highlighted selection of multiple commits in the GitKraken commit graph." />
<figcaption style="text-align: center; color: #888">Select one or more commits from the commit graph</figcaption>
</figure>

2. Click the **Explain** button in the top-right corner of the Commit Panel.

<figure>
<img src="/wp-content/uploads/gkd-11-AI-Explain.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Merged diff view of selected commits in GitKraken, with the Explain button highlighted for AI assistance." />
<figcaption style="text-align: center; color: #888">Use the Explain button to trigger AI-generated summaries</figcaption>
</figure>

3. GitKraken provides an AI-generated summary of what changed in that commit.

<figure>
<img src="/wp-content/uploads/gkd-11-commit-explain-2.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="AI-generated summary and changelog for multiple commits, shown in the Commit Panel of GitKraken." />
<figcaption style="text-align: center; color: #888">AI-generated explanation appears in the Commit Panel</figcaption>
</figure>

***

## AI-Generated Commit Messages

Generate clear, consistent commit messages based on your staged changes.

### How to generate a commit message

1. Stage your changes.

<figure>
<img src="/wp-content/uploads/gkd-11-stage-changes.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Commit Panel interface showing one unstaged file with the Stage File button highlighted." />
<figcaption style="text-align: center; color: #888">Stage your changes in the Commit Panel</figcaption>
</figure>

2. Click the **AI** button near the commit message input.

<figure>
<img src="/wp-content/uploads/gkd-11-commit-message-generation-1.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Commit Panel showing a staged file and a highlighted button for generating an AI commit message." />
<figcaption style="text-align: center; color: #888">Click the AI button to generate a commit message</figcaption>
</figure>

3. GitKraken suggests a summary and description, which you can review and edit.

<figure>
<img src="/wp-content/uploads/gkd-11-commit-message-generation-2.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="AI-generated commit summary and description shown in the Commit Panel." />
<figcaption style="text-align: center; color: #888">Review and edit the suggested commit message</figcaption>
</figure>

***

### Amend commit messages

To amend the most recent commit message:
1. Select the commit in the graph.
2. Click into its message box in the Commit Panel.

<figure>
<img src="/wp-content/uploads/amend-recent-commit-ai-2025.png" srcset="/wp-content/uploads/amend-recent-commit-ai-2025@2x.png" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Edit window open showing amended commit message and description using AI-suggested content." />
<figcaption style="text-align: center; color: #888">Select and edit the latest commit message</figcaption>
</figure>

You can then use the AI button again to generate a revised commit message.

<figure>
<img src="/wp-content/uploads/generate-ai-amend-message.png" srcset="/wp-content/uploads/generate-ai-amend-message@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Commit panel showing AI-assisted generation of an amended commit message and description." />
<figcaption style="text-align: center; color: #888">Use AI to regenerate an updated commit message</figcaption>
</figure>

***

## Explain Branch Changes with AI

Right-click any branch or `HEAD` commit and select **Explain Branch Changes** to generate a summary of all changes introduced on that branch.

<figure>
  <img src="/wp-content/uploads/explain-branch.png" srcset="/wp-content/uploads/explain-branch@2x.png" class="help-center-img img-bordered" alt="Context menu in GitKraken showing the Explain Branch Changes option for generating AI-based summaries of branch differences." />
  <figcaption style="text-align: center; color: #888">Right-click a branch or HEAD commit to explain changes.</figcaption>
</figure>

GitKraken AI selects all commits on the branch and compares the base commit to the `HEAD` commit. It uses this diff to generate change and impact summaries.

<figure>
  <img src="/wp-content/uploads/explain-branch-summaries.png" srcset="/wp-content/uploads/explain-branch-summaries@2x.png" class="help-center-img img-bordered" alt="AI-generated explanation panel in GitKraken summarizing branch changes, grouped by commit with a detailed breakdown of updates and their impact." />
  <figcaption style="text-align: center; color: #888">GitKraken AI summarizes the diff between the base and HEAD commits.</figcaption>
</figure>

To customize how **Explain Branch Changes** works, go to **Preferences > GitKraken AI > Explain Changes**.

***
## AI-Powered Merge Conflict Resolution

Resolve merge conflicts faster with GitKraken AI.

When you encounter a merge conflict, click into the conflicted file as usual. You’ll now see a new **Auto-resolve with AI** button that offers a context-aware resolution.

<figure>
<img src="/wp-content/uploads/Auto-resolve-with-AI-2025.png" srcset='/wp-content/uploads/Auto-resolve-with-AI-2025@2x.png 2x' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken merge conflict view showing AI-generated summary and resolution suggestions with confidence scores." />
<figcaption style="text-align: center; color: #888">Click 'Auto-resolve with AI' to generate a suggested resolution</figcaption>
</figure>

GitKraken AI analyzes the conflicting code and proposes a solution, complete with:

- A detailed explanation of the proposed resolution
- A confidence level for each conflicted hunk

You stay in control—review the AI output, make edits, or choose to accept or discard the changes. Use the confidence levels to decide which hunks might need more manual review.

### Customize Conflict Resolution Prompts

Want to fine-tune how AI handles your merge conflicts? You can add your own instructions for conflict resolution behavior.

Go to: <kbd>Preferences > GitKraken AI > Conflict Resolution</kbd>

<figure>
<img src="/wp-content/uploads/custom-instructions-conflict-resolution-2025.png" srcset='/wp-content/uploads/custom-instructions-conflict-resolution-2025@2x.png 2x' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken AI settings panel with editable fields for customizing instructions related to stash messages, pull requests, and conflict resolution." />
<figcaption style="text-align: center; color: #888">Set custom AI instructions for merge conflict resolution</figcaption>
</figure>

### Note on Preview Status

This feature is currently in **Preview**. It's live and functional, but still evolving. 

If GitKraken AI nails the merge, great! If it misses the mark, please share your experience or suggestions at [feedback.gitkraken.com](https://feedback.gitkraken.com).


***
## AI-Generated Stash Messages

Similar to commit messages, you can generate stash messages based on staged changes.

### How to generate a stash message

1. Stage your changes.

<figure>
<img src="/wp-content/uploads/gkd-11-stage-changes.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="File change view in GitKraken showing 'Stage File' button next to an unstaged markdown file on the main branch." />
<figcaption style="text-align: center; color: #888">Stage your changes for stashing</figcaption>
</figure>

2. Click the stash icon next to the "Commit" tab and then click the **AI** button.

<figure>
<img src="/wp-content/uploads/stash-ai-message.png" srcset="/wp-content/uploads/stash-ai-message@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Stash message input section with highlighted AI button labeled 'Generate a stash message with AI'." />
<figcaption style="text-align: center; color: #888">Use the AI button to generate a stash message</figcaption>
</figure>

3. GitKraken AI generates a stash message, which you can review and edit.

<figure>
<img src="/wp-content/uploads/stash-message-generated-2025.png" srcset="/wp-content/uploads/stash-message-generated-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Stash message input field populated with AI-generated text, 'Adds documentation for AI-generated stash messages feature.'" />
<figcaption style="text-align: center; color: #888">Review and edit the AI-generated stash message</figcaption>
</figure>

***

## AI-Generated Pull Request Title and Description

When connected to [GitHub, GitLab, Bitbucket, or Azure DevOps](/gitkraken-desktop/integrations/), you can use GitKraken AI to create a pull request with a generated title and description based on the incoming changes.

### How to generate a PR title and description

1. Create a pull request from the Left Panel or by drag-and-dropping a branch onto another.

<figure>
<img src="/wp-content/uploads/create-pr-v11-1-Q2-2025.png" srcset="/wp-content/uploads/create-pr-v11-1-Q2-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Sidebar showing pull request filters and a highlighted 'Create Pull Request' button." />
<figcaption style="text-align: center; color: #888">Start creating a pull request from the Left Panel or graph</figcaption>
</figure>

2. Click **Generate title and description**. If using [pull request templates](/gitkraken-desktop/pull-requests/#pull-request-templates), select the template first—GitKraken AI will apply it.

<figure>
<img src="/wp-content/uploads/pr-ai-title-desc-11-1.png" srcset="/wp-content/uploads/pr-ai-title-desc-11-1@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Pull request creation panel with an AI button to generate a title and description based on branch changes." />
<figcaption style="text-align: center; color: #888">Click the AI button to generate a pull request title and description</figcaption>
</figure>

3. GitKraken provides a suggested title and description for your PR.

<figure>
<img src="/wp-content/uploads/pr-ai-title-and-description.png" srcset="/wp-content/uploads/pr-ai-title-and-description@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Pull request form showing auto-generated title and description summarizing recent documentation changes." />
<figcaption style="text-align: center; color: #888">Review and edit the AI-generated title and description</figcaption>
</figure>


***

## Bring Your Own Key

By default, GitKraken AI uses **Gemini** to power commit explanations and message generation. No API key is needed and usage is included with your GitKraken subscription.

If you prefer using your own API key with **OpenAI**, **Azure**, **Anthropic**, or a **Custom URL**, you can configure this in:

<kbd>Preferences > GitKraken AI</kbd>

<figure>
<img src="/wp-content/uploads/gkd-11-Preferences-GitKraken-AI.png" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Preferences panel in GitKraken showing options to enable AI, select provider, and customize commit message instructions." />
<figcaption style="text-align: center; color: #888">Configure GitKraken AI providers in Preferences</figcaption>
</figure>

### Custom API Endpoint

For users with advanced security requirements, you may use a **Custom URL** to direct AI requests to a private or internal service.

This endpoint can handle:
- Commit explanations
- Commit and stash message generation
- Pull request title and description generation
- Conflict Resolution
- Commit Composer

<figure>
<img src="/wp-content/uploads/custom-url-11-1.png" srcset="/wp-content/uploads/custom-url-11-1@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Custom AI provider settings in GitKraken showing provider, endpoint URL, token limit, and API key fields." />
<figcaption style="text-align: center; color: #888">Example of configuring a custom AI endpoint</figcaption>
</figure>

The Custom URL option is ideal for developers connecting to local AI models or private endpoints. For example, you might connect to models hosted with Ollama, Hugging Face, OpenRouter, or an OpenAI-compatible service like LM Studio. 

However, GitKraken does not validate or debug third-party implementations. If the connection works, great, but if it doesn’t, we’re unable to troubleshoot issues with custom endpoints.

### Custom AI Prompt Instructions

Guide how GitKraken AI responds for specific scenarios like:
- Commit Message Generation
- Commit Explanations
- Stash Message Generation
- Pull Request Title/Description
- Conflict Resolution
- Commit Composer

<figure>
<img src="/wp-content/uploads/gkd-11-custom-instructions.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Custom instruction fields in GitKraken AI settings for commit message generation and commit explanations." />
<figcaption style="text-align: center; color: #888">Add custom AI instructions for personalized responses</figcaption>
</figure>

#### Commit Prompt Examples

Need help crafting instructions? Try these examples:

**Prompt for brevity**
```
Keep the summary short, but informative
```

**Prompt to add conventional commit prefix**
```
Format the summary as:

<type>: <summary>

Where <type> is one of:
  feat, fix, docs, style, refactor, perf, test, chore

<summary> should be a short, 72-character max imperative phrase.
Only return the final commit message—no extra formatting.
```
***

## Organization-wide AI Administration

To disable GitKraken AI, restrict which AI models are available, or set up organization-wide API keys and custom URLs, see the [GitKraken Dev Security Controls](https://help.gitkraken.com/gk-dev/gk-dev-security-controls/).

You can disable Gitkraken AI locally via <kbd>Preferences > GitKraken AI</kbd>. Keep in mind this setting is not enforced at the organization level and can be re-enabled by individual users.
***

## What’s Next?

Additional AI-powered features are in development to further streamline your workflow. GitKraken AI is built to reduce friction while keeping you in control.

<div class='callout callout--basic'>
    <p>Have more questions about GitKraken AI? Visit our <a href="https://help.gitkraken.com/general/gitkraken-ai-faq">GitKraken AI FAQ page</a> for details.</p>
</div>
