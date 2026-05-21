# netfix

DNS & connectivity troubleshooter for Linux.

## Usage

```bash
netfix              # quiet mode - curl result + issues only
netfix --verbose    # full diagnostic output
```

## What it does

1. Prompts for a target URL or IP
2. Gathers system info (interfaces, DNS config, firewall, connectivity)
3. Runs DNS lookups against multiple resolvers (1.1.1.1, 8.8.8.8, etc.)
4. Pings the target
5. Traceroutes the target
6. Fires a curl and shows HTTP status, timing, and response body
7. Reports any issues found

## Requirements

- `bash`
- `curl` (for HTTP tests)
- `dig` (for DNS lookups, optional)
- `ping`
- `traceroute` or `mtr` (optional)

## Installation

```bash
# Place anywhere in PATH, e.g.:
mv netfix ~/.local/bin/netfix
chmod +x ~/.local/bin/netfix
```

## Logs

Each run saves a timestamped log to `~/netfix/`.
