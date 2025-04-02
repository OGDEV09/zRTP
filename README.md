# 🌍 zRTP - Random Teleport Plugin 

✨ **Ein hochgradig anpassbares Random-Teleport-Menü-System für Minecraft-Server**

---

## 📋 Features
- 🖼️ **Schönes GUI-Menü** mit anpassbaren Buttons
- 🌎 **Multi-Welt-Support** (Overworld, Nether, End)
- ⏳ **Countdown-System** mit Bewegungsprüfung
- 🛠️ **Vollständig konfigurierbar** über config.yml
- 📊 **Berechtigungs-System** für Admin-Befehle
- 💬 **Anpassbare Nachrichten** und Action-Bars

---

## ⚠️ Voraussetzungen
- [BetterRTP](https://www.spigotmc.org/resources/betterrtp-random-wild-teleport.36081/) muss installiert sein!
- Minecraft Server 1.16+
- Java 8+

---

## 🚀 Installation
1. Installiere zuerst [BetterRTP](https://www.spigotmc.org/resources/betterrtp-random-wild-teleport.36081/)
2. Lade zRTP herunter
3. Platziere die `.jar`-Datei in deinem `plugins`-Ordner
4. Starte deinen Server neu
5. Konfiguriere das Plugin nach deinen Wünschen

---

## 🎮 Befehle & Berechtigungen
| Befehl | Beschreibung | Berechtigung |
|--------|--------------|--------------|
| `/rtp` | Öffnet das Random-Teleport-Menü | `zrtp.use` (default: true) |
| `/rtp reload` | Lädt die Konfiguration neu | `zrtp.reload` (default: op) |
| `/rtp help` | Zeigt die Hilfe an | - |

---

## ⚙️ Konfiguration
```yaml
# config.yml
menu:
  title: "&8ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ"
  items:
    overworld:
      material: GRASS_BLOCK
      name: "&aᴏᴠᴇʀᴡᴏʀʟᴅ"
      lore:
        - ""
        - "&fᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ ɪɴ ᴛʜᴇ &2ᴏᴠᴇʀᴡᴏʀʟᴅ"
        - ""
      slot: 11
    nether:
      material: NETHERRACK
      name: "&4ɴᴇᴛʜᴇʀ"
      lore:
        - ""
        - "&fᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ ɪɴ ᴛʜᴇ &4ɴᴇᴛʜᴇʀ"
        - ""
      slot: 13
    end:
      material: END_STONE
      name: "&eᴇɴᴅ"
      lore:
        - ""
        - "&f&lᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ ɪɴ ᴛʜᴇ &e&lᴇɴᴅ"
        - ""
      slot: 15

# BetterRTP Commands (MUSS installiert sein!)
commands:
  overworld: "betterrtp world {world}"
  nether: "betterrtp world {world}_nether"
  end: "betterrtp world {world}_the_end"

countdown:
  duration: 5 # Sekunden
  messages:
    - "&aTeleport in &e%time% &aSekunden... &cNicht bewegen!"
  cancelled: "&cTeleport abgebrochen, weil du dich bewegt hast!"
  no-permission: "&cDu hast keine Berechtigung!"
  players-only: "&cNur Spieler können dies nutzen!"
