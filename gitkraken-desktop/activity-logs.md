---
title: View Activity Logs in GitKraken Desktop
description: Learn how to view real-time Git actions, application events, and Git hook feedback using Activity Logs in GitKraken Desktop.
product: GitKraken Desktop
feature: Activity Logs
content_type: troubleshooting
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [generic]
integrations: []
hosted_variant: both
status: GA
last_verified: 2026-03
llms_include: true
tags: [activity-logs, logs, troubleshooting, git-actions, hooks]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to inspect Activity Logs in GitKraken Desktop when you need to see recent Git operations, application events, performance timing, or Git hook output. It explains the difference between the Application and Repository tabs, how extended logging changes the output, and how hook failures surface in the log UI.

**Requirements and limits**
- Scope: Real-time GitKraken Desktop application and repository event logs
- Access point: <kbd>Activity Logs</kbd> icon in the footer toolbar
- Application tab: Shows GitKraken Desktop instance events and is not tied to the active repository
- Repository tab: Shows Git operations for the currently active repository only
- Extended logging: Enable in <kbd>Preferences &gt; General</kbd> for more detailed repository log output
- Hook log behavior: Git hook failures surface in the Repository log and through snackbox links to the hook output

***

## Quick Start


1. Open GitKraken Desktop and open any repository.
2. Click the <kbd>Activity Logs</kbd> icon in the footer toolbar at the bottom of the window.
3. Select the **Application** tab to view actions taken by GitKraken Desktop itself, such as opening repositories or refreshing the Git config.
4. Select the **Repository** tab to see Git operations performed on the current repository, such as fetch, push, and merge.
5. To include more detail in the Repository tab, go to <kbd>Preferences > General</kbd> and enable **Use extended logging in activity log**.
6. If a Git hook fails, a snackbox notification will appear with a link to the hook log. Click it to view the hook output directly.

Each log entry includes a timestamp, a description of the action, and duration in milliseconds. Logs are displayed in plain text format and update in real time as you work.

***

## What Activity Logs are

The <kbd>Activity Logs</kbd> panel, located in the footer toolbar of GitKraken Desktop, provides real-time feedback on actions taken within the application and your repositories.

<figure>
  <img src='/wp-content/uploads/activity.gif' class="help-center-img img-bordered" alt="User clicking the Activity Logs icon in the GitKraken Desktop footer to view repository events and actions">
  <figcaption style="text-align:center; color:#888">Accessing Activity Logs from the footer toolbar</figcaption>
</figure>

Each log entry includes a timestamp, a description of the action, and performance data in milliseconds. The logs are stored in plain text and presented in a standard log format.

<figure>
  <img src='/wp-content/uploads/data-line@2x.png' class="help-center-img img-bordered" alt="Activity log entry showing a commit message being amended with timestamp and duration in milliseconds">
  <figcaption style="text-align:center; color:#888">Sample log line showing timestamp and performance data</figcaption>
</figure>

***

## How the Application log works

The **Application** tab in <kbd>Activity Logs</kbd> displays actions specific to the GitKraken Desktop instance. Events include:
- Creating a project
- Clearing SSH credentials
- Setting the global gitconfig

<figure>
  <img src='/wp-content/uploads/app-level@2x.png' class="help-center-img img-bordered" alt="Application activity log in GitKraken Desktop showing timestamps, actions, and durations for tasks like opening repositories and refreshing gitconfig">
  <figcaption style="text-align:center; color:#888">Application tab showing GitKraken Desktop actions</figcaption>
</figure>

This log remains static regardless of which repository is currently open.

***

## How the Repository log works

The **Repository** tab displays Git operations performed on the currently active repository, such as:
- Fetch
- Push
- Merge

<figure>
  <img src='/wp-content/uploads/repository-level@2x.png' class="help-center-img img-bordered" alt="Repository tab showing Git operations like fetch, push, reset, squash, and commit along with timestamps and durations">
  <figcaption style="text-align:center; color:#888">Repository-level Git actions displayed in the log</figcaption>
</figure>

Repository logs only reflect actions from the active repo.

<div class='callout callout--warning'>
    <p><strong>Note:</strong> For more detailed entries, go to <em>Preferences > General > Use extended logging in activity log</em>.</p>
</div>

Enabling extended logging adds more granularity, including details like Auto-fetch activity.

<figure>
  <img src='/wp-content/uploads/extended@2x.png' class="help-center-img img-bordered" alt="Repository Activity Logs displaying Git operations like fetch, pull request retrieval, commit creation, and auto-fetch with timestamps and durations">
  <figcaption style="text-align:center; color:#888">Extended logging shows additional Git operations</figcaption>
</figure>

***

## How the Git hook log works

If you use <a href="/working-with-repositories/githooks/">Git hooks</a>, the *Repository* tab will display hook activity such as:
- Success messages
- Warnings and failures
- Errors

<figure>
  <img src='/wp-content/uploads/githook-log.gif' class="help-center-img img-bordered" alt="Git hook log displaying a mismatch between the global commit email and the expected committing email, with hook process termination">
  <figcaption style="text-align:center; color:#888">Git hook activity displayed in the log</figcaption>
</figure>

This provides context for events, making it easier to troubleshoot issues.

Additionally, you can open the Git hook log directly from the snackbox notification if a hook-related error occurs.

<figure>
  <img src='/wp-content/uploads/snackbox-error@2x.png' class="help-center-img img-bordered" alt="GitKraken Desktop error snackbox with message 'pre-commit: Git Hook exited with 1' and options to view the log or dismiss the message">
  <figcaption style="text-align:center; color:#888">Error snackbox linking to Git hook log</figcaption>
</figure>
