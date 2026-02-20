# mWin Tools

<div align="center">

<!-- Badges -->
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-1.19.2-blue)](https://github.com/m-Software-Inc/mWinTools/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%2F11%20%2864--bit%29-lightgrey)](https://www.microsoft.com/en-us/windows)
[![Language: Rust](https://img.shields.io/badge/Language-Rust-orange)](https://www.rust-lang.org/)
[![GUI Framework](https://img.shields.io/badge/GUI-eframe%2Fegui-green)](https://github.com/emilk/egui)

<!-- Description -->
**A lightweight Windows desktop application for quick access to system tools with educational explanations.**

</div>

---

## 📋 Overview

mWin Tools is a native Windows desktop application built with Rust and the egui/eframe GUI framework. It provides quick and easy access to 20+ Windows built-in system tools, each with an educational popup that explains what the tool does before launching it.

Whether you're a beginner learning about Windows system tools or an advanced user needing quick access, mWin Tools makes system administration more accessible and educational.

---

## ⭐ Features

| Feature | Description |
|---------|-------------|
| **20+ Built-in Tools** | Access System, Security, Maintenance, Accessibility, and Advanced tools |
| **Educational Popups** | Learn what each tool does before launching it |
| **Modern Dark UI** | Clean, minimalistic dark theme interface |
| **Lightweight & Fast** | Single executable with native Rust performance |
| **Admin Detection** | Tools requiring administrator privileges are clearly marked |
| **No Dependencies** | Standalone executable, runs without additional installations |

---

## 📥 Download

### Latest Release

Download the latest installer from the [Releases](https://github.com/m-Software-Inc/mWinTools/releases) page:

| File | Description |
|------|-------------|
| `mwin-tools-setup-v1.19.2.exe` | Windows installer (recommended) |

---

## 🚀 Getting Started

### Requirements

- **Operating System**: Windows 10 or Windows 11 (64-bit)
- **Permissions**: Standard user account (some tools require admin rights)

### Installation

1. Download the latest `mwin-tools-setup-vX.X.X.exe` from the [Releases](https://github.com/m-Software-Inc/mWinTools/releases) page
2. Run the installer
3. Follow the on-screen instructions
4. Launch mWin Tools from the Start Menu or Desktop shortcut

---

## 💻 Building from Source

### Prerequisites

- [Rust](https://www.rust-lang.org/) 1.70 or later (stable channel)
- [Cargo](https://doc.rust-lang.org/cargo/) (included with Rust)
- Windows 10/11 64-bit

### Build Instructions

```bash
# Clone the repository
git clone https://github.com/m-Software-Inc/mWinTools.git
cd mWinTools

# Build in release mode
cargo build --release

# Run the application
cargo run --release
```

The compiled executable will be located at:
```
target/release/mwin-tools.exe
```

### Build Options

The project includes optimized release settings in `Cargo.toml`:

```toml
[profile.release]
opt-level = 3          # Maximum optimization
lto = true             # Link-time optimization
codegen-units = 1      # Better optimization
panic = "abort"        # Smaller binary
strip = true           # Strip symbols
```

---

## 🛠️ Included Windows Tools

### System Tools
| Tool | Description |
|------|-------------|
| System Restore | Restore system to a previous state |
| System Information | View detailed system specifications |
| Services | Manage Windows services |
| Task Scheduler | Create and manage scheduled tasks |
| Group Policy Editor | Configure local group policies (Windows Pro/Enterprise) |
| Control Panel | Access classic control panel |
| Network Connections | Manage network adapters |
| Programs and Features | Install/uninstall programs |
| System Properties | View and modify system configuration |
| Display Settings | Configure display preferences |

### Maintenance Tools
| Tool | Description |
|------|-------------|
| Disk Defragmenter | Optimize hard drive performance |
| Check Disk | Scan and repair disk errors |
| Disk Cleanup | Free up disk space |

### Security Tools
| Tool | Description |
|------|-------------|
| Security Center | View security status |
| Windows Firewall | Configure firewall settings |
| System File Checker | Scan and repair system files |
| User Accounts | Manage user accounts |

### Accessibility Tools
| Tool | Description |
|------|-------------|
| On-Screen Keyboard | Virtual keyboard |
| Magnifier | Screen magnification tool |
| Narrator | Screen reader |

### Advanced Tools
| Tool | Description |
|------|-------------|
| Device Manager | Manage hardware devices |
| Registry Editor | Edit Windows registry |
| Event Viewer | View system event logs |
| Command Prompt | Windows command line |
| PowerShell | Windows PowerShell |

---

## 🧩 Architecture

### Design Pattern

The application follows a modular architecture:

```
┌─────────────────────────────────────────────────────────┐
│                      main.rs                            │
│                    Entry Point                          │
└──────────────────────┬──────────────────────────────────┘
                       │
┌──────────────────────▼──────────────────────────────────┐
│                    MWinToolsApp                         │
│               Main Application Logic                    │
└──────────────────────┬──────────────────────────────────┘
                       │
     ┌─────────────────┼─────────────────┐
     │                 │                 │
┌────▼────┐      ┌─────▼────┐     ┌──────▼──────┐
│ Tools   │      │  State   │     │   Theme     │
│Registry │      │          │     │             │
└─────────┘      └──────────┘     └─────────────┘
                           │
                    ┌──────▼──────┐
                    │ Components  │
                    └─────────────┘
```

### Key Technologies

| Technology | Purpose |
|------------|---------|
| Rust | Programming language |
| eframe/egui | GUI framework |
| winapi | Windows API integration |

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add some amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Developer

**Mahfuj Ibn Mijan**  
Founder & Developer  
[m Software Inc.](https://github.com/m-Software-Inc)

- **Version**: 1.19.2
- **Email**: Contact through GitHub

---

## 🙏 Acknowledgments

- [egui/eframe](https://github.com/emilk/egui) - Excellent Rust GUI library
- [Rust Community](https://www.rust-lang.org/community) - For amazing tooling and support

---

## 📞 Support

If you encounter any issues or have questions:

1. Check the [Issues](https://github.com/m-Software-Inc/mWinTools/issues) page
2. Create a new issue if your problem isn't already reported

---

<div align="center">

**⭐ Star this repository if you find it useful! ⭐**

</div>
