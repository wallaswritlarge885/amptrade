# AmpTrade 
Amptrade allows users to connect, trade, replicate/copy trades to multiple brokers simultaneously. 

### Notes
This is a monorepo containing the following services:
- amptrade-web: The website frontend
| Development | `localhost:5178` |
- amptrade-api: The backend API
| Development | `localhost:3089` |
- amptrade-websocket: The websocket service for real-time data
| Development | `localhost:8789 to localhost:8795` |

### Getting Started (Windows – Non‑Technical)

Use these steps to install and run AmpTrade locally on a Windows PC.

#### Pre‑requisites
- Windows 10 or 11
- Internet connection for downloads
- Node.js (LTS) and npm:
  - Download and install from https://nodejs.org
- Python 3.10+:
  - Download and install from https://www.python.org
  - Check “Add Python to PATH” during installation
- A web browser
  - The start script opens Firefox automatically. If you use another browser, open the app manually at the link below.

#### Get the Files
- Ensure the folder exists at `G:\GitHub\amptrade` (if you already have this, skip).
- If you don’t use Git: download the repository as a ZIP and extract to `G:\GitHub\amptrade`.

#### Install Dependencies (One‑Click Recommended)
- Double‑click [install-all.bat](file:///g:/GitHub/amptrade/install-all.bat)
- Wait for “INSTALLATION COMPLETE”
- This sets up:
  - amptrade-web (website)
  - amptrade-api (backend)
  - amptrade-websocket (live data)

#### Manual Install (Fallback)
If the one‑click installer fails, install dependencies manually with these commands:

For the website:

```bat
cd /d g:\GitHub\amptrade\amptrade-web
npm install
```

For the API:

```bat
cd /d g:\GitHub\amptrade\amptrade-api
npm install
```

For the WebSocket service:

```bat
cd /d g:\GitHub\amptrade\amptrade-websocket
python -m pip install --upgrade pip
pip install -r requirements.txt
```

#### Start AmpTrade (Easy Way)
- Double‑click `g:\GitHub\amptrade\start-amptrade-dev-servers.bat`
- In the menu, type `1` and press Enter to “Start All Servers”
- What opens:
  - API tab: `http://localhost:3089`
  - App tab: `http://localhost:5178`
- If Windows Firewall prompts for Node.js or Python, click Allow
- If Firefox doesn’t open, open your preferred browser and go to `http://localhost:5178`

#### Stop AmpTrade
- Return to the small menu window and press any key when prompted
- This closes the servers and frees the ports
- Note: it stops all Node.js and Python processes currently running; save other work first

#### Open This Readme
- Double‑click `g:\GitHub\amptrade\readme.md`
- If it doesn’t open nicely, right‑click → “Open with” → “Visual Studio Code” or “Notepad”

#### Troubleshooting
- “node is not recognized” or “python is not recognized”:
  - Reinstall Node/Python, ensure PATH is set, then restart your PC
- App page doesn’t load:
  - Wait up to a minute on first run and refresh `http://localhost:5178`
- Port already in use:
  - Close other apps using those ports and run the start script again
- Firewall prompts:
  - Allow access for Node.js and Python when asked

### Screenshots

- AmpTrade Desktop Preview

![AmpTrade Desktop Preview](amptrade-web/src/assets/amptrade_preview_desktop.png)

- Manage Brokers

![Manage Brokers](amptrade-web/src/assets/manage_brokers.png)

- Quick SL/Target Controls

![SL and Target](amptrade-web/src/assets/trading_sl_target.png)

- Risk Management

![Risk Management](amptrade-web/src/assets/trading_risk_management.png)

- Scroll-To-Trade

![Scroll To Trade](amptrade-web/src/assets/trading_mouse_scroll.png)
