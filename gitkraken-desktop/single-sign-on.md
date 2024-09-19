---

title: Single Sign On (SSO)
description: How to enable and use Single Sign On (SSO)
taxonomy:
    category: gitkraken-desktop

---

Single Sign On (SSO) is an easy way to manage your users across all your services. This is only for use with the cloud versions of GitKraken, it is not available for On-Premise plans.

Once your organization has set up SSO with an Identity Provider (IdP), the Owner or an Admin on your GitKraken organization can link your organization to that identity provider. Then, any users associated with your IdP can login to GitKraken apps and services.

Note: You must have a GitKraken Teams or GitKraken Enterprise subscription to enable SSO. You also can try SSO during a 30-day multi-user trial.

***

## What is Single Sign-on (SSO)?

The <a href='https://en.wikipedia.org/wiki/Single_sign-on' target='_blank'>Wikipedia</a> definition of SSO:

*“Single sign-on is an authentication scheme that allows a user to log in with a single ID to any of several related, yet independent, software systems. True single sign-on allows the user to log in once and access services without re-entering authentication factors.”*

<img src="/wp-content/uploads/sso-example-diagram.png" class="img-bordered img-responsive center">

The above diagram depicts what a typical SSO setup entails. Here is some relevant terminology:

**Directory Server:**  A Directory Server is an application that stores information about the “objects” that belong to an organization. An object is typically something like: printers, computers, shared folders, users, or groups. Some objects can contain other objects which then allows them to reflect hierarchical structures.  

Examples of Directory Server applications are:
* <a href='https://docs.microsoft.com/en-us/windows-server/identity/ad-ds/ad-ds-getting-started' target='_blank'>Microsoft Active Directory</a> 
* <a href='https://www.oracle.com/security/identity-management/governance/' target='_blank'>Oracle Identity Governance (OIG) Suite</a> 
* <a href='https://jumpcloud.com/' target='_blank'>Jump Cloud</a> 

**Identity Provider:**  An identity provider (abbreviated IdP or IDP) is a system entity that creates, maintains, and manages identity information as well as provides authentication services to relying applications within a distributed network. An IdP provider stores 3 main components: Users, Groups, and Applications.

Examples of Identity Provider applications are:
* <a href='https://azure.microsoft.com/' target='_blank'>Azure Active Directory</a> 
* <a href='https://www.okta.com/' target='_blank'>Okta</a>
* <a href='https://cloud.google.com/identity-platform' target='_blank'>Google Identity Platform</a>

The Identity Providers provide services that allow third party applications to authenticate their users. The authentication mechanism they provide is called “Oauth”, which allows third party applications to authenticate users without accessing/storing their password. 

**Third party applications:** These are the applications that use IdP services to authenticate users. The end user is redirected to the IdP to instead login there. Then the Idp directs back to the 3rd party app to complete the login, confirming that the user is who they claim to be.

Examples of  third party apps:
* <a href='https://www.gitkraken.com/' target='_blank'>GitKraken</a> 
* <a href='https://slack.com/' target='_blank'>Slack</a> 
* <a href='https://www.atlassian.com/software/jira' target='_blank'>Jira</a> 

***

## SSO in GitKraken

GitKraken is a 3rd party application in this scenario. The owner or an admin of the GitKraken organization can set up SSO with GitKraken.

### Supported Identity Providers

GitKraken uses SAML 2.0 for SSO, therefore any IdP that supports SAML 2.0 should work with GitKraken.

### License Requirements

Single sign-on requires a GitKraken Teams, GitKraken Enterprise, or a 30-day multi-user trial. To use multiple domains requires GitKraken Enterprise or a 30-day multi-user trial.

### SSO Enforcement on GitKraken

- GitKraken SSO is enforced at the domain level. This means every account on GitKraken that has an email for the account which matches the domain is required to login using SSO.
  - Only users with the user or billing contact role are required to use SSO. The Owner and admins of the organization can login using any method of choice.
- SSO is also enforced by the organization. This means that all users that match the domain must be a part of the organization to login.
  - This also means that all members in the organization must match one of your SSO domains. Before turning on SSO, all non-matching users must be removed from the organization.
- Accounts belong to the domain and organization. When SSO is enabled:
  - Users cannot create additional organizations or subscriptions.
  - Accounts cannot self-leave the organization 
  - Users cannot change their account email or password.
  - Existing accounts that already have additional organizations or subscriptions will still have them.
  - Existing accounts cannot access their additional organizations or subscriptions until they can login using SSO and are a part of the organization.

### Just-in-time provisioning (JIT)

You can enable JIT on [gitkraken.dev/settings/sso](gitkraken.dev/settings/sso). With JIT enabled, when a user logs in with SSO successfully and is not part of your organization, they will automatically join your organization and consume a license. You do need to have spare licenses available for this to work, if all licenses are used then the user will not join automatically even if JIT is on.

### SSO login experience

- To login with SSO, click “SSO” on the login page.
- When a user that belongs to your domain logs in using anything but SSO, they will see a message explaining they need to login using SSO.
- When a user logs in using SSO successfully but is not a part of the organization, they will receive a message telling them to contact their admin to join the GitKraken organization.
- The owner and admins of the organization can log in using any method.

***

## Setup SSO

- Login to [gitkraken.dev](gitkraken.dev).
  - Login as an owner or admin.
  - Navigate the left sidebar to [Settings], then [Single sign-on].
- Click [Setup SSO].
  - If you have created SSO connections before then you should see a table of connections. If you would prefer to follow along from a blank state, delete all connections in the table.
- Fill out the form to create your first connection.
  - Connection name: this is to name the connection that will be shown to your users throughout GitKraken.
  - Domain: it’s best to add the domain in a basic form (e.g. gitkraken.com).
  - Identity URL: you need to copy and paste this into your identity provider to set up the integration.
  - Credentials: select the method of choice from Metadata URL, Metadata (raw), or Certificate. Copy it from your IdP and paste it in the textbox(es).
  - Once it is all filled out, click [Create Connection].
- Verify domain ownership.
  - Copy the TXT record shown on GitKraken.
  - Login to your DNS server.
  - Create a new record on the DNS server by pasting the TXT record in and saving it.
  - Return to GitKraken and click [Verify Ownership].
  - NOTE: it can take minutes or hours for the new record to reflect, depending on your DNS server.
- Add additional domains (optional).
  - If you have more than one domain present for your user base on GitKraken, then add additional domains before continuing to step 6 by clicking [Add Connection] and repeating steps 3 and 4 above.
- Enable SSO
  - Make sure the connections in the table are all enabled (if you see [Disable] in the table, that means the connection is enabled).
  - Turn on the [Enable SSO] switch at the top of the dashboard.
  - (Possible) Enabling SSO requires all members of the organization to match one of your domains. You might see a pop up that shows all the users that don’t match. You can remove them all here to continue or click [Cancel] and add additional domains before continuing (see step 5).
  - (Possible) Enabling SSO means that all users that match your SSO domains can no longer login until they join your organization. When enabling SSO a pop up may show all GitKraken accounts that belong to your domains but are not a part of the organization. Here you can choose which accounts to add to your organization. The ones you don’t add will not be able to login until you add them. If you are missing a domain, you can click [Cancel] and add additional domains before continuing (see step 5).
  - (Optional) turn on JIT to allow additional users to join the organization when they sign in with SSO (requires spare seats).

SSO should now be enabled and enforced across GitKraken for your domains! Be sure to test it. If you encounter issues this article doesn’t address, contact GitKraken support for more help.

*** 

## Example Identity Provider (IdP) setup instructions

<div class='callout callout--warning'>
    <p><strong>Note:</strong> These are example instructions to help you with Identity Provider setup. In most cases all you will need from us is the callback URL: https://api.gitkraken.com/oauth/sso/callback. If you need assistance please contact your IdP administrator or consult the IdP documentation for help.</p>
</div>

### G Suite

How to Create SAML Application in G Suite:

1. Go to https://admin.google.com/ 

2. Click on *Apps* and then *Web and mobile apps*.

<img src="/wp-content/uploads/sso-example-idp-1.jpg" class="img-bordered img-responsive center">

3. Click on *Add app*. 

<img src="/wp-content/uploads/sso-example-idp-2.jpg" class="img-bordered img-responsive center">

4. Click *Add custom SAML app*.

<img src="/wp-content/uploads/sso-example-idp-3.jpg" class="img-bordered img-responsive center">

5. Type in your app name (such as GitKraken SSO).

<img src="/wp-content/uploads/sso-example-idp-4.jpg" class="img-bordered img-responsive center">

6. Copy your *SSO URL* and *Certificate*.

<img src="/wp-content/uploads/sso-example-idp-5.jpg" class="img-bordered img-responsive center">

7. Enter the callback URL `https://api.gitkraken.com/oauth/sso/callback` for *ACS URL* and *Entity ID*.

<img src="/wp-content/uploads/sso-example-idp-6-1.jpg" class="img-bordered img-responsive center">

8. Add desired attributes and click on *Finish*.

<img src="/wp-content/uploads/sso-example-idp-7.jpg" class="img-bordered img-responsive center">

9. Click on *TEST SAML LOGIN*.

<img src="/wp-content/uploads/sso-example-idp-8.jpg" class="img-bordered img-responsive center">

10. Click on *ALLOW ACCESS*.

<img src="/wp-content/uploads/sso-example-idp-9.jpg" class="img-bordered img-responsive center">

11. Select *ON for everyone* and save.

<img src="/wp-content/uploads/sso-example-idp-10.jpg" class="img-bordered img-responsive center">

Now you are all set to [setup your SSO on a GitKraken Organization](/gitkraken-desktop/single-sign-on/#setting-up-sso-on-a-gitkraken-organization)

### Azure Active Directory

How to create SAML application in Azure Active Directory:

1. In a browser, go to Azure login portal.
2. Enter your azure credentials and login.
3. Go to *Azure Active Directory* from search bar.
4. In the left menu click on *Enterprise applications*.

<img src="/wp-content/uploads/sso-azure-1.png" class="img-bordered img-responsive center">

5. Click on *New application* from the top of the page.

<img src="/wp-content/uploads/sso-azure-2.png" class="img-bordered img-responsive center">

6. Select *Create your own application*. 

<img src="/wp-content/uploads/sso-azure-3.png" class="img-bordered img-responsive center">

7. Give your application name (such as "GitKraken SSO") and select "Integrate any other application you don't find in the gallery (Non-gallery)".

<img src="/wp-content/uploads/sso-azure-4.png" class="img-bordered img-responsive center">

8. Select *Single sign-on* from the left sidebar and then choose *SAML*.

<img src="/wp-content/uploads/sso-azure-5.png" class="img-bordered img-responsive center">

9. Click the edit icon in the top right corner to configure SAML.

<img src="/wp-content/uploads/sso-azure-6.png" class="img-bordered img-responsive center">

10.  Input the *Entity ID* URI and *Reply URL*. Both of these should direct to `https://api.gitkraken.com/oauth/sso/callback` for GitKraken SSO. 

<img src="/wp-content/uploads/sso-azure-7-1.png" class="img-bordered img-responsive center">

Now you are all set to [setup your SSO on a GitKraken Organization](/gitkraken-desktop/single-sign-on/#setting-up-sso-on-a-gitkraken-organization)
### Okta

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Logging through Okta Dashboard is not supported.</p>
</div>

How to Create SAML Application in Okta:

1. In a browser go to the Okta login page.
2. Enter your Okta credentials and login.
3. Go to admin dashboard and select *Applications* in navigation bar.

<img src="/wp-content/uploads/sso-okta-1.png" class="img-bordered img-responsive center">

4. Click on *Add Application*.  
5. Select *Create New App*. 

<img src="/wp-content/uploads/sso-okta-2.png" class="img-bordered img-responsive center">

6. Select *SAML 2.0* as a Sign on Method and click to next button.

<img src="/wp-content/uploads/sso-okta-3.png" class="img-bordered img-responsive center">

7. Enter a name of application (such as "GitKraken SSO").

<img src="/wp-content/uploads/sso-okta-4.png" class="img-bordered img-responsive center">

8. Configure SAML Integration. The *Single sign on URL* and *Audience URI* fields should direct to `https://api.gitkraken.com/oauth/sso/callback`.

<img src="/wp-content/uploads/sso-okta-5-1.png" class="img-bordered img-responsive center">

Step 9: Scroll down to the attribute statement and fill in the optional fields.

<img src="/wp-content/uploads/sso-okta-6.png" class="img-bordered img-responsive center">

Step 10: Select “I am an Okta customer adding an internal app” from option menu and then click to finish.

<img src="/wp-content/uploads/sso-okta-7.png" class="img-bordered img-responsive center">

Now you are all set to [setup your SSO on a GitKraken Organization](/gitkraken-desktop/single-sign-on/#setting-up-sso-on-a-gitkraken-organization)

### Ping Identity

How to Create SAML Application in Ping Identity

1. Go to https://www.pingidentity.com/en/account/sign-on.html

2. Create an account or sign in your existing one.

3. Go to the home page and click on *Add Environment*.

<img src="/wp-content/uploads/sso-pingidentity-3.png" class="img-bordered img-responsive center">

4. Select the appropriate solution based on your need (in this guide, we use *Customer solution*) and click *Next*.

<img src="/wp-content/uploads/sso-pingidentity-4.png" class="img-bordered img-responsive center">

5.	Select *PingOne SSO*, then click *Next*.

<img src="/wp-content/uploads/sso-pingidentity-5.png" class="img-bordered img-responsive center">

6.	Type in your environment name (in *TRIAL ENVIRONMENT NAME*), then click *Finish*. Now your environment is created. Go ahead and click on it.

<img src="/wp-content/uploads/sso-pingidentity-6.png" class="img-bordered img-responsive center">
<img src="/wp-content/uploads/sso-pingidentity-6-2.png" class="img-bordered img-responsive center">

7.	Select Identities to add some users. Once you are done adding them click on Groups, and then click on the plus button to add a group. (Make sure to add users with their email addresses).

<img src="/wp-content/uploads/sso-pingidentity-7.png" class="img-bordered img-responsive center">
<img src="/wp-content/uploads/sso-pingidentity-7-2.png" class="img-bordered img-responsive center">

8.	Select *Groups*, then click on the plus button to add a group. Once you have that, you can add the users to your group.

<img src="/wp-content/uploads/sso-pingidentity-8.png" class="img-bordered img-responsive center">

9.	Select *Connections*.

<img src="/wp-content/uploads/sso-pingidentity-9.png" class="img-bordered img-responsive center">

10.	Click on the plus button.

<img src="/wp-content/uploads/sso-pingidentity-10.png" class="img-bordered img-responsive center">

11.	Enter a name for your application, then select *SAML Application*. Next click on the *Configure* button which appears once you select your application type.

<img src="/wp-content/uploads/sso-pingidentity-11.png" class="img-bordered img-responsive center">

12.	Select *Manually Enter*. Type in the URL for *ACS URLs* and *Entity ID*, then click on *Save*.
(URL: `https://api.gitkraken.com/oauth/sso/callback`)


<img src="/wp-content/uploads/sso-pingidentity-12.png" class="img-bordered img-responsive center">

13.	Click on the toggle button so the users would have access to your application.

<img src="/wp-content/uploads/sso-pingidentity-13.png" class="img-bordered img-responsive center">

14.	Click on *Attributes* then add email as your new attribute.

<img src="/wp-content/uploads/sso-pingidentity-14.png" class="img-bordered img-responsive center">
<img src="/wp-content/uploads/sso-pingidentity-14-2.png" class="img-bordered img-responsive center">

15. Time to add the group we created in Step 8.

<img src="/wp-content/uploads/sso-pingidentity-15.png" class="img-bordered img-responsive center">

16.	Select the pencil icon pictured below.

<img src="/wp-content/uploads/sso-pingidentity-16.png" class="img-bordered img-responsive center">

17.	Click on the plus icon to add the group, then click on *Save*.

<img src="/wp-content/uploads/sso-pingidentity-17.png" class="img-bordered img-responsive center">
<img src="/wp-content/uploads/sso-pingidentity-17-2.png" class="img-bordered img-responsive center">

18.	Go to the *Configuration* tab to copy your *IDP Metadata URL* and download your metadata (*Download Metadata* button).

<img src="/wp-content/uploads/sso-pingidentity-18.png" class="img-bordered img-responsive center">

19.	Log into [gitkraken.dev/settings/sso](https://gitkraken.dev/settings/sso) and select "Setup SSO". Type in your Connection name and Domain. 

20.	Then use the *IDP Metadata URL* and *Metadata* from step 18 for *Metadata URL* and *Metadata*. Click on *Create Connection*

<img src="/wp-content/uploads/gkd-ping-identity-sso-connect.png" class="img-bordered img-responsive center">

21.	Now the users who were added in step 7 can *Sign in with SSO*.

