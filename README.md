# Info on aptX lossless
This repo contains info about aptX lossless (potentially aptX Adaptive v3)

## What I know (beyond the basics)
- Runs on QDSP6/Qualcomm Hexagon (see `binaries/qdsp6/encoder/libaptXAdaptiveEnc3.so`
- Compiled with `QuIC LLVM Hexagon Clang 8.2.03 (based on LLVM 5.0.0git-42babe2)`
- Linked using `QuIC LLVM Hexagon Clang version Linker 5.0`

## What I currently have
- Binaries (from [here](https://github.com/arkq/openaptx/issues/8#issuecomment-1219831805))
- `strings` output (check `reveng/strings/libaptXAdaptiveEnc3.so.txt`)

## TODO
- Get running on qemu or other emulator (qemu apparently has a hexagon emulator, has to built from source on arch though...)
- Reverse engineer and document how aptX lossless works (won't make anything beyond what's required to build your own encoder/decoder public because that's not cleanroom)
- ???
- hopefully works on devices without qualcomm bluetooth/wifi chipsets (currently have a laptop with intel wifi + bluetooth with a spare realtek wifi+bluetooth card lying somewhere; my PC is using a Qualcomm QCNCM865/FastConnect 7800/WCN785x for Wifi 7 + Bluetooth 5.4, and apparently has BLE Audio support, but none of my devices besides my phone (Pixel 10) supports it)
