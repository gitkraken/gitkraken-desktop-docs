---
title: Pull Request Filter Syntax in GitKraken Desktop
description: Use advanced filter syntax in GitKraken Desktop to find pull requests by title, author, label, branch, CI status, and more across supported integrations.
product: GitKraken Desktop
feature: Pull Request Filter Syntax
content_type: reference
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [GitHub, GitLab, Bitbucket, Azure DevOps]
integrations: [GitHub, GitLab, Bitbucket, Azure DevOps]
hosted_variant: both
status: GA
last_verified: 2026-03
llms_include: true
tags: [pull-requests, filters, syntax, search, ci]
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

This reference explains how to filter pull requests in GitKraken Desktop by title, author, assignee, branch, status, and other supported fields. Use it when you need to narrow large pull request lists quickly or want to know which filter operators work for GitHub and other hosted integrations.

***

## Pull request filters supported for GitHub

### How to search by title or description

| Filter            | Example               | Description                                                        |
|------------------|-----------------------|--------------------------------------------------------------------|
| Title/body search| `foo`                 | Matches PRs with `foo` in the title or description                |
| Exact match      | `foo bar`             | Matches PRs with `foo bar` in the title or description            |
| `in:` title only | `foo in:title`        | Matches PRs with `foo` in the title only                          |
| `in:` body only  | `foo in:body`         | Matches PRs with `foo` in the body only                           |

### How to filter by people

| Filter             | Example               | Description                                                      |
|-------------------|-----------------------|------------------------------------------------------------------|
| `author:`          | `author:keanu`        | PRs created by user `keanu`                                     |
| `assignee:`        | `assignee:keanu`      | PRs assigned to `keanu`                                         |
| `review-requested:`| `review-requested:jerry` | PRs needing review from `jerry`                             |
| `reviewed-by:`     | `reviewed-by:keanu`   | PRs already reviewed by `keanu`                                 |
| `involves:`        | `involves:jerry`      | PRs involving `jerry` via comment, review, or assignment        |

### How to filter by branch

| Filter     | Example            | Description                        |
|------------|--------------------|------------------------------------|
| `base:`    | `base:main`        | PRs targeting the `main` branch    |
| `head:`    | `head:development` | PRs from `development` branch      |

### How to filter by state and metadata

| Filter        | Example                | Description                                     |
|---------------|------------------------|-------------------------------------------------|
| `draft:`      | `draft:true`           | Draft PRs only                                 |
| `label:`      | `label:"Release Critical"` | PRs with the specified label             |
| `milestone:`  | `milestone:v1`         | PRs assigned to `v1` milestone                 |

### How to filter by review status

| Filter  | Example                 | Description                                       |
|---------|-------------------------|---------------------------------------------------|
| `review:`| `review:approved`      | PRs approved by at least one reviewer             |
|         | `review:changes_requested`| PRs with change requests                        |
|         | `review:none`           | PRs without any reviews                           |

### How to filter by CI status

| Filter    | Example          | Description                        |
|-----------|------------------|------------------------------------|
| `status:` | `status:success` | PRs with successful CI             |
|           | `status:pending` | PRs with pending CI                |
|           | `status:failure` | PRs with failed CI                 |

### How to filter for missing values

| Filter | Example         | Description                      |
|--------|-----------------|----------------------------------|
| `no:`  | `no:assignee`   | PRs without an assignee          |
|        | `no:status`     | PRs without a CI status          |

### How to filter by date

| Filter     | Example                  | Description                          |
|------------|--------------------------|--------------------------------------|
| `created:` | `created:2020-12-31`     | PRs created on or after this date    |
| `updated:` | `updated:2020-12-31`     | PRs updated on or after this date    |

### How to combine or exclude filters

You can combine filters using commas (OR logic) or use a dash (`-`) to exclude.

**Examples:**
- `label:Bug,Feature` – PRs with either label
- `-assignee:guy` – PRs not assigned to `guy`
- `label:Bug,Feature label:Important` – PRs with Bug or Feature, and also Important

***

## Pull request filters supported for other integrations

GitKraken Desktop supports some—but not all—filter options across integrations:

| Integration           | updated: | review-requested: | assignee: | title/body/in/no/created/base/head | reviewed-by, review, involves, label, milestone, draft, status |
|------------------------|:--------:|:------------------:|:---------:|:----------------------------------:|:-------------------------------------------------------------:|
| GitLab / Self-Managed | ✔        |                    | ✔        | ✔                                  |                                                               |
| Bitbucket             | ✔        |                    | ✔        | ✔                                  |                                                               |
| Bitbucket Data Center | ✔        | ✔                  |          | ✔                                  |                                                               |
| Azure DevOps          |          |                    | ✔        | ✔                                  |                                                               |

<div class='callout callout--basic'>
  <p><strong>Tip:</strong> Use filters in the pull request panel to narrow down by author, label, or merge target.</p>
</div>
