# Current Progress

**Last updated:** 2026-11-10

## Completed (approved) milestones
- **M0 — Project foundation & documentation** — Approved 2026-11-10
- **M1 — Unity 6 URP project + Git/GitHub** — Approved 2026-11-10
  - Unity 6000.6.8f1, URP, platform = Web. `github.com/becoeurscott/talking-baby` branch `main`.
  - Note: Web Build-And-Run test deferred (use a `Builds/Web` subfolder, not project root).
- **M2 — Baby character concept + prototype model** — Approved 2026-11-10
  - Concept 2 selected; `CHARACTER_BABY_SPEC.md` written.
  - Meshy Image-to-3D (meshy-t2.5 + meshy-n1, 15k tris, T-pose) + auto-rig + walk/run anims.
  - Files under `Assets/_Project/Art/Characters/Baby/` and `Assets/_Project/Animations/Locomotion/Baby/`.
  - Meshy credits used in M2: 20 / 1,100 (resets 2026-12-10).

## Current milestone
**M3 — Rig configured as Humanoid, idle / blink / smile, touch reactions** — Status: **Not started**

## Pending tasks
- Clean up accidentally-committed Unity build output (`Data/Plugins/lib_burst_generated.*`) via `.gitignore`.
- In Unity: import baby FBX as Humanoid; drop into scene; verify auto-Avatar.
- Create Animator Controller + idle (built-in or neutral pose).
- Procedural blink + simple head-look C# script.
- Touch detection (tap body → giggle/reaction); mouse-click doubles as tap for web.
- Smile reaction (blend shape if available in the Meshy FBX; otherwise a simple animation).

## Dependencies
- Unity open. Blender NOT yet needed for M3 — only for later polish (blend shapes, eye geometry).

## GitHub
- Repository: https://github.com/becoeurscott/talking-baby (branch `main`) — not yet connected; push happens at M1 step 5.

## Open questions
- Native test phone (needed only at M9): Android, iOS, or both?

## Dependencies
- Git 2.56 installed ✅. Unity Hub / Unity / Blender not found in default locations.

## Approved requirements
- Master development instructions (strict milestone approval) — captured in `CLAUDE.md`.
- M0 documentation set and roadmap (M0–M9).
