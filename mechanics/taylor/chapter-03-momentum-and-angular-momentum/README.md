# Taylor, Chapter 3 — Momentum and Angular Momentum

**Text:** John R. Taylor, *Classical Mechanics*  
**Chapter:** 3 — Momentum and Angular Momentum  
**Dates studied:**  
**Status:** Not started

---

## How to use this file

This is the notes and derivations sheet for Chapter 3. It is meant to help reconstruct the chapter, not merely collect formulas. Fill in the blank reflections in your own words and reproduce the essential derivations without looking at the book.

The separate exercise sheet is `Taylor_Chapter_3_Problems.md`.

---

# 1. Chapter purpose

## One-sentence summary

> Newton's laws for individual particles can be reorganized into laws for whole systems: external force controls total momentum and center-of-mass motion, while external torque controls total angular momentum.

## Why this chapter matters

In Chapters 1 and 2, the basic strategy was to identify every force and solve the resulting differential equation. Chapter 3 introduces a complementary strategy: choose a system and track quantities whose changes depend only on external influences. Internal forces may be complicated, but they often cancel from the evolution of total momentum or angular momentum.

This is not a loss of information so much as a deliberate change of question. Momentum methods often determine recoil, center-of-mass motion, or the consequences of an impulse without describing every internal force. Angular momentum does the analogous job for rotational motion.

## What should feel familiar?

- Newton's second and third laws;
- vector addition and cross products;
- choosing coordinates and signs;
- impulse and collisions from introductory physics;
- polar coordinates and angular velocity;
- solving separable differential equations.

## What is likely to be genuinely new or subtle?

- choosing the system boundary before invoking conservation;
- distinguishing internal and external forces;
- variable-mass systems and momentum flux;
- treating center-of-mass motion separately from internal motion;
- the dependence of angular momentum and torque on the chosen origin;
- why central internal forces are needed for the usual angular-momentum theorem;
- using conservation laws without assuming energy is conserved.

---

# 2. Learning objectives

By the end of the chapter, I should be able to:

- [ ] Define the system before deciding whether momentum is conserved.
- [ ] Derive $\dot{\mathbf P}=\mathbf F_{\mathrm{ext}}$ for many particles.
- [ ] Explain precisely why internal forces cancel from total momentum.
- [ ] Use impulse to relate a short force to a momentum change.
- [ ] Derive the rocket equation from momentum balance.
- [ ] Explain why writing $\mathbf F=d(m\mathbf v)/dt$ for the rocket alone is dangerous.
- [ ] Calculate and interpret the center of mass of discrete and continuous systems.
- [ ] Derive $M\ddot{\mathbf R}=\mathbf F_{\mathrm{ext}}$.
- [ ] Explain why an explosion does not alter the center-of-mass trajectory.
- [ ] Define angular momentum and torque about a stated origin.
- [ ] Derive $\dot{\mathbf L}=\boldsymbol\tau$ for one particle.
- [ ] Explain why a central force implies planar motion.
- [ ] Connect angular-momentum conservation to Kepler's second law.
- [ ] Derive the many-particle angular-momentum theorem and state its assumptions.
- [ ] Separate translation of the center of mass from rotation about the center of mass.
- [ ] Check conservation claims against external force, external torque, and system choice.

---

# 3. The organizing idea: choose a system

Before writing a conservation law, answer:

1. What objects are inside the system?
2. What interactions cross the system boundary?
3. Which forces are internal and which are external?
4. About what origin is angular momentum being calculated?
5. During what time interval is the approximation valid?

A quantity is not conserved merely because a collision, explosion, or rotation occurs. It is conserved when the corresponding external influence vanishes:

$$
\mathbf F_{\mathrm{ext}}=\mathbf 0
\quad\Longrightarrow\quad
\mathbf P=\text{constant},
$$

$$
\boldsymbol\tau_{\mathrm{ext}}=\mathbf 0
\quad\Longrightarrow\quad
\mathbf L=\text{constant}.
$$

These are vector statements. Conservation must hold component by component.

### My system-boundary checklist

> 

---

# 4. Section 3.1 — Conservation of Momentum

## Total momentum

For $N$ particles,

$$
\mathbf P=\sum_{\alpha=1}^N \mathbf p_\alpha
=\sum_{\alpha=1}^N m_\alpha\mathbf v_\alpha.
$$

For particle $\alpha$,

$$
\dot{\mathbf p}_\alpha
=\mathbf F_\alpha^{\mathrm{ext}}
+\sum_{\beta\ne\alpha}\mathbf F_{\alpha\beta},
$$

where $\mathbf F_{\alpha\beta}$ is the force on particle $\alpha$ due to particle $\beta$.

Summing over all particles gives

$$
\dot{\mathbf P}
=\sum_\alpha \mathbf F_\alpha^{\mathrm{ext}}
+\sum_\alpha\sum_{\beta\ne\alpha}\mathbf F_{\alpha\beta}.
$$

Newton's third law pairs the internal forces:

$$
\mathbf F_{\alpha\beta}=-\mathbf F_{\beta\alpha}.
$$

Therefore, the internal-force sum vanishes and

$$
\boxed{\dot{\mathbf P}=\mathbf F_{\mathrm{ext}}}.
$$

If $\mathbf F_{\mathrm{ext}}=\mathbf 0$, then

$$
\boxed{\mathbf P=\text{constant}}.
$$

## What cancellation does and does not mean

Internal forces do not disappear physically. They can change each particle's momentum and can convert energy among internal forms. They cancel only when the particle equations are added to obtain the change in total momentum.

### Explain in my own words

> 

## Impulse

Integrating the momentum equation over a time interval gives

$$
\Delta\mathbf P
=\int_{t_i}^{t_f}\mathbf F_{\mathrm{ext}}(t)\,dt
\equiv\mathbf J_{\mathrm{ext}}.
$$

For a short, strong interaction, gravity or other weak forces may deliver negligible impulse during the event even though they are not literally zero.

## Momentum versus energy

Momentum conservation does not imply kinetic-energy conservation. For an isolated system:

- total momentum is conserved;
- total energy is conserved if all relevant forms are included;
- kinetic energy alone may change.

An elastic collision is the special case in which total kinetic energy is also conserved.

## Checks for collision or explosion problems

- [ ] Write one vector momentum equation before components.
- [ ] Use velocities in a single inertial frame.
- [ ] Do not conserve kinetic energy unless justified.
- [ ] Check every momentum component.
- [ ] Distinguish a velocity relative to another body from a ground-frame velocity.

---

# 5. Section 3.2 — Rockets and Variable Mass

## Why a rocket is subtle

The mass of the rocket changes because exhaust crosses the chosen system boundary. The rocket by itself is therefore an open system. A careless application of

$$
\mathbf F=\frac{d}{dt}(m\mathbf v)
$$

mixes the momentum of matter still in the rocket with the momentum carried away by exhaust.

The safe procedure is to apply momentum conservation over a short interval to a closed collection consisting of the rocket plus the small parcel of exhaust expelled during that interval.

## Sign convention

For one-dimensional motion, take the rocket's forward direction as positive. Let

- $v$ be the rocket velocity in the inertial frame;
- $dm<0$ be the rocket's mass change;
- $v_{\mathrm{ex}}>0$ be the exhaust speed relative to the rocket, directed backward.

The exhaust velocity in the inertial frame is approximately

$$
v-v_{\mathrm{ex}}.
$$

## Derivation in free space

Initial momentum:

$$
p_i=mv.
$$

After a short interval, the rocket has mass $m+dm$ and velocity $v+dv$, while expelled mass $-dm$ moves at approximately $v-v_{\mathrm{ex}}$:

$$
p_f=(m+dm)(v+dv)+(-dm)(v-v_{\mathrm{ex}}).
$$

Discarding the second-order product $dm\,dv$ and setting $p_f=p_i$ gives

$$
m\,dv=-v_{\mathrm{ex}}\,dm.
$$

Thus

$$
m\dot v=-\dot m\,v_{\mathrm{ex}}.
$$

Because $\dot m<0$, the thrust $-\dot m\,v_{\mathrm{ex}}$ is positive.

Separating variables,

$$
dv=-v_{\mathrm{ex}}\frac{dm}{m}.
$$

For constant exhaust speed,

$$
\boxed{
v_f-v_i
=v_{\mathrm{ex}}\ln\left(\frac{m_i}{m_f}\right)
}.
$$

## With an external force

The one-dimensional equation becomes

$$
\boxed{
m\dot v=-\dot m\,v_{\mathrm{ex}}+F_{\mathrm{ext}}
}.
$$

For vertical ascent with upward positive and constant $g$,

$$
m\dot v=-\dot m\,v_{\mathrm{ex}}-mg.
$$

If $m(t)=m_0-kt$, where $k>0$, then

$$
\dot v=\frac{k v_{\mathrm{ex}}}{m_0-kt}-g.
$$

With $v(0)=0$,

$$
\boxed{
v(t)=v_{\mathrm{ex}}
\ln\left(\frac{m_0}{m_0-kt}\right)-gt
}.
$$

## Physical interpretation

The logarithm means equal increments of speed require equal ratios of mass, not equal amounts of fuel. The benefit of staging is that empty tanks are discarded rather than accelerated during later burns.

## Limiting and dimensional checks

- If $m_f=m_i$, then $\Delta v=0$.
- If $v_{\mathrm{ex}}=0$, expelling mass produces no thrust.
- $-\dot m v_{\mathrm{ex}}$ has units of force.
- For a small fuel fraction $\epsilon$, $\ln[1/(1-\epsilon)]\approx\epsilon$.
- Lift-off requires initial thrust to exceed initial weight.

### My explanation of why the rocket accelerates

> 

---

# 6. Section 3.3 — The Center of Mass

## Definition

For discrete particles with total mass $M=\sum_\alpha m_\alpha$,

$$
\boxed{
\mathbf R
=\frac{1}{M}\sum_\alpha m_\alpha\mathbf r_\alpha
}.
$$

For a continuous body,

$$
\boxed{
\mathbf R=\frac{1}{M}\int\mathbf r\,dm
}.
$$

Depending on the object,

$$
dm=\lambda\,dl,
\qquad
dm=\sigma\,dA,
\qquad
dm=\rho\,dV.
$$

## Symmetry before integration

Symmetry often determines one or more components immediately. State the symmetry first, then integrate only the component that can be nonzero.

For example, if a lamina is symmetric under $x\mapsto-x$, then

$$
X_{\mathrm{CM}}=0.
$$

## Momentum and the center of mass

Differentiate the definition for a fixed-mass system:

$$
M\dot{\mathbf R}
=\sum_\alpha m_\alpha\dot{\mathbf r}_\alpha
=\mathbf P.
$$

Differentiate again:

$$
\boxed{
M\ddot{\mathbf R}=\dot{\mathbf P}=\mathbf F_{\mathrm{ext}}
}.
$$

Thus the center of mass moves as though all mass were concentrated there and the net external force acted there. This statement describes the translational motion of the system; it does not say that the individual particles follow the center of mass.

## Explosions and internal motion

If an airborne object explodes, internal forces abruptly change the fragments' relative velocities. They do not change the center-of-mass trajectory. With gravity as the only external force,

$$
M\ddot{\mathbf R}=M\mathbf g,
$$

so the center of mass continues on the same projectile path the intact object would have followed.

This conclusion only applies while all fragments remain in the system and experience the assumed external forces. Once a fragment hits the ground, the ground supplies an additional external impulse.

## Decomposition into center-of-mass and internal motion

Write

$$
\mathbf r_\alpha=\mathbf R+\mathbf r'_\alpha,
\qquad
\mathbf v_\alpha=\mathbf V+\mathbf v'_\alpha.
$$

By definition,

$$
\sum_\alpha m_\alpha\mathbf r'_\alpha=\mathbf 0,
\qquad
\sum_\alpha m_\alpha\mathbf v'_\alpha=\mathbf 0.
$$

This separation anticipates a recurring theme in mechanics: whole-system translation plus motion relative to the center of mass.

### My interpretation of the center of mass

> 

---

# 7. Section 3.4 — Angular Momentum of One Particle

## Definitions about an origin $O$

For position $\mathbf r$ measured from $O$,

$$
\boxed{\mathbf L_O=\mathbf r\times\mathbf p},
$$

and

$$
\boxed{\boldsymbol\tau_O=\mathbf r\times\mathbf F}.
$$

Their magnitudes are

$$
L_O=rp\sin\theta=p r_\perp,
$$

$$
\tau_O=rF\sin\phi=F r_\perp.
$$

Angular momentum measures moment of momentum about an origin. It depends not only on motion, but also on the lever arm relative to that origin.

## Derivation of the angular-momentum theorem

Differentiate:

$$
\frac{d\mathbf L_O}{dt}
=\frac{d}{dt}(\mathbf r\times\mathbf p)
=\dot{\mathbf r}\times\mathbf p
+\mathbf r\times\dot{\mathbf p}.
$$

Since $\dot{\mathbf r}=\mathbf v$ and $\mathbf p=m\mathbf v$,

$$
\mathbf v\times m\mathbf v=\mathbf 0.
$$

Using $\dot{\mathbf p}=\mathbf F$,

$$
\boxed{
\frac{d\mathbf L_O}{dt}=\boldsymbol\tau_O
}.
$$

This derivation assumes that $O$ is fixed in an inertial frame. The center of mass is a special origin for which an analogous theorem remains valid even when it accelerates.

## Central forces

A central force has the form

$$
\mathbf F=f(r)\hat{\mathbf r}.
$$

Because $\mathbf r$ and $\mathbf F$ are parallel,

$$
\boldsymbol\tau_O=\mathbf r\times\mathbf F=\mathbf 0.
$$

Therefore,

$$
\mathbf L_O=\text{constant}.
$$

Since $\mathbf L$ is perpendicular to both $\mathbf r$ and $\mathbf p$, a constant nonzero $\mathbf L$ fixes a plane perpendicular to it. The orbit remains in that plane.

## Polar-coordinate form

For planar motion,

$$
\mathbf v=\dot r\,\hat{\mathbf r}+r\dot\phi\,\hat{\boldsymbol\phi}.
$$

Then

$$
\mathbf L
=m\mathbf r\times\mathbf v
=mr^2\dot\phi\,\hat{\mathbf z}.
$$

Thus

$$
\boxed{L=mr^2\dot\phi}.
$$

## Kepler's second law

In a short time $dt$, the radius vector sweeps an approximate triangular area

$$
dA=\frac12 r(r\,d\phi).
$$

Hence

$$
\frac{dA}{dt}
=\frac12r^2\dot\phi
=\frac{L}{2m}.
$$

If the force is central, $L$ is constant, so

$$
\boxed{\frac{dA}{dt}=\text{constant}}.
$$

This is Kepler's second law. It follows from centrality alone, not specifically from the inverse-square form of gravity.

### Connection to Chapter 1 polar acceleration

The transverse component of acceleration is

$$
a_\phi=r\ddot\phi+2\dot r\dot\phi.
$$

For a central force, $a_\phi=0$. Multiplying by $mr$ gives

$$
m(r^2\ddot\phi+2r\dot r\dot\phi)
=\frac{d}{dt}(mr^2\dot\phi)=0,
$$

which is the same conservation law. This links the moving-basis derivation from Chapter 1 to the angular-momentum viewpoint.

---

# 8. Section 3.5 — Angular Momentum of Many Particles

## Total angular momentum

About a common origin $O$,

$$
\mathbf L_O
=\sum_\alpha \mathbf r_\alpha\times\mathbf p_\alpha.
$$

Differentiating gives external and internal torque terms:

$$
\dot{\mathbf L}_O
=\boldsymbol\tau_O^{\mathrm{ext}}
+\sum_\alpha\sum_{\beta\ne\alpha}
\mathbf r_\alpha\times\mathbf F_{\alpha\beta}.
$$

Pair the internal torques for particles $\alpha$ and $\beta$:

$$
\mathbf r_\alpha\times\mathbf F_{\alpha\beta}
+\mathbf r_\beta\times\mathbf F_{\beta\alpha}
=(\mathbf r_\alpha-\mathbf r_\beta)
\times\mathbf F_{\alpha\beta}.
$$

Newton's third law alone is not enough to make this zero. We also need the internal force to be central: $\mathbf F_{\alpha\beta}$ must lie along $\mathbf r_\alpha-\mathbf r_\beta$. Under these assumptions,

$$
\boxed{
\dot{\mathbf L}_O=\boldsymbol\tau_O^{\mathrm{ext}}
}.
$$

If the net external torque is zero,

$$
\boxed{\mathbf L_O=\text{constant}}.
$$

## Why angular momentum requires a stronger condition than linear momentum

For linear momentum, equal and opposite internal forces cancel directly. For angular momentum, equal and opposite forces can still form a couple unless they act along the line joining the particles. The central-force condition removes that internal couple.

### Explain this distinction in my own words

> 

## Translation plus internal angular momentum

Using $\mathbf r_\alpha=\mathbf R+\mathbf r'_\alpha$ and $\mathbf v_\alpha=\mathbf V+\mathbf v'_\alpha$,

$$
\boxed{
\mathbf L_O
=\mathbf R\times M\mathbf V
+\mathbf L_{\mathrm{CM}}
}.
$$

The first term is angular momentum of the center of mass about $O$. The second is angular momentum of motion relative to the center of mass.

This decomposition prevents a common mistake: treating all angular momentum as spin. A body can have angular momentum about an origin because its center of mass is moving, because it spins about its center of mass, or both.

## Fixed-axis rotation

For a rigid body rotating about the $z$ axis with angular speed $\omega$, a mass element at perpendicular distance $\rho$ has speed $v=\rho\omega$. Its $z$-component of angular momentum is

$$
dL_z=\rho v\,dm=\rho^2\omega\,dm.
$$

Therefore,

$$
\boxed{L_z=I_z\omega},
$$

where

$$
\boxed{I_z=\int\rho^2\,dm}.
$$

This is a component relation for rotation about a fixed axis. In general three-dimensional rigid-body motion, $\mathbf L$ need not be parallel to $\boldsymbol\omega$.

---

# 9. Essential derivations to reproduce

## Derivation 1 — Total momentum theorem

- [ ] Write the equation for each particle.
- [ ] Sum over particles.
- [ ] Pair internal forces.
- [ ] State exactly where Newton's third law is used.
- [ ] Conclude $\dot{\mathbf P}=\mathbf F_{\mathrm{ext}}$.

## Derivation 2 — Rocket equation

- [ ] Define the inertial-frame and relative exhaust velocities.
- [ ] Compare momentum before and after $dt$.
- [ ] Drop only second-order differentials.
- [ ] Obtain $m\,dv=-v_{\mathrm{ex}}\,dm$.
- [ ] Integrate to $\Delta v=v_{\mathrm{ex}}\ln(m_i/m_f)$.

## Derivation 3 — Center-of-mass equation

- [ ] Start from $M\mathbf R=\sum m_\alpha\mathbf r_\alpha$.
- [ ] Differentiate to show $M\dot{\mathbf R}=\mathbf P$.
- [ ] Differentiate again to show $M\ddot{\mathbf R}=\mathbf F_{\mathrm{ext}}$.
- [ ] Explain the exploding-projectile consequence.

## Derivation 4 — Single-particle angular-momentum theorem

- [ ] Differentiate $\mathbf L=\mathbf r\times\mathbf p$.
- [ ] Explain why $\mathbf v\times m\mathbf v=0$.
- [ ] Obtain $\dot{\mathbf L}=\boldsymbol\tau$.
- [ ] State the origin assumption.

## Derivation 5 — Kepler's second law

- [ ] Derive $L=mr^2\dot\phi$.
- [ ] Derive $dA/dt=r^2\dot\phi/2$.
- [ ] Conclude $dA/dt=L/(2m)$.
- [ ] State why the result applies to any central force.

## Derivation 6 — Many-particle angular momentum

- [ ] Separate external and internal torques.
- [ ] Pair the two torque terms for each particle pair.
- [ ] Use both the third law and centrality.
- [ ] Obtain $\dot{\mathbf L}=\boldsymbol\tau_{\mathrm{ext}}$.

---

# 10. Common traps

## Trap 1 — Conserving momentum without defining the system

Ask what matter is included and what crosses the boundary. A rocket alone is not a closed fixed-mass system.

## Trap 2 — Mixing reference frames

Muzzle speed and exhaust speed are often given relative to the gun or rocket, while momentum must be written using velocities in one inertial frame.

## Trap 3 — Assuming internal forces do nothing

Internal forces can dramatically change individual motions and internal energy. They cancel only in selected whole-system equations.

## Trap 4 — Conserving kinetic energy in an explosion

Chemical or internal energy can become kinetic energy. Momentum conservation does not imply kinetic-energy conservation.

## Trap 5 — Forgetting the angular-momentum origin

Always write $\mathbf L_O$ and $\boldsymbol\tau_O$ until the origin is unambiguous.

## Trap 6 — Using the third law alone for internal torques

Equal and opposite internal forces cancel total force. For their torques to cancel, the forces must also be central.

## Trap 7 — Writing $\mathbf L=I\boldsymbol\omega$ universally

$L_z=I_z\omega$ is valid for the fixed-axis setting used here. The full vector relationship is subtler and belongs to rigid-body dynamics.

## Trap 8 — Applying the center-of-mass trajectory after impact

Once a fragment hits the ground, the ground supplies an external force. The original free-flight center-of-mass argument must be revised.

---

# 11. Mastery checks

I am ready to move on when I can answer these without notes.

## Conceptual

1. Why do internal forces cancel from $\dot{\mathbf P}$?
2. Why is a rocket not handled by simply differentiating its instantaneous $m\mathbf v$?
3. What can the center of mass do while particles move violently relative to it?
4. Why does a central force imply planar motion?
5. Why is Newton's third law sufficient for total linear momentum but not, by itself, for total angular momentum?
6. In what sense is angular momentum origin-dependent?

## Derivational

- [ ] Derive the rocket equation from a short-time momentum balance.
- [ ] Derive $M\ddot{\mathbf R}=\mathbf F_{\mathrm{ext}}$.
- [ ] Derive $\dot{\mathbf L}=\boldsymbol\tau$.
- [ ] Derive Kepler's equal-area law from angular momentum.
- [ ] Derive the cancellation of internal torque under central forces.

## Problem-solving

- [ ] Solve a recoil problem using relative velocities correctly.
- [ ] Analyze a rocket with gravity.
- [ ] Find a continuous body's center of mass using symmetry and integration.
- [ ] Analyze an explosion using center-of-mass motion.
- [ ] Use angular momentum about a carefully chosen point.
- [ ] Compare two valid choices of origin for a rolling body.

---

# 12. Questions, mistakes, and changed understanding

## Questions to revisit

1. 
2. 
3. 

## Mistakes worth preserving

1. 
2. 
3. 

## What changed in my understanding?

> 

## Connection to later chapters

- Chapter 4 will add energy as another whole-system quantity.
- Chapter 7 will show that conservation laws arise naturally from generalized-coordinate structure.
- Chapter 8 will use angular momentum to reduce central-force motion to an effectively one-dimensional radial problem.
- Chapter 10 will develop the full rigid-body meaning of $\mathbf L$, $I$, and $\boldsymbol\omega$.
- In quantum mechanics, linear and angular momentum become generators of translations and rotations; the classical conservation structure developed here remains central.

---

# 13. End-of-chapter summary

Complete after finishing the problems.

## Five ideas I want to retain

1. 
2. 
3. 
4. 
5. 

## Three derivations I can now reproduce

1. 
2. 
3. 

## One idea that still feels incomplete

> 
