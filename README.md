# Packer Template for Fedora

![](https://img.shields.io/github/license/nickstamat/packer-fedora?style=flat-square)
![](https://img.shields.io/badge/fedora-31-3c6eb4?style=flat-square)

## Overview

This repository contains configuration for [Packer](https://www.packer.io/) to create VMware virtual machines running [Fedora](https://getfedora.org/) with a minimal set of packages.

## Motivation

Most of the time I do all software development in VMs due to their portability. Fedora is currently my go-to distribution for this purpose. However, being able to spin up such development boxes in a reproducible manner has been a problem that I wanted to tackle since my early days in the field. Packer proved to be the right tool for the job.

## What's in the Box

**Fedora version: 31**

The package groups specified in _http/kickstart.cfg_ will install a basic desktop environment, with only a few window managers (i3, awesome, and others).

The result is a lightweight system with (relatively) few packages, which is a great basis for my development boxes:

```
$ rpm -qa | wc -l
950
```

## How to Build

```
$ packer build fedora-31-x86_64.json
```
