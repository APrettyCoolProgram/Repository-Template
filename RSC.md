<!--
  README.md template for source code repositories.
  R26.4.0.0-161055
  260416_code
  260416_documentation
-->

<!-- [PROJECT MESSAGE] =========================================================
* Project message (optional)
---------------------------------------------------------------------------- -->

> [!IMPORTANT]  
> This is a message everyone should see.

<!--
This divider separates the this section from the rest of the README. If you are
not using the this section, comment this divider out.
--->
---

<!-- ===================================================== [PROJECT MESSAGE] -->

<!-- [PROJECT INTRO] ===========================================================
* Project logo
* Project title (optional)
* Project badges
---------------------------------------------------------------------------- -->

<div align="center">

  <!--
  There are references for both a "light" and "dark" images. The dark image
  should have a background of HEX #0d1117, to match the dark mode of GitHub.
  The light image is the fallback.
  -->
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/repository/logo/repository-logo-dark.jpg">
    <source media="(prefers-color-scheme: light)" srcset=".github/repository/logo/repository-logo-light.jpg">
    <img alt="Fallback image description" src=".github/repository/logo/repository-logo-light.jpg">
  </picture>

  <h1>Source Code Repository README.md Template</h1>

  Catchphrase!

  ![RELEASE](https://img.shields.io/badge/Release\/Version-25.0.0.0-teal)&nbsp;
  ![STAGE](https://img.shields.io/badge/ALPHA/BETA-red)&nbsp; <!-- Alpha = Red, Beta = Yellow, Stable = Green -->
  ![LICENSE](https://img.shields.io/badge/license-apache-blue)&nbsp;
  ![Build](https://img.shields.io/badge/Build-Passing-brightgreen)
  ![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey)&nbsp;

</div>

<!--
This divider separates this section from the rest of the README. This should
not be modified.
--->
---

<!-- ======================================================= [PROJECT INTRO] -->

<!-- [PROJECT DETAIL] ==========================================================
* Project screenshot (optional)
---------------------------------------------------------------------------- -->

A second paragraph with a bit more detail — what problem this solves, who it is for, and
what makes it worth using over alternatives.

<div align="center">

  <!--
  There are references for both a "light" and "dark" images. The dark image
  should have a background of HEX #0d1117, to match the dark mode of GitHub.
  The light image is the fallback.
  -->
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/repository/readme/screenshot01-dark.jpg">
    <source media="(prefers-color-scheme: light)" srcset=".github/repository/readme/screenshot01-light.jpg">
    <img alt="Fallback image description" src=".github/repository/readme/screenshot01-light.jpg">
  </picture>
  <h6>The Screenshot</h6>

</div>

<!--
This divider separates the this section from the rest of the README. If you are
not using the this section, comment this divider out.
--->
---

<!-- ====================================================== [PROJECT DETAIL] -->

## Contents

- [Features](#features)
- [Quick start](#quick-start)
- [Installing](#installing)
- [Configuration](#configuration)
- [Usage](#usage)
- [Building from source](#building-from-source)
- [Testing](#testing)
- [Updating and uninstalling](#updating-and-uninstalling)
- [FAQ](#faq)
- [Contributing](#contributing)
- [License](#license)

---

## Features

- **Feature one** — What it does and why it matters.
- **Feature two** — What it does and why it matters.
- **Feature three** — What it does and why it matters.
- **Feature four** — What it does and why it matters.

---

## Quick start

The shortest possible path from nothing to working:

```shell
# 1. Clone the repository
git clone https://github.com/owner/%ProjectName%.git
cd %ProjectName%

# 2. Install dependencies
dotnet restore

# 3. Run
dotnet run --project src/%ProjectName%.csproj
```

> [!NOTE]
> See [Installing](#installing) for platform-specific instructions and
> [Configuration](#configuration) before running in a non-default environment.

---

## Installing

### Prerequisites

| Requirement | Minimum version | Notes |
|-------------|-----------------|-------|
| [.NET SDK](https://dotnet.microsoft.com/download) | 10.0 | Required to build and run. |
| Requirement two | X.x | Notes. |
| Requirement three | X.x | Notes. |

### Windows

1. Download the latest release from the [Releases](https://github.com/owner/%ProjectName%/releases) page.
2. Run the installer and follow the prompts.
3. Verify the installation:

   ```shell
   %ProjectName% --version
   ```

### macOS

1. Step one.
2. Step two.
3. Verify:

   ```shell
   %ProjectName% --version
   ```

### Linux

1. Step one.
2. Step two.
3. Verify:

   ```shell
   %ProjectName% --version
   ```

---

## Configuration

Configuration is stored in `%ProjectName%.config.json` in the application directory.
A default config file is generated on first run.

### Required settings

These must be set before the application will start:

| Key | Type | Description |
|-----|------|-------------|
| `ConnectionString` | `string` | Database connection string. |
| `ApiKey` | `string` | API key for the external service. |

### Optional settings

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| `LogLevel` | `string` | `"Warning"` | Minimum log level: `Trace`, `Debug`, `Info`, `Warning`, `Error`. |
| `MaxRetries` | `int` | `3` | Number of retry attempts on transient failures. |
| `TimeoutSeconds` | `int` | `30` | Request timeout in seconds. |

**Example configuration:**

```json
{
  "ConnectionString": "Server=localhost;Database=mydb;",
  "ApiKey": "your-api-key-here",
  "LogLevel": "Info",
  "MaxRetries": 3,
  "TimeoutSeconds": 30
}
```

---

## Usage

### Basic usage

```shell
%ProjectName% [command] [options]
```

### Commands

| Command | Description |
|---------|-------------|
| `run` | Starts the application. |
| `init` | Initializes a new configuration file. |
| `status` | Displays the current status. |
| `help` | Displays help information. |

### Common examples

**Initialize a new configuration:**

```shell
%ProjectName% init --output ./config
```

**Run with a specific configuration file:**

```shell
%ProjectName% run --config /path/to/%ProjectName%.config.json
```

**Display help for a specific command:**

```shell
%ProjectName% run --help
```

---

## Building from source

### 1. Clone and restore

```shell
git clone https://github.com/owner/%ProjectName%.git
cd %ProjectName%
dotnet restore
```

### 2. Build

```shell
# Debug build
dotnet build

# Release build
dotnet build --configuration Release
```

### 3. Publish a self-contained executable

```shell
dotnet publish src/%ProjectName%.csproj \
  --configuration Release \
  --runtime win-x64 \
  --self-contained true \
  --output ./dist
```

Replace `win-x64` with `osx-x64`, `osx-arm64`, or `linux-x64` as needed.

---

## Testing

```shell
# Run all tests
dotnet test

# Run with detailed output
dotnet test --logger "console;verbosity=detailed"

# Run a specific test project
dotnet test tests/%ProjectName%.Tests/%ProjectName%.Tests.csproj
```

---

## Updating and uninstalling

### Updating

1. Download the latest release.
2. Replace the existing installation directory with the new files.
3. Run `%ProjectName% init --migrate` to apply any configuration schema changes.

### Uninstalling

**Windows:** Use *Add or Remove Programs* in Settings, or run the bundled uninstaller.

**macOS / Linux:** Delete the application directory and remove the entry from your `PATH`.

---

## FAQ

**Q: Does this work offline?**  
A: Core functionality works without a network connection. Features that depend on the external API require connectivity.

**Q: Where are logs stored?**  
A: Logs are written to `%APPDATA%\%ProjectName%\logs` on Windows and `~/.local/share/%ProjectName%/logs` on macOS and Linux.

**Q: Can I run multiple instances at the same time?**  
A: Yes, as long as each instance uses a separate configuration file and data directory.

---

## Contributing

Contributions are welcome. Please follow these steps:

1. **Search existing issues** before opening a new one to avoid duplicates.
2. **Open an issue** to discuss the change you want to make.
3. **Fork the repository** and create a feature branch from `main`.
4. **Make your changes** — keep commits focused and write clear commit messages.
5. **Run the test suite** and ensure all tests pass before submitting.
6. **Open a pull request** against `main` and fill in the pull request template.

Please read the [contributing guidelines](docs/CONTRIBUTING.md) and
[code of conduct](docs/CODE_OF_CONDUCT.md) before contributing.

---

## License

Distributed under the [Apache 2.0 License](LICENSE).  
Copyright &copy; 2026 %Owner%

---

<sub>Last updated: 260416</sub>
