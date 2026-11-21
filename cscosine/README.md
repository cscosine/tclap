# tclap: the cscosine copy

TCLAP (Templatized C++ Command Line Parser, header-only), as built and released by
[third_party_base_libs](https://github.com/cscosine/third_party_base_libs) for the cscosine projects. Not maintained as
a fork (no syncs with upstream): it is to be replaced; until then it stays as it is.

| | |
|---|---|
| Came from | <https://sourceforge.net/projects/tclap/>, through the GitHub mirror <https://github.com/mirror/tclap> |
| Base | upstream `master`, commit `8b35dd1` (2020-12-30, "Add example for how to use a pair as a custom type."): the 1.4 development line, never released as 1.4 (the last release is 1.2.5) |
| Our version | `1.0.0` (`project()` of our `CMakeLists.txt`): a version of our own |
| License | upstream's (`COPYING`, MIT) |

## What we changed

A csCMake project around the headers: the headers moved from `include/tclap/` to `tclap/`, our `CMakeLists.txt`
(package `tclap`), `CMakePresets.json` and `csCMakeProjectSetup.json` (csCMake presets), the examples built with it,
a VS Code workspace. `git log 8b35dd1..main` lists the commits.
