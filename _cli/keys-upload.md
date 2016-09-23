---
title: keys upload
layout: page
---

Upload an SSH public key to Stolos.

## Usage

```
Usage: stolos keys upload [OPTIONS] [PUBLIC_KEY_PATH]

  Upload an SSH public key to Stolos

Options:
  --stolos-url TEXT  The URL of the Stolos server to use, if not the default
  --name TEXT        The name of this key, default to this machine's hostname
  --help             Show this message and exit.
```

## Example

```
$ stolos keys upload
Public key ~/.ssh/id_rsa.pub uploaded successfully
```
