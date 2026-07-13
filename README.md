# 🎮 Shield Controller Bridge

<div align="center">

### 🇬🇧 Use your NVIDIA Shield Controller on PC — wirelessly, with near-zero input lag and full rumble support.
### 🇵🇱 Podłącz kontroler NVIDIA Shield do PC bezprzewodowo — z minimalnym input lagiem i pełnym wsparciem wibracji.

[![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Android-0078d4?style=for-the-badge&logo=windows)](#)
[![Root Required](https://img.shields.io/badge/Android-ROOT%20required-red?style=for-the-badge&logo=android)](#)
[![ViGEmBus](https://img.shields.io/badge/driver-ViGEmBus-brightgreen?style=for-the-badge)](https://github.com/nefarius/ViGEmBus/releases)
[![Xbox 360](https://img.shields.io/badge/emulates-Xbox%20360-107c10?style=for-the-badge&logo=xbox)](#)
[![License](https://img.shields.io/badge/license-Personal%20Use-lightgrey?style=for-the-badge)](#)

</div>

---

## en English

### 🕹️ What is this?

**Shield Controller Bridge** is a two-part application that wirelessly transmits input signals from the **NVIDIA Shield Controller** — via a Shield Tablet — directly to a Windows PC, presenting it as a **virtual Xbox 360 controller** (XInput).

Two connection modes are supported:
- 🔌 **USB Tethering (RNDIS)** — recommended, creates a private TCP/IP link over cable with near-wired latency
- 📶 **Wi-Fi** — works when tablet and PC are on the same local network (higher latency than cable)

---

### 📦 What's Included

| File | Platform | Description |
|---|---|---|
| `TabletSender v1.1.apk` | 🤖 Android | App for NVIDIA Shield Tablet |
| `PCReceiverGUI v1.1.exe` | 🖥️ Windows | Client application for PC |

---

### ✅ Requirements

**🤖 Android (Shield Tablet)**
- Unlocked **ROOT access** (e.g. via Magisk or SuperSU)
- Required to intercept low-level controller input via `/dev/input/eventX`

**🖥️ Windows (PC)**
- **[ViGEmBus](https://github.com/nefarius/ViGEmBus/releases)** driver installed
- Creates a virtual Xbox 360 controller recognized by all XInput games

---

### 🚀 Quick Start

> **⚠️ Make sure [ViGEmBus](https://github.com/nefarius/ViGEmBus/releases) is installed on Windows before you begin!**

1. 📲 Install `TabletSender v1.1.apk` on the Shield Tablet *(ignore Play Protect warnings — app uses root/su)*
2. 💾 Copy `PCReceiverGUI v1.1.exe` to any folder on your PC
3. 🔗 **Pair** the Shield Controller with the tablet via **Wi-Fi Direct**
4. 🔌 Connect the tablet to PC with a **USB cable**
5. 📡 On the tablet enable **USB Tethering** *(Settings → Network → Hotspot & Tethering → USB Tethering)*
6. ▶️ Launch `TabletSender` on the tablet — grant **ROOT** permission when prompted
7. ▶️ Launch `PCReceiverGUI` on your PC
8. 🌐 Default IP: `192.168.42.129` — click **Connect**
9. ✅ Tablet shows **"Connected"** — Shield Controller is now a virtual Xbox 360 pad!

> 💡 **Wi-Fi mode:** If tablet and PC are on the same network, you can connect without a cable — just enter the tablet's local IP address instead of the RNDIS one. USB Tethering is still recommended for lowest latency.

---

### ⚙️ PC Application Features

| Feature | Description |
|---|---|
| ⚡ **AutoTethering** | Automatically forces USB Tethering on the tablet via ADB when cable is plugged in |
| 🔄 **Background Autostart** | Launches with Windows, minimizes silently to the system tray |
| 📳 **Rumble Rate-Limiter** | Caps vibration packets at 1 per 150ms — eliminates rumble loops and motor stutter |
| 🎛️ **Key Mapping / Macro Editor** | Full visual profile editor — map any keyboard key or macro to any controller button |
| 🕹️ **Built-in Controller Tester** | Real-time input tester built into the app — verify buttons, axes and triggers live |
| 🔁 **Rapid Fire** | Assign rapid-fire to any button with adjustable fire rate |

---

### 🕹️ Advanced Analog Stick Modes

Each analog stick can be independently set to one of **4 operating modes**:

| Mode | Description |
|---|---|
| 🕹️ **Analog** | Standard analog input — full axis range, default mode |
| 🔲 **Digital** | Stick snaps to 8 directions — acts like a D-Pad |
| 🖱️ **Mouse** | Stick controls mouse cursor movement on PC |
| ⌨️ **Keyboard** | Stick directions mapped to keyboard keys |

---

### 🎮 Advanced Controller Configuration

| Option | Description |
|---|---|
| ↔️ **Dead Zones** | Adjustable inner and outer dead zones for both analog sticks and triggers |
| 🔄 **D-Pad ↔ Left Stick Swap** | Digitally swap D-Pad and Left Analog Stick functions |
| 🎚️ **Trigger Range Adjustment** | Set custom min/max range for analog triggers — fine-tune sensitivity |
| ⚡ **Rapid Fire** | Per-button rapid fire |
| 🗺️ **Profiles** | Save and load multiple configuration profiles for different games |

---

### 🔋 Battery Saving

| Metric | Value |
|---|---|
| 🔋 Battery saving vs screen-on | **~95%** |
| 🧠 CPU usage | **~4.5%** |
| 💤 Screen required? | **No** |

> Thanks to deep **Smali-level optimization** and asynchronous root flag handling.


---

### 📋 Troubleshooting

| ❓ Problem | ✅ Solution |
|---|---|
| Can't connect | Enable USB Tethering **before** launching PCReceiverGUI |
| Root not granted | Whitelist the app in Magisk Superuser settings |
| Controller not detected | Install / reinstall [ViGEmBus](https://github.com/nefarius/ViGEmBus/releases) |
| Wrong IP address | Run `ipconfig` in Windows — check the RNDIS adapter gateway (usually `192.168.42.129`) |
| Wi-Fi connection fails | Make sure tablet and PC are on the **same local network** and firewall isn't blocking the port |

---

### 📄 License

Released for **personal, non-commercial use only**. Redistribution of modified versions requires credit to the original author.

---
---

## 🇵🇱 Polski

### 🕹️ Co to jest?

**Shield Controller Bridge** to dwuskładnikowa aplikacja umożliwiająca bezprzewodowe przesyłanie sygnałów z **kontrolera NVIDIA Shield** — za pośrednictwem tabletu Shield — bezpośrednio do komputera PC, gdzie pojawia się jako **wirtualny kontroler Xbox 360** (XInput).

Obsługiwane są dwa tryby połączenia:
- 🔌 **Tethering USB (RNDIS)** — zalecany, tworzy prywatne łącze TCP/IP przez kabel z minimalnym opóźnieniem
- 📶 **Wi-Fi** — działa gdy tablet i PC są w tej samej sieci lokalnej (większy input lag niż kabel)

---

### 📦 Co jest w paczce

| Plik | Platforma | Opis |
|---|---|---|
| `TabletSender v1.1.apk` | 🤖 Android | Aplikacja na tablet NVIDIA Shield |
| `PCReceiverGUI v1.1.exe` | 🖥️ Windows | Aplikacja kliencka na PC |

---

### ✅ Wymagania

**🤖 Android (Tablet Shield)**
- Odblokowany dostęp **ROOT** (np. przez Magisk lub SuperSU)
- Niezbędny do odczytu niskopoziomowego wejścia kontrolera przez `/dev/input/eventX`

**🖥️ Windows (PC)**
- Zainstalowany sterownik **[ViGEmBus](https://github.com/nefarius/ViGEmBus/releases)**
- Tworzy wirtualny kontroler Xbox 360 wykrywany przez gry obsługujące XInput

---

### 🚀 Szybki start

> **⚠️ Upewnij się, że [ViGEmBus](https://github.com/nefarius/ViGEmBus/releases) jest zainstalowany na Windows zanim zaczniesz!**

1. 📲 Zainstaluj `TabletSender v1.1.apk` na tablecie *(zignoruj ostrzeżenia Play Protect — aplikacja wymaga root/su)*
2. 💾 Skopiuj `PCReceiverGUI v1.1.exe` do dowolnego folderu na PC
3. 🔗 **Sparuj** kontroler Shield z tabletem przez **Wi-Fi Direct**
4. 🔌 Podłącz tablet do PC kablem **USB**
5. 📡 Na tablecie włącz **Tethering USB** *(Ustawienia → Sieć → Hotspot i tethering → Tethering USB)*
6. ▶️ Uruchom `TabletSender` na tablecie — zatwierdź uprawnienia **ROOT**
7. ▶️ Uruchom `PCReceiverGUI` na komputerze
8. 🌐 Domyślny adres IP: `192.168.42.129` — kliknij **Connect**
9. ✅ Tablet wyświetli **„Połączono"** — kontroler działa jako wirtualny pad Xbox 360!

> 💡 **Tryb Wi-Fi:** Jeśli tablet i PC są w tej samej sieci, możesz połączyć się bez kabla — wpisz lokalny adres IP tabletu zamiast adresu RNDIS. Tethering USB nadal zalecany dla najniższego input lagu.

---

### ⚙️ Funkcje aplikacji 

| Funkcja | Opis |
|---|---|
| ⚡ **AutoTethering** | Automatycznie włącza Tethering USB na tablecie przez ADB po wykryciu kabla |
| 🔄 **Autostart w tle** | Uruchamia się z Windows i minimalizuje do zasobnika systemowego |
| 📳 **Stabilizator wibracji** | Ogranicza pakiety rumble do 1 na 150ms — eliminuje pętle i zacinanie silników |
| 🎛️ **Edytor mapowań / makr** | Pełny edytor wizualny profili — przypisz dowolny klawisz lub makro do każdego przycisku |
| 🕹️ **Wbudowany tester kontrolera** | Tester wejść w czasie rzeczywistym — sprawdź przyciski, osie i triggery na żywo |
| 🔁 **Rapid Fire** | Przypisz rapid fire do dowolnego przycisku |

---

### 🕹️ Tryby pracy analogów

Każdy analog można niezależnie ustawić w jednym z **4 trybów pracy**:

| Tryb | Opis |
|---|---|
| 🕹️ **Analog** | Standardowy sygnał analogowy — pełny zakres osi, tryb domyślny |
| 🔲 **Cyfrowy** | Analog działa jak D-Pad — snap do 8 kierunków |
| 🖱️ **Mysz** | Ruch analoga steruje kursorem myszy na PC |
| ⌨️ **Klawiatura** | Kierunki analoga mapowane na klawisze klawiatury |

---

### 🎮 Zaawansowana konfiguracja kontrolera

| Opcja | Opis |
|---|---|
| ↔️ **Martwe strefy** | Regulowane wewnętrzne i zewnętrzne martwe strefy dla analogów i triggerów |
| 🔄 **Zamiana D-Pad ↔ Lewy Analog** | Cyfrowa zamiana funkcji D-Pada i lewego analoga |
| 🎚️ **Zakres pracy triggerów** | Ustaw własny zakres min/max dla triggerów analogowych — precyzyjna regulacja czułości |
| ⚡ **Rapid Fire** | Rapid fire per-przycisk z regulowaną częstotliwością |
| 🗺️ **Profile** | Zapisywanie i wczytywanie wielu profili konfiguracji dla różnych gier |

---

### 🔋 Oszczędzanie baterii
