# 📡 TransShare

**Wireless file transfer application with QR code sharing**

Fast and secure file sharing between PC and mobile devices over local network. No internet connection required.

<img width="552" height="519" alt="image" src="https://github.com/user-attachments/assets/94941d04-dd0b-4d94-824b-816fce3b4f14" />

---

## ✨ Features

- 🔄 **Wireless Transfer** - Share files via WiFi without cables
- 📱 **QR Code Scanning** - Instant connection from mobile devices
- 🔒 **Password Protection** - Secure your transfers with optional password
- 🔗 **URL Shortener** - Clean, short URLs for easy sharing
- 📦 **Compression** - Automatic ZIP compression for folders and multiple files
- 🚀 **Fast Transfer** - Direct HTTP server, no third-party services
- 🎨 **Modern UI** - Clean glassmorphism design with dark/light themes
- 🔥 **No Installation on Mobile** - Works in any browser

---

## 🖥️ System Requirements

- **OS:** Windows 10/11
- **Python:** 3.8 or higher
- **Network:** WiFi connection

---

## 🚀 Quick Start

### Basic File Transfer

1. Launch TransShare
2. Click **File** tab → Select file or folder
3. Click **Share** tab → Press **Start Server**
4. Scan QR code with mobile device
5. File downloads automatically

### With Password Protection

1. Go to **Security** tab
2. Enable "Защитить файл паролем"
3. Enter password (minimum 4 characters)
4. Start server
5. Enter password on mobile when prompted

---

## 📖 User Guide

### Interface Tabs

| Tab | Description |
|-----|-------------|
| 🔄 **Share** | QR code, URL display, server controls |
| 📄 **File** | File/folder selection, multi-file support |
| 🔒 **Security** | URL shortener, password protection |
| ⚙️ **Settings** | Port, compression, theme, network profile |
| ✓ **Dev** | Application info, version, author |

### File Selection

**Single File:**
- Click "Выбрать файл" → Select file

**Multiple Files:**
- Click "Выбрать несколько файлов" → Select multiple files
- Automatically creates ZIP archive

**Folder:**
- Click "Выбрать папку" → Select folder
- Automatically creates ZIP archive

### Server Configuration

**Port Settings:**
- Default: `8080`
- Range: `1024-65535`
- Configure in Settings tab

**Network Profile:**
- **Private** (recommended) - Windows firewall allows connection
- **Public** - May block connections

**Auto-stop:**
- Server stops automatically after first download
- Enable in Settings tab

---

## 🔒 Security Features

### URL Shortener

Converts long URLs to short format:
```
Before: http://192.168.0.100:8080/download
After:  http://192.168.0.100:8080/s/abc123
```

**Benefits:**
- Easier to type manually
- Cleaner appearance
- Hides internal paths

### Password Protection

**Setup:**
1. Security tab → Enable "Защитить файл паролем"
2. Enter password (min 4 characters)
3. Start server

**Access Flow:**
1. User opens URL
2. Password prompt appears
3. Correct password → Download starts
4. Wrong password → Access denied

---

## ⚙️ Configuration

### Settings Options

| Setting | Description | Default |
|---------|-------------|---------|
| **Port** | Server port | 8080 |
| **Compression** | Enable ZIP compression | On |
| **Auto-stop** | Stop after download | Off |
| **Theme** | Dark/Light mode | Dark |
| **Network Profile** | Private/Public | Private |

### Firewall Configuration

TransShare automatically adds Windows Firewall rule:
```
Rule Name: TransShare Server
Port: Configured port
Protocol: TCP
Action: Allow
```

---

## 🌐 Network Setup

### PC and Mobile Connection

Both devices must be on the same WiFi network:

**PC:**
- Connected to WiFi: `MyHomeNetwork`
- IP: `192.168.0.100`

**Mobile:**
- Connected to WiFi: `MyHomeNetwork`
- Scans QR code → Opens URL

### IP Address

TransShare automatically detects your PC's local IP address.

**Manual Check (Windows):**
```bash
ipconfig
```
Look for "IPv4 Address" under your WiFi adapter.

---

## 📱 Mobile Usage

### Android

1. Open Camera app
2. Point at QR code
3. Tap notification
4. File downloads to `/Downloads`

### iPhone

1. Open Camera app
2. Point at QR code
3. Tap banner
4. File downloads (Safari → Downloads)

### Manual Entry

If QR scanning fails:
1. Note URL from PC
2. Open mobile browser
3. Type URL
4. Download starts

---

## 🛠️ Troubleshooting

### Connection Issues

**Problem:** Mobile can't connect

**Solutions:**
1. Check both devices on same WiFi
2. Disable VPN on PC
3. Check Windows Firewall:
   - Settings → Network → Firewall
   - Allow TransShare
4. Try different port (Settings → Port)
5. Restart server

### File Not Downloading

**Problem:** URL opens but no download

**Solutions:**
1. Check file exists (File tab)
2. Restart server
3. Check server status (Share tab - green = active)

### QR Code Issues

**Problem:** QR code not scanning

**Solutions:**
1. Increase screen brightness
2. Hold phone steady
3. Use manual URL entry
4. Check QR code is visible (not cut off)

---



### HTTP Server

- **Protocol:** HTTP/1.1
- **Method:** GET
- **Streaming:** Chunked transfer (8KB chunks)
- **Progress:** Real-time tracking

### URL Shortener

- **Code Length:** 6 characters
- **Character Set:** a-z, 2-9 (excludes similar: 0,o,1,l)
- **Storage:** In-memory dictionary
- **Collision:** Regenerates on conflict

---

## 🤝 Contributing

Contributions are welcome!

1. Fork repository
2. Create feature branch: `git checkout -b feature/AmazingFeature`
3. Commit changes: `git commit -m 'Add AmazingFeature'`
4. Push to branch: `git push origin feature/AmazingFeature`
5. Open Pull Request

---

## 📄 License

This project is licensed under the MIT License - see [LICENSE](LICENSE) file for details.

---

## 👤 Author

**SelfCode**

- GitHub: [@SelfCode](https://github.com/SelfC0de)

---

## 🙏 Acknowledgments

- PyQt5 for the GUI framework
- QR code generation library
- Glassmorphism design inspiration

---

## 📊 Version History

### v1.0.0 (Current)
- ✅ QR code file sharing
- ✅ Password protection
- ✅ URL shortener
- ✅ Multi-file support
- ✅ Automatic compression
- ✅ Dark/Light themes
- ✅ Real-time progress tracking
- ✅ Automatic firewall configuration

---

## 🐛 Known Issues

None currently. Report issues on [GitHub Issues](https://github.com/SelfC0de/transshare/issues).

---

## 📞 Support

- **Issues:** [GitHub Issues](https://github.com/SelfC0de/transshare/issues)
- **Email:** selfcode.dev@gmail.com

---

<p align="center">Made with ❤️ for easy file sharing</p>
