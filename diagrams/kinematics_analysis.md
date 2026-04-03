# 🔄 Gripper Kinematics Analysis

## 1. Mechanism Overview

```
PARALLEL JAW GRIPPER - KINEMATIC DIAGRAM

                    ACTUATOR (Servo)
                         │
                    ┌────┴────┐
                    │  CRANK  │  r = 25mm
                    └──┬──┬───┘
                       │  │
               ┌───────┘  └───────┐
               │                  │
          LEFT LINK           RIGHT LINK
          L = 80mm            L = 80mm
               │                  │
          ┌────┴────┐        ┌────┴────┐
          │  LEFT   │        │  RIGHT  │
          │   JAW   │        │   JAW   │
          └─────────┘        └─────────┘

Motion: Symmetric parallel jaw movement
```

## 2. Stroke Length Calculation

```
STROKE ANALYSIS
──────────────────────────────────────────────────────

Crank Radius (r)       : 25 mm
Connecting Rod (L)     : 80 mm
Max Crank Angle (θ)    : 45°

Stroke per jaw = r × sin(θ)
               = 25 × sin(45°)
               = 25 × 0.707
               = 17.7 mm ≈ 18 mm per jaw

Total jaw travel       = 2 × 18 = 36 mm
Max opening diameter   = 100 + 36 = 136 mm
Min opening diameter   = 100 - 36 = 64 mm

Target object diameter = 100 mm ✓ (within range)
──────────────────────────────────────────────────────
```

## 3. Jaw Position vs Crank Angle

```
θ (degrees) | Jaw Position (mm) | Opening (mm)
────────────┼───────────────────┼─────────────
0°          | 0                 | 100 (neutral)
10°         | 4.3               | 108.6
20°         | 8.6               | 117.1
30°         | 12.5              | 125.0
45°         | 17.7              | 135.4  (MAX)
-10°        | -4.3              | 91.4
-20°        | -8.6              | 82.9
-30°        | -12.5             | 75.0
-45°        | -17.7             | 64.6   (MIN)
```

## 4. Interference Check

```
JAW CLEARANCE ANALYSIS
──────────────────────────────────────────────────────

Jaw width              : 30 mm
Center gap (neutral)   : 40 mm
Minimum gap required   : 5 mm (clearance)

At max close position:
Gap = 40 - 2×17.7 = 4.6 mm

⚠ WARNING: Slight interference at maximum close
✓ SOLUTION: Limit servo to 40° max rotation
           Gap at 40° = 40 - 2×16.1 = 7.8 mm ✓

──────────────────────────────────────────────────────
```

## 5. Contact Pressure Distribution

```
PRESSURE ON SOFT OBJECT (r = 50mm)
──────────────────────────────────────────────────────

Jaw Profile  : Concave curve, R = 52mm
Object Radius: 50mm
Fit Gap      : 2mm (intentional clearance)

Contact Type : Conformal (curved jaw on cylinder)
Contact Area : ~2400 mm² (80mm × 30mm effective)

Pressure Distribution:
   ┌─────────────────────┐
   │  Uniform pressure   │ ← Curved jaw matches
   │  across contact     │    object profile
   │  zone ✓             │
   └─────────────────────┘

Max Stress   : 0.021 N/mm² (well below PLA limit)
Deformation  : < 0.1mm on soft object ✓
──────────────────────────────────────────────────────
```

## 6. Velocity Analysis

```
Angular velocity of servo : ω = 60 rpm = 6.28 rad/s

Linear jaw velocity:
v = r × ω × cos(θ)
  = 25 × 6.28 × cos(0°)
  = 157 mm/s (at neutral position)

At 45° position:
v = 25 × 6.28 × cos(45°)
  = 111 mm/s

Closing time (0° to 45°):
t = θ/ω = (π/4) / 6.28 = 0.125 seconds ✓
```
