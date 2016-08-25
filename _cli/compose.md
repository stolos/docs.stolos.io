---
title: compose
layout: page
---

Run Docker Compose commands in Stolos.

## Usage

```
Usage: stolos compose [OPTIONS]

  Run Docker Compose commands in Stolos

Options:
  --help  Show this message and exit.
```

## Example

```
$ stolos compose ps
                   Name                                 Command               State                 Ports
------------------------------------------------------------------------------------------------------------------------
84b22c56c7664334b6d8912fc98c2835_cache_1     docker-entrypoint.sh redis ...   Up      6379/tcp
84b22c56c7664334b6d8912fc98c2835_db_1        /docker-entrypoint.sh postgres   Up      5432/tcp
84b22c56c7664334b6d8912fc98c2835_watcher_1   ./check_n_run.sh make watch      Up
84b22c56c7664334b6d8912fc98c2835_wdb_1       /bin/sh -c wdb.server.py - ...   Up      0.0.0.0:32796->1984/tcp, 19840/tcp
84b22c56c7664334b6d8912fc98c2835_web_1       ./check_n_run.sh make dev        Up      0.0.0.0:32797->8000/tcp
84b22c56c7664334b6d8912fc98c2835_worker_1    ./check_n_run.sh make worker     Up
```