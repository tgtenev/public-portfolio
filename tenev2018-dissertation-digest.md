# An Elastic Constitutive Model of Spacetime and Its Applications — Digest

**Document Metadata**

| | |
|---|---|
| **Store** | public-portfolio |
| **Publication** | Digest of: Ph.D. dissertation, Dept. of Computational Engineering, Mississippi State University, Starkville, MS, USA, Dec. 2018 (ProQuest No. 10978458, open access) |
| **DOI / URL** | https://www.proquest.com/docview/2162607366 |
| **Cite as** | T. G. Tenev, "An elastic constitutive model of spacetime and its applications," Ph.D. dissertation, Dept. Comput. Eng., Mississippi State Univ., Starkville, MS, USA, 2018. |
| **Converted from** | Condensed from the full Markdown edition [tenev2018-dissertation.md](tenev2018-dissertation.md) in this repository, at commit `7999ab3` |

---

## About This Digest

This document is a **digest** — a condensed reading edition, not the original work. It compresses the roughly 50,000-word Ph.D. dissertation *An Elastic Constitutive Model of Spacetime and Its Applications* (Tichomir G. Tenev, Mississippi State University, December 2018) to under 10,000 words. It covers Chapters I (Introduction), III (Cosmic Fabric Model of Gravity), IV (Recovering Relativity), V (Spacetime Metric of a Spherically Symmetric Inclusion), VI (Dark Matter Effect), and VIII (Conclusions). It omits Chapter II (mathematical background on General Relativity and continuum mechanics), Chapter VII (the numerical simulation framework, summarized here only through the conclusions that depend on it), and Chapter IX (future research directions).

**Assumed audience:** an undergraduate sophomore pursuing a science degree — comfortable with calculus, vectors, and introductory mechanics, but with no prior exposure to general relativity, tensor notation, or continuum mechanics. Technical terms are explained as they arise, and the heavier derivations are sketched rather than reproduced.

**The complete work**, with all derivations, figures, tables, and references, is available on GitHub: [github.com/tgtenev/public-portfolio/blob/main/tenev2018-dissertation.md](https://github.com/tgtenev/public-portfolio/blob/main/tenev2018-dissertation.md). Figure and equation numbers in this digest follow the original, so any passage here can be traced back to its full treatment there.

---

## I. Introduction

The dissertation investigates a two-part proposition:

1. **Physical space exhibits material-like properties.** This idea is developed into the "Cosmic Fabric Model" of gravity: a formal analogy that treats the vacuum of three-dimensional space as a solid body — a thin, elastic plate — and the field equations of General Relativity as the bending equations of that body.
2. **Having material nature, space has inherent structure at multiple length scales.** This "Inherent Structure Hypothesis" offers a new approach to open problems in cosmology — in particular, explaining the gravitational anomalies currently attributed to dark matter.

In the model, space is identified with a solid "hyperplate" called the **cosmic fabric**: broad in the three ordinary spatial dimensions and very thin along a fourth spatial dimension. Matter behaves as **inclusions** in this fabric — think of grains embedded in a sheet — that force the surrounding material to strain, causing the fabric to bend into the fourth dimension. The fabric's intrinsic curvature corresponds to the curvature of space, and its volumetric strain (fractional change in volume) corresponds to the slowing of clocks — which, for weak gravity, is the same as the gravitational potential.

### Why take a material view of space seriously?

Material models of space — historically, "aether" theories — go back to Aristotle, and were developed by Newton, Laplace, Kelvin, and Maxwell, who used mechanical pictures of space to build electromagnetism. The line culminated in the Lorentz Aether Theory (LET): Lorentz explained the null result of the Michelson–Morley experiment (which found no motion of Earth through the aether) by showing that moving clocks slow down and moving rods contract in exactly the way needed to make the aether's rest frame undetectable.

Einstein's Special Relativity (1905) seemed to make the aether unnecessary — not wrong, just superfluous. But after developing General Relativity, Einstein himself revisited the question, arguing in his 1920 Leiden lecture that "to deny the aether is ultimately to assume that empty space has no physical qualities whatever," which conflicts with the fundamental facts of mechanics (rotation, for instance, is physically detectable even in otherwise empty space). Moreover, practical applications of General Relativity often *require* separating space from time — the Arnowitt–Deser–Misner (ADM) formalism used in numerical relativity does exactly that. A material model of space, which views space as an object progressing in time, does this separation naturally.

### The clue: Hooke's Law resembles Einstein's equation

The specific motivation for the model is a structural similarity between the two fields' central laws. Hooke's Law for an isotropic linear elastic material relates the stress tensor $\sigma^{kl}$ (internal force per unit area) to the strain tensor $\varepsilon_{ij}$ (dimensionless deformation):

$$
\sigma^{kl} = \frac{Y}{1+\nu} \left(\frac{\nu}{1-2\nu} g^{ij}g^{kl} + g^{ik}g^{jl}\right)\varepsilon_{ij} \quad (1.2)
$$

where $Y$ is Young's modulus (stiffness) and $\nu$ is Poisson's ratio (how much a stretched material narrows sideways). Einstein's field equations of General Relativity read:

$$
T_{\mu\nu} = \frac{1}{\kappa} \left(R_{\mu\nu} - \frac{1}{2}R g_{\mu\nu} \right) \quad (1.3)
$$

where $T_{\mu\nu}$ is the stress–energy tensor (energy and momentum content), $R_{\mu\nu}$ and $R$ measure spacetime curvature, $g_{\mu\nu}$ is the spacetime metric, and $\kappa \equiv 8\pi G/c^4$ is the Einstein constant. Both laws relate stress (left side) to deformation (right side) — a *constitutive relation*, the kind of material-specific law that distinguishes steel from rubber. The apparent mismatch is dimensional: strain is dimensionless while curvature has dimensions of 1/length². The resolution, developed in Chapter III, is to compare Einstein's equation not to stretching but to **plate bending**, where stress is proportional to the *second spatial derivative* of strain.

A century of related work has connected mechanics and relativity from various directions — relativistic generalizations of elasticity, entropy-based derivations treating spacetime as an elastic solid, and fluid analogies of gravity (which fall short because fluids carry no shear waves, while gravitational waves are transverse). Notably, Hehl and Kiefer independently arrived at elastic constants for a cosmic medium equivalent to Poisson's ratio $\nu = 1$ — the same value Chapter III derives. What distinguishes this dissertation is the insight that Einstein's equation corresponds to the *bending* of a plate rather than to simple stretch or shear; without it, the detailed correspondence between space and a material medium remains obscured.

### Length scales and inherent structure

A "length scale" is a range of distances over which certain physical laws and parameters dominate. The dissertation considers four: **substructure** ($10^{-36}$–$10^{-10}$ m, the discrete make-up of the fabric itself), **continuum** ($10^{-10}$–$10^{14}$ m, where space is smooth and General Relativity applies), **structure** ($10^{14}$–$3\times10^{24}$ m, galactic scales where dark-matter anomalies appear), and **cosmic** (above $3\times10^{24}$ m, the global geometry of the universe).

![Cosmic hierarchical length scales.](https://figures.tgtenev.com/tenev2018-dissertation/fig-lengthscales.svg)

**Figure 1.1.** Cosmic hierarchical length scales and the information bridges between them. The field equations of General Relativity — and analogously the constitutive equations of the cosmic fabric — dominate the continuum length scale (2). The dark matter effect is observed at the structure length scale (3). Structure at scales (3) and (4) contributes the $\overline{\mathcal{L}}$ term to the action; scale (1) contributes $\mathcal{L}_\text{M}$.

The analogy: at scales under a kilometer the Earth's surface is well approximated as flat; between 1 and 100 km local terrain matters; beyond 100 km the globe's curvature dominates. Those boundaries are not fundamental constants — they reflect how the Earth happens to be structured. Likewise, the Inherent Structure Hypothesis proposes that space has structure at galactic and cosmic scales reflecting the organization of the universe. Formally, this enters the Lagrangian (action) formulation of gravity as an extra term $\overline{\mathcal{L}}$:

$$
\mathcal{S} = \int_{\Omega}\left(\mathcal{L} - \overline{\mathcal{L}} + \mathcal{L}_\text{M} \right) d\Omega \quad (1.1)
$$

where $\mathcal{L}$ is the Lagrangian density from spacetime curvature, $\mathcal{L}_\text{M}$ accounts for matter–energy fields, and $\overline{\mathcal{L}}$ — a term not previously considered — is the correction due to the *inherent* (undeformed) curvature of space. Without $\overline{\mathcal{L}}$, the Cosmic Fabric model reproduces conventional General Relativity (Chapters III–V); with it, the model modifies General Relativity at galactic scales and above (Chapter VI).

### Dark matter and MOND

Galaxies rotate "too fast": stars far from the galactic center orbit at speeds that the visible mass cannot gravitationally sustain. Similar anomalies appear in the motions and gas pressure of galaxy clusters. The dissertation calls these observations the **Dark Matter (DM) effect** and distinguishes them from the **DM Hypothesis** — the proposal that invisible mass halos cause them. Despite decades of searches, no dark matter particle or compact object has been directly detected.

The leading alternative, Milgrom's Modified Newtonian Dynamics (MOND), postulates that for accelerations below a universal parameter $a_0 \approx 1.2\times10^{-10}\ \text{m s}^{-2}$, Newton's law is modified. MOND fits many galactic rotation curves remarkably well with a single parameter, but it remains empirical, has notable outlier galaxies, and lacks a settled theoretical foundation. Intriguingly, $2\pi a_0 \approx cH_0$ (where $H_0$ is Hubble's parameter) — hinting that $a_0$ may be related to the inherent geometry of the cosmos rather than being a new constant of nature. Chapter VI returns to this.

### Assumptions

Throughout, two simplifying assumptions apply (they keep the math tractable and are not fundamental to the model): **weak gravity** — the gravitational potential satisfies $|\Phi/c^2| \ll 1$, true nearly everywhere (at Earth's surface, the Sun contributes $\sim10^{-8}$) — and **nearly static fields** — gravitating masses move much slower than light, so time derivatives are negligible.

---

## III. The Cosmic Fabric Model of Gravity

This chapter constructs the analogy in detail: it specifies a material body whose behavior, derived solely from Hooke's Law, is demonstrably analogous to spacetime's behavior per General Relativity.

### The picture

Physical space is identified with the mid-surface of the cosmic fabric — a four-dimensional plate, thin along the fourth spatial dimension $x^4$, immersed in a flat four-dimensional "reference space." Matter–energy acts as inclusions that prescribe strain in the fabric. Because the prescribed strain is uneven — larger near the inclusion — the fabric must bend into the fourth dimension to accommodate it geometrically:

![Plate bending from flat into a curved geometry.](https://figures.tgtenev.com/tenev2018-dissertation/fig-plate-bending.svg)

**Figure 3.1.** A plate bending from flat geometry (a) into a curved geometry (b) because of an inclusion that prescribes an uneven strain field (dashed lines, diverging arrows): larger strain near the center, tapering off with distance. To accommodate the prescribed strain, the plate must bend into the transverse dimension.

This is the mechanical counterpart of "matter curves spacetime." Two coordinate systems track the deformation: **material coordinates** $x^I$ painted onto the fabric (they move with it as it deforms) and **reference coordinates** $y^I$ fixed in the enclosing hyperspace. An observer inside the fabric can only ever measure with rulers that are themselves part of the fabric — so stretching of the fabric is perceived from within as expansion of space, and differential stretching as intrinsic curvature of space. The reference space is a mathematical scaffold, not necessarily a physical entity.

![Material Coordinates versus Reference Coordinates.](https://figures.tgtenev.com/tenev2018-dissertation/fig-material-ref-coords.svg)

**Figure 3.2.** Material coordinates $x^I$ versus reference coordinates $y^I$, before (a) and after (b) deformation of a body $\mathcal{B}$. Material coordinates are carried along with the material as it deforms; reference coordinates remain fixed.

### Three postulates

**1. Elastic thin hyperplate.** The fabric is a stack of three-dimensional elastic layers, each isotropic and obeying Hooke's Law (1.2). Its small thickness $L$ — comparable to Planck's length, $l_p \approx 1.6\times10^{-35}$ m — creates resistance to bending, while leaving the fabric an essentially 3D object at ordinary scales.

**2. Inclusions.** Matter is a source of volumetric strain $\varepsilon$ (the fractional volume change of the fabric):

$$
\nabla^2 \varepsilon = -\frac{1}{2} c^2\kappa \rho \quad (3.2)
$$

where $\rho$ is the matter–energy density. Equivalently: the "Schwarzschild-radius density" of matter — its mass converted to a geometric length — is what sources strain. How pointlike particles move freely through a stiff fabric is answered by their wave nature (waves propagate readily through stiff media); the model abstracts those details and takes the prescribed strain field as its input.

**3. Lapse rate.** All matter–matter interactions are mediated by signals propagating in the fabric as shear waves. Where those waves propagate slower (relative to the reference space), *all* physical processes — hence all clocks — run proportionally slower, regardless of the clock's design. Quantitatively, the shear wave speed $v_s$ and the rate of proper time $\tau$ (clock time) relative to coordinate time $t$ both scale as:

$$
v_s = (1 + \varepsilon)^{-1}c, \qquad \frac{d\tau}{dt} = (1 + \varepsilon)^{-1} \quad (3.3-3.4)
$$

An observer inside the fabric always measures the *same* signal speed, because the clock slowdown exactly compensates the wave slowdown — the mechanical origin of the invariance of the speed of light.

### From Hooke's Law to the Einstein–Hilbert action

In physics, a system's dynamics are fully encoded in its **action** $\mathcal{S}$ — an integral whose extremization yields the equations of motion. Two theories with the same action have the same physics. General Relativity follows from the Einstein–Hilbert action; so if the fabric's elastic energy, computed purely from Hooke's Law, produces an action of the same form, the analogy is established.

The derivation proceeds in three steps. First, in the weak-field regime the spacetime metric is written $g_{\mu\nu} = \eta_{\mu\nu} + 2\varepsilon_{\mu\nu}$ — flat spacetime plus small deviations — and the deviations are identified *physically*: the spatial components are the fabric's strain, and the time–time component equals the volumetric strain, $\varepsilon_{00} = \varepsilon$ (from the lapse-rate postulate). Second, the elastic energy per unit volume is averaged across the plate's thickness and split into a **bending** part $U_\text{B}$ (strains that reverse sign across the mid-surface) and a **membrane** part $U_\text{M}$ (uniform in-plane stretching). Using thin-plate theory, the bending energy comes out proportional to the intrinsic curvature $R^\text{3D}$ of the mid-surface:

$$
U_\text{B} = - \frac{YL^2}{48} R^\text{3D} \quad (3.18)
$$

— *provided* Poisson's ratio is fixed at $\nu = 1$, the unique choice that removes an unphysical dependence on how the fabric sits in the reference space (its extrinsic curvature). Third, the membrane energy is shown to vanish for nearly static deformations. The fabric's Lagrangian density is then $-U_\text{B}\sqrt{|g|}$, which — using the linearized relation between spatial curvature $R^\text{3D}$ and the four-dimensional Ricci scalar $R$ — takes exactly the Einstein–Hilbert form:

$$
\mathcal{S}_\text{F} = \frac{YL^2}{48} \int R\sqrt{|g|}\ \mathrm{d}x^4 \quad \text{versus}\quad \mathcal{S}_\text{EH}= \frac{1}{2\kappa} \int R\sqrt{|g|}\ \mathrm{d}x^4 \quad (3.1)
$$

Identifying the two coefficients, $YL^2/48 = 1/(2\kappa)$, calibrates the model: the fabric's stiffness is fixed by Newton's constant.

### What the analogy buys: physical interpretations

**Gravitational potential is volumetric strain.** Combining the linearized-gravity relation between $\Phi$ and $g_{00}$ with the lapse-rate postulate gives $\Phi/c^2 = -\varepsilon$: where space is stretched, potential is negative and clocks run slow.

**The cosmic fabric is literally a fabric.** Known materials with $\nu = 1$ have fibrous, woven substructure (recently discovered "compressive dilatant" and "stretch densifying" materials are made of entangled wires and twisted threads). The model thus hints that space has a weave-like substructure.

**Only transverse waves — and why light speed is the maximum.** With $\nu = 1$, the shear modulus is $\mu = Y/4$ but the pressure-wave modulus is exactly zero: the fabric supports *no* longitudinal (pressure) waves, only transverse (shear) waves. In ordinary materials pressure waves outrun shear waves; here they are absent altogether, making the shear speed — the speed of light — the fastest possible signal. This matches observation: all waves known to propagate in vacuum (light, gravitational waves) are transverse.

**Gravitational waves are shear waves.** Assuming the Lagrangian extends to fast-changing fields, shear disturbances in the fabric obey the wave equation $\partial^2\varepsilon_{ij}/\partial t^2 = c^2\nabla^2 \varepsilon_{ij}$, identical in form to the solid-mechanics shear-wave equation with $c^2 = \mu/\rho_\text{F}$. Working out which strain components can oscillate independently leaves exactly two — the two polarizations of gravitational waves, here derived by solid-mechanics reasoning.

**Stiffness and density of free space.** Taking $L \sim l_p$ gives an enormous elastic modulus, $Y \sim 4.4\times10^{113}\ \text{N m}^{-2}$, and a fabric density $\rho_\text{F} = \mu/c^2 \sim 1.3\times10^{96}\ \text{kg m}^{-3}$ — agreeing to order of magnitude with Quantum Field Theory's estimate of the zero-point energy density of the vacuum.

**Table 3.1.** Comparison between the General Relativity and Solid Mechanics perspectives.

| General Relativity Perspective | Solid Mechanics Perspective |
|---|---|
| Physical space | Mid-hypersurface of a hyperplate called "cosmic fabric" |
| Spacetime | The world volume of the fabric's mid-hypersurface |
| Intrinsic curvature of space | Intrinsic curvature of the fabric's mid-hypersurface |
| Gravitational potential $\Phi$ | Volumetric strain $\varepsilon$, where $\varepsilon = -\Phi/c^2$ |
| Gravitational waves | Shear waves traveling at the speed of light |
| Matter curves spacetime. | Matter induces prescribed strain, causing the fabric to bend and time lapse to slow down. |
| Action in free space, $\mathcal{S} = \frac{1}{2\kappa} \int R\sqrt{\vert g\vert}\ d^4x$ | Action outside inclusions, $\mathcal{S} = \frac{L^2 Y}{48} \int R\sqrt{\vert g\vert}\ d^4x$ |
| Constants of nature: $G,\ \hbar,\ c$ | Elastic constants: $Y = 6c^7/(2\pi\hbar G^2),\ \nu=1$ |

The chapter concludes that postulating Einstein's field equations and postulating a cosmic fabric with these material properties are two approaches to the same underlying reality.

---

## IV. Recovering Relativity

The fabric ostensibly defines a hyperplane of absolute simultaneity — a preferred rest frame. Doesn't that contradict relativity? This chapter shows that it does not: at the continuum length scale, the preferred frame is *undetectable*, and both postulates of Special Relativity — (1) physical laws are the same in all inertial frames; (2) the speed of light is invariant — are *deduced* from the fabric's postulates rather than assumed.

### Invariance of the speed of signals

**Stationary observers at different locations.** Signals need not propagate at uniform speed relative to the reference space. But by the lapse-rate postulate, a clock located where signals travel slower ticks proportionally slower. Measuring the local signal speed with the local clock, the two effects cancel exactly: every stationary observer measures the same value, identified with the speed of light $c$.

**A moving observer.** Consider an observer moving with velocity $v$ through the fabric, timing a light signal's round trip across a fixed distance *transverse* to the motion. From the fabric frame, the signal traverses a diagonal path (Pythagoras), so its effective transverse speed is $\sqrt{c^2 - v^2}$. By the lapse-rate postulate, the moving observer's clocks slow by:

$$
\frac{d\tau'}{d\tau} = \sqrt{1 - \beta^2},\quad \beta \equiv \frac{v}{c} \quad (4.3)
$$

— time dilation, derived mechanically.

![Moving observer measuring light speed in transverse orientation.](https://figures.tgtenev.com/tenev2018-dissertation/fig-moving-observer.svg)

**Figure 4.2.** An observer moving with velocity $v$ relative to the fabric measures the round-trip time of a light signal traveling transverse to the motion, shown from the viewpoint of the moving observer (a) and a stationary observer (b). The effective transverse signal speed is $\sqrt{c^2 - v^2}$.

**Lengths along the motion.** Timing a round-trip signal along a rod carried with the motion (travel times $dl/(c+v)$ and $dl/(c-v)$) and applying the time-dilation result forces a choice: either the moving observer finds light speed different along the motion than across it — anisotropy that the Michelson–Morley experiment ruled out — or rods aligned with the motion change length, with the comoving observer's measured length $dl'$ related to the fabric-frame length by $dl' = dl/\sqrt{1-\beta^2}$. This is the familiar length contraction, seen from the fabric's side: a moving rod occupies less fabric-frame length than its rest measurement. The combined effects of time dilation and length change make the moving observer measure exactly $c$ in every direction. Lorentz reached the same conclusion for light; here it holds for *all* signals, because the fabric mediates all matter–matter interactions — which is why not just electromagnetic clocks but every physical process is affected.

### The Lorentz transformations, geometrically

With invariant signal speed established, the coordinate transformations between a stationary and a moving observer follow from symmetry alone. On a spacetime diagram with time scaled by $c$, a photon's path bisects the stationary observer's axes; by invariance it must also bisect the moving observer's axes, which tilt inward symmetrically (slopes $\beta$ and $1/\beta$). Translational symmetry of the fabric (valid at the continuum scale) forces the transformation to be linear, and requiring that the inverse transformation has the same form with $v \to -v$ pins down the coefficients:

$$
\begin{pmatrix} x' \\ c\tau' \end{pmatrix} = \gamma \begin{pmatrix} 1 & -\beta \\ -\beta & 1 \end{pmatrix} \begin{pmatrix} x \\ c\tau \end{pmatrix}, \qquad \gamma = \frac{1}{\sqrt{1-\beta^2}} \quad (4.9, 4.11)
$$

— the Lorentz transformations.

![Coordinate transformation between a moving and a stationary observer.](https://figures.tgtenev.com/tenev2018-dissertation/fig-lorentz-transform.svg)

**Figure 4.4.** A stationary (unprimed) and a moving (primed) observer as two sets of coordinate axes. With time scaled by $c$, the photon path bisects the unprimed axes; by light-speed invariance it must also bisect the primed axes.

Composing two Lorentz transformations yields another (with the relativistic velocity-addition law), so *any* two inertial frames — not just "moving versus rest" — transform between each other identically. No experiment at the continuum scale can single out the fabric's rest frame: the Principle of Relativity is recovered.

### When the rest frame becomes detectable

The derivation relied on translational symmetry, which holds only at the continuum scale. Where symmetry breaks, the rest frame becomes physical. At the **cosmic scale** it already has: for any point in space there is exactly one frame in which the Cosmic Microwave Background redshift is isotropic. From Earth, the CMB shows a dipole indicating the Solar System moves at about 600 km/s toward Centaurus. Local physics stays frame-independent, but cosmic-scale observations do distinguish states of motion. At **sub-continuum scales**, the fabric's woven substructure and thickness break the symmetry too — relevant, the dissertation argues, to any future quantum theory of gravity, where solid mechanics' techniques for bridging length scales within materials could be leveraged.

In summary: at the continuum scale, the Cosmic Fabric model stands to Lorentz Aether Theory as General Relativity stands to Special Relativity — a generalization to curved, deforming space — while additionally carrying length-scale parameters that the purely continuum theories lack.

---

## V. The Spacetime Metric of a Spherical Mass

Chapters III–IV treated the fabric *outside* matter. This chapter works out the matter–fabric interaction for the simplest case — a static, spherically symmetric body (a "ball" of matter) — and derives the resulting spacetime geometry from mechanics alone. Two results follow: the metric matches the Schwarzschild solution of General Relativity, and, unexpectedly, the model *requires matter to be made of discrete particles*.

### Setting up the deformation

A **metric** is the rule for computing real distances (and times) from coordinate differences; deriving it is equivalent to specifying the deformation completely. By symmetry, the deformation has two ingredients: an in-plane radial stretch $r = (1+e)\overline{r}$ (material initially at radius $\overline{r}$ moves to radius $r$), and a transverse displacement $w(r)$ into the fourth dimension:

![Profile of a spherically symmetric deformation.](https://figures.tgtenev.com/tenev2018-dissertation/fig-profile.svg)

**Figure 5.1.** The deformation is a radial displacement $r = r(\overline{r})$ (in-plane stretching) followed by a transverse displacement $w = w(r)$ into the fourth spatial dimension. Here $\overline{r}$ is distance from the origin prior to deformation.

The governing equations come from the Principle of Least Action applied to the total energy — bending energy $U_\text{B}$, membrane energy $U_\text{M}$, and the body's relativistic energy density $c^2\rho$: (1) the bending energy must balance the matter energy, $U_\text{B} + c^2\rho = 0$, which in geometric terms fixes the spatial curvature inside the body, $R^\text{3D} = 6/r_0^2$; (2) the inclusion postulate $\nabla^2\varepsilon = -\tfrac{3}{2}/r_0^2$; and (3) the total membrane energy must vanish (taken up below). Here mass is described geometrically: $r_s \equiv 2GM/c^2$ is the body's Schwarzschild radius (its mass as a length), $r_g$ its actual radius, and $r_0 \equiv \sqrt{r_g^3/r_s}$ encodes its density.

Solving these ordinary differential equations (with regularity at the center and continuity at the surface) yields closed forms for $w$, $\varepsilon$, and $e$. Outside the body, the transverse displacement is $w_\text{ext} = 2\sqrt{r_s(r - r_s)}$ — and the strains fall off as $\varepsilon_\text{ext} = r_s/(2\overline{r})$.

### Recovering the Schwarzschild metric

Assembling the strains into the line element (the squared spacetime distance $ds^2$) gives, outside the body:

$$
ds^2_\text{ext} = -\left(1-\frac{r_s}{\overline{r}}\right) c^2 dt^2 + \left(1+\frac{r_s}{\overline{r}} - \frac{2 r_s r_g^2}{5\overline{r}^3}\right) d\overline{r}^2 + \left(1+\frac{r_s r_g^2}{5\overline{r}^3}\right) \overline{r}^2 d\Omega^2 \quad (5.40)
$$

with a corresponding interior solution. For comparison, the linearized Schwarzschild metric of General Relativity is:

$$
ds^2_\text{ext} = -\left(1-\frac{r_s}{r}\right) c^2 dt^2 + \left(1+\frac{r_s}{r}\right) dr^2 + r^2 d\Omega^2 \quad (5.53)
$$

The time coefficients are identical, and both metrics produce the same intrinsic spatial curvature everywhere. The spatial coefficients differ only because the fabric solution tracks the in-plane stretch $e(\overline{r})$, which General Relativity regards as physically meaningless coordinate relabeling. Substituting $r = (1+e)\overline{r}$ into (5.40) recovers (5.53) exactly: **the two metrics are equivalent up to a coordinate rescaling.** This validates the model's postulates. The fabric version carries extra physical content, though: it is simultaneously the deformation tensor of a solid, and it shows that the fractional volumetric stretch of space always equals the fractional slowdown of time.

The *shape* the fabric bends into is also recognizable. In 1916 Ludwig Flamm showed that the spatial part of the Schwarzschild solution can be visualized as a paraboloid of revolution (exterior) capped by a spherical dome (interior) in four-dimensional space — long used as a teaching picture. Here, Flamm's paraboloid appears as an actual material body: the computed $w(r)$ is exactly Flamm's profile.

![Flamm's Paraboloid.](https://figures.tgtenev.com/tenev2018-dissertation/fig-flamms-paraboloid.svg)

**Figure 5.5.** The bending of the cosmic fabric due to a spherically symmetric inclusion of radius $r_g$ assumes the shape known as Flamm's Paraboloid: a paraboloid in the exterior and a spheroid cap of radius $r_0$ in the interior.

### Why matter must be discrete

The remaining constraint — vanishing membrane energy — has a surprising consequence. Computing the total membrane energy $W_\text{M}$ for a *perfectly continuous* spherical body gives a negative quantity whose magnitude saturates at:

$$
\max |W_\text{M}| = \frac{27 c^4 r_s^2 r_g}{35 G L^2} \quad (5.47)
$$

This grows as the *square* of the mass ($r_s^2$), while the body's own relativistic energy grows only linearly ($\propto r_s$). For the fabric's response not to overwhelm the energy of the body that caused it, one must require $r_s r_g \lesssim \frac{35}{54}L^2$ — an upper bound on how massive a *continuous* body can be, set by the fabric's thickness $L$. Proposing $L = \sqrt{2hG/c^3} = 5.7\times10^{-35}$ m (the energy scale where a body's Schwarzschild radius equals its de Broglie wavelength), the maximum continuous mass works out to $\sim2.5\times10^{-8}$ kg — a Planck-scale speck. Anything more massive **must be composed of discrete particles**.

Checking real particles against the bound $54\, r_s r_g/(35 L^2) \lesssim 1$: the electron scores $\sim0.002$ (comfortably within), the proton $\sim1.0$, and the neutron $\sim1.3$ — essentially saturating it. That the proton and neutron slightly exceed the bound is consistent with the fact that they, unlike the electron, have substructure (quarks). Moreover, if individual particles prescribe *asymmetric* strains (longitudinal or oblate rather than perfectly spherical) — plausible given their wave nature — the membrane energy vanishes identically, while the body still appears continuous and spherically symmetric at large scales:

![Substructure of a spherically symmetric body.](https://figures.tgtenev.com/tenev2018-dissertation/fig-substructure.svg)

**Figure 5.4.** The substructure of an ostensibly continuous body, progressively revealed: (a) idealized as continuous; (b) each cell's mass concentrated into a small particle; (c) each particle locally anisotropic, while the body remains ostensibly isotropic overall.

The significance: General Relativity, a strictly continuum theory, cannot make statements about the granularity of matter. The Cosmic Fabric model, carrying a built-in length-scale parameter ($L$), *predicts* discreteness — and the prediction agrees with the known constitution of matter.

---

## VI. The Dark Matter Effect

This chapter presents the dissertation's proposed alternative to dark matter: the **Inherent Structure Hypothesis (ISH)** — the gravitational anomalies attributed to dark matter are manifestations of the *inherent curvature* of space, curvature that exists apart from matter. In fabric terms: the relaxed, unstrained shape of the cosmic fabric need not be flat. In General Relativity terms: the field equations are modified so that where the stress–energy tensor vanishes, curvature does not vanish but equals the inherent curvature. Because ISH invokes no new dynamics — only a different initial geometry — it escapes the criticism (based on the gravitational-wave event GW170817) that felled several "dark matter emulator" theories: photons and gravitational waves follow the same geodesics here.

### How inherent curvature amplifies gravity

Consider space with a spherically symmetric inherent curvature, described by a transverse displacement profile $\overline{w}(\overline{r})$ in the fourth dimension, where $\overline{r}$ is the *coordinate* (projected) distance from the symmetry center. Because the fabric is sloped, the **proper** distance $\overline{l}$ — what an observer inside space actually measures — exceeds the projected distance: $d\overline{l} = \sqrt{1 + (\overline{w}')^2}\, d\overline{r}$.

Placing a gravitating mass at the center and following a test particle along its geodesic (using the inclusion postulate with curvature-aware covariant derivatives), the chapter derives a strikingly simple differential equation for the proper gravitational acceleration $a$, whose solution is:

$$
a(\overline{r}) = -\frac{G M(\overline{r})}{\overline{r}^2} \quad (6.23)
$$

**Newton's inverse-square law holds — but in terms of the projected distance $\overline{r}$, not the proper distance $\overline{l}$.** Since $\overline{r} \le \overline{l}$, the measured acceleration at a given *measured* distance is stronger than the inverse-square law predicts. An astronomer applying Newton's law with $\overline{l}$ would infer extra invisible mass:

![Inherent shape of space causing the "Dark Matter" effect.](https://figures.tgtenev.com/tenev2018-dissertation/fig-dark-matter-effect.svg)

**Figure 6.2.** A test particle at $P$, a proper distance $\overline{l}$ from a body of mass $M_B$ at $B$, experiences acceleration $a_P$ greater than the inverse-square law predicts in terms of $\overline{l}$ — but matching it in terms of the projected distance $\overline{r}$. The critical distance $r_c$ bounds the region where the hypothesis is observationally equivalent to a dark matter halo.

### Equivalence with dark matter halos — and where it breaks

Can inherent curvature mimic *any* dark matter distribution? Yes: given enclosed visible mass $M(\overline{r})$ and hypothetical dark mass $M_\text{DM}(\overline{r})$, the equivalent curvature profile is $\overline{l} = \overline{r}\sqrt{1 + M_\text{DM}/M}$, which is geometrically consistent for all realistic distributions (dark matter is always observed alongside visible matter, with the dark fraction growing outward).

The converse fails, and that is where the hypothesis becomes falsifiable. For a curvature profile to be interpretable as physically admissible dark matter (non-negative density), the profile must satisfy $\overline{l}'' \ge 0$ — the slope must keep growing. But unless the inherent curvature extends over the whole cosmos, the profile must eventually flatten out and rejoin the global geometry: beyond some **critical radius $r_c$**, the concavity reverses, and no dark matter distribution can reproduce the effect. This yields three testable predictions distinguishing ISH from dark matter:

1. **Far beyond $r_c$, the dark matter effect reverses and disappears** — a distant orbiting test particle behaves as if no halo were enclosed.
2. Gravitational systems exhibiting the effect will show a relatively pronounced edge near $r_c$.
3. At the cosmic scale, "dark matter" contributes nothing net to the universe's contents (the famous 27% figure is model-dependent, not a direct observation).

### Equivalence with MOND, and galaxy data

Choosing a specific curvature profile reproduces MOND exactly (up to $r_c$). Working backwards from MOND's acceleration law with the standard interpolation function yields the required profile in closed form, governed by a single scale parameter $s \equiv \sqrt{GM/a_0}$ characterizing the gravitating mass:

![MOND-equivalent inherent structure profile.](https://figures.tgtenev.com/tenev2018-dissertation/fig-mond-profile.svg)

**Figure 6.3.** The inherent curvature profile whose effect is equivalent to MOND up to a critical distance $r_c$, beyond which the actual profile may diverge from the MOND-equivalent one. The scale parameter is $s \equiv \sqrt{GM/a_0}$.

Surveying fourteen galaxies and clusters spanning masses of $10^9$–$2\times10^{15}$ solar masses and distances from 25 thousand to 13.4 billion light years (Table 6.1 in the full text — Milky Way, the Magellanic Clouds, Andromeda, M33, Pinwheel, Whirlpool, M77, Malin 1, the Phoenix Cluster, GN-z11, and others), the visible radius $R$ falls within an order of magnitude of $s$ for nearly all: $R/s$ ranges from about 0.1 to 3, with outliers like the oddly-shaped Cartwheel galaxy ($R/s \approx 10.7$). The same relationship even holds for the Solar System ($R/s = 0.14$, taking $R$ as the Sun–Sedna distance). Since MOND fits most observations well, this correspondence validates ISH — while ISH additionally accommodates MOND's outliers naturally: galaxies that "prefer" a larger or smaller $a_0$ simply have more or less inherent curvature. And two empirical "coincidences" — the MOND length $c^2/a_0 \approx 7.5\times10^{26}$ m being comparable to the Hubble distance, and $s$ tracking each system's geometric size — both point toward a geometrical, structural origin for the effect. MOND, on this reading, is a first-order approximation to the inherent structure of space.

### Implications for cosmology

Like MOND, ISH is incompatible with the standard $\Lambda$CDM model, which requires non-baryonic dark matter and presupposes the Cosmological Principle (no structure above 100 Mpc). ISH takes the opposite premise — structure is fundamental at every length scale. The galaxy data show inherent curvature *correlated* with matter, yet inherent curvature is by definition uncaused by matter; the suggested resolution is reversed causality: **the inherent structure of space is what caused matter to organize into galaxies and clusters in the first place** — potentially also explaining the universe's large-scale walls and filaments, which are too extended to be gravitationally bound. Inherent structure could serve future cosmological models as the seed for structure formation, the role $\Lambda$CDM assigns to cold dark matter.

---

## VIII. Conclusions

The dissertation explored the analogy between physical space and a material solid, on the premise that the universe is a functional system exhibiting structure at multiple length scales — and that space, as a component of that system, does too. The theoretical foundation (the Cosmic Fabric model) was established first, then applied to a concrete cosmological problem (the dark matter effect), analytically and numerically. The principal takeaways, condensed from the original's twenty-one points:

1. **Space is material-like.** Physical space behaves as the mid-surface of a thin elastic hyperplate — the cosmic fabric — deforming in a four-dimensional reference space and obeying Hooke's Law (Ch. III).
2. **Matter acts as inclusions** prescribing strain ($\nabla^2\varepsilon = -c^2\kappa\rho/2$) that bends the fabric; the fabric mediates all matter–matter interactions via shear-wave signals, and clock rates track the local signal speed — so the spacetime metric is fully specified by the fabric's mechanical state (Ch. III).
3. **The actions agree.** The fabric's elastic action equals the Einstein–Hilbert action; Einstein's equations are analogous to plate-bending equations, with the Einstein constant as the stiffness constant (Ch. III).
4. **Relativity is recovered, not assumed.** Signal speed is invariant for all observers; Lorentz transformations apply between all frames; the fabric's rest frame is undetectable at the continuum scale — explaining Michelson–Morley — though it becomes detectable where symmetry breaks (e.g., the CMB rest frame). The model generalizes Lorentz Aether Theory the way General Relativity generalizes Special Relativity (Ch. IV).
5. **Physically meaningful quantities.** The linearized-gravity perturbations $h_{\mu\nu}$ are twice the fabric strains; gravitational potential is negative volumetric strain, $\Phi/c^2 = -\varepsilon$ (Ch. III).
6. **Poisson's ratio is unity**, implying weave-like substructure, no pressure waves in space (all vacuum waves are transverse, consistent with Birkhoff's theorem), gravitational waves as two-polarization shear waves, an elastic modulus $Y \sim 10^{113}\ \text{N m}^{-2}$, and a fabric density matching Quantum Field Theory's zero-point energy density (Ch. III).
7. **Schwarzschild recovered; Flamm's paraboloid materialized.** The metric around a spherical mass, derived purely from solid mechanics, is the Schwarzschild solution up to coordinate rescaling — with added meaning: volumetric stretch of space always equals the fractional slowdown of time. The fabric bends into Flamm's paraboloid, now a material body rather than a teaching picture (Ch. V).
8. **Matter must be discrete.** Membrane-energy analysis bounds the mass of any perfectly continuous body ($\max M \sim 2.5\times10^{-8}$ kg), so matter must consist of small particles — a cross-length-scale prediction General Relativity cannot make, consistent with the proton, neutron, and electron (Ch. V).
9. **Inherent curvature explains the dark matter effect.** Curvature of space uncaused by matter amplifies the gravity of ordinary matter (Newton's law holds in projected, not proper, distance), reproducing dark-matter and MOND phenomenology within a critical radius and diverging from both beyond it — a falsifiable distinction (Ch. VI).
10. **A numerical framework substantiates it.** An enhanced particle-mesh method accounting for non-flat spatial geometry (Ch. VII, not digested here) computed the rotation curve of the Triangulum galaxy (M33): inherent spatial curvature produced rotation curves of exactly the kind traditionally attributed to dark matter.

---

*End of digest. For the full development — including the mathematical background (Ch. II), all derivations, the numerical framework and its verification benchmarks (Ch. VII), future research directions (Ch. IX), and the complete reference list — see the [complete dissertation on GitHub](https://github.com/tgtenev/public-portfolio/blob/main/tenev2018-dissertation.md).*
