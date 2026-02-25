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

## ❓ Frequently Asked Questions

---

**Q1: Why doesn't it greet everyone around me, only my friends?**
> The default mode is **Friends Only**. Open `/wavekeeper` → **General → Who to Greet** and switch the mode to **Everyone**. You can also choose **Whitelist Only** if you want to control exactly who gets greeted.

---

**Q2: How do I spam emotes on someone like Copycat does?**
> Enable **Reply & Mimic → Mimic Mode**, then set the **Mimic Cooldown to 0 seconds**. Every emote someone directs at you will be mirrored back instantly with no cooldown, just like Copycat.

---

**Q3: Someone waved at me but WaveKeeper didn't reply. Why?**
> Auto-Reply is **off by default**. Go to **Reply & Mimic → Auto-Reply** and enable it. Also check your greet mode — if you're on **Friends Only**, WaveKeeper will only reply to people on your friends list.

---

**Q4: It greeted someone once but never again even though they're still nearby. Why?**
> WaveKeeper keeps a greeted list per session and won't greet the same person twice. Click **Clear Greeted** at the top of the settings window to reset it, or simply change zones — the list clears automatically.

---

**Q5: How do I make it wait a few seconds before greeting someone?**
> Go to **General → Timing → Greet Delay** and set it to however many seconds you want. A value of 3–5 seconds feels natural and avoids greeting someone who's just passing through.

---

**Q6: How do I assign a specific emote to a specific friend?**
> Go to **Player Lists → Per-Player Emotes**, enter the player's exact name and the emote command (e.g. `/dote`), then click **Add**. That player will always receive that emote instead of your default one.

---

**Q7: How do I stop it from greeting people while I'm crafting, mounted, or in combat?**
> Go to **Filters** and tick the relevant checkboxes — **Mounted**, **Crafting**, **Gathering**, and **Combat** are all available. WaveKeeper will automatically pause whenever those states are active.

---

**Q8: How do I make it only work in specific zones like my FC house?**
> Go to **Filters → Zone Whitelist**, enable it, search for your zone by name, and click **+** to add it. WaveKeeper will only greet players while you're inside a whitelisted zone and stay silent everywhere else.

---

**Q9: People keep getting greeted the moment they appear. Can I add a warmup after zoning?**
> Yes — go to **Filters → Zone Warmup** and set a delay in seconds. WaveKeeper will wait that long after you load into a zone before it starts greeting anyone, avoiding spam on zone-in.

---

**Q10: How do I send a goodbye emote when someone walks away?**
> Go to **Goodbye**, enable it, and set your emote command. WaveKeeper will automatically send it when a player you've already greeted moves out of your configured range.

---

**Q11: How do I run multiple emotes in a row after greeting someone?**
> Go to **Emote Chain**, enable it, pick when it fires (**Proactive Only**, **Replies Only**, **All Greets**, or **Goodbye Only**), then add steps with a command, delay, and motion toggle. WaveKeeper fires them in order after the initial emote.

---

**Q12: How do I greet FC members and party members too, not just friends?**
> In **General → Who to Greet**, set the mode to **Everyone** — or keep **Friends Only** and additionally enable **FC Members** and **Party Members** toggles so those groups are included alongside friends.

---

**Q13: How do I use a special emote only for sprouts or returners?**
> Go to **Sprout & Returner**, enable **Greet Sprouts** and/or **Greet Returners**, then set the emote you want to use for each. WaveKeeper will automatically use those instead of your default emote when it detects one nearby.

---

**Q14: How do I quickly enable or disable WaveKeeper without opening the settings?**
> Click the **WK ●** / **WK ○** entry in your server info bar (DTR bar) at the top of the screen. It toggles WaveKeeper on and off instantly. You can also use the **Enable/Disable** button in the Compact overlay (`/wavekeeper compact`).

---

**Q15: How do I make WaveKeeper only run during certain hours, like when I'm usually online?**
> Go to **Time & Auto-Disable → Time-Based Activation**, enable it, and set your **Start Hour** and **End Hour**. WaveKeeper will enable and disable itself automatically based on your local system clock.

---

**Q16: How do I stop someone from being greeted without fully ignoring them?**
> Go to **Player Lists → Ignore List** and add their name. They'll be permanently skipped for all greets, replies, mimic, and goodbyes — without affecting anything else.

---

**Q17: How do I see who I've greeted the most and export my history?**
> Click **Stats** at the top of the settings window or type `/wavekeeper stats`. You'll see session stats, all-time totals, your most greeted players, and a full timestamped history log. Click **Export CSV** to save it to a file.

---

**Q18: I have different playstyles — RP, casual, AFK farming. Can I save separate configs?**
> Yes — go to **Profiles**, give your current setup a name and click **Save New**. Switch between profiles any time from the **Active** dropdown. Each profile stores all settings independently.

---

**Q19: How do I stop WaveKeeper from printing messages in chat every time it greets someone?**
> Go to **Chat & Sound → Chat Toggle** and disable chat notifications entirely. Alternatively, customize the **Chat Prefix** or **Chat Color** to make them less intrusive if you still want to see them.

---

**Q20: WaveKeeper greeted someone who just briefly ran past me. How do I avoid that?**
> Increase the **Greet Delay** under **General → Timing** so WaveKeeper waits before acting. If the player leaves range before the delay expires, the queued greet is automatically cancelled — so a longer delay naturally filters out passersby.

---

**Q21: Why are my emotes queued with a delay when I use Mimic/Copycat mode?**
> WaveKeeper uses a **Queue Spacing** system to avoid sending emotes too fast and hitting the game's chat rate limit. Go to **General → Timing → Queue Spacing** and lower it closer to **0.5 seconds** for near-instant firing. Setting it too low however may cause emotes to silently fail if the game throttles them.

---

**Q22: Someone spammed emotes at me and now there's a huge backlog of queued emotes firing one by one. How do I stop it?**
> Click **Clear Greeted** at the top of the settings window — this also flushes the entire emote queue immediately. Alternatively, set a **Mimic Cooldown** (even just 2–3 seconds) to prevent the queue from building up in the first place.

---

**Q23: Can I use WaveKeeper alongside Copycat at the same time?**
> Technically yes, but it's not recommended. Both plugins hook into emote events and will both try to react to incoming emotes, causing **doubled replies** and queue conflicts. Pick one or the other for mimic/reply behaviour and disable that feature in whichever plugin you're not using for it.

---

**Q24: My emote fires but it targets the wrong person when multiple people are nearby. Why?**
> WaveKeeper targets the player it's replying to before firing the emote. However if your target changes between the time the emote is queued and when it actually fires (due to queue spacing delay), it may land on whoever you're currently targeting. Enable **Target Before Greeting** in **General** to make WaveKeeper always re-target the correct player right before each emote fires.

---

**Q25: The queue keeps firing even after I disabled WaveKeeper mid-session. Is that normal?**
> This was a known issue in earlier versions. In the current version, disabling WaveKeeper mid-session will **stop the queue from draining** immediately. Any already-queued emotes are held and won't fire until you re-enable it — or you can flush them instantly with **Clear Greeted**.

---

## 🙏 Credits

**Made by sm0var**

Thanks to Kingo, Iridescent, Sora, Brit, Willow & Wyno 💜

---

## 📜 License

This project is licensed under the [MIT License](https://github.com/sm0kez/WaveKeeper/blob/main/LICENSE).
