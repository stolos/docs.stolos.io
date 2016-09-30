---
title: Troubleshooting
layout: page
permalink: /troubleshooting/
redirect_from:
  - /start/troubleshooting-stolos
---

This article will help you with any Stolos related problems you might encounter. It includes known issues, special cases and workarounds.

## Windows issues

### Execute permission is not supported in Windows
Since your services with stolos will run in a Unix environment, you might encounter cases where the execute permission has to be set.

#### Identifying the problem
If execution permission of a file is required in one of your services, you will notice that `stolos up` command will not be able to successfully start your services. Search your logs for something like `filename: Permission denied`.  
For example, in the following case, `web` service fails to start due to permission issues with `manage.py`:

```
web_1      | ./manage.py runserver 0.0.0.0:8000
web_1      | make: execvp: ./manage.py: Permission denied
```

#### Workaround
To change the permissions of a file you have to run something like:  
`stolos compose run -d service_name chmod +x filename`  
This will add execute permission to `filename` file.  
In the example above, `manage.py` of `web` service was not executable so it was fixed by running `stolos compose run -d web chmod +x manage.py`

### Interactive mode of docker compose is not supported in Windows

#### Identifying the problem
If you attempt to run `stolos compose run ...` or `stolos compose exec ...` you will notice that the command will fail with the following message:  
`Interactive mode is not yet supported on Windows. Please pass the -d flag when using 'docker-compose exec'.`

#### Workaround
As the error message suggests, add the `-d` flag on the command to run in detached mode.

## Node issues

### Installing libraries
Node projects save their dependencies inside the codebase. This means that even if the Dockerfile makes sure the `npm install` command runs, since the code is mounted inside Stolos projects, the Node installations will not be present.

#### Workaround
In order to make sure the Node dependencies are installed in your project, you should follow the following commands:

{% highlight bash %}
# First, fetch your code

# Then, create a new project
stolos projects create company/stack .

# Sync your files once, so that your package.json file lands in the server
stolos sync --oneoff

# Install dependencies - see below for the --unsafe-perm flag
stolos compose run --rm web npm install --unsafe-perm

# Start your project
stolos up
{% endhighlight %}

### Node warning: `npm cannot run in wd`
If you see the message above while installing dependencies, it means that one or more of your dependencies has a pre/post installation script. Since Stolos containers run as root, you need to instruct npm to run those scripts nevertheless.

### Workaround
When installing Node dependencies, remember to use the `npm install --unsafe-perm` flag. 
