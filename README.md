<h2 align="center">
  <a href=#><img src="https://raw.githubusercontent.com/armbian/.github/master/profile/logosmall.png" alt="Armbian logo"></a>
  <br><br>
</h2>

### Purpose of This Repository

The **Armbian firmware** repository provides a curated set of binary firmware files required by various hardware components on ARM-based single board computers (SBCs) supported by Armbian.

### Purpose

- Distribute essential **proprietary firmware blobs**.
- Enable **Wi-Fi**, **Bluetooth**, **GPU**, **VPU**, and other peripherals.
- Ensure **hardware compatibility** out-of-the-box.
- Provide a **leaner alternative** to full upstream `linux-firmware` packages by including only relevant firmware for supported boards.

### Usage in Armbian

- Packaged as `armbian-firmware` and installed automatically during OS setup or upgrades.
- Used by Armbian's custom kernels and U-Boot bootloaders to support board-specific features.

### Includes Firmware for

- Realtek and Broadcom Wi-Fi/Bluetooth chips
- Mali and other ARM GPU/VPU components
- Various embedded controllers, USB devices, and more

### Structure

The layout generally follows upstream `linux-firmware` standards, with additional Armbian-specific filtering and optimizations.

> ⚠️ Note: Some firmware files are proprietary and distributed under their respective licenses. Redistribution is limited to non-commercial or usage-only contexts.
