# aur-audit

AUR package audit tool for Arch Linux.

## Features

- **Orphan Detection** - Find AUR packages with no maintainer
- **Stale Package Detection** - Find packages not updated in 2+ years
- **Quick Scanning** - Uses AUR RPC API for efficient batch queries

## Usage

```bash
./aur-audit              # Scan with colors
./aur-audit --plain     # Plain text output
./aur-audit --help      # Show help
```

## Example Output

```
󰐪 AUR Audit

  Scanning 25 AUR packages...

󰚤 Orphaned Packages (no maintainer)
  * logo-ls
  * yay-debug

Summary
  Total AUR packages: 25
  Orphans: 6
  Stale: 0
```

## What it checks

- **Orphans** - Packages with no maintainer in AUR
- **Stale** - Packages not updated in 730+ days
