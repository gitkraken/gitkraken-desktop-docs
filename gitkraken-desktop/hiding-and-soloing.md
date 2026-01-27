---
title: Hide and Solo Branches in GitKraken Desktop
description: Learn how to reduce visual clutter in GitKraken Desktop by hiding or soloing branches, tags, remotes, and stashes from the Left Panel.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

The Left Panel lets you control the Commit Graph view for better focus. Use _Hide_ to temporarily remove references, or _Solo_ to spotlight specific branches.

***

<figure class='figure center'>
  <img src="/wp-content/uploads/solo-hide.gif" class="help-center-img img-bordered" alt="Animated demonstration of soloing and hiding branches in GitKraken Desktop's Left Panel">
  <figcaption style="text-align: center; color: #888;">Animation demonstrating hiding and soloing branches from the Left Panel.</figcaption>
</figure>

<div class="flex-wrap" style="align-items: flex-start">
  <div class="flex-item">
    <img src="/wp-content/uploads/gk-hide-icon-green.svg" class='img-responsive' style="width: 70px; height: 70px">
  </div>
  <div class="flex-item">
    <h3>Hide</h3>
    <p>Hiding a branch removes it from the Commit Graph view without affecting your repository.</p>
    <p>To hide a branch, hover over it in the Left Panel and click the <i class='fa fa-eye icon-green'></i> icon that appears. Or right-click the branch and select <kbd>Hide</kbd> from the context menu.</p>
    <p>Hidden branches are marked with a gray <i class='fa fa-eye-slash'></i> icon. Click the icon to show the branch again.</p>
  </div>
</div>

<div class="flex-wrap" style="align-items: flex-start">
  <div class="flex-item">
    <img src="/wp-content/uploads/gk-solo-icon-orange.svg" class='img-responsive' style="width: 70px; height: 70px">
  </div>
  <div class="flex-item">
    <h3>Solo</h3>
    <p>Soloing a branch hides all others that haven’t been explicitly soloed. This narrows your focus to selected references.</p>
    <p>Right-click a branch and select <kbd>Solo</kbd> to enter Solo Mode. Soloed branches display with an orange <i class='fa fa-dot-circle-o icon-orange'></i> icon.</p>
    <p>To solo or unsolo additional branches, click the semi-opaque icon beside each name.</p>
    <p>You can also hide or solo entire remotes to isolate just the few branches you need.</p>
  </div>
</div>

### Hide or Show All References

You can hide or show all **Remotes**, **Tags**, **Branches**, or **Stashes** from the Left Panel. Right-click the corresponding header to access bulk options.

<figure class='figure center'>
  <img src='/wp-content/uploads/hide-show-all.png' 
       srcset='/wp-content/uploads/hide-show-all@2x.png' 
       class="help-center-img img-bordered"
       alt="Context menu showing the 'Show all remotes' option after right-clicking the REMOTE section in GitKraken Desktop">
  <figcaption style="text-align: center; color: #888;">
    Right-click section headers to hide or show all references.
  </figcaption>
</figure>
