# Chapter 2 — Problems

**Text:** John R. Taylor, *Classical Mechanics*  
**Chapter:** 2 — Projectiles and Charged Particles

---

## Purpose of this problem set

This is a deliberately **small, balanced set**. The goal is not to work every exercise in Chapter 2.

The set is chosen to make sure I can:

- reason physically about drag;
- solve and interpret the important differential equations;
- use approximations correctly;
- handle quadratic drag;
- understand magnetic motion and complex exponentials;
- do one meaningful computational problem;
- push beyond the standard derivations with one or two stretch problems.

There are **no optional filler problems**. The core problems are the problems I intend to complete. The two stretch problems are part of the plan, but should come after the core work.

---

# 1. Core problems

## Problem 2.1 — When linear versus quadratic drag matters

### Why this problem is here

This checks whether I understand the physical meaning of

```math
f_{\rm lin}=bv,
\qquad
f_{\rm quad}=cv^2,
```

rather than treating them as arbitrary formulas.

### What I should get from it

- compare the two drag terms;
- identify the crossover speed;
- understand why quadratic drag dominates at higher speeds;
- connect object size and speed to the appropriate drag model.

### Work

#### Ratio of drag terms

```math
\frac{f_{\rm quad}}{f_{\rm lin}}
=
```

#### Condition for equal importance

```math
f_{\rm quad}=f_{\rm lin}
```

implies

```math
v=
```

### Physical interpretation

> 

### What I should recognize next time

> 

---

## Problem 2.6 — Recover free fall from the linear-drag solution

### Why this problem is here

This is the chapter's first important **limiting-case / approximation** problem.

The exact linear-drag solution must reduce to ordinary free fall before the object has had enough time to build up significant drag.

### Starting point

For an object dropped from rest,

```math
v(t)
=
v_{\rm ter}
\left(
1-e^{-t/\tau}
\right).
```

Use

```math
e^{-t/\tau}
=
1-\frac{t}{\tau}
+\frac12\left(\frac{t}{\tau}\right)^2
-\cdots.
```

### Velocity limit

Show that for \(t\ll\tau\),

```math
v(t)\approx gt.
```

### Position limit

Use the corresponding position solution to show

```math
y(t)\approx\frac12gt^2.
```

### Conceptual question

Why is the relevant small quantity \(t/\tau\), rather than simply \(t\)?

> 

### What I should recognize next time

> 

---

## Problem 2.17 — Eliminate time and derive the trajectory

### Why this problem is here

This makes me connect the separate \(x(t)\) and \(y(t)\) solutions into the actual path of a projectile.

### Starting equations

Write Taylor's linear-drag projectile equations:

```math
x(t)=
```

```math
y(t)=
```

### Solve for time

From \(x(t)\),

```math
t=
```

### Substitute

Obtain

```math
\boxed{
y=y(x)
}.
```

### Checks

- [ ] Dimensions are correct.
- [ ] \(y(0)=0\).
- [ ] The expression has the correct vacuum limit.
- [ ] I understand the vertical asymptote / limiting horizontal distance.

### Physical interpretation

> 

### What I should recognize next time

> 

---

## Problem 2.35 — Derive the quadratic-drag fall solution

### Why this problem is here

This is the main analytic quadratic-drag derivation. It combines Newton's law, separation of variables, terminal velocity, hyperbolic functions, and limiting behavior.

### Starting equation

Take downward as positive:

```math
m\dot v
=
mg-cv^2.
```

### Terminal speed

Derive

```math
\boxed{
v_{\rm ter}
=
\sqrt{\frac{mg}{c}}
}.
```

Then rewrite the ODE as

```math
\dot v
=
g
\left(
1-\frac{v^2}{v_{\rm ter}^2}
\right).
```

### Separation

```math
\frac{dv}
{1-v^2/v_{\rm ter}^2}
=
g\,dt.
```

Carry out the integral and derive

```math
\boxed{
v(t)
=
v_{\rm ter}
\tanh
\left(
\frac{gt}{v_{\rm ter}}
\right)
}.
```

### Position

Integrate again to obtain \(y(t)\).

```math
y(t)=
```

### Checks

- [ ] \(v(0)=0\).
- [ ] \(v(t)\to v_{\rm ter}\).
- [ ] Small-time behavior matches vacuum free fall.
- [ ] Late-time position is approximately linear in \(t\).

### Physical interpretation

> 

### What I should recognize next time

> 

---

## Problem 2.52 — Interpret the complex magnetic solution

### Why this problem is here

This makes sure complex exponentials are not just formal manipulation. I should be able to recover the real velocity components and see the circular motion.

### Starting point

Use Taylor's complex transverse velocity

```math
\eta(t)=v_x(t)+iv_y(t).
```

Write the solution in exponential form and use

```math
e^{i\theta}
=
\cos\theta+i\sin\theta.
```

### Extract the real components

```math
v_x(t)=
```

```math
v_y(t)=
```

### Show constant transverse speed

```math
v_x^2+v_y^2=
```

### Interpretation

- angular frequency:
- speed:
- direction of rotation:
- effect of changing the sign of \(q\):

### What I should recognize next time

> 

---

## Problem 2.53 — Lorentz force and full 3D motion

### Why this problem is here

This is the core magnetic-force problem. It requires turning

```math
\mathbf F
=
q
\left(
\mathbf E+\mathbf v\times\mathbf B
\right)
```

into equations of motion and then interpreting the resulting trajectory.

### Step 1 — Draw the geometry

Define the directions of \(\mathbf E\), \(\mathbf B\), and the coordinate axes.

### Step 2 — Compute the cross product

```math
\mathbf v\times\mathbf B=
```

### Step 3 — Component equations

```math
m\dot v_x=
```

```math
m\dot v_y=
```

```math
m\dot v_z=
```

### Step 4 — Solve

Find

```math
v_x(t),\qquad v_y(t),\qquad v_z(t).
```

Then integrate for position.

### Physical interpretation

Describe the motion in words before looking at the final algebra:

> 

### Checks

- [ ] Magnetic force is perpendicular to transverse velocity.
- [ ] Magnetic part does no work.
- [ ] The sign of \(q\) controls rotation direction.
- [ ] The \(z\)-motion agrees with the electric force.

### What I should recognize next time

> 

---

# 2. Required computational problem

## Problem 2.43 — Two-dimensional projectile motion with quadratic drag

### Why this problem is here

Quadratic drag in two dimensions gives genuinely coupled nonlinear differential equations. This is the natural computational problem for Chapter 2.

Unlike the Chapter 1 skateboard problem, the numerical method is not just being used to compare an exact nonlinear equation with a linear approximation. Here the full two-dimensional equations generally do not decouple into simple analytic solutions.

### Model

With \(y\) upward,

```math
m\dot v_x
=
-cvv_x,
```

```math
m\dot v_y
=
-mg-cvv_y,
```

where

```math
v
=
\sqrt{v_x^2+v_y^2}.
```

Add

```math
\dot x=v_x,
```

```math
\dot y=v_y.
```

### First-order system

Write the state vector

```math
\mathbf z
=
(x,y,v_x,v_y).
```

Then write

```math
\dot{\mathbf z}
=
```

explicitly.

### Computational tasks

- [ ] Set the initial position and launch velocity from Problem 2.43.
- [ ] Solve the coupled system numerically.
- [ ] Stop the integration when the projectile hits the floor.
- [ ] Plot the quadratic-drag trajectory.
- [ ] Plot the vacuum trajectory on the same axes.
- [ ] Compute the horizontal range in both cases.
- [ ] Plot \(v_x(t)\) and \(v_y(t)\).
- [ ] Plot the speed \(v(t)\).
- [ ] Verify the initial conditions numerically.
- [ ] Explain the physical differences between the two trajectories.

### Suggested notebook

```text
code/problem-2-43-quadratic-drag.ipynb
```

### Questions to answer from the computation

1. How much does quadratic drag reduce the range?
2. How does the ascent differ from the descent?
3. Does \(v_x\) ever change sign?
4. Why do \(v_x\) and \(v_y\) have to be solved simultaneously?
5. Which features of the solution can be predicted before running the code?

### What I should recognize next time

> 

---

# 3. Stretch problems

These are deliberately chosen to deepen the chapter rather than add repetitive practice.

## Problem 2.41 — Upward motion with quadratic drag

### Why this is a stretch problem

The force changes its mathematical form depending on the direction of motion because drag always opposes the velocity.

This problem also uses the identity

```math
a
=
v\frac{dv}{dy},
```

which provides another way to solve Newton's equation.

### Goals

- [ ] Write the correct equation during the upward journey.
- [ ] Replace \(\dot v\) with \(v\,dv/dy\).
- [ ] Separate variables.
- [ ] Derive \(v(y)\).
- [ ] Derive the maximum height.
- [ ] Compare with the vacuum result.
- [ ] Explain physically why drag reduces the maximum height.

### Main conceptual question

Why must the upward and downward portions of quadratic-drag motion be treated carefully as separate cases?

> 

### What I should recognize next time

> 

---

## Problem 2.54 — Solve the magnetic equations without complex numbers

### Why this is a stretch problem

The chapter solves the magnetic equations elegantly using

```math
v_x+iv_y.
```

This problem makes me solve the same physics using ordinary real differential equations.

That comparison should clarify what the complex-number trick is actually buying me.

### Starting equations

```math
\dot v_x=\Omega v_y,
```

```math
\dot v_y=-\Omega v_x.
```

Differentiate the first equation:

```math
\ddot v_x=
```

Use the second equation to show

```math
\boxed{
\ddot v_x+\Omega^2v_x=0
}.
```

### Solve

```math
v_x(t)=
```

Then obtain

```math
v_y(t)=
```

from the original first-order relation.

### Compare with the complex solution

Write one paragraph answering:

> Why is the complex-exponential method shorter, and what physical structure does it make especially clear?

### What I should recognize next time

> 

---

# 4. Completion checklist

## Core

- [ ] 2.1 — Linear versus quadratic drag
- [ ] 2.6 — Vacuum limit / Taylor expansion
- [ ] 2.17 — Projectile trajectory \(y(x)\)
- [ ] 2.35 — Vertical quadratic drag
- [ ] 2.52 — Complex magnetic solution
- [ ] 2.53 — Lorentz force and 3D motion

## Computational

- [ ] 2.43 — Coupled quadratic-drag projectile

## Stretch

- [ ] 2.41 — Upward quadratic drag
- [ ] 2.54 — Magnetic motion without complex notation

---

# 5. End-of-chapter reflection

## Hardest problem

> 

## Most useful problem

> 

## Most important mistake

> 

## Problem I should repeat later

> 

## What I understand now that I did not understand before

> 

## One mathematical skill I had to review

> 
