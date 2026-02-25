# 🌊 WaveKeeper

A Dalamud plugin for Final Fantasy XIV that automatically greets nearby players with emotes and replies when someone emotes at you.

<img width="360" height="2173" alt="image" src="https://github.com/user-attachments/assets/b36154f7-d939-4142-a2ae-8dae76120ed6" />


---

## ✨ Features

### Core Greeting
- **Auto-Greet** — Automatically sends an emote to nearby players when they enter range
- **Auto-Reply** — Detects when someone emotes at you and replies back
- **Mimic Mode** — Reply with the same emote someone used on you
- **Goodbye Emote** — Send a farewell emote when a friend leaves range
- **Emote Chain** — Execute multiple emotes in sequence with custom delays
- **Emote Randomizer** — Pick from a custom list of emotes randomly
- **Returning Greet** — Different emote for first encounter of the day vs. returning later

### Who to Greet
- **Friends Only Mode** — Limit greetings to your friends list
- **FC Members** — Optionally greet Free Company members
- **Party Members** — Optionally greet party members
- **Whitelist Mode** — Only greet a specific list of named players
- **Per-Player Emotes** — Assign specific emotes to specific friends
- **Sprout Greeting** — Special emote for new adventurers (sprouts)
- **Returner Greeting** — Special welcome-back emote for returners

### Smart Filters
- **AFK Filter** — Pause greets/replies when you're AFK, or ignore AFK players
- **Activity Filters** — Pause while mounted, crafting, gathering, or in combat
- **Cutscene/Loading Filter** — Pause during cutscenes and loading screens
- **Duty/Instance Filter** — Automatically disable in duties and instances
- **Zone Whitelist/Blacklist** — Enable or disable in specific zones
- **Level Range Filter** — Only greet players within a specific level range
- **Zone Warmup** — Delay greetings for X seconds after loading into a new zone
- **Re-Greet Cooldown** — Don't re-greet someone for X minutes if they leave/return

### Stats & Tracking
- **Daily Greet Counter** — Track how many players were greeted today
- **Most Greeted Friend** — Track the player you encounter most often
- **Session Stats** — View greets, replies, and goodbyes for current session
- **Greet History Window** — Scrollable log with timestamps of all interactions
- **Export to CSV** — Save history data to CSV files

### UI & Quality of Life
- **Compact Mode** — Small floating overlay showing status and counts
- **Profiles/Presets** — Save and switch between different settings profiles
- **DTR Bar Toggle** — Clickable icon on the server info bar for quick enable/disable
- **Custom Chat Prefix** — Change `[WaveKeeper]` to a custom string
- **Chat Color** — Set a custom color for chat notifications
- **Chat Toggle** — Option to completely hide all WaveKeeper messages

### Scheduling
- **Time-Based Activation** — Only active during specific hours of the day
- **Auto-Disable Timer** — Turn off automatically after X minutes of activity

---

## 📥 Installation

1. Open FFXIV and type `/xlsettings` in chat
2. Go to the **Experimental** tab
3. Scroll down to **Custom Plugin Repositories**
4. Copy the repo URL below and paste it into the empty box
5. Click the **+** button, then **Save and Close**
6. Open the Plugin Installer with `/xlplugins`
7. Search for **WaveKeeper** and click **Install**

**Repository URL:**
```
https://raw.githubusercontent.com/sm0kez/MyDalamudPlugins/main/pluginmaster.json
```

Type `/wavekeeper` to open the settings window.

---

## 🔧 How It Works

1. **Scanning** — WaveKeeper periodically scans for nearby players within your configured range
2. **Filtering** — Players are filtered based on your settings (friends, FC, party, whitelist, AFK status, level, etc.)
3. **Greeting** — When a valid player is detected, it queues a greeting with your configured delay
4. **Reply Detection** — Uses a game emote hook to detect when someone emotes directly at you
5. **Auto-Reply / Mimic** — If someone emotes at you, it automatically replies (or mimics their emote)
6. **Goodbye** — When a greeted player leaves range, optionally sends a goodbye emote
7. **Cleanup** — Players are removed from the greeted list when they leave the area

---

## 💬 Commands

| Command | Description |
|---------|-------------|
| `/wavekeeper` | Open settings window |
| `/wavekeeper stats` | Open stats window |
| `/wavekeeper compact` | Toggle compact overlay |

---

## 📊 Stats Window

Click the **Stats** button in the main window or use `/wavekeeper stats` to view:

- Session greets, replies, and goodbyes
- Total and daily greet counts
- Most greeted players
- Full history log with timestamps
- Export to CSV

---

## 🎯 Quick Toggle (DTR Bar)

WaveKeeper adds a clickable entry to the server info bar (DTR):

- **WK ●** = Active (click to disable)
- **WK ○** = Inactive (click to enable)

---

## 🙏 Credits

**Made by sm0var**

Thanks to Kingo, Iridescent, Sora, Brit, Willow & Wyno 💜

---

## 📜 License

This project is licensed under the [MIT License](https://github.com/sm0kez/WaveKeeper/blob/main/LICENSE).
