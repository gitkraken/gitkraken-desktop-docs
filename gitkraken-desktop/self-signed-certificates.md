---
title: Installing Self-Signed Certificates for GitKraken Desktop
description: Learn how to install a self-signed SSL certificate so GitKraken Desktop can recognize it. Follow step-by-step guides for Windows, macOS, and Linux.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

GitKraken's remote hosting platform integrations may require users to have a certificate in place. Follow the instructions below to add a certificate to your local certificate store.

***

## Adding a Self-Signed Certificate

Self-signed certificates must be added to your trusted root directory before GitKraken will recognize the cert. This can be done through your operating system or in many browsers.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> If you have the <a href="https://help.gitkraken.com/gitkraken-desktop/experimental-features/#git-executable">Git Executable</a> enabled, SSL settings in the global <code>.gitconfig</code> file are honored by GitKraken Desktop for actions performed by the Git executable.</p>
</div>

### Using Google Chrome on Windows

An easy way to install a certificate so that GitKraken can use it is via <a href='https://www.google.com/chrome/index.html' target='_blank'>Google Chrome</a>.

To generate a self-signed certificate, navigate to your remote hosting service's website. You should see something like this:

<figure>
    <img src="/wp-content/uploads/chrome-0a-export.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Certificate view in Chrome with export option</figcaption>
</figure>

Click on the certificate, go to <kbd>Details</kbd>, click <kbd>Copy to File...</kbd>, and follow the Certificate Export Wizard.

<figure>
    <img src="/wp-content/uploads/chrome-0b-export.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Certificate export wizard in Chrome</figcaption>
</figure>

Open Chrome's <kbd>Settings</kbd> menu from the top-right <kbd><i class="fas fa-ellipsis-v"></i></kbd>.

<figure>
    <img src="/wp-content/uploads/chrome-1-settings.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Chrome settings menu</figcaption>
</figure>

Navigate to <kbd>Privacy & Security <i class='fa fa-caret-right'></i> Security</kbd>:

<figure>
    <img src="/wp-content/uploads/chrome-2-security.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Privacy & Security settings in Chrome</figcaption>
</figure>

Scroll down and click <em>Manage certificates</em>. Use the wizard to import the certificate.

<figure>
    <img src="/wp-content/uploads/chrome-3-manage-certs.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Certificate management dialog in Chrome</figcaption>
</figure>

Ensure that the certificate is added to your trusted root certificates.

<figure>
    <img src="/wp-content/uploads/chrome-4-wizard.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Wizard with trusted root option</figcaption>
</figure>

### Using Safari on Mac

Open Safari and navigate to your remote hosting service.

<figure>
    <img src="/wp-content/uploads/safari-1a.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Remote host with invalid certificate in Safari</figcaption>
</figure>

Click to open the certificate window:

<figure>
    <img src="/wp-content/uploads/safari-1b.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Certificate details window in Safari</figcaption>
</figure>

Hold down the <kbd>Option</kbd> key and drag the certificate icon to the desktop. This saves it as a `.pem` file.

<figure>
    <img src="/wp-content/uploads/safari-2.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Dragging certificate to save it as a .pem file</figcaption>
</figure>

Double-click the file to open your macOS Keychain.

<figure>
    <img src="/wp-content/uploads/safari-4.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">macOS Keychain interface</figcaption>
</figure>

Locate the certificate in the **login** section and double-click to configure.

<figure>
    <img src="/wp-content/uploads/safari-5-6.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Certificate settings in Keychain Access</figcaption>
</figure>

Set the trust level to *Always Trust*. Restart your computer to apply the changes.

### Using Chrome on Ubuntu Linux

Follow the same certificate export steps described in the [Windows section](/integrations/self-signed-certificates/#using-google-chrome-on-windows). Then:

1. Open a terminal and go to your <kbd>Downloads</kbd> folder.
2. Run the following commands:

```
openssl x509 -outform der -in DOWNLOADED-CERT-NAME -out DOWNLOADED-CERT-NAME.crt
```

```
certutil -d sql:$HOME/.pki/nssdb -A -t "CT,C,C" -n DOWNLOADED-CERT-NAME.crt -i DOWNLOADED-CERT-NAME.crt
```

3. Verify the certificate:

```
certutil -d sql:$HOME/.pki/nssdb -L
```

Close and reopen Chrome to confirm the certificate warning no longer appears.

### Common Certificate Errors

#### Error: `Invalid SSL Certificate`

<figure>
    <img src="/wp-content/uploads/invalid-error-2.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">GitKraken invalid SSL certificate warning</figcaption>
</figure>

This usually indicates the certificate is invalid or missing. [Add a certificate](/integrations/self-signed-certificates/#adding-a-self-signed-certificate) to your local store.

#### Additional Details

<figure>
    <img src="/wp-content/uploads/invalid-error-1.png" class="help-center-img img-bordered" style="max-width: 75%;">
    <figcaption style="text-align:center;color:#888">Detailed certificate error from GitKraken</figcaption>
</figure>

These errors often point to issues like a missing *Server Alternate Name (SAN)*. Contact your server administrator to fix and reissue the certificate.

### Operating System Guides

Use the links below for more help installing certificates by OS:

<table class='table table--bordered table--shortcuts'>
    <tbody>
        <tr>
            <td>Windows</td>
            <td><a href='https://docs.microsoft.com/en-us/skype-sdk/sdn/articles/installing-the-trusted-root-certificate' target='_blank'>Microsoft Docs</a></td>
        </tr>
        <tr>
            <td>OSX</td>
            <td><a href='https://support.apple.com/guide/keychain-access/add-certificates-to-a-keychain-kyca2431/mac' target='_blank'>Apple Docs</a></td>
        </tr>
        <tr>
            <td>Linux</td>
            <td><a href='https://ubuntu.com/server/docs/security-certificates' target='_blank'>Ubuntu Docs</a></td>
        </tr>
    </tbody>
</table>
