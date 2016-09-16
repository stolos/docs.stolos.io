---
title: projects connect
layout: cli_page
---

Connect the current directory to an existing Stolos project.

## Usage

```
Usage: stolos projects connect [OPTIONS] PROJECT_UUID

  Connect the current directory to an existing Stolos project

Options:
  --stolos-url TEXT  The URL of the Stolos server to use, if not the default
  --help             Show this message and exit.
```

## Example

```
$ stolos projects connect 7c3bc55d-d7d5-40d4-8765-cbc2e41b1978
Connecting to project "7c3bc55d-d7d5-40d4-8765-cbc2e41b1978"...		Ok.
Your project is ready! Run "stolos up" to launch it!
```
