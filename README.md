# symmetrical-barnacle
A tool for tracking moves by the world's largest hedge fund managers, based on public **SEC 13F** filings and **Congress trade** disclosures.
# 🐋 Smart Money Tracker

> **Ελληνικά** | [English](#english)

---

## Ελληνικά

Εργαλείο παρακολούθησης κινήσεων των μεγαλύτερων hedge fund managers, βασισμένο σε δημόσια αρχεία **SEC 13F** και αποκαλύψεις **Congress trades**.

### Χρήση

Άνοιξε το `smart-money-tracker.html` σε οποιοδήποτε browser. Δεν χρειάζεται εγκατάσταση ή διακομιστής.

---

### Tabs

#### 📊 Hedge Funds (13F)
- Κλίκαρε μια **κάρτα επενδυτή** για να δεις τις θέσεις του.
- Κλίκαρε **κεφαλίδα στήλης** για ταξινόμηση (ascending/descending).
- Χρησιμοποίησε το **πλαίσιο αναζήτησης** για φιλτράρισμα ανά εταιρεία.
- Τύποι θέσεων: `SH` = μετοχές (long) · `Call` = ανοδική επιλογή · `Put` = καθοδική επιλογή · `PRN` = ομολογία.
- Τα 13F είναι **τριμηνιαία** — δείχνουν θέσεις στο τέλος κάθε quarter με καθυστέρηση 45 ημερών.
- Για μεγάλα funds (Bridgewater, Citadel, Millennium, Tudor) υπάρχει σύνδεσμος προς SEC EDGAR και WisdomWale.

#### 🏛 Congress Trades
- Σύνδεσμοι προς live πλατφόρμες παρακολούθησης συναλλαγών βουλευτών & γερουσιαστών.
- Οι πολιτικοί υποχρεούνται να αποκαλύπτουν συναλλαγές εντός **45 ημερών** (νόμος STOCK Act).
- Ο πίνακας κάτω δείχνει ενδεικτικές γνωστές κινήσεις — για πλήρη live δεδομένα χρησιμοποίησε τους συνδέσμους.

#### 🔔 Real-Time Insider
- Τελευταίες συναλλαγές **Form 4** από το [Dataroma](https://dataroma.com/m/rt.php) — αρχεία υποβλημένα στη SEC από μεγάλους επενδυτές εντός 2 εργάσιμων ημερών.
- Σύνοψη αγορών/πωλήσεων στην κορυφή + πλήρης πίνακας με ημερομηνία, fund, τίτλο, τύπο κίνησης, μετοχές, τιμή και αξία.
- `Buy` = bullish · `Sell` = bearish.

#### 🎯 Smart Money Score
- Ενοποιεί 13F + Form 4 + Congress trades σε ένα βαθμό πεποίθησης (0–100) ανά μετοχή.
- Εμφανίζει μόνο μετοχές που κατέχουν 2+ επενδυτές.
- Φόρμουλα: Αριθμός επενδυτών 35% · Αξία 13F 35% · Insider RT ±15% · Congress ±10% · Συγκέντρωση 5% · Put penalty −5.
- Badges: 🔥 ≥60 · ✅ 40–59 · ⚠️ 20–39 · 🔵 <20.
- Φιλτράρισμα: Όλες / Με signal / Μόνο Congress.

#### 📈 Κοινές Θέσεις
- Μετοχές που κατέχουν **2 ή περισσότεροι** επενδυτές ταυτόχρονα.
- **Τιμή Q1 2026** = κλείσιμο 31/3/2026, υπολογισμένη από τα 13F: `(Αξία $000 × 1000) ÷ Μετοχές`.
- **Τιμή σήμερα** = ανανεώνεται με το κουμπί 🔄 από Yahoo Finance.
- Η μπάρα χρώματος δείχνει το μέγεθος της κίνησης: 🟢 άνοδος / 🔴 πτώση.
- `PUT⚠️` = ο επενδυτής έχει bearish θέση (κερδίζει αν πέσει η μετοχή).

---

### Κουμπιά

| Κουμπί | Λειτουργία |
|--------|-----------|
| `🌙` / `☀️` | Εναλλαγή dark / light mode. Η επιλογή αποθηκεύεται αυτόματα. |
| `EN` / `ΕΛ` | Εναλλαγή γλώσσας. Αλλάζει όλο το interface. Αποθηκεύεται αυτόματα. |
| `❓ Οδηγίες` | Ανοίγει το παράθυρο βοήθειας (κλείνει με `Esc` ή κλικ εκτός). |
| `🔄 Ανανέωση τιμών` | Συνδέεται με Yahoo Finance για τρέχουσες τιμές στο tab Κοινές Θέσεις. |

---

### Επενδυτές

| Επενδυτής | Fund | Περίοδος |
|-----------|------|----------|
| Michael Burry | Scion Asset Management | Q3 2025 |
| Bill Ackman | Pershing Square | Q1 2026 |
| Stan Druckenmiller | Duquesne Family Office | Q1 2026 |
| David Tepper | Appaloosa LP | Q1 2026 |
| Warren Buffett | Berkshire Hathaway | Q1 2026 |
| George Soros | Soros Fund Management | Q1 2026 |
| Carl Icahn | Icahn Capital | N/A (σταμάτησε 2011) |
| Ray Dalio | Bridgewater Associates | Q1 2026 |
| Paul Tudor Jones | Tudor Investment Corp | Q1 2026 |
| Israel Englander | Millennium Management | Q1 2026 |
| Ken Griffin | Citadel Advisors | Q4 2025 |

---

### Πηγές Δεδομένων

- [SEC EDGAR 13F Filings](https://www.sec.gov/cgi-bin/browse-edgar)
- [WisdomWale](https://whalewisdom.com) — πλήρεις θέσεις μεγάλων funds
- [Capitol Trades](https://www.capitoltrades.com) — Congress trades
- [Quiver Quant](https://www.quiverquant.com/congresstrading/) — Congress trading live
- [Senate Stock Watcher](https://senatestockwatcher.com) — Γερουσία
- [Open Insider](https://openinsider.com) — Form 4 insider trades
- [Unusual Whales](https://unusualwhales.com/politics) — Politics & options

---

---

## English

A tool for tracking moves by the world's largest hedge fund managers, based on public **SEC 13F** filings and **Congress trade** disclosures.

### Usage

Open `smart-money-tracker.html` in any browser. No installation or server required.

---

### Tabs

#### 📊 Hedge Funds (13F)
- Click an **investor card** to view their holdings.
- Click any **column header** to sort ascending/descending.
- Use the **search box** to filter by company name.
- Position types: `SH` = shares (long) · `Call` = bullish option · `Put` = bearish option · `PRN` = bond/note.
- 13F filings are **quarterly** — they show positions at quarter-end with a 45-day delay.
- For large funds (Bridgewater, Citadel, Millennium, Tudor) a link to SEC EDGAR and WisdomWale is provided.

#### 🏛 Congress Trades
- Links to live platforms tracking trades by Representatives and Senators.
- Politicians are required to disclose trades within **45 days** (STOCK Act).
- The table below shows sample known trades — for full live data use the links above.

#### 🔔 Real-Time Insider
- Latest **Form 4** transactions from [Dataroma](https://dataroma.com/m/rt.php) — SEC filings submitted by major investors within 2 business days.
- Summary of buys/sells at the top + full table with date, fund, security, action, shares, price, and value.
- `Buy` = bullish · `Sell` = bearish.

#### 🎯 Smart Money Score
- Combines 13F + Form 4 + Congress trades into a single conviction score (0–100) per stock.
- Only shows stocks held by 2+ investors.
- Formula: Investor count 35% · 13F value 35% · Insider RT ±15% · Congress ±10% · Concentration 5% · Put penalty −5.
- Badges: 🔥 ≥60 · ✅ 40–59 · ⚠️ 20–39 · 🔵 <20.
- Filters: All / With signal / Congress only.

#### 📈 Common Holdings
- Stocks held by **2 or more** investors simultaneously.
- **Q1 2026 price** = closing price on 31/3/2026, derived from 13F: `(Value $000 × 1000) ÷ Shares`.
- **Today's price** = refreshed via the 🔄 button from Yahoo Finance.
- The color bar shows move magnitude: 🟢 up / 🔴 down.
- `PUT⚠️` = the investor holds a bearish position (profits if the stock falls).

---

### Buttons

| Button | Function |
|--------|----------|
| `🌙` / `☀️` | Toggle dark / light mode. Preference is saved automatically. |
| `EN` / `ΕΛ` | Switch language. Changes the entire interface. Saved automatically. |
| `❓ Guide` | Opens the help window (close with `Esc` or click outside). |
| `🔄 Refresh prices` | Connects to Yahoo Finance for current prices in the Common Holdings tab. |

---

### Investors

| Investor | Fund | Period |
|----------|------|--------|
| Michael Burry | Scion Asset Management | Q3 2025 |
| Bill Ackman | Pershing Square | Q1 2026 |
| Stan Druckenmiller | Duquesne Family Office | Q1 2026 |
| David Tepper | Appaloosa LP | Q1 2026 |
| Warren Buffett | Berkshire Hathaway | Q1 2026 |
| George Soros | Soros Fund Management | Q1 2026 |
| Carl Icahn | Icahn Capital | N/A (stopped 2011) |
| Ray Dalio | Bridgewater Associates | Q1 2026 |
| Paul Tudor Jones | Tudor Investment Corp | Q1 2026 |
| Israel Englander | Millennium Management | Q1 2026 |
| Ken Griffin | Citadel Advisors | Q4 2025 |

---

### Data Sources

- [SEC EDGAR 13F Filings](https://www.sec.gov/cgi-bin/browse-edgar)
- [WisdomWale](https://whalewisdom.com) — full holdings for large funds
- [Capitol Trades](https://www.capitoltrades.com) — Congress trades
- [Quiver Quant](https://www.quiverquant.com/congresstrading/) — live Congress trading
- [Senate Stock Watcher](https://senatestockwatcher.com) — Senate only
- [Open Insider](https://openinsider.com) — Form 4 insider trades
- [Unusual Whales](https://unusualwhales.com/politics) — Politics & options
