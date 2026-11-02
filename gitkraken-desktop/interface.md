---
title: GitKraken Desktop Interface Guide | Toolbar, Panels, and Graph
description: Learn the GitKraken Desktop interface, including the toolbar, Left Panel, Commit Panel, and Commit Graph, where your work and coding agent work appear together.
product: GitKraken Desktop
feature: Interface
content_type: overview
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-11
llms_include: true
tags: [interface, toolbar, left-panel, commit-graph, commit-panel, status-bar]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: November 2026</kbd>

Use this page to find your way around the main areas of the GitKraken Desktop interface: the toolbar, Left Panel, Commit Graph, Commit Panel, Status Bar, and tabs. Each area links to a task guide when you need the full steps.

**Requirements and limits**
- Scope: Interface overview, not full task-specific workflows
- Main areas: Toolbar, Left Panel, Commit Graph, Commit Panel, Status Bar, and tabs
- Repository context: Most of these controls appear only when a repository is open
- Left Panel modes: The Left Panel shows either List view or the Agents view
- Left Panel behavior: You can show, hide, resize, collapse, or expand its sections
- Toolbar behavior: Some buttons, such as LFS, appear only when the relevant feature or repository state is available
- Zoom: The status bar zoom selector offers 80%, 90%, 100%, 110%, 120%, 130%, 140%, 150%, 175%, 200%, 250%, and 300%. The <kbd>View</kbd> menu has **Increase Zoom**, **Decrease Zoom**, and **Reset Zoom**
- Detailed workflows: Follow the linked feature pages for the steps and limits of each task

***

## Quick Start


- **Left Panel**: Shows repository references, worktrees, and integrations. In `List | Agents`, click **List** for the traditional reference-based view or **Agents** for the Agents view, which organizes worktrees around coding agent sessions.
- **Commit Graph**: Displays the visual commit history of the current repository. Click any commit to view its details in the Commit Panel. Click the WIP node at the top to view and stage pending changes.
- **Commit Panel**: Shows file changes for the selected commit or WIP. Displays diffs, staged/unstaged files, and co-author information. Use it to stage files and write commit messages.
- **Toolbar**: At the top of the window. Has buttons for Undo, Redo, Pull, Push, Branch, Stash, and Pop. Use the adjacent dropdowns to customize pull behavior or branch options.
- **Status Bar**: At the bottom of the window. Shows the [Launchpad](/gitkraken-desktop/gitkraken-launchpad/) summary, your current plan, and a zoom selector with levels from 80% to 300%. You can also zoom from <kbd>View > Increase Zoom</kbd>, <kbd>View > Decrease Zoom</kbd>, and <kbd>View > Reset Zoom</kbd>, or with <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>=</kbd>, <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>-</kbd>, and <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>0</kbd>.

To open the Command Palette at any time, press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>P</kbd>. To toggle the Left Panel, use <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>J</kbd> or the toggle in the toolbar. To open Preferences and integrations, click the gear icon in the upper-right corner.

***

From left to right, GitKraken Desktop displays the Left Panel, Commit Graph, and Commit Panel when working with a repository. The Left Panel can show either List view or the Agents view.

<figure class='figure center'>
    <img alt="Simplified diagram of the GitKraken Desktop window, showing the Left Panel on the left, the Commit Graph in the center, and the Commit Panel on the right, with unlabeled callout lines." src="/wp-content/uploads/interface.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">GitKraken Desktop UI includes Left Panel, Commit Graph, and Commit Panel.</figcaption>
</figure>

## How the toolbar works

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/Xv9EAJqucOI?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

The main toolbar has buttons for common repository actions, including Undo, Redo, Pull, Push, and Branch.

### History actions

| Icon | Button | What it does |
| --- | --- | --- |
| <img alt="" src='/wp-content/uploads/gk-new-undo-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Undo** | The <kbd>Undo</kbd> button is active when you can undo an action. Click it to reverse the last undoable action. |
| <img alt="" src='/wp-content/uploads/gk-new-redo-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Redo** | Click <kbd>Redo</kbd> to reverse the last undo command. |

### Sync actions

| Icon | Button | What it does |
| --- | --- | --- |
| <img alt="" src='/wp-content/uploads/gk-new-pull-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Pull** | Click to pull changes from the remote repository. Use the adjacent dropdown to choose pull behavior: |
| <img alt="" src='/wp-content/uploads/gk-new-push-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Push** | Push changes to the upstream remote repository. |

* Fetch All
* Pull (fast-forward if possible)
* Pull (fast-forward only): same as `git fetch && git merge --ff-only`
* Pull (rebase): same as `git fetch && git rebase`

<div class='callout callout--basic'><p><strong>Tip:</strong> Click the <i class="fa fa-circle"></i> next to a pull type to make it the default. The selected default displays a <i class="fa fa-dot-circle"></i>.</p></div>

### Branch actions

| Icon | Button | What it does |
| --- | --- | --- |
| <img alt="" src='/wp-content/uploads/gk-new-branch-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Branch** | Create a new branch from your current HEAD. |

### Work-in-progress actions

| Icon | Button | What it does |
| --- | --- | --- |
| <img alt="" src='/wp-content/uploads/gk-new-stash-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Stash** | Save your changes in a stash without committing them. |
| <img alt="" src='/wp-content/uploads/gk-new-pop-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Pop Stash** | Restore changes from the most recent stash. |

### Conditional actions

| Icon | Button | What it does |
| --- | --- | --- |
| <img alt="" src='/wp-content/uploads/gk-lfs-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **LFS** | This button appears if <a href="/gitkraken-desktop/git-lfs/">LFS</a> is enabled for your repository. |

<div class='callout callout--basic'><p><strong>Note:</strong> To show labels under the toolbar icons, go to <kbd><strong>Preferences > UI Customization</strong></kbd> and enable <code>Show toolbar icon labels</code>.</p></div>

***

## How the Left Panel works

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/4uSXlUUU0ds?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

The Left Panel shows repository references, such as local branches, remotes, and tags. You can:

* Collapse or expand sections
* Resize the panel and sections
* Show or hide sections from the context menu
* Maximize a section by double-clicking its header

To switch the Left Panel mode, use the `List | Agents` segmented control at the top of the panel:

* Click **List** for the traditional reference-based view described below.
* Click **Agents** to open the **Agents view**, which organizes the same worktrees around coding agent sessions, status, and quick actions. See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/) for agent session setup and workflows.

To hide the segmented control, go to <kbd>Preferences > UI Customization</kbd>. For general worktree management, see [Manage Git Worktrees in GitKraken Desktop](/gitkraken-desktop/worktrees/).

<div class='callout callout--basic'>
    <p><strong>List view and the Agents view use the same underlying worktrees.</strong> Use List view for general branch and worktree management. Use the Agents view for coding agent sessions, agent status, and related quick actions.</p>
</div>

For in-app terminal behavior, worktree-specific terminal sessions, and manual coding agent workflows, see [GitKraken Terminal Guide](/gitkraken-desktop/terminal/).

<figure class='figure center'>
    <img src='/wp-content/uploads/left-panel-resize-and-collapse.gif' class="help-center-img img-bordered" alt="GitKraken Desktop Left Panel with repository branches and pull requests, with its sections being resized and collapsed.">
    <figcaption style="text-align: center; color: #888;">Resize, collapse, or expand any section of the Left Panel.</figcaption>
</figure>

| Icon | Section | What it does |
| --- | --- | --- |
| <img alt="" src='/wp-content/uploads/gk-new-local-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Local** | <p>References to local branches that point to specific commits.</p><p>For help with branches, see <a href="/working-with-repositories/branching-and-merging">Branching and Merging</a>.</p> |
| <img alt="" src='/wp-content/uploads/gk-new-remote-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Remote** | <p>References to remote branches.</p><p>For more information, see <a href="/working-with-repositories/pushing-and-pulling">Pushing and Pulling</a>.</p> |
| <img alt="" src='/wp-content/uploads/gk-new-pull-requests-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Pull Requests** | <p>Shows active pull requests for merging one branch into another.</p><p>With a supported integration, you can create pull requests directly from GitKraken Desktop. For more information, see <a href="/working-with-repositories/pull-requests">Pull Requests</a>.</p> |
| <i class="fa fa-list-ul" aria-hidden="true" style="display: inline-flex; align-items: center; justify-content: center; width: 36px; height: 36px; font-size: 36px;"></i> | **Issues** | <p>Shows issues connected to your repository integrations.</p><p>For more information, see <a href="/integrations/jira/">Jira</a>, <a href="/integrations/github-issues/">GitHub Issues</a>, <a href="/integrations/gitlab-issues/">GitLab Issues</a>, or <a href="/integrations/trello/">Trello</a>.</p> |
| <i class="fa fa-users" aria-hidden="true" style="display: inline-flex; align-items: center; justify-content: center; width: 36px; height: 36px; font-size: 36px;"></i> | **Teams** | <p>See what your <a href="/working-with-repositories/team-view/">Team</a> members are working on.</p> |
| <img alt="" src='/wp-content/uploads/gk-new-tags-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Tags** | <p>References that point to specific commits and do not move.</p><p>For more information, see <a href="/working-with-repositories/tags">Tags</a>.</p> |
| <img alt="" src='/wp-content/uploads/gk-new-stash-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Stashes** | <p>Stored file changes from the working copy.</p><p>For more information, see <a href="/working-with-commits/stashing">Stashing</a>.</p> |
| <img alt="" src='/wp-content/uploads//gk-new-submodules-icon.svg' class='img-responsive' style='width: 36px; height: 36px; object-fit: contain;'> | **Submodules** | <p>A Git repository in a subdirectory of the current repository.</p><p>For more information, see <a href="/working-with-repositories/submodules">Submodules</a>.</p> |

### How to filter the Left Panel

Type in the Left Panel **Filter** box, or press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>Option</kbd>/<kbd>Alt</kbd> + <kbd>F</kbd> to focus it. The Left Panel shows only the items whose names match what you type. The match does not need to be exact, so you can type part of a name.

To find a branch on a specific remote, start the filter with the remote name, followed by `/` or `:`, such as `origin/main` or `origin:main`. GitKraken Desktop adds that remote's matching branches to the results.


***
## How the Commit Panel works

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/ujgcCLBQvm0?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

Use the Commit Panel to stage and commit files and changes from your working directory.

<figure class='figure center'>
    <img src='/wp-content/uploads/commit-graph-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop commit panel showing commit graph, file changes, and metadata for staging and committing">
    <figcaption style="text-align: center; color: #888;">The Commit Panel displays file changes and commit metadata.</figcaption>
</figure>

The Commit Panel has 3 sections, in the order you use them:

1. _Unstaged Files_ - Modified files not yet added to the index.
2. _Staged Files_ - Files staged for the next commit.
3. _Commit Message_ - A message in 2 parts:
   * **Summary**: A brief, informative message shown in the graph.
   * **Description**: Additional details to support the summary.

<figure class='figure center'>
    <img src='/wp-content/uploads/color-guide-2025.png' class="help-center-img img-bordered" alt="Color-coded icons representing file changes: modified, added, deleted, and renamed">
    <figcaption style="text-align: center; color: #888;">Color indicators help distinguish file changes (e.g., renamed, deleted).</figcaption>
</figure>

For more about staging and committing, see [committing work](/working-with-commits/commits).

***

## How the Commit Graph works

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/YWGpKPMALOs?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

<figure class='figure center'>
    <img src='/wp-content/uploads/commit-graph-adjust-2025.gif' class="help-center-img img-bordered" alt="Animated Commit Graph in GitKraken Desktop being resized by dragging column dividers">
    <figcaption style="text-align: center; color: #888;">Resize the Commit Graph by dragging column dividers.</figcaption>
</figure>

The Commit Graph shows your repository's history as a graph of each commit and its relationships to other commits.

Each row is a commit, with the most recent at the top. Columns represent branches, and lines show merges and relationships.

Work from coding agents appears in the Commit Graph the same way. Each agent session runs on its own branch in its own worktree, with its own WIP node for pending changes. See [Coding Agents in GitKraken Desktop](/gitkraken-desktop/agents/).

<figure class='figure center'>
    <img src='/wp-content/uploads/graph-elements.png' class="help-center-img img-bordered" alt="Legend showing GitKraken Desktop graph elements including Commit, Merge Commit, WIP, Branches, and Stash Node">
    <figcaption style="text-align: center; color: #888;">Legend for interpreting commit history and branching paths.</figcaption>
</figure>

You can trace branch history from bottom to top and right to left.

### How ghost branches work

Hover over or select a commit to see its nearest containing branch ("ghost" branch). Double-click to check out its head.

<figure class='figure center'>
    <img src="/wp-content/uploads/ghost.gif" class="help-center-img img-bordered" alt="GitKraken Desktop showing ghost branches connecting commits to their nearest reference">
    <figcaption style="text-align: center; color: #888;">Ghost branches help locate a commit’s closest reference.</figcaption>
</figure>

### How commit highlighting works

Hovering over a branch highlights all related commits.

<figure class='figure center'>
    <img src="/wp-content/uploads/Commit-highlight.png" class="help-center-img img-bordered" alt="GitKraken Desktop showing faded unrelated commits while hovering over a branch named enterprise-rename">
    <figcaption style="text-align: center; color: #888;">Unrelated commits fade when a branch is hovered.</figcaption>
</figure>

To turn this behavior on or off, go to <kbd>Preferences > UI Customization</kbd> and select or clear **Highlight associated rows when hovering over a branch**.

***

## How tabs work

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/QWmjobrj0Qw?ecver=1" frameborder="0" allowfullscreen></iframe>
</div>

Switch between multiple repositories using tabs.

<figure class='figure center'>
    <img src='/wp-content/uploads/tabs-2025.gif' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing tabs being rearranged by drag-and-drop between repositories">
    <figcaption style="text-align: center; color: #888;">Rearrange tabs via drag-and-drop.</figcaption>
</figure>

To switch tabs, press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>1</kbd> to <kbd>9</kbd>. To open a new tab, click <kbd>+</kbd> or press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>T</kbd>. To close a tab, middle-click it or press <kbd>Cmd</kbd>/<kbd>Ctrl</kbd> + <kbd>W</kbd>.

Each [profile](/start-here/profiles/) keeps its own set of tabs.

<figure class='figure center'>
    <img src='/wp-content/uploads/profile-tabs-2025.gif' class="help-center-img img-bordered" alt="GitKraken Desktop interface showing repository tabs changing automatically when switching between user profiles">
    <figcaption style="text-align: center; color: #888;">Tabs adjust automatically when switching profiles.</figcaption>
</figure>

<figure class='figure center'>
    <img src='/wp-content/uploads/tab-drop-down-2025.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing dropdown menu with a list of all open repository tabs including Release Notes and support.gitkraken.com">
    <figcaption style="text-align: center; color: #888;">Dropdown icon displays all open repositories.</figcaption>
</figure>

<figure class='figure center'>
    <img alt="Hover to view file paths associated with open tabs" src='/wp-content/uploads/tab-hover-2025.png' class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Hover to view file paths associated with open tabs.</figcaption>
</figure>

### Worktree tab groups

When you open 2 or more tabs from the same repository, such as the main repository and its [worktrees](/gitkraken-desktop/worktrees/), GitKraken Desktop groups them together in the tab bar. A group has a border around its tabs and a dotted handle on its left edge.

- Drag the handle to move the whole group.
- Right-click the handle and select **Close group** to close every tab in the group.
- Right-click a tab in the group and select **Close group** or **Close others in group**.
- In the tabs dropdown, grouped tabs appear indented under the repository name.

A group ends when fewer than 2 of its tabs are open. To stop grouping worktree tabs, go to <kbd>Preferences > UI Customization</kbd> and clear **Automatically group worktree tabs together**.

<figure class='figure center'>
    <img alt="The GitKraken Desktop tab bar with a Launchpad tab and a tab group holding the Playground2026 repository tab and its login-form and readme-typo worktree tabs. The dotted group handle on the group's left edge is highlighted." src="/wp-content/uploads/gkd-worktree-tab-groups-01-v2@2x.png" class="help-center-img img-bordered">
    <figcaption style="text-align: center; color: #888;">Tabs for a repository and its worktrees are grouped together.</figcaption>
</figure>

### Tab alias and name

Right-click a tab and select <kbd>Alias repository</kbd> to assign a custom name.

<figure class='figure center'>
    <img src='/wp-content/uploads/repository-alias.png' class="help-center-img img-bordered" alt="GitKraken Desktop showing repository alias tooltip for support.gitkraken.com with file path preview">
    <figcaption style="text-align: center; color: #888;">Assign aliases to distinguish repositories in tabs.</figcaption>
</figure>

***

## Columns

GitKraken Desktop displays these default columns: <kbd>Branch/Tag</kbd>, <kbd>Graph</kbd>, and <kbd>Commit Message</kbd>. You can rearrange the columns.

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

GitKraken Desktop saves column selections, widths, and order for each repository. You can also configure columns from <kbd><strong>Preferences > UI Customization</strong></kbd>.

For more advanced views, see [Hiding and Soloing](/working-with-repositories/hiding-and-soloing).
