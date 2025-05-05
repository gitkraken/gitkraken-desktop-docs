---

title: GitKraken AI
description: Generate plain text commit explanations and more with GitKraken AI
taxonomy:
    category: gitkraken-desktop

---
<kbd>Last updated: May 2025</kbd>

Let the app handle the boring parts! GitKraken offers built-in AI features to fast track your code contributions.

<div class='callout callout--warning'>
    <p>GitKraken AI requires a paid GitKraken subscription.</p>
</div>

## AI-Powered Commit Explain

GitKraken can generate natural language explanations of your commits, right from the UI.

### How to use Commit Explain

1. Open GitKraken Desktop and select one or more commits (Use <kbd>Shift</kbd> or <kbd>Ctrl/Cmd</kbd>)

<img src="/wp-content/uploads/gkd-11-Select-Commits.png" class="help-center-img img-bordered">

2. Click the **Explain** button in the top-right corner of the Commit Panel.  

<img src="/wp-content/uploads/gkd-11-AI-Explain.png" class="help-center-img img-bordered">

3. GitKraken provides an AI-generated summary of what changed in that commit.

<img src="/wp-content/uploads/gkd-11-commit-explain-2.png" class="help-center-img img-bordered">

## AI-Generated Commit Messages

You can generate clear, consistent commit messages based on your staged changes.

### How to generate a commit message

1. Stage your changes. 

<img src="/wp-content/uploads/gkd-11-stage-changes.png" class="help-center-img img-bordered">

2. Click the **AI** button near the commit input.

<img src="/wp-content/uploads/gkd-11-commit-message-generation-1.png" class="help-center-img img-bordered">

3. GitKraken suggests a summary and description, which you can review and edit.

<img src="/wp-content/uploads/gkd-11-commit-message-generation-2.png" class="help-center-img img-bordered">

### Amend commit messages

You may amend the most recent commit message by selecting the commit in the graph, and then clicking into its message box in the Commit Panel.

<img src="/wp-content/uploads/amend-recent-commit-ai-2025.png" srcset="/wp-content/uploads/amend-recent-commit-ai-2025@2x.png" class="help-center-img img-bordered">

Similar to commit messages, you may use AI to generate an updated commit message and description for your amended commit. 

<img src="/wp-content/uploads/generate-ai-amend-message.png" srcset="/wp-content/uploads/generate-ai-amend-message@2x.png" class="help-center-img img-bordered">

## AI-Generated Stash Messages

Similar to commit messages, you can generate stash messages based on the staged changes. 

### How to generate a stash message

1. Stage your changes. 

<img src="/wp-content/uploads/gkd-11-stage-changes.png" class="help-center-img img-bordered">

2. Click on the stash icon next to the "Commit" tab and then click the **AI** button.

<img src="/wp-content/uploads/stash-ai-message.png" srcset="/wp-content/uploads/stash-ai-message@2x.png" class="help-center-img img-bordered">

3. GitKraken AI generates a stash message, which you can review and edit.

<img src="/wp-content/uploads/stash-message-generated-2025.png" srcset="/wp-content/uploads/stash-message-generated-2025@2x.png" class="help-center-img img-bordered">

## AI-Generated Pull Request Title and Description

When connected to [GitHub, GitLab, Bitbucket, or Azure DevOps](/gitkraken-desktop/integrations/), you get the ability to create a pull request from inside GitKraken Desktop. Use AI to populate the title and description based on the incoming changes. 

### To generate a PR title and description:

1. Create a pull request from the Left Panel or by drag and dropping a branch to another branch. 

<img src="/wp-content/uploads/create-pr-v11-1-Q2-2025.png" srcset="/wp-content/uploads/create-pr-v11-1-Q2-2025@2x.png" class="help-center-img img-bordered">

2. Click the **Generate title and descritption** button. If using [pull request templates](/gitkraken-desktop/pull-requests/#pull-request-templates), be sure to first select your template and GitKraken AI will apply it. 

<img src="/wp-content/uploads/pr-ai-title-desc-11-1.png" srcset="/wp-content/uploads/pr-ai-title-desc-11-1@2x.png" class="help-center-img img-bordered">

3. GitKraken suggests a title and description, which you can review and edit.

<img src="/wp-content/uploads/pr-ai-title-and-description.png" srcset="/wp-content/uploads/pr-ai-title-and-description@2x.png" class="help-center-img img-bordered">

## Bring your own key

By default, commit explanations and message generation use **Gemini**, and no API key is required—requests are included as part of your GitKraken subscription.

If you prefer to use **OpenAI**, **Azure**, **Anthropic**, or a Custom URL with your own API key, you may configure this in your settings from <kbd>Preferences > GitKraken AI</kbd>.

<img src="/wp-content/uploads/gkd-11-Preferences-GitKraken-AI.png" class="help-center-img img-bordered">

Additionally you may include **custom instructions** to guide how GitKraken AI generates messages or explanations for Commit Message Generation, Explain Commits, Stash Message Generation, and Pull Requests title and description respectively: 

<img src="/wp-content/uploads/gkd-11-custom-instructions.png" class="help-center-img img-bordered">

### Commit Prompt Examples

Not sure how to advise GitKraken AI? Here are some starter prompts, and we encourage tinkering!

#### Prompt for brevity

```
Keep the summary short, but informative
```

#### Prompt to add conventional commit prefix

```
Format the summary as:

<type>: <summary>

Where <type> is one of the following prefixes:

    feat: A new feature

    fix: A bug fix

    docs: Documentation only changes

    style: Changes that do not affect the meaning of the code (e.g. formatting)

    refactor: Code changes that neither fix a bug nor add a feature

    perf: Code changes that improve performance

    test: Adding or updating tests

    chore: Routine tasks or maintenance not related to source code

The <summary> should be a short (max 72 characters) description of what was changed, in the imperative mood (e.g., "add login button", "fix broken link", "refactor user auth logic").

Only output the final commit message — no explanations, no extra formatting.
```

#### Prompt for different language 

```
Write the output in Spanish.
```

## What’s Next?

Additional AI-powered features are in development to help automate repetitive tasks and keep you focused on what matters. These tools are built to reduce friction while giving you full control over your development workflow.

<div class='callout callout--basic'>
    <p>More questions about Gitkraken AI? Please see our <a href="https://help.gitkraken.com/general/gitkraken-ai-faq">GitKraken AI FAQ page</a> for more details</p>
</div>
