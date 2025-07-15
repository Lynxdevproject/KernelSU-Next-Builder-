# 🔧 Universal Kernel Builder + KernelSU-Next

A GitHub Actions workflow for compiling Android kernels with optional KernelSU-Next root patch — powered by a flexible UI form, inspired by the original **Universal Kernel Builder** by [lynxdevproject](https://github.com/lynxdevproject). This is the root-enabled edition, designed for seamless CI rituals from source pull to flashable ZIP 🎯

## 🛠️ Features

- ✅ UI-based input form (source, branch, defconfig, packaging, developer tag)
- ✅ Toggle switch to inject [KernelSU-Next](https://github.com/KernelSU-Next/KernelSU-Next) root patch
- ✅ Safe compiler flags (`LLVM=1 LLVM_IAS=1`) for compatibility
- ✅ Android 14 Clang toolchain + GCC 4.9 (arm64 + arm32)
- ✅ Optional ZIP packaging via AnyKernel3
- ✅ Slim artifact upload (ZIP only + boot images)

## 🧙 KernelSU-Next Integration

Toggle `🔘 Enable KernelSU-Next patch?` in the workflow UI to inject KernelSU with:

## bash
'''git clone --depth=1 https://github.com/KernelSU-Next/KernelSU-Next.git KernelSU
bash KernelSU/tools/init_kernelsu.sh kernel-source

## 🧙 KernelSU-Next Integration

Toggle 🔘 Enable KernelSU-Next patch? in the workflow UI to inject KernelSU with:

bash
git clone --depth=1 https://github.com/KernelSU-Next/KernelSU-Next.git KernelSU
bash KernelSU/tools/init_kernelsu.sh kernel-source
`

The root patch is applied directly into your kernel source before compile.

🚀 How to Use

1. Go to Actions tab in your repo  
2. Select Universal Kernel Builder + KernelSU-Next  
3. Click Run workflow  
4. Fill in the following inputs:
   - 🔗 Kernel source repo (e.g. https://github.com/...)
   - 🌿 Branch name (e.g. main)
   - 🧪 Defconfig (e.g. begoniauserdefconfig)
   - 👤 Developer name/ID (e.g. lynx@workspace)
   - 📦 Use AnyKernel3 packaging (true/false)
   - 🔘 Enable KernelSU-Next patch (true/false)
   - 📝 Custom ZIP base name (optional)  

5. Let the shrine builder summon your kernel ZIP — uploaded as artifact and ready to flash

📦 Output Format

`
ReogKernelSU-lynx@workspace-2025-07-15_18-50.zip
`

## 🧪 Example Devices

- Redmi Note 8 Pro (begonia)
- POCO X3 Pro (vayu)
- Realme Narzo Series
- Redmi K20 Pro (raphael)
- POCO F5 (marble)
- Mi A2 (jasmine_sprout)

## 🙌 Credits

- Original Builder: lynxdevproject — the base CI framework with UI form magic
- Root Patch: KernelSU-Next by community contributors
- Packaging: AnyKernel3 maintained by osm0sis
- Toolchain Sources: LineageOS, AOSP

---

> “A shrine builder forged in CI. Rooted in ritual. Summoned with style.” 🔥🧙‍♂️
`

---
