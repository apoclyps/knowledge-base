---
title: "System Setup"
date: 2019-02-11T19:27:37+10:00
weight: 1
summary: "Configure your device and setup common system dependencies."
---

### Install Brew

Homebrew installs the stuff you need that Apple (or your Linux system) didn’t.

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Install Formation

Formation is a shell script to set up a macOS laptop for development. It can be run multiple times on the same machine safely. It installs, upgrades, or skips packages based on what is already installed on the machine.

The fork contained on [https://github.com/apoclyps/formation](https://github.com/apoclyps/formation) adds support for `brew taps` from [#17](https://github.com/minamarkham/formation/pulls) and adds additional backend dependencies.

```bash
git clone https://github.com/apoclyps/formation

cd formation

./slay 2>&1 | tee ~/slay.log
```
