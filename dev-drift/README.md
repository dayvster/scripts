# dev-drift

Dev Environment Drift Detector - scan projects for version mismatches.

## Features

- Detects version drift between global tools and project requirements
- Scans for Node, Rust, Zig, Go, Python version files
- Recursive scanning across multiple projects
- Warns on global vs project version mismatches
- Shows version conflicts across projects

## Usage

```bash
dev-drift                      # Scan current directory
dev-drift /path/to/project    # Scan specific directory
dev-drift -r /projects        # Recursive scan
dev-drift --plain             # No colors
```

## Scans For

- Node.js: package.json, .nvmrc, .node-version
- Rust: rust-toolchain.toml, rust-toolchain, Cargo.toml
- Zig: build.zig.zon, .zig-version
- Go: go.mod
- Python: pyproject.toml, requirements.txt

## Example Output

```
󰠮 Dev Environment Drift Detector

Global Versions:
  node   : v25.7.0
  rust   : 1.85.0
  zig    : 0.15.2

Scanning recursively...
Project Versions:
  /projects/web-app
    node: >=18
      ⚠ global node: v25.7.0
  /projects/api
    rust: stable

Drift Summary:
  ✓ No version conflicts
```
