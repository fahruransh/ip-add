# ip-add

Format a proxy list: add an `http://`, `SOCKS4://`, or `SOCKS5://` prefix to every line that
is missing one, and make sure each line ends with a trailing `/`.

## How it works

`ip.py` asks for an input file, then asks which protocol to apply:

| Choice | Prefix added | Output file |
|---|---|---|
| 1 — HTTP | `https://` | `https.txt` |
| 2 — SOCKS4 | `socks4://` | `socks4.txt` |
| 3 — SOCKS5 | `socks5://` | `socks5.txt` |

Lines that already start with a protocol are left as-is (only the trailing `/` is added if
missing). An existing output file is replaced.

## Requirements

- Python 3 (standard library only — no extra packages needed)

## Usage

```bash
python ip.py
```

1. Enter the input file name (e.g. `input.txt`), one proxy per line.
2. Pick a protocol: `1` for HTTP, `2` for SOCKS4, `3` for SOCKS5.
3. The formatted list is written to `https.txt`, `socks4.txt`, or `socks5.txt`.

## Tech

- Python (standard library only)
