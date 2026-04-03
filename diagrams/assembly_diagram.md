# 🏗️ Gripper Assembly Diagram

## Exploded View (ASCII)

```
GRIPPER ASSEMBLY - EXPLODED VIEW

                    [5] SERVO MOTOR
                         ↓
              ┌──────────────────────┐
              │   [4] ACTUATOR MOUNT │
              └──────────┬───────────┘
                         │
            ┌────────────┴────────────┐
            │                        │
     [3a] LEFT LINK            [3b] RIGHT LINK
            │                        │
    ┌───────┴────────┐      ┌────────┴───────┐
    │ [2a] LEFT RAIL │      │[2b] RIGHT RAIL │
    └───────┬────────┘      └────────┬───────┘
            │                        │
    ┌───────┴────────┐      ┌────────┴───────┐
    │  [1a] LEFT JAW │      │[1b] RIGHT JAW  │
    └────────────────┘      └────────────────┘
            │                        │
            └──────────┬─────────────┘
                  [0] BASE FRAME
```

## Assembly Steps

```
STEP-BY-STEP ASSEMBLY
──────────────────────────────────────────────────────

STEP 1: Base Frame Preparation
   • Verify all slots are clear
   • Test fit rail slots (should slide freely)
   • Sand if needed for smooth movement

STEP 2: Install Sliding Rails
   • Insert left rail into left slot
   • Insert right rail into right slot
   • Verify parallel alignment
   • Rails should slide 18mm each direction

STEP 3: Attach Jaw Fingers
   • Align jaw with rail end
   • Insert M3 × 10mm bolt through jaw
   • Thread into rail T-nut
   • Tighten (not over-torque - PLA)

STEP 4: Install Actuator Mount
   • Position on center of base frame
   • Secure with 4× M3 × 8mm bolts
   • Verify perpendicular alignment

STEP 5: Mount Servo Motor
   • Insert servo into actuator pocket
   • Secure with servo mounting screws
   • Route servo cable through channel

STEP 6: Connect Linkage Arms
   • Attach left link to servo horn (left hole)
   • Attach right link to servo horn (right hole)
   • Connect other ends to jaw sliders
   • Use M3 × 6mm bolts with nylock nuts

STEP 7: Functional Test
   • Power servo to neutral (90°)
   • Check jaw opening = 100mm
   • Rotate to +45° → jaws open to ~135mm
   • Rotate to -45° → jaws close to ~65mm
   • Verify smooth motion, no binding

STEP 8: Gripper Test
   • Place soft cylinder (r=50mm) between jaws
   • Actuate to closed position
   • Verify firm grip without deformation
   • Test lift capability
──────────────────────────────────────────────────────
```

## Bill of Materials (BOM)

| Item | Description | Qty | Material/Type |
|------|-------------|-----|---------------|
| 1 | Base Frame | 1 | PLA Print |
| 2 | Sliding Rail | 2 | PLA Print |
| 3 | Jaw Finger | 2 | PLA Print |
| 4 | Actuator Mount | 1 | PLA Print |
| 5 | Linkage Arm | 2 | PLA Print |
| 6 | Servo Motor | 1 | MG996R / SG90 |
| 7 | M3 × 8mm Bolt | 8 | Stainless Steel |
| 8 | M3 × 10mm Bolt | 4 | Stainless Steel |
| 9 | M3 Nut | 8 | Stainless Steel |
| 10 | M3 Nylock Nut | 4 | Stainless Steel |
| 11 | M3 Washer | 12 | Stainless Steel |

## DfAM Benefits Achieved

```
TRADITIONAL vs DfAM DESIGN
──────────────────────────────────────────────────────
              Traditional    DfAM Design    Saving
Part Count  :     18            11          -39%
Assembly    :   45 min         20 min       -56%
Weight      :   320g           185g         -42%
Support Mat :    35g             8g         -77%
Print Time  :   14 hrs          9 hrs       -36%
──────────────────────────────────────────────────────
```
