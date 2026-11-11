---
title: Use GitKraken Desktop with Windows Subsystem for Linux (WSL 2)
description: Step-by-step guide to using GitKraken Desktop in WSL 2, including setup, installation, GUI support, known issues, and file system access.
product: GitKraken Desktop
feature: WSL 2 Support
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, WSL]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [wsl, wsl2, windows, linux, setup]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-working-with-repositories"
    nav_label: "Windows Subsystem for Linux (WSL 2)"
    nav_order: 180
    nav_parent: "desktop-working-with-repositories"
    page_type: "content"
    card_icon: "brand-windows"
    card_color: "amber"
    card_description: "Run GitKraken Desktop in WSL 2"
---
<kbd>Last updated: November 2026</kbd>

Use this page to install and run GitKraken Desktop inside Windows Subsystem for Linux 2 (WSL 2) when your repositories live on the Linux file system.

**Requirements and limits**
- Windows requirement: Windows 11 or Windows 10 build 19044+
- Linux requirement: WSL 2 distribution with WSLg support
- GitKraken Desktop requirement: GitKraken Desktop 9.1.0+ for Linux
- Repository location rule: Keep repositories on the same file system as the GitKraken Desktop installation you use
- Cross-file-system warning: Opening WSL repositories from GitKraken Desktop on Windows, or Windows repositories from GitKraken Desktop in WSL, can cause degraded performance or broken features
- Coding agent note: In WSL, Windows-installed coding agent CLIs can take precedence over WSL-installed CLIs and prevent agent sessions from starting correctly
- Known issues: WSLg may have HiDPI scaling and window-snapping limitations

***

## Quick Start


1. **Update WSL 2**: From PowerShell or Command Prompt (run as Administrator), run `wsl --update`. To install WSL with Ubuntu, run `wsl --install -d ubuntu` and reboot.
2. **Download GitKraken Desktop for Linux**: For Ubuntu, run:
   ```bash
   wget https://api.gitkraken.dev/releases/production/linux/x64/active/gitkraken-amd64.deb
   sudo apt install ./gitkraken-amd64.deb
   ```
3. **Launch GitKraken Desktop**: Run `gitkraken` in your WSL 2 terminal. With WSLg installed, the app displays natively within Windows.

Keep your repositories on the same file system as the GitKraken Desktop installation you use. Opening repositories across file systems (for example, opening a WSL repository from GitKraken Desktop installed on Windows) degrades performance or breaks features. When you do this, GitKraken Desktop prompts you to open the repository with the correct installation.

## What WSL and WSL 2 are

<a href="https://learn.microsoft.com/en-us/windows/wsl/about" target="_blank">Windows Subsystem for Linux (WSL)</a> lets you run a Linux distribution and use Linux tools directly on Windows. <a href="https://learn.microsoft.com/en-us/windows/wsl/compare-versions" target="_blank">WSL 2</a> runs an actual Linux kernel in a managed VM, which gives better performance and full system call compatibility.

To run Linux GUI apps, WSL 2 uses <a href="https://learn.microsoft.com/en-us/windows/wsl/tutorials/gui-apps" target="_blank">WSLg</a>, which shows Linux apps on the Windows desktop. WSLg lets GitKraken Desktop for Linux run within WSL 2.

> Microsoft recommends storing project files on the same operating system as the tools you're using to avoid cross-OS performance issues.

## How to use GitKraken Desktop with WSL 2

<figure class='figure center'>
    <img src="/wp-content/uploads/wsl-full-screen@2x.png" 
         class="help-center-img img-bordered" 
         alt="Full-screen view of GitKraken Desktop running on a WSL 2 environment with the repository, branches, commit graph, and details visible.">
    <figcaption style="text-align: center; color: #888;">GitKraken Desktop running inside WSL 2.</figcaption>
</figure>

GitKraken Desktop works with repositories stored on your WSL 2 file system when installed and launched inside the WSL environment. With <a href="https://learn.microsoft.com/en-us/windows/wsl/tutorials/gui-apps" target="_blank">WSLg</a>, GitKraken Desktop displays natively within Windows.

> **Note:** GitKraken Desktop does not support accessing repos across file systems. Install GitKraken Desktop on the OS where your repos are stored to avoid degraded performance or non-functional features.


> **Warning:** **Coding agent note:** If you use the Agents view in WSL, make sure the coding agent CLI you want to run is the one available in your WSL environment. In some cases, a Windows-installed coding agent can take precedence over a WSL-installed one, which can prevent the agent session from starting correctly. For more information, see <a href="/gitkraken-desktop/agents/">Coding Agents in GitKraken Desktop</a>.

GitKraken Desktop notifies you when you open a repository from the other environment. For more information, see [How cross-file-system access works in WSL 2](#how-cross-file-system-access-works-in-wsl-2).

### How to set up GitKraken Desktop in WSL 2

To get started:

1. **Update WSL 2**: Make sure the latest version is installed with WSLg support.
2. **Download GitKraken Desktop**: Get the latest Linux version.
3. **Install in WSL**: Run the installer from your WSL 2 terminal.
4. **Launch GitKraken Desktop**: Run `gitkraken` in your WSL 2 terminal.

> Most WSL distributions include Git by default. If needed, [install or update Git for Linux](https://git-scm.com/download/linux).

---

## WSL 2 and WSLg requirements

- Windows 11 or Windows 10 build 19044+
- WSL 2 distribution
- GitKraken Desktop version 9.1.0+ for Linux

---

## How to install or update WSL 2 with WSLg support

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

This installation includes WSLg.

---

## How to download and install GitKraken Desktop on WSL 2

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

> If you installed the `.tar.gz` version, make sure `gitkraken` is in your `PATH` so this command works.

---

## How WSL-specific GitKraken preferences work

In WSL, you can choose where GitKraken Desktop opens URLs and files. To configure these settings, go to <kbd>Preferences > General</kbd>.

<figure class='figure center'>
    <img src="/wp-content/uploads/wsl-host-settings@2x.png" class="help-center-img img-bordered" alt="GitKraken WSL host settings">
    <figcaption style="text-align: center; color: #888;">Choose where to open URLs and files when using GitKraken within WSL 2.</figcaption>
</figure>

By default:
- URLs open in your Windows default browser.
- GitKraken Desktop tries to open files on the WSL host distribution.

---

## Known issues with WSL 2

GitKraken Desktop has these known limitations with WSLg:

- <a href="https://github.com/microsoft/wslg/issues/388" target="_blank">HiDPI displays</a> may cause WSLg to inconsistently scale the UI.
- <a href="https://github.com/microsoft/wslg/issues/727" target="_blank">Window snapping</a> might not function properly within WSLg.
- Windows-installed coding agent CLIs can take precedence over WSL-installed CLIs, which may cause coding agent sessions to fail to start as expected.

---

## How to troubleshoot WSL 2 issues

If GitKraken Desktop opens with a black screen or other display issues, try these fixes:

- Reopen GitKraken Desktop as administrator.
- Update your graphics drivers.

If issues persist, you can disable GPU acceleration:

```bash
gitkraken --disable-gpu
```

To bypass certificate errors (for example, `NET::ERR_CERT_AUTHORITY_INVALID`), run:

```bash
gitkraken --ignore-certificate-errors
```

To fully restart WSL, run this command from PowerShell or Command Prompt as administrator:

```bash
wsl --shutdown
```

Then, reopen your Linux distribution or GitKraken Desktop.

### How to sign in and connect integrations from WSL 2

When you sign in to your GitKraken account or connect an integration from GitKraken Desktop in WSL 2, the sign-in page opens in your Windows browser. GitKraken Desktop on Windows then completes the sign-in for GitKraken Desktop in your WSL distribution, so install GitKraken Desktop on Windows as well as in WSL.

If the hand-off fails, GitKraken Desktop on Windows shows one of these messages:

- **Could not complete sign-in: GitKraken Desktop is not installed in WSL distro {name}.** Install GitKraken Desktop in that distribution.
- **Could not complete sign-in: failed to launch GitKraken Desktop in WSL distro {name}.** Start GitKraken Desktop in WSL, then try again.
- **Could not complete sign-in: invalid WSL distro name.**

Each message ends with **Sign in again from GitKraken Desktop in WSL.** Start the sign-in again from GitKraken Desktop in WSL. If GitKraken Desktop is not installed on Windows, sign in with **Manually enter authentication code** in the **Sign In to GitKraken** window instead: paste the code from your browser and click **Save**.

---

## How cross-file-system access works in WSL 2

GitKraken Desktop does not support opening repos stored on a different file system than the one where GitKraken Desktop is installed.

For the best experience:
- Install GitKraken Desktop on both Windows and WSL.
- Open each repository with the GitKraken Desktop installation on the same file system.

When you open a repository stored in WSL from GitKraken Desktop on Windows, or the reverse, GitKraken Desktop shows a prompt:

<figure class='figure center'>
    <img src="/wp-content/uploads/wsl-toast@2x.png" 
         class="help-center-img img-bordered" 
         alt="Warning prompt in GitKraken Desktop stating that working with repositories stored on WSL is not recommended from GitKraken on Windows, with options to open Help Center, open with GitKraken in Ubuntu, or open the repository anyway.">
    <figcaption style="text-align: center; color: #888;">Prompt for cross-system repo access in GitKraken Desktop.</figcaption>
</figure>

You can choose:
- **Open Help Center**: Opens this guide.
- **Open with GitKraken in Ubuntu** (your distribution's name) or **Open with GitKraken in Windows**: Switches to the GitKraken Desktop installation on the same file system as the repository.
- **Open Repository Anyway**: Tries to open the repository, which may degrade performance or break features.
- **Close**: Cancels the action.

> **Note:** GitKraken Desktop cannot detect cross-system access through mapped network drives, which can lead to unexpected behavior.
