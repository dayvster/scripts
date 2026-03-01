# pacintel

Package intelligence tool for Arch Linux.

## Features

- **Package Info** - Version, repo, arch, size, install date, last build, deps count, reverse deps
- **Type** - Explicit vs dependency
- **Status** - Active or abandoned (>2 years)
- **Abandoned Detection** - Find packages not updated in X days
- **Orphan Detection** - Show orphan packages and their dependency chains
- **Explicit/Dep Lists** - List explicitly installed or dependency-only packages
- **Dependencies** - Show what a package depends on and what requires it

## Usage

```bash
# Package info
./pacintel firefox

# Dependencies
./pacintel firefox -D

# Abandoned packages (>365 days)
./pacintel -a 365

# Orphans with dependency chains
./pacintel -o

# Explicitly installed
./pacintel -e

# Dependency-only packages
./pacintel -d

# List all packages
./pacintel -l

# Plain text output
./pacintel firefox --plain
```

## Options

| Flag | Description |
|------|-------------|
| `-h, --help` | Show help |
| `-p, --plain` | Plain text output (no colors) |
| `-a, --abandoned <days>` | Show packages not updated in X days (default: 730) |
| `-o, --orphans` | Show orphan packages and their dependencies |
| `-e, --explicit` | List explicitly installed packages |
| `-d, --deps` | List dependency-only packages |
| `-l, --list` | List all installed packages with info |
| `-D, --depends` | Show dependencies for a package |

## Example Output

```
󰮯 firefox
  Fast, Private & Safe Web Browser

  Version    : 148.0-1
  Repo       : extra
  Arch       : x86_64
  Size       : 279.47 MiB
  Installed  : Sun 01 Mar 2026 10:45:29 AM CET
  Last Build : Mon 23 Feb 2026 09:14:19 PM CET (5d ago)
  Deps       : 31  RDep : -

  Type       : Explicit
  Status     : Active
```
