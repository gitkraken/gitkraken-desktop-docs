---

title: Git Hooks
description: Compare your changes with diffs in GitKraken Desktop. Learn about where to access diffs, file blame, and more.
taxonomy:
    category: gitkraken-desktop

---

<kbd>Last updated: April 2025</kbd>

Git hooks are shell scripts that execute after an event such as a commit or push.

In the following video, we will take you through the basics of what a Git hook is and demonstrate how to use one in GitKraken Desktop.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ZZgyILr-TjA?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>


***

## Where are Git hooks?

Hooks are stored in the `hooks` subdirectory of the `.git` directory. This folder is automatically created when you initialize a new repository in GitKraken Desktop and is located in `.git\hooks` in your project directory with a `README.sample` file in it.

Hooks are unique to your local repository and will not be copied over if you create a new repository nor will be tracked by Git. Feel free to add, change, or remove scripts from this folder as necessary.

<img src='/wp-content/uploads/gkc_hook_location_terminal.png' srcset='/wp-content/uploads/gkc_hook_location_terminal@2x.png 2x' class="help-center-img img-bordered" />

<img src='/wp-content/uploads/gkc_hook_location_explorer.png' srcset='/wp-content/uploads/gkc_hook_location_explorer@2x.png 2x' class="help-center-img img-bordered" />


GitKraken Desktop will seamlessly detect any Git hooks in your repository, but if you are running OSX or Linux, you need to give execution rights to the hook file. If you forgot to set your files to executables, GitKraken Desktop will throw an error like the one shown below.

<img src='/wp-content/uploads/gkc_hook_exit_error_126.png' srcset='/wp-content/uploads/gkc_hook_exit_error_126@2x.png 2x' class="help-center-img img-bordered" />

Any script that exits with anything other than exit code 0 is considered a fail.

***

## Define a custom hook path

Users can define a custom path for Git hooks by going to <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> Git Hooks</em>. <button class="button button--primary button--ui button--nolink">Browse</button> to the location or enter the path to your Git hook folder.

This custom Git hook path is defined on a per-repository basis.

<img src='/wp-content/uploads/gkc_hook_preferences.png' srcset='/wp-content/uploads/gkc_hook_preferences@2x.png 2x' class="help-center-img img-bordered" />

***

## What hooks are supported by GitKraken Desktop?

Here are the hooks supported by GitKraken Desktop. Where appropriate, beneath each hook are the actions during which GitKraken Desktop calls that hook:

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

Git hooks are scripts that perform automated actions when a specific action is performed in GitKraken Desktop or the command line. The Git hook name usually indicates the hook’s trigger (e.g. pre-commit).

Git hooks live under the .git folder of your repo in a directory called hooks. The path to the hooks will look similar to <kbd>repo/.git/hooks</kbd>.
### Tools needed
- GitKraken Desktop
- Text Editor - I will be using [Visual Studio Code](https://code.visualstudio.com/)
- Terminal - I will be using the in-app [GitKraken Terminal](https://help.gitkraken.com/gitkraken-desktop/terminal/)

### Hook Purpose
In this example, we'll create a `pre-commit` hook. This hook validates the Git config's global user email. The hook is useful so that the commits contain the correct committer email address.

### Creating the git hook

#### Step 1
First navigate to the hooks directory for the target repo. Open a Visual Studio Code window and navigate to <kbd><strong>~/repo/.git/hooks</strong></kbd>. From here, add a new file to the `.git/hooks` directory called `pre-commit`.

<img src='/wp-content/uploads/vscode-to-hooks.png' class="help-center-img img-bordered" />

<div class='callout callout--warning'>
    <p>Note 📝 - To make the .git folder visible in Visual Studio Code you will need to remove **/.git from files.exclude in the Visual Studio Code settings.</p>
</div>

#### Step 2
Now that we have our pre-commit file, we need to make it executable. To do this we will need the command line.

Open the GitKraken Terminal window by clicking the Terminal <i class="fa fa-terminal" aria-hidden="true"> </i> icon in toolbar (or by searching "terminal" in the Command Palette). Once the terminal is open, change directory to `.git/hooks`.

Then use the command `chmod +x pre-commit` to make the pre-commit file executable.

<img src='/wp-content/uploads/gkc-chmod-pre-commit.gif' class="help-center-img img-bordered" />

<div class='callout callout--warning'>
    <p>Note 📝 - If you do not have your terminal setup in GitKraken Desktop, please review the <a href="/start-here/tips/#9-open-terminal">Start Here Tips</a> for setup details.</p>
</div>

#### Step 3
Now we create our script using bash. Open the pre-commit file in VS Code as we did before. 

The first instruction we need to specify is the shell used in the script, do this by using `#!/bin/bash` at the beginning of your script for bash or `#!/bin/sh` if using the sh shell. 

This `pre-commit` hook watches for incorrect commit authors using the script below.

**Script variables:**<br>
`globalEmail` - Get email in global git config<br>
`workEmail` - This is your target email address. The email needed to commit successfully.<br>

In the first condition we validate that the global git config user.email matches with our workEmail. If it fails we will see:

```
        echo "Commit email and global git config email differ"
        echo "Global commit email: "$globalEmail""
        echo "Committing email expected: $workEmail"
        exit 1

```

If the condition is successful the script will run and the commit will be made.

#### Full script
```
#!/bin/bash

globalEmail=`git config --global --get user.email`
workEmail="example@gitkraken.com"

if [[ $globalEmail != $workEmail ]];
then
        echo "Commit email and global git config email differ"
        echo "Global commit email: "$globalEmail""
        echo "Committing email expected: $workEmail"
        exit 1
else
        echo ""
        exit 0
fi
```

### Git hook in action
<img src='/wp-content/uploads/gkc-hook-in-action.gif' class="help-center-img img-bordered" />

### Environment Variables & Git Hooks

On macOS, GUI applications do not have access to the environment variables set in your shell profile. This means that if you have environment variables set in your shell profile that you want to use in your Git hooks, you need to use the following command:

```
launchctl setenv YOURVAR variable
```

### Bypass git hooks

There may be times when you want to skip your Git hooks when making a commit. This can be done on a commit-by-commit basis by selecting the `Commit and skip hooks` option. 

<div class='callout callout--warning'>
    <p>Note 📝 - Using this option will bypass all hooks that trigger with git commit action.</p>
</div>

<img src='/wp-content/uploads/bypass-git-hooks.png' class="help-center-img img-bordered" />

### Global Git Hooks

GitKraken Desktop honors global Git hooks setting in your .gitconfig file. These hooks are applied to all repositories that you have cloned.

To set this up, you can add the following to your .gitconfig file:

```
[core]
    hooksPath = /path/to/your/hooks
```


