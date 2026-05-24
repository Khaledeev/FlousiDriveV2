# 🚗 Flousi Drive — كيفاش تربح بزاف

> The financial toolkit for Moroccan ride-hailing drivers. Stop losing money to hidden costs.

Flousi Drive is a mobile-first web app built for drivers working across **inDrive, Careem, Uber, Yango, and Heetch** in Morocco. It makes every dirham visible — platform commissions, fuel costs, dead miles — so drivers know their real net profit, not just the gross fare.

---

## ✨ MVP Features

### 🟢 Shift Tracker
Start and end your shift with one tap. The app tracks elapsed time, kilometers driven, and calculates fuel cost automatically based on your vehicle profile. No typing while driving.

### 💰 Trip Logger
Log a completed ride in under 5 seconds — fare amount via numpad, platform selector, cash or card. No keyboard. Net profit calculated instantly after deducting commission and fuel cost.

### 🧮 inDrive Négociateur
Enter the trip distance and get a **minimum acceptable price** and a **suggested counter-offer** — calculated from real fuel cost + your minimum profit margin + platform commission. Includes a *Retour à vide* toggle for airport and long-distance trips that doubles the fuel calculation for the empty return leg.

### ⚠️ inDrive Debt Tracker
inDrive deducts its ~10% commission from a prepaid wallet. This tracker keeps a running total of what you owe and alerts you in yellow / orange / red before you get blocked from new ride requests.

### 📊 Stats Dashboard
Total net profit, trip count, average fare, and a breakdown by platform — across all your logged history.

### ⚙️ Settings
Switch vehicle, update fuel price, set your daily net profit target, and adjust the commission rate per platform.

---

## 📱 Design Principles

- **Mobile-first, RTL-first** — built for Moroccan drivers on mid-range Android phones
- **Darija UI** — labels and messages in Moroccan Arabic (Arabic script, RTL layout)
- **No keyboard during entry** — all fare/km inputs use a custom numpad
- **Offline-ready** — all data stored in `localStorage`, no internet required
- **Single HTML file** — zero build step, zero dependencies to install

---

## 🗂 Tech Stack

| Layer | Technology |
|---|---|
| UI | HTML5 + Tailwind CSS (CDN) |
| Fonts | Cairo (Arabic) + IBM Plex Mono |
| Logic | Vanilla JavaScript (ES6+) |
| Storage | localStorage |
| Icons | Inline SVG |

No framework. No bundler. No backend. Open the file and it works.

---

## 🚀 Getting Started

```bash
git clone https://github.com/your-username/flousi-drive.git
cd flousi-drive
open flousi-drive.html   # or just drag it into your browser
```

That's it. No `npm install`. No server needed.

---

## 🗺 Roadmap

This is the MVP. The full product blueprint covers:

- [ ] Screenshot OCR auto-logging (AI extracts fare from inDrive/Careem screenshots)
- [ ] Waqt Lmezyan — crowdsourced demand heatmap by zone and time
- [ ] Klyani CRM — private client list with 1-tap WhatsApp templates (0% commission rides)
- [ ] Lflouss — financial calendar for vignette, insurance, Eid expenses
- [ ] Lkarnet — maintenance logbook with service interval alerts
- [ ] Drive Mode — horizontal dashboard optimized for glances at speed
- [ ] Ghost Taximeter — crowdsourced fair price bands per route
- [ ] Lhala Dyali — driver wellness & fatigue prompts
- [ ] B'Ssif — emergency income mode
- [ ] Multi-city support: Casablanca, Rabat, Marrakech, Agadir

---

## 💡 Vehicle Profiles Included

Pre-loaded consumption data for the most common cars on Moroccan roads:

- Dacia Logan 1.5 dCi · Sandero 1.5 dCi · Dokker 1.5 dCi
- Renault Symbol 1.5 dCi · Renault Master
- Hyundai i10 1.0
- Opel Astra J 1.6
- Volkswagen Polo 1.4
- Peugeot 208 1.4 HDi
- Custom entry for any unlisted vehicle

---

## 🧮 How Net Profit Is Calculated

```
Gross Fare
  − Platform Commission (%)
  − Fuel Cost (km × consumption rate × fuel price per liter)
─────────────────────────────
= Net Profit
```

The Négociateur adds a minimum profit margin on top and works backwards from there.

---

## 🔒 Privacy

All data lives on your device. Nothing is sent anywhere. No account required for the MVP. localStorage can be cleared from Settings at any time.

---

## 📄 License

MIT — free to use, modify, and distribute.

---

*Flousi Drive · Built for Moroccan Drivers · كيفاش تربح بزاف*
