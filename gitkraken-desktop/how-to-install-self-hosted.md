---
title: Install GitKraken Self-Hosted Server
description: How to install GitKraken Self-Hosted Server
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

GitKraken Self-Hosted Server runs on a Linux virtual machine (CentOS, Ubuntu, or RHEL7) inside Docker containers. To begin, you'll first need to install Docker.

<div class='callout callout--warning'>
    <p>GitKraken Desktop Self-Hosted and On-Premise Serverless versions are sold separately from standard subscriptions. To purchase, visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing?_gl=1*vtr4xk*_up*MQ..*_gs*MQ..&gclid=Cj0KCQjwqIm_BhDnARIsAKBYcmv98H0EKgytPnuCPuTqdL2vy4GQaCsizBMO9m8mz2n1hMMXO3AAw7YaAiyKEALw_wcB?source=help_center&product=gitkraken'>On-Premise Pricing</a> page.</p>
</div>

<ul>
  <li><a href="#install_centos">Install on CentOS</a></li>
  <li><a href="#install_ubuntu">Install on Ubuntu</a></li>
  <li><a href="#install_rhel7">Install on RHEL7</a></li>
</ul>

***

<a id="install_centos"></a>

## Install Docker CE on CentOS

These instructions are based on the official [Docker documentation](https://docs.docker.com/engine/installation/linux/centos/#install-docker).

### With internet access

1. Install required packages:
```bash
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
```

2. Set up the stable repository:
```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

3. Update the yum package index:
```bash
sudo yum makecache fast
```

4. Install Docker:
```bash
sudo yum install docker-ce
```

5. Configure the Docker daemon:
```json
{
  "storage-driver": "devicemapper"
}
```
Edit or create the `/etc/docker/daemon.json` file with the above content.

6. Start Docker:
```bash
sudo systemctl start docker
```

7. Switch to root user:
```bash
sudo su
```

8. Download Docker Compose:
```bash
curl -L https://github.com/docker/compose/releases/download/1.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
```

9. Apply executable permissions:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

10. Proceed to the installation section.

### Without internet access

1. Download Docker CE and Docker Compose on a different machine.
  * [Docker CE for CentOS](https://download.docker.com/linux/centos/7/x86_64/stable/Packages/)
  * [Docker Compose](https://github.com/docker/compose/releases/download/1.14.0/docker-compose-Linux-x86_64)

2. Transfer the packages to the target server.

3. Install the packages:
```bash
sudo yum install /path/to/docker-ce-selinux-package.rpm
sudo yum install /path/to/docker-ce-package.rpm
```

4. Move and rename Docker Compose:
```bash
sudo mv docker-compose-Linux-x86_64 /usr/local/bin/docker-compose
```

5. Change permissions:
```bash
chmod +x /usr/local/bin/docker-compose
```

6. Configure the Docker daemon as previously described.

7. Start Docker:
```bash
sudo systemctl start docker
```

8. Continue to the installation section.

<a id="install_ubuntu"></a>

## Install Docker CE on Ubuntu

Refer to the official [Docker documentation](https://docs.docker.com/engine/installation/linux/ubuntu/#install-docker).

### With internet access

1. Install required packages:
```bash
sudo apt-get install apt-transport-https ca-certificates curl software-properties-common
```

2. Add Docker’s GPG key:
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

3. Verify the key:
```bash
sudo apt-key fingerprint 0EBFCD88
```

4. Set up the stable repository:
```bash
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
```

5. Update the apt package index:
```bash
sudo apt-get update
```

6. Install Docker:
```bash
sudo apt-get install docker-ce
```

7. Switch to root user:
```bash
sudo su
```

8. Download Docker Compose:
```bash
curl -L https://github.com/docker/compose/releases/download/1.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
```

9. Apply executable permissions:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

10. Proceed to the installation section.

<a id="install_rhel7"></a>

## Install Docker CE on RHEL7

### With internet access

1. Install required packages:
```bash
sudo yum install -y yum-utils device-mapper-persistent-data lvm2
```

2. Set up the Docker repository:
```bash
sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo
```

3. Update the yum package index:
```bash
sudo yum makecache fast
```

4. Install Docker:
```bash
sudo yum install --setopt=obsoletes=0 docker-ce-17.03.2.ce-1.el7.centos.x86_64 docker-ce-selinux-17.03.2.ce-1.el7.centos.noarch
```

5. (Optional) To view available Docker versions:
```bash
yum list docker-ce --showduplicates | sort -r
```

6. Configure the Docker daemon:
```json
{
  "storage-driver": "devicemapper"
}
```
Edit or create the `/etc/docker/daemon.json` file with the above content.

7. Start Docker:
```bash
sudo systemctl start docker
```

8. Switch to root user:
```bash
sudo su
```

9. Download Docker Compose:
```bash
curl -L https://github.com/docker/compose/releases/download/1.14.0/docker-compose-`uname -s`-`uname -m` > /usr/local/bin/docker-compose
```

10. Apply executable permissions:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

11. Proceed to the installation section.


<a id="install_enterprise"></a>

##  Install GitKraken Self-Hosted Server

<span>1.</span> Extract _GitKrakenEnterpriseServer.zip_ in a folder of your choosing
(all commands in the following instructions will be performed in that folder).

<span>2.</span> Load the images into Docker:
```
sudo sh loadImages.sh
```

<span>3.</span> Configure what port GitKraken Self-Hosted should run on the host server.
By default GitKraken Self-Hosted server will run on port 3000.

  You can change the port by opening up the _docker-compose.yml_ file and making a few modifications.  
  First, find the `ports` section under `gk-enterprise-controller`:
  ```yaml
    ports:
      "3000:3000"
  ```

  Modify the first `3000` to the desired port
  For example, to use port 80 change it to:

  ```yml
    ports:
      "80:3000"
  ```

  Then update the `GITKRAKEN_ENTERPRISE_URL` environment variable to use the desired port.  Again, for port 80 it would look like:
  ```yaml
    environment:
        GITKRAKEN_ENTERPRISE_URL: http://localhost:80
  ```

  Finally, find the `GITKRAKEN_ENTERPRISE_URL` environment variable in the `gk-services` section and modify the port.  For port 80, this would look like:
  ```yaml
    environment:
        GITKRAKEN_ENTERPRISE_URL: http://localhost:80
  ```
<span>4.</span> *Optional* Update the base URL from localhost. If you want to access the user management page from outside of this server, you will want to update the base URL. This means updating `GITKRAKEN_ENTERPRISE_URL` wherever it exists in the `docker-compose.yml` file. An example:

  ```yaml
    environment:
        GITKRAKEN_ENTERPRISE_URL: http://gitkraken.example.com:80
  ```
  
<span>5.</span> Configure where GitKraken Desktop releases are stored on your host server.
By default the releases folder is set to _./gk-data/release_. You can change the location by opening up
the _docker-compose.yml_ file and finding the section under `gk-enterprise-controller`:
```
volumes:
 ./gk-data/release:/controller/release # The volume where GitKraken Self-Hosted clients go.
```
and modifying _./gk-data/release_ to point to another directory on your host server.

<span>6.</span> Create the folder specified in the above step on your host server.

<span>7.</span> Extract _release.zip_ in the folder you created on your host server
(releases will always be extracted in this folder).

<span>8.</span> In the same folder containing the _docker-compose.yml_ file, run the following command:
```
sudo docker-compose up
```
  * To run this command in the background, use `docker-compose up -d` instead.
  * Note: If installing in CentOS or RHEL7, you may need to specify the full path to the docker-compose installation.  The following commands should allow you to run the docker-compose command successfully:
```
sudo systemctl start docker.service
sudo /usr/local/bin/docker-compose up
```

<span>9.</span> Navigate to http://localhost:3000 and complete the setup
(the port in the URL should match the port from step 3, and the URL should match step 4, if either was changed).
