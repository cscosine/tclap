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
<!-- cs-template:end -->
