---
title: Sign Commits with GPG or SSH in GitKraken Desktop
description: Learn how to verify your commits using GPG or SSH keys in GitKraken Desktop. Includes setup, configuration, and troubleshooting for Git commit signing.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: June 2025</kbd>

## What is Commit Signing?

In Git, you may commit using any name and email address. However, Git supports signing commits and annotated tags using a GPG or SSH key pair.

By signing a commit, others with your public key can verify that the commit was created by you. Public keys can also be uploaded to remote hosting services like GitHub so commits appear as verified.

---

## Commit Signing with GPG

### Requirements

Before signing commits, install and configure GPG.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Close GitKraken Desktop before installing GPG.</p>
</div>

- **Windows:** Use [Gpg4win](https://gpg4win.org/download.html) and follow the installer.
- **Mac:** Use [Homebrew](https://brew.sh/):
  ```bash
  brew install gpg
  ```
- **Linux:** Use your package manager:
  - Debian/Ubuntu: `apt install gnupg`
  - Fedora: `dnf install gnupg2`
  - CentOS/RHEL: `yum install gnupg2`

More downloads at [gnupg.org](https://www.gnupg.org/download/index.html).

To verify installation:
```bash
gpg --version
```

<img src="/wp-content/uploads/gpg-version-2025.png" srcset="/wp-content/uploads/gpg-version-2025@2x.png 2x" class="help-center-img img-bordered" alt="GPG version output">

<div class='callout callout--success'>
    <p><strong>Note:</strong> Use <code>gpg2</code> if <code>gpg</code> isn’t aliased. Prefix commands accordingly.</p>
</div>

### Generate a GPG Key in GitKraken

Once GPG is installed:

1. Go to <kbd>Preferences > Commit Signing</kbd>.
2. Click **Generate new GPG Key**.
3. (Optional) Enter a passphrase before generating.

<img src="/wp-content/uploads/generate-new-gpg-key-2025.png" srcset="/wp-content/uploads/generate-new-gpg-key-2025@2x.png 2x" class="help-center-img img-bordered" alt="Generate new GPG key in Preferences">

<div class='callout callout--success'>
    <p><strong>Note:</strong> Ensure GPG is configured in GitKraken. See <a href="#configure-gpg-in-gitkraken">Configure GPG in GitKraken</a>.</p>
</div>

### Configure GPG in GitKraken

1. Navigate to <kbd>Preferences > Commit Signing</kbd>.
2. Set the **Signing Key** from the dropdown list. If it’s empty:
   - Configure the GPG Program path.
   - Restart GitKraken after installing GPG.
3. Specify the **GPG Program** location or use the <kbd>Browse</kbd> button if not auto-detected.
   ```bash
   which gpg # macOS/Linux
   where gpg # Windows
   ```
   <img src="/wp-content/uploads/gpg-browse-button.png" srcset="/wp-content/uploads/gpg-browse-button.png 2x" class="help-center-img img-bordered" alt="Browse to GPG executable">
4. Enable **Sign Commits by Default** and/or **Sign Tags by Default** as needed.

### Verifying Signed Commits

Signed commits show an icon next to the SHA in the Commit Panel.

<img src="/wp-content/uploads/gpg-icon-2025.png" srcset="/wp-content/uploads/gpg-icon-2025@2x.png 2x" class="help-center-img img-bordered" alt="Signed commit badge">

Hover to view signature details:

<img src="/wp-content/uploads/gpg-sig-details-2025.png" srcset="/wp-content/uploads/gpg-sig-details-2025@2x.png 2x" class="help-center-img img-bordered" alt="GPG signature details tooltip">

**Common GPG signature codes:**

- `GOODSIG`: Valid signature.
- `EXPSIG`: Signature is expired.
- `EXPKEYSIG`: Signed with expired key.
- `REVKEYSIG`: Signed with revoked key.
- `BADSIG`: Signature not verified.
- `ERRSIG`: Unable to check signature (missing key or unsupported algorithm).

### Uploading GPG Key to Hosting Service

To display signed commits as verified:

- [GitHub GPG setup](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-gpg-key-to-your-github-account)
- [GitLab GPG setup](https://docs.gitlab.com/ee/user/project/repository/signed_commits/gpg.html#add-a-gpg-key-to-your-account)
- [Bitbucket GPG setup](https://support.atlassian.com/bitbucket-cloud/docs/use-gpg-keys-to-sign-commits/#Add-a-GPG-key)

In GitKraken: <kbd>Preferences > GPG</kbd> → Copy GPG Public Key.

### Editing a GPG Key

To add emails or renew a key:

1. List keys:
   ```bash
   gpg --list-secret-keys --keyid-format LONG
   ```
   <img src="/wp-content/uploads/list-secret-keys.png" class="help-center-img img-bordered" alt="List GPG secret keys">
2. Edit:
   ```bash
   gpg --edit-key YOUR_KEY_ID
   ```
3. Use commands:
   - `adduid`: Add email
   - `deluid`: Remove email
   - `trust`: Update trust level
   - `expire`: Change expiration
   - `save`: Save and exit

[GNU’s full GPG key guide](https://www.gnupg.org/gph/en/manual/r899.html)

After editing, re-upload the key to your host. See <a href="#uploading-gpg-key-to-hosting-service">Uploading Your GPG Key to a Remote Hosting Service</a>.

### Deleting a GPG Key

To delete:
```bash
gpg --delete-secret-keys
```
Append your key ID or name.

<img src="/wp-content/uploads/delete-key.png" class="help-center-img img-bordered" alt="Delete GPG key confirmation">
<img src="/wp-content/uploads/delete-key-for-sure.png" class="help-center-img img-bordered" alt="Final delete confirmation">

---

## Commit Signing with SSH

SSH signing is available through Git Executable.

### Requirements

- **macOS/Linux:** Git and OpenSSH are usually preinstalled.
  ```bash
  git -v
  ssh -V
  ```
- **Windows:** Install [Git Bash](https://git-scm.com/).

### Steps to Enable SSH Signing

1. **Create SSH key:**
   ```bash
   ssh-keygen -t ed25519 -C "your_email@example.com"
   ```
   <img src="/wp-content/uploads/gkc-ssh-keygen.png" srcset="/wp-content/uploads/gkc-ssh-keygen@2x.png 2x" class="help-center-img img-bordered" alt="Generating SSH key">

2. **Enable Git Executable:**
   Go to <kbd>Preferences > Experimental > Git Executable</kbd>.
   <img src="/wp-content/uploads/gkc-git-executable.png" srcset="/wp-content/uploads/gkc-git-executable@2x.png 2x" class="help-center-img img-bordered" alt="Enable Git Executable">

3. **Set GPG Format to SSH:**
   <kbd>Preferences > Commit Signing > GPG Format</kbd> → select <kbd>SSH</kbd>.

4. **Select signing key:**
   On <kbd>Signing Key</kbd>, browse to the `.pub` key.

5. **Create allowed_signers file:**
   ```bash
   touch ~/.ssh/allowed_signers
   echo "$(git config --get user.email) namespaces=\"git\" $(cat ~/.ssh/YOUR_KEY.pub)" >> ~/.ssh/allowed_signers
   ```
   Select this file in GitKraken.

6. **Enable Signing by Default:**
   <kbd>Preferences > Commit Signing</kbd> → enable **Sign Commits** and/or **Sign Tags**.

7. **Add SSH Key to Host:**
   - [GitHub SSH setup](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account)
   - [GitLab SSH setup](https://docs.gitlab.com/ee/user/project/repository/signed_commits/gpg.html#add-a-gpg-key-to-your-account)
   - ⚠️ Bitbucket does **not** support SSH-signed commit verification.
