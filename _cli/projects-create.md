---
title: projects create
layout: page
---

Create a new Stolos project.

## Usage

```
Usage: stolos projects create [OPTIONS] STACK PROJECT_DIRECTORY

  Create a new Stolos project

Options:
  --public-url TEXT  The public URL of your project, defaults to random hex
  --stolos-url TEXT  The URL of the Stolos server to use, if not the default
  --help             Show this message and exit.
```

## Example

```
$ stolos projects create sourcelair/stolos stolos
Assigning random public URL "sourcelair-stolos-akalipetis-czimkp.akalipetis.sourcelair.stolos.io"
Creating project "stolos"...		Ok.
Project "stolos" is ready! Change directory with "cd stolos" and run "stolos up" to launch it!
```