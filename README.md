# Caldura — Thermal Management, Fan Curve & Hardware Monitoring Engine

Caldura is an advanced, low-level hardware thermal management utility, fan curve builder, and GPU/CPU power tuner for Windows and Linux. Built with C++20 and Qt 6 / QML (**Vulkan 1.3 and DirectX 12 (Feature Level 12_1) First/Only**), Caldura provides fine-grained control over system fan speeds, liquid cooling pumps, thermal sensor curves, and GPU power limits with zero background bloat.

---

## ⚡ Core Subsystems & Status Matrix

| Subsystem | Features & Capabilities | Status / Roadmap |
|---|---|---|
| **Graphics Engine** | **Vulkan 1.3 & DirectX 12 (Feature Level 12_1) First/Only** desktop viewport | Active |
| **Fan Curve Supervisor** | Multi-point custom fan curves, temp source mixing, hysteresis & delay smoothing | Active |
| **Acoustic Optimization** | Automatic acoustic noise optimization, zero-RPM mode, liquid cooling flow sensor | Roadmap |
| **GPU Power Tuner** | Core/memory clock offsets, power target sliders, thermal limit monitoring | Active |
| **Automated Tuner** | Per-game auto power profiles, undervolting curve optimizer, multi-GPU balance | Roadmap |
| **Sensor Telemetry** | Low-overhead polling (CPU Tdie, GPU Hotspot/VRAM, VRM), tray temp icon, CSV logger | Active |
| **In-Game OSD & Alerts** | Direct3D/Vulkan OSD overlay, desktop widget overlay, thermal throttling alerts | Roadmap |

---

## 🌡️ Key Features & Module Breakdown

### 🌀 Dynamic Fan Curve Engine (`fans`)
- **Current**: Multi-point custom fan curves, hysteresis controls, temperature source mixing (max of CPU/GPU/VRAM temps), and step-up/step-down delay smoothing.
- **Planned / Roadmap**: Automatic acoustic noise optimization, zero-RPM fan mode toggle, and water cooling flow rate sensor integration.

### ⚡ GPU Power & Voltage Tuner (`power`)
- **Current**: GPU core/memory clock offset adjustments, power target sliders, temperature limit tuning, and voltage curve monitoring.
- **Planned / Roadmap**: Per-game automated power profile switching, undervolting curve optimizer, and multi-GPU balance control.

### 📊 Thermal Telemetry & OSD (`telemetry`)
- **Current**: Low-overhead hardware sensor polling (CPU Tdie/Tctl, GPU Hotspot/VRAM, Motherboard VRM), tray icon temperature display, and CSV sensor logger.
- **Planned / Roadmap**: Custom Direct3D/Vulkan On-Screen Display (OSD), desktop widget overlay, and thermal throttling alert system.

---

## 🏗️ Architecture & Technology Stack

- **Graphics APIs**: Vulkan 1.3 & DirectX 12 (Feature Level 12_1) First/Only.
- **UI & Controls**: Qt 6.12, QML, Custom Material 3 dark dashboard layout.
- **Core Engine**: C++20, Direct Win32 Ring-0 hardware driver interface / Linux `/sys/class/hwmon` sysfs interface.
- **Licensing**: AGPL-3.0.

---

## 🛠️ Building & Running

### Desktop
```bat
build.bat Release
run.bat
```

---

## 📜 License

Caldura is released under the **GNU Affero General Public License v3.0** (AGPL-3.0). See [`LICENSE`](LICENSE) for details.
