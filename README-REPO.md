<!--
  README-REPO.md for Repository-Template.
  R26.4
  260416_documentation
-->

<div align="center">

  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/repository/logo/repository-logo-dark.jpg">
    <source media="(prefers-color-scheme: light)" srcset=".github/repository/logo/repository-logo-light.jpg">
    <img alt="Repository Template logo" src=".github/repository/logo/repository-logo-light.jpg">
  </picture>

  <br>

  ![RELEASE](https://img.shields.io/badge/Release-26.4-teal)&nbsp;&nbsp;
  ![LICENSE](https://img.shields.io/badge/license-Apache%202.0-blue)

# Repository Template

</div>

***

## Contents

- [About this repository](#about-this-repository)
- [Repository layout](#repository-layout)
- [Using the template](#using-the-template)
- [README variants](#readme-variants)
- [Supporting documentation](#supporting-documentation)
- [License](#license)

***

## About this repository

This repository is a reusable starting point for GitHub repositories. It collects a root README, alternate README
templates, standard supporting documentation, and GitHub metadata so a new repository can start with a consistent
structure instead of an empty scaffold.

## Repository layout

```text
.
|-- .github/
|   |-- .do-not-commit/
|   |-- archive/
|   |-- copilot/
|   |-- development/
|   |   |-- old-src/
|   |   |-- scratch/
|   |   |-- working/
|   |-- repository/
|   |   |-- logo/
|   |   |-- readme/
|   |-- third-party/
|   |-- workspace/
|
|-- docs/
|   |-- api/
|   |-- man/
|   |-- ADDITIONAL-INFORMATION.md
|   |-- CHANGELOG.md
|   |-- CODEOWNERS
|   |-- CONTRIBUTORS.md
|   |-- KNOWN-ISSUES.md
|   |-- NOTICES.md
|   |-- ROADMAP.md
|   |-- SECURITY.md
|   |-- SUPPORT.md
|   |-- TESTING.md
|   |-- TROUBLESHOOTING.md
|
|-- src/
|-- Collection-README.md
|-- LICENSE
|-- README.md
|-- README-REPO.md
|-- SourceCode-README.md
```

## Using the template

1. Create a new repository from this template, or copy the parts you want into an existing repository.
2. Decide which README variant best matches the new repository (see [README variants](#readme-variants) below).
3. Copy the selected README template into the target repository as `README.md` and replace the placeholder text,
   badges, links, screenshots, and release details.
4. Review the files in [docs](docs) and remove any documents the new repository does not need.
5. Update the repository assets under [.github/repository](.github/repository), especially the logo and README
   screenshots, so the new repository branding matches the project.
6. Add the `.do-not-commit/` folder to `.github/`.
7. Clean up any template-only content before publishing.

## README variants

| File | Use when... |
|------|-------------|
| [Collection-README.md](Collection-README.md) | The repository primarily collects links, notes, or documentation. |
| [SourceCode-README.md](SourceCode-README.md) | The repository contains buildable software or other source code. |

## Supporting documentation

The [docs](docs) folder contains the following standard documents:

| File | Purpose |
|------|---------|
| [ADDITIONAL-INFORMATION.md](docs/ADDITIONAL-INFORMATION.md) | Supplementary information not covered elsewhere. |
| [CHANGELOG.md](docs/CHANGELOG.md) | History of notable changes across releases. |
| [CODEOWNERS](docs/CODEOWNERS) | GitHub code ownership assignments. |
| [CONTRIBUTORS.md](docs/CONTRIBUTORS.md) | Acknowledgment of project contributors. |
| [KNOWN-ISSUES.md](docs/KNOWN-ISSUES.md) | Documented known issues and workarounds. |
| [NOTICES.md](docs/NOTICES.md) | Legal notices and third-party attributions. |
| [ROADMAP.md](docs/ROADMAP.md) | Planned work and future direction. |
| [SECURITY.md](docs/SECURITY.md) | Security policy and vulnerability reporting guidance. |
| [SUPPORT.md](docs/SUPPORT.md) | How to get help and file issues. |
| [TESTING.md](docs/TESTING.md) | Testing strategy and instructions. |
| [TROUBLESHOOTING.md](docs/TROUBLESHOOTINGS.md) | Common problems and solutions. |

## License

This repository is licensed under the [Apache 2.0 License](LICENSE).

***

<sub>Last updated: 260416</sub>
