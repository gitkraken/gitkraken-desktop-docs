---
title: GitKraken Desktop – Common Issues and Fixes
description: Troubleshoot common GitKraken Desktop problems, including login errors, GitHub integrations, performance issues, and experimental Git behavior.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

***

Use this page to troubleshoot common GitKraken Desktop problems related to licensing, integrations, SSH, WSL, platform-specific behavior, and known error messages. Start with the Quick Start checklist for the most common fixes, then use the matching section below when you need issue-specific recovery steps.

***

## Quick Start

Use this page to diagnose and resolve common problems in GitKraken Desktop. Find the section that matches your issue and follow the steps listed.

- **Account or license not recognized**: Verify you are signed in with the email address linked to your subscription, and that the correct organization is selected in GitKraken Desktop and on gitkraken.dev.
- **Integration errors (1002, 1003, 1005, 1007)**: Sign out of your browser, clear its cache, and reconnect your integration from <kbd>Preferences > Integrations</kbd>.
- **Clone always uses HTTPS instead of SSH**: Add or generate an SSH key under <kbd>Preferences > Integrations > [Integration]</kbd>, then restart GitKraken Desktop.
- **Commit Details panel missing**: Go to <kbd>View > Show Commit Details panel</kbd> to restore it.
- **Performance problems**: See the [Performance Issues](/gitkraken-desktop/performance-issues/) guide, or try running <kbd>Perform Repo Maintenance</kbd> from the Command Palette.
- **Push failed with `Cannot read property 'fullName' of undefined`**: Rename your local branch to match the remote branch name exactly.
- **WSL issues**: Avoid running GitKraken Desktop as root; use native WSL2 GUI support instead of XServer.

If the steps on this page do not resolve your issue, contact [GitKraken Support](https://help.gitkraken.com/gitkraken-desktop/contact-support/).

***

## How to fix account, license, and entitlement issues

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

## How to fix common GitKraken Desktop issues

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

## How to fix WSL issues

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

## How to fix Linux issues on Ubuntu

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

## How to fix Windows-specific issues

### Use GitKraken Desktop with PuTTY/Plink
- Set `GIT_SSH` or `GIT_SSH_COMMAND` to point to Plink
- Or configure `core.sshCommand` in `.gitconfig`
- Also update Git Executable under <kbd>Preferences > Experimental > Git Executable</kbd>

---

## How to fix macOS-specific issues

### Git hooks fail with `command not found`
GUI apps on macOS do not inherit shell environment variables.
- Try launching GitKraken from terminal
- Use `launchctl setenv YOURVAR value` to set GUI-accessible environment variables

---

## How to troubleshoot GitKraken Desktop 9.4.0 and later

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

## How to fix 1000-series integration errors

Error codes include:
- 1002
- 1003
- 1005
- 1007

<figure class='figure center'>
  <img src="/wp-content/uploads/error-1002@2x.png" class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Example: Authentication error during integration.</figcaption>
</figure>

**Solution:**
- Check credentials
- Sign out from your browser, then try again in GitKraken
- Clear browser cache
- Try a different default browser

Still stuck? [Contact Support](https://www.gitkraken.com/contact?product=gitkraken&source=help_center)

---

## How to fix the `Cannot read property 'fullName' of undefined` push error

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

## How to fix missing branches or files caused by capitalization issues

On case-insensitive file systems like Windows, branches or files differing only by case may not appear correctly.

<small class='text-muted'>End of document.</small>

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
