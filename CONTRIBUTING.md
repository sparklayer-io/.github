# Contributing

This guide applies to every SparkLayer repository. A repository's own README or `AGENTS.md` covers anything specific to it, such as setup, commands and extra review rules.

Start with the [Developer Handbook](https://www.notion.so/sparklayer/Handbook-Developers-b8898a282c084c40a9f45c7892e5b77d), in particular [Rules and advice for developers](https://www.notion.so/sparklayer/Rules-and-advice-for-developers-21dddfba557a80b48bdfd36a1a0571c6) and [Best Practices](https://www.notion.so/sparklayer/Best-Practices-2ed6e89003e74842934b7402538b0af0).

## Local development

Run services locally through [spark-docker](https://github.com/sparklayer-io/spark-docker). See [Local Development](https://www.notion.so/sparklayer/Local-Development-b1f0fcf331db4c9894ac094aea4cb016) for setup.

## Branches and commits

- Branch from the default branch and keep each pull request to one change.
- Write commit messages and pull request titles as [Conventional Commits](https://www.conventionalcommits.org/), for example `fix(cart): keep the PO number on reorder`.
- Add the Linear ticket key when there is one, for example `(SPARK-123)`.

## Pull requests

See [Pull Requests](https://www.notion.so/sparklayer/Pull-Requests-f996658dd9bd456c8bf73fa734169784) for the full guidance.

- Fill in the [pull request template](https://github.com/sparklayer-io/.github/blob/main/PULL_REQUEST_TEMPLATE.md).
- Review your own diff before asking anyone else to.
- Request reviewers who know the code. Include the UI team for anything user facing, with a screenshot or recording.
- Let people know about the change in Slack.
- Ask for another review if you make significant changes after approval.
- Link any `TODO` comment to a ticket.

## Merging

Merging to the default branch deploys most repositories to production for every client, so treat a merge as a release. A pull request is ready to merge when:

- a reviewer who knows the code has approved it, with no outstanding change requests
- every review conversation is resolved
- all checks pass

Branch rules on each repository enforce the minimum number of approvals.

## The dev environment

- Claim it in `#technical` before deploying a branch there, and strike through your message when you're done.
- Bring your branch up to date with the default branch before deploying it.
- Get database migrations and Pulumi changes reviewed before running them on dev.

## Documentation

- Public docs and API specs live at [docs.sparklayer.io](https://docs.sparklayer.io/).
- Keep a repository's own docs in its `docs` folder and link to them from its README.
- Use Whimsical for diagrams.

## Security

- Never commit credentials, tokens or secrets.
- Never share secrets over Slack or email.
