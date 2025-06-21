
# stepnet ( not the final name )

**stepnet** is a modular, scalable, and networked stepper motor control system built with ESP32 microcontrollers. Designed for kinetic sculptures, interactive installations, robotics, and precise motion control, each node can be independently configured, discovered, and commanded over OSC.

---

## ✨ Features

- 📡 OSC over Wi-Fi (UDP) for real-time control
- 🎛 Soft zeroing, soft limits, and PID stall detection
- 🧠 Modular firmware with AccelStepper and encoder feedback
- 🧱 Industrial-grade DM542 stepper driver support
- 🌐 Web-based configuration UI + centralized dashboard
- 🧩 TouchDesigner + openFrameworks compatibility
- 🔌 Web interface for WiFi config and static IP setup

---

## 📦 Hardware Requirements (Per Node)

- ESP32 DevKit board
- Stepper motor (e.g. NEMA 17/23)
- DM542 stepper driver
- 48V power supply (≥5A recommended)
- Optional: Optical encoder, limit switches, temperature sensor
- JST / GX16 / screw terminal connectors
- Enclosure with cable glands and labeling

---

## 🛠 Firmware Features

- OSC messaging:
  - `/motor/position`, `/motor/jog`, `/motor/zero`, `/motor/enable`
  - Group commands: `/group/zero`, `/group/home`
  - `/announce` for auto-discovery
- Configurable via web interface:
  - Soft min/max limits
  - Soft zero offset
  - Project name + node ID
- AccelStepper + encoder feedback in one integrated firmware file
- Modular class-based code structure

---

## 🌐 Web Dashboard

- View all connected nodes and statuses
- Jog motors, send home/zero commands
- Assign IP, project name, and monitor temperature/feedback
- Optional: host dashboard from ESP32 or local computer

---

## 🎛 TouchDesigner Integration (example)

- Auto-detect `/announce` OSC messages
- Dynamic UI panel per motor
- Live jog sliders, home/zero buttons

---

## 📁 Project Structure

```
stepnet/
├── firmware/                      # ESP32 source code
│   └── esp32_stepper_class_firmware.ino
├── web-ui/                        # Web dashboard & config pages
│   └── esp32_stepper_dashboard.html
├── docs/                          # Markdown guides
│   ├── esp32_dm542_hardware_guide.md
│   ├── esp32_stepper_summary_document.md
│   └── esp32_motor_features_todo.md
└── diagrams/                      # Wiring and enclosure diagrams
```

---

## 🔮 Roadmap

- [ ] WebSocket-based dashboard updates
- [ ] Host dashboard from ESP32 via LittleFS
- [ ] Automatic motor calibration routine
- [ ] QR code per node for setup and IP scan
- [ ] Dynamic TouchDesigner interface patch

---



---



