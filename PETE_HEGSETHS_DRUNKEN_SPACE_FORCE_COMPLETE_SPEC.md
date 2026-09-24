# Pete Hegseth's Drunken Space Force
## Complete Game Specification

**Format:** Single-file HTML software (SFHS)  
**Primary platform:** Android phone, portrait orientation  
**Distribution / phone-test route:** GitHub Pages  
**Genre:** Endless vertical scrolling shooter with survivor-style run upgrades  
**Tone:** Political satire, pulp science fiction, arcade absurdity  
**Core control model:** Touch-drag movement with continuous autofire  
**Run structure:** Endless, escalating, score-driven, highly replayable  
**Presentation target:** Satirical caricature + pulp sci-fi + bright arcade-console readability

---

## 1. High Concept

**Pete Hegseth's Drunken Space Force** is a low-friction endless arcade shooter built around a simple contradiction:

> The more recklessly powerful Pete becomes, the harder his own ship becomes to control.

The player controls a fictionalized satirical version of Pete Hegseth, who personally pilots a heavily armed American space fighter because he considers himself the most qualified person available. The ship autofires continuously. The player moves it by touching and dragging around the screen.

The game begins as a readable, responsive top-down shooter in the lineage of classic vertical arcade shooters, then grows into a survivor-like escalation of weapons, wingmen, upgrades, political interruptions, battlefield reversals, intoxication, debt, propaganda, contradictory orders, and shifting allegiances.

The game is intentionally easy to understand and difficult to keep under control.

The central run tension is not merely survival. It is whether the player can resist increasingly tempting forms of overreach.

Booze makes Pete stronger while making movement less precise. Emergency boosts consume absurd amounts of government money. Selling bonds replenishes the money reserve but reduces score. Staying in debt too long causes the Emperor to scapegoat Pete. Allies can become enemies. Enemies can suddenly become allies. Good weapons can be replaced by inferior contractor technology. A golden Imperial flagship can enter the battle and force Pete to remain useful without visibly outperforming the Emperor.

The game should feel like a compact arcade machine whose rules are continually being rewritten by a confident authority figure who never accepts responsibility for failure.

The satire is expressed primarily through mechanics, visual presentation, event timing, and short command interruptions rather than long exposition.

---

## 2. Fiction and Satirical Framing

The game is overtly fictional satire.

Its portrayal of public figures, intoxication, military commands, money use, election-related events, alliances, contractors, and combat scenarios is exaggerated fictional comedy and is not presented as a factual account of real events or behavior.

The fictional political structure is deliberately absurd. Donald Trump appears in caricature as **the Emperor**, an arcade authority figure whose central logic is:

- he loves winners;
- he hates losers;
- his decisions are always retrospectively correct;
- success proves his leadership;
- failure proves the subordinate failed;
- when circumstances change, history changes with them.

Pete's relationship with the Emperor drives much of the game's reactive comedy.

Pete wants approval, firepower, victory, and another drink.

The Emperor wants visible winning and complete credit.

The player is trapped between those two systems.

---

## 3. Design Pillars

### 3.1 Immediate Play

The game must be understandable almost instantly.

Touch and drag to move.  
Pete shoots automatically.  
Avoid damage.  
Collect upgrades.  
Decide whether to grab booze.  
Use emergency money when necessary.

The player should be playing within seconds of loading the page.

### 3.2 Temptation Instead of Simple Punishment

The game's strongest mechanics offer real benefits paired with escalating consequences.

Booze must genuinely improve combat power.

Debt must genuinely save runs.

Aggressive upgrades must genuinely make Pete more dangerous.

The joke works because bad decisions are attractive, not because the game simply labels them bad.

### 3.3 Mechanical Satire

Most jokes should have gameplay consequences.

Examples:

- an order to reverse course reverses the scroll direction;
- a contractor mandate changes the player's actual weapon;
- selling bonds changes the actual score;
- election funding removes the player's actual emergency cash;
- scapegoating changes friendly ships into hostile attackers;
- the Emperor's arrival changes how much visible success is desirable.

### 3.4 Arcade Readability

No matter how ridiculous the run becomes, the player must retain enough readable information to make meaningful decisions.

Visual drunkenness can distort presentation, but core positional play remains understandable.

The ship responds to touch input at all intoxication levels. Drunkenness affects momentum, overshoot, recoil, aim spread, sway, and presentation rather than arbitrarily ignoring the player's input.

### 3.5 Endless Escalation

There is no conventional campaign requirement.

The ideal run becomes progressively more absurd:

- more enemies;
- more bullets;
- larger formations;
- more wingmen;
- stronger weapons;
- stranger upgrades;
- more command interruptions;
- worse debt;
- greater intoxication;
- faster reversals;
- more faction changes;
- more political interference.

The player eventually loses because the situation becomes unmanageable, not because the game reaches a scripted ending.

---

## 4. Platform and Delivery

The product is designed first for the user's Android phone.

### Primary orientation

Portrait.

### Primary interaction

Single-finger drag movement with optional secondary thumb presses for large emergency controls.

### Delivery

GitHub Pages is the normal live testing and delivery route.

The deployed page must represent the current reported build.

The game should be loadable directly from the phone without requiring the user to assemble a project, run a development server, install a package manager, or operate a desktop build chain.

### Acceptance

Phone behavior is the acceptance route.

Desktop or PC behavior may support engineering work where useful, but it does not substitute for phone acceptance and should not be reported as though it proves the user-facing result.

The final playable release should work as one HTML artifact served through GitHub Pages and should remain compatible with direct single-file distribution.

Offline operation is preferred once the artifact has been loaded or saved, subject to the actual packaging choices made during implementation.

---

## 5. Core Screen Layout

The playfield occupies almost the entire portrait screen.

The interface should feel integrated into the cockpit rather than layered on as a generic mobile game UI.

### Upper area

Contains compact persistent status information:

- score;
- current debt / negative score state;
- cash reserve measured in billions;
- Imperial Favor / patience state;
- Pete portrait;
- current intoxication presentation;
- current major weapon identity;
- wingman status.

### Central area

The battlefield.

The player ship should remain visually dominant enough to track even under heavy effects.

### Lower area

Large thumb-readable emergency controls:

**SELL BONDS**  
Converts score into emergency funds.

**BURN $1B**  
Consumes one billion dollars from reserve for an emergency propulsion burst.

These controls should remain visually readable even when the decorative UI is affected by intoxication.

The rest of the screen remains available for touch-drag movement. The implementation should prevent accidental emergency-button activation during normal ship dragging.

---

## 6. Player Ship

Pete pilots the primary ship personally.

The craft should look like a satirical excess of patriotic military design rather than a generic triangle.

Visual traits can include:

- oversized intakes;
- unnecessary fins;
- chrome;
- patriotic markings;
- aggressive nose art;
- too many hardpoints;
- conspicuous exhaust;
- oversized insignia;
- visible upgrades bolted onto the hull;
- visual damage and soot as the run deteriorates.

The ship must have a strong silhouette readable on a phone.

### Movement

The player touches and drags.

The ship follows the intended motion with a handling model influenced by intoxication and temporary effects.

The ship should not require a virtual joystick unless testing proves that direct drag is inferior.

At low intoxication the craft feels tight and precise.

At higher intoxication the craft can develop:

- inertia;
- overshoot;
- lateral drift;
- recoil displacement;
- delayed settling;
- slight oscillation;
- exaggerated banking;
- imprecise weapon alignment.

The ship remains controllable throughout.

---

## 7. Autofire Combat

Pete fires continuously whenever gameplay is active.

There is no normal fire button.

Autofire keeps the player's attention on:

- movement;
- positioning;
- pickups;
- debt;
- booze;
- upgrades;
- Emperor events;
- faction identity;
- emergency decisions.

Weapons can still vary dramatically in behavior.

Possible weapon families include:

- machine cannons;
- spread cannons;
- rockets;
- missiles;
- beam weapons;
- flak;
- chain lightning;
- drone weapons;
- side guns;
- rear guns;
- orbital strikes;
- wingman-linked fire;
- unstable contractor weapons.

Weapons should become visually satisfying and excessive as the run develops.

---

## 8. Booze System

Booze is the game's central risk-reward pickup.

It should always remain tempting.

The system should not have a state where sobriety is obviously correct in all situations or where drinking is simply mandatory.

### Benefits

Increasing intoxication may provide combinations of:

- increased fire rate;
- extra projectiles;
- larger projectile size;
- increased damage;
- wider spread;
- stronger explosives;
- stronger recoil-based attacks;
- more aggressive wingman behavior;
- faster special effects;
- temporary armor;
- score multipliers;
- pickup attraction;
- unusual weapon mutations.

### Costs

Increasing intoxication can produce:

- increased ship momentum;
- overshoot;
- recoil movement;
- wider firing spread;
- slight positional sway;
- more difficult precision movement;
- blurred secondary UI;
- ghosted text;
- double vision;
- slight screen banking;
- color fringing;
- portrait deterioration.

### Recovery

Intoxication gradually declines over time.

The player can return toward greater precision without requiring a separate sobriety mechanic.

This creates a recurring temptation loop:

1. Pete becomes stable.
2. Combat pressure rises.
3. Booze appears.
4. The player knows it will solve the immediate firepower problem.
5. The player takes it.
6. The battlefield becomes easier to destroy and harder to navigate.
7. The effects gradually recede.
8. Another opportunity appears.

### Presentation

The game should avoid relying entirely on a literal BAC meter.

Pete's portrait, weapon effects, handling, and HUD distortion should communicate the state naturally.

A compact readiness indicator may exist if needed, but the character and game feel should do most of the work.

---

## 9. Pete Portrait

Pete's cockpit portrait is one of the game's primary storytelling systems.

It appears as a live portrait rather than a distant commander.

The portrait should visibly deteriorate with the run.

Possible visual states include:

### Mission Ready

- immaculate hair;
- rigid posture;
- confident expression;
- pristine headset;
- formal uniform presentation.

### Extra Ready

- loosened posture;
- broad grin;
- slightly crooked headset;
- more animated reactions.

### Extremely Ready

- rumpled clothing;
- flushed or exaggerated comic expression;
- headset slipping;
- messy hair;
- drink entering frame.

### Personally Handling It

- enthusiastic, disheveled confidence;
- crooked gear;
- drink or bottle present;
- exaggerated thumbs-up or shouting;
- complete visual certainty despite battlefield collapse.

The portrait should react to:

- upgrades;
- booze pickups;
- large kills;
- debt;
- Emperor praise;
- Emperor criticism;
- wingman betrayal;
- emergency money burns;
- near death;
- the Emperor's arrival.

The portrait should be expressive enough to create comedy without dialogue-heavy scenes.

---

## 10. Score, Money, Bonds, and Debt

Score represents performance and political standing while also serving as a resource base.

### Positive Score

The player is visibly winning.

Imperial Favor is easier to maintain.

Pete receives praise.

The player can sell some of this accumulated success for emergency funding.

### Sell Bonds

The player may press **SELL BONDS** to obtain emergency cash.

A bond sale:

- adds money to the emergency reserve;
- immediately lowers score;
- can push the score below zero;
- creates a real tradeoff between survival and final result.

The transaction should be immediate and visible.

A short satirical receipt or banner may appear.

### Emergency Reserve

Money is measured in absurdly large units, typically billions.

The reserve powers emergency systems.

The baseline emergency action costs:

**$1,000,000,000**

### Negative Score

The game allows the score to fall below zero.

Debt is not immediate failure.

Instead it creates political danger.

The player can continue borrowing and fighting while attempting to recover.

---

## 11. Emergency Money Burn

The **BURN $1B** button is Pete's panic button.

It consumes one billion dollars from the emergency reserve.

The burn should feel extremely powerful and extremely wasteful.

Possible effects:

- violent forward or directional thrust;
- brief damage immunity;
- projectile clearing;
- collision escape;
- huge exhaust plume;
- money / bond / document particles;
- dramatic camera shake;
- loud engine surge;
- large spending notification.

The move exists primarily as a reliable emergency escape.

It should remain useful even when Pete is heavily intoxicated.

A short recovery interval prevents a large reserve from becoming permanent invulnerability.

The comedy comes from using a billion dollars to solve a problem created several seconds earlier by grabbing another bottle.

---

## 12. Imperial Favor and Scapegoating

The Emperor loves visible winners and rejects visible losers.

Imperial Favor should behave as a dynamic political pressure system rather than a morality meter.

### Favor Rises When

Pete is performing visibly well.

Examples can include:

- sustained positive score growth;
- strong enemy destruction;
- surviving Emperor events;
- supporting the Emperor during his personal appearance;
- recovering from debt;
- maintaining momentum.

### Favor Falls When

Pete appears unsuccessful or inconvenient.

Examples can include:

- prolonged negative score;
- obvious battlefield failure;
- embarrassing the Emperor;
- excessive debt;
- performing badly while the Emperor is present;
- performing too well while the Emperor wants the credit.

### Debt Patience

When score remains negative for too long, Imperial Patience drains.

If the player recovers above zero, patience can gradually recover.

Briefly crossing zero should not completely erase the history of a serious debt spiral.

### Scapegoat State

When patience is exhausted:

**SCAPEGOAT DESIGNATED**

Pete's own forces begin attacking him.

Friendly insignia remain recognizable.

The message is not that the allies changed sides. The message is that Pete has been declared the problem.

Scapegoat status is reversible.

If Pete claws his way back to visible success, the Emperor can abruptly restore him to favor and behave as though the rejection never happened.

This reversal is central to the joke.

---

## 13. Wingman System

Pete normally has a simple endless wingman.

The wingman creates attachment and gives later betrayal mechanics weight.

The baseline wingman:

- follows Pete loosely;
- shoots automatically;
- can be damaged or temporarily destroyed;
- returns after an appropriate delay;
- may receive upgrades;
- has a recognizable silhouette;
- is readable as Pete's ally without requiring text.

The wingman does not require deep AI.

It should be dependable, simple, and useful.

Survivor-style upgrades may add:

- additional wingmen;
- heavier wingman weapons;
- defensive wingmen;
- missile wingmen;
- repair / shield support;
- aggressive formations;
- risky drunken wingman behavior.

An Emperor event can later designate Pete's own wingman or allied formation as hostile.

That betrayal should be visually clear and mechanically immediate.

---

## 14. Factions

The battlefield contains multiple exaggerated space factions.

Faction identity should be communicated through:

- ship silhouettes;
- insignia;
- projectile styles;
- formation behavior;
- palette;
- animation language.

They should not be represented as abstract geometry alone.

### 14.1 Plutonians

The Plutonians are the primary recurring enemy faction.

Their running grievance is that Pluto was declared not to be a planet.

This is treated as a ridiculous civilization-scale resentment.

Visual direction:

- icy;
- cratered;
- jagged;
- violet / blue / black;
- cold propulsion;
- dwarf-planet imagery;
- compact hostile craft;
- enormous chip-on-the-shoulder energy.

Their designs can mix planetary geology with angry retro spacecraft.

Plutonian enemy families can include:

- scouts;
- interceptors;
- bombers;
- turret barges;
- asteroid carriers;
- mine layers;
- elite revenge ships;
- boss-scale planetary grievance machines.

### 14.2 China-Themed Allied Fleet

A fictionalized arcade space ally inspired by recognizable Chinese state/military visual language without attempting simulation.

It should have its own:

- silhouettes;
- insignia;
- formation style;
- weapons;
- ally color language.

### 14.3 EU-Themed Allied Fleet

A stylized European bloc fleet with clean, organized visual identity and recognizable celestial / ring motifs.

### 14.4 NATO-Themed Allied Fleet

A stylized allied defense fleet with a more conventional military-space appearance and strong alliance insignia.

### Faction Fluidity

The political relationship of any faction can change during the run.

The game should support:

- ally becoming enemy;
- enemy becoming ally;
- temporary neutrality;
- sudden retargeting;
- Emperor denial that the previous relationship ever existed.

Faction changes must be clearly announced and visually communicated before hostile fire creates unavoidable damage.

---

## 15. Emperor Command System

The Emperor periodically interrupts the run.

These events are one of the game's defining systems.

They should be brief, forceful, mechanically consequential, and easy to understand.

The Emperor appears with a large portrait, command banner, voice-like text treatment, or other theatrical interruption.

The battlefield may briefly slow enough for the player to understand the new rule.

Then play continues.

The Emperor's orders are not merely jokes. They rewrite active gameplay.

### Command 1: Normal Imperial Commentary

The Emperor praises winning and distances himself from losing.

Examples of tone:

- Pete is great because the Emperor selected him.
- Pete has always been questionable once performance drops.
- a successful reversal was always the plan.
- a failed reversal was Pete's misunderstanding.
- restored success immediately restores historical loyalty.

These lines should be concise and reactive.

### Command 2: Turn on Your Allies

An allied group, including potentially Pete's wingman, is redesignated hostile.

Targeting indicators change.

The affected ships visibly turn before attacking.

The event can later reverse.

The player should always be able to understand who is currently hostile.

### Command 3: Emergency — Buy the Election

The Emperor announces an urgent political funding need.

The event confiscates Pete's available emergency cash reserve.

It does not independently subtract score again.

The consequence is that Pete suddenly loses the safety buffer he expected to use for emergency burns.

The event is especially effective when triggered after the player has become intoxicated or accumulated substantial cash.

### Command 4: Mind Change — Reverse Course

The Emperor orders the mission to reverse direction.

The scroll:

1. slows;
2. stops;
3. reverses.

Pete's craft turns to face the new direction.

The battlefield's spatial logic changes.

Enemies that were behind the player may become relevant.

The input mapping remains intuitive: dragging in a direction still moves Pete in that direction.

The Emperor may trigger this because:

- Pete is deeply in debt;
- Pete is winning too quickly;
- the current mission has become politically inconvenient;
- pure randomness would create a good moment.

The reversal should feel like a real mechanical event, not a camera trick.

### Command 5: Mandatory Private Contractor Technology

The Emperor orders Pete to replace his current weapon with equipment from a favored private contractor.

The replacement should look expensive and impressive while performing in entertainingly compromised ways.

Possible contractor weapons include:

- missile system with excessive lock-on delay;
- giant cannon with bad accuracy;
- beam weapon that overheats immediately;
- smart missiles with questionable target selection;
- beautifully animated gun with poor sustained damage;
- absurd recoil weapon;
- weapon that requires repeated reboot cycles;
- expensive defensive field with inconsistent uptime.

The event is funniest when the player had a strong, reliable build immediately beforehand.

Booze and normal upgrades can still interact with contractor weapons.

The game should not make the event an automatic death sentence. The player is forced to adapt.

### Command 6: The Emperor Joins the Battle

The Emperor personally arrives in an enormous golden ship.

This is a temporary special mode.

The entrance should be one of the game's biggest visual moments.

The golden craft should be:

- excessive;
- polished;
- unmistakable;
- theatrical;
- much larger than Pete's ship;
- equipped with spectacular weapon effects.

The Emperor's ship is effectively protected from ordinary failure.

During this event Pete must remain useful without visibly making the Emperor look bad.

The success window becomes deliberately awkward:

- perform too poorly and Pete looks incompetent;
- outperform the Emperor too visibly and Pete steals the spotlight;
- support the Emperor effectively and Imperial Favor rises.

The Emperor may steal kills, claim destruction he did not cause, block lines of fire, or deliver exaggerated finishing attacks.

The event should change scoring/favor incentives temporarily without requiring a separate game mode or map.

---

## 16. Survivor-Style Upgrade System

The game uses run-based upgrade choices similar to survivor games.

Upgrades should appear periodically based on accumulated combat progress.

The upgrade presentation must be fast enough not to destroy arcade rhythm.

A brief pause, slow-motion state, or compact choice overlay can work.

Upgrade choices should meaningfully alter the current run.

### Weapon Growth

Examples:

- additional forward guns;
- side cannons;
- rear coverage;
- spread;
- piercing;
- explosive rounds;
- missile racks;
- chain effects;
- beam amplification;
- projectile size;
- fire rate;
- critical bursts;
- orbital support.

### Wingman Growth

Examples:

- additional wingman;
- heavier wingman weapon;
- synchronized fire;
- defensive intercept;
- missile support;
- rotating escort;
- temporary replacement after destruction.

### Ship Growth

Examples:

- increased armor;
- improved handling;
- reduced recoil;
- faster acceleration;
- improved pickup attraction;
- improved emergency recovery;
- better shield behavior.

### Financial Growth

Examples:

- more reserve capacity;
- better bond conversion;
- larger score recovery bonuses;
- reduced emergency burn recovery interval;
- reward for surviving while in debt.

### Booze Growth

Examples:

- increased power gained per intoxication tier;
- slower intoxication decay with stronger bonuses;
- better handling while intoxicated;
- stronger drunk-only projectile mutations;
- increased pickup attraction when intoxicated;
- temporary shield after drinking.

### Risk Growth

Some upgrades can deliberately encourage unstable builds:

- enormous damage with major recoil;
- high score multiplier while heavily intoxicated;
- stronger weapons while negative;
- Imperial Favor bonuses for reckless proximity;
- more aggressive but less controllable wingmen;
- faster upgrade gain in exchange for more frequent Emperor interruptions.

The upgrade pool should support both disciplined precision runs and spectacular self-destructive escalation.

---

## 17. Enemy Design

Enemies should be visually expressive and behaviorally simple enough to support many simultaneous objects.

The game benefits more from combinations of clear enemy behaviors than from complicated individual AI.

Useful behavior families include:

### Straight Attackers

Enter in formation and fire predictable patterns.

### Swoopers

Dive toward Pete and curve away.

### Turret Barges

Slow-moving platforms that create area denial.

### Bombers

Cross the screen and release mines or explosive hazards.

### Pursuers

Track Pete more aggressively.

### Snipers

Telegraph long-range shots.

### Carriers

Spawn smaller craft.

### Shield Ships

Protect nearby enemies.

### Financial / Propaganda Hazards

Special enemies or objects can interfere with score, pickups, favor, or targeting without requiring separate combat rules.

### Elite Variants

Enemies can gain:

- armor;
- extra fire;
- altered movement;
- shields;
- escort formations;
- faction-specific effects.

The system should support endless scaling through spawn rate, formation complexity, projectile density, elite frequency, and event overlap.

---

## 18. Boss and Large-Ship Encounters

The game can include boss-scale encounters without abandoning endless structure.

Large enemies should appear as events within the run rather than level endpoints.

Possible encounters:

- Plutonian revenge dreadnought;
- asteroid fortress;
- massive propaganda satellite;
- orbital weapons platform;
- rogue allied carrier after a faction reversal;
- contractor demonstration ship;
- golden Imperial ceremonial target.

Bosses should be visually memorable and mechanically legible.

The game does not require elaborate multi-minute bullet-hell scripting for every boss. Strong silhouettes, a few clear patterns, destructible sections, and interaction with the existing event systems are enough to create spectacle.

---

## 19. Damage, Health, and Death

Pete needs enough survivability for escalation to develop.

A run should not end from one minor collision.

Possible health presentation:

- armor segments;
- shields;
- hull integrity;
- visible ship damage;
- portrait reaction.

Damage should create urgency without turning the UI into an RPG dashboard.

### Death

When Pete dies, the game stops and produces a satirical result screen.

The Emperor's messaging preserves his own victory while attributing failure elsewhere.

The result screen can include:

- final score;
- highest positive score;
- deepest debt;
- money burned;
- bonds sold;
- maximum intoxication;
- enemies destroyed;
- allies destroyed;
- wingmen lost;
- contractor systems endured;
- number of reversals;
- number of faction changes;
- time survived;
- Emperor appearances;
- highest weapon state.

The player should be able to restart quickly.

---

## 20. Difficulty Scaling

Difficulty should increase continuously but not simply by multiplying enemy health.

The run should become more complicated through:

- denser enemy formations;
- additional projectile patterns;
- more elite enemies;
- more simultaneous factions;
- faster event cadence;
- larger ships;
- more frequent alliance changes;
- increasing pressure to use booze;
- stronger temptation to borrow;
- greater consequences for unstable builds.

The game should preserve the possibility of skillful sober play while making reckless escalation increasingly tempting.

The player should feel that collapse resulted from a web of choices and circumstances rather than an invisible timer deciding the run was over.

---

## 21. Event Interaction Philosophy

The most memorable runs will come from systems colliding.

The game should deliberately support combinations such as:

- Pete drinks heavily;
- the Emperor confiscates the emergency reserve;
- a reverse-course order arrives;
- Pete sells bonds to regain cash;
- the debt timer begins;
- a contractor weapon replaces Pete's reliable gun;
- the wingman is designated hostile;
- Pete falls negative;
- scapegoat mode begins;
- the Emperor arrives personally;
- Pete suddenly has to perform well enough to survive but not well enough to steal credit.

These interactions are the game's procedural comedy engine.

The architecture should allow systems to combine rather than scripting every joke as a one-off sequence.

---

## 22. Art Direction

The visual identity should feel like:

**satirical illustrated caricature + lurid pulp science fiction + polished arcade-console readability.**

The desired energy can evoke the irreverence of classic magazine satire, the intensity of adult pulp sci-fi illustration, and the clarity and toy-like appeal of high-quality console arcade art without copying a specific publication, artist, franchise, or game.

### Character Art

- strong caricature;
- exaggerated facial expressions;
- bold silhouettes;
- painted comic shading;
- highly readable at small size;
- expressive eyes and mouth;
- visible deterioration across intoxication states;
- intentionally theatrical posing.

### Spacecraft

Ships should look designed rather than symbolic.

They should have:

- coherent silhouettes;
- recognizable faction identity;
- exaggerated engineering;
- readable weapon mounts;
- strong front/back directionality;
- satisfying damage and firing effects;
- visual personality.

### Pete's Ship

Patriotic excess.

### Emperor's Ship

Golden imperial excess.

### Plutonians

Cold, jagged, resentful planetary machinery.

### Allies

Distinct, recognizable fleets with their own shape language and insignia.

### Effects

Combat should feel juicy and arcade-like:

- muzzle flashes;
- recoil;
- smoke;
- sparks;
- projectile trails;
- explosions;
- shield effects;
- debris;
- money burn exhaust;
- screen shake;
- impact flashes;
- controlled bloom / glow where practical.

### Background

The background can evolve procedurally through:

- starfields;
- nebulae;
- planetary limbs;
- satellites;
- debris;
- orbital infrastructure;
- propaganda signage;
- distant fleet traffic;
- parallax layers.

The environment should suggest a large absurd war without requiring a large authored world.

---

## 23. Drunken Visual Effects

Intoxication affects the visual presentation progressively.

Useful effects include:

- mild UI ghosting;
- duplicate text offsets;
- lens-like blur on decorative HUD elements;
- slight chromatic separation;
- screen sway;
- portrait instability;
- subtle starfield smear;
- exaggerated projectile trails;
- temporary focus pulses;
- slight perspective wobble.

Core gameplay information remains legible.

The player ship, dangerous projectiles, major pickups, emergency controls, and faction hostility cues must remain readable enough for skillful play.

The effect should make the player feel compromised, not cheated.

---

## 24. UI Tone and Copy

The interface combines:

- military instrumentation;
- propaganda graphics;
- tabloid bombast;
- arcade score presentation;
- bureaucratic financial language.

Possible recurring labels include:

- COMBAT READINESS;
- IMPERIAL FAVOR;
- STRATEGIC RESERVE;
- SELL BONDS;
- BURN $1B;
- CONTRACTOR UPGRADE;
- SCAPEGOAT DESIGNATED;
- MISSION PRIORITIES UPDATED;
- ALLIANCE STATUS CORRECTED;
- STRATEGIC REALIGNMENT;
- IMPERIAL VICTORY.

The UI can confidently rename obvious disasters as successes.

Text should be short enough to read during active play.

---

## 25. Audio Direction

Audio should reinforce the pulp arcade identity.

### Music

Fast, aggressive, comic militaristic space-rock / synth energy.

The soundtrack can intensify with:

- intoxication;
- high enemy density;
- Emperor appearance;
- scapegoat state;
- boss encounters.

### Sound Effects

Important sounds include:

- autofire;
- pickups;
- booze collection;
- bond sale;
- money burn;
- warning banners;
- faction switch;
- wingman destruction;
- contractor malfunction;
- Emperor arrival;
- explosions;
- score gain;
- favor changes.

The emergency $1B burn should have one of the loudest and most satisfying sounds in the game.

Audio should be designed for phone speakers while remaining pleasant through headphones.

A mute control should be immediately available and remembered locally.

---

## 26. Input and Mobile Feel

Touch is the primary control system.

The game should feel designed for a phone rather than adapted from keyboard controls.

### Movement

Direct drag should be explored as the primary scheme.

The ship can follow the finger with a configurable vertical offset so the player's finger does not completely cover the ship.

Movement should remain stable during multitouch use.

### Emergency Controls

The player should be able to drag with one finger and press an emergency button with another where supported.

Touch cancellation, leaving the browser bounds, interruptions, and resumed input should recover cleanly.

The screen should avoid browser gestures interfering with gameplay where appropriate and standards-compliant.

---

## 27. Pause and Resume

The game should handle ordinary mobile interruptions gracefully.

Possible pause conditions:

- app loses focus;
- tab becomes hidden;
- browser interrupts input;
- device locks;
- pause button is pressed.

Returning to the game should not cause Pete to jump, continue stale movement, or immediately die because old input remained active.

A short resume countdown or safe resume state can be used if it improves phone behavior.

---

## 28. Persistence

Local persistence should be lightweight.

Useful saved data:

- high score;
- best survival time;
- lifetime statistics;
- sound preference;
- control preference if alternatives are eventually added;
- discovered upgrade entries;
- optional cosmetic unlocks;
- satire/event history if used.

The game does not need account infrastructure for the core product.

---

## 29. Replayability

Replayability comes from interacting systems rather than content volume alone.

Each run can differ through:

- upgrade draws;
- booze timing;
- event timing;
- faction changes;
- debt decisions;
- weapon combinations;
- contractor interruptions;
- Emperor appearances;
- wingman growth;
- enemy formations;
- boss encounters.

The ideal game creates stories the player wants to describe afterward.

Example:

> “I was completely hammered with six wingmen and a beam cannon, then the Emperor confiscated my reserve, reversed the war, declared NATO hostile, forced me onto a broken contractor missile system, and showed up in the gold ship while I was $8 billion underwater.”

That emergent run story is the product.

---

## 30. Technical Direction

This is SFHS: Single-File HTML Software.

The final playable product should be distributed as one HTML artifact.

Construction method is open.

The implementation can use whatever approach best serves the game, including:

- Canvas 2D;
- PixiJS;
- WebGL;
- DOM/CSS for interface;
- embedded generated assets;
- compact runtime modules during development;
- reusable SFHS infrastructure;
- another suitable browser-game technology.

The implementation should choose tools based on actual product benefit.

A mature rendering library is appropriate if it reduces burden for:

- sprite batching;
- particles;
- effects;
- asset organization;
- scaling;
- mobile rendering;
- animation.

The game architecture should remain understandable and proportional to the product.

The development source may be modular even though the released artifact is one HTML file.

Useful internal separations can include:

- game state;
- run director;
- renderer;
- controls;
- entities;
- factions;
- weapons;
- upgrades;
- Emperor events;
- finance/debt system;
- intoxication system;
- audio;
- UI;
- persistence;
- asset registry;
- build/pack path.

These separations should support the game rather than becoming a framework project of their own.

Reusable SFHS fixes discovered during development can be isolated into shared infrastructure when they genuinely belong there, while game-specific mechanics remain in the game.

---

## 31. Art Asset Strategy

The project should use actual illustrated assets rather than relying on abstract primitives as the finished visual language.

The art pipeline can mix:

- generated concept art;
- hand-tuned raster sprites;
- vector UI;
- procedural effects;
- layered portrait components;
- sprite sheets;
- embedded image assets.

Portrait assets should support multiple intoxication and reaction states.

Ship assets should support:

- faction recognition;
- damage states where valuable;
- muzzle locations;
- animation;
- readable scaling.

The single-file pack process should embed the assets into the final artifact.

Art should be judged on the phone at actual gameplay size.

---

## 32. Performance Direction

The game should remain smooth on the target Android phone during dense late-run conditions.

The implementation should be prepared for:

- many projectiles;
- many enemies;
- particles;
- parallax;
- portrait animation;
- UI effects;
- faction changes;
- screen effects;
- simultaneous event logic.

Performance work should focus on actual measured bottlenecks.

Entity pooling, sprite batching, reduced overdraw, simplified collision checks, or other techniques can be used where evidence shows they help.

The late game should feel intentionally chaotic rather than accidentally sluggish.

---

## 33. Collision and Combat Rules

Collision rules should be consistent and readable.

Possible interactions:

- player projectiles damage current hostiles;
- hostile projectiles damage Pete;
- ally fire does not damage Pete unless the alliance state changes;
- wingmen can be targeted when made hostile;
- faction transitions include a safe telegraph window;
- emergency burn can clear or ignore immediate collision hazards;
- shields absorb damage visibly;
- explosions have clear effective areas.

Autofire should not punish the player for a faction swap before the game has communicated the new relationship.

---

## 34. Run Director

A run director should coordinate escalation without hard scripting every second.

It can consider:

- elapsed run time;
- current score;
- debt;
- intoxication;
- weapon power;
- number of wingmen;
- recent damage;
- recent Emperor event;
- current faction relationships;
- current enemy pressure;
- Imperial Favor.

The director can use this information to choose:

- enemy formations;
- pickup opportunities;
- booze temptation;
- upgrade timing;
- major events;
- Emperor commands;
- boss appearances.

The director should produce interesting pressure and comedy without feeling like it is simply countering every strong player choice.

---

## 35. Political Event Timing

Emperor interruptions should be memorable enough to matter and spaced enough that normal shooter play can breathe.

The cadence can accelerate later in the run.

The system should avoid stacking so many rule changes at once that the player cannot identify what happened.

However, late-run overlaps are desirable once the player has had time to learn the systems.

The game can intentionally allow chaotic combinations after clear individual mechanics have been established within the run.

---

## 36. Opening

The opening should be extremely short.

A title treatment introduces the game.

Pete's portrait appears.

A line establishes that the mission requires the best available pilot and Pete has selected himself.

The game begins immediately.

The player should not have to watch a long intro on repeat runs.

---

## 37. Tutorialization

The game should teach primarily through play and contextual prompts.

Examples:

- first drag prompt;
- first booze pickup explanation;
- first SELL BONDS explanation;
- first BURN $1B explanation;
- first Emperor command explanation;
- first upgrade selection.

Prompts should disappear once understood.

Repeat runs should start quickly.

---

## 38. End-of-Run Presentation

The death screen is part of the satire.

The Emperor always frames the overall outcome as his success.

Pete's result is evaluated separately through the numbers.

The screen should provide both comedy and useful run feedback.

It should encourage immediate replay.

A large **TRY AGAIN** control returns directly to play.

The game can preserve high-score and notable-run records locally.

---

## 39. Optional Long-Term Expansion Space

The core design naturally supports future content without requiring the initial architecture to predict every expansion.

Potential additions include:

- additional space factions;
- more ally blocs;
- more contractor weapons;
- more Emperor commands;
- additional wingman personalities;
- bosses;
- more portrait states;
- alternate Pete ships;
- cosmetic propaganda themes;
- challenge modifiers;
- local daily seeds;
- achievements;
- additional financial absurdities;
- more political command contradictions;
- special event chains;
- unlockable historical run statistics.

These possibilities should remain additive to the core loop rather than becoming prerequisites for initial playability.

---

## 40. Quality Standard

The game should feel like a finished arcade object, not a technology demo.

A successful release has:

- satisfying touch movement;
- strong autofire feedback;
- readable enemy and faction design;
- compelling booze risk/reward;
- meaningful survivor-style upgrades;
- useful wingmen;
- functional bond/debt economy;
- satisfying emergency money burn;
- clear Imperial Favor behavior;
- reversible scapegoat state;
- mechanically real Emperor commands;
- a memorable golden-ship appearance;
- coherent art direction;
- stable phone performance;
- clear portrait-mode presentation;
- replayable endless escalation;
- a current GitHub Pages build ready for phone use;
- a single-file HTML artifact representing the same game.

---

## 41. Development and Delivery Authority

Codex should treat this as one continuous bounded product task.

The expected flow is continuous through:

- implementation;
- integration;
- art and asset work;
- gameplay tuning;
- testing;
- repair;
- packaging;
- deployment to the authorized GitHub Pages route;
- verification of the deployed result;
- delivery of the current phone-playable build.

The project should not stop after producing a plan, scaffold, architecture document, partial prototype, or disconnected development package.

The implementation is free to make reasonable product decisions within this specification when evidence from actual play shows a better solution.

The product repository is authoritative for game mechanics, assets, behavior, and acceptance.

Shared SFHS infrastructure may be used or repaired where it clearly helps, while Pete-specific mechanics and content remain in the product.

Testing should focus on the real product and the real phone experience.

The live GitHub Pages result and single-file artifact should stay aligned with the code being reported.

---

## 42. Final Product Identity

The intended finished experience is:

> A frantic portrait-mode arcade shooter where a fictionalized Pete Hegseth personally pilots an absurdly armed space fighter, automatically firing into an endless war while the player drags him through waves of Plutonians, shifting allies, survivor-style upgrades, booze-powered combat escalation, debt-financed emergency thrust, Imperial scapegoating, contractor sabotage, battlefield reversals, and the occasional arrival of an enormous golden Emperor ship that Pete must help without overshadowing.

The player is always trying to survive one more wave.

The game is always offering one more bad idea that might actually work.

That is the loop.
