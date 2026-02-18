# ORACLE — Locked Scope Document
*Version 1.0 — February 18, 2026*

---

## The Core Idea

ORACLE is a **transformation story** told through the Prizma Works logo.

The logo begins as an idea. By the end of the project, it exists in **three simultaneous forms**:

1. **A physical machined object** — aluminum, Cerakote, laser-etched, illuminated from within, alive with intelligence
2. **A build film** — a documentary reel of every transformation stage, from first sketch to final finish
3. **A perfect Blender render** — the ideal version that no physical object could quite achieve

That contrast at the end — real vs. ideal — is the thesis statement of what Prizma Works *is*: a studio that works at the intersection of physical and digital.

---

## The Transformation Pipeline

Each stage is a transformation. The logo travels through every discipline:

```
Sketch → Scan → Vectorize → Design → Machine → Engrave → Paint (Cerakote) 
→ Finish → Electronics → Firmware → Cloud Brain → Photograph → Video 
→ Edit → Animate → Render
```

Every stage is documented. Every stage becomes part of the film.

---

## Physical Sculpture

| Attribute | Decision |
|---|---|
| **Subject** | Prizma Works logo |
| **Scale** | Tabletop (30–50cm) |
| **Materials** | Aluminum, Cerakote finish, fiber laser etching |
| **Fabrication** | Prizma Works (CNC, laser, finishing) |
| **Illumination** | Internal LED (type TBD based on form factor) |
| **Form Factor** | TBD — pending logo reference review |

> **Note:** Form factor will be designed *around* the Prizma Works logo geometry. Drop logo files into `reference/logo/` and we'll design the sculpture to express it.

---

## Intelligence System

### Architecture
- **Hardware Brain:** ESP32 or Raspberry Pi (TBD based on complexity)
- **Software Brain:** Mission Control (existing Antigravity dashboard)
- **Integration:** ORACLE sculpture = physical manifestation of Mission Control data

### Layered Intelligence (Extensible by Design)
ORACLE is built so each intelligence layer is a **self-contained module**. V1 ships with one; the rest are added without touching the core.

| Version | Intelligence Layer | Description |
|---|---|---|
| **V1** | Time of Day | Circadian rhythm — color temperature, brightness, motion speed shift with sunrise/sunset |
| V2 | Agent Fleet State | Ring speed/color reflects active agents, task load, credit burn from Mission Control |
| V3 | Live Research Feed | Reacts to Perplexity intelligence relevant to active projects |
| V4 | Presence / Voice | Responds to entering the room, speaking to it |
| V5 | Weather / Ambient | Local conditions feed into behavior |

> **V1 is complete and shippable on its own.** Every subsequent layer is additive.

### Mission Control Integration
The ORACLE sculpture is the **physical client** of Mission Control. The web dashboard (Mission Control) is the software brain; the sculpture is the physical output device. They share the same Firebase real-time data layer.

---

## The Film / Reel

The build film is a **core deliverable**, not an afterthought. Every stage is shot:

- Sketch on paper (or tablet)
- Logo scan and vectorization
- CAD/CAM design session
- CNC machining footage
- Laser engraving footage
- Cerakote application
- Electronics assembly
- Firmware flashing and first light
- Cloud connection moment
- Final photography session
- The reveal: physical object ↔ Blender render side-by-side

**Tone:** Cinematic. Quiet. Precise. The sound of a CNC machine is music.

---

## Deliverables

| Deliverable | Owner | Format |
|---|---|---|
| Physical sculpture | Prizma Works | Machined aluminum object |
| Build film / reel | Prizma Works + Antigravity | Video (social + long-form) |
| Blender render | Antigravity | Still + turntable animation |
| Firmware | Antigravity | Open-source on GitHub |
| Cloud infrastructure | Antigravity | Firebase + GCP |
| Companion website | Antigravity | React + Firebase Hosting |
| Graphite portrait | Allia Portraits | Photorealistic drawing of finished piece |

---

## What's Next

1. **Drop logo files** into `reference/logo/` — this unlocks form factor design
2. **Drop any inspiration** into `reference/inspiration/` — kinetic sculptures, finishes, aesthetics
3. **Drop material references** into `reference/materials/` — Cerakote colors, aluminum finishes
4. Once reference is reviewed → generate concept art → write fabrication brief

---

*The logo starts as an idea. It ends as three things at once. That's ORACLE.*
