---
title: Activity Logs 
description: Learn where to find feedback Activity Logs in GitKraken Desktop.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: May 2025</kbd>

Learn how to view all Git and application-level actions made in GitKraken Desktop using Activity Logs.

***

## What are Activity Logs?

The <kbd>Activity Logs</kbd> panel, located in the footer toolbar of GitKraken Desktop, provides real-time feedback on actions taken within the application and your repositories.

<figure>
  <img src='/wp-content/uploads/activity.gif' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Accessing Activity Logs from the footer toolbar</figcaption>
</figure>

Each log entry includes a timestamp, a description of the action, and performance data in milliseconds. The logs are stored in plain text and presented in a standard log format.

<figure>
  <img src='/wp-content/uploads/data-line.png' srcset='/wp-content/uploads/data-line@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Sample log line showing timestamp and performance data</figcaption>
</figure>

***

## Application Log

The **Application** tab in <kbd>Activity Logs</kbd> displays actions specific to the GitKraken Desktop instance. Events include:
- Creating a project
- Clearing SSH credentials
- Setting the global gitconfig

<figure>
  <img src='/wp-content/uploads/app-level.png' srcset='/wp-content/uploads/app-level@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Application tab showing GitKraken Desktop actions</figcaption>
</figure>

This log remains static regardless of which repository is currently open.

***

## Repository Log

The **Repository** tab displays Git operations performed on the currently active repository, such as:
- Fetch
- Push
- Merge

<figure>
  <img src='/wp-content/uploads/repository-level.png' srcset='/wp-content/uploads/repository-level@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Repository-level Git actions displayed in the log</figcaption>
</figure>

Repository logs only reflect actions from the active repo.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> For more detailed entries, go to <em>Preferences > General > Use extended logging in activity log</em>.</p>
</div>

Enabling extended logging adds more granularity, including details like Auto-fetch activity.

<figure>
  <img src='/wp-content/uploads/extended.png' srcset='/wp-content/uploads/extended@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Extended logging shows additional Git operations</figcaption>
</figure>

***

## Git Hook Log

If you use <a href="/working-with-repositories/githooks/">Git hooks</a>, the *Repository* tab will display hook activity such as:
- Success messages
- Warnings and failures
- Errors

<figure>
  <img src='/wp-content/uploads/githook-log.gif' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Git hook activity displayed in the log</figcaption>
</figure>

This provides context for events, making it easier to troubleshoot issues.

Additionally, you can open the Git hook log directly from the snackbox notification if a hook-related error occurs.

<figure>
  <img src='/wp-content/uploads/snackbox-error.png' srcset='/wp-content/uploads/snackbox-error@2x.png' class="help-center-img img-bordered">
  <figcaption style="text-align:center; color:#888">Error snackbox linking to Git hook log</figcaption>
</figure>
