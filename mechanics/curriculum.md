# Taylor Mechanics Mastery Map

This document defines what to learn. It is not merely a reading checklist.

Status key:

- `[ ]` not started
- `[-]` in progress
- `[x]` demonstrated

A topic is mastered when you can explain it, derive or reconstruct its principal
results, solve representative problems, and check the answer physically.

---

# Chapter 1 — Newton's Laws of Motion

## 1. Classical mechanics as a model

### Understand
- [ ] State the domain in which classical mechanics is expected to work.
- [ ] Distinguish a physical system from the model used to represent it.
- [ ] Identify assumptions such as point-particle behavior, rigidity, and negligible drag.
- [ ] Explain why an approximation can be useful without being exact.

### Demonstrate
- [ ] Take a physical situation and list the included and neglected effects.
- [ ] Explain how you would determine whether a neglected effect matters.

---

## 2. Space, time, position, velocity, and acceleration

### Understand
- [ ] Distinguish position, displacement, distance, velocity, and speed.
- [ ] Interpret velocity as the time derivative of position.
- [ ] Interpret acceleration as the time derivative of velocity.
- [ ] Move between vector notation and Cartesian components.

### Derive or reconstruct
- [ ] Obtain velocity and acceleration from a given position function.
- [ ] Recover position from velocity using initial conditions.

### Solve
- [ ] One-dimensional motion with a time-dependent acceleration.
- [ ] Two-dimensional motion using independent Cartesian components.

### Math used
- Derivatives and integrals
- Vectors and components
- Initial conditions

---

## 3. Mass and force

### Understand
- [ ] Explain inertial mass operationally.
- [ ] Distinguish individual forces from the net force.
- [ ] Draw a correct free-body diagram.
- [ ] Recognize common force models: gravity, normal force, tension, spring force, drag.

### Demonstrate
- [ ] Translate a verbal description into a free-body diagram and equations of motion.
- [ ] State which body each force acts on and which interaction produces it.

---

## 4. Newton's first and second laws; inertial frames

### Understand
- [ ] State Newton's first and second laws precisely.
- [ ] Explain why the first law identifies inertial frames.
- [ ] Explain why acceleration, not velocity, is determined by net force.
- [ ] Distinguish equilibrium from zero velocity.

### Derive or reconstruct
- [ ] Write Newton's second law as a differential equation.
- [ ] Resolve it into Cartesian components.

### Solve
- [ ] Constant-force motion.
- [ ] Inclined-plane motion.
- [ ] Connected-body or tension problems.
- [ ] A force that depends on time, position, or velocity.

### Checks
- [ ] Units
- [ ] Sign convention
- [ ] Initial conditions
- [ ] Zero-force limit

---

## 5. Newton's third law and momentum conservation

### Understand
- [ ] Identify valid third-law pairs.
- [ ] Explain why third-law forces act on different bodies.
- [ ] Distinguish internal and external forces for a chosen system.
- [ ] Explain how momentum conservation follows for an isolated two-body system.

### Derive or reconstruct
- [ ] Derive conservation of total momentum from Newton's second and third laws.

### Solve
- [ ] Recoil or interaction problems using system momentum.
- [ ] Diagnose when momentum is and is not conserved.

---

## 6. Newton's second law in Cartesian coordinates

### Understand
- [ ] Explain why Cartesian component equations can be solved independently.
- [ ] Choose axes that simplify a problem.
- [ ] Express constraints through component relationships.

### Demonstrate
- [ ] Build and solve a complete component model from a free-body diagram.
- [ ] Reassemble the component solution into vector form.

---

## 7. Polar coordinates

### Understand
- [ ] Interpret the radial and angular unit vectors.
- [ ] Explain why the polar basis vectors change with time.
- [ ] Interpret radial and transverse velocity.
- [ ] Interpret radial and transverse acceleration, including centripetal terms.

### Derive or reconstruct
- [ ] Derive velocity in plane polar coordinates.
- [ ] Derive acceleration in plane polar coordinates.

### Solve
- [ ] Uniform circular motion.
- [ ] Nonuniform circular motion.
- [ ] A problem with changing radius and angle.

### Compute
- [ ] Plot a planar trajectory from prescribed \(r(t)\) and \(\phi(t)\).
- [ ] Numerically compare Cartesian derivatives with the polar formulas.

---

## Chapter 1 mastery test

- [ ] I can construct equations of motion from a physical description.
- [ ] I can explain inertial frames and identify valid third-law pairs.
- [ ] I can derive the polar-coordinate acceleration from a blank page.
- [ ] I have solved at least 8–12 representative problems.
- [ ] I have completed one small computational check.
- [ ] I can explain the chapter's main ideas without referring to the text.

---

# Chapter 2 — Projectiles and Charged Particles

## 1. Modeling resistance forces

### Understand
- [ ] Explain why drag opposes relative motion through a medium.
- [ ] Distinguish linear and quadratic drag laws.
- [ ] Identify the regimes in which each is plausible.
- [ ] Recognize drag coefficients as model parameters rather than universal constants.

### Demonstrate
- [ ] Write the vector drag force and its component equations.
- [ ] State the assumptions behind a chosen drag model.

---

## 2. Linear air resistance in one dimension

### Understand
- [ ] Interpret the characteristic time \(\tau=m/b\).
- [ ] Interpret terminal speed as a dynamical equilibrium.
- [ ] Describe transient and long-time behavior.

### Derive or reconstruct
- [ ] Solve \(m\,dv/dt=mg-bv\) with an arbitrary initial velocity.
- [ ] Integrate velocity to obtain position.
- [ ] Recover the no-drag limit.
- [ ] Recover terminal velocity in the long-time limit.

### Solve
- [ ] Falling from rest.
- [ ] Throwing an object vertically upward.
- [ ] Finding time, velocity, or distance under linear drag.

### Compute
- [ ] Plot velocity and position for several values of \(\tau\).
- [ ] Verify the analytical solution with a numerical ODE solver.

---

## 3. Projectile motion with linear drag

### Understand
- [ ] Explain why horizontal and vertical equations differ.
- [ ] Describe how drag changes height, range, flight time, and trajectory symmetry.
- [ ] Explain why the trajectory is no longer a parabola.

### Derive or reconstruct
- [ ] Derive \(v_x(t)\) and \(v_y(t)\).
- [ ] Derive \(x(t)\) and \(y(t)\).
- [ ] Apply launch initial conditions correctly.

### Solve
- [ ] Determine the trajectory parametrically.
- [ ] Find flight time or range numerically when an explicit expression is unavailable.
- [ ] Compare with the vacuum result.

### Compute
- [ ] Plot vacuum and linear-drag trajectories together.
- [ ] Explore sensitivity to launch angle, speed, mass, and drag coefficient.
- [ ] Numerically determine the range-maximizing launch angle.

---

## 4. Quadratic air resistance

### Understand
- [ ] Explain why the force direction must oppose the velocity vector.
- [ ] Interpret terminal speed under quadratic drag.
- [ ] Explain why two-dimensional quadratic drag usually requires numerical work.

### Derive or reconstruct
- [ ] Solve the one-dimensional downward-fall equation.
- [ ] Identify the appropriate hyperbolic-function form or equivalent expression.
- [ ] Check initial and terminal limits.

### Solve
- [ ] Vertical fall under quadratic drag.
- [ ] Set up, but not necessarily solve analytically, the two-dimensional equations.

### Compute
- [ ] Numerically solve a two-dimensional quadratic-drag trajectory.
- [ ] Compare vacuum, linear-drag, and quadratic-drag models.
- [ ] Investigate how model choice changes optimal launch angle.

---

## 5. Charged-particle motion in a uniform magnetic field

### Understand
- [ ] Explain why the magnetic force does no work.
- [ ] Explain why speed remains constant while direction changes.
- [ ] Relate charge sign to direction of rotation.
- [ ] Identify cyclotron frequency and orbit radius.

### Derive or reconstruct
- [ ] Write the Cartesian component equations from the Lorentz force.
- [ ] Derive circular motion for velocity perpendicular to the field.
- [ ] Derive helical motion when a parallel velocity component is present.

### Solve
- [ ] Determine radius, angular frequency, period, and handedness.
- [ ] Determine a trajectory from initial position and velocity.

### Compute
- [ ] Simulate trajectories for positive and negative charges.
- [ ] Confirm constant speed numerically.
- [ ] Visualize circular and helical trajectories.

---

## 6. Complex exponentials as a mechanics tool

### Understand
- [ ] Use Euler's formula to connect complex exponentials with sine and cosine.
- [ ] Explain why complex notation can combine coupled real equations.
- [ ] Extract real physical quantities from a complex solution.

### Demonstrate
- [ ] Solve the planar magnetic-motion equations using \(v_x+i v_y\).
- [ ] Translate the complex solution back into real components.

---

## Chapter 2 mastery test

- [ ] I can derive the complete linear-drag projectile solution.
- [ ] I can explain terminal velocity physically and mathematically.
- [ ] I can formulate quadratic drag for numerical solution.
- [ ] I can derive charged-particle motion in a uniform magnetic field.
- [ ] I have solved at least 10–15 representative problems.
- [ ] I have produced one validated notebook comparing analytical and numerical results.

---

# Chapter 3 — Momentum and Angular Momentum

## 1. Momentum conservation for many-particle systems

### Understand
- [ ] Define total momentum for a system.
- [ ] Separate internal and external forces.
- [ ] State the conditions for momentum conservation.
- [ ] Explain why system choice matters.

### Derive or reconstruct
- [ ] Derive \(d\mathbf{P}/dt=\mathbf{F}_{\mathrm{ext}}\).
- [ ] Show the cancellation of internal forces under Newton's third law.

### Solve
- [ ] Explosion and recoil problems.
- [ ] Collisions where momentum is conserved.
- [ ] Problems with a nonzero external impulse.

---

## 2. Rockets and variable-mass systems

### Understand
- [ ] Explain why naïvely writing \(F=m\,dv/dt\) can fail for a variable-mass system.
- [ ] Define exhaust velocity carefully, including sign conventions.
- [ ] Interpret the logarithmic dependence of speed change on mass ratio.

### Derive or reconstruct
- [ ] Derive the ideal rocket equation from momentum balance.
- [ ] Include an external force such as gravity.
- [ ] State the assumptions behind the ideal result.

### Solve
- [ ] Find speed change from a mass ratio.
- [ ] Find required fuel fraction.
- [ ] Analyze a vertically rising rocket with gravity.

### Compute
- [ ] Plot achievable \(\Delta v\) against mass ratio.
- [ ] Simulate a rocket with prescribed burn rate and gravity.

---

## 3. Center of mass

### Understand
- [ ] Define center of mass for discrete and continuous systems.
- [ ] Explain why the center of mass responds only to net external force.
- [ ] Relate total momentum to center-of-mass velocity.
- [ ] Separate center-of-mass motion from internal motion.

### Derive or reconstruct
- [ ] Derive \(\mathbf{P}=M\mathbf{V}_{\mathrm{cm}}\).
- [ ] Derive \(M\mathbf{A}_{\mathrm{cm}}=\mathbf{F}_{\mathrm{ext}}\).

### Solve
- [ ] Center of mass of discrete masses.
- [ ] Center of mass of rods, plates, or other continuous bodies.
- [ ] Motion of interacting particles through center-of-mass coordinates.

### Compute
- [ ] Animate particles together with their center of mass.
- [ ] Numerically verify uniform center-of-mass motion in an isolated system.

---

## 4. Angular momentum of one particle

### Understand
- [ ] Define angular momentum about a chosen origin.
- [ ] Define torque about the same origin.
- [ ] Explain the geometric meaning of the cross product.
- [ ] State when angular momentum is conserved.
- [ ] Explain origin dependence.

### Derive or reconstruct
- [ ] Derive \(d\mathbf{L}/dt=\boldsymbol{\tau}\).
- [ ] Show why a central force produces zero torque about the force center.

### Solve
- [ ] Compute angular momentum and torque using components.
- [ ] Analyze motion under a central force.
- [ ] Use conservation of angular momentum to relate radius and speed.

---

## 5. Angular momentum of many-particle systems

### Understand
- [ ] Define total angular momentum.
- [ ] Separate internal and external torques.
- [ ] State conditions under which internal torques cancel.
- [ ] Decompose total angular momentum into center-of-mass and internal pieces.

### Derive or reconstruct
- [ ] Derive \(d\mathbf{L}_{\mathrm{tot}}/dt=\boldsymbol{\tau}_{\mathrm{ext}}\).
- [ ] Derive or explain the center-of-mass decomposition.

### Solve
- [ ] Multi-particle conservation problems.
- [ ] Orbital-angular-momentum problems.
- [ ] Problems where the choice of origin matters.

### Compute
- [ ] Verify linear and angular momentum conservation in a particle simulation.
- [ ] Track numerical conservation error across time-step choices.

---

## Chapter 3 mastery test

- [ ] I can derive the many-particle momentum equation.
- [ ] I can derive the rocket equation with a consistent sign convention.
- [ ] I can explain center-of-mass motion independently of internal details.
- [ ] I can derive the torque-angular-momentum relation.
- [ ] I have solved at least 10–15 representative problems.
- [ ] I have numerically checked conservation laws in at least one simulation.
