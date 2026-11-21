# 🛰️ ORBITWATCH // Space & Celestial Object Tracker

A real-time **1 Hz SGP4 Orbital Approach Radar** and **First-Person AR Sky Tracker** built for both **Desktop PC (`index.html`)** and **Google Pixel Phones (PWA + Live Compass/Gyro)**.

---

## ✨ Key Features

### 1. 🛰️ Screen 1 (Default): Top-Down Orbital Radar & Approach Tracker (Satellites Only)
- **Dual-Zone Top-Down Polar Radar**:
  - **Inner Sky Dome (`0°` to `90°` Elevation)**: Objects currently above your local horizon (`90°` Zenith at center).
  - **Outer Near / Approach Zone (`0°` down to `-15°` Elevation / ~3,500 km)**: See nearby orbital objects approaching your sky before they cross the horizon, or switch between `Overhead + Near Zone (-15°)`, `Overhead Only (0°+)`, and `Wide Regional (-25° / 5,000 km)`.
- **Moving Closer vs. Moving Away (Live Radial Range-Rate $\dot{\rho}$)**:
  - Computes exact line-of-sight range rate ($\text{km/s}$) and Time to Closest Approach (**TCA**) every second:
    - 🟢 **`▼ MOVING CLOSER`** ($\dot{\rho} < -0.04\text{ km/s}$): Approaching your location, with countdown to closest approach and minimum distance.
    - 🟠 **`▲ MOVING AWAY`** ($\dot{\rho} > +0.04\text{ km/s}$): Receding from your location.
- **Global Ground Track & Footprint Map**:
  - Uses **CartoDB Dark Matter**, **Esri Dark Gray**, and **Esri World Satellite Imagery** tiles (plus a built-in vector graticule) that work both online and when `index.html` is opened directly from a local PC folder via `file://` (solving OpenStreetMap's `403 Access blocked` tile policy on local files).

### 2. 🔭 Screen 2: First-Person Sky View (Point Phone N / E / S / W + Moon & Planets)
- **Moon & 5 Visible Planets (Exclusive to First-Person Sky View)**:
  - Real-time astronomical ephemeris for **The Moon** (with custom-rendered illuminated phase terminator, illumination %, and phase name) and **Mercury (`☿`)**, **Venus (`♀`)**, **Mars (`♂`)**, **Jupiter (`♃`)**, and **Saturn (`♄`, with tilted planetary rings)**, alongside 16 named bright reference stars (`Sirius`, `Vega`, `Arcturus`, `Polaris`, etc.) and overhead satellites.
- **Pixel Phone Live Compass & 2-Axis Gyro**:
  - Tap **`🧭 Point Phone (Live Compass / Gyro)`** to point your phone North, East, South, West, and anywhere in between, or tilt upward toward the zenith (`0°` to `85°` elevation).
  - Includes clickable off-screen target guide arrows on the left/right edges of the viewport to guide you toward the Moon, planets, or selected satellites.
