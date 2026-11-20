# What’s new in the ORAC release candidate

This release candidate updates the previous tester package with working end-to-end pit stops,
smoother control, selectable update rates and revised class balance.

## Autonomous pit stops

ORAC now manages the complete pit-stop cycle for AI cars:

- decides when to stop using the fuel window, tyre wear and damage;
- chooses an appropriate tyre compound for the conditions;
- brings the car into the pit lane, stops at its box for service and drives back out; and
- accounts for the car's real fuel capacity when planning refuelling.

Fuel-stop timing is spread across the useful strategy window rather than sending the whole field
to the pits at the first opportunity.

## Smoother steering

The recommended **60/180** mode makes 60 planning decisions per second and updates steering and
pedals 180 times per second. The higher control rate gives finer, smoother inputs.

A steering filter also reduces the repeating wobble associated with the planning update rate. It
is set to half strength in the supplied configuration, and each cadence mode has a filter setting
matched to that mode.

Steering through the pit lane now follows a smooth path for the whole visit, including entry and
exit.

## Three cadence modes

- **60/180** — the recommended default, launched by `Launch ORAC.bat`.
- **45/180** — fewer planning updates with the same control update rate.
- **30/90** — lower planning and control update rates.

Each mode loads its own ini file in `C:\orac`. F9 changes are saved to the mode currently in use,
so you can experiment with one mode without changing the others.

## Revised balance between classes

Tyre difficulty now has updated defaults for individual vehicle classes. This gives different
types of car a more appropriate balance instead of applying one tyre value to the whole roster.
The controls remain available under **F9 → Tweaks → Pace & difficulty**.

## Still worth knowing

An occasional pit-entry spin remains possible with some car and track combinations. The release
is tuned primarily for the game's shipped roster. LMDh hybrid deployment is not enabled, and
mod-track support is not included in this release.

See `README.md` for installation and known limitations, and `TUNING.md` for the settings guide.
