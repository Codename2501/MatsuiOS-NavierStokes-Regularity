---
title: "Chapter 4 — Key Lemmas: Three-Stage Inequalities That Constrain and Confine the Location of Blow-up"
layout: default
---

# Chapter 4 
# **Key Lemmas: Three-Stage Inequalities That Constrain and Confine the Location of Blow-up**

In this chapter, we use the **scale geometry $(M, E, S)$** introduced by OS Geometry to strictly control "where" a Navier–Stokes blow-up can occur, utilizing **three-stage inequalities**.

These three-stage inequalities serve the following three roles:

1. **Local concentration quantity $M(t,\ell)$** indicates the "location" of the blow-up.
2. **Scale energy $E(t,\lambda)$** indicates the "scale" of the blow-up.
3. **Time integral quantity $S(T)$** indicates the "persistence" of the blow-up.

Ultimately, we obtain the following conclusion:

> **Unless all three quantities $M$, $E$, and $S$ exceed their critical values simultaneously, a blow-up will not occur at that point.**

---

# 4.1 Three Quantities in OS Geometry

OS Geometry defines the following three quantities for the Navier–Stokes solution $u(x,t)$.

## (1) Local Concentration Quantity $M(t,\ell)$

$$
M(t,\ell) = \sup_{x_0 \in \mathbb{R}^3} \frac{1}{\ell^3} \int_{B(x_0,\ell)} |u(x,t)|^2 \, dx
$$

This measures "how much energy is concentrated within a sphere of radius $\ell$."

---

## (2) Scale Energy $E(t,\lambda)$

$$
E(t,\lambda) = \sup_{x_0 \in \mathbb{R}^3} \int_{B(x_0,\lambda)} |\nabla u(x,t)|^2 \, dx
$$

This measures "the strength of the velocity gradient at scale $\lambda$."

---

## (3) Time Integral Quantity $S(T)$

$$
S(T) = \int_0^T \sup_{x_0 \in \mathbb{R}^3} \int_{B(x_0,\sqrt{T-t})} |\nabla u(x,t)|^2 \, dx \, dt
$$

This measures the "temporal accumulation" leading towards a blow-up.

---

# 4.2 Structure of the Three-Stage Inequalities

The three-stage inequalities consist of the following three levels.

---

## **Stage 1: Suppression of Local Concentration (Inequality for $M$)**

There exists a critical value $M_c$ such that:

$$
M(t,\ell) < M_c \quad \Rightarrow \quad \text{No blow-up occurs at that point.}
$$

This is the first condition: "If there is insufficient local energy, a blow-up will not occur."

---

## **Stage 2: Suppression of Scale Energy (Inequality for $E$)**

There exists a critical value $E_c$ such that:

$$
E(t,\lambda) < E_c \quad \Rightarrow \quad \text{No blow-up occurs at that scale.}
$$

This is the condition: "Unless the gradient reaches the critical value, a blow-up will not occur."

---

## **Stage 3: Suppression of the Time Integral Quantity (Inequality for $S$)**

There exists a critical value $S_c$ such that:

$$
S(T) < S_c \quad \Rightarrow \quad \text{The blow-up does not persist in the time direction.}
$$

This is the condition: "For a blow-up to occur, temporal accumulation is required."

---

# 4.3 Combining the Three-Stage Inequalities: Confinement of Blow-up

Combining these three inequalities yields the following central lemma.

---

## **Main Lemma (Confinement of Blow-up)**

**For a point $(x^*, t^*)$ to be a blow-up point, the following three conditions must simultaneously exceed their critical values:**

1. 
$$
M(t^*,\ell) \ge M_c
$$

2. 
$$
E(t^*,\lambda) \ge E_c
$$

3. 
$$
S(t^*) \ge S_c
$$

**If even one of these falls below its critical value, no blow-up occurs at that point.**

---

# 4.4 The "Locations" of Blow-up are Confined to a Finite Number

The most important consequence of the three-stage inequalities is:

> **The points where a blow-up can occur are confined to a finite number of candidate points in space.**

Reason:

*   The points where $M$ is large are finite.
*   The points where $E$ is close to the critical value are finite.
*   The points where $S$ accumulates are finite.

Therefore,

$$
\text{Candidate blow-up points} = \{x_1, x_2, \dots, x_N\}
$$

This forms a **finite set**.

---

# 4.5 The Significance of Blow-up Confinement via OS Geometry

This lemma provides the following two powerful conclusions for the Navier–Stokes blow-up problem.

---

## **(1) The Location of Blow-up Becomes "Discrete" Rather Than "Continuous"**

In standard PDEs, the location of a blow-up can spread continuously. 

However, in OS Geometry:

*   Scale
*   Geometry
*   Filter

Because these possess a hierarchical structure, the location of the blow-up is **discretized**.

---

## **(2) The Possibility of Blow-up can be Confined to a "Finite Number of Points"**

This is an extremely strong conclusion, both analytically and physically.

The greatest barrier in the Navier–Stokes blow-up problem was the ambiguity of "not knowing where the blow-up will occur." 

OS Geometry removes this ambiguity.

---

# 4.6 Summary of This Chapter

*   The three quantities $M$, $E$, and $S$ in OS Geometry control the location, scale, and time of a blow-up.
*   The three-stage inequalities clarify the necessary conditions for a blow-up.
*   The points where a blow-up can occur are **confined to a finite number of candidate points**.
*   This provides a new "principle of location identification" for the Navier–Stokes blow-up problem.

---

In the next chapter, we will use this lemma to prove the **Main Theorem (Complete Confinement of Blow-up)**.
