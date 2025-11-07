# 📥 Installation Guide - 2-Player Tetris Battle V2.2.0

## 🚀 **Quick Start (M5Burner - Recommended)**

### **Requirements**
- M5StickC Plus2 device(s) 
- M5Burner application ([Download here](https://m5stack.com/pages/download))
- USB-C cable

### **Installation Steps**
1. **Download Firmware**
   - Get `TETRIS_V2.2.0_FINAL_M5BURNER.bin` from [Releases](https://github.com/Coreymillia/Tetris-for-M5StickCPlus2-FastGhost/releases)

2. **Flash with M5Burner**
   - Open M5Burner
   - Connect M5StickC Plus2 via USB
   - Select the downloaded .bin file
   - Click "Burn" - done!

3. **For 2-Player Battles**
   - Repeat steps 1-2 for second device
   - Both devices need same firmware

## 🛠️ **Developer Installation (PlatformIO)**

### **Requirements**
- [PlatformIO IDE](https://platformio.org/) or PlatformIO CLI
- Git
- M5StickC Plus2 device

### **Setup Steps**
```bash
# Clone repository
git clone https://github.com/Coreymillia/Tetris-for-M5StickCPlus2-FastGhost.git
cd Tetris-for-M5StickCPlus2-FastGhost

# Build and upload
pio run --target upload
```

### **Library Dependencies** 
*(Auto-installed by PlatformIO)*
- `M5StickCPlus2 @ ^1.0.2`
- `IRremoteESP8266 @ ^2.8.6` 
- `WiFi @ ^2.0.0`
- `Wire @ ^2.0.0`

## 🎮 **First Time Setup**

### **Single Device Setup**
1. Power on M5StickC Plus2
2. Device shows "v.2.2.0" and Tetris splash
3. Press M5 button to start
4. Select level and enjoy!

### **2-Player Battle Setup**  
1. **Device 1 (Host)**:
   - Power on
   - Press Left+Right buttons → "HOST mode"
   - Wait for "Client connected!" message

2. **Device 2 (Client)**:
   - Power on  
   - Press UP on joystick → "SCAN mode"
   - Device automatically connects to host

3. **Start Battle**:
   - Both devices show level select
   - Choose your levels
   - Game countdown: "3 2 1 GO!"
   - Battle begins!

## 🔧 **Hardware Setup**

### **Required Hardware**
- **Primary**: M5StickC Plus2 (1-2 devices for multiplayer)
- **Optional**: Mini Joy C Hat (enhanced controls)

### **Optional Joy C Hat Connection**
- **SDA**: GPIO 0
- **SCL**: GPIO 26  
- **Power**: 3.3V
- **Ground**: GND

## 🚨 **Troubleshooting**

### **Flash Issues**
- **Device not detected**: Check USB cable and drivers
- **Flash failed**: Try different USB port or cable
- **Permission denied**: Run with administrator/sudo

### **WiFi Battle Issues**  
- **Connection failed**: Restart both devices and retry
- **Lag/Disconnection**: Ensure devices are close together
- **Host timeout**: Client must connect within 30 seconds

### **Gameplay Issues**
- **Controls not working**: Check joystick connection (if using hat)
- **Pieces not dropping**: Restart device
- **Display corruption**: Power cycle device

### **Common Solutions**
```bash
# Reset device completely
Hold PWR button for 10 seconds

# Check serial output (developers)
pio device monitor --baud 115200

# Reflash firmware
pio run --target upload --upload-port [YOUR_PORT]
```

## 📊 **Performance Notes**

### **Optimal Performance**
- **Frame Rate**: 60fps smooth gameplay
- **Latency**: <50ms for battle communications
- **Memory Usage**: 50KB RAM, 1MB Flash
- **Battery Life**: ~2-3 hours continuous play

### **Network Performance**
- **Range**: ~10 meters indoor WiFi Direct
- **Bandwidth**: Minimal (~1KB/sec battle data)
- **Reconnection**: Automatic with 30-second timeout

## 🔄 **Updating Firmware**

### **From M5Burner**
1. Download new .bin file from releases
2. Flash over existing firmware (settings preserved)
3. No need to erase - direct upgrade

### **From Source**
```bash
git pull origin main
pio run --target upload
```

## 📞 **Support**

- **Issues**: [GitHub Issues](https://github.com/Coreymillia/Tetris-for-M5StickCPlus2-FastGhost/issues)
- **Discussions**: [GitHub Discussions](https://github.com/Coreymillia/Tetris-for-M5StickCPlus2-FastGhost/discussions)
- **M5Stack Community**: [Official Forum](https://community.m5stack.com/)

---

**Happy Gaming! 🎮**