# Nvidia Rebirth: Minimal Nvidia Driver for Low Latency Gaming!

![Cover](https://raw.githubusercontent.com/rakhalfps/Nvidia-Rebirth/124142ccbc11b8949b91383703d8b243ea138518/Media/Cover.png)

[![Downloads](https://img.shields.io/github/downloads/rakhalfps/Nvidia-Rebirth/total?color=blue)]()

---

**Nvidia Rebirth** is a minimal, performance-focused Nvidia graphics driver designed to reduce latency and improve frame stability by removing telemetry, GeForce Experience, and unnecessary background services. Ideal for competitive gamers and creators who demand responsive and smooth GPU performance.

- Supports GTX 10 to RTX 50 series GPUs (desktop and laptop)  
- Optimized for high refresh rate gaming (144Hz and above)  
- Reduces input lag and improves frame pacing  
- Removes telemetry and background processes for a lightweight footprint  
- Maintains full compatibility with CUDA, DirectX, OpenGL, and Vulkan  
- Compatible with hybrid GPU (Optimus) laptop setups  

---

### Installation Guide

1. **Download**  
   Download the latest release from the [Releases page](https://github.com/rakhalfps/Nvidia-Rebirth/releases).

2. **Uninstall Existing Drivers**  
   Use [Display Driver Uninstaller (DDU)](https://www.wagnardsoft.com/) in Safe Mode to fully remove all existing Nvidia drivers.

3. **Restart**  
   Reboot your system normally.

4. **Install Nvidia Rebirth**  
   Run the installer and follow the on-screen instructions. This installs the optimized driver with no telemetry or extra bloat.

5. **(Optional) Configure Settings**  
   Open Nvidia Control Panel to adjust power management, V-Sync, or other preferences to your liking.

---

### Features

- **Low Latency & Input Lag Reduction:** Streamlined processes reduce system overhead and improve input responsiveness.  
- **Stable Frame Pacing:** Optimizations ensure smoother frame delivery under heavy CPU or GPU load.  
- **No Telemetry & No Bloat:** All data collection, GeForce Experience, and unnecessary background services removed.  
- **Broad GPU Support:** Covers a wide range of Nvidia GPUs, including the latest RTX 50 series.  
- **Safe & Reliable:** Built on official Nvidia drivers without reverse engineering, maintaining stability and compatibility.  
- **Easy Installation & Updates:** Clean installation process with manual update support.  

---

### Frequently Asked Questions (FAQ)

- **Will this increase my FPS?**  
  Primarily focused on latency and frame stability; FPS improvements depend on your system and game.

- **Is GeForce Experience included?**  
  No, it’s intentionally removed to keep the driver lightweight.

- **Does it support Nvidia ShadowPlay or Overlay?**  
  No, those features require GeForce Experience.

- **Is this safe for my hardware?**  
  Absolutely. The core driver remains official Nvidia code with telemetry and extras removed.

- **Will it work on laptops?**  
  Yes, including systems with hybrid GPU (Optimus) configurations.

- **Can I add GeForce Experience back?**  
  While possible, it is discouraged as it may impact performance and stability.

- **Is it legal?**  
  Yes. Nvidia Rebirth repackages official Nvidia drivers with optional components removed.

- **How do I update?**  
  Download and install new releases manually from this repository.

- **Is it suitable for creative workflows?**  
  Yes. Full support for CUDA, DirectX, OpenGL, and Vulkan is retained.

- **Is the source code available?**  
  Yes. Everything is open source and available on GitHub for review and contributions.

---

For support, bug reports, or feature requests, please open an issue on [GitHub Issues](https://github.com/rakhalfps/Nvidia-Rebirth/issues) or join our [Discord community](https://discord.gg/krpUAHkf5m).
