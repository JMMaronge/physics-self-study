# Chapter 2 — Projectiles and Charged Particles

**Text:** John R. Taylor, *Classical Mechanics*  
**Chapter:** 2 — Projectiles and Charged Particles  
**Dates studied:**  
**Status:** Not started

---

## How to use this file

This is the **notes and derivations sheet** for Chapter 2.

Use it to record:

- the chapter's main ideas;
- definitions and assumptions;
- physical interpretations;
- derivations I should be able to reproduce;
- approximations and limiting cases;
- computational checks;
- questions, mistakes, and connections.

The separate exercise sheet is:

`chapter2_problems.md`

The goal is not to memorize formulas. By the end of the chapter, I should be able to start from Newton's second law and derive the important results.

---

# 1. Chapter purpose

## One-sentence summary

> 

## My current interpretation

Chapter 2 takes the Newtonian framework from Chapter 1 and applies it to forces that depend on velocity. The two main examples are resistive forces on projectiles and the magnetic Lorentz force on charged particles.

The chapter is also a mathematical bridge: exponential decay, terminal behavior, Taylor expansions, coupled differential equations, hyperbolic functions, and complex exponentials all appear naturally from physical problems.

## What should feel familiar from Chapter 1?

- Newton's second law as a differential equation;
- choosing coordinates;
- resolving vectors into components;
- initial-value problems;
- first- and second-order differential equations;
- checking limiting cases.

## What is likely to be genuinely new or rusty?

- velocity-dependent forces;
- linear versus quadratic drag;
- terminal velocity and characteristic times;
- coupled differential equations;
- Taylor-series approximations;
- hyperbolic functions;
- the Lorentz force;
- complex exponentials as a tool for two-dimensional motion.

---

# 2. Learning objectives

By the end of the chapter, I should be able to:

- [ ] Write a drag force as a vector opposite the velocity.
- [ ] Distinguish linear and quadratic drag physically and mathematically.
- [ ] Explain when linear or quadratic drag dominates.
- [ ] Solve one-dimensional motion with linear drag.
- [ ] Derive and interpret terminal velocity.
- [ ] Interpret the characteristic time \(\tau=m/b\).
- [ ] Solve projectile motion with linear drag in Cartesian components.
- [ ] Eliminate time to obtain a trajectory \(y(x)\).
- [ ] Recover the vacuum limit using a Taylor expansion.
- [ ] Explain why quadratic drag couples the Cartesian equations.
- [ ] Derive the vertical quadratic-drag solution.
- [ ] Explain why \(\tanh\) and \(\ln\cosh\) appear.
- [ ] Write and interpret the magnetic Lorentz force.
- [ ] Explain why a magnetic field changes direction but not speed.
- [ ] Derive circular and helical motion in a uniform magnetic field.
- [ ] Use Euler's formula and complex exponentials comfortably.
- [ ] Combine two coupled real ODEs into one complex ODE.
- [ ] Interpret a complex solution as real physical motion.

---

# 3. Section notes

## 2.1 Air Resistance

### Central idea

For a nonrotating projectile in a stationary fluid, drag acts opposite the velocity:

```math
\mathbf f=-f(v)\hat{\mathbf v}.
```

Why is the minus sign there?

> 

### Linear and quadratic terms

Taylor models the magnitude approximately as

```math
f(v)=bv+cv^2.
```

Thus

```math
\mathbf f
=
-\left(bv+cv^2\right)\hat{\mathbf v}.
```

Interpret:

- \(b\):
- \(c\):

The ratio is

```math
\frac{f_{\rm quad}}{f_{\rm lin}}
=
\frac{cv}{b}.
```

Therefore:

- small \(v\):
- large \(v\):

### Physical questions

- Why does drag depend on velocity relative to the medium?
- Why can linear drag dominate at low speed?
- Why can quadratic drag dominate at high speed?
- What assumptions are hidden in assuming drag is exactly opposite \(\mathbf v\)?

### My takeaway

> 

---

## 2.2 Linear Air Resistance

Assume

```math
\mathbf f=-b\mathbf v.
```

The useful feature is that the Cartesian components separate.

---

### Horizontal motion

Newton's second law gives

```math
m\dot v_x=-bv_x.
```

Define

```math
\tau=\frac{m}{b}.
```

Then

```math
\dot v_x=-\frac{1}{\tau}v_x.
```

Derive

```math
v_x(t)=v_{x0}e^{-t/\tau}.
```

Integrate to obtain

```math
x(t)
=
v_{x0}\tau
\left(1-e^{-t/\tau}\right)
```

for \(x(0)=0\).

### Interpretation of the time constant

At \(t=\tau\),

```math
v_x(\tau)=\frac{v_{x0}}{e}.
```

What does this mean physically?

> 

What happens as \(t\to\infty\)?

> 

---

### Vertical fall with linear drag

Take downward as positive:

```math
m\dot v
=
mg-bv.
```

Rearrange:

```math
\dot v
+
\frac{1}{\tau}v
=
g.
```

### Terminal speed

At terminal speed,

```math
\dot v=0.
```

Therefore

```math
\boxed{
v_{\rm ter}
=
\frac{mg}{b}
=
g\tau
}.
```

Explain physically what terminal velocity means:

> 

### General velocity

Derive

```math
v(t)
=
v_{\rm ter}
+
\left(v_0-v_{\rm ter}\right)e^{-t/\tau}.
```

For release from rest:

```math
v(t)
=
v_{\rm ter}
\left(1-e^{-t/\tau}\right).
```

### Position

For \(v_0=0\) and \(y(0)=0\), derive

```math
y(t)=
```

### Limiting-case check

For \(t\ll\tau\),

```math
e^{-t/\tau}
\approx
1-\frac{t}{\tau}
+\frac12\left(\frac{t}{\tau}\right)^2-\cdots.
```

Show that

```math
v\approx gt,
```

and

```math
y\approx\frac12gt^2.
```

### What I should recognize next time

> Linear drag produces exponential relaxation toward terminal behavior. The natural timescale is \(\tau=m/b\).

---

## 2.3 Trajectory and Range in a Linear Medium

Take \(y\) positive upward and launch with

```math
v_{x0}=v_0\cos\theta,
```

```math
v_{y0}=v_0\sin\theta.
```

### Component equations

```math
m\dot v_x=-bv_x,
```

```math
m\dot v_y=-mg-bv_y.
```

Why are these equations uncoupled?

> 

### Solve for velocity

```math
v_x(t)=
```

```math
v_y(t)=
```

### Solve for position

```math
x(t)=
```

```math
y(t)=
```

### Eliminate time

Solve \(x(t)\) for \(t\):

```math
t=t(x).
```

Substitute into \(y(t)\):

```math
y=y(x).
```

### Compare with vacuum motion

Vacuum:

```math
y_{\rm vac}(x)
=
x\tan\theta
-
\frac{gx^2}
{2v_0^2\cos^2\theta}.
```

What changes when drag is present?

> 

Why does the linear-drag trajectory have a finite limiting horizontal coordinate?

> 

### Range

The range is determined by

```math
y(R)=0.
```

Why does this become a transcendental equation?

> 

### Approximation strategy

Taylor expansions allow a complicated exact relation to be approximated when a dimensionless quantity is small.

General workflow:

```text
exact expression
→ identify small dimensionless parameter
→ expand
→ keep leading terms
→ solve simpler equation
→ check neglected terms
```

### What I should recognize next time

> 

---

## 2.4 Quadratic Air Resistance

Assume

```math
\mathbf f
=
-cv^2\hat{\mathbf v}.
```

Since

```math
\mathbf v=v\hat{\mathbf v},
```

we can write

```math
\mathbf f=-cv\mathbf v.
```

### Why the 2D equations are coupled

```math
f_x=-cvv_x,
```

```math
f_y=-cvv_y,
```

with

```math
v=\sqrt{v_x^2+v_y^2}.
```

Explain why neither equation can be solved independently of the other:

> 

This is an important contrast with linear drag.

---

### Vertical fall

Take downward as positive:

```math
m\dot v=mg-cv^2.
```

At terminal speed:

```math
mg=cv_{\rm ter}^2.
```

Thus

```math
\boxed{
v_{\rm ter}
=
\sqrt{\frac{mg}{c}}
}.
```

Rewrite the equation as

```math
\dot v
=
g
\left(
1-\frac{v^2}{v_{\rm ter}^2}
\right).
```

Separate:

```math
\frac{dv}
{1-v^2/v_{\rm ter}^2}
=
g\,dt.
```

For release from rest, derive

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

Integrate \(v(t)\) and obtain

```math
y(t)=
```

Why does \(\ln\cosh\) appear?

> 

### Limiting cases

Check:

- \(t\to0\): recover free fall;
- \(t\to\infty\): \(v\to v_{\rm ter}\);
- at late times: \(y(t)\) becomes approximately linear.

### Linear versus quadratic drag

| Feature | Linear drag | Quadratic drag |
|---|---|---|
| Force magnitude | \(bv\) | \(cv^2\) |
| Terminal speed |  |  |
| 2D Cartesian equations | uncoupled | coupled |
| Typical analytic functions | exponentials | hyperbolic functions |
| Most important at |  |  |

### What I should recognize next time

> 

---

## 2.5 Motion of a Charge in a Uniform Magnetic Field

The Lorentz force is

```math
\boxed{
\mathbf F
=
q\left(
\mathbf E+\mathbf v\times\mathbf B
\right)
}.
```

For a pure magnetic field,

```math
\mathbf F=q\mathbf v\times\mathbf B.
```

### Why magnetic fields do no work

Because

```math
\mathbf v\times\mathbf B
```

is perpendicular to \(\mathbf v\),

```math
\mathbf F\cdot\mathbf v=0.
```

Therefore

```math
\frac{d}{dt}
\left(
\frac12mv^2
\right)
=0.
```

So a magnetic field changes:

- [ ] speed
- [ ] direction

Explain:

> 

---

### Choose \(\mathbf B=B\hat{\mathbf z}\)

Write

```math
\mathbf v
=
v_x\hat{\mathbf x}
+
v_y\hat{\mathbf y}
+
v_z\hat{\mathbf z}.
```

Compute

```math
\mathbf v\times\mathbf B=
```

and derive

```math
m\dot v_x=
```

```math
m\dot v_y=
```

```math
m\dot v_z=
```

### Consequences

What happens to \(v_z\)?

> 

What happens in the \(xy\)-plane?

> 

### Cyclotron frequency

```math
\boxed{
\omega_c=\frac{|q|B}{m}
}.
```

Why does the sign of \(q\) reverse the direction of rotation without changing the frequency magnitude?

> 

### Radius

For perpendicular motion,

```math
|q|v_\perp B
=
\frac{mv_\perp^2}{R}.
```

Thus

```math
\boxed{
R
=
\frac{mv_\perp}{|q|B}
}.
```

Interpret how \(R\) changes with:

- \(m\):
- \(v_\perp\):
- \(B\):
- \(|q|\):

### Helical motion

If \(v_z\neq0\), explain why the trajectory becomes a helix:

> 

### What I should recognize next time

> 

---

## 2.6 Complex Exponentials

### Euler's formula

```math
\boxed{
e^{i\theta}
=
\cos\theta+i\sin\theta
}.
```

Therefore

```math
\cos\theta
=
\frac{e^{i\theta}+e^{-i\theta}}{2},
```

```math
\sin\theta
=
\frac{e^{i\theta}-e^{-i\theta}}{2i}.
```

### Geometry

For

```math
z=re^{i\theta},
```

interpret:

- \(r\):
- \(\theta\):

What does multiplication by \(e^{i\alpha}\) do geometrically?

> 

### Differentiation

```math
\frac{d}{dt}
e^{i\omega t}
=
i\omega e^{i\omega t}.
```

Why is this useful for rotational motion?

> 

### Key conceptual point

Complex notation is a mathematical representation of two real quantities. If

```math
u=v_x+iv_y,
```

then

```math
v_x=\operatorname{Re}u,
```

```math
v_y=\operatorname{Im}u.
```

### What I should recognize next time

> Complex exponentials package sine and cosine into a single object whose derivative has the same form.

---

## 2.7 Solution for the Charge in a \(B\) Field

For \(\mathbf B=B\hat{\mathbf z}\), the planar equations are coupled.

Write them in the form

```math
\dot v_x=\Omega v_y,
```

```math
\dot v_y=-\Omega v_x,
```

where the sign of

```math
\Omega=\frac{qB}{m}
```

contains the charge sign.

### Complex velocity

Define

```math
u=v_x+iv_y.
```

Then

```math
\dot u
=
\dot v_x+i\dot v_y.
```

Use the real equations to show

```math
\dot u=
```

and solve:

```math
u(t)=
```

### Recover the physical solution

Extract:

```math
v_x(t)=
```

```math
v_y(t)=
```

Then integrate to obtain:

```math
x(t)=
```

```math
y(t)=
```

### Physical interpretation

Show that the trajectory in the plane perpendicular to \(\mathbf B\) is circular.

Identify:

- angular frequency:
- radius:
- center:
- direction of rotation:

### What I should recognize next time

> Two coupled real first-order equations describing rotation can often be combined into one complex first-order equation.

---

# 4. Essential derivations

## Derivation 1 — Linear drag in one dimension

Start from

```math
m\dot v=-bv.
```

Derive

```math
v(t)=v_0e^{-t/\tau},
\qquad
\tau=\frac{m}{b},
```

then integrate for \(x(t)\).

### Reproduce from memory

- [ ] First attempt
- [ ] One-week review
- [ ] End-of-chapter review

---

## Derivation 2 — Terminal velocity with linear drag

Start from

```math
m\dot v=mg-bv.
```

Derive

```math
v_{\rm ter}=\frac{mg}{b}=g\tau
```

and

```math
v(t)
=
v_{\rm ter}
+
(v_0-v_{\rm ter})e^{-t/\tau}.
```

### Reproduce from memory

- [ ] Terminal velocity
- [ ] General velocity
- [ ] Position
- [ ] Small-time limit

---

## Derivation 3 — Linear-drag projectile trajectory

Derive \(x(t)\) and \(y(t)\), eliminate \(t\), and obtain \(y(x)\).

### Checks

- [ ] Explain why the components decouple.
- [ ] Recover the vacuum limit.
- [ ] Explain the limiting horizontal distance.

---

## Derivation 4 — Vertical quadratic drag

Start from

```math
m\dot v=mg-cv^2.
```

Derive

```math
v_{\rm ter}=\sqrt{\frac{mg}{c}}
```

and

```math
v(t)
=
v_{\rm ter}
\tanh\left(
\frac{gt}{v_{\rm ter}}
\right).
```

Then integrate for \(y(t)\).

### Reproduce from memory

- [ ] Separation of variables
- [ ] Hyperbolic-function integral
- [ ] Position
- [ ] Limiting cases

---

## Derivation 5 — Circular motion in a magnetic field

Start from

```math
m\dot{\mathbf v}
=
q\mathbf v\times\mathbf B.
```

For \(\mathbf B=B\hat{\mathbf z}\):

1. compute the cross product;
2. derive the component equations;
3. show that speed is constant;
4. derive

```math
\omega_c=\frac{|q|B}{m};
```

5. derive

```math
R=\frac{mv_\perp}{|q|B}.
```

### Reproduce from memory

- [ ] Cross product
- [ ] Component equations
- [ ] Constant-speed argument
- [ ] Frequency
- [ ] Radius

---

## Derivation 6 — Complex solution of the magnetic equations

Define

```math
u=v_x+iv_y.
```

Combine the coupled equations into one ODE, solve it, and extract the real motion.

### Reproduce from memory

- [ ] Combine equations
- [ ] Solve complex ODE
- [ ] Extract \(v_x,v_y\)
- [ ] Integrate for position
- [ ] Interpret circle

---

# 5. Mathematics review

## Separation of variables

Recognize

```math
\dot y=f(y)
```

and rewrite it as

```math
\frac{dy}{f(y)}=dt.
```

- [ ] I can identify when separation is valid.
- [ ] I can apply limits directly when initial conditions are known.

---

## First-order linear ODEs

Recognize

```math
\dot y+ay=b.
```

Be able to solve using:

- homogeneous + particular solution;
- separation when possible;
- integrating factor if needed.

- [ ] Comfortable
- [ ] Needs review

---

## Taylor series

Know the core expansions:

```math
e^x
=
1+x+\frac{x^2}{2!}
+\frac{x^3}{3!}
+\cdots,
```

```math
\sin x
=
x-\frac{x^3}{3!}
+\frac{x^5}{5!}
-\cdots,
```

```math
\cos x
=
1-\frac{x^2}{2!}
+\frac{x^4}{4!}
-\cdots,
```

```math
\ln(1+x)
=
x-\frac{x^2}{2}
+\frac{x^3}{3}
-\cdots.
```

Questions:

- Why should the expansion parameter be dimensionless?
- How do I know how many terms to keep?
- How can I estimate the size of the neglected term?

---

## Hyperbolic functions

```math
\sinh x
=
\frac{e^x-e^{-x}}{2},
```

```math
\cosh x
=
\frac{e^x+e^{-x}}{2},
```

```math
\tanh x
=
\frac{\sinh x}{\cosh x}.
```

Know

```math
\frac{d}{dx}\tanh x
=
\operatorname{sech}^2x,
```

and

```math
1-\tanh^2x
=
\operatorname{sech}^2x.
```

Why is \(\tanh\) a natural function for terminal velocity?

> 

---

## Complex numbers

```math
i^2=-1,
```

```math
z=x+iy,
```

```math
|z|=\sqrt{x^2+y^2},
```

```math
e^{i\theta}
=
\cos\theta+i\sin\theta.
```

The important idea is not complex arithmetic for its own sake. It is that planar rotations naturally have the same algebraic structure as multiplication by a complex phase.

---

# 6. Computational experiment

The required computational work for this chapter is **Taylor Problem 2.43** in the separate problems sheet.

The goal is to solve the coupled two-dimensional equations for quadratic drag numerically and compare the result with vacuum projectile motion.

Suggested code location:

```text
code/problem-2-43-quadratic-drag.ipynb
```

Suggested outputs:

- trajectory with quadratic drag;
- trajectory in vacuum;
- horizontal range comparison;
- velocity components versus time;
- speed versus time;
- a short physical interpretation.

---

# 7. Mistake and confusion log

| Issue | Why I was confused | Resolution |
|---|---|---|
| | | |
| | | |
| | | |
| | | |

---

# 8. Connections

## Connection to Chapter 1

Chapter 1 emphasized

```math
m\ddot{\mathbf r}
=
\mathbf F(\mathbf r,\dot{\mathbf r},t).
```

Chapter 2 now gives important examples in which the force explicitly depends on velocity:

```math
\mathbf f=-b\mathbf v,
```

```math
\mathbf f=-cv\mathbf v,
```

```math
\mathbf F_B=q\mathbf v\times\mathbf B.
```

This makes the differential-equation viewpoint from Chapter 1 essential.

---

## Approximation as a physics tool

Chapter 1 used

```math
\sin\phi\approx\phi.
```

Chapter 2 uses the same philosophy more systematically:

```text
exact model
→ identify a small dimensionless quantity
→ expand
→ truncate
→ solve
→ compare with the exact/numerical result
```

This is a major recurring pattern in physics.

---

## Coupled equations

Linear drag in Cartesian coordinates gives uncoupled equations.

Quadratic drag gives coupled equations because

```math
v=\sqrt{v_x^2+v_y^2}.
```

Magnetic motion also gives coupled equations, but they have a special rotational structure that can be simplified using complex numbers.

Question:

> What structural feature makes the magnetic equations analytically solvable while general 2D quadratic drag usually requires numerical methods?

---

## Future connection to linear algebra

The magnetic equations can be written as

```math
\frac{d}{dt}
\begin{pmatrix}
v_x\\
v_y
\end{pmatrix}
=
A
\begin{pmatrix}
v_x\\
v_y
\end{pmatrix}.
```

This will later connect naturally to:

- eigenvalues;
- matrix exponentials;
- normal modes;
- Hamiltonian mechanics;
- quantum mechanics.

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

## Three derivations I must reproduce

1. 
2. 
3. 

## Hardest idea

> 

## Most useful idea

> 

## Most important mistake

> 

## One problem I should repeat

> 

## One remaining question

> 

---

# 10. Mastery check

I am ready to move to Chapter 3 when I can:

- [ ] Explain linear versus quadratic drag.
- [ ] Derive the linear-drag exponential solution.
- [ ] Derive terminal velocity and explain \(\tau=m/b\).
- [ ] Derive the linear-drag projectile equations.
- [ ] Eliminate time to obtain \(y(x)\).
- [ ] Recover the vacuum limit using a Taylor expansion.
- [ ] Explain why quadratic drag couples \(x\) and \(y\).
- [ ] Derive the vertical quadratic-drag solution.
- [ ] Explain the role of \(\tanh\) and \(\ln\cosh\).
- [ ] Set up and numerically solve the 2D quadratic-drag equations.
- [ ] Compute \(\mathbf v\times\mathbf B\) correctly.
- [ ] Explain why a magnetic field does no work.
- [ ] Derive the cyclotron frequency and radius.
- [ ] Explain circular and helical motion.
- [ ] Use Euler's formula comfortably.
- [ ] Solve the magnetic equations using complex notation.
- [ ] Complete the Chapter 2 problem set.
