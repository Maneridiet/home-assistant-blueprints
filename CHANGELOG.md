# Changelog

All notable changes to the blueprints will be documented in this file.

## ☕ Coffee Machine Reminder (iOS interactive)

### 1.1.0 - 2025-08-26
- Added Android versions (DE/EN) with platform-specific optimizations:
  - Custom notification channel
  - Vibration pattern support
  - High-priority and sticky notifications
  - Android-specific device filtering
- Full language support for both German and English Android versions

### 1.0.0 - 2025-08-26
- Initial release with both German (DE) and English (EN) versions for iOS
- Features:
  - Configurable runtime monitoring (default: 40 minutes)
  - Interactive iOS notifications with action buttons
  - Configurable response timeout (default: 5 minutes)
  - Automatic cleanup of notifications
  - Support for multiple iOS devices
- Both language versions use the same efficient notification structure
- Full support for Home Assistant Blueprint Import feature