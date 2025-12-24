# Maneridiet's Home Assistant Blueprints & Dashboards

A growing collection of reusable [Home Assistant](https://www.home-assistant.io) blueprints (automations), dashboard configurations, and themes.  
All blueprints are importable with a single click via the **Home Assistant Blueprint Import** feature.

---

## 📥 How to use

1. Click the **Import Blueprint** badge below each automation.  
2. Home Assistant will open and let you review the blueprint before saving.  
3. Create an automation from the imported blueprint and customize the inputs.  

> Each blueprint has its own description, inputs, and changelog.  
> For support and discussion, check the linked [Community Forum](https://community.home-assistant.io/c/blueprints-exchange/53).

---

## 📊 Dashboards

Custom Home Assistant dashboard configurations for inspiration and reuse.

### 🏠 Maneridiet's Homescreen

A comprehensive, feature-rich Home Assistant dashboard that showcases advanced UI design and integration capabilities.

**File:** [`dashboards/maneridiets_homescreen.yaml`](./dashboards/maneridiets_homescreen.yaml)

**Features:**
- **Energy Monitoring**: Real-time power flow visualization with solar production, grid consumption, and individual device tracking (heat pump, etc.)
- **Weather Integration**: Live weather warnings with detailed alerts from weather services (DWD or similar)
- **Smart Status Chips**: Dynamic notification system for waste collection reminders, system alerts, weather warnings, and appliance status
- **Media Controls**: Integrated media player with conditional visibility
- **Pet Tracking**: Visual indicators for pet location and activity detection
- **Climate Monitoring**: Indoor and outdoor temperature/humidity displays with weather condition icons
- **Appliance Monitoring**: Washing machine timer, robot vacuum control, and litter box counter
- **Voice Assistant**: Quick access to Home Assistant voice commands
- **Navigation Bar**: Seamless navigation between dashboard views

**Custom Cards Required:**
- `custom:digital-clock` - Stylish clock display
- `custom:mushroom-chips-card` - Smart status indicators
- `custom:mini-media-player` - Media player controls
- `custom:button-card` - Custom interactive buttons
- `custom:power-flow-card-plus` - Energy flow visualization
- `custom:navbar-card` - Dashboard navigation
- `card_mod` - Card styling and customization

**Setup Instructions:**
1. Install all required custom cards via HACS (Home Assistant Community Store)
2. Copy the YAML configuration to your Home Assistant dashboard
3. Replace placeholder entity IDs with your own entities:
   - Weather sensors (`weather.forecast_home`, `sensor.outdoor_temperature`, etc.)
   - Power/energy sensors (`sensor.solar_power_production`, `sensor.grid_power_consumption`, etc.)
   - Waste collection sensors (`sensor.general_waste`, `sensor.organic_waste`)
   - Device trackers (`device_tracker.pet_tracker`)
   - Media players (`media_player.living_room`)
   - Climate sensors (`sensor.indoor_temperature`, `sensor.indoor_humidity`)
   - Appliance entities (`vacuum.robot_vacuum`, `timer.washing_machine`, etc.)
4. Replace image IDs with your own uploaded images
5. Update device IDs for service calls
6. Adjust navigation paths to match your dashboard setup
7. Customize theme and styling to your preferences

**Screenshots:**

*Winter Background*

![Winter Background](https://github.com/user-attachments/assets/14defdd1-48f0-412e-8b7b-8b0a818b4353)

*Generic Background*

![Generic Background](https://github.com/user-attachments/assets/28377f8e-981c-4cd2-965f-d8089a7e48a5)

> **Note:** This dashboard uses extensive templating and conditional logic. All personal information (addresses, specific device IDs, names) has been generalized for privacy. The YAML is heavily commented to help you understand and customize each section.

---

## 🎨 Themes

Custom Home Assistant themes to enhance your dashboard's visual appearance.

### Hodor3 Theme

A dark, elegant theme featuring golden yellow accents on a rich brown/black background. Perfect for a sophisticated, warm aesthetic.

**File:** [`themes/hodor3.yaml`](./themes/hodor3.yaml)

**Color Palette:**
- **Primary Color**: Golden Yellow (`#EEC051`)
- **Accent Color**: Darker Golden Yellow (`#C89E3A`)
- **Background**: Deep Brown/Black (`#16120E`)
- **Text**: Warm Beige (`#E5DFC7`)
- **Secondary Background**: Brown (`#4B4330`)

**Setup Instructions:**
1. Copy the contents of `themes/hodor3.yaml`
2. Add it to your Home Assistant `themes` folder (typically `config/themes/`)
3. If you don't have a `themes` folder, create one in your Home Assistant configuration directory
4. Add the following to your `configuration.yaml` if not already present:
   ```yaml
   frontend:
     themes: !include_dir_merge_named themes/
   ```
5. Restart Home Assistant
6. Go to your profile (click your username in the bottom left)
7. Select "hodor3" from the Theme dropdown

> **Tip:** This theme pairs beautifully with the Maneridiet's Homescreen dashboard for a cohesive, polished look.

---

## ☕ Coffee Machine Reminder

Interactive notification system that monitors your coffee machine and helps prevent it from staying on too long.

### iOS Version 📱

**Languages:** 🇩🇪 Deutsch · 🇬🇧 English  
**Description:** Sends an interactive iOS push notification if the coffee machine has been on too long. Choose *Keep On* or *Turn Off*. Auto-off after timeout.

**Features:**
- Configurable runtime before notification (default: 40 minutes)
- Configurable response timeout (default: 5 minutes)
- Interactive push notifications with action buttons
- Time-sensitive notifications support
- Automatic cleanup of notifications
- Support for multiple iOS devices

**Requirements:**
- iOS device(s) with Home Assistant Companion app
- A switch entity (e.g., coffee machine, smart plug)

**DEUTSCH:**

[![Import DE](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_ios_de.yaml)

**ENGLISH:**

[![Import EN](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_ios_en.yaml)

### Android Version 🤖

**Languages:** �🇪 Deutsch · �🇬🇧 English  
**Description:** Android-optimized version with interactive notifications and vibration patterns for better alerts.

**Features:**
- All core features of the iOS version
- Android-specific notification channel
- Custom vibration pattern
- High-priority notifications
- Sticky notifications until acted upon
- Support for multiple Android devices

**Requirements:**
- Android device(s) with Home Assistant Companion app
- A switch entity (e.g., coffee machine, smart plug)

**DEUTSCH:**

[![Import DE](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_android_de.yaml)

**ENGLISH:**

[![Import EN](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_android_en.yaml)

---

## 📖 Version History

See [CHANGELOG.md](./CHANGELOG.md) for detailed version history and features added in each release.  
All blueprints follow [Semantic Versioning](https://semver.org/) (MAJOR.MINOR.PATCH).

---

## 📜 License

This repository is licensed under the [MIT License](./LICENSE).  
You are free to use, share, and adapt the blueprints with attribution.