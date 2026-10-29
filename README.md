# spork main drawer

Command-line tools for [spork](https://github.com/spork-pm/spork), the macOS package manager that needs no admin rights.

spork's installer adds this drawer for you. To add it by hand:

```bash
spork drawer add main https://github.com/spork-pm/main
```

## Packages

| Package | Description |
|---|---|
| `apfel` | On-device AI from the command line via Apple Intelligence: CLI, chat and OpenAI-compatible server |
| `azure-cli` | A cross-platform command-line tool to connect to Azure and execute administrative commands on Azure resources |
| `azure-kubelogin` | A client-go credential (exec) plugin implementing Azure authentication |
| `docker` | Docker command-line client, for a Docker engine running elsewhere (Colima, a VM or a remote host) |
| `dotnet10-sdk` | .NET 10 SDK, for building and running .NET apps |
| `fd` | A simple, fast and user-friendly alternative to find |
| `gh` | GitHub's official command-line tool |
| `git` | A free and open source distributed version control system |
| `helm` | The package manager for Kubernetes |
| `jq` | Command-line JSON processor |
| `kubectl` | Control the Kubernetes cluster manager |
| `nodejs-lts` | An asynchronous event driven JavaScript runtime designed to build scalable network applications (Long Term Support) |
| `nodejs` | An asynchronous event driven JavaScript runtime designed to build scalable network applications |
| `python` | A programming language that lets you work quickly and integrate systems more effectively |
| `ripgrep` | Recursively search directories for a regex pattern |
| `starship` | The minimal, blazing fast, and extremely customizable prompt for any shell |
| `terraform` | Create and manage infrastructure as code using simple declarative configuration files |

## Adding a package

Add one JSON manifest per package in [drawer/](drawer/), named after the package (`drawer/<name>.json`).
This drawer is for command-line tools (anything linked into ~/.spork/bin). GUI apps go in [apps](https://github.com/spork-pm/apps). The manifest format is described in
[spork's README](https://github.com/spork-pm/spork#manifest-format). Get checksums with `spork hash <url>`, and test
with `spork install ./drawer/<name>.json` before opening a pull request.
