---
title: GitKraken Desktop Interface Guide | Toolbar, Panels, and Graph
description: Learn how to navigate the GitKraken Desktop interface. Explore the toolbar, Left Panel, Commit Panel, and Commit Graph with visual guides and tips.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

GitKraken Desktop's interface simplifies Git usage by providing a visual layout of core actions and repository elements.

***

From left to right, GitKraken Desktop displays a Left Panel, Commit Graph, and the Commit Panel when working with a repository.

<figure class='figure center'>
    <img src="/wp-content/uploads/interface.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">GitKraken Desktop UI includes Left Panel, Commit Graph, and Commit Panel.</figcaption>
</figure>

## Toolbar

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Xv9EAJqucOI?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

The main toolbar provides quick access to common repository actions, including Undo, Redo, Pull, Push, Branching, and more.

### Undo
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-undo-icon.svg' class='img-responsive'></div>
	<div class="flex-item">
		<p>If an action can be undone, the <kbd>Undo</kbd> button is activated. Click to reverse the last undoable action.</p>
	</div>
</div>

### Redo
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-redo-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>Click <kbd>Redo</kbd> to reverse the last undo command.</p>
	</div>
</div>

### Pull
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-pull-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>Click to pull changes from the remote repository. Use the adjacent dropdown to choose pull behavior:</p>
	</div>
</div>

* Fetch All
* Pull (fast-forward if possible)
* Pull (fast-forward only): same as `git fetch && git merge --ff-only`
* Pull (rebase): same as `git fetch && git rebase`

<div class='callout callout--basic'><p><strong>Tip:</strong> Click the <i class="fa fa-circle"></i> next to a pull type to make it the default. The selected default displays a <i class="fa fa-dot-circle"></i>.</p></div>

### Push
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-push-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>Push changes to the upstream remote repository.</p>
	</div>
</div>

### Branch
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-branch-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>Create a new branch from your current HEAD.</p>
	</div>
</div>

### Stash
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-stash-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>Temporarily save your changes without committing using a stash.</p>
	</div>
</div>

### Pop Stash
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-pop-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>Restore changes from the most recent stash.</p>
	</div>
</div>

### LFS
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-lfs-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>This button appears if <a href="/gitkraken-desktop/git-lfs/">LFS</a> is enabled for your repository.</p>
	</div>
</div>

<div class='callout callout--basic'><p><strong>Note:</strong> To toggle toolbar labels, go to <kbd><strong>Preferences > UI Preferences</strong></kbd> and enable <code>Show toolbar icon labels</code>.</p></div>

***

## Left Panel

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/4uSXlUUU0ds?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

The Left Panel provides access to repository references, such as local branches, remotes, and tags. You can:

* Collapse or expand sections
* Resize the panel and sections
* Toggle visibility via the context menu
* Maximize a section by double-clicking the header

<figure class='figure center'>
    <img src='/wp-content/uploads/left-panel-resize-and-collapse.gif' class="help-center-img img-bordered" alt="GitKraken interface showing left panel with repository branches and pull requests, highlighting resizing and collapsing sections">
    <figcaption style="text-align: center; color: #888;">Resize, collapse, or expand any section of the Left Panel.</figcaption>
</figure>

<h3>Local</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-local-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>References to local branches &mdash; pointers to specific commits allowing work to be separated.</p>
		<p>If you need help with branches, visit our <a href="/working-with-repositories/branching-and-merging">Branching and Merging</a> page.</p>
	</div>
</div>


<h3>Remote</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-remote-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>References to remote branches.</p>
		<p>Set sail into <a href="/working-with-repositories/pushing-and-pulling">pushing and pulling remotes</a> for more.</p>
	</div>
</div>

<h3>Pull Requests</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-pull-requests-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>This shows active requests for merging one branch into another. With the GitHub or Bitbucket integration, new PRs can be created directly from GitKraken Desktop.</p>
		<p>Create your <a href="/working-with-repositories/pull-requests">Pull Request</a> to get your contribution merged.</p>
	</div>
</div>

<h3>Issues</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<i class="fa fa-list-ul fa-3x" aria-hidden="true"></i>
	</div>
	<div class="flex-item">
		<p>Lets you see and work with your issues in GitKraken Desktop</p>
		<p>Hook up to your remote issue tracker of choice - such as <a href="/integrations/jira/">Jira</a>, <a href="/integrations/github-issues/">GitHub</a>, <a href="/integrations/gitlab-issues/">GitLab</a>, or <a href="/integrations/trello/">Trello</a>.</p>
	</div>
</div> 

<h3>Teams</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<i class="fa fa-users fa-3x" aria-hidden="true"></i>
	</div>
	<div class="flex-item">
		<p>Easily see what your <a href="/working-with-repositories/team-view/">Team</a> members are working on.</p>
	</div>
</div>

<h3>Tags</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-tags-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>These represent active pointers to commits but never move. <a href="/working-with-repositories/tags">Tag</a>, you're it!</p>
	</div>
</div>

<h3>Stashes</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads/gk-new-stash-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>Stored file changes in the working copy.</p>
		<p>For saving your loot to play with later, here's more on <a href="/working-with-commits/stashing">stashes</a>.</p>
	</div>
</div>


<h3>Submodules</h3>
<div class="flex-wrap">
	<div class="flex-item">
		<img src='/wp-content/uploads//gk-new-submodules-icon.svg' class='img-responsive'>
	</div>
	<div class="flex-item">
		<p>A Git repository in a subdirectory of the current repository.</p>
		<p>Git-inception with <a href="/working-with-repositories/submodules">submodules</a> anyone?</p>
	</div>
</div>


***

<!-- CONTENT ABOVE THIS LINE OMITTED FOR REVIEW -->

## Commit Panel

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ujgcCLBQvm0?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

The Commit Panel is where files and changes from your working directory are staged and committed.

<figure class='figure center'>
    <img src='/wp-content/uploads/commit-graph-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop commit panel showing commit graph, file changes, and metadata for staging and committing">
    <figcaption style="text-align: center; color: #888;">The Commit Panel displays file changes and commit metadata.</figcaption>
</figure>

The three sections in order of operations are:

1. _Unstaged Files_ — Modified files not yet added to the index.
2. _Staged Files_ — Files staged for the next commit.
3. _Commit Message_ — A two-part message interface:
   * **Summary**: A brief, informative message shown in the graph.
   * **Description**: Additional details to support the summary.

<figure class='figure center'>
    <img src='/wp-content/uploads/color-guide-2025.png' class="help-center-img img-bordered" alt="Color-coded icons representing file changes: modified, added, deleted, and renamed">
    <figcaption style="text-align: center; color: #888;">Color indicators help distinguish file changes (e.g., renamed, deleted).</figcaption>
</figure>

To explore more about staging and committing, visit [committing work](/working-with-commits/commits).

***

## Commit Graph

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/YWGpKPMALOs?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

<figure class='figure center'>
    <img src='/wp-content/uploads/commit-graph-adjust-2025.gif' class="help-center-img img-bordered" alt="Animated Commit Graph in GitKraken Desktop being resized by dragging column dividers">
    <figcaption style="text-align: center; color: #888;">Resize the Commit Graph by dragging column dividers.</figcaption>
</figure>

The Commit Graph is a visual representation of your repo’s Directed Acyclic Graph (DAG), showing each commit and its relationships.

Each row is a commit, with the most recent at the top. Columns represent branches; lines indicate merges and relationships.

<figure class='figure center'>
    <img src='/wp-content/uploads/graph-elements.png' class="help-center-img img-bordered" alt="Legend showing GitKraken Desktop graph elements including Commit, Merge Commit, WIP, Branches, and Stash Node">
    <figcaption style="text-align: center; color: #888;">Legend for interpreting commit history and branching paths.</figcaption>
</figure>

You can trace branch history from bottom to top and right to left.

### Ghost branches

Hover over or select a commit to see its nearest containing branch ("ghost" branch). Double-click to check out its head.

<figure class='figure center'>
    <img src="/wp-content/uploads/ghost.gif" class="help-center-img img-bordered" alt="GitKraken Desktop showing ghost branches connecting commits to their nearest reference">
    <figcaption style="text-align: center; color: #888;">Ghost branches help locate a commit’s closest reference.</figcaption>
</figure>

### Commit highlighting

Hovering over a branch highlights all related commits.

<figure class='figure center'>
    <img src="/wp-content/uploads/Commit-highlight.png" class="help-center-img img-bordered" alt="GitKraken Desktop showing faded unrelated commits while hovering over a branch named enterprise-rename">
    <figcaption style="text-align: center; color: #888;">Unrelated commits fade when a branch is hovered.</figcaption>
</figure>

Toggle this behavior from <kbd>Preferences > UI Customization</kbd>.

***

## Tabs

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/QWmjobrj0Qw?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

Switch between multiple repositories using tabs.

<figure class='figure center'>
    <img src='/wp-content/uploads/tabs-2025.gif' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing tabs being rearranged by drag-and-drop between repositories">
    <figcaption style="text-align: center; color: #888;">Rearrange tabs via drag-and-drop.</figcaption>
</figure>

Use shortcuts <kbd>cmd/ctrl</kbd>+<kbd>1-9</kbd> to switch tabs. Open new tabs with <kbd>+</kbd> or <kbd>cmd/ctrl</kbd>+<kbd>T</kbd>, and close tabs with middle-click or <kbd>cmd/ctrl</kbd>+<kbd>W</kbd>.

Tabs persist per [profile](/start-here/profiles/).

<figure class='figure center'>
    <img src='/wp-content/uploads/profile-tabs-2025.gif' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing repository tabs changing automatically when switching between user profiles">
    <figcaption style="text-align: center; color: #888;">Tabs adjust automatically when switching profiles.</figcaption>
</figure>

<figure class='figure center'>
    <img src='/wp-content/uploads/tab-drop-down-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing dropdown menu with a list of all open repository tabs including Release Notes and support.gitkraken.com">
    <figcaption style="text-align: center; color: #888;">Dropdown icon displays all open repositories.</figcaption>
</figure>

<figure class='figure center'>
    <img src='/wp-content/uploads/tab-hover-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Hover to view file paths associated with open tabs.</figcaption>
</figure>

### Tab alias and name

Right-click a tab and select <kbd>Alias repository</kbd> to assign a custom name.

<figure class='figure center'>
    <img src='/wp-content/uploads/repository-alias.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing repository alias tooltip for support.gitkraken.com with file path preview">
    <figcaption style="text-align: center; color: #888;">Assign aliases to distinguish repositories in tabs.</figcaption>
</figure>

***

## Columns

GitKraken Desktop displays these default columns: <kbd>Branch/Tag</kbd>, <kbd>Graph</kbd>, <kbd>Commit Message</kbd>. Columns are rearrangeable.

<figure class='figure center'>
    <img src='/wp-content/uploads/columns-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing branch, graph, and commit message columns with headers outlined for reordering.">
    <figcaption style="text-align: center; color: #888;">Drag column headers to reorder.</figcaption>
</figure>

Right-click headers to toggle columns like <kbd>Author</kbd>, <kbd>Date/Time</kbd>, or <kbd>Sha</kbd>. You can also use the gear icon.

<figure class='figure center'>
    <img src='/wp-content/uploads/customize-columns-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop column settings dropdown showing options to toggle Branch, Graph, Commit message, Author, Date/Time, and Sha columns.">
    <figcaption style="text-align: center; color: #888;">Enable/disable columns using header context menu.</figcaption>
</figure>

<figure class='figure center'>
    <img src='/wp-content/uploads/gear-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop column customization menu opened from gear icon, showing options to toggle visibility of various columns like Branch, Graph, Commit message, Author, Date/Time, and SHA.">
    <figcaption style="text-align: center; color: #888;">Customize columns using the gear icon menu.</figcaption>
</figure>

Filter commits by author via the <i class='fa fa-filter'></i> in the AUTHOR column.

<figure class='figure center'>
    <img src='/wp-content/uploads/filter-author@2x.png' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing filter dropdown to search commit graph by author or team, with options like Support, Marketing, and IT.">
    <figcaption style="text-align: center; color: #888;">Search and filter by commit author or team.</figcaption>
</figure>

GitKraken Desktop saves column selections, widths, and order per repo. Columns are also configurable from <kbd><strong>Preferences > UI Customization</strong></kbd>.

For more advanced views, see [Hiding and Soloing](/working-with-repositories/hiding-and-soloing).
