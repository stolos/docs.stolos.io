---
title: login
layout: cli_page
---

Simple command that logs you into Stolos, using your username and password. Your access token is being stored in `~/.stolos/config.yaml`.

## Usage

```
Usage: stolos login [OPTIONS]

  Log in to a Stolos environment

Options:
  --username TEXT    Your Stolos username
  --password TEXT    Your stolos password
  --stolos-url TEXT  The URL of the Stolos server to use
  --help             Show this message and exit.
```

## Example

```
$ stolos login --stolos-url=https://sourcelair.stolos.io
Username: paris
Password (typing will be hidden):
Authentication successful.
```