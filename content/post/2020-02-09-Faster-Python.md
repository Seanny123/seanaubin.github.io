+++
title = "Faster Scientific Python"
subtitle = "When you're computation-bound, what do you do?"
date = "2020-02-09"
categories = ["Programming", "Software"]
+++

*\[epistemic status: hastily written, high-level overview lacking practical grounding\]*

# Bottlenecks

Python isn't the fastest programming language out there. It's interpreted and it's interpreter is [purposefully dumb](https://nullprogram.com/blog/2019/02/24/). This is usually fine, because you're just trying to ship a gosh-darned website or quickly whip together a data-cleaning pipeline. Typically, other bottlenecks, such as network speed, memory access times, algorithmic limitatoins or user perception are important.

But sometimes, the throughput of your code and it's memory consumption is an actual limitation. In my experience, this typically happens when you're dealing with scientific code.

For example, Python has been a computational bottleneck for me when I was implementing Dynamic Time Warping and when developping the Nengo CPU backend.

# Desiderata

Ideally, any method that makes Python faster, should have the following features:

- Easy to integrate with Python
- Easy to debug, ideally with a graphical debugger
- Has a good community, either on StackOverflow or a custom forum

# Options

## Using a different interpreter

Python's defaut interpreter is CPython. There are alternative interpreters, such as Jython (for integrating with Java applications) and IronPython (for integrating with .Net applications), but the most up-to-date interpreter is PyPy. PyPy makes Python a JIT compiled language, which greatly improves it's performance, both in terms of computational throughput and memory usage. However, PyPy has limited compatibility with CPython C API, which means certain modules cannot be run. For example, as of time of writing, Matplotlib is not supported, but support for Numpy was recently added.

This was attempted with Nengo a couple of years ago, but certain Numpy functionality was not supported. I would definitely try it for a new project.

## Staying in the Python ecosystem

### [`mypy.c`](https://github.com/python/mypy/tree/master/mypyc)

Python supports type annotations (also called "type-hints") using MyPy, which has been included in the core Python release, as of 3.5. Although the CPython interpreter [cannot be made faster](https://stackoverflow.com/q/43859626/1079075) with type-hints, type-hints can be used to compile Python code into Python C extensions.

This is currently being used in the Black Python auto-formatter.

### cython

If your Python code runs, then your Cython code will run. But you won't be able to debug it?

There is the cydb, but that isn't a graphical debugger. I never got comfortable with command-line debuggers.


### Numba

Numba is weird and I don't understand it. But it helped make Nengo way faster.

## Using a different language

If I absolutely must leave the Python ecosystem, I would like to still have:

- Sane developer tooling, like a package manager and graphical debugger
- Similar syntax which would still be legible to a Python developper
- Easily distributable to my co-workers

For example, I would consider Haskell's syntax to not be legible to the average Python developer and would consider Zig's tooling to not be mature enough.

To be clear, this use case considers using Python to call a function written in another language. My co-workers know Python. I'm not making them learn a whole new programming language. I'm not rewriting our whole code-base for this project in a new language

### Julia

I love Julia. I love it's aspirations as a language with easy prototyping and performance-tuning capabilities. I love how it combines a pretty nice type-system with metaprogramming capabilities. I love Julia, but I know it's not ready.

Maybe one day Julia will replace Python for High-Performance Computing problems, but that day has not yet arrived. Calling Julia from Python is way too hard. I dream of the day where I can compile a subset of Julia to a binary without a PhD in Programming Language Theory and 5 years of experience with LLVM.

### C/C++

I'd really rather not. My ex-flatmate frequently said Julia was equivalent to C++ and I cannot yet articulate why I disagree with him. I mean, I can cite [a bunch of tweets](https://twitter.com/i/moments/1226639307710095360) from people smarter than I, but I don't feel like that's a very articulate argument.

### Go

The new hotness for parallel systems, Go. It doesn't look like Python and does have limitations in terms of low-level optimizations, which is a problem for this use-case.

### Rust

Looks even less like Python than Go. Super hard to learn coming from Python. No interactive debugger.

### Nim

Created with the intention to look like Python! Incredibly experimental. Integrates with Visual Studio Code and has a package manager. Has no debugger.

# Summary: There is no panacea

If you aren't using incompatible libraries, PyPy is a good idea.

If you have a small standalone function, you should probably start with Cython or Numba.

`mypy.c` is a really exciting tool, but is still experimental.

If the function causing the bottleneck looks like it can keep expanding in scope, you probably want to go to another language. I can't judge you for choosing Go, but I'd personally rather use Rust. However, I have not yet written anything substantial in either language, so my opinion is worthless.

I'm really cheering for Nim and Julia to keep getting better. They both have sustainable forms of funding, so the hope is still alive!

I will report back with another blog post
