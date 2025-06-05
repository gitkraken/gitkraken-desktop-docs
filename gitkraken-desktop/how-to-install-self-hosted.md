---
title: Install GitKraken Self-Hosted Server with Docker
description: Step-by-step guide to installing GitKraken Self-Hosted Server on CentOS, Ubuntu, or RHEL7 using Docker and Docker Compose.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

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

### Without internet access

1. Download Docker CE package from a machine with internet access.
  * [Docker CE for Ubuntu](https://download.docker.com/linux/ubuntu/dists/)

   Check your version:
```bash
lsb_release -a
```

2. Download Docker Compose:
  * [Docker Compose](https://github.com/docker/compose/releases/download/1.14.0/docker-compose-Linux-x86_64)

3. Transfer both files to the host server.

4. Install Docker:
```bash
sudo dpkg -i /path/to/package.deb
# Example:
sudo dpkg -i docker-ce_17.06.0-ce-0-ubuntu_amd64.deb
```

5. Move and rename Docker Compose:
```bash
sudo mv docker-compose-Linux-x86_64 /usr/local/bin/docker-compose
```

6. Apply executable permissions:
```bash
sudo chmod +x /usr/local/bin/docker-compose

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

### Without internet access

1. Download Docker CE and Docker Compose packages from a machine with internet access.

   * [Docker CE for CentOS](https://download.docker.com/linux/centos/7/x86_64/stable/Packages/)  (select both the docker-ce-selinux and the docker-ce package of the same version, e.g., 17.03.1)
   * [Docker Compose](https://github.com/docker/compose/releases/download/1.14.0/docker-compose-Linux-x86_64)

2. Transfer the files to the host server.

3. Install Docker:
```bash
sudo yum install /path/to/docker-ce-selinux-package.rpm
sudo yum install /path/to/docker-ce-package.rpm
```

4. Move Docker Compose to the appropriate directory:
```bash
sudo mv docker-compose-Linux-x86_64 /usr/local/bin/docker-compose
```

5. Apply executable permissions:
```bash
sudo chmod +x /usr/local/bin/docker-compose
```

6. Configure the Docker daemon:

Edit or create the `/etc/docker/daemon.json` file:
```json
{
  "storage-driver": "devicemapper"
}
```

7. Start Docker:
```bash
sudo systemctl start docker
```

8. Proceed to the [installation section](#install_enterprise).

## Install GitKraken Self-Hosted Server

1. Extract the `GitKrakenEnterpriseServer.zip` file into a directory of your choice. All subsequent commands assume you are operating within this directory.

2. Load the Docker images:
```bash
sudo sh loadImages.sh
```

3. Configure the port on which GitKraken Self-Hosted should run. By default, it runs on port 3000. To change it, edit the `docker-compose.yml` file:

Find the `ports` section under `gk-enterprise-controller`:
```yaml
ports:
  - "3000:3000"
```

Change the first value to your desired port. For example, to use port 80:
```yaml
ports:
  - "80:3000"
```

Update the `GITKRAKEN_ENTERPRISE_URL` in both the `gk-enterprise-controller` and `gk-services` sections:
```yaml
environment:
  GITKRAKEN_ENTERPRISE_URL: http://localhost:80
```

4. *(Optional)* To access GitKraken Self-Hosted from outside the server, update `GITKRAKEN_ENTERPRISE_URL` with your domain:
```yaml
environment:
  GITKRAKEN_ENTERPRISE_URL: http://gitkraken.example.com:80
```

5. Configure the folder where GitKraken Desktop releases will be stored. The default path is `./gk-data/release`. To change this, update the volume under `gk-enterprise-controller`:
```yaml
volumes:
  - /your/custom/path:/controller/release
```

6. Create the directory you specified for storing releases on the host machine.

7. Extract `release.zip` into the directory you created in step 6.

8. In the directory containing `docker-compose.yml`, start the application:
```bash
sudo docker-compose up
```
* To run in detached mode:
```bash
sudo docker-compose up -d
```

* For CentOS or RHEL7, you may need to use the full path:
```bash
sudo systemctl start docker.service
sudo /usr/local/bin/docker-compose up
```

9. Visit `http://localhost:3000` (or the configured URL/port) in your browser to complete the setup.