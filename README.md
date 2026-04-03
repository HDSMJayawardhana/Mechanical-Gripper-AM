# 🦾 Mechanical Gripper Design Using Additive Manufacturing

> **Course:** PR521 – Additive Manufacturing
> **Level:** Final Year Coursework Project
> **Year:** 2025
> **University:** University of Peradeniya

---

## 📌 Project Overview

A **task-specific mechanical gripper** designed and
fabricated using **Additive Manufacturing (AM)**
techniques. The gripper is optimized for handling
**soft cylindrical objects** of approximately **5cm radius**
without causing surface deformation.

---

## 🎯 Design Goal

```
Target Object    : Soft cylinder (r = 50mm)
Grip Type        : Non-destructive parallel jaw
Manufacturing    : FDM 3D Printing (DfAM optimized)
Validation       : SolidWorks simulation
Fabrication      : Ultimaker Cura + FDM printer
```

---

## 🏗️ System Architecture

```
         ┌─────────────────────────────┐
         │        GRIPPER SYSTEM       │
         ├─────────────────────────────┤
         │                             │
         │   ┌──────┐      ┌──────┐   │
         │   │ LEFT │      │RIGHT │   │
         │   │ JAW  │ OBJ  │ JAW  │   │
         │   │      │(5cm) │      │   │
         │   └──┬───┘      └───┬──┘   │
         │      │   LINKAGE    │      │
         │      └──────┬───────┘      │
         │         ACTUATOR           │
         │         (Servo)            │
         └─────────────────────────────┘
```

---

## 📂 Repository Structure

```
Mechanical-Gripper-AM/
│
├── README.md
├── docs/
│   └── project_description.md
├── cad/
│   └── gripper.step
│   └── gripper.PNG
├── design/
│   ├── design_parameters.md      ← All dimensions
│   ├── dfam_principles.md        ← DfAM guidelines
│   └── kinematics_analysis.md    ← Motion analysis
├── diagrams/
│   ├── gripper_components.md     ← Part diagrams
│   ├── mechanism_diagram.md      ← Mechanism layout
│   ├── dimensions.md             ← Dimension drawings
│   └── assembly_diagram.md       ← Assembly guide
├── simulation/
│   ├── solidworks_setup.md       ← Simulation guide
│   └── motion_analysis.md        ← Results
├── fabrication/
│   ├── cura_settings.md          ← Print settings
│   └── fdm_process.md            ← Process guide
└── calculations/
    └── gripper_calculations.md   ← Force & kinematics
```

---

## 📐 Key Specifications

| Parameter | Value |
|-----------|-------|
| Target Object Radius | 50 mm |
| Max Jaw Opening | 135 mm |
| Min Jaw Opening | 65 mm |
| Stroke per Jaw | ~18 mm |
| Gripping Force | 50 N |
| Total Weight | ~185 g |
| Print Material | PLA |
| Infill | 40% Gyroid |
| Total Print Time | ~9 hours |

---

## ⚙️ DfAM Principles Applied

| Principle | Implementation | Benefit |
|-----------|----------------|---------|
| Part Consolidation | Multi-part → single print | -39% part count |
| Topology Optimization | Remove non-structural material | -42% weight |
| Support Minimization | Orient parts strategically | -77% support material |
| Living Hinges | Integrated flexible joints | Reduced assembly |
| Infill Optimization | Gyroid 40% pattern | Best strength/weight |

---

## 🖥️ Simulation Results

| Check | Tool | Result |
|-------|------|--------|
| Stroke Length | SolidWorks Motion | ✅ 18mm/jaw |
| Jaw Interference | SolidWorks Collision | ✅ No collision |
| Pressure Distribution | SolidWorks FEA | ✅ Uniform |
| Von Mises Stress | SolidWorks FEA | ✅ Within limits |
| Deflection | SolidWorks FEA | ✅ < 0.5mm |

---

## 🖨️ Print Settings Summary

| Setting | Value |
|---------|-------|
| Slicer | Ultimaker Cura |
| Layer Height | 0.2 mm |
| Infill | 40% Gyroid |
| Wall Count | 4 |
| Nozzle Temp | 205°C |
| Bed Temp | 60°C |
| Print Speed | 50 mm/s |
| Support | Minimal |

---

## ✅ Results

- ✅ Fully functional prototype fabricated
- ✅ Non-destructive grasping demonstrated
- ✅ Uniform pressure confirmed on soft objects
- ✅ Part count reduced by **39%** vs traditional
- ✅ Weight reduced by **42%** through DfAM
- ✅ Print time reduced by **36%**

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| **Fusion 360** | 3D CAD Design |
| **SolidWorks** | Simulation & Validation |
| **Ultimaker Cura** | Slicing & Print Preparation |
| **FDM 3D Printer** | Physical Fabrication |

---

## 📚 References

- PR521 Additive Manufacturing Course Notes (2025)
- Design for Additive Manufacturing Guidelines
- Ultimaker Cura Documentation
- Autodesk Fusion 360 Reference
- SolidWorks Simulation Manual

---

## 👤 Author

```
Name       : Jayawardhana H.D.S.M.
Index No   : E/19/169
Course     : PR521 - Additive Manufacturing
Year       : 2025
University : University of Peradeniya
```

---

*© 2025 - University of Peradeniya*
