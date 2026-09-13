# Gearbox Machine Design Analysis

Mechanical design and verification of a multi-stage helical gearbox developed as part of the **Fundamentals of Machine Design** course at **Politecnico di Torino**.

The project covers the complete mechanical verification workflow of the gearbox, including gear-force calculation, shaft loading, static and fatigue verification, gear-tooth strength analysis, and rolling-bearing life assessment.

---

## Project Overview

The objective of this project was to evaluate the structural integrity and expected service life of the main mechanical components of a helical gearbox.

The analysis included:

- Gear torque and force calculations
- Shaft support reactions
- Internal normal forces and bending moments
- Torsional loading
- Shaft static stress verification
- Shaft fatigue verification
- Stress concentration effects
- Fatigue-limit correction factors
- Gear-tooth bending verification
- Gear contact and pitting verification
- Rolling-bearing equivalent loads
- Bearing fatigue-life estimation
- Bearing static safety verification

The complete derivation and detailed calculations are available in the project report and supporting handwritten notes.

---

## Gearbox Load Analysis

The analysis starts from the transmitted power and rotational speed.

Key operating values:

| Parameter | Value |
|---|---:|
| Input power | 36 kW |
| Input torque | 229.18 N·m |
| Output torque | 2062.64 N·m |
| Gear pair 1 tangential force | 9223.9 N |
| Gear pair 2 tangential force | 15812.75 N |

The corresponding radial and axial forces were then used to determine the bearing reactions and internal shaft loading.

---

## Shaft Analysis

Shaft **A2** was selected as the critical shaft for detailed verification.

The shaft analysis includes:

- Support reaction forces
- Internal axial forces
- Bending moments about both principal axes
- Resultant bending moment
- Torsional moment
- Normal, bending, and torsional stresses
- Equivalent stress evaluation

### Internal Load Diagrams

![Shaft A2 internal loads](figures/shaft_A2_internal_loads.png)

For the static verification, section **V4** was identified as the most critical cross-section.

The calculated equivalent stress at V4 was approximately:

**75.93 MPa**

with a static safety factor of approximately:

**12.24**

---

## Fatigue Verification

Fatigue verification was performed by separating the mean and alternating stress components and accounting for geometric stress concentration effects.

The analysis included:

- Stress concentration factors
- Fatigue notch factors
- Size correction factor
- Surface-finish correction factor
- Equivalent mean and alternating stresses
- Haigh-diagram verification

### Haigh Diagrams

![Shaft fatigue Haigh diagrams](figures/shaft_fatigue_haigh_diagrams.png)

The most critical section for fatigue was:

**V3**

with a fatigue safety factor of approximately:

**3.97**

---

## Gear Tooth Verification

The most critical gear considered in the tooth-strength analysis was **pinion G3**.

The analysis included:

- Overload factor
- Rim-thickness factor
- Dynamic factor
- Load-distribution factor
- Size factor
- Bending-strength geometry factor
- Stress-cycle life factor
- Temperature factor
- Reliability factor

### Gear Bending Verification

![Gear tooth bending verification](figures/gear_tooth_bending_verification.png)

The calculated maximum tooth bending stress was approximately:

**221.95 MPa**

with a bending safety factor of approximately:

**3.78**

---

## Gear Contact and Pitting Verification

A Hertzian-contact-based verification was also performed to evaluate the resistance of the gear teeth to surface fatigue.

The calculated maximum contact stress was approximately:

**70.25 MPa**

and the corresponding wear/contact safety factor was approximately:

**19.83**

---

## Bearing Life Analysis

The gearbox contains six analyzed bearing positions: **A, B, C, D, E, and F**.

The bearing analysis included:

- Radial and axial bearing loads
- Equivalent dynamic load
- Equivalent static load
- Dynamic load rating
- Static load rating
- Lubricant viscosity selection
- ISO life-correction factors
- Corrected bearing rating life
- Static safety verification

### Bearing Life Results

![Bearing life summary](figures/bearing_life_summary.png)

The calculations confirm that the selected bearings satisfy the required static and fatigue-life conditions for the analyzed operating case.

---

## Key Results

| Analysis | Result |
|---|---:|
| Input power | 36 kW |
| Input torque | 229.18 N·m |
| Output torque | 2062.64 N·m |
| Critical shaft | A2 |
| Critical static section | V4 |
| Static safety factor at V4 | ≈ 12.24 |
| Critical fatigue section | V3 |
| Minimum shaft fatigue safety factor | ≈ 3.97 |
| Critical gear | G3 |
| Maximum gear bending stress | ≈ 221.95 MPa |
| Gear bending safety factor | ≈ 3.78 |
| Maximum gear contact stress | ≈ 70.25 MPa |
| Gear contact safety factor | ≈ 19.83 |

---

## Repository Structure

```text
gearbox-machine-design-analysis/
│
├── README.md
│
├── report/
│   ├── README.md
│   └── gearbox_machine_design_report.pdf
│
├── calculations/
│   ├── README.md
│   └── handwritten_engineering_calculations.pdf
│
└── figures/
    ├── README.md
    ├── shaft_A2_internal_loads.png
    ├── shaft_fatigue_haigh_diagrams.png
    ├── gear_tooth_bending_verification.png
    └── bearing_life_summary.png
