# Assignment 00: Install required software

This assignment is meant to help you install the bsaic set of software tools that we will need for this course.

You will be doing all of the install in a command shell/terminal emulator.

## Mac users

1. Open a Terminal

2. Check to see if you have software installed or not.

You should already have VIM and CURL installed.
To check this, type `which vim` and `which curl`, respectively.

The output should look something like:

```
$ which vim
/usr/bin/vim
$ which curl
/usr/bin/curl
```

This works for all the software you are installing.

3. Install Git.

Follow the directions here to install Git if it is not already installed:

https://git-scm.com/book/en/v2/Getting-Started-Installing-Git#_installing_on_macos

4. Check SHELL.

To determine which shell you are using, type: `echo $SHELL`.

If it is not `/bin/bash`, then change the shell to bash with the `chsh` command:

```
chsh -s /bin/bash
```

## Windows users

1. Windows users must install the Windows Subsystem for Linux. 

Follow the instructions here to install it:

https://docs.microsoft.com/en-us/windows/wsl/install

The autograder runners use Ubuntu, so that is the safest bet for choosing a distribution.
You could also install Debian 11, which is very similar to Ubuntu.

2. Once you have installed WSL, you can start it by opening either a Command Shell or Powershell and typing `wsl`.

Now you will be able to follow the instructions for installing the rest of the software on Linux below.

## Linux users

1. You can install most everything you need all at once:

```
$ sudo apt install vim git curl
```

You can also check to see if something is installed (and see its full path) by typing `which` followed by whatever program you are looking for.

## EVERYONE

1. Install NVM.

The Node Version Manager (NVM) is package that helps you install, update, and switch between multiple versions of Node.js.

To install it, follow these directions:

https://github.com/nvm-sh/nvm#install--update-script

Since you have `curl` installed, you can run that entire first command:

```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```

2. Install Node.js.

We will be using the Long Term Support (LTS) version of Node.
This is the version that GitHub Actions (autograder) uses by default.

```
$ nvm install --lts
```

3. Check what version is installed:

```
nvm ls
->     v16.17.0
default -> lts/* (-> v16.17.0)
iojs -> N/A (default)
unstable -> N/A (default)
node -> stable (-> v16.17.0) (default)
stable -> 16.17 (-> v16.17.0) (default)
lts/* -> lts/gallium (-> v16.17.0)
lts/argon -> v4.9.1 (-> N/A)
lts/boron -> v6.17.1 (-> N/A)
lts/carbon -> v8.17.0 (-> N/A)
lts/dubnium -> v10.24.1 (-> N/A)
lts/erbium -> v12.22.12 (-> N/A)
lts/fermium -> v14.20.0 (-> N/A)
lts/gallium -> v16.17.0
```

You should see a v16 installed.

## Review

You should now have the following commands available on your system:

1. vim
2. curl
3. git
4. nvm
5. node
