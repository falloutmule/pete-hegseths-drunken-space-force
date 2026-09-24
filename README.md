# Pete Hegseth's Drunken Space Force

[Play the game](https://falloutmule.github.io/pete-hegseths-drunken-space-force/)

[Read the original complete game specification](PETE_HEGSETHS_DRUNKEN_SPACE_FORCE_COMPLETE_SPEC.md)

The original specification is included unchanged and remains the product reference for future edits.

A portrait arcade shooter and fictional political satire. The release is one self-contained HTML file with embedded artwork, game code, and synthesized audio.

Drag in the battlefield to fly; weapons fire automatically. A second finger can press SELL BONDS or BURN $1B. PLAY FULLSCREEN enters phone fullscreen and starts a run. Pause contains sensitivity, effects, sound, and fullscreen settings.

This repository contains the playable release. GitHub Pages publishes the root of `main`. The canonical development checkout retains the editable source and tests.

Current build: `dsf-20260924-r8`. Source game commit: `f599943`. Automated testing is separate from physical phone acceptance.

## Phone-play repair

- The segmented HULL rail shows remaining health and reacts to damage.
- BURN $1B purchases a 14-missile emergency homing salvo. SELL BONDS replenishes money. Ordinary missile pickups and the regular missile upgrade are removed.
- Early upgrades have roughly twice the breathing room, with shorter minimum gaps later.
- The booze system now uses the four states described below.

The original specification above is preserved unchanged. These confirmed phone-play changes supersede its earlier health, fullscreen, upgrade-cadence, and burn/missile details.

## Booze rework

- SOBER retains normal weapons and controls.
- DRUNK 1 raises damage, shot size and fire rate. Controls and vision remain normal.
- DRUNK 2 adds still more firepower and double vision. Controls remain normal.
- DRUNK 3 adds the strongest firepower, stable reversed movement and irregular vibration where supported.
- Each bottle advances one tier and refills its timer. Without another drink, intoxication steps back down through every tier to sober, removing the relevant impairment each time.
- Pete's existing portraits, explicit level labels and a sobriety timer show the current state. Held touch movement rebases safely when controls reverse or return to normal.

These confirmed booze changes supersede the original specification's intoxication details and the previous temporary booze freeze. The original specification remains unchanged for reference. Automated tests verify phone-sized touch input, fullscreen, every tier transition, native browser vibration requests, and unsupported API fallback. Actual vibration strength and touch feel still require physical phone hardware.

## Visible combat repair

Incoming ships now enter the visible battlefield before they can attack or take damage. This prevents player, escort, Imperial and explosive fire from killing enemies offscreen and leaving only drifting pickups. Opening formations are larger and more frequent, with varied lanes and staggered entry. Ordinary pickup clutter is capped. Enemy health, booze power/impairments, bottle timing, upgrade spacing and the bond/salvo economy remain unchanged.

Verified with ordinary sober phone-sized touch play, offscreen-hit regression tests and the existing phone/fullscreen/intoxication suites. The original specification remains unchanged; these confirmed repairs supersede its corresponding implementation details.
