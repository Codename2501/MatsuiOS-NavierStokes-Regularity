---
layout: default
title: "Chapter 2: OS Geometry"
---

# Chapter 2. OS Geometry: Scale, Geometry, and Critical Structure

## 2.1 Definition of the Scale Hierarchy

OS Geometry generates the **scale structure** $\ell$ after the transition `OS-atm → OS-dir` produces directional structure.

The scale hierarchy begins at the minimal scale $\ell$:

$$ \ell, 2\ell, 4\ell, 8\ell, \dots $$

This hierarchy functions as a **geometric coordinate system** for classifying localization, concentration, and diffusion of vorticity. It allows fluid structure to be interpreted as:

> **“At which scale is the danger located?”**

---

## 2.2 Local Concentration $M(t,\ell)$

Defined by the supremum of the local $L^2$ norm of vorticity:

$$ M(t,\ell) = \sup_{x\in\mathbb{R}^3} \int_{B(x,\ell)} |\omega(t,y)|^2\,dy $$

### Interpretation
*   **Small $\ell$ + Large $M$:** Sharp concentration (High danger).
*   **Large $\ell$ + Large $M$:** Broad concentration (Relative stability).
*   **Blow-up condition:** Any blow-up must cause $M$ to diverge at some scale.

Thus, **$M$ is the first danger indicator.**

---

## 2.3 Scale-wise Enstrophy $E(t,\lambda)$

Defined by:

$$ E(t,\lambda) = \lambda^2 \int_{\mathbb{R}^3} |\omega_\lambda(t,x)|^2\,dx $$

### Role
*   Measures energy distribution across scales.
*   **Small-scale energy growth** signals potential instability.
*   **Large-scale energy** provides global stabilization.
*   Total integral relates directly to the $L^2$ norm.

Thus, **$E$ quantifies the geometry of scales.**

---

## 2.4 Generation of the Critical Scale $\ell_c(t)$

The core of OS Geometry is the existence of a **critical scale**:

$$ \ell_c(t) = \inf\{\ell > 0 : M(t,\ell) \text{ exceeds a critical threshold}\} $$

### Meaning
*   **Below $\ell_c(t)$:** Viscosity always suppresses concentration.
*   **Above $\ell_c(t)$:** Nonlinearity may dominate.
*   **Location:** Any blow-up must occur at a finite scale $\ell \approx \ell_c(t)$.

Thus, OS Geometry **pinpoints the location of possible blow-up.**

---

## 2.5 The Three-Stage Structure of OSG (M, E, S)

OS Geometry classifies blow-up using three OS quantities:

1.  **$M$ — Local Concentration:** The first sign of geometric danger.
2.  **$E$ — Scale Energy:** Controls energy flow between hierarchies.
3.  **$S$ — OSG2ADV BKM Quantity:** The final blow-up criterion (Beale-Kato-Majda type).

Together, they **completely confine blow-up.**

---

## 2.6 Purpose of This Chapter

The purpose of this chapter is:

> **To build the foundation for treating Navier–Stokes blow-up as a geometry of scales.**

OS Geometry provides the structural framework that makes the rigorous analysis in Chapters 3–5 possible.
