---

title: GitKraken Desktop – Data Security and Storage Practices
description: Learn how GitKraken Desktop collects, transmits, and stores user and repository data securely. Includes encryption methods, data storage locations, and compliance details.
taxonomy:
    category: gitkraken-desktop

---

## Information Collection/Storage
Below is a chart outlining some basic security information regarding the type of data that we collect and how we store it.

<table>
  <thead>
    <tr>
      <th><strong>Service</strong></th>
      <th><strong>What info are we collecting</strong></th>
      <th><strong>How is this info secured in transfer</strong></th>
      <th><strong>Where is this info stored</strong></th>
      <th><strong>How is this info secured in storage</strong></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>Workspaces/Insights</td>
      <td>Repository info: URL, org name, repo name, and issue count.<br>Pull request info: URL, author, title, description, comment count, and PR state.</td>
      <td>Encrypted with TLS</td>
      <td>MongoDB Atlas</td>
      <td>Encrypted at rest (AES-256)</td>
    </tr>
    <tr>
      <td>Teams &amp; Users</td>
      <td>Repo-relative file paths, number of lines changed, name of branch currently checked out, first commit SHA of the repository</td>
      <td>Encrypted with TLS</td>
      <td>MongoDB Atlas</td>
      <td>Encrypted at rest (AES-256)</td>
    </tr>
    <tr>
      <td>Subscriptions</td>
      <td>Billing info: name, payment type (credit card, paypal, ACH, etc.), last four digits of payment method, zip code, country, credit card type (mastercard, visa, etc.)</td>
      <td>Encrypted with TLS</td>
      <td>MongoDB Atlas</td>
      <td>Encrypted at rest (AES-256)</td>
    </tr>
    <tr>
      <td>Launchpad</td>
      <td>URLs of issues and pull requests, issue tracker and Git provider filters for saved views</td>
      <td>Encrypted with TLS</td>
      <td>Postgres (RDS)</td>
      <td>Encrypted at rest (AES-256)</td>
    </tr>
    <tr>
      <td>Cloud Patches</td>
      <td>Info related to the patch (repo name/URL/provider/base branch name/etc.) + the patch content itself.</td>
      <td>Encrypted with TLS</td>
      <td>Patch info is stored in a Postgres database, patch content is stored in AWS S3.</td>
      <td>SSE-S3, which uses 256-bit Advanced Encryption Standard (AES-256)</td>
    </tr>
    <tr>
      <td>Proactive Conflict Detection</td>
      <td>Repo-relative file paths, name and commit SHA of relevant branches, names of files changed, line numbers with changes, and first commit SHA of the repository</td>
      <td>Encrypted with TLS</td>
      <td>Redis (max TTL of 108 hours)</td>
      <td>Encrypted at rest (AES-256)</td>
    </tr>
  </tbody>
</table>

## SOC2
GitKraken and it’s tools are now SOC 2 Certified! If you would like to request a copy of our SOC2 report, please visit our [Trust Center](https://trust.gitkraken.com/) to get the request process started. Please note that in order to provide a copy of the report, we will need you to sign an MNDA.

<div class="bbb-callout bbb--info">
    <div class="irow">
    <div class="ilogobox">
        <span class="logoimg"></span>
    </div>
    <div class="imsgbox">
       SOC 2 reports are only available for Business and Enterprise customers.
    </div>
    </div>
</div>
