---
title: projects create
layout: cli_page
---

Create a new Stolos project.

## Usage

```
Usage: stolos projects create [OPTIONS] PROJECT_DIRECTORY

  Create a new Stolos project

Options:
  --public-url TEXT               The public URL of your project, defaults to
                                  random hex
  --subdomains / --no-subdomains  If this project should use subdomains for
                                  services, defaults to false
  --stolos-url TEXT               The URL of the Stolos server to use, if not
                                  the default
  --stack TEXT                    The stack to use for this project, defaults
                                  to no stack
  --help                          Show this message and exit.
```

## Example

```
$ stolos projects create sourcelair/stolos stolos
Assigning random public URL "sourcelair-stolos-akalipetis-czimkp.akalipetis.sourcelair.stolos.io"
Creating project "stolos"...		Ok.
Project "stolos" is ready! Change directory with "cd stolos" and run "stolos up" to launch it!
```