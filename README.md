# 🧭 Compass

A beautiful, installable compass web app that uses your phone's magnetometer for accurate heading. Works on Android and iOS.

**[Open Compass](https://osama-lotfy.github.io/compass/)** ← tap on your phone

## Features

- 🧭 Real-time compass heading using `AbsoluteOrientationSensor` API
- 📍 GPS coordinates display
- 🌙 Dark theme, easy on the eyes
- 📱 Install as PWA — works offline, appears on your home screen
- 🔒 100% client-side — no data ever leaves your device

## How to Install

1. Open the [live demo](https://osama-lotfy.github.io/compass/) in Chrome on Android or Safari on iOS
2. Tap the **Enable** button to activate sensors
3. For app-like experience: Chrome menu → "Add to Home Screen"

## How It Works

The app queries either:
- **`AbsoluteOrientationSensor`** (modern Android Chrome — quaternion-based, most accurate)
- **`deviceorientationabsolute`** event (Android — absolute heading)
- **`deviceorientation`** with `webkitCompassHeading` (iOS Safari)

The quaternion from the sensor is converted to a yaw (heading) angle, which drives the compass dial rotation.

## Tech

- Vanilla HTML/CSS/JS — zero dependencies
- PWA with service worker for offline support
- Hosted on GitHub Pages (HTTPS required for sensor APIs)
