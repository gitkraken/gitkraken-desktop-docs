---
title: Configure GitKraken Self-Hosted Server (LDAP, SMTP, and Super User)
description: Step-by-step instructions to configure GitKraken Self-Hosted Server. Set up licensing, LDAP authentication, SMTP server, and Super User access.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: June 2025</kbd>

After installing GitKraken Self-Hosted Server (also known as Enterprise Self-Hosted), you're ready to configure your server.

<div class='callout callout--warning'>
  <p>GitKraken Desktop Self-Hosted and On-Premise Serverless products are sold separately from standard subscriptions. Visit our <a href='https://www.gitkraken.com/git-client/on-premise-pricing?source=help_center&product=gitkraken'>On-Premise Pricing</a> page to learn more.</p>
</div>

***

<a id="server-license"></a>

## Server License

Navigate to your GitKraken Self-Hosted server.

<figure>
<img src='/wp-content/uploads/select-license.png' srcset='/wp-content/uploads/select-license@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Prompt to upload your GitKraken Self-Hosted license file</figcaption>
</figure>

Click **Browse for license** and upload the license file provided with your installation package. Once selected, license details will be displayed.

<figure>
<img src='/wp-content/uploads/license-details.png' srcset='/wp-content/uploads/license-details@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Details view of your Self-Hosted license</figcaption>
</figure>

<a id="authentication"></a>

## Authentication

Choose the authentication configuration for your server:

- **Built-in**: Users sign in using an email and password.
- **LDAP**: Users authenticate using LDAP credentials.

<figure>
<img src='/wp-content/uploads/auth-config.png' srcset='/wp-content/uploads/auth-config@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Select authentication mode: Built-in or LDAP</figcaption>
</figure>

If using Built-in authentication, [skip to the SMTP Server section](#smtp-server).

<a id="ldap-configuration"></a>

### LDAP Configuration

Enter your LDAP server hostname and port:

<figure>
<img src='/wp-content/uploads/ldap-host-port.png' srcset='/wp-content/uploads/ldap-host-port@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Configure hostname and port for LDAP</figcaption>
</figure>

Choose the corresponding encryption method:

<figure>
<img src='/wp-content/uploads/encryption-method.png' srcset='/wp-content/uploads/encryption-method@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Select the appropriate LDAP encryption method</figcaption>
</figure>

Specify the following LDAP configuration fields:

- **Base Distinguished Names** – Top-level directory paths to search for users.
- **Access Group Common Names** – Groups that are granted GitKraken licenses. If omitted, all found users are granted access.
- **Admin Group Common Names** – Groups granted administrative access. If omitted, no users receive admin rights.

<figure>
<img src='/wp-content/uploads/base-dn.png' srcset='/wp-content/uploads/base-dn@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Assign base DNs and group CNs for LDAP integration</figcaption>
</figure>

Set the required user attribute mappings:

- **Username Attribute** – Maps to GitKraken usernames (required).
- **Email Attribute** – Maps to user emails (required).
- **Name Attribute** – Maps to user display names (optional).

<figure>
<img src='/wp-content/uploads/user-attributes.png' srcset='/wp-content/uploads/user-attributes@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Assign LDAP attributes for username, email, and name</figcaption>
</figure>

Provide the DN of a search user account with read access to users and groups:

<figure>
<img src='/wp-content/uploads/search-user.png' srcset='/wp-content/uploads/search-user@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Designate an LDAP search user account</figcaption>
</figure>

<div class='callout callout--warning'>
  <p>Note: The Domain Search Password field will always appear blank, even when a value is set.</p>
</div>

Enable the Sync Server if you want GitKraken to regularly sync with LDAP:

<figure>
<img src='/wp-content/uploads/sync-server.png' srcset='/wp-content/uploads/sync-server@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Configure LDAP sync interval</figcaption>
</figure>

If Sync Server is disabled, you'll need to manage user accounts manually.

<a id="smtp-server"></a>

## SMTP Server

An SMTP server is required unless you're using LDAP authentication.

Specify the server details:
- **SMTP IP address or hostname**
- **SMTP port**
- **From Address**

Enable secure protocols if necessary and provide authentication credentials. Use the test connection button to verify:

<figure>
<img src='/wp-content/uploads/smtp-setup.png' srcset='/wp-content/uploads/smtp-setup@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Set up SMTP server settings and test connection</figcaption>
</figure>

<a id="super-user"></a>

## Super User

The Super User is the license owner of GitKraken Self-Hosted. This account:

- Does not consume a user license
- Cannot log into GitKraken Desktop
- Cannot be viewed or modified via the account site user management page

<figure>
<img src='/wp-content/uploads/super-user.png' srcset='/wp-content/uploads/super-user@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Define the Super User account</figcaption>
</figure>

<div class='callout callout--neutral'>
  <p>Note: To reset the Super User password, visit the <a href="/enterprise/upgrade-enterprise/#reset-the-super-user-password">upgrade guide</a>.</p>
</div>

Configuration is now complete! You should see the 'Manage Users' screen, where you can begin adding users.

<figure>
<img src='/wp-content/uploads/manage-users.png' srcset='/wp-content/uploads/manage-users@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Manage Users interface after setup</figcaption>
</figure>

<a id="adding-users"></a>

## Adding Users

To add a user, click **Add user** and enter the user's email address:

<figure>
<img src='/wp-content/uploads/user-email.png' srcset='/wp-content/uploads/user-email@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Enter email address to add a new user</figcaption>
</figure>

By default, users can self-register on the GitKraken Self-Hosted site. To disable self-registration, go to the **Registration** tab:

<figure>
<img src='/wp-content/uploads/registration-settings.png' srcset='/wp-content/uploads/registration-settings@2x.png' style="max-width: 66%; height: auto; margin: 0 auto;" class="help-center-img img-bordered" />
<figcaption style="text-align: center; color: #888">Modify user registration settings</figcaption>
</figure>
