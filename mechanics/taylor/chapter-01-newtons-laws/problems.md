# Chapter 1 — Problems

**Text:** John R. Taylor, *Classical Mechanics*  
**Chapter:** 1 — Newton's Laws of Motion  

---

## How to use this file

This is the **problem sheet only**.

The notes and major derivations are in:

[`README.md`](README.md)

For each full problem:

1. Try it without consulting a solution.
2. Draw a diagram and define the coordinate system.
3. Write the governing equations before doing algebra.
4. Record where you got stuck.
5. End with **What I should recognize next time**.

---

# 1. Quick diagnostic problems

These should be completed briefly. A polished write-up is unnecessary unless
they reveal a gap.

## Problem 1.10 — Circular motion and vector differentiation

### Purpose

Check that you can move from a vector-valued position function to velocity
and acceleration and interpret their directions geometrically.

### Checklist

- [ ] Write the position vector in Cartesian components.
- [ ] Differentiate once to obtain velocity.
- [ ] Differentiate again to obtain acceleration.
- [ ] Show that velocity is tangent to the circular path.
- [ ] Show that acceleration points toward the center.
- [ ] Relate the acceleration magnitude to $v^2/R$.

### Work

### Where I got stuck

### What I should recognize next time

---

## Problem 1.24 — First-order differential equations

### Purpose

Connect the order of a differential equation to the number of arbitrary
constants in its general solution.

### Checklist

- [ ] Solve an equation of the form
  ```math
  \dot f=f.
  ```
- [ ] Identify the arbitrary constant.
- [ ] Explain why one initial condition determines the solution.
- [ ] Contrast this with a second-order equation of motion.

### Work

### Where I got stuck

### What I should recognize next time

---

# 2. Core written problems

## Problem 1.26 — Inertial and noninertial reference frames

### Purpose

Understand why constant-velocity transformations preserve zero acceleration
while accelerating frames do not.

### Useful transformations

For a frame moving at constant velocity,

```math
x'=x-vt.
```

For an accelerating frame,

```math
x''=x-\frac12at^2.
```

### Questions

- [ ] What trajectory does the puck follow in the original frame?
- [ ] What trajectory does it follow in the constant-velocity frame?
- [ ] What trajectory does it follow in the accelerating frame?
- [ ] Which frames are inertial?
- [ ] Why is Newton's first law needed to identify inertial frames?

### Diagram and frame definitions

### Coordinate transformations

### Velocity and acceleration in each frame

### Physical interpretation

### What I should recognize next time

---

## Problem 1.28 — Three-particle momentum conservation

### Purpose

Make every internal-force cancellation explicit before generalizing to an
$N$-particle system.

### Starting equations

```math
\dot{\mathbf p}_1
=
\mathbf F_{12}+\mathbf F_{13}+\mathbf F_1^{\mathrm{ext}},
```

```math
\dot{\mathbf p}_2
=
\mathbf F_{21}+\mathbf F_{23}+\mathbf F_2^{\mathrm{ext}},
```

```math
\dot{\mathbf p}_3
=
\mathbf F_{31}+\mathbf F_{32}+\mathbf F_3^{\mathrm{ext}}.
```

### Checklist

- [ ] Add the three equations.
- [ ] Group each third-law force pair.
- [ ] Use
  ```math
  \mathbf F_{ij}=-\mathbf F_{ji}.
  ```
- [ ] Derive
  ```math
  \frac{d\mathbf P}{dt}
  =
  \mathbf F_{\mathrm{ext}}.
  ```
- [ ] State when total momentum is conserved.
- [ ] Explain why the system boundary matters.

### Work

#### Total momentum

```math
\mathbf P=
```

#### Sum of the equations of motion

#### Internal-force cancellations

#### Final result

### What I should recognize next time

---

## Problem 1.38 — Newton's law in tilted Cartesian coordinates

### Purpose

Practice choosing axes that align with a constrained surface and simplify
the equations of motion.

### Setup checklist

- [ ] Draw the tilted board.
- [ ] Choose axes within the board.
- [ ] Include the normal force in the complete free-body diagram.
- [ ] Resolve gravity into the chosen directions.

### Useful equation

Perpendicular to the board,

```math
N-mg\cos\theta=0.
```

Within the board,

```math
m\ddot x=F_x,
\qquad
m\ddot y=F_y.
```

### Tasks

- [ ] Derive the component equations.
- [ ] Apply the initial velocity.
- [ ] Find $x(t)$ and $y(t)$.
- [ ] Determine the requested return time.
- [ ] Find the corresponding displacement.
- [ ] Check the answer when $\theta\to0$.

### Free-body diagram

### Coordinate definitions

### Force components

### Equations of motion

### Initial conditions

### Trajectory

### Checks

### What I should recognize next time

---

## Problem 1.43 — Polar basis vectors

### Purpose

Derive the time dependence of the polar-coordinate basis vectors.

### Begin with

```math
\hat{\mathbf r}
=
\cos\phi\,\hat{\mathbf x}
+
\sin\phi\,\hat{\mathbf y},
```

```math
\hat{\boldsymbol\phi}
=
-\sin\phi\,\hat{\mathbf x}
+
\cos\phi\,\hat{\mathbf y}.
```

### Checklist

- [ ] Derive both basis vectors geometrically.
- [ ] Differentiate $\hat{\mathbf r}$.
- [ ] Differentiate $\hat{\boldsymbol\phi}$.
- [ ] Show that
  ```math
  \dot{\hat{\mathbf r}}
  =
  \dot\phi\,\hat{\boldsymbol\phi}.
  ```
- [ ] Show that
  ```math
  \dot{\hat{\boldsymbol\phi}}
  =
  -\dot\phi\,\hat{\mathbf r}.
  ```
- [ ] Explain both signs geometrically.
- [ ] Draw the basis vectors at two nearby angles.

### Work

### Geometric interpretation

### What I should recognize next time

---

## Problem 1.41 — Uniform circular motion in polar coordinates

### Purpose

Apply the polar-coordinate form of Newton's second law.

### Given conditions

```math
r=R,
\qquad
\dot r=0,
\qquad
\ddot r=0,
\qquad
\dot\phi=\omega,
\qquad
\ddot\phi=0.
```

### Checklist

- [ ] Write the radial acceleration.
- [ ] Identify the direction of the string tension.
- [ ] Apply Newton's second law in the radial direction.
- [ ] Derive
  ```math
  T=mR\omega^2.
  ```
- [ ] Explain the sign convention.
- [ ] Check the units.

### Work

#### Radial equation

#### Angular equation

#### Final result

### What I should recognize next time

---

# 3. Computational problem

## Problem 1.50 — Exact nonlinear motion versus the small-angle approximation

### Purpose

Compare the nonlinear equation of motion with its linear approximation.

### Exact equation

```math
\ddot\phi
=
-\frac{g}{R}\sin\phi.
```

### Small-angle equation

```math
\ddot\phi
=
-\frac{g}{R}\phi.
```

### Initial conditions

```math
\phi(0)=\phi_0,
\qquad
\dot\phi(0)=0.
```

### Suggested initial angles

```math
\phi_0
\in
\left\{
5^\circ,\,
20^\circ,\,
45^\circ,\,
90^\circ
\right\}.
```

### Computational tasks

- [ ] Convert the second-order equation into two first-order equations.
- [ ] Solve the exact nonlinear model numerically.
- [ ] Compute the analytic small-angle solution.
- [ ] Plot both trajectories for each initial angle.
- [ ] Compare their periods.
- [ ] Calculate the maximum absolute trajectory difference.
- [ ] Identify when the approximation becomes visibly poor.
- [ ] Explain the physical meaning of the discrepancy.

### Code location

```text
code/problem-1-50-skateboard.ipynb
```

### First-order system

Define

```math
\omega_\phi=\dot\phi.
```

Then

```math
\dot\phi=
```

```math
\dot\omega_\phi=
```

### Results

### Interpretation

### What I should recognize next time

---

# 4. Optional stretch problems

## Problem 1.31 — Momentum conservation implies the third law

### Purpose

Study the converse of the usual momentum-conservation argument.

### Central question

If every isolated two-particle system conserves momentum, can you derive

```math
\mathbf F_{12}=-\mathbf F_{21}?
```

### Work

---

## Problem 1.45 — Constant-magnitude vector

### Purpose

Show the relationship between constant magnitude and a perpendicular time
derivative.

### Goal

Prove

```math
|\mathbf v|=\text{constant}
\quad\Longleftrightarrow\quad
\mathbf v\cdot\dot{\mathbf v}=0.
```

### Hint

Differentiate

```math
\mathbf v\cdot\mathbf v.
```

### Work

---

## Problem 1.46 — Rotating reference frame

### Purpose

Describe the same free motion in both an inertial frame and a rotating frame.

### Work

---

## Problem 1.47 — Cylindrical-coordinate extension

### Purpose

Extend the polar-coordinate velocity and acceleration derivation into
three dimensions.

### Work

---

# 5. Completion checklist

## Quick diagnostics

- [ ] Problem 1.10
- [ ] Problem 1.24

## Core written problems

- [ ] Problem 1.26
- [ ] Problem 1.28
- [ ] Problem 1.38
- [ ] Problem 1.43
- [ ] Problem 1.41

## Computational work

- [ ] Problem 1.50
- [ ] Code committed
- [ ] Figures saved
- [ ] Physical interpretation written

## Optional

- [ ] Problem 1.31
- [ ] Problem 1.45
- [ ] Problem 1.46
- [ ] Problem 1.47

---

# 6. End-of-chapter reflection

## Hardest problem

## Most useful problem

## Most important mistake

## Problem I should repeat later

## What I now understand that I did not understand before
