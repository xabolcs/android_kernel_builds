# Build Android Kernel

This uses .... for building Android kernel.


Example [workflow](./.github/workflows/main.yaml):

```yaml
name: CI

on:
  workflow_dispatch:

jobs:
  build-kernel:
    name: Build Kernel
    runs-on: ubuntu-20.04
    steps:
      - name: Build
        uses: dabao1955/kernel_build_action@main
        with:
          kernel-url: https://github.com/AcmeUI-Devices/android_kernel_xiaomi_cas
          branch: taffy
          config: cas_defconfig
          arch: arm64
          aosp-gcc: true
          aosp-clang: true
          python-27: true
          android-version: 12
          aosp-clang-version: r383902
```