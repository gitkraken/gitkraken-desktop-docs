---

title: Detached HEAD state
description: Learn how to enter detached HEAD state to interact with commits without impact to other branches
taxonomy:
    category: gitkraken-desktop

---

Git power-users of GitKraken Desktop: rejoice! Entering detached HEAD state is just a right click away.

***
Detached HEAD state gives you the power to check out any commit and explore the older state of a repository without having to create a local branch. 

### Entering detached HEAD state

Right click on the commit you’d like to checkout, and navigate to <kbd><strong>Checkout this commit</strong></kbd>. 

<img src='/wp-content/uploads/checkout.png' srcset='/wp-content/uploads/checkout@2x.png 2x' class="help-center-img img-bordered">

The checked out commit will be tagged as `HEAD`, serving as your indication that you’ve entered detached HEAD state. 

<img src='/wp-content/uploads/head-tag.png' srcset='/wp-content/uploads/head-tag@2x.png 2x' class="help-center-img img-bordered">

You now have access to the full history of the commit. 

### Leaving detached HEAD state 

Feel free to stay a while; you can look around, make some experimental changes and commit them, all without impacting other branches. The commits you make in this state are “detached” from the rest of your project’s development - so when you’re ready to discard the commits you’ve made in this state, simply checkout a branch. 

When you check out a branch, the `HEAD` tag indicator will disappear and your repo will be business as usual. 

<img src='/wp-content/uploads/discard-commits.gif' class="help-center-img img-bordered">
 
<div class='callout callout--danger'>
    <p><strong>IMPORTANT:</strong> Any commits made in detached HEAD state will be lost when you check out any branch. 
</p>
</div>

Luckily, GitKraken Desktop will explicitly remind you of your detached state when you make a commit. You'll find this warning in at the top of the commit panel.

<img src='/wp-content/uploads/detached-warning.png' srcset='/wp-content/uploads/detached-warning@2x.png 2x' class="help-center-img img-bordered">

### Keeping your commits 

If you hit that stride and create changes in the detached HEAD state that you’d ultimately like to keep, you can easily do so by right clicking on your checked out commit and selecting <kbd><strong>Create branch here</strong></kbd>.

<img src='/wp-content/uploads/create-branch.png' srcset='/wp-content/uploads/create-branch@2x.png 2x' class="help-center-img img-bordered">

### Recovering lost commits

If you unintentionally checkout another branch, you can [Undo](https://support.gitkraken.com/working-with-commits/undo-and-redo/) to recover the commit. If you are unable to undo the change, these commits will still be tracked in the repository. Using the CLI, you can use [git reflog](https://git-scm.com/docs/git-reflog) to find the SHA of the missing commit and [git checkout <SHA\>](https://git-scm.com/docs/git-checkout) to checkout that commit.