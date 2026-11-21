# WiFi QR Scanner (`myqr`)

Modern, self-contained QR Code Scanner for MikroTik Hotspot Voucher/Member login.

## Features
- Native `BarcodeDetector` API (hardware-accelerated) + `jsQR` fallback (100% self-hosted, no external CDN requests).
- Modern dark responsive UI with scanning frame animation.
- Flashlight / Torch toggle, Front/Rear camera switcher, and Gallery image upload (`Chọn ảnh QR`).
- Automatically redirects to MikroTik Hotspot login URLs (`http://.../login?username=...`).

## MikroTik Setup
Add `zunzhong.github.io` to Hotspot Walled Garden:
```routeros
/ip hotspot walled-garden ip
add action=accept comment="ZunZhong QR Scanner" disabled=no dst-host=zunzhong.github.io
```
