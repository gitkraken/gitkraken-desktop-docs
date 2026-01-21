---
title: Install GitKraken Desktop on Windows, macOS & Linux | Setup Guide
description: Step-by-step installation guide for GitKraken Desktop on Windows, macOS, and Linux. Includes system requirements, video tutorials, and tips for WSL users.

taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

GitKraken Desktop is a graphical Git client designed to make version control easier for developers, builders, and teams.

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

