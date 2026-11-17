<div align="center">

# ★ Cosmo Raider ★

**A retro handheld space-shooter that runs in any web browser.**

<img src="images/gameplay.gif" alt="Cosmo Raider gameplay: the cannon slides along the bottom row and shoots at a marching formation of red aliens" width="300">

[▶ Watch the how-to video](images/cosmo-raider-how-to-play.mp4) · [Quick start](#quick-start) · [Controls](#controls) · [How to play](#how-to-play) · [Ways to use it](#ways-to-use-it)

</div>

---

Cosmo Raider is styled after the red-glow VFD (vacuum fluorescent display) tabletop games of the late 1970s. It has a fixed 7 × 9 grid, faint "ghost" segments showing where sprites can appear, a 7-segment score readout and chunky yellow buttons.

The whole game is **one HTML file**. There's nothing to install, no build step and no server code. It works with a keyboard on a computer or with touch on a phone or tablet.

## Contents

1. [How-to video](#how-to-video)
2. [Quick start](#quick-start)
3. [Controls](#controls)
4. [How to play](#how-to-play)
5. [How a game flows](#how-a-game-flows)
6. [Difficulty: PRO vs AM](#difficulty-pro-vs-am)
7. [Full screen and mobile](#full-screen-and-mobile)
8. [Ways to use it](#ways-to-use-it)
9. [Using it in teaching](#using-it-in-teaching)
10. [Troubleshooting](#troubleshooting)
11. [Repository layout](#repository-layout)
12. [Technical notes](#technical-notes)

---

## How-to video

[![How-to video: click to play the one-minute guide](images/video-poster.jpg)](images/cosmo-raider-how-to-play.mp4)

**[▶ Play the video](images/cosmo-raider-how-to-play.mp4)** (MP4, about 1 minute, with the game's sound effects)

The video shows real gameplay with captions, in eight steps:

| # | Step | What you'll see |
|---|---|---|
| 1 | Turn it on | Flipping the ON/OFF switch |
| 2 | Move your cannon | The left and right arrow keys |
| 3 | Fire! | Shooting, one shot at a time |
| 4 | Clear the wave | The formation marching, bombs, shields |
| 5 | Hit the mystery UFO | Timing a bonus shot |
| 6 | PRO or AM? | Changing the difficulty mid-game |
| 7 | Lives and game over | Losing lives, the HI score, restarting |
| 8 | Full screen and sound | The enlarged view and the mute button |

> **Tip for GitHub:** GitHub doesn't play MP4 files from a repository inline, so the links above open the video file. For an inline player, edit this README on github.com, drag `cosmo-raider-how-to-play.mp4` into the editor, and GitHub will swap in a hosted video link.

---

## Quick start

<img src="images/01-power-off.png" alt="The Cosmo Raider handheld switched off, with the ON/OFF switch on the right" width="280" align="right">

1. **Open the game** in a browser (see [Ways to use it](#ways-to-use-it)).
2. **Switch it on** with the **ON/OFF** switch on the right of the device. It pulses until you use it. You can also press **O**.
3. **Move** with the yellow arrow keys (or **←** **→**) and **fire** with the **FIRE** button (or **Space**).
4. **Destroy every alien** before the formation reaches your row.

> **Sound:** browsers block audio until you interact with the page, so the bleeps start after your first button press or key press.

<br clear="right">

---

## Controls

![Annotated diagram of the Cosmo Raider controls](images/diagram-controls.png)

| Action | Keyboard | On screen / touch |
|---|---|---|
| Move left | **←** or **A** (hold to keep moving) | Left yellow arrow key |
| Move right | **→** or **D** (hold to keep moving) | Right yellow arrow key |
| Fire | **Space**, **↑** or **W** | **FIRE** button (bottom left) |
| Restart after game over | **Space**, **↑** or **W** | **FIRE** button, when it pulses |
| Power on / off | **O** | ON/OFF switch (right) |
| Difficulty PRO / AM | **P** | PRO/AM switch (left) |
| Sound on / off | **M** | **SOUND** button (bottom right) |
| Full screen | **F** | Corner icon (top right of the page) |

A shortcut reminder appears under the device on computers with a mouse. It's hidden on touch devices.

---

## How to play

![Diagram of the 7 by 9 playfield, showing the UFO row, alien formation, shot, bomb, shields and cannon](images/diagram-playfield.png)

### The rules

- **Your cannon** sits on the bottom row and moves one column at a time across 7 columns.
- **You get one shot at a time.** You can't fire again until your shot hits something or leaves the top of the screen.
- **The alien formation** marches side to side and drops a row each time it reaches an edge. The first wave has 2 rows of 4 aliens; every wave after that has 3 rows.
- **The formation speeds up** as you thin it out, and each new wave starts faster than the last.
- **Aliens drop bombs** (zig-zag shapes) from the lowest alien in a column. A bomb that hits your cannon costs a life.
- **Shots and bombs cancel each other out** if they meet in the same square, so you can shoot bombs down.
- **Three shields** sit just above your cannon. Each one absorbs 3 bomb hits, losing a segment per hit, and comes back at full strength every wave. Your own shots pass straight through them. If the aliens march down onto a shield, it's destroyed.
- **A mystery UFO** sometimes flies across the top row. Hit it for bonus points.
- **Clear every alien** to finish the wave. The shields flash and the next wave begins.

### Scoring

| Target | AM | PRO |
|---|---|---|
| Alien | 1 | 2 |
| UFO | 5 | 10 |

The display shows three digits, so the maximum score is **999**.

### Lives and game over

<img src="images/03-game-over.png" alt="Game-over screen with the FIRE button glowing to restart" width="220" align="right">

- You start with **3 lives**, shown as the red bars to the right of the score.
- You lose a life each time a bomb hits you.
- **If the aliens reach your row, the game ends immediately**, however many lives you have left.
- On the game-over screen your cannon blinks and the display switches between your **SCORE** and the **HI** (high score).
- When the **FIRE** button starts glowing, press it (or **Space**) to start a new game.

Your best score is saved in your browser. It's kept per browser and per device, and it's lost if you clear site data or use a private window.

<br clear="right">

---

## How a game flows

![Flowchart: power on, new wave, play, then wave cleared, hit by a bomb, or aliens reach row 9, leading to game over and restart](images/diagram-flow.png)

---

## Difficulty: PRO vs AM

The switch on the left sets the difficulty. The game starts in **AM** (amateur), with the knob down.

| | AM | PRO |
|---|---|---|
| Formation speed | Normal | Faster |
| Bomb speed | Normal | Faster |
| Bombs on screen at once | Up to 2 | Up to 3 |
| Chance of a bomb on each march step | Lower | Higher |
| Points | Standard | Double |

You can change the switch mid-game. It takes effect straight away and doesn't restart the game.

---

## Full screen and mobile

<table>
<tr>
<td align="center"><img src="images/04-full-screen.png" alt="Full-screen mode with the device enlarged on a dark background" width="260"><br><b>Full screen</b></td>
<td align="center"><img src="images/05-mobile.png" alt="Cosmo Raider on a phone-sized screen" width="230"><br><b>On a phone</b></td>
</tr>
</table>

- Tap the **corner icon** or press **F** to enlarge the game, and do the same again to exit.
- Where the browser allows it, the page goes properly full screen (and tries to lock phones to portrait). Where it doesn't (iPhone Safari, for example, or an embedded frame without permission), the device is enlarged to fill the window on a dark background instead.
- On touch screens, all the controls are on the device itself. The buttons react the moment you touch them and repeat while held.

---

## Ways to use it

![Four ways to use Cosmo Raider: open directly, host on GitHub Pages, embed in Moodle or a docs site, play on a phone or tablet](images/diagram-usage.png)

### 1. Open it directly

- Open the claude.ai artifact link, **or**
- Download `index.html` and double-click it. It opens in your default browser and works offline (the label fonts fall back to system fonts without an internet connection).

### 2. Host it on GitHub Pages

1. Create a new repository on GitHub, for example `cosmo-raider`.
2. Upload `index.html` (plus this `README.md` and the `images/` folder, if you want the documentation too).
3. Go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**, select **`main`** and **`/ (root)`**, then click **Save**.
5. After a minute or so the game is live at:

   ```
   https://<your-username>.github.io/cosmo-raider/
   ```

### 3. Embed it in Moodle or a docs site

First host the game (option 2) so it has a URL. Then paste this snippet where you want it to appear:

```html
<iframe
  src="https://<your-username>.github.io/cosmo-raider/"
  title="Cosmo Raider"
  width="440" height="860"
  style="border:0; max-width:100%;"
  allow="fullscreen">
</iframe>
```

- **Moodle:** add a **Page** (or a **Text and media area** / Label), open the editor's **Source code** view (`</>`), paste the snippet and save. If the iframe disappears when you save, your site may only allow embedded content from trusted users, so ask your Moodle administrator.
- **Just the Docs / Jekyll / any Markdown site:** paste the snippet straight into the page's `.md` file. Raw HTML is allowed.
- **Sizing:** the device scales down to fit smaller frames. 440 × 860 shows it at full size. Use a smaller height (around 640) for a more compact embed.
- **Full screen:** keep `allow="fullscreen"` so the corner icon can use real full screen. Without it, the game falls back to its enlarged layout.
- **Keyboard:** players need to click or tap the game once so the frame receives their key presses.

### 4. Play on a phone or tablet

1. Open the game's URL in Safari or Chrome.
2. Tap the corner icon for full screen.
3. Optional: use **Share → Add to Home Screen** (iOS) or **⋮ → Add to Home screen** (Android) for one-tap access.

---

## Using it in teaching

A few ideas for using the game with students:

- **A warm-up or reward activity:** embed it on a course page and run a "beat the HI score" challenge.
- **A code-reading exercise:** the whole game is about 600 readable lines in one file. Students can trace how it uses a game loop (`requestAnimationFrame`), a simple state machine (`play` → `dying` → `wave` → `over`), canvas drawing, Web Audio sound generation and pointer/keyboard input.
- **A starter project to modify:** students can change the colours, the sprites (they're drawn from text grids such as `"..XXX.."`), the scoring or the difficulty, and then publish their version to GitHub Pages.
- **A UX discussion piece:** compare skeuomorphic hardware controls with standard web UI, and look at touch target sizes, feedback and the hint bar.

---

## Troubleshooting

| Problem | Fix |
|---|---|
| No sound | Press any button first, since browsers block audio until you interact. Check the **SOUND** light is red and your device isn't muted. |
| Keys don't do anything | Click or tap the game once, especially when it's embedded in another page. Make sure the game is switched **ON**. |
| Full screen just makes it bigger | That's the fallback layout, used on iPhone Safari or when an iframe lacks `allow="fullscreen"`. It plays the same. |
| High score has gone | It's stored in the browser, so it's lost after clearing site data or in a private window, and it doesn't carry over between devices. |
| Iframe vanishes in Moodle | Your site filters embedded content, so ask an administrator. Or link to the game's URL instead. |
| Fonts look different | The label fonts load from Google Fonts. Offline, system fonts are used instead and the game is unaffected. |

---

## Repository layout

```
cosmo-raider/
├── index.html                          ← the game (everything in one file)
├── README.md                           ← this guide
└── images/
    ├── gameplay.gif                    ← animated preview at the top
    ├── cosmo-raider-how-to-play.mp4    ← captioned how-to video
    ├── video-poster.jpg                ← video thumbnail
    ├── diagram-controls.png            ← annotated controls
    ├── diagram-playfield.png           ← playfield explained
    ├── diagram-flow.png                ← game flowchart
    ├── diagram-usage.png               ← ways to use it
    ├── 01-power-off.png                ← screenshots…
    ├── 02-playing.png
    ├── 03-game-over.png
    ├── 04-full-screen.png
    └── 05-mobile.png
```

---

## Technical notes

- **Single file:** HTML, CSS and JavaScript all live in `index.html`. The game is drawn on `<canvas>`, and sound effects are generated live with the Web Audio API, so there are no image or audio assets.
- **Dependencies:** none apart from two Google Fonts (*Archivo Black* and *Barlow Condensed*) for the device labels.
- **Responsive:** the device scales to fit the screen's width and height, and the canvas renders at your screen's pixel density.
- **Input:** pointer events for touch and mouse (with hold-to-repeat on the arrow keys), plus keyboard shortcuts.
- **Storage:** the high score is kept in `localStorage` under the key `cosmoRaiderHi`.
- **Artwork:** all sprites (aliens, cannon, UFO, explosion) are original pixel designs defined as text grids in the script.
