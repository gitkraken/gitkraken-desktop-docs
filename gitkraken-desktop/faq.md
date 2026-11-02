---
title: GitKraken Desktop FAQ | Common Questions & Troubleshooting
description: Get answers to frequently asked questions about GitKraken Desktop. Learn about features, integrations, installations, SSH issues, and troubleshooting steps.
product: GitKraken Desktop
feature: FAQ
content_type: faq
audience: all
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps, generic]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps]
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [faq, troubleshooting, ssh, plans, os-support]

taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Find quick answers to common GitKraken Desktop questions about supported platforms, account and plan limits, authentication, remote access, and troubleshooting, including Linux support, SSH behavior, proxy issues, and subscriptions.

**Key facts:**

| Topic | Current answer |
|-------|----------------|
| Supported Linux distributions | Ubuntu 18.04 LTS+, RHEL 8+, Fedora 39+ |
| Multiple accounts | Supported with a paid license by using Profiles |
| Windows SSH agent | Pageant is the supported SSH agent on Windows |
| Subscription shows Community | Make sure you are signed in with the email address associated with your subscription |

<div class='faq container'>
  <section class='pts pbm'>
    <div class='callout'>
      <h4>Need a quick reference? These resources may help:</h4>
      <ul class='dl-list plm prm'>
        <li><a href='https://www.gitkraken.com/resources/gitkraken-cheat-sheet?product=gitkraken&source=help_center' target='_blank'><em>GitKraken Desktop Cheat Sheet</em></a></li>
        <li><a href='https://www.gitkraken.com/resources/gitkraken-github-cheat-sheet?product=gitkraken&source=help_center' target='_blank'><em>GitKraken for GitHub Users Cheat Sheet</em></a></li>
      </ul>
    </div>
  </section>
</div>

---

## About GitKraken Desktop

Get a short overview of GitKraken Desktop and what you can do with it.

### What is GitKraken Desktop?

GitKraken Desktop is a Git client for Windows, macOS, and Linux built around a visual Commit Graph. It works with your existing repositories and with hosts such as GitHub, GitLab, Bitbucket, and Azure DevOps.

You can also run coding agents such as Claude Code, Codex CLI, and Copilot CLI from GitKraken Desktop. Each agent session gets its own branch and worktree. You see what the agent changed in the Commit Graph and diff, and you can undo or revert it with the same Git actions you use for your own work. See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

## Common coding agent and worktree questions

Get answers about running coding agents and worktrees in GitKraken Desktop.

### What is the Agents view?

The Agents view is a Left Panel mode in GitKraken Desktop that organizes worktrees around coding agent sessions, status, and quick actions. For more information, see [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

### Can I run multiple coding agent sessions at the same time?

Yes. Each coding agent session runs in its own worktree and working directory, so you can run parallel sessions in the same repository.

### Can I use a coding agent that GitKraken Desktop does not explicitly integrate with?

Yes. GitKraken Desktop explicitly integrates with supported coding agent CLIs such as Claude Code, Codex CLI, Copilot CLI, Cursor CLI, Gemini CLI, and OpenCode, but you can still run other coding agents manually in the embedded terminal. For more information, see [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/) and [GitKraken Terminal Guide](/gitkraken-desktop/terminal/).

### Do List view and the Agents view show different worktrees?

No. They show the same underlying worktrees. List view is reference-focused, while the Agents view is agent-focused. For more information, see [Manage Git Worktrees in GitKraken Desktop](/gitkraken-desktop/worktrees/).

### Are the Agents view and coding agent workflows available for on-prem customers?

Yes. On-premises deployments use the same GitKraken Desktop client for local workflows such as worktrees, the Agents view, and terminal-based coding agent workflows. However, which coding agents you can use depends on your on-premises environment.

OpenCode and Gemini CLI can run in fully air-gapped environments when they are configured to use an internal model endpoint. Claude Code, Codex CLI, Copilot CLI, and Cursor CLI are also supported when your organization permits them and the required services are reachable from the environment. For more information, see [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/), [Set Up GitKraken Self-Hosted Server (On-Premise)](/gitkraken-desktop/self-hosted/), and [GitKraken On-Premise Serverless (Stand-Alone) Setup](/gitkraken-desktop/serverless/).

---

## Common feature and interface questions

Get answers about integrations, platforms, accounts, and everyday tasks.

### Does GitKraken support TFS, Visual Studio Team Services, or Azure DevOps?
Yes. GitKraken Desktop integrates with [Azure DevOps](/integrations/azure-devops/). For TFS, clone the repository manually using <kbd>File > Clone Repo</kbd> and provide the HTTPS URL. On Mac or Linux, enable _Basic Authentication_ in IIS for TFS. If password authentication fails, use a personal access token (PAT).

For more information, see [SSH and HTTPS authentication](/integrations/authentication).

### What Linux distributions are supported?
GitKraken Desktop supports:
- Ubuntu 18.04 LTS+
- RHEL 8+
- Fedora 39+

Other distributions may work but are not officially supported.

### Can I use multiple GitHub/GitLab/Bitbucket/Azure DevOps accounts?
Yes, with a paid license. Use [Profiles](/start-here/profiles) to configure separate integrations for each account.

### How do I change my commit avatar?
GitKraken Desktop shows the [Gravatar](https://gravatar.com/) linked to the email address in your `.gitconfig`. To change your avatar, update your Gravatar.

### Can I use GitKraken on multiple computers?
Yes. Subscriptions are linked to your email address, not a specific machine.

### Why can’t I see remotes under the integration drop-down?
The drop-down only shows forks. Use the [URL option](/gitkraken-desktop/pushing-and-pulling/#adding-remotes) to add other remotes.

### How do I push a local project to GitHub or other remotes?
1. [Initialize a new project](/working-with-repositories/open-clone-init/#initialize-a-new-project) remotely.
2. [Open your local project](/working-with-repositories/open-clone-init/#opening-an-existing-project).
3. Add the new project as a [remote](/working-with-repositories/pushing-and-pulling/).
4. Set your branch's [upstream](/working-with-repositories/pushing-and-pulling/#setting-the-upstream-branch).
5. Push and confirm the Force Push prompt.

### How do I sign in to GitKraken?
GitKraken Desktop signs you in through your browser at gitkraken.dev. When you click a sign-in or sign-up option, GitKraken Desktop shows the **Sign In to GitKraken** window and opens your browser. Finish signing in there, and GitKraken Desktop signs you in.

If your browser does not open, click **open it manually** or **copy the URL** in the **Sign In to GitKraken** window. If GitKraken Desktop does not receive the sign-in from your browser, click **Manually enter authentication code**, paste the code from your browser, and click **Save**.

### How do I sign out of GitKraken?
Do one of the following:
- Click your profile icon, then click <kbd>Sign Out</kbd>.
- Select <kbd>File > Sign Out</kbd>.

GitKraken Desktop shows **Successfully signed out**. Signing out also disconnects the integrations you connected through your GitKraken account. To learn what reconnects when you sign in again, see [Integrations](/gitkraken-desktop/integrations/).

On GitKraken On-Premise (Self-Hosted Server or Serverless), sign-in stays in GitKraken Desktop and these options read <kbd>Sign into a different account</kbd>.

To reset all GitKraken Desktop data, delete the `~/.gitkraken` folder.

---

## Common technical troubleshooting questions

Fix common launch, authentication, connection, and display problems.

### Why am I getting a repo compatibility error? 
Close other tools, such as IDEs, then relaunch GitKraken Desktop. Run `git status` to check for uncommitted changes. You can also try switching branches or cloning the repository to a new directory.

### Why won’t GitKraken launch on Linux?
Launch GitKraken Desktop from a terminal to check for missing dependencies. See the [installation guide](/gitkraken-desktop/how-to-install/).

### Why does my subscription show COMMUNITY?  
Make sure you are signed in with the email address associated with your subscription. Click your profile icon and check the email address under **Account**. To use a different account, click **Sign Out**, then sign in with the right account.

<figure class='figure center'>
  <img src="/wp-content/uploads/gkd-profile-menu-sign-out-01-v3@2x.png" class="help-center-img img-bordered" alt="The GitKraken Desktop profile and account menu, signed in: Current profile with the profile, commit signature and Manage profiles, then Account with the account name and email, Manage account, and Sign Out highlighted.">
  <figcaption style="text-align: center; color: #888;">Check your account and sign out from the profile menu.</figcaption>
</figure>

### Why isn’t GitKraken authenticating my SSH key?
- Confirm remote URLs start with `ssh://` or `{user}@{host}:{repo}`.
- On Windows, GitKraken Desktop supports only the Pageant SSH agent. [Download Pageant](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).

### Why can’t GitKraken access my GitHub remote?
- Confirm that GitKraken Desktop is [authorized in your GitHub application settings](https://github.com/settings/applications).
- Organization access may require approval from an organization owner. [Request organization access](https://github.com/settings/connections/applications/a7557949433b7d282a76).

### Why can’t GitKraken connect to the internet (firewall or proxy)?
- GitKraken Desktop works with most firewalls, but some proxy auto-config (PAC) files or proxy settings need manual configuration.
- Use `http.proxy` or `remote.<name>.proxy` in Git config. See [Authentication](/integrations/authentication).

### Why is the graph missing commits or showing errors?
Run `git gc` in a terminal, or clone the repository into a new directory.

### Why is the window blank or UI not displaying properly?
Launch GitKraken Desktop with:
```bash
gitkraken --disable-gpu
```

### Why is my file encoding incorrect or unreadable?
In the repository's **Encoding** preference, set the encoding to `UTF-8` or choose `GUESS ENCODING`.

### How can I enable extended logging for troubleshooting?
1. Close GitKraken Desktop.
2. Rename or delete `~/.gitkraken/logs`.
3. Start GitKraken Desktop with `gitkraken -d SILLY`.
4. Reproduce the issue.
5. Find the logs in the new `logs` folder.

### I can't select repo folders on Ubuntu 20.04 or prior versions. How do I fix this?
This is a known issue. To work around it, start GitKraken Desktop with:
```bash
gitkraken --xdg-portal-required-version=3
```

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
