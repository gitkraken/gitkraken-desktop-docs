---
title: GitKraken Desktop – Common Issues and Fixes
description: Troubleshoot common GitKraken Desktop problems, including login errors, GitHub integrations, performance issues, and experimental Git behavior.
product: GitKraken Desktop
feature: Common Issues
content_type: troubleshooting
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, generic]
integrations: [GitHub]
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [troubleshooting, login, github, performance, issues]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

***

Use this page to troubleshoot common GitKraken Desktop problems related to licensing, integrations, SSH, WSL, platform-specific behavior, and known error messages. For the most frequent fixes, start with the Quick Start checklist.

**Requirements and limits**
- Integration recovery: Signing out in your browser, clearing its cache, and reconnecting from <kbd>Preferences &gt; Integrations</kbd> resolves many 1000-series errors
- WSL limitation: Do not run GitKraken Desktop as root, and prefer native WSL2 GUI support over XServer-based setups
- Experimental Git note: Some issues may be tied to the Git Executable setting in <kbd>Preferences &gt; Experimental</kbd>
- Escalation path: Contact GitKraken Support if the matching section does not resolve the problem

***

## Quick Start


- **Account or license not recognized**: Verify you are signed in with the email address linked to your subscription, and that the correct organization is selected in GitKraken Desktop and on gitkraken.dev.
- **Integration errors (1002, 1003, 1005, 1007)**: Sign out of your browser, clear its cache, and reconnect your integration from <kbd>Preferences > Integrations</kbd>.
- **Clone always uses HTTPS instead of SSH**: Add or generate an SSH key under <kbd>Preferences > Integrations > [Integration]</kbd>, then restart GitKraken Desktop.
- **Commit Details panel missing**: Go to <kbd>View > Show Commit Details Panel</kbd> to restore it.
- **Performance problems**: See the [Performance Issues](/gitkraken-desktop/performance-issues/) guide, or try running <kbd>Perform Repo Maintenance</kbd> from the Command Palette.
- **Push failed with `Cannot read property 'fullName' of undefined`**: Rename your local branch to match the remote branch name exactly.
- **WSL issues**: Avoid running GitKraken Desktop as root; use native WSL2 GUI support instead of XServer.
- **Coding agent sessions fail in WSL**: Make sure the coding agent CLI you want to use is installed and available in WSL, not only on Windows. See [Use GitKraken Desktop with Windows Subsystem for Linux (WSL 2)](/gitkraken-desktop/windows-subsystem-for-linux/) and [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

If these steps do not resolve your issue, contact [GitKraken Support](https://help.gitkraken.com/gitkraken-desktop/contact-support/).

***

## How to fix account, license, and entitlement issues

If GitKraken Desktop shows the wrong plan or no AI credits, check which account and organization you are using.

### My account shows Trial/Free/Community despite being a paid customer
In GitKraken Desktop, click your profile icon and check the name and email address under **Account**. If it is the wrong account, click **Sign Out**, then sign in again with the account linked to your subscription:
<figure class='figure center'>
  <img alt="The GitKraken Desktop profile and account menu, signed in: Current profile with the profile, AI usage, commit signature and Manage profiles, then Account with the account name and email, Manage account, and Sign Out." src="/wp-content/uploads/gkd-profile-menu-sign-out-01-v2@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Ensure you are signed in with the email address linked to your subscription. Avoid using GitHub or Google login options if your subscription is tied to an email address.</figcaption>
</figure>

### The account is correct but it says I don't have AI credits
Make sure the correct organization is selected:
<figure class='figure center'>
  <img alt="AI credit access is determined by the selected organization" src="/wp-content/uploads/GKD-Common-Issue-2.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">AI credit access is determined by the selected organization.</figcaption>
</figure>

If the organization is correct, you may have used this week's AI credits. To check, go to <kbd>Preferences > GitKraken AI</kbd> and look at the **Usage Details** card:

- Your credits used this week, and the date they reset.
- **Shared Organization Pool**: the organization's credits this week, split into **Your usage**, **Rest of organization** and **Remaining**.

When you reach your own weekly limit, the card shows **You've reached your weekly credit limit**. GitKraken AI then uses your organization's shared credit pool, which resets weekly. On a paid plan, organization owners and admins can click **Get more AI credits**; trial users see **Upgrade to get more credits**.

If a request goes above the weekly usage included in your plan or trial, GitKraken Desktop shows **GitKraken AI Weekly Limit Reached**:

- **Trial or free users:** Click **Upgrade GitKraken** to purchase a GitKraken plan.
- **Paid organization owners and admins:** Click **Purchase more AI credits**.
- **Paid organization members:** Contact your organization admin or owner to request more AI credits.

### GitKraken.dev shows my account as TRIAL / COMMUNITY
Select the correct organization:
<figure class='figure center'>
  <img alt="GitKraken.dev with a red arrow pointing to the organization switcher, open to show the organizations you can switch between." src="/wp-content/uploads/GKD-Common-Issue-3.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">This issue can occur if you're viewing an organization that does not have a subscription.</figcaption>
</figure>

---

## How to fix common GitKraken Desktop issues

These fixes apply to GitKraken Desktop on every platform.

### Clone repo always uses HTTPS instead of SSH
GitKraken Desktop defaults to HTTPS. To use SSH:
1. Go to <kbd>Preferences > Integrations > [Integration]</kbd>.
2. Add or generate an SSH key.
3. Restart GitKraken Desktop.

### Issue tracker error appears on repo startup or tab switch
This error appears when a disconnected issue tracker is set as the default. To fix it:
1. Go to <kbd>Preferences > Issue Tracker</kbd>.
2. Select <kbd>None</kbd>.
3. Select <kbd>Use this as the default for all repositories</kbd>.

### Commit details panel is missing
To show the panel again, select <kbd>View > Show Commit Details Panel</kbd>.
<figure class='figure center'>
  <img alt="The right-side commit panel can be toggled from the View menu" src="/wp-content/uploads/GKD-Common-Issue-4.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">The right-side commit panel can be toggled from the View menu.</figcaption>
</figure>

### Interface is too large or too small
Use the zoom options in the **View** menu:
- **Increase Zoom**: <kbd>Ctrl/Cmd</kbd> + <kbd>=</kbd>
- **Decrease Zoom**: <kbd>Ctrl/Cmd</kbd> + <kbd>-</kbd>
- **Reset Zoom**: <kbd>Ctrl/Cmd</kbd> + <kbd>0</kbd> returns to 100%

You can also pick a zoom level from 80% to 300% in the zoom selector in the status bar.

### File watching is not working
If GitKraken Desktop shows **File watching is not working** after you open a repository, GitKraken Desktop is not receiving file change events from your operating system, so it does not detect changes you make outside the app. Restart your computer to fix this.

### Can't minimize/maximize or exit full-screen mode
To toggle full-screen mode, press <kbd>F11</kbd> on Windows and Linux, or <kbd>Ctrl</kbd> + <kbd>Cmd</kbd> + <kbd>F</kbd> on macOS.
<figure class='figure center'>
  <img alt="Keyboard shortcut to toggle full screen in GitKraken Desktop" src="/wp-content/uploads/GKD-Common-Issue-5.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Keyboard shortcut to toggle full screen in GitKraken Desktop.</figcaption>
</figure>

### Diff shows entire file instead of changes
Differences in line endings or encoding can cause this. To check:
- Enable **Ignore Leading/Trailing Whitespace**.
- If the message changes to **File contents are unchanged.**, the files are identical.
<figure class='figure center'>
  <img alt="Line ending or whitespace differences may cause misleading diffs" src="/wp-content/uploads/GKD-Common-Issue-6.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Line ending or whitespace differences may cause misleading diffs.</figcaption>
</figure>

### Private organization repositories not visible (GitHub)
Make sure GitKraken Desktop has access to the organization in your GitHub application settings:
<figure class='figure center'>
  <img alt="Check your GitHub application settings to confirm permissions" src="/wp-content/uploads/GKD-Common-Issue-7.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Check your GitHub application settings to confirm permissions.</figcaption>
</figure>

To check, open [GitHub Application Access Settings](https://github.com/settings/connections/applications/a7557949433b7d282a76).

---

## How to fix WSL issues

These fixes apply when you run GitKraken Desktop in Windows Subsystem for Linux (WSL).

### GitKraken window is too small
GitKraken Desktop may not follow Windows DPI scaling when it runs in WSL. As a workaround, launch it with `gitkraken --force-device-scale-factor=1.5`.

### GitKraken doesn't launch from the console
Do not run GitKraken Desktop as root. Switch to a regular user.

### GitKraken closes suddenly and won't reopen
Network changes can trigger this known WSL issue. To recover:
1. Close GitKraken Desktop: `pkill -f gitkraken`
2. Launch another GUI app, such as `gedit`, to restore GUI functionality.

### GitKraken GUI does not launch or scales incorrectly under WSL2 with XServer
GitKraken Desktop does not need XServer. Use native WSL2 GUI support instead.

### Coding agent sessions fail to start in WSL
Windows-installed coding agent CLIs can take precedence over WSL-installed CLIs.

- Make sure the coding agent CLI you want to use is installed in your WSL environment.
- Avoid relying on a Windows-installed coding agent when GitKraken Desktop is running inside WSL.
- For more information, see [Use GitKraken Desktop with Windows Subsystem for Linux (WSL 2)](/gitkraken-desktop/windows-subsystem-for-linux/) and [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

---

## How to fix Linux issues on Ubuntu

These fixes apply to GitKraken Desktop on Ubuntu.

### File explorer does not open
The file explorer window may open hidden behind GitKraken Desktop. Minimize GitKraken Desktop or press <kbd>Alt + Tab</kbd> to find it.

### GitKraken does not load my environment variables
GitKraken Desktop loads environment variables from `.bashrc` or `.zshrc`, so define them in one of those files.

### File watching failed to start
Increase the file watcher limits in `/etc/sysctl.conf`:
```bash
fs.inotify.max_user_instances=8192
fs.inotify.max_user_watches=524288
```

---

## How to fix Windows-specific issues

These fixes apply to GitKraken Desktop on Windows.

### Use GitKraken Desktop with PuTTY/Plink
To use Plink for SSH:
- Set `GIT_SSH` or `GIT_SSH_COMMAND` to the path of Plink, or set `core.sshCommand` in `.gitconfig`.
- Update the Git Executable setting in <kbd>Preferences > Experimental > Git Executable</kbd>.

---

## How to fix macOS-specific issues

These fixes apply to GitKraken Desktop on macOS.

### Git hooks fail with `command not found`
GUI apps on macOS do not inherit shell environment variables.
- Launch GitKraken Desktop from the terminal.
- Use `launchctl setenv YOURVAR value` to set environment variables that GUI apps can read.

---

## How to troubleshoot GitKraken Desktop 9.4.0 and later

The [Git Executable](/gitkraken-desktop/experimental-features/#git-executable) option may affect Git behavior. To change which Git version GitKraken Desktop uses:
1. If needed, [download Git](https://git-scm.com/download).
2. Go to <kbd>Preferences > Experimental</kbd>.
3. Under **Git Executable**, choose your system Git instead of the bundled one.

<figure class='figure center'>
  <img alt="Switch Git Executable version under Preferences > Experimental" src="/wp-content/uploads/gkc-git-executable-version.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Switch Git Executable version under Preferences > Experimental.</figcaption>
</figure>

If problems continue, clear **Use Git Executable**:
<figure class='figure center'>
  <img alt="Disable Git Executable if needed" src="/wp-content/uploads/gkc-use-git-executable.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Disable Git Executable if needed.</figcaption>
</figure>

If the problem persists, report it to [GitKraken Support](https://help.gitkraken.com/gitkraken-desktop/contact-support/).

---

## How to fix 1000-series integration errors

These integration errors have the following codes:
- 1002
- 1003
- 1005
- 1007

<figure class='figure center'>
  <img alt="Example: Authentication error during integration" src="/wp-content/uploads/error-1002@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Example: Authentication error during integration.</figcaption>
</figure>

To fix these errors:
- Check your credentials.
- Sign out in your browser, then try again in GitKraken Desktop.
- Clear your browser cache.
- Try a different default browser.

If the error continues, [contact GitKraken Support](https://www.gitkraken.com/contact?product=gitkraken&source=help_center).

---

## How to fix the `Cannot read property 'fullName' of undefined` push error

<figure class='figure center'>
  <img alt="Push error caused by case mismatch in branch name" src="/wp-content/uploads/push-error.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Push error caused by case mismatch in branch name.</figcaption>
</figure>

This push error appears when your local branch name differs from the remote branch name only by case. To fix it, rename the local branch to match the remote branch exactly. If needed, use an intermediate name:
```bash
git branch -m Test-branch temp-branch
git branch -m temp-branch test-branch
```

---

## How to fix missing branches or files caused by capitalization issues

On case-insensitive file systems, such as the one Windows uses, branches or files whose names differ only by case may not appear correctly.

---

## How to delete the GitKraken CLI after uninstalling GitKraken

**GitLens and GitKraken MCP also use the GitKraken CLI. If you still use either of them, do not uninstall the GitKraken CLI.**

If you have uninstalled GitKraken Desktop but the GitKraken CLI is still installed, you can remove it manually.

### Uninstall GitKraken CLI on MacOS(Homebrew)

1. Run the uninstall command:
```bash
gk uninstall
```
2. Remove the Homebrew cask:
```bash
brew uninstall --cask gitkraken-cli
```

### Uninstall GitKraken CLI on Windows(winget)

1. Run the uninstall command:
```bash
gk uninstall
```
2. Remove the winget package:
```bash
winget uninstall gitkraken.cli
```

### Uninstall the GitKraken CLI on Linux
1. Run the uninstall command:
```bash
gk uninstall
```
2. Remove the binary.

If you installed with Snap:
```bash
sudo snap remove gitkraken-cli 
```

If you installed manually:
```bash
sudo rm /usr/local/bin/gk
```
