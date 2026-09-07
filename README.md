# Hi there 👋

I'm a backend and platform engineer in the Netherlands. I work on the parts of a system that fail expensively: deployment pipelines, data migrations, authorization boundaries, and framework upgrades that have to happen while the product keeps shipping.

Most of my professional work lives in private company repositories, so you'll only find personal projects here. What it doesn't show: three years of platform engineering at a performance-marketing group, including taking technical ownership of a contractor-built content platform serving four European markets, running a four-major-version framework upgrade on a live product with no feature freeze, and designing a federated deny-by-default authorization layer for an internal identity system.

## What I'm building

### home-budgeter 

A Python API for household budgeting, self-hosted and deployed. The interesting problem isn't budgeting, it's idempotent ingestion: bank exports arrive with overlapping date ranges, restated rows, and corrections that shift every balance after them, so every import is a merge against existing state rather than an append. None of those cases has a correct answer, which is why the repository carries a decision log with the alternatives I rejected and why. Money is integer cents with no division, so splits are exact by construction and the type system enforces it.

### claudesidion 

A developer-tooling plugin that persists an AI coding agent's working context into a git-versioned Obsidian vault, wired into the agent's session lifecycle via shell hooks. It runs in an environment that guarantees nothing: no interactive shell profile, possibly no jq or git, a vault that may not exist, and a date binary whose flags differ by platform. So every hook fails open and exits cleanly on any missing precondition. It cannot break the host's session. Cross-platform on macOS and Linux, packaged for one-command installation.

## Working with

Python · Bash · GCP (Cloud SQL, Pub/Sub, GKE) · Docker · Kubernetes · GitLab CI/CD · PostgreSQL · MySQL · Linux · Cloudflare · Datadog

Also fluent in PHP/Laravel, JavaScript/TypeScript and Vue, which is where most of the last three years went.
