---
title: up
layout: page
---

Run all your services and sync your files.

## Usage

```
Usage: stolos up [OPTIONS]

  Run all your services and sync your files

Options:
  -d, --detach        Sync files once and run services in the background.
  --logs / --no-logs  Print/Do not print services logs.
  --build             Build service images before starting service containers.
  --help              Show this message and exit.
```

## Example

```
$ stolos up
Syncing...
Okay.
Starting services...
Starting 84b22c56c7664334b6d8912fc98c2835_cache_1
Starting 84b22c56c7664334b6d8912fc98c2835_db_1
Starting 84b22c56c7664334b6d8912fc98c2835_worker_1
Starting 84b22c56c7664334b6d8912fc98c2835_web_1
Starting 84b22c56c7664334b6d8912fc98c2835_watcher_1
Started services at sourcelair-stolos-akalipetis-zzqouw.sourcelair.stolos.io
db_1       | Logs here...
cache_1    | Logs here...
worker_1   | Logs here...
web_1      | Logs here...
```
