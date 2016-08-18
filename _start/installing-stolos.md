---
title: Installing Stolos
layout: page
---

This guide will help you install the Stolos Command Line Interface on your local machine, according to your operating system. Stolos works on all major operating systems (OS X, Windows and Linux).

## OS X

### 1. Install Unison

Install [**Unison**](https://www.cis.upenn.edu/~bcpierce/unison/) via [**Homebrew**](http://brew.sh/),  to enable the real-time file syncing feature of Stolos.

To do this run the following command in your terminal:

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install unison
```

### 2. Install Stolos

Run the following command in your terminal to install the Stolos Command Line Interface:

```
pip install https://cf979153cd14525475d4-f860d1dda29fa1b9bcbf643d12472ae9.ssl.cf1.rackcdn.com/stolosctl-0.1.zip#egg=stolos[compose]
```

## Windows

### 1. Set up Cygwin
First thing you need to do to install and work with Stolos on Windows is to setup [**Cygwin**](https://cygwin.com/) on your machine. To do this follow this steps

1. Download the 64-bit version of Cygwin from https://cygwin.com/install.html
2. Run `setup-x86_64.exe`
3. Install the following:
    - `openssh` from **Net**
    - `python` from **Python**
    - `unison2.48` from **Utils**
    - `wget` from **Web**

### 2. Install pip
Run the following command in the Cygwin terminal to install [**pip**](https://pip.pypa.io/):

```
python -m ensurepip
```

### 3. Install Docker Compose for Windows
Run the following command in the Cygwin terminal to install [**Docker Compose**](https://docs.docker.com/compose/) for Windows:

```
wget https://github.com/docker/compose/releases/download/1.8.0/docker-compose-Windows-x86_64.exe -O /usr/bin/docker-compose
```

### 4. Install Stolos
Run the following command in the Cygwin terminal to install the Stolos Command Line Interface:

```
pip install https://cf979153cd14525475d4-f860d1dda29fa1b9bcbf643d12472ae9.ssl.cf1.rackcdn.com/stolosctl-0.1.zip#egg=stolos
```

## Linux

### 1. Install Unison
Install [**Unison**](https://www.cis.upenn.edu/~bcpierce/unison/) to enable the real-time file syncing feature of Stolos.

To do this run the following command in your terminal:

```
wget https://cf979153cd14525475d4-f860d1dda29fa1b9bcbf643d12472ae9.ssl.cf1.rackcdn.com/unison/unison-2.48.3-4.02 -O /usr/local/bin/unison
```

## 2. Install Stolos

Run the following command in your terminal to install the Stolos Command Line Interface:

```
pip install https://cf979153cd14525475d4-f860d1dda29fa1b9bcbf643d12472ae9.ssl.cf1.rackcdn.com/stolosctl-0.1.zip#egg=stolos[compose]
```

After the installation procedure completes you will be able to use the `stolos` command in your terminal.
