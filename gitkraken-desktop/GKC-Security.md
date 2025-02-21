---

title: Security Information for GitKraken Desktop
description: Data Security Information for GitKraken Desktop
taxonomy:
    category: gitkraken-desktop

---

Below is a chart outlining some basic security information regarding the type of data that we collect and how we store it.

| Service | What information are we collecting | How is this information secured in the transfer| Where is this information stored | How is this information secured in storage |
| --- | --- | --- | --- | --- |
| Workspaces/Insights | Repository info: URL, org name, repo name, and issue count.<br>Pull request info: URL, author, title, description, comment count, and PR state. | Encrypted with TLS | MongoDB Atlas | Encrypted at rest (AES-256) |
| Teams & Users | Repo-relative file paths, number of lines changed, name of branch currently checked out, first commit SHA of the repository | Encrypted with TLS | MongoDB Atlas | Encrypted at rest (AES-256) |
| Subscriptions | Billing info: name, payment type (credit card, paypal, ACH, etc.), last four digits of payment method, zip code, country, credit card type (mastercard, visa, etc.) | Encrypted with TLS | MongoDB Atlas | Encrypted at rest (AES-256) |
| Launchpad | URLs of issues and pull requests, issue tracker and Git provider filters for saved views | Encrypted with TLS | Postgres (RDS) | Encrypted at rest (AES-256) |
| Cloud Patches | Info related to the patch (repo name/URL/provider/base branch name/etc.) + the patch content itself. | Encrypted with TLS | Patch info is stored in a Postgres database, patch content is stored in AWS S3. | SSE-S3, which uses 256-bit Advanced Encryption Standard (AES-256) |
| Proactive Conflict Detection | Repo-relative file paths, name and commit SHA of relevant branches, names of files changed, line numbers with changes, and first commit SHA of the repository | Encrypted with TLS | Redis (max TTL of 108 hours) | Encrypted at rest (AES-256)