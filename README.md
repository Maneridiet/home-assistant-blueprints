# Maneridiet's Home Assistant Blueprints

A growing collection of reusable [Home Assistant](https://www.home-assistant.io) blueprints (automations).  
All blueprints are importable with a single click via the **Home Assistant Blueprint Import** feature.

---

## 📥 How to use

1. Click the **Import Blueprint** badge below each automation.  
2. Home Assistant will open and let you review the blueprint before saving.  
3. Create an automation from the imported blueprint and customize the inputs.  

> Each blueprint has its own description, inputs, and changelog.  
> For support and discussion, check the linked [Community Forum](https://community.home-assistant.io/c/blueprints-exchange/53).

---

## ☕ Coffee Machine Reminder (iOS interactive)

**Languages:** 🇩🇪 Deutsch · 🇬🇧 English  
**Description:** Sends an interactive iOS push notification if the coffee machine has been on too long. Choose *Keep On* or *Turn Off*. Auto-off after timeout.

**Features:**
- Configurable runtime before notification (default: 40 minutes)
- Configurable response timeout (default: 5 minutes)
- Interactive push notifications with action buttons
- Automatic cleanup of notifications
- Support for multiple iOS devices

**Requirements:**
- iOS device(s) with Home Assistant Companion app
- A switch entity (e.g., coffee machine, smart plug)

**DEUTSCH:**

[![Import DE](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_ios_de.yaml)

**ENGLISH:**

[![Import EN](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_ios_en.yaml)

---

## 📖 Version History

See [CHANGELOG.md](./CHANGELOG.md) for detailed version history and features added in each release.  
All blueprints follow [Semantic Versioning](https://semver.org/) (MAJOR.MINOR.PATCH).

---

## 📜 License

This repository is licensed under the [MIT License](./LICENSE).  
You are free to use, share, and adapt the blueprints with attribution.