# **Deep Notes: Vectors, Tensors & Coordinate Systems**

---

## **1. Introduction to Vectors and Tensors**

### Vectors

* A **vector** is a quantity having both **magnitude** and **direction**.
* Represented as **A = (Ax, Ay, Az)** in 3D Cartesian coordinates.
* Can be added, subtracted, scaled.

👉 **Examples:**

* Displacement, Velocity, Force.

### Tensors

* A **tensor** is a mathematical object that generalizes scalars and vectors:

  * **Scalar (0th order tensor):** Only magnitude (e.g., temperature, mass).
  * **Vector (1st order tensor):** Magnitude + direction (e.g., force, velocity).
  * **2nd order tensor:** Needs a matrix of components (e.g., stress, strain).
  * **Higher-order tensors:** e.g., elasticity tensor (4th order).

👉 **Example (Stress Tensor):**

$$
\sigma =
\begin{bmatrix}
\sigma_{xx} & \sigma_{xy} & \sigma_{xz} \\
\sigma_{yx} & \sigma_{yy} & \sigma_{yz} \\
\sigma_{zx} & \sigma_{zy} & \sigma_{zz}
\end{bmatrix}
$$

Each component shows stress acting on a plane in a given direction.

---

## **2. Coordinate Systems**

* **Cartesian (x, y, z):** Rectangular, most common in mechanics.
* **Cylindrical (r, θ, z):** Used in pipes, shafts, rotating bodies.
* **Spherical (r, θ, φ):** Used in planetary motion, EM fields.

👉 **Conversion Example:**
Cartesian to Cylindrical:

* x = r cos θ
* y = r sin θ
* z = z

---

## **3. Vector and Tensor Algebra**

### Vector Algebra

* **Dot Product (Scalar Product):**

  $$
  \mathbf{A} \cdot \mathbf{B} = |A||B|\cos\theta
  $$

  👉 Gives scalar, measures "projection".
  Example: Work = Force · Displacement.

* **Cross Product (Vector Product):**

  $$
  \mathbf{A} \times \mathbf{B} = |A||B|\sin\theta \, \mathbf{n}
  $$

  👉 Gives vector perpendicular to plane.
  Example: Torque = r × F.

### Tensor Algebra

* **Addition/Multiplication:** Tensors add component-wise, multiply like matrices.
* **Contraction:** Reduces order of tensor by summing repeated indices.
  Example: δᵢᵢ = 3 (Kronecker delta contraction).

---

## **4. Indicial Notation (Index Notation)**

* Very compact notation for tensors.
* Rules:

  * Repeated indices = summation (Einstein summation convention).
  * Free indices = remain in expression.

👉 Example:

* Dot product:

  $$
  A_i B_i = \sum_{i=1}^3 A_i B_i
  $$
* Stress transformation:

  $$
  \sigma'_{ij} = a_{ip} a_{jq} \sigma_{pq}
  $$

---

## **5. Symmetric and Anti-Symmetric Tensors**

* **Symmetric Tensor:**
  $T_{ij} = T_{ji}$
  Example: Stress tensor (σxy = σyx).

* **Anti-Symmetric Tensor:**
  $T_{ij} = -T_{ji}$
  Example: Rotation tensor.

👉 Any 2nd order tensor can be split into:

$$
T_{ij} = \underbrace{\tfrac{1}{2}(T_{ij}+T_{ji})}_{\text{symmetric}} + \underbrace{\tfrac{1}{2}(T_{ij}-T_{ji})}_{\text{anti-symmetric}}
$$

---

## **6. Eigenvalues and Principal Axes**

* **Eigenvalue Problem:**
  For tensor $A$, if

  $$
  A x = \lambda x
  $$

  then $x$ = eigenvector, $\lambda$ = eigenvalue.

* **Principal Axes:**
  Directions in which tensor acts as pure scaling (no shear).
  👉 For stress tensor → principal stresses = eigenvalues, principal directions = eigenvectors.

👉 Example (2D stress):

$$
\sigma =
\begin{bmatrix}
10 & 5 \\
5 & 20
\end{bmatrix}
$$

Eigenvalues → principal stresses.

---

## **7. 3D Rotation: Euler’s Theorem**

* **Euler’s Theorem:**
  Any 3D rotation can be described as a **rotation about some axis** through an angle θ.

* **Axis-Angle Formulation:**
  Rotation matrix =

  $$
  R = I \cos\theta + (1-\cos\theta)(nn^T) + \sin\theta [n]_\times
  $$

  where **n = unit vector along axis**, $[n]_\times$ = skew-symmetric matrix.

👉 Example: Rotate vector 90° about z-axis →

$$
R =
\begin{bmatrix}
0 & -1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1
\end{bmatrix}
$$

---

## **8. Euler Angles (φ, θ, ψ)**

* Three successive rotations:

  1. Rotate about z-axis by φ
  2. Rotate about new x-axis by θ
  3. Rotate about new z-axis by ψ

* Widely used in **aerospace, robotics, 3D graphics**.

👉 Example: Aircraft orientation (yaw, pitch, roll).

---

## **9. Coordinate Transformation of Vectors and Tensors**

### Vector Transformation

* If basis changes, vector components change:

  $$
  v'_i = a_{ij} v_j
  $$

  where $a_{ij}$ = direction cosines.

### Tensor Transformation

* For 2nd order tensor:

  $$
  T'_{ij} = a_{ip} a_{jq} T_{pq}
  $$

👉 Example: Stress tensor on rotated axis system.

---

# **Features & Importance**

1. **Vectors** = handle direction + magnitude.
2. **Tensors** = generalize forces, stresses, strains.
3. **Indicial notation** = compact way of writing.
4. **Symmetric tensors** = physical quantities like stress.
5. **Eigenvalues** = principal stresses, natural modes.
6. **Euler angles** = orientation description in 3D.
7. **Coordinate transformation** = must for mechanics, robotics, aerospace.

---

# **Quick Summary Chart**

| Concept              | Formula/Key                  | Example                |
| -------------------- | ---------------------------- | ---------------------- |
| Vector dot product   | $A·B = A_iB_i$               | Work = F·d             |
| Vector cross product | $A×B$                        | Torque = r×F           |
| Tensor symmetry      | $T_{ij}=T_{ji}$              | Stress tensor          |
| Eigenvalue           | $Ax = λx$                    | Principal stresses     |
| Euler theorem        | Any rotation = axis + angle  | Rotate cube 90°        |
| Vector transform     | $v'_i=a_{ij}v_j$             | Coordinate rotation    |
| Tensor transform     | $T'_{ij}=a_{ip}a_{jq}T_{pq}$ | Stress on rotated axes |

---
👉 Kya mai tere liye **5–6 solved numericals** bana du is topic ke (step by step)?
