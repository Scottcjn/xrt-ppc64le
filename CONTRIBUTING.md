# Contributing

Thanks for contributing to the XRT ppc64le build notes and artifacts. This repo
documents a POWER8 build of Xilinx Runtime, so changes should preserve
reproducibility and clearly identify the hardware and software stack used.

## Getting Started

1. Read `README.md` for the exact XRT version, architecture, build host, and
   installation layout.
2. Review `BCOS.md` for project context.
3. Work on a focused branch:

   ```bash
   git checkout -b your-change-name
   ```

## Development Workflow

Keep changes scoped to one category:

- Build documentation and dependency notes.
- Installation instructions for `bin/`, `lib/`, and Python bindings.
- Hardware compatibility notes for Alveo devices on POWER systems.
- Packaging or artifact metadata.

Avoid mixing binary artifact changes with documentation cleanup. If an artifact
changes, explain how it was produced and what source revision or patch set was
used.

## Validation

For installation or build changes, include:

- POWER system model and OS version.
- XRT version and source commit/tag.
- CMake, GCC/Clang, Python, and kernel versions.
- Alveo device model and device ID if tested.
- Commands run, such as `xrt-smi`, `xbmgmt`, or `xclbinutil`.

If you cannot test on POWER hardware, state that clearly and include static
validation such as command review, path checks, or packaging inspection.

## Documentation Guidelines

- Keep architecture labels explicit: `ppc64le`, POWER8, POWER9, Ubuntu/RHEL.
- Do not claim hardware support unless it was tested or sourced from upstream
  documentation.
- Include exact commands and expected outputs where possible.
- Note any manual patching needed for CMake or hardware-emulation dependencies.

## Pull Request Checklist

Before opening a PR, include:

- Summary of the build, install, or hardware area affected.
- Validation commands and outputs.
- Hardware/software environment used.
- Known limitations, untested paths, or follow-up work.

