<div align="center">

  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/logo/RepositoryTemplate-Logo-dark-279x272.jpg">
    <source media="(prefers-color-scheme: light)" srcset=".github/logo/RepositoryTemplate-Logo-light-279x272.jpg">
    <img alt="Repository Template logo" src=".github/logo/RepositoryTemplate-Logo-light-279x272.jpg">
  </picture>

  <br>

  ![RELEASE](https://img.shields.io/badge/Release-September_2026-teal)&nbsp;&nbsp;
  ![LICENSE](https://img.shields.io/badge/license-Apache%202.0-blue)

# Repository Template

</div>

| CONTENTS |
|----------|
| [About this repository](#about-this-repository) |
| [What this repository includes](#what-this-repository-includes) |
| [Using the template](#using-the-template) |
| [Repository layout](#repository-layout) |
| [Supporting documentation](#supporting-documentation) |

***

## About this repository

This is a GitHub repository template, which provides a consistent starting structure for new repositories.

### What this repository includes

* A [.github/](.github) folder for repository resources.
* A [docs/](docs) folder for repository documentation.
* A [project/](project) folder for [*project repositories*](#project-repositories).
* A [src/](src) folder for [*source code repositories*](#source-code-repositories).
* A `.gitignore` file.
* An `AGENTS.md` file.
* A `LICENSE` file.
* The repository's main `README.md`, which will be replaced by:
  * The [Collection-README.md](Collection-README.md) for collection-style repositories.
  * The [Project-README.md](Project-README.md) for project-style repositories.
  * The [SourceCode-README.md](SourceCode-README.md) for software or source-code repositories.

## Using the template

### Collection repositories

A *collection repository* is a repository that primarily collects links, notes, or documentation and **does not contain** source code.

[The Documentation Project](https://github.com/APrettyCoolProgram/TheDocumentationProject) is an example of a collection repository.

To create a collection repository:

1. Create a new repository using this template.
2. Remove the following files/folders:
  * `src/`
  * `projects/`
  * `README.md` (this file!)
  * `SourceCode-README.md`
  * `Projects-README.md`
3. Rename `Collection-README.md` to `README.md`.
4. Modify `README.md` to reflect the content and purpose of the repository.
5. Review the files in [docs/](docs) and remove any folders/documents the new repository does not need.
6. Replace %RepositoryName% with the name of the new repository in all relevant files.
7. Add the `.do-not-commit/` folder to `.github/` (optional, but helpful)

### Project repositories

A *project repository* is a repository that contains multiple *projects*, which may include source code, documentation, and other assets.

The difference between a *project repository* and a *source code repository* is that a *project repository* contains projects that are loosely related - or not related at all - whereas a *source code repository* primarily focuses on a single codebase.

The [Experiments](https://github.com/APrettyCoolProgram/Experiments) repository is an example of a project repository.

To create a project repository:

1. Create a new repository using this template.
2. Remove the following files/folders:
  * `src/`
  * `README.md` (this file!)
  * `Collection-README.md`
  * `SourceCode-README.md`
3. Rename `Projects-README.md` to `README.md`.
4. Modify `README.md` to reflect the content and purpose of the repository.
5. Review the files in [docs/](docs) and remove any folders/documents the new repository does not need.
6. Replace %RepositoryName% with the name of the new repository in all relevant files.
7. Add the `.do-not-commit/` folder to `.github/` (optional, but helpful)

Each project within the repository should have its own dedicated folder under [projects/](projects).

### Source code repositories

A *source code repository* is a repository that primarily contains buildable software or other source code.

To create a source code repository:

1. Create a new repository using this template.
2. Remove the following files/folders:
  * `projects/`
  * `README.md` (this file!)
  * `Collection-README.md`
  * `Projects-README.md`
3. Rename `SourceCode-README.md` to `README.md`.
4. Modify `README.md` to reflect the content and purpose of the repository.
5. Review the files in [docs/](docs) and remove any folders/documents the new repository does not need.
6. Replace %RepositoryName% with the name of the new repository in all relevant files.
7. Add the `.do-not-commit/` folder to `.github/` (optional, but helpful)

## Repository layout

### . (root directory)

| Item | Description |
| ---- | ------- |
| `.github/` | Repository resources (logos, workflows, etc.) |
| `docs/` | Documentation (changelogs, roadmaps, manuals, etc.) |
| `projects/` | Only used with [project repositories](#project-repositories)
| `src/` | Only used with [source code repositories](#source-code-repositories)
| `.gitignore` | The repository .gitignore |
| `LICENSE` | The repository license |
| `README.md` | The repository README |

```text
.
|-- .github/
|-- docs/
|-- project/
|-- src/
|-- .gitignore
|-- LICENSE
|-- README.md
```









```text
.
|-- .github/
|   |-- agents/
|   |-- archive/
|   |-- development/
|   |   |-- old-src/
|   |   |-- scratch/
|   |   |-- template/
|   |   |-- working/
|   |   |-- DesignDocument.md
|   |   |-- Development-KnownIssues.md
|   |   |-- Development-Notes.md
|   |   |-- Development-Roadmap.md
|   |   |-- ScratchPad.md
|   |-- logo/
|   |-- repository/
|   |   |-- readme/
|   |-- third-party/
|   |-- workspace/
|   
|-- docs/
|   |-- api/
|   |-- man/
|   |-- CHANGELOG.md
|   |-- CODEOWNERS
|   |-- CONTRIBUTORS.md
|   |-- DEVELOPMENT.md
|   |-- FAQ.md
|   |-- KNOWN-ISSUES.md
|   |-- NOTICES.md
|   |-- ROADMAP.md
|   |-- SECURITY.md
|   |-- SUPPORT.md
|   |-- TESTING.md
|   |-- TROUBLESHOOTING.md
|
|-- src/
|-- .gitignore
|-- Collection-README.md
|-- LICENSE
|-- README.md
|-- SourceCode-README.md
```


### .github/

All types of repositories should include a `.github/` folder for GitHub-specific configurations and workflows:

```text
.
|-- .github/
|   |-- agents/
|   |-- archive/
|   |-- development/
|   |   |-- old-src/
|   |   |-- scratch/
|   |   |-- template/
|   |   |-- working/
|   |   |-- DesignDocument.md
|   |   |-- Development-KnownIssues.md
|   |   |-- Development-Notes.md
|   |   |-- Development-Roadmap.md
|   |   |-- ScratchPad.md
|   |-- logo/
|   |-- repository/
|   |   |-- readme/
|   |-- third-party/
|   |-- workspace/
```

```text
.
|-- .github/
|   |-- agents/
|   |-- archive/
|   |-- development/
|   |   |-- old-src/
|   |   |-- scratch/
|   |   |-- template/
|   |   |-- working/
|   |   |-- DesignDocument.md
|   |   |-- Development-KnownIssues.md
|   |   |-- Development-Notes.md
|   |   |-- Development-Roadmap.md
|   |   |-- ScratchPad.md
|   |-- logo/
|   |-- repository/
|   |   |-- readme/
|   |-- third-party/
|   |-- workspace/
|   
|-- docs/
|   |-- api/
|   |-- man/
|   |-- CHANGELOG.md
|   |-- CODEOWNERS
|   |-- CONTRIBUTORS.md
|   |-- DEVELOPMENT.md
|   |-- FAQ.md
|   |-- KNOWN-ISSUES.md
|   |-- NOTICES.md
|   |-- ROADMAP.md
|   |-- SECURITY.md
|   |-- SUPPORT.md
|   |-- TESTING.md
|   |-- TROUBLESHOOTING.md
|
|-- src/
|-- .gitignore
|-- Collection-README.md
|-- LICENSE
|-- README.md
|-- SourceCode-README.md
```




## Supporting documentation

The [docs](docs) folder contains the following standard documents:

| File | Purpose |
|------|---------|
| [CHANGELOG.md](docs/CHANGELOG.md) | History of notable changes across releases. |
| [CODEOWNERS](docs/CODEOWNERS) | GitHub code ownership assignments. |
| [CONTRIBUTORS.md](docs/CONTRIBUTORS.md) | Acknowledgment of project contributors. |
| [DEVELOPMENT.md](docs/DEVELOPMENT.md) | Developer setup, workflow, and contribution guidance. |
| [FAQ.md](docs/FAQ.md) | Answers to frequently asked questions. |
| [KNOWN-ISSUES.md](docs/KNOWN-ISSUES.md) | Documented known issues and workarounds. |
| [NOTICES.md](docs/NOTICES.md) | Legal notices and third-party attributions. |
| [ROADMAP.md](docs/ROADMAP.md) | Planned work and future direction. |
| [SECURITY.md](docs/SECURITY.md) | Security policy and vulnerability reporting guidance. |
| [SUPPORT.md](docs/SUPPORT.md) | How to get help and file issues. |
| [TESTING.md](docs/TESTING.md) | Testing strategy and instructions. |
| [TROUBLESHOOTING.md](docs/TROUBLESHOOTING.md) | Common problems and resolution steps. |
