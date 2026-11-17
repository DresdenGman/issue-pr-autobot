# issue-pr-autobot

This repository runs a weekly GitHub Actions job that discovers open,
unassigned issues labeled `good first issue` and publishes a single updated
candidate list as a GitHub Issue.

## Run it

- The workflow runs every Monday at 06:00 UTC.
- It can also be started manually from **Actions > Discover candidate issues > Run workflow**.

## External pull requests

Discovery is intentionally separate from implementation. Before opening PRs
in another public repository, review the repository's contribution policy and
whether automated contributions are allowed.

External PR creation requires a fine-grained personal access token with access
to the target organization/repository and permission to:

- fork public repositories;
- create branches;
- create pull requests;
- read repository contents and issues.

Store the token as `ISSUE_PR_PAT` in this repository's GitHub Actions secrets.
Never commit a token or expose it in workflow logs.
Scheduled discovery and implementation of candidate GitHub issues
