---
title: Sign Commits with GPG or SSH in GitKraken Desktop
description: Learn how to verify your commits using GPG or SSH keys in GitKraken Desktop. Includes setup, configuration, and troubleshooting for Git commit signing.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

***

Use this page to sign Git commits and tags in GitKraken Desktop with either GPG or SSH keys so hosting providers can verify your identity. It covers setup requirements, key generation, GitKraken configuration, verification behavior, and the extra Git Executable requirement for SSH-based signing.

**Requirements and limits**
- Scope: Commit and tag signing with GPG or SSH keys
- GPG requirement: Install GPG before configuring signing in GitKraken Desktop
- Restart requirement: Close and reopen GitKraken Desktop after installing GPG
- SSH signing requirement: Git Executable must be enabled
- SSH signing setup: Requires a `.pub` signing key and an `allowed_signers` file
- Host verification note: GitHub and GitLab support SSH-signed commit verification; Bitbucket does not
- Verification behavior: Signed commits show a badge in the Commit Panel with signature details on hover

***

## Quick Start

Sign Git commits in GitKraken Desktop using a GPG or SSH key to verify your identity when pushing to services like GitHub or GitLab.

**To sign commits with GPG:**
1. Install GPG for your operating system (Gpg4win on Windows, `brew install gpg` on macOS, or your Linux package manager).
2. Close and reopen GitKraken Desktop.
3. Go to <kbd>Preferences > Commit Signing</kbd>.
4. Select a **Signing Key** from the dropdown, or click **Generate new GPG Key**.
5. Set the **GPG Program** path if it is not auto-detected.
6. Enable **Sign Commits by Default** and/or **Sign Tags by Default**.
7. Copy your public key from <kbd>Preferences > GPG</kbd> and upload it to your hosting service (GitHub, GitLab, or Bitbucket).

**To sign commits with SSH:**
1. Generate an SSH key and enable the **Git Executable** under <kbd>Preferences > Experimental</kbd>.
2. Go to <kbd>Preferences > Commit Signing</kbd>, set the **GPG Format** to **SSH**, and select your `.pub` key file.
3. Create an `allowed_signers` file and select it in GitKraken Desktop.
4. Enable **Sign Commits by Default**.

Signed commits display a badge next to the SHA in the Commit Panel. Hover over it to view signature details.

## What commit signing is

In Git, you may commit using any name and email address. However, Git supports signing commits and annotated tags using a GPG or SSH key pair.

By signing a commit, others with your public key can verify that the commit was created by you. Public keys can also be uploaded to remote hosting services like GitHub so commits appear as verified.

---

## How to sign commits with GPG

### GPG requirements

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

<img src="/wp-content/uploads/gpg-version-2025@2x.png" class="help-center-img img-bordered" alt="GPG version output">

<div class='callout callout--success'>
    <p><strong>Note:</strong> Use <code>gpg2</code> if <code>gpg</code> isn’t aliased. Prefix commands accordingly.</p>
</div>

### How to generate a GPG key in GitKraken Desktop

Once GPG is installed:

1. Go to <kbd>Preferences > Commit Signing</kbd>.
2. Click **Generate new GPG Key**.
3. (Optional) Enter a passphrase before generating.

<img src="/wp-content/uploads/generate-new-gpg-key-2025@2x.png" class="help-center-img img-bordered" alt="Generate new GPG key in Preferences">

<div class='callout callout--success'>
    <p><strong>Note:</strong> Ensure GPG is configured in GitKraken. See <a href="#configure-gpg-in-gitkraken">Configure GPG in GitKraken</a>.</p>
</div>

### How to configure GPG in GitKraken Desktop

1. Navigate to <kbd>Preferences > Commit Signing</kbd>.
2. Set the **Signing Key** from the dropdown list. If it’s empty:
   - Configure the GPG Program path.
   - Restart GitKraken after installing GPG.
3. Specify the **GPG Program** location or use the <kbd>Browse</kbd> button if not auto-detected.
   ```bash
   which gpg # macOS/Linux
   where gpg # Windows
   ```
   <img src="/wp-content/uploads/gpg-browse-button.png" class="help-center-img img-bordered" alt="Browse to GPG executable">
4. Enable **Sign Commits by Default** and/or **Sign Tags by Default** as needed.

### How to verify signed commits

Signed commits show an icon next to the SHA in the Commit Panel.

<img src="/wp-content/uploads/gpg-icon-2025@2x.png" class="help-center-img img-bordered" alt="Signed commit badge">

Hover to view signature details:

<img src="/wp-content/uploads/gpg-sig-details-2025@2x.png" class="help-center-img img-bordered" alt="GPG signature details tooltip">

**Common GPG signature codes:**

- `GOODSIG`: Valid signature.
- `EXPSIG`: Signature is expired.
- `EXPKEYSIG`: Signed with expired key.
- `REVKEYSIG`: Signed with revoked key.
- `BADSIG`: Signature not verified.
- `ERRSIG`: Unable to check signature (missing key or unsupported algorithm).

### How to upload a GPG key to your hosting service

To display signed commits as verified:

- [GitHub GPG setup](https://docs.github.com/en/authentication/managing-commit-signature-verification/adding-a-gpg-key-to-your-github-account)
- [GitLab GPG setup](https://docs.gitlab.com/ee/user/project/repository/signed_commits/gpg.html#add-a-gpg-key-to-your-account)
- [Bitbucket GPG setup](https://support.atlassian.com/bitbucket-cloud/docs/use-gpg-keys-to-sign-commits/#Add-a-GPG-key)

In GitKraken: <kbd>Preferences > GPG</kbd> → Copy GPG Public Key.

### How to edit a GPG key

To add emails or renew a key:

1. List keys:
   ```bash
   gpg --list-secret-keys --keyid-format LONG
   ```
   <img src="/wp-content/uploads/list-secret-keys@2x.png" class="help-center-img img-bordered" alt="List GPG secret keys">
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

### How to delete a GPG key

To delete:
```bash
gpg --delete-secret-keys
```
Append your key ID or name.

<img src="/wp-content/uploads/delete-key.png" class="help-center-img img-bordered" alt="Delete GPG key confirmation">
<img src="/wp-content/uploads/delete-key-for-sure.png" class="help-center-img img-bordered" alt="Final delete confirmation">

---

## How to sign commits with SSH

SSH signing is available through Git Executable.

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
   <img src="/wp-content/uploads/gkc-ssh-keygen@2x.png" class="help-center-img img-bordered" alt="Generating SSH key">

2. **Enable Git Executable:**
   Go to <kbd>Preferences > Experimental > Git Executable</kbd>.
   <img src="/wp-content/uploads/gkc-git-executable@2x.png" class="help-center-img img-bordered" alt="Enable Git Executable">

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

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
