---
title: "Simple Mechs for Classic Traveller"
slug: 'ct_mechs'
date: 2026-06-30
categories: ['thoughts']
tags: ['ttrpg', 'design', "traveller"]
---

Much of this is adapted from the ATV rules in _Across the Bright Face_.

## Basics

Mechs are a type of vehicle and use the Vehicle (Mech) cascade skill.
While a variety of designs exist, most are about 10 tons in weight and about 4-5m tall.
They can travel at about 80km/hr consistently, with only extremely rough terrain slowing them down.
They normally have only a single pilot.

Mechs are generally a little complicated and finnicky.
They require maintenance once a week or after any combat in which a hit is taken.
Maintenance is a mechanics throw; failing (or not doing maintenance) penalises any DMs by 1 per missed maintenance window.

## Power

Power is supplied by a miniaturised version of a ship-style hydrogen powerplant.
This has 50 power points (pp) when fully fueled.
Life support requires 1pp/hr in most situations; extreme temperatures may consume more.
Movement costs 1pp/hr in normal terrain, 2pp/hr in very rough terrain.
Movement in combat requires 1pp/turn, but will move 1 range-band extra for each extra pp spent, up to 3.
The mech can be refuelled using standard starship fuel, or more slowly, from sizeable amounts of ice or water in the environment.

## Weapons

Standard armament is a large laser, but if you like Book 4 then feel free to add FGMPs or PGMPs instead.
Should it be removed, the laser is not usable without a mount and various connections to a fixed power supply.
The number of pp devoted to firing affects the hit probability.
Each pp used after the first adds +1 to the hit throw.

### Weapon Tables

Weapon | Nothing | Jack | Mesh | Cloth | Reflec | Ablat | Combat
|---|---|---|---|---|---|---|---|
Mech Laser | +4 | +3 | +2 | +2 | -6 | -5 | -5 |

Weapon | Close | Medium | Long | Very Long | Wounds
|------|-------|--------|------|-----------|-------|
Mech Laser | -5 | -1 | +2 | +2 | 6D

## Defences

Mechs are armoured, and most human-portable weapons (small arms) will do little damage.
Treat the mech as having combat armour.
For every 20 damage taken from small arms, make one roll on the damage table.
Ignore any results that are not Gun, Visor, or Lights.
Exceptions may be made for weapons intended to handle armoured targets (anti-tank missiles, FGMPs, mech lasers, &c) which get a roll on the damage table normally.

d6 | Front | Side | Rear
---|---|---|---
1 | Breach | Breach | Breach
2 | Visor | Gun | Fuel
3 | Gun | Motor | Hatch
4 | Gun | Motor | Power
5 | Lights | Fuel | Motor
6 | Motor | Power | Breach

- **Breach**: The armour has been cracked. Life support cost is increased by 1. A patch will let the mech repressurise in about 30 minutes. Roll 2D. On a 2 the pilot has been hit for 1/2 damage.
- **Fuel**: A shot has damaged the fuel tank. Lose half of the remaing fuel. A third hit leaves the vehicle unpowered.
- **Gun**: The main weapon has been damaged, halving damage output. A second hit disables it entirely.
- **Hatch**: The entry hatch has jammed. Escaping the mech will take a successful Mechanic roll or some other means of forcing the hatch open.
- **Lights**: Any external lights on the mech have been hit. This slows it down unless night vision is used.
- **Motor**: One of the motors to a random limb is damaged and movement is halved. A second hit prevents any movement until a repair is made.
- **Power**: The powerplant has been damaged. All power costs are doubled. A second hit disables the plant then make a 2D throw. On a result of 2, the powerplant fails catastrophically.
- **Visor**: The viewport has been damaged. All hit chances are worsened by 2. Additional hits are treated as a breach.
