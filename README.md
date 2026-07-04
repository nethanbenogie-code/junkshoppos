# Junkshop POS (PWA)

Simple nga POS para sa junkshop — timbang, presyo, gastos, resibo, ug report. Mogana sa cellphone, tablet, ug desktop, ug pwede i-install isip app (PWA) nga mogana bisan walay internet.

## Mga file

| File | Para sa unsa |
|---|---|
| `index.html` | Ang tibuok app — tanan nga code naa sa usa ka file |
| `sw.js` | Service worker aron mogana offline (kinahanglan sa browser nga bulag kini nga file) |

## Unsaon pag-upload sa GitHub Pages (libre)

1. Paghimo og bag-ong repository sa GitHub (pananglitan `junkshop-pos`).
2. I-upload ang `index.html` ug `sw.js` sa root sa repo (Add file → Upload files).
3. Adto sa **Settings → Pages**.
4. Sa "Source", pilia ang **Deploy from a branch**, branch: `main`, folder: `/ (root)`, unya **Save**.
5. Human sa 1-2 ka minuto, maabli na ang app sa:
   `https://IMONG-USERNAME.github.io/junkshop-pos/`

## Unsaon pag-install sa cellphone

**Android (Chrome):** Ablihi ang link → menu (⋮) → **Add to Home screen** / **Install app**.

**iPhone (Safari):** Ablihi ang link → Share button → **Add to Home Screen**.

Kung na-install na, mogana kini bisan walay signal o WiFi. Ang tanan nga presyo, rekord, ug gastos naka-save sa mismong device (localStorage).

## Mga tab

- **Timbang** — palit gikan sa suki o baligya sa buyer, per kilo, daghang item sa usa ka resibo
- **Presyo** — usba ang presyo sa palit/baligya matag kilo, idugang o papasa ang mga item, detalye sa shop
- **Gastos** — irekord ang mga gasto (kuryente, tubig, sweldo, plete, ug uban pa)
- **Rekord** — tanang transaksyon matag adlaw, pwede i-print pag-usab ang resibo
- **Report** — karon / 7 adlaw / bulan / tanan, apil ang gastos ug netong ginansya, pwede i-print

## Pag-print

- **Resibo** — pindota ang 🖨 tapad sa transaksyon sa Rekord tab, o i-on ang auto-print sa Presyo tab. Ang resibo naka-format para sa 58mm thermal printer (pwede sab regular printer).
- **Report** — sa Report tab, pilia ang panahon unya pindota ang "I-print ang report". Apil sa report ang mga gastos ug ang netong ginansya (baligya − palit − gastos).
- Sa Android, mogana ang print sa bisan unsang printer nga naka-setup sa phone (ang Bluetooth thermal printers kasagaran adunay kaugalingong print service app nga mogawas sa print dialog).

## Importante nga pahinumdom

- Ang data naka-save **sa device lang** (localStorage). Kung papason ang browser data o lahi nga device ang gamiton, dili mobalhin ang rekord.
- Usa ka device = usa ka rekord. Kung gusto og backup o multi-device sync, kinahanglan og server/database (bulag kini nga proyekto).
