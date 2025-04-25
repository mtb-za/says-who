---
title: 'Ship Information System'
slug: 'traveller_ais'
date: 2025-02-10
categories: ['thoughts']
tags: ['traveller', 'tools', 'development']
---

One thing that might be useful for thinking about in SF settings is what information ships broadcast. While all sorts of things _could_ be, a good model for what information might be valuable is to look at the [Automatic Information System](https://en.wikipedia.org/wiki/Automatic_identification_system) (AIS) used by shipping here on Earth. This is a transmitter that broadcasts a position and other identifying information reguarly, originally for collision avoidance, but which is now used for a variety of other things.

The core of the information is sent every few seconds while underway:

- Vessel Maritime Mobile Service Identity (MMSI): a unique nine digit identification number.
- Navigation status: e.g., "at anchor", "under way using engine(s)", "not under command", etc.
- Rate of turn: right or left, from 0 to 720 degrees per minute
- Speed over ground: 0.1-knot (0.19 km/h) resolution from 0 to 102 knots (189 km/h)
- Positional resolution:
  - Longitude: to 0.0001 arcminutes precision
  - Latitude: to 0.0001 arcminutes precision
- Course over ground: relative to true north to 0.1° precision
- True heading: 0 to 359° (for example from a gyro compass)
- True bearing at own position: 0 to 359°
- UTC seconds: The seconds field of the UTC time when these data were generated. A complete timestamp is not present.

And then some additional information every few minutes:

- IMO ship identification number: a seven-digit number that remains unchanged upon transfer of the ship's registration to another country
- Radio call sign: international radio call sign
- Name: name of the vessel
- Type of ship/cargo
- Dimensions of ship, to nearest meter
- Location of positioning system's (e.g., GPS) antenna on board the vessel
- Type of positioning system: such as GPS, DGPS or LORAN-C.
- Draught of ship: 0.1–25.5 meters
- Destination
- Estimated time of arrival (ETA) at destination: UTC month/date hour:minute
- Optional: high precision time request, a vessel can request other vessels provide a high precision UTC time- and date-stamp

Translating this into something for space games, we should probably simplify this down somewhat. This looks like the core of it to me, with some reasoning:

- Some sort of fixed unique ID code which 'never changes', even if owner does, and is not shared by any other vessel in the registry. This is the sort of thing that governments are going to crack down hard on trying to hack, and so the sort of thing that pirates are going to try and spoof if they are running false flag operations.
- Alphanumeric string for a name. This is the name that the vessel uses in day-to-day life. There is no enforced uniqueness, and could be in multiple languages or similar. For some areas of space, there might be multiple name fields for different major languages spoken in that area.
- Some sort of ID code for internal use, issued by home planet/corporation or similar. This is mostly nice to let players get a feel for which corporation (if any) owns a given ship. If all of the vessels owned by Gozon Corporation have the same sort of code, then it is a nice way to find or avoid them.
- Ship class. Depending on what is available in your setting, you might have traders, military types (frigate, cruiser, battleship, &c), various commercial types (liners, tankers, freighters)
- Current location. In reality this is probably some sort of spherical coordinate relative to the central star or a given planet[oid], but just 'Tycho Naval Base' or 'Carrington Downport' is going to be enough for a game.
- Next destination. This is probably only needed in-system: "Derys Highport"; "Surface", "Leaving System", that sort of thing.
- Tonnage
- Jump drive level (This might vary according to the setting/system that you are using, so is probably optional.)
- ETA at destination

For a game, the easiest way to have an AIS-like tool would probably be to automate the generation of it through code. With some good name generation, that could kick out a handful of AIS transmissions like this:

```
AISID: df2ad945-153a-4430-a88b-563fcc5686dd
Ship Name: The Naughty Sausage
Ship Class: Tramp Trader
Jump: 2
Tonnage: 200
Readable ID: GOZ-U2591
Location: Japhantis High Orbit
Destination: Japhantis City High Port
ETA: 63 minutes
```

Here we have the 200 ton tramp trader _The Naughty Sausage_, moving from Japhantis High Orbit to Japhantis City Starport, landing in just over an hour. The Readable ID indicates that it belongs to Gozon Corporation.

This should be something that is readily usable in a game set around common space travel.
