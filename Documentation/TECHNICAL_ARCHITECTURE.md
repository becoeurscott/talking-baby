# Technical Architecture — MY LITTLE LIFE

> Status: **PROPOSED — NOT IMPLEMENTED.** Nothing here exists in a Unity project yet. Each part is built and approved milestone by milestone.

## Stack
| Component | Technology |
|---|---|
| Engine | Unity 6 LTS |
| Rendering | Universal Render Pipeline (URP) |
| Language | C# |
| 3D / rigging / animation | Blender (+ Mixamo as a body-animation starting point) |
| Facial animation | Blend shapes + procedural blink / eye tracking |
| Audio | Unity Audio Mixer |
| Local save | JSON (versioned schema) |
| Cloud save | Firebase — later, not in first playable |
| Version control | Git + GitHub |

Avoid adding technologies not needed for the current milestone.

## Module map
- **Game Core:** Life Progression, Character Needs, Interaction System, Save System, Economy (later)
- **Presentation:** Character Animator, Facial Expressions, Audio & Lip Sync, Camera & UI
- **Content (ScriptableObjects):** Baby, Toddler, Child, Teen, Adult, Family

## Unity folder structure (planned)
```
Assets/
├── _Project/
│   ├── Art/ (Characters/Baby…Adult, Environments, Materials, UI)
│   ├── Animations/ (Locomotion, Facial, Interactions, LifeStages)
│   ├── Audio/
│   ├── Prefabs/
│   ├── Scenes/
│   ├── Scripts/ (Core, Character, Progression, Interaction, Needs, Economy, Save, UI)
│   ├── ScriptableObjects/
│   └── Settings/
└── Plugins/
```

## Key principles
- **ScriptableObjects for data:** per-stage config (need decay rates, sleep needs, available interactions, animation refs, growth requirements, sounds) so new stages don't require rewrites.
- **Events for decoupling:** systems communicate via C# events, not direct references everywhere.
- **Logic vs UI separation:** UI reads state and raises requests; it doesn't own game rules.
- **Minimal `Update()`:** prefer events, coroutines, or timed ticks for needs decay.

## Animation
Animator Controller with layers (base body, face/additive, upper-body interactions). States: Idle, Happy, Sad, Crying, Talking, Eating, Sleeping, Playing.
Rules: priorities, transition conditions and **interaction locks** — no sleeping while eating, no random interruptions.

## Interaction flow (on tap)
1. Raycast / detect object or body part
2. Check character can interact (state, lock, stage)
3. Position character if needed
4. Play animation
5. Update needs
6. Play audio
7. Return to idle

## Progression (illustrative)
```csharp
public enum LifeStage { Baby, Toddler, Child, Teenager, YoungAdult, Parent, IndependentAdult }
```
Stage derived from in-game day (1–30 Baby, 31–90 Toddler, …). Internal clock independent of device clock; pausable, adjustable speed. The real system also tracks experience, attributes, milestones, relationships, money, inventory, unlocked locations, major decisions.

## Save schema (draft v1)
```json
{
  "schemaVersion": 1,
  "character": { "name": "", "lifeStage": "Baby", "currentDay": 1,
    "happiness": 0, "health": 0, "intelligence": 0, "social": 0, "energy": 0 },
  "progression": { "completedMilestones": [], "schoolUnlocked": false,
    "married": false, "hasChildren": false, "movedOut": false },
  "economy": { "coins": 0 }
}
```
Auto-save, works offline, validate on load, keep a backup copy. Never trust client currency if online purchases are added.

## Mobile performance targets (to confirm at M9)
Test early on a lower-end Android device. Watch texture sizes, mesh density, audio compression, draw calls.
