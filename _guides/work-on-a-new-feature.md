---
title: Work on a new feature
layout: page
---

Stolos makes it extremely easy to start working on a new feature with the least friction possible. There are two options on how to do this:

1. **the Stolos way** - with a dedicated project for this feature
2. **the traditional way** - reusing your existing project

## The Stolos way
Working on a new feature the Stolos way, means having a dedicated and disposable development environment for this feature. The benefits of this method is:

1. you have a clean slate for work
2. you don't have to switch between Git branches
3. you don't need a staging or QA server for testing

### Step 1 - Copy your existing project

The first thing you have to do is copy the contents of your existing project's directory to a new one. Typically you do this by running `cp` in your terminal.

#### Example

```
$ cp -r old-project new-project
```

### Step 2 - Create a branch for your feature

Most probably you are using Git or some sort of source control system to develop your software (e.g. Mercurial, SVN, TFS, etc.), so it's a good practice to start a fresh branch for your work.

#### Example (Git)

With Git you could do this by running the following command in your terminal

```
$ git checkout -b new-feature master
```

### Step 3 - Start a Stolos project for your feature

Start a new Stolos project for your feature by running the `stolos projects create STACK PROJECT_DIRECTORY` command in your terminal.

This command will provide you also for a dedicated Public URL to view your project, which you can share with your colleagues for testing purposes.


#### Example

```
$ stolos projects create yourcompany/project new-project
Assigning random public URL "yourcompany-new-project-username-czimkp.username.company.stolos.io"
Creating project "new-project"...        Ok.
Project "project" is ready! Change directory with "cd new-project" and run "stolos up" to launch it!
```

### Step 4 - Start your project's processes

Last you have to start your projects processes by getting inside your project's directory and running `stolos up` in your terminal.

#### Example

```
$ cd new-project
$ stolos up
```

Now you are ready to start developing this new feature and share your project's Public URL at any time with your colleagues for easier and faster testing.

## The traditional way

With Stolos you can treat your development environment as more permanent, like you we were used to and develop your new feature without changing a thing in your flow.
