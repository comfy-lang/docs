---
weight: 100
title: "Get Started"
description: "Tutorial on how to get started with programming in comfy."
icon: "article"
date: "2025-07-20T15:41:13+02:00"
lastmod: "2025-07-20T15:41:13+02:00"
draft: false
toc: true
---

**comfy** is a low-level, compiled scripting language similar to languages like C and Zig. It is designed to be simple and efficient, making it easy to write scripts that interact directly with the operating system. It is meant to provide a comfortable programming experience while maintaining low-level capabilities, including direct access to syscalls.

## Installation

The recommended way to install and use comfy is through the [cozy CLI tool](https://github.com/comfy-lang/cozy). This tool will help you manage your comfy installations and projects easily.

With cozy installed, simply run the following command to install the latest version of comfy:

```bash
$ cozy get-compiler
```

If you want to specfiy an installation path, you can use the `--path` option:

```bash
$ cozy get-compiler --path /path/to/your/comfy
```

## Compiling the Hello World Program

To get started, create a new comfy project using `cozy new`:

```bash
$ cozy new my-comfy-project
```

This will create a new directory called `my-comfy-project` with a basic Hello World program in it.

Next, navigate to your project directory:

```bash
$ cd my-comfy-project
```

The entry point to your newly created comfy project is located at `src/main.comfy`.

To run your comfy program, use the cozy CLI tool:

```bash
$ cozy run src/main.comfy
```

or if you want to simply compile it to a binary, you can use:

```bash
$ cozy build
```

The compiled binary will be located in the `/build` directory of your project.

## Learning More
To learn more about comfy, you can check out the [official documentation](https://docs.comfylang.org)