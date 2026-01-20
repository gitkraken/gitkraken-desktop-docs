---
title: GitKraken Desktop FAQ | Common Questions & Troubleshooting
description: Get answers to frequently asked questions about GitKraken Desktop. Learn about features, integrations, installations, SSH issues, and troubleshooting steps.

taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

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
