---
title: Authentication with Other Git Hosts in GitKraken Desktop
description: Learn how to authenticate with TFS, AWS CodeCommit, Google Cloud Source Repositories, and custom Git hosts using HTTPS or SSH in GitKraken Desktop.
taxonomy:
  category: gitkraken-desktop
---

<kbd>Last updated: June 2025</kbd>

GitKraken Desktop supports authentication with most repository hosting services (e.g., TFS, AWS CodeCommit, [Google Cloud Source Repositories](/integrations/authentication/#google-cloud-source-repositories), and custom services) over HTTPS or SSH.

<figure>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/OA9o09Bq5M8?ecver=1" frameborder="0" allowfullscreen title="Authentication Overview Video"></iframe>
</div>
</figure>

***

## HTTPS Authentication

This is the default and most common method for interacting with remotes. It requires your Git username and password.

### How to clone with HTTPS

1. Copy the HTTPS URL from your hosting service, which typically looks like:

    ```
    https://example.com/username/myrepository.git
    ```

2. In GitKraken Desktop, go to <kbd><strong>File > Clone Repo</strong></kbd>.

<figure>
<img src='/wp-content/uploads/clone-repository-menu-2025.png' srcset='/wp-content/uploads/clone-repository-menu-2025@2x.png 2x' alt="GitKraken Clone Repo Menu" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Cloning a repository using HTTPS</figcaption>
</figure>

3. Paste the URL, click <button class='button button--success button--ui button--nolink'>Clone the repo</button>, and open it in GitKraken.

The remote tracking at `origin` is automatically set using this HTTPS format.

***

## SSH Authentication

<figure>
<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/z7jVOenqFYk?ecver=1" frameborder="0" allowfullscreen title="SSH Authentication Video"></iframe>
</div>
</figure>

Before cloning via SSH, you must first set up your SSH keys in GitKraken Desktop.

### Set up SSH keys

1. Navigate to <kbd><strong>Preferences > SSH</strong></kbd>.

<figure>
<img src="/wp-content/uploads/ssh-preferences-2025.png" srcset="/wp-content/uploads/ssh-preferences-2025@2x.png" alt="SSH Preferences Menu" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">SSH preferences in GitKraken Desktop</figcaption>
</figure>

2. You can browse to select an existing SSH key pair or generate a new one (recommended).
3. Copy the public key to your remote hosting service.

### Clone over SSH

1. Copy the SSH URL from your hosting service.
2. In GitKraken Desktop, go to <em class='context-menu'>File <i class="fa fa-caret-right"></i> Clone</em>.

<figure>
<img src='/wp-content/uploads/ssh-clone-2025.png' srcset='/wp-content/uploads/ssh-clone-2025@2x.png 2x' alt="Clone over SSH UI" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
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

### Custom SSH ports

Use this format:

    ssh://{user}@{host}:{port}/{repo}

### Use a Local SSH Agent

Using a local agent can simplify SSH management, especially across multiple profiles. From <kbd><strong>Preferences > SSH</strong></kbd>, check _Use local SSH agent_.

> Tip: This allows automatic key usage if already loaded in your system's agent.

### Troubleshooting SSH

- **Windows**: Only Pageant is supported. Download from [PuTTY's site](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).
- **Misconfiguration**: Double-check your remote URL format and SSH settings.
- **SSH config files**: GitKraken Desktop does **not** support `.ssh/config` aliases. Load your key directly or use your OS’s agent.

***

## Forget All Credentials

Reset stored usernames and passwords from <kbd><strong>Preferences > General</strong></kbd>:

<figure>
<img src="/wp-content/uploads/forget-all-2025.png" srcset="/wp-content/uploads/forget-all-2025@2x.png" alt="Forget All Credentials UI" style="max-width: 75%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Reset saved credentials</figcaption>
</figure>

***

## Proxy Configuration

GitKraken Desktop supports proxies for Windows, macOS, and Linux.

### Windows

Your system will prompt for proxy credentials when needed.

### macOS & Linux

GitKraken Desktop prompts for credentials directly.

On Linux, run with this flag if needed:

    --proxy-server=10.200.0.1:8080

***

## Google Cloud Source Repositories

Due to formatting, you may need to adjust SSH URLs:

Original:

    ssh://example@gitkraken.com@source.developers.google.com:2021/p/test-project-12345/r/Test-Repo-1

Fixed:

    ssh://example%40gitkraken.com@source.developers.google.com:2021/p/test-project-12345/r/Test-Repo-1
