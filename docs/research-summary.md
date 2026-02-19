# ORACLE — Research Summary
*Phase 0 Research — February 18, 2026*

---

## Kinetic Sculpture Precedents

### Best-in-Class References

**Swinging Sticks® (INFINITY / PRESTIGE)**
- Perfectly balanced anodized aluminum double pendulums
- Electromagnetic impulse drive — nearly silent, perpetual-seeming motion
- Individual rods hand-tuned for maximum smoothness
- **Lesson for ORACLE:** Electromagnetic drive is cleaner than motors for desk objects. Balance and silence matter as much as motion.

**Hypnotiq Hypnoloid**
- CNC-machined aerospace aluminum, anodized finish
- Pure geometry — the Oloid shape creates hypnotic motion with no electronics
- 40mm diameter, 117g — proves small can be powerful
- **Lesson for ORACLE:** The geometry *is* the mechanism. Design the form so the motion is inherent.

**Kyle's Kinetics**
- Handcrafted metalwork, $140–$6,500 range
- Proves the market exists for premium handmade kinetic desk art
- **Lesson for ORACLE:** Handcrafted + precision machined = premium positioning

### Gap in the Market
No current mainstream kinetic desk sculpture integrates:
- LED illumination as a primary feature
- Cloud/AI intelligence
- A brand narrative this specific

**ORACLE has no direct competition.**

---

## Electronics Stack (Recommended)

### Microcontroller: ESP32
- WiFi + Bluetooth built-in
- Sufficient GPIO for LED control + motor control + sensors
- WLED firmware runs natively
- Large maker community, excellent documentation
- **Cost:** ~$10–15 for dev board

### LED System: WLED + RGBCCT Strip
- **WLED firmware** (open source) handles circadian CCT natively in v0.15+
- **RGBCCT strips** (e.g., WS2805) allow true Kelvin color temperature control
- Time-of-day schedule: 6500K cool morning → 2700K warm evening
- NTP time sync over WiFi — no RTC needed
- **V1 is essentially WLED + a schedule.** Extremely achievable.

### Circadian Rhythm Algorithm (V1)
```
6:00 AM  → 3000K (warm sunrise)
9:00 AM  → 5500K (cool daylight)
12:00 PM → 6500K (peak cool)
3:00 PM  → 5000K (afternoon)
6:00 PM  → 3500K (golden hour)
9:00 PM  → 2700K (warm evening)
11:00 PM → 1800K (candlelight, dim)
```
Smooth interpolation between points. WLED handles this natively.

### Motor (for kinetic element, if used)
- **Stepper motor** (NEMA 17 or smaller) for precise, controllable rotation
- **Driver:** A4988 or TMC2208 (silent operation)
- Speed controlled by time-of-day data (slow at night, active during day)
- **Alternative:** Brushless DC with encoder for smoother, quieter operation

### Power
- **Battery:** 18650 Li-ion cells (3–4 cells for ~10,000mAh)
- **BMS:** Standard 3S/4S BMS board
- **Runtime estimate:** 8–12 hours on LEDs only; 4–6 hours with motor
- **Charging:** USB-C PD charging port (hidden in base)

---

## Materials & Finish

### Primary Material: 6061-T6 Aluminum
- Standard CNC machining alloy
- Excellent surface finish after machining
- Takes Cerakote well
- Available in stock sizes suitable for 30–50cm sculpture

### Cerakote Finish Recommendation

| Element | Cerakote Color | Code | Notes |
|---|---|---|---|
| Main body | Gun Metal Grey | H-146 | Matte, industrial, premium |
| Accent / ray fins | Aztec Teal | H-349 | Matches brand teal exactly |
| Base | Bright Nickel | H-157 | Metallic contrast, premium feel |
| Inner triangle void | Raw aluminum | — | Polished, reflects LED light |

**Why this works:** The dark grey body makes the teal pop. The nickel base adds a third tone. The raw polished inner void acts as a light reflector/diffuser for the LED glow.

### Alternative: Raw + Teal Only
- Leave main body as brushed/raw aluminum (no Cerakote on body)
- Cerakote only the ray fins in Aztec Teal
- More minimal, lets the machining speak

---

## Form Factor Options (for Concept Art Phase)

Three directions to explore visually:

### Option A: Flat Relief Panel
- Logo machined as high-relief into a flat aluminum panel
- Ray fins as individual 3D blades standing proud of the surface
- Backlit with teal LED from behind
- Mounted on weighted base at slight angle
- **Pros:** Truest to the 2D logo, most legible, easiest to machine
- **Cons:** Less dramatic as a 3D object

### Option B: Full 3D Prism
- Literal triangular prism solid (equilateral triangle cross-section)
- Logo elements on the front face (engraved/relief)
- Ray fins on the right face, ruler marks on the left face
- LED inside the prism, glowing through precision-cut apertures
- **Pros:** Most dramatic, most "sculptural," the prism IS the logo
- **Cons:** More complex machining, heavier

### Option C: Hybrid — Prism Base + Relief Face
- Triangular prism base (solid, heavy, stable)
- Separate relief panel mounted on the front face
- Ray fins as rotating kinetic element on the right side
- **Pros:** Best of both — 3D presence + detailed front face + kinetic element
- **Cons:** Most complex assembly

**Recommendation:** Option C. The prism base gives it weight and presence. The relief face gives it legibility. The rotating fins give it life.

---

## Film Production Notes

### Footage Checklist (Every Stage = A Shot)
- [ ] Sketch on paper / tablet
- [ ] Logo files open in Illustrator/CAD
- [ ] CAM toolpath generation
- [ ] CNC machine running (close-up of cutter, chips flying)
- [ ] Laser engraver running (close-up of beam)
- [ ] Cerakote application (spray gun, oven cure)
- [ ] Electronics assembly (soldering, component placement)
- [ ] First firmware flash (terminal, first LED light)
- [ ] WiFi connection / WLED dashboard
- [ ] Final assembly
- [ ] Product photography setup
- [ ] The finished piece, lit, alive

### Three Cuts
| Cut | Length | Key Moment |
|---|---|---|
| The Spark | ~10s | CNC chips → finished piece. One cut. |
| The Reel | 60–90s | Full pipeline, fast cuts, score-driven |
| The Film | 3–5min | Every stage, breathing room, possibly narrated |

### Blender Animation Sequence
1. Precision input side animates (ruler marks, measurement detail)
2. BTS clips play inside the prism (machining, designing)
3. Light refracts out — each beam lands on a finished product
4. Physical object ↔ Blender render side-by-side contrast moment

---

## Next Steps

1. **Concept art** — generate renders of Options A, B, C
2. **Form factor decision** — pick one (or hybrid)
3. **Electronics spec doc** — `firmware/electronics-spec.md`
4. **Fabrication brief** — `docs/fabrication-brief.md` for Prizma Works
5. **Blender storyboard** — rough animation sequence doc
