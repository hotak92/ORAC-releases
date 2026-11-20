# What's new in this ORAC release candidate

## Braking
- Cars learn how hard they can really brake (from the torque at the wheel hubs), separately from how much grip the
  tyres have, and plan their braking from it.
- Braking is planned with a short build-up, as a real driver squeezes the pedal, and every brake zone starts on time.
- Lock-ups and rear slides under braking are caught earlier and more gently, so cars keep turning into the corner and
  spin far less — while the brakes are never cut away completely.
- Result in our Monza tests: about a second a lap quicker for the prototypes, half a second for GT3, with fewer
  contacts and spins.

## Race start and pit stops
- Each AI car starts on the tyre and the fuel ORAC chose for the race (the conditions, the race length and the car's
  own consumption).
- The pit strategy plans the whole race: fuel, tyre wear, damage and the right tyres for the conditions, and stops
  only when the stop pays off.
- Cars know their own pit box from the start, plan their braking into the pit lane early, respect the pit limiter
  and stop at the box.
- Full grids work at tracks with fewer pit boxes or grid slots than cars: the extra cars share a pit box, and the
  extra grid slots are added at the back of the grid (before, the game could crash while loading).

## Four update-rate modes
- **60/60** — the default, launched by `Launch ORAC.bat`.
- **60/180**, **45/180** and **30/90** — each with its own launcher and its own settings file in `C:\orac`, tuned for
  that mode. F9 changes are saved to the mode you are using.

## Share and help
- **`Share ORAC data.bat`** sends ORAC's learned car data (and, if you agree, your best AI laps for the leaderboard)
  to openracingai.com, where everyone's data is combined into better figures for all players.
- On the website you can browse, download and rate shared racing lines and tweaks, filter by class and car, and share
  or download performance envelopes for mod cars. Accounts use your e-mail and a password.

See `KNOWN ISSUES.md` for what is still being worked on.
