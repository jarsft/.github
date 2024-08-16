## Health Files

Repository for default files which are applied to all of the organization's repositories.

### Reusable Github Workflows

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

## Licensing

**Copyright (C) 2024 Jarsoft, Inc. - All Rights Reserved.**<br>
This repository is licensed under the [**Mozilla Public License 2.0 (MPL-2.0)**](https://github.com/jarsft/.github/blob/feat/add-proprietary/LICENSE) which permits integration of this repository with other projects, including commercial and closed source, but asks you to publish source-level modifications you make to this repository.

The **Jarsoft Proprietary Software License** which exists as a template for the organization's internal projects does not have any effect on this repository, it [the repository] is still licensed under MPL-2.0, and it's licensing terms apply.

### Disclaimer

Any code/software (if available) within this repository is provided on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. By using any code in this repository, you agree that you're aware of it's condition.
