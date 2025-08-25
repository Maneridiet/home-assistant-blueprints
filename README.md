# Home Assistant Blueprint – Coffee Prompt iOS

After a configurable run time (default **40 min**), send an interactive iOS push with
**An lassen** / **Ausschalten** for a selected switch. If there’s no reply within
**5 min**, it can switch off automatically. The original notification is cleared in all outcomes.

## Import
[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https://raw.githubusercontent.com/Maneridiet/home-assistant-blueprints/main/blueprints/automation/Maneridiet/coffee_prompt_ios.yaml)

## Notes
- Uses `mobile_app` device notifications (no hard-coded notify services)
- iOS “time-sensitive” push included (harmless on Android) 
- Version: v1.0.0
