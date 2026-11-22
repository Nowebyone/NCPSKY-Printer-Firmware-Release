# NCPSKY Firmware (public)

Public **OTA package** repository for NCPSKY printer products.

- **Not** full application source (that stays in the private `ncpsky-printer-dev` workspace).
- Layout follows NCPSKY OTA static hosting conventions.

```text
ncpsky-ota/
  manifest.json
  channels/{stable,beta,dev}.json
  packages/*.zip|*.bin (+ .sha256)
catalogs/          # human-readable per-printer notes
```

## Current baseline (FLSun T1 Max / NCPSKY ▲ DTMax)

| Package | Version | Notes |
|---------|---------|-------|
| stack | `2026.11.23.1` | Host Klipper+Moonraker+macros; **KlipperCore 0.14.0** |
| mcu | `mcu-20261122` | `stm32f103xe`; flash requires on-panel confirm |
| panel | (ship separately when publishing panel zips) | semver |

`firmware_target` must be `FLSun T1 Max`.

## Consume on device

Point `ota/config.json` → this repo’s raw/static URL or a mirror, channel `dev`/`beta`/`stable`.
