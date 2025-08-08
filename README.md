# SuperRyzenS™ Sweet (MIUI)

This is a custom kernel for Redmi Note 10 Pro/Pro Max (codename: sweet) designed for MIUI ROMs, based on Linux kernel 4.14.356 with enhanced performance and power efficiency in mind.

## Features

- Based on latest stable tree (4.14.356)
- Full Link-Time Optimization (LTO)
- Inline Optimization
- Build with LLVM/Clang toolchain
- Optimized KCFLAGS=-O3
- Thin archives: CONFIG_THIN_ARCHIVES
- Support for MLGO, BOLT, PGO ready (optional, not yet merged)
- KernelSU with SuSFS patch included
- Dimens! Fix for MIUI display calibration

---

## How to Build

You can build it with GitHub Actions or locally.

### GitHub Actions

Just go to **Actions tab** and click Run workflow.

### Manual (for advanced users)

```bash
# Prepare environment  
export ARCH=arm64  
export PATH="$(PMD)/clang/bin:$(PMD)/gcc64/bin:$(PMD)/gcc/bin:$PATH"  
export KBUILD_BUILD_USER=runner  
export KBUILD_BUILD_HOST=slipzsix  
export LLVM=1  
export LLVM_IAS=1  
export CLANG_TRIPLE=aarch64-linux-gnu-  
export CROSS_COMPILE=aarch64-linux-android-  
export CROSS_COMPILE_ARM32=arm-linux-androideabi-

