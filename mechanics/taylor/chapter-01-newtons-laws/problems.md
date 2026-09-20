# Chapter 1 — Problems

**Text:** John R. Taylor, **Classical Mechanics**  

**Chapter:** 1 — Newton's Laws of Motion

---

# 1. Quick diagnostic problems

## Problem 1.10 — Circular motion and vector differentiation

### Purpose

Check that you can move from a vector-valued position function to velocity and acceleration and interpret their directions geometrically.

### Work

For uniform circular motion of radius $R$, with $\phi(0)=0$ and constant angular velocity

$$

\omega=\frac{d\phi}{dt},

$$

integration gives

$$

\phi=\omega t.

$$

Therefore the position vector is

$$

\mathbf r(t)

=

R\cos(\omega t)\,\hat{\mathbf x}

+

R\sin(\omega t)\,\hat{\mathbf y}.

$$

Differentiating once,

$$

\mathbf v(t)

=

-\omega R\sin(\omega t)\,\hat{\mathbf x}

+

\omega R\cos(\omega t)\,\hat{\mathbf y}.

$$

Its magnitude is

$$

|\mathbf v|

=

\sqrt{\omega^2R^2\sin^2(\omega t)+\omega^2R^2\cos^2(\omega t)}

=

\omega R.

$$

Also,

$$

\mathbf r\cdot\mathbf v

=

-\omega R^2\cos(\omega t)\sin(\omega t)

+

\omega R^2\sin(\omega t)\cos(\omega t)

=

0,

$$

so the velocity is perpendicular to the radius and therefore tangent to the circular path.

Differentiating again,

$$

\mathbf a(t)

=

-\omega^2R\cos(\omega t)\,\hat{\mathbf x}

-

\omega^2R\sin(\omega t)\,\hat{\mathbf y}.

$$

Thus

$$

\boxed{\mathbf a(t)=-\omega^2\mathbf r(t)},

$$

so the acceleration points toward the center.

Its magnitude is

$$

|\mathbf a|=\omega^2R.

$$

Since $v=\omega R$,

$$

\boxed{|\mathbf a|=\frac{v^2}{R}}.

$$

### Where I got stuck

No major conceptual difficulty after writing the motion in Cartesian components.

### What I should recognize next time

For uniform circular motion, Cartesian differentiation makes the geometry appear automatically: the velocity is perpendicular to the radius, while the acceleration is proportional to $-\mathbf r$ and therefore points toward the center.

---

## Problem 1.24 — First-order differential equations

### Work

Start with

$$

\dot f=f.

$$

Then

$$

\frac{df}{dt}=f

\quad\Longrightarrow\quad

\frac{df}{f}=dt.

$$

Integrating,

$$

\int\frac{df}{f}

=

\int dt,

$$

so

$$

\ln|f|=t+C.

$$

Exponentiating,

$$

f=e^{t+C}=Ae^t,

$$

where $A=e^C$ is an arbitrary constant. Therefore

$$

\boxed{f(t)=Ae^t}.

$$

If one initial condition is supplied, for example

$$

f(0)=f_0,

$$

then

$$

A=f_0

$$

and

$$

\boxed{f(t)=f_0e^t}.

$$

A first-order differential equation therefore requires one initial condition to determine the arbitrary constant.

By contrast, a second-order equation generally contains two arbitrary constants. For example,

$$

\ddot f=f

$$

has the general solution

$$

f(t)=Ae^t+Be^{-t}.

$$

Two independent initial conditions, usually $f(0)$ and $\dot f(0)$, are therefore needed. This is the same reason that Newton's second-order equation of motion normally requires an initial position and an initial velocity.

### Where I got stuck

I initially tried to generalize the separation-of-variables step directly to higher derivatives. A higher derivative such as $d^2f/dt^2$ cannot be separated in the same way as $df/dt=f$.

### What I should recognize next time

The order of a differential equation tells me how many independent initial conditions are generally required: a first-order equation needs one, while Newton's second-order equation of motion needs position and velocity.

---

# 2. Core written problems

## Problem 1.26 — Inertial and noninertial reference frames

### Diagram and frame definitions

Let $S$ be the original frame. The puck starts at the origin and moves in the $+\hat{\mathbf y}$ direction with speed $v_0$.

Let $S'$ move east, in the $+\hat{\mathbf x}$ direction, at constant speed $v$.

Let $S''$ accelerate east with constant acceleration $a_0$.

### Coordinate transformations

For the constant-velocity frame,

$$

x'=x-vt.

$$

For the accelerating frame,

$$

x''=x-\frac12a_0t^2.

$$

### Velocity and acceleration in each frame

In $S$,

$$

\mathbf a=0,

$$

$$

\mathbf v=v_0\hat{\mathbf y},

$$

and, taking the initial position to be the origin,

$$

\boxed{\mathbf r(t)=v_0t\,\hat{\mathbf y}}.

$$

In $S'$,

$$

\mathbf a'=0,

$$

$$

\mathbf v'

=

-v\hat{\mathbf x}+v_0\hat{\mathbf y},

$$

and

$$

\boxed{

\mathbf r'(t)

=

-vt\,\hat{\mathbf x}

+

v_0t\,\hat{\mathbf y}

}.

$$

The trajectory is still a straight line with constant velocity.

In $S''$,

$$

\mathbf a''

=

-a_0\hat{\mathbf x}.

$$

With coincident origins at $t=0$,

$$

\mathbf v''

=

-a_0t\,\hat{\mathbf x}

+

v_0\hat{\mathbf y},

$$

and

$$

\boxed{

\mathbf r''(t)

=

-\frac12a_0t^2\,\hat{\mathbf x}

+

v_0t\,\hat{\mathbf y}

}.

$$

The accelerating observer therefore sees a curved trajectory even though no physical force was added to the puck.

### Physical interpretation

Newton's first law says that if the net external force on an object is zero, the object remains at rest or moves in a straight line with constant velocity.

The puck has zero acceleration in both $S$ and $S'$, so both frames satisfy Newton's first law and are inertial.

In $S''$, the puck appears to accelerate in the direction opposite the acceleration of the frame even though no physical force acts on it. Newton's first law therefore does not hold in $S''$ unless a fictitious force is introduced, so $S''$ is noninertial.

This also shows why Newton's first law is used to identify inertial frames: an inertial frame is one in which force-free objects move with constant velocity.

### What I should recognize next time

Frames related by constant-velocity transformations have the same acceleration and are both inertial. An accelerating frame changes the observed acceleration and can make a force-free object appear to accelerate.

---

## Problem 1.28 — Three-particle momentum conservation

### Work

#### Total momentum

For three particles,

$$

\boxed{

\mathbf P

=

\mathbf p_1+\mathbf p_2+\mathbf p_3

}.

$$

The equations of motion are

$$

\dot{\mathbf p}_1

=

\mathbf F_{12}

+

\mathbf F_{13}

+

\mathbf F_1^{\mathrm{ext}},

$$

$$

\dot{\mathbf p}_2

=

\mathbf F_{21}

+

\mathbf F_{23}

+

\mathbf F_2^{\mathrm{ext}},

$$

$$

\dot{\mathbf p}_3

=

\mathbf F_{31}

+

\mathbf F_{32}

+

\mathbf F_3^{\mathrm{ext}}.

$$

#### Sum of the equations of motion

Adding,

$$

\dot{\mathbf P}

=

\mathbf F_{12}

+

\mathbf F_{13}

+

\mathbf F_{21}

+

\mathbf F_{23}

+

\mathbf F_{31}

+

\mathbf F_{32}

+

\mathbf F_1^{\mathrm{ext}}

+

\mathbf F_2^{\mathrm{ext}}

+

\mathbf F_3^{\mathrm{ext}}.

$$

#### Internal-force cancellations

Newton's third law gives

$$

\mathbf F_{12}=-\mathbf F_{21},

$$

$$

\mathbf F_{13}=-\mathbf F_{31},

$$

and

$$

\mathbf F_{23}=-\mathbf F_{32}.

$$

Therefore all internal-force pairs cancel.

#### Final result

The remaining terms are the external forces:

$$

\boxed{

\frac{d\mathbf P}{dt}

=

\mathbf F_1^{\mathrm{ext}}

+

\mathbf F_2^{\mathrm{ext}}

+

\mathbf F_3^{\mathrm{ext}}

=

\mathbf F_{\mathrm{ext}}

}.

$$

If

$$

\mathbf F_{\mathrm{ext}}=0,

$$

then

$$

\frac{d\mathbf P}{dt}=0

$$

and

$$

\boxed{\mathbf P=\text{constant}}.

$$

Total momentum is therefore conserved when all interactions internal to the chosen system are included and the net external force on the system is zero.

The system boundary matters because it determines whether a force is internal or external. If two interacting particles are both inside the system, their third-law forces are internal and cancel. If only one of them is inside the system, the force exerted by the other particle crosses the system boundary and must be counted as an external force.

### What I should recognize next time

Momentum conservation is a statement about a chosen system. Internal third-law force pairs cancel; only the net external force can change the total momentum of that system.

---

## Problem 1.38 — Newton's law in tilted Cartesian coordinates

### Free-body diagram

The complete free-body diagram includes

- the weight $m\mathbf g$, vertically downward;

- the normal force $N$, perpendicular to the board.

### Coordinate definitions

Choose coordinates attached to the board:

- $x$: across the board;

- $y$: up the board;

- $z$: perpendicular to the board.

The important point is to define the axes first and then project gravity onto them.

### Force components

Gravity has no component in the $x$-direction:

$$

F_x=0.

$$

Along the board,

$$

F_y=-mg\sin\theta.

$$

Perpendicular to the board,

$$

F_z=N-mg\cos\theta.

$$

Because the puck remains on the board,

$$

a_z=0,

$$

so

$$

\boxed{N=mg\cos\theta}.

$$

The sine/cosine components follow from projections onto the chosen axes. The component along the tilted board is $mg\sin\theta$, while the component normal to it is $mg\cos\theta$.

### Equations of motion

Within the board,

$$

m\ddot x=0,

$$

$$

m\ddot y=-mg\sin\theta.

$$

Therefore

$$

\boxed{\ddot x=0},

\qquad

\boxed{\ddot y=-g\sin\theta}.

$$

### Initial conditions

Let the initial velocity components in the chosen board coordinates be

$$

\dot x(0)=v_{0x},

\qquad

\dot y(0)=v_{0y},

$$

with

$$

x(0)=y(0)=0.

$$

### Trajectory

Integrating the $x$-equation,

$$

\dot x=v_{0x},

$$

so

$$

\boxed{x(t)=v_{0x}t}.

$$

Integrating the $y$-equation,

$$

\dot y=v_{0y}-g\sin\theta\,t,

$$

so

$$

\boxed{

y(t)

=

v_{0y}t

-

\frac12g\sin\theta\,t^2

}.

$$

If the requested return corresponds to $y=0$, the nonzero return time satisfies

$$

0

=

v_{0y}t

-

\frac12g\sin\theta\,t^2,

$$

so

$$

\boxed{

t_{\mathrm{return}}

=

\frac{2v_{0y}}{g\sin\theta}

}.

$$

The corresponding displacement across the board is

$$

x_{\mathrm{return}}

=

v_{0x}t_{\mathrm{return}}

=

\boxed{

\frac{2v_{0x}v_{0y}}{g\sin\theta}

}.

$$

### Checks

As

$$

\theta\to0,

$$

the component of gravity along the board satisfies

$$

g\sin\theta\to0.

$$

The board becomes horizontal, so there is no acceleration within the board. In that limit the puck moves with constant in-plane velocity, as expected.

### What I should recognize next time

The safest way to resolve a force in rotated coordinates is to define the axes first and use projections. I initially switched the sine and cosine components by reasoning from which side of a triangle looked adjacent. The component of a vector along an axis is determined by the angle between the vector and that axis, not by the visual orientation of the sketch.

---

## Problem 1.43 — Polar basis vectors

### Work

The radial unit vector is

$$

\boxed{

\hat{\mathbf r}

=

\cos\phi\,\hat{\mathbf x}

+

\sin\phi\,\hat{\mathbf y}

}.

$$

The unit vector in the direction of increasing $\phi$ is

$$

\boxed{

\hat{\boldsymbol\phi}

=

-\sin\phi\,\hat{\mathbf x}

+

\cos\phi\,\hat{\mathbf y}

}.

$$

Differentiate $\hat{\mathbf r}$ with respect to $\phi$:

$$

\frac{d\hat{\mathbf r}}{d\phi}

=

-\sin\phi\,\hat{\mathbf x}

+

\cos\phi\,\hat{\mathbf y}

=

\hat{\boldsymbol\phi}.

$$

Using the chain rule,

$$

\boxed{

\dot{\hat{\mathbf r}}

=

\frac{d\hat{\mathbf r}}{d\phi}\dot\phi

=

\dot\phi\,\hat{\boldsymbol\phi}

}.

$$

Similarly,

$$

\frac{d\hat{\boldsymbol\phi}}{d\phi}

=

-\cos\phi\,\hat{\mathbf x}

-

\sin\phi\,\hat{\mathbf y}

=

-\hat{\mathbf r},

$$

so

$$

\boxed{

\dot{\hat{\boldsymbol\phi}}

=

-\dot\phi\,\hat{\mathbf r}

}.

$$

This immediately gives the polar-coordinate velocity:

$$

\mathbf r=r\hat{\mathbf r},

$$

so

$$

\mathbf v

=

\frac{d}{dt}(r\hat{\mathbf r})

=

\dot r\,\hat{\mathbf r}

+

r\dot{\hat{\mathbf r}},

$$

and hence

$$

\boxed{

\mathbf v

=

\dot r\,\hat{\mathbf r}

+

r\dot\phi\,\hat{\boldsymbol\phi}

}.

$$

Differentiating once more gives

$$

\boxed{

\mathbf a

=

(\ddot r-r\dot\phi^2)\hat{\mathbf r}

+

(r\ddot\phi+2\dot r\dot\phi)\hat{\boldsymbol\phi}

}.

$$

### Geometric interpretation

As $\phi$ increases, $\hat{\mathbf r}$ rotates toward the direction of increasing angle, which is $+\hat{\boldsymbol\phi}$. Therefore its derivative points in the $+\hat{\boldsymbol\phi}$ direction.

At the same time, $\hat{\boldsymbol\phi}$ rotates so that its change points inward, toward $-\hat{\mathbf r}$. This gives the minus sign in

$$

\dot{\hat{\boldsymbol\phi}}

=

-\dot\phi\,\hat{\mathbf r}.

$$

### What I should recognize next time

Polar coordinates are not just a different way to label a point. The basis vectors themselves rotate as the particle moves. The extra terms in polar velocity and acceleration arise from differentiating these moving basis vectors.

---

## Problem 1.41 — Uniform circular motion in polar coordinates

### Work

For uniform circular motion,

$$

r=R,

\qquad

\dot r=0,

\qquad

\ddot r=0,

\qquad

\dot\phi=\omega,

\qquad

\ddot\phi=0.

$$

Using

$$

\mathbf a

=

(\ddot r-r\dot\phi^2)\hat{\mathbf r}

+

(r\ddot\phi+2\dot r\dot\phi)\hat{\boldsymbol\phi},

$$

we obtain

$$

\mathbf a

=

(0-R\omega^2)\hat{\mathbf r}

+

0\hat{\boldsymbol\phi}.

$$

Therefore

$$

\boxed{

\mathbf a=-R\omega^2\hat{\mathbf r}

}.

$$

This is the centripetal acceleration. The negative sign means that it points inward because $+\hat{\mathbf r}$ points outward.

#### Radial equation

The string tension points inward:

$$

\mathbf T=-T\hat{\mathbf r}.

$$

Newton's second law gives

$$

-T=-mR\omega^2,

$$

so

$$

\boxed{T=mR\omega^2}.

$$

Since $v=R\omega$,

$$

\boxed{

T=\frac{mv^2}{R}

}.

$$

#### Angular equation

There is no tangential force and no tangential acceleration:

$$

F_\phi=ma_\phi=0.

$$

#### Final result

$$

\boxed{T=mR\omega^2=\frac{mv^2}{R}}.

$$

The units are

$$

[mR\omega^2]

=

\mathrm{kg}\,\mathrm m\,\mathrm s^{-2}

=

\mathrm N.

$$

### What I should recognize next time

For fixed-radius uniform circular motion, the full polar acceleration formula immediately reduces to an inward radial acceleration. The radial force must therefore point inward and have magnitude $mR\omega^2$.

---

# 3. Computational problem

## Problem 1.50 — Exact nonlinear motion versus the small-angle approximation

### Derivation of the exact equation

For motion constrained to a circular ramp of radius $R$,

$$

r=R,

\qquad

\dot r=\ddot r=0.

$$

The tangential component of gravity is

$$

F_\phi=-mg\sin\phi.

$$

The tangential component of Newton's second law is

$$

F_\phi

=

m(r\ddot\phi+2\dot r\dot\phi).

$$

Since $r=R$ is constant,

$$

-mg\sin\phi

=

mR\ddot\phi.

$$

Therefore

$$

\boxed{

\ddot\phi

=

-\frac{g}{R}\sin\phi

}.

$$

This equation is nonlinear because the unknown $\phi$ appears inside the nonlinear function $\sin\phi$.

### Small-angle approximation

For small angles measured in radians,

$$

\sin\phi\approx\phi.

$$

Therefore

$$

\ddot\phi

=

-\frac{g}{R}\phi.

$$

Define

$$

\omega^2=\frac{g}{R}.

$$

Then

$$

\ddot\phi+\omega^2\phi=0.

$$

The general solution is

$$

\phi(t)

=

A\sin(\omega t)

+

B\cos(\omega t).

$$

For

$$

\phi(0)=\phi_0,

\qquad

\dot\phi(0)=0,

$$

we get

$$

B=\phi_0,

\qquad

A=0.

$$

Thus

$$

\boxed{

\phi_{\mathrm{small}}(t)

=

\phi_0\cos(\omega t)

},

$$

where

$$

\omega=\sqrt{\frac gR}.

$$

The small-angle period is

$$

\boxed{

T_{\mathrm{small}}

=

\frac{2\pi}{\omega}

=

2\pi\sqrt{\frac Rg}

}.

$$

### First-order system

To solve the nonlinear second-order equation numerically, define

$$

\omega_\phi=\dot\phi.

$$

Then

$$

\boxed{

\dot\phi=\omega_\phi

}

$$

and

$$

\boxed{

\dot\omega_\phi

=

-\frac{g}{R}\sin\phi

}.

$$

This is the form used by the numerical ODE solver.

### Results

The [Python notebook for Problem 1.50](code/problem-1-50-skateboard.ipynb)

contains the computational analysis. It:

- solves the exact nonlinear equation numerically with `solve_ivp`;

- computes the analytic small-angle solution;

- compares the exact and approximate angle trajectories;

- compares the corresponding paths on the circular ramp;

- examines multiple initial angles;

- calculates maximum absolute and RMS trajectory errors over an angle sweep;

- checks numerically that the exact and approximate solutions agree for a very small initial angle;

- contains the separate period comparison and additional computational work completed for the problem.

### Interpretation

At small initial angles,

$$

\sin\phi\approx\phi,

$$

so the nonlinear and small-angle equations produce nearly identical motion.

As the initial angle becomes larger, $\sin\phi$ increasingly differs from $\phi$. For positive $\phi$,

$$

\sin\phi<\phi,

$$

so the exact restoring acceleration has smaller magnitude than the linearized model predicts. The exact motion therefore takes longer to complete a cycle.

The small-angle model predicts an amplitude-independent period

$$

T=2\pi\sqrt{\frac Rg},

$$

whereas the exact nonlinear period increases with amplitude. As a result, the exact and approximate trajectories gradually drift out of phase at larger initial angles.

### What I should recognize next time

The skateboard problem is an initial-value problem for a nonlinear second-order differential equation. The main workflow is:

$$

\text{forces}

\longrightarrow

\text{coordinate components}

\longrightarrow

\text{equation of motion}

\longrightarrow

\text{initial conditions}

\longrightarrow

\text{analytic or numerical solution}.

$$

The small-angle approximation changes the nonlinear equation into a linear harmonic oscillator. The computational comparison shows when that approximation is justified and when its error becomes physically important.

---

# 4. Optional stretch problems

## Problem 1.31 — Momentum conservation implies the third law

### Work

Not completed.

---

## Problem 1.45 — Constant-magnitude vector

### Work

Not completed.

---

## Problem 1.46 — Rotating reference frame

### Work

Not completed.

---

## Problem 1.47 — Cylindrical-coordinate extension

### Work

Not completed.

---

# 5. Completion checklist

## Quick diagnostics

- [x] Problem 1.10

- [x] Problem 1.24

## Core written problems

- [x] Problem 1.26

- [x] Problem 1.28

- [x] Problem 1.38

- [x] Problem 1.43

- [x] Problem 1.41

## Computational work

- [x] Problem 1.50

- [x] Code completed

- [x] Figures generated

- [x] Physical interpretation written



---

# 6. End-of-chapter reflection

## Hardest problem

Problem 1.50 was the hardest because it required several ideas at once: polar-coordinate dynamics, force decomposition, differential equations, initial conditions, linearization, and numerical solution. The main material I had to review was differential equations, especially how a second-order equation is treated as an initial-value problem and how it is converted into a first-order system for numerical work.

## Most useful problem

Problem 1.50 was the most useful because it connected most of the chapter. Problem 1.43 was also especially useful because deriving the rotating polar basis vectors made the later polar-coordinate equations much less mysterious.

## Most important mistake

The most important mistake occurred in Problem 1.38. I initially switched the sine and cosine components of gravity because I was reasoning from which side of the drawn triangle looked adjacent. The better method is to define the coordinate axes first and then project the force vector onto each axis.

## Problem I should repeat later

I should repeat Problem 1.43, especially the derivation of the polar-coordinate velocity and acceleration formulas. I want to be able to reproduce these from the Cartesian definitions of $\hat{\mathbf r}$ and $\hat{\boldsymbol\phi}$ rather than memorize the final formulas.

## What I now understand that I did not understand before

Polar coordinates now make sense to me as a moving basis rather than just another way to label points. The basis vectors $\hat{\mathbf r}$ and $\hat{\boldsymbol\phi}$ change direction as the particle moves, and the extra terms in the polar acceleration formula arise from differentiating those moving basis vectors.

I also have a clearer picture of Newtonian mechanics as a general workflow:

$$

\boxed{

\text{physical forces}

\longrightarrow

\text{coordinate components}

\longrightarrow

\text{differential equations}

\longrightarrow

\text{initial conditions}

\longrightarrow

\text{motion}

}

$$

The skateboard problem made this connection especially clear. I needed to refresh differential equations in order to solve the equation of motion, and once the polar-coordinate derivation was understood, the structure of the problem became much more natural.