---
title: GitKraken Desktop Themes | Customize Light, Dark & Custom UI
description: Learn how to switch between light and dark themes in GitKraken Desktop, sync with your system theme, and create custom themes using JSONC files.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: February 2026</kbd>

<figure>
  <div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/_TMprlLc740?ecver=1" frameborder="0" allowfullscreen></iframe>
  </div>
  <figcaption style="text-align:center; color:#888">Watch how to switch and create themes in GitKraken Desktop.</figcaption>
</figure>

***

## Quick Start

Change the GitKraken Desktop theme or create a custom theme to match your preferred visual style.

**To switch themes:** Go to <kbd>Preferences > UI Customization</kbd> and select a theme, or open the Command Palette and type `switch theme`.

**To sync with your system theme:** Enable the system theme sync option in <kbd>Preferences > UI Customization</kbd>. GitKraken Desktop will follow your OS light or dark setting when supported.

**To create a custom theme:**
1. Open <kbd>Preferences > UI Customization > Theme</kbd> and click the folder to navigate to `~/.gitkraken/themes/`.
2. Copy a `.jsonc-default` template file and rename it with a `.jsonc` extension.
3. Open the file in a text editor and set a unique `meta.name` and a `scheme` value of `light` or `dark`.
4. Save the file. Your custom theme appears in the theme list immediately. Changes take effect live without restarting GitKraken Desktop.

Custom themes have been disabled as of version 11.8.0 while the UI is being modernized. Built-in themes remain available.

***
<div class='callout callout--warning'>
<notice info>
  <p><strong>Note:</strong>Custom themes have been disabled in 11.8.0 as we modernize the UI for better performance and maintainability.</p>
</notice>
</div>

***
## Built-in Themes

To change your GitKraken Desktop theme:
- Go to <i class="fas fa-cog"></i> <em class='context-menu'>Preferences <i class='fa fa-caret-right'></i> UI Customization</em>
- Or open the <i class="fa fa-magic" style="transform: rotate(225deg)"></i> [Command Palette](/start-here/command-palette/) and type `switch theme`

<figure>
  <img src="/wp-content/uploads/theme-switch.gif" class="help-center-img img-bordered" alt="Switching GitKraken Desktop themes using Command Palette">
  <figcaption style="text-align:center; color:#888">Switch themes from the Command Palette.</figcaption>
</figure>

### Sync with System Theme

If your OS supports theme switching, GitKraken Desktop can follow your system’s light/dark setting. Enable this from <kbd>Preferences > UI Customization</kbd>.

***

## Custom Themes

GitKraken Desktop supports user-defined themes. To create a custom theme:

### Locate Theme Files

Theme files live in:
```
~/.gitkraken/themes/
```
You can open this folder from <kbd>Preferences > UI Customization > Theme</kbd>. Each `.jsonc-default` file is a template.

### Create Your Custom Theme

1. Copy a `.jsonc-default` file you want to base your theme on.
2. Rename the file (e.g., `MyCustomTheme.jsonc`).
3. Open it in a text editor.
4. Set a unique value for `meta.name`. This is the theme name shown in GitKraken.
5. Define your theme’s `scheme` as either `light` or `dark`.
6. Save your file and return to GitKraken.

Your custom theme will appear under <kbd>Preferences > UI Customization > Theme</kbd>.

### Live Theme Editing

Changes to your theme file take effect immediately—no need to restart GitKraken. If the file contains invalid syntax, GitKraken will revert to the default dark theme.

<div class='callout callout--basic'>
  <p><strong>Note:</strong> Theme files must follow correct JSONC formatting. Invalid files will be skipped and replaced by the default theme until corrected.</p>
</div>

***

## Supported Functions

### CSS Functions
GitKraken supports these CSS functions:
- `calc`
- `hsl` / `hsla`
- `max`, `min`
- `rgb` / `rgba`
- `var`

See [CSS functions](https://www.w3schools.com/cssref/css_functions.asp) for reference.

### LESS Functions
Supported LESS functions include:
- `darken`, `lighten`, `fade`
- `saturate`, `desaturate`
- `mix`, `mixLess`

See [LESS functions](https://lesscss.org/functions) for full documentation.

***

## Community Themes 

Looking for inspiration? Some users share their custom themes online, such as the collection at [jonbunator.github.io/gitkraken-custom-themes](https://jonbunator.github.io/gitkraken-custom-themes). 

Please note that this site is not affiliated with GitKraken, and we do not provide support for external or user-generated themes.

<style>
pre{position:relative}
.copy-btn{position:absolute;top:8px;right:8px;display:flex;align-items:center;justify-content:center;width:28px;height:28px;padding:0;background:rgba(128,128,128,.12);border:1px solid rgba(128,128,128,.2);border-radius:4px;cursor:pointer;color:#999;opacity:0;transition:opacity .15s,background .15s,color .15s}
pre:hover .copy-btn{opacity:1}
.copy-btn:hover{background:rgba(128,128,128,.25);color:#555}
.copy-btn.copied{color:#22c55e;border-color:rgba(34,197,94,.3)}
</style>
<script>(function(){var C='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="9" y="9" width="13" height="13" rx="2" ry="2"></rect><path d="M5 15H4a2 2 0 0 1-2-2V4a2 2 0 0 1 2 2v1"></path></svg>',K='<svg xmlns="http://www.w3.org/2000/svg" width="14" height="14" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><polyline points="20 6 9 17 4 12"></polyline></svg>';function cp(t){if(navigator.clipboard&&window.isSecureContext)return navigator.clipboard.writeText(t);var x=document.createElement('textarea');x.value=t;x.style.cssText='position:fixed;opacity:0';document.body.appendChild(x);x.select();try{document.execCommand('copy')}catch(e){}document.body.removeChild(x);return Promise.resolve()}function init(){document.querySelectorAll('pre').forEach(function(p){if(p.querySelector('.copy-btn'))return;var b=document.createElement('button');b.className='copy-btn';b.setAttribute('aria-label','Copy code');b.innerHTML=C;p.appendChild(b);b.addEventListener('click',function(){var el=p.querySelector('code')||p;cp(el.innerText.replace(/\n$/,'')).then(function(){b.innerHTML=K;b.classList.add('copied');setTimeout(function(){b.innerHTML=C;b.classList.remove('copied')},2000)})})})}document.readyState==='loading'?document.addEventListener('DOMContentLoaded',init):init()})()</script>
