# An Elastic Constitutive Model of Spacetime and Its Applications

**Document Metadata**

| | |
|---|---|
| **Store** | public-portfolio |
| **Publication** | Ph.D. dissertation, Dept. of Computational Engineering, Mississippi State University, Starkville, MS, USA, Dec. 2018 |
| **DOI / URL** | ProQuest Dissertations & Theses, Publication No. 10978458 (open access); https://www.proquest.com/docview/2162607366 |
| **Cite as** | T. G. Tenev, "An elastic constitutive model of spacetime and its applications," Ph.D. dissertation, Dept. Comput. Eng., Mississippi State Univ., Starkville, MS, USA, 2018. |
| **Converted from** | Local git source `tgtenev/thesis`, commit `e83fbaf` ("Published version") |

---

**Tichomir G. Tenev**
Department of Computational Engineering, Mississippi State University, Starkville, MS 39759, USA
ticho@tenev.com

A dissertation submitted for the degree of Doctor of Philosophy.

**Major Professor:** Mark F. Horstemeyer
**Committee:** Anzhong Wang, Tomasz Haupt, Shantia Yarahmadian
**Dean, Bagley College of Engineering:** Jason M. Keith

*Degree conferred December 2018.*

---

## Abstract

We introduce an elastic constitutive model of gravity that enables the interpretation of cosmological observations in terms of established ideas from Solid Mechanics and multi-scale modeling. The behavior of physical space is identified with that of a material-like medium called "cosmic fabric," which exhibits constitutive behavior. This cosmic fabric is a solid hyperplate that is broad in the three ordinary spatial dimensions and thin in a fourth hyperspatial dimension. Matter in space is treated as fabric inclusions that prescribe in-plane (three-dimensional) strain causing the transverse bending of the fabric into the fourth hyperspatial dimension. The linearized Einstein–Hilbert action, which governs the dynamics of physical space, is derived from postulating Hooke's Law for the fabric, and the Schwarzschild metric is recovered from investigating matter–fabric interactions. At the continuum length scale, the Principle of Relativity is shown to apply for both moving and stationary observers alike, so that the fabric's rest reference frame remains observationally indistinguishable at such a length scale. Within the Cosmic Fabric paradigm, the structural properties of space at different hierarchical length scales can be investigated using theoretical notions and computational tools from solid mechanics to address outstanding problems in cosmology and fundamental physics. For example, we propose and offer theoretical support for the "Inherent Structure Hypothesis," which states that the gravitational anomalies currently attributed to dark matter may in fact be manifestations of the inherent (undeformed) curvature of space. In addition, we develop a numerical framework wherein one can perform numerical "experiments" to investigate the implications of said hypothesis.

**Keywords:** modified gravity; constitutive model; spacetime; cosmic fabric; hierarchical length scales; dark matter; particle-mesh method

## Contents

The full text is split into per-chapter files below so that GitHub renders the equations reliably (a single combined file exceeds GitHub's per-page math-rendering limit). Each chapter is self-contained with its own equation numbering.

1. [I. Introduction](tenev2018-dissertation/ch1-introduction.md)
2. [II. Background](tenev2018-dissertation/ch2-background.md)
3. [III. Cosmic Fabric Model of Gravity](tenev2018-dissertation/ch3-cosmic-fabric-model.md)
4. [IV. Recovering Relativity](tenev2018-dissertation/ch4-recovering-relativity.md)
5. [V. Spacetime Metric of a Spherically Symmetric Inclusion](tenev2018-dissertation/ch5-spacetime-metric.md)
6. [VI. Dark Matter Effect](tenev2018-dissertation/ch6-dark-matter-effect.md)
7. [VII. Numerical Framework for Weak Gravity Dynamics](tenev2018-dissertation/ch7-numerical-framework.md)
8. [VIII. Conclusions](tenev2018-dissertation/ch8-conclusions.md)
9. [IX. Future Research](tenev2018-dissertation/ch9-future-research.md)

[References](tenev2018-dissertation/references.md)

## Dedication

To the Lord Jesus Christ through Whom all things were made and without Whom nothing was made that was made. In Him we live and move and have our being.

## Acknowledgments

Before all, I thank my Heavenly Father Who is the source of all good and perfect gifts, and Who provided the time and finances, the ideas, environment, and people to allow me to accomplish this dissertation work. May it be pleasing to Him. Amen.

Mark Horstemeyer encouraged me to move to Mississippi and subsequently became my doctoral advisor and collaborator. I thank him for this and for teaching me mechanical engineering and what it means to be a scientist.

I am also thankful to the members of my graduate committee for their continual supervision and encouragement. Anzhong Wang introduced me to the General Relativity community and guided me in that area. Shantia Yarahmadian supervised my study in applied math, and shared his insights with me on the nature of time. Byron Williams introduced me to Mississippi State's graduate program and became a committee member in addition to becoming a good friend. Tomasz Haupt stepped in during the final months of my program to take Byron's place on the committee whose job had taken him elsewhere.

I would like to acknowledge the wonderful group of colleagues with whom I fellowshipped at the University's Center for Advanced Vehicular Systems (CAVS): Denver Seeley, Robert Allen, Heechen Cho, Sungkwan Moon, Nayeon Lee, and others.

John Baumgardner, Russ Humphreys, and Andrew McIntosh offered unfiltered feedback and from the beginning were a source of inspiration and encouragement.

Also, I would like to acknowledge Tamas Morvai for the helpful discussions on the nature of time, and Youseff Hammi for his gracious help with Abaqus.

Finally, I would like to acknowledge my wife, Rong Tenev, without whose support, deep insight, and encouragement, this work would not have been possible.

## List of Symbols, Abbreviations, and Nomenclature

| Symbol | Meaning |
|---|---|
| $Y$ | Young's modulus of elasticity. |
| $\nu$ | Poisson's ratio (when not used as an index). |
| $L$ | Cosmic fabric thickness. |
| $\hbar$ | The reduced Planck constant, $\hbar = 1.054571800\times 10^{-34}\ \mathrm{m}^2\ \mathrm{kg}\ \mathrm{s}^{-1}$. |
| $G$ | The gravitational constant, $G = 6.67408\times 10^{-11}\ \mathrm{m}^3\ \mathrm{kg}^{-1}\mathrm{s}^{-2}$. |
| $c$ | Speed of light, $c = 299{,}792{,}458\ \mathrm{m\ s}^{-1}$. |
| $\kappa$ | The Einstein constant, $\kappa \equiv 8\pi G / c^4$. |
| $\partial_{a},\ \partial_{ab}$ | Partial derivatives, $\partial_{a}\equiv\partial/\partial x_{a}$, and $\partial_{ab}\equiv\partial/\partial x_{a}\partial x_{b}$. |
| $\nabla^{2}$ | The Laplace operator for spatial coordinates, $\nabla^{2}\equiv\partial_{11}+\partial_{22}+\partial_{33}$. |
| $\delta_{b}^{a}$ | Kronecker delta: $\delta_{a}^{b}=\delta_{ab}=\delta^{ab}=\lbrace 1,\ a=b;\ 0,\ a\neq b\rbrace$. |
| $g_{ij}$ | The three-dimensional metric tensor. |
| $\overline{g}_ {ij}$ | The three-dimensional undeformed metric tensor. In general, a bar decoration indicates that a quantity pertains to the undeformed configuration. |
| $g_{\mu\nu},\ g$ | The spacetime metric and its determinant, $g \equiv \det g_{\mu\nu}$. |
| $\eta_{\mu\nu}$ | The Minkowski metric for flat spacetime, $\eta_{00}=-1,\ \eta_{0i}=\eta_{i0}=0,\ \eta_{ij}=\delta_{ij}$. |
| $\varepsilon_{ij},\ \varepsilon$ | Small strain tensor and its trace, $\varepsilon \equiv \overline{g}^{ij}\varepsilon_{ij}$ in three dimensions. |
| $R_{\mu\nu},\ R$ | The four-dimensional Ricci curvature tensor and scalar, $R\equiv g^{\mu\nu}R_{\mu\nu}$. |
| $R_{ij}^{\mathrm{3D}},\ R^{\mathrm{3D}}$ | The three-dimensional Ricci curvature tensor and scalar, $R^{\mathrm{3D}}\equiv g^{ij}R_{ij}^{\mathrm{3D}}$. |
| $T_{\mu\nu},\ T$ | The stress-energy tensor of General Relativity and its trace, $T\equiv g^{\mu\nu}T_{\mu\nu}$. |

Furthermore, the following notational conventions will be used: Lower case Latin indexes, $i,j,k,l = 1\ldots3$, run over the three ordinary spatial dimensions. Upper case Latin indexes, $I,J,K,L = 1\ldots4$, run over the four hyperspace dimensions, while Greek indexes, $\mu,\nu,\alpha,\beta = 0\ldots3$, run over the four spacetime dimensions, where indexes $0$ and $4$ represent, respectively, the time dimension and the extra spatial dimension. Sometimes, we will use $t$ to denote coordinate time such that $x^0 \equiv ct$, where $c$ is the speed of light. For spacetime, we adopt the space-like metric signature $(-,+,+,+)$ and denote the flat (Minkowskian) metric tensor as $\eta_{\mu\nu}$, where $[\eta_{\mu\nu}] \equiv \mathrm{diag}[-1,1,1,1]$.

Except when explicitly stated otherwise, we will use the Einstein summation convention for repeated indexes. Thus, when two quantities appear in the same term with a repeated index, we understand that they represent the sum of multiple terms over that index. For example, $A_{ij} B^{jk} \equiv \sum_{i = 1\ldots 3} A_{ij} B^{jk}$. Note that the range $i,j = 1\ldots 3$ is implied by the use of lower case Latin indexes. Also, the pair of repeated indexes over which the summation is performed will be in opposite position, top (contravariant) and bottom (covariant) or vice versa.

---

## Errata

This Markdown edition corrects a small number of errors present in the published version of record (ProQuest No. 10978458): a few typographical slips and two factor-of-two coefficient errors. Every correction is confined to notation and to coefficients appearing in *preview/summary* statements; the detailed derivations in the body already produce the corrected values, so no derivation, result, or physical conclusion is affected. Each entry gives the form as printed in the published version and the corrected form used here.

| Location | Published version | Corrected here | Reason |
|---|---|---|---|
| Ch. I, preview of the SM Lagrangian | $\mathcal{L} = RL^2\mu/(24c)$ | $\mathcal{L} = RL^2\mu/(12c)$ | Factor-of-two slip. With $\mu = Y/4$ this coefficient is $\frac{\mu L^2}{24}$, half of the derived $\frac{\mu L^2}{12} = \frac{YL^2}{48} = \frac{1}{2\kappa}$ (Eqs. 3.18, 3.25). The corrected form also matches the elastic modulus $Y \sim 24/(l_p^2\kappa)$ of Eq. (3.29). |
| Eq. (3.1), Eq. (3.24), and the paragraph opening *Formulation of the Cosmic Fabric Model of Gravity* | coefficient $\frac{YL}{48}$ | $\frac{YL^2}{48}$ | The exponent on the fabric thickness $L$ was dropped. The Lagrangian density derived in Eq. (3.23) and the identification $\frac{YL^2}{48} = \frac{1}{2\kappa}$ in Eq. (3.25) both carry $L^2$, and the analogy $\mathcal{S}_ \text{F} = \mathcal{S}_ \text{EH}$ with the Einstein–Hilbert action requires it. |
| Table 3.1, Solid Mechanics action cell | $\mathcal{S} = \frac{L^2 Y}{24}\int R\sqrt{\ldots}\ d^4x$ | $\mathcal{S} = \frac{L^2 Y}{48}\int R\sqrt{\ldots}\ d^4x$ | Factor-of-two slip in the opposite direction. Equals $\frac{1}{2\kappa}$ per Eq. (3.25); the table's own elastic-constant entry $Y = \frac{6c^7}{2\pi\hbar G^2}$ is consistent only with the $\frac{L^2Y}{48}$ coefficient. |
| Eq. (4.5) | $d\tau' = dt\sqrt{1-\beta^2}$ | $d\tau' = d\tau\sqrt{1-\beta^2}$ | The quantity being time-dilated is the stationary observer's round-trip proper time $d\tau$ from Eq. (4.4), per the dilation relation Eq. (4.3). No coordinate time $t$ is defined in this derivation. |
| Eq. (5.37) | $ds = g_{tt}c^2dt^2 + \ldots$ | $ds^2 = g_{tt}c^2dt^2 + \ldots$ | The left-hand side is the squared line element; the right-hand side is written in squared differentials. |
| Eq. (5.41), hoop term | $\left(1 + 2\varepsilon_\Omega\right)d\overline{r}^2\  d\Omega^2$ | $\left(1 + 2\varepsilon_\Omega\right)\overline{r}^2\  d\Omega^2$ | Matches the $g_{\Omega\Omega}\overline{r}^2 d\Omega^2$ term of Eq. (5.37); the hoop term carries $\overline{r}^2$, not $d\overline{r}^2$. |
| Eq. (5.53), exterior line | $\ldots + r^2 d\Omega$ | $\ldots + r^2 d\Omega^2$ | Matches the interior line and the definition $d\Omega^2 \equiv d\theta^2 + \sin^2\theta\  d\varphi^2$. |
| Eq. (6.12), first line | $\overline{\Gamma}^1_{11} = \dfrac{\overline{l}'\ \overline{l}''}{(l)^2}$ | $\overline{\Gamma}^1_{11} = \dfrac{\overline{l}'\ \overline{l}''}{(\overline{l}')^2}$ | Consistent with $\overline{\Gamma}^1_{11} = \tfrac{1}{2}\overline{g}^{11}\partial_1\overline{g}_ {11}$ and $\overline{g}^{11} = (\overline{l}')^{-2}$, and with the two sibling lines of the same equation. |
| Ch. VII, `wfunMOND` code listing | `r = sqsrt(x{1}.^2 + x{2}.^2 + x{3}.^3)` | `r = sqrt(x{1}.^2 + x{2}.^2 + x{3}.^2)` | Slips in the reproduced MATLAB code: the function name is `sqrt`, and the radial distance is $r=\sqrt{x_1^2+x_2^2+x_3^2}$ (the third term's exponent is 2, not 3). |

The published version also contains the misprints below, which this edition leaves as printed. They repeat slips of the journal papers on which Chapters I and III–V are based. Each entry gives the form as printed and the form it should take.

| Location | Published version | Should read | Reason |
|---|---|---|---|
| Ch. I, section *Recent Research Relating Mechanics and Relativity* | $\nu = \frac{\lambda}{2(\lambda -\mu)}$ | $\nu = \frac{\lambda}{2(\lambda + \mu)}$ | This is the standard relation between the Poisson ratio and the Lamé parameters. With $\lambda = -1$ and $\mu = \frac{1}{2}$ it gives $\nu = 1$, as the sentence states, while the printed form gives $\nu = \frac{1}{3}$. |
| Eq. (3.16) | $U_\text{B} = L^2C^{ijkl}\left[b_{ij}b_{kl} + \mathcal{O}(b^3 L)\right]$ | $U_\text{B} = \frac{L^2}{24}C^{ijkl}\left[b_{ij}b_{kl} + \mathcal{O}(b^3 L)\right]$ | With $\varepsilon_{ij}^\text{B} = -b_{ij}\xi$, Eq. (3.15) gives the factor $\frac{1}{2L}\int_{-L/2}^{L/2}\xi^2\ \mathrm{d}\xi = \frac{L^2}{24}$. Eqs. (3.17) and (3.18) include it. |
| Eq. (3.17) | $U_\text{B} = -\frac{L^2 Y}{24(1+\nu)} \left(R^\text{3D} + \frac{1-\nu}{1-2\nu} b^i_i b^k_k\right)$ | $U_\text{B} = -\frac{L^2 Y}{24(1+\nu)} \left(R^\text{3D} - \frac{1-\nu}{1-2\nu} b^i_i b^k_k\right)$ | With $R^\text{3D} = b^i_i b^k_k - b^k_j b^j_k$, Hooke's Law (1.2) gives $C^{ijkl}b_{ij}b_{kl} = \frac{Y}{1+\nu}\left(\frac{1-\nu}{1-2\nu}b^i_i b^k_k - R^\text{3D}\right)$. The term vanishes at $\nu = 1$, so Eq. (3.18) is unaffected. |
| Eq. (3.30) | $\rho_\text{F} \sim 1.3 \times 10^{96}\ \mathrm{kg}\ \mathrm{m}^{-3}$ | $\rho_\text{F} \sim 1.23 \times 10^{96}\ \mathrm{kg}\ \mathrm{m}^{-3}$ | With $Y$ from Eq. (3.29), $\rho_\text{F} = Y/4c^2 = 3c^5/4\pi\hbar G^2 = 1.23 \times 10^{96}\ \mathrm{kg}\ \mathrm{m}^{-3}$. |
| Eq. (4.11) | $a_{12} = a_{21} = -\beta = -v/c$ | $a_{12} = a_{21} = -\gamma\beta = -\gamma v/c$ | Eq. (4.9) gives the off-diagonal coefficients as $-\gamma\beta$, as the Lorentz transformation requires. |
| Eq. (5.51) | $\max(r_s) \sim 3.713\times 10^{-35}\ \text{m}$ and $\max(M) \sim 2.500\times 10^{-8}\ \text{kg}$ | $\max(r_s) \sim 4.61\times 10^{-35}\ \text{m}$ and $\max(M) \sim 3.1\times 10^{-8}\ \text{kg}$ | Eq. (5.49) with $L = 5.729\times 10^{-35}\ \text{m}$ from Eq. (5.50) gives $\sqrt{35/54}\ L = 4.61\times 10^{-35}\ \text{m}$. The printed value is $(35/54)L$. The mass follows as $\max(r_s)c^2/2G$. |
| Eq. (5.55), exterior entries | $\overline{r}_ \text{ext} = \left(1 - \frac{r_s r_0^2}{10r^3}\right)r$ and $d\overline{r}_ \text{ext} = \left(1 + \frac{r_s r_0^2}{5r^3}\right)dr$ | $\overline{r}_ \text{ext} = \left(1 - \frac{r_s r_g^2}{10r^3}\right)r$ and $d\overline{r}_ \text{ext} = \left(1 + \frac{r_s r_g^2}{5r^3}\right)dr$ | These follow from Eq. (5.54) with $e_\text{ext} = r_s r_g^2/10\overline{r}^3$ from Eq. (5.36). Only with $r_s r_g^2$ does substituting Eq. (5.55) into Eq. (5.40) give Eq. (5.53). |

The published version also contains the following errors of argument, which this edition leaves as printed.

| Location | Error |
|---|---|
| Ch. III, section *Gravitational Waves*, Eqs. (3.31)–(3.38) | With the time–space components set to zero, the harmonic condition of Eq. (3.32), $\partial_k \varepsilon_{ik} = 0$, leaves no shear wave. For any displacement, $2\partial_k \varepsilon_{ik} = \nabla^2 u_i + \partial_{ik} u_k$, so at $\partial_k u_k = 0$ the condition requires $\nabla^2 u_i = 0$. Eq. (3.37) then gives $\partial^2 u_i/\partial t^2 = 0$. The bracket of Eq. (3.31), which the text sets to zero as torsion, is the rotation of the material, and a shear wave is a wave of rotation. Eq. (3.38) also holds only on one axis. No field of material displacements gives its strain throughout a region, since that strain violates the compatibility condition $\partial_{33}\varepsilon_{11} + \partial_{11}\varepsilon_{33} = 2\partial_{13}\varepsilon_{13}$. The displacement $u_1 = \frac{1}{2}hx^1\cos k(x^3 - ct)$, $u_2 = -\frac{1}{2}hx^2\cos k(x^3 - ct)$ gives $\varepsilon_{11} = -\varepsilon_{22}$, but its $\varepsilon_{13}$ and $\varepsilon_{23}$ grow in proportion to $x^1$ and $x^2$ and vanish only on the axis $x^1 = x^2 = 0$. |
| Ch. V, Eqs. (5.17)–(5.19) | The step from the principle of least action to the requirement that the total energy $W$ of Eq. (5.17) vanish is not variational. An extremum of the action requires the first variation of $W$ with respect to $e$ and $w$ to vanish, not $W$ itself. $W$ can also be negative: $U_\text{B} = -R^\text{3D}/2\kappa$ is negative inside the body, and Eq. (5.46) gives $W_\text{M} < 0$. The solution of the chapter is also not stationary for $W$. At small strain $\int U_\text{B}\ dx^3$ reduces to a boundary term, so the variation of $W$ comes from $W_\text{M}$ alone. Eq. (5.45) gives $W_\text{M} = -4\pi Y\int ue\overline{r}^2\ d\overline{r}$, whose variation with respect to $e$ is $-4\pi Yu\overline{r}^2$. This vanishes only where the fabric does not bend. Eq. (5.19) itself agrees with the constraint equation of General Relativity for a static body, $R^\text{3D} = 2\kappa c^2\rho$. |
| Ch. VI, section *Comparison with Modified Newtonian Dynamics (MOND)*, Eqs. (6.29)–(6.34) | The equivalence with MOND holds for the acceleration of a body at rest, not for rotation speeds. In the metric of Eq. (6.8), the circle at coordinate radius $\overline{r}$ has geodesic curvature $1/(\overline{r}\ \overline{l}')$, so the geodesic equation (6.13) gives a circular orbit the speed $v^2 = \overline{r}\ \overline{l}'\ \lvert a\rvert$. With $a = -GM/\overline{r}^2$ from Eq. (6.23) and the profile of Eq. (6.32), $\overline{l}' \to 2\overline{r}/s$ far from the center, and the flat speed satisfies $v^4 = 4GMa_0$. MOND gives $v^4 = GMa_0$, so the profile of Eq. (6.34) gives twice MOND's $v^2$. |
| Ch. VII, Eq. (7.28) | The formula drops the term $-\overline{\Gamma}^k_{\ ij}v^iv^j$ of Eq. (7.20) on the ground that rotation speeds are much less than $c$. That term is of order $v^2/\overline{r}$, not $v^2/c^2$. For the profile of Eq. (6.34), it is the fraction $1 - 1/(\overline{l}')^2$ of the centripetal acceleration, about 0.75 at $10\ \text{kpc}$ for the scale mass $M = 10^{11} M_\odot$ of Figure 7.5. With the term kept, a circular orbit at coordinate radius $\overline{r}$ has $v^2 = c^2\overline{r}\ \lvert\partial_1\varepsilon\rvert$. Applied as printed, Eq. (7.28) gives speeds that fall with radius beyond most of the galaxy's mass, so the rising curve for M33 in Figure 7.5 cannot be reproduced from the printed formulas. |

---
