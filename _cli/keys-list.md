---
title: keys list
layout: page
---

List your SSH public keys.

## Usage

```
Usage: stolos keys list [OPTIONS]

  List your SSH public keys

Options:
  --stolos-url TEXT  The URL of the Stolos server to use, if not the default
  --md5 / --sha256   The hasing algorithm to use, defaults to MD5
  --help             Show this message and exit.
```

## Example

```
$ stolos keys list
UUID                                  Name                  MD5
------------------------------------  --------------------  ---------------------------------------------------
f9c6c116-a9ae-410a-bf27-2c1a8adf0a30  akalipetis-mbp.local  MD5:ac:95:bd:2c:23:87:c9:74:f3:56:ba:25:27:21:34:50
```
