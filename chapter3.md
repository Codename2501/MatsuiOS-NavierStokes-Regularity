---
layout: default
title: "Chapter 3: OSG2ADV"
---

# Chapter 3. OSG2ADV: A Filtered Vorticity Equation Fully Equivalent to Navier–Stokes

## 3.1 Definition of the Filtered Vorticity \( \omega_\ell \)

For a given scale \( \ell \), the filtered vorticity is defined by:

$$
\omega_\ell(t,x) = (K_\ell * \omega)(t,x),
$$

where

$$
K_\ell(x) = \ell^{-3} K(x/\ell)
$$

is a smooth scale filter, and

$$
\omega = \nabla \times v
$$

is the vorticity of the Navier–Stokes velocity field.

This filtering operation extracts the **local structure of vorticity at scale \( \ell \)**.  
Because it aligns naturally with the scale hierarchy of OS Geometry,  
the fundamental variable of OSG2ADV is \( \omega_\ell \).

---

## 3.2 Derivation of OSG2ADV

The vorticity formulation of the Navier–Stokes equations is:

$$
\partial_t \omega + (v\cdot\nabla)\omega
= (\omega\cdot\nabla)v + \nu\Delta\omega.
$$

Applying the filter \( K_\ell \) yields:

$$
\partial_t \omega_\ell
+ (v\cdot\nabla)\omega_\ell
=
(\omega\cdot\nabla)v_\ell
+ \nu\Delta\omega_\ell
+ R(v,\omega,\ell),
$$

where the commutator (exchange error) is:

$$
R(v,\omega,\ell)
=
K_\ell * \big[(v\cdot\nabla)\omega\big]
-
(v\cdot\nabla)(K_\ell * \omega).
$$

Rewriting this equation in a form aligned with OS Geometry yields  
the **OSG2ADV (OS Geometry 2 – Advection Form)** equation:

$$
\partial_t \omega_\ell
=
A_\ell(\omega_\ell)
+
S_\ell(\omega_\ell)
+
\nu\Delta\omega_\ell
+
R(v,\omega,\ell),
$$

where:

- \( A_\ell \): OS-type advection operator  
- \( S_\ell \): OS-type stretching operator  
- \( R \): scale-interaction (commutator) term  

This formulation is fully consistent with the three-stage structure  
\( M, E, S \) of OS Geometry.

---

## 3.3 Complete Equivalence with the Navier–Stokes Vorticity Equation (Theorem 1)

### **Theorem 1 (OSG2ADV = Filtered Navier–Stokes Vorticity Equation)**

Let \( v \) be a sufficiently smooth solution of the Navier–Stokes equations.  
Then the filtered vorticity

$$
\omega_\ell = K_\ell * \omega
$$

satisfies the OSG2ADV evolution equation.

Conversely, if a family of functions \( \{\omega_\ell\}_{\ell>0} \)  
satisfies OSG2ADV together with appropriate reconstruction conditions, then:

$$
\omega = \lim_{\ell\to 0} \omega_\ell
$$

is a solution of the Navier–Stokes vorticity equation.

---

### Sketch of Proof

**(NS → OSG2ADV)**  
Applying the filter \( K_\ell \) to the NS vorticity equation:

- linear terms commute with the filter  
- nonlinear terms produce the commutator \( R \)

Thus the OSG2ADV form is obtained.

**(OSG2ADV → NS)**  
As \( \ell \to 0 \):

$$
\omega_\ell \to \omega,\qquad
v_\ell \to v,\qquad
R(v,\omega,\ell) \to 0,
$$

so OSG2ADV converges to the NS vorticity equation.

---

## 3.4 OS Decomposition of the Stretching Term

The stretching term:

$$
(\omega\cdot\nabla)v_\ell
$$

is the core mechanism behind potential blow-up.

OS Geometry decomposes it according to scale structure:

$$
(\omega\cdot\nabla)v_\ell
=
\underbrace{\omega_\ell\cdot\nabla v_\ell}_{\text{same-scale}}
+
\underbrace{(\omega - \omega_\ell)\cdot\nabla v_\ell}_{\text{higher-scale}}.
$$

This yields a **two-stage OS control**:

- same-scale term → controlled by \( M \)  
- higher-scale term → controlled by \( E \)

This decomposition is the foundation of  
**Theorem 2 (complete control of stretching)** in Chapter 4.

---

## 3.5 Structure of Scale Interactions

The commutator \( R(v,\omega,\ell) \)  
encodes interactions between different scales.

A key estimate is:

$$
\|R(v,\omega,\ell)\|
\le
C\,\ell\,\|\nabla v\|_{L^\infty}\,\|\omega\|_{L^\infty}.
$$

Thus:

- the smaller the scale \( \ell \), the smaller the error  
- \( R \to 0 \) as \( \ell \to 0 \)  
- OSG2ADV and NS coincide exactly in the limit  

This supports the claim that  
**OSG2ADV is simply another representation of NS**.

---

## 3.6 Purpose of This Chapter

The purpose of this chapter is:

**To establish, as a theorem, that OSG2ADV is fully equivalent  
to the Navier–Stokes vorticity equation.**

This equivalence allows the scale structure of OS Geometry  
to be applied directly to the blow-up analysis of Navier–Stokes.
