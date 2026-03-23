---
title: Configure GitKraken Self-Hosted Server (LDAP, SMTP, and Super User)
description: Step-by-step instructions to configure GitKraken Self-Hosted Server. Set up licensing, LDAP authentication, SMTP server, and Super User access.
product: GitKraken Self-Hosted
feature: Self-Hosted Configuration
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
tags: [self-hosted, ldap, smtp, super-user, configuration]
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to complete the first-time configuration of GitKraken Self-Hosted Server after installation. It covers license upload, authentication mode selection, LDAP setup, SMTP settings, Super User creation, and initial user-management steps needed before the server is ready for administrators and users.

**Requirements and limits**
- Use this page after the GitKraken Self-Hosted Server installation is already running and reachable in a browser.
- A valid Self-Hosted license file is required before configuration can be completed.
- Choose either Built-in authentication or LDAP; SMTP is required unless you use LDAP authentication.
- The Super User account manages the server, does not consume a user license, and cannot sign in to GitKraken Desktop directly.
- LDAP setup requires server connection details, group mappings, and user attribute mappings before users can authenticate successfully.

<div class='callout callout--warning'>
  <p>GitKraken Desktop Self-Hosted and On-Premise Serverless products are sold separately from standard subscriptions. Visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing?source=help_center&product=gitkraken'>On-Premise Pricing</a> page to learn more.</p>
</div>

***

## Quick Start

Configure GitKraken Self-Hosted Server after installation by completing the license, authentication, SMTP, and Super User setup steps.

1. Navigate to your GitKraken Self-Hosted server in a browser.
2. Click **Browse for license** and upload the license file included with your installation package.
3. Choose an authentication method: **Built-in** (email and password) or **LDAP**.
   - If using LDAP, enter your server hostname, port, encryption method, base DNs, group CNs, and user attribute mappings. Optionally enable the Sync Server for automatic user syncing.
4. If using Built-in authentication, configure your SMTP server: enter the hostname, port, From Address, and credentials, then click the test connection button to verify.
5. Create a Super User account by entering an email and password. This account manages the server but cannot log in to GitKraken Desktop directly.
6. Click **Save** to complete configuration. The Manage Users screen will appear, where you can begin adding user accounts.

To add users, click **Add user** and enter the user's email. To disable self-registration, adjust the setting in the **Registration** tab.

***

<a id="server-license"></a>

## How to upload the server license

Navigate to your GitKraken Self-Hosted server.

<figure>
<img src='/wp-content/uploads/select-license@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Prompt to upload your GitKraken Self-Hosted license file</figcaption>
</figure>

Click **Browse for license** and upload the license file provided with your installation package. Once selected, license details will be displayed.

<figure>
<img src='/wp-content/uploads/license-details@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Details view of your Self-Hosted license</figcaption>
</figure>

<a id="authentication"></a>

## How authentication setup works

Choose the authentication configuration for your server:

- **Built-in**: Users sign in using an email and password.
- **LDAP**: Users authenticate using LDAP credentials.

<figure>
<img src='/wp-content/uploads/auth-config@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Select authentication mode: Built-in or LDAP</figcaption>
</figure>

If using Built-in authentication, [skip to the SMTP Server section](#smtp-server).

<a id="ldap-configuration"></a>

### How to configure LDAP

Enter your LDAP server hostname and port:

<figure>
<img src='/wp-content/uploads/ldap-host-port@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Configure hostname and port for LDAP</figcaption>
</figure>

Choose the corresponding encryption method:

<figure>
<img src='/wp-content/uploads/encryption-method@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Select the appropriate LDAP encryption method</figcaption>
</figure>

Specify the following LDAP configuration fields:

- **Base Distinguished Names** – Top-level directory paths to search for users.
- **Access Group Common Names** – Groups that are granted GitKraken licenses. If omitted, all found users are granted access.
- **Admin Group Common Names** – Groups granted administrative access. If omitted, no users receive admin rights.

<figure>
<img src='/wp-content/uploads/base-dn@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Assign base DNs and group CNs for LDAP integration</figcaption>
</figure>

Set the required user attribute mappings:

- **Username Attribute** – Maps to GitKraken usernames (required).
- **Email Attribute** – Maps to user emails (required).
- **Name Attribute** – Maps to user display names (optional).

<figure>
<img src='/wp-content/uploads/user-attributes@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Assign LDAP attributes for username, email, and name</figcaption>
</figure>

Provide the DN of a search user account with read access to users and groups:

<figure>
<img src='/wp-content/uploads/search-user@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Designate an LDAP search user account</figcaption>
</figure>

<div class='callout callout--warning'>
  <p>Note: The Domain Search Password field will always appear blank, even when a value is set.</p>
</div>

Enable the Sync Server if you want GitKraken to regularly sync with LDAP:

<figure>
<img src='/wp-content/uploads/sync-server@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Configure LDAP sync interval</figcaption>
</figure>

If Sync Server is disabled, you'll need to manage user accounts manually.

<a id="smtp-server"></a>

## How to configure the SMTP server

An SMTP server is required unless you're using LDAP authentication.

Specify the server details:
- **SMTP IP address or hostname**
- **SMTP port**
- **From Address**

Enable secure protocols if necessary and provide authentication credentials. Use the test connection button to verify:

<figure>
<img src='/wp-content/uploads/smtp-setup@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Set up SMTP server settings and test connection</figcaption>
</figure>

<a id="super-user"></a>

## How to configure the Super User

The Super User is the license owner of GitKraken Self-Hosted. This account:

- Does not consume a user license
- Cannot log into GitKraken Desktop
- Cannot be viewed or modified via the account site user management page

<figure>
<img src='/wp-content/uploads/super-user@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Define the Super User account</figcaption>
</figure>

<div class='callout callout--neutral'>
  <p>Note: To reset the Super User password, visit the <a href="/enterprise/upgrade-enterprise/#reset-the-super-user-password">upgrade guide</a>.</p>
</div>

Configuration is now complete! You should see the 'Manage Users' screen, where you can begin adding users.

<figure>
<img src='/wp-content/uploads/manage-users@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Manage Users interface after setup</figcaption>
</figure>

<a id="adding-users"></a>

## How to add users

To add a user, click **Add user** and enter the user's email address:

<figure>
<img src='/wp-content/uploads/user-email@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Enter email address to add a new user</figcaption>
</figure>

By default, users can self-register on the GitKraken Self-Hosted site. To disable self-registration, go to the **Registration** tab:

<figure>
<img src='/wp-content/uploads/registration-settings@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Modify user registration settings</figcaption>
</figure>
