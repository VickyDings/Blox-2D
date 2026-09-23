# Blox 2D

A 2D blocky online game built in one HTML file. Build, battle, run obbies, and chat with friends.

The whole game is in `blox-2d.html`: the website, the physics engine, the level editor and the multiplayer code. There is nothing to install and no build step. Current version: **7.6** (see [CHANGELOG.md](CHANGELOG.md)).

## Play it

- **On your computer:** download `blox-2d.html` and open it in Chrome, Edge, Firefox or Safari.
- **Online:** open the hosted link (see [Host it](#host-it) below).

The first time, pick a username or press **Play as a guest**. Your account is saved in that browser.

## How to play

### Controls

| Action | Keyboard / mouse | Phone / tablet |
| --- | --- | --- |
| Move | A / D or ← / → | Left stick |
| Jump | Space, W or ↑ | JUMP |
| Sprint | Hold Shift | — |
| Use gear (sword, rocket…) | F or click | USE |
| Switch gear | 1–5 | Tap a slot |
| Talk to townsfolk | E | — |
| Chat | T, Enter or / | SAY |
| Emote | `/e dance`, `/cheer`, … or the Emote button | Emote button |
| Leave the game | Esc | Leave game |

Emotes: dance, wave, laugh, point, sit, cheer, shrug, salute, flex.

### The places

There are twelve hand-built places on the **Games** tab:

- **Obbies** (Escape the Lava Temple, Frostbite Peak): reach the flag. Checkpoints catch you when you fall, and your best time is saved.
- **Brick battles** (Four Corners, Rocket Arena, Swordfights in the Sky, Spirefall Brickbattle): be the first to reach the knockout target. Health packs (+35) sit on the ledges.
- **Disasters** (Natural Disaster Island, The Rising Water): survive floods, meteors and earthquakes.
- **Town and home** (Town of Tiles, Happy Home on the Hill): collect coins to finish an errand, and press E to talk to people.
- **Build** (Build a Base and Defend, Sunset Sandbox): hold off raider waves, or just build.

Every place has a badge. Earn all of them for **Grand Tour**.

### Tickets, Bolts and the catalog

- **Tickets** come from playing: the daily bonus, the daily challenge, coins, knockouts, finishing obbies, winning rounds and more. The **Earn** tab lists everything and what it pays.
- **Bolts** buy limited items and premium gear. Convert between them any time (10 Tickets → 1 Bolt, 1 Bolt → 8 Tickets).
- **Limited items** have a market price that changes daily. Collectors buy them back for 90% of that day's price.
- There are **no real-money purchases**. Nothing in the game asks for a card.

### Studio (build your own place)

1. Go to **Studio** → **Open Studio**.
2. Click to place a brick. Hold and drag to lay a row. Right-click, or the **Placing/Removing** button, switches to erasing.
3. Pick a colour, size and type in the toolbar: normal, lava, trampoline, slippery, spawn point, decoration, checkpoint, coin or finish flag. A place with a finish flag becomes a timed obby.
4. Press **↶ Undo** or Ctrl+Z to step back.
5. Press **Test it** to play it, and **Leave game** to go back to editing.
6. It saves by itself. Your place appears on the Games page under **Places built in Studio**.

To share a place, press **Share** for a `BLOX1:` code anyone can paste in, or **Host online** and give friends the six-character room code.

### Playing with friends

- **Online rooms:** on the Games tab choose **Online — real people**, then press Play. Pick a server number to meet on the same one.
- **Party Chat:** set a party code on the Party Chat tab. Friends type the same code to chat, even outside a game.
- **Moving your account:** Account → **Make a transfer code**, then paste it on the other device's login screen. It makes a copy, not a live sync.

### Parental controls

The **Parental controls** tab uses a 4-digit PIN. It can:
- turn off online play, gear, spending or Studio
- limit chat to a safe phrase menu, or turn chat off
- choose which game types are allowed
- set a daily time limit

The settings live in the browser. They stop a child from flipping switches, but they are not a vault: clearing browser data clears them.

## Host it

The game is a single static file, so any static host works. Serve it over `https://` so online play and the install button work (they don't from a `file://` page).

### GitHub Pages (free)

1. In this repository on GitHub: **Settings → Pages**.
2. Under **Build and deployment**, choose **Deploy from a branch**, pick `main` and `/ (root)`, and save.
3. After a minute the game is at `https://<your-username>.github.io/Blox-2D/`. The included `index.html` forwards straight to `blox-2d.html`.

### Netlify (free)

Drag the repository folder onto <https://app.netlify.com/drop>, or connect the GitHub repo. No build command and no publish directory are needed.

### Online play on any network: set up a relay

At home, online play works automatically through free public servers. School and office networks often block those. To fix that, run your own free relay:

1. In the game, open **Account → Online play**.
2. Press **Open Deno Deploy** and sign in (free, no card), then create a **New Playground**.
3. Press **Copy relay code** in the game, paste it into the playground, and press **Save & Deploy**.
4. Copy the address Deno gives you (like `https://abc123.deno.dev`), paste it into the game, press **Save**, then **Test**.

Everyone who wants to play together on that relay pastes the same address.

## Making changes

- Everything lives in `blox-2d.html`. Places are in `LAYOUTS`, catalog items in `CATALOG`, badges in `BADGES`, daily challenges in `CHALLENGES` and themes in `THEME_PRESETS`.
- Raise `BLOX_VERSION` near the top of the script and add a line to `CHANGES` (shown on the Roadmap tab) and to `CHANGELOG.md`.
- Opening the page with `window.__BLOX_TEST__ = true` set first exposes a `window.__blox` object for automated tests.

A fan-made homage to the classic era of blocky building games. All code, art, names and sounds are original.
