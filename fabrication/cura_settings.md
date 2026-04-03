# 🖨️ Ultimaker Cura Print Settings

## Printer Configuration

```
PRINTER SETTINGS
──────────────────────────────────────────────────────
Printer Model    : Ultimaker S3 / Generic FDM
Nozzle Diameter  : 0.4 mm
Build Volume     : 230 × 190 × 200 mm
──────────────────────────────────────────────────────
```

## Material Settings

| Part | Material | Reason |
|------|----------|--------|
| Base Frame | PLA | Rigid, stable |
| Jaw Fingers | PLA | Stiff contact |
| Sliding Rail | PLA | Dimensional accuracy |
| Flexible Joints | PETG | Slight flex allowed |

## Print Profiles

### Profile 1: Structural Parts (Frame, Rail)

```
STRUCTURAL PARTS PROFILE
──────────────────────────────────────────────────────
Layer Height     : 0.2 mm
Initial Layer    : 0.3 mm
Wall Count       : 4 (perimeters)
Top/Bottom Layers: 5
Infill           : 40% - Gyroid pattern
Print Speed      : 50 mm/s
Wall Speed       : 30 mm/s
Infill Speed     : 60 mm/s
Travel Speed     : 150 mm/s
Nozzle Temp      : 205°C (PLA)
Bed Temp         : 60°C
Cooling Fan      : 100% (after layer 3)
Support          : None (DfAM optimized)
Adhesion         : Brim (5mm)
──────────────────────────────────────────────────────
```

### Profile 2: Jaw Fingers

```
JAW FINGERS PROFILE
──────────────────────────────────────────────────────
Layer Height     : 0.15 mm (finer for curve)
Wall Count       : 5 (stronger contact surface)
Infill           : 60% - Cubic pattern
Print Speed      : 40 mm/s (slower for accuracy)
Support          : Minimal (curved inner face)
Support Angle    : 50°
Support Density  : 15%
──────────────────────────────────────────────────────
```

## Print Orientation

```
OPTIMAL PRINT ORIENTATIONS
──────────────────────────────────────────────────────

Base Frame:
   Flat on bed → Best layer adhesion for XY loads
   ┌────────────────────┐
   │////////////////////│ ← Layers
   └────────────────────┘ ← Build plate

Jaw Fingers:
   Curved face UP → No support on contact surface
   
        ___
       /   \  ← Curved contact (top, no support)
      │     │
      │     │
   ───┴─────┴─── ← Build plate

Sliding Rail:
   Long axis horizontal → Best rail strength
   ══════════════════════ ← Horizontal print
──────────────────────────────────────────────────────
```

## Post-Processing Steps

```
POST PROCESSING CHECKLIST
──────────────────────────────────────────────────────
Step 1: Remove from build plate (after cooling)
Step 2: Remove brim with flush cutters
Step 3: Sand contact surfaces (220 grit)
Step 4: Test fit all components
Step 5: Light sanding on rail slots (smooth fit)
Step 6: Assembly with M3 bolts
Step 7: Functional test (open/close motion)
Step 8: Gripper test on soft object
──────────────────────────────────────────────────────
```

## Estimated Print Times

| Component | Time | Material Used |
|-----------|------|---------------|
| Base Frame | ~4 hrs | ~85g PLA |
| Left Jaw | ~1.5 hrs | ~25g PLA |
| Right Jaw | ~1.5 hrs | ~25g PLA |
| Sliding Rail ×2 | ~1 hr | ~20g PLA |
| Actuator Mount | ~1 hr | ~18g PLA |
| **Total** | **~9 hrs** | **~173g** |
