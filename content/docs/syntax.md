---
weight: 200
title: "Syntax"
description: "Overview of Comfy's syntax and structure."
icon: "article"
date: "2025-07-20T18:13:18+02:00"
lastmod: "2025-07-20T18:13:18+02:00"
draft: false
toc: true
---

Comfy's syntax is designed to be simple and intuitive, making it easy for developers to write and understand code. Below are some of the key syntax elements in Comfy.

## Functions
Functions in Comfy are defined using the `fn` keyword, followed by the function name and parameters. The body of the function is enclosed in curly braces `{}`.

```comfy
fn main() {
    $write(1, "Comfy world!\n");
    $exit(0);
}
```
> Note how we need to call the `exit` syscall at the end of the program just like we would in assembly or C. This is because Comfy is a low-level language that interacts directly with the operating system.

## Variables
Comfy is a statically typed language, meaning you must declare the type of a variable when you create it. Currently supported types are `bool`,
`char`, `int8`, `int16`, `int32` and `str`. All variables are immutable by default. If you want to create a mutable variable, use the `mut` keyword before declaring a type.

```comfy
fn main() {
    mut int32 x = 42;
    x = 100; // This is allowed because x is mutable

    $exit(x);
}
```

## Syscalls
Comfy provides handy abstractions to syscalls, allowing you to interact with the operating system directly. You can use the `$` prefix to call syscalls.

```comfy
fn main() {
    $write(1, "Hello, Comfy!\n");
    $exit(0);
}
```
> Syscalls are specific to the architecture and operating system you are compiling for. To select the target architecture, you can set the `arch` field in your `project.comfx` file. For example, to compile to arm32, you would set `arch = "arm32"`.