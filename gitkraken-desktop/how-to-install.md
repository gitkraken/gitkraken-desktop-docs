---
title: How to Install GitKraken Desktop
description: Step-by-step installation instructions for GitKraken Desktop on Windows, macOS, and Linux.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: May 2025</kbd>

There are three steps to success with GitKraken Desktop. That's it!

1. [Download](https://gitkraken.com/download?product=gitkraken&source=help_center) GitKraken Desktop
2. Install GitKraken Desktop
3. Use GitKraken Desktop

No Git tools are required for GitKraken Desktop, so once you’ve run the installer, you can open the app and get going.

If you want to utilize additional features such as the terminal, experimental features, or LFS, <a href='https://git-scm.com/' target="_blank">download Git</a>.

Below are platform-specific instructions and details on minimum requirements.

<div class='callout callout--basic'>
<p><strong>Looking for GitKraken On-Premise Self-Hosted installation instructions?</strong> Then please start with our <a href="https://help.gitkraken.com/gitkraken-enterprise/on-premise-system-requirements/">On-Premise System Requirements</a> page.</p>
</div>

---

## Requirements</a> page.</p>
</div>

## Requirements

Before installing, ensure your system meets these requirements:

- An internet connection to download and authorize GitKraken.
- A Git hosting service account (e.g., GitHub, GitLab, Bitbucket) to connect your repos.

---

## Windows Installation

<div class='embed-container embed-container--16-9'>
<iframe width='560' height='315' src='https://www.youtube.com/embed/d1BhUwbI4IM' frameborder='0' allowfullscreen title="GitKraken Windows Installation Guide"></iframe>
</div>

<img src="/wp-content/uploads/install-windows-2025.png" class="help-center-img img-bordered" alt="GitKraken Windows installer screen">

Download and run the installer:

[Download GitKraken for Windows](https://www.gitkraken.com/download?platform=windows&product=gitkraken&source=help_center)

The installer automatically handles updates and path configuration.

To verify installation:

1. Open GitKraken from the Start Menu.
2. Check the version under <kbd>Preferences > About GitKraken</kbd>.

### GitKraken Data Location on Windows

GitKraken Desktop data is stored with your home profile at:

<code>C:\Users\{user}\AppData\Roaming\.gitkraken</code>

To view this location from the app:

Go to <kbd>Preferences > About GitKraken</kbd> and click the link under <strong>Data location</strong> to open the folder in Explorer.

---

## macOS Installation

<div class='embed-container embed-container--16-9'>
<iframe width='560' height='315' src='https://www.youtube.com/embed/22HD1ZnNytk?ecver=1' frameborder='0' allowfullscreen title="GitKraken macOS Installation Guide"></iframe>
</div>

<figure class='figure center'>
<img src="/wp-content/uploads/install-mac-2025.png" class="help-center-img img-bordered" alt="GitKraken macOS drag-to-install screen">
<figcaption style="text-align: center; color: #888;">Drag and drop the GitKraken icon to the Applications folder.</figcaption>
</figure>

[Download GitKraken for macOS](https://www.gitkraken.com/download?platform=mac&product=gitkraken&source=help_center)

After installing:

1. Launch GitKraken from the Applications folder.
2. Authorize when prompted.

---

## Linux Installation

<div class='embed-container embed-container--16-9'>
<iframe width="560" height="315" src="https://www.youtube.com/embed/Cx4aQzlMSw4?ecver=1" frameborder="0" allowfullscreen title="GitKraken Linux Installation Guide"></iframe>
</div>

### GitKraken Data Location on Linux

GitKraken Desktop stores user data in your home directory at:

<code>~/.config/gitkraken</code>

GitKraken supports the following Linux distributions:

- `.deb` packages: Ubuntu 18.04+ LTS or Debian 10+
- `.rpm` packages: RHEL 8+ or Fedora 39+

<div class='callout callout--basic'>
<p><strong>Note:</strong> While GitKraken Desktop may be able to be installed on other Linux distributions, we cannot guarantee that it will work as expected.</p>
</div>

<img src="/wp-content/uploads/install-linux-2025.png" class="help-center-img img-bordered" alt="GitKraken Linux install options">

GitKraken is available for `.deb`, `.rpm`, and `.tar.gz` formats.

### Debian/Ubuntu (.deb)
```bash
sudo dpkg -i gitkraken-amd64.deb
sudo apt-get install -f
```

### Fedora/RHEL (.rpm)
```bash
sudo dnf install ./gitkraken-amd64.rpm
```

### Generic (.tar.gz)
```bash
tar -xvzf gitkraken.tar.gz
./gitkraken
```

For all Linux versions:

- Install from [gitkraken.com](https://www.gitkraken.com/download?platform=linux&product=gitkraken&source=help_center).
- GitKraken Desktop is also available via Snap. You can learn more at the <a href="https://snapcraft.io/gitkraken" target="_blank">Snapcraft GitKraken page</a>. To install:
  ```bash
  sudo snap install gitkraken --classic
  ```
- GitKraken is not officially supported on WSL. If you choose to install it within a WSL environment, you may experience unexpected behavior. For more information, see <a href="https://help.gitkraken.com/gitkraken-desktop/wsl/" target="_blank">GitKraken and WSL</a>.
- After installing, launch GitKraken and connect your Git provider.

---

## Git Executable CLI (Optional)

GitKraken Desktop includes an internal Git binary. For advanced use or compatibility, you can configure GitKraken to use your system’s Git executable.

Enable this from <kbd>Preferences > Experimental > Git Executable</kbd>.

<img src="/wp-content/uploads/enable-git-executable-2025.png" class="help-center-img img-bordered" alt="Enable Git Executable in Preferences">

You can also specify a Git path manually.

---

## GitKraken CLI (Optional)

GitKraken Desktop includes a built-in GitKraken CLI, offering terminal-style Git operations with visual feedback.

You can open the CLI by pressing <kbd>Ctrl/Cmd + Shift + P</kbd> or selecting <kbd>Open GitKraken CLI</kbd> from the toolbar.

<img src="/wp-content/uploads/open-gitkraken-cli-2025.png" class="help-center-img img-bordered" alt="Open GitKraken CLI">

---

## WSL

If you're attempting to use GitKraken Desktop within Windows Subsystem for Linux (WSL), visit our page on <a href="https://help.gitkraken.com/gitkraken-desktop/windows-subsystem-for-linux/">How to use GitKraken Desktop with WSL</a> for additional details.

## Run GitKraken Desktop

Upon installation, some Linux distros do not automatically create shortcuts to the app.

To run GitKraken Desktop manually, open the terminal and type `gitkraken` to start the app.

## GitKraken Desktop Overview

Watch the video below to explore GitKraken Desktop features:

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/LBlijN29gb8?rel=0&vq=hd1080' frameborder='0' allowfullscreen title="GitKraken Desktop Overview"></iframe>
</div>
