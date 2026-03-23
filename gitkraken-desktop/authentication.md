---
title: Authentication with Other Git Hosts in GitKraken Desktop
description: Learn how to authenticate with TFS, AWS CodeCommit, Google Cloud Source Repositories, and custom Git hosts using HTTPS or SSH in GitKraken Desktop.
taxonomy:
  category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to authenticate GitKraken Desktop with Git hosts that do not have a dedicated integration page, including TFS, AWS CodeCommit, Google Cloud Source Repositories, and custom services. It covers HTTPS cloning, SSH key setup, SSH agent usage, proxy handling, and credential reset behavior.

<figure>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OA9o09Bq5M8?ecver=1" frameborder="0" allowfullscreen title="Authentication Overview Video"></iframe>
</div>
</figure>

***

## Quick Start

Authenticate GitKraken Desktop with a Git hosting service using either HTTPS or SSH.

**To clone with HTTPS:**
1. Copy the HTTPS URL from your hosting service (e.g., `https://example.com/username/repo.git`).
2. In GitKraken Desktop, go to <kbd>File > Clone Repo</kbd>.
3. Paste the URL and click **Clone the repo**.

**To set up SSH and clone with SSH:**
1. Go to <kbd>Preferences > SSH</kbd>.
2. Generate a new SSH key pair or browse to an existing one.
3. Copy the public key and add it to your hosting service's SSH settings.
4. Copy the SSH URL from your hosting service.
5. Go to <kbd>File > Clone</kbd>, paste the SSH URL, and click **Clone the repo**.

To use a local SSH agent instead of managing keys manually, enable **Use local SSH agent** under <kbd>Preferences > SSH</kbd>. To reset stored HTTPS credentials, go to <kbd>Preferences > General</kbd> and click **Forget All**.

***

## How HTTPS authentication works

This is the default and most common method for interacting with remotes. It requires your Git username and password.

### How to clone with HTTPS

1. Copy the HTTPS URL from your hosting service, which typically looks like:

    ```
    https://example.com/username/myrepository.git
    ```

2. In GitKraken Desktop, go to <kbd><strong>File > Clone Repo</strong></kbd>.

<figure>
<img src='/wp-content/uploads/clone-repository-menu-2025@2x.png' alt="GitKraken Clone Repo Menu" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Cloning a repository using HTTPS</figcaption>
</figure>

3. Paste the URL, click <button class='button button--success button--ui button--nolink'>Clone the repo</button>, and open it in GitKraken.

The remote tracking at `origin` is automatically set using this HTTPS format.

***

## How SSH authentication works

<figure>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/z7jVOenqFYk?ecver=1" frameborder="0" allowfullscreen title="SSH Authentication Video"></iframe>
</div>
</figure>

Before cloning via SSH, you must first set up your SSH keys in GitKraken Desktop.

### How to set up SSH keys

1. Navigate to <kbd><strong>Preferences > SSH</strong></kbd>.

<figure>
<img src="/wp-content/uploads/ssh-preferences-2025@2x.png" alt="SSH Preferences Menu" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">SSH preferences in GitKraken Desktop</figcaption>
</figure>

2. You can browse to select an existing SSH key pair or generate a new one (recommended).
3. Copy the public key to your remote hosting service.

### How to clone over SSH

1. Copy the SSH URL from your hosting service.
2. In GitKraken Desktop, go to <em class='context-menu'>File <i class="fa fa-caret-right"></i> Clone</em>.

<figure>
<img src='/wp-content/uploads/ssh-clone-2025@2x.png' alt="Clone over SSH UI" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Cloning a repository using SSH</figcaption>
</figure>

3. Paste the SSH URL, click <button class='button button--success button--ui button--nolink'>Clone the repo</button>, and open the repo.

### Supported SSH formats

    ssh://{user}@{host}/{repo}
    {user}@{host}:{repo}

Where:
- `{host}` is the domain (e.g., example.com)
- `{user}` is the username (typically `git`)
- `{repo}` is the path to the repository

<figure>
<figcaption style="text-align: center; color: #888">Example: git@example.com:org/username/myrepository.git</figcaption>
</figure>

### How to use custom SSH ports

Use this format:

    ssh://{user}@{host}:{port}/{repo}

### How to use a local SSH agent

Using a local agent can simplify SSH management, especially across multiple profiles. From <kbd><strong>Preferences > SSH</strong></kbd>, check _Use local SSH agent_.

> Tip: This allows automatic key usage if already loaded in your system's agent.

### How to troubleshoot SSH

- **Windows**: Only Pageant is supported. Download from [PuTTY's site](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).
- **Misconfiguration**: Double-check your remote URL format and SSH settings.
- **SSH config files**: GitKraken Desktop does **not** support `.ssh/config` aliases. Load your key directly or use your OS’s agent.

***

## How to forget all credentials

Reset stored usernames and passwords from <kbd><strong>Preferences > General</strong></kbd>:

<figure>
<img src="/wp-content/uploads/forget-all-2025@2x.png" alt="Forget All Credentials UI" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Reset saved credentials</figcaption>
</figure>

***

## How proxy configuration works

GitKraken Desktop supports proxies for Windows, macOS, and Linux.

### How proxy prompts work on Windows

Your system will prompt for proxy credentials when needed.

### How proxy prompts work on macOS and Linux

GitKraken Desktop prompts for credentials directly.

On Linux, run with this flag if needed:

    --proxy-server=10.200.0.1:8080

***

## How to format Google Cloud Source Repositories SSH URLs

Due to formatting, you may need to adjust SSH URLs:

Original:

    ssh://example@gitkraken.com@source.developers.google.com:2021/p/test-project-12345/r/Test-Repo-1

Fixed:

    ssh://example%40gitkraken.com@source.developers.google.com:2021/p/test-project-12345/r/Test-Repo-1
