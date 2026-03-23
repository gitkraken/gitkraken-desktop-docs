---
title: Upgrade GitKraken Self-Hosted Server (Docker & Client Instructions)
description: Step-by-step guide to upgrading GitKraken Self-Hosted Server, Docker images, client installers, and license file—including how to reset the Super User password.
product: GitKraken Self-Hosted
feature: Self-Hosted Upgrade
content_type: how-to
audience: enterprise-admin
plan_required: Enterprise
os_support: [server-linux]
git_hosts: [n/a]
integrations: []
hosted_variant: self-hosted
status: GA
last_verified: 2026-03
llms_include: true
tags: [self-hosted, upgrade, docker, license, super-user]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to upgrade GitKraken Self-Hosted Server, client installers, and license files when your deployment runs on Docker. It also covers the Super User password reset flow, so administrators can handle both standard upgrades and recovery tasks from the same procedure.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately from standard subscriptions. To purchase, see our <a href='https://www.gitkraken.com/git-client/on-premise-pricing?source=help_center&product=gitkraken'>On-Premise Pricing</a> page.</p>
</div>

***

## Quick Start


**To upgrade the server:**
1. Navigate to the folder containing `docker-compose.yml` and run `sudo docker-compose down`.
2. Back up the existing `docker-compose.yml`.
3. Extract the new `GitKrakenEnterpriseServer.zip` into the same folder.
4. Compare the old and new `docker-compose.yml` for port, volume, or environment variable changes.
5. Run `sudo sh loadImages.sh` to load the new Docker images.
6. Run `sudo docker-compose up` to restart the server.

**To upgrade client installers:** Locate the release volume path in `docker-compose.yml` under `gk-enterprise-controller`, navigate to the host path, and extract the new `release.zip` into that directory.

**To update the license:** Copy the new `license.dat` file to the server, open the License tab on your Enterprise site, and upload the file.

**To reset the Super User password:** Stop the server, add `SUPER_USER_RESET: 1` to the `gk-services` environment in `docker-compose.yml`, restart, and visit `/reset/super-user` in your browser.

***

## How to upgrade the self-hosted server

1. Navigate to the folder where GitKraken Self-Hosted is installed (the folder with `docker-compose.yml`).

2. Take down the current instance:
   ```bash
   sudo docker-compose down
   ```

3. Back up the `docker-compose.yml` file.

4. Extract `GitKrakenEnterpriseServer.zip` in the same folder. This will overwrite `docker-compose.yml`.

5. Compare the new and old `docker-compose.yml` for differences, such as:
   - Port configurations
   - Volume mount paths
   - Environment variable updates

6. If you are not using `docker-compose` (e.g., Nomad setup), adjust image names/tags in your swarm manager accordingly.

7. Load Docker images:
   ```bash
   sudo sh loadImages.sh
   ```

8. Restart the server from the same directory:
   ```bash
   sudo docker-compose up
   ```

**Note:** Always run `docker-compose up` from the original directory. On CentOS or RHEL7, you may need full paths:
```bash
sudo systemctl start docker.service
sudo /usr/local/bin/docker-compose up
```

***

## How to upgrade self-hosted clients

1. Open your `docker-compose.yml` file.

2. Find the `gk-enterprise-controller` service. Under `volumes`, identify the client volume:
   ```
   - ./gk-data/release:/controller/release
   ```

3. This line splits into:
   - Host path: `./gk-data/release`
   - Container path: `/controller/release`

4. Navigate to the release folder on the host machine. Extract `release.zip` and overwrite existing content.

5. After extracting, your folder should look like:
   ```
   ./gk-data/
      └── release/
          ├── linux/
          ├── darwin/
          ├── win32/
          └── win64/
   ```

6. GitKraken Self-Hosted users will now receive the latest client.

***

## How to update the license

To update your GitKraken Self-Hosted license:

1. Copy the new `license.dat` file to the server.
2. Open the License tab on your Enterprise site.
3. Browse to and select the new license file.

<figure class='figure center'>
  <img src='/wp-content/uploads/license-settings@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Use the License tab to upload a new license file.</figcaption>
</figure>

***

## How to reset the Super User password

1. Stop GitKraken Self-Hosted:
   ```bash
   sudo docker-compose down
   ```

2. Add the environment variable `SUPER_USER_RESET: 1` under `gk-services` in `docker-compose.yml`:
   ```yaml
   environment:
     SUPER_USER_RESET: 1
   ```

3. Start the instance:
   ```bash
   sudo docker-compose up
   ```

4. Visit `/reset/super-user` in your browser to set a new password.

5. Confirm login works, then shut down the server:
   ```bash
   sudo docker-compose down
   ```

6. Remove the `SUPER_USER_RESET` variable from `docker-compose.yml`.

7. Restart GitKraken Self-Hosted:
   ```bash
   sudo docker-compose up
   ```

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;height:28px;padding:0 8px;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s;font-size:11px;font-family:sans-serif}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='Copy',K='Copied!';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).trimEnd()).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
