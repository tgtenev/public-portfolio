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
| $\hbar$ | The reduced Planck constant, $\hbar = 1.054571800\times 10^{-34}\ \mathrm{m}^2\,\mathrm{kg}\,\mathrm{s}^{-1}$. |
| $G$ | The gravitational constant, $G = 6.67408\times 10^{-11}\ \mathrm{m}^3\,\mathrm{kg}^{-1}\mathrm{s}^{-2}$. |
| $c$ | Speed of light, $c = 299{,}792{,}458\ \mathrm{m\,s}^{-1}$. |
| $\kappa$ | The Einstein constant, $\kappa \equiv 8\pi G / c^4$. |
| $\partial_{a},\ \partial_{ab}$ | Partial derivatives, $\partial_{a}\equiv\partial/\partial x_{a}$, and $\partial_{ab}\equiv\partial/\partial x_{a}\partial x_{b}$. |
| $\nabla^{2}$ | The Laplace operator for spatial coordinates, $\nabla^{2}\equiv\partial_{11}+\partial_{22}+\partial_{33}$. |
| $\delta_{b}^{a}$ | Kronecker delta: $\delta_{a}^{b}=\delta_{ab}=\delta^{ab}=\{1,\ a=b;\ 0,\ a\neq b\}$. |
| $g_{ij}$ | The three-dimensional metric tensor. |
| $\overline{g}_{ij}$ | The three-dimensional undeformed metric tensor. In general, a bar decoration indicates that a quantity pertains to the undeformed configuration. |
| $g_{\mu\nu},\ g$ | The spacetime metric and its determinant, $g \equiv \det g_{\mu\nu}$. |
| $\eta_{\mu\nu}$ | The Minkowski metric for flat spacetime, $\eta_{00}=-1,\ \eta_{0i}=\eta_{i0}=0,\ \eta_{ij}=\delta_{ij}$. |
| $\varepsilon_{ij},\ \varepsilon$ | Small strain tensor and its trace, $\varepsilon \equiv \overline{g}^{ij}\varepsilon_{ij}$ in three dimensions. |
| $R_{\mu\nu},\ R$ | The four-dimensional Ricci curvature tensor and scalar, $R\equiv g^{\mu\nu}R_{\mu\nu}$. |
| $R_{ij}^{\mathrm{3D}},\ R^{\mathrm{3D}}$ | The three-dimensional Ricci curvature tensor and scalar, $R^{\mathrm{3D}}\equiv g^{ij}R_{ij}^{\mathrm{3D}}$. |
| $T_{\mu\nu},\ T$ | The stress-energy tensor of General Relativity and its trace, $T\equiv g^{\mu\nu}T_{\mu\nu}$. |

Furthermore, the following notational conventions will be used: Lower case Latin indexes, $i,j,k,l = 1\ldots3$, run over the three ordinary spatial dimensions. Upper case Latin indexes, $I,J,K,L = 1\ldots4$, run over the four hyperspace dimensions, while Greek indexes, $\mu,\nu,\alpha,\beta = 0\ldots3$, run over the four spacetime dimensions, where indexes $0$ and $4$ represent, respectively, the time dimension and the extra spatial dimension. Sometimes, we will use $t$ to denote coordinate time such that $x^0 \equiv ct$, where $c$ is the speed of light. For spacetime, we adopt the space-like metric signature $(-,+,+,+)$ and denote the flat (Minkowskian) metric tensor as $\eta_{\mu\nu}$, where $[\eta_{\mu\nu}] \equiv \operatorname{diag}[-1,1,1,1]$.

Except when explicitly stated otherwise, we will use the Einstein summation convention for repeated indexes. Thus, when two quantities appear in the same term with a repeated index, we understand that they represent the sum of multiple terms over that index. For example, $A_{ij} B^{jk} \equiv \sum_{i = 1\ldots 3} A_{ij} B^{jk}$. Note that the range $i,j = 1\ldots 3$ is implied by the use of lower case Latin indexes. Also, the pair of repeated indexes over which the summation is performed will be in opposite position, top (contravariant) and bottom (covariant) or vice versa.

---

## Errata

This Markdown edition corrects a small number of errors present in the published version of record (ProQuest No. 10978458): a few typographical slips and two factor-of-two coefficient errors. Every correction is confined to notation and to coefficients appearing in *preview/summary* statements; the detailed derivations in the body already produce the corrected values, so no derivation, result, or physical conclusion is affected. Each entry gives the form as printed in the published version and the corrected form used here.

| Location | Published version | Corrected here | Reason |
|---|---|---|---|
| Ch. I, preview of the SM Lagrangian | $\mathcal{L} = RL^2\mu/(24c)$ | $\mathcal{L} = RL^2\mu/(12c)$ | Factor-of-two slip. With $\mu = Y/4$ this coefficient is $\frac{\mu L^2}{24}$, half of the derived $\frac{\mu L^2}{12} = \frac{YL^2}{48} = \frac{1}{2\kappa}$ (Eqs. 3.18, 3.25). The corrected form also matches the elastic modulus $Y \sim 24/(l_p^2\kappa)$ of Eq. (3.29). |
| Eq. (3.1), Eq. (3.24), and the paragraph opening *Formulation of the Cosmic Fabric Model of Gravity* | coefficient $\frac{YL}{48}$ | $\frac{YL^2}{48}$ | The exponent on the fabric thickness $L$ was dropped. The Lagrangian density derived in Eq. (3.23) and the identification $\frac{YL^2}{48} = \frac{1}{2\kappa}$ in Eq. (3.25) both carry $L^2$, and the analogy $\mathcal{S}_\text{F} = \mathcal{S}_\text{EH}$ with the Einstein–Hilbert action requires it. |
| Table 3.1, Solid Mechanics action cell | $\mathcal{S} = \frac{L^2 Y}{24}\int R\sqrt{\ldots}\,d^4x$ | $\mathcal{S} = \frac{L^2 Y}{48}\int R\sqrt{\ldots}\,d^4x$ | Factor-of-two slip in the opposite direction. Equals $\frac{1}{2\kappa}$ per Eq. (3.25); the table's own elastic-constant entry $Y = \frac{6c^7}{2\pi\hbar G^2}$ is consistent only with the $\frac{L^2Y}{48}$ coefficient. |
| Eq. (4.5) | $d\tau' = dt\sqrt{1-\beta^2}$ | $d\tau' = d\tau\sqrt{1-\beta^2}$ | The quantity being time-dilated is the stationary observer's round-trip proper time $d\tau$ from Eq. (4.4), per the dilation relation Eq. (4.3). No coordinate time $t$ is defined in this derivation. |
| Eq. (5.37) | $ds = g_{tt}c^2dt^2 + \ldots$ | $ds^2 = g_{tt}c^2dt^2 + \ldots$ | The left-hand side is the squared line element; the right-hand side is written in squared differentials. |
| Eq. (5.41), hoop term | $\left(1 + 2\varepsilon_\Omega\right)d\overline{r}^2\, d\Omega^2$ | $\left(1 + 2\varepsilon_\Omega\right)\overline{r}^2\, d\Omega^2$ | Matches the $g_{\Omega\Omega}\overline{r}^2 d\Omega^2$ term of Eq. (5.37); the hoop term carries $\overline{r}^2$, not $d\overline{r}^2$. |
| Eq. (5.53), exterior line | $\ldots + r^2 d\Omega$ | $\ldots + r^2 d\Omega^2$ | Matches the interior line and the definition $d\Omega^2 \equiv d\theta^2 + \sin^2\theta\, d\varphi^2$. |
| Eq. (6.12), first line | $\overline{\Gamma}^1_{11} = \dfrac{\overline{l}'\,\overline{l}''}{(l)^2}$ | $\overline{\Gamma}^1_{11} = \dfrac{\overline{l}'\,\overline{l}''}{(\overline{l}')^2}$ | Consistent with $\overline{\Gamma}^1_{11} = \tfrac{1}{2}\overline{g}^{11}\partial_1\overline{g}_{11}$ and $\overline{g}^{11} = (\overline{l}')^{-2}$, and with the two sibling lines of the same equation. |
| Ch. VII, `wfunMOND` code listing | `r = sqsrt(x{1}.^2 + x{2}.^2 + x{3}.^3)` | `r = sqrt(x{1}.^2 + x{2}.^2 + x{3}.^2)` | Slips in the reproduced MATLAB code: the function name is `sqrt`, and the radial distance is $r=\sqrt{x_1^2+x_2^2+x_3^2}$ (the third term's exponent is 2, not 3). |

---

## I. Introduction

In this dissertation work, we investigate the two-part proposition that: 1) physical space exhibits material-like properties and, that 2) having material nature, physical space has inherent structure at multiple length scales, which affects its behavior. The first part of the proposition underlies what we call the "Cosmic Fabric Model" of gravity. The second part of the proposition, which we call the "Inherent Structure Hypothesis," offers a new approach for solving conundrums of modern cosmology, such as explaining phenomena currently attributed to dark matter. We also show how the Cosmic Fabric model of gravity makes the computational tools of modern mechanics applicable to studying the inherent structure of cosmic space. Much of the work presented here is based on the publications by Tenev and Horstemeyer [160, 161], which introduced the Cosmic Fabric Model of gravity and began to illustrate its application to studying the inherent structure of space.

The Cosmic Fabric model is a formal analogy between General Relativity (GR) and Solid Mechanics (SM) that interprets physical space as a solid body and the field equations of GR as the bending equations governing the dynamics of said body. The vacuum of three-dimensional space is identified with a solid hyperplate called "cosmic fabric" that is embedded in a four-dimensional hyperspace and has a small thickness along the fourth hyperspatial dimension. The fabric deforms elastically due to matter inclusions, such that its intrinsic curvature corresponds to that of space, while its volumetric strain to the reduction in the rate of time lapse, which in the case of weak gravity, is the same as the gravitational potential.

In the context of the Lagrangian formulation of gravity, the inherent structure of space figures as the additional term $\overline{\mathcal{L}}$ in the following modification to the Einstein–Hilbert action integral,

$$
\begin{split}
\mathcal{S} = \int_{\Omega}\left(\mathcal{L} - \overline{\mathcal{L}} + \mathcal{L}_\text{M} \right) d\Omega
\end{split}
\tag{1.1}
$$

where the integral is taken over all of spacetime $\Omega$ and $d\Omega \equiv \sqrt{|g|}\,dx^4$ represents the proper volume element of spacetime with $g$ being its metric and $dx^4$ the coordinate volume element. The various $\mathcal{L}$ terms are Lagrangian densities, where $\mathcal{L}$ is due to the curvature of spacetime, $\overline{\mathcal{L}}$ is a correction to $\mathcal{L}$ due to the inherent (or undeformed) curvature of space, and $\mathcal{L}_\text{M}$ accounts for energy–matter fields. The governing differential equations of spacetime (or the cosmic fabric) can be derived by variation of the action $\mathcal{S}$ with respect to the metric tensor $g$. From GR's perspective, $\mathcal{L} = R/(2c\kappa)$, where $R$ is the Ricci curvature scalar, $\kappa \equiv 8\pi G/c^4$ is the Einstein constant, $c$ is the speed of light, and $G$ is the gravitational constant. We show in Chapter III that from SM's perspective, $\mathcal{L} = RL^2\mu/(12c)$, where $L$ and $\mu$ are, respectively, the average thickness and shear modulus of the cosmic fabric. The interpretation of $\mathcal{L}_\text{M}$ is one and the same within both GR's and SM's paradigms. The term $\overline{\mathcal{L}}$, which represents the curvature of spacetime that is not due to matter–energy fields, has not been considered until now, but the need for it becomes apparent in the context of the material analogy. The unstrained cosmic fabric need not be flat, but could, for example, have global curvature and local relief, which is what we mean by "inherent structure." Chapters III–V show that without accounting for the $\overline{\mathcal{L}}$ term, the Cosmic Fabric model is analogous to conventional General Relativity, whereas the introduction of inherent curvature, which is discussed in Chapters VI–VII, represents a modification to GR at galactic length scales and above.

In the following sections, we introduce the relevant prior art that has motivated and led to the ideas presented in the later chapters.

### Early Material Models of Cosmic Space

The early material models of space, commonly known as aether theories, have played an indispensable role in our understanding the nature of space. The notion of an aether has been thought about from different perspectives over time, probably initially by Aristotle [140], who considered it to be the fifth element comprising the heavenly spheres and bodies. For some time after Aristotle, the aether was viewed as a fluid. For example, although Newton [71] described aether as "capable of contraction and dilatation, strongly elastic," which makes one think that he was alluding to a solid aether, he also discussed [72] a universal fluid aether filling the cosmos at the largest length scale but a dynamic short-range interaction of aether and matter at the smallest length scales. It was aether whose multiple functions admitted transmitted forces to produce the phenomena in the universe that we see, including gravitation. Later, Laplace [84, 85] furthered the thought that gravity propagated through a liquid aether that had a lower length scale basis from molecules. Fresnel [57] proposed that aether was partially entrained by matter, but Stokes [155] argued that such entrainment was complete. Kelvin [78] described the aether at the smallest length scales as vortex atoms comprising a frictionless, elastic material with "the hypothesis that space is continuously occupied by an incompressible frictionless liquid acted on by no force, and that material phenomena of every kind depend solely on motions created in this liquid." They argued that electromagnetism had to be based on a mechanical notion like that of aether. Maxwell [104, 105] used the idea of an aether to build the theory of electromagnetic phenomena. Lodge [92, 93] presented mechanical Lagrangian models to illustrate the aether's phenomenological effects.

The Lorentz Aether Theory (LET) [96, 97, 98] was the culmination of earlier material models of space. Based on Lodge's work [92, 93], Lorentz [94, 95, 96, 97, 98, 114] developed an electron–aether theory where matter (electrons) and aether were different entities in which the aether was completely motionless. This stationary configuration would not be in motion close to matter. By contrast to earlier electron models, the electromagnetic field of the aether appears as a mediator between the electrons, so a signal cannot propagate faster than the speed of light. The basic concept of Lorentz's theory [98] was the "theorem of corresponding states" in which an observer moving relative to the aether makes equivalent observations as a stationary observer. Lorentz [97] changed the space–time variables between one reference frame and another, and introduced concepts like a physical length contraction and a local time to explain the Michelson and Morley work [111, 112, 113], which had shown that the stationary reference frame of the aether was undetectable. Lorentz [95, 96] and Larmor [86, 87] discussed that the notion of a local time is accompanied by a time dilation of matter moving in the aether. In other words, there is an elastic aether strain [87] that arises when electrons (matter) are present. Larmor [87] tried to view aether in the context of different length scales: electrons, atoms, molecules, and cosmos. Lorentz later noted [94, 114] that he considered a clock stationary in the aether gave the "true" time, while local time was thought of as a working hypothesis with a dynamical mathematical backing. Therefore, Lorentz's theorem is viewed by modern authors as being a mathematical transformation from a "real" stationary reference frame in the aether into a dynamic "fictitious" configuration.

### Relativity and the Material View of Space

Initially, the Theory of Special Relativity [48] appeared to have supplanted the material view of space, not because the latter was flawed, but because it seemed no longer needed. However, the more complete understanding came later when General Relativity [50] reinstated the relevance of attributing material-like nature to space. Poincaré [132, 133, 134] had already introduced the Principle of Relativity in the context of Lorentz's work and declared it as a general law of nature, including gravitation, as he corrected some of Lorentz's mistakes and proved the Lorentz covariance of the electromagnetic equations. He included aether as an undetectable medium that distinguished between apparent and real time. Shortly thereafter, Einstein [48] proposed the Special Theory of Relativity in which aether was not necessary, and Dirac [42] claimed that aether was "abandoned" because of Einstein [48]. However, Einstein [49] later came back and discussed the necessity of an aether in the context of the General Theory of Relativity [50]. Lorentz wrote a letter to Einstein in which he speculated that within General Relativity the aether was re-introduced. In his response Einstein wrote that one can in fact speak about a new stationary aether but not a dynamic aether [47, 51, 52]. In a lecture, which Einstein [49] was invited to give at Lorentz's university in Leiden, Einstein sought to reconcile the theory of relativity with Lorentzian aether. In this lecture Einstein stressed that special relativity does not rule out the aether:

> "To deny the aether is ultimately to assume that empty space has no physical qualities whatever. The fundamental facts of mechanics do not harmonize with this view. For the mechanical behaviour of a corporeal system hovering freely in empty space depends not only on relative positions (distances) and relative velocities, but also on its state of rotation, which physically may be taken as a characteristic not appertaining to the system in itself. In order to be able to look upon the rotation of the system, at least formally, as something real, Newton's objective space. Since he classes his absolute space together with real things, for him rotation relative to an absolute space is also something real. Newton might no less well have called his absolute space 'Aether'; what is essential is merely that besides observable objects, another thing, which is not perceptible, must be looked upon as real, to enable acceleration or rotation to be looked upon as something real."

Although Einstein did eventually affirm the validity of the material view of space, Special Relativity (SR) remained dominant by a wide margin in part because its generalization, that is General Relativity (GR), explained gravitational phenomena better than the Lorentz Aether Theory (LET), which was the state-of-the-art aether theory at the time. In addition, the Principle of Relativity, which is the cornerstone of SR and GR, brought about the unification of space and time into a mathematically elegant spacetime continuum. Nevertheless, the need to separate space from time, such as in the Arnowitt–Deser–Misner (ADM) [13, 14] formalism of General Relativity, remained indispensable for GR's practical applications. Although the ADM formalism is not a material model per se, the need for such a formulation points to the continual relevance of a material model of gravity. Such a model, as is LET or the Cosmic Fabric model introduced herein, necessarily separates space from time, because space is viewed as a material object progressing in time.

The possible confluence between Hooke's Law and Einstein's Gravitational Law motivated the material analogy of space that is explored here. In 1678, Robert Hooke, a contemporary of Isaac Newton, published what later became known as Hooke's Law [66]. In 1827, Cauchy [5] advanced Hooke's Law by defining the tensorial formulation of stress. For an isotropic linear elastic material, Hooke's Law states in tensorial form that,

$$
\begin{split}
\sigma^{kl} = \frac{Y}{1+\nu} \left(\frac{\nu}{1-2\nu} g^{ij}g^{kl} + g^{ik}g^{jl}\right)\varepsilon_{ij}
\end{split}
\tag{1.2}
$$

where $\sigma^{kl}$, $\varepsilon_{ij}$, and $g^{ij}$ are the stress, strain, and the metric tensors, respectively, $Y$ is Young's elastic modulus, and $\nu$ is the Poisson's ratio. Latin indexes, $i,j,k,l = 1 \ldots 3$, run over the three spatial dimensions, and the Einstein summation convention is employed. In 1916, Einstein published the field equations of General Relativity [50], which can be written as,

$$
\begin{split}
T_{\mu\nu} = \frac{1}{\kappa} \left(R_{\mu\nu} - \frac{1}{2}R g_{\mu\nu} \right)
\end{split}
\tag{1.3}
$$

where $T_{\mu\nu}$, $R_{\mu\nu}$, and $g_{\mu\nu}$ are the stress-energy tensor, Ricci curvature tensor, and spacetime metric tensor, respectively; $R \equiv R^\mu_\mu$ is the Ricci scalar, $\kappa \equiv 8\pi G/c^4$ is the Einstein constant as $c$ and $G$ are the speed of light and gravitational constant, respectively. Greek indexes, $\mu,\nu = 0 \ldots 3$, run over the four dimensions of spacetime with the $0^{\text{th}}$ dimension representing time. For the purposes of this dissertation work, we have omitted the Cosmological Constant, which is sometimes included in Equation (1.3), because its value is negligible for length scales below the size of the observable universe. Einstein's Gravitational Law (1.3) suggests a material-like constitutive relation, similar to Hooke's Law (1.2), because it relates stress, on the left-hand side, to deformation on the right-hand side. At first glance, the similarity appears imperfect because the right-hand sides differ in dimensionality: whereas the strain term, $\varepsilon_{ij}$, is dimensionless, the curvature terms, $R_{\mu\nu}$ and $R$, have dimensions of $\text{Length}^{-2}$. However, we resolve this problem by considering bending deformation instead of just straightforward stretch, contraction, or shear deformation. In the equations for bending, stress is proportional to the second spatial derivative of strain.

### Recent Research Relating Mechanics and Relativity

After Einstein's publication of General Relativity [50], a number of researchers have investigated the relationship between Mechanics notions and General Relativity.

One category of publications dealt with generalizing the equations of Solid Mechanics to account for relativistic effects. Synge [157] formulated a constitutive relationship in relativistic settings. Rayner [139] extended Hooke's Law to a relativistic context. Maugin [103] generalized the special relativistic continuum mechanics theory developed by Grot and Eringen [62] to a general relativistic context. More recently, Kijowski and Magli [79] presented the relativistic elasticity theory as a gauge theory. A detailed review of relativistic elasticity can be found in Karlovini and Samuelsson [77].

Another category of publications interprets General Relativity in Solid Mechanical terms. Kondo [82] mentions an analogy between the variation formalism of his theory of global plasticity and General Relativity. Gerlach and Scott [59] introduce a "metric elasticity" tensor in addition to the elasticity of matter itself and "stresses due to geometry." However, these stress and strain terms are not a constitutive model of gravity, because they are not expected to apply in the absence of ordinary matter. Tartaglia [158] attempted to describe spacetime as a four-dimensional elastic medium in which one of the spatial dimensions has been converted into a time dimension by assuming a uniaxial strain. However, many of the ideas in Tartaglia's paper appear to be incomplete. Antoci and Mihich [12] explored the physical meaning of the straightforward formal extension of Hooke's Law to spacetime, but did not consider the possibility, which is explored in this dissertation work, that Einstein's Gravitational Law may be related to Hooke's Law. Padmanabhan [128] treated spacetime as an elastic solid and used entropy consideration to arrive at the Field Equations (1.3), but unlike the work presented here, he was not concerned with developing the correspondence between the gravitational properties of cosmic space and the mechanical attributes of said solid, such as its strain and elastic modulus. Beau [20] pushed the material analogy further by interpreting the cosmological constant $\Lambda$ as related to a kind of a spacetime bulk modulus, but the analogy is to a fluid-like material and not a solid. A set of recent publications, for which Rangamani [138] presents a literature review, explore the applicability of the Navier–Stokes equations of Fluid Dynamics to gravity. While a fluid analogy is useful for some applications, it does not account for shear waves in space, such as gravity waves, because fluids are only capable of propagating pressure waves and not shear waves. Unlike the prior literature recounted above, the work presented here begins with the premise that space exhibits material-like behavior subject to a constitutive relationship that can be expressed in terms of Hooke's Law (1.2).

Very recently, Hehl and Kiefer [64] related the three-dimensional DeWitt Metric [40] with Hooke's Law [66] using the elastic constants as a fourth-rank tensor, which was based on the work of Marsden and Hughes [100]. Also, in relation to dark matter, Böhmer et al. [25] modified the General Theory of Relativity by using anisotropic continuum mechanics. In agreement with our results, but derived via independent means, Hehl and Kiefer determined that the first and second Lamé parameters of the cosmic material must be $\lambda = -1$ and $\mu = \frac{1}{2}$, respectively, for some appropriately chosen units, which is equivalent to stating that the Poisson ratio $\nu$ is unity, since $\nu = \frac{\lambda}{2(\lambda -\mu)}$. Nevertheless, a critical insight of our work, which has not been mentioned in any publication so far, is relating Einstein's Gravitational Law (1.3) to the bending deformation of a material plate as opposed to straightforward longitudinal or shear type of deformation. Without this insight, the detailed correspondence between physical space and a material medium remains largely obscured, thus limiting the practical applications of the material analogy.

### The Hierarchical Length Scale Structure of Space

The notion of inherent structure must be clarified in the context of the notion of length scale, because there can be diverse kinds of structures depending on the length scale. By "length scale" we understand a specific range of distances for which certain physical parameters and laws dominate, while others are of lesser significance. For our purpose, we consider the following four length scales: substructure ($10^{-36} - 10^{-10}\,\text{m}$), continuum ($10^{-10} - 10^{14}\,\text{m}$), structure ($10^{14}-3\times 10^{24}\,\text{m}$), and cosmic ($3 \times 10^{24} - 10^{27}\,\text{m}$) length scales (see Figure 1.1). The specific ranges are indicated for the sake of concreteness, but are not intended to be precise. By analogy, the substructure length scale in a conventional material corresponds to the discrete entities comprising the material. Chapters IV and V discuss briefly the ramification of physical space having substructure. A more extensive treatment is a subject of subatomic physics and is beyond the scope of this dissertation work. At continuum length scale, as the name suggests, physical space is treated as a differentiable manifold. General Relativity is strictly a continuum scale theory, and at this length scale, the Cosmic Fabric model (Chapters III–V) yields equivalent results with it. The structure length scale in a conventional material describes the components of which a mechanical system is built, such as the trusses in a bridge, for example. The behavior of these components depends not only on the continuum properties of their material but also on their shape. Our investigation of the Inherent Structure Hypothesis focuses on this length scale, where we have supposed that the space medium forms certain structures whose intrinsic curvatures can be measured and which in fact manifest as the effects currently attributed to dark matter. Finally, the cosmic length scale pertains to the global geometry of the cosmos. To use an analogy: the relationship between the global geometry of the cosmos versus the geometry at its structure length scale is like the relationship between the Earth's global geometry, which is approximately spherical, versus that of the local terrain at various regions on the Earth's surface. The Solid Mechanics perspective interprets the Lagrangian components $\mathcal{L}$, $\overline{\mathcal{L}}$ and $\mathcal{L}_\text{M}$ from Equation (1.1) as due to features of the cosmic fabric at different length scales. Figure 1.1 illustrates a breakdown of these features that is analogous to similar breakdowns used in the multi-scale modeling of materials [68, 69].

![Cosmic hierarchical length scales.](https://figures.tgtenev.com/tenev2018-dissertation/fig-lengthscales.svg)

**Figure 1.1.** Cosmic hierarchical length scales and the information bridges between them. The field equations of General Relativity and, analogously, the constitutive equations of the cosmic fabric dominate the continuum length scale (2). The effects of dark matter are directly observed at the structure length scale (3). The structures at length scales (3) and (4) contribute the $\overline{\mathcal{L}}$ terms to the action equation, while length scale (1) contributes the $\mathcal{L}_\text{M}$ term. The effects of structure at length scales below and above the continuum length scale are accounted for by the Lagrangian terms $\overline{\mathcal{L}}$ and $\mathcal{L}_\text{F}$ within the Einstein–Hilbert action.

The physical motivation for the sizes of the aforementioned length scales is based on the various kinds of inherent curvature and not on fixed physical constants. As an analogy, consider again the Earth's surface. At scales less than 1 km, for example, one could approximate the surface as flat, but between 1 km – 100 km, the local relief (mountains and hills) becomes significant. At larger length scales (greater than 100 km), the curvature of the globe begins to be significant. These length scale boundaries, 1 km and 100 km, are not fundamental in the same way in which, for example, Planck's constant is fundamental, but stem from the specific structure of the Earth and its design. In the same way, the Inherent Structure Hypothesis proposes that cosmic space has inherent structure at galactic length scales as well as at cosmic length scales, which reflect the organization of the universe.

Different governing equations characterize different length scales. Information bridges, indicated as arrows in Figure 1.1, convey aggregate information from one length scale to another in the form of state variables. These state variables figure as parameters into each of the Lagrangian components $\mathcal{L}$, $\overline{\mathcal{L}}$ and $\mathcal{L}_\text{M}$. For example, $\mathcal{L}$ is parameterized by the Ricci scalar $R$, while $\mathcal{L}_\text{M}$ by the energy and momentum of matter. The term $\overline{\mathcal{L}}$ is parameterized by the inherent curvature of space, which is discussed in Chapter VI. Note that inherent curvature can exist at multiple length scales, such as (3) and (4) as indicated in the figure. Information about inherent curvature that propagates to a higher length scale can be treated in aggregate as a kind of texture. At the Continuum Scale, we expect the effects of larger scale structures to be negligible, but at the Structure and Cosmic scales these would become significant and manifest as, for example, the "dark matter" effect (see Chapters VI and VII) or as the organization of matter into walls, filaments, and sheets, which are too large to be explainable by conventional gravity.

### Computational Methods

Below, we review some of the numerical methods commonly used to solve boundary value problems (BVPs) and initial value problems (IVPs) within the fields of Solid Mechanics, General Relativity, and Cosmology. We focus on the Finite Element Method (FEM), Finite Difference Method (FDM), and the N-Body Method, each of which finds applications in all three fields. Finally, we briefly review the state of Numerical Relativity, which is the area of research for applying computational methods to solving the field equations of General Relativity.

The Finite Element Method (FEM) [19, 54] divides the problem domain into smaller subdomains within which the unknown variables are approximated with a linear combination of a finite set of known interpolation functions. Solving for the unknown variables amounts to calculating the coefficients that multiply the interpolation functions. These coefficients are determined by solving a system of linear equations. FEM is typically used in Solid Mechanics to model configurations that are in a static or quasi-static equilibrium. For example, modeling low strain rate deformation falls into this category. FEM can also be used in General Relativity and other fields for the simulation of boundary value problems.

The Finite Difference Method (FDM) approximates infinitesimal differentials with partial differences [38]. It is commonly used for the numerical solution of differential equations, in which time figures as one of the independent variables, such as initial value problems (IVP). FDM is also used to solve boundary value problems (BVPs) where time is not an explicit parameter, but for such situations FEM yields superior precision since FEM is better suited to handle complex geometries. At the same time, compared to FEM, FDM is conceptually simpler and applies to a broader range of problems, such as problems in dynamics, fluid mechanics and general relativity, whose governing equations may be nonlinear. The initial value problem (IVP) specifies the state of the system at some initial time $t_0$ along with boundary conditions and the governing partial differential equations (PDEs) for evolving the system. In Solid Mechanics, FDM is used to solve IVPs, such as high strain rate deformation and wave propagation. In general relativistic numerical simulations, FDM is used in conjunction with the Arnowitt–Deser–Misner (ADM) formalism of General Relativity [14]. The ADM formalism treats spacetime as foliated into space-like surfaces $\Sigma_t$, where $t$ is the time coordinate while the metric tensor and conjugate momenta are the independent variables. Essentially, ADM casts the equations of General Relativity in the form of an IVP solvable by FDM. Stability and convergence is a common challenge with FDM codes. This is especially true for explicit FDM codes for which the maximum time step $\Delta t$ that ensures convergence depends on the mesh spacing. Such restriction on $\Delta t$ is known as the Courant–Friedrich–Lewy (CFL) condition [36].

The N-Body Method simulates the behavior of systems that can be described as a set of point particles by numerically simulating the interactions between the particles [90, 163]. In Cosmology, this method is used to simulate gravitational interaction between bodies [163] and to study structure formation in the universe at various length scales [23]. The Millennium Run [152] and the Bolshoi Simulation [80] are specific examples. The method is also used in Solid Mechanics for simulating the interactions between atoms [60].

Numerical Relativity uses computational techniques to study black holes, gravitational waves, neutron stars, and other gravitational phenomena. The early results concerned the simulation of black holes [11, 102, 153], but subsequent improvements were needed to avoid singularity problems, for which the techniques of excision and puncture were used. With the excision technique, the region around the singularity of a black hole is left unevolved but without affecting the results [6, 7, 8, 26, 29, 34, 135, 150]. The puncture method separates the solution into two parts: an analytical solution around the black hole singularity, and a numerical solution that is further away from the singularity [16, 28, 30, 135]. Adaptive mesh refinement techniques were also introduced [55, 70].

Besides the tools used in Numerical Relativity, two other numerical tools pertinent to cosmology are: CMBFAST by Seljak and Zaldarriaga [149, 172], and the Code for Anisotropies of the Microwave Background (CAMB) by Lewis and Challinor [88]. Both tools are used for analyzing the cosmic microwave background (CMB) and calculating the parameters of the Standard Cosmological Model.

### Dark Matter

Kapteyn and Oort [76, 127] were the first to hypothesize the existence of hidden mass as a way to explain their observations of stellar motions. Shortly afterwards, Zwicky [173] coined the term "dark matter," which he used to explain the observed galactic motions at the edges of the Coma galaxy cluster. Babcock [15] was the first to discover the anomalies in the rotation curves of galaxies when studying the Andromeda nebula, which he attributed to dark matter. His discovery was later confirmed by Rubin and Ford [145].

Some of the arguments for the existence of dark matter (DM) are based on indirect observations, which we call the "Dark Matter Effect," while others are model dependent. Since DM has not been directly observed, we will use the term "Dark Matter Hypothesis" for the notion that DM is the explanation for the DM Effect. The DM effect is observed in the motions of stars within galaxies and galactic clusters. For example, the rotation curves of most galaxies indicate higher velocities compared to what can be accounted for by the observed amount of visible galactic mass. The rotation curve of a galaxy is the relationship between the linear velocity with which stars revolve around the galactic center and their distance from it. The DM Hypothesis postulates a spherical halo of dark matter around each galaxy to account for the observed rotation curves. The DM effect is also present in the statistical distribution of galactic velocities within galaxy clusters, and in the pressure of the gas within them, measurable from its X-ray emissions. Such observations indicate more gravity than can be accounted for by the present visible mass. Additionally, the correctness of various cosmological theories, such as the $\Lambda$CDM model, is predicated on the existence of non-baryonic mass, which is viewed as supporting evidence for the DM hypothesis.

At the same time, there are significant challenges against the Dark Matter Hypothesis. The most significant one is the lack of direct observational evidence. Dark matter is speculated to exist either in the form of an elementary particle, such as neutrinos or some other particles, or as compact objects, such as primordial black holes. However, decades of searching for any of these candidates has found nothing [89], which has led researchers to consider non-DM explanations for the DM Effect.

The Modified Newtonian Dynamics (MOND) theory proposed by Milgrom [115] is an alternative explanation for the gravitational anomalies currently attributed to dark matter. It postulates a modification to Newton's Second Law of motion stating that the net force acting on an object is proportional to the square of that object's acceleration for accelerations less than some parameter $a_0$. Milgrom [115] envisioned that the parameter $a_0$ is a new constant of nature. With these adjustments to classical Newtonian dynamics, MOND could predict accurately the observed galactic rotation curves for many galaxies of diverse types, as well as the observed dynamics of galaxy clusters. In regards to the problem of the missing mass within galactic clusters, MOND reduces the discrepancy from a factor of $\sim 10$ to a factor of $\sim 2$ [118]. The seemingly coincidental relationship between MOND's experimentally determined parameter $a_0$ and Hubble's parameter $H_0$, which is $2\pi a_0 \approx c H_0$, suggests that perhaps the relationship is not coincidental after all, and that $a_0$ may be related to the inherent geometry of the cosmos.

While MOND has been successful in producing predictions that agree with observations, the theoretical basis for it is still under development. Bekenstein and Milgrom [21] first introduced a complete MOND theory based on the modification of the classical Newtonian Lagrangian. Later, Bekenstein [22] proposed a relativistic theory that yields MOND behavior. However, as Milgrom writes in a recent review of MOND [118]:

> "Beyond the basic tenets, we need to construct full-fledged theories, generalizing Newtonian dynamics and general relativity, that satisfy the basic tenets, that are, preferably, derived from an action, and that can be applied to any system and situation. There exist several nonrelativistic theories of MOND as modified gravity incorporating its basic tenets. Recent years have seen the advent of several relativistic formulations of MOND. These account well for the observed gravitational lensing, but do not yet provide a satisfactory description of cosmology and structure formation. While these theories are useful in many ways, it may well be that none of them points to the correct MOND theory."

Another issue with MOND is the notable outlier galaxies that do not fit its simple one-parameter model, such as galaxies appearing to have too little dark matter [43]. Chapter VI adds more information about the DM Hypothesis and MOND, and offers an alternative explanation for the DM effect.

### Assumptions and Limitations

The following are simplifying assumptions that apply to all of the work presented here, except when explicitly stated otherwise: weak gravity and nearly static fields.

We conduct our study under the assumption of weak gravitational fields in order to keep the math tractable. However, this assumption is not fundamental to the model, and we expect that it could be relaxed or removed in the future. Under the material model of space introduced herein, the weak field regime, which is the subject of Linearized Gravity [119], is analogous to the small strain condition, which is the subject of Solid Mechanics' Infinitesimal Strain Theory. We consider a gravitational potential $\Phi$ to be weak if $\left| \Phi / c^2 \right| \ll 1$ (note that $\Phi/c^2$ is a dimensionless quantity). By this definition, most gravitational fields that we experience on an everyday basis are weak. For example, the values for $\left| \Phi / c^2 \right|$ at the Earth's surface due to the gravitational fields of the Earth, Sun, and Milky Way are $6.7\times 10^{-10}$, $1.0\times 10^{-8}$, and $1.4 \times 10^{-6}$, respectively [171]. As such, we consider these gravity fields to be weak.

Except in regards to gravity waves, we will assume nearly static fields in addition to weak fields. A field is considered nearly static if the gravitating masses generating the field move with velocities much less than the speed of light. This is the case for most gravitational fields that we experience. The nearly static field assumption means that differentiation with respect to time results in negligibly small values.

### Contributions and Organization of the Dissertation

This dissertation work introduces and numerically substantiates an elastic constitutive model of gravity that can be used to address outstanding problems in Cosmology such as explaining gravitational phenomena currently attributed to dark matter.

To this end, in Chapters III–V, we develop the theoretical model that relates the equations of General Relativity to those of the continuum mechanics of solids and we identify analogous concepts between the two fields. The analogy allows a problem in one field to be mapped to a problem in the other, and consequently promotes a wider exchange of ideas, theories and tools.

In Chapters VI and VII, we apply the theoretical model referenced above to a specific cosmological problem. We investigate whether the inherent structure of space, such as the existence of galactic-scale inherent spatial curvature (that is, one uncaused by the matter within space), could manifest as the Dark Matter Effect, that is, the gravitational anomalies that are currently attributed to dark matter. Chapter VI contains the theoretical work showing that such an inherent spatial curvature amplifies the gravitational effects of ordinary matter. This Inherent Structure Hypothesis, as we call it, is tested numerically in Chapter VII, where we develop a numerical framework for this purpose. Finally, we summarize and conclude in Chapter VIII. Chapter II contains the requisite background material from the fields of General Relativity and solid mechanics, and Chapter IX includes recommendations for future research based on the ideas presented here.

---

## II. Background

Below, we introduce the requisite concepts from differential geometry, continuum mechanics, and General Relativity that are used in the remainder of this dissertation work.

### Differential Geometry

Differential geometry employs calculus techniques to study curvature and deformation. It is used extensively within the General Theory of Relativity, and also to some extent within continuum mechanics. Here, we introduce briefly the concepts of: covariance, contravariance, metric, and curvature. The material below was first published by Tenev and Horstemeyer [159].

#### Contravariant and Covariant Representation of Points, Reciprocal Basis

This subsection is based on the lecture notes by Vainchtein [170]. Within this and the following subsection only, we will use **boldface** to denote vector quantities, while we motivate and explain the contravariant and covariant notation that is used in the remainder of this dissertation. Also, without loss of generality, we work in two-dimensional (2D) space to simplify the examples used here.

In order to refer to points in space we need a set of basis vectors and a reference point, also known as the origin. For example, let $\mathbf{e_1}$ and $\mathbf{e_2}$ be basis vectors in 2D space such that they are both attached at the origin but not overlapping each other. Each basis vector defines a coordinate axis and a measuring ruler for that axis, by which a numerical value can be assigned to any point on the axis. Since $\mathbf{e_1}$ and $\mathbf{e_2}$ are not parallel to each other, we can reference any point in space by stating the numerical values of its projection points along the $\mathbf{e_1}$ and $\mathbf{e_2}$ axes respectively. Thus, the following expression is a way to describe a point $\mathbf{a}$ in terms of the given basis vectors:

$$
\begin{split}
\mathbf{a}=a^1\mathbf{e_1}+a^2\mathbf{e_2} =
\begin{pmatrix} a^1 \\ a^2 \end{pmatrix}
\end{split}
\tag{2.1}
$$

The choice of basis vectors $\mathbf{e_1}$ and $\mathbf{e_2}$ is arbitrary with the only limitation being that they should not be parallel to one another. The point $\mathbf{a}$ exists independent of the choice of basis vectors. However, the indexes $a^1$ and $a^2$ are only meaningful in the context of the basis and change when another basis is chosen.

The coefficients $a^1$ and $a^2$ form the *contravariant* representation of the point $\mathbf{a}$. The term "contravariant" signifies that these coefficients vary inversely in relation to the length of their respective basis vectors. In other words, if we were to choose longer basis vectors then the same point $\mathbf{a}$ would be represented by smaller coefficients and vice versa.

How are the contravariant coefficients $a^1$ and $a^2$ determined for a given basis? In the case of a Cartesian orthonormal basis, the coefficients are the lengths of the orthogonal projections of the point $\mathbf{a}$ onto the respective basis vectors. Therefore determining $a^1$ and $a^2$ amounts to computing the dot product between $\mathbf{a}$ and the basis. However, this procedure does not apply for any general set of basis vectors that may not necessarily be orthonormal. Nevertheless, we can choose a *reciprocal* set of basis vectors $\mathbf{e^1}$ and $\mathbf{e^2}$ such that,

$$
\begin{split}
\mathbf{e_1}\cdot\mathbf{e^1} = 1\quad & \mathbf{e_1}\cdot\mathbf{e^2} = 0 \\
\mathbf{e_2}\cdot\mathbf{e^1} = 0\quad & \mathbf{e_2}\cdot\mathbf{e^2} = 1
\end{split}
\tag{2.2}
$$

With the help of these reciprocal basis vectors we can compute each contravariant coefficient as the dot product between the given point $\mathbf{a}$ and the respective reciprocal basis vector. For example,

$$
\begin{split}
\mathbf{a}\cdot\mathbf{e^1} = (a^1\mathbf{e_1} + a^2\mathbf{e_2})\cdot\mathbf{e^1}
= a^1(\mathbf{e_1}\cdot\mathbf{e^1}) + a^2(\mathbf{e_2}\cdot\mathbf{e^1})
= a^1
\end{split}
\tag{2.3}
$$

and likewise for $a^2$.

Since $\mathbf{e^1}$ and $\mathbf{e^2}$ themselves form another basis, the given point $\mathbf{a}$ has a representation in that basis too as follows:

$$
\begin{split}
\mathbf{a}=a_1\mathbf{e^1}+a_2\mathbf{e^2}.
\end{split}
\tag{2.4}
$$

The coefficients $a_1$ and $a_2$ form the *covariant* representation of point $\mathbf{a}$. The term "covariant" signifies that these coefficients would increase or decrease when the original set of basis vectors $\mathbf{e_1}$ and $\mathbf{e_2}$ increase or decrease in length respectively. That is, the covariant coefficients vary in the same way as the original basis vectors.

#### Metric and Metric Tensor

A metric specifies how distances between points are computed for a given set of basis vectors. For example, let $\mathbf{e_1}$ and $\mathbf{e_2}$ be the basis vectors and let $\mathbf{a}$ and $\mathbf{b}$ be two points in space. If the line segment between $\mathbf{a}$ and $\mathbf{b}$ happened to be along one of the basis vectors, then we could use that basis vector as the measuring rod to count off the distance between the two points. However, there is no inherent mechanism for determining the length of a segment in a general orientation. In such case, we would use a combination of all measuring rods, but the manner in which these rods are to be combined must be specified in addition to specifying the basis. The metric tensor provides this additional information.

Let $\Delta \mathbf{x}=\mathbf{b}-\mathbf{a}$ be the vector between points $\mathbf{a}$ and $\mathbf{b}$ so that

$$
\begin{split}
\Delta x^i = b^i - a^i, \quad i = \{1,2\}
\end{split}
\tag{2.5}
$$

and

$$
\begin{split}
\Delta \mathbf{x} = \Delta x^1\mathbf{e_1} + \Delta x^2 \mathbf{e_2}
\end{split}
\tag{2.6}
$$

By definition, the length $\Delta s$ of the segment connecting points $\mathbf{a}$ and $\mathbf{b}$ is determined as follows:

$$
\begin{split}
(\Delta s)^2 = g_{11}\Delta x^1\Delta x^1 + g_{12}\Delta x^1\Delta x^2 + g_{21}\Delta x^2\Delta x^1 + g_{22}\Delta x^2\Delta x^2
\end{split}
\tag{2.7}
$$

where the coefficients $g_{ij}, i,j=\{1,2\}$ are called the *metric*. It is possible to show that these coefficients obey tensor transformation rules under change of basis and thus show that they are the components of a tensor $\mathbf{g}$ known as the *metric tensor*. Being a tensor means that $\mathbf{g}$ represents a quantity that is independent of the choice of basis so that only the specific representation of $\mathbf{g}$ in terms of its components $g_{ij}$ depends on the basis.

Indeed, we can write the equation above in a basis-independent way as follows:

$$
\begin{split}
(\Delta s)^2 = \Delta \mathbf{x}^T\mathbf{g}\Delta \mathbf{x}
\end{split}
\tag{2.8}
$$

Therefore it is the tensor $\mathbf{g}$ alone, independent from the choice of basis, that is responsible for defining distances between points in space. From here on, we will use the terms "metric" and "metric tensor" interchangeably.

In general, $\mathbf{g}$ may vary from point to point in space. In other words, $\mathbf{g}=\mathbf{g}(\mathbf{x})$ is a tensor field. Therefore, the metric equation above is only valid within a small region in space for which we can treat $\mathbf{g}$ as approximately constant. To signify that, we typically write the metric equation in terms of the infinitesimal distance like so:

$$
\begin{split}
(ds)^2 = d\mathbf{x}^T\mathbf{g}\,d\mathbf{x}
\end{split}
\tag{2.9}
$$

##### Relationship to the Dot Product of Vectors

Once we have established the notion of distance, we can derive other notions such as perpendicularity, geodesic (the generalization of a straight line), and dot product. Since the metric tensor defines how distances are measured, it is also involved in defining the dot product between two vectors.

We begin by defining the square of the line segment distance $ds$ as the dot product of the vector $d\mathbf{x}$ with itself. By expanding the dot product in terms of the contravariant representation we get the following:

$$
\begin{split}
ds^2 = d\mathbf{x}\cdot d\mathbf{x} = \left(dx^i\mathbf{e_i}\right)\cdot \left(dx^j\mathbf{e_j}\right) = dx^i dx^j(\mathbf{e_i}\cdot\mathbf{e_j}) = g_{ij}dx^i dx^j
\end{split}
\tag{2.10}
$$

where summation of repeated indexes is implied. The last equality above follows from the definition of the metric coefficients $g_{ij}$ in terms of their use in computing the square of the line segment $ds^2$ per Equation (2.7). For the last equality to be true for any choice of line segment, it follows that:

$$
\begin{split}
g_{ij} = \mathbf{e_i}\cdot\mathbf{e_j}, \quad i,j = \{1,2\}
\end{split}
\tag{2.11}
$$

Next, consider the dot product of any arbitrary two vectors $d\mathbf{x}$ and $d\mathbf{y}$ as follows:

$$
\begin{split}
d\mathbf{x}\cdot d\mathbf{y}
= \left( dx^i\mathbf{e_i}\right)\cdot \left( dy^j\mathbf{e_j}\right)
= dx^i dy^j(\mathbf{e_i}\cdot\mathbf{e_j})
= g_{ij}dx^i dy^j
= d\mathbf{x}^T \mathbf{g}\, d\mathbf{y}
\end{split}
\tag{2.12}
$$

In other words, the metric tensor is the dot-product operator. While for Cartesian coordinates in Euclidean space we could have just used $d\mathbf{x}\cdot d\mathbf{y} = d\mathbf{x}^T d\mathbf{y}$, in the general case we need to use the metric tensor to compute the dot product as per Equation (2.12) above.

##### Raising and Lowering of Indexes

Consider the following expression for one of the covariant components of an arbitrary point $\mathbf{a}$. By using both covariant and contravariant representations of $\mathbf{a}$, we can derive the following:

$$
\begin{split}
a_1 & = (a_1\mathbf{e^1} + a_2\mathbf{e^2})\cdot \mathbf{e_1} = \mathbf{a} \cdot \mathbf{e_1} \\
& = (a^1\mathbf{e_1} + a^2\mathbf{e_2})\cdot \mathbf{e_1}
= a^1(\mathbf{e_1}\cdot \mathbf{e_1}) + a^2 (\mathbf{e_2} \cdot \mathbf{e_1}) \\
& = g_{11} a^1 + g_{12}a^2
\end{split}
\tag{2.13}
$$

In other words, we conclude that the metric tensor coefficients can be used to convert between contravariant and covariant representation. In general:

$$
\begin{split}
a_i &= g_{ij}a^j \\
a^j &= g^{ij}a_j
\end{split}
\tag{2.14}
$$

In the above equation the $g^{ij}$ coefficients are the coefficients of the metric tensor in terms of the reciprocal basis vectors. These constitute the contravariant representation of $\mathbf{g}$ while the coefficients $g_{ij}$ make up the covariant representation. It is straightforward to show that,

$$
\begin{split}
& g^{ij} g_{ij} = \delta_{ij} \\
\therefore\ g^{ij} &= [g_{ij}]^{-1}
\end{split}
\tag{2.15}
$$

The conversion from contravariant to covariant representation and vice versa is known as lowering and raising of indexes, respectively, and the metric tensor's covariant or contravariant representation is used to perform it.

##### Flat Space with Cartesian Coordinates

In Cartesian coordinates the metric is simply the following expression, which is the direct application of the Pythagorean theorem:

$$
\begin{split}
ds^2 = (dx^1)^2 + (dx^2)^2
\end{split}
\tag{2.16}
$$

Therefore, the metric tensor is the identity tensor, whose components are as follows:

$$
\begin{split}
g_{11} = g_{22} = 1,\quad g_{12} = g_{21} = 0
\end{split}
\tag{2.17}
$$

Likewise, the flat three-dimensional Cartesian metric tensor is: $g_{ij} = \delta_{ij}$, where $\delta_{ij}$ is the Kronecker delta. The four-dimensional tensor for Minkowskian (flat) spacetime is $g_{\mu\nu} = \eta_{\mu\nu}$, for $\mu,\nu=0\ldots 3$, where

$$
\begin{split}
\eta_{00}=-1, \; \eta_{0i}=\eta_{i0}=0, \; \eta_{ij} =\delta_{ij} \quad (i,j=1\ldots 3)
\end{split}
\tag{2.18}
$$

##### Non-Cartesian Coordinates

Consider a set of unit basis vectors $\mathbf{e_1}$ and $\mathbf{e_2}$ that subtend some arbitrary angle $\theta$ with each other as illustrated in Figure 2.1a. We can use simple trigonometry as shown in the diagram to compute the length of an arbitrary line segment $ds$ as follows,

$$
\begin{split}
ds^2 & = (dx^2+dx^1 \cos \theta)^2+(dx^1 \sin \theta)^2 \\
& = (dx^1)^2 + 2dx^1dx^2 \cos \theta + (dx^2)^2
\end{split}
\tag{2.19}
$$

Therefore the metric tensor's representation for the given basis vectors is as follows:

$$
\begin{split}
g_{11} = g_{22} = 1,\quad g_{12} = g_{21} = \cos\theta
\end{split}
\tag{2.20}
$$

![A line segment $ds$ in skewed Cartesian (a) and spherical (b) coordinates.](https://figures.tgtenev.com/tenev2018-dissertation/fig-metric.svg)

**Figure 2.1.** A line segment $ds$ in skewed Cartesian (a) and spherical (b) coordinates. The metric for case (a), when the basis are unit vectors subtending some angle $\theta$ with each other, is $ds^2 = (dx^1)^2 + (dx^2)^2 + 2dx^1 dx^2 \cos \theta$. For case (b) of the coordinates $(\theta, \varphi)$ for the surface of a sphere with radius $R$, the metric is $ds^2 = R^2 d\theta^2 + R^2 \sin^2 \theta\, d\varphi^2$.

Just as with the previous example of Cartesian coordinates, the current one also involves a flat (Euclidean) space and yet the metric tensor's representation is no longer one and the same as the identity tensor. That is because the metric tensor's representation depends on the choice of basis vectors. At the same time, in both of the above cases the metric is constant throughout space.

In spherical coordinates, the great circles serve as coordinate axes and, as illustrated in Figure 2.1b, the square length $ds^2$ of an infinitesimal line segment can be computed as follows:

$$
\begin{split}
ds^2 = R^2 d\theta^2 + R^2 \sin^2 \theta\, d\varphi^2
\end{split}
\tag{2.21}
$$

where $R$ is the radius of the sphere, $\theta$ is the elevation angle, and $\varphi$ is the azimuth angle. Based on Equation (2.21) we conclude that the metric tensor for spherical coordinates has the following form:

$$
\begin{split}
g_{11} = R^2;\quad g_{22} = R^2 \sin^2 \theta; \quad g_{12} = g_{21} = 0
\end{split}
\tag{2.22}
$$

Unlike the previous examples, which were all for Euclidean space, in this case the metric tensor varies from point to point on the sphere because its value depends on the elevation angle.

#### Affine Connection and Covariant Derivative

The following section is based on Sections 85 and 86 in Landau and Lifshitz [83].

An *affine connection* specifies how vectors located at different points in space can be compared to one another, which is needed to compute the differential of a vector field along a given direction in space. Such differential is known as the *covariant derivative* of the vector field. In Euclidean geometry, the difference between two vectors can be computed by parallel transporting one to the location of the other and using the triangle rule to subtract one from the other. In non-Euclidean geometry, parallel transport is not well defined because it depends on the path taken. Therefore, additional information is needed to compute differences between vectors at different locations. This additional information is the *affine connection* and like the metric, an affine connection is not inherent within a given space but must be specified as a matter of choice. The affine connection specifies how the contravariant components of vectors change under *parallel transport*, which is the "relocation" of a vector from one place to another without changing its value.

Let $v^i$ be some vector at location $x^i$ that we wish to parallel transport to another location $x^i + dx^i$. The vector change $dv^i$ under parallel transport along the infinitesimal displacement $dx^i$ is given by the following:

$$
\begin{split}
dv^i = \Gamma^i_{jk} v^j dx^k
\end{split}
\tag{2.23}
$$

Equation (2.23) expresses the notion that over an infinitesimal displacement, the change $dv^i$ can be approximated by a linear expression in terms of the vector's own components and the components of the displacement vector. The linear coefficients $\Gamma^i_{jk}$ are known as *connection coefficients* or *Christoffel symbols*. Just like the metric, the Christoffel symbols can vary from one point in space to another. Note the similarity between the above expression and the expression in Equation (2.12). It appears as if each component $dv^i$ is the result of the inner product between $v^j$ and $dx^k$ where $\Gamma^i_{jk}$ plays the role of the inner product operator. However, unlike the metric tensor, the Christoffel symbols are not tensors since they do not obey tensor transformation rules.

Although the connection is a matter of choice, there is a specific connection that is in a sense natural for the given metric. It is known as the *Levi-Civita Connection*. Its Christoffel symbols can be derived from differentiating the metric tensor with respect to spatial displacements as follows:

$$
\begin{split}
\Gamma_{ij}^{k} = \frac{1}{2}g^{kl}\left(\partial_{j}g_{il}+\partial_{i}g_{jl}-\partial_{l}g_{ij}\right)
\end{split}
\tag{2.24}
$$

#### Intrinsic Curvature

Equation (2.24) shows that for Euclidean space the Christoffel symbols all vanish, so it is reasonable to expect that these have something to do with the curvature of space. Indeed, the components of the Riemann curvature tensor $R_{bcd}^{a}$, those of the Ricci tensor $R_{ab}$, and the Ricci scalar curvature can be expressed in terms of the Christoffel symbols and their gradients as follows,

$$
\begin{split}
R_{bcd}^{a} = \partial_{c}\Gamma_{bd}^{a}-\partial_{b}\Gamma_{cd}^{a}+\Gamma_{cf}^{a}\Gamma_{bd}^{f}-\Gamma_{df}^{a}\Gamma_{cb}^{f}
\end{split}
\tag{2.25}
$$

$$
\begin{split}
R_{ab} \equiv R_{acb}^{c}
\end{split}
\tag{2.26}
$$

$$
\begin{split}
R \equiv R_{ab}g^{ab}
\end{split}
\tag{2.27}
$$

In the case of small curvatures, that is when $g_{ab}=\eta_{ab}+h_{ab}$ for some small perturbation $|h_{ab}|\ll1$, and for an appropriate choice of coordinates, namely those that conform to the harmonic gauge, the Ricci Curvature tensor is approximated as the following [120],

$$
\begin{split}
R_{ab} \approx -\frac{1}{2}\eta^{cd}\partial_{cd}h_{ab}, \quad (g_{ab}=\eta_{ab}+h_{ab},\quad |h|_{ab}\ll1)
\end{split}
\tag{2.28}
$$

### Continuum Mechanics

Continuum mechanics models the kinematics and kinetics of solids and fluids in the context of a differentiable continuum. Below we review the following concepts: deformation, strain, stress, and elastic moduli, which are basic notions in this field of science.

#### Deformation, Material and Reference Coordinates

Let $x^i$ be the material coordinates assigned to a body, and let $g_{ij}$ be its metric tensor. By *material coordinates*, we understand those that are attached to the body (as if painted onto it) and displace with its material as it deforms. Thus, deformation does not change the coordinates of a given material point but does change distances between points. The metric tensor defines how coordinate differences relate to distances. Thus, the distance element $ds$ between two nearby material points is given by,

$$
\begin{split}
ds^2 = g_{ij}dx^i dx^j
\end{split}
\tag{2.29}
$$

The distance element $d\overline{s}$ between the same two material points prior to deformation is the following:

$$
\begin{split}
d\overline{s}^2 = \overline{g}_{ij} dx^i dx^j
\end{split}
\tag{2.30}
$$

where $\overline{g}_{ij}$ is the metric of the body prior to deformation. From here on, a bar over the name of a variable indicates that the referenced quantity pertains to the undeformed configuration. Oftentimes, the material coordinates are assigned such that they are arranged in a Cartesian grid prior to the body's deformation, in which case the undeformed metric is $\overline{g}_{ij} = \delta_{ij}$.

Let $y^i$ be a set of *reference coordinates* associated with the enclosing space. Each material point of the body can also be described in terms of these reference coordinates. However, unlike its material coordinates, the point's reference coordinates are not attached to it so the same material point may have different reference coordinates before and after the deformation. Throughout the work presented here, we will always consider reference coordinates that are arranged in a fixed Cartesian grid, so that the metric associated with the reference space is simply $\delta_{ij}$.

The deformation gradient of the body, which fully describes the body's deformation up to a rigid translation, is defined as follows,

$$
\begin{split}
F^i_j \equiv \frac{\partial y^i}{\partial x^j}.
\end{split}
\tag{2.31}
$$

The relationship between the deformed metric $g_{ij}$ and $F^i_j$ can be derived as follows: Consider the distance element $ds$ with material and reference coordinate differences $dx^i$ and $dy^i$ respectively. Then,

$$
\begin{split}
g_{ij}dx^i dx^j = ds^2 = \delta_{kl} dy^k dy^l = \delta_{kl} \frac{\partial y^k}{\partial x^i}\frac{\partial y^l}{\partial x^j}dx^i dx^j = \delta_{kl} F^k_i F^l_j dx^i dx^j
\end{split}
\tag{2.32}
$$

Since Equation (2.32) must be true for any arbitrary distance element $ds$, it follows that:

$$
\begin{split}
g_{ij} = \delta_{kl} F^k_i F^l_j,
\end{split}
\tag{2.33}
$$

which is also the same expression as for the Cauchy–Green deformation tensor. In other words, for the coordinate assignments described above and used throughout this work, the deformed metric tensor $g_{ij}$ is one and the same as the Cauchy–Green deformation tensor, if the undeformed metric is the flat Cartesian metric: $\overline{g}_{ij} = \delta_{ij}$.

#### Small Strain

The small strain tensor $\varepsilon_{ij}$ quantifies the amount of relative length change as a result of deformation. By definition, $\varepsilon_{ij}$ is such that,

$$
\begin{split}
2\varepsilon_{ij}dx^i dx^j & = ds^2 - d\overline{s}^2 = (g_{ij} - \overline{g}_{ij})dx^i dx^j \\
\therefore\ \varepsilon_{ij} &= \frac{1}{2}(g_{ij} - \overline{g}_{ij})
\end{split}
\tag{2.34}
$$

Each component $\varepsilon_{ij}$ represents the amount of relative stretch in the $j^\text{th}$ direction along the cross section surface normal to the $i^\text{th}$ direction (see Figure 2.2b).

![Stress, strain and Poisson effect.](https://figures.tgtenev.com/tenev2018-dissertation/fig-stress-strain-poisson.svg)

**Figure 2.2.** Stress, strain and Poisson effect. Multi-axial stress state (a), and a uniaxial deformation of an object (b) from the transparent to the opaque shape. Each component $\sigma_{ij}$ represents the stress through the $i^\text{th}$ surface in the $j^\text{th}$ direction. The Poisson's ratio $\nu$ is the negative of the transverse strain (perpendicular to the direction of tension) divided by the axial strain (along the direction of tension). For a uniaxial stress state, $\varepsilon_{jj} = (-\nu/Y) \sigma_{ii} = -\nu\varepsilon_{ii}$ for $i \neq j$.

The three-dimensional (3D) volumetric strain, defined as

$$
\begin{split}
\varepsilon \equiv \varepsilon^i_i \equiv \varepsilon^1_1 + \varepsilon^2_2 + \varepsilon^3_3 \equiv \overline{g}^{ij} \varepsilon_{ij},
\end{split}
\tag{2.35}
$$

is a scalar field that represents the fractional increase of the body's mid-hypersurface volume after deformation. In other words, $dV/d\overline{V} = (1+\varepsilon)$, where $dV$ and $d\overline{V}$ are, respectively, the deformed and undeformed volume elements.

#### Stress and Elastic Moduli

The stress tensor $\sigma_{ij}$ represents the force per unit area that is applied in the $j^\text{th}$ direction along the cross section plane that is normal to the $i^\text{th}$ direction (see Figure 2.2a). Hooke's Law (1.2) relates the stress and strain tensor quantities to each other via a set of elastic moduli that characterize the constitutive properties of the material. Constitutive properties are those that are intrinsic to the material and characterize its internal structure. In the most general case, there can be up to 21 independent elastic moduli, but for an isotropic material there are just two.

In this dissertation work, we will most often use the Young's elastic modulus $Y$ and the Poisson ratio $\nu$ as the two independent elastic moduli that figure in Hooke's Law (1.2). Any other elastic moduli, such as the shear modulus $\mu$ and the First Lamé parameter $\lambda$, which will also be considered on occasion, can be expressed in terms of $Y$ and $\nu$. The Young's elastic modulus $Y$ is the amount of longitudinal stress $\sigma_{ii}$ in the $i^\text{th}$ direction needed to produce a unit amount of longitudinal strain $\varepsilon_{ii}$ in the same direction under a uniaxial stress condition (no summation intended over the index $i$). The Poisson ratio $\nu$ is the negative of the transverse strain (perpendicular to the direction of tension) divided by the axial strain (along the direction of tension) (see Figure 2.2).

### General Relativity

Below we attempt to provide an intuitive description of the physics that underlies the mathematics of General Relativity (GR).

Consider a test particle $P$ situated a distance $r$ from a body of mass $M$. Newton's Gravitational Law views gravity as a force causing $P$ to accelerate with acceleration $a_P$ as follows:

$$
\begin{split}
a_p = -\frac{G M}{r^2}
\end{split}
\tag{2.36}
$$

where $G$ is the gravitational constant.

By contrast, according to General Relativity (GR) gravity is a two-part phenomenon:

1. Bent spacetime causes matter to accelerate. (Newton's First Law for bent spacetime)
2. Matter bends spacetime.

Consequently, $P$ accelerates $M$-ward because it finds itself in a spacetime that $M$ has bent. Therefore, according to GR, gravity is not a force but the manifestation of spacetime curvature.

What does it mean for spacetime to bend? Spacetime bends when time flows slower in some locations relative to other locations. Picture a sheet of lasagna extruding from a pasta maker; when some parts of the sheet are extruded slower than others, the sheet wrinkles. In this analogy, the sheet represents the trail that physical space leaves behind in time. Notice that the bending of space alone does not necessarily produce bent spacetime unless there is a variation in time lapse rates across space.

Why does bent space cause matter to accelerate? The effect is the generalization of Newton's First Law to bent spacetime, which states that a body free of forces moves along a geodesic (shortest distance between points) in spacetime. Geodesics are curved in bent spacetime. A curved trajectory in spacetime represents changing velocity and hence acceleration. Therefore, a body free of forces accelerates in curved spacetime!

Mathematically stated, the proper acceleration $a_P$ of the aforementioned particle $P$ can be derived from the equation of a geodesic in spacetime, which is as follows:

$$
\begin{split}
\ddot{x}^\alpha + \Gamma^\alpha_{\mu\nu}\dot{x}^\mu \dot{x}^\nu = 0
\end{split}
\tag{2.37}
$$

where the dots represent differentiation with respect to proper time. Essentially, Equation (2.37) states that the covariant derivative of the space-time velocity vector (also known as four-velocity) should not change. Recall from the Differential Geometry section that $\Gamma^\alpha_{\mu\nu}$ is the correction term to the ordinary derivative of the velocity vector that accounts for the effect of curvature. By "proper time" and "proper acceleration", respectively, we mean the time and acceleration measured within the particle's rest reference frame, that is, using a hypothetical clock attached to the accelerating particle. For radial acceleration from rest ($\dot{x}^0 = c, \dot{x}^i = 0$) towards a spherically symmetric body, Equation (2.37) simplifies as follows:

$$
\begin{split}
& \ddot{r} + c^2\Gamma^r_{00} = 0 \\
& a_P = \sqrt{g_{rr}}\,\ddot{r} = c^2\frac{\partial_r g_{00}}{2 \sqrt{g_{rr}}}
\end{split}
\tag{2.38}
$$

where $g_{00}$ and $g_{rr}$ are, respectively, the temporal and radial coefficients of the metric.

Why does matter bend spacetime? GR offers no explanation, but postulates the fact mathematically in the form of the well-known Einstein field equations [50], namely:

$$
\begin{split}
R_{\mu\nu} - \frac{1}{2}R g_{\mu\nu} = \kappa T_{\mu\nu}
\end{split}
\tag{2.39}
$$

where $R_{\mu\nu}$ and $R$ are, respectively, the Ricci tensor and Ricci scalar curvature, which were introduced in the Differential Geometry section, $\kappa \equiv 8\pi G/c^4$ is the Einstein constant, and $T_{\mu\nu}$ is the stress-energy tensor, which is visualized in Figure 2.3.

![Interpretation of the stress-energy tensor.](https://figures.tgtenev.com/tenev2018-dissertation/fig-stress.svg)

**Figure 2.3.** Interpretation of the stress-energy tensor $T_{\mu\nu}$. For an infinitesimal material volume element, the spatial components $T_{ij}=\sigma_{ij}$ are the same as the components of the mechanical stress tensor. $T_{00}=\rho c^2$ represents the relativistic energy density of the material, where $\rho$ is the mass density. $T_{i0}=T_{0i}=c p_i$ represent the momentum density $p_i$ in the $i^\mathrm{th}$ direction. All components $T_{\mu\nu}$ also have the meaning of momentum density fluxes in the $\nu$ direction with respect to the $\mu$ spacetime hypersurface.

For the case of weak gravity and nearly static mass density $\rho$, $T_{00} = c^2 \rho$, $T_{\mu\nu} = 0$ for $\mu,\nu \neq 0$, and Equation (2.39) reduces to the classical Newtonian gravity per Equation (2.36), which can be shown briefly as follows: Contracting Equation (2.39) with $g^{\mu\nu}$ yields that $R = -\kappa T$, where $T \equiv g^{\mu\nu}T_{\mu\nu}$, which when substituted back into Equation (2.39) produces the following:

$$
\begin{split}
R_{\mu\nu} = \kappa \left(T_{\mu\nu} - \frac{1}{2}g_{\mu\nu} T\right) = \frac{\kappa c^2}{2}\rho \delta_{\mu\nu}
\end{split}
\tag{2.40}
$$

Let $g_{\mu\nu} = \eta_{\mu\nu} + h_{\mu\nu}$, where $|h_{\mu\nu}| \ll 1$. Applying the linearized approximation for $R_{\mu\nu}$ from Equation (2.28) and ignoring the time derivative of the metric based on the nearly static assumption, Equation (2.40) expressed for just the time–time component becomes the following:

$$
\begin{split}
-\frac{1}{2}\nabla^2 h_{00} = \frac{\kappa c^2}{2}\rho = \frac{4 \pi G \rho}{c^2},
\end{split}
\tag{2.41}
$$

which is in fact the Poisson's equation of gravity with $-c^2 h_{00}/2$ disguising as the gravitational potential. Therefore, for a body of gravitating mass $M$, the solution to this equation is the following:

$$
\begin{split}
-\frac{c^2 h_{00}}{2} = -\frac{G M}{r}
\end{split}
\tag{2.42}
$$

Consequently,

$$
\begin{split}
c^2 \partial_r g_{00} = c^2 \partial_r h_{00} = -\frac{2 G M }{r^2}
\end{split}
\tag{2.43}
$$

When we substitute the result from Equation (2.43) into Equation (2.38) and we approximate $g_{rr} \approx 1$ for the case of weak gravity, we arrive at the classical Newtonian Equation (2.36) for the gravitational acceleration.

---

## III. Cosmic Fabric Model of Gravity

In this chapter, we develop a formal analogy between Solid Mechanics and General Relativity. Most of the content has been published in Tenev and Horstemeyer [160]. We identify physical space with the mid-hypersurface of a four-dimensional hyperplate, called the "cosmic fabric," which has a small thickness along a fourth spatial dimension and exhibits a constitutive stress–strain behavior. Matter–energy fields act as inclusions within the fabric causing it to expand longitudinally and consequently to bend. The effect, illustrated in Figure 3.1, is analogous to the result from General Relativity in which matter causes space to bend resulting in gravity. Unlike other theoretical paradigms that introduce additional spatial dimensions, such as string theory [61], or Brane world quantum models [45], our formulation is based on conventional Solid Mechanics theories that operate strictly within the three ordinary spatial dimensions.

![Plate bending from flat into a curved geometry.](https://figures.tgtenev.com/tenev2018-dissertation/fig-plate-bending.svg)

**Figure 3.1.** Plate bending from flat into a curved geometry. A plate bending from flat geometry (a) into a curved geometry (b) because of an inclusion that prescribes an uneven strain field, as indicated by the concentric dashed lines and the diverging arrows. The strain is larger near the center and tapers off with the distance from it. For the geometry of the plate to accommodate the prescribed strain, the plate must bend into the transverse dimension.

We conduct our study in the limit of weak and nearly static gravitational fields, and demonstrate that outside of inclusions, the fabric's action $\mathcal{S}_\text{F}$ assumes the form of the Einstein–Hilbert action $\mathcal{S}_\text{EH}$ as follows,

$$
\begin{split}
\mathcal{S}_\text{F} = \frac{YL^2}{48} \int R\sqrt{|g|}\,\mathrm{d}x^4 \quad \text{versus}\quad \mathcal{S}_\text{EH}= \frac{1}{2\kappa} \int R\sqrt{|g|}\,\mathrm{d}x^4
\end{split}
\tag{3.1}
$$

where $L$ is the reference thickness of the fabric, $g \equiv \det g_{\mu\nu}$, and the integral is taken over a large enough volume of spacetime that is sufficient to ensure convergence. The action integral of any physical system fully determines its dynamics, because the system's equations of motion can be derived from the variation of the action with respect to the metric. Therefore, once we recognize $\mathcal{S}_\text{F}$ as analogous to $\mathcal{S}_\text{EH}$, we can interpret various attributes of the cosmic fabric, such as its shape, strain, vibrations, and elastic moduli as analogous to properties of gravity and space, such as curvature, gravitational potential, gravitational waves, and the zero-point energy density of space.

Our approach ostensibly resembles the Arnowitt–Deser–Misner (ADM) [14] and DeWitt [40] formulations of gravity in the way time lapse is separated from spatial extent. For example, under the ADM approach, spacetime is foliated into space-like hypersurfaces related to each other via shift and lapse functions. Like ADM, DeWitt also considers the time evolution of the three-dimensional spatial metric. Nevertheless, the Cosmic Fabric model differs from these formulations in that it associates constitutive behavior with the geometric description of gravity and derives its governing equations from a material-like constitutive relation. Furthermore, unlike these formulations, the cosmic fabric specifies a hyperplane of absolute simultaneity.

The Cosmic Fabric model of gravity allows General Relativity problems to be formulated as Solid Mechanics problems, solved within the Solid Mechanics domain, and the solution interpreted back in General Relativity terms. The reverse is also true. Thus, ideas, methodologies and tools from each field become available to the other field. Over the past century, Solid Mechanics and General Relativity have advanced independently from each other with few researchers having expertise in both. Consequently, significant terminology and focus gaps exist between these two fields, which obscure their underlying physical similarities. Our research attempts to bridge these gaps.

The remainder of this chapter is organized as follows: In the section *Formulation of the Cosmic Fabric Model of Gravity* we develop the solid mechanics analogy of gravity by specifying a material body whose behavior, determined solely based on Hooke's Law (1.2), is demonstrably analogous to the behavior of spacetime. In the *Discussion* section we discuss the implications of the resulting model, and summarize and conclude in the *Summary and Conclusion* section.

### Formulation of the Cosmic Fabric Model of Gravity

Consider a four-dimensional hyperplate, called here the "cosmic fabric," which is thin in the fourth spatial dimension, $x^4$. We show that, for suitably chosen constitutive parameters, the fabric's Lagrangian density outside of inclusions is $\mathcal{L}_\text{F} = (YL^2/48)R\sqrt{|g|}$, where $\mathcal{L}_\text{F}$ is the integrand in Equation (3.1). This result enables us to subsequently analyze how the remaining kinematic properties of the cosmic fabric correspond to properties of gravity.

### Coordinate Assignment and Reference Space

We consider the cosmic fabric as immersed in a four-dimensional (4D) hyperspace within which it can deform. Moreover this 4D hyperspace is flat and has been assigned a Cartesian coordinate grid with coordinates $y^I$. Another set of coordinates $x^I$ is painted on the fabric in the following manner: prior to deformation the $x^I$ coordinates are painted such that they coincide with the $y^I$ coordinates. As the fabric deforms (see Figure 3.2), the $x^I$ coordinates remain attached to each material point and displace along with it. We call $y^I$ the *reference coordinates*, and we call the 4D hyperspace the *reference space*. Also, we call $x^I$ the *material coordinates*, because they name material points. At any given moment, each point on the fabric can be specified by either its reference coordinates $y^I$ or material coordinates $x^I$, such that prior to deformation, $y^I = x^I$. These two sets of coordinates are commonly used in Solid Mechanics where "reference coordinates" are also known as "spatial coordinates." The reference space described here is a mathematical construct that helps us build the analogy between Solid Mechanics and General Relativity, but unlike the cosmic fabric itself, it is not necessarily a physical entity. For example, an observer within the fabric is unable to measure directly any attributes of this reference space.

![Material Coordinates versus Reference Coordinates.](https://figures.tgtenev.com/tenev2018-dissertation/fig-material-ref-coords.svg)

**Figure 3.2.** Material coordinates $x^I$ versus reference coordinates $y^I$, before (a) and after (b) deformation of a body $\mathcal{B}$. The material coordinates are attached to each material point and are carried along with the material as it deforms, while reference coordinates remain fixed during deformation. In the diagram, two of the spatial dimensions have been suppressed for clarity.

With respect to the reference space, metric rulers do not change length as the fabric deforms. When the fabric is stretched the number of rulers that can fit between two given points increases. Since metric rulers define the unit of length within the fabric, its stretching is perceived from within the fabric as the expansion of physical space. The term *strain* refers to either the stretch or contraction of a body. The differential straining of the fabric gives rise to its intrinsic curvature and is perceived from within it as the intrinsic curvature of physical space.

The fabric and its enclosing reference space share the same coordinate time $t$. Thus, their respective time coordinates $x^0$ and $y^0$ are such that $x^0 = y^0 \equiv ct$. Note, however, that the proper time $\tau$, which is measured by clocks within the fabric, is not necessarily one and the same as $t$, and that in general, $d\tau/dt \le 1$.

#### Postulates

We postulate the cosmic fabric to be (1) an elastic thin hyperplate, with (2) matter–energy fields as inclusions, and (3) lapse rate of proper time proportional to the shear wave speed $v_s$. Each of these postulates is described and motivated in the sections below.

##### Elastic Thin Hyperplate

Cosmic space is identified with the mid-hypersurface of a hyperplate called the Cosmic Fabric that is thin along the fourth spatial dimension. We imagine the fabric as foliated into 3D hypersurfaces each of which is isotropic and elastic, and each is subject to Hooke's Law (see Figure 3.3). Thus, Hooke's Law (1.2) together with concepts such as stress, strain and the Poisson effect (see Figure 2.2) apply as conventionally understood in Solid Mechanics, because they pertain to individual hypersurfaces, which are 3D bodies.

Because of its correspondence to physical space, the intrinsic curvature, $R^\text{3D}$, of the fabric's mid-hypersurface corresponds to that of three-dimensional (3D) space. Likewise, the intrinsic curvature $R$ of the fabric's world volume corresponds to that of four-dimensional (4D) spacetime. The term "world volume" refers to the four-dimensional shape traced out by an object in spacetime as it advances in time.

The small transverse thickness of the fabric is needed to create resistance to bending, but once such resistance is accounted for, we treat the fabric as essentially a 3D hypersurface that bends within the 4D reference hyperspace. The thickness must be very small so that the fabric can behave as an essentially 3D object at ordinary length scales and be an appropriate analogy of 3D physical space. The thickness itself defines a microscopic length scale at which the behavior of the physical world would have to differ significantly from our ordinary experience. A value equal or comparable to Planck's length $l_p$ meets this criterion. However, the exact value of the thickness is not essential to the model as long as it is small but not vanishingly so.

##### Inclusions

Matter–energy fields behave as inclusions in the fabric inducing *membrane* strains leading to transverse displacements and hence bending (Figure 3.1). The following equation postulates that matter is a source of volumetric strain $\varepsilon$,

$$
\begin{split}
\nabla^2 \varepsilon = -\frac{1}{2} c^2\kappa \rho
\end{split}
\tag{3.2}
$$

where $c$ is the speed of light, $\kappa$ is the Einstein constant, and $\rho$ is the density of matter–energy. The term "membrane" strain (or stress) refers to strains (or stresses) that change in-plane but are uniform across the thickness of the fabric as opposed to bending strains (or stresses) that switch sign through the thickness across the mid-hypersurface.

The mass content of matter, rather than its spatial extent, is what causes the displacement of fabric material. In the context of General Relativity, mass can be related to geometry through its Schwarzschild radius. Thus, one meter of mass is the amount of mass whose Schwarzschild radius is two meters. In the same way, the geometric significance of a matter–energy field, represented by the right-hand side of Equation (3.2), can be understood as the Schwarzschild radius density and $c^2\kappa$ as a units conversion factor. In other words, Equation (3.2) postulates that the Schwarzschild radius density of a matter–energy field is a source of volumetric strain in the cosmic fabric.

The analogy between a body in empty space and an inclusion in the cosmic fabric raises the question of how such an inclusion can move freely through a stiff fabric in the same way as a body can move through empty space. The wave nature of matter, at the length scale of the body's elementary particles, suggests the answer. Just like waves can propagate through a very stiff material, in the same way, elementary particles, which have wave nature, could propagate through the fabric. A detailed treatment of the matter–fabric interaction requires extending our model to include a theory about the nature of matter, which is beyond the scope of this work. Instead, the details of the underlying matter–fabric interactions are abstracted and only the effect is considered, namely, that matter inclusions prescribe a strain field on the fabric. This strain field is then treated as the input to our model (see Chapter V for more details). Representing matter as a strain field within the fabric allows us to aggregate the effects of individual elementary particles over large length scales, and treat planets and stars as individual inclusions.

##### Lapse Rate

The Lapse Rate postulate relates the flow of proper time to the geometry of the cosmic fabric. All matter–matter interactions are mediated by signals propagating in the fabric as shear waves. Therefore, the rate of such interactions varies proportionally to the shear wave speed. A clock placed where fabric waves propagate slower would tick proportionally slower compared to a clock placed where fabric waves propagate faster. Such effect is independent of the clock's design, because the speed of fabric waves affects all matter–matter interactions. In other words, the lapse rate at each point in the fabric, that is how fast clocks tick, is proportional to the speed of shear waves propagating in the fabric when measured in relation to the reference space.

Notice that the shear wave speed will appear to have remained constant when measured by an observer within the fabric, because the reduction in lapse rate exactly compensates for the reduction in shear wave speed. This perceived invariance of the shear wave speed is analogous to the speed of light invariance in General Relativity.

Stated quantitatively, we postulate that the shear wave speed $v_s$ depends on the fabric's volumetric strain $\varepsilon$ as follows,

$$
\begin{split}
v_s = (1 + \varepsilon)^{-1}c
\end{split}
\tag{3.3}
$$

Consequently, the lapse rate, that is the relationship between proper time $\tau$ and coordinate time $t$, is as follows,

$$
\begin{split}
\frac{d \tau}{d t} = (1 + \varepsilon)^{-1}
\end{split}
\tag{3.4}
$$

We motivate the above postulate by connecting the shear wave speed $v_s$ to the mechanical properties of the cosmic fabric. A well-known result from Solid Mechanics is that $v_s = \sqrt{\mu/\rho}$ where $\mu$ and $\rho$ are, respectively, the shear modulus and density of the material. When such material is stretched, its density decreases by a factor of $(1+\varepsilon)$ because the same amount of material now occupies $(1+\varepsilon)$ times more volume. The elastic modulus also changes when the fabric is stretched, but its relationship to strain depends on the internal structure of the material. The choice of modulus–strain relationship becomes a parameter in our model that controls the effect of time dilation. By fixing this relationship to be such that,

$$
\begin{split}
\mu = (1+\varepsilon)^{-3}\mu_0
\end{split}
\tag{3.5}
$$

where $\mu_0$ is the reference modulus of the undeformed fabric, we can recover Equation (3.3). One reason why the modulus changes is that the internal structure of the material weakens under stretch. As discussed in Allison et al. [9], there are materials which exhibit a modulus–strain relationship similar to the one in Equation (3.5).

#### Linearized Spacetime Metric

Under the weak field condition, the metric tensor can be approximated as,

$$
\begin{split}
g_{\mu\nu} = \eta_{\mu\nu} + 2\varepsilon_{\mu\nu}, \quad |\varepsilon_{\mu\nu}| \ll 1
\end{split}
\tag{3.6}
$$

where the term $2\varepsilon_{\mu\nu}$ plays the same role as the small quantities $h_{\mu\nu}$ that are commonly used in General Relativity literature in discussions on Linearized Gravity, such as in Misner et al. [119]. However, note that except under special conditions, $\varepsilon_{\mu\nu}$ does not necessarily comply with the harmonic gauge condition, which is often employed in Linearized Gravity.

From Equation (2.34) we recognize the spatial components $\varepsilon_{ij}$ as the strain of the fabric's mid-hypersurface. The component $\varepsilon_{00}$, as well as the other time components, are related to the flow of proper time. Below, we compute a relationship between $\varepsilon_{00}$ and the fabric's strain.

From Equation (3.4) we can deduce an expression for the time–time component $g_{00}$ of the fabric's spacetime metric $g_{\mu\nu}$ as follows. Applying the metric equation for a stationary point on the fabric,

$$
\begin{split}
-c^2 d\tau^2 &= g_{00} c^2 dt^2 = -(1+\varepsilon)^{-2} c^2 dt^2 \\
\therefore\ g_{00} &= -(1+\varepsilon)^{-2}
\end{split}
\tag{3.7}
$$

Notice that since $(1+\varepsilon)$ is approximately the volumetric expansion of the fabric, then $\det[g_{ij}] \approx \sqrt{1+\varepsilon}$, because $g_{ij}$ is the fabric's Cauchy–Green deformation tensor (see the *Continuum Mechanics* section of Chapter II) and therefore:

$$
\begin{split}
g_{00} = -\frac{1}{\det[g_{ij}]}
\end{split}
\tag{3.8}
$$

Furthermore, for the case of nearly static fields, as assumed here, $g_{0i} = g_{i0} \approx 0$, so from Equation (3.8) follows that,

$$
\begin{split}
\det[g_{\mu\nu}] \approx g_{00}\det[g_{ij}] = -1
\end{split}
\tag{3.9}
$$

Combining Equations (3.7) and (3.6), we note that

$$
\begin{split}
-1 + 2\varepsilon_{00} &\approx g_{00} = -(1+\varepsilon)^{-2} \approx -1 + 2\varepsilon \\
\therefore\ \varepsilon_{00} &= \varepsilon
\end{split}
\tag{3.10}
$$

which, by the application of the Inclusion Postulate (3.2), yields the following result,

$$
\begin{split}
\nabla^2 \varepsilon_{00} = \nabla^2 \varepsilon = -\frac{1}{2} c^2\kappa \rho
\end{split}
\tag{3.11}
$$

#### Bending Energy Density

Rather than treating the fabric as a 4D hyperplate, it is convenient to approximate it as a 3D hypersurface. This can be accomplished once we have averaged the fabric's elastic energy density $U$ across its thickness and assigned it to its mid-hypersurface. At that point, we can use the fabric's mid-hypersurface as a proxy for the whole fabric in further calculations.

![Hypersurfaces.](https://figures.tgtenev.com/tenev2018-dissertation/fig-hypersurfaces.svg)

**Figure 3.3.** Hypersurfaces. The cosmic fabric is treated as a stack of three-dimensional hypersurfaces $\Sigma_{\xi}$ each parameterized by $\xi \equiv x^4 = \text{const}$, and $L$ is its thickness.

To compute $U$, we adapt the work of Efrati et al. [46] concerning the bending of conventional thin plates. For ease of notation, let $\xi \equiv x^4$ denote the coordinate offset from the mid-hypersurface of the fabric. The fabric is regarded as foliated into infinitely many hypersurfaces $\Sigma_\xi$ each parameterized by $\xi = \text{const.}$ (Figure 3.3). We carry over the simplifying assumption from Kirchhoff–Love thin plate theory [3] to thin hyperplates and assume that the set of material points along any given hypersurface that were along a normal prior to bending remain along the normal after bending.

It can be shown [46] that the metric $g_{ij} = g_{ij}(\xi)$ of each $\Sigma_{\xi}$ takes the form,

$$
\begin{split}
g_{ij} = a_{ij} - 2b_{ij} \xi + c_{ij} \xi^2
\end{split}
\tag{3.12}
$$

where $a_{ij} = a_{ij}(x^i)$ and $b_{ij} = b_{ij}(x^i)$ are, respectively, the first and second fundamental forms of the mid-hypersurface, and $c_{ij} = a^{kl}b_{ik}b_{jl}$.

The total elastic energy density of a linearly elastic solid is half of the inner product of its stress and strain tensors. The dependence of the cosmic fabric's modulus on strain adds a degree of nonlinearity, which would have resulted in a correction factor of about $(1+\varepsilon)^{-2}$. However, under the small strain conditions, $\varepsilon \ll 1$, allowing us to approximate $(1+\varepsilon)^{-2} \approx 1$, and thus to neglect the nonlinear effect. Applying Hooke's Law (1.2), the total elastic energy density $U_{\xi}$ of each hypersurface $\Sigma_{\xi}$ is given by,

$$
\begin{split}
U_{\xi} &= \frac{1}{2} \sigma^{ij} \varepsilon_{ij} = \frac{1}{2} C^{ijkl}\varepsilon_{ij}\varepsilon_{kl} \\
& \text{such that} \quad C^{ijkl} \equiv \frac{Y}{1+\nu} \left(\frac{\nu}{1-2\nu} g^{ij}g^{kl} + g^{ik}g^{jl}\right)
\end{split}
\tag{3.13}
$$

where $\sigma_{ij} = \sigma_{ij}(\xi)$ and $\varepsilon_{ij} = \varepsilon_{ij}(\xi)$ are, respectively, the stress and strain at each hypersurface $\Sigma_{\xi}$. Note that here and for the remainder of the chapter, we compute the elastic energy density with respect to the coordinate volume as opposed to the proper volume.

Next, we compute the total elastic energy density $U$ averaged across the fabric's thickness, and we separate it into a bending term $U_\text{B}$ and a membrane stretch term $U_\text{M}$. For this purpose, we split the strain at each surface, $\varepsilon_{ij}$, into a membrane strain $\varepsilon^\text{M}_{ij}$ and a bending strain $\varepsilon^\text{B}_{ij}$ as follows:

$$
\begin{split}
\varepsilon_{ij} & = \frac{1}{2}(g_{ij} - \delta_{ij}) = \varepsilon^\text{M}_{ij} + \varepsilon^\text{B}_{ij} \\
\varepsilon^\text{M}_{ij} & = \frac{1}{2}(a_{ij} - \delta_{ij}) \\
\varepsilon^\text{B}_{ij} & = -b_{ij}\xi + \mathcal{O}(b^2\xi^2)
\end{split}
\tag{3.14}
$$

$$
\begin{split}
U &= \frac{1}{L} \int_{-\frac{L}{2}}^{\frac{L}{2}} U_{\xi}\, \mathrm{d}\xi = \frac{1}{2L} \int_{-\frac{L}{2}}^{\frac{L}{2}} C^{ijkl}(\varepsilon^\text{M}_{ij}\varepsilon^\text{M}_{kl} + \varepsilon^\text{B}_{ij}\varepsilon^\text{B}_{kl} + [\varepsilon^\text{M}_{ij}\varepsilon^\text{B}_{kl} + \varepsilon^\text{B}_{ij}\varepsilon^\text{M}_{kl}])\, \mathrm{d}\xi \\
& = U_\text{M} + U_\text{B} \\
U_\text{M} &= \frac{1}{2L} \int_{-\frac{L}{2}}^{\frac{L}{2}} C^{ijkl}\varepsilon^\text{M}_{ij}\varepsilon^\text{M}_{kl}\, \mathrm{d}\xi \\
U_\text{B} &= \frac{1}{2L} \int_{-\frac{L}{2}}^{\frac{L}{2}} C^{ijkl}\varepsilon^\text{B}_{ij}\varepsilon^\text{B}_{kl}\, \mathrm{d}\xi
\end{split}
\tag{3.15}
$$

The term $\mathcal{O}(b^2\xi^2)$ stands for an expression whose order of magnitude is comparable to the square of the elements $b_{ij}$ multiplied by $\xi^2$. The mixed terms inside the square brackets in Equation (3.15) vanish under integration because the bending strain reverses sign across the mid-hypersurface; hence $\varepsilon^\text{B}_{ij} = \varepsilon^\text{B}_{ij}(\xi)$ is an odd function, while $\varepsilon^\text{M}_{ij} = \varepsilon^\text{M}_{ij}(\xi)$ is an even function.

For the remainder of this subsection, we focus on evaluating the term $U_\text{B}$. The term $U_\text{M}$ will be addressed in the following subsection where we show that it vanishes under appropriately chosen material properties and deformation kinematics. Also, Chapter V shows that this term vanishes in general once we account for the discrete substructure of matter.

Evaluating $U_\text{B}$ from Equation (3.15), we obtain the following:

$$
\begin{split}
U_\text{B} = L^2C^{ijkl}\left[b_{ij}b_{kl} + \mathcal{O}(b^3 L)\right]
\end{split}
\tag{3.16}
$$

The extrinsic curvature terms $b_{ij}$ have magnitudes comparable to the inverse of the curvature radius. The curvature radius is much greater than the thickness of the fabric, so $\mathcal{O}(b L) \ll 1$, which allows us to ignore the term $\mathcal{O}(b^3 L)$ in the above expression. Using the identity $R^\text{3D}_{lijk} = b_{ik}b_{jl} - b_{ij}b_{kl}$, where $R^\text{3D}_{lijk}$ is the Riemann curvature tensor of the mid-hypersurface, and setting $\mathcal{O}(b^3 L) = 0$, we can express $U_\text{B}$ in terms of the intrinsic three-dimensional spatial curvature $R^\text{3D}$ as follows,

$$
\begin{split}
U_\text{B} = -\frac{L^2 Y}{24(1+\nu)} \left( R^\text{3D} + \frac{1-\nu}{1-2\nu} b^i_i b^k_k \right)
\end{split}
\tag{3.17}
$$

The Poisson's ratio of the cosmic fabric had remained unspecified as a freedom to be fixed at a later time such as now. In order for $U_\text{B}$ to be physical, it should not depend on the extrinsic curvature $b_{ij}$ that is not already incorporated into the intrinsic curvature $R^\text{3D}$. The $b^i_i b^k_k$ term would vanish if we chose Poisson's ratio $\nu = 1$. In this case, the bending energy becomes as follows,

$$
\begin{split}
U_\text{B} = - \frac{YL^2}{48} R^\text{3D}
\end{split}
\tag{3.18}
$$

subject to the following condition,

$$
\begin{split}
\nu = 1
\end{split}
\tag{3.19}
$$

#### Membrane Energy Density

We now show that for any given small-strain deformed configuration, we can identify a material displacement field that results in no membrane energy. Consequently, we conclude that the bending energy $U_\text{B}$ is the only contribution to the total elastic energy of the fabric for the case of nearly static fields. Since General Relativity (GR) is only concerned with the curvature of the deformed body, in developing the material analogy of GR we have freedom to prescribe a specific material displacement field for the deformation.

Let us consider a displacement field where each point of the mid-hypersurface, $x^4 = 0$, of the fabric is displaced within a reference space by the amount $w = w(x^i)$ along a geodesic normal to the hypersurface. It should be evident that using such a displacement field, one can deform a flat body into any given shape that represents a small deviation from flatness and does not contain folds. Let $y^I$ be the coordinates in reference space of the position to which the material point at $x^i$ is displaced. Thus, $y^i = x^i$ and $y^4 = w$. The metric tensor of the deformed hypersurface can be computed from the dot product of the position differentials as follows,

$$
\begin{split}
g_{ij} & = \partial_i y^K \partial_j y^K = \partial_i x^k \partial_j x^k + \partial_i w \partial_j w = \delta_{ij} + \partial_i w \partial_j w \\
\therefore\ \varepsilon_{ij} & = \frac{1}{2}(g_{ij} - \delta_{ij}) = \frac{1}{2} \partial_i w \partial_j w
\end{split}
\tag{3.20}
$$

Using the formula for elastic energy density, $U_\text{M} = \sigma^{kl}\varepsilon_{kl}/2$, and applying Hooke's Law (1.2) to Equation (3.20) with $\nu = 1$, we find that,

$$
\begin{split}
U_\text{M} & \propto \sigma^{kl}\varepsilon_{kl} \propto (g^{ik}g^{jl} - g^{ij}g^{kl})\varepsilon_{ij}\varepsilon_{kl} = \\
& = \varepsilon^k_j \varepsilon^j_k - \varepsilon^j_j \varepsilon^k_k \propto \partial^k w \partial_j w \partial^j w \partial_k w - \partial^j w \partial_j w \partial^k w \partial_k w = 0 \\
\therefore\ U_\text{M} & = 0
\end{split}
\tag{3.21}
$$

Hence, fixing the fabric's deformation to material displacements only along the hypersurface normals is a valid approximation under the assumption of nearly static fields. In such cases, the reason for the deformation would have been to geometrically accommodate inclusions by bending into the $y^4$ dimension. Once bending has taken place, the material points of the fabric can shift within the plane of the fabric to minimize its membrane energy without affecting the geometrical constraints imposed by the inclusion. For nearly static situations, we have shown that the membrane energy can be minimized to where it vanishes. In such cases, the net displacement would have taken the form described in this subsection.

#### Lagrangian Density

Ignoring the kinetic energy component, under the simplifying assumption of nearly static fields, the Lagrangian density is $\mathcal{L}_\text{F} = - U_\text{B} \sqrt{|g|} \propto R^\text{3D} \sqrt{|g|}$, where $g \equiv \det[g_{\mu\nu}]$. The factor $\sqrt{|g|}$, which converts from a coordinate volume to a proper volume, is needed for $\mathcal{L}_\text{F}$ to be a tensor density, which requires invariance under coordinate transformations.

Next, we derive an expression for $\mathcal{L}_\text{F}$ in terms of the Ricci curvature $R$ of the fabric's world volume. According to the gauge-invariant linearized expression for $R$ per Misner et al. [119],

$$
\begin{split}
R & = 2\left( -\partial_\alpha \partial^\alpha \varepsilon^\mu_\mu + \partial_{\alpha\mu}\varepsilon^{\alpha\mu} \right) \\
& = 2\left( -\partial_k \partial^k \varepsilon^i_i + \partial_{ik} \varepsilon^{ik} - \partial_k \partial^k \varepsilon^0_0 - \partial_0 \partial^0 \varepsilon^k_k + 2\partial^{0k}\varepsilon_{0k} \right) \\
& \approx R^\text{3D} + 2\nabla^2 \varepsilon_{00}
\end{split}
\tag{3.22}
$$

In the last step of the above derivation, we have recognized that the purely spatial terms add up to the gauge-independent linearized expression for $R^\text{3D}$. Furthermore, the terms differentiated with respect to $x^0$ are negligible because of the nearly static fields assumption. Also, lowering or raising a single $0$ index, which is accomplished using $\eta_{\mu\nu}$, changes the sign of the term.

In free space $\nabla^2 \varepsilon_{00} = 0$ per Equation (3.11). Consequently, after combining Equations (3.18) and (3.22), we finally arrive at,

$$
\begin{split}
\mathcal{L}_\text{F} = -U_\text{B} \sqrt{|g|} = \frac{YL^2}{48} R \sqrt{|g|}
\end{split}
\tag{3.23}
$$

which has the same form as the Einstein–Hilbert Lagrangian density. The resulting action is simply the integral of the Lagrangian density over coordinate spacetime, namely,

$$
\begin{split}
\mathcal{S}_\text{F} = \int \mathcal{L}_\text{F}\, \mathrm{d}x^4 = \frac{YL^2}{48} \int R\sqrt{|g|}\,\mathrm{d}x^4
\end{split}
\tag{3.24}
$$

which is what we had set out to demonstrate as stated earlier per Equation (3.1).

### Discussion

In the previous sections, we postulated a material body, which we named the "cosmic fabric," whose constitutive behavior outside of inclusions is analogous to the behavior of gravity, and have shown the sequential mathematical development. For the analogy to be useful, it should allow us to map between notions in Solid Mechanics and General Relativity. Such a mapping is possible on the basis of identifying the fabric Lagrangian density $\mathcal{L}_\text{F}$ with the Lagrangian density from the Einstein–Hilbert action, $\mathcal{L}_\text{EH}$, as applying to free space. Specifically,

$$
\begin{split}
\mathcal{L}_\text{F} = \frac{YL^2}{48}R\sqrt{|g|} = \mathcal{L}_\text{EH} = \frac{1}{2\kappa}R\sqrt{|g|}
\end{split}
\tag{3.25}
$$

where $\kappa$ is the Einstein constant.

In the subsections below, we discuss the correspondence between mechanical properties of the cosmic fabric and known properties of gravity.

#### Fabric Strain and Gravitational Potential

It is a well-known result from Linearized Gravity that given the choice of coordinates adopted here, the classical gravitational potential $\Phi$ is related to the time–time component of the metric in the following way [119],

$$
\begin{split}
\Phi/c^2 = -\left(g_{00} - \eta_{00}\right)/2
\end{split}
\tag{3.26}
$$

Combined with Equation (3.10) the above becomes,

$$
\begin{split}
\Phi/c^2 = -\left(g_{00} + 1\right)/2 = -\varepsilon_{00} = -\varepsilon
\end{split}
\tag{3.27}
$$

In other words, the gravitational potential corresponds to the volumetric expansion of the fabric.

#### Poisson's Ratio and the Substructure of Space

Known materials with a Poisson's ratio of $\nu = 1$ have a fibrous substructure, which suggests that the cosmic fabric is, in fact, a fabric! For $\nu = 1$, the bulk modulus is $K = Y/[3(1-2\nu)] < 0$. A negative bulk modulus means that compressing the fabric results in an overall increase of the material volume and vice versa. Although such behavior is unusual for most conventional materials, there are recently discovered *compressive dilatant* [142] and *stretch densifying* [18] materials, for which $\nu=1$ in either compression or tension, respectively. Compressive dilatant materials are artificially manufactured and their substructure consists of entangled stiff wires. Stretch densifying materials have textile-like substructure comprised of woven threads each consisting of twisted fibers.

#### Fabric Vibrations and Gravitational Waves

Having Poisson's ratio $\nu = 1$ also implies that there can only be transverse (shear) waves in the fabric but no longitudinal (pressure) waves. The shear modulus $\mu$ and the p-wave modulus $M$ are as follows,

$$
\begin{split}
\mu & = \frac{Y}{2(1+\nu )} = \frac{Y}{4} \\
M &= Y \frac{1-\nu}{(1-2\nu)(1+\nu)} = 0
\end{split}
\tag{3.28}
$$

implying that the transverse (shear) wave velocity $v_s = \sqrt{\mu/\rho_\text{F}} \neq 0$, while the longitudinal (pressure) wave velocity $v_p = \sqrt{M/\rho_\text{F}} = 0$, where $\rho_\text{F}$ is the density of the fabric. This result shows why the speed of light is the fastest entity of the universe, given that a longitudinal wave is typically faster than a shear wave. For a shear wave to be the fastest, the Poisson's Ratio must be 1. This conclusion is consistent with observations, because all known waves that propagate in free space, such as gravity or electromagnetic waves, are transverse. The section *Gravitational Waves* explores in detail the mechanical analogy of gravity waves.

#### Elastic Modulus and Density of Free Space

From the result in Equation (3.25), the fabric's elastic modulus $Y$ could be computed given an estimate for the fabric's thickness $L$. As reasoned in the *Elastic Thin Hyperplate* section, Planck's length $l_p \equiv \sqrt{\hbar G/c^3}$ is a suitable estimate for $L$, where $\hbar$ is the reduced Planck's constant. Assuming $L \sim l_p$, we can estimate $Y$ to be,

$$
\begin{split}
Y \sim \frac{24}{l^2_p \kappa} = 4.4 \times 10^{113}\ \text{N m}^{-2}
\end{split}
\tag{3.29}
$$

The density of the fabric $\rho_\text{F}$ is related to the wave speed and shear modulus, as shown in the *Fabric Vibrations and Gravitational Waves* section, and can now be computed,

$$
\begin{split}
\rho_\text{F} = \frac{\mu}{c^2} = \frac{Y}{4c^2} \sim 1.3 \times 10^{96}\ \mathrm{kg}\,\mathrm{m}^{-3}
\end{split}
\tag{3.30}
$$

In accordance with the Cosmic Fabric analogy, the density of the fabric corresponds to the density of free space, which is also known as the zero-point energy density. The computed value for $\rho_\text{F}$ agrees to an order of magnitude with the predictions of Quantum Field Theory ($\sim 10^{96}\ \mathrm{kg}\,\mathrm{m}^{-3}$) for the energy density of free space [146]. Note that the predictions of Quantum Field Theory are also based on using Planck's length $l_p$ as a length-scale parameter.

#### Gravitational Waves

Let us consider whether shear waves in the fabric are analogous to gravitational waves. Such an analogy depends on demonstrating that the fabric's behavior parallels that of spacetime for fast changing fields as well. We leave the rigorous proof as future work, and for the rest of this subsection we assume that the fabric's behavior implied by the Lagrangian (3.23) also holds for fast changing fields. Based on this assumption, we proceed to investigate in-plane shear waves propagating through the fabric and their correspondence to gravitational waves.

First, we show that if static fields are negligible and in the absence of torsion, then the strain $\varepsilon_{\mu\nu}$ satisfies the harmonic gauge condition, $\partial_\alpha \varepsilon^{\mu\alpha} = (1/2)\partial^\mu \varepsilon^\alpha_\alpha$. For shear waves, $\varepsilon = 0$, and by Equation (3.10), $\varepsilon_{00} = 0$, implying that $\varepsilon^{\alpha}_{\alpha} = 0$. Therefore, proving the harmonic gauge condition is reduced to demonstrating that $\partial_\alpha \varepsilon^{\mu\alpha} = 0$. Furthermore, the shear time–space components must vanish, $\varepsilon_{4j} = \varepsilon_{j4} = 0 = \varepsilon_{0j} = \varepsilon_{j0}$, because we are assuming negligible static fields and in-plane shear waves. Therefore, in order to prove that the harmonic gauge condition holds, we just need to show that $\partial_k \varepsilon_{ik} = 0$. Let $u_i$ be the material displacement field. In terms of the displacement field, the strain is $2\varepsilon_{ij} = \partial_j u_{i} + \partial_i u_{j}$, and so,

$$
\begin{split}
2\varepsilon_{ij} &= 2\partial_i u_j + [\partial_j u_{i} - \partial_i u_{j}] \\
2\partial_k \varepsilon_{ik} &= 2\partial_{ki} u_{k} + \partial_k [\partial_k u_{i} - \partial_i u_{k}]
\end{split}
\tag{3.31}
$$

But $\partial_{ki} u_{k} = 0$ since $\varepsilon_{kk} = \partial_k u_{k} = 0$. The difference in the square brackets corresponds to material torsion and must vanish too, so,

$$
\begin{split}
\partial_k \varepsilon_{ik} &= 0 \\
\therefore\ \partial_\alpha \varepsilon^{\mu\alpha} &= (1/2)\partial^\mu \varepsilon^\alpha_\alpha
\end{split}
\tag{3.32}
$$

Since $\varepsilon_{\mu\nu}$ satisfies the harmonic gauge condition, we can apply the linearized approximation for the Ricci tensor,

$$
\begin{split}
R_{\mu\nu} \approx -\partial^\alpha \partial_\alpha \varepsilon_{\mu\nu}
\end{split}
\tag{3.33}
$$

After substituting into the Einstein Field Equations (1.3), and taking into account that $R \approx \partial^\mu \partial_\mu \varepsilon^\alpha_\alpha = 0$, and that in empty space $T_{\mu\nu} = 0$, we arrive at,

$$
\begin{split}
\partial^\alpha \partial_\alpha \varepsilon_{\mu\nu} & = \nabla^2 \varepsilon_{ij} - \partial_{00} \varepsilon_{ij} = 0 \\
\therefore\ & \partial_{00} \varepsilon_{ij} = \nabla^2 \varepsilon_{ij}
\end{split}
\tag{3.34}
$$

which is a wave equation with solutions that are traveling waves at the speed of light $c$. To see this clearly, let us re-write Equation (3.34) in terms of the coordinate time variable $t$, where $x^0 \equiv ct$,

$$
\begin{split}
\frac{1}{c^2} \frac{\partial^2}{ \partial t^2} \varepsilon_{ij} = \nabla^2 \varepsilon_{ij}
\end{split}
\tag{3.35}
$$

The above equation can be related to the Solid Mechanics equation for the propagation of a shear wave in an elastic medium with density $\rho_\text{F}$ and shear modulus $\mu$. In the absence of body forces, the equation of motion is the following,

$$
\begin{split}
\rho_\text{F} \frac{\partial^2}{\partial t^2} u_i = \partial_j \sigma_{ij}
\end{split}
\tag{3.36}
$$

Applying Hooke's Law (1.2) and recognizing that $\varepsilon_{ij} = (\partial_j u_{i} + \partial_i u_{j})/2$, $\mu = Y/[2(\nu+1)]$, and $\partial_k u_{k} = \varepsilon_{kk} = 0$, we arrive at,

$$
\begin{split}
\rho_\text{F} \frac{\partial^2}{\partial t^2} u_i & = \mu \nabla^2 u_i \\
\rho_\text{F} \frac{\partial^2}{\partial t^2} \left(\partial_j u_{i} + \partial_i u_{j}\right) & = \mu \nabla^2 \left( \partial_j u_{i} + \partial_i u_{j} \right) \\
\therefore\ \rho_\text{F} \frac{\partial^2}{\partial t^2} \varepsilon_{ij} & = \mu \nabla^2 \varepsilon_{ij}
\end{split}
\tag{3.37}
$$

The parallel between Equations (3.35) and (3.37) confirms that gravitational waves are analogous to shear waves propagating in a solid material and that furthermore the speed of propagation, which is the speed of light $c$, is related to the shear modulus and density of the medium per $c^2 = \mu/\rho_\text{F}$.

Although Equation (3.34) suggests that there are ostensibly ten strain components, $\varepsilon_{\alpha\beta}$, oscillating independently, in reality only two are independent and the rest are coupled to the two. To show this, consider a wave propagating along the $x^3$ direction. It is necessary that $\varepsilon_{3\alpha} = \varepsilon_{\alpha 3} = 0$ for the wave to be a shear wave. Furthermore, as shown previously, $\varepsilon_{00} = \varepsilon = 0$ and $\varepsilon_{j0} = \varepsilon_{0j}=0$. Finally, we have $\varepsilon = \varepsilon_{11} + \varepsilon_{22} = 0$, because $\varepsilon_{33} = 0$ already. Therefore,

$$
\begin{split}
\varepsilon_{11} &= -\varepsilon_{22} \\
\varepsilon_{12} &= \varepsilon_{21}
\end{split}
\tag{3.38}
$$

are the only two independent degrees of freedom left, which implies just two types of wave polarizations. The fact that Equation (3.38) is in terms of the material strain, which has a definite physical meaning, ensures that the waves must also be physical as opposed to being mere coordinate displacements. This result, derived from a Solid Mechanic's perspective, is consistent with the analogous result from General Relativity about the polarization of gravitational waves [119].

### Summary and Conclusion

We showed that the behavior of spacetime per Einstein's Field Equations (1.3) is analogous to that of an appropriately chosen material body termed the "cosmic fabric" that is governed by a simple constitutive relation per Hooke's Law (1.2). In the *Formulation of the Cosmic Fabric Model of Gravity* section, we postulated several basic properties of the fabric and how they correspond to physical space and matter in space. Constitutive properties, such as the Poisson ratio and the elastic modulus' dependence on strain, were left unconstrained as model parameters. These were subsequently chosen such that the Lagrangian of the fabric could take the form of the Einstein–Hilbert Lagrangian of General Relativity. After the Cosmic Fabric model was calibrated in this way, the *Discussion* section applied it to interpret various properties of gravity in terms of the fabric's mechanics and vice versa. To a great extent, the interpretations seemed physically meaningful from both perspectives of General Relativity and Solid Mechanics. Table 3.1 summarizes the correspondence between concepts from one field to analogous concepts in the other.

**Table 3.1.** Comparison between the General Relativity and Solid Mechanics Perspectives.

| General Relativity Perspective | Solid Mechanics Perspective |
|---|---|
| Physical space | Mid-hypersurface of a hyperplate called "cosmic fabric" |
| Spacetime | The world volume of the cosmic fabric's mid-hypersurface |
| Intrinsic curvature of physical space | Intrinsic curvature of the fabric's mid-hypersurface |
| Intrinsic curvature of spacetime | Intrinsic curvature of the fabric's world volume |
| Gravitational potential $\Phi$ | Volumetric strain $\varepsilon$, where $\varepsilon = -\Phi/c^2$ |
| Gravitational waves | Shear waves traveling at the speed of light |
| Matter curves spacetime. | Matter induces prescribed strain causing the fabric to bend and time lapse to slow down. |
| Action integral in free space, $\mathcal{S} = \frac{1}{2\kappa} \int R\sqrt{|g|}\,d^4x$ | Action integral outside of inclusions, $\mathcal{S} = \frac{L^2 Y}{48} \int R\sqrt{|g|}\,d^4x$ |
| Constants of Nature: $G,\ \hbar,\ c$ | Elastic constants: $Y = 6c^7/2\pi\hbar G^2,\ \nu=1$ |

The research presented in this chapter suggests an equivalence between postulating the field equations of General Relativity and postulating a cosmic fabric having material-like properties as described here. We believe that these are two different approaches for studying the same underlying reality. The Cosmic Fabric model introduces a new paradigm for interpreting cosmological observations based on well-established ideas from Solid Mechanics.

---

## IV. Recovering Relativity from the Cosmic Fabric Model

Whereas in Chapter III we showed that the Cosmic Fabric model is a valid analogy to General Relativity for nearly static observers, herein we extend the analogy to include moving observers as well. Although the model ostensibly defines a hyperplane of absolute simultaneity and therefore a preferred reference frame, we demonstrate that to both moving and stationary observers alike, such a preferred reference frame remains undetectable at continuum length scales. In the *Discussion* section, we mention briefly how the Cosmic Fabric model is conducive to generalizations outside of the continuum length scale. The essential contribution of this chapter is to expand the descriptive power of the model to include moving observers and show that all reference frames are phenomenologically equivalent with one another, which is to say that the Principle of Relativity applies within the cosmic fabric. Consequently, we conclude that the model has at least the descriptive power of Special Relativity (SR) and Lorentz Aether Theory (LET), and also, from Chapter III, the descriptive power of General Relativity (GR) for the case of weak gravity. Therefore, the work herein contributes toward a material model of space that generalizes LET similarly to how GR generalized SR.

The remainder of this chapter is organized as follows: In the *Invariance of the Speed of Signals* section, we show that the speed of signal propagation within the fabric, which we had previously identified with the speed of light in free space, is invariant for all observers within all reference frames in the fabric. This result recovers the Second Postulate of Special Relativity, which states that the speed of light is invariant for all inertial reference frames. In the *Lorentz Transformations* section, we derive the transformations between the coordinates of a stationary and a moving observer, which we recognize as the Lorentz transformations [86, 87, 97, 98]. Because these apply in like manner between any two inertial reference frames and not only between a stationary and a moving reference frame, it follows that no reference frame can be singled out as special by an observer within the fabric. Consequently, we recover the First Postulate of Special Relativity [48], which states that all physical laws are the same in all inertial reference frames. In the *Discussion* section we discuss how the Cosmic Fabric model compares with Special Relativity and Lorentz Aether Theory, and we conclude in the *Conclusion* section.

### Invariance of the Speed of Signals

In this section, we show that the speed of signal propagation is invariant with respect to any inertial reference frame for any observer within the fabric. First, we demonstrate the invariance for stationary observers at different locations. Next, we show that the invariance also applies for a moving and a stationary observer at a given location. The combination of these two results leads to the desired conclusion about the speed of a signal's invariance.

#### Stationary Observers at Different Locations

The formulation of the Cosmic Fabric model (see Chapter III) postulates that the fabric mediates all matter–matter interactions via signals that travel as mechanical disturbances within it. It is convenient to consider the fabric as immersed within a four-dimensional reference hyperspace (not necessarily physical), which also has its own time coordinate (see Figure 4.1). Such a reference space is somewhat similar to Dicke's "Newtonian coordinate system" [41], except in the context of four spatial dimensions. From the perspective of this reference space, the rate of matter–matter interactions is proportional to the speed of signal propagation. Consequently, the rate of clock ticks, that is the time lapse rate, is also proportional to the speed of signal propagation.

![Stationary observers.](https://figures.tgtenev.com/tenev2018-dissertation/fig-stationary-observers.svg)

**Figure 4.1.** Stationary observers $A$ and $B$ located within the cosmic fabric and measuring proper times $\tau_a$ and $\tau_b$, respectively. The fabric is considered immersed in a four-dimensional hyperspace (not necessarily physical) with coordinates $(t, y^1, y^2, y^3, y^4)$. The third spatial dimension is suppressed for clarity.

Although signals need not propagate with uniform speed when measured with respect to the enclosing reference space, nevertheless their speed will appear constant from the perspective of observers within the fabric for the following reason: A clock placed where fabric signals propagate relatively slow in relation to the enclosing reference space will also tick slow. Therefore, to an observer within the fabric, the signal speed would appear to have remained unchanged, because the slowdown of the clock used to measure the signal speed would exactly compensate for the reduction of said speed. Consequently, the signal speed within the fabric appears to be invariant for any stationary observer. In the description of the Cosmic Fabric model, we had identified the speed of signal propagation with the speed of light in free space $c$. Below we provide an algebraic derivation of this result.

Let $v_a$ and $v_b$ be, respectively, the speeds of signal propagation at locations $A$ and $B$ of the fabric measured in relation to the enclosing reference space. By definition, $v_a = dl_a/dt$, where $dl_a$ is a distance element at location $A$, and $dt$ is the travel time, reckoned with respect to the enclosing reference space. According to the Time Lapse postulate of the Cosmic Fabric model (see the *Lapse Rate* section of Chapter III), $d\tau_a/dt = \left(\frac{1}{v_0}\right) v_a$, where $\left(\frac{1}{v_0}\right)$ is a constant of proportionality. Therefore, the speed of signal propagation $c_a$ measured at location $A$ within the fabric is,

$$
\begin{split}
c_a = \frac{dl_a}{d\tau_a} = \frac{dl_a}{dt}\frac{dt}{d\tau_a} = v_a\frac{v_0}{v_a} = v_0.
\end{split}
\tag{4.1}
$$

In the same way, we can show that the speed of signal propagation $c_b$ at location $B$ is $c_b = v_0$. Thus, we conclude that the speed of signal propagation at both locations $A$ and $B$ is one and the same with respect to stationary observers in the fabric. The magnitude of this speed can be identified with the speed of light in free space $c$:

$$
\begin{split}
c_a = c_b = v_0 = c.
\end{split}
\tag{4.2}
$$

Since locations $A$ and $B$ were arbitrary, it follows that the speed of signal propagation is invariant for all stationary observers within the fabric.

#### Moving Observer

We now consider the situation of an observer at a given location moving with velocity $v$ with respect to the fabric (see Figure 4.2). Let $\tau'$ and $\tau$ represent the time measured by the moving observer and a stationary observer at the same location, respectively. As illustrated in Figure 4.2, from the Pythagorean Theorem follows that the effective signal speed in any orientation transverse to the motion of the observer is $\sqrt{c^2 - v^2}$. Therefore, by the Time Lapse postulate of the Cosmic Fabric model we conclude that the moving observer's clocks must tick slower by a factor of $(\sqrt{c^2 - v^2})/c = \sqrt{1 - \beta^2}$ where $\beta \equiv v/c$. In other words,

$$
\begin{split}
\frac{d\tau'}{d\tau} = \sqrt{1 - \beta^2},\quad \beta \equiv \frac{v}{c}
\end{split}
\tag{4.3}
$$

We considered the signal speed in a transverse orientation to avoid any direction-specific effects, such as length contraction.

![Moving observer measuring light speed in transverse orientation.](https://figures.tgtenev.com/tenev2018-dissertation/fig-moving-observer.svg)

**Figure 4.2.** An observer moving with velocity $v$ with respect to the fabric. The observer measures the round-trip time of a light signal traveling a fixed distance in a direction transverse to the motion. The situation is represented from the viewpoint of the moving observer (a) and a stationary observer (b), respectively. The effective transverse signal propagation speed is $\sqrt{c^2 - v^2}$.

Next, we consider how lengths are affected along the orientation of motion. We measure lengths by the round-trip time of signals (see Figure 4.3). In all of our thought experiments we use round-trip times to avoid complications due to clock synchronization. Let $dl$ be the rest length of a rod oriented along the direction of motion. From the perspective of the stationary observer, the total time $d\tau$ it takes for the signal to travel from one end of the rod and back is as follows,

$$
\begin{split}
d\tau = \frac{dl}{c + v} + \frac{dl}{c - v} = 2\frac{dl}{c}\frac{1}{1-\beta^2}, \quad \beta \equiv \frac{v}{c}.
\end{split}
\tag{4.4}
$$

From the viewpoint of the moving observer, per Equation (4.3) the round-trip travel time $d\tau'$ is as follows,

$$
\begin{split}
d\tau' = d\tau\sqrt{1 - \beta^2} = 2\frac{dl}{c}\frac{1}{\sqrt{1 - \beta^2}}
\end{split}
\tag{4.5}
$$

The above equation can be interpreted in one of two ways: either the moving observer perceives the round-trip signal speed to differ in the direction of motion compared to any transverse direction, or the rod's length changed such that the new length $dl'$ is $dl' = dl/\sqrt{1-\beta^2}$. The former possibility implies that signal speed, and therefore light speed, would be anisotropic. The Michelson–Morley experiment [113] was designed to measure such anisotropy, and its negative outcome rules out the former possibility. Therefore, one must conclude that measuring rods oriented along the motion of the reference frame experience length change per,

$$
\begin{split}
dl' = \frac{dl}{\sqrt{1 - \beta^2}}.
\end{split}
\tag{4.6}
$$

![Moving observer measuring light speed along the direction of motion.](https://figures.tgtenev.com/tenev2018-dissertation/fig-moving-observer-2.svg)

**Figure 4.3.** A rod $AB$ with rest length $dl$, moving with velocity $v$, and aligned along the orientation of motion. A comoving observer is measuring the rod by timing the round-trip signal sent from one end of the rod to the other and back. The situation is represented from the viewpoint of a stationary observer.

Due to the combined effects of time dilation and length contraction, the signal speed $c$ is measured to be one and the same by both the moving and stationary observers. Thus,

$$
\begin{split}
\frac{dl}{d\tau} = \frac{dl'}{d\tau'} = c
\end{split}
\tag{4.7}
$$

The above result is the same as what Lorentz [96, 97, 98] concluded in constructing his aether theory, except he considered only the speed of light as opposed to a more general speed of signals as per the Cosmic Fabric model. In the Cosmic Fabric model, the speed of signal propagation is more fundamental than the speed of light, because it controls all matter–matter interactions and not just those pertaining to electromagnetic phenomena. This is why the variation of speed of signal propagation affects not only the rate of clock ticks but also the length of measuring rods.

### Lorentz Transformations

Next, we recover the Lorentz transformations from the speed of light invariance and from basic considerations of spatial symmetry. The method is detailed below.

Figure 4.4 shows the spacetime coordinates of an unprimed and primed observer, where the primed observer travels with velocity $v$ with respect to the unprimed one. Let $\beta \equiv v/c$ be the scaled relative speed. The origin represents an event when $x = x' = 0$ and $c\tau = c\tau' = 0$. Because the time coordinates are scaled by $c$, a photon emitted at the origin in the positive $x$ direction will traverse a straight line trajectory that bisects the angle between the unprimed axes. A particle stationary at the primed origin traverses a straight line trajectory of slope $1/\beta$ with respect to the unprimed coordinates. Therefore, the primed time axis must have a slope $1/\beta$ with respect to the unprimed coordinates. Due to the speed of light invariance, the trajectory of the aforementioned photon must also bisect the angle between the primed axes, and consequently, the primed space axis must have a slope of $\beta$ with respect to the unprimed coordinates.

![Coordinate transformation between a moving and a stationary observer.](https://figures.tgtenev.com/tenev2018-dissertation/fig-lorentz-transform.svg)

**Figure 4.4.** A stationary (unprimed) and a moving (primed) observer are represented, respectively, by two sets of coordinate axes: $(x, c\tau)$ and $(x', c\tau')$. The primed observer moves with velocity $v$ in the positive $x$ direction. The time dimension is scaled by the speed of light $c$, so that the path traversed by a photon bisects the unprimed axes. Due to the light speed invariance, the same photon path must also bisect the primed axes. For clarity, only one spatial dimension is shown, but the other two are implied.

Consider a sufficiently small region around the origin where the cosmic fabric is translationally symmetric in space and time. Such translational symmetry is only applicable at the continuum length scale, at which discrete substructure can be ignored or homogeneously included into the fabric's continuous smoothness. The translational symmetry implies that the coordinate transformations we seek must be linear, so let:

$$
\begin{split}
\begin{pmatrix} x' \\ c\tau' \end{pmatrix} = \begin{pmatrix} a_{11} & a_{12} \\ a_{21} & a_{22} \end{pmatrix} \begin{pmatrix} x \\ c\tau \end{pmatrix}
\end{split}
\tag{4.8}
$$

where the coefficients $a_{\mu\nu}$ only depend on the relative velocity $v$. Events along the primed time axis ($x'= 0$) must have unprimed coordinates such that $c\tau = x/\beta$. Therefore, $a_{12} = -\beta a_{11}$. Likewise, events along the unprimed time axis ($x = 0$) must have primed coordinates such that $x' = -\beta c\tau'$, and hence $a_{12} = -\beta a_{22}$. Finally, events along the primed spatial axis ($c\tau' = 0$) must have unprimed coordinates such that $c\tau = \beta x$, from where we conclude that $a_{21} = - \beta a_{22}$. Consequently, letting $\gamma = a_{11} = a_{22}$, Equation (4.8) becomes the following,

$$
\begin{split}
\begin{pmatrix} x' \\ c\tau' \end{pmatrix} = \gamma \begin{pmatrix} 1 & -\beta \\ -\beta & 1 \end{pmatrix} \begin{pmatrix} x \\ c\tau \end{pmatrix}
\end{split}
\tag{4.9}
$$

The inverse of the transformation in Equation (4.9) should also have the same form and correspond to equal and opposite velocity, which leads to the following requirement:

$$
\begin{split}
\begin{pmatrix} 1 & 0 \\ 0 & 1 \end{pmatrix} & = \gamma^2 \begin{pmatrix} 1 & -\beta \\ -\beta & 1 \end{pmatrix} \begin{pmatrix} 1 & \beta \\ \beta & 1 \end{pmatrix} \\
& = \gamma^2 \begin{pmatrix} 1 - \beta^2 & 0 \\ 0 & 1 - \beta^2 \end{pmatrix}
\end{split}
\tag{4.10}
$$

Therefore, we deduce that coefficients $a_{\mu\nu}$ must be as follows,

$$
\begin{split}
a_{11} &= a_{22} = \gamma, \quad a_{12} = a_{21} = -\beta = -v/c \\
\gamma & = \frac{1}{\sqrt{1-\beta^2}} = \frac{1}{\sqrt{1-v^2/c^2}}
\end{split}
\tag{4.11}
$$

which are in fact the coefficients of the well-known Lorentz transformations.

So far, we have derived the coordinate transformations between the stationary and a moving reference frame. It is straightforward to verify that the composition of two Lorentz transformations corresponding to scaled velocities $\beta_1$ and $\beta_2$ is also a Lorentz transformation corresponding to scaled velocity $\beta = (\beta_1 + \beta_2)/(1+\beta_1 \beta_2)$. Since a transformation between any two arbitrary reference frames can be treated as a transformation from the one to the special rest frame and from the rest frame to the other, therefore coordinate transformations between any two arbitrary reference frames is also a Lorentz transformation. Because all reference frames within the fabric transform between each other in like manner, it will be impossible to distinguish which one is the special rest reference frame. Thus, we have shown that the Principle of Relativity, which is the first postulate of the Theory of Special Relativity, can be deduced from the postulates of the Cosmic Fabric Model.

### Discussion

As pointed out in the introduction, the Lorentz Aether Theory (LET) [97] and Einstein's Special Relativity (SR) [48] are mathematically equivalent. In a sense, LET describes reality from the perspective of the fabric's enclosing hyperspace, while SR describes the same reality from the perspective of an observer within the fabric. The phenomenological equivalence of LET and SR with the Cosmic Fabric model is limited to the continuum length scale and to the absence of gravity. Indeed, both LET and SR are continuum theories, which means that they treat physical space as smooth and governed by local laws; that is, laws unaffected by any large scale attributes of space. Furthermore, both LET and SR view physical space as flat (Euclidean), and spacetime also as flat (Minkowskian). The latter limitation is removed by the Theory of General Relativity (GR), which extends SR to curved spacetime. In this sense, one can view the Cosmic Fabric model as extending LET to account for aether curvature and time dilation in a way similar to how GR extends SR. Nevertheless, like SR, General Relativity remains strictly a continuum theory, whereas the Cosmic Fabric model includes parameters, such as its thickness, texture, and an inherent (undeformed) shape, that capture information about the structure of physical space at length scales below and above the continuum scale.

The derivation of the Lorentz transformations in the *Lorentz Transformations* section depended on the translational symmetry of the fabric, which only holds true at a continuum length scale. At lower length scales, the substructure of the fabric, namely its weave-like composition and its thickness, become significant and break the translational symmetry. The weave-like composition of the fabric, which was inferred from its Poisson Ratio being unity, was discussed in Chapter III. Examples of materials with a Poisson Ratio of unity include those of Rodney et al. [141] and Baughman and Fonseca [18], all of which have complex fibrous substructure. Symmetry can also be broken by structure at length scales above the continuum, such as at the length scale of the visible universe. Whenever symmetry is broken, the special rest reference frame of the cosmic fabric becomes physically detectable.

For example, red shift observations of the Cosmic Microwave Background (CMB) [131] can be used to define a kind of universal rest frame. For any point in space, there is exactly one inertial reference frame within which the CMB red shift appears isotropic. Since the red shift is associated with the expansion of cosmic space, this special reference frame represents an observer that is "attached" to space and moves along with it as it expands. Except for this special reference frame, within all other reference frames, the CMB red shift will appear to have a directional dipole indicating the direction and relative velocity of the observer. For example, the dipole we observe from Earth suggests that the Solar System is moving at about 600 km/s in the direction of the constellation Centaurus [4, 81]. The existence of the special CMB rest reference frame means that while local physical observations remain independent of the observer's velocity and position, at the same time cosmic scale observations will differ according to the observer's relative motion in relation to the CMB.

Just like a special rest frame can be identified at cosmological length scales, we speculate that, in a similar way, a special rest frame could be identified at sub-continuum length scales. For example, if space itself has a complex topological structure as suggested by Misner et al. [120], then at sufficiently small length scales, such as quantum length scales, it can no longer be modeled as a continuum. That is why a quantum theory of gravity will need to offer a way for bridging between the continuum and sub-continuum length scales. As discussed by Horstemeyer [68, 69], the field of Solid Mechanics has developed techniques for bridging between length scales within a material. The Cosmic Fabric model, which treats space as a solid material body, provides a way to leverage such existing techniques in the effort for developing a quantum theory of gravity.

### Conclusion

Herein we demonstrated that the material analogy of space, as previously introduced in Chapter III for the case of nearly static observers, also applies for observers in motion. In the context of continuum length scale, the two postulates of Special Relativity were deduced from the postulates of the Cosmic Fabric model, and all reference frames, whether stationary or moving, were shown to transform between each other using the Lorentz transformations. Therefore, at the continuum length scale, the special rest reference frame remains indistinguishable from any other reference frame and the Principle of Relativity is recovered.

At a continuum length scale, the Cosmic Fabric model is to the Lorentz Aether Theory what General Relativity is to Special Relativity. At other length scales, the Cosmic Fabric model predicts that there be a physically detectable special rest reference frame. This prediction is consistent with observations of the CMB and is also likely pertinent in the development of a quantum gravity theory.

---

## V. Spacetime Metric of a Spherically Symmetric Inclusion

Whereas in Chapter III and Chapter IV we considered the behavior of the cosmic fabric in the exterior of matter inclusions, herein we focus on the interaction between the cosmic fabric (physical space) and matter. As in Chapter III we assume nearly static conditions and weak gravity (small strains), in order to keep the math tractable. As explained in Chapter I, these conditions correspond to our ordinary experience of gravity and speeds on Earth and within our Solar System. The limitations of spherical symmetry, small strains, and nearly static bodies can be obviated in the future by solving numerically the pertinent differential equations.

The contribution of this chapter is twofold as follows:

1. We extend the descriptive power of the Cosmic Fabric model presented thus far in Chapter III and Chapter IV to include the behavior of the cosmic fabric (physical space) in the interior of matter inclusions. Consequently, we show that the Schwarzschild metric [148], which is a solution of the Einstein Field Equations [50], can also be deduced from the governing equations of the cosmic fabric. To this end, we work with spherically symmetric inclusions to provide a simple illustration of the method, but the ideas described herein are not fundamentally limited to spherical symmetry.
2. We illustrate and validate the length scale dependent nature of the Cosmic Fabric model as we demonstrate that it predicts the discrete nature of matter. In particular, the model shows that matter above a certain small size cannot be continuous but must be made of discrete particles. Subsequently, we validate this prediction from considering the size of common subatomic particles that make up matter.

Accomplishing the above two goals demonstrates that the Cosmic Fabric model leads to results consistent with accepted theories at both continuum as well as sub-continuum length scales. At the continuum length scale, the model yields results consistent with General Relativity, while at the sub-continuum length scale the model relates to notions from particle physics. The term "continuum length scale" refers to characteristic lengths at which the physical quantities under consideration, such as the fabric strain and the relativistic energy density of inclusions, can be treated as continuous and differentiable fields. By contrast, the term "sub-continuum length scale" refers to much shorter characteristic lengths at which continuity is no longer a good approximation, but the discrete nature of the underlying structure becomes significant.

The remainder of this chapter is organized as follows: The *Geometry of Spherically Symmetric Deformation* section introduces the mathematical tools used for handling the geometry of spherically symmetric hypersurfaces. In the *Spacetime Metric due to Spherically Symmetric Inclusion* section, we formulate the governing equations for the bending of the fabric and derive its spacetime metric (that is, the metric of its world volume), and in the *Membrane Energy and the Discrete Nature of Matter* section we address the length scale dependent nature of the membrane energy. The *Discussion* section compares the fabric's spacetime metric derived herein to the Schwarzschild metric [148]; it also compares the shape of the fabric's deformation to Flamm's paraboloid [56]. Finally, we summarize and conclude in the *Conclusion* section.

### Geometry of Spherically Symmetric Deformation

We consider a spherically symmetric inclusion, which allows us to describe the resulting deformation as a radial stretch $r = r(\overline{r})$ followed by a transverse displacement $w = w(r)$ into the fourth hyperspace dimension (see Figure 5.1).

![Profile of a spherically symmetric deformation.](https://figures.tgtenev.com/tenev2018-dissertation/fig-profile.svg)

**Figure 5.1.** The deformation is specified by a radial displacement $r = r(\overline{r})$, which represents an in-plane stretching, and a transverse displacement $w = w(r)$ into the fourth spatial dimension, applied after the stretching. Here, $\overline{r}$ is the distance from the origin prior to deformation.

Let $r = (1+e)\overline{r}$, where $e = e(\overline{r})$ is the stretch factor by which material points initially at distance $\overline{r}$ from the origin are displaced away from it. The overall deformation is fully specified by the functions $e = e(\overline{r})$ and $w = w(r)$. Note that $\overline{r}$ represents the undeformed 3D distance of a point that has been deformed to be at distance $r$. Table 5.1 summarizes the common variables pertaining to the geometry of the hypersurface that are used in the remainder of this chapter.

**Table 5.1.** Kinematic variables pertaining to a spherically symmetric deformation of a hypersurface.

| Variable(s) | Description |
|---|---|
| $y^K,\ K =1\ldots 4$ | Hyperspatial coordinates of the embedding hyperspace (Cartesian) |
| $x^i,\ i =1\ldots 3$ | Material rectilinear coordinates |
| $t, \overline{r}, \theta, \varphi$ | Material polar coordinates. Note that $t$ represents time and $ct = x^0$. |
| $\overline{r} = \sqrt{\sum_{i=1}^{3} (x^i)^2}$ | Undeformed distance from the origin |
| $e = y^i/x^i - 1$ | Common stretch factor for all $i = 1\ldots 3$ |
| $r = (e+1)\overline{r}$ | Stretched distance from the origin prior to transverse displacement. |
| $w = w(r)$ | Transverse displacement along $y^4$ following the radial stretch. |
| $u \equiv \frac{(w')^2}{2(1+(w')^2)}$ | Convenient variable substitution that happens to represent the portion of volumetric strain due to transverse displacement. |
| $\varepsilon, \varepsilon_r, \varepsilon_\Omega$ | Volumetric strain, radial strain, and hoop strain |

In the context of a spherically symmetric inclusion causing the fabric to deform, we derive the following pertinent quantities in terms of $e$ and $w$: metric tensor, strain tensor, extrinsic curvature tensor, and intrinsic curvature scalar. The following subsections detail the derivation for each of these quantities.

#### Material (Spatial) Metric Tensor

The spatial metric $g_{ij}$ can be computed from the inner product of the three surface tangent vectors $\partial_i y^L$:

$$
\begin{split}
g_{ij} = \partial_i y^L \partial_j y^L
\end{split}
\tag{5.1}
$$

So, we begin by computing the first derivatives of the hyperspatial coordinates $y^{L}$. The second derivatives of $y^L$ are also useful for the computation of other geometric quantities, such as extrinsic and intrinsic curvature, which is why we calculate both types of derivatives below. Our strategy is to first determine the general expressions, and next, evaluate these at conveniently chosen coordinates to take advantage of the spherical symmetry.

Let $y^K$, $K = 1\ldots 4$ be the hyperspatial coordinates of a material point after deformation, and let $x^i$, $i = 1\ldots 3$, be its material coordinates. Then,

$$
\begin{split}
y^4 &= w\quad \text{(by construction)} \\
\partial_i y^4 & = \frac{x^i}{\overline{r}} w'r' \\
\partial_{ij} y^4 &= \frac{x^i x^j}{\overline{r}^2}(w''(r')^2 + w'r'') + \frac{1}{\overline{r}}w'r'\left[\delta_{ij} - \frac{x^i x^j}{\overline{r}^2}\right] \\
y^k &= x^k (1+e) \quad \text{(by construction)} \\
\partial_i y^k &= \delta_{ki} (1+e) + \frac{x^i x^k}{\overline{r}}e' \\
\partial_{ij} y^k &= \frac{x^i x^j x^k}{\overline{r}^2} e'' + \left[\delta_{ki}\frac{x^j}{\overline{r}} + \delta_{jk} \frac{x^i}{\overline{r}} + \delta_{ij}\frac{x^k}{\overline{r}} - \frac{x^i x^j x^k}{\overline{r}^3}\right]e'
\end{split}
\tag{5.2}
$$

where $e' \equiv de/d\overline{r}$, $r' \equiv dr/d\overline{r}$, and $w' \equiv dw/dr$. Notice that unlike $e'$ and $r'$, the shorthand derivative notation $w'$ represents differentiation with respect to the stretched distance $r$ and not the undeformed distance $\overline{r}$. The reason is that $w = w(r)$ is specified as a function of $r$ and not $\overline{r}$.

Because of the spherical symmetry, without loss of generality, we only need to know the values of the above derivatives at a point with conveniently chosen coordinates. Thus, let us choose,

$$
\begin{split}
x^1 = \overline{r}, \quad x^2 = x^3 = 0
\end{split}
\tag{5.3}
$$

where the first derivatives of $y^K$ are as follows:

$$
\begin{split}
[\partial_i y^K] = \begin{pmatrix}
r' & 0 & 0 & w'r' \\
0 & (1+e) & 0 & 0 \\
0 & 0 & (1+e) & 0
\end{pmatrix}
\end{split}
\tag{5.4}
$$

Likewise, the second derivatives of $y^K$ at the chosen coordinates are as follows:

$$
\begin{split}
[\partial_{ij} y^1] &= \begin{pmatrix} r'' & 0 & 0 \\ 0 & e' & 0 \\ 0 & 0 & e' \end{pmatrix}
\quad [\partial_{ij} y^2] = \begin{pmatrix} 0 & e' & 0 \\ e' & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}
\quad [\partial_{ij} y^3] = \begin{pmatrix} 0 & 0 & e' \\ 0 & 0 & 0 \\ e' & 0 & 0 \end{pmatrix} \\
[\partial_{ij} y^4] &= \begin{pmatrix} w''(r')^2 + w'r'' & 0 & 0 \\ 0 & w'r'\overline{r}^{-1} & 0 \\ 0 & 0 & w'r'\overline{r}^{-1} \end{pmatrix}
\end{split}
\tag{5.5}
$$

Substituting the values for $\partial_i y^K$ from Equation (5.4) into Equation (5.1) for the chosen coordinates given in Equation (5.3) yields the following result:

$$
\begin{split}
[g_{ij}] = \begin{pmatrix}
(r')^2(1+(w')^2) & 0 & 0 \\
0 & (1 + e)^2 & 0 \\
0 & 0 & (1 + e)^2
\end{pmatrix}.
\end{split}
\tag{5.6}
$$

#### Intrinsic Curvature

The intrinsic curvature scalar $R^\text{3D}$ can be computed from the extrinsic curvature tensor $b_{ij}$ according to the following identity from differential geometry,

$$
\begin{split}
R^\text{3D} = (b^i_i)^2 - b^j_k b^k_j
\end{split}
\tag{5.7}
$$

Furthermore, the extrinsic curvature can be computed from the derivatives of the tangent vectors $\partial_i y^L$ as follows,

$$
\begin{split}
b_{ij} = -\partial_{ij} y^K \hat{n}^K
\end{split}
\tag{5.8}
$$

where $\hat{n}^K$ is the surface unit normal vector, and the indexes have been raised using the deformed spatial metric $g_{ij}$. Because of the spherical symmetry, we only need to work out the values of $b_{ij}$ and $\hat{n}^K$ for the chosen coordinates stated in Equation (5.3).

The normal vector $\hat{n}$ is given by the following equation:

$$
\begin{split}
\hat{n}^I = \frac{1}{|n^I|} n^I, \quad n^I = \epsilon^I_{JKL}\partial_1 y^J \partial_2 y^K \partial_3 y^L.
\end{split}
\tag{5.9}
$$

where $\epsilon^I_{JKL}$ is the permutation operator. Substituting Equation (5.4) into Equation (5.9) produces the following result:

$$
\begin{split}
\begin{pmatrix} \hat{n}^1 \\ \hat{n}^2 \\ \hat{n}^3 \\ \hat{n}^4 \end{pmatrix} = \frac{1}{\sqrt{1+(w')^2}} \begin{pmatrix} w' \\ 0 \\ 0 \\ -1 \end{pmatrix}.
\end{split}
\tag{5.10}
$$

Evaluating Equation (5.8) for the chosen coordinates yields the extrinsic curvature $b_{ij}$,

$$
\begin{split}
b_{11} &= \frac{w''(r')^2}{\sqrt{1+(w')^2}} \\
b_{22} &= b_{33} = \frac{(1 + e)^2 w'}{r\sqrt{1+(w')^2}} \\
b_{ij} &= 0\quad \text{for} \quad i \neq j.
\end{split}
\tag{5.11}
$$

Therefore, the components $b_i^k = b_{ij} g^{jk}$ are as follows:

$$
\begin{split}
b^1_1 &= \frac{b_{11}}{g_{11}} = \frac{w''}{(1+(w')^2)^{3/2}} \\
b^2_2 &= \frac{b_{22}}{g_{22}} = \frac{w'}{r (1+(w')^2)^{1/2}} \\
b^3_3 &= \frac{b_{33}}{g_{33}} = \frac{w'}{r (1+(w')^2)^{1/2}} \\
b^i_j &= 0,\quad i \neq j.
\end{split}
\tag{5.12}
$$

The following variable substitution helps simplify the subsequent algebra. Let $u$ be defined as follows:

$$
\begin{split}
u \equiv \frac{(w')^2}{2\left(1 + (w')^2\right)}
\end{split}
\tag{5.13}
$$

As we shall see later in Equation (5.33), $u$ also happens to represent the portion of the volumetric stretch that is due to transverse displacement into the fourth spatial dimension. In terms of $u$, the displacement $w$ and its derivatives are as follows:

$$
\begin{split}
(w')^2 &= 2u(1-2u)^{-1} \\
(w')^2 + 1 &= (1-2u)^{-1} \\
w' &= (2u)^{1/2}(1-2u)^{-1/2} \\
w'' &= (2u)^{-1/2}(1-2u)^{-3/2}
\end{split}
\tag{5.14}
$$

When the above identities are substituted into Equation (5.12), we obtain the following result for the extrinsic curvature:

$$
\begin{split}
[b^i_j] = \begin{pmatrix}
u'/\sqrt{2u} & 0 & 0 \\
0 & \sqrt{2u}/r & 0 \\
0 & 0 & \sqrt{2u}/r
\end{pmatrix}
\end{split}
\tag{5.15}
$$

Substituting the result from Equation (5.15) into Equation (5.7) and taking into consideration the identity $ru' + u = (ru)'$, produces the following result for the intrinsic curvature scalar.

$$
\begin{split}
R^\text{3D} = 4 \frac{(ru)'}{r^2}, \quad u \equiv \frac{(w')^2}{2(1+(w')^2)}
\end{split}
\tag{5.16}
$$

Notice that $R^\text{3D}$ only depends on the transverse displacement $w$ and not on the horizontal stretch $e$. This is expected, because according to continuum mechanics theory, compatible deformations do not affect the intrinsic curvature. A "compatible" deformation is one that does not introduce overlaps or tears in the material. Therefore, any purely 3D deformation will not contribute to the 3D intrinsic curvature.

### Spacetime Metric due to Spherically Symmetric Inclusion

In this section we formulate the equations that govern the interaction between a spherically symmetric inclusion and the fabric, and we calculate the resulting spacetime metric. We work in the limit of nearly static bodies and small strains to determine the fabric deformation caused by an inclusion. The result, expressed in terms of the metric tensor that characterizes the deformation, represents the spatial components of the fabric's spacetime metric. The temporal component can be determined from Equation (3.7), which is based on the Time Lapse Postulate (the *Lapse Rate* section of Chapter III). The following paragraphs detail the derivation.

#### Formulation of the Governing Equations

The governing equations are formulated in terms of the radial stretch factor $e(r) = r/\overline{r} - 1$ and the transverse displacement $w(r)$ based on the following constraints: 1) the bending energy density must balance the relativistic energy density of the inclusion, 2) inclusions are sources of strain, and 3) the total membrane energy must vanish. As Chapter III discusses in detail, the term "bending energy" means the portion of the elastic energy due to bending whereby the mid-hypersurface of the fabric remains unstrained and the hypersurfaces on each side of it are being either stretched or compressed. By contrast, the term "membrane energy" is the elastic energy attributed to the stretching of the mid-hypersurface.

The above constraints are motivated as follows: Consider the Fabric's action $\mathcal{S} = \int \mathcal{L}_\text{F} \sqrt{|g|}\, dx^4$ where $\mathcal{L}_\text{F}$ is the Lagrangian of the fabric together with the inclusion; $g \equiv \det [g_{\mu\nu}]$ is the determinant of the spacetime metric; and the integral is taken over a sufficiently large volume of spacetime such that the integral converges. According to the Principle of Least Action, physical systems progress along a trajectory that extremizes the action (the action is either minimized or maximized). For a nearly static situation the kinetic components of $\mathcal{L}_\text{F}$ can be ignored, so only the contributions from the fabric's elastic energy and the body's relativistic energy need to be considered. Thus, $\mathcal{L}_\text{F} = -(U_\text{M} + U_\text{B} + c^2 \rho)$. Furthermore, per Equation (3.9) the determinant $|g| \approx 1$. Therefore, since the total energy integrated over all of three-dimensional space should be non-negative, the action $\mathcal{S}$ would reach an extremum if the deformation functions $e$ and $w$ were such that the total elastic energy $W$ vanished, where $W$ is defined as follows:

$$
\begin{split}
W \equiv \int_\text{all space} (U_\text{M} + U_\text{B} + c^2 \rho)\, dx^3 = 0
\end{split}
\tag{5.17}
$$

As the *Membrane Energy and the Discrete Nature of Matter* section demonstrates, the membrane energy component of the above integral is length scale dependent because it varies disproportionately with the mass of the gravitating body unlike the other two components which are length scale independent. Therefore, in order for $W$ from Equation (5.17) to vanish for inclusion of any mass, it follows that the total membrane energy $W_\text{M}$, defined per Equation (5.18), must vanish independently from the other two components. Consequently, Equation (5.17) yields these two independent equations:

$$
\begin{split}
W_\text{M} \equiv \int_\text{all space} U_\text{M}\, dx^3 = 0
\end{split}
\tag{5.18}
$$

$$
\begin{split}
U_\text{B} + c^2\rho = 0
\end{split}
\tag{5.19}
$$

In Equation (5.19) we have replaced the requirement that the integral vanishes with the ostensibly stronger requirement that the integrand vanishes too. Because $U_\text{B}$ and $\rho$ are both scale independent, the requirement that the integral should vanish for any size and density gravitating body implies that the integrand must vanish identically.

In addition, as previously postulated in Chapter III, the inclusion is a source of strain per the following equation:

$$
\begin{split}
\nabla^2 \varepsilon = -\frac{1}{2}c^2 \kappa \rho.
\end{split}
\tag{5.20}
$$

where $\rho$ is the density of the inclusion.

Equations (5.19) and (5.20) represent the first and second constraints respectively, while Equation (5.18) represents the third constraint. The first two constraints are sufficient to produce a solution for the fabric's spacetime metric, which is the focus of this section. The *Membrane Energy and the Discrete Nature of Matter* section addresses the third constraint where we examine the conditions under which the total membrane energy vanishes, and we show that it does indeed vanish for the case of matter made up of small particles, which is true for all known matter.

It is convenient to work with the geometric equivalents of the parameters describing the gravitating body. For example, rather than working with the mass of the body $M$, we use its Schwarzschild radius $r_s = 2GM/c^2$. Also, because the relativistic energy density of the gravitating body is $\rho = M/[(4/3)\pi r_g^3]$, where $r_g$ is the radius of the gravitating body, we derive the substitution,

$$
\begin{split}
\kappa c^2 \rho = \frac{3r_s}{r_g^3} \equiv \frac{3}{r_0^2}, \quad r_0 \equiv \sqrt{\frac{r_g^3}{r_s}}
\end{split}
\tag{5.21}
$$

where $r_0$, as defined above, is a geometric quantity characterizing the density of the inclusion. Finally, the result from the Cosmic Fabric model expressed in Equation (3.18) and Equation (3.25) provides a geometric interpretation for the bending energy of the Fabric due to the gravitating body acting as an inclusion. Table 5.2 summarizes the geometric parameters used to describe a gravitating body.

**Table 5.2.** Geometric parameters pertaining to a spherically symmetric gravitating body of mass $M$.

| Parameter | Description |
|---|---|
| $r_g$ | Radius of the gravitating body after the initial stretch but before the transverse displacement. Note that this is not the actual geometric radius which is slightly larger due to the transverse displacement |
| $\overline{r}_g$ | Undeformed radius of the gravitating body. Since we work in the small strains (weak gravity) regime $\overline{r}_g \approx r_g$. |
| $r_s \equiv 2 G M/c^2$ | Schwarzschild radius, which is the geometric equivalent of the body's mass. |
| $r_0 \equiv \sqrt{r_g^3/r_s}$ | Geometric equivalent of the body's density $\rho$. Specifically, $\kappa c^2\rho = 3/r_0^2$, where $\kappa \equiv 8 \pi G/c^4$ is the Einstein constant. |
| $R^\text{3D} = -2\kappa U_\text{B}$ | The intrinsic curvature scalar of the cosmic fabric is the geometric equivalent of the bending elastic energy caused by the matter inclusion. |

In terms of these parameters, Equations (5.19) and (5.20) become the following:

$$
\begin{split}
R^\text{3D} = \frac{6}{r_0^2}
\end{split}
\tag{5.22}
$$

$$
\begin{split}
\nabla^2 \varepsilon = -\frac{3}{2 r_0^2}
\end{split}
\tag{5.23}
$$

These equations govern the bending of the fabric due to a spherically symmetric inclusion, and the following sections detail their solutions. We first solve for the transverse displacement $w = w(r)$ where $r \equiv (1+e)\overline{r}$ and the volumetric strain $\varepsilon = \varepsilon(\overline{r})$. The results are used to solve for the stretch factor $e = e(\overline{r})$. Finally, we derive the solution for the spacetime metric.

#### Transverse Displacement

We solve for the transverse displacement, $w$, by combining Equation (5.22) with the result from Equation (5.16), which yields the following equation,

$$
\begin{split}
(ru)' = \frac{3r^2}{2r_0^2}, \quad u \equiv (w')^2/2(1+(w')^2)
\end{split}
\tag{5.24}
$$

Let us consider separately the interior ($0 \le r < r_g$), versus the exterior region ($r_g \le r$) of the gravitating body. Within the interior, the mass density has a finite value $\rho$ and a finite geometric equivalent $r_0$, whereas in the exterior, $\rho = 0$ and $r_0 = \infty$. Let $u_\text{int}$ and $u_\text{ext}$ be the interior and exterior solutions, respectively. Equation (5.24) implies that,

$$
\begin{split}
u_\text{int} = \frac{r^2}{2 r_0^2} + \frac{C_1}{r}; \quad u_\text{ext} = \frac{C_2}{r}
\end{split}
\tag{5.25}
$$

where $C_1$ and $C_2$ are constants of integration. The constant $C_1$ must vanish to avoid a singularity at $r = 0$. Furthermore, for $u(r)$ to be continuous we require that $u_\text{int}(r_g) = u_\text{ext}(r_g)$ from where we conclude that $C_2 = r_s/2$. Finally, we arrive at the following solutions for $u$ and $w$:

$$
\begin{split}
u_\text{int} = \frac{r^2}{2r_0^2}; \quad u_\text{ext} = \frac{r_s}{2r}
\end{split}
\tag{5.26}
$$

$$
\begin{split}
w_\text{int} &= (2r_s + r_g)\sqrt{r_g/r_s - 1} - \sqrt{r_0^2 - r^2} + C \\
w_\text{ext} &= 2\sqrt{r_s(r - r_s)} + C
\end{split}
\tag{5.27}
$$

where $C$ is a constant of integration that represents an arbitrary rigid translation of the fabric, and $r = (1+e)\overline{r}$ is the stretched distance from the center of the gravitating body.

#### Volumetric Strain

Below we solve for the volumetric strain $\varepsilon = \varepsilon(\overline{r})$, from which we can determine the radial stretch factor $e = e(\overline{r})$.

Let $f(\overline{r}) \equiv d\varepsilon(\overline{r})/d\overline{r}$. By successive differentiation we determine the following,

$$
\begin{split}
\frac{\partial}{\partial x^i} \varepsilon &= f \frac{x^i}{\overline{r}} \\
\frac{\partial^2}{(\partial x^i)^2} \varepsilon &= f'\frac{(x^i)^2}{\overline{r}^2} + f\frac{1}{\overline{r}} - f\frac{(x^i)^2}{\overline{r}^3} \\
\therefore\ \nabla^2 \varepsilon & \equiv \sum_{i=0}^3 \frac{\partial^2}{(\partial x^i)^2} \varepsilon = f' + 2f\frac{1}{\overline{r}} = \frac{(\overline{r}^2 f)'}{\overline{r}^2}.
\end{split}
\tag{5.28}
$$

When the above identity is substituted into Equation (5.23) the result is as follows:

$$
\begin{split}
\frac{(\overline{r}^2 f)'}{\overline{r}^2} &= -\frac{3}{2}\frac{1}{r_0^2} \\
f &= -\frac{1}{2}\frac{\overline{r}}{r_0^2} - \frac{C_3}{\overline{r}^2} \\
\varepsilon &= C_4 - \frac{1}{4}\frac{\overline{r}^2}{r_0^2} + \frac{C_3}{\overline{r}},
\end{split}
\tag{5.29}
$$

where $C_3$ and $C_4$ are constants of integration. Let $\varepsilon_\text{int}$ and $\varepsilon_\text{ext}$ represent the interior and exterior solutions, respectively. For the interior solution, $0\le \overline{r} \le \overline{r}_g$, we determine that $C_3 = 0$, or else $\varepsilon_\text{int}$ diverges as $\overline{r} \rightarrow 0$. For the exterior case, $r_0 = \infty$, so $\varepsilon_\text{ext} = C_4 + C_3/r$, but $C_4$ must vanish, for $\varepsilon_\text{ext}$ to vanish at infinity. Thus, we conclude so far the following,

$$
\begin{split}
\varepsilon_\text{int} = C_4 - \frac{1}{4}\frac{r^2}{r_0^2}; \quad \varepsilon_\text{ext} = \frac{C_3}{r}.
\end{split}
\tag{5.30}
$$

For it to be physically admissible, $\varepsilon$ and its first derivative must be continuous throughout three-dimensional space. Therefore,

$$
\begin{split}
&\varepsilon_\text{int}(r_g) = \varepsilon_\text{ext}(r_g); \quad \left.\frac{d}{d\overline{r}}\varepsilon_\text{int}\right|_{r = r_g} = \left.\frac{d}{d\overline{r}}\varepsilon_\text{ext}\right|_{r = r_g} \\
&\therefore\ C_3 = \frac{r_s}{2}; \quad C_4 = \frac{3r_g^2}{4r_0^2},
\end{split}
\tag{5.31}
$$

which finally produces the following result:

$$
\begin{split}
\varepsilon_\text{int} = \frac{3}{4}\frac{\overline{r}_g^2}{r_0^2} - \frac{1}{4}\frac{\overline{r}^2}{r_0^2}; \quad \varepsilon_\text{ext} = \frac{1}{2}\frac{r_s}{\overline{r}}
\end{split}
\tag{5.32}
$$

#### Radial Stretch

We solve for the radial stretch $e(\overline{r})$ by relating it to the volumetric stretch $\varepsilon$ and the transverse displacement $w$. To simplify the math, we will use linearized approximations based on the fact that under the small strains regime adopted here the quantities $e$ and $u \equiv (w')^2/\left[2(1+(w')^2)\right]$ are all much less than 1.

From the definition of volumetric strain in Equation (2.35) and the result for the metric from Equation (5.6), we derive the following:

$$
\begin{split}
2\varepsilon &= (r')^2 (1+(w')^2) + 2(1+e)^2 - 3 \\
& = (e'\overline{r} + e + 1)^2 (1-2u)^{-1} + 2(1+e)^2 - 3 \\
& \approx (2e'\overline{r} + 2e + 1)(1 + 2u) + 2(1+ 2e) - 3 \\
\varepsilon & = e'\overline{r} + 3e + u = \frac{(e\overline{r}^3)'}{\overline{r}^2} + u
\end{split}
\tag{5.33}
$$

Therefore,

$$
\begin{split}
(e\overline{r}^3)' = \overline{r}^2 \varepsilon - \overline{r}^2 u.
\end{split}
\tag{5.34}
$$

After substituting the result for $\varepsilon$ and $u$ from Equation (5.32) and Equation (5.26), respectively, into Equation (5.34) and approximating $\overline{r}_g \approx r_g$, we obtain the following general solution:

$$
\begin{split}
\frac{(e_\text{int}\overline{r}^3)'}{\overline{r}^2} &= \frac{3r_g^2 - \overline{r}^2}{4r_0^2} - \frac{\overline{r}^2}{2r_0^2} = \frac{3(r_g^2 - \overline{r}^2)}{4r_0^2} \\
\therefore\ e_\text{int} &= \frac{1}{4}\frac{r_g^2}{r_0^2} - \frac{3}{20}\frac{\overline{r}^2}{r_0^2} + \frac{C_5}{\overline{r}^3} \\
\frac{(e_\text{ext}\overline{r}^3)'}{\overline{r}^2} &= \varepsilon_\text{ext} - u = \frac{1}{2}\frac{r_s}{\overline{r}} - \frac{1}{2}\frac{r_s}{\overline{r}} = 0 \\
\therefore\ e_\text{ext} &= \frac{C_6}{\overline{r}^3},
\end{split}
\tag{5.35}
$$

where $C_5$ and $C_6$ are constants of integration. The constant $C_5$ must vanish to avoid the singularity at $r = 0$. The constant $C_6$ can be determined by requiring that $e_\text{int}(r_g) = e_\text{ext}(r_g)$. Consequently, we arrive at the following solution for $e(\overline{r})$:

$$
\begin{split}
e_\text{int} = \frac{1}{4}\frac{r_g^2}{r_0^2}- \frac{3}{20}\frac{\overline{r}^2}{r_0^2},\quad e_\text{ext} = \frac{1}{10}\frac{r_g^5}{r_0^2 \overline{r}^3} = \frac{1}{10}\frac{r_s r_g^2}{\overline{r}^3}
\end{split}
\tag{5.36}
$$

#### Metric

We are now ready to derive the spacetime metric of the deformed fabric in terms of the geometric characteristics of the inclusion that is the source of the deformation. These are: the inclusion's Schwarzschild radius $r_s$, its spatial radius $r_g$, and the geometric equivalent of its density $r_0$.

Because of the spherical symmetry, it is useful to derive the metric using the polar material coordinates $(t, \overline{r}, \theta, \varphi)$ corresponding, respectively, to time, undeformed radius, altitude angle, and azimuth angle. In terms of these coordinates, the spacetime line element $ds$ is given by,

$$
\begin{split}
ds^2 = g_{tt} c^2 dt^2 + g_{\overline{r}\overline{r}} d\overline{r}^2 + g_{\Omega\Omega}\overline{r}^2 d\Omega^2
\end{split}
\tag{5.37}
$$

where $d\Omega^2 \equiv d\theta^2 + \cos^2 \theta\, d\varphi^2$, and where $g_{tt}$, $g_{\overline{r}\overline{r}}$, and $g_{\Omega\Omega}$ are the polar metric coefficients.

For the chosen rectilinear coordinates in Equation (5.3), we can identify the spatial polar metric coefficients with the rectilinear coefficients $g_{ij}$ as follows,

$$
\begin{split}
g_{\overline{r}\overline{r}} &= g_{11} = (r')^2 (1+(w')^2) \\
& = (1 + e + e'\overline{r})^2(1-2u)^{-1} \\
& \approx 1 + 2(e + e'\overline{r} + u) \\
g_{\Omega\Omega} &= g_{22} = g_{33} = (1+e)^2 \approx 1 + 2e
\end{split}
\tag{5.38}
$$

In the above derivation, we have used the result for $g_{ij}$ from Equation (5.6) into which we have substituted $r = (1+e)\overline{r}$, and expressed $(1+(w')^2)$ in terms of $u$ per Equation (5.14). Due to the spherical symmetry, the above expressions only depend on the radial functions $e$ and $u$. Therefore, they apply for all points in space and not just for the specially chosen coordinates.

We also identify the time–time metric coefficient $g_{tt}$ with $g_{00}$. The latter can be determined from the Time Lapse Postulate of the Cosmic Fabric model (see Equation (3.7)) as follows,

$$
\begin{split}
g_{tt} = g_{00} = -(1+\varepsilon)^{-2} \approx -(1 - 2\varepsilon);
\end{split}
\tag{5.39}
$$

Finally, after substituting the results for $u$, $\varepsilon$, and $e$ from Equations (5.26), (5.32), and (5.36) into Equations (5.38) and (5.39), we arrive at the following result for the spacetime element $ds$:

$$
\begin{split}
ds^2_\text{int} &= -\left(1 - \frac{3r_g^2}{2r_0^2} + \frac{\overline{r}^2}{2r_0^2}\right) c^2 dt^2 \\
& + \left(1 + \frac{r_g^2}{2r_0^2} + \frac{\overline{r}^2}{10r_0^2}\right) d\overline{r}^2 \\
& + \left(1 + \frac{r_g^2}{2r_0^2} - \frac{3\overline{r}^2}{10r_0^2}\right) \overline{r}^2 d\Omega^2, \quad 0 \le \overline{r} < r_g \\
ds^2_\text{ext} &= -\left(1-\frac{r_s}{\overline{r}}\right) c^2 dt^2 \\
& + \left(1+\frac{r_s}{\overline{r}} - \frac{2 r_s r_g^2}{5\overline{r}^3}\right) d\overline{r}^2 \\
& + \left(1+\frac{r_s r_g^2}{5\overline{r}^3}\right) \overline{r}^2 d\Omega^2, \quad r_g \le r
\end{split}
\tag{5.40}
$$

where $ds_\text{int}$ and $ds_\text{ext}$ represent, respectively, the interior and exterior solutions for the metric. The *Discussion* section compares the result from Equation (5.40) to the Schwarzschild metric and demonstrates that they are equivalent up to a coordinate rescaling.

From a solid mechanics perspective, the three metric coefficients in Equation (5.40) can be expressed in terms of the volumetric strain $\varepsilon$, radial strain $\varepsilon_r$, and hoop strain $\varepsilon_\Omega$ of the fabric as follows:

$$
\begin{split}
ds^2 =& -\left(1 - 2\varepsilon\right)c^2dt^2 + \left(1 + 2\varepsilon_r\right)d\overline{r}^2 + \left(1 + 2\varepsilon_\Omega\right)\overline{r}^2 d\Omega^2
\end{split}
\tag{5.41}
$$

Figure 5.2 shows the profiles of these strains as a function of the undeformed radius $\overline{r}$. Note that $\varepsilon = \varepsilon_r + 2\varepsilon_\Omega$, as one would expect, because a single radial and two hoop orientations form an orthogonal triad at any point along a spherical shell. Furthermore, the reason why the radial and hoop strains vanish at different rates ($\propto \overline{r}^{-1}$ versus $\propto \overline{r}^{-3}$, respectively) is because the radial strain depends on both the transverse displacement $w$ as well as the radial displacement ($\overline{r}$ displacing into $r$), whereas the hoop strain only depends on the radial displacement (see Figure 5.1).

![Profiles of strains.](https://figures.tgtenev.com/tenev2018-dissertation/fig-strain.svg)

**Figure 5.2.** Profiles of the volumetric strain $\varepsilon$, radial strain $\varepsilon_r$, and hoop strain $\varepsilon_\Omega$ at distance $\overline{r}$ from the center of a gravitating body with Schwarzschild radius $r_s$ and geometric radius $r_g$. Note that $\varepsilon = \varepsilon_r + 2\varepsilon_\Omega$.

### Membrane Energy and the Discrete Nature of Matter

The fabric's elastic energy density $U$ can be decomposed into membrane and bending terms, $U_\text{M}$ and $U_\text{B}$, respectively, such that $U = U_\text{M} + U_\text{B}$. The *Spacetime Metric due to Spherically Symmetric Inclusion* section considered the bending term, while here we focus on the membrane term. Chapter III showed that $U_\text{M}$ vanishes in the absence of in-plane stretching. However, the solution for the spacetime metric we derived in Equation (5.40) includes in-plane stretch, which ostensibly leads to non-vanishing membrane energy density. Nevertheless, we can show that the fabric's membrane energy due to the inclusion of a gravitating body vanishes under the following conditions: 1) the body is made up of discrete particles, as opposed to being perfectly continuous, which is the case for all known matter, and 2) each individual particle induces a certain type of asymmetric deformation as discussed in the *Discrete Substructure* section. So, while the body may appear continuous and spherically symmetric at the continuum length scale, the spherical symmetry does not hold at substructure length scale. The fact that the Cosmic Fabric model requires for matter to be discrete is significant and is a consequence of the length scale dependence built into the model via the fabric's thickness $L$.

We arrive at the above conclusion by reasoning progressively as follows: First, we consider the total membrane energy of the fabric due to the inclusion of a perfectly continuous spherically symmetric body. Next, we analyze how the membrane energy is different in a spherically symmetric body that has discontinuous substructure.

#### Total Membrane Energy of a Homogeneous Spherically Symmetric Body

The total membrane energy $W_\text{M} = W_\text{M}(\overline{r})$ within a ball of physical space of radius $\overline{r}$ concentric with the gravitating body is, by definition, the following:

$$
\begin{split}
W_\text{M}(\overline{r}) = 4\pi \int_{0}^{\overline{r}} U_\text{M}(\zeta) \zeta^2 d\zeta.
\end{split}
\tag{5.42}
$$

where $\zeta$ is the variable of integration representing undeformed distance from the origin. The membrane energy density $U_\text{M}$ is the elastic energy density of the fabric's mid-hypersurface given by $U_\text{M} = \sigma^{ij}\varepsilon_{ij}/2$, which by application of Hooke's Law (1.2) with $\nu = 1$ is the following:

$$
\begin{split}
U_\text{M} = \frac{Y}{4}\left(\varepsilon^k_j\varepsilon^j_k - \varepsilon^i_i \varepsilon^k_k\right),
\end{split}
\tag{5.43}
$$

Due to the spherical symmetry, without loss of generality, we can evaluate the above result for the choice of coordinate values from Equation (5.3). Since the undeformed metric is $\overline{g}^{ij} = \delta^{ij}$, therefore $\varepsilon^i_j = \varepsilon_{ij}$ and so from the definition of small strain in Equation (2.34) and the result in Equation (5.6) it follows that,

$$
\begin{split}
\varepsilon^1_1 &= (g_{11} - 1)/2 = \left[(1+e+e'\overline{r})^2 (1-2u)^{-1} - 1\right]/2 \approx e + e'\overline{r} + u \\
\varepsilon^2_2 &= (g_{22} - 1)/2 = [(1+e)^2-1]/2 \approx e \\
\varepsilon^3_3 &= (g_{33} - 1)/2 = [(1+e)^2-1]/2 \approx e
\end{split}
\tag{5.44}
$$

Substituting Equation (5.44) into Equation (5.43) leads to the following result for the membrane energy density:

$$
\begin{split}
U_\text{M}(\overline{r}) = -\frac{Y}{2}\left(3e^2+2ee'\overline{r} + 2ue\right) = -\frac{Y}{2\overline{r}^2}\left[(e^2 \overline{r}^3)' + 2ue\overline{r}^2 \right]
\end{split}
\tag{5.45}
$$

We can now substitute the solutions for $u$ and $e$ from Equation (5.26) and Equation (5.36), respectively, into Equation (5.45), and integrate the resulting expression for $U_\text{M}$ per Equation (5.42) to produce the following result for $W_\text{M}$:

$$
\begin{split}
W_\text{M} &= -\frac{3c^4 r_s^2 r_g}{50 G L^2} \times
\begin{cases}
\left(\frac{5}{2} - \frac{3}{2}\xi^2\right)^2\xi^3 + 5\left(1 -\frac{3}{7}\xi^2\right)\xi^5, & 0 \le \xi < 1 \\
\xi^{-3} - 10\xi^{-1} + \frac{90}{7}, & 1\le \xi
\end{cases},
\end{split}
\tag{5.46}
$$

where $\xi \equiv \overline{r}/r_g$. Also, we have used the result for $Y$ from Equation (3.28) and we have taken the approximation $r \approx \overline{r}$, which holds under the small strain regime assumed here.

Figure 5.3 shows the changing membrane energy $W_\text{M}$ as a function of the undeformed distance $\overline{r}$ from the center of the gravitating body. The calculated total energy is negative and converges at infinity to the following value:

$$
\begin{split}
\max |W_\text{M}| = \lim_{\overline{r} \to \infty} |W_\text{M}| = \frac{27 c^4 r_s^2 r_g}{35 G L^2}
\end{split}
\tag{5.47}
$$

![Total membrane energy of the fabric due to a continuous inclusion.](https://figures.tgtenev.com/tenev2018-dissertation/fig-total-membrane-energy.svg)

**Figure 5.3.** The total membrane energy $W_\text{M}$ due to a continuous gravitating body of radius $r_g$ and a Schwarzschild radius $r_s$ versus the undeformed distance $\overline{r}$.

The fact that $W_\text{M}$ saturates at infinity was expected, because the effect of a gravitating body on the total energy of the fabric should become negligible at sufficiently large distances. However, the result in Equation (5.47), which is illustrated in Figure 5.3, also reveals two potential problems: 1) the total membrane energy $W_\text{M}$ is length scale dependent and can become disproportionately large for more massive bodies relative to less massive ones, and 2) the total membrane energy is negative. As demonstrated below, both of these issues are resolved once we allow for the existence of substructure within the gravitating body instead of the body being perfectly continuous.

Equation (5.47) shows that the amplitude of the fabric's membrane energy due to the inclusion of a body grows as the square of the body's Schwarzschild radius $r_s$, whereas the body's relativistic energy grows only linearly with $r_s$. Consequently, very massive bodies will result in membrane energies with disproportionately greater magnitudes compared to less massive bodies. This situation suggests that there must be a limit to the massiveness of a perfectly continuous body, or equivalently, to the size of its Schwarzschild radius. The fabric's thickness $L$, which figures into the equation for $\max|W_\text{M}|$ serves as a length scale parameter that determines an upper bound for $r_s$, so that a spherically symmetric body with $r_s$ that is larger than said upper bound cannot be itself perfectly continuous but must be composed of smaller particles. To quantify this limit, we require that the effect of a gravitating body in terms of the total membrane energy $W_\text{M}$ should be comparable or less to the body's own relativistic energy, which in terms of the body's Schwarzschild radius $r_s$ is $r_s c^4 / (2 G)$. In other words, we assert that,

$$
\begin{split}
\frac{r_s c^4}{2G} &\gtrsim \max|W_\text{M}| = \frac{27 c^4 r_s^2 r_g}{35 G L^2} \\
\therefore\ r_s r_g &\lesssim \frac{35}{54}L^2
\end{split}
\tag{5.48}
$$

Since also $r_s \le r_g$, the maximum possible mass is achieved for a body such that $r_s = r_g$. In that case,

$$
\begin{split}
\max(r_s) \le \sqrt{\frac{35}{54}}L.
\end{split}
\tag{5.49}
$$

Chapter III explains that the thickness of the fabric $L$ must be comparable to Planck's length $l_p = 1.616229\times 10^{-35}\,\text{m}$. Herein we propose a more precise value for $L$ founded on the notion that $L$ represents the intersection of two energy-based length scales: one derived from General Relativity and one from Quantum Mechanics. From General Relativity, one can assign a length value to the energy of a body using its Schwarzschild radius $r_s$, since the body's energy is given by $E = r_s c^4/(2G)$. Alternatively, one can also assign a length value to the body's energy from Quantum Mechanics using the body's De Broglie wavelength $\lambda$, in which case its energy is $E = hc/\lambda$, where $h$ is the Planck's constant. Notice that $r_s$ is proportional to the energy of the body, but $\lambda$ is inversely proportional. We propose that $L$ corresponds to the energy scale at which these two length values coincide. Therefore,

$$
\begin{split}
\frac{h c}{L} &= \frac{r_s c^4}{2G} \\
\therefore\ L &= \sqrt{\frac{2 h G}{c^3}} = 5.729\times 10^{-35}\,\text{m}
\end{split}
\tag{5.50}
$$

which is still comparable to $l_p$ but slightly larger. From Equation (5.50) and Equation (5.49), it follows that the upper bound for the Schwarzschild radius $\max(r_s)$ of a perfectly continuous body and therefore the upper bound for its mass $\max(M)$ are given by:

$$
\begin{split}
\max(r_s) & \sim 3.713\times 10^{-35}\,\text{m} \\
\max(M)& = \max(r_s)\frac{c^2}{2G} \sim 2.500\times 10^{-8}\,\text{kg}
\end{split}
\tag{5.51}
$$

The maximum continuous mass derived above represents the mass of a tiny black hole, because we had assumed that $r_g = r_s$. For ordinary matter, however, $r_g \gg r_s$. How does the constraint expressed in Equation (5.48) apply to the particles that comprise matter?

Table 5.3 lists the values of $r_s$ and $r_g$ for the proton, neutron, and electron. Subatomic particles do not have definite radii, but the size of their radii can be modeled based on how they interact with other particles. For example, the root mean square charge radius of a proton is determined from electron scattering experiments; it has a well-accepted value [168], which is the one used in Table 5.3 for the proton radius. Modern particle theory considers the electron to be a point particle, but its classical radius $r_e$, which is what we use in Table 5.3, can be calculated as the combination of fundamental constants: $r_e = e^2/(4\pi \varepsilon_0 m_e c^2)$ where $e$, $m_e$, and $\varepsilon_0$ are the electron charge, electron mass, and the permittivity of free space, respectively. The radius of the neutron is relatively challenging to compute because of its overall neutral charge. Several researchers [2, 63, 154] have studied $^{208}$Pb to determine the difference between the neutron and proton radii with results in the range of $0.15 - 0.33$ fm. Based on this research, Table 5.3 uses an estimate for the neutron's radius that is $0.2$ fm larger than the proton's. One conclusion from the values of $r_s$ and $r_g$ for the listed particles is that because $r_g \gg r_s$, the regime of small strains (weak gravity) applies and so the approximations used in our calculations herein apply too.

**Table 5.3.** Length scales and energy scales of common sub-atomic particles. The length scales are expressed in terms of the particle's geometric radii $r_g$ and Schwarzschild radii $r_s$, respectively, and compared to the fabric's thickness $L$.

| Particle | $M$ [kg] | $r_g$ [m] | $r_s$ [m] | $54 r_s r_g/(35 L^2)$ |
|---|---|---|---|---|
| proton [167, 168] | $1.7 \times 10^{-27}$ | $8.8 \times 10^{-16}$ | $2.5 \times 10^{-54}$ | $1.0 \times 10^{0}$ |
| neutron [2, 63, 154, 166] | $1.7 \times 10^{-27}$ | $1.1 \times 10^{-15}$ | $2.5 \times 10^{-54}$ | $1.3 \times 10^{0}$ |
| electron [164, 165] | $9.1 \times 10^{-31}$ | $2.8 \times 10^{-15}$ | $1.4 \times 10^{-57}$ | $1.8 \times 10^{-3}$ |

Table 5.3 also shows that the constraint expressed in Equation (5.48) applies with some tolerance to the proton, neutron, and electron. While the electron fits well within the constraint, the proton and neutron exceed it slightly by about 2% and 30%, respectively. Unlike the electron, however, both the proton and the neutron have substructure, since they are made up of yet smaller particles known as quarks, so exceeding the constraint slightly in their case is not necessarily a problem. In reality, modeling subatomic particles as tiny spheres is an approximation anyway, since these particles also have wave nature and lack definite boundaries. In fact, as the following subsection discusses, if we account for the possibility that these subatomic particles oscillate between various non-spherically symmetric configurations, then an arrangement is possible for which the total membrane energy vanishes completely.

#### Discrete Substructure

Next we show that a spherically symmetric inclusion can be arbitrarily massive as long as it is not perfectly continuous. In other words, continuity of matter is not admissible at any arbitrary length scale, but bodies must be composed of discrete particles. At the same time, a body could be treated as spherically symmetric and ostensibly continuous at sufficiently large length scales even while composed of discrete particles (see Figure 5.4).

![Substructure of a spherically symmetric body.](https://figures.tgtenev.com/tenev2018-dissertation/fig-substructure.svg)

**Figure 5.4.** The substructure of an ostensibly continuous and isotropic body is progressively revealed in (a) through (c), where (a) shows the body idealized as perfectly continuous and spherically symmetric. The dashed lines represent imaginary subdivisions of the body into cells. In (b), the mass of each cell is revealed to be concentrated into a small particle, while the overall mass density of the body remains unaffected. In (c), each particle is revealed to be locally anisotropic, while the body remains overall ostensibly isotropic.

We show herein that if individual particles prescribe asymmetric fabric strains, such as oblate or longitudinal expansion, then there would be no resulting membrane energy. Thus, it is possible for the gravitating body to cause in-plane fabric strain that appears symmetric at the continuum length scale, but without incurring any membrane energy.

Figure 5.4 shows a spherically symmetric body whose substructure is revealed progressively from most idealized (no substructure) in Figure 5.4a to least idealized (most detailed substructure) in Figure 5.4c. At a sufficiently large length scale, the body appears continuous and isotropic, but at smaller length scales continuity and isotropy need not necessarily apply as Figure 5.4c illustrates. In Figure 5.4, the gravitating body is pictured as subdivided into cells whose total mass remains the same from one subfigure to another, but the distribution of the mass within each cell is revealed to be different from one subfigure to another. Equation (5.47) shows that the membrane energy depends on the spatial radius $r_g$ of a gravitating body. Therefore, the membrane energy due to each cell within the body is reduced from Figure 5.4a to Figure 5.4b. To get an idea of the reduction, consider for example, that the mass of the Hydrogen atom with radius of about $5.3\times 10^{-11}\,\text{m}$ is concentrated in its nucleus, which is a single proton with radius of about $8.8\times 10^{-16}\,\text{m}$. So, simply by refining the picture we have for the hydrogen atom from a continuous solid sphere to a nearly hollow sphere with a nucleus, we would have to adjust our calculation for its resulting membrane energy by a factor of $\times 10^{-5}$. However, we can do even better than that and completely eliminate the membrane energy if we allowed non-spherically symmetric strain at the substructure length scale as described below.

Consider the strain tensor $\varepsilon^i_j$ of the fabric due to a single sub-scale particle inclusion such as one of the anisotropic particles in Figure 5.4c. Let us choose for convenience a coordinate system orientation in which this strain tensor is represented by a diagonal matrix, and let $\varepsilon_i \equiv \varepsilon^i_i\ i = 1\ldots 3$ (no summation) be the diagonal entries. From Equation (5.43) we see that,

$$
\begin{split}
U_\text{M} & \propto (\varepsilon_1)^2 + (\varepsilon_2)^2 + (\varepsilon_3)^2 - (\varepsilon_1 + \varepsilon_2 + \varepsilon_3)^2 = -2\left[\varepsilon_1 \varepsilon_2 + \varepsilon_2 \varepsilon_3 + \varepsilon_3 \varepsilon_1 \right]
\end{split}
\tag{5.52}
$$

For any arbitrary value of the volumetric strain $\varepsilon = \varepsilon_1 + \varepsilon_2 + \varepsilon_3 \neq 0$, the membrane energy $U_\text{M}$ can be made to vanish under a variety of conditions. For example, one such condition is purely a longitudinal strain: $\varepsilon = \varepsilon_1;\ \varepsilon_2 = \varepsilon_3 = 0$, while another condition is an oblate strain: $\varepsilon_1 = \varepsilon_2;\ \varepsilon_3 = -\varepsilon_1/2;\ \varepsilon = 3\varepsilon_1/2$. Therefore, if the substructure of all matter is closest to the one represented in Figure 5.4c, then there would be no resulting membrane energy: $U_\text{M} = 0$.

Is the substructure depicted in Figure 5.4c a reasonable description of matter? Indeed. Ordinary matter at different length scales exhibits anisotropies all the way down to subatomic particles that are themselves not solid spheres but waves and therefore not perfectly spherically symmetric. It is reasonable to expect that due to the subatomic particles' wave nature, they induce oscillating strains within the fabric that are asymmetric at any given instant in time but average to an overall isotropic and symmetric volumetric strain in a homogenized manner.

### Discussion

In the previous sections we developed a method for calculating the deformation metric of the cosmic fabric as it bends due to a spherically symmetric inclusion, and we derived a closed form solution (see Equation (5.40)) for the metric in the regime of small strain (weak gravity). Below, we compare this result to the Schwarzschild solution [148] of the Field Equations of General Relativity and to Flamm's visualization of the same [56]. We also discuss future generalizations using numerical methods.

#### Comparison with the Schwarzschild Metric

The Schwarzschild Metric [148] is a solution of the Field Equations of General Relativity for a static spherically symmetric gravitating body. In the weak gravity regime, as assumed here, the Schwarzschild metric can be written in linearized form as follows:

$$
\begin{split}
ds^2_\text{int} &= -\left(1 - \frac{3r_g^2}{2r_0^2} + \frac{r^2}{2r_0^2}\right) c^2 dt^2 + \left(1 + \frac{r^2}{r_0^2}\right) dr^2 + r^2 d\Omega^2 \\
ds^2_\text{ext} &= -\left(1-\frac{r_s}{r}\right) c^2 dt^2 + \left(1+\frac{r_s}{r}\right) dr^2 + r^2 d\Omega^2
\end{split}
\tag{5.53}
$$

where $d\Omega^2 \equiv d\theta^2 + \sin^2\theta\, d\varphi^2$, and $r_0^2 \equiv r_g^3/r_s$. Furthermore, $\overline{r}$, $\theta$ and $\varphi$ are the material polar coordinates in three-dimensional space, and $r = (1+e)\overline{r}$ is the stretched radius as Figure 5.1 indicates.

Both the Schwarzschild metric in Equation (5.53) and the one derived in Equation (5.40) describe the same spacetime as it has been deformed due to a gravitating body of radius $r_g$ and Schwarzschild radius $r_s$. Notice that the time coefficients are the same in both metrics. Also, both metrics result in the same Ricci curvature of space, which is $R^\text{3D} = 6/r_0^2$ in the interior, and $R^\text{3D} = 0$ in the exterior of the gravitating body. The main difference between the two metrics are the spatial coefficients. The metric derived in Equation (5.40) shows that the fractional amount by which space is stretched volumetrically equals the fractional amount by which time lapse has been retarded. While this is true for the exterior Schwarzschild metric, it is not the case for the interior according to Equation (5.53). The reason for this difference is that the metric we derived in Equation (5.40) accounts for the in-plane stretch of physical space that is specified by the radial function $e(\overline{r})$. Without attributing material properties to space, however, the radial stretch $e$ does not have physical meaning, since it does not produce a measurable intrinsic curvature. Therefore, in classical General Relativity, the stretch $e(\overline{r})$ would be viewed as mere coordinate relabeling.

If we expressed the metric we derived in Equation (5.40) in terms of the stretched polar coordinates $(t, r, \theta, \varphi)$ instead of the material polar coordinates $(t, \overline{r}, \theta, \varphi)$, we would recover the linearized Schwarzschild metric per Equation (5.53). Indeed, from $r = (1 + e)\overline{r}$ follows,

$$
\begin{split}
\overline{r} &\approx (1-e)r \\
d\overline{r} & \approx (1 - e - e'r)dr
\end{split}
\tag{5.54}
$$

Consequently,

$$
\begin{split}
\overline{r}_\text{int} &= \left(1 - \frac{r_g^2}{4r_0^2} + \frac{3r^2}{20r_0^2}\right)r; \quad \overline{r}_\text{ext} = \left(1 - \frac{r_s r_0^2}{10r^3}\right)r \\
d\overline{r}_\text{int} &= \left(1 - \frac{r_g^2}{4r_0^2} + \frac{9r^2}{20r_0^2}\right)dr; \quad d\overline{r}_\text{ext} = \left(1 + \frac{r_s r_0^2}{5r^3}\right)dr
\end{split}
\tag{5.55}
$$

Substituting the above into Equation (5.40) yields the linearized form of the Schwarzschild metric in Equation (5.53). Therefore from the perspective of General Relativity, the two metrics are equivalent, because the above substitution constitutes mere coordinate rescaling. In General Relativity, the Schwarzschild solution has a slightly simpler form than the one derived here, which may be the reason why it is preferred, but the solution derived here is consistent with attributing material properties to spacetime.

Arriving at a metric that is equivalent to the classical Schwarzschild metric is significant, because it validates the postulates underlying the Cosmic Fabric model. At the same time, the derived metric has the additional meaning of describing the deformation of a solid and as such it is equivalent to the fabric's Cauchy–Green deformation tensor (see the *Continuum Mechanics* section of Chapter II). This equivalence is also significant, because: 1) it shows that the solid mechanics analogy of gravity is internally consistent, and 2) enables us to relate the rate of time lapse at a point in space to the volumetric expansion of the fabric at that point, which allows us to construct the full spacetime metric from the deformation metric of physical space.

#### Flamm's Paraboloid

Shortly after Karl Schwarzschild published his solution to the Field Equations of General Relativity for the case of spherical symmetry [148], Ludwig Flamm [56] offered a geometric interpretation of it. Flamm considered the spatial geometry of the Schwarzschild metric at a fixed time coordinate. He recognized that the interior metric is equivalent to the metric of a spherical cap and the exterior to that of a paraboloid. The interior cap is generated by revolving a circular arc of radius $r_0$ around its perpendicular bisector within four-dimensional Euclidean space, where $r_0$ is as defined in Table 5.2. The paraboloid is generated by revolving a parabola around its directrix within the same four-dimensional space. In both cases, the axes of revolution coincide with each other and are aligned along a fictitious fourth spatial dimension. Figure 5.5 visualizes the resulting shape, where $w$ is the additional spatial dimension, while the three ordinary spatial dimensions are $x^i,\ i=1\ldots 3$. The shape is known today as "Flamm's Paraboloid," and is used mainly as a pedagogic tool for teaching General Relativity.

![Flamm's Paraboloid.](https://figures.tgtenev.com/tenev2018-dissertation/fig-flamms-paraboloid.svg)

**Figure 5.5.** The bending of the cosmic fabric due to a spherically symmetric inclusion of radius $r_g$ assumes the shape known as Flamm's Paraboloid, which consists of a paraboloid in the exterior of the inclusion, and a spheroid cap of radius $r_0 = 3/(\kappa c^2 \rho)$ within the interior, where $\rho$, $\kappa$, and $c$ are the density of the inclusion, the Einstein constant, and the speed of light, respectively. Only two of the ordinary spatial dimensions are depicted, but the third is implied.

Let $w = w(r)$ be the radial profile of Flamm's paraboloid, where $r$ is the distance from the axis of revolution, and $w$ represents the offset into the fictitious fourth spatial dimension. The closed form for $w$ which Flamm [56] computed is identical to the solution we derived in Equation (5.27) for the transverse displacement $w$ of the cosmic fabric when bending as a result of an inclusion. In other words, the shape that the cosmic fabric attains when bending due to an inclusion is none other than Flamm's Paraboloid.

Until now Flamm's Paraboloid [56] has been mainly referenced for instructional purposes as a way to visualize the bending of space due to a spherical mass. For the first time, we show that Flamm's Paraboloid can be treated as a material body with constitutive properties, whose behavior is dictated by said properties according to solid mechanic's principles.

In addition to arriving at the shape of Flamm's Paraboloid, the solution of the fabric's governing equations also includes a radial stretch, which does not affect the curvature of the fabric. Such a radial stretch is not included in the description of Flamm's Paraboloid, because from a General Relativity perspective, it bears no physical significance and can be construed as mere coordinate rescaling. For the solid mechanics model, however, the radial stretch is significant, because it affects the time lapse rate and the membrane energy density of the fabric.

### Conclusion

In this chapter, we advanced the Cosmic Fabric model beyond what Chapter III and Chapter IV had accomplished, by investigating the details of how mass–energy inclusions interact with the fabric and cause it to bend. This investigation complemented the work in Chapter III which had focused on how the cosmic fabric bends outside of inclusions. In the process, we developed a method for calculating the spacetime metric of the cosmic fabric, which we applied for the case of initially flat fabric and a spherically symmetric inclusion. The derived metric was equivalent to Schwarzschild's [148] up to a rescaling factor that accounted for in-plane stretch. Furthermore, we showed that the fabric bends into the shape known as Flamm's Paraboloid [56].

We demonstrated the scale-dependent nature of the Cosmic Fabric model which is related to its thickness. From an investigation of the total elastic energy, we determined an upper limit for the mass of the largest possible continuous inclusion. We showed that the total membrane energy $W_\text{M}$ varies disproportionately with the size of the inclusion and is therefore length scale dependent, where the fabric's thickness $L$ serves as the length scale parameter. To avoid disproportionately large membrane energy, we reasoned that there must be a limit on the largest possible continuous material body, which we expressed in Equations (5.48), (5.49), and (5.51). Consequently we concluded that matter must have discontinuous substructure as Figure 5.4 illustrated. This result is consistent with the known constitution of matter at atomic and subatomic length scales.

The work presented in this and the previous chapters further validates the Cosmic Fabric model of gravity by showing that it produces results consistent with General Relativity. Unlike General Relativity, however, the Cosmic Fabric model includes a built-in length scale parameter, which leads to interesting predictions such as the discrete nature of matter. By contrast, General Relativity is strictly a continuum theory and therefore has no means of modeling substructure length scales. The length scale dependence that is part of the Cosmic Fabric model but lacks in General Relativity is a necessary and useful aspect of the model that helps bridge between a theory of gravity and other physical theories, such as fundamental theories of matter.

---

## VI. Dark Matter Effect

### Introduction

De Swart et al. [39] present a good review of the historical analysis of dark matter. The notion of dark matter (DM) was introduced in the 1920's and 1930's by Kapteyn [76], Oort [126, 127], Zwicky [173, 174], Holmberg [65], and Smith [151]. Later, in the 1970's and 1980's the notion was popularized by Rubin et al. [144, 145] as a way to explain anomalous rotational curves of galaxies. In addition, DM was also invoked [89] to explain gravitational lensing which was discovered by Lynds and Petrosian [99]. Herein we will use the term "Dark Matter effect" (DM effect) to describe such observations of anomalous gravity. The development of the Standard Cosmological Model, also known as $\Lambda$CDM (where "CDM" stands for Cold Dark Matter), appealed to DM as a means to balance the contents of the universe and provide a mechanism for structure formation during the early epoch since its inception [89]. In this context, the $\Lambda$CDM model predicted that DM must be non-baryonic and has to make up a certain fraction of the total contents of the cosmos, namely about 27%, which is more than 5 times the ordinary (baryonic) matter which, according to the $\Lambda$CDM model, is supposed to comprise only about 5% of the cosmic content [89]. Whereas the DM effect provides an observational support for DM, by contrast, the idea that DM must make up 27% of the contents of the universe is model dependent.

Despite the overwhelming evidence for the DM effect, there has been no direct confirmation [91] for the existence of DM, such as would be, for example, the discovery of the particle responsible for DM. The lack of direct evidence for DM has prompted the development of other models to explain the DM effect, such as the Modified Newtonian Dynamics (MOND) theory introduced in the 1980's by Milgrom [116]. According to MOND, Newton's Second Law of motion must be modified so that in the case of very weak acceleration $a$ such that $a \ll a_0$, where $a_0$ is a universal acceleration scale parameter, the force $F$ associated with $a$ is no longer linear with respect to $a$ but is proportional to its square. A more narrow formulation of MOND is one where only Newton's Gravitational Law needs to be modified as follows:

$$
\begin{split}
ma = F = \frac{G M m}{\mu(a/a_0) \overline{l}^2}, \quad a_0 = 1.2 \times 10^{-10}\ \text{m}\,\text{s}^{-2}
\end{split}
\tag{6.1}
$$

where $M$ and $m$ are, respectively, the mass of a gravitating body and that of a test particle situated a distance $\overline{l}$ from each other and attracted to each other with force $F$. Also, $\mu(x)$ is an interpolation function such that $\mu(x) \to x$ for $x \ll 0$, and $\mu(x)\to 1$ otherwise. Using this simple modification to the Gravity Law, MOND has been successful in explaining the dark matter effect for a great majority of observations [117]. However, there have also been notable outliers, such as galaxies appearing to have too little dark matter [43] to fit into MOND's simple one-parameter model. Randriamampandry and Carignan [137] show that among a sample of fifteen galaxies, six do not fit well MOND if $a_0$ were treated as a universal constant but prefer larger or smaller values for it compared to the one given in Equation (6.1). Problems such as these, and also MOND's empirical nature, that is the lack of satisfactory explanation from first principles, have been continual sources of criticisms. Most recently, Boran et al. [27] have argued that the detection of gravitational waves known as GW170817 [1] has falsified MOND [116] and other [22, 121] "Dark Matter Emulator" theories as they call them, because these would have predicted, contrary to observations, that photons and gravitational waves move along different geodesics.

Herein we propose an alternative explanation to the DM effect, which we call the "Inherent Structure Hypothesis" (ISH). The ISH is the idea that physical space has inherent structure, such as inherent curvature, that exists apart from matter and leads to modified gravity effects. While the ISH refers to inherent structure in general, herein we focus specifically on inherent curvature being one of its quantifiable attributes.

The Cosmic Fabric analogy of General Relativity proposed in Chapters III–V helps motivate and analyze the effect of the Inherent Structure Hypothesis. In the context of the material model of space proposed in this dissertation work, if solid matter can have structure, and space is like a solid object, then it is reasonable to suppose that space too has structure. The work presented here fits within the current limitations of the Cosmic Fabric model, namely weak gravity and nearly static fields, because Dark matter effect is observed at such conditions.

The inherent curvature figures as the additional $\overline{\mathcal{L}}$ term in Equation (1.1) from Chapter I. The extra Lagrangian term represents a modification to the equations of general relativity (Equation (1.3)), because it implies that in the absence of any matter–energy fields ($T_{\mu\nu} = 0$), the intrinsic curvature does not vanish ($R_{\mu\nu} \neq 0$), but equals the inherent curvature of space. Since the Cosmic Fabric model is an analogy of General Relativity (GR), any results derived through it should also be derivable from conventional GR once its field equations have been modified to account for background spatial curvature. Because the ISH does not invoke new physics, but only new initial configuration, namely an initially curved physical space, it therefore avoids the flaw that Boran et al. [27] point out regarding other DM emulator theories.

The idea that the DM effect has a geometrical explanation is not new, but has received relatively little attention so far. For example, Böhmer et al. [24] and later Usman [169] propose an "$f(R)$ modified theory of gravity" to explain the DM effect where the Ricci scalar $R$, which figures in the Einstein–Hilbert action, is replaced with some more general expression $f(R)$. In a limited sense, our approach can be viewed as a special case of an $f(R)$ theory provided that the inherent curvature of space were constant and can be incorporated as a parameter into $f(R)$. However, per the ISH proposed here, the inherent curvature must be a field, and so the ISH is not the same as an $f(R)$ theory. Dolginov [44] does consider the inherent geometry of space as the cause for the DM effect and offers several arguments against the conventional DM explanation, such as the absence of dense dark matter clouds. He states that such problems do not exist if "the dark matter effect is a result of local non-flat geometry of the empty space." However, Dolginov [44] goes only as far as to raise the possibility for the role that inherent structure plays, but comes short of quantifying the effect, and does not compare it to existing DM models as we have done here.

This chapter presents the case for the Inherent Structure Hypothesis (ISH), namely that the Dark Matter (DM) effect is the manifestation of the inherent structure of cosmic space above continuum length scale. We show that the inherent curvature of space amplifies the gravity of ordinary matter that resides in it and we quantify the effect demonstrating that it can feasibly be one and the same as the DM effect. By "inherent curvature" we mean the curvature of space that is uncaused by any matter inclusions. In the context of the Cosmic Fabric analogy of physical space, the inherent curvature corresponds to the neutral shape of the cosmic medium prior to it being tensed or compressed. As part of our presentation, we analyze the range of observations for which the ISH produces equivalent results to other models, such as the DM or MOND explanations, and we propose ways in which the ISH can be experimentally distinguished from these models. In order that we can work with closed form expressions, our calculations are for a spherically symmetric configuration and nearly static conditions, but such limitations are not fundamental to the ideas presented here. Furthermore, although we develop the Inherent Structure Hypothesis in the context of the Cosmic Fabric model, its validity does not depend on said model and the same conclusions can be reached by considering solutions to the GR equations that have been modified to account for inherent intrinsic curvature.

In the remainder of the chapter, we introduce the mathematical tools used for handling spherically symmetric inherent curvature (the *Spherically Symmetric Inherent Curvature* section), after which we derive the expressions for how said curvature affects gravity of ordinary matter (the *Gravity in the Context of Inherent Spherically Symmetric Curvature* section) and how much of it is required to reproduce the effect of a given hypothetical DM distribution. In the *Discussion* section we analyze the conditions under which the Inherent Structure Hypothesis (ISH) proposed here is observationally equivalent with DM and we offer ways to distinguish between the two explanations; we also compare ISH with MOND in the context of sample galactic data, and discuss implication to cosmological models and future work. Finally, we summarize and conclude in the *Summary and Conclusion* section.

### Spherically Symmetric Inherent Curvature

We adapt the coordinate conventions described in the *Deformation, Material and Reference Coordinates* section of Chapter II for a cosmic fabric with a spherically symmetric inherent curvature. The cosmic fabric (physical space) is considered as immersed in a four-dimensional hyperspace within which it can deform. The enclosing hyperspace is flat and has been assigned Cartesian coordinates $y^K,\,K=1\ldots 4$. Within this space, the fabric's spherical symmetry manifests as radial symmetry whose profile is visualized in Figure 6.1. Let $y^K$ be such that $y^4$ is aligned with the axis of symmetry and $y^4 = \overline{w}(\overline{r})$, where $\overline{r}$ is the distance from $y^4$. Another set of coordinates $x^i,\,i=1\ldots 3$ is painted on the fabric, such that $x^i = y^i$. The time coordinate of the fabric, $x^0$, is defined as usual such that $x^0 \equiv c t$, where $c$ is the speed of light and $t$ is time.

![Profile of a spherically symmetric inherent curvature.](https://figures.tgtenev.com/tenev2018-dissertation/fig-dm-profile.svg)

**Figure 6.1.** Profile of a spherically symmetric hypersurface (cylindrically symmetric in four-dimensional space) with material coordinates $(x^1, x^2, x^3)$ immersed within a four-dimensional reference space with coordinates $(y^1, y^2, y^3, y^4)$. The axis of symmetry is $y^4$, and the $y^4$ coordinate of the fabric is such that $y^4 = w(\overline{r})$, where $\overline{r}$ is the distance from the symmetry axis. The hypersurface coordinates $x^i$ have been assigned such that $x^i = y^i$. The relationship between the radial distance element $d\overline{r}$, transverse displacement element $d\overline{w}$, and proper length element $d\overline{l}$ is also indicated.

#### Derivatives of Radial Functions

Spherical symmetry allows us to define and analyze the configuration in terms of radial functions that only depend on the distance $\overline{r}$ from the symmetry center. The mathematical technique used below has been adapted and extended from Chapter V.

Consider the radial function $f = f(\overline{r})$. Given that $\overline{r}^2 = \sum_{i=1}^3 (x^i)^2$, therefore:

$$
\begin{split}
\partial_i \overline{r} &= \frac{x^i}{\overline{r}} \\
\partial_i f &= f'\partial_i \overline{r} = f' \frac{x^i}{\overline{r}} \\
\partial_{ii} f &= f''\frac{(x^i)^2}{\overline{r}^2} + f'\frac{1}{\overline{r}} - f'\frac{(x^i)^2}{\overline{r}^3},\;\text{(no summation)} \\
\nabla^2 f &= f'' + 3 f'\frac{1}{\overline{r}} - f'\frac{1}{\overline{r}} = f'' + 2f'\frac{1}{\overline{r}}
\end{split}
\tag{6.2}
$$

Also, due to the spherical symmetry and without loss of generality, we will only need the values of the above derivatives at conveniently chosen coordinates, such as the following:

$$
\begin{split}
x^1 = \overline{r}; \quad x^2 = x^3 = 0
\end{split}
\tag{6.3}
$$

At these coordinates, the derivatives of $f$ are as follows:

$$
\begin{split}
\partial_1 f = f'; \quad \partial_{11} f = f''; \quad \partial_{22} f = \partial_{33} f = \frac{1}{\overline{r}}f'
\end{split}
\tag{6.4}
$$

where apostrophe indicates differentiation with respect to $\overline{r}$.

#### Derivatives of the Reference Coordinates

The derivatives of the reference coordinates $y^K$ are used to calculate other geometric quantities. We first evaluate the general form of these derivatives, after which we evaluate them for the choice of coordinates (6.3).

Let $\partial_i y^K \equiv \frac{\partial}{\partial x^i} y^K$ and $\overline{w}' \equiv \frac{d}{d\overline{r}}\overline{w}$, and likewise for the second derivatives. Then,

$$
\begin{split}
\partial_i y^4 & = \frac{x^i}{\overline{r}} \overline{w}' \\
\partial_{ij} y^4 &= \frac{x^i x^j}{\overline{r}^2}\overline{w}'' + \frac{1}{\overline{r}}\overline{w}'\left(\delta_{ij} - \frac{x^i x^j}{\overline{r}^2}\right) \\
\partial_i y^k &= \delta_{ki}
\end{split}
\tag{6.5}
$$

where $\delta_{ij}$ is the Kronecker delta. At the chosen coordinates (6.3), the derivatives of $y^K$ become as follows (and likewise, for the second derivatives of $y^K$):

$$
\begin{split}
[\partial_i y^K] &= \begin{pmatrix}
1 & 0 & 0 & \overline{w}'r' \\
0 & 1 & 0 & 0 \\
0 & 0 & 1 & 0
\end{pmatrix};
\quad
[\partial_{ij} y^4] = \begin{pmatrix}
\overline{w}'' & 0 & 0 \\
0 & \frac{1}{\overline{r}} \overline{w}' & 0 \\
0 & 0 & \frac{1}{\overline{r}} \overline{w}'
\end{pmatrix}; \quad \partial_{ij} y^k = 0
\end{split}
\tag{6.6}
$$

#### Spatial Metric Tensor

The undeformed spatial metric $\overline{g}_{ij}$ can be computed as the inner product of the three surface tangent vectors $\partial_i y^L$,

$$
\begin{split}
\overline{g}_{ij} = \partial_i y^L \partial_j y^L
\end{split}
\tag{6.7}
$$

For the chosen coordinates (6.3),

$$
\begin{split}
[\overline{g}_{ij}] &= \begin{pmatrix}
1+(\overline{w}')^2 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} = \begin{pmatrix}
(\overline{l}')^2 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix} \\
[\overline{g}^{ij}] &= [\overline{g}_{ij}]^{-1} = \begin{pmatrix}
(\overline{l}')^{-2} & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{pmatrix}
\end{split}
\tag{6.8}
$$

where we have made the following substitution:

$$
\begin{split}
(\overline{l}')^2 = (\overline{w}')^2 + 1
\end{split}
\tag{6.9}
$$

such that $\overline{l} = \overline{l}(\overline{r})$ represents the proper radial distance from the center of symmetry, that is, the distance as measured from within the fabric (see Figure 6.1).

The first derivatives of the metric can be computed by differentiating Equation (6.7) and evaluating for the special coordinates (6.3). The only non-vanishing derivatives are the following:

$$
\begin{split}
\partial_1 \overline{g}_{11} &= 2 \overline{l}'\overline{l}'' \\
\partial_2 \overline{g}_{12} &= \partial_2 \overline{g}_{21} = \partial_3 \overline{g}_{13} = \partial_3 \overline{g}_{31} = \frac{(\overline{l}')^2 - 1}{\overline{r}}
\end{split}
\tag{6.10}
$$

#### Christoffel Symbols

The Christoffel symbols $\overline{\Gamma}^m_{\;ij}$ characterize how inherent curvature affects field derivatives (see the *Affine Connection and Covariant Derivative* section of Chapter II). These can be calculated from the metric as follows:

$$
\begin{split}
\overline{\Gamma}^m_{\;ij} = \frac{1}{2} \overline{g}^{mk}\left(\partial_j \overline{g}_{ki} + \partial_i \overline{g}_{jk} - \partial_k \overline{g}_{ij}\right),
\end{split}
\tag{6.11}
$$

We proceed to evaluate these for the special coordinate choice (6.3). For the chosen coordinates, the metric is diagonal so we will only need to evaluate the Christoffel symbols for which $i = j$. We do so using the metric values from Equations (6.8) and (6.10). Of the evaluated Christoffel symbols, only the following are non-vanishing:

$$
\begin{split}
\overline{\Gamma}^1_{11} &= \frac{1}{2}\overline{g}^{11}\partial_1 \overline{g}_{11} = \frac{\overline{l}'\overline{l}''}{(\overline{l}')^2} \\
\overline{\Gamma}^1_{22} &= \overline{g}^{11}\partial_2 \overline{g}_{12} = \frac{(\overline{l}')^2-1}{\overline{r} (\overline{l}')^2} \\
\overline{\Gamma}^1_{33} &= \overline{g}^{11}\partial_3 \overline{g}_{13} = \frac{(\overline{l}')^2-1}{\overline{r} (\overline{l}')^2}
\end{split}
\tag{6.12}
$$

### Gravity in the Context of Inherent Spherically Symmetric Curvature

Consider physical space with radially symmetric inherent curvature specified by the displacement function $\overline{w}$ as per the discussion in the *Spherically Symmetric Inherent Curvature* section, which has been deformed due to the presence of a gravitating mass where $g_{ij}$ represents its deformed metric, and $g_{\mu\nu}$ is the metric of the resulting spacetime. A free-falling particle moves along a spacetime geodesic whose equation is given by,

$$
\begin{split}
& \ddot{x}^\alpha + \Gamma^{\alpha}_{\mu\nu} \dot{x}^\mu \dot{x}^\nu = 0, \quad \text{such that}\quad g_{\alpha\beta}\Gamma^{\alpha}_{\mu\nu} = \frac{1}{2} \left( \partial_\nu g_{\mu\beta} + \partial_{\mu} g_{\beta\nu} - \partial_\beta g_{\mu\nu} \right)
\end{split}
\tag{6.13}
$$

where the dot notation represents differentiation with respect to proper time. Consider a particle initially at rest with respect to the fabric and located at the chosen coordinates given in Equation (6.3). Due to the spherical symmetry, the following reasoning applies to any particle that is a distance $\overline{r}$ from the symmetry center. Because the particle is at rest, its initial four-velocity is such that $\dot{x}^0 = c$ and $\dot{x}^i = 0$, where $c$ is the speed of light. Under these circumstances, Equation (6.13) reduces to the following,

$$
\begin{split}
\ddot{x}^1 +c^2\Gamma^1_{00} &= 0, \quad \text{s.t.} \quad g_{11}\Gamma^{1}_{00} = \frac{1}{2}\left(- \partial_1 g_{00} \right) \\
\therefore\ \ddot{x}^1 &= c^2 \frac{\partial_1 g_{00}}{2g_{11}} \approx c^2 \frac{\partial_1 g_{00}}{2 \overline{g}_{11}} = c^2 \frac{\partial_1 g_{00}}{2 (\overline{l}')^2}
\end{split}
\tag{6.14}
$$

The approximation in Equation (6.14) invokes the weak gravity (small strains) assumption due to which the deformed and undeformed metrics are nearly identical, $g_{ij} \approx \overline{g}_{ij}$. However, note that such approximation does not necessarily apply for the spatial derivatives of $g_{ij}$ and $\overline{g}_{ij}$.

Let $a \equiv \ddot{l}$ be the proper radial acceleration, where $l$ stands for the deformed radial distance. Again, due to the weak gravity (small strains) assumption, we can approximate $l \approx \overline{l}$ (the deformed and undeformed proper distances are about the same), and because of the assumed nearly static conditions, the approximation can be carried to the time derivatives so that $\ddot{l} \approx \ddot{\overline{l}}$. Under the nearly static conditions, $\overline{l}'$ also does not change significantly in time, so $\ddot{\overline{l}} \approx \ddot{x}^1 \overline{l}'$ and thus $a \approx \ddot{x}^1 \overline{l}'$, which combined with Equation (6.14) produces the following:

$$
\begin{split}
a \approx \ddot{x}^1 \overline{l}' = c^2 \frac{\partial_1 g_{00}}{2\overline{l}'} = c^2 \frac{\partial_r g_{00}}{2\overline{l}'}
\end{split}
\tag{6.15}
$$

The last equality takes advantage of the spherical symmetry to generalize the expression for $a$ to any location that is a distance $\overline{r}$ from the symmetry center.

From the Time Lapse postulate of the Cosmic Fabric model (see the *Lapse Rate* section of Chapter III) we had derived the following relationship between the time–time component of the deformed spacetime metric and the three-dimensional volumetric strain $\varepsilon$ (see Equation (3.10)):

$$
\begin{split}
g_{00} = -(1 + \varepsilon)^{-2} \approx -1 + 2\varepsilon
\end{split}
\tag{6.16}
$$

Recall that the volumetric strain $\varepsilon$ is a scalar field characterizing the deformation of the fabric in terms of its fractional volumetric increase at a given location in space. Equation (6.16) combined with Equation (6.15) yields the following:

$$
\begin{split}
a = c^2\frac{\varepsilon'}{\overline{l}'},
\end{split}
\tag{6.17}
$$

where we have replaced the approximation sign with an equality sign that applies in the regime of weak gravity (small strains) and nearly static conditions. Notice that the radial derivative of the acceleration, $a'$, is as follows:

$$
\begin{split}
a' = c^2\frac{1}{\overline{l}'}\varepsilon'' - c^2\frac{\overline{l}''}{(\overline{l}')^2}\varepsilon'
\end{split}
\tag{6.18}
$$

The Inclusion Postulate of the Cosmic Fabric model (see the *Inclusions* section of Chapter III) relates the volumetric strain $\varepsilon$ to the density of the gravitating mass. For inherently curved space we must use covariant derivatives, in terms of which the Inclusion Postulate is as follows:

$$
\begin{split}
\nabla_i (\nabla^i \varepsilon) = -\frac{1}{2}c^2 \kappa \rho
\end{split}
\tag{6.19}
$$

where $\nabla_i$ is the covariant derivative with respect to the $x^i$ coordinate, $c$ is the speed of light, $\rho$ is the density of the inclusion, and $\kappa$ is the Einstein constant. The covariant Laplacian can be evaluated from the following identity and using the Christoffel symbols (6.12):

$$
\begin{split}
\nabla_i (\nabla^i \varepsilon) &= \overline{g}^{ij}\left( \partial_{ij} \varepsilon - \overline{\Gamma}^m_{\;ij} \partial_m \varepsilon \right) \\
& = \overline{g}^{11}\partial_{11}\varepsilon - \overline{g}^{11}\overline{\Gamma}^{1}_{\;11}\partial_1 \varepsilon + \overline{g}^{22}\partial_{22} \varepsilon - \overline{g}^{22}\overline{\Gamma}^1_{\;22}\partial_1 \varepsilon + \overline{g}^{33}\partial_{33} \varepsilon - \overline{g}^{33}\overline{\Gamma}^1_{\;33}\partial_1 \varepsilon \\
& = \frac{1}{(\overline{l}')^2}\left[\varepsilon'' - \frac{\overline{l}''}{\overline{l}'}\varepsilon' + \frac{2}{\overline{r}}\varepsilon'\right]
\end{split}
\tag{6.20}
$$

In the last step of the above derivation, we have used the result from Equation (6.2) for the derivatives of a radial function. Combining Equations (6.17)–(6.20), we arrive at the following surprisingly simple differential equation in terms of the proper acceleration:

$$
\begin{split}
a' + \frac{2}{\overline{r}}a = -\frac{1}{2}c^4 \kappa\rho \overline{l}'
\end{split}
\tag{6.21}
$$

whose general solution has the following form:

$$
\begin{split}
a(\overline{r}) = -\frac{1}{\overline{r}^2}\left(C_1 + \frac{1}{2}c^4 \kappa \int_0^r \rho \overline{l}' \xi^2 d\xi\right)
\end{split}
\tag{6.22}
$$

where $C_1$ is a constant of integration, and $\xi$ is the integration variable representing distance from the center of symmetry. To avoid instability as $\overline{r} \to 0$, we require that $C_1 = 0$. Furthermore, since $\kappa \equiv 8\pi G /c^4$, where $G$ is the gravitational constant, Equation (6.22) becomes the following,

$$
\begin{split}
a(\overline{r}) = -\frac{G}{\overline{r}^2} \int_0^{\overline{r}} \rho (4\pi \xi^2) \overline{l}' d\xi = -\frac{G M(\overline{r})}{\overline{r}^2}
\end{split}
\tag{6.23}
$$

where $M(\overline{r})$ represents the gravitating mass enclosed within the coordinate radius $\overline{r}$. That is because the expression $(4\pi \xi^2) \overline{l}' d\xi$ represents the volume of a spherical shell with coordinate radius $\overline{r}$, surface area $4\pi \xi^2$ and thickness $\overline{l}' d\xi$.

Equation (6.23) is none other than Newton's Gravitational Law but expressed in terms of the coordinate distance to the gravitating mass instead of the proper distance. This result is true for our particular choice of coordinates where the coordinate distance $\overline{r}$ is actually the projection of the proper distance $\overline{l}$ onto a flat hypersurface that is perpendicular to the axis of symmetry, as illustrated in Figure 6.2.

Equation (6.23) and Figure 6.2 show how the presence of inherent curvature amplifies the gravitational effect of ordinary matter: since $\overline{r} \le \overline{l}$, the resulting acceleration is greater than what one would have expected from applying Newton's Gravity Law with the proper distance $\overline{l}$. The additional gravitational acceleration might be interpreted as caused by invisible mass, that is dark matter. However, as we demonstrated above, such extra gravitational acceleration could also arise from the inherent curvature of space.

![Inherent shape of space causing the "Dark Matter" effect.](https://figures.tgtenev.com/tenev2018-dissertation/fig-dark-matter-effect.svg)

**Figure 6.2.** The inherent shape of space causing the "Dark Matter" effect. A test particle at $P$ and a proper distance $\overline{l}$ from a body of mass $M_B$ that is located at $B$ experiences gravitational acceleration $a_P$. The magnitude of $a_P$ is greater than predicted by the Inverse Square Law in terms of $\overline{l}$, but matches the prediction of said law when the projected (coordinate) distance $\overline{r}$ is used instead of $\overline{l}$. The critical coordinate distance $r_c$ represents the limit within which the Inherent Structure Hypothesis is observationally equivalent to the hypothetical presence of dark matter. Typically, $r_c$ extends beyond the edge of visible galactic matter.

### Discussion

Below we compare the Inherent Structure Hypothesis (ISH) to other explanations of the Dark Matter effect, and propose how these can be experimentally distinguished from one another. We also discuss the implication of the ISH to cosmological models.

#### Conditions for Observational Equivalence and Falsifiability

We analyze below under what conditions is the Inherent Structure Hypothesis observationally equivalent to the Dark Matter explanation of the Dark Matter effect. For this purpose, we consider the following two questions:

1. Can the effect of any given dark matter distribution be equivalently explained by a geometrically consistent inherent curvature, and
2. Can the effect of any given inherent curvature be equivalently explained by a physically admissible dark matter distribution?

By "geometrically consistent" we mean that the fabric's material does not intersect itself and has no kinks. Also, for the dark matter distribution to be "physically admissible," we require that it has non-negative and finite density. Below, we answer the above questions in the context of spherical symmetry, but we expect that the responses also apply more generally.

To answer the first question above, consider the radial functions $M_\text{DM} = M_\text{DM}(\overline{r})$ and $M = M(\overline{r})$ representing, respectively, the hypothetical dark matter mass and ordinary mass enclosed within some coordinate radius $\overline{r}$ that corresponds to proper distance from the center $\overline{l} = \overline{l}(\overline{r})$. According to the Dark Matter Hypothesis, one would expect that proper acceleration is $a = -G(M + M_\text{DM})/\overline{l}^2$, which in view of Equation (6.23) implies the following:

$$
\begin{split}
\overline{l} = \overline{r} \sqrt{1 + \frac{M_\text{DM}}{M}}
\end{split}
\tag{6.24}
$$

$$
\begin{split}
\overline{l}' = \sqrt{1 + \frac{M_\text{DM}}{M}} + \frac{\overline{r}(M_\text{DM}/M)'}{2\sqrt{1 + M_\text{DM}/M}}
\end{split}
\tag{6.25}
$$

Equation (6.25) fully specifies the equivalent inherent curvature, because once $\overline{l}'$ is known, the displacement function $\overline{w}$ can be computed from Equation (6.9) up to a rigid translation. For the resulting curvature to be geometrically consistent, we require that $1 \le \overline{l}' < \infty$. From Equation (6.25), it is clear that except in the complete absence of visible matter ($M = 0$) it must be the case that $\overline{l}' < \infty$. Furthermore, as long as the ratio between dark to visible matter increases with distance from the center, then $(M_\text{DM}/M)'\ge 0$ and so $\overline{l}' \ge 1$. Both of these are consistent with known observations, because the Dark Matter effect is always observed along with visible matter. Also, dark matter is supposed to dominate the exterior of the galaxies, so that the ratio of the dark to visible matter content enclosed within a given radius increases in the outward direction. Therefore, any known distribution of dark matter can be modeled as inherent curvature.

To answer the second question above, we now consider how an inherent curvature profile specified by the proper distance function $\overline{l} = \overline{l}(\overline{r})$ is interpreted as dark matter content $M_\text{DM}(\overline{r})$. For simplicity, we will focus on distances sufficiently far away from the center of symmetry beyond which the enclosed visible mass does not increase appreciably so that $M(\overline{r}) \approx const$. This simplification is consistent with the structure of galaxies and dark matter models where most of the visible mass is concentrated within the galactic center, while the dark matter halo is supposed to extend well beyond the visible mass of the galaxy. By rearranging Equation (6.24) we obtain the following:

$$
\begin{split}
M_\text{DM} = M\left(\frac{\overline{l}^2}{\overline{r}^2} - 1\right); \quad M'_\text{DM} = 2\frac{M l}{\overline{r}^2}\left(\overline{l}' - \frac{l}{\overline{r}}\right)
\end{split}
\tag{6.26}
$$

For $M_\text{DM}$ to be physically admissible, we require that $M'_\text{DM} \ge 0$, since the reverse implies negative dark matter density. Therefore, we require that,

$$
\begin{split}
\overline{l}' \ge \frac{l}{\overline{r}}
\end{split}
\tag{6.27}
$$

Beyond the boundary of the hypothetical dark matter halo, $M'_\text{DM} = 0$, so $\overline{l}' = \overline{l}/\overline{r}$ implying that $\overline{l}' = const$. Therefore, within the dark matter halo where $M'_\text{DM} > 0$, we would expect that $\overline{l}'$ is monotonically increasing. So, in general, $\overline{l}'$ has to be non-decreasing for the DM effect due to inherent curvature to be explainable by actual dark matter. In other words, we conclude the following:

$$
\begin{split}
\overline{l}'' \ge 0
\end{split}
\tag{6.28}
$$

Given the relationship between $\overline{w}$ and $\overline{l}$ where $(\overline{w}')^2 = (\overline{l}')^2 - 1$, Equation (6.28) means that the radial function $\overline{w}(\overline{r})$ should not change concavity for the equivalent dark matter to be physically admissible as such.

Unless the inherent curvature of space can be maintained globally for the entire cosmos, it will necessarily be the case that beyond certain critical radius $r_c$ the condition stated in Equation (6.28) no longer applies. As Figure 6.2 and Figure 6.3 illustrate, beyond $r_c$, the concavity of $\overline{w}(\overline{r})$ must reverse for the local inherent curvature to return to flat or to some lesser curvature that can be maintained globally. Therefore, beyond such $r_c$ the Inherent Structure and Dark Matter hypotheses are no longer observationally equivalent.

Beyond the critical radius $r_c$, the expected observational differences between the Inherent Structure and Dark Matter explanations provide a way to verify one and falsify the other. In particular, per the Inherent Structure Hypothesis (ISH):

1. At sufficiently large distances from the center of the hypothetical dark matter halo, the dark matter effect will reverse and eventually disappear as if the halo were not present. In other words, a test particle orbiting a galaxy well beyond the critical distance $r_c$ will behave as if no dark matter were enclosed within its orbit.
2. Gravitational systems for which the DM effect is observed will exhibit a relatively more pronounced edge at approximately the critical distance $r_c$ compared to gravitational systems that do not exhibit the DM effect.
3. On the cosmic length scale, the hypothetical "dark matter" will have no net contributions to the contents of the universe. Note that the currently estimated 27% dark matter content is a model-dependent result and therefore does not necessarily falsify the ISH.

Confirming or falsifying any of the above predictions will either confirm or falsify the Inherent Structure hypothesis.

#### Comparison with Modified Newtonian Dynamics (MOND)

We show below that the Inherent Structure Hypothesis yields equivalent results with MOND to within a critical radius $r_c$ for an appropriately chosen inherent curvature profile $\overline{w}(\overline{r})$. For this purpose, we use the following interpolation function:

$$
\begin{split}
\mu(a/a_0) = \frac{1}{1 + a_0/a}
\end{split}
\tag{6.29}
$$

Substituting Equation (6.29) into Equation (6.1) and solving for $a$ yields the following:

$$
\begin{split}
a = -\frac{GM}{2\overline{l}^2}\left(1 + \sqrt{1 + \frac{4a_0 \overline{l}^2}{GM}}\right)
\end{split}
\tag{6.30}
$$

At the same time, since $a = -GM/\overline{r}^2$ per Equation (6.23), where $\overline{r}$ is the coordinate distance, therefore:

$$
\begin{split}
\frac{1}{\overline{r}^2} & = \frac{1}{2\overline{l}^2}\left(1 + \sqrt{1 +\frac{4a_0 \overline{l}^2}{GM}}\right),
\end{split}
\tag{6.31}
$$

which when solved for $\overline{l}$, produces the following result:

$$
\begin{split}
\overline{l} = \overline{r}\sqrt{1 + a_0\frac{\overline{r}^2}{G M}}
\end{split}
\tag{6.32}
$$

From Equation (6.32) we can determine $\overline{l}'$, which substituted into Equation (6.9) brings us to the following result for the displacement $\overline{w}$:

$$
\begin{split}
(\overline{w}')^2 & = \overline{r}^2 \frac{3s^2 + 4 \overline{r}^2}{s (s^2 + \overline{r}^2)}; \quad s \equiv \sqrt{\frac{G M}{a_0}}\\
\overline{w}' &= \frac{\overline{r}}{s}\sqrt{\frac{3 s^2 + 4 \overline{r}^2}{s^2 + \overline{r}^2}}
\end{split}
\tag{6.33}
$$

where $s$ is a scale parameter characterizing the gravitating mass $M$. The solution for $\overline{w}$, which is also plotted in Figure 6.3, is as follows:

$$
\begin{split}
\overline{w} &= \frac{s}{2}\sqrt{AB} - \frac{s}{4}\ln\left( 2\sqrt{A} + \sqrt{B} \right)\\
\text{where} \quad A &\equiv (\overline{r}/s)^2 + 1; \quad B \equiv 4(\overline{r}/s)^2 + 3,
\end{split}
\tag{6.34}
$$

The actual profile of the inherent structure of space need not match exactly the MOND-equivalent one; Figure 6.3 shows how the two might diverge beyond certain critical distance $r_c$. If $r_c$ is sufficiently far outside the edge of the gravitational system under consideration, then the variance with MOND may not be readily observed. That is why in Figure 6.3, the critical distance is illustrated for the case where $r_c > s$. When the actual inherent structure profile illustrated in Figure 6.3 is revolved around the transverse axis, the result is the shape in Figure 6.2.

![MOND-equivalent inherent structure profile.](https://figures.tgtenev.com/tenev2018-dissertation/fig-mond-profile.svg)

**Figure 6.3.** The inherent curvature profile whose effect is equivalent to the MOND model up to a certain critical distance $r_c$. The deviation of the actual inherent structure profile from the MOND-equivalent one takes place beyond the critical distance. The vertical displacement is given by $\overline{w} = \frac{1}{2}s\sqrt{AB} - \frac{1}{4}s\ln\left( 2\sqrt{A} + \sqrt{B} \right)$, where $A \equiv (\overline{r}/s)^2 + 1$, $B \equiv 4(\overline{r}/s)^2 + 3$, $s \equiv \sqrt{GM / a_0}$, and $a_0$, $G$, and $M$ are, respectively, the MOND parameter, the gravitational constant, and the gravitating mass whose gravity is being amplified by the inherent curvature.

Table 6.1 shows that within a diverse sample of galaxies, the vast majority conform to the profile illustrated in Figure 6.3. The table shows that for most galaxies, the characteristic scale $s$ is greater than the radius $R$ of the visible galactic mass, and is also within an order of magnitude of it. Note that in this case $R$ represents the proper distance, which is in general longer than the corresponding undeformed coordinate distance. Therefore, $s$ being greater than $R$ also implies that $s$ is greater than the corresponding coordinate distance. In a few cases, like the Cartwheel galaxy, where the galactic radius appears to exceed the characteristic scale $s$, the associated inherent structure of space likely differs from the generic profile in Figure 6.3. In the case of the Cartwheel galaxy, for example, such variance is not surprising because of the unusual shape of that galaxy.

Interestingly, the relationship between $R$ and $s$ illustrated in Table 6.1 also holds for our Solar System, which suggests that it may apply to smaller gravitational systems and not just galaxies. For example, in the case of the Solar System, $M \approx 1\ \text{M}_\odot$, $R = 1.43\times 10^{14}\ \text{m}$ (the distance between the Sun and Sedna), and consequently $R/s = 0.14$.

The above comparison between the Inherent Structure Hypothesis (ISH) and MOND serves to validate ISH, because MOND has been empirically shown to provide good explanation for the DM effect in most cases [117, 118].

**Table 6.1.** Apparent masses and sizes of galaxies $25\times 10^3$ – $13.4\times 10^9$ light years from Earth. The list is sorted by distance from Earth. The scale factor $s=\sqrt{GM/a_0}$, where $a_0$ is the MOND parameter, is characteristic of the inherent curvature of space associated with that galaxy. The visible radius $R$ is to within an order of magnitude of the characteristic scale $s$. This relationship appears to hold for a broad variety of galaxies. The acronyms LMC and SMC stand for Large Magellanic Cloud and Small Magellanic Cloud, respectively.

| Galaxy | Mass $M$ $[10^9\,\text{M}_\odot]$ | Radius $R$ $[10^3\,\text{ly}]$ | $R/s$ |
|---|---|---|---|
| Milky Way [73, 75, 107, 108, 123] | 1000 | 50.0 | 0.45 |
| LMC [129] | 10 | 7.0 | 0.63 |
| SMC [129] | 7 | 3.5 | 0.38 |
| Andromeda [31, 74, 130] | 1000 | 110.0 | 0.99 |
| M33 [35, 58] | 50 | 30.0 | 1.21 |
| Pinwheel [33] | 100 | 85.0 | 2.42 |
| Whirlpool [124, 162] | 160 | 30.0 | 0.67 |
| Sunflower (M63) [109] | 140 | 49.0 | 1.18 |
| M77 [110] | 1000 | 85.0 | 0.76 |
| Condor [53, 67] | 100 | 261.0 | 7.42 |
| Cartwheel [10] | 4 | 75.0 | 10.67 |
| Malin 1 [17] | 1000 | 325.0 | 2.92 |
| Phoenix Cluster [106] | 2000000 | 550.0 | 0.11 |
| GN-z11 [125] | 1 | 1.5 | 0.43 |

At the same time, the ISH provides a more general and potentially more accurate explanation than MOND. Being a single-parameter model, MOND still leaves a considerable number of outliers [137] where $a_0$ is either too large or too small. By contrast per the ISH such cases simply reflect, respectively, less or more inherent curvature. Furthermore, MOND calls for the modification of a fundamental law of nature, such as Newton's Second Law of motion, or at the very least Newton's Gravity Law, which has far reaching effects. By contrast, the ISH only refers to the properties of a specific object of nature, namely physical space, and only in a specific region. Finally, there are clues within MOND and also from the analysis above to suggest that the likely explanation for the MOND effect is geometrical in nature. One such clue is that the MOND parameter $a_0$, which has been empirically derived, when expressed as length, $l_\text{MOND} \equiv c^2/a_0 = 7.5\times 10^{26}\,\text{m}$, is comparable to the Hubble distance, $l_\text{H} = c/H_0 = 1.4\times 10^{26}\ \text{m}$ where $H_0$ is the Hubble parameter. At the same time, the Hubble distance is characteristic of the size of the visible universe. Another clue is that the characteristic length scale $s$ computed for each gravitational system based on the MOND hypothesis happens to be comparable to the geometrical size of said system (see Table 6.1). Both of these "coincidences" are empirical as opposed to an artifact of the model, so they point to some geometrical (or structural) characteristics of the underlying reality. In fact, MOND's single parameter model seems like a first order approximation for the inherent structure of space.

#### Implication to Cosmological Models

Like MOND and other dark matter alternative models, the Inherent Structure Hypothesis (ISH) is incompatible with the $\Lambda$CDM model, which critically depends on the existence of non-baryonic dark matter [89]. Even more fundamentally, the $\Lambda$CDM model depends on the presupposition known as the Cosmological Principle [89] that at the cosmic length scale (greater than 100 Mpc or $3\times 10^{24}\ \text{m}$) the universe is homogeneous and isotropic, which in essence is a presupposition about the absence of structure at that scale.

By contrast, ISH is based on the presupposition that structure is a fundamental property of nature, and as such, it is an essential element in cosmological models that adopt the same view. Indeed, common experience shows that every sufficiently complex functioning system exhibits structure at its greatest length scale and so the cosmos should be no exception. For this reason, it is quite likely that new cosmological data will soon conclusively repudiate the Cosmological Principle triggering the revision of the Standard Cosmological Model to account for structure at every length scale. The ISH will be well fitted for such revised cosmological model.

What would a cosmological model based on the presupposition of structure look like? According to the ISH, the inherent curvature of space is uncaused by matter, and yet, the galaxy data in Table 6.1 demonstrates a correlation between inherent curvature and matter. Therefore, one must conclude that there is a causal relationship after all but in reverse: the inherent structure of space is what causes matter to form galaxies and galactic clusters in the first place. This idea may also explain the so-called Large Scale Structure of the universe consisting of walls and filaments made up of galaxies and galactic clusters that appear organized into definite forms but are not gravitationally bound together. New cosmological models may appeal to the inherent structure of space as the seed needed for matter-structure formation similarly to how the $\Lambda$CDM model appeals to dark matter for the same purpose.

### Summary and Conclusion

In this chapter we showed that the inherent curvature of physical space (that is curvature uncaused by matter) amplifies the gravitational effects of ordinary matter and produces the kind of gravitational anomalies that are currently attributed to the presence of dark matter. We proposed the Inherent Structure Hypothesis (ISH) stating that the so-called Dark Matter (DM) effect is the manifestation of the inherent structure of space at galactic length scales, and not the result of invisible mass.

We validated the ISH by demonstrating that any DM effect, which can be explained by the Modified Newtonian Dynamics (MOND) theory or by the presence of a DM halo, can be equally well explained by ISH. At the same time, we showed that ISH allows for DM effects that cannot be explained by MOND or by the DM halos. The inherent structure explanation is equivalent to the DM explanation to within some distance from the center of a gravitating system, but beyond that distance, the ISH predicts that the gravitational impact of the hypothetical DM begins to be reversed and is nearly completely eliminated at sufficiently far distances. This is a verifiable prediction that would distinguish our model from other explanations of the DM effect.

In the comparison between the ISH and MOND we noted an interesting relationship between the size of a gravitational system and its Schwarzschild radius through the MOND parameter $a_0$. Such relationship hinted at the structural underpinnings of the DM effect.

The Inherent Structure Hypothesis stems from the principle that structure is a fundamental aspect of matter, space, and nature in general, and as such can be incorporated into cosmological models that subscribe to the same principle.

---

## VII. Numerical Framework for Weak Gravity Dynamics

Earlier chapters detailed the theoretical basis that enables one to use the numerical tools of solid mechanics for solving problems within General Relativity and cosmology. Herein, we apply these ideas as we contribute with a numerical framework that is suited for a category of problems in cosmology, namely those concerning weak gravitational dynamics at galactic length scales.

The *Computational Methods* section of Chapter I discussed a number of mainstream computational techniques, such as the Finite Element Method (FEM), Finite Difference Method (FDM), and the N-Body Method, which find a variety of applications in solid mechanics, General Relativity and Cosmology. To this list, we add the Particle Mesh Method, which is a combination of the FDM and the N-Body Method, where the bodies do not interact with each other directly but through the gravitational potential. In turn, the latter is computed using FDM to solve a Boundary Value Problem based on the Poisson Equation of gravity.

Nearly all numerical methods consist of the following stages: preprocessing, solving, and post-processing. Also, most computational methods include a discretization strategy for reducing the solution domain from infinite to finite number of parameters. The Preprocessing Stage maps the physical problem onto a mathematical model, which usually involves configuring the geometry of the simulated bodies and their initial and boundary conditions. Typically, such a mathematical model is an idealization of the original problem. For example, when modeling the deformation of a body, not all surface details of the body are represented in the model but only what is considered relevant. Likewise, when modeling the large structure formation of the cosmos, stars and even galaxies may be treated as point particles. A divide-and-conquer strategy is often applied during the preprocessing stage, such as defining an element mesh in the case of FEM and FDM, or using a nested set of cells for the N-Body Method. The Solving Stage computes the result of the numerical simulation. Iterative solvers, such as used in FDM and the N-Body Method, compute the result incrementally so that a growing portion of the result becomes available before the computation terminates. By contrast, direct solvers, such as used with FEM, compute the result in one big step by, for example, solving a system of linear equations, so that any part of the result only becomes available upon the completion of the computation. Finally, the Post-Processing stage is when the computation result is analyzed and visualized.

This chapter introduces a MATLAB®-based framework that we have developed for performing numerical experiments in the category of weak gravity dynamics under the conditions of non-flat inherent geometry of space. The chapter also includes several such experiments that illustrate the use of the framework and whose results support the Inherent Structure Hypothesis introduced in Chapter VI. Our framework is based on the Particle Mesh method that has been modified to account for the presence of inherent intrinsic curvature of space. The numerical method described here assumes weak gravity (small strain) and nearly static gravitational fields (low strain rates). As stated in Chapter I, these assumptions are valid for our common experience of gravity. They are also consistent with the conditions under which the Dark Matter effect (see Chapter VI) has been observed, such as the conditions in the peripheries of galaxies and in galactic clusters.

The weak gravity (small strain) assumption allows us to reduce what is generally a four-dimensional (4D) problem to a three-dimensional (3D) one and solve it with conventional 3D numerical tools. That is because under the small strain assumption, the displacement of grid nodes is not a significant factor in the calculations and can be ignored. Geometric quantities, such as the hyperspatial displacement, $w$, the undeformed metric, $\overline{g}_{ij}$, and Christoffel symbols, $\overline{\Gamma}^k_{ij}$, are treated as generic field quantities whose discrete values have been assigned to the nodes of a fixed grid. The metric and Christoffel symbols pertaining to spacetime and to deformed space are also treated in the same way. Although grid nodes are not displaced during deformation, by accounting for these geometric quantities at each node, we are still taking into consideration the undeformed curvature.

The terms "mesh" and "grid" are used interchangeably in this chapter. Typically the former refers to any general subdivision of a body into smaller elements whose vertexes are the nodes of the mesh, while the latter implies a rectangular organization of the nodes. The framework described here is based on a rectangular grid of nodes, in which context both terms have essentially the same meaning.

The broad contributions of the work presented in this chapter include: 1) the modifications to the Particle Mesh method that generalize it for the case of non-flat space, and 2) the specific numerical experiments that showcase the framework and demonstrate that the Inherent Structure Hypothesis is a plausible explanation for the Dark Matter effect.

In the following sections, we describe the mathematical underpinnings of the numerical framework (the *Mathematical Model and Discretization* section) and what it does (the *Numerical Framework* section), and in the *Numerical Experiments* section we apply it to specific numerical experiments. In the *Discussion* section we comment on the important factors for the design of the framework and the experiments that are based on it. Finally, we summarize and conclude in the *Summary and Conclusion* section.

### Mathematical Model and Discretization

Our setup consists of a three-dimensional (3D) rectangular grid of nodes and a set of particles within the grid (see Figure 7.1). Various field quantities, such as density and curvature, can be assigned to each node of the grid and subsequently deduced for an arbitrary point in space by spline interpolation from the nearby node quantities. The inherent intrinsic curvature of space is specified via a displacement function, $\overline{w} = \overline{w}(x^i)$, like the one discussed in Chapter VI and visualized in Figure 6.1, except that here the displacement function is not necessarily spherically symmetric, but can vary independently in each coordinate direction.

![Particle-Mesh grid.](https://figures.tgtenev.com/tenev2018-dissertation/fig-grid.svg)

**Figure 7.1.** The grid nodes, indexed as $(a, b, c)$, are represented with round dots, while particles, indexed with subscript $p$, are represented as larger hollow disks. The indexes $i,j,k = 1\ldots 3$ run over the three spatial dimensions. Some of the quantities associated with the grid nodes and particles are also represented such as: $x^k_{abc}$ (node position), $g_{ij}(x^k_{abc})$ (the metric tensor at location $x^k_{abc}$), $x^i_p$ (the position of the $p^\text{th}$ particle) and $m_p$ (the mass of the $p^\text{th}$ particle). The spacing $h^1_a$ between the grid nodes in dimension 1 varies along that dimension, but remains constant along the remaining dimensions, and likewise for the spacings $h^2_b$ and $h^3_c$.

We will use the following notation:

- $\rho_{abc}$: Latin subscripts in the alphabet range of $a, b, c$ are used to denote the grid indexes of the node to which the subscripted quantity applies, where $a = 1\ldots a_\text{max}$, $b = 1\ldots b_\text{max}$, and $c = 1\ldots c_\text{max}$ on a grid of size $a_\text{max} \times b_\text{max} \times c_\text{max}$ (see Figure 7.1). For example, $\rho_{abc}$ means the mass density at grid node $(a, b, c)$.
- $m_p$: Latin subscript $p$ specifies the particle index. For example, $m_p$ is the mass of the $p^\text{th}$ particle, where $p = 1\ldots p_\text{tot}$ and $p_\text{tot}$ is the total number of particles.
- $x^i$: Latin indexes in the alphabet range of $i, j, k, l = 1\ldots 3$ correspond to the spatial components of vectors and tensors. For example, $x^i_{abc}$ refers to the three spatial coordinates for the grid node $(a, b, c)$. Similarly, $x^i_p$ are the three spatial coordinates of the $p^\text{th}$ particle. Note that $\rho_{abc} \equiv \rho(x^i_{abc})$, because being a field quantity, $\rho$ is a function of the position $x^i$. This alternative way of denoting a field quantity helps with tensor notation where writing the node indexes as subscripts to the tensor quantity could be awkward. For example, $g_{ij}(x^k_{abc})$ denotes the value of the metric tensor $g_{ij}$ at the node $(a,b,c)$.
- $x^\mu, \Gamma^{\mu}_{\;\alpha\beta}$: As usual, Greek indexes $\mu,\nu, \alpha,\beta = 0\ldots 3$ run over the four spacetime dimensions with the $0^\text{th}$ dimension corresponding to time.

We consider a grid of dimensions $a_\text{max} \times b_\text{max} \times c_\text{max}$, for which the spacing between the grid nodes is not necessarily uniform but is specified by the differences $h^1_a$, $h^2_b$, and $h^3_c$, where $a = 1\ldots (a_\text{max}-1)$, and likewise for $b$ and $c$. In other words, $x^1_{abc} = x^1_{(a-1)bc} + h^1_{(a-1)}$, and likewise for $x^2_{abc}$ and $x^3_{abc}$ (see Figure 7.1). The non-uniform spacing of the grid is useful when higher fidelity is needed at some locations but not others, such as the center of a gravitational system compared to its outskirts.

The following are the two governing differential equations, which are based on the Cosmic Fabric analogy of General Relativity under the conditions of weak gravity (small strain) and slow changing fields:

$$
\begin{split}
\ddot{x}^\alpha + \Gamma^{\alpha}_{\mu\nu} \dot{x}^\mu \dot{x}^\nu = 0
\end{split}
\tag{7.1}
$$

$$
\begin{split}
\nabla_i (\nabla^i \varepsilon) = -\frac{1}{2}c^2 \kappa \rho
\end{split}
\tag{7.2}
$$

where $\rho$, $\varepsilon$, $\kappa$, and $c$ are, respectively, matter density, cosmic fabric volumetric strain, the Einstein constant, and the speed of light. Also, $\nabla_i$ is the covariant gradient, so that $\nabla^i \nabla_i$ represents the covariant Laplacian and Equation (7.2) is the covariant Poisson equation. The dot notation stands for differentiation with respect to proper time. Equation (7.1) is that of a geodesic in spacetime, which is the generalization of a straight line to curved space. This equation states mathematically the generalization of Newton's First Law of motion, namely, that a particle free of any forces moves along a geodesic in spacetime. Equation (7.2), which is the same as Equation (3.2) copied here for convenience, is the Inclusion Postulate of the Cosmic Fabric model. Equations (7.1) and (7.2) reflect General Relativity's two-part view of gravity (see the *General Relativity* section of Chapter II), namely that: 1) bent space causes matter to accelerate, and 2) matter bends space.

Equations (7.1) and (7.2) relate to each other via the metric tensor through the following geometric identity,

$$
\begin{split}
g_{\alpha\beta}\Gamma^{\alpha}_{\mu\nu} = \frac{1}{2} \left( \partial_\nu g_{\mu\beta} + \partial_{\mu} g_{\beta\nu} - \partial_\beta g_{\mu\nu} \right),
\end{split}
\tag{7.3}
$$

and through the Time Lapse postulate of the Cosmic Fabric, which for weak gravity can be stated as follows (see Equation (3.7)):

$$
\begin{split}
g_{00} \approx -1 + 2\varepsilon
\end{split}
\tag{7.4}
$$

where $\varepsilon$ is the volumetric strain of the fabric.

In the following subsections, we convert the above equations to a discretized form suitable for use in a numerical simulation. The goal is to be able to compute particle accelerations, so that we can evolve the system starting from a set of initial particle positions and velocities. We begin by developing the technique for discretizing first and second derivatives. Next we use this technique to discretize the metric and Christoffel symbols, the geodesic Equation (7.1), and the covariant Poisson Equation (7.2). Finally, we discuss how the density field quantity $\rho$ is computed for each grid node from the particle masses.

#### Discretization of First and Second Derivatives

We will use a three point stencil along each dimension to discretize the first and second partial derivatives. Following the approach outlined by Sundqvist and Veronis [156], let $f(x^i)$ be a field quantity and let $f_{abc} = f(x^i_{abc})$ be the specific values of this quantity assigned to each grid node. We seek to compute the values $\partial_i f_{abc}$, and $\partial_{ij} f_{abc}$. Below, we do so using concrete values for $i$ and $j$ from which the generalization to any values of $i,j=1\ldots 3$ should be clear.

First, we compute the single and double derivatives, $\partial_i$ and $\partial_{ii}$, respectively, for $i = 1$. Using the Taylor series expansions for $f_{(a-1)bc}$ and $f_{(a+1)bc}$ around the point $x_{abc}$ we obtain the following two equations:

$$
\begin{split}
f_{(a-1)bc} = f_{abc} - h^1_{(a-1)} \partial_1 f_{abc} + \frac{\left(h^1_{(a-1)}\right)^2}{2}\partial_{11} f_{abc} - \frac{\left(h^1_{(a-1)}\right)^3}{6}\partial_{111} f_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.5}
$$

$$
\begin{split}
f_{(a+1)bc} = f_{abc} + h^1_{a} \partial_1 f_{abc} + \frac{\left(h^1_{a}\right)^2}{2}\partial_{11} f_{abc} + \frac{\left(h^1_{a}\right)^3}{6}\partial_{111} f_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.6}
$$

The third power term in the expansion is included to convey the error due to the approximation. By first solving the above two equations for $\partial_1 f_{abc}$ and then for $\partial_{11} f_{abc}$ we obtain the following results:

$$
\begin{split}
\partial_1 f_{abc} = d^1_a {f_{(a+1)bc}}- e^1_a {f_{(a-1)bc}} + (e^1_a - d^1_a){f_{abc}} - \frac{h^1_{(a-1)}h^1_{a}}{6}\partial_{111} f_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.7}
$$

$$
\begin{split}
\partial_{11} f_{abc} &= 2 \left[\frac{d^1_a}{h^1_{(a-1)}}f_{(a+1)bc} + \frac{e^1_a}{h^1_a}f_{(a-1)} - \left(\frac{d^1_a }{h^1_{(a-1)}} + \frac{e^1_a}{h^1_{a}}\right)f_{abc}\right] \\
& - \frac{h^1_{a} - h^1_{(a-1)}}{3}\partial_{111} f_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.8}
$$

where we have made the following substitutions:

$$
\begin{split}
d^1_a & \equiv \frac{h^1_{(a-1)}}{(h^1_{(a-1)} + h^1_a) h^1_a}, \; a = 2\ldots (a_\text{max}-1); \quad d^1_1 \equiv \frac{1}{h^1_1}; \quad d^1_{a_\text{max}} \equiv 0 \\
e^1_a & \equiv \frac{h^1_a}{(h^1_{(a-1)} + h^1_a) h^1_{(a-1)}}, \; a = 2\ldots (a_\text{max}-1); \quad e^1_1 \equiv 0 \quad e^1_{a_\text{max}} \equiv \frac{1}{h^1_{(a_\text{max}-1)}}
\end{split}
\tag{7.9}
$$

After dropping the high-order terms, we can write the finite difference approximations of the first and second derivative in terms of the operators $\Delta_{1}$ and $\Delta_{11}$ defined as follows:

$$
\begin{split}
\partial_1 f_{abc} \approx \Delta_1 f_{abc} \equiv d^1_a {f_{(a+1)bc}}- e^1_a {f_{(a-1)bc}} + (e^1_a - d^1_a){f_{abc}}
\end{split}
\tag{7.10}
$$

$$
\begin{split}
\partial_{11} f_{abc} \approx \Delta_{11} f_{abc} \equiv 2 \left[\frac{d^1_a}{h^1_{(a-1)}}f_{(a+1)bc} + \frac{e^1_a}{h^1_a}f_{(a-1)} - \left(\frac{d^1_a }{h^1_{(a-1)}} + \frac{e^1_a}{h^1_{a}}\right)f_{abc}\right]
\end{split}
\tag{7.11}
$$

The discretization of $\partial_i$ and $\partial_{ii}$ for $i = 2, 3$ can be computed analogously. The approximation of the second derivative in Equation (7.11) is known as the central differencing scheme.

Equations (7.10) and (7.11) show that the discretized derivative for a value at a node is some linear combination of the values at adjacent nodes. Based on this observation, we can replace the finite difference operators $\Delta_i$ and $\Delta_{ii}$ with linear ones. Let us define:

$$
\begin{split}
n_{abc} &\equiv 1 + a_\text{max} b_\text{max}(c-1) + a_\text{max}(b-1) + (a-1) \\
n_\text{max} & \equiv a_\text{max} b_\text{max} c_\text{max} \\
F_{n_{abc}} &\equiv f_{abc} \\
D^{(1)}_{n_{abc}n_{(a+1)bc}} & \equiv d^1_a; \quad D^{(1)}_{n_{abc}n_{(a-1)bc}} \equiv -e^1_a; \quad D^{(1)}_{n_{abc}n_{abc}} \equiv e^1_a - d^1_a \\
D^{(11)}_{n_{abc}n_{(a+1)bc}} & \equiv \frac{2d^1_a}{h^1_{(a-1)}}; \quad D^{(11)}_{n_{abc}n_{(a-1)bc}} \equiv \frac{2e^1_a}{h^1_a}; \quad D^{(11)}_{n_{abc}n_{abc}} \equiv -\frac{2d^1_a }{h^1_{(a-1)}} - \frac{2e^1_a}{h^1_{a}}
\end{split}
\tag{7.12}
$$

and likewise for $D^{(i)}_{nm}$ and $D^{(ii)}_{nm}$ where $i = 2,3$ and $n, m = 1\ldots n_\text{max}$. Note that the above definitions only apply when the indexes $(a,b,c)$ are within their respective bounds. So, for example, $D^{(1)}_{n_{abc}n_{(a-1)bc}}$ is only defined for $a = 2\ldots a_\text{max}$. The discretization of the mixed derivative $\partial_{ij}$ for $i \neq j$, is simply the combination of the respective first derivatives:

$$
\begin{split}
D^{(ij)}_{nm} = D^{i}_{nt} D^{j}_{tm}, i \neq j
\end{split}
\tag{7.13}
$$

where summation of repeated indexes is implied. Given the above definitions, Equations (7.10) and (7.11) can be formulated as follows:

$$
\begin{split}
F^{(i)}_n &= D^{(i)}_{nm} F_m \\
F^{(ij)}_n &= D^{(ij)}_{nm} F_m
\end{split}
\tag{7.14}
$$

where we have let $F^{(i)}_{n_{abc}} \equiv \Delta_i f_{abc}$ and $F^{(ij)}_{n_{abc}} \equiv \Delta_{ij} f_{abc}$. Notice that the $D$ matrices only depend on the grid spacing and can therefore be precomputed during the preprocessing stage.

The method described above applies to computing field derivatives at the location of each grid node. In order to compute a field derivative of some field quantity at an arbitrary location, we would first compute the field derivative at the grid nodes and use spline interpolation to determine the value of the derivative at the given location.

#### Discretization of the Undeformed Metric and Christoffel Symbols

The undeformed metric and Christoffel symbols can be computed during the preprocessing stage from the following analytical formula:

$$
\begin{split}
\overline{g}_{ij} &= \delta_{ij} + \partial_i \overline{w} \partial_j \overline{w} \\
\overline{\Gamma}^{k}_{\;ij} &= \frac{1}{2}\overline{g}^{kl}\left(\partial_j \overline{g}_{il} + \partial_i \overline{g}_{lj} - \partial_l \overline{g}_{ij} \right).
\end{split}
\tag{7.15}
$$

where $\overline{w} = \overline{w}(x^i)$ is the displacement of the cosmic fabric into the fourth hyperspatial dimension, by which the user specifies inherent curvature (see Chapter VI). In discretized form, the above formula becomes the following:

$$
\begin{split}
G^{(ij)}_n &= \delta_{ij} + \left(D^{(i)}_{nm}W_m\right)\circ(D^{(j)}_{nm}W_m) \\
J^{(kij)}_n &= \frac{1}{2}\operatorname{inv}\left[G^{(kl)}_n\right]\circ \left( D^{(j)}_{nm}G^{(il)}_m + D^{(i)}_{nm}G^{(lj)}_m - D^{(l)}_{nm}G^{(ij)}_m \right)
\end{split}
\tag{7.16}
$$

where $G^{(ij)}_{n_{abc}}\equiv \overline{g}_{ij}(x^k_{abc})$, $W \equiv \overline{w}_{abc}$, and $J^{(kij)}_n \equiv \overline{\Gamma}^{k}_{\;ij}(x^k_{abc})$. Furthermore, the operator $\operatorname{inv}$ applies to $G$'s parenthesized indexes and represents a $3 \times 3$ matrix inversion, the binary operator $\circ$ represents element-wise multiplication *with respect to the unparenthesized indexes*, summation over repeated indexes is implied, and the $D$ matrices are defined per Equations (7.12) and (7.13). Note that the element-wise multiplication of vector elements that is represented by the binary operator $\circ$ can be substituted with regular matrix multiplication provided that the vectors are treated as diagonal matrices with the diagonal elements being the vector elements.

#### Discretization of the Geodesic Equation

The geodesic equation is used to compute particle acceleration for a given gravitational field. Using the chain rule, we can rewrite Equation (7.1) to be in terms of coordinate time instead of proper time:

$$
\begin{split}
\partial_{00} x^{\mu} = -\Gamma^{\mu}_{\;\alpha\beta}\partial_0 x^\alpha \partial_0 x^\beta + \Gamma^0_{\;\alpha\beta}\partial_0 x^\alpha \partial_0 x^\beta \partial_0 x^\mu
\end{split}
\tag{7.17}
$$

For simulation purposes, we need to use a notion of time that is common to all particles, but proper time is by definition particle-specific. This is why we work in terms of coordinate time. Thus, $\partial_{00} x^{\mu}$ is the $\mu^\text{th}$ component of the particle's coordinate acceleration, while $\partial_0 x^\mu$ is the $\mu^\text{th}$ component of the particle's coordinate velocity. Notice that for $\mu = 0$ (acceleration in the time direction), both sides of Equation (7.17) vanish identically since $\partial_0 x^0 = 1$, because the speed of coordinate time is always one second per second. In fact, we are only interested in the spatial components of the particle acceleration, $\partial_{00}x^k$.

In the case of slow changing fields, the time derivatives, $\partial_0$, of field quantities and the time-space components of the metric, $g_{i0}$ and $g_{0i}$, are all negligible. Consequently, some of the Christoffel symbols vanish and the remaining ones are as follows:

$$
\begin{split}
\Gamma^0_{\;i0} &= \Gamma^0_{\;0i} = \frac{\partial_i g_{00}}{2g_{00}};\quad \Gamma^0_{00} = \Gamma^0_{ij} = 0 \\
\Gamma^k_{00} &= -\frac{1}{2}g^{kl}\partial_l g_{00}; \quad \Gamma^{k}_{\;i0} = \Gamma^{k}_{\;0i} = 0 \\
\Gamma^{k}_{\;ij} &= \frac{1}{2}g^{kl}\left(\partial_j g_{il} + \partial_i g_{lj} - \partial_l g_{ij} \right),
\end{split}
\tag{7.18}
$$

which when substituted into Equation (7.17) and evaluated for the spatial components of the particle acceleration, produce the following:

$$
\begin{split}
\partial_{00} x^k &= -\Gamma^k_{\;00}(\partial_0 x^0)^2 + 2 \Gamma^0_{\;0i}\partial_0 x^k \partial_0 x^i - \Gamma^k_{\;ij} \partial_0 x^i\partial_0 x^j \\
& = \frac{1}{2}g^{kl}\partial_l g_{00} + \frac{\partial_i g_{00}}{g_{00}}\partial_0 x^i \partial_0 x^k - \Gamma^k_{\;ij} \partial_0 x^i\partial_0 x^j
\end{split}
\tag{7.19}
$$

Notice that although we have assumed that the fields are slow changing, we do not assume that particle velocities are slow, but that individual particles could achieve speeds comparable to $c$. Therefore, while we can approximate the time derivatives of field quantities as vanishing, we do not make the same approximation for the time derivatives of particle quantities. In a typical configuration, such as a galaxy, the total gravitational field is the combined effect of a large number of particles (billions of stars), so as long as the collection of particles as a whole moves slowly through space, then the motion of individual particles (stars) will not cause the gravitational field to change rapidly except in its immediate vicinity.

Next, we invoke the weak gravity (small strain) assumption to approximate the spatial curvature of the deformed fabric with that of the undeformed one: $g_{ij} \approx \overline{g}_{ij}$ and $\Gamma^k_{\;ij} \approx \overline{\Gamma}^k_{\;ij}$. Furthermore, from Equation (7.4) follows that $\partial_l g_{00} \approx 2\partial_l \varepsilon$. Finally, we recognize that since $x^0 = ct$, where $t$ is coordinate time, then $a^k = c^2 \partial_{00} x^k$ and $v^k = c \partial_0 x^k$, where $a^k$ and $v^k$ are, respectively, the particle's coordinate acceleration and velocity. When these substitutions are made into Equation (7.19), we arrive at the following formula for the acceleration $a^k$:

$$
\begin{split}
a^k = c^2\overline{g}^{kl} \partial_l \varepsilon - \frac{2 \partial_i \varepsilon}{1 - 2\varepsilon} v^i v^k - \overline{\Gamma}^k_{\;ij}(x^k) v^i v^j
\end{split}
\tag{7.20}
$$

Note that in the absence of intrinsic curvature ($\overline{g}^{ij} = \delta^{ij}$) and for the case of slow particle velocities ($v^i \ll c$) the last two terms vanish. Moreover, per Equation (3.27), $\varepsilon = -\Phi/c^2$, so Equation (7.20) becomes the classical equation for gravitational acceleration: $a^k = -\partial^k \Phi(x^k)$. Notice also that in the case when a particle's velocity is a non-negligible fraction of the speed of light, then the second term in Equation (7.20) reduces the coordinate acceleration, which prevents the particle from achieving superluminal speed. This is why accounting for this term is important for the numerical simulation. Finally, the last term represents the influence of the inherent (undeformed) curvature on the acceleration computation for the case of fast particles.

The discretized version of the particle acceleration Equation (7.20) can now be derived and is as follows:

$$
\begin{split}
A^{(k)}_p = \left. c^2 \operatorname{inv}\left[G^{(kl)}_n\right]\circ D^{(l)}_{nm}E_m \right|_p - \left. \frac{2 D^{(i)}_{nm} E_m}{1 - 2 E_n}\right|_p \circ V^{(i)}_p \circ V^{(k)}_p - \left. J^{(kij)}_n \right|_p \circ V^{(i)}_p \circ V^{(j)}_p
\end{split}
\tag{7.21}
$$

where $E_n$ is an $n$-component vector, such that $E_{n_{abc}} \equiv \varepsilon_{abc}$. Furthermore, $V^{(k)}_p$ and $A^{(k)}_p$ are, respectively, the velocity and acceleration components of the $p^\text{th}$ particle. The notation $\left.X\right|_p$ means that the quantity $X$ should be interpolated from its grid node values for the location of the $p^\text{th}$ particle. The division operation in the second term of the above expression should be understood as element-wise.

#### Discretization of the Poisson Equation

Given the following expansion of the covariant Laplace operator in terms of the metric and Christoffel symbols,

$$
\begin{split}
\nabla_i (\nabla^i \varepsilon) = \overline{g}^{ij}\left( \partial_{ij} - \overline{\Gamma}^k_{\;ij} \partial_k \right)\varepsilon
\end{split}
\tag{7.22}
$$

the Covariant Laplacian $\nabla_i (\nabla^i \varepsilon)$ is discretized as follows:

$$
\begin{split}
L_{nm} \equiv \operatorname{inv}\left[G^{(ij)}_n\right]\circ \left(D^{(ij)}_{nm} - J^{(kij)}_n \circ D^{(k)}_{nm} \right)
\end{split}
\tag{7.23}
$$

where the matrix inversion is with respect to the upper indexes $(ij)$.

Discretizing the Poisson Equation (7.2) requires that we take into account the following boundary conditions,

$$
\begin{split}
\varepsilon_{abc} = \varepsilon^{*}_{abc}, \quad \text{for boundary nodes } (a,b,c)
\end{split}
\tag{7.24}
$$

where a "boundary node" $(a, b, c)$, as opposed to an "interior node" is one for which at least one of the following is the case: $a \in \{0, a_\text{max}\} \text{ or } b \in \{0, b_\text{max}\}, \text{ or } c \in \{0, c_\text{max}\}$. Furthermore, the strains $\varepsilon^{*}_{abc}$ stand for user-specified boundary quantities. Consequently, we arrive at the following discretization for the Poisson Equation:

$$
\begin{split}
&Q_{nm} E_m = S_n \\
&\quad \text{where} \\
& \quad Q_{n_{abc}m} \equiv \begin{cases} L_{n_{abc}m}, & \text{when } (a,b,c) \text{ is an interior node} \\ 1, & \text{when } (a, b, c) \text{ is a boundary node} \end{cases} \\
& \quad S_{n_{abc}} = \begin{cases} -\frac{1}{2}c^2\kappa \rho_{abc}, & \text{when } (a,b,c) \text{ is an interior node} \\ \varepsilon^{*}_{abc}, & \text{when } (a,b,c) \text{ is a boundary node} \end{cases} \\
& \quad E_{m_{abc}} = \varepsilon_{abc}
\end{split}
\tag{7.25}
$$

Solving Equation (7.25) amounts to solving a linear system of $n$ equations where the matrix $Q_{nm}$ is sparse and banded. A banded matrix consists of a main diagonal and $m$ pairs of secondary diagonals that are parallel to the main one within a narrow band. An optimal solver for such type of matrices can compute the solution within $\mathcal{O}(m^2 n_\text{max})$ time. For the case of flat geometry, $m = 3$, but could be as large as $m = 13$ for non-flat geometry. Numerical platforms, such as MATLAB®, have built-in routines to perform just this type of calculation. Notice also that the matrix $Q_{nm}$ in Equation (7.25) can be computed during the preprocessing stage.

#### Density Computation

The matter density, which figures as the source in the Poisson Equation (7.2) and in its discretized version in Equation (7.25), is computed from the following two sources: 1) predefined fixed matter density associated with each node, and 2) density due to the particle distributions, which may vary from one time step to another. The former is specified directly by the user as part of setting up a numerical experiment; the computation of the latter is described below. These two are added together to produce the total density and its value is assigned to each grid node.

Each particle contributes to the matter density value associated with the grid nodes in its immediate neighborhood. Let $\Omega_{abc}$ represent the rectangular space bounded by eight adjacent grid nodes such that two of them are $(a, b, c)$ and $(a+1, b+1, c+1)$, and let $p \in \Omega_{abc}$ denote the fact that the $p^\text{th}$ particle is located somewhere within $\Omega_{abc}$. Define $\xi^1_a \equiv x^1_p - x^1_{abc}$ to denote the coordinate differences between the coordinates of the particle and the node $(a, b, c)$, and likewise for $\xi^2_b$ and $\xi^3_c$. Therefore, the following expression $(1 - \xi^1_a/h^1_a)(1-\xi^2_b/h^2_b)(1-\xi^3_c/h^3_c)$ represents the fraction of the particle's mass that will be ascribed to node $(a, b, c)$, while $(\xi^1_a/h^1_a)(\xi^2_b/h^2_b)(\xi^3_c/h^3_c)$ is the fraction of mass ascribed to node $(a+1, b+1, c+1)$, and so on for the other six nodes that are the vertexes of $\Omega_{abc}$. Note that the sum of all such fractional contributions is unity.

To compute the mass density $\rho_{abc}$ at a given node $(a,b,c)$, we will consider all of the particles' contributions from the eight adjacent spaces, $\Omega_{(a-1)(b-1)(c-1)}, \Omega_{a(b-1)(c-1)}\ldots \Omega_{abc}$. Therefore,

$$
\begin{split}
\rho_{abc} &= \rho^{*}_{abc} + \frac{8}{\mathcal{V}_{abc}} \left\{ \sum_{p\in \Omega_{(a-1)(b-1)(c-1)}} m_p \frac{\xi^1_{(a-1)}}{h^1_{(a-1)}}\frac{\xi^2_{(b-1)}}{h^2_{(b-1)}}\frac{\xi^3_{(c-1)}}{h^3_{(c-1)}} \right. \\
& +\sum_{p\in \Omega_{a(b-1)(c-1)}} m_p \left(1 - \frac{\xi^1_{a}}{h^1_{a}}\right)\frac{\xi^2_{(b-1)}}{h^2_{(b-1)}}\frac{\xi^3_{(c-1)}}{h^3_{(c-1)}} + \ldots \\
& \left. +\sum_{p\in \Omega_{abc}} m_p \left(1 - \frac{\xi^1_{a}}{h^1_{a}}\right) \left(1 - \frac{\xi^2_{b}}{h^2_{b}}\right) \left(1 - \frac{\xi^3_{c}}{h^3_{c}}\right) \right\} \\
& \text{where} \quad \mathcal{V}_{abc} \equiv \sqrt{\overline{g}_{abc}}\,(h^1_{(a-1)} + h^1_a)(h^1_{(b-1)} + h^1_b)(h^1_{(c-1)} + h^1_c)
\end{split}
\tag{7.26}
$$

where $\mathcal{V}_{abc}$ represents the proper volume of the rectangular space bounded by the nodes $(a-1, b-1, c-1)$ and $(a+1, b+1, c+1)$ that is made up of the eight smaller rectangular spaces each of which corresponds to a summation expression in Equation (7.26). Furthermore, $\overline{g}_{abc} \equiv \det \overline{g}_{ij}(x^k_{abc})$, and $\rho^{*}_{abc}$ is the fixed density at node $(a,b,c)$ that has been pre-assigned by the user. Note that $\mathcal{V}_{abc}$ can be computed during the preprocessing stage.

We have found out that the precision of the particle density calculation worsens with larger variations of the grid spacing. For such situations, we use an auxiliary grid of uniform spacing at whose nodes we calculate the particle densities by the above scheme. Then, we interpolate the resulting values onto the nodes of the main grid. The number of nodes in this auxiliary grid can be much larger than those of the main grid, because it does not affect the solving of the Poisson Equation, which is typically the most time consuming step of the simulation.

### Numerical Framework

Using MATLAB®, we implemented a numerical framework based on the mathematical model discussed in the *Mathematical Model and Discretization* section. Its features allow the user to define and run numerical experiments in weak gravity under conditions of various kinds of intrinsic curvature (or none) that may involve point particles or gravitating mass densities or both. The difference between point particles and mass densities is that the former are modeled as having no spatial extent but can move, while the latter occupy finite volume but are fixed. Point particles and mass densities interact indirectly with each other through the gravitational field in whose creation they participate. The framework does not model direct interaction such as collision or friction between particles and densities.

There are two broad categories of numerical experiments that can be performed with the framework: 1) static evaluation of gravitational fields, and 2) time evolution of point particles. For experiments in the first category, the Poisson equation of gravity, Equation (7.25), is solved once and the resulting gravitational field is analyzed. The experiments presented in the *Numerical Experiments* section fall into this category. For the second category of experiments, the Poisson Equation is solved once for each time step. At each iteration, the volumetric strain, which is the solution of the Poisson Equation, is used to compute the accelerations of the point particles and update their positions and velocities.

#### Input Parameters

The following are the input parameters that specify a numerical experiment within the framework:

1. Configuration of a three-dimensional rectangular mesh that has $a_\text{max} \times b_\text{max} \times c_\text{max}$ nodes and represents a volume of space that is $|x^1_\text{max} - x^1_\text{min}| \times |x^2_\text{max} -x^2_\text{min}| \times |x^3_\text{max} - x^3_\text{min}|$ large. The nodes along each edge need not be evenly spaced, so some parts of the mesh can be finer than others. The framework allows edge nodes to be distributed linearly, quadratically, or cubicly within user-specified ranges. In the latter cases, the points are denser in the middle of a range and less so near its two ends according to a quadratic or cubic function, respectively.
2. Intrinsic curvature defined in terms of the function $w = w(x^1, x^2, x^3)$, which is the displacement into the fourth (hyperspatial) dimension.
3. A set of fixed mass density distributions, such as those representing large gravitating bodies or dust clouds.
4. A set of point particles specified in terms of their masses $m_p$ where $p = 1\ldots p_\text{tot}$ and $p_\text{tot}$ is the total number of particles, their initial positions $x^i_p$ and velocities $v^i_p$.
5. Boundary conditions specifying the volumetric fabric strain at the edge nodes and face nodes of the mesh. (In the current implementation, the boundary values of the volumetric strain are assumed to approximately vanish, which is generally true if the mesh is made large enough such that gravitating masses are near the center of the mesh.)

#### Preprocessing Stage

During the preprocessing stage, the framework builds the grid illustrated in Figure 7.1, computes the derivative matrices $D^{(i)}_{nm}$ and $D^{(ij)}_{nm}$ (see the *Discretization of First and Second Derivatives* section), which are then used to compute the metric $G^{(ij)}_{n}$ and the Christoffel symbols. Finally, the $Q_{nm}$ matrix is computed (see the *Discretization of the Poisson Equation* section) that is used in the solution of the Poisson equation. At this stage, the framework also pre-computes the velocity-independent coefficients in the geodesic Equation (7.21), which is used during the Solving Stage to evaluate particle accelerations. Some of these preprocessing operations are computationally expensive and being able to perform them ahead of time and not at each iteration during the solving stage is important for the efficiency of the algorithm.

#### Solving Stage

The Solving Stage begins by computing the aggregate density distribution of matter within the mesh, which consists of accounting for particle density and user-inputted fixed densities as described in the *Density Computation* section. This aggregate density (from point particles and fixed density) figures in the right-hand side of the Poisson Equation (7.25). Solving Equation (7.25) is at the heart of the solving stage and is the most computationally intensive step. MATLAB®, which is the engine running our framework, uses a set of heuristics to decide the best way to solve the linear system of equations [101]. In our case, since the $Q_{mn}$ matrix is banded, a banded solver is used. In the current implementation of the framework, we assume that the grid is always constructed large enough so that the strain at the boundary is nearly vanishing. In other words, we assume that in Equation (7.25) the quantities $\varepsilon^{*}_{abc} = 0$.

The volumetric strain field $\varepsilon$ is evaluated as the solution of the Poisson Equation. It is used in the computation of particle accelerations based on the Geodesic Equation (7.21). What happens in the next step of the Solver Stage depends on the type of numerical experiment that is being conducted. If the goal is to study the gravitational field for a particular configuration, then the Solving Stage ends here. The first coefficient in Equation (7.21) describes the acceleration field for particles that are at rest (or nearly at rest) and can be used to compute, for example, galaxy rotation curves, as we have done in the numerical experiments presented in the *Numerical Experiments* section.

Alternatively, if the goal is to study the evolution of particles, then as its next step, the Solver Stage determines individual particle accelerations from Equation (7.21). For a given time step, the framework advances the particles' positions based on their velocities, and updates the particles' velocities based on the thusly computed accelerations, as the following code snippet illustrates:

```matlab
function runStep(obj, timeStep)
% Runs the simulation for one time step

    obj.computeDensity;
    obj.solvePoisson;
    obj.computeParticleAccelerations;

    for i = 1:3
        obj.px{i} = obj.px{i} + obj.pv{i}*timeStep;
        obj.pv{i} = obj.pv{i} + obj.pa{i}*timeStep;
    end
end
```

where `obj` refers to the simulation object instance, while `px`, `pv`, and `pa` are MATLAB®'s representation of the $x^i_p$, $v^i_p$ and $a^i_p$ vectors corresponding, respectively, to the particles' positions, velocities, and acceleration. For example, `px{1}` is represented numerically as a vector of $p_\text{tot}$ elements where the $p^\text{th}$ element corresponds to the $x^1$ coordinate of the $p^\text{th}$ particle and so on.

#### Post Processing Stage

The Post Processing Stage is when various numerical "measurements" are performed on the state of the system to extract and visualize information about simulated physical quantities. Below is a list of the kinds of measurements supported by the framework.

1. Visualization of the grid nodes used for diagnostics and debugging. Figure 7.1 illustrates this type of visualization.
2. Visualization of a scalar field, such as the density $\rho$, the metric determinant, $|g|$, the displacement function $w$, and volumetric strain $\varepsilon$. The top panels of Figure 7.4 and Figure 7.3a illustrate this type of visualization.
3. Visualization of particle scalar quantities, such as their masses, and particle vector quantities, such as their velocities and accelerations.
4. Profile of a scalar quantity along a path, such as the volumetric strain $\varepsilon$ along the $x^1$ dimension, which is illustrated in the bottom panels of Figure 7.4 and Figure 7.3a.

#### Validation

Validation of the framework includes validating its individual components as well as end-to-end validation. The latter involves applying the framework to a well understood configuration and comparing the outcome to the expected result; such validation is discussed in the *Numerical Experiments* section. Component validation consisted of verifying that all of the following procedures behave as expected: mesh generation, discretization of the derivatives, metric and Christoffel symbol computation, and density computation.

Validating the mesh was performed by generating meshes with different ranges and spacing for the edge nodes, and visualizing the result to verify that the mesh was built correctly. Figure 7.2 illustrates an example of mesh visualization. Validating the discretization of derivatives, the computation of the metric tensor and Christoffel symbols was performed together because the latter two depended on the former. Once computed, the components of the metric and of the Christoffel symbols were visualized using MATLAB® slice plots to verify that these quantities have the expected form. A "slice plot" is used to visualize three-dimensional data through a combination of planar color map visualizations that slice through the data at predefined locations. In addition, the above tests were performed using variable as well as fixed node spacing to ensure that introducing node spacing variation does not qualitatively affect the result. Density computation was validated by generating spherically distributed particles and then visualizing the resulting density through slice plots, as well as integrating the density over the volume and verifying that the result matches the total particle mass to within some tolerance.

### Numerical Experiments

Using the numerical framework described in the *Numerical Framework* section, below we performed two sets of numerical experiments. The first experiment is used to validate the model by simulating gravity under known conditions, namely that of our Sun, and comparing the results to the theoretical predictions of classical Newtonian gravity. The second experiment applies the framework to analyze the effects of inherent curvature on the rotation curve of the Triangulum galaxy, which is also known as Messier 33 (M33).

#### Validation of the Framework by Simulating the Sun's Gravity

The goal of this experiment was to validate the framework by modeling the gravitational acceleration due to the Sun using the building blocks of the framework and comparing the result to the theoretical predictions. We did not include any inherent curvature. The mesh, which is visualized in Figure 7.1, was configured with variable spacing, and initialized according to the following code:

```matlab
SUN_R       = 6.95508e+8;           % Solar radius [m]
SUN_EARTH   = 1.496e+11;            % Sun-Earth distance [m]
SUN_SEDNA   = 1.346e+13;            % Sun-Sedna distance [m]

mesh_extent = 20*SUN_SEDNA;         % Spatial extent of the mesh

%
% Specify the edge points from which the mesh is built. There are three
% sets of these to get the optimal resolution with least total amount of
% nodes, as follows: 1) for resolving the shape of the sun, 2) for
% resolving the volume of space containing the Sun-Earth system, and
% 3) for resolving the entire space covered by the mesh.
%
mesh = ParticleMesh(mesh_extent*ones(3,1));
mesh.addCenteredEdgePoints(mesh_extent, 20, @mesh.spaceCube);
mesh.removeCenteredEdgePoints(1.5*SUN_EARTH);
mesh.addCenteredEdgePoints(1.5*SUN_EARTH, 25, @mesh.spaceCube);
mesh.removeCenteredEdgePoints(2.0*SUN_R);
mesh.addCenteredEdgePoints(2.0*SUN_R, 20, @mesh.spaceLinear);
mesh.buildMesh;
```

The planet Sedna is considered to be at the limit of the Solar System [122], which is why we use twice the Sun-Sedna distance to define the extent of the mesh. The latter needs to be large so that we can approximate the cosmic fabric strain as vanishing at the edge of the mesh, which is our assumed boundary condition.

The following code snippet introduces the Sun as a spherical density into the mesh:

```matlab
SUN_MASS    = 1.989e+30;            % Solar mass [kg]
SUN_R       = 6.95508e+8;           % Solar radius [m]
SUN_VOL     = (4/3)*pi*SUN_R^3;     % Solar volume [m^3]
SUN_RHO     = SUN_MASS/SUN_VOL;     % Solar density [kg/m^3]

% Specify the Sun's density's profile as a step function:
r = linspace(0, 1.5*SUN_R);
rho_sun = zeros(size(r));
rho_sun(r <= SUN_R) = SUN_RHO;
mesh.addDensitySphere(r, rho_sun);
```

![Mesh used for simulating the Sun's gravity plotted at different length scales.](https://figures.tgtenev.com/tenev2018-dissertation/fig-mesh.svg)

**Figure 7.2.** The mesh used for simulating the Sun's gravity is shown here in perspective (a), and as planar views in decreasing length scales as follows: the complete region covered by the mesh (b), the region that includes the Sun-Earth system (c) and the region that includes the Sun's globe (d). The mesh nodes are represented as dots. Notice that at the two higher length scales, the spacing between nodes increases away from the center, which was the effect of specifying cubic distribution of edge nodes as part of the mesh configuration.

Figure 7.3 shows the result from solving the Poisson equation for the mesh constructed above. Since the Sun's gravity is weak (see the *Assumptions and Limitations* section of Chapter I), its gravitational acceleration follows the classical Newtonian Gravity Law according to which:

$$
\begin{split}
a =
\begin{cases}
-\frac{4}{3}\pi G \rho_\odot r, & r \le r_\odot \\
-G M_\odot r^{-2}, & r > r_\odot
\end{cases}
\end{split}
\tag{7.27}
$$

where $r$ represents the distance from the Sun's center, and $M_\odot$, $\rho_\odot$, and $r_\odot$ are its mass, mass density, and radius, respectively. Figure 7.3 (right) shows a comparison between the theoretical acceleration and that which has been simulated. The discrepancy between theory and simulation is very small both in the vicinity of the Sun as well as at distances comparable to the Sun-Earth distance.

![Fabric strain and acceleration due to the Sun.](https://figures.tgtenev.com/tenev2018-dissertation/fig-sun.svg)

**Figure 7.3.** Panel (a) shows the variation of density $\rho$ and the fabric's volumetric strain in the vicinity of the Sun. Panels (b) and (c) compare the theoretical value for the gravitational acceleration due to the Sun with the simulated value that was output from simulating the Sun's gravity. The comparison is shown within two radial ranges: in the vicinity of the Sun (b), and in the vicinity of the Earth (c). The mesh used in this experiment had $58\times 58\times 58 = 195,112$ nodes.

#### Modeling the Effect of Inherent Curvature on the Gravity of Messier 33

We now apply the framework to investigating the Inherent Structure Hypothesis (see Chapter VI) as a possible explanation for the Dark Matter Effect. We do so by considering the rotational velocity curve (or "rotation curve" for short) of a given galaxy for the cases of with- and without inherent curvature. For the following experiment, we chose the Triangulum galaxy, also known as Messier 33 (M33), because it is a relatively well studied subject for the Dark Matter effect [35, 36, 37, 147], which effect is inferred from the rotation curve of the galaxy. For example, Figure 5 in Corbelli [35] shows the rotation curve of M33 decomposed into contributions due to the stellar disk, galactic gases, and the hypothetical dark matter. It is clear from this and similar other figures in the literature that based on the contributions from ordinary matter alone (stars and gases), rotational velocities are expected to begin to decline after some distance from the center. By contrast, measurements show that rotational velocities tend to increase monotonically with their distance from the galactic center. Such a discrepancy is commonly attributed to the presence of dark matter.

About two thirds of the ordinary (visible) matter of M33 resides in the stellar disk, while the remaining third is in the form of molecular and atomic Hydrogen. For the experiment herein, we used the total surface density data reported in Figure 10 of Corbelli et al. [37], which we have plotted at the bottom panels of Figure 7.4. Because most galaxies are thin disks, as is the case with M33, it is customary to report their matter density as surface density in units of solar masses per square parsecs ($M_\odot/\text{pc}^{2}$). For the purposes of the numerical simulation, however, we need volume density. Therefore, following Ciardullo et al. [32] we have assumed a constant galactic half-thickness of $z_{*} = 175\ \text{pc}$. As Saburova and Zasov [147] point out, such constant thickness is an idealization, but for the purposes of our comparison we assume that the effects of varying transverse thickness are insignificant.

As discussed in Chapter VI, we specify the inherent curvature via a function $w = w(x^i)$ that maps a point $x^i$ onto a transverse offset $w$ along the fourth hyperspatial dimension. For our experiment we run the same mesh once with two different functions $w(x^i)$, which are constructed according to the following code snippet:

```matlab
function wfun = makewfunFlat()
    wfun = @(x) ParticleMesh.wfunFlat(x);
end

function wfun = makewfunMOND(mass)
    wfun = @(x) ParticleMesh.wfunMOND(x, mass);
end

function w = wfunMOND(x, mass)
    % function w = wfunMOND(x)
    %       Assigns spherically symmetric transverse offset that
    %       produces Dark Matter effect consistent with the Modified
    %       Newtonian Dynamics (MOND) theory. The 'mass' parameter,
    %       which is comparable to the mass of a galaxy, determines
    %       the strength of the effect. Larger values correspond to
    %       weaker effect.
    r = sqrt(x{1}.^2 + x{2}.^2 + x{3}.^2);
    s = sqrt(SIConst.G*mass/SIConst.a_MOND);
    AA = (r./s).^2 + 1;
    BB = 4*(r./s).^2 + 3;
    w = (s/2)*sqrt(AA.*BB) - (s/4)*log(2*sqrt(AA) + sqrt(BB));
end

function w = wfunFlat(x)
    % function w = wfunFlat(x)
    %       Assigns 0 transverse offset to all points.
    if isnumeric(x)
    w = zeros(size(x));
    else
    w = zeros(size(x{1}));
    end
end
```

The function `wfunMOND` implements the MOND-equivalent profile from Equation (6.33) and Equation (6.34), where the `mass` parameter is one and the same as $M$ in Equation (6.33) and determines the length scale factor $s$. For our experiment, we discovered that setting this parameter to 100 billion solar masses (about 10 times the mass of M33) resulted in the best fit of the observational data. We conducted the experiment using spherically symmetric inherent curvature. Note, however, that the overall configuration was not spherically symmetric, because the general shape of M33 is a disk and not a ball.

Since this experiment involves inherent curvature, we need to be careful to distinguish between coordinate distances versus proper distances and be clear about when to use which. For example, all comparisons of the results obtained with and without inherent curvature are done in terms of proper distances, and so figures are labeled in terms of proper distances. At the same time, the code uses coordinate distances for internal computations. Conversion between the proper and coordinate distances was done by interpolation from a lookup table that was constructed from numerically integrating $(1 + w')$.

The region of space that we consider of interest is a cube with a half-side of $20\ \text{kpc}$. Its size was chosen to be somewhat larger than the visible disk of M33. The total mesh extent is 100 times larger than the region of interest, which allowed us to treat the fabric's volumetric strain at the edge of the mesh as approximately vanishing. We initialized a $50 \times 50 \times 50$ node mesh, where nodes were distributed per the following code:

```matlab
mesh_extent = 100*m33_extent;

mesh = ParticleMesh(mesh_extent*ones(3,1));
mesh.addEdgePoints(mesh.xlim, [25, 25, 43], @mesh.spaceCube);

xlim = [[-m33_extent, -m33_extent, -2*m33_z]; ...
             [m33_extent, m33_extent, 2*m33_z]];
mesh.removeEdgePoints(xlim);
mesh.addEdgePoints(xlim, [30, 30, 10], @mesh.spaceQuad);
```

where `@mesh.spaceCube` and `@mesh.spaceLinear` specify the manner of distributing the points along each edge. A linear distribution spaces the nodes evenly, but a cubic distribution concentrates more nodes near the center and less near the ends of the specified range. The M33 object was introduced into the mesh as a cylindrical density of uniform half-thickness $z_{*} = 175\ \text{pc}$.

Figure 7.4 and Figure 7.5 show the results of the computation in terms of the cosmic fabric strain and the galaxy rotation curve, respectively. The rotational velocities $v$ plotted in Figure 7.5 were calculated using the formula,

$$
\begin{split}
\frac{v^2}{r} = a^1_\text{proper} = \frac{a^1}{\sqrt{g_{11}}}, \quad a^1 = c^2\overline{g}^{1i}\partial_i \varepsilon
\end{split}
\tag{7.28}
$$

where $a^1_\text{proper}$ is the proper radial acceleration and $a^1$ is the coordinate radial acceleration that were measured in the $x^1$ direction. The last equality is an approximation of Equation (7.20), in which the velocity terms are treated as insignificant on the assumption that rotation velocities are much less than the speed of light, which is the case here.

![Fabric strain due to the M33 galaxy.](https://figures.tgtenev.com/tenev2018-dissertation/fig-m33-strain.svg)

**Figure 7.4.** Fabric strain due to the M33 galaxy without (a) and with (b) inherent curvature. The top panels visualize a quadrant of the strain field, while the bottom panels show the density and strain profiles. The density profile used here is from Figure 10 of Corbelli et al. [37].

![Rotation curve of the M33 galaxy.](https://figures.tgtenev.com/tenev2018-dissertation/fig-rot-v.svg)

**Figure 7.5.** The top panel shows M33's observed rotation curve [35] along those computed with and without inherent curvature. The inherent curvature was specified by a radially symmetric hyperspatial displacement $w = w(x^i)$ (bottom panel) that produces MOND-equivalent effect per Equation (6.33). The displayed fit was achieved with a scale mass of $M = 10^{11} M_\odot$, which is about $10\times$ the mass of M33. The bottom panel also shows $\sqrt{g_{11}}$ which represents the ratio between the proper distance element $dl$ and the coordinate element $dx^1$.

These results illustrate that for an appropriately chosen inherent curvature, the simulated velocity curve fits well with the data. The fit is quite good although there was only one parameter to adjust for choosing the inherent curvature (the scale mass $M$). In principle, the inherent curvature is free to have any shape provided it is geometrically consistent (no kinks, intersects or tears), so an even better fit could be achieved when a more detailed relief is chosen for the inherent spatial structure.

### Discussion

The following factors are important in the design of the numerical framework and experiments: trade-off between reducing numerical errors versus reducing computational costs; avoiding numerical instability, and ensuring convergence. Below we discuss how each of these factors has been addressed.

Achieving optimal trade-off between reduction of numerical errors and computational cost relies on understanding the sources of errors. For example, one such source is imprecision of the input data. It would be computationally wasteful to try to achieve numerical precision that is higher than the input precision. Another source of error is the defeaturing (idealization) of modeled entities. Reducing this error involves using more grid nodes at the location of the entity whose feature we want to express. For example, the accurate modeling of the Sun as part of the validation experiment in the *Numerical Experiments* section required that more mesh nodes were introduced in its vicinity compared to the rest of the grid. The discretization of derivatives per Equations (7.7) and (7.8) introduces numerical errors by omitting higher order terms that depend on the grid spacing. Notably, for the discretization of the second derivative, the error is linear in terms of the difference between adjacent grid spacing values. So, one must be careful not to vary the grid spacing too suddenly. Finally, numerical errors are also introduced during the post processing stage when the output from the solver is often interpolated to extract meaningful outcome.

Numerical instability is a unique source of errors, which is manifested when a small perturbation in the input leads to dramatic changes in the output. We have found such instability to arise, for example, when the $Q$ matrix that is constructed in the solution of the Poisson Equation is poorly scaled. This can happen if the numerical values of the boundary coefficients, which are set to unity per Equation (7.25), differ by many orders of magnitude from the coefficients in the $L$ matrix. To avoid this problem, we first scale all interior node coefficients $Q_{mn}$ by some fixed scale factor before setting the boundary node coefficients to unity, and then apply this scale factor to the outcome from solving the Poisson equation. Pathological choice for the location of grid nodes can be another cause of numerical instability, such as placing them close to a location at which the node values would be singular or nearly so.

Ensuring convergence means achieving grid fidelity beyond which adding more nodes does not qualitatively change the result of the computation, but only incrementally increases its precision. Without ensuring convergence, the meaningfulness of the numerical results is questionable. To check convergence for a given number of mesh nodes, we rerun the same calculation with fewer number of nodes and note whether the result changes qualitatively. If the precision of the result is only incrementally decreased, then we assume to have achieved convergence.

Understanding the physics of the modeled variables also helps achieve optimal trade-off between reducing error and computational cost. For example, the error in Equations (7.7) and (7.8) depends on the third derivative of the differentiated quantity, which happens to be the volumetric strain $\varepsilon$ in the case of solving the Poisson Equation. Since $\varepsilon$ diminishes approximately as the inverse distance to the center of the gravitating system, therefore the error will be diminishing as the inverse cube of the distance from the center of the system. This enabled us to use cubic distribution for the edge nodes, whereby node spacing increases proportional to the square of the distance to the center.

For the category of numerical experiments where time is involved, the choice of the time step must also be considered. We use an explicit method for computing the time evolution of the system, which means that the future configuration is computed from the current one. For this type of computation, the Courant–Friedrichs–Lewy (CFL) condition [136] limits the size of the time step $\Delta t$, such that $\Delta t \le h/c$, where $h$ is the characteristic grid spacing and $c$ is the speed of signal propagation, which in our case is the speed of light. An implication of the CFL condition is that whenever the grid is refined by reducing $h$, the time step $\Delta t$ must also be reduced to ensure that the simulation remains convergent. Such coupling between the spatial spacing and the time step results in higher computational cost.

### Summary and Conclusion

We presented a working numerical framework for investigating the dynamics of gravitational systems in the regime of weak gravity. The framework is suited to studying the Dark Matter effect in the context of the Inherent Structure Hypothesis discussed in Chapter VI. It uses the Finite Differences Method to solve the Covariant Poisson equation, which lets it account for the effects of inherent spatial curvature.

The proper functioning of the framework was validated by modeling the gravity of the Sun and comparing the result to the prediction of Newtonian gravity. The result was within 16% of the theoretical prediction for a relatively coarse mesh of $60\times 60\times 60$ nodes. More accurate results can be achieved in the future at the expense of more computational power (both CPU and memory).

The framework was applied to studying the effect of inherent curvature on the gravity of stellar object Messier 33 (M33), which is also known as the Triangulum Galaxy. The results, which are visualized in Figure 7.4 and Figure 7.5, demonstrated that the presence of inherent curvature does in fact cause the galaxy rotation velocities to monotonically increase with distance from the center in a manner similar to the effect of a hypothetical dark matter halo. Furthermore, for an appropriately chosen inherent curvature, the simulated rotation curve fitted well the observational data. This result validates the ideas presented in Chapter VI.

The primary goal of the work presented in this chapter was the development of the numerical framework, while conducting numerical experiments based on it was a secondary goal. Although the experimental results were promising, future work is needed for a thorough assessment of their significance and for better quantification of the error by accounting for uncertainties in the input data. The framework should be extended to allow for more flexible specification of the boundary conditions, and a greater variety of galactic shapes and inherent curvatures should be investigated.

---

## VIII. Conclusions

In this dissertation work, we explored the analogy between physical space and a material solid to understand how the structure of space itself affects the behavior and structure of matter within it. Fundamental to the ideas presented here was the proposition that the universe as a whole is a functional system and as such, it exhibits complexity and structure at multiple length scales. Furthermore, physical space, being a component of said system, must also exhibit structure at multiple length scales, whose effects can be measured and numerically simulated as it is done with components of ordinary mechanical systems.

Our approach was to first establish the theoretical basis for the material analogy of physical space, which we called the *Cosmic Fabric Model*. Next, we used this model to propose and numerically substantiate a solution to an outstanding problem in cosmology, namely, the explanation of galactic-scale gravitational anomalies. We referred to these as "Dark Matter effect" since they are currently attributed to the presence of invisible mass. We proposed the *Inherent Structure Hypothesis* as an alternative explanation for the Dark Matter effect. In support of this hypothesis, we first showed analytically that inherent spatial curvature can emulate the effects of dark matter distribution by amplifying the gravity of ordinary masses. Our analytical solution was limited to spherically symmetric configurations. To overcome this limitation, we built a numerical framework, which can test the Inherent Structure Hypothesis under a wide variety of configurations including asymmetric ones. Using this framework we performed several numerical experiments demonstrating that inherent spatial curvature does indeed extend the gravitational influence of ordinary matter and is able to produce the type of galactic rotation curves that had been traditionally used as indicators of dark matter.

Below we recount in greater detail the list of takeaway points:

1. **Physical space is material-like.** The behavior of physical space is like that of an elastic material subject to Hooke's Law. It can be modeled as the mid-hypersurface of a four-dimensional (4D) hyperplate that deforms within 4D hyperspace. We called this hyperplate "cosmic fabric." The enclosing 4D hyperspace, which we called "reference space," is not directly observable at continuum length scales (see Chapter III).
2. **Matter acts as inclusions.** Matter acts as inclusions inducing prescribed strain that causes the fabric to bend. The induced volumetric strain $\varepsilon$ relates to the matter-energy density $\rho$ of the inclusion per: $\nabla^2 \varepsilon = -c^2\kappa \rho /2$, where $\kappa$ is the Einstein constant and $c$ is the speed of light. In the presence of inherent curvature, the Laplace operator $\nabla^2$ should be replaced by the more general covariant Laplacian $\nabla_i (\nabla^i)$ (see Chapter III and Chapter V).
3. **Medium for matter–matter interactions.** The cosmic fabric mediates matter–matter interactions by signals propagating through it. These are mechanical-like disturbances within the fabric whose speed, measured with respect to the reference space, depends on the fabric's mechanical properties and state (see Chapter III).
4. **Time lapse rate depends on the signal speed.** The rate of clock ticks within the fabric depends on the rate of interaction amongst the clocks' internal components, which in turn depends on the speed of signal propagation. The observed rate of clock ticks is inversely proportional to the volumetric stretch $\varepsilon$. Because clock rates specify the time components of the spacetime metric tensor $g_{\mu\nu}$ and clock rates themselves depend on the deformation state of the fabric, it follows that $g_{\mu\nu}$ is fully specified by the mechanical state of the fabric (see Chapter III).
5. **Action equivalence.** The action integral of the cosmic fabric computed from energy considerations based on Hooke's Law is equivalent to the Einstein–Hilbert action of spacetime (see Chapter III).
6. **Gravity equations are analogous to plate bending equations.** The Einstein Field Equations of gravity are analogous to the plate bending equations from thin plate theory with Einstein's constant being analogous to the stiffness constant. The fabric's thickness is needed to offer resistance to bending (see Chapter III).
7. **Signal speed appears invariant to all observers within the fabric and is $c$.** Because signal speed affects clock rates within the fabric, the measurement of such speed within the fabric appears one and the same irrespective of the observer's reference frame. This observed signal speed is identified with the speed of light in vacuum (see Chapter IV).
8. **Lorentz Transformations apply.** Coordinate transformations of events within the fabric conform to Lorentz Transformations (see Chapter IV).
9. **Relativity applies.** Although the fabric ostensibly defines a special rest reference frame, such reference frame is undetectable from within the fabric based on just local observations at the continuum length scale. This undetectability of the special rest reference frame is also the explanation for the negative outcome of the Michelson and Morley experiment (see Chapter IV).
10. **Generalization of Lorentz Aether Theory.** At the continuum length scale, the Cosmic Fabric model of gravity generalizes Lorentz Aether Theory similarly to how General Relativity does Special Relativity.
11. **Physically meaningful coordinate assignment.** For an appropriate choice of coordinates, which was the type of coordinate choice used throughout this dissertation work, the $h_{\mu\nu}$ quantities from Linearized Gravity have the meaning of twice the strain components, that is $2\varepsilon_{\mu\nu}$, which, being strain, has concrete physical meaning. By contrast, most applications of Linearized Gravity choose a type of coordinate assignments that make mathematical expressions involving $h_{\mu\nu}$ simple at the expense of obfuscating the direct physical meaning of these quantities (see Chapter III).
12. **Gravitational potential corresponds to volumetric strain.** Under the weak gravity regime, the classical gravitational potential $\Phi$ relates to the volumetric strain $\varepsilon$ per $\Phi/c^2 = -\varepsilon$ (see Chapter III).
13. **Poisson ratio is unity.** The Poisson ratio of the cosmic fabric is $\nu=1$. Such Poisson ratio implies that cosmic space has non-trivial weave-like substructure (see Chapter III and Chapter V).
14. **No pressure waves.** Because Poisson's ratio is unity, the pressure wave modulus vanishes. Consequently, we expect that no pressure (longitudinal) waves can propagate in the fabric but only shear waves. This conclusion agrees with observations since waves propagating in vacuum, such as gravity and electromagnetic radiation, all oscillate in directions perpendicular to the direction of propagation. The fact that there can be no pressure waves in space is also consistent with Birkhoff's theorem, which states in part that all spherically symmetric solutions of Einstein's Field Equations must be static (see Chapter III).
15. **Gravity waves as shear waves in the fabric.** Gravity waves are analogous to transverse waves in the fabric and exhibit the same number of polarizations (just two). The latter conclusion can be derived from solid mechanics reasoning (see Chapter III).
16. **Materialization of Flamm's Paraboloid.** Gravity of a stationary spherically symmetric body can be understood in terms of the cosmic fabric bending into the shape of Flamm's Paraboloid (see Chapter V).
17. **Natural reparametrization of the Schwarzschild solution.** A reparametrized version of the Schwarzschild metric can be derived for a static spherically symmetric body from purely solid mechanics principles. It is equivalent with the Schwarzschild metric up to coordinate re-scaling. Such rescaling does not affect General Relativity's use of the metric because of coordinate assignment freedoms. However, from a solid mechanics' perspective, the particular choice of coordinates attributes additional physical meaning to the resulting metric, namely, that of describing the deformation of the fabric. Specifically, the metric derived from solid mechanics' considerations shows that the fractional amount by which space is stretched volumetrically always equals the fractional amount by which time lapse rate decreases (see Chapter V).
18. **Discrete substructure of matter.** Investigating the fabric's membrane energy as due to matter-fabric interaction led to the conclusion that matter cannot exist in large continuous chunks but must be made up of small discrete particles. This conclusion is consistent with our understanding of matter that comes from outside the field of General Relativity (GR). Reaching such a conclusion illustrated the cross-length scale aspect of the Cosmic Fabric model. In this particular case, the thickness of the fabric, which is on the order of Planck's length, functioned as a length-scale parameter (see Chapter V).
19. **Length-scale effects.** The cosmic fabric model generalizes GR by naturally introducing additional length scale parameters, such as the fabric's thickness, at the minutest scale, and its inherent curvature at the galactic length scale and above. The former may be giving rise to quantum effects, while the latter, as we showed in Chapter VI, is likely the cause of the Dark Matter effect. Only at the continuum length scale is the Cosmic Fabric model equivalent to GR, because GR is strictly a continuum scale theory (see Chapter IV, Chapter V, and Chapter VI).
20. **Inherent structure of space causes the "dark matter" effect.** The presence of inherent curvature of space (one that is uncaused by matter) amplifies the gravity of ordinary bodies and could manifest as the gravitational anomalies currently attributed to dark matter (see Chapter VI).
21. **A computational framework was introduced** that is suitable for weak gravity simulations in the presence of inherent curvature. We built a numerical framework by enhancing the Particle Mesh method to take into consideration non-flat geometry of space. Using this framework and galactic density data found in the literature, we computed the rotation curve of the Triangulum galaxy (also known as M33) and showed that the presence of inherent spatial curvature did result in a rotation curve consistent with the Dark Matter effect.

---

## IX. Future Research

A goal of the work presented in earlier chapters was to open the door for the flow of ideas and techniques between the fields of solid mechanics and General Relativity (GR), and between mechanical engineering and Cosmology. As such, we hope that it would spur new types of scientific research and the development of new types of technologies. Even the work that has been done so far as a foretaste also leaves many areas incomplete which, due to time and resource constraints, were left to be continued when more hands and minds can join in. Below we enumerate a sample list of potential future projects, which we have categorized as: 1) further development of the cosmic fabric model, 2) further research into the inherent structure hypothesis, 3) additional categories of computational simulations, and 4) implications to cosmology and fundamental physics.

### Further Development of the Cosmic Fabric Model

We began introducing the Cosmic Fabric model in Chapter III subject to certain limitations, some of which were eliminated and relaxed in Chapter IV and Chapter V, but some have remained.

The future work needed to overcome the remaining limitations of the model includes completing the analogy with General Relativity for the cases of strong gravity (large strains) and rapidly changing gravitational fields (high strain rates). The weak gravity (small strain) condition was imposed so we could use the linearized equations for gravity and, analogously, for strain. To relax this condition, we will need to account for the higher order terms in the equations of strain and also use covariant derivatives instead of ordinary differentiation for all field variables. Imposing the nearly static field condition allowed us to ignore the kinetic energy term in the fabric's Lagrangian. Without the condition of nearly static fields, we will need to take into account the kinetic and membrane energies of the fabric and also consider a more complex deformation state. An incremental improvement would be to consider the condition of high strain rates (fast changing fields) but without static deformation (away from static gravitational fields), and derive a closed-form result for the fabric's Lagrangian. This is the condition under which we would study gravitational waves.

It would be fruitful to explore new hypotheses, which are not readily seen under the GR paradigm, but are naturally made apparent under the solid mechanics paradigm. One such is the Inherent Structure Hypothesis, which was proposed in Chapter VI. If space is a material body, as proposed herein, it is natural to suppose that it should have inherent structure, but within the GR paradigm, such notion would manifest as modifications to the GR equations and so it is not as apparent under that paradigm. Other such solid mechanics notions that can be explored in the future include: dissipation, damage, and internal state variables (ISV) in general. Another example is fitting the Rose equation of state [143] as a means of probing the substructure of the fabric. The Rose equation relates the total bending energy to the node separation within a lattice.

In fact, many novel hypotheses can be formulated based on the notion that space has substructure as well as large-scale structure. It would be desirable to provide a general theoretical framework for working with the multi-scale structure of space. Such framework could be based on a Lagrangian formulation similar to what was sketched in Figure 1.1. The framework should also provide a way for translating solutions developed within the mechanical paradigm to the General Relativity paradigm.

The method for calculating the cosmic fabric's metric that was introduced in Chapter V can be readily generalized to non-flat initial geometry and asymmetric configuration. In such a case, the governing equations reasoned in the *Formulation of the Governing Equations* section of Chapter V do not necessarily have closed form solutions but must be solved numerically. If the initial geometry of the fabric and its inclusion are spherically symmetric, then the method still reduces to a single first order ordinary differential equation, which is straightforward to solve using well known numerical techniques. If the configuration is not spherically symmetric, however, it may still be possible to approximate it with linear superposition of a finite number of spherically symmetric sub-configurations. These can be solved individually, and their solutions superimposed. Such a decomposition into spherically symmetric configurations and the subsequent linear superposition is valid in the regime of small strains (weak gravity).

Another potentially straightforward generalization of our method is for the spherically symmetric case of large strains (strong gravity). The majority of the steps used in earlier sections that derive the various kinematic and energy quantities of the fabric are also applicable for the case of large strains. Calculating the metric tensor, extrinsic, and intrinsic curvature are such examples. The small strain assumption is mainly a convenience to avoid complicated radicals in the closed form solution, but that is not an issue when using numerical techniques.

### Further Research into the Inherent Structure Hypothesis

With the help of numerical simulations, the work presented in Chapter VI can be used to interpret existing observations of the Dark Matter effect to create a map of the inherent structure of cosmic space much like echo sonars can create a relief map of the ocean floor. If the resulting "relief" map reveals an inherent cosmic structure that is geometrically consistent, then such discovery will add more credence to the Inherent Structure Hypothesis.

Another area for future work is devising experiments that can distinguish between the Inherent Structure Hypothesis (ISH) and other models that attempt to explain the Dark Matter effect. As discussed in Chapter VI, such experiments would involve, for example, measuring anomalous gravity in regions far outside the edges of galaxies in an effort to detect whether the assumed inherent curvature begins to attenuate (see the dashed line in Figure 6.3).

### Additional Categories of Computational Simulations

There are at least three broad categories of numerical experiments that can be based on the cosmic fabric model: large strain experiments, high-strain rate, and small strain dynamics. The numerical framework discussed in Chapter VII only addresses the latter category, while the first two are left for future work. Below we describe each of them in detail.

Large strain (strong gravity) experiments pertain to situations that involve black holes or neutron stars. The Finite Element Method (FEM) appears to be the most appropriate technique for this situation because of the large strains involved. Unlike the type of mesh we used in Chapter VII, which was a fixed mesh, the nodes of the FEM mesh will need to be capable of displacing in four dimensions (4D). Existing FEM methods used for the modeling of ordinary materials will have to be generalized to 4D. These methods could use either 4D volume elements or shell elements since the fabric is thin in the fourth dimension. One challenge against developing an FEM simulation of the cosmic fabric is its unusual Poisson ratio of unity, since that implies a negative bulk modulus, which means that only anisotropic strains are admitted below a certain length scale. Perhaps, this issue can be solved by predefining a pattern for the anisotropy (a kind of texture) that the solver can reckon as underlying each isotropic strain quantity above some length scale.

High-strain rate (rapidly changing gravity) simulations are relevant for the study of gravitational waves. An FDM scheme formulated as an Initial Value Problem (IVP) is likely the best technique for this case. Depending on the situation, either an explicit or implicit solver can be used. The latter yields greater precision and is not limited by the Courant–Friedrichs–Lewy condition [136], which was discussed in Chapter VII, but poses higher computational requirements.

In addition to developing the new categories of simulations described above, some future enhancements of the framework presented in Chapter VII are also in order. These include: more flexible handling of boundary conditions, and propagating uncertainties from the inputs to the results.

### Implications to Cosmology and Fundamental Physics

Below are some questions to consider in the context of future research:

If space is a kind of material through which gravity waves propagate at the speed of light, could the same material also carry electromagnetic radiation? Could this be the key to the unification of the fundamental forces of gravity and electromagnetism? John Baumgardner had suggested in a private conversation that one could model electromagnetic fields in vacuum as due to the displacement of charges within the cosmic fabric. As discussed in Chapter III the fabric's substructure may be fibrous. Could there be multiple types of fibers such that some differ from the others according to their electric charge? While the fabric remains undisturbed, the charges cancel each other and the overall state is neutral, but certain types of fabric disturbances cause the charges to separate temporarily thereby creating a field of charged dipoles, which is perceived as an electromagnetic field. If this hypothesis is correct, it would not only lead to the unification of gravity and electromagnetism, but could also provide a way to manipulate the curvature of space, and hence gravity, through the coupling between electromagnetism and the cosmic fabric.

Could the Inherent Structure Hypothesis applied at the length scale of the visible universe explain the observations currently attributed to dark energy? Presently, dark energy is invoked to explain the departure from linearity in the Hubble relation (the relation between the redshift of distant astronomical objects and their distances from Earth). One interpretation of this observation is that the universe expanded slower in the past than it does today, so its expansion must be accelerating. Dark energy, which is postulated to have anti-gravity properties, is invoked to explain the inferred acceleration of the expansion. An alternative possibility is that the observed redshift is caused, at least in part, by cosmic-scale gravitational anomalies, which in turn may be the manifestation of cosmic-scale spatial structures.

In general, what would a cosmological model look like that is based on the presupposition of structure at each length scale including the scale of the visible universe? By contrast, the current Standard Cosmological Model is fundamentally dependent on the Cosmological Principle, which is the presupposition that at length scales greater than 100 Mpc, the universe lacks any structure and is approximately homogeneous and isotropic. Yet, the Cosmological Principle is an unprovable assumption that may be falsified in the future as a result of new observations. Indeed, every functional system we can observe exhibits structure at its greatest length scale, so why should the largest such system known to man be an exception? The material model of space could be the basis for a cosmological model that appropriately accommodates structure at all length scales and is not vulnerable to the eventual repudiation of the Cosmological Principle.


---

## References

1. B. P. Abbott, "GW170817: Observation of Gravitational Waves from a Binary Neutron Star Inspiral", 2017. doi: 10.1103/PhysRevLett.119.161101.
2. S. Abrahamyan et al., "Measurement of the Neutron Radius of 208Pb Through Parity-Violation in Electron Scattering", *Physical Review Letters*, vol. 108, no. 11, p. 112502, 2012. doi: 10.1103/PhysRevLett.108.112502.
3. A. E. H. Love, "The Small Free Vibrations and Deformation of a Thin Elastic Shell on JSTOR", *Philosophical Transactions of the Royal Society of London. A*, vol. 179, pp. 491–546, 1888.
4. N. Aghanim et al., "Planck 2013 results. XXVII. Doppler boosting of the CMB: Eppur si muove", *Astronomy & Astrophysics*, vol. 571, p. A27, 2014. doi: 10.1051/0004-6361/201321556.
5. A.-L. Cauchy, "De la pression ou tension dans un corps solide, [On the pressure or tension in a solid body]", *Exercices de Mathématiques*, vol. 2, p. 42, 1827.
6. M. Alcubierre, "Hyperbolic slicings of spacetime: singularity avoidance and gauge shocks", *Classical and Quantum Gravity*, vol. 20, no. 4, pp. 607–623, 2003. doi: 10.1088/0264-9381/20/4/304.
7. M. Alcubierre, "Simple excision of a black hole in 3 + 1 numerical relativity", *Physical Review D*, vol. 63, no. 10, p. 104006, 2001. doi: 10.1103/PhysRevD.63.104006.
8. M. Alcubierre et al., "Gauge conditions for long-term numerical black hole evolutions without excision", *Physical Review D*, vol. 67, no. 8, p. 084023, 2003. doi: 10.1103/PhysRevD.67.084023.
9. P. G. Allison, M. F. Horstemeyer, H. R. Brown, "Modulus dependence on large scale porosity of powder metallurgy steel", *Journal of Materials Engineering and Performance*, vol. 21, no. 7, pp. 1422–1425, 2012. doi: 10.1007/s11665-011-0001-6.
10. P. Amram, C. Boulesteix, J. Balkowski, "The H$\alpha$ kinematic of the Cartwheel galaxy", *Astronomy and Astrophysics*, vol. 330, pp. 881–893, 1998.
11. P. Anninos, J. Seidel, E. Suen, W. M. Towns, J. Towns, "Three-dimensional numerical relativity: The evolution of black holes", *Physical Review D*, vol. 52, no. 4, pp. 2059–2082, 1995. doi: 10.1103/PhysRevD.52.2059.
12. S. Antoci, L. Mihich, "A four-dimensional Hooke's law can encompass linear elasticity and inertia", *Nuovo Cimento B*, p. 8, 1999.
13. R. Arnowitt, S. Deser, C. W. Misner, "Dynamical Structure and Definition of Energy in General Relativity", *Physical Review*, vol. 116, no. 5, pp. 1322–1330, 1959. doi: 10.1103/PhysRev.116.1322.
14. R. Arnowitt, S. Deser, C. W. Misner, "The Dynamics of General Relativity", *General Relativity and Gravitation*, vol. 40, no. 9, pp. 1997–2027, 2004. doi: 10.1007/s10714-008-0661-1.
15. H. Babcock, "The rotation of the Andromeda Nebula", *Lick Observatory Bulletin*, 1939.
16. J. G. Baker, J. Centrella, D. I. Choi, M. Koppitz, J. Meter, "Gravitational-Wave Extraction from an Inspiraling Configuration of Merging Black Holes", *Physical Review Letters*, vol. 96, no. 11, p. 111102, 2006. doi: 10.1103/PhysRevLett.96.111102.
17. A. J. Barth, "A Normal Stellar Disk in the Galaxy Malin 1", *The Astronomical Journal*, vol. 133, no. 3, pp. 1085–1091, 2007. doi: 10.1086/511180.
18. R. H. Baughman, A. F. Fonseca, "Architectured materials: Straining to expand entanglements.", *Nature materials*, vol. 15, no. 1, pp. 7–8, 2016. doi: 10.1038/nmat4436.
19. J. R. Baumgardner, "Three-dimensional finite element model for mantle convection.", *Dissertation Abstracts International Part B: Science and Engineering[DISS. ABST. INT. PT. B- SCI. & ENG.],*, vol. 45, no. 1, 1984.
20. M. Beau, "Théorie des champs des contraintes et déformations en relativité générale et expansion cosmologique: Theory of stress and strain fields in general relativity and cosmological expansion", *Annales de la Fondation Louis de Broglie*, vol. 40, 2015.
21. J. Bekenstein, M. Milgrom, "Does the missing mass problem signal the breakdown of Newtonian gravity?", *Astrophysical Journal*, vol. 286, p. 7, 1984. doi: 10.1086/162570.
22. J. D. Bekenstein, "Relativistic gravitation theory for the modified Newtonian dynamics paradigm", *Physical Review D*, vol. 70, no. 8, p. 083509, 2004. doi: 10.1103/PhysRevD.70.083509.
23. E. Bertschinger, "SIMULATIONS OF STRUCTURE FORMATION IN THE UNIVERSE", *Annual Review of Astronomy and Astrophysics*, vol. 36, no. 1, pp. 599–654, 1998. doi: 10.1146/annurev.astro.36.1.599.
24. C. Bohmer, T. Harko, F. Lobo, "Dark matter as a geometric effect in f(R)f(R) gravity", *Astroparticle Physics*, vol. 29, no. 6, pp. 386–392, 2008. doi: 10.1016/j.astropartphys.2008.04.003.
25. C. G. Tamanini, N. Wright, "On galaxy rotation curves from a continuum mechanics approach to modified gravity", *International Journal of Modern Physics D*, vol. 27, no. 02, p. 1850007, 2018. doi: 10.1142/S0218271818500074.
26. C. Bona, J. Seidel, E. Stela, "New Formalism for Numerical Relativity", *Physical Review Letters*, vol. 75, no. 4, pp. 600–603, 1995. doi: 10.1103/PhysRevLett.75.600.
27. S. Boran, S. Desai, E. O. Kahya, R. P. Woodard, "GW170817 falsifies dark matter emulators", *Physical Review D*, vol. 97, no. 4, p. 041501, 2018. doi: 10.1103/PhysRevD.97.041501.
28. S. Brandt, "A Simple Construction of Initial Data for Multiple Black Holes", *Physical Review Letters*, vol. 78, no. 19, pp. 3606–3609, 1997. doi: 10.1103/PhysRevLett.78.3606.
29. B. Tichy, W. Jansen, "Numerical Simulation of Orbiting Black Holes", *Physical Review Letters*, vol. 92, no. 21, p. 211101, 2004. doi: 10.1103/PhysRevLett.92.211101.
30. M. Campanelli, C. O. Lousto, P. Marronetti, Y. Zlochower, "Accurate Evolutions of Orbiting Black-Hole Binaries without Excision", *Physical Review Letters*, vol. 96, no. 11, p. 111101, 2006. doi: 10.1103/PhysRevLett.96.111101.
31. S. C. Chapman et al., "A Kinematically Selected, Metal‐poor Stellar Halo in the Outskirts of M31", *The Astrophysical Journal*, vol. 653, no. 1, pp. 255–266, 2006. doi: 10.1086/508599.
32. R. Ciardullo et al., "The Planetary Nebula System of M33", *The Astrophysical Journal*, vol. 614, no. 1, pp. 167–185, 2004. doi: 10.1086/423414.
33. G. Comte, G. Monnet, M. Rosado, "An Optical Study of the Galaxy M 101", *Astronomy and Astorphysics*, vol. 72, pp. 73–81, 1979.
34. G. B. Cook et al., "Boosted Three-Dimensional Black-Hole Evolutions with Singularity Excision", *Physical Review Letters*, vol. 80, no. 12, pp. 2512–2516, 1998. doi: 10.1103/PhysRevLett.80.2512.
35. E. Corbelli, "Dark matter and visible baryons in M33", *Monthly Notices of the Royal Astronomical Society*, vol. 342, no. 1, pp. 199–207, 2003. doi: 10.1046/j.1365-8711.2003.06531.x.
36. E. Corbelli, P. Salucci, "The extended rotation curve and the dark matter halo of M33", *Monthly Notices of the Royal Astronomical Society*, vol. 311, no. 2, pp. 441–447, 2000. doi: 10.1046/j.1365-8711.2000.03075.x.
37. E. Corbelli, D. Thilker, S. Zibetti, C. Giovanardi, P. Salucci, "Dynamical signatures of a $\Lambda$CDM-halo and the distribution of the baryons in M 33", *Astronomy & Astrophysics*, vol. 572, p. A23, 2014. doi: 10.1051/0004-6361/201424033.
38. H. Ullrich, "Introduction To Computational PDEs Course Notes for AMATH 442 / CM 452", Department of Applied Mathematics, University of Waterloo, 2009.
39. J. G. Bertone, "How dark matter came to matter", *Nature Astronomy*, vol. 1, 2017. doi: 10.1038/s41550-017-0059.
40. B. S. Dewitt, "Quantum theory of gravity. I. the canonical theory", *Physical Review*, vol. 160, no. 5, pp. 1113–1148, 1967. doi: 10.1103/PhysRev.160.1113.
41. R. H. Dicke, "Gravitation without a Principle of Equivalence", *Reviews of Modern Physics*, vol. 29, no. 3, pp. 363–376, 1957. doi: 10.1103/RevModPhys.29.363.
42. P. A. M. Dirac, "Is there an Æther?", *Nature*, vol. 168, no. 4282, pp. 906–907, 1951. doi: 10.1038/168906a0.
43. P. Dokkum et al., "A galaxy lacking dark matter", *Nature*, vol. 555, no. 7698, pp. 629–632, 2018. doi: 10.1038/nature25767.
44. A. Z. Dolginov, "Dark Matter in Universe as the Geometry of Empty Space", 2011.
45. M. J. Duff, T. Inami, C. N. Pope, E. Sezgin, K. S. Stelle, "Semiclassical quantization of the supermembrane", *Nuclear Physics B*, vol. 297, no. 3, pp. 515–538, 1988. doi: 10.1016/0550-3213(88)90316-1.
46. E. Efrati, E. Sharon, R. Kupferman, "Elastic theory of unconstrained non-Euclidean plates", *Journal of the Mechanics and Physics of Solids*, vol. 57, no. 4, pp. 762–775, 2009. doi: 10.1016/j.jmps.2008.12.004.
47. A. Einstein, "Raum, Äther und Feld in der Physik", 1930.
48. A. Einstein, "Zur Elektrodynamik bewegter Körper", *Annalen der Physik*, vol. 322, no. 10, pp. 891–921, 1905. doi: 10.1002/andp.19053221004.
49. A. Einstein, "Aether and the Theory of Relativity", *Sidelights on Relativity*, 1922.
50. A. Einstein, "Die Grundlage der allgemeinen Relativitätstheorie", *Annalen der Physik*, vol. 354, no. 7, pp. 769–822, 1916. doi: 10.1002/andp.19163540702.
51. A. Einstein, "Ether and the Theory of Relativity", 1922.
52. A. Einstein, "Uber den Ather", *Schweizerische Naturforschende Gesellschaft Verhandlungen*, vol. 105, pp. 85–93, 1924.
53. R. T. Eufrasio et al., "Star Formation Histories Across the Interacting Galaxy NGC 6872, the Largest-known Spiral", *The Astrophysical Journal*, vol. 795, no. 1, p. 89, 2014. doi: 10.1088/0004-637X/795/1/89.
54. J. Fish, T. Belytschko, "A first course in finite elements", 2007.
55. D. R. Fiske, J. G. Baker, J. R. Meter, D. I. Choi, J. M. Centrella, "Wave zone extraction of gravitational radiation in three-dimensional numerical relativity", *Physical Review D*, vol. 71, no. 10, p. 104036, 2005. doi: 10.1103/PhysRevD.71.104036.
56. L. Flamm, "Republication of: Contributions to Einstein's theory of gravitation", *General Relativity and Gravitation*, vol. 47, no. 6, p. 72, 2015. doi: 10.1007/s10714-015-1908-2.
57. A. Fresnel, "Lettre d'Augustin Fresnel à François Arago sur l'influence du mouvement terrestre dans quelques phénomènes d'optique", *Annales de chimie et de physique*, vol. 9, pp. 57–66, 1818.
58. G. P. Michon, "Sizing up the Universe - Stars, Sand and Nucleons", 2016.
59. U. H. Gerlach, J. F. Scott, "Metric elasticity in a collapsing star: Gravitational radiation coupled to torsional motion", *Physical Review D*, vol. 34, no. 12, pp. 3638–3649, 1986. doi: 10.1103/PhysRevD.34.3638.
60. A. Y. Grama, J. Fogarty, H. Aktulga, S. Pandit, D. Padua, "N-Body Computational Methods", *Encyclopedia of Parallel Computing*, pp. 1259–1268, 2011. doi: 10.1007/978-0-387-09766-4_97.
61. D. J. Gross, J. A. Harvey, E. Martinec, R. Rohm, "Heterotic String", *Physical Review Letters*, vol. 54, no. 6, pp. 502–505, 1985. doi: 10.1103/PhysRevLett.54.502.
62. R. A. Grot, A. C. Eringen, "Relativistic continuum mechanics", *International Journal of Engineering Science*, vol. 4, no. 6, pp. 639–670, 1966. doi: 10.1016/0020-7225(66)90009-7.
63. K. Hebeler, J. M. Lattimer, C. J. Pethick, A. Schwenk, "Constraints on Neutron Star Radii Based on Chiral Effective Field Theory Interactions", *Physical Review Letters*, vol. 105, no. 16, p. 161102, 2010. doi: 10.1103/PhysRevLett.105.161102.
64. F. W. Hehl, C. Kiefer, "Comparison of the DeWitt metric in general relativity with the fourth-rank constitutive tensors in electrodynamics and in elasticity theory", *General Relativity and Gravitation*, vol. 50, no. 1, p. 8, 2018. doi: 10.1007/s10714-017-2329-1.
65. E. Holmberg, "A Study of Double and Multiple Galaxies Together with Inquiries into some General Metagalactic Problems", *Annals of the Observatory of Lund*, vol. 6, pp. 3–173, 1937.
66. R. Hooke, "Lectures de Potentia Restitutiva, Or of Spring Explaining the Power of Springing Bodies. - 1678", John Martyn, London, 1678.
67. C. Horellou, B. Koribalski, "Stars and gas in the very large interacting galaxy NGC 6872", *Astronomy & Astrophysics*, vol. 464, no. 1, pp. 155–165, 2007. doi: 10.1051/0004-6361:20066023.
68. M. F. Horstemeyer, "Integrated Computational Materials Engineering (ICME) for Metals", *Integrated Computational Materials Engineering (ICME) for Metals: Using Multiscale Modeling to Invigorate Engineering Design with Science*, 2012. doi: 10.1002/9781118342664.
69. M. F. Horstemeyer, "Integrated Computational Materials Engineering (ICME) for Metals: Concepts and Case Studies", p. 688, Wiley, 2018.
70. B. Imbiriba et al., "Evolving a puncture black hole with fixed mesh refinement", *Physical Review D*, vol. 70, no. 12, p. 124025, 2004. doi: 10.1103/PhysRevD.70.124025.
71. I. Newton, "Letter from Newton to Robert Boyle", pp. 288–95, Cambridge University Library, 1678.
72. I. Newton, "Philosophiae Naturalis Principia Mathematica", Londini : Jussu Societatis Regiae ac Typis Josephi Streater. Prostat, 1687.
73. P. R. Kafle, S. Sharma, G. F. Lewis, J. Bland-Hawthorn, "Kinematics of the Stellar Halo and the Mass Distribution of the Milky Way Using Blue Horizontal Branch Stars", *The Astrophysical Journal*, vol. 761, no. 2, p. 98, 2012. doi: 10.1088/0004-637X/761/2/98.
74. P. R. Kafle, S. Sharma, G. F. Lewis, A. S. G. Robotham, S. P. Driver, "The need for speed: escape velocity and dynamical mass measurements of the Andromeda galaxy", *Monthly Notices of the Royal Astronomical Society*, vol. 475, no. 3, pp. 4043–4054, 2018. doi: 10.1093/mnras/sty082.
75. P. R. Kafle, S. Sharma, G. F. Lewis, J. Bland-Hawthorn, "ON THE SHOULDERS OF GIANTS: PROPERTIES OF THE STELLAR HALO AND THE MILKY WAY MASS DISTRIBUTION", *The Astrophysical Journal*, vol. 794, no. 1, p. 59, 2014. doi: 10.1088/0004-637X/794/1/59.
76. J. C. Kapteyn, "First Attempt at a Theory of the Arrangement and Motion of the Sidereal System", *The Astrophysical Journal*, vol. 55, p. 302, 1922. doi: 10.1086/142670.
77. M. Karlovini, L. Samuelsson, "Elastic stars in general relativity: I. Foundations and equilibrium models", *Classical and Quantum Gravity*, vol. 22, no. 4, p. 771, 2005. doi: 10.1088/0264-9381/22/4/C02.
78. W. T. B. Kelvin, P. G. Tait, "Treatise on natural philosophy", vol. 1, Clarendon Press, 1867.
79. J. Kijowski, "Relativistic Elastomechanics is a Gauge--Type Theory", p. 12, 1994.
80. A. A. Klypin et al., "Dark Matter Halos in the Standard Cosmological Model: Results from the Bolshoi Simulation", *The Astrophysical Journal*, vol. 740, no. 2, p. 102, 2011. doi: 10.1088/0004-637X/740/2/102.
81. A. Kogut et al., "Dipole Anisotropy in the COBE Differential Microwave Radiometers First-Year Sky Maps", *The Astrophysical Journal*, vol. 419, p. 1, 1993. doi: 10.1086/173453.
82. K. Kondo, "On the analytical and physical foundations of the theory of dislocations and yielding by the differential geometry of continua", *International Journal of Engineering Science*, vol. 2, no. 3, pp. 219–251, 1964. doi: 10.1016/0020-7225(64)90022-9.
83. L. D. Landau, E. M. Lifshitz, "The Classical Theory of Fields - Vol. 2", Butterworth-Heinemann, Oxford OX2 8DP, 2000.
84. P. S. Laplace, "P.S. Laplace, Exposition du système du monde, first edition (1796); Traité de mécanique céleste (1799–1823/1827)", *Landmark Writings in Western Mathematics 1640-1940*, pp. 242–257, 2005. doi: 10.1016/B978-044450871-3/50099-1.
85. P. S. Laplace, "Traité de mécanique céleste", p. 5 v., De L'Imprimerie de Crapelet : Chez J.B.M. Duprat ..., 1798.
86. J. Larmor, "A Dynamical Theory of the Electric and Luminiferous Medium. Part III. Relations with Material Media", *Philosophical Transactions of the Royal Society A: Mathematical, Physical and Engineering Sciences*, vol. 190, pp. 205–493, 1897. doi: 10.1098/rsta.1897.0020.
87. J. Larmor, "Aether and matter; a development of the dynamical relations of the aether to material systems on the basis of the atomic constitution of matter including a discussion of the influence of the earth's motion on optical phenomena, being an Adams prize essay", Cambridge University Press, 1900.
88. A. Lewis, A. Challinor, "CAMB: Code for Anisotropies in the Microwave Background", *Astrophysics Source Code Library, record ascl:1102.026*, 2011.
89. A. Liddle, "An Introduction to Modern Cosmology", Wiley, 2015.
90. T. Lindholm, "N-body algorithms", 1999.
91. J. Liu, X. Chen, X. Ji, "Current status of direct dark matter detection experiments", *Nature Physics*, vol. 13, no. 3, 2017. doi: 10.1038/nphys4039.
92. O. J. Lodge, "Aberration Problems. A Discussion concerning the Motion of the Ether near the Earth, and concerning the Connexion between Ether and Gross Matter; with Some New Experiments", *Philosophical Transactions of the Royal Society A: Mathematical, Physical and Engineering Sciences*, vol. 184, pp. 727–804, 1893. doi: 10.1098/rsta.1893.0015.
93. O. J. Lodge, "Experiments on the Absence of Mechanical Connexion between Ether and Matter", *Philosophical Transactions of the Royal Society A: Mathematical, Physical and Engineering Sciences*, vol. 189, pp. 149–166, 1897. doi: 10.1098/rsta.1897.0006.
94. H. A. Lorentz, "Deux mémoires de Henri Poincaré sur la physique mathématique [Two Papers of Henri Poincaré on Mathematical Physics]", *Acta Mathematica*, vol. 38, pp. 293–308, 1921. doi: 10.1007/BF02392073.
95. H. A. Lorentz, "Electromagnetic phenomena in a system moving with any velocity smaller than that of light", *Proceedings of the Royal Naetherlands Academy of Arts and Sciences*, vol. 6, pp. 809–831, 1904.
96. H. A. Lorentz, "Simplified theory of electrical and optical phenomena in moving systems", *Koninklijke Nederlandse Akademie van Wetenschappen Proceedings Series B Physical Sciences*, vol. 1, pp. 427–442, 1898.
97. H. A. Lorentz, "The relative motion of the earth and the ether", *Versl. Kon. Akad. Wetensch*, vol. 1, p. 74, 1892.
98. H. A. Lorentz, "Versuch einer Theorie der electrischen und optischen Erscheinungen in bewegten Körpern [Attempt of a Theory of Electrical and Optical Phenomena in Moving Bodies]", E.J. Brill, 1895.
99. R. Lynds, V. Petrosian, "Giant luminous arcs in galaxy clusters", *Bulletin of the American Astronomical Society*, vol. 18, p. 1014, 1986.
100. J. E. Marsden, T. J. R. Hughes, "Methematical Foundations of Elasticity", Prentice-Hall, Englewoods Cliffs, NJ, 1983.
101. MathWorks, "mldivide", 2018.
102. R. A. Matzner et al., "Geometry of a Black Hole Collision", *Science*, vol. 270, no. 5238, pp. 941–947, 1995. doi: 10.1126/science.270.5238.941.
103. G. A. Maugin, "Magnetized deformable media in general relativity", *Ann. Inst. Henri Poincare*, vol. 4, pp. 275–302, 1971.
104. J. C. Maxwell, "A Treatise on Electricity and Magnetism", no. v. 1, Clarendon Press, 1873.
105. J. C. Maxwell, "Aether", *Encyclopædia Britannica,*, pp. 568–572, 1878.
106. M. McDonald et al., "A massive, cooling-flow-induced starburst in the core of a luminous cluster of galaxies", *Nature*, vol. 488, no. 7411, pp. 349–352, 2012. doi: 10.1038/nature11379.
107. P. J. McMillan, "Mass models of the Milky Way", *Monthly Notices of the Royal Astronomical Society*, vol. 414, no. 3, pp. 2446–2457, 2011. doi: 10.1111/j.1365-2966.2011.18564.x.
108. P. J. McMillan, "The mass distribution and gravitational potential of the Milky Way", *Monthly Notices of the Royal Astronomical Society*, vol. 465, no. 1, pp. 76–94, 2017. doi: 10.1093/mnras/stw2759.
109. Messier-objects.com, "Messier 63: Sunflower Galaxy", 2015.
110. Messier-objects.com, "Messier 77: Cetus A", *Messier Objects*, 2015.
111. A. A. Michelson, "The relative motion of the Earth and of the luminiferous ether", *American Journal of Science*, vol. s3-22, no. 128, pp. 120–129, 1881. doi: 10.2475/ajs.s3-22.128.120.
112. A. A. Michelson, E. W. Morley, "Influence of motion of the medium on the velocity of light", *American Journal of Science*, vol. s3-31, no. 185, pp. 377–385, 1886. doi: 10.2475/ajs.s3-31.185.377.
113. A. A. Michelson, E. W. Morley, "On the relative motion of the Earth and the luminiferous ether", *American Journal of Science*, vol. s3-34, no. 203, pp. 333–345, 1887. doi: 10.2475/ajs.s3-34.203.333.
114. A. A. Michelson, H. A. Lorentz, D. C. Miller, R. J. Kennedy, E. R. Hedrick, P. S. Epstein, "Conference on the Michelson-Morley Experiment Held at Mount Wilson, February, 1927", *The Astrophysical Journal*, vol. 68, p. 341, 1928. doi: 10.1086/143148.
115. M. Milgrom, "A Modification of the Newtonian Dynamics - Implications for Galaxy Systems", *The Astrophysical Journal*, vol. 270, p. 384, 1983. doi: 10.1086/161130.
116. M. Milgrom, "A modification of the Newtonian dynamics as a possible alternative to the hidden mass hypothesis", *The Astrophysical Journal*, vol. 270, p. 365, 1983. doi: 10.1086/161130.
117. M. Milgrom, "MOND laws of galactic dynamics", *Monthly Notices of the Royal Astronomical Society*, vol. 437, no. 3, pp. 2531–2541, 2014. doi: 10.1093/mnras/stt2066.
118. M. Milgrom, "The MOND paradigm of modified dynamics", *Scholarpedia*, vol. 9, no. 6, p. 31410, 2014. doi: 10.4249/scholarpedia.31410.
119. C. W. Misner, K. S. Thorne, J. A. Wheeler, "Gravitation", *Gravitation*, 1973.
120. C. W. Misner, K. S. Thorne, J. A. Wheeler, "Gravitation", *Gravitation*, 1973.
121. J. W. Moffat, "Scalar–tensor–vector gravity theory", *Journal of Cosmology and Astroparticle Physics*, vol. 2006, no. 03, pp. 004–004, 2006. doi: 10.1088/1475-7516/2006/03/004.
122. NASA, "Planet-Like Body Discovered at Fringes of Our Solar System", *Nasa.gov*, 2004.
123. NASA, "The Milky Way", *Goddard Space Flight Center*, 2018.
124. NASA, "The Whirlpool Galaxy", 2015.
125. P. A. Oesch et al., "A Remarkably Luminous Galaxy at Z = 11.1 Measured with Hubble Space Telescope Grism Spectroscopy", *The Astrophysical Journal*, vol. 819, no. 2, p. 129, 2016. doi: 10.3847/0004-637X/819/2/129.
126. J. H. Oort, "Observational evidence confirming Lindblad's hypothesis of a rotation of the galactic system", *Bulletin of the Astronomical Institutes of the Netherlands*, vol. 3, p. 275, 1927.
127. J. H. Oort, "The force exerted by the stellar system in the direction perpendicular to the galactic plane and some related problems", *Bulletin of the Astronomical Institutes of the Netherlands*, vol. 6, p. 249, 1932. doi: 10.1007/s13398-014-0173-7.2.
128. T. Padmanabhan, "Gravity as Elasticity of Spacetime: a Paradigm to Understand Horizon Thermodynamics and Cosmological Constant", *International Journal of Modern Physics D*, vol. 13, no. 10, pp. 2293–2298, 2004. doi: 10.1142/S0218271804006358.
129. P. W. Hodge, "Magellanic Cloud", *Encyclopaedia Britannica*, 2009.
130. J. Ma, Y. Z. Walker, M. G. McConnachie, "A dynamical model of the local cosmic expansion", *Monthly Notices of the Royal Astronomical Society*, vol. 443, no. 3, pp. 2204–2222, 2014. doi: 10.1093/mnras/stu879.
131. A. A. Penzias, R. W. Wilson, "A Measurement of Excess Antenna Temperature at 4080 Mc/s.", *The Astrophysical Journal*, vol. 142, p. 419, 1965. doi: 10.1086/148307.
132. H. Poincaré, "Sur la dynamique de l'électron", *Rendiconti del Circolo matematico di Palermo*, vol. 21, no. 1, pp. 129–175, 1906. doi: 10.1007/BF03013466.
133. H. Poincaré, "The Principles of Mathematical Physics", *Source: The Monist*, vol. 15, no. 1, pp. 1–24, 1905.
134. H. Poincaré, "The theory of Lorentz and the principle of reaction", *Archives néerlandaises des sciences exactes et naturelles*, vol. 5, no. 2, pp. 252–278, 1900.
135. F. Pretorius, "Evolution of Binary Black-Hole Spacetimes", *Physical Review Letters*, vol. 95, no. 12, p. 121101, 2005. doi: 10.1103/PhysRevLett.95.121101.
136. R. Courant, K. Friedrichs, H. Lewy, "On the Partial Difference Equations of Physics", *New York*, p. 92, 1956.
137. T. H. Randriamampandry, C. Carignan, "Galaxy mass models: MOND versus dark matter haloes", *Monthly Notices of the Royal Astronomical Society*, vol. 439, no. 2, pp. 2132–2145, 2014. doi: 10.1093/mnras/stu100.
138. M. Rangamani, "Gravity and hydrodynamics: lectures on the fluid-gravity correspondence", *Classical and Quantum Gravity*, vol. 26, no. 22, p. 224003, 2009. doi: 10.1088/0264-9381/26/22/224003.
139. C. B. Rayner, "Elasticity in General Relativity", *Proceedings of the Royal Society A: Mathematical, Physical and Engineering Sciences*, vol. 272, no. 1348, pp. 44–53, 1963. doi: 10.1098/rspa.1963.0040.
140. R. Campbell, "Aristotle's On the Heavens", *Ancient History Encyclopedia*, 2016.
141. D. Rodney, B. Gadot, O. R. Martinez, S. R. Roscoat, "Reversible dilatancy in entangled single-wire materials", *Nature Materials*, vol. 15, no. 1, pp. 72–77, 2015. doi: 10.1038/nmat4429.
142. D. Rodney, B. Gadot, O. R. Martinez, S. R. Roscoat, "Reversible dilatancy in entangled single-wire materials.", *Nature materials*, vol. 15, no. 1, pp. 72–7, 2016. doi: 10.1038/nmat4429.
143. J. H. Rose, J. R. Smith, F. Guinea, J. Ferrante, "Universal features of the equation of state of metals", *Physical Review B*, vol. 29, no. 6, pp. 2963–2969, 1984. doi: 10.1103/PhysRevB.29.2963.
144. V. C. Rubin, N. Thonnard, W. K. J. Ford, "Rotational properties of 21 SC galaxies with a large range of luminosities and radii, from NGC 4605 /R = 4kpc/ to UGC 2885 /R = 122 kpc/", *The Astrophysical Journal*, vol. 238, p. 471, 1980. doi: 10.1086/158003.
145. V. C. Rubin, W. K. J. Ford, "Rotation of the Andromeda Nebula from a Spectroscopic Survey of Emission Regions", *The Astrophysical Journal*, vol. 159, p. 379, 1970. doi: 10.1086/150317.
146. S. E. Rugh, H. Zinkernagel, "The quantum vacuum and the cosmological constant problem", *Studies in History and Philosophy of Science Part B: Studies in History and Philosophy of Modern Physics*, vol. 33, no. 4, pp. 663–705, 2002. doi: 10.1016/S1355-2198(02)00033-3.
147. A. S. Saburova, A. V. Zasov, "On the mass and density of the stellar disk of M33", *Astronomy Letters*, vol. 38, no. 3, pp. 139–146, 2012. doi: 10.1134/S1063773712030048.
148. K. Schwarzschild, "On the gravitational field of a mass point according to Einstein's theory", *Sitzungsber. Preuss. Akad. Wiss. Berlin (Math. Phys.)*, vol. 1916, pp. 189–196, 1916.
149. U. Seljak, M. Zaldarriaga, "A Line of Sight Integration Approach to Cosmic Microwave Background Anisotropies", 1996.
150. D. Shoemaker, K. Smith, U. Sperhake, P. Laguna, E. Schnetter, D. Fiske, "Moving black holes via singularity excision", *Classical and Quantum Gravity*, vol. 20, no. 16, pp. 3729–3743, 2003. doi: 10.1088/0264-9381/20/16/313.
151. S. Smith, "The mass of the Virgo cluster", *Contributions from the Mount Wilson Observatory/Carnegie Institution of Washington*, vol. 532, pp. 1–8, 1936.
152. V. Springel et al., "Simulations of the formation, evolution and clustering of galaxies and quasars", *Nature*, vol. 435, no. 7042, pp. 629–636, 2005. doi: 10.1038/nature03597.
153. R. F. Stark, T. Piran, "Gravitational-Wave Emission from Rotating Gravitational Collapse", *Physical Review Letters*, vol. 55, no. 8, pp. 891–894, 1985. doi: 10.1103/PhysRevLett.55.891.
154. A. W. Steiner, J. M. Lattimer, E. F. Brown, "The Equation of State from Observed Masses and Radii of Neutron Stars", *The Astrophysical Journal*, vol. 722, no. 1, pp. 33–54, 2010. doi: 10.1088/0004-637X/722/1/33.
155. G. G. Stokes, "III. On the aberration of light", *The London, Edinburgh, and Dublin Philosophical Magazine and Journal of Science*, vol. 27, no. 177, pp. 9–15, 1845. doi: 10.1080/14786444508645215.
156. H. Sundqvist, G. Veronis, "A simple finite-difference grid with non-constant intervals", 1970. doi: 10.3402/tellusa.v22i1.10155.
157. J. L. Synge, "A theory of elasticity in general relativity", *Mathematische Zeitschrift*, vol. 72, no. 1, pp. 82–87, 1959. doi: 10.1007/BF01162939.
158. A. Tartaglia, "Four Dimensional Elasticity and General Relativity", p. 10, 1995.
159. T. G. Tenev, "Preliminaries to Studying Non-Euclidean Geometry", *ICME Wiki*, 2015.
160. T. G. Tenev, M. F. Horstemeyer, "Mechanics of spacetime — A Solid Mechanics perspective on the theory of General Relativity", *International Journal of Modern Physics D*, vol. 27, no. 08, p. 1850083, 2018. doi: 10.1142/S0218271818500839.
161. T. G. Tenev, M. F. Horstemeyer, "Recovering the Principle of Relativity from the Cosmic Fabric Model of Space", 2018.
162. Theplanets.org, "Whirlpool Galaxy Facts • The Planets", 2010.
163. M. Trenti, P. Hut, "N-body simulations (gravitational)", *Scholarpedia*, vol. 3, no. 5, p. 3930, 2008. doi: 10.4249/scholarpedia.3930.
164. National Institute of Standards and Technology, "CODATA Value: classical electron radius", *The NIST Reference on Constants, Units, and Uncertainty.*, 2014.
165. National Institute of Standards and Technology, "CODATA Value: electron mass", *The NIST Reference on Constants, Units, and Uncertainty*, 2014.
166. National Institute of Standards and Technology, "CODATA Value: neutron mass", *The NIST Reference on Constants, Units, and Uncertainty*, 2014.
167. National Institute of Standards and Technology, "CODATA Value: proton mass", *The NIST Reference on Constants, Units, and Uncertainty.*, 2014.
168. National Institute of Standards and Technology, "CODATA Value: proton rms charge radius", *The NIST Reference on Constants, Units, and Uncertainty.*, 2014.
169. M. Usman, "On the dark matter as a geometric effect in f(R) gravity", *General Relativity and Gravitation*, vol. 48, no. 11, p. 147, 2016. doi: 10.1007/s10714-016-2142-2.
170. A. Vainchtein, "Change of basis, reciprocal basis, covariant and contravariant components of a vector and metric tensor", 2014.
171. World Heritage Encyclopedia, "Gravitational potential", 2014.
172. M. Zaldarriaga, U. Seljak, E. Bertschinger, "Integral Solution for the Microwave Background Anisotropies in Nonflat Universes", *The Astrophysical Journal*, vol. 494, p. 491, 1998. doi: 10.1086/305223.
173. F. Zwicky, "Die Rotverschiebung von extragalaktischen Nebeln", *Helvetica Physica Acta, Vol. 6, p. 110-127*, vol. 6, pp. 110–127, 1933.
174. F. Zwicky, "On the Masses of Nebulae and of Clusters of Nebulae", *The Astrophysical Journal*, vol. 86, p. 217, 1937. doi: 10.1086/143864.
