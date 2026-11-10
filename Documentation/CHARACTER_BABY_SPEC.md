# Baby Character Specification (v1)

> Status: **concept approved look pending user sign-off.** Reference image: `Assets/_Project/Art/Characters/Baby/concept_baby_v1_PROTOTYPE.png` (PROTOTYPE, 2D concept — not the game model).
> Original character. Talking Tom is a quality reference only; nothing here derives from it.

## Chosen look (concept 2)
- Chubby, wholesome infant; warm and friendly.
- **Head:** very large relative to body (classic cute proportions), round, soft cheeks with rosy blush.
- **Eyes:** large, warm brown, round, bright catchlights — the key expressive feature; must read as "looking at the player."
- **Hair:** short, soft light-brown, small tuft on top.
- **Mouth:** small, open happy smile with lower lip and a hint of tongue.
- **Skin:** soft, smooth, subtle subsurface warmth at ears/cheeks/hands.
- **Outfit:** plain mint-green onesie (long sleeves, footless), barefoot.
- **Build:** soft rounded limbs, small hands/feet, no sharp edges.

## Proportions (targets for the modeller)
- Head ≈ 1/2.2 of total height (large-head cartoon baby).
- Eyes large and set fairly wide; iris fills most of the visible eye.
- Short limbs, round belly, stubby fingers/toes (modelled but simplified).

## Palette (reference)
| Part | Colour (approx) |
|---|---|
| Skin | warm light peach |
| Cheeks | soft rosy pink |
| Hair | light warm brown |
| Eyes (iris) | medium warm brown |
| Onesie | soft mint green |

## Customisation (FUTURE — not v1)
Player customisation (skin tone, hair, eye colour, onesie colour) is a planned later-version feature. Build the v1 model and materials so colours live on swappable materials/textures to make this easier later, but do **not** build the customisation UI or system in the first version.

## 3D modelling requirements (for phase 2)
- **Topology:** clean quad-dominant mesh; edge loops around eyes and mouth for deformation; even loops on limbs for bending. Keep polycount mobile-friendly (target a few thousand tris for the baby; confirm at optimisation).
- **Separate parts where helpful:** eyes as spheres (for rotation/eye tracking), eyelids able to close, mouth cavity, teeth/tongue simple.
- **Scale/orientation:** real-world-ish scale, facing +Z, Y up, origin at feet — so Unity import is predictable.
- **UVs:** non-overlapping, one main texture set for skin + one for outfit (supports future recolour).

## Rig requirements
- Humanoid-friendly skeleton (so Unity Humanoid + Mixamo retargeting can work): hips, spine, neck, head, shoulders, arms, hands (simple), legs, feet.
- Extra bones/controls for head and eyes (eye aim) if not done purely by blend shapes.

## Facial blend shapes (minimum set for the first playable)
Eyes: BlinkL, BlinkR (or combined Blink), EyeWide, look handled by eye bones/UV.
Brows: BrowUp, BrowDown/Frown.
Mouth: Smile, MouthOpen, Frown/Cry, Pout.
Cheeks: CheekRaise (for genuine smile/laugh).
These drive the required reactions: smile, laugh, cry, surprise, sleepy (droopy lids + slight frown).

## Open decision for phase 2
How to produce the model: (a) AI 3D generation + cleanup, (b) hand-model in Blender, (c) license a base baby model and restyle. Requires Blender installed.
