---
title: Installing Self-Signed Certificates for GitKraken Desktop
description: Learn how to install a self-signed SSL certificate so GitKraken Desktop can recognize it. Follow step-by-step guides for Windows, macOS, and Linux.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

GitKraken's remote hosting platform integrations may require users to have a certificate in place. Follow the instructions below to add a certificate to your local certificate store.

***

## Quick Start

Install a self-signed SSL certificate so GitKraken Desktop can connect to your remote hosting service.

**On Windows (Chrome):**
1. Navigate to your remote hosting service in Chrome and open the certificate details.
2. Export the certificate using the Certificate Export Wizard.
3. Open Chrome Settings, go to **Privacy and Security > Security**, and click **Manage certificates**.
4. Import the certificate and add it to the Trusted Root Certificates store.

**On macOS (Safari):**
1. Open Safari and navigate to your remote host.
2. Hold **Option** and drag the certificate icon to your desktop to save it as a `.pem` file.
3. Double-click the file to open Keychain Access.
4. Find the certificate in the login keychain, open it, and set trust to **Always Trust**.
5. Restart your computer.

**On Linux (Chrome/Ubuntu):**
1. Export the certificate using the steps from the Windows Chrome section.
2. Convert and install using `openssl` and `certutil` in the terminal.
3. Reopen Chrome to confirm the warning no longer appears.

If you have the Git Executable enabled, SSL settings in your global `.gitconfig` are also honored.

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

<style>
pre{position:relative;min-height:3em}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;width:28px;height:28px;padding:0;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s,width .15s,padding .15s}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3);width:auto;padding:0 8px;gap:4px}
</style>
<script>(function(){var C='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2 2v1"></path></svg>',K='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg><span style="font-size:11px;margin-left:4px;font-family:sans-serif">Copied!</span>';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p,cl=el.cloneNode(true),bn=cl.querySelector('.copy-btn');if(bn)bn.remove();cp((cl.innerText||cl.textContent).replace(/[\r\n]+$/, '')).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
