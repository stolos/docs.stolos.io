---
title: Testing with Stolos
layout: guides_page
---

Stolos makes it extremely easy to let others take a look on and test what you are working on, without needing any central staging or testing server.

## Step 1 - Copy your project

The first thing you have to do is copy the contents of your project's directory to a new one. Typically you do this by running `cp` in your terminal.

#### Example

```
$ cp -r my-project testing-project
```

### Step 2 - Start a Stolos project for testing purposes

Start a new Stolos project for testing by running the `stolos projects create STACK PROJECT_DIRECTORY` command in your terminal.

This command will provide you also with a dedicated Public URL to view your testing project.

#### Example

```
$ stolos projects create yourcompany/project testing-project
Assigning random public URL "yourcompany-testing-project-username-czimkp.username.company.stolos.io"
Creating project "testing-project"...        Ok.
Project "project" is ready! Change directory with "cd testing-project" and run "stolos up" to launch it!
```

> **PS:** Note your Public URL and share it with your colleagues to let them take a look and test what you are working on.

> In the above example the Public URL is **yourcompany-testing-project-username-czimkp.username.company.stolos.io**.

### Step 3 - Start your testing project's processes

Last you have to start your testing project's processes by getting inside your project's directory and running `stolos up -d` in your terminal. Also by using the `-d` flag, all processes are being run in the background, so you don't have to occupy your terminal for this.

#### Example

```
$ cd testing-project
$ stolos up -d
```

Now you are ready to share your project's Public URL with your colleagues and enjoy easier and faster testing.