# Taylor Classical Mechanics — Chapter 1
## Problems and Essential Derivations

Use this file after finishing Chapter 1. The goal is not to complete every exercise in the chapter, but to solve a focused set that checks the main conceptual and technical ideas.

---

## How to use this file

For each full problem:

1. Try it without consulting the solution manual.
2. Draw a diagram and define the coordinate system.
3. Write the governing equations before doing algebra.
4. Record where you got stuck.
5. Finish with a short note titled **What I should recognize next time**.

For each derivation:

1. Reproduce it from a blank page.
2. Explain each step in words.
3. Check units, signs, and special cases.
4. Repeat it later if you had to look anything up.

---

# Part I — Quick Diagnostic Problems

These should be completed briefly. A full polished write-up is unnecessary unless you find a gap in your understanding.

## Problem 1.10 — Circular motion and vector differentiation

### Purpose

Check that you can move from a vector-valued position function to velocity and acceleration and interpret their directions geometrically.

### Before solving

- [ ] Write the position vector in Cartesian components.
- [ ] Differentiate once to obtain velocity.
- [ ] Differentiate again to obtain acceleration.
- [ ] Show that velocity is tangent to the circular path.
- [ ] Show that acceleration points toward the center.
- [ ] Relate the acceleration magnitude to \(v^2/R\).

### Notes

**Where I got stuck:**

**What I should recognize next time:**

---

## Problem 1.24 — First-order differential equations

### Purpose

Connect the order of a differential equation to the number of arbitrary constants in its general solution.

### Before solving

- [ ] Solve an equation of the form
  \[
  \dot f=f.
  \]
- [ ] Identify the arbitrary constant.
- [ ] Explain why one initial condition determines the solution.
- [ ] Contrast this with a second-order equation of motion.

### Notes

**Where I got stuck:**

**What I should recognize next time:**

---

# Part II — Core Written Problems

These deserve full solutions.

## Problem 1.26 — Inertial and noninertial reference frames

### Purpose

Understand why constant-velocity coordinate transformations preserve zero acceleration while accelerating frames do not.

### Key ideas to use

For a frame moving at constant velocity,

\[
x'=x-vt.
\]

For a frame accelerating relative to the original frame,

\[
x''=x-\frac12 at^2.
\]

### Questions to answer

- [ ] What trajectory does the puck follow in the original frame?
- [ ] What trajectory does it follow in the constant-velocity frame?
- [ ] What trajectory does it follow in the accelerating frame?
- [ ] Which frames are inertial?
- [ ] Why is Newton's first law needed to identify inertial frames?

### Solution workspace

#### Diagram and frame definitions

#### Coordinate transformations

#### Velocity and acceleration in each frame

#### Physical interpretation

### What I should recognize next time

---

## Problem 1.28 — Three-particle momentum conservation

### Purpose

Make every internal-force cancellation in the momentum-conservation proof explicit.

### Start with

\[
\dot{\mathbf p}_1
=
\mathbf F_{12}+\mathbf F_{13}+\mathbf F_1^{\mathrm{ext}},
\]

\[
\dot{\mathbf p}_2
=
\mathbf F_{21}+\mathbf F_{23}+\mathbf F_2^{\mathrm{ext}},
\]

\[
\dot{\mathbf p}_3
=
\mathbf F_{31}+\mathbf F_{32}+\mathbf F_3^{\mathrm{ext}}.
\]

### Tasks

- [ ] Add the three equations.
- [ ] Group each third-law force pair.
- [ ] Use
  \[
  \mathbf F_{ij}=-\mathbf F_{ji}.
  \]
- [ ] Derive
  \[
  \frac{d\mathbf P}{dt}
  =
  \mathbf F_{\mathrm{ext}}.
  \]
- [ ] State the condition under which total momentum is conserved.
- [ ] Explain why the system boundary matters.

### Solution workspace

#### Total momentum

\[
\mathbf P=
\]

#### Sum of the equations of motion

#### Internal-force cancellations

#### Final result

### What I should recognize next time

---

## Problem 1.38 — Newton's law in tilted Cartesian coordinates

### Purpose

Practice choosing axes that align with a constrained surface and simplify the equations of motion.

### Setup checklist

- [ ] Draw the tilted board.
- [ ] Choose one axis along the board.
- [ ] Choose the second axis perpendicular to the first within the board.
- [ ] Include the force normal to the board in the full free-body diagram.
- [ ] Resolve gravity into the chosen directions.

### Useful equations

Perpendicular to the board,

\[
N-mg\cos\theta=0.
\]

Within the board, the equations will have the form

\[
m\ddot x=F_x,
\qquad
m\ddot y=F_y.
\]

### Tasks

- [ ] Derive the component equations.
- [ ] Apply the initial velocity.
- [ ] Find \(x(t)\) and \(y(t)\).
- [ ] Determine when the puck returns to the relevant boundary or height.
- [ ] Find the corresponding displacement.
- [ ] Check the answer when \(\theta\to0\).

### Solution workspace

#### Free-body diagram

#### Coordinate definitions

#### Force components

#### Equations of motion

#### Initial conditions

#### Trajectory

#### Checks

### What I should recognize next time

---

## Problem 1.43 — Polar basis vectors

### Purpose

Derive the time dependence of the polar-coordinate basis vectors.

### Begin with

\[
\hat{\mathbf r}
=
\cos\phi\,\hat{\mathbf x}
+
\sin\phi\,\hat{\mathbf y},
\]

\[
\hat{\boldsymbol\phi}
=
-\sin\phi\,\hat{\mathbf x}
+
\cos\phi\,\hat{\mathbf y}.
\]

### Tasks

- [ ] Derive both basis vectors geometrically.
- [ ] Differentiate \(\hat{\mathbf r}\) with respect to time.
- [ ] Differentiate \(\hat{\boldsymbol\phi}\) with respect to time.
- [ ] Show that
  \[
  \dot{\hat{\mathbf r}}
  =
  \dot\phi\,\hat{\boldsymbol\phi},
  \]
  and
  \[
  \dot{\hat{\boldsymbol\phi}}
  =
  -\dot\phi\,\hat{\mathbf r}.
  \]
- [ ] Explain both signs geometrically.
- [ ] Draw the basis vectors at two nearby angles.

### Solution workspace

#### Cartesian representation

#### Derivative of \(\hat{\mathbf r}\)

#### Derivative of \(\hat{\boldsymbol\phi}\)

#### Geometric interpretation

### What I should recognize next time

---

## Problem 1.41 — Uniform circular motion in polar coordinates

### Purpose

Apply the polar-coordinate form of Newton's second law to a simple physical system.

### Given conditions

\[
r=R,
\qquad
\dot r=0,
\qquad
\ddot r=0,
\qquad
\dot\phi=\omega,
\qquad
\ddot\phi=0.
\]

### Tasks

- [ ] Write the radial acceleration.
- [ ] Identify the direction of the string tension.
- [ ] Apply Newton's second law in the radial direction.
- [ ] Derive
  \[
  T=mR\omega^2.
  \]
- [ ] Explain the sign convention.
- [ ] Check the units.

### Solution workspace

#### Radial equation

#### Angular equation

#### Final result

### What I should recognize next time

---

# Part III — Computational Problem

## Problem 1.50 — Exact nonlinear motion versus the small-angle approximation

### Purpose

Compare the nonlinear equation of motion with its linear approximation and learn to solve a mechanics problem numerically.

### Exact equation

\[
\ddot\phi
=
-\frac{g}{R}\sin\phi.
\]

### Small-angle approximation

\[
\ddot\phi
=
-\frac{g}{R}\phi.
\]

### Initial conditions

\[
\phi(0)=\phi_0,
\qquad
\dot\phi(0)=0.
\]

### Suggested initial angles

\[
\phi_0
\in
\left\{
5^\circ,\,
20^\circ,\,
45^\circ,\,
90^\circ
\right\}.
\]

### Computational tasks

- [ ] Convert the second-order equation into two first-order equations.
- [ ] Solve the exact nonlinear model numerically.
- [ ] Compute the analytic small-angle solution.
- [ ] Plot both trajectories for each initial angle.
- [ ] Compare their periods.
- [ ] Calculate the maximum absolute trajectory difference.
- [ ] Identify when the small-angle approximation becomes visibly poor.
- [ ] Explain the physical meaning of the discrepancy.

### First-order system

Define

\[
\omega_\phi=\dot\phi.
\]

Then write

\[
\dot\phi=
\]

\[
\dot\omega_\phi=
\]

### Suggested outputs

- `phi_exact(t)`
- `phi_small_angle(t)`
- period estimate
- maximum absolute error
- relative period error

### Optional statistical extension

Treat the initial angle as uncertain:

\[
\phi_0\sim\text{Truncated Normal}(\mu,\sigma^2).
\]

Simulate the induced distribution of:

- oscillation period;
- maximum speed;
- approximation error.

### Interpretation

**What changed as \(\phi_0\) increased?**

**Why did the approximation fail?**

**What I should recognize next time:**

---

# Part IV — Essential Derivations

## Warm-up — Newton's second law as an initial-value problem

### Goal

Show how Newton's second law becomes a differential equation whose integration constants are determined by initial conditions.

### Starting equation

\[
m\ddot x=F_0.
\]

### Derivation

First integration:

\[
\dot x(t)=
\]

Second integration:

\[
x(t)=
\]

Apply

\[
x(0)=x_0,
\qquad
\dot x(0)=v_0.
\]

Final result:

\[
\boxed{
x(t)
=
x_0+v_0t+\frac{F_0}{2m}t^2
}
\]

### Explain in words

- Why are there two constants?
- What physical information do they represent?
- What changes if the force depends on \(x\), \(\dot x\), or \(t\)?

### Mastery check

- [ ] I can derive this without looking.
- [ ] I can explain why a second-order ODE needs two initial conditions.

---

## Big Derivation 1 — Momentum conservation for an \(N\)-particle system

### Goal

Derive

\[
\boxed{
\frac{d\mathbf P}{dt}
=
\sum_\alpha \mathbf F_\alpha^{\mathrm{ext}}
}
\]

and identify the assumptions required for conservation.

### Definitions

Total momentum:

\[
\mathbf P
=
\sum_{\alpha=1}^{N}
\mathbf p_\alpha.
\]

Equation of motion for particle \(\alpha\):

\[
\dot{\mathbf p}_\alpha
=
\sum_{\beta\ne\alpha}
\mathbf F_{\alpha\beta}
+
\mathbf F_\alpha^{\mathrm{ext}}.
\]

### Derivation workspace

Differentiate total momentum:

\[
\frac{d\mathbf P}{dt}
=
\]

Substitute the particle equations:

\[
\frac{d\mathbf P}{dt}
=
\]

Separate internal and external forces:

\[
\frac{d\mathbf P}{dt}
=
\]

Use Newton's third law:

\[
\mathbf F_{\alpha\beta}
+
\mathbf F_{\beta\alpha}
=
0.
\]

Show that the internal-force sum vanishes:

\[
\sum_\alpha
\sum_{\beta\ne\alpha}
\mathbf F_{\alpha\beta}
=
\]

Final result:

\[
\frac{d\mathbf P}{dt}
=
\]

For an isolated system:

\[
\mathbf F_{\mathrm{ext}}=0
\quad\Longrightarrow\quad
\mathbf P=
\]

### Questions to answer

- Why does every internal force appear twice?
- Why must the two appearances have opposite signs?
- What assumptions about the interactions are being made?
- How does redefining the system change which forces are external?
- What does conservation of momentum say physically?

### Mastery check

- [ ] I can first demonstrate the result for three particles.
- [ ] I can reproduce the indexed \(N\)-particle proof.
- [ ] I can explain the role of Newton's third law.

---

## Big Derivation 2 — Polar basis vectors and their derivatives

### Goal

Derive the rotating polar basis from fixed Cartesian unit vectors.

### Begin with the geometry

\[
\hat{\mathbf r}
=
\cos\phi\,\hat{\mathbf x}
+
\sin\phi\,\hat{\mathbf y},
\]

\[
\hat{\boldsymbol\phi}
=
-\sin\phi\,\hat{\mathbf x}
+
\cos\phi\,\hat{\mathbf y}.
\]

### Derivative of \(\hat{\mathbf r}\)

\[
\dot{\hat{\mathbf r}}
=
\]

Rewrite the result in the polar basis:

\[
\boxed{
\dot{\hat{\mathbf r}}
=
\dot\phi\,\hat{\boldsymbol\phi}
}
\]

### Derivative of \(\hat{\boldsymbol\phi}\)

\[
\dot{\hat{\boldsymbol\phi}}
=
\]

Rewrite the result in the polar basis:

\[
\boxed{
\dot{\hat{\boldsymbol\phi}}
=
-\dot\phi\,\hat{\mathbf r}
}
\]

### Geometric explanation

Explain why the derivative of a unit vector is perpendicular to that vector.

Explain why:

- \(\hat{\mathbf r}\) rotates toward \(\hat{\boldsymbol\phi}\);
- \(\hat{\boldsymbol\phi}\) rotates toward \(-\hat{\mathbf r}\).

### Mastery check

- [ ] I can draw the basis vectors.
- [ ] I can derive their Cartesian forms.
- [ ] I can derive both time derivatives.
- [ ] I understand the signs without memorizing them.

---

## Big Derivation 3 — Velocity and acceleration in polar coordinates

### Goal

Derive

\[
\boxed{
\mathbf v
=
\dot r\,\hat{\mathbf r}
+
r\dot\phi\,\hat{\boldsymbol\phi}
}
\]

and

\[
\boxed{
\mathbf a
=
\left(\ddot r-r\dot\phi^2\right)\hat{\mathbf r}
+
\left(r\ddot\phi+2\dot r\dot\phi\right)
\hat{\boldsymbol\phi}
}.
\]

### Position

\[
\mathbf r=r\hat{\mathbf r}.
\]

### Velocity derivation

Use the product rule:

\[
\mathbf v
=
\frac{d}{dt}
\left(r\hat{\mathbf r}\right).
\]

Then

\[
\mathbf v
=
\]

Substitute

\[
\dot{\hat{\mathbf r}}
=
\dot\phi\hat{\boldsymbol\phi}.
\]

Final result:

\[
\mathbf v
=
\]

### Interpret the two velocity terms

\[
\dot r\,\hat{\mathbf r}
\]

means:

\[
r\dot\phi\,\hat{\boldsymbol\phi}
\]

means:

### Acceleration derivation

Begin with

\[
\mathbf a
=
\frac{d}{dt}
\left(
\dot r\,\hat{\mathbf r}
+
r\dot\phi\,\hat{\boldsymbol\phi}
\right).
\]

Expand every term using the product rule:

\[
\mathbf a
=
\]

Substitute

\[
\dot{\hat{\mathbf r}}
=
\dot\phi\hat{\boldsymbol\phi},
\qquad
\dot{\hat{\boldsymbol\phi}}
=
-\dot\phi\hat{\mathbf r}.
\]

Collect radial terms:

\[
a_r=
\]

Collect angular terms:

\[
a_\phi=
\]

Final result:

\[
\boxed{
\mathbf a
=
\left(\ddot r-r\dot\phi^2\right)\hat{\mathbf r}
+
\left(r\ddot\phi+2\dot r\dot\phi\right)
\hat{\boldsymbol\phi}
}
\]

### Interpret every term

| Term | Interpretation |
|---|---|
| \(\ddot r\) | |
| \(-r\dot\phi^2\) | |
| \(r\ddot\phi\) | |
| \(2\dot r\dot\phi\) | |

### Special-case checks

#### Pure radial motion

Set

\[
\dot\phi=0.
\]

Then:

\[
\mathbf a=
\]

#### Uniform circular motion

Set

\[
r=R,
\quad
\dot r=\ddot r=0,
\quad
\dot\phi=\omega,
\quad
\ddot\phi=0.
\]

Then:

\[
\mathbf a=
\]

#### Circular motion with angular acceleration

Set

\[
r=R,
\quad
\dot r=\ddot r=0.
\]

Then:

\[
\mathbf a=
\]

### Mastery check

- [ ] I can derive the formula from a blank page.
- [ ] I can explain where all four terms originate.
- [ ] I can recover uniform circular motion as a special case.
- [ ] I do not need to memorize the formula mechanically.

---

## Big Derivation 4 — Exact skateboard equation and small-angle motion

### Goal

Derive the nonlinear equation of motion and its simple-harmonic approximation.

### Setup

A mass is constrained to move at fixed radius:

\[
r=R.
\]

The tangential component of gravity is

\[
F_\phi=-mg\sin\phi.
\]

For fixed radius, the angular acceleration component is

\[
a_\phi=R\ddot\phi.
\]

### Exact equation

Apply Newton's second law:

\[
mR\ddot\phi
=
-mg\sin\phi.
\]

Cancel \(m\):

\[
\boxed{
\ddot\phi
=
-\frac{g}{R}\sin\phi
}
\]

or

\[
\boxed{
\ddot\phi
+
\frac{g}{R}\sin\phi
=
0
}.
\]

### Why it is nonlinear

Explain why the appearance of \(\sin\phi\) makes this a nonlinear differential equation.

### Small-angle approximation

For small angles in radians,

\[
\sin\phi\approx\phi.
\]

Then

\[
\ddot\phi
+
\frac{g}{R}\phi
=
0.
\]

Define

\[
\omega_0^2=\frac{g}{R}.
\]

Then

\[
\ddot\phi+\omega_0^2\phi=0.
\]

### General solution

\[
\phi(t)
=
A\cos(\omega_0t)
+
B\sin(\omega_0t).
\]

For

\[
\phi(0)=\phi_0,
\qquad
\dot\phi(0)=0,
\]

derive

\[
\phi(t)=
\]

### Period

\[
\boxed{
T
=
2\pi\sqrt{\frac{R}{g}}
}
\]

### Questions to answer

- Why must \(\phi\) be measured in radians?
- Why does the approximate period not depend on amplitude?
- Does the exact nonlinear period depend on amplitude?
- What happens to the approximation as \(\phi_0\) grows?
- Why is this a useful example of model approximation?

### Mastery check

- [ ] I can derive the exact equation from the force diagram.
- [ ] I can justify the small-angle approximation.
- [ ] I can solve the approximate equation.
- [ ] I can explain why the exact and approximate solutions diverge.

---

# Part V — Optional Stretch Problems

Complete these only if you want more depth after finishing the core set.

## Problem 1.31 — Momentum conservation implies the third law

### Purpose

Study the logical converse of the usual momentum-conservation derivation.

### Central question

If the momentum of every isolated two-particle system is conserved, can you derive

\[
\mathbf F_{12}=-\mathbf F_{21}?
\]

### Notes

---

## Problem 1.45 — Constant-magnitude vector

### Purpose

Show the geometric relationship between constant magnitude and perpendicular time derivative.

### Goal

Prove

\[
|\mathbf v|=\text{constant}
\quad\Longleftrightarrow\quad
\mathbf v\cdot\dot{\mathbf v}=0.
\]

### Hint

Differentiate

\[
\mathbf v\cdot\mathbf v.
\]

### Notes

---

## Problem 1.46 — Rotating reference frame

### Purpose

Describe the same free motion from both an inertial frame and a rotating frame.

### Notes

---

## Problem 1.47 — Cylindrical-coordinate extension

### Purpose

Extend the polar-coordinate velocity and acceleration derivation into three dimensions.

### Notes

---

# Final Chapter 1 Completion Checklist

## Problems

- [ ] 1.10 completed
- [ ] 1.24 completed
- [ ] 1.26 completed
- [ ] 1.28 completed
- [ ] 1.38 completed
- [ ] 1.43 completed
- [ ] 1.41 completed
- [ ] 1.50 computational notebook completed

## Derivations

- [ ] Constant-force initial-value problem
- [ ] \(N\)-particle momentum conservation
- [ ] Polar basis-vector derivatives
- [ ] Polar velocity and acceleration
- [ ] Exact skateboard equation
- [ ] Small-angle approximation and period

## Mastery standard

I am ready to move on when I can:

- explain inertial frames clearly;
- distinguish internal and external forces;
- derive momentum conservation;
- choose effective Cartesian coordinates;
- derive polar velocity and acceleration from scratch;
- recover circular motion as a special case;
- derive the nonlinear skateboard equation;
- explain when and why the small-angle approximation works.
