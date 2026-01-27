---
title: Use GitKraken Desktop with Windows Subsystem for Linux (WSL 2)
description: Step-by-step guide to using GitKraken Desktop in WSL 2, including setup, installation, GUI support, known issues, and file system access.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

Learn how to run GitKraken Desktop on Windows Subsystem for Linux (WSL 2), including GUI integration and installation requirements.

## What is WSL/WSL 2?

<a href="https://learn.microsoft.com/en-us/windows/wsl/about" target="_blank">Windows Subsystem for Linux (WSL)</a> enables developers to run a Linux distribution and use Linux tools directly on Windows. <a href="https://learn.microsoft.com/en-us/windows/wsl/compare-versions" target="_blank">WSL 2</a> runs an actual Linux kernel in a managed VM, offering better performance and full system call compatibility.

To support Linux GUI apps, Microsoft introduced <a href="https://learn.microsoft.com/en-us/windows/wsl/tutorials/gui-apps" target="_blank">WSLg</a>, which integrates Linux apps into the Windows desktop experience. This feature makes GitKraken Desktop for Linux run smoothly within WSL 2.

> Microsoft recommends storing project files on the same operating system as the tools you're using to avoid cross-OS performance issues.

## How to use GitKraken Desktop with WSL 2

<figure class='figure center'>
    <img src="/wp-content/uploads/wsl-full-screen.png" 
         srcset="/wp-content/uploads/wsl-full-screen@2x.png" 
         class="help-center-img img-bordered" 
         alt="Full-screen view of GitKraken Desktop running on a WSL 2 environment with the repository, branches, commit graph, and details visible.">
    <figcaption style="text-align: center; color: #888;">GitKraken Desktop running inside WSL 2.</figcaption>
</figure>

GitKraken Desktop works with repositories stored on your WSL 2 file system when installed and launched inside the WSL environment. With <a href="https://learn.microsoft.com/en-us/windows/wsl/tutorials/gui-apps" target="_blank">WSLg</a>, GitKraken Desktop displays natively within Windows.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitKraken Desktop does not support accessing repos across file systems. Install GitKraken on the OS where your repos are stored to avoid degraded performance or non-functional features.</p>
</div>

GitKraken will notify you when accessing repos across environments. For more, see [Working Across File Systems](#working-across-file-systems-in-wsl-2).

### Setup Steps

Follow these four steps to get started:

1. **Update WSL 2** — Ensure the latest version is installed with WSLg support.
2. **Download GitKraken Desktop** — Get the latest Linux version.
3. **Install in WSL** — Run the installer from your WSL 2 terminal.
4. **Launch GitKraken Desktop** — You're ready to start working!

> Most WSL distributions include Git by default. If needed, [install or update Git for Linux](https://git-scm.com/download/linux).

---

## WSL 2/WSLg Requirements

- Windows 11 or Windows 10 build 19044+
- WSL 2 distribution
- GitKraken Desktop version 9.1.0+ for Linux

---

## Install or Update WSL 2 with WSLg Support

GitKraken Desktop requires WSL 2 with WSLg support on Windows 11 or Windows 10 build 19044 or later.

To update WSL from PowerShell or Command Prompt (run as Administrator):

```bash
wsl --update
```

To install WSL with Ubuntu as the default distribution:

```bash
wsl --install -d ubuntu
```

After rebooting, complete the setup by creating a Linux username and password.

WSLg is automatically included in this installation.

---

## Download and Install GitKraken Desktop on WSL 2

To install GitKraken Desktop within WSL, follow the <a href="https://help.gitkraken.com/gitkraken-desktop/how-to-install/#linux-deb-rpm-and-tar-gz-files" target="_blank">Linux installation instructions</a>.

For Ubuntu users:

```bash
wget https://api.gitkraken.dev/releases/production/linux/x64/active/gitkraken-amd64.deb
sudo apt install ./gitkraken-amd64.deb
```

If dependencies are missing, fix broken packages with:

```bash
sudo apt --fix-broken install
```

Then, launch GitKraken Desktop with:

```bash
gitkraken
```

> If using the `.tar.gz` version, ensure `gitkraken` is in your PATH for the above command to work.

---

## Preferences for GitKraken on WSL 2

GitKraken Desktop offers preferences to control how URLs and files are opened from the WSL environment. Navigate to `Preferences` > `General` to configure them.

<figure class='figure center'>
    <img src="/wp-content/uploads/wsl-host-settings.png" srcset="/wp-content/uploads/wsl-host-settings@2x.png" class="help-center-img img-bordered" alt="GitKraken WSL host settings">
    <figcaption style="text-align: center; color: #888;">Choose where to open URLs and files when using GitKraken within WSL 2.</figcaption>
</figure>

By default:
- URLs open in your Windows default browser.
- Files attempt to open on the WSL host distribution.

---

## Known Issues with WSL 2

Here are known limitations when using GitKraken Desktop with WSLg:

- <a href="https://github.com/microsoft/wslg/issues/388" target="_blank">HiDPI displays</a> may cause WSLg to inconsistently scale the UI.
- <a href="https://github.com/microsoft/wslg/issues/727" target="_blank">Window snapping</a> might not function properly within WSLg.

---

## Troubleshooting WSL 2

If GitKraken opens with a black screen or other display issues, try these fixes:

- Reopen GitKraken Desktop as administrator.
- Update your graphics drivers.

If issues persist, you can disable GPU acceleration:

```bash
gitkraken --disable-gpu
```

To bypass certificate errors (e.g., `NET::ERR_CERT_AUTHORITY_INVALID`), run:

```bash
gitkraken --ignore-certificate-errors
```

To fully restart WSL (use PowerShell or Command Prompt as administrator):

```bash
wsl --shutdown
```

Then, reopen your Linux distribution or GitKraken Desktop.

---

## Working Across File Systems in WSL 2

GitKraken Desktop does not support opening repos stored on a different file system than where GitKraken is installed.

For the best experience:
- Install GitKraken Desktop on both Windows and WSL.
- Use the correct GitKraken instance based on repo location.

When accessing a repo stored on WSL from GitKraken installed on Windows (or vice versa), you'll see a prompt:

<figure class='figure center'>
    <img src="/wp-content/uploads/wsl-toast.png" 
         srcset="/wp-content/uploads/wsl-toast@2x.png" 
         class="help-center-img img-bordered" 
         alt="Warning prompt in GitKraken Desktop stating that working with repositories stored on WSL is not recommended from GitKraken on Windows, with options to open Help Center, open with GitKraken in Ubuntu, or open the repository anyway.">
    <figcaption style="text-align: center; color: #888;">Prompt for cross-system repo access in GitKraken Desktop.</figcaption>
</figure>

You can choose:
- **Open Help Center** — Opens this guide.
- **Open with GitKraken on Ubuntu/Windows** — Switch to the correct GitKraken instance.
- **Open Anyway** — Attempt to open the repo (may result in degraded performance or broken features).
- **Close** — Cancels the action.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitKraken cannot detect cross-system access when using mapped network drives. This may lead to unintended behavior.</p>
</div>


