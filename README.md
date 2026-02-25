# 🌊 WaveKeeper

A Dalamud plugin for Final Fantasy XIV that automatically greets nearby players with emotes and replies when someone emotes at you.

<img width="360" height="2173" alt="image" src="https://github.com/user-attachments/assets/ae9545dd-96aa-49e6-bc11-e82b0ad18f9f" />



## Features

- **Auto-Greet** — Automatically sends an emote to nearby players when they enter range
- **Auto-Reply** — Detects when someone emotes at you and replies back
- **Friends Only Mode** — Limit greetings to your friends list
- **Ignore List** — Block specific players from being greeted
- **Target Before Greeting** — Optionally targets the player before emoting
- **Customizable Emotes** — Choose any emote for greetings and replies
- **Adjustable Timing** — Configure scan intervals, greet delays, and reply delays
- **Adjustable Range** — Set how close a player needs to be before greeting

## Installation

1. Open FFXIV and type `/xlsettings` in chat
2. Go to the **Experimental** tab
3. Scroll down to **Custom Plugin Repositories**
4. Copy the repo URL below and paste it into the empty box
5. Click the **+** button, then **Save and Close**
6. Open the Plugin Installer with `/xlplugins`
7. Search for **WaveKeeper** and click **Install**

**Repository URL:**

```text
https://raw.githubusercontent.com/sm0kez/MyDalamudPlugins/main/pluginmaster.json
```
Type `/wavekeeper` to open the settings window.

### Settings Overview

| Setting | Description | Default |
|---|---|---|
| Enabled | Toggle auto-greeting on/off | On |
| Emote Command | Emote used for greeting | `/wave` |
| Friends Only | Only greet players on your friends list | Off |
| Target Before Greeting | Target the player before emoting | On |
| Greet Delay | Seconds to wait before greeting | 3s |
| Scan Interval | How often to scan for new players | 3s |
| Greet Range | Distance (yalms) to detect players | 15 |
| Enable Auto-Reply | Reply when someone emotes at you | On |
| Reply Emote | Emote used for replies | `/wave` |
| Reply Delay | Seconds to wait before replying | 2s |

### Actions

- **Clear Greeted List** — Resets the memory of who you've already greeted, so everyone nearby will be greeted again

## How It Works

1. **Scanning** — WaveKeeper periodically scans for nearby players within your configured range
2. **Greeting** — When a new player is detected, it queues a greeting with your configured delay
3. **Reply Detection** — Uses a game emote hook to detect when someone emotes directly at you
4. **Auto-Reply** — If someone emotes at you and you haven't replied yet, it automatically replies with your configured emote
5. **Cleanup** — Players are removed from the greeted list when they leave the area

## Chat Notifications

WaveKeeper sends echo messages (only visible to you) when it:
- Detects a player and queues a greeting
- Sends a greeting
- Detects an incoming emote and queues a reply
- Sends a reply

🗺️ Roadmap & Future Ideas
✅ Confirmed for v1.1

    Default State: Disabled on first run
    New Defaults: (Emote: /dote, Scan: 8s, Range: 5y, Friends Only: True, Reply: /pet disabled)
    AFK Filter: Pause greets when player is AFK
    AFK Filter: Pause auto-reply when player is AFK
    AFK Filter: Ignore players who are currently AFK

🎭 Emote & Behavior

    Cooldown per player: Don't re-greet someone for X minutes if they leave/return
    Emote randomizer: Pick from a custom list of emotes randomly
    Reply mirror mode: Automatically reply with the exact same emote used on you
    Returning greet: Different emote for first encounter of the day vs. returning later
    Emote chain: Execute multiple emotes in sequence with custom delays
    Emote queue system: Stagger greetings when multiple friends arrive simultaneously
    Goodbye emote: Send a farewell emote when a friend leaves range

🛡️ Filters & Smart Behavior

    In-combat filter: Automatically pause greetings while in combat
    Cutscene/loading filter: Pause during cutscenes and loading screens
    Mounted filter: Skip greeting while mounted
    Crafting/gathering filter: Don't interrupt active crafting or gathering
    Duty/instance filter: Automatically disable in duties and PvP
    Zone Blacklist: Disable functionality in specific user-defined zones
    Zone Whitelist: Only active functionality in specific zones
    Level range filter: Only greet players within a specific level range
    Warmup delay: Delay greetings for X seconds after loading into a new zone

📊 Tracking & Stats

    Daily greet counter: Track how many players were greeted today
    Most greeted friend: Track the player you encounter most often
    Session stats: View greets, replies, and ignored players for current session
    Greet history window: Scrollable log with timestamps of all interactions
    Export stats: Save history data to text or CSV files

🎨 UI & Quality of Life

    Compact mode: Small floating overlay showing status and greeting counts
    Profiles/presets: Save and switch between different settings profiles
    Quick toggle (DTR bar): Clickable icon on the server info/DTR bar
    Custom chat prefix: Change [WaveKeeper] to a custom string
    Chat color options: Select custom colors for echo messages
    Chat notification toggle: Option to completely hide [WaveKeeper] messages

🤝 Social & Group

    FC members mode: Specific toggle to greet Free Company members
    Party member mode: Specific toggle to greet party members
    Linkshell/CWLS mode: Greet members of your Linkshells
    Whitelist mode: Only greet a specific list of named players
    Per-player emote override: Assign specific emotes to specific friends
    Newcomer greeting: Special emote for players with the "New Adventurer" (Sprout) icon
    Returner greeting: Special welcome-back emote for players with the "Returner" icon
    Name color coding: Different colors for Friends, FC, and Party members in logs

⏰ Scheduling

    Time-based activation: Only active during specific hours of the day
    Auto-disable timer: Turn off functionality after X minutes of activity
    Sound notification: Play a UI sound when someone emotes at you

## Credits

**Made by sm0var**

Thanks to Kingo, Iridescent, Sora, Brit, Willow & Wyno 💜

## License

This project is licensed under the [MIT License](LICENSE).
