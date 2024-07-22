# Health Files

Repository for default files which are applied to all of the organization's repositories.

## Reusable Github Workflows

This project provides several GitHub workflows that [can be reused](https://docs.github.com/en/actions/learn-github-actions/reusing-workflows) in other repositories. As an example, this code, which is cited from the above-linked Github documentation page, shows how reusable workflows are generally used:

Read [GitHub's docs](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file) to learn more.

```yaml
name: Call a reusable workflow
on:
    pull_request:
        branches:
            - latest
jobs:
    call-workflow:
        uses: jarsft/.github/.github/workflows/example-workflow.yml@latest

    call-workflow-passing-data:
        uses: jarsft/.github/.github/workflows/example-workflow.yml@latest
        with:
            foo: bar
        secrets:
            token: ${{ secrets.TOKEN }}
```
