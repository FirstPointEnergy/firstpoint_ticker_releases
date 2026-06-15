# ⚡ FirstPoint Ticker

### Your solar battery's heartbeat — on a beautiful, glanceable display.

The **FirstPoint Ticker** turns a tiny ESP32-S3 screen into a live window onto
your **EG4 solar + battery system**. State-of-charge, solar production, house
load, grid flow, and generator — the whole energy picture, updating in real time,
sitting on your desk or wall instead of buried in an app you have to go open.

No laptop. No dashboard tab. Just look up and *know*.

> 📦 **This repo hosts the firmware releases that ship to devices.** The Ticker
> updates itself over the air — every binary your device flashes overnight comes
> from right here. Grab the latest under [**Releases**](../../releases/latest).

---

## ✨ What it does

- **🔋 Live state-of-charge, front and center.** A bold, instantly-readable
  battery ring tells you exactly how much runway you have left — at a glance,
  from across the room.
- **🌞 The whole power flow, animated.** Watch energy move: solar → house →
  battery → grid. Charging and discharging animate in real time so the system
  *feels* alive, not like a spreadsheet.
- **📊 48-hour history graph.** Swipe over to a gorgeous kW + SOC timeline. Tap
  any point to inspect the exact moment — perfect for "what happened last night?"
- **🏠 Smart house-load math.** Even when your inverter under-reports
  consumption, the Ticker derives true house load from the energy balance — the
  same way the pros do it.
- **🔌 Generator-aware.** When the genny kicks in, the Ticker knows.
- **🎛️ A details view for the curious.** One tap surfaces per-string PV voltage,
  per-leg load, battery voltage, state-of-health, and more.

## 🛰️ Two ways to connect — your choice

| Mode | How it works | Needs internet? |
|------|--------------|-----------------|
| **☁️ Cloud** | Logs into the EG4 monitor portal over Wi-Fi | Yes |
| **🔗 Local (RS485)** | Reads the inverter **directly** over Modbus/RS485 | **No!** |

The **local RS485 mode** is the magic trick: a fully **offline**, internet-free
readout that talks straight to the inverter over a wire. Your data never leaves
the building. It's **read-only** by design — the Ticker *listens*, it never
writes to your inverter.

## 🖥️ Runs on multiple displays

One firmware, multiple form factors — pick the screen that fits your space:

- **CrowPanel 1.28" round** — a jewel of a display driven by a satisfying rotary
  knob. Tiny, gorgeous, desk-friendly.
- **Waveshare 7" touch** — a big, bright 800×480 touchscreen dashboard with
  swipeable history and tap-to-explore details.

## 🔄 It updates itself

Set it and forget it. Every night the Ticker quietly checks for new firmware,
and if there's an update it downloads and installs it **all on its own** — then
boots straight back to your dashboard. No cables, no fuss, no "is my firmware
out of date?" Ever. (Prefer to do it now? **Settings → Check for updates.**)

Updates are delivered straight from this public release channel and verified for
integrity before they're ever booted — a bad download can never brick your
device.

## 🚀 Get a device updated

1. Grab the binary for your board from [**the latest release**](../../releases/latest):
   - `crowpanel-128.bin` — CrowPanel 1.28" round
   - `esp32s3-touch-lcd-7.bin` — Waveshare 7" touch
2. Flash it once. After that, the Ticker keeps *itself* current automatically.

---

<div align="center">

**FirstPoint Ticker** — built by [FirstPoint Energy](https://fpes.ca) ⚡<br>
*See your power. Trust your power.*

</div>
