# Chapter 1 — Newton's Laws of Motion

**Text:** John R. Taylor, **Classical Mechanics**  

**Dates studied:** July--August 2026  

**Status:** Chapter review complete  

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

> Chapter 1 gives a foundation of Newtonian Mechanics and reviews the basics of vector calculus and differential equations

## My current interpretation

This chapter establishes the basic objects and assumptions of Newtonian

mechanics and shows how physical forces are converted into differential

equations for motion.

## What was review?

- Newton's Laws

- Harmonic Motion

- Conservation of Momentum

## What was genuinely new or rusty?

- I feel like I truly understand the basis in polar coordinates instead of just memorizing equations.

- Differential equations were rusty. The skateboard problem forced me to reconnect the order of an ODE with the number of initial conditions and to convert a second-order ODE into a first-order system for numerical solution.

- Resolving vectors in rotated coordinate systems was rusty. Problem 1.38 showed me that I should define the axes first and project the force onto them rather than decide sine versus cosine from how a triangle looks.





---

# 2. Learning objectives

By the end of the chapter, I should be able to:

- [x] Explain the domain in which classical mechanics is appropriate.

- [x] Define position, velocity, and acceleration as vectors.

- [x] Differentiate vectors written in a fixed Cartesian basis.

- [x] Explain the physical meaning of mass and force.

- [x] State Newton's three laws precisely.

- [x] Explain why Newton's first law defines inertial frames.

- [x] Treat Newton's second law as a differential equation.

- [x] Explain the role of initial conditions.

- [x] Derive conservation of momentum for an isolated system.

- [x] Distinguish internal forces from external forces.

- [x] Choose useful Cartesian coordinates.

- [x] Derive velocity and acceleration in two-dimensional polar coordinates.

- [x] Interpret every term in the polar acceleration formula.

- [x] Derive the nonlinear skateboard equation.

- [x] Explain and test the small-angle approximation.

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

- When we are not moving close to the speed of light





### My takeaway

> Why does Taylor begin with the Newtonian formulation?

It is the one most are familiar with and it came first

---

## 1.2 Space and Time

### Position

$$

\mathbf r(t)

=

x(t)\hat{\mathbf x}

+y(t)\hat{\mathbf y}

+z(t)\hat{\mathbf z}.

$$

### Velocity and acceleration

$$

\mathbf v

=

\frac{d\mathbf r}{dt},

\qquad

\mathbf a

=

\frac{d\mathbf v}{dt}

=

\frac{d^2\mathbf r}{dt^2}.

$$

In Cartesian coordinates,

$$

\mathbf v

=

\dot x\hat{\mathbf x}

+\dot y\hat{\mathbf y}

+\dot z\hat{\mathbf z}.

$$

> Why Cartesian differentiation is simple

The Cartesian basis vectors are fixed in time.

### Scalar product

$$

\mathbf a\cdot\mathbf b

=

ab\cos\theta.

$$

Geometric meaning: The scalar magnitude of 2 vectors

Important uses:

- If a force acts on an object through a small displacement, the work is the dot product

- the square root of a dot product of a vector with itself gives the magmitude of the vector

### Vector product

$$

\mathbf a\times\mathbf b

=

ab\sin\theta\,\hat{\mathbf n}.

$$

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

Classical Newtonian mechanics assumes an absolute, universal time: all inertial observers use the same time coordinate. Time is independent of the observer's state of motion. This is one of the assumptions that must be modified in special relativity.

### Questions

- Revisit this when studying relativity and compare Galilean time with relativistic spacetime.





---

## 1.3 Mass and Force

### Mass

My physical interpretation:

> Mass measures resistance to acceleration.

How could two masses be compared operationally?

Apply the same known force to each object and compare the accelerations. Since $F=ma$, the object with the smaller acceleration has the larger mass. Equivalently,

$$

\frac{m_1}{m_2}=\frac{a_2}{a_1}

$$

when the same force is applied.

### Force

My physical interpretation:

A force is an interaction that changes an object's motion; in an inertial frame its net effect is measured by the acceleration it produces.

How could force be measured operationally?

For a known mass, measure the acceleration and use

$$

\mathbf F_{\mathrm{net}}=m\mathbf a.

$$

A particular force law then specifies how that force depends on position, velocity, time, or other physical variables.

### Net force

$$

\mathbf F_{\mathrm{net}}

=

\sum_i \mathbf F_i.

$$

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

Newton's second law tells me what the net force **does**: it determines the acceleration. A force law tells me the specific physical origin and mathematical form of a force, such as gravity, a spring force, friction, or drag. The equation $F=ma$ is not by itself a model for gravity or a spring; those require separate force laws.

---

## 1.4 Newton's First and Second Laws

### Newton's first law

State it in my own words: an object in motion will stay in the exact same motion unless acted on by a force

### Newton's second law

$$

\mathbf F_{\mathrm{net}}

=

m\mathbf a.

$$

For constant mass,

$$

\mathbf F_{\mathrm{net}}

=

\frac{d\mathbf p}{dt},

\qquad

\mathbf p=m\mathbf v.

$$

### Why the first law is not redundant

Setting $\mathbf F=0$ in the second law appears to give

$\mathbf a=0$, but this statement is only valid in an inertial frame.

### Inertial frame

My definition:

$$

\mathbf F_{\mathrm{net}}=0

\quad\Longrightarrow\quad

\mathbf v=\text{constant}.

$$

Examples of approximately inertial frames:

- Watching the ice puck slide on the floor of a train

Examples of noninertial frames:

- Being in another train that is accelerating

- Being on a merry-go-round as the puck moves in a straight line

### Newton's second law as a differential equation

$$

m\ddot{\mathbf r}(t)

=

\mathbf F(\mathbf r,\dot{\mathbf r},t).

$$

The unknown is:

$$

\mathbf r(t).

$$

A second-order equation normally requires:

$$

\mathbf r(0)=\mathbf r_0,

\qquad

\dot{\mathbf r}(0)=\mathbf v_0.

$$

### My takeaway

> A mechanics problem consists of identifying the force law, constructing

> the differential equation, and solving it subject to initial conditions.

---

## 1.5 Newton's Third Law and Momentum Conservation

### Newton's third law

$$

\mathbf F_{12}

=

-\mathbf F_{21}.

$$

Define carefully:

- $\mathbf F_{12}$: the force exerted on particle 1 by particle 2.

- $\mathbf F_{21}$: the force exerted on particle 2 by particle 1.

### Third-law pair checklist

A third-law pair:

- acts on two different objects;

- comes from the same interaction;

- has equal magnitude;

- points in opposite directions.

### Total momentum

For a system of particles,

$$

\mathbf P

=

\sum_\alpha \mathbf p_\alpha.

$$

The central result is

$$

\boxed{

\frac{d\mathbf P}{dt}

=

\mathbf F_{\mathrm{ext}}

}.

$$

For an isolated system,

$$

\mathbf F_{\mathrm{ext}}=0

\quad\Longrightarrow\quad

\boxed{\mathbf P=\text{constant}}.

$$

### System boundary

The distinction between internal and external forces depends on:

> How the system is defined.

Example:

If two particles push on each other and both are included in the system, the two interaction forces are internal and cancel in the total-momentum equation. If only one particle is included, the force exerted by the other particle crosses the system boundary and must be counted as an external force.

### My takeaway

> Momentum conservation concerns the total momentum of a properly defined

> isolated system.

---

## 1.6 Newton's Second Law in Cartesian Coordinates

### Component equations

$$

F_x=m\ddot x,

\qquad

F_y=m\ddot y,

\qquad

F_z=m\ddot z.

$$

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

- Weight: $m\mathbf g$, vertically downward.

- Normal force: $N$, perpendicular to the board.

- Other forces: none for the frictionless puck.

Choose coordinates attached to the board:

- $x$: across the board, where gravity has no component.

- $y$: up the board.

- $z$: perpendicular to the board.

The key lesson from this problem was to define the axes first and then project gravity onto them. The in-plane component is $mg\sin\theta$ and the normal component is $mg\cos\theta$.

Normal equation:

$$

N-mg\cos\theta=0.

$$

Equations within the board:

$$

m\ddot x=0,

$$

$$

m\ddot y=-mg\sin\theta.

$$

Thus,

$$

x(t)=v_{0x}t,

$$

$$

y(t)=v_{0y}t-\frac12g\sin\theta\,t^2,

$$

for an initial position at the origin.

If the puck returns to $y=0$, the nonzero return time is

$$

t_{\rm return}=\frac{2v_{0y}}{g\sin\theta},

$$

and the corresponding displacement across the board is

$$

x_{\rm return}=\frac{2v_{0x}v_{0y}}{g\sin\theta}.

$$

### Checks

- [x] Correct units

- [x] Correct behavior when $\theta\to0$

- [x] Correct initial position

- [x] Correct initial velocity

- [x] Clear physical interpretation

---

## 1.7 Two-Dimensional Polar Coordinates

### Coordinate definitions

$$

x=r\cos\phi,

\qquad

y=r\sin\phi.

$$

$$

\mathbf r=r\hat{\mathbf r}.

$$

### Polar basis vectors

$$

\hat{\mathbf r}

=

\cos\phi\,\hat{\mathbf x}

+

\sin\phi\,\hat{\mathbf y},

$$

$$

\hat{\boldsymbol\phi}

=

-\sin\phi\,\hat{\mathbf x}

+

\cos\phi\,\hat{\mathbf y}.

$$

### Why polar coordinates are different

Unlike Cartesian basis vectors,

$$

\hat{\mathbf r}

\quad\text{and}\quad

\hat{\boldsymbol\phi}

$$

change direction as the particle moves.

### Basis-vector derivatives

$$

\boxed{

\dot{\hat{\mathbf r}}

=

\dot\phi\,\hat{\boldsymbol\phi}

}

$$

$$

\boxed{

\dot{\hat{\boldsymbol\phi}}

=

-\dot\phi\,\hat{\mathbf r}

}

$$

Explain the signs geometrically:

As $\phi$ increases, $\hat{\mathbf r}$ rotates toward the direction of increasing angle, $+\hat{\boldsymbol\phi}$. Meanwhile $\hat{\boldsymbol\phi}$ rotates inward toward $-\hat{\mathbf r}$. This is why

$$

\dot{\hat{\mathbf r}}=\dot\phi\hat{\boldsymbol\phi},

\qquad

\dot{\hat{\boldsymbol\phi}}=-\dot\phi\hat{\mathbf r}.

$$

### Velocity

$$

\boxed{

\mathbf v

=

\dot r\,\hat{\mathbf r}

+

r\dot\phi\,\hat{\boldsymbol\phi}

}

$$

Interpret:

- $\dot r\hat{\mathbf r}$: radial velocity, the rate at which the distance from the origin changes.

- $r\dot\phi\hat{\boldsymbol\phi}$: tangential velocity caused by rotation about the origin. Its magnitude is radius times angular speed.

### Acceleration

$$

\boxed{

\mathbf a

=

\left(\ddot r-r\dot\phi^2\right)\hat{\mathbf r}

+

\left(r\ddot\phi+2\dot r\dot\phi\right)

\hat{\boldsymbol\phi}

}

$$

### Interpretation of the terms

| Term | Interpretation |
|---|---|
| $\ddot r$ | Change in radial speed; radial acceleration from changing $\dot r$ |
| $-r\dot\phi^2$ | Inward centripetal acceleration caused by changing direction while rotating |
| $r\ddot\phi$ | Tangential acceleration from changing angular speed |
| $2\dot r\dot\phi$ | Tangential contribution that appears when the radius changes while the particle is also rotating |

### Newton's second law in polar form

$$

F_r

=

m\left(\ddot r-r\dot\phi^2\right),

$$

$$

F_\phi

=

m\left(r\ddot\phi+2\dot r\dot\phi\right).

$$

### Special cases

#### Pure radial motion

Set

$$

\dot\phi=0.

$$

Then:

$$

\mathbf a=\ddot r\,\hat{\mathbf r}.

$$

#### Uniform circular motion

Set

$$

r=R,

\qquad

\dot r=\ddot r=0,

\qquad

\dot\phi=\omega,

\qquad

\ddot\phi=0.

$$

Then:

$$

\mathbf a=-R\omega^2\hat{\mathbf r}.

$$

The acceleration is purely inward (centripetal).

#### Circular motion with angular acceleration

Set

$$

r=R,

\qquad

\dot r=\ddot r=0.

$$

Then:

$$

\mathbf a=-R\dot\phi^2\hat{\mathbf r}+R\ddot\phi\hat{\boldsymbol\phi}.

$$

There is an inward radial component from the changing direction of the velocity and a tangential component from the changing angular speed.

### Fixed-radius skateboard equation

For $r=R$,

$$

F_\phi=-mg\sin\phi.

$$

Newton's second law gives

$$

mR\ddot\phi=-mg\sin\phi,

$$

so

$$

\boxed{

\ddot\phi

=
-\frac{g}{R}\sin\phi

}.

$$

Why is this nonlinear?

Because the unknown function $\phi(t)$ appears inside $\sin\phi$. The equation is not linear in $\phi$.

### Small-angle approximation

For small $\phi$ in radians,

$$

\sin\phi\approx\phi.

$$

Therefore,

$$

\ddot\phi+\frac{g}{R}\phi=0.

$$

Define

$$

\omega_0^2=\frac{g}{R}.

$$

Then

$$

\phi(t)

=

A\cos(\omega_0t)

+

B\sin(\omega_0t).

$$

The approximate period is

$$

\boxed{

T

=

2\pi\sqrt{\frac{R}{g}}

}.

$$

### Exact versus approximate motion

Exact:

$$

\ddot\phi

=

-\frac{g}{R}\sin\phi.

$$

Approximate:

$$

\ddot\phi

=

-\frac{g}{R}\phi.

$$

What changes as the initial angle increases?

The small-angle approximation becomes less accurate. For positive $\phi$, $\sin\phi<\phi$, so the exact restoring acceleration is weaker in magnitude than the linear approximation predicts. The exact motion therefore takes longer to complete a cycle, and the two trajectories develop an increasing phase difference. The exact nonlinear period depends on amplitude, whereas the small-angle period does not.

### Connection to later chapters

Why does this calculation motivate generalized coordinates and

Lagrangian mechanics?

The skateboard is constrained to a circle, so its motion has only one independent coordinate, $\phi$. In Newtonian mechanics I can enforce the constraint by working in polar coordinates and carrying the radial normal force along even though it does not determine the motion in $\phi$. Generalized coordinates let me describe the system directly with the independent coordinate, which can avoid explicitly solving for constraint forces that are not needed to determine the motion.

---

# 4. Essential derivations

These belong in the notes because they are part of the chapter's core

understanding, not merely exercises.

## Derivation 1 — Constant-force motion as an initial-value problem

### Starting equation

$$

m\ddot x=F_0.

$$

### First integration

$$

\dot x(t)

=

\frac{F_0}{m}t+C_1.

$$

### Second integration

$$

x(t)

=

\frac{F_0}{2m}t^2+C_1t+C_2.

$$

Apply

$$

x(0)=x_0,

\qquad

\dot x(0)=v_0.

$$

Then

$$

C_1=v_0,

\qquad

C_2=x_0.

$$

Therefore,

$$

\boxed{

x(t)

=

x_0+v_0t+\frac{F_0}{2m}t^2

}.

$$

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

$$

\mathbf P

=

\sum_{\alpha=1}^{N}

\mathbf p_\alpha.

$$

For particle $\alpha$,

$$

\dot{\mathbf p}_\alpha

=

\sum_{\beta\ne\alpha}

\mathbf F_{\alpha\beta}

+

\mathbf F_\alpha^{\mathrm{ext}}.

$$

Differentiate the total momentum:

$$

\frac{d\mathbf P}{dt}

=

\sum_\alpha

\dot{\mathbf p}_\alpha.

$$

Substitute the equations of motion:

$$

\frac{d\mathbf P}{dt}

=

\sum_\alpha

\sum_{\beta\ne\alpha}

\mathbf F_{\alpha\beta}

+

\sum_\alpha

\mathbf F_\alpha^{\mathrm{ext}}.

$$

Each internal interaction appears twice:

$$

\mathbf F_{\alpha\beta}

+

\mathbf F_{\beta\alpha}

=

0

$$

by Newton's third law. Therefore,

$$

\sum_\alpha

\sum_{\beta\ne\alpha}

\mathbf F_{\alpha\beta}

=

0.

$$

Hence,

$$

\boxed{

\frac{d\mathbf P}{dt}

=

\sum_\alpha

\mathbf F_\alpha^{\mathrm{ext}}

}.

$$

For an isolated system,

$$

\sum_\alpha

\mathbf F_\alpha^{\mathrm{ext}}

=

0,

$$

so

$$

\boxed{

\mathbf P=\text{constant}

}.

$$

### Questions to answer

- Why does every internal force appear twice?

- Why do the two appearances have opposite signs?

- How does the choice of system boundary affect the proof?

- What assumptions about the force law are being used?

### Reproduce from memory

- [x] Three-particle version

- [x] $N$-particle version

- [x] Explain the physical meaning aloud

---

## Derivation 3 — Polar basis-vector derivatives

Begin with

$$

\hat{\mathbf r}

=\cos\phi\,\hat{\mathbf x}

+

\sin\phi\,\hat{\mathbf y},

$$

$$

\hat{\boldsymbol\phi}

=-\sin\phi\,\hat{\mathbf x}

+

\cos\phi\,\hat{\mathbf y}.

$$

Differentiate $\hat{\mathbf r}$:

$$

\dot{\hat{\mathbf r}}

=-\sin\phi\,\dot\phi\,\hat{\mathbf x}

+

\cos\phi\,\dot\phi\,\hat{\mathbf y}.

$$

Factor out $\dot\phi$:

$$

\dot{\hat{\mathbf r}}

=\dot\phi\left(-\sin\phi\,\hat{\mathbf x}+

\cos\phi\,\hat{\mathbf y}\right).

$$

Therefore,

$$

\boxed{

\dot{\hat{\mathbf r}}=\dot\phi\,\hat{\boldsymbol\phi}}

$$

Now differentiate $\hat{\boldsymbol\phi}$:

$$

\dot{\hat{\boldsymbol\phi}}

=-\cos\phi\,\dot\phi\,\hat{\mathbf x}

-

\sin\phi\,\dot\phi\,\hat{\mathbf y}.

$$

Thus,

$$

\boxed{

\dot{\hat{\boldsymbol\phi}}=-\dot\phi\,\hat{\mathbf r}}

$$

### Geometric interpretation

- $\hat{\mathbf r}$ rotates toward $\hat{\boldsymbol\phi}$.

- $\hat{\boldsymbol\phi}$ rotates toward $-\hat{\mathbf r}$.

- A unit vector's derivative is perpendicular to the vector itself.

### Reproduce from memory

- [x] Draw the basis

- [x] Derive both Cartesian expressions

- [x] Derive both time derivatives

- [x] Explain the signs geometrically

---

## Derivation 4 — Velocity and acceleration in polar coordinates

Begin with

$$

\mathbf r=r\hat{\mathbf r}.

$$

Differentiate:

$$

\mathbf v=\dot r\,\hat{\mathbf r}+r\dot{\hat{\mathbf r}}.

$$

Using

$$

\dot{\hat{\mathbf r}}=\dot\phi\,\hat{\boldsymbol\phi},

$$

we obtain

$$

\boxed{

\mathbf v=\dot r\,\hat{\mathbf r}+r\dot\phi\,\hat{\boldsymbol\phi}}

$$

Differentiate again:

$$

\mathbf a=

\frac{d}{dt}\left(\dot r\,\hat{\mathbf r}+r\dot\phi\,\hat{\boldsymbol\phi}\right).

$$

Apply the product rule:

$$

\mathbf a=

\ddot r\,\hat{\mathbf r}

+

\dot r\,\dot{\hat{\mathbf r}}

+

\dot r\dot\phi\,\hat{\boldsymbol\phi}

+

r\ddot\phi\,\hat{\boldsymbol\phi}

+

r\dot\phi\,\dot{\hat{\boldsymbol\phi}}.

$$

Substitute

$$

\dot{\hat{\mathbf r}}=\dot\phi\,\hat{\boldsymbol\phi},

\qquad

\dot{\hat{\boldsymbol\phi}}=-\dot\phi\,\hat{\mathbf r}.

$$

Then

$$

\mathbf a=

\ddot r\,\hat{\mathbf r}

+

\dot r\dot\phi\,\hat{\boldsymbol\phi}

+

\dot r\dot\phi\,\hat{\boldsymbol\phi}

+

r\ddot\phi\,\hat{\boldsymbol\phi}

-

r\dot\phi^2\,\hat{\mathbf r}.

$$

Collect terms:

$$

\boxed{

\mathbf a

=

\left(\ddot r-r\dot\phi^2\right)\hat{\mathbf r}

+

\left(r\ddot\phi+2\dot r\dot\phi\right)

\hat{\boldsymbol\phi}

}.

$$

### Interpret every term

| Term | Interpretation |
|---|---|
| $\ddot r$ | Change in radial speed |
| $-r\dot\phi^2$ | Inward centripetal acceleration |
| $r\ddot\phi$ | Tangential acceleration from changing angular speed |
| $2\dot r\dot\phi$ | Tangential contribution from changing radius while rotating |

### Special-case checks

For uniform circular motion,

$$

r=R,

\qquad

\dot r=\ddot r=0,

\qquad

\dot\phi=\omega,

\qquad

\ddot\phi=0,

$$

so

$$

\boxed{

\mathbf a

=

-R\omega^2\hat{\mathbf r}

}.

$$

### Reproduce from memory

- [x] Velocity

- [x] Full acceleration

- [x] Interpretation of all four terms

- [x] Uniform circular-motion check

---

## Derivation 5 — Exact skateboard equation and small-angle motion

For fixed radius $R$,

$$

a_\phi=R\ddot\phi.

$$

The tangential component of gravity is

$$

F_\phi=-mg\sin\phi.

$$

Newton's second law gives

$$

mR\ddot\phi

=

-mg\sin\phi.

$$

Therefore,

$$

\boxed{

\ddot\phi

+

\frac{g}{R}\sin\phi

=

0

}.

$$

This equation is nonlinear because the unknown $\phi$ appears inside

the nonlinear function $\sin\phi$.

For small angles measured in radians,

$$

\sin\phi\approx\phi.

$$

Then

$$

\ddot\phi

+

\frac{g}{R}\phi

=

0.

$$

Define

$$

\omega_0^2=\frac{g}{R}.

$$

The solution is

$$

\phi(t)

=

A\cos(\omega_0t)

+

B\sin(\omega_0t).

$$

For

$$

\phi(0)=\phi_0,

\qquad

\dot\phi(0)=0,

$$

we obtain

$$

\boxed{

\phi(t)

=

\phi_0\cos(\omega_0t)

}.

$$

The approximate period is

$$

\boxed{

T

=

2\pi\sqrt{\frac{R}{g}}

}.

$$

### Questions to answer

- Why must the angle be measured in radians?

- Why is the approximate period independent of amplitude?

- Does the exact nonlinear period depend on amplitude?

- Why does the approximation worsen at large angles?

### Reproduce from memory

- [x] Exact equation

- [x] Small-angle approximation

- [x] Solution under the stated initial conditions

- [x] Period

---

# 5. Computational experiment

## Exact skateboard motion versus the small-angle approximation

### Exact model

$$

\ddot\phi

=

-\frac{g}{R}\sin\phi.

$$

### Approximate model

$$

\ddot\phi

=

-\frac{g}{R}\phi.

$$

### Initial conditions

$$

\phi(0)=\phi_0,

\qquad

\dot\phi(0)=0.

$$

### Angles to investigate

$$

\phi_0\in\left\{

5^\circ,\,

20^\circ,\,

45^\circ,\,

90^\circ

\right\}.

$$

### Outputs

- [x] Exact numerical trajectory

- [x] Small-angle trajectory

- [x] Comparison plot

- [x] Estimated exact period

- [x] Approximate period

- [x] Relative period error

- [x] Maximum trajectory difference

### Code location

```text

code/problem-1-50-skateboard.ipynb

```

Save plots in:

```text

figures/

```





### Interpretation

> Describe the physical result, not merely what the plot looks like.

The small angle approximation is off by a phase shift compared to the exact result for large enough $\phi$. This means that it takes longer under the exact equation to compleate a full cycle relative to the small angle approximation 

---

# 6. Mistake and confusion log

| Issue | Why I was confused | Resolution |
|---|---|---|
| I did not understand basis vectors well | I always pictured a basis vector as being tied to the origin. | In polar coordinates the basis is local: $\hat{\mathbf r}$ and $\hat{\boldsymbol\phi}$ are defined at the particle's current angle and rotate as $\phi$ changes. A coordinate pair $(r,\phi)$ is not the same thing as the position vector $\mathbf r=r\hat{\mathbf r}$. |
| I switched sine and cosine in the tilted-board gravity components | I was deciding which component was adjacent by looking at the triangle rather than asking which axis the vector was being projected onto. | Define the axes first. The component of a vector along an axis is its projection onto that axis. For the tilted board this gives $mg\sin\theta$ along the board and $mg\cos\theta$ normal to it. |
| Differential equations were rusty in the skateboard problem | I understood the physics equation but had to review how a second-order ODE is solved and how initial conditions enter. | The order of an ODE tells me the number of independent initial conditions normally required. For numerical work, introduce a new variable for $\dot\phi$ and convert the second-order equation into two first-order equations. |









# 7. Connections

## Differential equations

How does the order of an equation determine the number of initial conditions?

> An $n$th-order ODE generally requires $n$ independent initial conditions. Each integration introduces an arbitrary constant. For Newton's second-order equation of motion, those conditions are usually initial position and initial velocity.









## Lagrangian mechanics

Why might generalized coordinates be easier than resolving Newton's law

into polar components? 

> Generalized coordinates can build the constraint directly into the coordinates. In the skateboard problem the radius is fixed, so the motion has only one independent coordinate, $\phi$. A Lagrangian treatment can work directly with $\phi$ instead of carrying the radial equation and normal force when they are not needed to determine the motion.

## Hamiltonian mechanics

Which quantities in this chapter will later become position and momentum

coordinates in phase space? 

> Will find out eventually, should revisit after Hamiltonian mechanics chapter

---
# 8. Final chapter summary

## Five central ideas

1. Newton's laws turn physical statements about forces into differential equations for motion.

2. Newton's first law identifies inertial frames: a force-free object moves with constant velocity only in an inertial frame.

3. Momentum conservation follows because internal third-law force pairs cancel; only the net external force changes total momentum.

4. Coordinate choice is part of solving the physics. Good coordinates align with constraints and simplify force components.

5. Polar coordinates use a moving basis. The time dependence of $\hat{\mathbf r}$ and $\hat{\boldsymbol\phi}$ produces the extra terms in polar velocity and acceleration.

## Three equations I must know

1. Newton's second law:

$$

\mathbf F_{\rm net}=m\mathbf a.

$$

2. Total momentum:

$$

\frac{d\mathbf P}{dt}=\mathbf F_{\rm ext}.

$$

3. Polar acceleration:

$$

\mathbf a=

(\ddot r-r\dot\phi^2)\hat{\mathbf r}

+

(r\ddot\phi+2\dot r\dot\phi)\hat{\boldsymbol\phi}.

$$

## Two derivations I must reproduce

1. Derive the polar basis-vector derivatives and then derive polar velocity and acceleration from $\mathbf r=r\hat{\mathbf r}$.

2. Derive momentum conservation by summing the particle equations of motion and cancelling the internal third-law force pairs.

## One remaining question

1. Revisit how the same constrained skateboard problem is formulated with generalized coordinates in Lagrangian mechanics, and compare that derivation directly with the Newtonian polar-coordinate derivation.

---

# 8.5 End-of-chapter reflection

**Hardest problem:** Problem 1.50. The hard part was not mainly the Python; it was bringing together polar-coordinate dynamics, force decomposition, differential equations, initial conditions, linearization, and numerical solution.

**Most useful problem:** Problem 1.50, because it tied most of the chapter together. Problem 1.43 was also especially useful because understanding the rotating polar basis made the later formulas feel derived rather than memorized.

**Most important mistake:** In Problem 1.38 I initially switched the sine and cosine components of gravity. The lesson is to define the axes first and project the force onto them rather than infer components from the appearance of a triangle.

**Problem I should repeat later:** The polar basis-vector and acceleration derivation. I want to be able to reconstruct it from the Cartesian expressions for $\hat{\mathbf r}$ and $\hat{\boldsymbol\phi}$ without looking up the final formula.

**What I now understand that I did not understand before:** Polar coordinates are a moving basis, not just a different labeling system. The extra acceleration terms come from differentiating basis vectors that rotate with the particle. I also now see the general Newtonian workflow more clearly:

$$

\text{physical forces}

\longrightarrow

\text{coordinate components}

\longrightarrow

\text{differential equations}

\longrightarrow

\text{initial conditions}

\longrightarrow

\text{motion}.

$$

---

# 9. Mastery check

I am ready to move to Chapter 2 when I can:

- [x] Explain inertial frames without consulting the book.

- [x] Construct a correct free-body diagram.

- [x] Convert a force model into differential equations.

- [x] Explain why initial position and velocity are required.

- [x] Derive momentum conservation.

- [x] Choose effective Cartesian coordinates.

- [x] Derive polar basis-vector derivatives.

- [x] Derive polar velocity and acceleration from scratch.

- [x] Explain every term in the polar acceleration formula.

- [x] Derive the exact skateboard equation.

- [x] Explain when the small-angle approximation is valid.

- [x] Complete the selected problems in `problems.md`.

- [x] Complete the numerical comparison in Problem 1.50.
