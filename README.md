# Junkshop POS (PWA)

Isang simpleng POS para sa junkshop — timbang, presyo, resibo, at ulat. Gumagana sa cellphone, tablet, at desktop, at pwedeng i-install bilang app (PWA) na gumagana kahit walang internet.

## Mga file

| File | Para saan |
|---|---|
| `index.html` | Ang buong app — lahat ng code nasa isang file |
| `sw.js` | Service worker para gumana offline (kailangan ng browser na hiwalay itong file) |

## Paano i-upload sa GitHub Pages (libre)

1. Gumawa ng bagong repository sa GitHub (hal. `junkshop-pos`).
2. I-upload ang `index.html` at `sw.js` sa root ng repo (Add file → Upload files).
3. Pumunta sa **Settings → Pages**.
4. Sa "Source", piliin ang **Deploy from a branch**, branch: `main`, folder: `/ (root)`, tapos **Save**.
5. Pagkatapos ng 1-2 minuto, bubuksan ang app sa:
   `https://IYONG-USERNAME.github.io/junkshop-pos/`

## Paano i-install sa cellphone

**Android (Chrome):** Buksan ang link → menu (⋮) → **Add to Home screen** / **Install app**.

**iPhone (Safari):** Buksan ang link → Share button → **Add to Home Screen**.

Kapag na-install na, gagana ito kahit walang signal o WiFi. Ang lahat ng presyo at talaan ay naka-save sa mismong device (localStorage).

## Pag-print

- **Resibo** — pindutin ang 🖨 sa tabi ng transaksyon sa Talaan tab, o i-on ang auto-print sa Presyo tab. Ang resibo ay naka-format para sa 58mm thermal printer (pwede ring regular printer).
- **Ulat** — sa Ulat tab, piliin ang panahon (Ngayon / 7 Araw / Buwan / Lahat) tapos pindutin ang "I-print ang ulat".
- Sa Android, gumagana ang print sa kahit anong printer na naka-setup sa phone (Bluetooth thermal printers ay karaniwang may sariling print service app na lalabas sa print dialog).

## Mahalagang paalala

- Ang data ay naka-save **sa device lang** (localStorage). Kung buburahin ang browser data o iba ang device na gagamitin, hindi lilipat ang talaan.
- Isang device = isang talaan. Kung gusto ng backup o multi-device sync, kailangan ng server/database (hiwalay na proyekto ito).
