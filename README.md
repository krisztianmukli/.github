🇬🇧 [en](README.md)  |  🇭🇺 [hu](README.hu.md)

# Github Community Health Files

*Default [community health files](https://help.github.com/en/github/building-a-strong-community/creating-a-default-community-health-file) 
for all my open-source projects.*

This repository defines the **default community guidelines**, **issue and pull 
request templates** that all of my project repositories automatically inherit, 
unless a given project overrides them with its own files.

The goal is to ensure that every project operates with consistent standards and 
contribution processes.

## What guidelines does it include?

- **[Code of Conduct](CODE_OF_CONDUCT.md)**: defines the expected behavior of contributors.
- **[Contribution Guide](CONTRIBUTION.md)**: instructions for contributors on how to participate in 
the project.
- **[Governance Model](GOVERNANCE.md)**: describes the project’s governance structure (roles, 
responsibilities, decision-making).
- **[Security Policy](SECURITY.md)**: guidance on reporting vulnerabilities and handling 
supported versions.
- **[Support and Help](SUPPORT.md)**: explains where and how users can request help, and what 
level of support the project can provide.

## What additional templates does it store?

- **Issue templates**: the following categories are distinguished, and the 
project [does not accept](.github/ISSUE_TEMPLATE/config.yml) other issue types:
    - [bug reports](.github/ISSUE_TEMPLATE/bug.yml)
    - [maintenance suggestions or issues](.github/ISSUE_TEMPLATE/chore.yml)
    - [documentation suggestions or issues](.github/ISSUE_TEMPLATE/documentation.yml)
    - [feature requests](.github/ISSUE_TEMPLATE/feature.yml)
    - [localization suggestions or issues](.github/ISSUE_TEMPLATE/localisation.yml)
    - [questions related to project usage](.github/ISSUE_TEMPLATE/question.yml)
    - [refactoring suggestions](.github/ISSUE_TEMPLATE/refactoring.yml)

- **[Pull Request template](/.github/PULL_REQUEST_TEMPLATE.md)**: defines the accepted structure and required 
sections for pull requests.

- **[CODEOWNERS](.github/CODEOWNERS)**: this file defines which individuals or teams are responsible 
for which files or directories across the organization’s repositories. GitHub 
uses this file to:
    - Automatically request reviews from the designated code owners
    - Enforce that merges require approval from code owners (if branch 
protections are configured)
    - Determine who maintains specific components or paths 

- **[FUNDING.yml](.github/FUNDING.yml)**: this file enables the display of sponsorship or funding 
links on GitHub repository pages.
