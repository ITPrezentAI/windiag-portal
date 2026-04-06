# WinDiag Portal

Windows Log Analyzer — web portal for IT support teams.

## What it does
- Displays the PowerShell script to collect Windows logs (last 7 days)
- Accepts CSV upload from the script output
- Analyzes logs and shows a dashboard with issues + fix checklist

## Deploy to Railway (new service in same project)

### Option A — Deploy from GitHub
1. Push this folder to a GitHub repo (or subfolder)
2. In Railway → your existing project → click **+ New Service**
3. Choose **GitHub Repo** → select this repo
4. Set **Root Directory** to the folder if it's a subfolder
5. Railway auto-detects Node.js and runs `npm start`
6. Go to **Settings → Networking → Generate Domain** for the public URL

### Option B — Railway CLI
```bash
npm install -g @railway/cli
railway login
railway link          # link to your existing project
railway up            # deploy as new service
railway domain        # get your URL
```

## Local development
```bash
npm install
npm start
# open http://localhost:3000
```

## File structure
```
windiag-portal/
├── public/
│   └── index.html      ← full single-page app
├── server.js           ← Express static server
├── package.json
├── railway.toml        ← Railway config
└── .gitignore
```
