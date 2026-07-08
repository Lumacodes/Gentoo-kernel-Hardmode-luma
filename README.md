
# Gentoo-kernel-unbloatedxLuma

This is a fully manual Gentoo kernel configuration tuned ONLY for AMD CPUs.  
Intel support is completely removed. If you try to boot this config on an Intel CPU, **your system will not boot**.  
This kernel is stripped down aggressively — only the bear_minimum 

![AMD-only kernel config screenshot](https://github.com/Lumacodes/Gentoo-kernel-Hardmode-luma/blob/main/screenshot-2025-11-28_22-34-17.png)
---

## ⚠️⚠️⚠️ IMPORTANT WARNING (READ BEFORE USING)

**If you have an Intel CPU:  
DO NOT USE THIS CONFIG.  
Your machine will NOT boot.**  
Intel CPU drivers, Intel platform support, Intel ACPI quirks, Intel thermal drivers, Intel iGPU, i915, Intel P-states, and multiple Intel subsystems have been manually disabled.

This kernel is **AMD-only, no exceptions**.

Even some AMD features are disabled if I don’t use them, so this is not a “universal AMD kernel” either.  
This is a **minimal, personal, hand-built config**.

---

## 🧱 How This Kernel Was Built

- Installed Gentoo manually from a **stage3 tarball**
- Chrooted from another Linux system into `/mnt/gentoo`
- Built everything manually (no genkernel, no auto-kernel)
- Used `make menuconfig` to disable:
  - Intel CPU support  
  - Intel power management  
  - Intel ACPI platform drivers  
  - Intel network, GPU, and chipset modules  
  - AMD features I don’t use  
  - Filesystems and drivers I don’t need  
- Kernel is designed to be:
  - **minimal**
  - **fast**
  - **small in size**
  - **clean from unnecessary complexity**

This config was created during a real-world Gentoo install on a separate HDD (`/dev/sda`), not in a VM.

---

## 🎯 What This Kernel Is Optimized For

### ✔ AMD CPUs Only  
(Modern Ryzen / Zen architectures)

### ✔ Minimal hardware support  
Only the hardware I use is enabled.  
Anything unnecessary was turned off.

### ✔ Small kernel size  
Unused AMD modules also removed to shrink the build.

### ✔ Clean & fast boot  
Only essential drivers compiled built-in.

### ✔ Transparent learning  
I manually toggled every subsystem.

---

## ❌ What This Kernel DOES NOT Support

- Intel CPUs  
- Intel iGPU (i915)  
- Intel P-state / C-state / SpeedStep  
- Intel ACPI-specific drivers  
- Intel WiFi / Bluetooth / Thunderbolt  
- Intel storage controllers  
- Old legacy hardware  
- Generic “everything enabled” distro compatibility  
- Random filesystems (only the ones I use are enabled)  
- Exotic USB, HID, sound cards, old GPUs, etc.

If your system needs ANY of these:  
You must re-enable them manually in `menuconfig`.

---

## 📦 Using This Kernel Config

Place it in your Linux source directory:

```sh
cp gentoo-kernel-hardmode-luma /usr/src/linux/.config
```
## I Have Rent To Pay :) ...
<div align="center">
  <a href="https://ko-fi.com/lumacodes" target="_blank">
    <img src="https://cdn.ko-fi.com/cdn/kofi3.png?v=3" alt="Support Me on Ko-fi" height="50">
  </a>
</div>
