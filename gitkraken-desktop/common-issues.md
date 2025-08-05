---
title: GitKraken Desktop – Common Issues and Fixes
description: Troubleshoot common GitKraken Desktop problems, including login errors, GitHub integrations, performance issues, and experimental Git behavior.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: August 2025</kbd>

***
### Account/License/Entitlement issue
#### My account shows Trial/Free/Community despite being a paid customer
In Gitkraken Desktop: Verify you are logging with the correct account here:
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-1.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">If the account is not correct, go to Sign into a different account and enter the email address associated with the subscription (Do not use Github or Google sign in options).</figcaption>
</figure>

#### The account is correct and license is applied but says I dont have AI tokens 
Confirm you have the correct organization selected:
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-2.png" class="help-center-img img-bordered">
</figure>

#### Gitkraken.dev says my account is TRIAL / COMMUNITY
Select the correct organization:
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-3.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">This can happen sometimes if the wrong organization is selected that does not have a subscription</figcaption>
</figure>

### Gitkraken Desktop
##### Clone repo always uses HTTPS, I want to use SSH
By default, Gitkraken Desktop always use HTTPS URL when cloning. If you want to switch to SSH by default, you have to add an SSH key in the integration of your remote.
Go to Preferences > Integrations > [INTEGRATION] > Add or generate SSH key > Restart Gitkraken Desktop.

##### Gitkraken throws error about issue tracker cannot be initialized every time I start or switch repo tab
This happens because you have set a default issue tracker that is disconnected.

WIth a repo tab open, go to Preferences > Issue Tracker > Select "None" > Check "Use this as the default for all repositories"

##### I dont see the right panel anymore
Go to View > Show Commit Details panel
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-4.png" class="help-center-img img-bordered">
</figure>

##### No way to minimize/maximize or I cant get out of full screen mode
To toggle the full-screen mode press Ctrl + Shift + F
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-5.png" class="help-center-img img-bordered">
</figure>

##### Diff is displaying entire file
This happens when both versions of the file have a different encoding or line ending (CRLF <> LF). 
If you enable the ignore trailing/whitespaces, does the diff changes to "File contents are unchanged"?
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-6.png" class="help-center-img img-bordered">
</figure>

##### I cant see my org private repos (Github)
Please verify Gitkraken app has permissions to access the organization at (Github:)[https://github.com/settings/connections/applications/a7557949433b7d282a76]
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-7.png" class="help-center-img img-bordered">
</figure>


#### WSL issues
##### Scaling/Window too small
This display issue is a known limitation when running GUI apps inside WSL, including GitKraken Desktop, they do not respect Windows DPI scaling settings, which can cause the interface to appear too small on high-resolution monitors.
As a workaround, you can try launching GitKraken Desktop with a manual scaling flag:
gitkraken --force-device-scale-factor=1.5

##### I run gitkraken in the console but nothing happens
This typically occurs when GitKraken is run as the root user. Please switch to a standard user and try again.

##### Gitkraken closes suddenly and does not start again, I have to shutdown WSL
Certain GUI applications running within WSL may close unexpectedly when network conditions change, such as switching Wi-Fi networks, connecting/disconnecting a VPN, or a network adapter disconnecting. This is a known bug in WSL, documented (here)[https://github.com/microsoft/wslg/issues/1092].

Suggested workarounds for GitKraken users:
Terminate all GitKraken processes (`pkill -f gitkraken`) and restart the application.
Open another GUI application (e.g., gedit or nautilus); this may restore the GitKraken window.

##### I have GitKraken installed inside WSL2 and have an XServer running on Windows. Scaling is incorrect or does not open the window.
WSL2 already supports GUI apps without Xserver. Please try using WSL2.

#### Ubuntu/Linux
##### File Explorer not opening
This is a known Electron issue. The browser window is opening in the background. Minimize the GitKraken window or use Alt+Tab.

##### GKD not using my environment variables
Gitkraken Desktop sources the environment variables set in .bashrc or .zshrc

##### File watching failed to start for this repository
This error can be caused when GitKraken Desktop hits the limit of file watchers set in your system.
To increase the number of file watch instances add the following in the file /etc/sysctl.conf:
fs.inotify.max_user_instances=8192 
fs.inotify.max_user_watches=524288 

#### Windows
##### [SSH] I want to use Gitkraken Desktop with Putty/Plink
Set GIT_SSH/GIT_SSH_COMMAND as environment variable to plink executable or use core.sshComand in .gitconfig.

Also, change the Git Executable version to yours, instead of Bundled (Preferences > Experimental > Git Executable > Select installed version).

#### MacOS
##### Githooks fail with X: command not found
This is because the command/executable is not in your PATH env variable for GUI apps.
If you start GitKraken from the CLI using gitkraken, does the hook run as expected?

If so, on macOS, GUI applications do not have access to the environment variables set in your shell profile. This means that if you have environment variables set in your shell profile that you want to use in your Git hooks, you need to use the following command:

launchctl setenv YOURVAR variable


### General Troubleshooting for GitKraken Desktop 9.4.0+

GitKraken Desktop 9.4.0 introduced an [experimental Git Executable feature](/gitkraken-desktop/experimental-features/#git-executable). This option can impact how Git operations perform.

To adjust this:
- Go to <kbd>Preferences > Experimental</kbd>
- Switch from the **Bundled with GitKraken** Git version to your system-installed version
- Download Git if needed from [git-scm.com](https://git-scm.com/download)

<figure class='figure center'>
  <img src="/wp-content/uploads/gkc-git-executable-version.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Switch Git Executable version under Preferences > Experimental.</figcaption>
</figure>

If issues persist, try disabling the executable by unchecking <kbd>Use Git Executable</kbd>.

<figure class='figure center'>
  <img src="/wp-content/uploads/gkc-use-git-executable.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Disable Git Executable if needed.</figcaption>
</figure>

This feature will become the default method for Git operations in future releases. If you encounter any issues, [contact support](https://help.gitkraken.com/gitkraken-desktop/contact-support/) to report them.

Read more in this [blog post](https://www.gitkraken.com/blog/gitkraken-client-migrating-from-libgit2-to-git-executable?product=gitkraken&source=help_center).

***

## Integration - 1000 Series Errors

When connecting to a service, you may see:
- Error 1002
- Error 1003
- Error 1005
- Error 1007

<figure class='figure center'>
  <img src="/wp-content/uploads/error-1002.png" srcset="/wp-content/uploads/error-1002@2x.png 2x" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Example: Authentication error during integration.</figcaption>
</figure>

### Solution
These are authentication-related errors. Try the following:

- Confirm your credentials are correct
- Sign out of the service in your default browser, then retry in GitKraken
- Clear browser cache and sign out of the hosting service
- Change your system’s default browser and retry

If none of these resolve the issue, [contact support](https://www.gitkraken.com/contact?product=gitkraken&source=help_center).

***

## Push Failed: `Cannot read property 'fullName' of undefined`

<figure class='figure center'>
  <img src="/wp-content/uploads/push-error.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Push error caused by case mismatch in branch name.</figcaption>
</figure>

### Solution
Rename your local branch to match the casing of the remote branch exactly. If needed, use an intermediate name:

> Example: `Test-branch` → `temp-name` → `test-branch`

***

## Branches or Files Missing – Capitalization Issues

This typically occurs on case-insensitive file systems (e.g., Windows) when multiple branches or files differ only by case.

### Symptoms
- Only one version of a similarly named branch appears
- Files with differing capitalization may disappear, appear deleted, or misbehave
- Staged files may not show as staged via `git status`

### Recommendation
Use unique naming for all branches, files, and remotes to avoid conflicts.

***

## Cannot Log In: `Cannot read property 'email' of null`

This error usually results from interference by proxy, firewall, or security tools such as Zscaler.

### Solution
1. Sign in using GitHub authentication
2. Approve GitKraken
3. Continue as Free user with 0 days
4. Click the Free badge in the bottom right to trigger authentication within GitKraken
5. Restart GitKraken and log in normally

***

## Missing Taskbar Icon on Windows

This happens when the shortcut path changes from:
- `C:\Users\USER\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\Axosoft, LLC`
- to `C:\Users\USER\AppData\Roaming\Microsoft\Windows\Start Menu\Programs\GitKraken`

### Solution
Delete the old folder, then launch GitKraken from the Start Menu and re-pin to the taskbar.

***

## GitHub Remotes or Permissions Issues

If GitHub repositories or remotes are missing, and you see errors about organization permissions:

<figure class='figure center'>
  <img src="/wp-content/uploads/error.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">GitHub authorization error when accessing remotes.</figcaption>
</figure>

### Checklist
- Check [GitHub application access](https://github.com/settings/connections/applications/a7557949433b7d282a76)
- Ensure the organization approves GitKraken under [Organization Approval](https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/)
- If using another person’s repo, fork it or ask them to [install GitKraken](/gitkraken-desktop/how-to-install/) and connect GitHub
- Learn more from [GitHub’s app restriction guide](https://help.github.com/articles/about-third-party-application-restrictions/)

***

## Rust Socket Bridge Error

You may see this error during Git actions like push/pull/clone/fetch:

<figure class='figure center'>
  <img src="/wp-content/uploads/gkd-10-4-rust-socket-bridge-error.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Rust Socket Bridge blocked by security software.</figcaption>
</figure>

### Solution
Ask your IT department to allow the Rust Socket Bridge executable or add an exclusion for GitKraken Desktop’s installation directory.
