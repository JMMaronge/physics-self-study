# Chapter 1 — Newton's Laws of Motion

**Text:** John R. Taylor, *Classical Mechanics*  
**Dates studied:**  
**Status:** In progress  
**Problems completed:**  

---

## How to use these notes

Do not try to copy the chapter. Use this file to record:

- the ideas you need to remember;
- derivations you can reproduce;
- assumptions behind the equations;
- physical interpretations;
- questions and mistakes;
- connections to later mechanics and statistics.

The detailed problem checklist and derivation workspaces are in
[`problems-and-derivations.md`](problems-and-derivations.md).

---

# 1. Chapter purpose

## One-sentence summary

> Write one sentence explaining what Chapter 1 accomplishes.

## My current interpretation

This chapter establishes the basic objects and assumptions of Newtonian
mechanics and shows how physical forces are converted into differential
equations for motion.

## What was review?

- 
- 
- 

## What was genuinely new or rusty?

- 
- 
- 

---

# 2. Learning objectives

By the end of the chapter, I should be able to:

- [ ] Explain the domain in which classical mechanics is appropriate.
- [ ] Define position, velocity, and acceleration as vectors.
- [ ] Differentiate vectors written in a fixed Cartesian basis.
- [ ] Explain the physical meaning of mass and force.
- [ ] State Newton's three laws precisely.
- [ ] Explain why Newton's first law defines inertial frames.
- [ ] Treat Newton's second law as a differential equation.
- [ ] Explain the role of initial conditions.
- [ ] Derive conservation of momentum for an isolated system.
- [ ] Distinguish internal forces from external forces.
- [ ] Choose useful Cartesian coordinates.
- [ ] Derive velocity and acceleration in two-dimensional polar coordinates.
- [ ] Interpret every term in the polar acceleration formula.
- [ ] Derive the nonlinear skateboard equation.
- [ ] Explain and test the small-angle approximation.

---

# 3. Section notes

## 1.1 Classical Mechanics

### Central idea

What does Taylor mean by classical mechanics?

### Three formulations

- Newtonian:
- Lagrangian:
- Hamiltonian:

### Relationship among them

Explain why these are alternative formulations of the same mechanics.

### Domain of validity

Classical mechanics works well when:

- 
- 

It becomes inadequate when:

- 
- 

### My takeaway

> Why does Taylor begin with the Newtonian formulation?

---

## 1.2 Space and Time

### Position

\[
\mathbf r(t)
=
x(t)\hat{\mathbf x}
+y(t)\hat{\mathbf y}
+z(t)\hat{\mathbf z}.
\]

### Velocity and acceleration

\[
\mathbf v
=
\frac{d\mathbf r}{dt},
\qquad
\mathbf a
=
\frac{d\mathbf v}{dt}
=
\frac{d^2\mathbf r}{dt^2}.
\]

In Cartesian coordinates,

\[
\mathbf v
=
\dot x\hat{\mathbf x}
+\dot y\hat{\mathbf y}
+\dot z\hat{\mathbf z}.
\]

### Why Cartesian differentiation is simple

> The Cartesian basis vectors are fixed in time.

### Scalar product

\[
\mathbf a\cdot\mathbf b
=
ab\cos\theta.
\]

Geometric meaning:

Important uses:

- 
- 

### Vector product

\[
\mathbf a\times\mathbf b
=
\]

Geometric meaning:

Important uses:

- 
- 

### Reference frames

A reference frame specifies:

- 
- 
- 

Why can a good choice of frame simplify a problem?

### Classical time

What assumption does classical mechanics make about time?

### Questions

- 
- 

---

## 1.3 Mass and Force

### Mass

My physical interpretation:

> Mass measures resistance to acceleration.

How could two masses be compared operationally?

### Force

My physical interpretation:

How could force be measured operationally?

### Net force

\[
\mathbf F_{\mathrm{net}}
=
\sum_i \mathbf F_i.
\]

### Force-identification checklist

For the object of interest:

1. What objects touch it?
2. What contact forces can they exert?
3. What long-range forces act on it?
4. Which apparent forces act on some other object?
5. Have I included the direction of every force?

### Common forces

| Force | Typical form | Direction |
|---|---:|---|
| Weight | \(m\mathbf g\) | Downward |
| Normal force | \(N\) | Perpendicular to a surface |
| Kinetic friction | \(f_k=\mu_kN\) | Opposite relative motion |
| Tension | \(T\) | Along a string or cable |
| Spring force | \(-k\mathbf x\) | Toward equilibrium |

### My takeaway

> What is the difference between defining force and determining a
> particular force law?

---

## 1.4 Newton's First and Second Laws

### Newton's first law

State it in my own words:

### Newton's second law

\[
\mathbf F_{\mathrm{net}}
=
m\mathbf a.
\]

For constant mass,

\[
\mathbf F_{\mathrm{net}}
=
\frac{d\mathbf p}{dt},
\qquad
\mathbf p=m\mathbf v.
\]

### Why the first law is not redundant

Setting \(\mathbf F=0\) in the second law appears to give
\(\mathbf a=0\), but this statement is only valid in an inertial frame.

### Inertial frame

My definition:

\[
\mathbf F_{\mathrm{net}}=0
\quad\Longrightarrow\quad
\mathbf v=\text{constant}.
\]

Examples of approximately inertial frames:

- 

Examples of noninertial frames:

- 
- 

### Newton's second law as a differential equation

\[
m\ddot{\mathbf r}(t)
=
\mathbf F(\mathbf r,\dot{\mathbf r},t).
\]

The unknown is:

\[
\mathbf r(t).
\]

A second-order equation normally requires:

\[
\mathbf r(0)=\mathbf r_0,
\qquad
\dot{\mathbf r}(0)=\mathbf v_0.
\]

### Constant-force warm-up

Starting equation:

\[
m\ddot x=F_0.
\]

First integration:

\[
\dot x(t)=
\]

Second integration:

\[
x(t)=
\]

How do the initial conditions determine the constants?

### My takeaway

> A mechanics problem consists of identifying the force law, constructing
> the differential equation, and solving it subject to initial conditions.

---

## 1.5 Newton's Third Law and Momentum Conservation

### Newton's third law

\[
\mathbf F_{12}
=
-\mathbf F_{21}.
\]

Define carefully:

- \(\mathbf F_{12}\):
- \(\mathbf F_{21}\):

### Third-law pair checklist

A third-law pair:

- acts on two different objects;
- comes from the same interaction;
- has equal magnitude;
- points in opposite directions.

### Total momentum

For a system of particles,

\[
\mathbf P
=
\sum_\alpha \mathbf p_\alpha.
\]

The central result is

\[
\boxed{
\frac{d\mathbf P}{dt}
=
\mathbf F_{\mathrm{ext}}
}.
\]

For an isolated system,

\[
\mathbf F_{\mathrm{ext}}=0
\quad\Longrightarrow\quad
\boxed{\mathbf P=\text{constant}}.
\]

### Three-particle cancellation

Write the equations for each particle and show explicitly that

\[
\mathbf F_{12}+\mathbf F_{21}=0,
\]

\[
\mathbf F_{13}+\mathbf F_{31}=0,
\]

\[
\mathbf F_{23}+\mathbf F_{32}=0.
\]

### System boundary

The distinction between internal and external forces depends on:

> How the system is defined.

Example:

### My takeaway

> Momentum conservation concerns the total momentum of a properly defined
> isolated system.

---

## 1.6 Newton's Second Law in Cartesian Coordinates

### Component equations

\[
F_x=m\ddot x,
\qquad
F_y=m\ddot y,
\qquad
F_z=m\ddot z.
\]

### Problem-solving workflow

1. Define the system.
2. Draw a free-body diagram.
3. Choose coordinates.
4. Resolve the forces into components.
5. Write one equation per coordinate.
6. Apply constraints.
7. Solve the equations of motion.
8. Apply initial conditions.
9. Check units and limiting cases.

### Coordinate choice

A useful coordinate system should:

- align with constraints;
- reduce the number of nonzero components;
- exploit symmetry;
- separate independent equations when possible.

### Tilted-board example

Draw the complete free-body diagram.

Forces:

- Weight:
- Normal force:
- Other forces:

Choose:

- \(x\):
- \(y\):

Normal equation:

\[
N-mg\cos\theta=0.
\]

Equations within the board:

\[
m\ddot x=
\]

\[
m\ddot y=
\]

Trajectory:

\[
x(t)=
\]

\[
y(t)=
\]

### Checks

- [ ] Correct units
- [ ] Correct behavior when \(\theta\to0\)
- [ ] Correct initial position
- [ ] Correct initial velocity
- [ ] Clear physical interpretation

---

## 1.7 Two-Dimensional Polar Coordinates

### Coordinate definitions

\[
x=r\cos\phi,
\qquad
y=r\sin\phi.
\]

\[
\mathbf r=r\hat{\mathbf r}.
\]

### Polar basis vectors

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

### Why polar coordinates are different

Unlike Cartesian basis vectors,

\[
\hat{\mathbf r}
\quad\text{and}\quad
\hat{\boldsymbol\phi}
\]

change direction as the particle moves.

### Basis-vector derivatives

\[
\boxed{
\dot{\hat{\mathbf r}}
=
\dot\phi\,\hat{\boldsymbol\phi}
}
\]

\[
\boxed{
\dot{\hat{\boldsymbol\phi}}
=
-\dot\phi\,\hat{\mathbf r}
}
\]

Explain the signs geometrically:

### Velocity

\[
\boxed{
\mathbf v
=
\dot r\,\hat{\mathbf r}
+
r\dot\phi\,\hat{\boldsymbol\phi}
}
\]

Interpret:

- \(\dot r\hat{\mathbf r}\):
- \(r\dot\phi\hat{\boldsymbol\phi}\):

### Acceleration

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

### Interpretation of the terms

| Term | Interpretation |
|---|---|
| \(\ddot r\) | |
| \(-r\dot\phi^2\) | |
| \(r\ddot\phi\) | |
| \(2\dot r\dot\phi\) | |

### Newton's second law in polar form

\[
F_r
=
m\left(\ddot r-r\dot\phi^2\right),
\]

\[
F_\phi
=
m\left(r\ddot\phi+2\dot r\dot\phi\right).
\]

### Special cases

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
\qquad
\dot r=\ddot r=0,
\qquad
\dot\phi=\omega,
\qquad
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
\qquad
\dot r=\ddot r=0.
\]

Then:

\[
\mathbf a=
\]

### Fixed-radius skateboard equation

For \(r=R\),

\[
F_\phi=-mg\sin\phi.
\]

Newton's second law gives

\[
mR\ddot\phi=-mg\sin\phi,
\]

so

\[
\boxed{
\ddot\phi
=
-\frac{g}{R}\sin\phi
}.
\]

Why is this nonlinear?

### Small-angle approximation

For small \(\phi\) in radians,

\[
\sin\phi\approx\phi.
\]

Therefore,

\[
\ddot\phi+\frac{g}{R}\phi=0.
\]

Define

\[
\omega_0^2=\frac{g}{R}.
\]

Then

\[
\phi(t)
=
A\cos(\omega_0t)
+
B\sin(\omega_0t).
\]

The approximate period is

\[
\boxed{
T
=
2\pi\sqrt{\frac{R}{g}}
}.
\]

### Exact versus approximate motion

Exact:

\[
\ddot\phi
=
-\frac{g}{R}\sin\phi.
\]

Approximate:

\[
\ddot\phi
=
-\frac{g}{R}\phi.
\]

What changes as the initial angle increases?

### Connection to later chapters

Why does this calculation motivate generalized coordinates and
Lagrangian mechanics?

---

# 4. Essential derivations

The detailed workspaces are in
[`problems-and-derivations.md`](problems-and-derivations.md).

## Warm-up

- [ ] Constant-force initial-value problem

## Big derivations

- [ ] Momentum conservation for an \(N\)-particle system
- [ ] Polar basis vectors and their derivatives
- [ ] Polar velocity and acceleration
- [ ] Exact skateboard equation
- [ ] Small-angle approximation and oscillation period

## Most important technical result

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

I should be able to derive this rather than only memorize it.

---

# 5. Selected problem set

See [`problems-and-derivations.md`](problems-and-derivations.md) for prompts,
workspaces, and mastery checks.

## Quick diagnostics

- [ ] Problem 1.10 — Circular motion and vector differentiation
- [ ] Problem 1.24 — First-order differential equations

## Core written problems

- [ ] Problem 1.26 — Inertial and noninertial frames
- [ ] Problem 1.28 — Three-particle momentum conservation
- [ ] Problem 1.38 — Tilted Cartesian coordinates
- [ ] Problem 1.43 — Polar basis vectors
- [ ] Problem 1.41 — Uniform circular motion in polar coordinates

## Computational problem

- [ ] Problem 1.50 — Nonlinear motion versus the small-angle approximation

## Optional stretch problems

- [ ] Problem 1.31 — Momentum conservation implies the third law
- [ ] Problem 1.45 — Constant-magnitude vector
- [ ] Problem 1.46 — Rotating frame
- [ ] Problem 1.47 — Cylindrical coordinates

---

# 6. Computational experiment

## Exact skateboard motion versus the small-angle approximation

### Exact model

\[
\ddot\phi
=
-\frac{g}{R}\sin\phi.
\]

### Approximate model

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

### Angles to investigate

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

### Outputs

- [ ] Exact numerical trajectory
- [ ] Small-angle trajectory
- [ ] Comparison plot
- [ ] Estimated exact period
- [ ] Approximate period
- [ ] Relative period error
- [ ] Maximum trajectory difference

### Code location

Put the notebook or script in:

```text
code/
```

Suggested filename:

```text
problem-1-50-skateboard.ipynb
```

or

```text
problem-1-50-skateboard.py
```

Save generated plots in:

```text
figures/
```

### Statistical extension

Treat the initial angle as uncertain and simulate the induced distribution
of the period, maximum speed, and approximation error.

### Interpretation

> Describe the physical result, not merely what the plot looks like.

---

# 7. Mistake and confusion log

| Issue | Why I was confused | Resolution |
|---|---|---|
| | | |
| | | |
| | | |

Questions to revisit:

- Did I confuse velocity with speed?
- Did I combine forces acting on different objects?
- Did I mistake balancing forces for a third-law pair?
- Did I forget that polar basis vectors change with time?
- Did I apply the small-angle approximation without checking the angle?
- Did I apply all required initial conditions?

---

# 8. Connections

## Differential equations

How does the order of an equation determine the number of initial conditions?

## Statistics

What is analogous to:

- a state variable;
- an initial condition;
- a deterministic forward model;
- uncertainty propagation through a model?

## Lagrangian mechanics

Why might generalized coordinates be easier than resolving Newton's law
into polar components?

## Hamiltonian mechanics

Which quantities in this chapter will later become position and momentum
coordinates in phase space?

---

# 9. Final chapter summary

## Five central ideas

1. 
2. 
3. 
4. 
5. 

## Three equations I must know

1. 
2. 
3. 

## Two derivations I must reproduce

1. 
2. 

## One remaining question

1. 

---

# 10. Mastery check

I am ready to move to Chapter 2 when I can:

- [ ] Explain inertial frames without consulting the book.
- [ ] Construct a correct free-body diagram.
- [ ] Convert a force model into differential equations.
- [ ] Explain why initial position and velocity are required.
- [ ] Derive momentum conservation.
- [ ] Choose effective Cartesian coordinates.
- [ ] Derive polar basis-vector derivatives.
- [ ] Derive polar velocity and acceleration from scratch.
- [ ] Explain every term in the polar acceleration formula.
- [ ] Derive the exact skateboard equation.
- [ ] Explain when the small-angle approximation is valid.
- [ ] Complete the selected core problems.
- [ ] Complete the numerical comparison in Problem 1.50.
