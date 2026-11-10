# Hogwarts Legends: The Sixth Weasley Part 1

**Hogwarts Legends: The Sixth Weasley Part 1** is a short fan game in two plots about Ron, the sixth Weasley child, in his final year at Hogwarts.

- **Plot 1, The Chamber (first person):** Ron goes down into the flooded Chamber of Secrets alone to face a blinded, enraged basilisk, armed with only his wand and his nerve.
- **Plot 2, The Sky Road (third person):** Ron flies the family's sky-blue car north above the Hogwarts train, with Harry beside him, when Death Eaters come out of the clouds.

> Unofficial, non-commercial fan game. Not affiliated with or endorsed by the Harry Potter rights holders.

## The story

Far below the castle, the Chamber of Secrets lies open, and its ancient guardian is awake. A phoenix sweeps out of the dark and claws out the serpent's eyes. Blind and screaming, it can no longer see you. But it can still hear you.

Then the last year begins. The black steam train runs north through the glens, and two of its passengers have decided to fly instead, until green curses tear out of the clouds ahead.

## Gameplay

### Plot 1: The Chamber

- **Incendio:** a fast stream of fire that keeps the pressure on.
- **Stupefy:** stuns the basilisk for 7 seconds and makes your attacks hit harder. It takes 15 seconds to recharge, shown by a bar on its icon.
- **Venom volleys:** the basilisk spits a wide spread of venom every 1.45 seconds, aimed at where you're about to be.
- **Rams:** once it's badly hurt, it starts charging at you. Watch for the red warning line, roll out of the way, and lure it into a pillar to daze it.

### Plot 2: The Sky Road

- **Goal:** stun 13 Death Eaters within 2 minutes 30 seconds. One hit from Harry's red Stupefy sends a Death Eater tumbling out of the sky.
- **They strike first:** Death Eaters open fire as soon as they arrive, with fast green curses aimed at where the car is heading. Flying straight is deadly, so keep swerving and changing speed.
- **Ron steers, Harry casts:** hold right-click to lock on, and locked spells curve onto their target.
- **Car health:** shown at the bottom left. Hits make the car smoke, then catch fire; too many and it goes down.
- **Two at a time:** two Death Eaters hunt the car at once, and they get faster and more aggressive the more you stun. When only three are left, all three come for you together. They shout curses and laugh as they attack.
- **Win** and the car sweeps over the castle and lands on the lawn.

## Editions

There are two editions. They install side by side, so you can have both.

| Edition | What's different |
|---|---|
| **Standard** | Plot 2 unlocks once Plot 1 is won. |
| **Plot Select** | Both plots are on the main menu from the start. |

## Features

- A cinematic opening with a phoenix attack and spoken narration, and an ending cutscene when the basilisk falls
- A horned, armoured basilisk with a hide made from a real reptile-skin scan
- Venom that wobbles in flight, splashes, sizzles on the floor and spatters your view
- A flooded hall of scanned stone, with fluted serpent pillars, carved friezes, chained fire bowls, rippling water, mist and shafts of light
- Plot 2: volumetric clouds you can fly straight through, sun shadows across the Highlands, dense forests, stone-walled fields, sheep and lochs
- A detailed black steam train in the glen below, and a castle on a loch for the ending
- Crackling, sparking spell beams: red for Harry, green for the Death Eaters
- Spoken dialogue for every character, and an adventure score for the Plot 2 ending
- Automatic quality: on weaker laptops the game lowers its resolution to stay smooth
- Memory protection: the game won't start without enough free memory, and closes itself before the PC runs out

## Controls

### Plot 1: The Chamber

| Key | Action |
|---|---|
| W A S D | Move |
| Mouse | Look |
| Left click | Cast (hold to keep casting) |
| Scroll | Switch between Incendio and Stupefy |
| Space + A / Space + D | Roll left / right |

### Plot 2: The Sky Road

| Key | Action |
|---|---|
| W / S | Fly faster (with a speed blur) / slower |
| A / D | Steer left / right |
| Mouse | Move Harry's aim |
| Right click (hold) | Lock on to a Death Eater |
| Left click | Harry casts Stupefy |

### Both plots

| Key | Action |
|---|---|
| Esc | Pause (Resume, Main Menu, Quit) |
| Enter | Skip a cutscene |
| Ctrl + Shift + Q | Quit instantly, even if the game hangs |

## Install on Windows

1. Download **HogwartsLegends-Setup.exe** (or **HogwartsLegends-PlotSelect-Setup.exe**) from the [Releases](../../releases) page.
2. Run it. Windows may show "Windows protected your PC", because the installer isn't signed by a paid publisher. Click **More info**, then **Run anyway**.
3. Start the game from the desktop or Start menu shortcut.

To uninstall, use **Settings → Apps** in Windows. Installing over the earlier "Ron vs the Basilisk" version replaces it, shortcuts included.

**Requirements:**

- Windows 10 or 11, with Microsoft Edge (included with Windows). Nothing else to install.
- About 3 GB of free memory when starting.
- A graphics card is recommended. Integrated graphics work, at a lower resolution.

## Install on Linux

The Linux version runs the same game in Electron, which uses the same Chromium engine as the Windows version, so it looks and plays the same. Each edition comes as a .deb package and as a portable folder.

| Edition | .deb package | Portable folder |
|---|---|---|
| Standard | `hogwarts-legends_1.0.0_amd64.deb` | `HogwartsLegends-linux-x64.tar.gz` |
| Plot Select | `hogwarts-legends-plotselect_1.0.0_amd64.deb` | `HogwartsLegends-PlotSelect-linux-x64.tar.gz` |

**Ubuntu, Debian, Linux Mint, Pop!_OS:** download the .deb from [Releases](../../releases), then double-click it, or run:

```bash
sudo apt install ./hogwarts-legends_1.0.0_amd64.deb
```

Start it from the applications menu, or by running `hogwarts-legends`. To uninstall:

```bash
sudo apt remove hogwarts-legends
```

**Any other 64-bit distribution:** download the .tar.gz, then unpack it and start it:

```bash
tar -xzf HogwartsLegends-linux-x64.tar.gz
./HogwartsLegends/start.sh
```

Run `./HogwartsLegends/add-to-menu.sh` to add it to your applications menu.

- **Requirements:** a desktop (X11 or Wayland), about 3 GB of free memory, and a working graphics driver (Mesa for AMD and Intel, or the NVIDIA driver). Without one, the game warns you that it's drawing with the processor and will be slow.
- **Laptops with two graphics chips:** the menu entry asks for the stronger card automatically.
- **Extra keys:** F11 switches full screen on and off.

## Running from source

The game is plain HTML and JavaScript and needs no build step. Serve the `game/` folder with any local web server and open it in Microsoft Edge or Chrome.

### Windows installers

Run these in PowerShell from the repository folder. They use the C# compiler that comes with Windows (.NET Framework 4).

```powershell
powershell -ExecutionPolicy Bypass -File installer/build.ps1
```

```powershell
powershell -ExecutionPolicy Bypass -File installer/build.ps1 -PlotSelect
```

They write `dist/HogwartsLegends-Setup.exe` and `dist/HogwartsLegends-PlotSelect-Setup.exe`.

### Linux packages

Download `electron-v45.2.3-linux-x64.zip` from [Electron's releases](https://github.com/electron/electron/releases/tag/v45.2.3), then run these. They use the same built-in C# compiler, so they run on Windows:

```powershell
powershell -ExecutionPolicy Bypass -File linux/build.ps1 -ElectronZip "path\to\electron-v45.2.3-linux-x64.zip"
```

```powershell
powershell -ExecutionPolicy Bypass -File linux/build.ps1 -ElectronZip "path\to\electron-v45.2.3-linux-x64.zip" -PlotSelect
```

They write the .deb and .tar.gz files listed above into `dist/`.

## Project layout

| Folder | Contents |
|---|---|
| `game/` | The game: `index.html`, scripts in `js/` (Plot 2 in `js/plot2/`), embedded models, textures, voices and music in `assets/`, and three.js in `vendor/` |
| `installer/` | The Windows installer and launcher (`Setup.cs`) and its build script |
| `linux/` | The Linux app (`app/main.js`, an Electron shell with the Windows launcher's safeguards), the launcher and menu scripts, the .deb install scripts, and the packer (`Pack.cs`) |
| `tools/` | Developer tools used to prepare the character models and record the voices. They need a local web server to run. |

## Credits

The game is built on [three.js](https://threejs.org). The Linux version runs on [Electron](https://www.electronjs.org) (MIT), whose licence and Chromium's are included in the Linux packages. Third-party material is listed with its licence in [`game/CREDITS.txt`](game/CREDITS.txt):

- Characters by Grab3D (CC0)
- First-person hand from Microsoft Rocketbox (MIT)
- Phoenix by NORBERTO-3D (CC BY 4.0), recoloured
- Basilisk hide, chamber and castle stone from ambientCG (CC0)
- Plot 2 sky and ground textures from Poly Haven (CC0)
- Voices recorded with the Kokoro-82M speech model by hexgrad (Apache 2.0)
- Death Eater laughs from "Evil Laughs Pack" by Eldritch Grim (CC0)
- Plot 2 ending music: "Adventurer's Path" by vitalezzz (CC0)

## Licence

No licence is granted for this project. The original code is shared for viewing only. Third-party material keeps its own licence, as listed in `game/CREDITS.txt`. Harry Potter characters, names and places belong to their respective owners.
