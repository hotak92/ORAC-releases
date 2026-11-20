# ORAC — known issues

This is a release candidate. These are the things we know about and are working on.

## Switched off in this release
- **Hybrid deployment (LMDh, LMH, LMP1):** ORAC can't use the game's own deploy strategy, so we need to build our own.
  We're working on it, but it takes quite a lot of effort and isn't good enough yet to turn on. Hybrid cars race
  without electric deployment for now.

## Known issues
- Some cars can still spin now and then when entering the pits at some tracks.
- Very large fields (about 30 cars) can make the game run slower than real time on some PCs. A smaller field helps.
  A performance round is planned.
- Mod tracks are not supported yet.
- Mod cars need their performance envelopes before ORAC can drive them well. Generate them with
  `orac\orac_generate_ai.bat` and `orac\orac_generate_player.bat` (see `orac\README.txt`; the player ones take about
  11 minutes per car), or download ones other players shared on openracingai.com (the mod car's page).
- ORAC works only with game version 2.3.0.3. A Steam update can stop it working until a matching ORAC is released.
- Offline single-player only. Don't use ORAC in multiplayer.
- On openracingai.com, the sign-in e-mail can land in your spam folder.

Found something else? Report it on openracingai.com with the track, the car and the time in the race.
