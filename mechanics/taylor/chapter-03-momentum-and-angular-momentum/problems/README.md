# Taylor, Chapter 3 — Selected Problems

**Text:** John R. Taylor, *Classical Mechanics*  
**Chapter:** 3 — Momentum and Angular Momentum  
**Purpose:** A non-repetitive homework set chosen for conceptual coverage and progression  
**Companion notes:** `Taylor_Chapter_3_Notes.md`

> Use Taylor's text for the complete problem statements. The descriptions below explain why each problem was selected and what the finished solution should demonstrate; they are not substitutes for the book.

---

# 1. Selection philosophy

The core set contains ten problems. It is meant to function like a serious upper-level mechanics assignment rather than an attempt to complete every exercise.

The sequence moves through:

1. vector momentum conservation;
2. momentum plus kinetic-energy conservation;
3. variable-mass motion;
4. center-of-mass geometry and dynamics;
5. computational verification;
6. angular momentum and central-force motion;
7. a final synthesis involving translation, rotation, and choice of origin.

The optional problems deepen a topic without being necessary for basic Chapter 3 mastery.

---

# 2. Standard solution format

For each problem:

1. **Define the system.** State what objects or mass elements are included.
2. **Choose the frame and coordinates.** Identify relative velocities explicitly.
3. **State the governing law in vector form.** Use momentum, impulse, center-of-mass motion, or angular momentum.
4. **Explain conservation.** Name the external force or torque that vanishes or is negligible.
5. **Solve symbolically before substituting numbers.**
6. **Check the result.** Use dimensions, symmetry, limits, initial conditions, or a special case.
7. **Interpret the physics in one or two sentences.**

For angular-momentum problems, always name the origin.

---

# 3. Core problem set

## Problem 3.1 — Gun recoil and relative velocity

**Role:** Quick diagnostic  
**Main skill:** Momentum conservation when the given muzzle speed is relative to the gun

### Why this problem is included

This is a compact test of system choice, signs, and reference frames. The main danger is inserting the shell's gun-relative speed directly into a ground-frame momentum equation.

### Your solution should include

- [ ] Gun plus shell as the system.
- [ ] A stated positive direction.
- [ ] Separate ground-frame velocities for the gun and shell.
- [ ] The relation between muzzle speed and those two velocities.
- [ ] A limiting check when $M\gg m$.

### Reflection

Why does the shell's ground speed differ from its muzzle speed?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.5 — Equal-mass elastic collision

**Role:** Conceptual vector proof  
**Main skill:** Combining vector momentum conservation with scalar kinetic-energy conservation

### Why this problem is included

This problem shows that momentum and energy supply different information. It also produces a geometric conclusion—perpendicular outgoing velocities—without solving a long system component by component.

### Your solution should include

- [ ] The vector momentum equation.
- [ ] The scalar kinetic-energy equation.
- [ ] A dot-product or squared-magnitude step.
- [ ] A clear proof that the final velocity vectors are perpendicular.
- [ ] An explanation of why the conclusion depends on equal masses and elasticity.

### Reflection

Which step would fail for an inelastic collision?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.7 — Space-shuttle rocket estimate

**Role:** First rocket calculation  
**Main skill:** Applying the ideal rocket equation and estimating thrust

### Why this problem is included

This problem makes the logarithmic mass-ratio law concrete and forces comparison of thrust with weight. It is a useful bridge from the formal derivation to physical scale.

### Your solution should include

- [ ] Identification of initial and final mass.
- [ ] Application of $\Delta v=v_{\mathrm{ex}}\ln(m_i/m_f)$.
- [ ] Calculation of the average mass-loss rate.
- [ ] Calculation of thrust from $-\dot m v_{\mathrm{ex}}$.
- [ ] Comparison of thrust with initial Earth weight.
- [ ] A note that the free-space speed ignores gravity and atmospheric drag.

### Reflection

Why is the thrust approximately constant in this model while the acceleration is not?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.11 — Rocket motion with gravity

**Role:** Essential derivation  
**Main skill:** Extending the rocket equation to include an external force

### Why this problem is included

This is the most important rocket problem in the chapter. It combines momentum flux, a changing mass, gravity, separation of variables, and physical interpretation of the lift-off condition.

### Your solution should include

- [ ] Derivation of $m\dot v=-\dot m v_{\mathrm{ex}}+F_{\mathrm{ext}}$.
- [ ] A clearly stated upward-positive convention.
- [ ] Substitution of $m(t)=m_0-kt$.
- [ ] Integration using the initial condition.
- [ ] Comparison with the free-space result.
- [ ] Explanation of what occurs when initial thrust is smaller than weight.

### Required checks

- [ ] $v(0)=0$.
- [ ] The $g\to0$ limit gives the ideal rocket result.
- [ ] The derivative at $t=0$ has the physically expected sign.

### Reflection

Why does gravity produce a term proportional to elapsed time while the rocket contribution depends on a mass ratio?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.18 — Geometry of the two-particle center of mass

**Role:** Short proof  
**Main skill:** Interpreting the vector definition of center of mass

### Why this problem is included

The formulas for center of mass are easy to use mechanically. This proof makes their geometry explicit: the center of mass lies on the joining line and divides it in the inverse ratio of the masses.

### Your solution should include

- [ ] The center-of-mass vector for two particles.
- [ ] The vector from either particle to the center of mass.
- [ ] Proof of collinearity.
- [ ] The ratio of the two distances.
- [ ] Interpretation when one mass is much larger.

### Reflection

Why is the center of mass closer to the larger mass?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.19 — Exploding projectile

**Role:** Core conceptual application  
**Main skill:** Separating center-of-mass motion from fragment motion

### Why this problem is included

This is one of the clearest demonstrations that violent internal motion does not alter center-of-mass motion. It also tests the boundary of the argument when fragments land at different times.

### Your solution should include

- [ ] The external force on the complete fragment system while airborne.
- [ ] The center-of-mass trajectory after the explosion.
- [ ] The equal-mass position relation at the stated landing time.
- [ ] A careful answer to the different-landing-time part.
- [ ] Identification of the new external force after a fragment hits the ground.

### Reflection

At exactly what point does the simple parabolic center-of-mass argument cease to apply?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.23 — Computational exploding-grenade trajectory

**Role:** Required computational problem  
**Main skill:** Numerically visualizing center-of-mass invariance

### Why this problem is included

This is the computational counterpart of Problem 3.19. The plot should make a system-level conservation statement visually obvious while the two fragments follow different trajectories.

### Deliverable

Create `taylor_problem_3_23.ipynb` with:

- [ ] A brief Markdown statement of the model and assumptions.
- [ ] The intact projectile trajectory through the explosion time.
- [ ] Momentum-based calculation of the second fragment's velocity.
- [ ] Both fragment trajectories after the explosion.
- [ ] Position markers at the times requested by Taylor.
- [ ] The center-of-mass trajectory plotted separately or overlaid.
- [ ] A numerical check that the fragment CM agrees with the unbroken trajectory.

### Good coding practice

- Use named variables for initial velocity, gravity, and explosion time.
- Write a small function for projectile position after arbitrary initial conditions.
- Keep the physics derivation in Markdown rather than hiding it in code.
- Report the maximum numerical discrepancy in the CM check.

### Reflection

What does the plot reveal more clearly than the algebra alone?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.26 — Central force and planar motion

**Role:** Essential conceptual proof  
**Main skill:** Connecting zero torque, constant angular momentum, and orbital geometry

### Why this problem is included

This is the conceptual foundation for Chapter 8. The important result is not merely that angular momentum is conserved, but that a constant angular-momentum direction confines the orbit to a plane.

### Your solution should include

- [ ] A stated origin at the force center.
- [ ] Proof that the torque about that origin vanishes.
- [ ] The conclusion that $\mathbf L$ is constant in magnitude and direction.
- [ ] A geometrical explanation of why $\mathbf r$ and $\mathbf v$ remain in one plane.
- [ ] Treatment of the special case $\mathbf L=\mathbf 0$.

### Reflection

Why does a three-dimensional position vector still lead to a two-dimensional orbit?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.27 — Kepler's second law

**Role:** Central derivation  
**Main skill:** Translating angular-momentum conservation into an observable geometrical law

### Why this problem is included

This problem links the polar-coordinate work from Chapter 1 to angular momentum and previews central-force dynamics. It also separates what follows from a central force from what requires the inverse-square law.

### Your solution should include

- [ ] Derivation of $L=mr^2\dot\phi$.
- [ ] Derivation of $dA/dt=r^2\dot\phi/2$.
- [ ] The relation $dA/dt=L/(2m)$.
- [ ] A clear statement of Kepler's second law.
- [ ] An explanation of why the inverse-square form is unnecessary here.

### Reflection

If a planet is nearer the Sun, why must its angular speed be larger?

> 

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

## Problem 3.35 — Disk rolling down an incline

**Role:** Capstone synthesis  
**Main skill:** Choosing an angular-momentum origin strategically and reconciling two valid solution routes

### Why this problem is included

This is the chapter's best synthesis problem. It combines a free-body diagram, translation of the center of mass, torque, moment of inertia, the no-slip constraint, and two different choices of origin.

### Your solution should include

- [ ] A clear free-body diagram.
- [ ] A stated positive direction along the incline.
- [ ] A solution using angular momentum about the contact point.
- [ ] A second solution using torque about the center of mass plus translation.
- [ ] Use of the no-slip relation with consistent signs.
- [ ] Agreement of the two accelerations.
- [ ] The direction and role of static friction.

### Required interpretation

Explain why choosing the contact point eliminates the torque from friction and the normal force, but does not mean those forces are absent.

> 

### Checks

- [ ] Acceleration has the dimensions of $g$.
- [ ] Acceleration is smaller than $g\sin\theta$.
- [ ] Both origin choices give the same physical result.

**Status:** [ ] Not started [ ] Attempted [ ] Checked [ ] Polished

---

# 4. Optional and stretch problems

## Problem 3.12 — Multistage rocket

**Why do it:** Builds intuition for why discarding empty structure increases attainable $\Delta v$.

**Recommended if:** The logarithmic mass-ratio structure still feels formal after Problems 3.7 and 3.11.

**Status:** [ ] Optional

---

## Problem 3.21 — Center of mass of a semicircular lamina

**Why do it:** Provides a clean continuous center-of-mass integral in polar coordinates.

**Recommended if:** You want more practice with $dm=\sigma r\,dr\,d\phi$ and symmetry.

**Status:** [ ] Optional

---

## Problem 3.30 — Derive $L_z=I\omega$

**Why do it:** Makes the fixed-axis relation emerge from the particle definition rather than treating it as a memorized formula.

**Recommended if:** The transition from particle angular momentum to rigid-body notation feels too abrupt.

**Status:** [ ] Optional

---

## Problem 3.31 — Moment of inertia of a disk

**Why do it:** Reinforces the meaning of $I=\int\rho^2\,dm$ using a polar-coordinate integral.

**Recommended if:** You have not recently derived standard moments of inertia yourself.

**Status:** [ ] Optional

---

## Problem 3.37 — Angular momentum about an accelerating center of mass

**Why do it:** Proves the subtle result that $\dot{\mathbf L}_{\mathrm{CM}}=\boldsymbol\tau^{\mathrm{ext}}_{\mathrm{CM}}$ even when the center of mass accelerates.

**Recommended if:** You want the most theoretically important stretch problem in the chapter.

**Status:** [ ] Stretch

---

# 5. Suggested schedule

## Block A — Linear momentum

- Read Sections 3.1–3.2.
- Do Problems 3.1 and 3.5.
- Reproduce the many-particle momentum proof.
- Do Problems 3.7 and 3.11.

## Block B — Center of mass

- Read Section 3.3.
- Do Problems 3.18 and 3.19.
- Build the notebook for Problem 3.23.
- Add Problem 3.21 only if the continuous integral needs reinforcement.

## Block C — Angular momentum

- Read Sections 3.4–3.5.
- Do Problems 3.26 and 3.27.
- Reproduce the internal-torque cancellation proof.
- Finish with Problem 3.35.
- Add Problems 3.30, 3.31, or 3.37 as needed.

---

# 6. Homework grading rubric

These solutions should be assessed as homework for an upper-level classical-mechanics course, not as publication-ready exposition.

| Criterion | Weight |
|---|---:|
| Correct physical setup and system choice | 30% |
| Correct governing conservation law or equation | 25% |
| Mathematical execution | 25% |
| Physical interpretation and checks | 15% |
| Clear enough notation to follow the reasoning | 5% |

Full credit is appropriate when the physics and mathematics are correct. Minor notation or presentation issues should be comments rather than deductions unless they create consequential ambiguity or lead to an incorrect result.

---

# 7. Progress tracker

| Problem | Topic | First attempt | Checked | Polished | Revisit |
|---|---|---:|---:|---:|---:|
| 3.1 | Recoil and relative velocity | [ ] | [ ] | [ ] | [ ] |
| 3.5 | Elastic collision geometry | [ ] | [ ] | [ ] | [ ] |
| 3.7 | Rocket estimate and thrust | [ ] | [ ] | [ ] | [ ] |
| 3.11 | Rocket with gravity | [ ] | [ ] | [ ] | [ ] |
| 3.18 | Two-body center of mass | [ ] | [ ] | [ ] | [ ] |
| 3.19 | Exploding projectile | [ ] | [ ] | [ ] | [ ] |
| 3.23 | Computational CM trajectory | [ ] | [ ] | [ ] | [ ] |
| 3.26 | Central force and plane | [ ] | [ ] | [ ] | [ ] |
| 3.27 | Kepler's second law | [ ] | [ ] | [ ] | [ ] |
| 3.35 | Rolling disk synthesis | [ ] | [ ] | [ ] | [ ] |

---

# 8. End-of-chapter self-test

Do this before moving to Chapter 4.

## Explain

- [ ] I can explain why total momentum ignores internal forces.
- [ ] I can explain why the rocket equation requires momentum flux.
- [ ] I can explain why an explosion leaves the CM trajectory unchanged.
- [ ] I can explain how angular momentum depends on the origin.
- [ ] I can explain why central force implies planar motion.
- [ ] I can explain the extra assumption needed for internal torques to cancel.

## Derive

- [ ] $\dot{\mathbf P}=\mathbf F_{\mathrm{ext}}$.
- [ ] $\Delta v=v_{\mathrm{ex}}\ln(m_i/m_f)$.
- [ ] $M\ddot{\mathbf R}=\mathbf F_{\mathrm{ext}}$.
- [ ] $\dot{\mathbf L}=\boldsymbol\tau$.
- [ ] $dA/dt=L/(2m)$.

## Apply

- [ ] I can distinguish relative and inertial-frame velocities.
- [ ] I can decide whether momentum or angular momentum is conserved.
- [ ] I can choose an origin that simplifies a torque calculation.
- [ ] I can separate center-of-mass and relative motion.
- [ ] I can verify a conservation claim computationally.

## Chapter complete when

- [ ] All ten core problems have honest first attempts.
- [ ] Incorrect solutions have been revised in a different color or clearly annotated.
- [ ] At least three important derivations can be reproduced without the book.
- [ ] The computational notebook runs from top to bottom.
- [ ] I can explain the chapter's structure aloud without relying on formulas alone.
