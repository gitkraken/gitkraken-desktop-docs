---
title: Git Hooks in GitKraken Desktop
description: Learn how to create, configure, and manage Git hooks in GitKraken Desktop. Supports custom hook paths, error handling, and pre-push validations.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: January 2026</kbd>

Git hooks are shell scripts that execute after Git events such as commits or pushes.

<figure>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZZgyILr-TjA?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>
<figcaption style="text-align: center; color: #888">Overview of Git hooks and demonstration in GitKraken Desktop</figcaption>
</figure>

***

## Where are Git hooks?

Hooks reside in the `hooks` subdirectory of the `.git` folder, created automatically when initializing a repository in GitKraken Desktop. You'll find it at `.git/hooks`, typically containing a `README.sample` file.

Hooks are specific to your local repository and are neither tracked by Git nor copied to new repositories.

<figure>
  <img src='/wp-content/uploads/terminal-hooks.png' srcset='/wp-content/uploads/terminal-hooks@2x.png 2x' class="help-center-img img-bordered" alt="Terminal output showing contents of the .git/hooks directory including various sample hook scripts" />
  <figcaption style="text-align: center; color: #888">Terminal view of the .git/hooks directory</figcaption>
</figure>

<figure>
<img src='/wp-content/uploads/gkc_hook_location_explorer.png' srcset='/wp-content/uploads/gkc_hook_location_explorer@2x.png 2x' class="help-center-img img-bordered" alt="Finder window showing the path to the Git hooks directory within a repository's .git folder" />
<figcaption style="text-align: center; color: #888">Explorer view of the Git hooks directory</figcaption>
</figure>

If you're on OSX or Linux, you must set hook files to be executable. GitKraken Desktop will throw an error (e.g., exit code 126) if the file lacks executable permissions.

<figure>
<img src='/wp-content/uploads/gkc_hook_exit_error_126.png' srcset='/wp-content/uploads/gkc_hook_exit_error_126@2x.png 2x' class="help-center-img img-bordered" alt="Error notification in GitKraken Desktop indicating a pre-commit Git hook failed with exit code 126" />
<figcaption style="text-align: center; color: #888">Git hook execution error in GitKraken Desktop (exit code 126)</figcaption>
</figure>

Any script that returns a non-zero exit code is considered a failure.

***

## Define a custom hook path

To use a custom Git hook path:

1. Go to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> Git Hooks</em>.
2. Click <button class="button button--primary button--ui button--nolink">Browse</button> to set or enter the path.

This setting is defined per repository.

<figure>
<img src='/wp-content/uploads/git-hooks-pref-2025.png' srcset='/wp-content/uploads/git-hooks-pref-2025@2x.png 2x' class="help-center-img img-bordered" alt="GitKraken Desktop Preferences panel showing Git Hooks settings and custom directory option" />
<figcaption style="text-align: center; color: #888">Setting a custom Git hooks path in Preferences</figcaption>
</figure>

***

## What hooks are supported by GitKraken Desktop?

GitKraken Desktop supports a wide array of Git hooks. Each hook is triggered by specific actions like commit, merge, or rebase.

<table class='table table--bordered table--shortcuts'>
  <tbody>
      <tr>
          <td style="width: 35%;"> <h3> <code>pre-commit</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Amend</li>
              <li>Commit</li>
              <li>Merge Resolve</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3><code>prepare-commit-msg</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Amend</li>
              <li>Commit</li>
              <li>Cherrypick</li>
              <li>Merge</li>
              <li>Revert</li>
              <li>Squash</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>commit-msg</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Amend</li>
              <li>Commit</li>
              <li>Merge Resolve</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-commit</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Amend</li>
              <li>Cherrypick</li>
              <li>Commit</li>
              <li>Merge Resolve</li>
              <li>Revert</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>pre-rebase</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Rebase</li>
              <li>Squash</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-checkout</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Checkout</li>
              <li>Discard Changes (selectively)</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-merge</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Fast-Forward</li>
              <li>Merge (Without Conflicts)</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>post-rewrite</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Amend</li>
              <li>Rebase</li>
              <li>Squash</li>
            </ul>
          </td>
      </tr>
      <tr>
          <td style="width: 35%;"> <h3> <code>pre-push</code></h3> </td>
          <td style="width: 65%;">
            <ul>
              <li>Delete Remote Branch</li>
              <li>Delete Remote Tag</li>
              <li>Push Branch</li>
              <li>Push Tag</li>
            </ul>
          </td>
      </tr>
  </tbody>
</table>


***

## Git hooks example

Git hooks automate actions when Git events occur in GitKraken Desktop or the command line. Here's a basic `pre-commit` hook example to validate the global Git user email.

### Tools needed
- GitKraken Desktop
- Text Editor (e.g., [Visual Studio Code](https://code.visualstudio.com/))
- Terminal (e.g., [GitKraken Terminal](https://help.gitkraken.com/gitkraken-desktop/terminal/))

### Step-by-step setup

**1. Navigate to hooks directory**  
Open Visual Studio Code and go to <kbd><strong>~/repo/.git/hooks</strong></kbd>. Create a new file named `pre-commit`.

<figure>
<img src='/wp-content/uploads/vscode-to-hooks.png' class="help-center-img img-bordered" alt="VS Code file explorer showing the creation of a new pre-commit file inside the .git/hooks directory" />
<figcaption style="text-align: center; color: #888">Creating a new Git hook file in VS Code</figcaption>
</figure>

<div class='callout callout--warning'>
    <p>Note 📝 - You may need to make the .git folder visible in VS Code by adjusting <code>files.exclude</code> settings.</p>
</div>

**2. Make the file executable**  
Open the GitKraken Terminal and change to the `.git/hooks` directory. Run:

```
chmod +x pre-commit
```

<figure>
<img src='/wp-content/uploads/gkc-chmod-pre-commit.gif' class="help-center-img img-bordered" alt="GitKraken Desktop terminal changing into .git/hooks directory to make the pre-commit file executable" />
<figcaption style="text-align: center; color: #888">Making the pre-commit file executable using terminal</figcaption>
</figure>

<div class='callout callout--warning'>
    <p>Note 📝 - If your terminal isn't set up in GitKraken Desktop, refer to the <a href="/start-here/tips/#9-open-terminal">Start Here Tips</a>.</p>
</div>

**3. Write your bash script**  
Use a text editor to define your `pre-commit` script. Start with the correct shebang:

```
#!/bin/bash
```

Then add your validation logic using variables like:
- `globalEmail` - value from Git global config
- `workEmail` - required email for commits

The script should compare the current global email with the required email and display an error if they do not match. If the values match, the commit proceeds.

**Example:**

```bash
#!/bin/bash
globalEmail=$(git config --global user.email)
workEmail="you@example.com"

if [ "$globalEmail" != "$workEmail" ]; then
  echo "Error: global email does not match required work email ($workEmail)."
  exit 1
fi
exit 0
```

Save the file. Your `pre-commit` hook is now ready to enforce proper committer email usage before any commit is made.

### Git hook in action
<figure>
<img src='/wp-content/uploads/gkc-hook-in-action.gif' class="help-center-img img-bordered" alt="GitKraken Desktop showing a pre-commit Git hook error after attempting to commit a staged file" />
<figcaption style="text-align: center; color: #888">Git hook example triggered during commit</figcaption>
</figure>

***

## Environment Variables & Git Hooks

On macOS, GUI applications do not inherit shell profile variables. If your Git hooks rely on environment variables set in your shell, use the following command to make them available:

```
launchctl setenv YOURVAR value
```

## Bypass Git hooks

To skip Git hooks during a commit, use the `Commit and skip hooks` option.

<div class='callout callout--warning'>
    <p>Note 📝 - This option disables all hooks triggered by the commit action.</p>
</div>

<figure>
<img src='/wp-content/uploads/skip-hook-2025.png' srcset='/wp-content/uploads/skip-hook-2025@2x.png 2x' class="help-center-img img-bordered" alt="GitKraken Desktop commit panel showing a checkbox to skip Git hooks during commit" />
<figcaption style="text-align: center; color: #888">Option to commit while skipping hooks in GitKraken Desktop</figcaption>
</figure>

## Global Git Hooks

GitKraken Desktop respects global Git hook paths set in your `.gitconfig` file. These hooks apply to all cloned repositories.

To configure a global path, add the following to your `.gitconfig`:

```
[core]
    hooksPath = /path/to/your/hooks
```

