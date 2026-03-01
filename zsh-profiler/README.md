# zsh-profiler

Zsh startup profiler - measure load time per plugin.

## Features

- **Load Time** - Total Zsh startup time
- **Slowest Plugins** - Shows plugins taking the most time
- **Duplicate Detection** - Finds duplicate source statements
- **Bar Visualization** - Visual representation of load times

## Usage

```bash
./zsh-profiler              # Profile with colors
./zsh-profiler --plain     # Plain text output
./zsh-profiler -s 20       # Set slow threshold to 20ms
./zsh-profiler --help      # Show help
```

## Example Output

```
󰨰 Zsh Startup Profiler

  zsh load: 178ms

Slowest:
  copilot.lua     45ms ███████████
  nvm             32ms ████████
  zsh-autosuggest 28ms ███████

Files sourced: 4
Plugins: 3
```
