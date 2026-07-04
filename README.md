# Meat Shop POS (PWA)

POS para sa **karnehan sa merkado** — digital scale display nga adunay keypad para sa kilo, sukli calculator, imbentaryo nga awtomatik maminusan ang stock, report nga adunay ginansya, ug backup. Mogana sa cellphone, tablet, ug desktop, ug pwede i-install isip app nga mogana bisan walay internet.

## Mga file

| File | Para sa unsa |
|---|---|
| `index.html` | Ang tibuok app — apil na ang mga icon |
| `sw.js` | Service worker aron mogana offline |

## Unsaon pag-upload sa GitHub Pages (libre)

1. Paghimo og bag-ong repository sa GitHub (pananglitan `meatshop-pos`).
2. I-upload ang `index.html` ug `sw.js` sa root sa repo.
3. **Settings → Pages** → Source: **Deploy from a branch** → branch `main`, folder `/ (root)` → **Save**.
4. Maabli ang app sa: `https://IMONG-USERNAME.github.io/meatshop-pos/`

## Pag-install sa cellphone

**Android (Chrome):** Ablihi ang link → menu (⋮) → **Install app** / **Add to Home screen**.
**iPhone (Safari):** Share button → **Add to Home Screen**.

## Mga tab

- **Timbang** — ang tindahan. Pilia ang putol sa karne, i-type ang **kilo** sa keypad (makita sa scale display ang presyo dayon), idugang sa resibo. Daghang item sa usa ka resibo. **Bayad**: i-type ang kwarta ug makita dayon ang **sukli**.
- **Karne** — ang imbentaryo. Naka-andam na ang naandang mga putol (Liempo, Kasim, Pigue, Buto-buto, Pata, Giniling, Manok, Pecho, Pakpak, Baka, Chorizo, Longganisa) — **usba ang presyo aron motakdo sa presyo sa merkado karon**. Pwede magdugang, adunay litrato (opsyonal, gamit ang camera), presyo, puhunan, ug stock sa kilo. Ang matag produkto pwede **kada kilo** o **kada piraso** (para sa chorizo, longganisa, itlog, ubp.). Awtomatik nga maminusan ang stock kada halin.
- **Rekord** — tanang halin matag adlaw; pwede i-print pag-usab ang resibo.
- **Report** — karon / 7 adlaw / bulan / tanan: halin, puhunan, **ginansya**, kilo nga nabaligya, ug per-produkto nga breakdown; pwede i-print.
- **Setting** — ngalan sa karnehan, auto-print sa resibo, **gidak-on sa letra (A− / A+)**, backup ug restore.

## Database ug Backup

- Ang data naka-save sa **IndexedDB** sa mismong device — kaya niini ang daghang produkto nga adunay litrato.
- **Backup (JSON)** sa Setting tab — kompleto nga kopya. I-download kada semana ug i-save sa Google Drive o email. **I-restore** aron ibalik o ibalhin sa bag-ong cellphone.
- **CSV — halin** ug **CSV — produkto** — pwede ablihan sa Excel.

## Pahinumdom

- Ang presyo sa karne mausab kanunay — dali ra kining usbon: Karne tab → pindota ang produkto → usba ang presyo → I-save.
- Usa ka device = usa ka database. Kung gusto og sync tali sa duha ka cellphone, kinahanglan og server (bulag nga proyekto).
- Ayaw i-clear ang browser data — kanunay adunay backup.
