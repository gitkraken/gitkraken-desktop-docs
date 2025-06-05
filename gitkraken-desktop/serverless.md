---
title: GitKraken On-Premise Serverless (Stand-Alone) Setup
description: Learn how to install, license, and run GitKraken On-Premise Serverless on Windows, macOS, and Linux in offline or secure environments.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

**GitKraken On-Premise Serverless** (also known as *GitKraken Stand-Alone*) is designed for teams operating in disconnected or secure environments. It includes most core <a href="https://www.gitkraken.com/git-client" target=_blank>GitKraken features</a>, with additional advantages:

- Works without internet access
- Requires no account creation
- Requires no server installation

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-example-2025.png" srcset="/wp-content/uploads/serverless-example-2025@2x.png 2x" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Example view of GitKraken Serverless in use.</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately. Visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing'>On-Premise Pricing</a> page to purchase.</p>
</div>

<div class='callout callout--basic'>
    <p>To request a trial key, email <a href="mailto:sales@gitkraken.com">sales@gitkraken.com</a>.</p>
</div>

***

## How to Install GitKraken Serverless

Follow these steps to get started:

<ol>
<li><a href="https://www.gitkraken.com/download-on-premise-serverless" target=_blank>Download GitKraken Serverless</a></li>
<li>Install GitKraken Serverless</li>
<li>Load your <code>.dat</code> license file</li>
</ol>

---

### 1. Download GitKraken Serverless

Download the appropriate client for your operating system from our <a href="https://www.gitkraken.com/download-on-premise-serverless" target=_blank>downloads page</a>.

If the page is inaccessible, contact your GitKraken administrator for internal distribution options.

---

### 2. Install GitKraken Serverless

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

### 3. Load License File

At first launch, you’ll be prompted to load the `.dat` license file.

If you don’t have the file, contact your GitKraken admin. Admins can retrieve it from app.gitkraken.com. For older accounts or help locating the file, <a href="https://help.gitkraken.com/gitkraken-desktop/contact-support/">contact support</a>.

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-2025.png" srcset="/wp-content/uploads/serverless-2025@2x.png 2x" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">GitKraken Serverless ready after license activation.</figcaption>
</figure>

---

### License File Locations

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

### Updating Your License File

If your license expires, you can:

- Replace the file in one of the directories listed above
- Or, update manually:
  - In GitKraken, click the license text in the bottom-left corner
  - Select <kbd>Update License</kbd>

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-license-2025.png" srcset="/wp-content/uploads/serverless-license-2025@2x.png 2x" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Update your license manually from the client footer.</figcaption>
</figure>
