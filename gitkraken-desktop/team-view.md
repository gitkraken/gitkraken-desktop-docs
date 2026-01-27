---
title: Team View in GitKraken Desktop
description: Learn how to use Team View in GitKraken Desktop to see branch activity, detect conflicts, and manage team visibility settings.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: January 2026</kbd>

The <i class="fas fa-users"></i> Team View allows you to see what branches and files members of your organization are currently working on. This is helpful for avoiding and collaborating on merge conflicts.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> Team View is only available for Advanced subscription tiers or higher. See the <a href="/start-here/teams/">Teams</a> page for more information on managing teams.</p>
</div>

***

## Select a Team

Select any team you're a member of from the Team dropdown. You can also choose a team for the repository in <kbd>Preferences > Team</kbd>, and optionally check <em>Use this as the default for all repositories</em>.

For each team member, Team View displays their checked-out branch and any files with local, uncommitted changes.

<figure>
  <img src="/wp-content/uploads/team-view-2025.png" srcset="/wp-content/uploads/team-view-2025@2x.png" class="help-center-img img-bordered" alt="Team View showing branches and files with changes">
  <figcaption style="text-align:center; color:#888">See teammates' active branches and modified files</figcaption>
</figure>

Lines added by a teammate appear in <span style="color: green;">green</span>, and removed lines in <span style="color: red;">red</span>. If you and a teammate have local changes in the same file, GitKraken displays an <i class="fas fa-exclamation-triangle" style="color:orange"></i> icon to signal a potential conflict.

<figure>
  <img src="/wp-content/uploads/team-view-conflict-2025.png" srcset="/wp-content/uploads/team-view-conflict-2025@2x.png" class="help-center-img img-bordered" alt="Warning icon on file with overlapping edits">
  <figcaption style="text-align:center; color:#888">Potential conflict warning icon on a file</figcaption>
</figure>

Learn more about [how to create a team](/start-here/teams/).

***

## Status Indicators

The <i class="fas fa-circle" style="color:green"></i> **status** icon appears on team member avatars to show who is currently active in GitKraken Desktop. This indicator is visible in both the Team View and the Organization section of Preferences.

<figure>
  <img src="/wp-content/uploads/status-in-teams.png" class="help-center-img img-bordered" alt="Avatars with status circles in Team View">
  <figcaption style="text-align:center; color:#888">Status icons display user activity</figcaption>
</figure>

Users can set their own status to “Active” or “Away” from the circle icon in the top-right corner or via the <kbd>Profile/Account</kbd> menu.

<figure>
  <img src="/wp-content/uploads/active-away-2025.png" srcset="/wp-content/uploads/active-away-2025@2x.png" class="help-center-img img-bordered" alt="Status toggle in Profile dropdown">
  <figcaption style="text-align:center; color:#888">Manually set your status as Active or Away</figcaption>
</figure>

***

## Opt Out of Team View

You can opt out of team sharing by disabling <em>Share work-in-progress status with my team</em> in <kbd>Preferences > General</kbd>.

<figure>
  <img src="/wp-content/uploads/team-setting.png" srcset="/wp-content/uploads/team-setting@2x.png" class="help-center-img img-bordered" alt="Setting to disable team sharing">
  <figcaption style="text-align:center; color:#888">Disable sharing work-in-progress status</figcaption>
</figure>

***

## More Team Features

Take advantage of these additional collaboration tools:

- [Group users](/gitkraken-desktop/teams/) – Create and manage teams in your GitKraken organization.
- [Share a Workspace](/workspaces/#create-a-cloud-workspace) – Manage and collaborate across repositories. <em>Pro plan and above</em>.
- [Share a Cloud Patch](experimental-features/#elementor-toc__heading-anchor-3) – Send a patch file to teammates securely.
