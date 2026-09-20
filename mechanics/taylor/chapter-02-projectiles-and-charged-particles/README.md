# Chapter 2 — Projectiles and Charged Particles

**Text:** John R. Taylor, *Classical Mechanics*  
**Status:** Completed  
**Purpose:** Consolidated notes based on the chapter, my worked solutions, and follow-up discussions.

> These notes are meant to preserve the reasoning I should carry forward, not merely a list of formulas. The central habit is to begin with the vector force law and a declared coordinate convention, derive the differential equation, apply the initial conditions, and then check dimensions and limiting cases.

---

# 1. Chapter purpose

## One-sentence summary

Chapter 2 applies Newton's second law to velocity-dependent forces, using air resistance and the magnetic Lorentz force to develop intuition for exponential relaxation, terminal behavior, coupled differential equations, approximations, hyperbolic functions, numerical solutions, and complex representations of planar motion.

## How Chapter 2 extends Chapter 1

Chapter 1 established the general structure

```math
m\ddot{\mathbf r}=\mathbf F(\mathbf r,\dot{\mathbf r},t).
```

Chapter 2 focuses on important cases in which the force depends explicitly on velocity:

```math
\mathbf F_d=-b\mathbf v,
```

```math
\mathbf F_d=-cv\mathbf v,
```

```math
\mathbf F_B=q\mathbf v\times\mathbf B.
```

This makes the differential-equation viewpoint essential. The force determines how velocity changes, and the velocity must then be integrated to determine the trajectory.

## Core habits from this chapter

1. Declare the positive directions before assigning signs.
2. Write the force as a vector before taking components.
3. Distinguish a signed component from a nonnegative magnitude.
4. Use the initial conditions to select a particular solution.
5. Identify the natural dimensional scales of the problem.
6. Check short-time, long-time, zero-drag, and dimensional limits.
7. Recognize when an analytic solution is inconvenient or unavailable and use numerical integration.

---

# 2. Drag forces and sign conventions

## General drag law

For a nonrotating object moving through a stationary fluid, the drag force points opposite the object's velocity relative to the fluid:

```math
\mathbf F_d=-f(v)\hat{\mathbf v},
\qquad
v=|\mathbf v|.
```

The minus sign means “opposite the velocity vector.” It does not mean “always downward” or “always negative in a chosen coordinate system.”

An approximate drag magnitude is

```math
f(v)=bv+cv^2,
```

so

```math
\mathbf F_d=-(bv+cv^2)\hat{\mathbf v}.
```

## Linear versus quadratic drag

The two magnitudes are

```math
f_{\mathrm{lin}}=bv,
\qquad
f_{\mathrm{quad}}=cv^2.
```

Their ratio is

```math
\frac{f_{\mathrm{quad}}}{f_{\mathrm{lin}}}=\frac{cv}{b}.
```

Therefore:

- linear drag is relatively more important at low speeds;
- quadratic drag is relatively more important at high speeds;
- the crossover occurs when $v=b/c$.

The relevant velocity is the velocity relative to the medium. If the air itself moves with velocity $\mathbf u$, then the drag law depends on $\mathbf v-\mathbf u$.

## One-dimensional sign rules

With upward chosen as positive, gravity is always

```math
F_g=-mg.
```

Linear drag is

```math
F_d=-bv.
```

This automatically reverses direction:

- if $v>0$ while the object rises, then $F_d<0$ and drag points downward;
- if $v<0$ while the object falls, then $F_d>0$ and drag points upward;
- at the apex, $v=0$, so the instantaneous drag force is zero, but gravity remains $-mg$.

Quadratic drag must preserve the same directional information. In one dimension,

```math
\boxed{F_d=-cv|v|}.
```

Thus

```math
F_d=
\begin{cases}
-cv^2, & v>0,\\
+cv^2, & v<0.
\end{cases}
```

Writing only $-cv^2$ loses the reversal of direction because $v^2$ is always nonnegative.

## Main takeaway

The coordinate sign of drag should be derived from the velocity, not memorized separately for rising and falling motion.

---

# 3. Linear drag in one dimension

## Horizontal motion without gravity

Start from

```math
m\dot v=-bv.
```

Define the characteristic time

```math
\boxed{\tau=\frac{m}{b}}.
```

Then

```math
\dot v=-\frac{v}{\tau}.
```

Separating variables gives

```math
\frac{dv}{v}=-\frac{dt}{\tau},
```

and therefore

```math
\boxed{v(t)=v_0e^{-t/\tau}}.
```

For $x(0)=0$,

```math
x(t)=\int_0^t v_0e^{-t'/\tau}\,dt'
=v_0\tau\left(1-e^{-t/\tau}\right).
```

Hence

```math
\boxed{x_\infty=v_0\tau}.
```

This result makes physical sense: $v_0$ sets the initial distance traveled per unit time, while $\tau$ sets how long appreciable horizontal motion persists. Their product is the natural distance scale.

## The meaning of $\tau$

The characteristic time is the natural clock of the system:

- $t\ll\tau$: the velocity has changed little;
- $t\sim\tau$: drag has produced an order-one change;
- $t\gg\tau$: the initial transient is mostly gone.

At $t=\tau$,

```math
v(\tau)=\frac{v_0}{e}\approx0.368v_0.
```

The value $1/e$ is not a special physical threshold. It occurs because exponential decay is the solution of a system whose instantaneous rate of change is proportional to its current value. One time constant is defined as the time that makes the exponent equal to $-1$.

After each additional interval of length $\tau$, the remaining deviation is multiplied by another factor of $1/e$.

At $t=\tau$, the object has traveled

```math
x(\tau)=x_\infty\left(1-\frac1e\right)\approx0.632x_\infty.
```

## Vertical fall with linear drag

Choose downward as positive. Newton's law is

```math
m\dot v=mg-bv.
```

Terminal speed is found by setting the acceleration equal to zero:

```math
0=mg-bv_{\mathrm{ter}},
```

so

```math
\boxed{v_{\mathrm{ter}}=\frac{mg}{b}=g\tau}.
```

Terminal velocity is a dynamical equilibrium: gravity and drag balance, so acceleration vanishes. It is not necessarily the largest speed an object can ever have. An object can begin faster than its terminal speed and then decelerate toward it.

The general solution is

```math
\boxed{
v(t)=v_{\mathrm{ter}}+left(v_0-v_{\mathrm{ter}}\right)e^{-t/\tau}
}.
```

This is best interpreted as

```math
v(t)-v_{\mathrm{ter}}
=\left(v_0-v_{\mathrm{ter}}\right)e^{-t/\tau}.
```

The velocity does not merely decay toward zero; its deviation from equilibrium decays toward zero.

For release from rest,

```math
v(t)=v_{\mathrm{ter}}\left(1-e^{-t/\tau}\right).
```

Integrating with $y(0)=0$ gives

```math
\boxed{
y(t)=v_{\mathrm{ter}}
\left[t-\tau\left(1-e^{-t/\tau}\right)\right]
}.
```

## Short-time limit and Taylor expansion

The dimensionless expansion parameter is $t/\tau$:

```math
e^{-t/\tau}
=1-\frac{t}{\tau}
+\frac12\left(\frac{t}{\tau}\right)^2
-\frac16\left(\frac{t}{\tau}\right)^3+\cdots.
```

For velocity, the first nonzero term gives

```math
v(t)approx v_{\mathrm{ter}}\frac{t}{\tau}=gt.
```

For position, the constant and linear contributions cancel:

```math
t-\tau\left(1-e^{-t/\tau}\right)
\approx t-\tau\left(\frac{t}{\tau}
-\frac{t^2}{2\tau^2}\right)
=\frac{t^2}{2\tau}.
```

Therefore

```math
y(t)\approx\frac12gt^2.
```

### How many Taylor terms are enough?

Keep terms until the first nonzero physical contribution survives all substitutions and cancellations. The necessary order depends on the initial conditions:

```math
y(t)=y_0+v_0t+\frac12a_0t^2+\cdots.
```

If $y_0=0$ and $v_0=0$, the constant and linear terms vanish, so the quadratic term is the leading behavior. Obtaining zero from a lower-order approximation does not mean the object does not move; it means the approximation has not yet reached the first nonzero term.

---

# 4. Projectile motion with linear drag

Choose $x$ horizontal and $y$ vertically upward. Then

```math
m\dot v_x=-bv_x,
```

```math
m\dot v_y=-mg-bv_y.
```

The equations are uncoupled because each drag component depends only on the corresponding velocity component. Gravity appears only in the vertical equation.

For

```math
v_{x0}=v_0\cos\theta,
\qquad
v_{y0}=v_0\sin\theta,
```

the velocities are

```math
\boxed{v_x(t)=v_{x0}e^{-t/\tau}},
```

```math
\boxed{
v_y(t)=\left(v_{y0}+g\tau\right)e^{-t/\tau}-g\tau
}.
```

The vertical terminal velocity is $-g\tau$ because upward is positive.

Taking $x(0)=y(0)=0$,

```math
\boxed{
x(t)=v_{x0}\tau\left(1-e^{-t/\tau}\right)
},
```

```math
\boxed{
y(t)=\left(v_{y0}+g\tau\right)\tau
\left(1-e^{-t/\tau}\right)-g\tau t
}.
```

## Eliminating time

From the horizontal position,

```math
e^{-t/\tau}=1-\frac{x}{v_{x0}\tau}.
```

Therefore

```math
\boxed{
t=-\tau\ln\left(1-\frac{x}{v_{x0}\tau}\right)
}.
```

Substituting into $y(t)$ gives

```math
\boxed{
y(x)=
\frac{v_{y0}+g\tau}{v_{x0}}x
+g\tau^2
\ln\left(1-\frac{x}{v_{x0}\tau}\right)
}.
```

The logarithm arises from inverting exponential decay.

## Finite horizontal distance

As $t\to\infty$,

```math
x(t)\to v_{x0}\tau.
```

This is not primarily because the projectile eventually hits the ground. It follows mathematically from the integrability of the exponentially decaying horizontal velocity:

```math
\int_0^\infty v_{x0}e^{-t/\tau}\,dt=v_{x0}\tau.
```

In the idealized model continued indefinitely, the object approaches this horizontal coordinate asymptotically.

## Vacuum limit

For weak drag or short times, expand in the small dimensionless ratio $t/\tau$. The component solutions reduce to

```math
x(t)\approx v_{x0}t,
```

```math
y(t)\approx v_{y0}t-\frac12gt^2,
```

which leads to the familiar vacuum trajectory

```math
y(x)=x\tan\theta
-\frac{gx^2}{2v_0^2\cos^2\theta}.
```

The vacuum limit is a crucial check: as $b\to0$, $	au=m/b\to\infty$, so the drag solution must approach ordinary projectile motion.

## Range

The range $R$ satisfies $y(R)=0$. Because $y(x)$ contains

```math
\ln\left(1-\frac{x}{v_{x0}\tau}\right),
```

the equation for $R$ is transcendental: the unknown occurs both algebraically and inside a logarithm. It generally requires approximation or numerical solution.

---

# 5. Quadratic drag

## Vector form

Quadratic drag has magnitude $cv^2$ and points opposite the velocity:

```math
\mathbf F_d=-cv^2\hat{\mathbf v}.
```

Since $\mathbf v=v\hat{\mathbf v}$,

```math
\boxed{\mathbf F_d=-cv\mathbf v}.
```

## Why the two-dimensional equations are coupled

With $y$ upward,

```math
m\dot v_x=-cvv_x,
```

```math
m\dot v_y=-mg-cvv_y,
```

where

```math
v=\sqrt{v_x^2+v_y^2}.
```

Although the force components look separate, the common speed $v$ depends on both $v_x$ and $v_y$. Each differential equation therefore depends on both components. Unlike linear drag, the system is nonlinear and coupled.

## Vertical fall

Choose downward as positive. Then

```math
m\dot v=mg-cv^2.
```

At terminal speed,

```math
mg=cv_{\mathrm{ter}}^2,
```

so

```math
\boxed{v_{\mathrm{ter}}=\sqrt{\frac{mg}{c}}}.
```

The equation becomes

```math
\dot v=g\left(1-\frac{v^2}{v_{\mathrm{ter}}^2}\right).
```

Separate variables:

```math
\frac{dv}{1-v^2/v_{\mathrm{ter}}^2}=g\,dt.
```

For release from rest,

```math
\boxed{
v(t)=v_{\mathrm{ter}}
\tanh\left(\frac{gt}{v_{\mathrm{ter}}}\right)
}.
```

Define the quadratic-drag time scale

```math
\tau_q=\frac{v_{\mathrm{ter}}}{g}
=\sqrt{\frac{m}{gc}}.
```

Then

```math
v(t)=v_{\mathrm{ter}}\tanh(t/\tau_q).
```

The function $\tanh$ is natural because it begins linearly,

```math
\tanh z\approx z \quad (z\ll1),
```

and saturates at one,

```math
\tanh z\to1 \quad (z\to\infty).
```

It therefore captures both initial free fall and eventual terminal motion.

## Position for vertical fall

Integrating the velocity,

```math
y(t)=v_{\mathrm{ter}}
\int_0^t\tanh\left(\frac{gt'}{v_{\mathrm{ter}}}\right)dt'.
```

Since

```math
\frac{d}{dz}\ln\cosh z=\tanh z,
```

we obtain

```math
\boxed{
y(t)=\frac{v_{\mathrm{ter}}^2}{g}
\ln\cosh\left(\frac{gt}{v_{\mathrm{ter}}}\right)
}.
```

At short times, $y\approx gt^2/2$. At long times, $\ln\cosh z\approx z-\ln2$, so position becomes approximately linear with slope $v_{\mathrm{ter}}$.

## Upward and downward motion

With upward positive, the compact equation valid through a reversal is

```math
\boxed{m\dot v=-mg-cv|v|}.
```

Equivalently,

```math
m\dot v=
\begin{cases}
-mg-cv^2, & v>0 \quad \text{(rising)},\\
-mg+cv^2, & v<0 \quad \text{(falling)}.
\end{cases}
```

If the branches are solved separately, they meet at the apex, where $v=0$ at $t=t_{\mathrm{up}}$. They do not meet at $t=0$ unless the object is released from rest at the apex.

## Changing the independent variable: the $v\,dv/dy$ rule

If velocity is regarded as a function of position, $v=v(y)$, then the chain rule gives

```math
\boxed{
\dot v=\frac{dv}{dt}
=\frac{dv}{dy}\frac{dy}{dt}
=v\frac{dv}{dy}
}.
```

This is useful when the question asks for speed as a function of height or for a maximum height. It eliminates time directly.

For a baseball thrown vertically upward,

```math
m\dot v=-mg-cv^2
```

on the upward branch. Using $v_{\mathrm{ter}}^2=mg/c$,

```math
v\frac{dv}{dy}
=-g\left(1+\frac{v^2}{v_{\mathrm{ter}}^2}\right).
```

Integrating from $(0,v_0)$ to $(y,v)$ gives

```math
\boxed{
y(v)=\frac{v_{\mathrm{ter}}^2}{2g}
\ln\left[
\frac{1+(v_0/v_{\mathrm{ter}})^2}
{1+(v/v_{\mathrm{ter}})^2}
\right]
}.
```

At the maximum height, $v=0$:

```math
\boxed{
y_{\max}=\frac{v_{\mathrm{ter}}^2}{2g}
\ln\left(1+\frac{v_0^2}{v_{\mathrm{ter}}^2}\right)
}.
```

## Numerical two-dimensional motion

For general two-dimensional quadratic drag, use the first-order state

```math
\mathbf s=(x,y,v_x,v_y).
```

The system is

```math
\dot x=v_x,
\qquad
\dot y=v_y,
```

```math
\dot v_x=-\frac{c}{m}
\sqrt{v_x^2+v_y^2}\,v_x,
```

```math
\dot v_y=-g-\frac{c}{m}
\sqrt{v_x^2+v_y^2}\,v_y.
```

This is the system used in Problem 2.43. A numerical solver advances all four state variables together because the acceleration at each instant depends on both velocity components.

## Linear versus quadratic drag

| Feature | Linear drag | Quadratic drag |
|---|---|---|
| Force | $-b\mathbf v$ | $-cv\mathbf v$ |
| Magnitude | $bv$ | $cv^2$ |
| Terminal speed | $mg/b$ | $\sqrt{mg/c}$ |
| 2D Cartesian equations | Uncoupled | Coupled through $v$ |
| Typical functions in 1D | Exponentials | $\tanh$ and $\ln\cosh$ |
| Relative importance | Lower speeds | Higher speeds |

---

# 6. Motion of a charged particle in uniform fields

## Lorentz force

The electromagnetic force is

```math
\boxed{
\mathbf F=q\left(\mathbf E+\mathbf v\times\mathbf B\right)
}.
```

For a pure magnetic field,

```math
m\dot{\mathbf v}=q\mathbf v\times\mathbf B.
```

## Why a magnetic field does no work

The cross product is perpendicular to $\mathbf v$, so

```math
\mathbf F_B\cdot\mathbf v=0.
```

Because power is $\mathbf F\cdot\mathbf v$,

```math
\frac{d}{dt}\left(\frac12mv^2\right)=0.
```

A magnetic field changes the direction of velocity but not its magnitude. Acceleration can therefore be nonzero even while speed remains constant.

## Component equations for $\mathbf B=B\hat{\mathbf z}$

Let

```math
\mathbf v=(v_x,v_y,v_z),
\qquad
\mathbf B=(0,0,B).
```

Then

```math
\mathbf v\times\mathbf B=(v_yB,-v_xB,0).
```

Define the signed angular frequency

```math
\Omega=\frac{qB}{m}.
```

The equations are

```math
\boxed{
\dot v_x=\Omega v_y,
\qquad
\dot v_y=-\Omega v_x,
\qquad
\dot v_z=0
}.
```

The parallel velocity $v_z$ is constant. The transverse velocity rotates in the $xy$-plane.

The cyclotron-frequency magnitude is

```math
\boxed{\omega_c=\frac{|q|B}{m}}.
```

Changing the sign of $q$ changes the sign of $\Omega$, reversing the direction of rotation, but it does not change $|\Omega|$.

## Real solution

Differentiate the first planar equation:

```math
\ddot v_x=\Omega\dot v_y=-\Omega^2v_x.
```

Thus

```math
\ddot v_x+\Omega^2v_x=0.
```

The general real solution is

```math
v_x(t)=A\cos(\Omega t)+B\sin(\Omega t).
```

The differential equation does not choose sine or cosine. Both are independent solutions, and the initial conditions select their linear combination.

For $v_x(0)=v_0$ and $v_y(0)=0$,

```math
\boxed{v_x(t)=v_0\cos(\Omega t)},
```

```math
\boxed{v_y(t)=-v_0\sin(\Omega t)}.
```

Indeed,

```math
v_x^2+v_y^2=v_0^2.
```

## Radius and circular motion

For perpendicular motion, the magnetic force supplies centripetal acceleration:

```math
|q|v_\perp B=\frac{mv_\perp^2}{R}.
```

Therefore

```math
\boxed{R=\frac{mv_\perp}{|q|B}}.
```

Consequently, $R$ increases with $m$ and $v_\perp$, and decreases with $|q|$ and $B$.

If $v_z\neq0$, the particle simultaneously moves uniformly along the field and circles around the field direction. The result is a helix with pitch

```math
p=v_z\frac{2\pi}{\omega_c}.
```

## Parallel electric and magnetic fields

If both fields point along $z$, the magnetic field still produces circular transverse motion, while the electric field accelerates the particle along $z$:

```math
\dot v_z=\frac{qE_z}{m}.
```

Thus

```math
v_z(t)=v_{z0}+\frac{qE_z}{m}t,
```

```math
z(t)=z_0+v_{z0}t+\frac{qE_z}{2m}t^2.
```

The trajectory is a helix whose pitch changes with time.

---

# 7. Complex exponentials and planar rotation

## Euler's formula

```math
\boxed{e^{i\theta}=\cos\theta+i\sin\theta}.
```

Multiplying a complex number by $e^{i\alpha}$ rotates it counterclockwise through angle $\alpha$ without changing its magnitude.

For

```math
z=re^{i\theta},
```

$r$ is the magnitude and $\theta$ is the angle in the complex plane.

## Why complex exponentials help

Differentiation preserves the exponential form:

```math
\frac{d}{dt}e^{i\omega t}=i\omega e^{i\omega t}.
```

The factor $i$ represents a $90^\circ$ rotation. This makes complex numbers a natural language for planar rotational dynamics.

## Complex magnetic-field solution

Define the complex velocity

```math
u(t)=v_x(t)+iv_y(t).
```

Using

```math
\dot v_x=\Omega v_y,
\qquad
\dot v_y=-\Omega v_x,
```

we find

```math
\dot u
=\dot v_x+i\dot v_y
=\Omega v_y-i\Omega v_x
=-i\Omega u.
```

Therefore

```math
\boxed{u(t)=u(0)e^{-i\Omega t}}.
```

For $u(0)=v_0$,

```math
u(t)=v_0\left[\cos(\Omega t)-i\sin(\Omega t)\right],
```

so

```math
v_x(t)=v_0\cos(\Omega t),
\qquad
v_y(t)=-v_0\sin(\Omega t).
```

The sign in the exponent matters. With the definition $u=v_x+iv_y$, these equations give $e^{-i\Omega t}$. Defining $u=v_x-iv_y$ would reverse the sign in the complex equation.

## Sine, cosine, and complex exponentials

The following are equivalent ways of expressing the same two-dimensional real solution space:

```math
A\cos(\omega t)+B\sin(\omega t),
```

```math
C\cos(\omega t-\phi),
```

```math
\operatorname{Re}\left(De^{i\omega t}\right).
```

Use the full $A\cos+B\sin$ form when applying arbitrary initial conditions. Use amplitude and phase when the geometry is clearer that way. Use complex exponentials when differentiation, coupling, or rotation becomes simpler.

---

# 8. Mathematical tools developed in this chapter

## Separation of variables

For

```math
\dot y=f(y),
```

write

```math
\frac{dy}{f(y)}=dt.
```

When the initial condition is known, definite integrals often avoid a separate integration constant:

```math
\int_{y_0}^{y(t)}\frac{dy'}{f(y')}
=\int_0^t dt'.
```

## First-order linear equations

An equation of the form

```math
\dot y+ay=b
```

has an equilibrium solution $y_{\mathrm{eq}}=b/a$, and the deviation from equilibrium decays exponentially:

```math
y(t)-y_{\mathrm{eq}}
=\left[y(0)-y_{\mathrm{eq}}\right]e^{-at}.
```

This is the general mathematical structure behind linear terminal velocity.

## Taylor expansions

Important expansions include

```math
e^x=1+x+\frac{x^2}{2!}+\frac{x^3}{3!}+\cdots,
```

```math
\sin x=x-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots,
```

```math
\cos x=1-\frac{x^2}{2!}+\frac{x^4}{4!}-\cdots,
```

```math
\ln(1+x)=x-\frac{x^2}{2}+\frac{x^3}{3}-\cdots.
```

The expansion parameter must be dimensionless. Statements such as “$t$ is small” are incomplete; the meaningful statement is $t/\tau\ll1$.

## Hyperbolic functions

```math
\sinh x=\frac{e^x-e^{-x}}2,
\qquad
\cosh x=\frac{e^x+e^{-x}}2,
```

```math
\tanh x=\frac{\sinh x}{\cosh x}.
```

Useful identities are

```math
\frac{d}{dx}\tanh x=\operatorname{sech}^2x,
```

```math
1-\tanh^2x=\operatorname{sech}^2x,
```

```math
\frac{d}{dx}\ln\cosh x=\tanh x.
```

## Linear coupled equations versus nonlinear coupled equations

The magnetic equations are coupled but linear with constant coefficients:

```math
\frac{d}{dt}
\begin{pmatrix}v_x\\v_y\end{pmatrix}
=
\begin{pmatrix}0&\Omega\\-\Omega&0\end{pmatrix}
\begin{pmatrix}v_x\\v_y\end{pmatrix}.
```

Their matrix generates rotations, so they can be solved exactly using trigonometric functions, eigenvalues, matrix exponentials, or complex numbers.

Two-dimensional quadratic drag is also coupled, but it is nonlinear because the coefficient

```math
\sqrt{v_x^2+v_y^2}
```

depends on the unknown solution. That nonlinear structure is why general analytic solutions are unavailable and numerical integration is natural.

---

# 9. Checks that catch mistakes

## Initial conditions

Evaluate every solution at $t=0$. It must reproduce the specified initial position and velocity.

## Dimensions

- $\tau=m/b$ must have units of time.
- $v_{\mathrm{ter}}=mg/b$ and $\sqrt{mg/c}$ must have units of speed.
- An exponential argument such as $t/\tau$ must be dimensionless.
- A logarithm must act on a dimensionless quantity.

## Physical limits

- $t\ll\tau$: drag should be initially negligible when the object begins from rest.
- $t\to\infty$: velocity should approach the correct terminal value.
- $b\to0$ or $c\to0$: recover vacuum motion where the limit is applicable.
- Pure magnetic field: speed and kinetic energy must remain constant.

## Sign diagnostics

- Exponential drag solutions should contain $e^{-t/\tau}$, not $e^{+t/\tau}$.
- Gravity has a fixed coordinate sign once the axis is chosen.
- Drag reverses when velocity reverses.
- For complex rotation, verify the exponent sign by differentiating the proposed solution and checking the original component equations.

---

# 10. Mistake and confusion log

| Issue | Resolution |
|---|---|
| Why is drag “always negative” if it changes direction? | The vector law is opposite velocity. In 1D, $-bv$ or $-cv|v|$ changes sign automatically when $v$ changes sign. |
| Is drag present at the top of an upward flight? | At the instant $v=0$, drag is zero. Gravity remains nonzero, so the object accelerates downward. |
| Why is $1/e$ the characteristic-time scale? | Exponential relaxation has the form $e^{-t/\tau}$; setting $t=\tau$ makes the exponent $-1$. It is a natural convention, not a physical threshold. |
| Why is $x_\infty=v_{x0}\tau$? | It is the integral of the exponentially decaying horizontal velocity over all time. |
| Why did a two-term Taylor approximation give zero position? | The initial conditions force the constant and linear position terms to vanish. The quadratic term is the first nonzero contribution. |
| How do I know how many Taylor terms to retain? | Continue until the first nonzero term survives the substitutions and cancellations, then check that the next neglected term is small. |
| Why use $v\,dv/dy$? | It is the chain rule with $v=v(y)$ and removes time when the desired result is velocity versus position. |
| Why must upward and downward quadratic-drag solutions be separated? | The scalar form of the force changes because drag reverses direction. The branches meet at the apex, not generally at $t=0$. |
| Why are quadratic-drag components coupled? | Both contain the total speed $v=\sqrt{v_x^2+v_y^2}$. |
| How do I choose sine or cosine? | Start with $A\cos+B\sin$ and let the initial conditions determine $A$ and $B$. |
| What does the complex magnetic solution represent? | Its real and imaginary parts are the two real velocity components. The complex phase compactly represents planar rotation. |
| How can acceleration be nonzero while speed is constant? | Acceleration can change the direction of velocity without changing its magnitude, as in magnetic circular motion. |

---

# 11. Essential derivations to reproduce

## 1. Linear relaxation

From

```math
m\dot v=-bv
```

derive

```math
v=v_0e^{-t/\tau},
\qquad
\tau=m/b,
```

and

```math
x=v_0\tau(1-e^{-t/\tau}).
```

## 2. Linear terminal velocity

From

```math
m\dot v=mg-bv
```

derive

```math
v_{\mathrm{ter}}=mg/b
```

and

```math
v-v_{\mathrm{ter}}
=(v_0-v_{\mathrm{ter}})e^{-t/\tau}.
```

## 3. Linear-drag projectile

Derive $v_x(t)$, $v_y(t)$, $x(t)$, and $y(t)$; eliminate time; explain $x_\infty=v_{x0}\tau$; recover the vacuum limit.

## 4. Vertical quadratic drag

From

```math
m\dot v=mg-cv^2
```

derive

```math
v_{\mathrm{ter}}=\sqrt{mg/c},
```

```math
v(t)=v_{\mathrm{ter}}\tanh(gt/v_{\mathrm{ter}}),
```

and

```math
y(t)=\frac{v_{\mathrm{ter}}^2}{g}
\ln\cosh(gt/v_{\mathrm{ter}}).
```

## 5. Magnetic circular motion

From

```math
m\dot{\mathbf v}=q\mathbf v\times\mathbf B
```

derive the component equations, constant speed, cyclotron frequency, and radius.

## 6. Complex magnetic solution

Define $u=v_x+iv_y$, derive

```math
\dot u=-i\Omega u,
```

solve

```math
u=u_0e^{-i\Omega t},
```

and recover the real velocity components.

---

# 12. Final chapter summary

## Five central ideas

1. Velocity-dependent forces require careful distinction between vector direction, scalar magnitude, and signed components.
2. Linear drag produces exponential relaxation governed by the natural time scale $\tau=m/b$.
3. Quadratic drag reverses through $-cv|v|$ in 1D and couples components through total speed in multiple dimensions.
4. Approximations are organized by small dimensionless parameters, and initial conditions determine the first nonzero Taylor term.
5. A magnetic field rotates velocity without changing speed; sine, cosine, and complex exponentials are equivalent descriptions of that rotation.

## Three equations to know

```math
\tau=\frac{m}{b},
\qquad
v-v_{\mathrm{eq}}=(v_0-v_{\mathrm{eq}})e^{-t/\tau},
```

```math
\mathbf F_d=-cv\mathbf v,
```

```math
\mathbf F=q(\mathbf E+\mathbf v\times\mathbf B).
```

These are more useful as structural templates than as isolated formulas.

## Three derivations to reproduce without notes

1. Linear drag with terminal velocity and its short-time limit.
2. Vertical quadratic drag leading to $\tanh$ and $\ln\cosh$.
3. Magnetic circular motion using either real components or complex velocity.

## Most important conceptual lesson

The form of the differential equation encodes the physics: exponential relaxation signals change proportional to deviation from equilibrium, $\tanh$ signals saturation toward a finite terminal speed, and imaginary exponential factors signal rotation rather than growth or decay.

## Most important technical lesson

State the coordinate convention and initial conditions explicitly. Most errors in this chapter came from a sign or constant being detached from its physical meaning, not from misunderstanding the underlying mechanics.

## Problem worth repeating later

Repeat Problem 2.41 because it combines force signs, quadratic drag, terminal-speed scaling, the chain rule $\dot v=v\,dv/dy$, separation of variables, and a physical comparison with vacuum motion.

---

# 13. Readiness for Chapter 3

I am ready to move on because I can now:

- [x] explain why drag reverses with velocity;
- [x] distinguish linear and quadratic drag;
- [x] derive linear-drag exponential relaxation;
- [x] interpret $\tau=m/b$ as the natural clock;
- [x] explain $x_\infty=v_{x0}\tau$;
- [x] derive and interpret terminal velocity;
- [x] recover vacuum motion using a Taylor expansion;
- [x] determine how many Taylor terms are required from the first nonzero contribution;
- [x] derive the linear-drag projectile equations and eliminate time;
- [x] derive the vertical quadratic-drag velocity and position;
- [x] use $\dot v=v\,dv/dy$;
- [x] set up two-dimensional quadratic drag for numerical solution;
- [x] compute $\mathbf v\times\mathbf B$ and derive the component equations;
- [x] explain why magnetic fields change direction but not speed;
- [x] derive circular and helical motion;
- [x] use the general sine-cosine solution with initial conditions;
- [x] combine two rotational ODEs into one complex equation;
- [x] interpret the real and imaginary parts as physical components;
- [x] complete and review the Chapter 2 problem set.

Chapter 2 does not need to be flawless before moving forward. The remaining improvement is procedural: maintain explicit sign conventions, label velocity components consistently, and check proposed solutions against the original differential equations.
