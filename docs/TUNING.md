# ORAC tuning guide

You do not need to tune ORAC before using it. Start with **`Launch ORAC.bat`** and the game's AI
difficulty setting. If you do make changes, alter one thing at a time and test it with the same
car, track and conditions.

## Where your settings are saved

Each launcher uses a separate file:

| Mode | Settings file |
|---|---|
| 60/180 — default | `C:\orac\orac_60_180.ini` |
| 45/180 | `C:\orac\orac_45_180.ini` |
| 30/90 | `C:\orac\orac_30_90.ini` |

Changes made in F9 are saved automatically to the file for the mode you launched. Your 60/180
changes therefore do not carry into 45/180 or 30/90.

The file does not need to list every setting. F9 normally saves values that differ from ORAC's
built-in defaults, along with a small number of standard entries.

## Using F9

1. Start a session through the launcher for the mode you want to tune.
2. Press **F9**, then open **Tweaks**.
3. Find the relevant page, such as **Pace & difficulty** or **Output**.
4. Make a small change. It takes effect immediately and is saved to the active mode's ini file.
5. Test before making another change.

Close the game before editing an ini file by hand or running the reset tool. Otherwise an F9 save
can overwrite your manual change. After a manual edit, restart the game to load the file again.

## The most useful controls

### Game AI difficulty

Use the normal AI difficulty setting in the race setup first. It is the simplest way to make the
field faster or slower without changing ORAC's tuning.

In **F9 → Tweaks → Pace & difficulty**, the **At slider 100** group sets the cornering, braking,
acceleration and tyre multipliers used at maximum game difficulty. The **At slider 90** and
**At slider 20** groups shape the lower difficulty levels. Leave those lower-level groups at their
release values unless you deliberately want to reshape the whole difficulty curve.

The main multipliers are:

- **Corner** — how much cornering performance the AI uses.
- **Acceleration** — how much acceleration performance it uses.
- **Brake** — how much braking performance it uses.
- **Tyre** — the overall tyre-performance allowance.

These are multipliers, not percentages added to the game's difficulty slider. Higher values allow
more performance; lower values leave more margin. Make small changes.

### Tyre per vehicle class

Under **Pace & difficulty → Tyre per vehicle class**, each class has its own tyre multiplier. This
is the useful control when one type of car is too strong or too weak relative to another.

Change only the class you are testing. Raising its value gives that class more tyre capability;
lowering it reduces the allowance. The supplied values are intentionally different between
classes, so a single value applied everywhere would discard the release balance.

### Steering filter

Under **Output → Steering emission limiters**, the steering notch filter reduces a repeating
steering wobble at the planning frequency.

- **Strength** controls how much of the filtered signal is used. **0** turns the filter off,
  **0.5** is the release setting, and **1** applies it fully.
- **Frequency** should match the mode's planning rate: **60** for 60/180, **45** for 45/180 and
  **30** for 30/90.
- **Q** controls how narrowly the filter targets that frequency. The supplied value is **8**;
  leave it there for normal tuning.

More filtering is not automatically better. If steering response changes in a way you do not like,
return Strength to **0.5** or temporarily set it to **0** to compare.

The supplied modes already have matching cadence and filter settings. Prefer the launchers over
copying one mode's ini onto another.

## Restore a setting or the package defaults

### Remove one manual override

With the game closed, open the active mode's ini file in a text editor and delete the line for the
setting you want to clear. Save the file and restart the game.

Deleting a line removes that file's override and returns the setting to ORAC's **built-in default**.
That is not necessarily the tuned value supplied with this package.

### Restore the supplied settings

Close the game and run **`Reset ORAC settings.bat`**. The reset tool restores the package settings,
backs up your current settings first, and leaves learned car data alone. Because the modes use
separate files, reset each mode you have changed rather than assuming one reset covers all three.

If you want to preserve an experiment, copy the relevant ini file somewhere safe before resetting
it.
