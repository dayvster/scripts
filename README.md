# Scripts

Collection of useful scripts for Arch Linux.

## Tools

### pacintel
Package intelligence tool. Shows detailed info about installed packages.

```bash
pacintel/firefox          # Package info
pacintel/firefox -D       # Dependencies
pacintel -a 365           # Abandoned packages
pacintel -o               # Orphans
pacintel -e               # Explicit installs
pacintel -l               # List all packages
```

### aur-audit
Scans AUR packages for issues.

```bash
aur-audit/aur-audit              # Scan AUR packages
aur-audit/aur-audit --plain     # Plain output
```

### check-updates
Check for system updates (pacman, AUR, Flatpak).

```bash
./check-updates
```

### safeupdate
Safely update Arch Linux with Btrfs snapshots.

```bash
sudo ./safeupdate
```
