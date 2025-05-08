---

title: Security Information for GitKraken Desktop
description: Data Security Information for GitKraken Desktop
taxonomy:
    category: gitkraken-desktop

---

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

