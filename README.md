<div align="center">

<img src="https://www.nvidia.com/content/nvidiaGDC/us/en_US/about-nvidia/legal-info/logo-brand-usage/_jcr_content/root/responsivegrid/nv_container_392921705/nv_container/nv_image.coreimg.svg/1776076920288/nvidia-logo-vert.svg" alt="Nvidia logo" width="260">

## NVIDIA Rebirth

**A minimal Nvidia driver package for low latency gaming.**

[![Version](https://img.shields.io/badge/version-1.2-76B900)](https://github.com/rakhalfps/Nvidia-Rebirth/releases) [![GPUs](https://img.shields.io/badge/GPUs-GTX%2010%20to%20RTX%2050-76B900?logo=nvidia&logoColor=white)](#supported-hardware) [![Platform](https://img.shields.io/badge/platform-Windows-0078D6?logo=windows&logoColor=white)](#install) [![Downloads](https://img.shields.io/github/downloads/rakhalfps/Nvidia-Rebirth/total?color=blue&label=downloads)](https://github.com/rakhalfps/Nvidia-Rebirth/releases) [![Discord](https://img.shields.io/badge/Discord-join-5865F2?logo=discord&logoColor=white)](https://discord.gg/krpUAHkf5m)

[Download v1.2](https://github.com/rakhalfps/Nvidia-Rebirth/releases/latest) | [Install](#install) | [What is removed](#what-is-removed-and-what-stays) | [Troubleshooting](#troubleshooting) | [FAQ](#faq)

</div>

---

Nvidia Rebirth is a stripped-down build of the official Nvidia graphics driver. It keeps the core driver and removes the parts a gaming PC does not need to run: telemetry, GeForce Experience and extra background services. The goal is a lighter install with fewer processes competing for your CPU, which helps input latency and frame pacing, especially on high refresh rate displays (144Hz and above).

The driver code itself is Nvidia's. Nvidia Rebirth repackages it with optional components left out and does not reverse engineer or modify the driver. CUDA, DirectX, OpenGL and Vulkan all stay fully supported, so the package suits creative and compute work as well as games.

**Version 1.2 is out.** Download it from the [Releases page](https://github.com/rakhalfps/Nvidia-Rebirth/releases/latest).

This project is independent. It is not affiliated with, endorsed by or supported by Nvidia Corporation.

> [!IMPORTANT]
> Always remove your current driver with Display Driver Uninstaller (DDU) in Safe Mode before installing. Installing over an existing driver can leave old files and services behind, which is the most common cause of problems. See [Install](#install).

## Highlights

Each point below says what changes in the package and what that means when you use it.

| Area | What changes | What it means for you |
|---|---|---|
| **Latency** | Telemetry, GeForce Experience and extra background services are removed, so fewer processes run alongside your game. | Less competition for CPU time and a more responsive feel, which matters most in fast competitive games where every millisecond of input delay counts. |
| **Frame pacing** | With less background work, frame delivery is less likely to be interrupted when the CPU or GPU is under heavy load. | Motion stays more even in demanding scenes, so frame times look steadier even when the average frame rate does not change. |
| **Privacy** | All telemetry and data collection that ship with the stock package are removed. | Your driver is not reporting usage data in the background, and there is no account-linked software running beside it. |
| **Footprint** | No GeForce Experience and no unneeded background services are installed. | A smaller install, a cleaner list of running processes and less to maintain or troubleshoot. |
| **Compatibility** | The core driver is untouched, so CUDA, DirectX, OpenGL and Vulkan all keep working. | Games, creative tools and compute workloads behave the same way they do on the stock driver. |
| **Hardware reach** | One package covers GTX 10 through RTX 50, on desktops and laptops, including Optimus systems. | You can use the same approach on a desktop gaming rig or a hybrid graphics laptop without a separate build. |
| **Transparency** | The project is open source and the full repository is available for review. | You can read exactly what the package does instead of trusting a black box. |

## Supported hardware

Nvidia Rebirth supports Nvidia GeForce GPUs from the **GTX 10 series through the RTX 50 series**, on both desktops and laptops. That covers the GTX 10 series as the oldest supported generation, the RTX 20, 30 and 40 series, and the RTX 50 series as the newest. If you are unsure about a specific model, check the release notes on the [Releases page](https://github.com/rakhalfps/Nvidia-Rebirth/releases) or ask on [Discord](https://discord.gg/krpUAHkf5m) before installing.

### System requirements

- **Operating system:** Windows. DDU, which this guide relies on, is a Windows tool.
- **Graphics hardware:** An Nvidia GeForce GPU from the GTX 10 series to the RTX 50 series.
- **Laptops:** Hybrid graphics (Optimus) laptops with an integrated GPU plus an Nvidia GPU are supported.
- **Displays:** Any display works. The package is tuned with high refresh rate gaming (144Hz and above) in mind.
- **Access:** Administrator rights, and the ability to boot into Safe Mode for the clean install.

### Not covered

GPUs older than the GTX 10 series are outside the supported range. AMD and Intel graphics are not covered either, because this is an Nvidia driver package.

## What is removed, and what stays

Nvidia Rebirth changes what is installed around the driver, not the driver itself.

### Removed

- **Telemetry:** Normally collects usage and system data and sends it back in the background. In Nvidia Rebirth it is removed, so nothing is collected or reported by the package.
- **GeForce Experience:** Normally the companion app for driver updates, game optimization and account features. It is removed on purpose to keep the install light, and updates are done manually from the Releases page instead.
- **Extra background services:** Normally helper services run alongside the driver and the companion app. They are removed, so fewer processes are running while you play.

### Kept

- **Core graphics driver:** Runs the GPU for display, 3D and compute. It is kept as official Nvidia code.
- **CUDA, DirectX, OpenGL and Vulkan:** The graphics and compute APIs used by games and creative software. They are fully kept, so existing games and apps keep working.
- **Nvidia Control Panel:** The settings for power management, V-Sync, display and 3D options. It is kept, so you can tune the driver as usual.
- **Hybrid GPU (Optimus) support:** Switches between integrated and Nvidia graphics on laptops. It is kept, so laptops behave normally.

### Not available as a result

- **ShadowPlay:** It depends on GeForce Experience. Use a separate recorder such as OBS if you record gameplay.
- **In-game overlay:** It also depends on GeForce Experience.

## Install

1. Download the latest release from the [Releases page](https://github.com/rakhalfps/Nvidia-Rebirth/releases/latest).
2. Create a system restore point so you can roll back if anything goes wrong.
3. Boot into Safe Mode and remove your current Nvidia driver with [Display Driver Uninstaller (DDU)](https://www.wagnardsoft.com/).
4. Restart Windows normally.
5. Run the Nvidia Rebirth installer and follow the on-screen instructions.
6. Optional: open Nvidia Control Panel and adjust power management, V-Sync and other settings to taste.

If you also want a different driver version later, repeat steps 3 to 5 with the new package rather than installing over the top.

## After installing

- **Power management and V-Sync** are set in Nvidia Control Panel, as with the stock driver.
- **Recording and overlay** features such as ShadowPlay are not part of this package. If you record gameplay, use a separate recorder such as OBS.
- **Updates** are manual. Watch the Releases page and install new versions the same clean way.

## Updating

Nvidia Rebirth does not update itself. When a new release appears:

1. Download it from the [Releases page](https://github.com/rakhalfps/Nvidia-Rebirth/releases/latest).
2. Remove the current driver with DDU in Safe Mode.
3. Restart, then run the new installer.

## Troubleshooting

### ▸ Installer fails or reports a conflict

An older Nvidia driver or its services are usually still present. Remove everything with DDU in Safe Mode, restart, and run the installer again.

### ▸ Black screen or no signal after install

Restart the PC and, if needed, boot into Safe Mode. Use DDU to remove the driver, restart, and reinstall. If the problem repeats, restore your system restore point and report it with your GPU model and Windows version.

### ▸ Nvidia Control Panel settings are missing or reset

Open Nvidia Control Panel again after a restart. If a setting still looks wrong, set it manually. A clean install resets the panel to defaults, so reapply your preferences.

### ▸ ShadowPlay or the overlay is missing

This is expected. Both require GeForce Experience, which Nvidia Rebirth does not include.

### ▸ Games or apps behave differently after switching drivers

Clear the shader cache for the game, or let it rebuild on the next launch. If an app that relies on CUDA, DirectX, OpenGL or Vulkan fails, report it with the app name and the error shown.

### ▸ Going back to the stock driver

Remove Nvidia Rebirth with DDU in Safe Mode, restart, then install the official driver from Nvidia.

## FAQ

**Will this raise my FPS?**
The focus is latency and frame stability. Any change in average FPS depends on your system and the game.

**Is it safe for my hardware?**
The core driver is official Nvidia code with telemetry and extras removed. As with any driver change, create a restore point first.

**Is it legal?**
Nvidia Rebirth repackages official Nvidia drivers with optional components left out. Nvidia's own license terms still apply to the driver, so review them before use.

**Does it work on laptops?**
Yes, including hybrid GPU (Optimus) laptops.

**Can I add GeForce Experience back?**
It is possible, but not recommended, because it can affect performance and stability and defeats the purpose of this package.

**Does it work for creative and compute workloads?**
Yes. CUDA, DirectX, OpenGL and Vulkan are all kept.

**Can I read the source?**
Yes. Everything is open source in this repository.

## Privacy

Nvidia Rebirth removes the telemetry and data collection that ship with the stock Nvidia package. It has no server of its own and collects nothing. Downloading a release from GitHub is subject to GitHub's own privacy practices, and GitHub sees your IP address as any site you visit does.

## Support

- Questions and discussion: [Discord](https://discord.gg/krpUAHkf5m)
- Bugs and feature requests: [GitHub Issues](https://github.com/rakhalfps/Nvidia-Rebirth/issues)

When you report a problem, include your GPU model, Windows version, the Nvidia Rebirth version and what you saw. Screenshots of any error message help.

## License

See the repository for license details. Nvidia, GeForce, CUDA and related names are trademarks of Nvidia Corporation. Windows is a trademark of Microsoft. This project is not affiliated with either company.
