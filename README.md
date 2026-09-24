# Pete Hegseth's Drunken Space Force

[Play the game](https://falloutmule.github.io/pete-hegseths-drunken-space-force/)

[Read the original complete game specification](PETE_HEGSETHS_DRUNKEN_SPACE_FORCE_COMPLETE_SPEC.md)

The original specification is included unchanged and remains the product reference for future edits.

A portrait arcade shooter and fictional political satire. The release is one self-contained HTML file with embedded artwork, game code, and synthesized audio.

Drag in the battlefield to fly; weapons fire automatically. A second finger can press SELL BONDS or BURN $1B. PLAY FULLSCREEN enters phone fullscreen and starts a run. Pause contains sensitivity, effects, sound, and fullscreen settings.

This repository contains the playable release. GitHub Pages publishes the root of `main`. The canonical development checkout retains the editable source and tests.

Current build: `dsf-20260924-r6`. Source game commit: `95caefd`. Automated testing is separate from physical phone acceptance.

## Phone-play repair

- The segmented HULL rail shows remaining health and reacts to damage.
- BURN $1B purchases a 14-missile emergency homing salvo. SELL BONDS replenishes money. Ordinary missile pickups and the regular missile upgrade are removed.
- Early upgrades have roughly twice the breathing room, with shorter minimum gaps later.
- Booze behavior is unchanged.

The original specification above is preserved unchanged. These confirmed phone-play changes supersede its earlier health, fullscreen, upgrade-cadence, and burn/missile details.
