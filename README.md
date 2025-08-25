# Home Assistant Blueprint – Kaffeemaschine Erinnerung (iOS interaktiv)

Dieses Blueprint überwacht einen Schalter (z. B. Kaffeemaschine).  
Wenn er länger als die eingestellte Zeit **eingeschaltet** bleibt (Standard: 40 Minuten), werden **interaktive iOS-Benachrichtigungen** verschickt.  

Du kannst dann direkt in der Push-Nachricht auswählen: **An lassen** oder **Ausschalten**.  
Reagierst du nicht innerhalb des eingestellten Zeitfensters (Standard: 5 Minuten), wird das Gerät automatisch ausgeschaltet.  
In allen Fällen wird die Benachrichtigung anschließend wieder entfernt.

---

## Importieren

[![Import Blueprint](https://my.home-assistant.io/badges/blueprint_import.svg)](https://my.home-assistant.io/redirect/blueprint_import/?blueprint_url=https%3A%2F%2Fraw.githubusercontent.com%2FManeridiet%2Fhome-assistant-blueprints%2Fmaster%2Fblueprints%2Fautomation%2FManeridiet%2Fcoffee_prompt_ios.yaml)

Oder in Home Assistant:  
**Einstellungen → Automatisierungen & Szenen → Blueprints → Importieren** und dort den RAW-Link einfügen:

https://raw.githubusercontent.com/Maneridiet/home-assistant-blueprints/master/blueprints/automation/Maneridiet/coffee_prompt_ios.yaml

---

## Eingaben

- **Kaffeemaschinen-Schalter**  
  Welcher Schalter überwacht/geschaltet wird.

- **Laufzeit bis zur Erinnerung**  
  Dauer, die der Schalter „an“ sein muss, bevor die Benachrichtigung ausgelöst wird.  
  *Standard: 40 Minuten*

- **Antwort-Zeitfenster**  
  Zeit, die nach der Benachrichtigung auf eine Antwort gewartet wird.  
  *Standard: 5 Minuten*

- **Zielgeräte (iOS)**  
  Ein oder mehrere iPhones/iPads mit Home Assistant Companion App.

- **Benachrichtigungs-Tag**  
  Kennung, um die Push später automatisch zu schließen.  
  *Standard: `coffee_prompt`*

- **Texte (Titel/Nachricht)**  
  Anpassbar für Erinnerung, Auto-Off und die Schaltflächen *An lassen* / *Ausschalten*.

---

## Features

- iOS **Zeitkritische Benachrichtigung** (interruption-level: time-sensitive)  
- Unterstützt mehrere iPhones/iPads gleichzeitig  
- Automatische Aufräumung der Push-Nachrichten  
- Automatisches Ausschalten bei Nicht-Reaktion  
- Keine hartkodierten `notify.mobile_app_*` Services → funktioniert auch bei umbenannten Geräten  

---

## Beispiel

- Die Kaffeemaschine läuft um 7:00 Uhr los.  
- Um 7:40 Uhr erscheint eine Push:  
  **„Kaffeemaschine läuft seit 40 Minuten“**  
  mit den Buttons **An lassen** / **Ausschalten**.  
- Wählst du **Ausschalten**, wird der Schalter sofort aus gemacht.  
- Keine Antwort bis 7:45 Uhr? → Auto-Off + Push „Keine Antwort – wurde automatisch ausgeschaltet“.

---

## Changelog

- **v1.0.0** – Erste Veröffentlichung

---

## Lizenz

[MIT License](./LICENSE)
