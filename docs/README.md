# ORAC for Project Motor Racing

**Release candidate**

ORAC is an independently developed, clean-room racing AI for Project Motor Racing. It takes over
the AI-controlled cars in offline single-player sessions, planning their speed and steering while
continuously correcting the steering, throttle and brake. It also manages pit stops, including
fuel, tyres, repairs and tyre choice for the conditions.

You drive your car normally; ORAC drives the other cars.

## Credits

- **Austin Ogonoski — tester**
- **Martino Cesaratto — developer**

## Requirements

- A **Windows PC**.
- **Project Motor Racing 2.3.0.3**, installed through **Steam**.
- Steam must be running before you use an ORAC launcher.
- **Offline single-player only.** Do not use ORAC in multiplayer.

This package is built for exactly version **2.3.0.3**. Keep the game on that version: a Steam
update can make ORAC incompatible. The installer checks the game before installing and stops if
the version does not match.

## Install

1. Close Project Motor Racing.
2. If you have never started the game on this PC, start it once and quit. This creates the
   settings file the installer needs.
3. Extract the **whole** ORAC zip into a normal folder. Do not run the installer from the zip
   preview.
4. Double-click **`Install.bat`** and approve the administrator prompt. Administrator access is
   needed for the game folder and `C:\orac`.
5. When installation finishes, use one of the launchers below.

The installer:

- finds Project Motor Racing in your Steam libraries, or asks you for its folder;
- verifies that the game is the supported 2.3.0.3 build;
- backs up the game settings file before enabling the overlay used by F9;
- backs up an existing `dinput8.dll` before replacing it;
- installs ORAC, its small game harness and its support data; and
- creates `C:\orac` for settings, car data and logs.

If you move the game to another folder or drive, run `Install.bat` again so ORAC can learn the
new location.

## Choose a launcher

| Launcher | AI decisions | Steering/pedal updates | Settings file |
|---|---:|---:|---|
| **`Launch ORAC.bat`** (recommended) | 60 per second | 180 per second | `C:\orac\orac_60_180.ini` |
| `ORAC 45-180.bat` | 45 per second | 180 per second | `C:\orac\orac_45_180.ini` |
| `ORAC 30-90.bat` | 30 per second | 90 per second | `C:\orac\orac_30_90.ini` |

`ORAC 60-180.bat` starts the same mode as the default launcher.

These numbers are the AI's **cadence**: how often it makes a plan and how often it updates the
car's controls. A higher control rate allows smoother steering and pedal inputs. The alternative
modes offer a different feel and update load. Start with **60/180**; it is the recommended release
configuration. The alternatives are available if you want to experiment, but their tuning may
differ.

Each mode has its own settings file. An F9 change made in one mode does not change the others.

## Your first race

1. Start Steam and wait until it is ready.
2. Double-click **`Launch ORAC.bat`**.
3. Set up a normal **offline single-player** session in Project Motor Racing.
4. Use the game's AI difficulty setting to choose how quick the opposition should be.
5. Start the race. You drive; ORAC drives the AI cars and handles their pit stops.

There is no pit-stop button you need to press for the AI. ORAC watches the fuel window, tyre wear
and damage, chooses tyres for the conditions, and takes the car through the pit lane for service.

## F9 and F6

- **F9** opens the ORAC overlay during a session.
  - **Tweaks** contains the live settings. Changes take effect immediately and are saved to the
    ini file for the mode you launched.
  - **Debug** contains visual information about the AI's inputs, intended path and speed.
- **F6** opens the debug camera while you are in a car. The camera controls let you follow and
  inspect the action.

You do not need to open either overlay for ORAC to work.

## Uninstall

1. Close Project Motor Racing.
2. Double-click **`Uninstall.bat`** and approve the administrator prompt.

The uninstaller restores the backed-up game files and removes ORAC from the game installation.
It leaves `C:\orac` in place so your settings and learned car data remain available if you
reinstall. Delete that folder manually only if you also want to remove those settings and data.

## Troubleshooting

**The installer says the game version is wrong.** ORAC requires exactly 2.3.0.3. Do not force an
installation onto another version. Keep the game on 2.3.0.3 or use an ORAC package made for your
game version.

**A launcher says ORAC is not installed, or the game was moved.** Run `Install.bat` again with
the game closed. It records the game's current location.

**A launcher says Steam is not running.** Start Steam, wait until it is ready, then try again.

**F9 does not show ORAC.** Close the game and run `Install.bat` again so it can enable the overlay.
Also make sure you started the game through an ORAC launcher.

**The game fails to start or closes unexpectedly.** Run `Uninstall.bat`, then check that the game
starts normally. Reinstall only on the supported game version.

**Your changes have made the AI behave badly.** See `TUNING.md` for restoring a single setting or
using `Reset ORAC settings.bat`.

## Known limitations

- This is a release candidate, not the final release.
- Some cars can still spin occasionally while entering the pits at some tracks. This is being
  improved.
- The AI is tuned primarily for the car roster supplied with the game. Other content may not be
  equally well balanced.
- Mod-track support and additional damage-reading support are not part of this release.
- LMDh hybrid deployment is not enabled in this release.

**ORAC is for offline single-player use only.**
