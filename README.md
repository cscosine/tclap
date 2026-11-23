# tclap

TCLAP, the Templatized C++ Command Line Parser (header-only): the cscosine copy, built and released by
[third_party_base_libs](https://github.com/cscosine/third_party_base_libs); to be replaced. Upstream's README:
[README](README); where this copy comes from and what we changed: [cscosine/README.md](cscosine/README.md). The
upstream files are kept as they are: no hook touches them (the `exclude:` of `.pre-commit-config.yaml`).

<!-- cs-template:begin (this block is owned by cs-project-template: do not edit; the rest of the file is the project's) -->
## Getting started

tclap is built by the project that consumes it: no setup or build CI of its own. Formatting and checks:
`pre-commit install` once, then `pre-commit run --all-files` (also run by `.github/workflows/checks.yml`).

The shared files (setup, checks, CI, agent rules) come from
[cs-project-template](https://github.com/cscosine/cs-project-template); to bring them to its latest version, on a
branch: `copier update --defaults`.

## Working in VS Code

Once the project that builds tclap has built it (csorchestrator), open VS Code with `./open-code.sh [filter]`
(Windows: `.\open-code.ps1 [filter]`).
The filter is a part of the build folder name or of the compiler (`gcc`, `clang`, `msvc`, `clang-cl`),
needed when there are several builds.

The script writes a **workspace file** for the chosen build, `<build>/tclap.code-workspace`, and opens it
(not the folder): it holds the build's settings (build folder, configurations, IntelliSense, debugger). The window title
shows `tclap - <build>`. To come back: run the script again, or File > Open Recent and pick that
workspace. Opening the folder itself (`code .`) gives a window without the build: CMake Tools would ask for a kit and
configure a new build of its own. Each build has its own workspace file and window, so gcc and clang can be open side
by side. The builds are found from the csCMake layout of `csCMakeProjectSetup.json`; CMake is the one that made the
build (its path is in the build's `CMakeCache.txt`).

Needs VS Code with its `code` command on the PATH (the Linux packages and the Windows installer add it; otherwise the
script says which file to open by hand) and, on Linux, gdb to debug.

The first time in a window (VS Code remembers it):

1. CMake Tools asks "Select a kit": pick **`[Unspecified]`**, the build keeps its own compiler. CMake Tools then
   configures (Output, CMake).
2. Linux: clangd asks to install itself, or to disable the other IntelliSense: yes. Windows (Visual Studio builds):
   nothing to do, IntelliSense comes from CMake Tools.

Every day:

- The configuration (those of the build) and Build (F7): the status bar.
- Tests: the Testing view (Catch2: one entry per test case), run or debug one.
- The launch target (status bar): Run and Debug, "Debug the launch target" (F5, it builds first); with Catch2 also
  "Debug the launch target (Catch2 test spec)" (a test name or a `[tag]`).
- Install (for the next libraries, the deployments): command palette, "CMake: Install".
<!-- cs-template:end -->
