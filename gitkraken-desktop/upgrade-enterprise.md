---
title: Upgrade GitKraken Self-Hosted Server (Docker & Client Instructions)
description: Step-by-step guide to upgrading GitKraken Self-Hosted Server, Docker images, client installers, and license file—including how to reset the Super User password.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

The upgrade procedure is the same whether you're running GitKraken Self-Hosted on CentOS, Ubuntu, or RHEL7.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately from standard subscriptions. To purchase, see our <a href='https://www.gitkraken.com/git-client/on-premise-pricing?source=help_center&product=gitkraken'>On-Premise Pricing</a> page.</p>
</div>

***

## Upgrade Self-Hosted Server

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

## Upgrade Self-Hosted Clients

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

## Update License

To update your GitKraken Self-Hosted license:

1. Copy the new `license.dat` file to the server.
2. Open the License tab on your Enterprise site.
3. Browse to and select the new license file.

<figure class='figure center'>
  <img src='/wp-content/uploads/license-settings.png' srcset='/wp-content/uploads/license-settings@2x.png 2x' class="help-center-img img-bordered">
  <figcaption style="text-align: center; color: #888;">Use the License tab to upload a new license file.</figcaption>
</figure>

***

## Reset the Super User Password

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
