# 🔴 RCB Dream XI Builder
> **Ee Sala Cup Namde** — Build your Ultimate Royal Challengers Bengaluru Dream Team

A luxury-designed, fully interactive fan experience for Royal Challengers Bengaluru supporters to craft their perfect 11-player squad from the current RCB roster.

---

## ✨ Features

### Fan Experience (`index.html`)
- **Page 1 — Fan Identity**: Enter your name and drag a slider to show how many years you've been an RCB fan
- **Page 2 — Dream XI Builder**:
  - 11 distinct player slots: **2 Openers · 1 Wicket Keeper · 2 Batsmen · 2 All-Rounders · 3 Prime Bowlers · 1 Impact Player**
  - Real RCB 2025 squad player cards with official IPL photos
  - **Top 3 career highlights** displayed on each player card
  - Live field diagram showing your lineup as you build
  - Tap any filled slot or bottom chip to assign captain
  - Players greyed out if already selected in another slot
  - Category accordions auto-collapse when that slot is filled
- **Page 3 — Your Dream XI**: Beautiful result card with full lineup display
- **Share Link**: Encoded URL (`#team=...`) lets you share your exact team with anyone — they open the link and see your team instantly

### Admin Dashboard (`admin.html`)
- Total submissions counter + today's count
- Average fan years + most popular captain stat
- Full sortable submissions table with fan name, team name, captain, and timestamp
- **Click "VIEW TEAM"** to see any fan's full 11-player lineup in a modal
- **Player Popularity Chart** — bar chart showing which players fans pick most
- **Export CSV** — download all submissions as a spreadsheet
- **Clear All** — wipe all data (with confirmation)

---

## 🎨 Design

| Element | Choice |
|---|---|
| Primary Font | Cinzel Decorative (headings) + Cinzel (labels) |
| Body Font | Rajdhani (UI) + Cormorant Garamond (accents) |
| Theme | Deep black · Luxury gold · Deep crimson red |
| Background | RCB Lion logo watermark · Red radial gradients · Noise texture |
| Animations | Fade-up on page transitions · Shimmer on CTA buttons · Hover lifts |

---

## 🚀 Deployment

### GitHub Pages (Recommended)

1. **Upload files** to a new GitHub repository
2. Go to **Settings → Pages**
3. Set source to `main` branch, `/ (root)` folder
4. Your site will be live at `https://yourusername.github.io/rcb-dream-xi/`

### Local Preview

Just open `index.html` in any modern browser. No build step, no dependencies.

```bash
# Or serve locally:
npx serve .
# or
python3 -m http.server 8080
```

---

## 📁 File Structure

```
rcb-dream-xi/
├── index.html      # Main fan-facing Dream XI builder
├── admin.html      # Admin dashboard (no password — add one if deploying publicly)
└── README.md       # This file
```

---

## 🔐 Admin Security Note

The admin page (`admin.html`) uses **localStorage** to read submission data. It's client-side only — all data lives in the browser of the user who submitted. For a shared server-side database, integrate with Firebase, Supabase, or a simple backend API.

To add basic protection, you can add a simple password prompt at the top of `admin.html`:

```javascript
if (prompt("Admin password:") !== "YOUR_PASSWORD") {
  window.location.href = "index.html";
}
```

---

## 🏏 RCB Squad 2025

| # | Player | Role |
|---|---|---|
| 1 | Virat Kohli | Opener · Right-hand |
| 2 | Phil Salt | Opener / WK · Right-hand |
| 3 | Rajat Patidar | Opener · Right-hand (Captain) |
| 4 | Jacob Bethell | Opener / AR · Left-hand |
| 5 | Dinesh Karthik | Wicket Keeper · Right-hand |
| 6 | Devdutt Padikkal | Batsman · Left-hand |
| 7 | Manoj Bhandage | Batsman · Right-hand |
| 8 | Liam Livingstone | Batsman / AR · Right-hand |
| 9 | Tim David | Batsman · Right-hand |
| 10 | Glenn Maxwell | All-rounder · Right-hand |
| 11 | Krunal Pandya | All-rounder · Left-hand |
| 12 | Swapnil Singh | All-rounder · Left-hand |
| 13 | Josh Hazlewood | Prime Bowler · Right-arm Fast |
| 14 | Mohammed Siraj | Prime Bowler · Right-arm Fast |
| 15 | Yash Dayal | Prime Bowler · Left-arm Fast |
| 16 | Suyash Sharma | Prime Bowler · Right-arm Leg-spin |
| 17 | Bhuvneshwar Kumar | Prime Bowler · Right-arm Medium |
| 18 | Rasikh Dar | Prime Bowler · Right-arm Fast |
| 19 | Lungi Ngidi | Prime Bowler · Right-arm Fast |

---

## 📜 License

Fan project — not officially affiliated with Royal Challengers Bengaluru or BCCI/IPL.

---

**Ee Sala Cup Namde** 🔴🏆
