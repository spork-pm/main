# spork main drawer

Command-line tools for [spork](https://github.com/spork-pm/spork), the macOS package manager that needs no admin rights.

spork's installer adds this drawer for you. To add it by hand:

```bash
spork drawer add main https://github.com/spork-pm/main
```

## Packages

| Package | Description |
|---|---|
| `dotnet10=sdk` | .NET Core 10 SDK |
| `fd` | A simple, fast and user-friendly alternative to find |
| `git` | A free and open source distributed version control system |
| `jq` | Command-line JSON processor |
| `nodejs-lts` | An asynchronous event driven JavaScript runtime designed to build scalable network applications (Long Term Support) |
| `nodejs` | An asynchronous event driven JavaScript runtime designed to build scalable network applications |
| `python` | A programming language that lets you work quickly and integrate systems more effectively |
| `ripgrep` | Recursively search directories for a regex pattern |
| `starship` | The minimal, blazing fast, and extremely customizable prompt for any shell |

## Adding a package

Add one JSON manifest per package in [drawer/](drawer/), named after the package (`drawer/<name>.json`).
This drawer is for command-line tools (anything linked into ~/.spork/bin). GUI apps go in [apps](https://github.com/spork-pm/apps). The manifest format is described in
[spork's README](https://github.com/spork-pm/spork#manifest-format). Get checksums with `spork hash <url>`, and test
with `spork install ./drawer/<name>.json` before opening a pull request.
