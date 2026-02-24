# 🌊 WaveKeeper

A Dalamud plugin for Final Fantasy XIV that automatically greets nearby players with emotes and replies when someone emotes at you.

![Preview](https://raw.githubusercontent.com/sm0kez/WaveKeeper/main/images/preview1.png)

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

## Credits

**Made by sm0var**

Thanks to Kingo, Iridescent, Sora, Brit, Willow & Wyno 💜

## License

This project is licensed under the [MIT License](LICENSE).
