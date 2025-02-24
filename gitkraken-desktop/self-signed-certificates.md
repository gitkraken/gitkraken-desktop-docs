---

title: Self-Signed Certificates
description: How to install a self-signed certificate that is recognized by GitKraken.
taxonomy:
    category: gitkraken-desktop

---

GitKraken's remote hosting platform integrations may require users to have a certificate in place. Follow the instructions below to add a certifiate to your local certificate store.

***

## Adding a Self-Signed Certificate

Self-signed certificates must be added to your trusted root directory before GitKraken will recognize the cert. This can be done through your operating system or in many browsers.

<div class='callout callout--basic'>
    <p><strong>Note:</strong> If you have the <a href="https://help.gitkraken.com/gitkraken-desktop/experimental-features/#git-executable">Git Executable</a> enabled, SSL settings in the global <code>.gitconfig</code> file are honored by GitKraken Desktop for actions performed by the Git executable.</p>
</div>

### Using Google Chrome on Windows

An easy way to install a certificate so that GitKraken can use it is via <a href='https://www.google.com/chrome/index.html' target='_blank'>Google Chrome</a>.

To generate a self-signed certificate, navigate to your remote hosting services web site. You should see somthing like this:

<img src="/wp-content/uploads/chrome-0a-export.png" srcset="/wp-content/uploads/chrome-0a-export.png" class="help-center-img img-bordered">

Click on the certificate, go to <kbd>Details</kbd> and click <kbd>Copy to File...</kbd> then follow the Certificate Export Wizard.

<img src="/wp-content/uploads/chrome-0b-export.png" srcset="/wp-content/uploads/chrome-0b-export.png" class="help-center-img img-bordered">

Once you have the certificate on your machine, in Chrome go to <kbd>Settings</kbd> from the <kbd><i class="fas fa-ellipsis-v"></i></kbd> menu in the top right.

<img src="/wp-content/uploads/chrome-1-settings.png" srcset="/wp-content/uploads/chrome-1-settings.png" class="help-center-img img-bordered">

Then navigate to <kbd><i> Privacy & Security   <i class='fa fa-caret-right'></i>     Security</i></kbd>:

<img src="/wp-content/uploads/chrome-2-security.png" srcset="/wp-content/uploads/chrome-2-security.png" class="help-center-img img-bordered">

Scroll down and then click <em>Manage certificates</em>. This will open a certificate import wizard dialog box, where you can click import. Follow the instructions in the wizard to browse to your certificate file and complete the installation.

<img src="/wp-content/uploads/chrome-3-manage-certs.png" srcset="/wp-content/uploads/chrome-3-manage-certs.png" class="help-center-img img-bordered">

Make sure to add the certificate to your trusted root certificates.
<img src="/wp-content/uploads/chrome-4-wizard.png" srcset="/wp-content/uploads/chrome-4-wizard.png" class="help-center-img img-bordered">


### Using Safari on Mac


Open Safari and browse to your remote hosting service.

<img src="/wp-content/uploads/safari-1a.png" srcset="/wp-content/uploads/safari-1a.png" class="help-center-img img-bordered">

Click to open cerificate window and view the certificate:

<img src="/wp-content/uploads/safari-1b.png" srcset="/wp-content/uploads/safari-1b.png" class="help-center-img img-bordered">

Hold down <kbd>Option</kbd> key and drag the certificate icon onto desktop. This should save the file with a `.pem` extension.

<img src="/wp-content/uploads/safari-2.png" srcset="/wp-content/uploads/safari-2.png" class="help-center-img img-bordered">

Now double click the file to open your mac keychains.

<img src="/wp-content/uploads/safari-4.png" srcset="/wp-content/uploads/safari-4.png" class="help-center-img img-bordered">

Locate the certificate in the **login** section.

<img src="/wp-content/uploads/safari-5-6.png" srcset="/wp-content/uploads/safari-5-6.png" class="help-center-img img-bordered">

Double click on the certificate to open the configuration window. In the first box, change the value to be *Always Trust*.

Finally, log out and back in again or restart your machine and the certifacte will be recognized.


### Using Chrome on Ubuntu Linux

Exporting the certificate onto your machine is very similar to the [Chrome instructions for Windows](/integrations/self-signed-certificates/#using-google-chrome-on-windows) above. However, after you have the certificate downloaded there are some commands required.

1. Open Google Chrome.
2. Navigate to the site affected by SSL issues.
3. Click the upper left <kbd>Not Secure</kbd> text, in the URL
4. Click the <kbd>Cerificate Is Not Valid</kbd> option
5. Click the <kbd>Details</kbd> tab
6. Click <kbd>Export...</kbd>
7. Save with a unique name (the below commands use `DOWNLOADED-CERT-NAME`), leave as <kbd>Base64-encoded ASCII, single certificate</kbd>
8. In a terminal, navigate to <kbd>Downloads</kbd>
9. Run  the following commands in the teminal:
```
openssl x509 -outform der -in DOWNLOADED-CERT-NAME -out DOWNLOADED-CERT-NAME.crt
```

```
certutil -d sql:$HOME/.pki/nssdb -A -t "CT,C,C" -n DOWNLOADED-CERT-NAME.crt -i DOWNLOADED-CERT-NAME.crt
```

Finally, run the following to verify it was added:
```
certutil -d sql:$HOME/.pki/nssdb -L
```

Now close Chrome completely and re-open. Navigate to the site to confirm that you are no longer recieving a certificate warning.

### Common certificate errors

Help, I am getting `Invalid SSL Certificate` errors!

<img src="/wp-content/uploads/invalid-error-2.png" srcset="/wp-content/uploads/invalid-error-2.png" class="help-center-img img-bordered">

This typically indicates that there is either an invalid certificate or no certificate detected. To ensure that GitKraken is able to use your certificate, follow the above instructions to [add a certificate](/integrations/self-signed-certificates/#adding-a-self-signed-certificate) to your local certificate store.


---

You may also recieve additional information about why the certificate is detected as invalid:

<img src="/wp-content/uploads/invalid-error-1.png" srcset="/wp-content/uploads/invalid-error-1.png" class="help-center-img img-bordered">

These will likely require the admin of the remote server to update the indicated field(s) and issue a new certificate. In this example a *Server Alternate Name (SAN)* is missing or incorrect.

---


### Operating system guides

Looking for another way to add a certificate? Use the below links to get pointed in the right direction for your operating system.

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

