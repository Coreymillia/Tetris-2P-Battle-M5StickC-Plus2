# 🎮 2-Player Tetris Battle V2.2.0 - M5StickC Plus2

**Professional 2-player Tetris battle system with enhanced gameplay features and WiFi networking**

![Version](https://img.shields.io/badge/version-2.2.0-blue)
![Device](https://img.shields.io/badge/device-M5StickC%20Plus2-orange)
![License](https://img.shields.io/badge/license-MIT-green)

## 🚀 Quick Start

### Installation
```bash
git clone https://github.com/YOUR_USERNAME/Tetris-2P-Battle-M5StickC-Plus2.git
cd Tetris-2P-Battle-M5StickC-Plus2
pio run --target upload
```

## ✨ Key Features

### 🎮 Enhanced Tetris Gameplay
- ✅ **HOLD System** - Store pieces strategically (BtnA)
- ✅ **NEXT Preview** - See upcoming pieces
- ✅ **Ghost Pieces** - Perfect placement guidance
- ✅ **20 Speed Levels** - From beginner (1000ms) to impossible (30ms)
- ✅ **Progressive Lock Delay** - Optimized for each skill level
- ✅ **Standard Colors** - Classic Tetris piece colors

### ⚔️ 2-Player WiFi Battles
- ✅ **Wireless Multiplayer** - No cables needed
- ✅ **Garbage Attack System** - "ATK!" and "HIT!" mechanics  
- ✅ **Mixed Skill Battles** - Different players, different speeds
- ✅ **Synchronized Gameplay** - Perfect timing control
- ✅ **Win/Lose Detection** - Proper competitive endings

### 🎨 Professional UI
- ✅ **Smart Blue Borders** - Clean field boundaries
- ✅ **Organized Layout** - HOLD/NEXT areas clearly defined
- ✅ **Battle Meter** - Real-time opponent status
- ✅ **60fps Performance** - Smooth, responsive gameplay

## 🎯 How to Play

### Single Player
1. Power on device
2. Press M5 button to start
3. Select level (0-19) with Left/Right buttons
4. Press M5 to begin game

### 2-Player Battle Setup
1. **Device 1**: Press Left+Right buttons → HOST battle
2. **Device 2**: Press UP → SCAN and connect
3. Both players select their preferred level
4. Game shows "BATTLE MODE! 3 2 1 GO!" countdown
5. Battle begins - clear lines to attack opponent!

## 🎮 Controls

| Input | Action |
|-------|--------|
| **M5 Button** | Rotate piece / Start game |
| **BtnA (Left)** | HOLD current piece |
| **BtnB (Right)** | Soft drop |
| **Joystick** | Move piece left/right |
| **PWR Button** | Pause / Reset |

### Battle Mode Setup
| Input | Action |
|-------|--------|
| **Left+Right** | Host WiFi battle |
| **UP** | Scan for battles |
| **Left/Right** | Select level |

## 🏆 Battle System

### Attack Mechanics
- **2 Lines (Double)** → 1 garbage row sent
- **3 Lines (Triple)** → 2 garbage rows sent  
- **4 Lines (Tetris)** → 4 garbage rows sent
- **T-Spins** → Bonus attack damage

### Victory Conditions
- First player to **top out** loses
- Game displays "YOU WIN!" / "YOU LOSE"
- Automatic return to level select

## 🔧 Technical Specifications

- **Platform**: M5StickC Plus2 (ESP32-PICO-V3-02)
- **Network**: WiFi P2P battle communication
- **Display**: 135x240 pixel TFT
- **Performance**: 60fps smooth gameplay
- **Memory**: 15.0% RAM, 77.3% Flash
- **Battery**: Real-time level monitoring

## 📁 Project Structure

```
src/
├── main.cpp              # Core game engine (53KB)
├── tet.h                 # Graphics assets (266KB)
├── wifi_beacon.cpp       # WiFi hosting
├── wifi_scanner.cpp      # Network discovery
└── UNIT_MiniJoyC.cpp     # Joystick controller
```

## 🙏 Credits

Built on foundations from:
- **AleksAlcDel/Tetris-for-M5StickCPlus2** - Original M5StickC Plus2 implementation
- **Hexagon/detris** - Modern Tetris mechanics inspiration
- **M5Stack** - Hardware libraries and framework

Enhanced with original implementations of battle mode, HOLD/NEXT/Ghost systems, and 20-level progression.

## 📄 License

MIT License - see [LICENSE](LICENSE) file for details.

## 🚀 Contributing

Contributions welcome! Please submit issues or pull requests.

---

**Made with ❤️ for the M5Stack community**
