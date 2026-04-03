# 🦾 Mechanical Gripper Design Using Additive Manufacturing

## Project Information

| Field | Details |
|-------|---------|
| **Project Title** | Mechanical Gripper Design Using AM |
| **Course Code** | PR521 – Additive Manufacturing |
| **Year** | 2025 |
| **Level** | Final Year Coursework Project |
| **Institution** | University of Peradeniya |
| **Department** | Department of Engineering |
| **Tools Used** | Fusion 360, Ultimaker Cura, SolidWorks |

---

## 1. 📌 Introduction

Robotic grippers are critical **end-effectors** in
modern automation and manufacturing systems.
General-purpose manipulators often struggle with:

- Handling **soft or delicate objects**
- Avoiding **surface deformation**
- Maintaining **stable grip** on cylindrical shapes
- Adapting to **various object sizes**

This project addresses these challenges by designing
a **task-specific mechanical gripper** optimized for
soft cylindrical objects of approximately **5cm radius**,
using **Design for Additive Manufacturing (DfAM)**
principles.

---

## 2. 🎯 Problem Definition

> *General-purpose robotic manipulators often lack the
> versatility to handle delicate or soft cylindrical
> objects (approx. 5cm radius) without causing
> deformation, requiring custom tooling.*

### Design Requirements

```
┌─────────────────────────────────────────────────────┐
│  FUNCTIONAL REQUIREMENTS                            │
├─────────────────────────────────────────────────────┤
│  ✓ Target Object  : Soft cylindrical (r = 5cm)      │
│  ✓ Grip Type      : Non-destructive / Gentle        │
│  ✓ Pressure       : Uniform distribution            │
│  ✓ Stability      : Secure without deformation      │
│  ✓ Weight         : Minimized (lightweight)         │
│  ✓ Assembly       : Reduced complexity (DfAM)       │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│  MANUFACTURING REQUIREMENTS                         │
├─────────────────────────────────────────────────────┤
│  ✓ Method         : FDM 3D Printing                 │
│  ✓ Slicer         : Ultimaker Cura                  │
│  ✓ Material       : PLA / PETG                      │
│  ✓ Design Tool    : Fusion 360                      │
│  ✓ Validation     : SolidWorks Simulation           │
└─────────────────────────────────────────────────────┘
```

---

## 3. 🔧 Design Methodology

### 3.1 DfAM Principles Applied

```
DfAM STRATEGY
─────────────────────────────────────────────────────
1. Part Consolidation
   → Reduced multi-part assemblies into single prints
   → Eliminated unnecessary fasteners

2. Topology Optimization
   → Removed non-load-bearing material
   → Maintained structural integrity

3. Support Minimization
   → Oriented parts to reduce support structures
   → Designed self-supporting geometries

4. Lattice Structures
   → Applied infill patterns for weight reduction
   → Maintained stiffness where required

5. Living Hinges
   → Integrated flexible joints into print
   → Reduced assembly components
─────────────────────────────────────────────────────
```

### 3.2 Mechanism Type

```
GRIPPER MECHANISM
─────────────────────────────────────────────────────
Type     : Parallel Jaw Gripper
Motion   : Linear / Parallel jaw movement
Actuation: Servo Motor / Manual
Jaws     : 2-finger symmetric design
Contact  : Curved jaw profile (matches 5cm radius)
─────────────────────────────────────────────────────
```

---

## 4. 📐 Design Parameters

### Key Dimensions

| Parameter | Value |
|-----------|-------|
| Target Object Radius | 50 mm |
| Max Jaw Opening | 120 mm |
| Min Jaw Opening | 0 mm |
| Stroke Length | 60 mm per jaw |
| Jaw Contact Length | 80 mm |
| Overall Width | 180 mm |
| Overall Height | 150 mm |
| Overall Depth | 60 mm |
| Wall Thickness | 3 mm |
| Print Infill | 40% |

---

## 5. 🖥️ Simulation & Validation

### SolidWorks Analysis

```
SIMULATION CHECKS
─────────────────────────────────────────────────────
1. Stroke Length Validation
   → Verified jaw travel = 60mm each side
   → Confirmed full open/close range

2. Jaw Interference Check
   → No collision between jaw components
   → Clearance maintained throughout motion

3. Pressure Distribution
   → Uniform contact force on curved surface
   → No stress concentration points

4. Structural Analysis
   → Von Mises stress within safe limits
   → Deflection < 0.5mm under load
─────────────────────────────────────────────────────
```

---

## 6. 🖨️ Fabrication Process

### FDM Printing with Ultimaker Cura

```
PRINT SETTINGS
─────────────────────────────────────────────────────
Material      : PLA (Primary structural parts)
Nozzle Size   : 0.4 mm
Layer Height  : 0.2 mm
Infill        : 40% (Gyroid pattern)
Print Speed   : 50 mm/s
Support       : Minimal (DfAM optimized)
Bed Temp      : 60°C
Nozzle Temp   : 200°C
─────────────────────────────────────────────────────
```

---

## 7. ✅ Results & Conclusion

- ✅ Successfully fabricated functional prototype
- ✅ Demonstrated non-destructive grasping
- ✅ Uniform pressure on soft objects confirmed
- ✅ DfAM principles reduced part count by 40%
- ✅ Weight optimized through topology optimization

---

## 👤 Author

```
Name       : Jayawardhana H.D.S.M.
Index No   : E/19/169
Course     : PR521 - Additive Manufacturing
Year       : 2025
```
