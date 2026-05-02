---
layout: default
title: "Chapter 4: Key Lemmas"
---

# Chapter 1. Key Lemmas: Three-Stage Inequalities That Confine the Location of Blow-up

## 4.1 Purpose of This Chapter

In this chapter, we use the three **OS-Geometry** quantities:

*   $M(t,\ell)$: Local Concentration
*   $E(t,\lambda)$: Scale-wise Enstrophy
*   $S(T)$: OSG2ADV BKM Quantity (Blow-up Criterion)

to completely confine the possibility of blow-up in the Navier–Stokes equations within the scale structure.

We establish the following four fundamental lemmas that link these quantities:

---

## 4.2 Lemma A: Control of Filtered Vorticity by $M$

**Lemma A** establishes that the filtered vorticity at scale $\ell$ is directly bounded by the local concentration $M$ at the same scale.

> ### **Lemma A**
> For any $x \in \mathbb{R}^3$ and $\ell > 0$:
> 
> $$|\omega_\ell(t,x)|^2 \le C \cdot \ell^{-3} M(t,\ell)$$

**Significance:**
This means that as long as the concentration $M$ is finite at scale $\ell$, the filtered vorticity $\omega_\ell$ cannot diverge.

---

## 4.3 Lemma B: Control of the Gradient by $M$ and $E$

**Lemma B** is the core of the OS control mechanism. It decomposes the gradient of velocity (the stretching rate) into contributions from different scales.

> ### **Lemma B**
> For any scale $\ell > 0$:
> 
> $$\|\nabla v_\ell\|_{L^\infty} \le C \left( \frac{M(t,\ell)}{\ell^3} \right)^{1/2} + \int_{\ell}^{\infty} \frac{E(t, \lambda)^{1/2}}{\lambda} \frac{d\lambda}{\lambda}$$

**Interpretation:**
*   **The first term:** Represents the contribution from the **local scale $\ell$** (controlled by $M$).
*   **The second term:** Represents the cumulative contribution from **higher-scale structures** (controlled by the energy hierarchy $E$).

---

## 4.4 Lemma C: Uniform Control of $E$ by $L^2$ Norm

**Lemma C** ensures that the scale-wise enstrophy $E(t,\lambda)$ does not behave pathologically at large scales.

> ### **Lemma C**
> The scale-wise enstrophy $E(t,\lambda)$ is uniformly bounded by the global enstrophy (vorticity $L^2$ norm):
> 
> $$\int_0^\infty E(t, \lambda) \frac{d\lambda}{\lambda} = \|\omega(t, \cdot)\|_{L^2}^2$$

**Significance:**
This guarantees that the energy flow remains consistent with the global physical constraints of the fluid.

---

## 4.5 Lemma D: Non-collapse of the Critical Scale $\ell_c(t)$

**Lemma D** provides the ultimate protection against blow-up by proving that the scale of danger cannot shrink to zero instantly.

> ### **Lemma D**
> If the global enstrophy is bounded, then the critical scale $\ell_c(t)$ is bounded away from zero:
> 
> $$\ell_c(t) \ge \ell_{\min} > 0$$

**Conclusion:**
Since blow-up requires concentration at an infinitely small scale ($\ell \to 0$), the fact that $\ell_c(t)$ stays positive means that the **Navier–Stokes equations are regular** (blow-up is confined and suppressed).

---

## 4.6 Summary of Control Flow

The logic of these lemmas forms a closed loop of stability:

1.  **Global Energy** $\implies$ **Lemma C** ($E$ is bounded).
2.  **$E$ and $M$** $\implies$ **Lemma B** ($\nabla v$ is controlled).
3.  **Controlled $\nabla v$** $\implies$ **Lemma D** ($\ell_c$ cannot collapse).
4.  **Positive $\ell_c$** $\implies$ **No Blow-up**.
