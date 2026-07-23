# Chapter 1 — Newton's Laws of Motion

**Text:** John R. Taylor, *Classical Mechanics*  
**Dates studied:**  
**Status:** In progress  

---

## How to use this file

This is the **notes and derivations sheet** for Chapter 1.

Use it to record:

- the chapter's main ideas;
- definitions and assumptions;
- physical interpretations;
- derivations you should be able to reproduce;
- questions, mistakes, and connections.

The separate exercise sheet is:

[`problems.md`](problems.md)

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

- Mechanics is the study of how things move. Classical mechanics generally means the mechanics derived by Newton, Lagrange, and Hamilton. From 1905-1925 it became clear that these mechanics fail when things are very small or move close to the speed of light. Classical mechanics generally means mechanics not including those domains

### Three formulations

- Newtonian: 1642-1727
- Lagrangian: 1736-1813
- Hamiltonian: 1805-1865

### Relationship among them

Explain why these are alternative formulations of the same mechanics.

Lagrangian and Hamiltonian Mechanics are equivalent to Newtonian, but can be much simpler for certain problems

### Domain of validity

Classical mechanics works well when:

- We are not dealing with atoms and other small things 
-  When we are not moving close to the speed of light


### My takeaway

> Why does Taylor begin with the Newtonian formulation?

It is the one most are familiar with and it came first

---

## 1.2 Space and Time

### Position

```math
\mathbf r(t)
=
x(t)\hat{\mathbf x}
+y(t)\hat{\mathbf y}
+z(t)\hat{\mathbf z}.
```

### Velocity and acceleration

```math
\mathbf v
=
\frac{d\mathbf r}{dt},
\qquad
\mathbf a
=
\frac{d\mathbf v}{dt}
=
\frac{d^2\mathbf r}{dt^2}.
```

In Cartesian coordinates,

```math
\mathbf v
=
\dot x\hat{\mathbf x}
+\dot y\hat{\mathbf y}
+\dot z\hat{\mathbf z}.
```

> Why Cartesian differentiation is simple

The Cartesian basis vectors are fixed in time.

### Scalar product

```math
\mathbf a\cdot\mathbf b
=
ab\cos\theta.
```

Geometric meaning: The scalar magnitude of 2 vectors

Important uses:

- If a force acts on an object through a small displacement, the work is the dot product
- the square root of a dot product of a vector with itself gives the magmitude of the vector

### Vector product

```math
\mathbf a\times\mathbf b
=
```

Geometric meaning: The cross product creates a vector perpindicular to each of the vectors we began with

Important uses:

- Rotational Motion
- 

### Reference frames

A reference frame specifies:

- Spacial origin
- Temporal origin
- Orientation

> Why can a good choice of frame simplify a problem?

If we have a block sliding down a plane, leveling the horizontal axis on the plane means the block move in the direction of are horizontal unit vector 

### Classical time

What assumption does classical mechanics make about time?

### Questions

- Not sure about the question about time above


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

```math
\mathbf F_{\mathrm{net}}
=
\sum_i \mathbf F_i.
```

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
| Weight | $m\mathbf g$ | Downward |
| Normal force | $N$ | Perpendicular to a surface |
| Kinetic friction | $f_k=\mu_kN$ | Opposite relative motion |
| Tension | $T$ | Along a string or cable |
| Spring force | $-k\mathbf x$ | Toward equilibrium |

### My takeaway

> What is the difference between defining force and determining a particular force law? 

Still confused about this

---

## 1.4 Newton's First and Second Laws

### Newton's first law

State it in my own words: an object in motion will stay in the exact same motion unless acted on by a force

### Newton's second law

```math
\mathbf F_{\mathrm{net}}
=
m\mathbf a.
```

For constant mass,

```math
\mathbf F_{\mathrm{net}}
=
\frac{d\mathbf p}{dt},
\qquad
\mathbf p=m\mathbf v.
```

### Why the first law is not redundant

Setting $\mathbf F=0$ in the second law appears to give
$\mathbf a=0$, but this statement is only valid in an inertial frame.

### Inertial frame

My definition:

```math
\mathbf F_{\mathrm{net}}=0
\quad\Longrightarrow\quad
\mathbf v=\text{constant}.
```

Examples of approximately inertial frames:

- Watching the ice puck slide on the floor of a train

Examples of noninertial frames:

- Being in another train that is accelerating
- Being on a merry-go-round as the puck moves in a straight line

### Newton's second law as a differential equation

```math
m\ddot{\mathbf r}(t)
=
\mathbf F(\mathbf r,\dot{\mathbf r},t).
```

The unknown is:

```math
\mathbf r(t).
```

A second-order equation normally requires:

```math
\mathbf r(0)=\mathbf r_0,
\qquad
\dot{\mathbf r}(0)=\mathbf v_0.
```

### My takeaway

> A mechanics problem consists of identifying the force law, constructing
> the differential equation, and solving it subject to initial conditions.

---

## 1.5 Newton's Third Law and Momentum Conservation

### Newton's third law

```math
\mathbf F_{12}
=
-\mathbf F_{21}.
```

Define carefully:

- $\mathbf F_{12}$:
- $\mathbf F_{21}$:

### Third-law pair checklist

A third-law pair:

- acts on two different objects;
- comes from the same interaction;
- has equal magnitude;
- points in opposite directions.

### Total momentum

For a system of particles,

```math
\mathbf P
=
\sum_\alpha \mathbf p_\alpha.
```

The central result is

```math
\boxed{
\frac{d\mathbf P}{dt}
=
\mathbf F_{\mathrm{ext}}
}.
```

For an isolated system,

```math
\mathbf F_{\mathrm{ext}}=0
\quad\Longrightarrow\quad
\boxed{\mathbf P=\text{constant}}.
```

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

```math
F_x=m\ddot x,
\qquad
F_y=m\ddot y,
\qquad
F_z=m\ddot z.
```

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

- $x$:
- $y$:

Normal equation:

```math
N-mg\cos\theta=0.
```

Equations within the board:

```math
m\ddot x=
```

```math
m\ddot y=
```

Trajectory:

```math
x(t)=
```

```math
y(t)=
```

### Checks

- [ ] Correct units
- [ ] Correct behavior when $\theta\to0$
- [ ] Correct initial position
- [ ] Correct initial velocity
- [ ] Clear physical interpretation

---

## 1.7 Two-Dimensional Polar Coordinates

### Coordinate definitions

```math
x=r\cos\phi,
\qquad
y=r\sin\phi.
```

```math
\mathbf r=r\hat{\mathbf r}.
```

### Polar basis vectors

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

### Why polar coordinates are different

Unlike Cartesian basis vectors,

```math
\hat{\mathbf r}
\quad\text{and}\quad
\hat{\boldsymbol\phi}
```

change direction as the particle moves.

### Basis-vector derivatives

```math
\boxed{
\dot{\hat{\mathbf r}}
=
\dot\phi\,\hat{\boldsymbol\phi}
}
```

```math
\boxed{
\dot{\hat{\boldsymbol\phi}}
=
-\dot\phi\,\hat{\mathbf r}
}
```

Explain the signs geometrically:

### Velocity

```math
\boxed{
\mathbf v
=
\dot r\,\hat{\mathbf r}
+
r\dot\phi\,\hat{\boldsymbol\phi}
}
```

Interpret:

- $\dot r\hat{\mathbf r}$:
- $r\dot\phi\hat{\boldsymbol\phi}$:

### Acceleration

```math
\boxed{
\mathbf a
=
\left(\ddot r-r\dot\phi^2\right)\hat{\mathbf r}
+
\left(r\ddot\phi+2\dot r\dot\phi\right)
\hat{\boldsymbol\phi}
}
```

### Interpretation of the terms

| Term | Interpretation |
|---|---|
| $\ddot r$ | |
| $-r\dot\phi^2$ | |
| $r\ddot\phi$ | |
| $2\dot r\dot\phi$ | |

### Newton's second law in polar form

```math
F_r
=
m\left(\ddot r-r\dot\phi^2\right),
```

```math
F_\phi
=
m\left(r\ddot\phi+2\dot r\dot\phi\right).
```

### Special cases

#### Pure radial motion

Set

```math
\dot\phi=0.
```

Then:

```math
\mathbf a=
```

#### Uniform circular motion

Set

```math
r=R,
\qquad
\dot r=\ddot r=0,
\qquad
\dot\phi=\omega,
\qquad
\ddot\phi=0.
```

Then:

```math
\mathbf a=
```

#### Circular motion with angular acceleration

Set

```math
r=R,
\qquad
\dot r=\ddot r=0.
```

Then:

```math
\mathbf a=
```

### Fixed-radius skateboard equation

For $r=R$,

```math
F_\phi=-mg\sin\phi.
```

Newton's second law gives

```math
mR\ddot\phi=-mg\sin\phi,
```

so

```math
\boxed{
\ddot\phi
=
-\frac{g}{R}\sin\phi
}.
```

Why is this nonlinear?

### Small-angle approximation

For small $\phi$ in radians,

```math
\sin\phi\approx\phi.
```

Therefore,

```math
\ddot\phi+\frac{g}{R}\phi=0.
```

Define

```math
\omega_0^2=\frac{g}{R}.
```

Then

```math
\phi(t)
=
A\cos(\omega_0t)
+
B\sin(\omega_0t).
```

The approximate period is

```math
\boxed{
T
=
2\pi\sqrt{\frac{R}{g}}
}.
```

### Exact versus approximate motion

Exact:

```math
\ddot\phi
=
-\frac{g}{R}\sin\phi.
```

Approximate:

```math
\ddot\phi
=
-\frac{g}{R}\phi.
```

What changes as the initial angle increases?

### Connection to later chapters

Why does this calculation motivate generalized coordinates and
Lagrangian mechanics?

---

# 4. Essential derivations

These belong in the notes because they are part of the chapter's core
understanding, not merely exercises.

## Derivation 1 — Constant-force motion as an initial-value problem

### Starting equation

```math
m\ddot x=F_0.
```

### First integration

```math
\dot x(t)
=
\frac{F_0}{m}t+C_1.
```

### Second integration

```math
x(t)
=
\frac{F_0}{2m}t^2+C_1t+C_2.
```

Apply

```math
x(0)=x_0,
\qquad
\dot x(0)=v_0.
```

Then

```math
C_1=v_0,
\qquad
C_2=x_0.
```

Therefore,

```math
\boxed{
x(t)
=
x_0+v_0t+\frac{F_0}{2m}t^2
}.
```

### Why this matters

- The equation of motion is second order.
- Two integrations introduce two constants.
- The initial position and velocity determine those constants.

### Reproduce from memory

- [ ] First attempt
- [ ] One-week review
- [ ] End-of-chapter review

---

## Derivation 2 — Momentum conservation for an $N$-particle system

Define

```math
\mathbf P
=
\sum_{\alpha=1}^{N}
\mathbf p_\alpha.
```

For particle $\alpha$,

```math
\dot{\mathbf p}_\alpha
=
\sum_{\beta\ne\alpha}
\mathbf F_{\alpha\beta}
+
\mathbf F_\alpha^{\mathrm{ext}}.
```

Differentiate the total momentum:

```math
\frac{d\mathbf P}{dt}
=
\sum_\alpha
\dot{\mathbf p}_\alpha.
```

Substitute the equations of motion:

```math
\frac{d\mathbf P}{dt}
=
\sum_\alpha
\sum_{\beta\ne\alpha}
\mathbf F_{\alpha\beta}
+
\sum_\alpha
\mathbf F_\alpha^{\mathrm{ext}}.
```

Each internal interaction appears twice:

```math
\mathbf F_{\alpha\beta}
+
\mathbf F_{\beta\alpha}
=
0
```

by Newton's third law. Therefore,

```math
\sum_\alpha
\sum_{\beta\ne\alpha}
\mathbf F_{\alpha\beta}
=
0.
```

Hence,

```math
\boxed{
\frac{d\mathbf P}{dt}
=
\sum_\alpha
\mathbf F_\alpha^{\mathrm{ext}}
}.
```

For an isolated system,

```math
\sum_\alpha
\mathbf F_\alpha^{\mathrm{ext}}
=
0,
```

so

```math
\boxed{
\mathbf P=\text{constant}
}.
```

### Questions to answer

- Why does every internal force appear twice?
- Why do the two appearances have opposite signs?
- How does the choice of system boundary affect the proof?
- What assumptions about the force law are being used?

### Reproduce from memory

- [ ] Three-particle version
- [ ] $N$-particle version
- [ ] Explain the physical meaning aloud

---

## Derivation 3 — Polar basis-vector derivatives

Begin with

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

Differentiate $\hat{\mathbf r}$:

```math
\dot{\hat{\mathbf r}}
=
-\sin\phi\,\dot\phi\,\hat{\mathbf x}
+
\cos\phi\,\dot\phi\,\hat{\mathbf y}.
```

Factor out $\dot\phi$:

```math
\dot{\hat{\mathbf r}}
=
\dot\phi
\left(
-\sin\phi\,\hat{\mathbf x}
+
\cos\phi\,\hat{\mathbf y}
\right).
```

Therefore,

```math
\boxed{
\dot{\hat{\mathbf r}}
=
\dot\phi\,\hat{\boldsymbol\phi}
}.
```

Now differentiate $\hat{\boldsymbol\phi}$:

```math
\dot{\hat{\boldsymbol\phi}}
=
-\cos\phi\,\dot\phi\,\hat{\mathbf x}
-
\sin\phi\,\dot\phi\,\hat{\mathbf y}.
```

Thus,

```math
\boxed{
\dot{\hat{\boldsymbol\phi}}
=
-\dot\phi\,\hat{\mathbf r}
}.
```

### Geometric interpretation

- $\hat{\mathbf r}$ rotates toward $\hat{\boldsymbol\phi}$.
- $\hat{\boldsymbol\phi}$ rotates toward $-\hat{\mathbf r}$.
- A unit vector's derivative is perpendicular to the vector itself.

### Reproduce from memory

- [ ] Draw the basis
- [ ] Derive both Cartesian expressions
- [ ] Derive both time derivatives
- [ ] Explain the signs geometrically

---

## Derivation 4 — Velocity and acceleration in polar coordinates

Begin with

```math
\mathbf r=r\hat{\mathbf r}.
```

Differentiate:

```math
\mathbf v
=
\dot r\,\hat{\mathbf r}
+
r\dot{\hat{\mathbf r}}.
```

Using

```math
\dot{\hat{\mathbf r}}
=
\dot\phi\,\hat{\boldsymbol\phi},
```

we obtain

```math
\boxed{
\mathbf v
=
\dot r\,\hat{\mathbf r}
+
r\dot\phi\,\hat{\boldsymbol\phi}
}.
```

Differentiate again:

```math
\mathbf a
=
\frac{d}{dt}
\left(
\dot r\,\hat{\mathbf r}
+
r\dot\phi\,\hat{\boldsymbol\phi}
\right).
```

Apply the product rule:

```math
\mathbf a
=
\ddot r\,\hat{\mathbf r}
+
\dot r\,\dot{\hat{\mathbf r}}
+
\dot r\dot\phi\,\hat{\boldsymbol\phi}
+
r\ddot\phi\,\hat{\boldsymbol\phi}
+
r\dot\phi\,\dot{\hat{\boldsymbol\phi}}.
```

Substitute

```math
\dot{\hat{\mathbf r}}
=
\dot\phi\,\hat{\boldsymbol\phi},
\qquad
\dot{\hat{\boldsymbol\phi}}
=
-\dot\phi\,\hat{\mathbf r}.
```

Then

```math
\mathbf a
=
\ddot r\,\hat{\mathbf r}
+
\dot r\dot\phi\,\hat{\boldsymbol\phi}
+
\dot r\dot\phi\,\hat{\boldsymbol\phi}
+
r\ddot\phi\,\hat{\boldsymbol\phi}
-
r\dot\phi^2\,\hat{\mathbf r}.
```

Collect terms:

```math
\boxed{
\mathbf a
=
\left(\ddot r-r\dot\phi^2\right)\hat{\mathbf r}
+
\left(r\ddot\phi+2\dot r\dot\phi\right)
\hat{\boldsymbol\phi}
}.
```

### Interpret every term

| Term | Interpretation |
|---|---|
| $\ddot r$ | Change in radial speed |
| $-r\dot\phi^2$ | Inward centripetal acceleration |
| $r\ddot\phi$ | Tangential acceleration from changing angular speed |
| $2\dot r\dot\phi$ | Tangential contribution from changing radius while rotating |

### Special-case checks

For uniform circular motion,

```math
r=R,
\qquad
\dot r=\ddot r=0,
\qquad
\dot\phi=\omega,
\qquad
\ddot\phi=0,
```

so

```math
\boxed{
\mathbf a
=
-R\omega^2\hat{\mathbf r}
}.
```

### Reproduce from memory

- [ ] Velocity
- [ ] Full acceleration
- [ ] Interpretation of all four terms
- [ ] Uniform circular-motion check

---

## Derivation 5 — Exact skateboard equation and small-angle motion

For fixed radius $R$,

```math
a_\phi=R\ddot\phi.
```

The tangential component of gravity is

```math
F_\phi=-mg\sin\phi.
```

Newton's second law gives

```math
mR\ddot\phi
=
-mg\sin\phi.
```

Therefore,

```math
\boxed{
\ddot\phi
+
\frac{g}{R}\sin\phi
=
0
}.
```

This equation is nonlinear because the unknown $\phi$ appears inside
the nonlinear function $\sin\phi$.

For small angles measured in radians,

```math
\sin\phi\approx\phi.
```

Then

```math
\ddot\phi
+
\frac{g}{R}\phi
=
0.
```

Define

```math
\omega_0^2=\frac{g}{R}.
```

The solution is

```math
\phi(t)
=
A\cos(\omega_0t)
+
B\sin(\omega_0t).
```

For

```math
\phi(0)=\phi_0,
\qquad
\dot\phi(0)=0,
```

we obtain

```math
\boxed{
\phi(t)
=
\phi_0\cos(\omega_0t)
}.
```

The approximate period is

```math
\boxed{
T
=
2\pi\sqrt{\frac{R}{g}}
}.
```

### Questions to answer

- Why must the angle be measured in radians?
- Why is the approximate period independent of amplitude?
- Does the exact nonlinear period depend on amplitude?
- Why does the approximation worsen at large angles?

### Reproduce from memory

- [ ] Exact equation
- [ ] Small-angle approximation
- [ ] Solution under the stated initial conditions
- [ ] Period

---

# 5. Computational experiment

## Exact skateboard motion versus the small-angle approximation

### Exact model

```math
\ddot\phi
=
-\frac{g}{R}\sin\phi.
```

### Approximate model

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

### Angles to investigate

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

### Outputs

- [ ] Exact numerical trajectory
- [ ] Small-angle trajectory
- [ ] Comparison plot
- [ ] Estimated exact period
- [ ] Approximate period
- [ ] Relative period error
- [ ] Maximum trajectory difference

### Code location

```text
code/problem-1-50-skateboard.ipynb
```

Save plots in:

```text
figures/
```

### Statistical extension

Treat the initial angle as uncertain and simulate the induced distribution
of the period, maximum speed, and approximation error.

### Interpretation

> Describe the physical result, not merely what the plot looks like.

---

# 6. Mistake and confusion log

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

# 7. Connections

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

# 8. Final chapter summary

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

# 9. Mastery check

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
- [ ] Complete the selected problems in `problems.md`.
- [ ] Complete the numerical comparison in Problem 1.50.
