# Nomic Foundation repository template

This is a template with some basic workflows and files that can be used by new and existing repos.

## How to use this template

1. Create a new repository with the "Use this template" button
2. Create a new [GitHub project](https://github.com/orgs/NomicFoundation/projects) in the org
3. Generate a [Personal Access Token](https://github.com/settings/tokens) with `repo` and `project` permissions. Use the "Classic" tokens because the new tokens don't support organization-scoped permissions at the time of writing this.
4. Add a [secret](https://docs.github.com/en/actions/security-guides/encrypted-secrets) to the repository named `ADD_TO_PROJECT_PAT` with the token you created in the previous step.
5. Open the [`add-issue-to-project.yml`](.github/workflows/add-issue-to-project.yml) file and replace `<id>` with the id of the project created in step 2.
