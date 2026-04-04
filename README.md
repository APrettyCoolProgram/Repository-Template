<!--
  README.md for Repository-Template.
  R26.4
  260402_code
  260402_documentation
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

This repository is a reusable starting point for GitHub repositories. It collects a root README, alternate README
templates, standard supporting documentation, and GitHub metadata so a new repository can start with a consistent 
structure instead of an empty scaffold.

## Contents

- [What this repository includes](#what-this-repository-includes)
- [Using the template](#using-the-template)
- [Repository layout](#repository-layout)
- [Supporting documentation](#supporting-documentation)

## What this repository includes

- A root README for the template repository itself.
- [Collection-README.md](Collection-README.md) for collection-style repositories.
- [SourceCode-README.md](SourceCode-README.md) for software or source-code repositories.
- A [docs](docs) folder containing common repository documents such as the changelog, roadmap, testing notes,
  support, and security guidance.
- A [src](src) folder for source code organization.
- A [.github](.github) folder for repository assets, workspace data, and repository-specific metadata.

## Using the template

1. Create a new repository from this template, or copy the parts you want into an existing repository.
2. Decide which README variant best matches the new repository:
   - Use [Collection-README.md](Collection-README.md) for repositories that primarily collect links, notes, or
     documentation.
   - Use [SourceCode-README.md](SourceCode-README.md) for repositories that contain buildable software or other
     source code.
3. Copy the selected README template into the target repository as `README.md` and replace the placeholder text,
   badges, links, screenshots, and release details.
4. Review the files in [docs](docs) and remove any documents the new repository does not need.
5. Update the repository assets under [.github/repository](.github/repository), especially the logo and README
   screenshots, so the new repository branding matches the project.
6. Add the `.do-not-commit/` folder to `.github/`
7. Clean up any template-only content before publishing.

## Repository layout

Your repository should look like this:

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
|
|-- src/
|-- LICENSE.md
|-- README.md
```
