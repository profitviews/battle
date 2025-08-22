# TA-Lib Installation Guide for Linux

This guide provides step-by-step instructions for installing the C library for TA-Lib (Technical Analysis Library) on Linux systems.

## Prerequisites

Before starting, ensure you have the following build tools installed:
- `gcc` (GNU C Compiler)
- `make` (Build automation tool)
- `wget` (File download utility)

### Check Prerequisites
```bash
which gcc make wget
```

## Installation Steps

### 1. Download Source Code
```bash
cd /tmp
wget http://prdownloads.sourceforge.net/ta-lib/ta-lib-0.4.0-src.tar.gz
```

### 2. Extract Archive
```bash
tar -xzf ta-lib-0.4.0-src.tar.gz
cd ta-lib
```

### 3. Configure Build
```bash
./configure --prefix=/usr/local
```

### 4. Compile Library
```bash
make
```

### 5. Install Library
```bash
sudo make install
```

### 6. Update Library Cache
```bash
sudo ldconfig
```

## Verification

### Check Installed Files
```bash
# Verify libraries
ls -la /usr/local/lib/libta_lib*

# Verify headers
ls -la /usr/local/include/ta-lib/

# Check version
ta-lib-config --version
```

## What Gets Installed

- **Libraries**: `/usr/local/lib/libta_lib.so*` (shared and static libraries)
- **Headers**: `/usr/local/include/ta-lib/` (all header files)
- **Utilities**: `/usr/local/bin/ta-lib-config` (configuration utility)

## Python
```bash
pip install TA-Lib
```
The Python package will automatically detect the installed C library.

## Troubleshooting

### Common Issues
- **Permission Denied**: Ensure you're using `sudo` for installation commands
- **Library Not Found**: Run `sudo ldconfig` after installation
- **Build Failures**: Verify you have all required build tools installed

### Alternative Installation Methods
- **Package Manager**: Some distributions may have TA-Lib packages available
- **Different Prefix**: Change `--prefix=/usr/local` to install in a different location

## System Requirements

- **OS**: Linux (tested on Ubuntu/Debian-based systems)
- **Architecture**: x86_64 (should work on other architectures)
- **Memory**: At least 512MB RAM for compilation
- **Disk Space**: Approximately 50MB for source and installation

## Notes

- Installation requires `sudo` privileges for system-wide installation
- The library is installed to `/usr/local/` by default
- Total installation time: approximately 5-10 minutes depending on system performance
- After installation, the library is available system-wide for all users

## Support

For more information about TA-Lib:
- [Official Website](http://ta-lib.org/)
- [SourceForge Project](https://sourceforge.net/projects/ta-lib/)
- [Documentation](http://ta-lib.org/documentation.html)

---

*This guide was created for Linux systems. For other operating systems, please refer to the official TA-Lib documentation.*
