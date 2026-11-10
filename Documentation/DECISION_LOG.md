# Decision Log

| Date | Decision | Reason | Status |
|---|---|---|---|
| 2026-11-10 | Unity 6 LTS + URP as engine/renderer | Proper 3D animation, lighting, mobile optimisation; not React Native/Flutter/web | From blueprint |
| 2026-11-10 | Blender for modelling, rigging, animation; blend shapes for faces | Free, industry standard, Unity-compatible | From blueprint |
| 2026-11-10 | Pre-recorded voice lines first; no real-time AI conversation in v1 | Cost, consistency, predictability | From blueprint |
| 2026-11-10 | Polish the Baby stage fully before building other stages | Validate the core before scaling | From blueprint |
| 2026-11-10 | Original IP only; Talking Tom as quality reference only | Copyright safety | From blueprint |
| 2026-11-10 | Local JSON save first, cloud save later | Offline play, simplicity | From blueprint |
| 2026-11-10 | Strict milestone approval workflow | User's master instructions | Approved by user |
| 2026-11-10 | Web (WebGL) build is the primary test target until M9; native Android/iOS builds from M9. Daily testing in Editor Play mode. Input code treats mouse click as tap. | Test in a browser without needing a phone setup; switching platform later needs no rewrite | Approved by user |
| 2026-11-10 | Installed official `Unity-Technologies/skills` (36 skills) into `.claude/skills/` for this project only. Verified: official Unity org repo, ~1.2k stars. Did NOT install the three unverified third-party packs. | Core Unity engine expertise for the agent | Approved by user |
| 2026-11-10 | CLAUDE.md and our milestone-approval process override any skill's own workflow (e.g. `new-unity-project` runs "paved/automatic" by default — we will run it guided and one step at a time). | Keep one consistent architecture and the strict approval rule | Standing rule |
