---

title: Common Issues
description: Learn about common issues that you may encounter when using GitKraken Desktop.
taxonomy:
    category: gitkraken-desktop

---

***
### General Troubleshooting for GitKraken Desktop 9.4.0+

In 9.4.0, GitKraken introduced the experimental feature for the [Git Executable](/gitkraken-desktop/experimental-features/#git-executable). As this is currently an experimental feature that our team is continuing to improve on, you can try adjusting your use of the Git Executable.

Under `Preferences > Experimental`, first try adjusting the `Git Executable` version used. If you are using the “Bundled with GitKraken” version (comes pre-installed with GitKraken) try changing this to your own version of Git. If you do not have this installed, it can be downloaded [here](https://git-scm.com/download).

The reason this may help is because the Bundled version is a minimal install of Git, which does not include all features (specifically bash programs that may be used in Git Hooks).

<img src="/wp-content/uploads/gkc-git-executable-version.png" class="help-center-img img-bordered">

If using your own version does not resolve the issue, try unchecking `Use Git Executable`.

<img src="/wp-content/uploads/gkc-use-git-executable.png" class="help-center-img img-bordered">

If this does resolve your issue, it is very important to note that GitKraken Desktop is transitioning all actions to the Git Executable (from LibGit2/nodegit) and the Git Executable will become the exclusive way GitKraken Desktop performs Git operations in a future release.

As such, it is crucial for our team to be made aware of any issues related to using the Git Executable so we can look into and address them. Please reach out to our [support team](https://help.gitkraken.com/gitkraken-desktop/contact-support/) if you experience any issues with using this Experimental feature.

For more information on what this feature is and why it is being implimented, you can check out this [blog post](https://www.gitkraken.com/blog/gitkraken-client-migrating-from-libgit2-to-git-executable).

***

## Integration - 1000 Error (1002, 1003, 1005, 1007)
When attempting to connect to one of our integrations, you may see `Error 1002`, `Error 1003`, `Error 1005` or `Error 1007`.

<img src="/wp-content/uploads/error-1002.png" srcset="/wp-content/uploads/error-1002@2x.png 2x" class="help-center-img img-bordered">

### Solution:
These are general authentication errors.  First, verify you used the correct credentials then try one of the following potential solutions:

- If your credentials are correct, you can try signing out of the service in your default browser first, and then attempting the authentication from GitKraken Desktop again.

- Clear your browser cache, sign out of the git hosting service, then restart GitKraken Desktop and try again.

- If that is not working you can also try changing your operating system default browser to be a different browser. Once this is changed you can restart GitKraken Desktop and attempt to authenticate again.

If that still does not work, please contact our [support team](https://www.gitkraken.com/contact) and we can troubleshoot further.

 
***

## Error when pushing a branch
When attempting to push a branch, you may see the following `Push Failed: Cannot read property 'fullName' of undefined` error:

<img src="/wp-content/uploads/push-error.png" class="help-center-img img-bordered">

### Solution:
This usually indicates that there is a casing difference between the local branch and the upstream remote branch.  You can rename the local branch to match the casing of the upstream remote branch, which will allow you to push the changes.  

<div class='callout callout--warning'>
    <p>Note: You may need an intermediate name change to get the branch named correctly.  For example: Test-branch > temp-name > test-branch</p>
</div>

***

## Some branches or files not appearing - Capitalization issue

This most often occurs when having multiple remote banches nested together, but the capitalization differs. For example: `Feature/foo` and `feature/foo` may either be detected as the same branch OR a different branch depending on how your operating sytem treats capitalization. Most often this appears on Windows machines.

Symptoms:

- Branches not appearing in GitKraken - only one of the branches will be detected when they share a name. 
- This can also apply to files. If two files share the same name with only different capitalization one may appear deleted, moved, or not at all.
- This can also manifest as the file being staged but not showing as staged when running a `git status`.

To avoid these capitalization issues, we recommend giving each branch, file, and remote a unique name.

***

## Cannot log in - Cannot read property 'email' of null
When trying to log in, you may see the following error: `Cannot read property 'email' of null`. This is commonly related to a network issue such as a proxy, firewall, or security application. The most common occurrence is something like Zscaler.

### Solution:
If you have any of the above in place try the following:

- Sign in with GitHub authentication
- Approve the GitKraken application
- Continue as free with 0 days
- Click on free icon in bottom right, this brings up a web page inside GitKraken Desktop which authenticates against Zscaler
- Restart GitKraken Desktop and authenticate normally

This should allow you to log in without issue.

***

## Windows taskbar icon is not showing the GitKraken logo
Some Windows users are seeing the taskbar icon show incorrectly for GitKraken. This is due to the start menu shortcut moving from ``C:\\Users\\USER\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Axosoft, LLC`` to ``C:\\Users\\USER\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\GitKraken``. 

### Solution:
You can delete the old folder ``C:\\Users\\USER\\AppData\\Roaming\\Microsoft\\Windows\\Start Menu\\Programs\\Axosoft, LLC``, start GitKraken from the start menu, and then pin it to the taskbar again to resolve this.

## Why can't I see my GitHub remotes or repositories in the drop down menu? Why am I getting an error about GitHub organization permissions?

In order to work with with a repository owned by a GitHub organization with the GitHub integrtion connected, you need an organization to first allow access.

<img src="/wp-content/uploads/error.png" class="help-center-img img-bordered">

* First check to see if access is allowed to GitKraken from your profile's [GitHub Applications](https://github.com/settings/connections/applications/a7557949433b7d282a76)
* If access has been allowed, then the organization will need to allow [Organization Approval](https://help.github.com/articles/requesting-organization-approval-for-your-authorized-applications/)
* If you are attempting to use GitKraken with a repository owned by a different individual, consider forking their repository to use GitKraken for your changes. Otherwise this other individual will need to first [install GitKraken](/gitkraken-desktop/how-to-install/) and connect it to GitHub to authorize GitKraken.
* For details about third-party application restrictions view [Third-party apps list](https://help.github.com/articles/about-third-party-application-restrictions/)

***

## Problem executing Rust Socket Bridge

If you are seeing the following error message when trying to push/pull/clone/fetch:

<img src="/wp-content/uploads/gkd-10-4-rust-socket-bridge-error.png" class="help-center-img img-bordered">

This is typically caused by the Rust Socket Bridge executable being blocked by your system's security software.

### Solution

Contact your IT department to allow the Rust Socket Bridge executable to run (optimally with an exclusion rule for Gitkraken Desktop installation directory).










