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

## 🚀 Installation
1. Lade die neueste Version herunter
2. Platziere die `.jar`-Datei in deinem `plugins`-Ordner
3. Starte deinen Server neu
4. Konfiguriere das Plugin nach deinen Wünschen

---

1. **Befehls-Tabelle** 
   - `/rtp` (Öffnet Menü)
   - `/rtp reload` (Neu laden der Konfig)
   - `/rtp help` (Hilfe anzeigen)

2. **Berechtigungen**
   - `zrtp.use` für Basis-Befehl
   - `zrtp.reload` für Reload-Befeh

---

## ⚙️ Konfiguration
```yaml
# config.yml Beispiel
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
    nether:
      material: NETHERRACK
      name: "&4ɴᴇᴛʜᴇʀ"
      lore:
        - ""
        - "&fᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ ɪɴ ᴛʜᴇ &4ɴᴇᴛʜᴇʀ"
        - ""
    end:
      material: END_STONE
      name: "&eᴇɴᴅ"
      lore:
        - ""
        - "&f&lᴄʟɪᴄᴋ ᴛᴏ ʀᴀɴᴅᴏᴍ ᴛᴇʟᴇᴘᴏʀᴛ ɪɴ ᴛʜᴇ &e&lᴇɴᴅ"
        - ""

commands:
  overworld: "betterrtp world world"
  nether: "betterrtp world world_nether"
  end: "betterrtp world world_the_end"

countdown:
  duration: 5
  messages:
    - "&aTeleporting in &e%time% &aseconds... &cDon't move!"
  cancelled: "&cTeleport cancelled because you moved!"
  no-permission: "&cYou don't have permission!"
  players-only: "&cOnly players can use this command!"
