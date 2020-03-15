+++
title = "Faster Scientific Python"
subtitle = "What to choose when calling a different language"
date = "2020-02-09"
draft = true
categories = ["Programming", "Software"]
+++

*\[epistemic status: hastily written, high-level overview lacking practical grounding\]*

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
