---
title: GitKraken Desktop FAQ | Common Questions & Troubleshooting
description: Get answers to frequently asked questions about GitKraken Desktop. Learn about features, integrations, installations, SSH issues, and troubleshooting steps.

taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

The answers to your most frequently asked questions.

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

## Features and Interface

### Does GitKraken support TFS, Visual Studio Team Services, or Azure DevOps?
Yes. GitKraken integrates with [Azure DevOps](/integrations/azure-devops/). For TFS, clone the repository manually using <kbd>File > Clone Repo</kbd> and provide the HTTPS URL. On Mac or Linux, enable _Basic Authentication_ in IIS for TFS. Consider using a Personal Access Token (PAT) if password authentication fails.

More info: [SSH and HTTPS authentication](/integrations/authentication)

### What Linux distributions are supported?
GitKraken supports:
- Ubuntu 18.04 LTS+
- RHEL 8+
- Fedora 39+

Other distributions may work but are not officially supported.

### Can I use multiple GitHub/GitLab/Bitbucket/Azure DevOps accounts?
Yes—with a paid license. Use [Profiles](/start-here/profiles) to configure separate integrations for each account.

### How do I change my commit avatar?
Your avatar is linked to your `.gitconfig` email address via [Gravatar](https://gravatar.com/). Update your Gravatar to change your displayed avatar.

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

### How do I sign out of GitKraken?
While there’s no sign-out button, you can:
- Click your profile icon → <kbd>Sign into a different account</kbd>
- Or delete the `~/.gitkraken` folder to reset data

---

## Technical Issues

### Why am I getting a repo compatibility error? 
Try closing other tools like IDEs, then relaunch GitKraken. Use `git status` to check for uncommitted changes. Try switching branches or cloning to a new directory.

### Why won’t GitKraken launch on Linux?
Launch from terminal to check for missing dependencies. Refer to the [installation guide](/gitkraken-desktop/how-to-install/).

### Why does my subscription show COMMUNITY?  
Verify that you're logged into the email associated with your subscription. Check this via your profile icon.

<figure class='figure center'>
  <img src="/wp-content/uploads/sign-into-a-different-account.png" class="help-center-img img-bordered" alt="Sign into a different GitKraken account">
  <figcaption style="text-align: center; color: #888;">Access alternate login via the profile menu.</figcaption>
</figure>

### Why isn’t GitKraken authenticating my SSH key?
- Confirm remote URLs start with `ssh://` or `{user}@{host}:{repo}`.
- GitKraken does not use `~/.ssh/config`. Load the key manually or use your OS agent.
- On Windows, only Pageant is supported. [Download here](http://www.chiark.greenend.org.uk/~sgtatham/putty/download.html).

### Why can’t GitKraken access my GitHub remote?
- Confirm GitKraken is [authorized](https://github.com/settings/applications).
- Org access may require approval from the owner. [Request access](https://github.com/settings/connections/applications/a7557949433b7d282a76).

### Why can’t GitKraken connect to the internet (firewall or proxy)?
- GitKraken works with most firewalls but some PACs or proxy settings may need manual config.
- Use `http.proxy` or `remote.<name>.proxy` in Git config. See [Authentication](/integrations/authentication).

### Why is the graph missing commits or showing errors?
Run `git gc` in terminal or clone into a fresh directory.

### Why is the window blank or UI not displaying properly?
Launch GitKraken with:
```bash
gitkraken --disable-gpu
```

### Why is my file encoding incorrect or unreadable?
Set encoding to `UTF-8` or use `GUESS ENCODING` under repository preferences.

### How can I enable extended logging for troubleshooting?
1. Close GitKraken  
2. Rename or delete `~/.gitkraken/logs`  
3. Start GitKraken using: `gitkraken -d SILLY`  
4. Reproduce the issue  
5. Logs will be saved in the new `logs` folder

### I can't select repo folders on Ubuntu 20.04 or prior versions. How do I fix this?
This is due to a known Electron issue. Start GitKraken with:
```bash
gitkraken --xdg-portal-required-version=3
```

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;width:28px;height:28px;padding:0;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s,width .15s,padding .15s}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3);width:auto;padding:0 8px;gap:4px}
</style>
<script>(function(){var C='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2 2v1"></path></svg>',K='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg><span style="font-size:11px;margin-left:4px;font-family:sans-serif">Copied!</span>';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).replace(/[\r\n]+$/, '')).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
