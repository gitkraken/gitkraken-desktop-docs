---
title: Sign Commits with GPG or SSH in GitKraken Desktop
description: Learn how to verify your commits using GPG or SSH keys in GitKraken Desktop. Includes setup, configuration, and troubleshooting for Git commit signing.
product: GitKraken Desktop
feature: Commit Signing
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [commit-signing, gpg, ssh, verification, security]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-git-workflows-and-extensions"
    nav_label: "Commit Signing"
    nav_order: 30
    nav_parent: "desktop-git-workflows-and-extensions"
    page_type: "content"
    card_icon: "certificate"
    card_color: "amber"
    card_description: "Sign commits and tags with GPG or SSH keys"
---

<kbd>Last updated: November 2026</kbd>

***

Use this page to sign Git commits and tags in GitKraken Desktop with either GPG or SSH keys so hosting providers can verify your identity.

## Requirements and limits

- Scope: Commit and tag signing with GPG or SSH keys
- GPG requirement: Install GPG before configuring signing in GitKraken Desktop
- Restart requirement: Close and reopen GitKraken Desktop after installing GPG
- SSH signing setup: Requires a `.pub` signing key, and an `allowed_signers` file to verify SSH signatures
- Host verification note: GitHub and GitLab support SSH-signed commit verification; Bitbucket does not
- Verification behavior: Signed commits show a badge in the Commit Panel with signature details on hover

***

## Quick Start


**To sign commits with GPG:**
1. Install GPG for your operating system (Gpg4win on Windows, `brew install gpg` on macOS, or your Linux package manager).
2. Close and reopen GitKraken Desktop.
3. Go to <kbd>Preferences > Commit Signing</kbd>.
4. Select a **Signing Key** from the dropdown, or click **Generate new GPG Key**.
5. Set the **GPG Program** path if it is not auto-detected.
6. Enable **Sign Commits by Default** and/or **Sign Tags by Default**.
7. Click **Copy GPG Public Key** in <kbd>Preferences > Commit Signing</kbd> and upload the key to your hosting service (GitHub, GitLab, or Bitbucket).

**To sign commits with SSH:**
1. Generate an SSH key.
2. Go to <kbd>Preferences > Commit Signing</kbd>, set the **GPG Format** to **SSH**, and select your `.pub` key file.
3. Create an `allowed_signers` file and select it in **Allowed Signers File**.
4. Enable **Sign Commits by Default**.

Signed commits display a badge next to the SHA in the Commit Panel. Hover over it to view signature details.

## What commit signing is

Git lets you commit with any name and email address. To prove that a commit is yours, you can sign commits and annotated tags with a GPG or SSH key pair.

When you sign a commit, anyone with your public key can verify that you created it. If you upload your public key to a hosting service such as GitHub, the service shows your signed commits as verified.

---

## How to sign commits with GPG

To sign with GPG, install GPG, set up a key in GitKraken Desktop, and upload the public key to your hosting service.

### GPG requirements

Before signing commits, install and configure GPG.

> **Note:** Close GitKraken Desktop before installing GPG.

- **Windows:** Use [Gpg4win](https://gpg4win.org/download.html) and follow the installer.
- **Mac:** Use [Homebrew](https://brew.sh/):
  ```bash
  brew install gpg
  ```
- **Linux:** Use your package manager:
  - Debian/Ubuntu: `apt install gnupg`
  - Fedora: `dnf install gnupg2`
  - CentOS/RHEL: `yum install gnupg2`

Other downloads are at [gnupg.org](https://www.gnupg.org/download/index.html).

To check that GPG is installed, run:
```bash
gpg --version
```

<figure>
  <img src="/wp-content/uploads/gpg-version-2025@2x.png" class="help-center-img img-bordered" alt="GPG version output">
  <figcaption style="text-align: center; color: #888">GPG version output.</figcaption>
</figure>

> **Note:** If <code>gpg</code> is not an alias for <code>gpg2</code>, run the commands with <code>gpg2</code> instead.

### How to generate a GPG key in GitKraken Desktop

After you install GPG:

1. Go to <kbd>Preferences > Commit Signing</kbd>.
2. Click **Generate new GPG Key**.
3. (Optional) Enter a passphrase before generating.

<figure>
  <img src="/wp-content/uploads/generate-new-gpg-key-2025@2x.png" class="help-center-img img-bordered" alt="Generate new GPG key in Preferences">
  <figcaption style="text-align: center; color: #888">Generate new GPG key in Preferences.</figcaption>
</figure>

> **Note:** Make sure GPG is configured in GitKraken Desktop. See <a href="#how-to-configure-gpg-in-gitkraken-desktop">How to configure GPG in GitKraken Desktop</a>.

### How to configure GPG in GitKraken Desktop

1. Go to <kbd>Preferences > Commit Signing</kbd>.
2. Select a **Signing Key** from the dropdown list. If the list is empty:
   - Set the **GPG Program** path.
   - Restart GitKraken Desktop after installing GPG.
3. If GitKraken Desktop does not detect the **GPG Program** location, enter it or click <kbd>Browse</kbd>. To find the path, run:
   ```bash
   which gpg # macOS/Linux
   where gpg # Windows
   ```
   <figure>
     <img src="/wp-content/uploads/gpg-browse-button.png" class="help-center-img img-bordered" alt="Browse to GPG executable">
     <figcaption style="text-align: center; color: #888">Browse to GPG executable.</figcaption>
   </figure>
4. Enable **Sign Commits by Default** and/or **Sign Tags by Default** as needed.

### How to verify signed commits

Signed commits show a badge next to the SHA in the Commit Panel.

<figure>
  <img src="/wp-content/uploads/gpg-icon-2025@2x.png" class="help-center-img img-bordered" alt="Signed commit badge">
  <figcaption style="text-align: center; color: #888">Signed commit badge.</figcaption>
</figure>

Hover over the badge to see the signature details:

<figure>
  <img src="/wp-content/uploads/gpg-sig-details-2025@2x.png" class="help-center-img img-bordered" alt="GPG signature details tooltip">
  <figcaption style="text-align: center; color: #888">GPG signature details tooltip.</figcaption>
</figure>

**Common GPG signature codes:**

- `GOODSIG`: Valid signature.
- `EXPSIG`: Signature is expired.
- `EXPKEYSIG`: Signed with expired key.
- `REVKEYSIG`: Signed with revoked key.
- `BADSIG`: Signature not verified.
- `ERRSIG`: Unable to check signature (missing key or unsupported algorithm).

### How to upload a GPG key to your hosting service

To have your hosting service show signed commits as verified:

1. In GitKraken Desktop, go to <kbd>Preferences > Commit Signing</kbd> and click **Copy GPG Public Key**.
2. Add the key to your hosting service:
   - [GitHub GPG setup](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-gpg-key-to-your-github-account)
   - [GitLab GPG setup](https://docs.gitlab.com/ee/user/project/repository/signed_commits/gpg.html#add-a-gpg-key-to-your-account)
   - [Bitbucket GPG setup](https://support.atlassian.com/bitbucket-cloud/docs/use-gpg-keys-to-sign-commits/#Add-a-GPG-key)

### How to edit a GPG key

To add an email address to a key or renew it, use the GPG command line:

1. List your keys:
   ```bash
   gpg --list-secret-keys --keyid-format LONG
   ```
   <figure>
     <img src="/wp-content/uploads/list-secret-keys@2x.png" class="help-center-img img-bordered" alt="List GPG secret keys">
     <figcaption style="text-align: center; color: #888">List GPG secret keys.</figcaption>
   </figure>
2. Open the key for editing:
   ```bash
   gpg --edit-key YOUR_KEY_ID
   ```
3. Run the commands you need:
   - `adduid`: Add an email address
   - `deluid`: Remove an email address
   - `trust`: Update the trust level
   - `expire`: Change the expiration date
   - `save`: Save and exit

For every option, see [GNU's full GPG key guide](https://www.gnupg.org/gph/en/manual/r899.html).

After editing, upload the key to your hosting service again. See <a href="#how-to-upload-a-gpg-key-to-your-hosting-service">How to upload a GPG key to your hosting service</a>.

### How to delete a GPG key

To delete a key, run this command followed by your key ID or name:
```bash
gpg --delete-secret-keys
```

<figure>
  <img src="/wp-content/uploads/delete-key.png" class="help-center-img img-bordered" alt="Delete GPG key confirmation">
  <figcaption style="text-align: center; color: #888">Delete GPG key confirmation.</figcaption>
</figure>
<figure>
  <img src="/wp-content/uploads/delete-key-for-sure.png" class="help-center-img img-bordered" alt="Final delete confirmation">
  <figcaption style="text-align: center; color: #888">Final delete confirmation.</figcaption>
</figure>

---

## How to sign commits with SSH

GitKraken Desktop signs with SSH through the Git selected in <kbd>Preferences > General > Git Executable</kbd>. If that Git's OpenSSH version is too old to sign commits, the **Git Executable** setting shows a warning with the detected version.

### SSH signing requirements

- **macOS/Linux:** Git and OpenSSH are usually preinstalled.
  ```bash
  git -v
  ssh -V
  ```
- **Windows:** Install [Git Bash](https://git-scm.com/).

### How to enable SSH signing

1. **Create SSH key:**
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```
   <figure>
     <img src="/wp-content/uploads/gkc-ssh-keygen@2x.png" class="help-center-img img-bordered" alt="Generating SSH key">
     <figcaption style="text-align: center; color: #888">Generating SSH key.</figcaption>
   </figure>

2. **Set GPG Format to SSH:**
   <kbd>Preferences > Commit Signing > GPG Format</kbd> → select <kbd>SSH</kbd>.

3. **Select signing key:**
   In <kbd>Signing Key</kbd>, browse to the `.pub` key.

4. **Create allowed_signers file:**
   ```bash
   touch ~/.ssh/allowed_signers
   echo "$(git config --get user.email) namespaces=\"git\" $(cat ~/.ssh/YOUR_KEY.pub)" >> ~/.ssh/allowed_signers
   ```
   In <kbd>Preferences > Commit Signing</kbd>, select this file in **Allowed Signers File**.

5. **Enable signing by default:**
   <kbd>Preferences > Commit Signing</kbd> → enable **Sign Commits by Default** and/or **Sign Tags by Default**.

6. **Add SSH Key to Host:**
   - [GitHub SSH setup](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
   - [GitLab SSH setup](https://docs.gitlab.com/ee/user/project/repository/signed_commits/gpg.html#add-a-gpg-key-to-your-account)
   - ⚠️ Bitbucket does **not** support SSH-signed commit verification.
