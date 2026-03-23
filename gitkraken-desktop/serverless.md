---
title: GitKraken On-Premise Serverless (Stand-Alone) Setup
description: Learn how to install, license, and run GitKraken On-Premise Serverless on Windows, macOS, and Linux in offline or secure environments.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to install and license GitKraken On-Premise Serverless, also called GitKraken Stand-Alone, when your team works in offline or tightly controlled environments. It covers platform-specific installation steps, supported license file locations, and the manual license update flow required after expiration or renewal.

**GitKraken On-Premise Serverless** (also known as *GitKraken Stand-Alone*) is designed for teams operating in disconnected or secure environments. It includes most core <a href="https://www.gitkraken.com/git-client" target=_blank>GitKraken features</a>, with additional advantages:

- Works without internet access
- Requires no account creation
- Requires no server installation

***

## Quick Start

Install and activate GitKraken On-Premise Serverless for use in offline or secure environments.

1. Download the GitKraken Serverless installer for your operating system from the [downloads page](https://www.gitkraken.com/download-on-premise-serverless).
2. Install the application:
   - **Windows**: Double-click the `.exe` file and follow the setup prompts.
   - **macOS**: Open the DMG and drag the GitKraken icon to your Applications folder.
   - **Linux (.deb)**: Run `wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.deb && dpkg -i gitkraken-amd64.deb`.
3. At first launch, load your `.dat` license file when prompted. If you do not have the file, contact your GitKraken administrator.

If your license expires, replace the `.dat` file in one of the supported directories or click the license text in the bottom-left corner of the app and select **Update License**. GitKraken Serverless is sold separately from standard subscriptions.

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-example-2025@2x.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Example view of GitKraken Serverless in use.</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately. Visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing'>On-Premise Pricing</a> page to purchase.</p>
</div>

<div class='callout callout--basic'>
    <p>To request a trial key, email <a href="mailto:sales@gitkraken.com">sales@gitkraken.com</a>.</p>
</div>

***

## How to install GitKraken Serverless

Follow these steps to get started:

<ol>
<li><a href="https://www.gitkraken.com/download-on-premise-serverless" target=_blank>Download GitKraken Serverless</a></li>
<li>Install GitKraken Serverless</li>
<li>Load your <code>.dat</code> license file</li>
</ol>

---

### How to download GitKraken Serverless

Download the appropriate client for your operating system from our <a href="https://www.gitkraken.com/download-on-premise-serverless" target=_blank>downloads page</a>.

If the page is inaccessible, contact your GitKraken administrator for internal distribution options.

---

### How to install GitKraken Serverless on each platform

#### Windows (.exe)

**System Requirements:** Windows 10+

**Install:** Double-click the downloaded `.exe` file and follow the setup instructions.

**Data Location:**
- `C:\Users\{user}\AppData\Roaming`
- `%APPDATA%\.gitkraken` (for older versions)

<figure class='figure center'>
  <img src="/wp-content/uploads/license.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Prompt to load license file after install.</figcaption>
</figure>

---

#### macOS (.dmg)

**System Requirements:**
- Intel: macOS 10.15+
- Apple Silicon: macOS 11+

**Install:** Open the DMG file and drag the GitKraken icon into your Applications folder.

**Data Location:** `/Users/{user}/.gitkraken` (or `~/.gitkraken`)

---

#### Linux (.deb, .rpm, .tar.gz)

**System Requirements:**
- `.deb`: Ubuntu 18.04+ LTS, Debian 10+
- `.rpm`: RHEL 8+, Fedora 39+

**Install Commands:**

`.deb`
```
wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.deb
dpkg -i gitkraken-amd64.deb
```

`.tar.gz`
```
wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.tar.gz
tar -xvzf gitkraken-amd64.tar.gz
```

`.rpm`
```
wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.rpm
sudo dnf install ./gitkraken-amd64.rpm
```

**Note:** For older distros, use `yum` if `dnf` is not available.

**Data Location:** `/home/{user}/.gitkraken` (or `~/.gitkraken`)

---

### How to load the license file

At first launch, you’ll be prompted to load the `.dat` license file.

If you don’t have the file, contact your GitKraken admin. Admins can retrieve it from app.gitkraken.com. For older accounts or help locating the file, <a href="https://help.gitkraken.com/gitkraken-desktop/contact-support/">contact support</a>.

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-2025@2x.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">GitKraken Serverless ready after license activation.</figcaption>
</figure>

---

### Where GitKraken checks for license files

GitKraken checks the following locations for license files:

**Linux/macOS:**
- `/usr/local/share/gitkraken`
- `/usr/share/gitkraken`
- Directory above application
- Application directory
- `~/.gitkraken`

**Windows:**
- `C:\ProgramData\GitKraken`
- Directory above the `.exe`
- Directory of the `.exe`
- `%APPDATA%\.gitkraken`

---

### How to update the license file

If your license expires, you can:

- Replace the file in one of the directories listed above
- Or, update manually:
  - In GitKraken, click the license text in the bottom-left corner
  - Select <kbd>Update License</kbd>

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-license-2025@2x.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Update your license manually from the client footer.</figcaption>
</figure>

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
