# Contributing to XRT for ppc64le

Thank you for contributing to XRT (Xilinx Runtime) for IBM POWER8/POWER9 systems.

## Project Overview

XRT for ppc64le provides GPU acceleration support for AMD/NVIDIA GPUs on IBM POWER8 and POWER9 systems via the XRT runtime environment.

## Development Setup

### Prerequisites

- IBM POWER8 (ppc64le) or POWER9 system
- Xilinx Alveo accelerator card (U200, U250, U280)
- Linux kernel 4.14+ on ppc64le
- XRT 2.13+ installed

### Environment Setup

```bash
git clone https://github.com/Scottcjn/xrt-ppc64le.git
cd xrt-ppc64le
make
sudo make install
```

## Building

```bash
# Build for ppc64le
make ppc64le

# Build for POWER9 specifically
make POWER9=1

# Run tests
make test
```

## Testing

```bash
# Hardware validation tests
./tests/validate.sh --card 0

# Performance benchmarks
./tests/benchmark.sh --device all
```

## Submitting Changes

1. Fork the repository
2. Create a branch: `git checkout -b fix/your-fix`
3. Test on real POWER hardware when possible
4. Submit a pull request

## Ideas for Contributions

- Additional Alveo card support (U50, U45)
- POWER10 compatibility
- Performance improvements for specific kernels
- Bug reports for hardware compatibility
