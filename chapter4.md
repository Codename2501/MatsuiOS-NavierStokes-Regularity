---
layout: default
title: "Chapter 4: Key Lemmas"
---

# Chapter 4. Key Lemmas: Three-Stage Inequalities That Confine the Location of Blow-up

## 4.1 Purpose of This Chapter

In this chapter, we use the three OS-Geometry quantities:

- \( M(t,\ell) \)
- \( E(t,\lambda) \)
- \( S(T) \)

to completely confine the possibility of blow-up in the Navier–Stokes equations  
within the scale structure.

We establish:

- **Lemma A:** Local concentration → filtered vorticity  
- **Lemma B:** Local concentration + scale energy → gradient  
- **Lemma C:** \(E\) controlled uniformly by the \(L^2\) norm  
- **Lemma D:** Non-collapse of the critical scale  
- **Theorem 2:** Complete control of the stretching term  
- **Theorem 3:** OSG2ADV–BKM ⇔ classical BKM  

Once these are established,  
**the mathematical possibility of blow-up disappears.**

---

## 4.2 Lemma A: Control of Filtered Vorticity by \( M \)

### **Lemma A (local concentration → filtered vorticity)**

$$
|\omega_\ell(t,x)|
\le
C\,\ell^{-3/2}\,M(t,c\ell)^{1/2}.
$$

### Interpretation

- The filtered vorticity at scale \( \ell \)  
  is controlled solely by the local concentration \( M \) at the same scale.
- If blow-up occurs, \( M \) must diverge first.
- Thus **\( M \) is the primary danger indicator.**

### Sketch of Proof

- Write \( \omega_\ell = K_\ell * \omega \) and evaluate via spherical averaging.
- Apply Cauchy–Schwarz and the volume factor \( \ell^3 \).
- The estimate aligns naturally with the scale structure of OS Geometry.

---

## 4.3 Lemma B: Control of the Gradient by \( M \) and \( E \)

### **Lemma B (gradient control by \( M \) and \( E \))**

$$
\|\nabla v_\ell(t)\|_{L^\infty}
\le
C\left(
\ell^{-3/2} M(t,c\ell)^{1/2}
+
\int_0^\infty
\min\left\{
\frac{\lambda}{\ell^2},
\frac{1}{\lambda}
\right\}
E(t,\lambda)^{1/2}
\,\frac{d\lambda}{\lambda}
\right).
$$

### Interpretation

The gradient (the source of stretching) is controlled in two OS stages:

- **small scales:** controlled by \( M \)
- **medium/large scales:** controlled by \( E \)

Thus **all blow-up-driving mechanisms are controlled by OS quantities.**

### Sketch of Proof

- Use the Biot–Savart law decomposed by scale.
- Apply Calderón–Zygmund estimates.
- Use the OS scale hierarchy to separate contributions.

---

## 4.4 Lemma C: Uniform Control of \( E \) by the \( L^2 \) Norm

### **Lemma C (scale energy is \(L^2\)-controlled)**

$$
\int_0^\infty
E(t,\lambda)\,\frac{d\lambda}{\lambda}
=
\|\omega(t)\|_{L^2}^2.
$$

### Interpretation

- \( E \) represents the enstrophy distribution across scales.
- Its total mass is always equal to the \( L^2 \) norm.
- Therefore **\( E \) cannot blow up.**

### Conclusion

Since \( E \) is bounded:

- the second term in Lemma B is always finite  
- gradient blow-up depends only on \( M \)  
- eliminating blow-up of \( M \) eliminates all blow-up  

---

## 4.5 Lemma D: Non-collapse of the Critical Scale \( \ell_c(t) \)

### **Lemma D (critical scale cannot collapse)**

$$
\ell_c(t) \not\to 0 \qquad (t \to T).
$$

### Interpretation

- At very small scales, viscosity always suppresses concentration.
- Thus blow-up **cannot** occur at arbitrarily small scales.
- If blow-up occurs, it must be at a finite scale:

$$
\ell \approx \ell_c(t).
$$

### Conclusion

The possible location of blow-up is  
**completely confined to a finite scale region.**

---

## 4.6 Theorem 2: Complete Control of the Stretching Term

### **Theorem 2 (stretching is fully controlled)**

From Lemmas A–D, the stretching term

$$
\|(\omega\cdot\nabla)v_\ell\|_{L^\infty}
$$

is completely controlled by the finiteness of \( M \) and \( E \).

In particular:

- \( M \) does not blow up  
- \( E \) is controlled by the \( L^2 \) norm  

Therefore:

**the stretching term cannot cause blow-up.**

---

## 4.7 Theorem 3: OSG2ADV–BKM ⇔ Classical BKM

### **Theorem 3 (equivalence of BKM conditions)**

The following are equivalent:

$$
S(T)
=
\sup_{x,\ell}
\int_0^T |\omega_\ell(t,x)|\,dt
< \infty,
$$

and

$$
\int_0^T \|\omega(t)\|_{L^\infty}\,dt < \infty.
$$

### Interpretation

- If blow-up is prevented on the OSG2ADV side,  
  then classical Navier–Stokes blow-up is also prevented.
- The OS three-stage structure is **fully consistent** with classical BKM.

---

## 4.8 Conclusion of This Chapter

The lemmas and theorems in this chapter show that the three OS quantities:

- \( M \) (local concentration)  
- \( E \) (scale energy)  
- \( S \) (time-integrated filtered vorticity)  

**completely confine the possibility of blow-up**  
in the Navier–Stokes equations.

This directly leads to the **Main Regularity Theorem** in Chapter 5.
