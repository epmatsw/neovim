![Neovim](https://raw.githubusercontent.com/neovim/neovim.github.io/master/logos/neovim-logo.png)

[Website](http://neovim.org) |
[Google Group](https://groups.google.com/forum/#!forum/neovim) |
[Twitter](http://twitter.com/Neovim) |
[Reddit](http://www.reddit.com/r/neovim) |
[Bountysource](https://www.bountysource.com/teams/neovim)

[![Build Status](https://travis-ci.org/neovim/neovim.svg?branch=master)](https://travis-ci.org/neovim/neovim)
[![Stories in Ready](https://badge.waffle.io/neovim/neovim.png?label=ready)](https://waffle.io/neovim/neovim)
[![Coverage Status](https://img.shields.io/coveralls/neovim/neovim.svg)](https://coveralls.io/r/neovim/neovim)
[![Coverity Scan Build](https://scan.coverity.com/projects/2227/badge.svg)](https://scan.coverity.com/projects/2227)
[![Clang Scan Build](http://neovim.org/doc/reports/clang/badge.svg)](http://neovim.org/doc/reports/clang)
[![Bountysource](https://www.bountysource.com/badge/tracker?tracker_id=461131)](https://www.bountysource.com/trackers/461131-neovim?utm_source=461131&utm_medium=shield&utm_campaign=TRACKER_BADGE)

Neovim is a project that seeks to aggressively refactor Vim in order to:

- Simplify maintenance and encourage contributions
- Split the work between multiple developers
- Enable the implementation of new/modern user interfaces without any
  modifications to the core source
- Improve extensibility with a new plugin architecture

For lots more details, see
[the wiki](https://github.com/neovim/neovim/wiki/Introduction)!

### What's been done so far

- Cleaned up source tree, leaving only core files
- Removed support for legacy systems and moved to C99
    - Removed tons of `FEAT_*` macros with [unifdef]
    - Reduced C code from 300k lines to 170k
- Enabled modern compiler features and [optimizations](https://github.com/neovim/neovim/pull/426)
- Formatted entire source with [uncrustify]
- Replaced autotools build system with [CMake]
- Implemented [continuous integration] and [test coverage]
- Wrote 100+ new unit tests
- Split large, monolithic files (`misc1.c`) into logical units
  (`path.c`, `indent.c`, `garray.c`, `keymap.c`, ...)
- [Implemented](https://github.com/neovim/neovim/pull/475) job control ("async")
- Reworked out-of-memory handling resulting in greatly simplified control flow
- Merged 50+ upstream patches (nearly caught up with upstream)
- [Removed](https://github.com/neovim/neovim/pull/635) 8.3 filename support
- [Changed](https://github.com/neovim/neovim/pull/574) to portable format
  specifiers (first step towards building on Windows)

[unifdef]: http://freecode.com/projects/unifdef
[uncrustify]: http://uncrustify.sourceforge.net/
[CMake]: http://cmake.org/
[continuous integration]: https://travis-ci.org/neovim/neovim
[test coverage]: https://coveralls.io/r/neovim/neovim

### What's being worked on now

- Porting all IO to libuv
- Lots of refactoring
- A VimL => Lua transpiler
- Formatting with `clint.py`
- msg-pack remote API

### How do I get it?

There is a formula for OSX/homebrew, a PKGBUILD for Arch Linux,
and detailed instructions for building on other OSes.

See [the wiki](https://github.com/neovim/neovim/wiki/Installing)!

### Community

Join the community on IRC in #neovim on Freenode or the [mailing list](https://groups.google.com/forum/#!forum/neovim)

### Contributing

...would be awesome! See [the wiki](https://github.com/neovim/neovim/wiki/Contributing) for more details.

### License

Neovim is licensed under the terms of the Apache 2.0 license, except for
parts that were contributed under the Vim license.

- Contributions committed before [b17d96][license-commit] by authors who did
  not sign the Contributor License Agreement (CLA) remain under the Vim license.

- Contributions committed after [b17d96][license-commit] are licensed under
  Apache 2.0 unless those contributions were copied from Vim (identified in 
  the commit logs by the `vim-patch` token).

See `LICENSE` for details.

    Vim is Charityware.  You can use and copy it as much as you like, but you are
    encouraged to make a donation for needy children in Uganda.  Please see the
    kcc section of the vim docs or visit the ICCF web site, available at these URLs:

            http://iccf-holland.org/
            http://www.vim.org/iccf/
            http://www.iccf.nl/

    You can also sponsor the development of Vim.  Vim sponsors can vote for
    features.  The money goes to Uganda anyway.

[license-commit]: https://github.com/neovim/neovim/commit/b17d9691a24099c9210289f16afb1a498a89d803

<!-- vim: set tw=80: -->
