# Taylor, Chapter 2: Solutions, Corrections, and Review

> **Authorship note:** The original solutions were written by Jacob Maronge and “graded” by ChatGPT. ChatGPT transcribed and reorganized the handwritten work, suggested corrections, and summarized the main themes.

This document collects solutions to Problems 2.1, 2.6, 2.17, 2.35, 2.41, 2.43, 2.52, 2.53, and 2.54 from John R. Taylor's *Classical Mechanics*. The cleaned derivations preserve the reasoning in the original solutions while standardizing notation and clearly identifying any corrections.

Numerical companion: [Taylor 2.43 notebook](../taylor_problem_2_43.ipynb)

## Overall assessment

**Overall grade: A (about 95%)**

The work is assessed as homework for an upper-level classical-mechanics course. Mathematically and physically correct solutions receive full credit; deductions are limited to substantive mathematical errors, consequential ambiguity, omitted requested results, or reasoning that produces an incorrect conclusion.

Overall, the mechanics is strong. The solutions consistently translate physical descriptions into appropriate equations of motion, and nearly all final answers are correct. The few deductions arise mainly from intermediate sign errors, notation ambiguity, or matching conditions applied to the wrong solution branch.

| Problem | Assessment | Grade |
|---|---|---:|
| 2.1 | Correct comparison of linear and quadratic drag; interpretation is sound | 10/10 |
| 2.6 | Correct short-time limits; good recognition that cancellation determines the required Taylor order | 10/10 |
| 2.17 | Correct trajectory after eliminating time; one missing minus sign in the intermediate expression for $t(x)$ | 9/10 |
| 2.35 | Correct separation-of-variables derivation of the quadratic-drag result | 10/10 |
| 2.41 | Correct requested $v\,dv/dy$ solution and numerical height; unnecessary earlier branch calculation contains a matching error | 8.5/10 |
| 2.43 | Correct coupled equations for two-dimensional quadratic drag and correct decision to solve numerically | 10/10 |
| 2.52 | Correct circular-motion equations and real solution; complex-exponential sign needs care | 8.5/10 |
| 2.53 | Correct velocity and position components, apart from minor notation ambiguity in the $z$ initial velocity | 9.5/10 |
| 2.54 | Correct use of the general sine-cosine solution and initial conditions | 10/10 |

---

## Problem 2.1 — When quadratic drag dominates linear drag

Taylor gives the ratio in the form

$$
\frac{f_{\mathrm{quad}}}{f_{\mathrm{lin}}}
=\left(1.6\times10^3\ \frac{\mathrm{s}}{\mathrm{m}^2}\right)Dv.
$$

The two drag forces are equal when this ratio is one:

$$
v_*=\frac{1}{(1.6\times10^3)D}.
$$

### Baseball

For $D=7\times10^{-2}\,\mathrm{m}$,

$$
v_* = \frac{1}{(1.6\times10^3)(7\times10^{-2})}
\approx 8.9\times10^{-3}\,\mathrm{m/s}.
$$

At $v=1\,\mathrm{m/s}$,

$$
\frac{f_{\mathrm{quad}}}{f_{\mathrm{lin}}}\approx112,
$$

so the linear force is less than 1% of the quadratic force. At ordinary baseball speeds, neglecting linear drag is completely reasonable.

### Beach ball

For $D=7\times10^{-1}\,\mathrm{m}$,

$$
v_*\approx 8.9\times10^{-4}\,\mathrm{m/s}.
$$

Again, essentially any ordinary motion in air is well inside the quadratic-drag regime.

### Grade and comments

**10/10.** The calculations and physical conclusion are correct. The especially important point is not merely that the crossover speeds are small, but that the ratio grows linearly with speed. Once the quadratic term dominates, it becomes increasingly dominant as $v$ rises.

---

## Problem 2.6 — Short-time behavior under linear drag

Take downward as positive. For an object released from rest under linear drag,

$$
v(t)=v_{\mathrm{ter}}\left(1-e^{-t/\tau}\right),
\qquad
v_{\mathrm{ter}}=\frac{mg}{b},
\qquad
\tau=\frac{m}{b}.
$$

### (a) Velocity at short times

For $t\ll\tau$,

$$
e^{-t/\tau}=1-\frac{t}{\tau}+O\!\left(\frac{t^2}{\tau^2}\right).
$$

Therefore,

$$
v(t)\approx v_{\mathrm{ter}}\frac{t}{\tau}
=\frac{mg}{b}\frac{bt}{m}
=gt.
$$

This is exactly the vacuum result at leading order. Physically, drag initially vanishes because the object starts with $v=0$, so gravity controls the first instant of motion.

### (b) Position at short times

With $y(0)=0$,

$$
y(t)=v_{\mathrm{ter}}\left[t-\tau\left(1-e^{-t/\tau}\right)\right].
$$

Now the first two terms in the exponential expansion are not enough:

$$
1-e^{-t/\tau}\approx\frac{t}{\tau}
\quad\Longrightarrow\quad
t-\tau\frac{t}{\tau}=0.
$$

This zero is not a prediction that the object fails to move. It says the constant and linear contributions cancel exactly, so the leading nonzero behavior lies at the next order. Keeping the quadratic term,

$$
e^{-t/\tau}
=1-\frac{t}{\tau}+\frac{t^2}{2\tau^2}
+O\!\left(\frac{t^3}{\tau^3}\right),
$$

gives

$$
y(t)\approx v_{\mathrm{ter}}\frac{t^2}{2\tau}
=\frac12gt^2.
$$

### Why velocity needs fewer terms than position

Velocity begins as $v(0)=0$ but has nonzero first derivative $\dot v(0)=g$, so its leading term is linear in $t$. Position has $y(0)=0$ and $\dot y(0)=v(0)=0$, while $\ddot y(0)=g\neq0$, so its first nonzero term is quadratic. The initial conditions tell us in advance which Taylor coefficients must vanish.

### Grade and comments

**10/10.** The final derivation is correct, and your observation that two terms yield zero but three recover $gt^2/2$ is exactly the important conceptual feature. Trying the shorter expansion first and then retaining the next term after seeing the cancellation is valid problem-solving, not a reason for a deduction.

---

## Problem 2.17 — Eliminating time from linear-drag projectile motion

The parametric solution can be written

$$
x(t)=v_{x0}\tau\left(1-e^{-t/\tau}\right),
$$

$$
y(t)=(v_{y0}+v_{\mathrm{ter}})\tau
\left(1-e^{-t/\tau}\right)-v_{\mathrm{ter}}t,
$$

where upward is positive and $v_{\mathrm{ter}}=g\tau$ denotes the positive magnitude of terminal speed.

From the horizontal equation,

$$
e^{-t/\tau}=1-\frac{x}{v_{x0}\tau}.
$$

Taking logarithms gives

$$
\boxed{t=-\tau\ln\left(1-\frac{x}{v_{x0}\tau}\right)}.
$$

Substitution into $y(t)$ gives

$$
\boxed{
y(x)=\frac{v_{y0}+v_{\mathrm{ter}}}{v_{x0}}x
+v_{\mathrm{ter}}\tau
\ln\left(1-\frac{x}{v_{x0}\tau}\right)
}.
$$

### Correction

The handwritten intermediate line omitted the minus sign in the expression for $t$. Your final $y(x)$ nevertheless has the correct sign because $-v_{\mathrm{ter}}t$ was effectively handled correctly.

The logarithm also explains the finite horizontal asymptote:

$$
x_{\infty}=v_{x0}\tau.
$$

As $t\to\infty$, horizontal velocity decays exponentially to zero, so the projectile accumulates only a finite horizontal displacement.

### Grade and comments

**9/10.** Correct final trajectory, with one intermediate sign error.

---

## Problem 2.35 — Vertical fall with quadratic drag

Choose downward as positive. For an object released from rest,

$$
m\dot v=mg-cv^2.
$$

Define the terminal speed

$$
v_{\mathrm{ter}}=\sqrt{\frac{mg}{c}}.
$$

Then

$$
\dot v=g\left(1-\frac{v^2}{v_{\mathrm{ter}}^2}\right).
$$

Separate variables:

$$
\frac{dv}{1-(v/v_{\mathrm{ter}})^2}=g\,dt.
$$

Let $u=v/v_{\mathrm{ter}}$. Since $dv=v_{\mathrm{ter}}du$,

$$
v_{\mathrm{ter}}\int\frac{du}{1-u^2}=gt+C.
$$

Thus

$$
v_{\mathrm{ter}}\operatorname{artanh}\left(\frac{v}{v_{\mathrm{ter}}}\right)
=gt+C.
$$

Using $v(0)=0$ gives $C=0$, so

$$
\boxed{
v(t)=v_{\mathrm{ter}}
\tanh\left(\frac{gt}{v_{\mathrm{ter}}}\right)
}.
$$

Since $v_{\mathrm{ter}}=g\tau$, this is also

$$
v(t)=v_{\mathrm{ter}}\tanh(t/\tau).
$$

### Grade and comments

**10/10.** Correct setup, substitution, and final form. Defining the sign convention and $v_{\mathrm{ter}}$ earlier would make the derivation easier to read, but that is advice rather than a homework-grade deduction.

---

## Problem 2.41 — Baseball thrown upward with quadratic drag

Choose upward as positive. During the upward journey, $v>0$, so gravity and drag both point downward:

$$
m\dot v=-mg-cv^2.
$$

Using

$$
v_{\mathrm{ter}}^2=\frac{mg}{c},
$$

we obtain

$$
\dot v=-g\left(1+\frac{v^2}{v_{\mathrm{ter}}^2}\right).
$$

Taylor asks for the $v\,dv/dy$ rule. Since $v=v(y)$,

$$
\dot v=\frac{dv}{dy}\frac{dy}{dt}
=v\frac{dv}{dy}.
$$

Therefore,

$$
v\frac{dv}{dy}
=-g\left(1+\frac{v^2}{v_{\mathrm{ter}}^2}\right).
$$

Separate and integrate from $(y,v)=(0,v_0)$ to $(y,v)$:

$$
\int_{v_0}^{v}
\frac{v'\,dv'}{1+(v'/v_{\mathrm{ter}})^2}
=-g\int_0^y dy'.
$$

This gives

$$
\frac{v_{\mathrm{ter}}^2}{2}
\ln\left[
\frac{1+(v/v_{\mathrm{ter}})^2}
{1+(v_0/v_{\mathrm{ter}})^2}
\right]
=-gy.
$$

Hence

$$
\boxed{
y(v)=\frac{v_{\mathrm{ter}}^2}{2g}
\ln\left[
\frac{1+(v_0/v_{\mathrm{ter}})^2}
{1+(v/v_{\mathrm{ter}})^2}
\right]
}.
$$

Solving explicitly for speed gives

$$
\boxed{
v(y)=v_{\mathrm{ter}}
\sqrt{
\left(1+\frac{v_0^2}{v_{\mathrm{ter}}^2}\right)
e^{-2gy/v_{\mathrm{ter}}^2}-1
}
},
$$

with the positive square root because this formula describes the upward branch.

At maximum height, $v=0$:

$$
\boxed{
y_{\max}=\frac{v_{\mathrm{ter}}^2}{2g}
\ln\left(1+\frac{v_0^2}{v_{\mathrm{ter}}^2}\right)
}.
$$

For $m=0.15\,\mathrm{kg}$, $D=0.07\,\mathrm{m}$, $c=\gamma D^2$ with $\gamma=0.25\,\mathrm{N\,s^2/m^4}$, and $v_0=20\,\mathrm{m/s}$,

$$
c=0.001225\,\mathrm{kg/m},
\qquad
v_{\mathrm{ter}}\approx34.6\,\mathrm{m/s},
$$

and

$$
y_{\max}\approx17.6\,\mathrm{m}.
$$

In a vacuum,

$$
y_{\max}^{(0)}=\frac{v_0^2}{2g}\approx20.4\,\mathrm{m}.
$$

Quadratic drag therefore reduces the maximum height by about $2.8\,\mathrm{m}$, or roughly 14%.

### Correction to the abandoned $v(t)$ approach

The compact equation valid for both directions is

$$
m\dot v=-mg-cv|v|.
$$

It is legitimate to solve separate $v>0$ and $v<0$ branches, but they meet at the apex, where $v=0$ at a nonzero time $t=t_{\mathrm{up}}$. They should not be matched to each other at $t=0$. For this problem, solving directly for $v(y)$ avoids that unnecessary complication.

### Grade and comments

**8.5/10.** The solution Taylor requested is correct, including the numerical result. The deduction is for the earlier branch-matching error and for stopping at $y(v)$ before explicitly displaying $v(y)$.

---

## Problem 2.43 — Projectile motion with two-dimensional quadratic drag

Quadratic drag has magnitude $cv^2$ and points opposite the velocity. Therefore,

$$
\mathbf F_{\mathrm{drag}}
=-cv^2\hat{\mathbf v}
=-cv\mathbf v,
\qquad
v=\sqrt{v_x^2+v_y^2}.
$$

With $y$ positive upward,

$$
m\dot v_x=-cvv_x,
$$

$$
m\dot v_y=-mg-cvv_y.
$$

Equivalently, the first-order numerical system is

$$
\dot x=v_x,
\qquad
\dot y=v_y,
$$

$$
\dot v_x=-\frac{c}{m}\sqrt{v_x^2+v_y^2}\,v_x,
$$

$$
\dot v_y=-g-\frac{c}{m}\sqrt{v_x^2+v_y^2}\,v_y.
$$

The initial conditions for launch speed $v_0$ and angle $\theta$ are

$$
x(0)=0,
\quad y(0)=0,
\quad v_x(0)=v_0\cos\theta,
\quad v_y(0)=v_0\sin\theta.
$$

The components are coupled through the common speed $v$. That coupling is exactly why the ordinary two-dimensional quadratic-drag problem does not reduce to separate elementary formulas for $x(t)$ and $y(t)$; numerical integration is the appropriate next step.

### Grade and comments

**10/10.** The vector force, component equations, and conclusion that numerical work is needed are all correct. It is also good that you did not incorrectly write the horizontal drag as $-cv_x^2$: the magnitude depends on total speed, so the correct component is $-cvv_x$.

---

## Problem 2.52 — Charge moving in a uniform magnetic field

Let

$$
\mathbf B=(0,0,B),
\qquad
\omega=\frac{qB}{m}.
$$

The Lorentz-force equation is

$$
m\dot{\mathbf v}=q\mathbf v\times\mathbf B.
$$

Since

$$
\mathbf v\times\mathbf B=(v_yB,-v_xB,0),
$$

the component equations are

$$
\dot v_x=\omega v_y,
\qquad
\dot v_y=-\omega v_x,
\qquad
\dot v_z=0.
$$

Differentiating the first equation gives

$$
\ddot v_x=-\omega^2v_x.
$$

For $v_x(0)=v_0$ and $v_y(0)=0$,

$$
\boxed{v_x(t)=v_0\cos(\omega t)},
$$

$$
\boxed{v_y(t)=-v_0\sin(\omega t)}.
$$

The speed is constant:

$$
v_x^2+v_y^2=v_0^2.
$$

This is physically necessary because the magnetic force is perpendicular to $\mathbf v$, and therefore does no work.

### Complex form

Define

$$
u(t)=v_x(t)+iv_y(t).
$$

Then

$$
\dot u
=\omega v_y-i\omega v_x
=-i\omega u,
$$

so

$$
\boxed{u(t)=u(0)e^{-i\omega t}}.
$$

Because

$$
e^{-i\omega t}=\cos(\omega t)-i\sin(\omega t),
$$

this reproduces the two real components above.

### Correction

The handwritten real solution is correct. The complex-exponential discussion needs the negative exponent for the chosen definition $u=v_x+iv_y$ and for positive $qB$. Using $e^{+i\omega t}$ describes the opposite sense of rotation unless one instead defines $u=v_x-iv_y$.

### Grade and comments

**8.5/10.** Strong component derivation and physical interpretation; the deduction is for the sign inconsistency in the complex form.

---

## Problem 2.53 — Parallel electric and magnetic fields

Let

$$
\mathbf E=(0,0,E_z),
\qquad
\mathbf B=(0,0,B),
\qquad
\omega=\frac{qB}{m}.
$$

The equation of motion is

$$
m\dot{\mathbf v}=q(\mathbf E+\mathbf v\times\mathbf B).
$$

Thus

$$
\dot v_x=\omega v_y,
\qquad
\dot v_y=-\omega v_x,
\qquad
\dot v_z=\frac{qE_z}{m}.
$$

For $v_x(0)=v_{x0}$, $v_y(0)=0$, and $v_z(0)=v_{z0}$,

$$
v_x(t)=v_{x0}\cos(\omega t),
$$

$$
v_y(t)=-v_{x0}\sin(\omega t),
$$

$$
v_z(t)=v_{z0}+\frac{qE_z}{m}t.
$$

Taking the initial position to be the origin and integrating,

$$
\boxed{x(t)=\frac{v_{x0}}{\omega}\sin(\omega t)},
$$

$$
\boxed{y(t)=\frac{v_{x0}}{\omega}\left[\cos(\omega t)-1\right]},
$$

$$
\boxed{z(t)=v_{z0}t+\frac{qE_z}{2m}t^2}.
$$

The motion is circular in the transverse $xy$-plane while accelerating along the field direction. In three dimensions this produces a helix whose pitch changes with time because $v_z$ changes linearly.

### Grade and comments

**9.5/10.** Correct equations and integrations. The small deduction is only for writing an un-subscripted $v_0$ in the final $z(t)$ expression where $v_{z0}$ is intended, leaving the initial velocity component slightly ambiguous.

---

## Problem 2.54 — Choosing sine, cosine, or a complex exponential

Starting from

$$
\dot v_x=\omega v_y,
\qquad
\dot v_y=-\omega v_x,
$$

we obtain

$$
\ddot v_x+\omega^2v_x=0.
$$

The general real solution is

$$
v_x(t)=A\sin(\omega t)+B\cos(\omega t).
$$

Using $v_y=\dot v_x/\omega$,

$$
v_y(t)=A\cos(\omega t)-B\sin(\omega t).
$$

Now impose the initial conditions $v_x(0)=v_0$ and $v_y(0)=0$:

$$
B=v_0,
\qquad
A=0.
$$

Therefore,

$$
\boxed{v_x(t)=v_0\cos(\omega t)},
\qquad
\boxed{v_y(t)=-v_0\sin(\omega t)}.
$$

### How to decide among sine, cosine, and $e^{i\omega t}$

You do not choose among three physically different solutions. They are different coordinate systems for the same two-dimensional solution space:

$$
A\cos(\omega t)+B\sin(\omega t),
$$

$$
C\cos(\omega t-\phi),
$$

or

$$
\operatorname{Re}\!\left(De^{i\omega t}\right).
$$

The differential equation determines the solution space. The initial conditions select the coefficients—or, equivalently, the amplitude and phase. Cosine is convenient when the quantity begins at a maximum; sine is convenient when it begins at zero with a nonzero derivative; complex exponentials are convenient for algebra and for representing rotation.

### Grade and comments

**10/10.** Your final reasoning is correct. The important breakthrough in the handwritten work is the realization that neither sine nor cosine should be guessed in isolation: begin with the general linear combination and let the initial conditions decide.

---

## Main themes across these problems

### 1. A force law is a vector statement before it is a scalar equation

This is the thread connecting the drag and magnetic-field problems.

- Linear drag: $\mathbf F_d=-b\mathbf v$.
- Quadratic drag: $\mathbf F_d=-cv\mathbf v=-cv^2\hat{\mathbf v}$.
- Magnetic force: $\mathbf F_B=q\mathbf v\times\mathbf B$.

The signs in component equations should be derived from these vector laws. A fixed minus sign means “opposite the signed velocity” only for linear drag. In one-dimensional quadratic drag, the compact expression is $-cv|v|$, not $-cv^2$ for both directions.

### 2. Choose and state the positive direction before writing components

Both “up positive” and “down positive” work. Trouble begins only when a derivation changes conventions midway. A good opening line is:

> Take upward as positive, so gravity contributes $-mg$.

That single sentence determines almost every later sign.

### 3. Initial conditions select a member of a solution family

The equation

$$
\ddot x+\omega^2x=0
$$

does not say “the answer is sine” or “the answer is cosine.” It says

$$
x=A\cos(\omega t)+B\sin(\omega t).
$$

Initial conditions determine $A$ and $B$. The same principle applies to integration constants in drag problems and to the phase of a complex exponential.

### 4. Taylor expansions are controlled by the first nonzero term

The number of terms required is not fixed in advance. Expand until the first nonzero contribution survives after all substitutions and cancellations. For a position released from rest, the constant and linear terms vanish because $y(0)=0$ and $v(0)=0$; the quadratic term is therefore the leading physics.

### 5. Characteristic scales organize the equations

For linear drag,

$$
\tau=\frac{m}{b},
\qquad
v_{\mathrm{ter}}=g\tau.
$$

For quadratic drag,

$$
v_{\mathrm{ter}}=\sqrt{\frac{mg}{c}},
\qquad
\tau=\frac{v_{\mathrm{ter}}}{g}.
$$

Writing equations in terms of $t/\tau$ and $v/v_{\mathrm{ter}}$ exposes their structure. These ratios tell us whether drag has had time to matter and whether the speed is near the terminal scale.

### 6. Choose the independent variable that matches the question

If the question asks for speed as a function of height, solving for $v(t)$ and then $y(t)$ is often unnecessary. The chain rule

$$
\dot v=v\frac{dv}{dy}
$$

eliminates time directly. This is not a trick; it is an ordinary change in which variable parametrizes the motion.

### 7. Coupling determines whether components can be solved separately

Linear drag produces separate equations such as

$$
\dot v_x=-\frac{b}{m}v_x,
\qquad
\dot v_y=-g-\frac{b}{m}v_y.
$$

Quadratic drag instead contains

$$
v=\sqrt{v_x^2+v_y^2},
$$

so each component depends on both. This is why the two-dimensional quadratic-drag problem naturally leads to numerical integration.

### 8. Use limiting cases as built-in checks

Several quick checks catch most mistakes:

- At $t=0$, do the formulas reproduce the initial position and velocity?
- For $t\ll\tau$, does the motion approach the vacuum result?
- As $t\to\infty$, does the speed approach the appropriate terminal speed?
- If $c\to0$ or $b\to0$, does the drag solution approach the no-drag solution?
- In a purely magnetic field, is speed constant?
- Are the dimensions correct?

## Recommended habits for the next chapter

1. State the coordinate convention in words.
2. Write the force law in vector form before taking components.
3. Define characteristic scales before integrating.
4. Keep integration constants until the initial condition is applied.
5. For oscillatory equations, write the full sine-cosine family before choosing a phase.
6. Check the result at $t=0$, at a physically important limit, and dimensionally.

The broad conclusion is encouraging: your conceptual mechanics is already ahead of your algebraic presentation. The next improvement is not learning a new collection of formulas; it is making sign conventions, domains, and initial conditions explicit enough that the written derivation reliably expresses the physical reasoning you already have.
