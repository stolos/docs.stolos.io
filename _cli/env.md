---
title: env
layout: page
---

Display the commands to set up the environment for the Docker client.

## Usage

```
Usage: stolos env [OPTIONS]

  Display the commands to set up the environment for the Docker client

Options:
  --shell TEXT  Give the shell of your choice
  --help        Show this message and exit.
```

## Example

```
$ stolos env

export COMPOSE_PROJECT_NAME="6b99c479-fd68-4e27-9700-315b21059983"
export COMPOSE_FILE="/Users/akalipetis/Developer/sourcelair/docs.stolos.io/docker-compose.yaml"
export DOCKER_TLS_VERIFY="1"
export DOCKER_HOST="tcp://sourcelair.stolos.io:2376"
export DOCKER_CERT_PATH="/Users/akalipetis/Developer/sourcelair/docs.stolos.io/.stolos"
export STOLOS_REMOTE_DIR="/mnt/stolos/6b99c479-fd68-4e27-9700-315b21059983/"
export UNISON="/Users/akalipetis/Developer/sourcelair/docs.stolos.io/.stolos"

# Run this command to configure your shell:
# eval $(stolos env)
```
