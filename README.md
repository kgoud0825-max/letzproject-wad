# SipStreak: HydroHero Hunt

A responsive college mini-project that turns daily hydration into a friendly team challenge.

## Project features

- Personal hydration dashboard and daily target calculator (body weight × 35 ml).
- One-tap water logging (+250 ml, +500 ml, +750 ml) and custom amounts.
- Squad creation, invite-code joining, member progress and team leaderboard.
- Team score based on average member goal completion, capped at 100% per member.
- Seven-day hydration chart, recent log and streak display.
- Virtual plant that grows as daily hydration increases.
- Optional 200 ml caffeine hydration buffer (a simplified demo feature).
- Printable bottle QR sticker with a preselected quick-log amount.
- Responsive layout for desktop, tablet and mobile.
- Browser `localStorage` persistence.

## Technology used

- HTML5
- CSS3 (responsive grid/flex layouts, transitions and animations)
- Modern JavaScript (ES6+, DOM, Canvas API, localStorage)
- QRCode.js CDN for QR generation
- Google Fonts for typography

## Run in Visual Studio Code

### Option 1 — easiest
1. Download and extract `SipStreak_HydroHero_Hunt.zip`.
2. Open Visual Studio Code.
3. Select **File → Open Folder**.
4. Choose the extracted `SipStreak_HydroHero_Hunt` folder.
5. Open `index.html`.
6. Right-click inside the editor and choose **Open with Live Server** (recommended).

If Live Server is not installed:
1. Open the Extensions panel in VS Code (`Ctrl + Shift + X`).
2. Search for **Live Server** by Ritwick Dey.
3. Install it.
4. Right-click `index.html` → **Open with Live Server**.

You can also double-click `index.html` to open it in a browser. Live Server is recommended for the QR sticker and URL query-string demo.

### Option 2 — run a local server from the VS Code terminal
Open **Terminal → New Terminal** in the project folder and run:

```bash
python -m http.server 5500
```

Then open `http://localhost:5500` in your browser.

## Demo walkthrough

1. Open Overview. The demo begins with Aarav Kumar in the Hydration Homies squad.
2. Click **+250 ml**, **+500 ml**, or **+750 ml**. The dashboard, member contribution and leaderboard update immediately.
3. Click **Edit my goal** to change the demo user's name and body weight. The target is recalculated using weight × 35 ml.
4. Open **My squad** to view members, copy the invite code, create a squad or join a demo squad.
5. Open **Leaderboard** to see teams ranked by average capped member completion.
6. Open **Hydration history** to view the seven-day chart and today's log.
7. Open **Virtual plant** to see the plant respond to your daily goal progress.
8. Open **Bottle QR sticker**, choose an amount, generate the QR, and print it. Scan it with a phone camera while the local site is accessible from that phone. A phone cannot normally open `localhost` on your laptop; use your laptop's LAN IP and allow the development server through the firewall if scanning from another device.

## Important project notes

- This is a front-end mini-project. Data is stored in the current browser using `localStorage`; it is not synchronized between different devices or users.
- The squads and members are sample/demo data. Joining accepts the demo invite identifiers shown by the app; this is not a real multi-user service.
- The QR library is loaded from a CDN, so QR generation needs an internet connection.
- The reminder toggle records a preference and shows an in-app check-in when the page is open. Browser notifications depend on browser permission and are not a guaranteed background reminder.
- The hydration formula is included to satisfy the project brief and is not medical advice. Real hydration needs vary by person and circumstances.
- History values are sample data for the mini-project demonstration. Today's log is saved locally.

## Folder structure

```text
SipStreak_HydroHero_Hunt/
├── index.html       # All page sections and UI structure
├── styles.css       # Theme, responsive design and animations
├── app.js           # App logic, demo data and local storage
├── README.md        # Setup and demo instructions
└── assets/
    └── (reserved for additional images/icons)
```

## Reset demo data

Open browser Developer Tools → Console and run:

```javascript
localStorage.removeItem("sipstreak-hydrohero-v1");
location.reload();
```
