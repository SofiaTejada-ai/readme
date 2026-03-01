#Project 1 Instructions



## Files

- `filecopy.c` — main program source


## Requirements

### Linux
- `gcc` (or `clang`)
- POSIX environment (standard on Linux)

### macOS
- `clang` (comes with Xcode Command Line Tools)

Install tools:
- **Ubuntu/Debian**: `sudo apt-get update && sudo apt-get install -y build-essential`
- **macOS**: `xcode-select --install`

---

## Compile

### GCC (recommended)
```bash
gcc -Wall -Wextra -Wpedantic -O2 -std=c11 filecopy.c -o filecopy
