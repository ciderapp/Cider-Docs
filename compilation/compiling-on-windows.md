---
description: >-
  This page allows you to figure out the steps and programs needed to compile
  your own version of Cider.
---

# Compiling on Windows

## Getting Started

Recommended / Required Development Utilities

* [NodeJS 14.0.0 or greater](https://nodejs.org/)
* [yarn](https://yarnpkg.com/) (_Optional, but highly recommended_)
* [Git](https://git-scm.com)
* [Python 3.8 or greater](https://www.python.org/downloads/)
* Basic Command Line Knowledge
* [windows-build-tools](https://github.com/nodejs/node-gyp#on-windows)

{% hint style="warning" %}
Yarn while not required it's **recommended** for compiling Cider and you can install it by using:

`npm install -g yarn`
{% endhint %}

{% hint style="danger" %}
You need windows-build-tools to be able to compile the native modules Cider uses for Windows. It should be installed with Node.js through the chocolatey package manager. If the installation fails you can install it using yarn/npm in an **administrator** powershell/cmd window and entering:

`yarn install -g windows-build-tools`

`or`

`npm install -g windows-build-tools`
{% endhint %}

### Cloning the repository

Open a command prompt window in the directory you'd like Git to clone to and enter the following command

```
git clone https://github.com/ciderapp/Cider.git
```

**Optionally**, if you'd like to use the **Development** branch of Cider to test upcoming features switch your branch by moving your terminal into the directory and using git to checkout the branch by entering the following commands&#x20;

```
cd Cider/
git checkout develop
```

{% hint style="success" %}
If you'd like to update your repository in the future to keep up to date use the command _(Make sure your in the directory you originally cloned in)_&#x20;

`git pull`
{% endhint %}

### Installing Dependencies

Now for the fun part, by using yarn or npm (we'll be using yarn in this case) enter the following command to automatically obtain all required dependencies for installation.

```
yarn install
```

{% hint style="info" %}
This step could take a little while on some machines.
{% endhint %}

### Compiling Cider

This step takes a little while on the first compilation so bare with it as it does what it needs to do.&#x20;

Compiling Cider for specific CPU architectures is a smart thing to do and you can do it by adding **switches** to the dist argument as displayed.

```
// For x86_64 machines. (Modern PC's)
yarn dist -w --x64

// For x86 ONLY machines. (Legacy PC's)
yarn dist -w --ia32
```

{% hint style="warning" %}
On some low-end machines this process could take up to \~5 minutes.
{% endhint %}

### Installing Cider

Your new Cider installation setup file is ready for you! You can find your setup executable in your cloned folder directory on your system in the subfolder `dist/` and from there you'll see your new Setup file.

{% hint style="success" %}
Congrats! You've successfully compiled your own build of Cider!
{% endhint %}
