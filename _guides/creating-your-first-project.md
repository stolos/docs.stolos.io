---
title: Creating your first project
layout: page
---

After setting up Stolos on your computer you are ready to create your first project!

## Step 1 - Create a Stolos project

The first thing you have to do is create an empty directory to work on your Stolos project with your local tools and then create a Stolos project with the [`stolos projects create`](/cli/projects-create/) command.

### Example

```
$ mkdir my-project
$ stolos projects create sourcelair/stolos stolos
Assigning random public URL "sourcelair-stolos-akalipetis-czimkp.akalipetis.sourcelair.stolos.io"
Creating project "stolos"...		Ok.
Project "stolos" is ready! Change directory with "cd stolos" and run "stolos up" to launch it!
```

## Step 2 - Clone your repositories

Now that you have created a Stolos project and a local directory to work, you have to clone your project services' repositories into this directory, in order to be able to work on them with your local tools.

### Example

```
$ cd my-project
$ git clone git@github.com:company/first-service
$ git clone git@github.com:company/second-service
```

**Attention!** The names of the directories in which you will clone your services should correspond to the ones defined in your project's stack!

## Step 3 - Launch your services

Next, launch all of your project's services by running the [`stolos up`](/cli/up/) command in your terminal. This will launch all Docker containers needed to run your project on Stolos and will make sure to sync all your local files with Stolos in real time and vice versa.

**Attention!** To ensure your files are synced with Stolos you should either have [`stolos up`](/cli/up/) running or run [`stolos sync`](/cli/sync/) manually.

### Example

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
Okay.
db_1       | Logs here...
cache_1    | Logs here...
worker_1   | Logs here...
web_1      | Logs here...
```

## Step 4 - Start working

Now you are ready to start working on your first project! Open and edit any file you would like with the editor of your choice (saving your file will upload it automatically to Stolos!).

To view your application in your web browser, just run the [`stolos launch`](/cli/launch/) command in your terminal.

### Example

```
$ stolos launch
Opening http://sourcelair-stolos-akalipetis-zzqouw.sourcelair.stolos.io...`
```
