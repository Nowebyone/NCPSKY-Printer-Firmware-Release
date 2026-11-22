# NCPSKY Firmware Release（公开仓 · 多产品共用）

本仓**只发 OTA 包**，不发完整私有源码。  
**一种产品一条目录**；多台同型号机器共用同一 `product_id` 通道。

```text
ota/
  <product_id>/                 # 例：ncpsky-dtmax、未来 ncpsky-xxx
    channels/{stable,beta,dev}.json
    packages/*.{zip,bin} + .sha256
    manifest.json               # 可选；通常 stable 切片
catalogs/
  INDEX.md
  <product_id>.json             # 人类可读基线说明
```

## 已登记产品

| product_id | 品牌 | firmware_target | 目录 |
|------------|------|-----------------|------|
| `ncpsky-dtmax` | NCPSKY ▲ DTMax | FLSun T1 Max | [`ota/ncpsky-dtmax/`](ota/ncpsky-dtmax/) |

新增产品：复制 `ota/_template/`（见下）→ `ota/<product_id>/`，并更新本表与 `catalogs/INDEX.md`。

## 机上怎么指到本仓

```json
"source": "github",
"github": {
  "owner": "Nowebyone",
  "repo": "NCPSKY-Printer-Firmware-Release",
  "ref": "main",
  "mode": "raw",
  "path_prefix": "ota/<product_id>"
}
```

Raw 例：  
`https://raw.githubusercontent.com/Nowebyone/NCPSKY-Printer-Firmware-Release/main/ota/ncpsky-dtmax/channels/dev.json`
