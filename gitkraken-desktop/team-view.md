---
title: Team View in GitKraken Desktop
description: Learn how to use Team View in GitKraken Desktop to see branch activity, detect conflicts, and manage team visibility settings.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to monitor what teammates are currently working on in GitKraken Desktop so you can spot overlapping edits and potential conflicts earlier. Team View shows each teammate’s checked-out branch, local file changes, and activity status, and it is available on Advanced subscription tiers or higher.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Team View is only available for Advanced subscription tiers or higher. See the <a href="/start-here/teams/">Teams</a> page for more information on managing teams.</p>
</div>

**Requirements and limits**
- Plan: Advanced subscription tier or higher
- Team requirement: You must belong to a team and select it in <kbd>Preferences &gt; Team</kbd>
- Shared data: Checked-out branch, local file changes, and activity status
- Conflict signal: Team View highlights overlapping local changes with an orange warning icon
- Privacy control: Disable **Share work-in-progress status with my team** to opt out
- Status scope: Users can set themselves to Active or Away; this affects what teammates see

***

## Quick Start

Use Team View in GitKraken Desktop to monitor teammate activity and detect potential merge conflicts before they occur.

**To enable Team View:**
1. Go to <kbd>Preferences > Team</kbd> and select a team from the dropdown.
2. Optionally check **Use this as the default for all repositories** to persist the selection.

**What Team View shows:**
- Each teammate's currently checked-out branch
- Files with local, uncommitted changes per team member
- Lines added by teammates appear in green; removed lines appear in red
- An orange warning icon appears on files where you and a teammate have overlapping local changes

**To set your status:** Click the circle icon in the top-right corner or use the Profile/Account menu to toggle between Active and Away.

**To stop sharing your work-in-progress:** Disable **Share work-in-progress status with my team** in <kbd>Preferences > General</kbd>.

Team View requires an Advanced plan or higher. Access it from the Team icon in the toolbar.

***

## How to select a team

Select any team you're a member of from the Team dropdown. You can also choose a team for the repository in <kbd>Preferences > Team</kbd>, and optionally check <em>Use this as the default for all repositories</em>.

<div class='callout callout--basic'>
  <p><strong>Use Team View when:</strong> you want early visibility into teammate activity and overlapping local changes in the same repository. <strong>Don't use it as your only coordination mechanism when:</strong> the work requires broader planning or decisions that still need direct team communication.</p>
</div>

For each team member, Team View displays their checked-out branch and any files with local, uncommitted changes.

<figure>
  <img src="/wp-content/uploads/team-view-2025@2x.png" class="help-center-img img-bordered" alt="Team View showing branches and files with changes">
  <figcaption style="text-align:center; color:#888">See teammates' active branches and modified files</figcaption>
</figure>

Lines added by a teammate appear in <span style="color: green;">green</span>, and removed lines in <span style="color: red;">red</span>. If you and a teammate have local changes in the same file, GitKraken displays an <i class="fas fa-exclamation-triangle" style="color:orange"></i> icon to signal a potential conflict.

<figure>
  <img src="/wp-content/uploads/team-view-conflict-2025@2x.png" class="help-center-img img-bordered" alt="Warning icon on file with overlapping edits">
  <figcaption style="text-align:center; color:#888">Potential conflict warning icon on a file</figcaption>
</figure>

Learn more about [how to create a team](/start-here/teams/).

***

## How status indicators work

The <i class="fas fa-circle" style="color:green"></i> **status** icon appears on team member avatars to show who is currently active in GitKraken Desktop. This indicator is visible in both the Team View and the Organization section of Preferences.

<div class='callout callout--basic'>
  <p><strong>Use status indicators when:</strong> you want a lightweight signal of who is active or away in GitKraken Desktop. <strong>Don't treat them as a full availability guarantee when:</strong> you need confirmation that someone is ready to respond or review work.</p>
</div>

<figure>
  <img src="/wp-content/uploads/status-in-teams.png" class="help-center-img img-bordered" alt="Avatars with status circles in Team View">
  <figcaption style="text-align:center; color:#888">Status icons display user activity</figcaption>
</figure>

Users can set their own status to “Active” or “Away” from the circle icon in the top-right corner or via the <kbd>Profile/Account</kbd> menu.

<figure>
  <img src="/wp-content/uploads/active-away-2025@2x.png" class="help-center-img img-bordered" alt="Status toggle in Profile dropdown">
  <figcaption style="text-align:center; color:#888">Manually set your status as Active or Away</figcaption>
</figure>

***

## How to opt out of Team View

You can opt out of team sharing by disabling <em>Share work-in-progress status with my team</em> in <kbd>Preferences > General</kbd>.

<div class='callout callout--basic'>
  <p><strong>Opt out when:</strong> you do not want to share work-in-progress status with your team from this machine or repository context. <strong>Don't opt out when:</strong> your team relies on Team View to spot conflicts early and coordinate overlapping work.</p>
</div>

<figure>
  <img src="/wp-content/uploads/team-setting@2x.png" class="help-center-img img-bordered" alt="Setting to disable team sharing">
  <figcaption style="text-align:center; color:#888">Disable sharing work-in-progress status</figcaption>
</figure>

***

## More team features

Take advantage of these additional collaboration tools:

- [Group users](/gitkraken-desktop/teams/) – Create and manage teams in your GitKraken organization.
- [Share a Workspace](/workspaces/#create-a-cloud-workspace) – Manage and collaborate across repositories. <em>Pro plan and above</em>.
- [Share a Cloud Patch](experimental-features/#elementor-toc__heading-anchor-3) – Send a patch file to teammates securely.
