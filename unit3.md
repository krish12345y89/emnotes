# **Structural Analysis Notes**

---

## **1. Equilibrium in Three Dimensions**

### English:

* For a rigid body in **3D equilibrium**:

  * Net force = 0
  * Net moment = 0

**Equations:**

$$
\Sigma F_x = 0, \; \Sigma F_y = 0, \; \Sigma F_z = 0
$$

$$
\Sigma M_x = 0, \; \Sigma M_y = 0, \; \Sigma M_z = 0
$$

### Hinglish:

3D me body equilibrium tab hoga jab uspar **koi net force** aur **net moment** na ho. Matlab na translation hoga, na rotation.

👉 **Example:** A 3D crane lifting load → Tensions in cables + load balance karte hain.

---

## **2. Trusses**

* A **truss** is a structure made of slender members connected at their ends.
* Assumption:

  * Members connected by **pin joints**.
  * Loads act only at **joints**.
  * Members are only in **tension or compression**.

### Methods of Analysis

#### (a) Method of Joints

* Apply equilibrium at each joint:

  * ΣFx = 0
  * ΣFy = 0
* Solve member forces step by step.

👉 Example:

* Start from joint with max 2 unknowns.
* Solve forces by taking equations of equilibrium.

#### (b) Method of Sections

* Cut through the truss (max 3 members at once).
* Apply equilibrium to one part of truss.
* Faster than method of joints for finding specific forces.

👉 Example:

* Large bridge truss → find force in one diagonal by section cut.

---

### Zero Force Members

* Special members in truss which carry **no force** (used for stability only).

Rules (shortcuts):

1. If **two non-collinear members** meet at a joint with **no external load**, both are zero-force members.
2. If **three members** meet at a joint, two collinear and one non-collinear, and no external load → the non-collinear one is zero-force member.

👉 Example:
Simple triangular truss often has vertical member carrying no load → zero-force member.

---

## **3. Beams**

* A **beam** is a structural element designed to resist **bending**.
* Loads cause bending moment + shear force.

### Types of Beams

1. **Simply Supported Beam** → supported at both ends.
2. **Cantilever Beam** → fixed at one end, free at other.
3. **Overhanging Beam** → extends beyond supports.
4. **Continuous Beam** → supported at more than 2 points.
5. **Fixed Beam** → both ends fixed.

👉 Example:

* Balcony = cantilever beam.
* Bridge span = simply supported beam.

---

## **4. Frames**

* **Frame** = Structure having multiple members, usually connected by pin joints, designed to support **multi-directional loads**.
* Members may carry **bending + axial + shear** forces.

👉 Example:

* Window frames, building skeletons.

---

## **5. Machines**

* **Machines** are structures with **moving parts** that transmit or modify force.
* Difference from frames:

  * Frames = no relative motion (static).
  * Machines = allow relative motion (dynamic).

👉 Example:

* Lifting jack, gear system, crane.

---

# **Key Features & Differences**

| Concept            | Key Point                             | Example                      |
| ------------------ | ------------------------------------- | ---------------------------- |
| Equilibrium (3D)   | 6 equations (3 forces + 3 moments)    | Crane stability              |
| Truss              | Pin-jointed, only tension/compression | Bridge truss                 |
| Method of Joints   | Solve joint-by-joint                  | Small truss                  |
| Method of Sections | Cut through members                   | Large truss analysis         |
| Zero Force Member  | No load, adds stability               | Vertical in triangular truss |
| Beam               | Resists bending                       | Cantilever balcony           |
| Frame              | Multi-member static structure         | Building skeleton            |
| Machine            | With relative motion                  | Crane, gear system           |

---

# **Summary (Easy Hinglish)**

* **Equilibrium 3D** → 6 equations, balance force & moment.
* **Trusses** → pin-jointed members; solve using **joints** (step-by-step) or **sections** (faster).
* **Zero Force Members** → stability ke liye, load carry nahi karte.
* **Beams** → resist bending, different types (cantilever, simply supported, etc.).
* **Frames** → load-bearing structures (static).
* **Machines** → motion + force transmission (dynamic).

---
