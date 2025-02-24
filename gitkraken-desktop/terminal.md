---

title: Terminal
description: A Git-enhanced terminal experience with GitKraken’s powerful visual Git commit graph
taxonomy:
    category: gitkraken-desktop

---

Open the Terminal to use Git CLI commands while still viewing the graph.

To get started open up a repository and click the Terminal <i class="fa fa-terminal" aria-hidden="true"></i> button in the toolbar or by searching for "terminal" in the <a href="/working-with-repositories/command-palette">command palette</a>.

<img src="/wp-content/uploads/open-gitkraken-terminal.gif" class="help-center-img img-bordered">


---

## Terminal Commands

### Git Commands and Auto-complete
Most <a href="https://git-scm.com/" target="_blank">Git</a> commands are supported and will appear in the Terminal's auto-complete suggestions, start typing `git` to see them.  

<img src="/wp-content/uploads/autocomplete-suggestions.png" class="help-center-img img-bordered">

Auto-complete suggestions will also appear for flags.

<img src="/wp-content/uploads/autocomplete-suggestions-flags.png" class="help-center-img img-bordered">

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Other auto-complete programs can cause the Terminal auto-complete suggestions to not work. You may need to uninstall or disable these programs before using the Terminal.</p>
</div>

---

### Terminal Preferences 

Navigate to <kbd><strong>Preferences > Terminal</strong></kbd> to change your Terminal preferences.

<img src="/wp-content/uploads/terminal-preferences.png" class="help-center-img img-bordered">

#### Setting the default terminal on Mac and Linux

ZSH and Bash are currently supported for Mac and Linux. To switch shells you'll need to set the new shell as default in your operating system settings and restart your computer for auto-complete to continue working as expected.

#### Setting the default terminal on Windows

PowerShell and Bash are currently supported for Windows. To switch shells, adjust the _Default Terminal_ under <em class='context-menu'>Preferences > Terminal</em>.