[![Build status](https://ci.appveyor.com/api/projects/status/uo4k9ug54ngexai8/branch/master?svg=true)](https://ci.appveyor.com/project/universalctags/ctags-win32/branch/master)
[![Github All Releases](https://img.shields.io/github/downloads/universal-ctags/ctags-win32/total.svg)](https://github.com/universal-ctags/ctags-win32/releases)

# Universal Ctags Win32/64 daily builds

This project provides daily builds of [universal-ctags](https://ctags.io) for Win32/64.

You can download the zip packages from the [releases](https://github.com/universal-ctags/ctags-win32/releases) page.

Four types of packages are provided:

* `ctags-{ctagsver}-x64.zip`: x64 release build
* `ctags-{ctagsver}-x64.debug.zip`: x64 debug build
* `ctags-{ctagsver}-x86.zip`: x86 release build
* `ctags-{ctagsver}-x86.debug.zip`: x86 debug build

`{ctagsver}` is an exact tag name of the [ctags repository](https://github.com/universal-ctags/ctags) or a generated name in the format of `YYYY-MM-DD_{tag}-N-gHHHHHHHH`.
Normally you may want to use the release builds. If you need unstripped binaries for debugging, use the debug builds.

# Note

Starting from the build [2017-10-14/d9944ef9](https://github.com/universal-ctags/ctags-win32/releases/tag/2017-10-14%2Fd9944ef9), Universal Ctags doesn't load `~/.ctags` and other exuberant-ctags compatible configuration files.
See `man/ctags.1.html` and `man/ctags-incompatibilities.7.html` in the zip packages. Also refer to [#1519](https://github.com/universal-ctags/ctags/pull/1519).

Starting from the build [2019-10-03/70b44e7d](https://github.com/universal-ctags/ctags-win32/releases/tag/2019-10-03%2F70b44e7d), the default directory separator has been changed from `\\` to `/`. This should improve the compatibilities to Exuberant Ctags, however if you still have a compatibility issue, try `--output-format=e-ctags` option. Also refer to [#2199](https://github.com/universal-ctags/ctags/pull/2199) and [#1325](https://github.com/universal-ctags/ctags/issues/1325).

Starting from the build [2019-12-10/9f494f08](https://github.com/universal-ctags/ctags-win32/releases/tag/2019-12-10%2F9f494f08), Universal Ctags uses [the UTF-8 code page](https://docs.microsoft.com/en-us/windows/uwp/design/globalizing/use-utf8-code-page) on Windows 10 version 1903 or later. This allows you to use Unicode file names on u-ctags. Also refer to [#2360](https://github.com/universal-ctags/ctags/pull/2360) and [#1837](https://github.com/universal-ctags/ctags/issues/1837).

# License

Universal Ctags itself (which is in the ctags subdirectory) is licensed under GPL 2 (or later).

The build scripts in this repository are based on the [vim-win32-installer](https://github.com/vim/vim-win32-installer) project, and [the Vim license](http://vimhelp.appspot.com/uganda.txt.html#license) applies to them.
