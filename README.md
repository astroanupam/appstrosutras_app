# AppstroSutras

**AppstroSutras by Anoopam Shukla** – a Vedic (sidereal) horoscope simulator and rule-book research workbench.

One codebase, three ways to use it:

| Platform | How |
|---|---|
| **Web** | Open the GitHub Pages link in any modern browser |
| **Android** | Open the link in Chrome → menu ⋮ → **Install app** / **Add to Home screen** |
| **iPhone / iPad (iOS)** | Open the link in **Safari** → Share → **Add to Home Screen** |
| **Desktop (Windows / Mac / Linux)** | Open the link in Chrome or Edge → install icon in the address bar → **Install** |

Once opened online the first time, the app works **offline**.

## Publish on GitHub (free, no coding)

1. Sign in at github.com → **New repository** → name it e.g. `appstrosutras` → **Public** → Create.
2. Click **uploading an existing file**, drag in **all files of this folder** (`index.html`, `manifest.webmanifest`, `sw.js`, the three `.png` icons, `README.md`) → **Commit changes**.
3. Repository → **Settings** → **Pages** → *Build and deployment* → Source: **Deploy from a branch** → Branch: **main**, folder **/ (root)** → **Save**.
4. After about a minute your app is live at `https://YOUR-USERNAME.github.io/appstrosutras/`.

### Releasing an update
Replace `index.html` in the repository with the new one, and change `CACHE = 'appstrosutras-v1'` in `sw.js` to `v2`, `v3`… so installed copies refresh.

## Settings (top bar)
- **Theme:** Auto / Light / Dark
- **Language:** English / हिन्दी / ગુજરાતી (menus, tables, planet, sign and nakshatra names; long explanatory notes stay in English)
- **Chart style:** North Indian / South Indian
Your choices are remembered on each device.

## Choosing a chart
On **Home** and **Birth Details** use *Select a chart*: type part of a name, tap a letter A-Z, or pick from the drop-down list. The selected chart is used by every menu.

## Horary
The **Horary** menu shows Natal D1, Natal D9 and Transit-on-D1 side by side, with the 3-level dasha, Ashtakavarga details, natal and transit planetary tables. *Locate an event*: pick any date/time (or a recorded life event) to see the dasha and transit for that moment; **Transit Now** jumps to the present.

## Consultation management
- **Home › Consultant details:** save your name, contact, email, city, country and expertise (Vedic / KP / Jaimini) and a disclaimer. They print at the bottom of every report.
- **Consultation menu:** select a chart; you get D1 · D9 · Transit side by side, the 3-level dasha, planetary details and Sarvashtakavarga. **Add Consultation** opens two boxes (*Your queries*, *Observation / Remedy*); **Save** logs it with the date and an ID such as **CON-NAR-50-13112026-01** (first 3 letters of the name, last 2 digits of the birth year, consultation date DDMMYYYY, running count for that chart). **Edit** reopens an entry and **Update** saves the change.
- **Report buttons:** Save (HTML file), Print, PDF (choose *Save as PDF* in the print window) and Browser view.

## Jaimini menu (after Dasha)
**Jaimini Sutras** shows D1 and D9 with bhava (orange) and graha (green) arudha padas marked, a planetary table with Chara Karaka and Arudha, Chara Karaka 7 / 8 choice, and the Chara and Kalachakra dashas. **Arudhas** has the Jagannatha-Hora-style options (exceptions for bhava and graha arudhas, Rahu/Ketu as co-lords, longitude-based, divisional longitudes, base = Lagna / planet / Bhavalagna) and a chart drop-down for D1-D60. Also **Chara Karakas** and **Rashi Drishti**.

**UKJ Chara Karaka** (Jaimini sub-menu): ranks planets by their position inside the occupied Navamsha (0'-200'), seven or eight karaka scheme, with tie detection, a Rahu rule option, a comparative tab (UKJ vs traditional), a full calculation trace and a built-in self-test table. It only reads the existing D-1 positions.

## Preferences (Home › Preferences)
Calculation defaults (ayanamsa, node, house system, divisional method for new charts; Chara Karaka 7/8; dasha year length; hora; weekday start; Sodhana) and display options (theme, language, chart style, text size, date, time and degree format), with Save, Restore Defaults, Parashari and KP presets, and *Apply to all saved charts*.

## Amsa Rulers (Charts › Amsa Rulers)
Division, index and ruler name for Lagna and planets in any varga (D-60 list loaded; other lists to be added).

## Panchang
**Astro Lab › Workspace** now ends the chart page with a complete *Panchang at birth*: vara, tithi, nakshatra, yoga and karana with start and end times; sunrise, sunset, moonrise, moonset; lunar month (Amanta and Purnimanta), ritu, ayana, Vikram and Shaka Samvat and Samvatsara; Rahu Kalam, Yamaganda, Gulika, Abhijit and Brahma Muhurta; and the 24 horas. **Astro Lab › Panchanga** shows the same for any date and time.

## KP (Krishnamurti Paddhati)
The **KP** menu (after Horary) has: KP chart and Chalit chart (Placidus houses); planets and cusps with sign / star / sub / sub-sub lords and the houses each lord signifies; house and planet significators (A-D levels); ruling planets, dasha and transit tables for any moment; event analysis; and **KP Horary** where you pick a number from 1 to 249 to set the Lagna. The KP page has its own controls (they do not change the rest of the app): **Ayanamsa** (any system, or **Custom** to type your own value as degrees or d:m:s), **Rahu/Ketu** True or Mean, and **Houses** Placidus or Equal. *Reset to KP defaults* returns to Krishnamurti ayanamsa, true node, Placidus.

## Text size
Use **A- / A+** in the top bar (next to Theme) to make text smaller or larger; click the percentage to reset.

## Default place
In **Birth Details › New Chart** tick *Keep this place as the default place for new charts*. The next new chart opens with that place filled in and locked; untick it to enter a different place.

## Your data
- Horoscopes, events and rules are stored **in the browser on each device** (nothing is sent to any server).
- Different devices do **not** sync. Use **Research → Backup & Export** to download a backup file and **Restore** it on another device.
- The repository contains only the program and four public-figure sample charts. Do not upload clients' birth data.

## Notes
- First load needs internet once (the planet-position library `astronomy-engine` is fetched from jsDelivr and then cached).
- Method notes and the conventions used for Shadbala, Sodhana, Chara/Narayana dasha and others are shown on each screen.
