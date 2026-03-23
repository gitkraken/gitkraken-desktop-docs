---
title: How to Search Git Commits in GitKraken Desktop
description: Discover how to find commits by message, SHA, or author in GitKraken Desktop. Learn how to configure graph limits and use the search bar or Command Palette.
taxonomy:
    category: gitkraken-desktop
---
<kbd>Last updated: March 2026</kbd>

Use this page to search commit history in GitKraken Desktop by message, SHA, or author and to control how much history is loaded into the Commit Graph. It is useful when search results seem incomplete because the graph depth is limited or when you want to jump into commit search from anywhere in the app.

**Requirements and limits**
- Search scope: Commit message, SHA, and author
- Default graph depth: GitKraken Desktop initially displays up to 2000 commits in the Commit Graph
- Search limitation: If the graph is not loading enough history, search results can appear incomplete
- Graph setting: Adjust <kbd>Initial Commits in Graph</kbd> or enable <kbd>Show All Commits in Graph</kbd> in Preferences
- Global access: You can jump into commit search from anywhere by opening the Command Palette

***
## How the initial number of displayed commits works

By default, GitKraken Desktop displays up to 2000 commits on the Commit Graph. To view a deeper history of your repo, set the initial number of commits to display on the graph to your preference. 

<div class='callout callout--basic'>
  <p><strong>Increase graph depth when:</strong> search results look incomplete because GitKraken Desktop has not loaded enough history. <strong>Don't raise the limit unnecessarily when:</strong> the missing result is likely due to the query itself rather than the current graph depth.</p>
</div>

Navigate to <kbd>Preferences</kbd> from the gear menu in the upper right corner, and find <kbd>Initial Commits in Graph</kbd> under <kbd>General</kbd>. There is no limit to how many commits can be displayed. 

<figure>
  <img src='/wp-content/uploads/max-commits-2025.png' 
       class="help-center-img img-bordered" 
       alt="Preferences > General view in GitKraken Desktop, with 'Initial Commits in Graph' highlighted to show where to set the number of commits to display.">
  <figcaption style="color:#888; text-align:center">Set the number of commits to display in the Commit Graph from Preferences.</figcaption>
</figure>

Above this setting, you'll also find an option to <kbd>Show All Commits in Graph</kbd> for large repositories. 

## How the search bar works

The search bar in the upper right of the application defaults to commit search.

<div class='callout callout--basic'>
  <p><strong>Use commit search when:</strong> you know part of a message, SHA, or author and want to jump directly to matching commits. <strong>Use the Command Palette when:</strong> you need to start a search workflow from anywhere in the app instead of from the current repo view.</p>
</div>

<figure>
  <img src='/wp-content/uploads/commit-search-2025.png' 
       class="help-center-img img-bordered" 
       alt="GitKraken Desktop view showing a commit search for the term 'unbreak'. The search bar and match are highlighted in the interface.">
  <figcaption style="color:#888; text-align:center">Use the search bar to find commits by message, SHA, or author.</figcaption>
</figure>

Search commits by message, SHA, or author. GitKraken Desktop updates the results live and highlights the commit in the Commit Graph.

To search from anywhere in the app, open the Command Palette:

<table class='table table--bordered table--shortcuts'>
    <thead>
        <tr>
            <th>&nbsp;</th>
            <th>Mac</th>
            <th>Windows/Linux</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>Toggle Command Palette</td>
            <td><kbd>&#8984;</kbd><kbd>P</kbd></td>
            <td><kbd>Ctrl</kbd><kbd>P</kbd></td>
        </tr>
    </tbody>
</table>
