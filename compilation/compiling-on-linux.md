---
description: >-
  This page allows you to figure out the steps and programs needed to compile
  your own version of Cider.
---

# Compiling on Linux

## Getting Started

Recommended / Required Development Utilities

* [NodeJS 14.0.0 or greater](https://nodejs.org/)
* [yarn](https://yarnpkg.com/) (_Optional, but highly recommended_)
* [Git](https://git-scm.com)
* [Python 3.8 or greater](https://www.python.org/downloads/)
* Basic Command Line Knowledge

{% hint style="warning" %}
Yarn while not required it's **recommended** for compiling Cider and you can install it by using:

`npm install -g yarn`
{% endhint %}
### Cloning the repository

Open a terminal window in the directory you'd like Git to clone to and enter the following command

```
git clone https://github.com/ciderapp/Cider.git
```

**Optionally**, if you'd like to use the **Development** branch of Cider to test upcoming features switch your branch by moving your terminal into the directory and using git to checkout the branch by entering the following commands&#x20;

```
cd Cider\
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

{% hint style="info" %}
Using npm in this stage may error out. to fix this, just simple use `--force` to supress the warnings.
{% endhint %}

### Compiling Cider

This step takes a little while on the first compilation so bare with it as it does what it needs to do.&#x20;

Compiling Cider for specific CPU architectures is a smart thing to do and you can do it by adding **switches** to the dist argument as displayed.

```
// For x86_64 machines. (Modern PC's)
yarn dist -l --x64

// For x86 ONLY machines. (Legacy PC's)
yarn dist -l --ia32
```

{% hint style="warning" %}
On some low-end machines this process could take up to \~10 minutes.
{% endhint %}

{% hint style="warning" %}
This command would build 3 seperate packages of Cider, AppImage, .deb, and .snap packages
{% endhint %}

### Compiling Cider from AUR

If you are on an arch-based Linux distribution and have an AUR helper (pacman/yay/paru/etc.), then you are in luck. Cider has 2 PKGBUILD's in the Arch User Repository.

Assuming you already have access to the AUR and have a friendly AUR helper (we will use `yay` for this example) enter the following command to automatically obtain all required dependencies for installation.

{% hint style="info" %}
If you like to live on the bleeding edge, use the `cider-git` package, this will compile directly from the [develop](https://github.com/ciderapp/Cider/tree/develop) branch.
{% endhint %}

```
yay -S cider
```

{% hint style="warning" %}
Running this on Node.js 17 or later will fail. This is due to Node.js 17 no longer writing `openssl_fips` to `config.gypi` so it's not there in Node.js 17's `process.config`. It is suggested to downgrade to ```nodejs-lts-gallium``` to resolve this issue.
{% endhint %}

### Installing Cider

Your new Cider installation setup file is ready for you! You can find your setup executable in your cloned folder directory on your system in the subfolder `dist/` and from there you'll see your new Setup files. Choose the installer that best matches your distro.

{% hint style="success" %}
Congrats! You've successfully compiled your own build of Cider!
{% endhint %}
