# XRT 2.21.70 for ppc64le (POWER8)

**First-ever build of Xilinx Runtime (XRT) for IBM POWER8 (ppc64le)**

## Build Info
- **Version**: XRT 2.21.70
- **Architecture**: ppc64le (POWER8)
- **Built On**: IBM Power System S824 (POWER8 16-core, 512GB RAM)
- **Build Date**: 2026-01-24
- **Ubuntu**: 20.04 LTS (Focal Fossa)

## Contents
- `bin/xrt-smi` - XRT System Management Interface
- `bin/xbmgmt` - XRT Board Management
- `bin/xclbinutil` - XCLBIN Utility
- `lib/` - Shared libraries (31 .so files)
- `python/` - Python bindings (pybind11)

## Installation
```bash
sudo cp bin/* /usr/local/bin/
sudo cp lib/*.so* /usr/local/lib/
sudo ldconfig
```

## Hardware Tested
- Xilinx Alveo U30 (device ID d03c)
- IBM Power System S824

## Build Notes
- Built from source with cmake patches for hwemu dependencies
- Required: `sed -i "s/xrt_hwemu/xrt_coreutil/g"` on CMakeLists.txt files
- Python bindings built against Python 3.8

## Credits
Built by Elyan Labs (elyan.io)


## 中文简介

Elyan Labs POWER 项目 - 为 IBM POWER 和复古系统提供现代支持。

Contributed by eelaine-wzw


## 中文简介

Elyan Labs 项目 - 为中文用户提供支持。

Contributed by eelaine-wzw
