# Game Design Document — MY LITTLE LIFE

> Tagline: *A little life. A million memories.*
> Source: `project.txt` §1, 2, 5. Status: design reference (living document).

## Identity
- **Genre:** virtual companion + life simulation
- **Platforms:** Android, iOS
- **Camera:** fixed frontal third-person, character centred, medium shot, smooth zoom to face for emotional moments
- **Business model:** free-to-play, optional cosmetics/expansions; no manipulative purchases (family audience)
- **Audience:** casual players, families, life-sim fans

## Pillars
1. **Emotional connection** — players get attached to their character.
2. **Interactive entertainment** — every touch feels responsive, animated, rewarding.
3. **Life progression** — curiosity about what happens next.

The game must feel like a living animated world, not a set of menus.

## Visual direction
Rounded appealing proportions, large expressive eyes, soft skin shading (subtle SSS), quality hair/clothing, soft shadows + AO, colourful but controlled palette, exaggerated-but-believable expressions. The character keeps a consistent identity across all ages.

## Life progression (365 in-game days)
| Days | Stage | Main gameplay |
|---|---|---|
| 1–30 | Baby | Feeding, sleeping, crying, playing |
| 31–90 | Toddler | Walking, first words, exploring |
| 91–150 | Child | School, friends, learning, mini-games |
| 151–210 | Teenager | Interests, fashion, relationships, independence |
| 211–270 | Young adult | Career, income, dating, furnishing |
| 271–330 | Parent | Partner, marriage, having/naming a child |
| 331–365 | Independent adult | Moving out, new household |

Game pacing, not realistic development. Time can be paused, slept through, and accelerated; pace is adjustable. Growth between stages must be a *moment* (animation/cinematic, new proportions, clothes, interactions, environment, narrative beat).

**Generational loop:** the child becomes a parent; the player raises the next generation while seeing the original parents age.

## Baby stage (first focus)
Interactions: feed, bottle, diaper, bath, sleep, toys, tickle feet, touch cheeks, make laugh, listen to babbling.

Mood-driven reactions:
- Hungry → cries, reaches for bottle
- Happy → smiles, laughs
- Sleepy → rubs eyes, yawns
- Excited → kicks legs, waves arms

## Needs / attributes
| Attribute | Improved by |
|---|---|
| Happiness | Play, toys, social activities |
| Health | Food, hygiene, exercise, sleep |
| Intelligence | School, reading, educational games |
| Social | Talking, friendship, family |
| Energy | Sleeping, resting |

The baby depends fully on the player; autonomy grows with age.

## Autonomy
The character occasionally acts unprompted (looks at player, yawns, plays with toy, waves, reacts to sounds) — driven by needs, mood, environment and stage, never random spam.

## First environment: bedroom/nursery
Bed (sleep), bottle (feed), toys (play), mirror (expressions), wardrobe (clothes), bath (hygiene), window (look outside), TV (entertainment). Every object has a purpose.

## UI
Minimal — the character is the star. Navigation: **Home**, **Character**, **Wardrobe**, **Life**. Large touch targets, clear icons, little text.

## Sound
Three layers: character (laugh, cry, babble, breathe, eat, sleep), environment (birds, wind, TV, toys), interface (taps, rewards, unlocks, growth). Original voice identity evolving with age; pre-recorded lines first, no real-time AI conversation initially.

## Definition of first playable
See `TESTING_CHECKLIST.md` — "First Playable".
