# fridump3 (Frida 17+ Compatible Fork)

This is a fork of [rootbsd/fridump3](https://github.com/rootbsd/fridump3) with improvements to ensure **compatibility with Frida 17.0.0 and later**.

## What's Changed

- **Updated Frida API usage** to reflect changes introduced in Frida 17+
- Fixed `session.create_script()` and memory reading API calls for new API structure
- Verified full functionality on Frida 17+ environments
- All original features (memory dump, section parsing, etc.) remain intact

## Requirements

- **Python** 3.8+
- **Frida** 17.0.0+

## Installation

```bash
git clone https://github.com/PeanutKingPeanut/fridump3
cd fridump3
```

Usage
---

```
usage: fridump [-h] [-o dir] [-u] [-H HOST] [-v] [-r] [-s] [--max-size bytes] process

positional arguments:
  process               the process that you will be injecting to

optional arguments:
  -h, --help            show this help message and exit
  -o dir, --out dir     provide full output directory path. (def: 'dump')
  -u, --usb             device connected over usb
  -H HOST, --host HOST  device connected over IP
  -v, --verbose         verbose
  -r, --read-only       dump read-only parts of memory. More data, more errors
  -s, --strings         run strings on all dump files. Saved in output dir.
  --max-size bytes      maximum size of dump file in bytes (def: 20971520)
```
