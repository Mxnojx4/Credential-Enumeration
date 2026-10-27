```ruby
 ██████╗██████╗ ███████╗██████╗ ███████╗███╗   ██╗██╗   ██╗███╗   ███╗
██╔════╝██╔══██╗██╔════╝██╔══██╗██╔════╝████╗  ██║██║   ██║████╗ ████║
██║     ██████╔╝█████╗  ██║  ██║█████╗  ██╔██╗ ██║██║   ██║██╔████╔██║
██║     ██╔══██╗██╔══╝  ██║  ██║██╔══╝  ██║╚██╗██║██║   ██║██║╚██╔╝██║
╚██████╗██║  ██║███████╗██████╔╝███████╗██║ ╚████║╚██████╔╝██║ ╚═╝ ██║
 ╚═════╝╚═╝  ╚═╝╚══════╝╚═════╝ ╚══════╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝     ╚═╝
```


> Post-access credential exposure detection for Linux systems, written in Nim.


## What It Does

- Scans Linux home directories for exposed credentials across 7 categories
- Detects unprotected SSH keys, plaintext cloud credentials, browser credential stores, shell history secrets, keyrings, Git tokens, and application credentials
- Classifies findings by severity based on file permissions and exposure risk
- Reports in terminal with color-coded output or structured JSON for automation
- Compiles to a single static binary with zero runtime dependencies

## Quick Start

```bash
bash install.sh
credenum
```

> Install: `curl -sSf https://just.systems/install.sh | bash -s -- --to ~/.local/bin`

## Stack

**Language:** Nim 2.2+ (ORC memory management)

**Build:** Just, Nimble, musl (static linking), UPX (compression), zigcc (cross-compilation)

**Testing:** Nim unittest, Docker (integration tests with planted credentials)

