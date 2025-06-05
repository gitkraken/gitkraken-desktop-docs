---
title: Pull Request Filter Syntax in GitKraken Desktop
description: Use advanced filter syntax in GitKraken Desktop to find pull requests by title, author, label, branch, CI status, and more across supported integrations.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: June 2025</kbd>

Use this syntax to filter pull requests in GitKraken Desktop and quickly find the items you need.

***

## GitHub

### Search by Title or Description

| Filter            | Example               | Description                                                        |
|------------------|-----------------------|--------------------------------------------------------------------|
| Title/body search| `foo`                 | Matches PRs with `foo` in the title or description                |
| Exact match      | `foo bar`             | Matches PRs with `foo bar` in the title or description            |
| `in:` title only | `foo in:title`        | Matches PRs with `foo` in the title only                          |
| `in:` body only  | `foo in:body`         | Matches PRs with `foo` in the body only                           |

### People Filters

| Filter             | Example               | Description                                                      |
|-------------------|-----------------------|------------------------------------------------------------------|
| `author:`          | `author:keanu`        | PRs created by user `keanu`                                     |
| `assignee:`        | `assignee:keanu`      | PRs assigned to `keanu`                                         |
| `review-requested:`| `review-requested:jerry` | PRs needing review from `jerry`                             |
| `reviewed-by:`     | `reviewed-by:keanu`   | PRs already reviewed by `keanu`                                 |
| `involves:`        | `involves:jerry`      | PRs involving `jerry` via comment, review, or assignment        |

### Branch Filters

| Filter     | Example            | Description                        |
|------------|--------------------|------------------------------------|
| `base:`    | `base:main`        | PRs targeting the `main` branch    |
| `head:`    | `head:development` | PRs from `development` branch      |

### State and Metadata

| Filter        | Example                | Description                                     |
|---------------|------------------------|-------------------------------------------------|
| `draft:`      | `draft:true`           | Draft PRs only                                 |
| `label:`      | `label:"Release Critical"` | PRs with the specified label             |
| `milestone:`  | `milestone:v1`         | PRs assigned to `v1` milestone                 |

### Review Status

| Filter  | Example                 | Description                                       |
|---------|-------------------------|---------------------------------------------------|
| `review:`| `review:approved`      | PRs approved by at least one reviewer             |
|         | `review:changes_requested`| PRs with change requests                        |
|         | `review:none`           | PRs without any reviews                           |

### CI Status

| Filter    | Example          | Description                        |
|-----------|------------------|------------------------------------|
| `status:` | `status:success` | PRs with successful CI             |
|           | `status:pending` | PRs with pending CI                |
|           | `status:failure` | PRs with failed CI                 |

### Missing Values

| Filter | Example         | Description                      |
|--------|-----------------|----------------------------------|
| `no:`  | `no:assignee`   | PRs without an assignee          |
|        | `no:status`     | PRs without a CI status          |

### Date Queries

| Filter     | Example                  | Description                          |
|------------|--------------------------|--------------------------------------|
| `created:` | `created:2020-12-31`     | PRs created on or after this date    |
| `updated:` | `updated:2020-12-31`     | PRs updated on or after this date    |

### Multiple and Excluded Filters

You can combine filters using commas (OR logic) or use a dash (`-`) to exclude.

**Examples:**
- `label:Bug,Feature` – PRs with either label
- `-assignee:guy` – PRs not assigned to `guy`
- `label:Bug,Feature label:Important` – PRs with Bug or Feature, and also Important

***

## Other Integrations

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
