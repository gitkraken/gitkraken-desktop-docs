---
title: GitKraken Desktop – Common Issues and Fixes
description: Troubleshoot common GitKraken Desktop problems, including login errors, GitHub integrations, performance issues, and experimental Git behavior.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: August 2025</kbd>

***

## Account, License, and Entitlement Issues

### My account shows Trial/Free/Community despite being a paid customer
In GitKraken Desktop, verify you're logged in with the correct account:
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-1.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Ensure you are signed in with the email address linked to your subscription. Avoid using GitHub or Google login options if your subscription is tied to an email address.</figcaption>
</figure>

### The account is correct but it says I don't have AI tokens
Make sure the correct organization is selected:
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-2.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">AI token access is determined by the selected organization.</figcaption>
</figure>

### GitKraken.dev shows my account as TRIAL / COMMUNITY
Select the correct organization:
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-3.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">This issue can occur if you're viewing an organization that doesn't have a subscription.</figcaption>
</figure>

---

## GitKraken Desktop Issues

### Clone repo always uses HTTPS instead of SSH
GitKraken Desktop defaults to HTTPS. To use SSH:
1. Go to <kbd>Preferences > Integrations > [INTEGRATION]</kbd>
2. Add or generate an SSH key
3. Restart GitKraken Desktop

### Issue tracker error appears on repo startup or tab switch
This happens if a disconnected issue tracker is set as default.
- Go to <kbd>Preferences > Issue Tracker</kbd>
- Select <kbd>None</kbd>
- Check <kbd>Use this as the default for all repositories</kbd>

### Commit details panel is missing
To re-enable it: <kbd>View > Show Commit Details panel</kbd>
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-4.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">The right-side commit panel can be toggled from the View menu.</figcaption>
</figure>

### Can't minimize/maximize or exit full-screen mode
Toggle full-screen mode with <kbd>F11 (for Windows/Linux) or Ctrl + Cmd + F (for macOS)</kbd>
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-5.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Keyboard shortcut to toggle full screen in GitKraken Desktop.</figcaption>
</figure>

### Diff shows entire file instead of changes
This can occur due to differences in line endings or encoding.
- Enable "Ignore trailing whitespace"
- If the message changes to "File contents are unchanged," the files are identical
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-6.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Line ending or whitespace differences may cause misleading diffs.</figcaption>
</figure>

### Private organization repositories not visible (GitHub)
Ensure GitKraken Desktop has organization access:
<figure class='figure center'>
  <img src="/wp-content/uploads/GKD-Common-Issue-7.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Check your GitHub application settings to confirm permissions.</figcaption>
</figure>

[GitHub Application Access Settings](https://github.com/settings/connections/applications/a7557949433b7d282a76)

---

## WSL Issues

### GitKraken window is too small
GitKraken Desktop may not respect Windows DPI scaling when running in WSL.
- Use this workaround: `gitkraken --force-device-scale-factor=1.5`

### GitKraken doesn't launch from the console
Avoid running GitKraken as root. Switch to a regular user.

### GitKraken closes suddenly and won't reopen
This is a known WSL issue triggered by network changes.
- Terminate GitKraken: `pkill -f gitkraken`
- Launch another GUI app (e.g., `gedit`) to restore GUI functionality

### GitKraken GUI does not launch or scales incorrectly under WSL2 with XServer
- XServer is not required. Use native WSL2 GUI support instead.

---

## Linux (Ubuntu)

### File explorer does not open
GitKraken’s Electron window may be hidden behind the app.
- Minimize GitKraken or use <kbd>Alt + Tab</kbd>

### GitKraken does not load my environment variables
- GitKraken sources `.bashrc` or `.zshrc` for environment variables

### File watching failed to start
Increase file watchers in `/etc/sysctl.conf`:
```bash
fs.inotify.max_user_instances=8192
fs.inotify.max_user_watches=524288
```

---

## Windows

### Use GitKraken Desktop with PuTTY/Plink
- Set `GIT_SSH` or `GIT_SSH_COMMAND` to point to Plink
- Or configure `core.sshCommand` in `.gitconfig`
- Also update Git Executable under <kbd>Preferences > Experimental > Git Executable</kbd>

---

## macOS

### Git hooks fail with `command not found`
GUI apps on macOS do not inherit shell environment variables.
- Try launching GitKraken from terminal
- Use `launchctl setenv YOURVAR value` to set GUI-accessible environment variables

---

## General Troubleshooting for GitKraken Desktop 9.4.0+

The [Git Executable](/gitkraken-desktop/experimental-features/#git-executable) option may affect Git behavior.

Steps to modify:
- Go to <kbd>Preferences > Experimental</kbd>
- Choose system Git version instead of the bundled one
- [Download Git](https://git-scm.com/download) if needed

<figure class='figure center'>
  <img src="/wp-content/uploads/gkc-git-executable-version.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Switch Git Executable version under Preferences > Experimental.</figcaption>
</figure>

Disable the executable if problems continue:
<figure class='figure center'>
  <img src="/wp-content/uploads/gkc-use-git-executable.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Disable Git Executable if needed.</figcaption>
</figure>

Report persistent issues via [GitKraken Support](https://help.gitkraken.com/gitkraken-desktop/contact-support/).

[Blog post on migrating to Git Executable](https://www.gitkraken.com/blog/gitkraken-client-migrating-from-libgit2-to-git-executable?product=gitkraken&source=help_center)

---

## Integration – 1000 Series Errors

Error codes include:
- 1002
- 1003
- 1005
- 1007

<figure class='figure center'>
  <img src="/wp-content/uploads/error-1002.png" srcset="/wp-content/uploads/error-1002@2x.png 2x" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Example: Authentication error during integration.</figcaption>
</figure>

**Solution:**
- Check credentials
- Sign out from your browser, then try again in GitKraken
- Clear browser cache
- Try a different default browser

Still stuck? [Contact Support](https://www.gitkraken.com/contact?product=gitkraken&source=help_center)

---

## Push Failed: `Cannot read property 'fullName' of undefined`

<figure class='figure center'>
  <img src="/wp-content/uploads/push-error.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Push error caused by case mismatch in branch name.</figcaption>
</figure>

**Solution:**
Rename the local branch to match the remote branch exactly. Use an intermediate name if necessary:
```bash
git branch -m Test-branch temp-branch
git branch -m temp-branch test-branch
```

---

## Branches or Files Missing – Capitalization Issues

On case-insensitive file systems like Windows, branches or files differing only by case may not appear correctly.

<small class='text-muted'>End of document.</small>
