# Nomic Foundation repository template

This is a template with some basic workflows and files that can be used by new and existing repos.

## How to use this template

1. Create a new repository with the "Use this template" button
2. Create a new [GitHub project](https://github.com/orgs/NomicFoundation/projects) in the org
3. Generate a [Personal Access Token](https://github.com/settings/tokens) with `repo` and `project` permissions. Use the "Classic" tokens because the new tokens don't support organization-scoped permissions at the time of writing this.
4. Add a [secret](https://docs.github.com/en/actions/security-guides/encrypted-secrets) to the repository named `ADD_TO_PROJECT_PAT` with the token you created in the previous step.
5. Open the [`add-issue-to-project.yml`](.github/workflows/add-issue-to-project.yml) file and replace the `project-url` value with the URL of the project created in step 2.
6. Change the content of the [issue templates](.github/ISSUE_TEMPLATE) according to the project needs. New projects might work well enough with blank issues; in that case, just delete that directory.

## Workflows

The repo contains two automation workflows:

- `add-issue-to-project.yml` adds every new issue and pull request to the configured project
- `add-label-to-new-issue.yml` adds the `status:triaging` label to all new issues and pull requests, unless they already have a label that starts with `status:`. This means that issues created by external users will get this label, but without affecting issues opened by repo owners that set a status during creation.

## Labels

The related GitHub project relies on certain labels being used in the issue tracker. This repo comes with a basic [set of labels](https://github.com/NomicFoundation/nomic-repository-template/labels) for that purpose, but each project can add new ones according to its needs.
