---

title: Tags
description: Designating important points of the Git history. Creating Tags in GitKraken Desktop on commits is easy with the graph.
taxonomy:
    category: gitkraken-desktop

---

Tags <em class='context-menu'><img style='translate:rotate(180deg);height:1em;' src='/wp-content/uploads/gk-tag-icon.svg'></em> are pointers to a commit.  Some examples of these are for marking versions of your product or important changes.

***
### Adding tags

To create a new tag in GitKraken Desktop, right click on the commit you'd like to tag, and select <kbd>Create tag here</kbd> at the bottom.

<img src="/wp-content/uploads/add-tag.png" srcset="/wp-content/uploads/add-tag.png" class="help-center-img img-bordered">


Tags are created locally, but available for remotes by right clicking the tag and selecting to push the tag to the remote.

<img src="/wp-content/uploads/tag-remote.png" srcset="/wp-content/uploads/tag-remote.png" class="help-center-img img-bordered">

Double click a tag in the left panel to jump to when the tag was added.  Tags can also be hidden and soloed just like branches from the right click menu.

<img src="/wp-content/uploads/tag-right.png" srcset="/wp-content/uploads/tag-right.png" class="help-center-img img-bordered">

***

### Checkout a tag

While you cannot directly checkout a tag, right-click on a tag and choose the <kbd>Create branch here</kbd> to create and then immediately checkout the commit tied with the tag.

<img src="/wp-content/uploads/tag-branch.png" srcset="/wp-content/uploads/tag-branch@2x.png" class="help-center-img img-bordered">

Alternatively, consider using the [detached HEAD state](/working-with-commits/detached-head-state/) to checkout the commit directly.

***

### Moving tags
To move a tag to the branch HEAD, checkout the new branch, right click the tag, and select fast-forward.

If a tag cannot be fast-forwarded, you can delete and then add a new one.  Be sure to delete the tag on remote as well.

***

### Tag messages
Create annotated tags by right clicking a branch or commit and selecting <kbd>Create annotated tag here</kbd>. You can annotate an existing tag by right clicking the tag and selecting <kbd>Annotate tag</kbd>. This message will be displayed when hovering over the tag in the left panel, or in the graph.

<img src="/wp-content/uploads/tag-annotation.png" srcset="/wp-content/uploads/tag-annotation.png" class="help-center-img img-bordered">

### Search or filter tags

You may filter tags from the filter bar in the left panel. Use this to quickly find a tag.

<img src="/wp-content/uploads/filter-tags.png" srcset="/wp-content/uploads/filter-tags@2x.png" class="help-center-img img-bordered">