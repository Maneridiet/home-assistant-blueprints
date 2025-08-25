# Home Assistant Blueprint – Coffee Machine / Kaffeemaschine Reminder (iOS interactive)

This repository provides a Home Assistant blueprint that monitors a switch (e.g. coffee machine).  
If the switch stays on longer than a defined time (default: **40 minutes**), an **interactive iOS notification** is sent.  

You can choose directly in the notification:  
- **Keep On** / **An lassen**  
- **Turn Off** / **Ausschalten**  

If no response is received within the answer window (default: **5 minutes**), the switch will be turned off automatically.  
In all cases, the notification will be cleared afterwards.

---

## 📥 Import

### 🇩🇪 Deutsch
[![Import Blueprint DE](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_ios_de.yaml)

### 🇬🇧 English
[![Import Blueprint EN](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_ios_en.yaml)

Or import manually in Home Assistant:  
**Settings → Automations & Scenes → Blueprints → Import Blueprint**  
and paste one of the RAW URLs above.

---

## ⚙️ Inputs

- **Switch (Schalter)** → The device to monitor and (if required) turn off.  
- **Runtime until reminder (Laufzeit bis Erinnerung)** → Default 40 minutes.  
- **Response timeout (Antwort-Zeitfenster)** → Default 5 minutes.  
- **Target devices (Zielgeräte)** → One or more iOS devices with HA Companion App.  
- **Notification tag (Benachrichtigungs-Tag)** → Identifier to clear the notification (default: `coffee_prompt`).  
- **Titles & messages (Titel & Texte)** → Fully customizable for reminder, auto-off and buttons.  

---

## ✨ Features

- Interactive **iOS push notification** with action buttons  
- iOS **time-sensitive** push (works harmlessly on Android)  
- Automatic clearing of notifications in all cases  
- Automatic turn-off after timeout if no response  
- Multiple devices supported  
- Uses `mobile_app` device notifications (no hard-coded `notify.mobile_app_*` service names)  

---

## 📝 Example Flow

1. Coffee machine is turned on at 07:00.  
2. At 07:40 → Notification:  
   **“Coffee machine has been running for 40 minutes”**  
   Buttons: **Keep On** / **Turn Off**  
3. If you choose **Turn Off** → switch turns off immediately.  
4. If no answer until 07:45 → Auto-off + push:  
   **“No response – turned off automatically.”**

---

## 📌 Changelog

- **v1.0.0** – Initial release (DE + EN)

---

## 📖 License

[MIT License](./LICENSE)
