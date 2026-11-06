---
title: GitKraken AI Features Overview
description: Use GitKraken AI to generate commit messages, PR descriptions, and explanations of code changes. Customize your AI provider and prompts to fit your workflow.
product: GitKraken AI
feature: GitKraken AI
content_type: overview
audience: developer
plan_required: Pro
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps]
hosted_variant: both
status: preview
last_verified: 2026-11
llms_include: true
tags: [ai, commit-messages, explain, pull-requests, providers]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "gkd-gitkraken-ai"
    nav_label: "GitKraken AI"
    nav_order: 100
    nav_parent: ""
    page_type: "content"
---

<kbd>Last updated: November 2026</kbd>

<div style="display:flex; flex-wrap:wrap; align-items:center; gap:8px 32px; margin-bottom:24px;">
  <p style="flex:1 1 300px; margin:0;">GitKraken AI in GitKraken Desktop helps developers generate commit messages, explain commits and branches, draft pull request text, resolve merge conflicts, and customize AI providers and prompts. Use this page to understand which AI workflows are available, when to use them, and which features require a paid GitKraken subscription.</p>
  <img src="/wp-content/uploads/GitKraken_Keif_ai-robot.png" alt="" width="748" height="750" loading="lazy" style="flex:0 0 auto; max-height:200px; width:auto; height:auto; max-width:100%; margin:0 auto;">
</div>

<div class='callout callout--warning'>
    <p>GitKraken AI requires a <a href="https://www.gitkraken.com/pricing?source=help_center&product=gitkraken" target="_blank">paid GitKraken subscription</a>.</p>
</div>

**Requirements and limits**
- Product: GitKraken Desktop with GitKraken AI enabled
- Plan: Paid GitKraken subscription required
- Setup location: <kbd>Preferences &gt; GitKraken AI</kbd> for provider, model, and prompt settings
- Preview feature on this page: AI Commit Composer

Status, plan, and setup location for each feature:

| Feature | What it generates or does | Status | Plan | Setup location |
|---------|----------------------------|--------|------|----------------|
| AI Commit Message | Commit message suggestions from staged changes | GA | Paid subscription | Commit Panel |
| AI Commit Composer | Compose or recompose commits into a cleaner history | Preview | Paid subscription | Commit Panel |
| AI Explain | Natural-language explanations of commits and branches | GA | Paid subscription | Commit Graph and context menus |
| AI Pull Request Description | Draft pull request summaries and descriptions | GA | Paid subscription | Pull request description field |
| AI provider and prompt settings | Model, provider, and prompt customization | GA | Paid subscription | <kbd>Preferences &gt; AI</kbd> |

***

<div class='callout callout--warning'>
  <p><strong>GitKraken On-Premise users:</strong> The default GitKraken-hosted AI provider is not available in Serverless or Self-Hosted Server deployments. To use GitKraken AI in an on-premises environment, you must configure a Custom URL that points to a private or internal AI service. See <a href="#how-to-use-a-custom-api-endpoint">How to use a custom API endpoint</a> for setup steps.</p>
</div>

## Quick Start

**To generate a commit message:**
1. Stage your changes in the Commit Panel.
2. Click the AI icon (sparkle) next to the commit message field.
3. Review the suggested message and adjust as needed before committing.

**To compose commits with AI from staged changes:**
1. Stage your changes, then click **Compose commits with AI** in the Commit Panel.
2. Review the commits GitKraken AI proposes. Reorder, squash, or edit their messages in the Commit Composer.
3. Click **Create Commits** to apply, or **Cancel** to discard.

**To recompose existing commits:**
1. Select a contiguous range of commits in the graph using <kbd>Shift</kbd> or <kbd>Cmd</kbd>/<kbd>Ctrl</kbd>.
2. Right-click the selection and choose **Recompose _n_ commits with AI**, or click **Recompose commits with AI** in the Commit Panel.
3. Adjust the proposed structure and click **Create Commits**.

**To generate a pull request description:**
- When you create a pull request, click **Generate title and description** to generate a summary of your changes.

To use a custom AI provider or customize the prompts, go to <kbd>Preferences > AI</kbd>.

***

## How to compose and recompose commits with AI (Preview)

Use AI to help organize your Git commits into clear, logical stories. To clean up commits a coding agent made before you open a pull request, see [Clean Up AI Coding Agent Commits Before Review](/gitkraken-desktop/clean-up-agent-commits/).

When you recompose commits, GitKraken AI keeps the original commit authors and adds co-authors when a new commit combines work from more than one person. While GitKraken AI composes, the progress notification shows the current stage and the number of files and hunks.

<div class='callout callout--basic'>
  <p><strong>Use AI Commit Composer when:</strong> your staged changes or recent commits need to be reorganized into a clearer narrative before you share them. <strong>Do not use it when:</strong> your commits are already atomic and you only need a quick manual message update.</p>
</div>

### What AI Commit Composer does

The AI-powered Commit Composer can:

- Break up unstaged changes into meaningful commits.
- Recompose selected previous commits into a new structure.
- Reorder, squash, or edit commit messages before pushing.

<figure>
  <img src="/wp-content/uploads/before-after-commit-compose@2x.png" class="help-center-img img-bordered" alt="GitKraken interface showing a selected range of commits before and after being composed into a cleaner history." />
  <figcaption style="text-align: center; color: #888">AI Commit Composer button in the Commit Panel</figcaption>
</figure>

### How to use AI Commit Composer

To generate commits with AI:

- **For uncommitted changes**:
  1. Stage your changes.
  2. In the Commit Panel, click **Compose commits with AI**.
  3. Review the results in the Commit Composer, which opens when GitKraken AI finishes composing the new commits:
     - You can reorder, squash, or edit the commit messages.
     - GitKraken Desktop does not update the branch until you click **Create Commits**.
     - To cancel the process, click **Cancel**.
     - To undo any changes made during composition (such as reordering or squashing), click **Reset**.

<figure>
  <img src="/wp-content/uploads/compose-WIP@2x.png" class="help-center-img img-bordered" alt="Selected WIP commits in GitKraken UI with arrow pointing to the 'Compose commits with AI' button in the commit panel." />
  <figcaption style="text-align: center; color: #888">Compose commits from your WIP.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/compose-WIP-UI@2x.png" class="help-center-img img-bordered" alt="Commit Composer composing 3 commits, each set to Pick in its dropdown." />
  <figcaption style="text-align: center; color: #888">Make adjustments, then confirm to create commits.</figcaption>
</figure>

- **For existing committed changes**:
  1. In the Commit Graph, select a contiguous range of commits using <kbd>Shift</kbd> or <kbd>Cmd</kbd>/<kbd>Ctrl</kbd>.
  2. Do one of the following:
     - Right-click the selection and choose **Recompose _n_ commits with AI** from the context menu.
     - Click **Recompose commits with AI** in the Commit Panel.
  3. Review the results in the Commit Composer, which opens when GitKraken AI finishes composing the new commits:
     - You can reorder, squash, or edit the commit messages.
     - GitKraken Desktop does not update the branch until you click **Create Commits**.
     - To cancel the process, click **Cancel**.
     - To undo any changes made during composition (such as reordering or squashing), click **Reset**.

<figure>
  <img src="/wp-content/uploads/compose-existing-commits@2x.png" class="help-center-img img-bordered" alt="Context menu for a selected commit showing the option to recompose a series of commits with AI." />
  <figcaption style="text-align: center; color: #888">Recompose an existing range of commits.</figcaption>
</figure>

<figure>
  <img src="/wp-content/uploads/commit-composer-UI@2x.png"  class="help-center-img img-bordered" alt="Commit Composer interface showing options to pick, squash, or reword each commit in a sequence." />
  <figcaption style="text-align: center; color: #888">Make adjustments, then confirm to create commits.</figcaption>
</figure>

### Commit selection rules for AI composition

- To compose from uncommitted changes, select the WIP node and use the Commit Panel.
- To compose from existing commits:
  - Selected commits must be contiguous and part of the current branch.
  - The range from the branch head commit to the parent of the oldest selected commit, inclusive, must contain no merge commits.

> **Tip**: To reverse composed commits, click **Undo** in the toolbar. **Undo** reverses a compose or recompose action.

***

## How to explain commits with AI

GitKraken AI explains in plain language what changed in the commits you select.

<div class='callout callout--basic'>
  <p><strong>Use AI Explain when:</strong> you need a fast summary of what changed in one or more commits. <strong>Do not use it when:</strong> you need authoritative implementation details that should come directly from reading the diff yourself.</p>
</div>

### How to use AI Commit Explain

1. In the Commit Graph, select one or more commits. Hold <kbd>Shift</kbd> or <kbd>Ctrl/Cmd</kbd> to select more than one. To explain 3 or more commits, select a contiguous range. For any other selection of 3 or more items, the Commit Panel shows **A combined diff is not shown for this selection** and offers no explain button.

<figure>
<img src="/wp-content/uploads/gkd-11-Select-Commits.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Highlighted selection of multiple commits in the GitKraken commit graph." />
<figcaption style="text-align: center; color: #888">Select one or more commits from the commit graph</figcaption>
</figure>

2. Click **Explain commits** (or **Explain commit** for a single commit) in the top-right corner of the Commit Panel.

<figure>
<img src="/wp-content/uploads/gkd-ai-explain-commits-01-v3@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="The Commit Panel in GitKraken Desktop with three consecutive commits selected: the header reads 3 commits selected with an Explain commits button, followed by Viewing diff of 3 commits and the three commits." />
<figcaption style="text-align: center; color: #888">Use the Explain button to trigger AI-generated summaries</figcaption>
</figure>

3. Read the summary GitKraken AI generates of what changed in the selected commits.

<figure>
<img src="/wp-content/uploads/gkd-11-commit-explain-2.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="AI-generated summary and changelog for multiple commits, shown in the Commit Panel of GitKraken." />
<figcaption style="text-align: center; color: #888">AI-generated explanation appears in the Commit Panel</figcaption>
</figure>

***

## How to generate commit messages with AI

Generate clear, consistent commit messages based on your staged changes.

<div class='callout callout--basic'>
  <p><strong>Use AI commit messages when:</strong> you want a strong starting point for summarizing staged changes. <strong>Do not use them when:</strong> the exact wording carries team-specific meaning and you already know the final message you need to write.</p>
</div>

### How to generate an AI commit message

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

3. Review and edit the summary and description that GitKraken AI suggests.

<figure>
<img src="/wp-content/uploads/gkd-11-commit-message-generation-2.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="AI-generated commit summary and description shown in the Commit Panel." />
<figcaption style="text-align: center; color: #888">Review and edit the suggested commit message</figcaption>
</figure>

***

### How to amend commit messages with AI

To amend the most recent commit message:
1. Select the commit in the graph.
2. Click its commit message in the Commit Panel.

<figure>
<img src="/wp-content/uploads/amend-recent-commit-ai-2025@2x.png" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Edit window open showing amended commit message and description using AI-suggested content." />
<figcaption style="text-align: center; color: #888">Select and edit the latest commit message</figcaption>
</figure>

Then click the **AI** button to generate a revised commit message.

<figure>
<img src="/wp-content/uploads/generate-ai-amend-message@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Commit panel showing AI-assisted generation of an amended commit message and description." />
<figcaption style="text-align: center; color: #888">Use AI to regenerate an updated commit message</figcaption>
</figure>

***

## How to explain branch changes with AI

Right-click any branch or `HEAD` commit and select **Explain Branch Changes** to generate a summary of all changes introduced on that branch.

<div class='callout callout--basic'>
  <p><strong>Use Explain Branch Changes when:</strong> you want a high-level summary before review, handoff, or pull request writing. <strong>Do not use it when:</strong> you need to inspect exact file-level behavior instead of a summarized narrative.</p>
</div>

<figure>
  <img src="/wp-content/uploads/explain-branch@2x.png" class="help-center-img img-bordered" alt="Context menu in GitKraken showing the Explain Branch Changes option for generating AI-based summaries of branch differences." />
  <figcaption style="text-align: center; color: #888">Right-click a branch or HEAD commit to explain changes.</figcaption>
</figure>

GitKraken AI selects all commits on the branch and summarizes the changes and their impact, based on the diff between the branch's base commit and its `HEAD` commit.

<figure>
  <img src="/wp-content/uploads/explain-branch-summaries@2x.png" class="help-center-img img-bordered" alt="AI-generated explanation panel in GitKraken summarizing branch changes, grouped by commit with a detailed breakdown of updates and their impact." />
  <figcaption style="text-align: center; color: #888">GitKraken AI summarizes the diff between the base and HEAD commits.</figcaption>
</figure>

To customize how **Explain Branch Changes** works, go to <kbd>Preferences > GitKraken AI > Explain Changes</kbd>.

***
## How to resolve merge conflicts with AI

GitKraken AI can suggest a resolution for a merge conflict. To combine the branches of two coding agents that worked in parallel, see [Resolve Merge Conflicts Between AI Agent Branches](/gitkraken-desktop/agent-merge-conflicts/).

<div class='callout callout--basic'>
  <p><strong>Use AI conflict resolution when:</strong> you want a suggested starting point for resolving a conflict and plan to review the result carefully. <strong>Do not use it when:</strong> the conflict involves sensitive logic or policy decisions that require a fully manual resolution.</p>
</div>

When you hit a merge conflict, open the conflicted file, then click **Auto-resolve with AI** to get a suggested resolution.

<figure>
<img src="/wp-content/uploads/Auto-resolve-with-AI-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken merge conflict view showing AI-generated summary and resolution suggestions with confidence scores." />
<figcaption style="text-align: center; color: #888">Click 'Auto-resolve with AI' to generate a suggested resolution</figcaption>
</figure>

GitKraken AI analyzes the conflicting code and proposes a resolution that includes:

- A detailed explanation of the proposed resolution
- A confidence level for each conflicted hunk

Review the result, edit it if needed, then accept or discard the changes. Use the confidence levels to decide which hunks need closer manual review.

### How to customize conflict resolution prompts

To change how GitKraken AI resolves merge conflicts, add your own instructions in <kbd>Preferences > GitKraken AI > Conflict Resolution</kbd>.

<figure>
<img src="/wp-content/uploads/custom-instructions-conflict-resolution-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken AI settings panel with editable fields for customizing instructions related to stash messages, pull requests, and conflict resolution." />
<figcaption style="text-align: center; color: #888">Set custom AI instructions for merge conflict resolution</figcaption>
</figure>

### Preview status for AI conflict resolution

AI conflict resolution is in **Preview**. To share your experience or suggestions, visit [feedback.gitkraken.com](https://feedback.gitkraken.com).


***
## How to generate stash messages with AI

GitKraken AI can generate a stash message from your staged changes, as it does for commit messages.

### How to generate an AI stash message

1. Stage your changes.

<figure>
<img src="/wp-content/uploads/gkd-11-stage-changes.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="File change view in GitKraken showing 'Stage File' button next to an unstaged markdown file on the main branch." />
<figcaption style="text-align: center; color: #888">Stage your changes for stashing</figcaption>
</figure>

2. Click the stash icon next to the "Commit" tab and then click the **AI** button.

<figure>
<img src="/wp-content/uploads/stash-ai-message@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Stash message input section with highlighted AI button labeled 'Generate a stash message with AI'." />
<figcaption style="text-align: center; color: #888">Use the AI button to generate a stash message</figcaption>
</figure>

3. Review and edit the stash message that GitKraken AI generates.

<figure>
<img src="/wp-content/uploads/stash-message-generated-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Stash message input field populated with AI-generated text, 'Adds documentation for AI-generated stash messages feature.'" />
<figcaption style="text-align: center; color: #888">Review and edit the AI-generated stash message</figcaption>
</figure>

***

## How to generate pull request titles and descriptions with AI

When GitKraken Desktop is connected to [GitHub, GitLab, Bitbucket, or Azure DevOps](/gitkraken-desktop/integrations/), you can use GitKraken AI to create a pull request with a generated title and description based on the incoming changes.

### How to generate an AI pull request title and description

1. Create a pull request from the Left Panel or by dragging a branch onto another branch.

<figure>
<img src="/wp-content/uploads/create-pr-v11-1-Q2-2025@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Sidebar showing pull request filters and a highlighted 'Create Pull Request' button." />
<figcaption style="text-align: center; color: #888">Start creating a pull request from the Left Panel or graph</figcaption>
</figure>

2. Click **Generate title and description**. If you use a [pull request template](/gitkraken-desktop/pull-requests/#pull-request-templates), select the template first. GitKraken AI applies it.

<figure>
<img src="/wp-content/uploads/pr-ai-title-desc-11-1@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Pull request creation panel with an AI button to generate a title and description based on branch changes." />
<figcaption style="text-align: center; color: #888">Click the AI button to generate a pull request title and description</figcaption>
</figure>

3. Review and edit the title and description that GitKraken AI suggests.

<figure>
<img src="/wp-content/uploads/pr-ai-title-and-description@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Pull request form showing auto-generated title and description summarizing recent documentation changes." />
<figcaption style="text-align: center; color: #888">Review and edit the AI-generated title and description</figcaption>
</figure>


***

## How to use your own AI provider key

By default, GitKraken AI uses **[Google Gemini Models](https://deepmind.google/models/gemini/)** to power commit explanations and message generation. No API key is needed and usage is included with your GitKraken subscription.

You can pick the model for each AI feature in <kbd>Preferences > GitKraken AI</kbd>. With the GitKraken-hosted provider, each model in the dropdown shows its AI credit multiplier after its name, such as **4.5x**. Hover over the multiplier to see what it means, for example **Uses 4.5x the credits of a baseline model**. A model with a higher multiplier uses your weekly AI credits faster. Models you use with your own API key show no multiplier.

<figure>
<img src="/wp-content/uploads/gkd-ai-model-credit-multiplier-01-v2@2x.png" style="max-width: 50%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="An open AI model dropdown listing GitKraken-hosted models with their AI credit multiplier after each name, such as 0.8x for Gemini 2.5 Flash and 4.5x for Claude Sonnet 4.5." />
<figcaption style="text-align: center; color: #888">Each GitKraken-hosted model shows its AI credit multiplier</figcaption>
</figure>

To use your own API key with **OpenAI**, **Azure**, **Anthropic**, **Google Gemini**, or a **Custom URL**, configure it in <kbd>Preferences > GitKraken AI</kbd>.

<figure>
<img src="/wp-content/uploads/gkd-11-preferences-gitkraken-ai-01-v2@2x.png" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="GitKraken Desktop Preferences > GitKraken AI with Use your own API Key to make AI requests checked and its section highlighted: Provider set to OpenAI, optional Endpoint URL, Provider API Key and Test Connection." />
<figcaption style="text-align: center; color: #888">Configure GitKraken AI providers in Preferences</figcaption>
</figure>

### How to use a custom API endpoint

If you have advanced security requirements, use a **Custom URL** to send AI requests to a private or internal service.

<div class='callout callout--basic'>
  <p><strong>GitKraken On-Premise users:</strong> If you are running GitKraken On-Premise Serverless or Self-Hosted Server, the default hosted provider is not reachable from your network. Custom URL is the only supported AI configuration in those environments.</p>
</div>

A Custom URL endpoint can handle:
- Commit explanations
- Commit and stash message generation
- Pull request title and description generation
- Conflict resolution
- Commit Composer

<figure>
<img src="/wp-content/uploads/custom-url-11-1@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Custom AI provider settings in GitKraken showing provider, endpoint URL, credit limit, and API key fields." />
<figcaption style="text-align: center; color: #888">Example of configuring a custom AI endpoint</figcaption>
</figure>

Use a Custom URL to connect to local AI models or private endpoints, for example models hosted with Ollama, Hugging Face, OpenRouter, or an OpenAI-compatible service like LM Studio.

GitKraken does not validate, debug, or troubleshoot third-party implementations, including custom endpoints.

### How to customize AI prompts

Add custom instructions in <kbd>Preferences > GitKraken AI</kbd> to guide how GitKraken AI responds. Each of these sections has its own instructions:
- Global Instructions
- Commit Message Generation
- Explain Changes
- Stash Message Generation
- Pull Request
- Conflict Resolution
- Commit Composer

<figure>
<img src="/wp-content/uploads/gkd-11-custom-instructions.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="Custom instruction fields in GitKraken AI settings for commit message generation and commit explanations." />
<figcaption style="text-align: center; color: #888">Add custom AI instructions for personalized responses</figcaption>
</figure>

#### Commit Prompt Examples

Try these example instructions for commit messages:

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

## How to manage GitKraken AI for an organization

To disable GitKraken AI, restrict which AI models are available, or set up organization-wide API keys and custom URLs, see the [GitKraken Dev Security Controls](https://help.gitkraken.com/gk-dev/gk-dev-security-controls/).

To turn off GitKraken AI on your own machine, clear **Enable GitKraken AI** in <kbd>Preferences > GitKraken AI</kbd>. Your organization does not enforce this setting, so each user can turn GitKraken AI back on.

If your organization's admin set an API key for your AI provider, the **Provider API Key** field in <kbd>Preferences > GitKraken AI</kbd> is disabled and the key stays hidden. Hover over the field to see **API key configured by your organization's admin**.

### What happens when you reach the weekly AI limit

When a request goes above the weekly AI usage included in your plan or trial, GitKraken Desktop shows **GitKraken AI Weekly Limit Reached**. What the message offers depends on your account:

- **Trial or free users:** Click **Upgrade GitKraken** to purchase a GitKraken plan.
- **Paid organization owners and admins:** Click **Purchase more AI credits** to add AI credits for your organization.
- **Paid organization members:** Contact your organization admin or owner to request more AI credits.

### How to keep or turn off GitKraken AI when you stop using it

If you have a paid plan and have not used GitKraken AI for 14 days, GitKraken Desktop shows the **You're in control of GitKraken AI** dialog once. Choose one option:

- **Keep GitKraken AI On:** AI features stay available. Click **Keep AI On**.
- **Turn GitKraken AI Off:** GitKraken Desktop hides all AI buttons and menu options and sends no AI requests. Click **Turn AI Off**.

To close the dialog without changing anything, click **Decide Later**. You can change this setting at any time in <kbd>Preferences > GitKraken AI</kbd>.

<figure>
<img src="/wp-content/uploads/gkd-ai-control-reminder-01-v2@2x.png" style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" alt="The You're in control of GitKraken AI dialog in GitKraken Desktop, noting that GitKraken AI features have not been used in the last 14 days, with two options: Keep GitKraken AI On (Current setting), listing its benefits, and Turn GitKraken AI Off, listing what turning it off does, plus Decide Later and Keep AI On buttons." />
<figcaption style="text-align: center; color: #888">Keep GitKraken AI on or turn it off</figcaption>
</figure>
***

## What’s Next?

<div class='callout callout--basic'>
    <p>Have more questions about GitKraken AI? See the <a href="https://help.gitkraken.com/general/gitkraken-ai-faq">GitKraken AI FAQ</a>.</p>
</div>

