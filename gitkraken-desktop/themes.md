
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
