# 🎵 Telegram Audio Downloader

<div align="center">

![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Status](https://img.shields.io/badge/Status-Production%20Ready-brightgreen.svg)
![Platform](https://img.shields.io/badge/Platform-Windows%20|%20Linux%20|%20macOS-lightgrey.svg)

**Ein leistungsstarker, asynchroner Python-Bot zum Herunterladen und Verwalten von Audiodateien aus Telegram-Gruppen**

> 🎵 Sammeln Sie mühelos Ihre Lieblingsmusik aus Telegram-Gruppen mit diesem professionellen Download-Tool!

</div>

---

## 🚀 **Features**

### **⚡ Performance & Effizienz**
- 🚀 **Parallele Downloads** mit konfigurierbarer Anzahl (Standard: 3)
- 🎯 **Intelligente Rate-Limiting** mit adaptivem Token-Bucket-Algorithmus
- 🧠 **Memory-Management** mit automatischer Garbage Collection
- 🔄 **Fortsetzbare Downloads** bei Unterbrechungen
- 📈 **Performance-Monitoring** in Echtzeit

### **🎵 Audio-Funktionalitäten**
- 🎼 **Erweiterte Metadaten-Extraktion** (Titel, Künstler, Album, etc.)
- 🔧 **Automatische Dateinamen-Bereinigung**
- 🎶 **Multi-Format-Support**: MP3, FLAC, OGG, M4A, WAV, OPUS
- ✅ **Checksum-Verifikation** für Datenintegrität
- 📝 **ID3-Tags** Extraktion und Verwaltung

---

## 📦 **Installation**

### **1. Repository klonen**
```bash
git clone https://github.com/Elpablo777/Telegram-Audio-Downloader.git
cd Telegram-Audio-Downloader
```

### **2. Abhängigkeiten installieren**
```bash
# Virtuelle Umgebung erstellen (empfohlen)
python -m venv venv
venv\Scripts\activate  # Windows

# Abhängigkeiten installieren
pip install -r requirements.txt
pip install -e .
```

### **3. Konfiguration**
```bash
# .env-Datei erstellen
cp .env.example .env
```

Bearbeiten Sie die `.env`-Datei:
```env
# Telegram API credentials (von https://my.telegram.org/apps)
API_ID=1234567
API_HASH=your_api_hash_here
SESSION_NAME=my_telegram_session
```

---

## ⚡ **Quick Start**

```bash
# Audiodateien aus einer Gruppe herunterladen
telegram-audio-downloader download @musikgruppe

# Mit erweiterten Optionen
telegram-audio-downloader download @musikgruppe --limit=50 --parallel=5 --output=./music

# Downloads durchsuchen
telegram-audio-downloader search "beethoven" --fuzzy --format=flac

# Performance überwachen
telegram-audio-downloader performance --watch
```

---

## 💻 **CLI-Befehle**

### **Download**
```bash
telegram-audio-downloader download <GRUPPE> [OPTIONS]
  --limit, -l       Maximale Anzahl Nachrichten
  --output, -o      Zielverzeichnis
  --parallel, -p    Parallele Downloads (Standard: 3)
```

### **Suche**
```bash
telegram-audio-downloader search [QUERY] [OPTIONS]
  --fuzzy, -f       Fuzzy-Suche aktivieren
  --format          Audioformat filtern
  --min-size        Minimale Dateigröße
  --max-size        Maximale Dateigröße
  --metadata, -m    Erweiterte Metadaten anzeigen
```

### **Performance**
```bash
telegram-audio-downloader performance [OPTIONS]
  --watch, -w       Echtzeit-Überwachung
  --cleanup, -c     System bereinigen
```

### **Verwaltung**
```bash
telegram-audio-downloader groups      # Bekannte Gruppen anzeigen
telegram-audio-downloader stats       # Download-Statistiken
telegram-audio-downloader metadata    # Metadaten analysieren
```

---

## 🐳 **Docker Support**

```bash
# Mit Docker Compose
docker-compose up -d
docker-compose exec telegram-audio-downloader telegram-audio-downloader download @gruppe

# Direkt mit Docker
docker build -t telegram-audio-downloader .
docker run -it --rm -v $(pwd)/.env:/app/.env telegram-audio-downloader
```

---

## 🧪 **Tests**

```bash
pytest                                    # Alle Tests
pytest --cov=src/telegram_audio_downloader  # Mit Coverage
pytest -v                                # Verbose-Modus
```

**30+ Unit-Tests** mit vollständiger Abdeckung aller wichtigen Komponenten.

---

## 🎯 **Erweiterte Funktionen**

- **🔍 Fuzzy-Suche** - Findet Dateien auch bei Schreibfehlern
- **📊 Performance-Dashboard** - Echtzeit-Monitoring mit Rich-Interface
- **🔄 Resume-Downloads** - Fortsetzung unterbrochener Downloads
- **🎵 Metadaten-Extraktion** - Automatische ID3-Tags und Cover-Art
- **📈 Statistiken** - Detaillierte Download- und Performance-Reports
- **🛡️ Error-Handling** - Robuste Fehlerbehandlung mit Retry-Logik

---

## 🤝 **Contributing**

Beiträge sind willkommen! Bitte lesen Sie [CONTRIBUTING.md](CONTRIBUTING.md) für Details.

### **Development Setup**
```bash
git clone https://github.com/IHR-USERNAME/Telegram-Audio-Downloader.git
python -m venv venv && source venv/bin/activate
pip install -e ".[dev]"
pre-commit install
```

---

## 📄 **Lizenz**

MIT License - siehe [LICENSE](LICENSE) für Details.

---

## 🙏 **Acknowledgments**

- [Telethon](https://github.com/LonamiWebs/Telethon) - Telegram-API
- [Rich](https://github.com/Textualize/rich) - Terminal-UI
- [Click](https://github.com/pallets/click) - CLI-Framework
- [Mutagen](https://github.com/quodlibet/mutagen) - Audio-Metadaten

---

<div align="center">

**⭐ Gefällt Ihnen das Projekt? Geben Sie uns einen Stern! ⭐**

[![GitHub stars](https://img.shields.io/github/stars/Elpablo777/Telegram-Audio-Downloader.svg?style=social&label=Star)](https://github.com/Elpablo777/Telegram-Audio-Downloader)

Made with ❤️ by [Elpablo777](https://github.com/Elpablo777)

</div>