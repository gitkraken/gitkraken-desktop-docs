---
title: GitKraken Desktop + Trello Integration
description: Connect GitKraken Desktop to Trello to preview, manage, and link cards with your branches and repositories.
product: GitKraken Desktop
feature: Trello Integration
content_type: how-to
audience: developer
plan_required: all
os_support: [Windows, macOS, Linux]
git_hosts: [Trello]
integrations: [Trello]
hosted_variant: cloud
status: GA
last_verified: 2026-11
llms_include: true
tags: [trello, cards, filters, branching, integration]
taxonomy:
    category: gitkraken-desktop
custom_fields:
    nav_category: "desktop-integrations-with-issue-trackers"
    nav_label: "Trello"
    nav_order: 80
    nav_parent: "desktop-integrations-with-issue-trackers"
    page_type: "content"
    card_icon: "brand-trello"
    card_color: "green"
    card_description: "Preview Trello cards and branch from them"
---

<kbd>Last updated: November 2026</kbd>

Use this page to connect GitKraken Desktop to Trello so you can preview, create, edit, filter, and branch from cards without leaving your Git workflow. Trello is view-only for Community users, while paid GitKraken subscriptions unlock the full card management workflow.

**Requirements and limits**
- Integration covered here: Trello
- Community plan limit: View-only access
- Paid subscription requirement: Creating, editing, and branching from cards requires a paid GitKraken subscription
- Connection scope: Trello cards appear in the ISSUES section after authorization
- Filters: Custom filters use Trello filter syntax

***

## Quick Start


1. Go to <kbd>Preferences > Integrations</kbd> or click the ISSUES section in the Left Panel.
2. Select **Trello** and click **Connect to Trello**, then finish connecting in your browser at gitkraken.dev. If Trello asks you to authorize the connection, click **Allow**.
3. Find your Trello cards in the Left Panel under the _All Cards_ filter, which is the default.

**To view and edit a card:** Click any card to open its detail view. You can edit the title, description, list, assignees, and comments. Changes sync with your Trello board in real time.

**To create a new card:** Click the **+** icon in the Left Panel, fill in the required fields, and submit. The card syncs to Trello automatically.

**To create a branch from a card:** Open the card detail view and click **Create branch**. GitKraken Desktop pre-fills the branch name from the card title, and the branch shows the Trello icon.

**To filter cards:** Use Trello's filter syntax in the Left Panel to narrow results by board, list, label, or member.

<div class='embed-container embed-container--16-9'>
    <iframe width="560" height="315" src="https://www.youtube.com/embed/huH2nZaGG-s" frameborder="0" allowfullscreen></iframe>
</div>

<div class='callout callout--basic'>
    <p>The Trello integration is view-only for Community users. To use all features, upgrade to a <a href="https://gitkraken.com/pricing?source=help_center&product=gitkraken">paid GitKraken subscription</a>.</p>
</div>

---

## How to connect the Trello integration

Set up the integration from the ISSUES section in the Left Panel or from <kbd>Preferences > Integrations</kbd>.

<div class='callout callout--basic'>
    <p><strong>Use the Trello integration when:</strong> your team tracks work in Trello and you want cards visible beside your repository workflow. <strong>Do not use it as a full replacement for Trello when:</strong> you need broader board management features outside the card workflows covered here.</p>
</div>

<figure>
  <img src="/wp-content/uploads/connect-trello-2025@2x.png" class="help-center-img img-bordered" alt="Connect Trello integration in Preferences">
  <figcaption style="text-align: center; color: #888">Connect Trello integration in Preferences.</figcaption>
</figure>

Trello connects through your GitKraken account, so sign in to GitKraken Desktop first. In <kbd>Preferences > Integrations</kbd>, select **Trello** and click **Connect to Trello**. Your browser opens gitkraken.dev to finish the connection. If Trello asks you to authorize the connection, scroll down and click <strong>Allow</strong>. You can also use the connection on your other computers and profiles. See [How integrations connect through your GitKraken account](/gitkraken-desktop/integrations/#how-integrations-connect-through-your-gitkraken-account).

<figure>
  <img src="/wp-content/uploads/trello-integration@2x.png" class="help-center-img img-bordered" alt="Trello authorization page">
  <figcaption style="text-align: center; color: #888">Trello authorization page.</figcaption>
</figure>

---

## How to preview Trello cards

After you connect, your Trello cards appear in the Left Panel under the default _All Cards_ filter.

<figure>
  <img src="/wp-content/uploads/trello-cards-2025@2x.png" class="help-center-img img-bordered" alt="Trello cards in Left Panel">
  <figcaption style="text-align: center; color: #888">Trello cards in Left Panel.</figcaption>
</figure>

Hover over any card to preview its title, description, list, labels, and members.

<figure>
  <img src="/wp-content/uploads/trello-card-hover-2025@2x.png" class="help-center-img img-bordered" alt="Card preview tooltip">
  <figcaption style="text-align: center; color: #888">Card preview tooltip.</figcaption>
</figure>

---

## How to view and edit Trello card details

Click a card to open its detail view.

<figure>
  <img src="/wp-content/uploads/trello-card-details-view-2025@2x.png" class="help-center-img img-bordered" alt="Trello card detail view">
  <figcaption style="text-align: center; color: #888">Trello card detail view.</figcaption>
</figure>

You can view and edit:

- Title and Description
- List
- Assignees
- Comments

Changes sync with your Trello board in real time.

---

## How to create a new Trello card

Click the <code>+</code> icon in the Left Panel to add a new card.

<figure>
  <img src="/wp-content/uploads/trello-create-card-2025@2x.png" class="help-center-img img-bordered" alt="Create new Trello card">
  <figcaption style="text-align: center; color: #888">Create new Trello card.</figcaption>
</figure>

Fields marked with <code>*</code> are required. GitKraken Desktop syncs the card to Trello automatically.

---

## How to create Trello card filters

You can use Trello’s filter syntax to create custom filters for your cards.

<div class='callout callout--basic'>
    <p><strong>Use custom card filters when:</strong> you need to focus on a board, list, label, or member-specific queue. <strong>Do not rely on the default All Cards view when:</strong> it mixes too much unrelated work together.</p>
</div>

<figure>
  <img src="/wp-content/uploads/trello-create-filter-2025@2x.png" class="help-center-img img-bordered" alt="Create Trello filter">
  <figcaption style="text-align: center; color: #888">Create Trello filter.</figcaption>
</figure>

See Trello’s [filtering guide](https://help.trello.com/article/808-searching-for-cards-all-boards) for syntax examples.

---

## How to create branches from Trello cards

To create a branch tied to a card, click <strong>Create branch</strong> in the card detail view, or right-click the card.

<div class='callout callout--basic'>
    <p><strong>Use card-based branch creation when:</strong> the branch should map directly to one Trello card. <strong>Do not use it when:</strong> the branch covers several cards or needs a branch name that should not be derived from the card title.</p>
</div>

<figure>
  <img src="/wp-content/uploads/create-branch-jira-integration.gif" class="help-center-img img-bordered" alt="Create branch from Trello card">
  <figcaption style="text-align: center; color: #888">Create branch from Trello card.</figcaption>
</figure>

GitKraken Desktop pre-fills the branch name from the card title. Branches created from a card show the Trello icon.

---

## How to copy a card link or open it in Trello

Click the <kbd><i class="fa fa-ellipsis-v"></i></kbd> icon or the <i class="fa fa-external-link" aria-hidden="true"></i> icon to copy the link or open the card in Trello.

<figure>
  <img src="/wp-content/uploads/trello-open-in-browser-2025@2x.png" class="help-center-img img-bordered" alt="Open Trello card in browser">
  <figcaption style="text-align: center; color: #888">Open Trello card in browser.</figcaption>
</figure>
