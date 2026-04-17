


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



<!-- ===================================================== [GETTING STARTED] -->






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