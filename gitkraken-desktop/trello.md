---
title: GitKraken Desktop + Trello Integration
description: Connect GitKraken to Trello to preview, manage, and link cards with your branches and repositories.
taxonomy:
    category: gitkraken-desktop
---

<kbd>Last updated: March 2026</kbd>

Use this page to connect GitKraken Desktop to Trello so you can preview, create, edit, filter, and branch from cards without leaving your Git workflow. Trello is view-only for Community users, while paid GitKraken subscriptions unlock the full card management workflow.

**Requirements and limits**
- Integration covered here: Trello
- Community plan limit: View-only access
- Paid subscription requirement: Creating, editing, and branching from cards requires a paid GitKraken subscription
- Connection scope: Trello cards appear in the ISSUES section after authorization
- Custom filters use Trello filter syntax

***

## Quick Start

Connect GitKraken Desktop to Trello to view, create, and manage cards alongside your Git workflow.

1. Go to <kbd>Preferences > Integrations</kbd> or click the ISSUES section in the Left Panel.
2. Select **Trello** and click to authorize. Complete the authorization on the Trello page that opens and click **Allow**.
3. Once connected, your Trello cards appear in the Left Panel under the _All Cards_ filter by default.

**To view and edit a card:** Click any card to open its detail view. You can edit the title, description, list, assignees, and comments. Changes sync with your Trello board in real-time.

**To create a new card:** Click the **+** icon in the Left Panel, fill in the required fields, and submit. The card syncs to Trello automatically.

**To create a branch from a card:** Open the card detail view and click **Create branch**. The branch name is pre-filled from the card title and displays the Trello icon.

**To filter cards:** Use Trello's filter syntax in the Left Panel to narrow results by board, list, label, or member.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/huH2nZaGG-s" frameborder="0" allowfullscreen></iframe>
</div>

<div class='callout callout--basic'>
    <p>The Trello integration is view-only for Community users. To unlock all features, consider upgrading to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken subscription</a>.</p>
</div>

---

## How to connect the Trello integration

Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>.

<div class='callout callout--basic'>
    <p><strong>Use the Trello integration when:</strong> your team tracks work in Trello and you want cards visible beside your repository workflow. <strong>Don't use it as a full replacement for Trello when:</strong> you need broader board management features outside the card workflows covered here.</p>
</div>

<img src="/wp-content/uploads/connect-trello-2025@2x.png" class="help-center-img img-bordered" alt="Connect Trello integration in Preferences">

You’ll be redirected to a Trello page to authorize the connection. Scroll down and click <strong>Allow</strong>.

<img src="/wp-content/uploads/trello-integration@2x.png" class="help-center-img img-bordered" alt="Trello authorization page">

Alternatively, copy the token from the _Success_ page and paste it into GitKraken Desktop.

---

## How to preview Trello cards

Once connected, your Trello cards will appear in the Left Panel under a default _All Cards_ filter.

<img src="/wp-content/uploads/trello-cards-2025@2x.png" class="help-center-img img-bordered" alt="Trello cards in Left Panel">

Hover over any card to preview its title, description, list, labels, and members.

<img src="/wp-content/uploads/trello-card-hover-2025@2x.png" class="help-center-img img-bordered" alt="Card preview tooltip">

---

## How to view and edit Trello card details

Click a card to open its detail view.

<img src="/wp-content/uploads/trello-card-details-view-2025@2x.png" class="help-center-img img-bordered" alt="Trello card detail view">

You can view and edit:

- Title and Description
- List
- Assignees
- Comments

Changes sync with your Trello board in real-time.

---

## How to create a new Trello card

Click the <code>+</code> icon in the Left Panel to add a new card.

<img src="/wp-content/uploads/trello-create-card-2025@2x.png" class="help-center-img img-bordered" alt="Create new Trello card">

Fields marked with <code>*</code> are required. Your card will sync automatically with Trello.

---

## How to create Trello card filters

You can use Trello’s filter syntax to create custom filters for your cards.

<div class='callout callout--basic'>
    <p><strong>Use custom card filters when:</strong> you need to focus on a board, list, label, or member-specific queue. <strong>Don't rely on the default All Cards view when:</strong> it mixes too much unrelated work together.</p>
</div>

<img src="/wp-content/uploads/trello-create-filter-2025@2x.png" class="help-center-img img-bordered" alt="Create Trello filter">

See Trello’s [filtering guide](https://help.trello.com/article/808-searching-for-cards-all-boards) for syntax examples.

---

## How to create branches from Trello cards

You can create branches tied to cards directly from the card detail view. Use the <strong>Create branch</strong> button or right-click a card.

<div class='callout callout--basic'>
    <p><strong>Use card-based branch creation when:</strong> the branch should map directly to one Trello card. <strong>Don't use it when:</strong> the branch covers several cards or needs a branch name that should not be derived from the card title.</p>
</div>

<img src="/wp-content/uploads/create-branch-jira-integration.gif" class="help-center-img img-bordered" alt="Create branch from Trello card">

Branch names are prefilled based on the card title. These branches display the Trello icon to indicate the connection.

---

## How to copy a card link or open it in Trello

Click the <kbd><i class="fa fa-ellipsis-v"></i></kbd> icon or the <i class="fa fa-external-link" aria-hidden="true"></i> icon to copy the link or open the card in Trello.

<img src="/wp-content/uploads/trello-open-in-browser-2025@2x.png" class="help-center-img img-bordered" alt="Open Trello card in browser">
