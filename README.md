# Waymark Consulting — Launch Playbook

An interactive 5-phase launch guide for Waymark Consulting, built with Vite + React.

## Project Structure

```
waymark-launch-playbook/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── GoldBar.jsx        # Animated progress bar
│   │   ├── StepCard.jsx       # Individual step card with checkbox
│   │   ├── TopBar.jsx         # Sticky header with phase nav
│   │   └── WaymarkLogo.jsx    # SVG logo component
│   ├── constants/
│   │   └── theme.js           # Color tokens (G palette)
│   ├── data/
│   │   └── phases.js          # All 5 phases + 26 steps content
│   ├── views/
│   │   ├── GuideView.jsx      # Step-by-step guide view
│   │   └── OverviewView.jsx   # All-phases overview
│   ├── App.jsx                # Root component + state
│   ├── index.css              # Global styles + button classes
│   └── main.jsx               # React entry point
├── index.html
├── package.json
├── vite.config.js
├── vercel.json
└── .gitignore
```

## Local Development

```bash
npm install
npm run dev
```

App will run at http://localhost:5173

## Build for Production

```bash
npm run build
```

Output goes to `/dist`.

## Deploy to Vercel

### Option A — Vercel CLI
```bash
npm install -g vercel
vercel
```
Follow the prompts. Vercel auto-detects Vite.

### Option B — GitHub + Vercel Dashboard
1. Push this repo to GitHub
2. Go to https://vercel.com/new
3. Import your repository
4. Vercel auto-detects settings:
   - Framework: Vite
   - Build Command: `npm run build`
   - Output Directory: `dist`
5. Click **Deploy**

The `vercel.json` handles SPA routing so page refreshes work correctly.

## Customization

- **Content**: Edit `src/data/phases.js` to update steps, tools, costs, or add new phases
- **Colors**: Edit `src/constants/theme.js` to adjust the brand palette
- **Styles**: Global button/chip classes are in `src/index.css`
