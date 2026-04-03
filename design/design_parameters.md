# 🔧 Gripper Design Parameters

## Overall Dimensions

```
┌─────────────────────────────────────────────────────┐
│              GRIPPER DIMENSIONS                     │
├──────────────────────────┬──────────────────────────┤
│  Parameter               │  Value                  │
├──────────────────────────┼──────────────────────────┤
│  Target Object Radius    │  50 mm                  │
│  Max Jaw Opening         │  120 mm (diameter)      │
│  Min Jaw Opening         │  0 mm                   │
│  Stroke per Jaw          │  60 mm                  │
│  Jaw Contact Length      │  80 mm                  │
│  Jaw Curve Radius        │  52 mm (2mm clearance)  │
│  Overall Width (open)    │  180 mm                 │
│  Overall Width (closed)  │  60 mm                  │
│  Overall Height          │  150 mm                 │
│  Overall Depth           │  60 mm                  │
│  Base Plate Width        │  100 mm                 │
│  Base Plate Height       │  20 mm                  │
│  Wall Thickness          │  3 mm (min)             │
│  Finger Width            │  30 mm                  │
│  Finger Thickness        │  8 mm                   │
│  Guide Rail Length       │  130 mm                 │
│  Guide Rail Width        │  10 mm                  │
│  Slot Width              │  11 mm (1mm clearance)  │
├──────────────────────────┼──────────────────────────┤
│  Print Infill            │  40%                    │
│  Layer Height            │  0.2 mm                 │
│  Wall Count              │  3 perimeters           │
└──────────────────────────┴──────────────────────────┘
```

## Component Breakdown

### Component 1: Base Frame

```
         180mm
┌────────────────────┐
│  ┌──┐        ┌──┐  │  ← Rail slots
│  │  │        │  │  │
│  │  │        │  │  │  Height: 150mm
│  │  │        │  │  │
│  └──┘        └──┘  │
│   ──────────────   │  ← Motor mount
└────────────────────┘
     Depth: 60mm
```

### Component 2: Jaw / Finger

```
        30mm
    ┌──────────┐
    │          │  ← Flat section
    │          │     Height: 40mm
    │          │
    └──┐    ┌──┘
       │    │     ← Curved section
       │    │        Radius: 52mm
       └────┘        Length: 80mm
```

### Component 3: Sliding Rail

```
   ══════════════════════  ← Rail
   Length: 130mm
   Width:  10mm
   Height: 15mm
   
   Slot for jaw connection:
   Width:  11mm (1mm clearance)
```

### Component 4: Actuator Mount

```
    ┌──────────┐
    │  O    O  │  ← Servo horn holes
    │          │
    │  ┌────┐  │  ← Servo pocket
    │  │    │  │     50x40mm
    │  └────┘  │
    └──────────┘
    Width:  70mm
    Height: 60mm
```

## Material Properties

| Property | PLA | PETG |
|----------|-----|------|
| Tensile Strength | 50 MPa | 53 MPa |
| Flexural Modulus | 3.5 GPa | 2.1 GPa |
| Density | 1.24 g/cm³ | 1.27 g/cm³ |
| Print Temp | 200°C | 230°C |
| Recommended Use | Frame, Base | Flexible joints |

## Force Analysis

```
GRIPPING FORCE CALCULATION
──────────────────────────────────────────────
Servo Torque     : 2.5 Nm (standard servo)
Arm Length       : 25 mm
Force at Jaw     : F = T/r = 2.5/0.025 = 100N

Safety Factor    : 2.0
Design Force     : 50N per jaw

Contact Area     : 80mm × 30mm = 2400 mm²
Pressure         : P = F/A = 50/2400
                 : P = 0.021 N/mm² (soft object safe)
──────────────────────────────────────────────
```
