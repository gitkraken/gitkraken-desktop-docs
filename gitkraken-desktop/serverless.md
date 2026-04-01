---
title: GitKraken On-Premise Serverless (Stand-Alone) Setup
description: Learn how to install, license, and run GitKraken On-Premise Serverless on Windows, macOS, and Linux in offline or secure environments.
product: GitKraken Serverless
feature: Serverless Setup
content_type: overview
audience: enterprise-admin
plan_required: Enterprise
os_support: [Windows, macOS, Linux]
git_hosts: [n/a]
integrations: []
hosted_variant: self-hosted
status: GA
last_verified: 2026-03
llms_include: true
tags: [serverless, on-premise, offline, setup, enterprise]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: April 2026</kbd>

Use this page to install and license GitKraken On-Premise Serverless, also called GitKraken Stand-Alone, when your team works in offline or tightly controlled environments. It covers platform-specific installation steps, supported license file locations, and the manual license update flow required after expiration or renewal.

**Requirements and limits**
- Product scope: GitKraken On-Premise Serverless / Stand-Alone
- Environment fit: Offline, disconnected, or tightly controlled environments
- Account model: No internet account creation required
- Activation requirement: A `.dat` license file must be loaded at first launch
- License maintenance: Expired or renewed licenses must be updated manually by replacing the `.dat` file or using **Update License**
- Commercial note: Serverless is sold separately from standard subscriptions and separately from Self-Hosted on-premise offerings

**GitKraken On-Premise Serverless** (also known as *GitKraken Stand-Alone*) is designed for teams operating in disconnected or secure environments. It includes most core <a href="https://www.gitkraken.com/git-client" target=_blank>GitKraken features</a>, with additional advantages:

- Works without internet access
- Requires no account creation
- Requires no server installation

***

## Quick Start


1. Download the GitKraken Serverless installer for your operating system from the [downloads page](https://www.gitkraken.com/download-on-premise-serverless).
2. Install the application:
   - **Windows**: Double-click the `.exe` file and follow the setup prompts.
   - **macOS**: Open the DMG and drag the GitKraken icon to your Applications folder.
   - **Linux (.deb)**: Run `wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.deb && dpkg -i gitkraken-amd64.deb`.
3. At first launch, load your `.dat` license file when prompted. If you do not have the file, contact your GitKraken administrator.

If your license expires, replace the `.dat` file in one of the supported directories or click the license text in the bottom-left corner of the app and select **Update License**. GitKraken Serverless is sold separately from standard subscriptions.

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-example-2025@2x.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Example view of GitKraken Serverless in use.</figcaption>
</figure>

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately. Visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing'>On-Premise Pricing</a> page to purchase.</p>
</div>

<div class='callout callout--basic'>
    <p>To request a trial key, email <a href="mailto:sales@gitkraken.com">sales@gitkraken.com</a>.</p>
</div>

***

## Feature support

GitKraken On-Premise Serverless supports most GitKraken Desktop features, including the major upgrades introduced in versions 10 and 11. Features that require connectivity to GitKraken cloud services or to external cloud hosting providers are not available.

### What is included

The following feature categories are fully supported in Serverless:

**Core Git client**: All standard Git operations, including commits, branches, merges, rebases, diffs, stashing, tagging, interactive rebase, cherry pick (including multi-commit interactive cherry pick), worktrees, shallow clone, and undo or redo of rebase and cherry pick operations.

**Launchpad**: Track pull requests and issues in a single view and filter by repository, branch, milestone, or sprint. Launchpad works with the following on-premises integrations: GitHub Enterprise Server, GitLab Self-Managed, Bitbucket Server and Data Center, Azure DevOps Server, and Jira Data Center. For a description of the differences between cloud and on-premises Launchpad, see [How On-Premise Launchpad differs from Cloud Launchpad](/gitkraken-desktop/gitkraken-launchpad/#how-on-premise-launchpad-differs-from-cloud-launchpad).

**Local Workspaces**: Organize multiple local Git repositories in one view. You can see the branch status of each repository and run multi-repository actions, such as fetch and pull, from a single place. Cloud Workspaces are not available in Serverless.

**Conflict detection**: GitKraken detects potential conflicts with your target branch before you reach the merge step and alerts you when your checked-out branch has diverged from its pull request target.

**GitKraken AI (bring your own key)**: All GitKraken AI features are available when you configure a Custom URL that points to a private or internal AI endpoint. For setup instructions, see [GitKraken AI in Serverless](#gitkraken-ai-in-serverless).

**ARM builds**: A native ARM installer is available for machines with ARM architecture.

**On-premises integrations**: GitKraken Serverless supports integrations with self-hosted Git hosting services and issue trackers. For the full list, see [Supported on-premises integrations](#supported-on-premises-integrations).

### What is not available

The following features require connectivity to GitKraken cloud services (`gitkraken.dev`) or to external cloud hosting providers and are not available in Serverless:

- Cloud Workspaces and features that depend on them, including Team Launchpad, Launchpad Saved Views, and Launchpad snooze and pin
- GitKraken Insights
- GitKraken AI using the default GitKraken-hosted provider
- Cloud Patch sharing
- Org Member conflict detection
- Integrations with cloud-hosted services: GitHub.com, GitLab.com, Bitbucket.org, Azure DevOps cloud, Jira Cloud, and Trello

### Feature support table

| Feature | Supported | Notes |
|---|---|---|
| Core Git client (commits, branches, merges, rebase, diff, stash) | Yes | |
| Interactive Rebase | Yes | |
| Multi-commit Cherry Pick | Yes | |
| Worktrees | Yes | Requires version 10.5.0 or later |
| Shallow Clone | Yes | |
| Undo rebases, cherry picks, and AI Commit Compose | Yes | |
| Local Workspaces | Yes | Stored on-device only; not shareable across machines |
| Cloud Workspaces | No | Requires gitkraken.dev |
| Launchpad with on-premises integrations | Yes | See supported integrations list |
| Launchpad Cloud Workspace filtering | No | |
| Launchpad Team View | No | |
| Launchpad Saved Views | No | |
| Launchpad snooze and pin | No | |
| Conflict detection (target branch) | Yes | |
| Conflict detection (Org Member awareness) | No | Requires cloud GitKraken Org |
| Cloud Patch sharing | No | |
| GitKraken AI (default hosted provider, no key required) | No | Calls GitKraken cloud endpoint |
| GitKraken AI (Custom URL or bring your own key) | Yes | Per-user opt-in; you provide the AI infrastructure |
| ARM builds | Yes | Separate ARM installer available |
| GitHub Enterprise Server integration | Yes | |
| GitLab Self-Managed integration | Yes | |
| Bitbucket Server and Data Center integration | Yes | |
| Azure DevOps Server integration | Yes | |
| Jira Data Center integration | Yes | |
| GitHub.com, GitLab.com, Bitbucket.org, Azure DevOps cloud, Jira Cloud | No | Require outbound internet access |
| GitKraken Insights | No | Requires gitkraken.dev |

### GitKraken AI in Serverless

GitKraken AI is available in GitKraken Serverless when you configure a Custom URL that directs AI requests to a private or internal service. The default GitKraken-hosted AI provider is not accessible in offline or air-gapped environments.

**To enable GitKraken AI in Serverless:**

1. Go to <kbd>Preferences > GitKraken AI</kbd>.
2. Select **Custom URL** as the provider.
3. Enter the endpoint URL for your internal AI service.
4. If your endpoint requires authentication, enter an API key.

This is an opt-in, per-user setting. GitKraken does not validate or support the configuration of third-party or self-hosted AI endpoints.

When you configure a Custom URL, the following AI features are available:

- Commit message generation
- Commit Composer (Preview)
- Explain commits
- Explain branch changes
- Pull request title and description generation (requires a configured on-premises integration)
- Auto-resolve merge conflicts (Preview)
- Stash message generation

To configure organization-wide AI controls, see [GitKraken Dev Security Controls](https://help.gitkraken.com/gk-dev/gk-dev-security-controls/).

### Supported on-premises integrations

GitKraken Serverless supports the following self-hosted integrations. These integrations communicate only within your network and do not require outbound internet access:

- GitHub Enterprise Server
- GitLab Self-Managed
- Bitbucket Server and Data Center
- Azure DevOps Server
- Jira Data Center

The cloud-hosted counterparts of these services (GitHub.com, GitLab.com, Bitbucket.org, Azure DevOps cloud, and Jira Cloud) are not supported in Serverless because they require outbound internet connectivity.

***

## How to install GitKraken Serverless

Follow these steps to get started:

<ol>
<li><a href="https://www.gitkraken.com/download-on-premise-serverless" target=_blank>Download GitKraken Serverless</a></li>
<li>Install GitKraken Serverless</li>
<li>Load your <code>.dat</code> license file</li>
</ol>

---

### How to download GitKraken Serverless

Download the appropriate client for your operating system from our <a href="https://www.gitkraken.com/download-on-premise-serverless" target=_blank>downloads page</a>.

If the page is inaccessible, contact your GitKraken administrator for internal distribution options.

---

### How to install GitKraken Serverless on each platform

#### Windows (.exe)

**System Requirements:** Windows 10+

**Install:** Double-click the downloaded `.exe` file and follow the setup instructions.

**Data Location:**
- `C:\Users\{user}\AppData\Roaming`
- `%APPDATA%\.gitkraken` (for older versions)

<figure class='figure center'>
  <img src="/wp-content/uploads/license.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Prompt to load license file after install.</figcaption>
</figure>

---

#### macOS (.dmg)

**System Requirements:**
- Intel: macOS 10.15+
- Apple Silicon: macOS 11+

**Install:** Open the DMG file and drag the GitKraken icon into your Applications folder.

**Data Location:** `/Users/{user}/.gitkraken` (or `~/.gitkraken`)

---

#### Linux (.deb, .rpm, .tar.gz)

**System Requirements:**
- `.deb`: Ubuntu 18.04+ LTS, Debian 10+
- `.rpm`: RHEL 8+, Fedora 39+

**Install Commands:**

`.deb`
```
wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.deb
dpkg -i gitkraken-amd64.deb
```

`.tar.gz`
```
wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.tar.gz
tar -xvzf gitkraken-amd64.tar.gz
```

`.rpm`
```
wget https://release.gitkraken.com/linux-standalone/gitkraken-amd64.rpm
sudo dnf install ./gitkraken-amd64.rpm
```

**Note:** For older distros, use `yum` if `dnf` is not available.

**Data Location:** `/home/{user}/.gitkraken` (or `~/.gitkraken`)

---

### How to load the license file

At first launch, you’ll be prompted to load the `.dat` license file.

If you don’t have the file, contact your GitKraken admin. Admins can retrieve it from app.gitkraken.com. For older accounts or help locating the file, <a href="https://help.gitkraken.com/gitkraken-desktop/contact-support/">contact support</a>.

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-2025@2x.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">GitKraken Serverless ready after license activation.</figcaption>
</figure>

---

### Where GitKraken checks for license files

GitKraken checks the following locations for license files:

**Linux/macOS:**
- `/usr/local/share/gitkraken`
- `/usr/share/gitkraken`
- Directory above application
- Application directory
- `~/.gitkraken`

**Windows:**
- `C:\ProgramData\GitKraken`
- Directory above the `.exe`
- Directory of the `.exe`
- `%APPDATA%\.gitkraken`

---

### How to update the license file

If your license expires, you can:

- Replace the file in one of the directories listed above
- Or, update manually:
  - In GitKraken, click the license text in the bottom-left corner
  - Select <kbd>Update License</kbd>

<figure class='figure center'>
  <img src="/wp-content/uploads/serverless-license-2025@2x.png" class="img-responsive img-bordered">
  <figcaption style="text-align: center; color: #888;">Update your license manually from the client footer.</figcaption>
</figure>

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
