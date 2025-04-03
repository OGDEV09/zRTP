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
        - "&fᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ "
        - ""
    nether:
      material: NETHERRACK
      name: "&4ɴᴇᴛʜᴇʀ"
      lore:
        - ""
        - "&fᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ"
        - ""
    end:
      material: END_STONE
      name: "&eᴇɴᴅ"
      lore:
        - ""
        - "&f&lᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ"
        - ""

commands:
  overworld: "betterrtp world world"
  nether: "betterrtp world world_nether"
  end: "betterrtp world world_the_end"

countdown:
  duration: 5
  messages:
    - "&7Teleporting in %time% &7seconds... &cDon't move!"
  cancelled: "&cTeleport cancelled because you moved!"
  no-permission: "&cYou don't have permission!"
  players-only: "&cOnly players can use this command!"
