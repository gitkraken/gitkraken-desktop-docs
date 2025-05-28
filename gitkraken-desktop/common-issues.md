---
title: Common Issues
description: Learn about common issues that you may encounter when using GitKraken Desktop.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

***

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
