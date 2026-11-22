# OTA product template

Copy this folder to `../<product_id>/` then add:

- `channels/dev.json` (and later beta/stable)
- `packages/` artifacts + `.sha256`

Keep `firmware_target` / `product` fields inside manifests accurate — devices reject mismatches.
