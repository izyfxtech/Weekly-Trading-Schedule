# IZY Weekly Schedule — PWA (Progressive Web App)

## 📱 How to Install on Android

### Method 1: Via Chrome (Recommended)
1. Open Chrome on your Android phone
2. Navigate to where you're hosting the app (or open `index.html` via a local server)
3. Chrome will show an **"Add to Home screen"** banner automatically
4. Tap **"Install"** or **"Add"**
5. IZY now appears on your home screen like a native app ✅

### Method 2: Manual Install
1. Open the site in Chrome
2. Tap the **⋮ menu** (top right)
3. Tap **"Add to Home screen"**
4. Confirm the install

---

## 🚀 How to Serve Locally (for testing)

You need a local HTTPS or localhost server (service workers require it).

### Option A: Python (quickest)
```bash
cd izy-pwa
python3 -m http.server 8080
```
Then open `http://localhost:8080` in Chrome on your PC, or use your local IP on your phone.

### Option B: VS Code Live Server
Install the "Live Server" extension in VS Code, right-click `index.html` → "Open with Live Server".

### Option C: Deploy Free (share with anyone)
Upload the entire `izy-pwa/` folder to:
- **Netlify Drop**: drag-and-drop at https://app.netlify.com/drop
- **Vercel**: `vercel --prod`
- **GitHub Pages**: push to a repo and enable Pages

---

## ✨ PWA Features Added
- **Offline support** — works without internet after first load
- **Installable** — appears on home screen like a native app
- **Fullscreen mode** — no browser chrome/address bar
- **Custom icon** — IZY amber icon on your home screen
- **Theme color** — espresso dark status bar
- **Font caching** — Google Fonts cached for offline use
- **Push notification ready** — service worker supports future reminders

## 📁 File Structure
```
izy-pwa/
├── index.html      ← Your app (modified with PWA support)
├── manifest.json   ← App metadata, icons, display settings
├── sw.js           ← Service worker (offline + caching)
└── icons/
    ├── icon-192.png
    └── icon-512.png
```

All your data is still saved to `localStorage` — works exactly as before.
