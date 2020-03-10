+++
title = "Faster Scientific Python"
subtitle = "When you're computation-bound, what are your options?"
date = "2020-02-09"
categories = ["Programming", "Software"]
+++

*\[epistemic status: hastily written, high-level overview lacking practical grounding\]*

# Bottlenecks

Python isn't known for it's speed. It has a [purposefully dumb interpreter](https://nullprogram.com/blog/2019/02/24/) which gets blown out of the water (in terms of throughput, memory consumption, and start-up speed) by almost all compiled languages. This is usually fine, because you're just trying to ship a gosh-darned website or quickly whip together a data-cleaning pipeline. Typically, other bottlenecks, such as network speed, memory access times, algorithmic approach, or the ability to scale across multiple machines take precedence.

But sometimes the throughput of your code and it's memory consumption on a single CPU-only machine _is_ the primary limitation. In my experience, this typically happens when you're dealing with scientific code. Specifically, when you're operating on large collections of array-structured data, often using the Numpy and Pandas libraries.

For example, Python has been a computational bottleneck for me when I was [implementing Dynamic Time Warping](https://github.com/Seanny123/pydtw) and when developing the [Nengo](https://www.nengo.ai/) CPU backend.

## Getting the details right

Before going wild with alternative interpreters, libraries or even a totally new language, it's important to make sure you're using Numpy and Pandas correctly.

### Proper use of Numpy and Pandas APIs

I assume you've already seen for yourself how Numpy and Pandas are faster than raw Python code. The internals of [how they do things faster](https://towardsdatascience.com/decoding-the-performance-secret-of-worlds-most-popular-data-science-library-numpy-7a7da54b7d72) is outside of the scope of this post. Basically, Pandas and Numpy store tables and arrays in a special format which allows for quick access from memory, takes up little space and run super fast in parallel using specialized CPU instructions.

However, Numpy and Pandas are only fast for certain use cases. Specifically, when writing Numpy and Pandas code, it is important to:

1. Avoid loops; they’re slow and often  unnecessary.

2. If you must loop, use built-in iterators, such as `group_by()` and `apply()`, instead of iterating over structures.

3. Operate on the whole array, series or DataFrame without indexing or iteration. This is typically called "vectorisation".

This is covered in greater depth in [this Pandas](https://engineering.upside.com/a-beginners-guide-to-optimizing-pandas-code-for-speed-c09ef2c6a4d6) and [this Numpy](https://scipy-lectures.org/advanced/optimizing/index.html#writing-faster-numerical-code) blog-post.
If you're using the Numpy and Pandas libraries, you gotta use them right.

If you're having trouble with vectorisation and using features correctly, I recommend posting questions on Code Review StackExchange. It helped me understand [Numpy vectorisation techniques](https://data.stackexchange.com/codereview/query/1197665/codereview-numpy) and [Pandas `group_by()`](https://codereview.stackexchange.com/q/166141/39441).

### Backends

Pandas and Numpy are essentially high-level interfaces to libraries of highly optimized numerical operations, such as MKL, OpenBLAS and Atlas. The performance of these libraries is extremely hardware-dependent. For example, MKL tends to work poorly on AMD hardware and should be replaced with OpenBLAS. In my experience, the easiest way to do this is by installing `numpy` with `conda`. However, if you really need every ounce of performance possible, each backend should be profiled and considered.

Sometimes using vectorized Numpy code isn't enough and you need to get weird. For example, Nengo implemented a computational graph compiler, discussed in [this PR](https://github.com/nengo/nengo/pull/1035) and [this paper](http://compneuro.uwaterloo.ca/publications/gosmann2017.html). Basically, many small Numpy computations were combined into fewer Numpy computations operating on larger arrays. This allowed the code to spend less time in Python and more time running Numpy routines.

Although carefully using and configuring Numpy and Pandas gets you quite far, you may eventually need to attack Python's interpreter speed itself.

# Desiderata

Ideally, any method that makes Python faster, should have the following features:

- Easy to integrate with Python
- Easy to debug, ideally with a graphical debugger
- Has a good community, either on StackOverflow or a custom forum

# Options

## Using a different interpreter

Python's default interpreter is CPython. There are alternative interpreters, such as Jython (for integrating with Java applications) and IronPython (for integrating with .Net applications), but the most up-to-date interpreter is PyPy. PyPy makes Python a JIT compiled language, which greatly improves it's performance, both in terms of computational throughput and memory usage. However, PyPy has limited compatibility with CPython C API, which means certain modules cannot be run. For example, as of time of writing, Matplotlib is not supported, but support for Numpy was recently added.

This was [attempted with Nengo](https://github.com/nengo/nengo/pull/1166) a couple of years ago, but certain Numpy functionality was not supported. I would definitely try it for a new project.

## Staying in the Python ecosystem

### [mypy.c](https://github.com/python/mypy/tree/master/mypyc)

Python supports type annotations (also called "type-hints") using MyPy, which has been included in the core Python release, as of 3.5. Although the CPython interpreter [cannot be made faster](https://stackoverflow.com/q/43859626/1079075) with type-hints, type-hints can be used to compile Python code into Python C extensions.

This is currently being used in Black, the opinionated Python auto-formatter.

### Cython

If your Python code runs, then your Cython code will run. But you won't be able to debug it? Cython has explicit support for Numpy and Pandas datatypes.

There is the `cydb`, but that isn't a graphical debugger. I never got comfortable with command-line debuggers, but Cython may force me to finally make the plunge.

### Numba

Numba is weird and I don't understand it. But it [helped make Nengo way faster](https://github.com/nengo/nengo/pull/1482).

For more on using Pandas with Cython and Numba, see [the official docs](https://pandas.pydata.org/pandas-docs/stable/user_guide/enhancingperf.html#using-numba).

## Using a different language

If I absolutely must leave the Python ecosystem, I would like to still have:

- Sane developer tooling, like a package manager and graphical debugger
- Similar syntax which would still be legible to a Python developer. I'm not making my co-workers learn a whole new programming language.
- Easily distributable to my co-workers

For example, I would consider Haskell's syntax to be illegible to the average Python developer and would consider Zig's tooling to not be mature enough.

### Julia

I love Julia. I love it's aspirations as a language with easy prototyping and performance-tuning capabilities. I love how it combines a nice type-system with metaprogramming capabilities. I love Julia, but I know it's not ready.

Maybe one day Julia will replace Python for all High-Performance Computing problems, but that day has not yet arrived. Calling Julia from Python is way too hard. I dream of the day where I can compile a subset of Julia to a binary, which would be a lot easier to call from Python, without a PhD in Programming Language Theory and 5 years of experience with LLVM.

### C/C++

I'd really rather not. My ex-flatmate frequently said Julia was equivalent to C++ and I cannot yet articulate why I disagree with him. I mean, I can cite [a bunch of tweets](https://twitter.com/i/moments/1226639307710095360) from people smarter than I, but that's not a very cogent argument.

### Go

The new hotness for parallel systems. It doesn't look like Python and does have limitations in terms of low-level optimizations, which is a problem for this use-case.

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

I will report back with another blog post, once I am more experienced.
