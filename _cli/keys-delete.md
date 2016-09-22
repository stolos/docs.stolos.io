---
title: keys delete
layout: page
---

Delete an SSH public key.

## Usage

```
Usage: stolos keys delete [OPTIONS] PUBLIC_KEY_UUID

  Delete an SSH public key

Options:
  --stolos-url TEXT  The URL of the Stolos server to use, if not the default
  --help             Show this message and exit.
```

## Example

```
$ stolos keys delete 291f2a1a-2feb-43d8-9111-d8cd111ec056                                                      
Deleting SSH public key "291f2a1a-2feb-43d8-9111-d8cd111ec056"...    Okay.
```
