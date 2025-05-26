---
title: How to Install GitKraken Desktop
description: Step-by-step installation instructions for GitKraken Desktop on Windows, macOS, and Linux.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: May 2025</kbd>

This guide covers how to install GitKraken Desktop across Windows, macOS, and various Linux distributions. It also explains optional command-line enhancements.

---

## Requirements

Before installing, ensure your system meets these requirements:

- An internet connection to download and authorize GitKraken.
- A Git hosting service account (e.g., GitHub, GitLab, Bitbucket) to connect your repos.

---

## Windows Installation

Download and run the installer:

[Download GitKraken for Windows](https://www.gitkraken.com/download?platform=windows&product=gitkraken&source=help_center)

The installer automatically handles updates and path configuration.

To verify installation:

1. Open GitKraken from the Start Menu.
2. Check the version under <kbd>Preferences > About GitKraken</kbd>.

---

## macOS Installation

Download the `.dmg` file and drag GitKraken to your Applications folder:

[Download GitKraken for macOS](https://www.gitkraken.com/download?platform=mac&product=gitkraken&source=help_center)

After installing:

1. Launch GitKraken from the Applications folder.
2. Authorize when prompted.

---

## Linux Installation

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

## GitKraken Desktop Overview

Watch the video below to explore GitKraken Desktop features:

<div class='embed-container embed-container--16-9'>
    <iframe width='560' height='315' src='https://www.youtube.com/embed/LBlijN29gb8?rel=0&vq=hd1080' frameborder='0' allowfullscreen title="GitKraken Desktop Overview"></iframe>
</div>
