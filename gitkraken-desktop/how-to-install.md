---
title: Install GitKraken Desktop on Windows, macOS & Linux | Setup Guide
description: Step-by-step installation guide for GitKraken Desktop on Windows, macOS, and Linux. Includes system requirements, video tutorials, and tips for WSL users.

taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

GitKraken Desktop is a graphical Git client designed to make version control easier for developers, builders, and teams.

***

## Quick Start

Install GitKraken Desktop on your operating system in three steps.

1. [Download GitKraken Desktop](https://gitkraken.com/download?product=gitkraken&source=help_center) for your platform.
2. Run the installer:
   - **Windows**: Double-click the `.exe` file. GitKraken Desktop installs and launches automatically.
   - **macOS**: Open the `.dmg` file and drag the GitKraken icon into your Applications folder.
   - **Linux (.deb)**: Run `wget https://release.gitkraken.com/linux/gitkraken-amd64.deb && sudo apt install ./gitkraken-amd64.deb`.
   - **Linux (.rpm)**: Run `wget https://release.gitkraken.com/linux/gitkraken-amd64.rpm && sudo dnf install ./gitkraken-amd64.rpm`.
3. Launch GitKraken Desktop:
   - **Windows/macOS**: Use the shortcut or Applications folder.
   - **Linux**: Run `gitkraken` in a terminal.

No Git command-line tools are required for basic use. For advanced features like the terminal, Git LFS, or experimental tools, [install Git from git-scm.com](https://git-scm.com/).

***

## Installation Instructions

There are three simple steps to get started with GitKraken Desktop:

1. [Download GitKraken Desktop](https://gitkraken.com/download?product=gitkraken&source=help_center)
2. Install GitKraken Desktop
3. Launch and start using GitKraken Desktop

No Git command-line tools are required. Once you run the installer, you can open the app and start working with your repositories.

If you want to use advanced features such as the terminal, experimental tools, or Git LFS, we recommend you [download Git from git-scm.com](https://git-scm.com/).

Below are platform-specific installation instructions and system requirements.

<div class='callout callout--basic'>
    <p>Looking for <em>GitKraken On-Premise Self-Hosted</em> installation instructions? Please begin with our <a href="/enterprise/system-requirements">On-Premise System Requirements</a> page.</p>
</div>

---

## Windows (.exe file)

**System requirements:** Windows 10+

- [Download GitKraken Desktop for Windows (64-bit)](https://gitkraken.com/download/windows64)

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/obIK_732_9M?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

### Install Instructions

In your terminal, run the following:

Double-click the downloaded executable file. A splash screen will appear while GitKraken Desktop is installed. The application will automatically start when installation completes.

### Windows Data Location

GitKraken Desktop data is stored in your user profile directory at:

```
C:\\Users\\{user}\\AppData\\Roaming\\.gitkraken
```

---

## macOS (.dmg file)

**System requirements:**
- Intel: macOS 12+
- Apple Silicon: macOS 12+

- [Download GitKraken Desktop for macOS](https://gitkraken.com/download/mac?product=gitkraken&source=help_center)

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/22HD1ZnNytk?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

### Install Instructions

Double-click the downloaded DMG file. When prompted, drag and drop the GitKraken icon into your Applications folder.

<figure class='figure center'>
    <img src="/wp-content/uploads/mac-install.png" class="help-center-img img-bordered" alt="Mac installation dialog prompting user to drag the GitKraken icon into the Applications folder.">
    <figcaption style="text-align: center; color: #888;">Drag and drop the GitKraken icon to the Applications folder.</figcaption>
</figure>

### macOS Data Location

GitKraken Desktop data is stored in:

```
/Users/{user}/.gitkraken
```

or using the shorthand:

```
~/.gitkraken
```

---

## Linux (.deb, .rpm, .tar.gz, Snap)

**System requirements:**
- **.deb**: Ubuntu 18.04+ LTS or Debian 10+
- **.rpm**: RHEL 8+ or Fedora 39+

<div class='callout callout--warning'>
    <p>Note 📝 - GitKraken Desktop officially supports Ubuntu 18.04+ LTS, RHEL 8+, and Fedora 39+. While it may run on other distributions, compatibility is not guaranteed.</p>
</div>

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Cx4aQzlMSw4?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

### .deb Installation
In your terminal, run:
```bash
wget https://release.gitkraken.com/linux/gitkraken-amd64.deb
sudo apt install ./gitkraken-amd64.deb
```
Or [download the .deb installation package](https://gitkraken.com/download/linux-deb?product=gitkraken&source=help_center).

### .rpm Installation
```bash
wget https://release.gitkraken.com/linux/gitkraken-amd64.rpm
sudo dnf install ./gitkraken-amd64.rpm
```
Or [download the .rpm installation package](https://gitkraken.com/download/linux-rpm?product=gitkraken&source=help_center).

> For older distributions without `dnf`, use `yum` instead.

### .tar.gz Installation
```bash
wget https://release.gitkraken.com/linux/gitkraken-amd64.tar.gz
sudo tar -xvzf gitkraken-amd64.tar.gz
```
Or [download the .tar.gz archive](https://gitkraken.com/download/linux-gzip?product=gitkraken&source=help_center).

### Snap Installation

Install GitKraken from [Snapcraft.io](https://snapcraft.io/gitkraken?product=gitkraken&source=help_center).

### Linux Data Location

GitKraken Desktop data is stored in:

```
/home/{user}/.gitkraken
```

or

```
~/.gitkraken
```

### WSL Support

To use GitKraken Desktop with Windows Subsystem for Linux (WSL), refer to [our WSL setup guide](https://help.gitkraken.com/gitkraken-desktop/windows-subsystem-for-linux/).

---

## Launching GitKraken Desktop

Once installed, launch GitKraken Desktop as follows:

- **Windows:** Use the Start Menu shortcut or search for GitKraken.
- **macOS:** Open the Applications folder and double-click GitKraken.
- **Linux:** Open a terminal and run:

```bash
gitkraken
```

You’re now ready to start using GitKraken! For help getting started with repositories, branches, and remotes, check out the [Getting Started Guide](https://help.gitkraken.com/gitkraken-client/introduction-to-gitkraken-client/).


<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;width:28px;height:28px;padding:0;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s,width .15s,padding .15s}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3);width:auto;padding:0 8px;gap:4px}
</style>
<script>(function(){var C='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2 2v1"></path></svg>',K='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg><span style="font-size:11px;margin-left:4px;font-family:sans-serif">Copied!</span>';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).replace(/[\r\n]+$/, '')).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
