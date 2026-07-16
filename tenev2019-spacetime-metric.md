# The Spacetime Metric of a Spherically Symmetric Deformation of Space Derived from the Cosmic Fabric Model of Gravity

**Document Metadata**

| | |
|---|---|
| **Store** | public-portfolio |
| **Publication** | Int. J. Mod. Phys. D, vol. 28, no. 8, art. 1950096, 2019 |
| **DOI / URL** | https://doi.org/10.1142/S0218271819500962 |
| **Cite as** | T. G. Tenev and M. F. Horstemeyer, "The spacetime metric of a spherically symmetric deformation of space derived from the cosmic fabric model of gravity," Int. J. Mod. Phys. D, vol. 28, no. 8, art. 1950096, 2019. |
| **Converted from** | Local Overleaf-cloned LaTeX source (`spacetime-metric-v1`), commit `d51a3d9` |

---

**T G Tenev**
Mississippi State University, Starkville, MS 39759, USA
ticho@tenev.com

**M F Horstemeyer**
Mississippi State University, Starkville, MS 39759, USA
mfhorst@me.msstate.edu

## Abstract

The Cosmic Fabric model of gravity that was previously introduced by Tenev and Horstemeyer [1, 2] is further developed to provide a method for deriving the spacetime metric of the fabric's deformation due to a spherically symmetric gravitating body. We show that the derived metric is equivalent to the Schwarzschild metric up to a rescaling factor. From analyzing the membrane portion of the elastic energy due to an inclusion, we conclude that matter cannot be continuous at arbitrary sizes but must comprise discrete particles. Therefore, we show that the Cosmic Fabric model leads to results consistent with accepted theories at both continuum as well as sub-continuum length scales.

**Keywords:** modified gravity; cosmic fabric; Schwarzschild metric

**PACS numbers:** 04.50.Kd (Modified theories of gravity); 46.90.+s (Other topics in continuum mechanics of solids)

## 1. Introduction

The Cosmic Fabric model proposed by Tenev and Horstemeyer [1, 2], is a formal analogy interpreting space as a solid fabric with appropriately chosen material properties, and the field equations of General Relativity as its bending equations. According to this model, gravitating bodies behave as inclusions in the fabric. These inclusions are sources of volumetric strains that cause the fabric to expand laterally into the three ordinary spatial dimensions, and consequently, to bend transversely into an additional fourth spatial dimension (see Fig. 1). Along this extra dimension, the fabric possesses a small thickness which is on the order of Planck's length and by which the fabric can resist bending.

![A plate bending from a flat geometry (a) into a curved geometry (b) because of an inclusion that acts as a source of strain, as indicated by the concentric dashed lines and the diverging arrows. For the geometry of the plate to accommodate the prescribed strain, the plate must bend into the transverse dimension.](https://figures.tgtenev.com/tenev2019-spacetime-metric/fig-plate-bending.svg)

**Figure 1.** A plate bending from a flat geometry (a) into a curved geometry (b) because of an inclusion that acts as a source of strain, as indicated by the concentric dashed lines and the diverging arrows. For the geometry of the plate to accommodate the prescribed strain, the plate must bend into the transverse dimension. The figure has been reproduced from Tenev and Horstemeyer [1].

Whereas in [1] we considered the behavior of the cosmic fabric in the exterior of matter inclusions, herein we focus on the interaction between the cosmic fabric (physical space) and matter. As in [1] we assume nearly static conditions and weak gravity (small strains), in order to keep the math tractable. These conditions correspond to our ordinary experience of gravity and speeds on Earth and within our Solar System. The limitations of spherical symmetry, small strains, and nearly static bodies can be obviated in the future by solving numerically the pertinent differential equations.

How does the Cosmic Fabric Model (CFM) of gravity relate to General Relativity (GR)? Previously, we had shown the equivalence between these two for the case of weak gravity with nearly static fields in the exterior of mass densities [1], and herein we add the case of mass density interior. We expect that in the future, the equivalence can be further extended to strong gravity and non-static fields. Rigorously demonstrating so involves incorporating additional constitutive parameters of the cosmic fabric, such as those controlling strain rate, nonlinear elasticity, and plasticity. By adjusting these, CFM can be calibrated to provide equivalent solutions with GR. Currently, the CFM does not account for electromagnetic (EM) fields, but we are considering future extensions of CFM which will be able to incorporate EM phenomena. At the same time, we expect that there may be situations where CFM and GR diverge in their descriptions of physical phenomena. For example, one such situation is describing the interior of a black hole, for which CFM may need additional postulates, but which GR already handles. At the same time, CFM can naturally account for space having inherent structure, which is beyond the scope of classical GR. This is the notion that physical space has structure, such as intrinsic curvature that is uncaused by matter, which we have explored in a separate publication [3].

The contribution of this paper is twofold as follows:

- We extend the descriptive power of the Cosmic Fabric model [1, 2] to include the behavior of the cosmic fabric (physical space) in the interior of matter inclusions. Consequently, we show that the Schwarzschild metric [4], which is a solution of the Einstein Field Equations [5], can also be deduced from the governing equations of the cosmic fabric. To this end, we work with spherically symmetric inclusions to provide a simple illustration of the method, but the ideas described here are not fundamentally limited to spherical symmetry. Herein, the terms "Schwarzschild solution" or "Schwarzschild metric" refer generally to the solution of the Einstein Field Equations for any non-rotating finite spherical body of neutral charge and not just to a delta-like mass distribution or a black hole.
- We illustrate and validate the length-scale dependent nature of the Cosmic Fabric model as we demonstrate that it predicts the discrete nature of matter. In particular, the model shows that matter above a certain small size cannot be continuous but must be made of discrete parts. Subsequently, we validate this prediction from considering the size of common subatomic particles that make up matter.

Accomplishing the above two goals demonstrates that the Cosmic Fabric model [1] leads to results consistent with accepted theories at both continuum as well as sub-continuum length scales. At the continuum length scale, the model yields results consistent with General Relativity, while at the sub-continuum length scale the model relates to notions from particle physics. The term "continuum length scale" refers to characteristic lengths at which the physical quantities under consideration, such as the fabric strain and the relativistic energy density of inclusions, can be treated as continuous and differentiable fields. By contrast, the term "sub-continuum length scale" refers to much shorter characteristic lengths at which continuity is no longer a good approximation, but the discrete nature of the underlying structure becomes significant.

The remainder of this paper is organized as follows: In §2 we review concepts from solid mechanics and the Cosmic Fabric model [1] that are used throughout this paper. §3 introduces the mathematical tools used for handling the geometry of spherically symmetric hypersurfaces. In §4, we formulate the governing equations for the bending of the fabric and derive its spacetime metric (that is, the metric of its world volume), and in §5 we address the length-scale dependent nature of the membrane energy. The Discussion section (§6) compares the fabric's spacetime metric derived herein to the Schwarzschild metric [4]; it also compares the shape of the fabric's deformation to Flamm's paraboloid [6]. Finally, we summarize and conclude in §7.

## 2. Preliminaries

Below, we introduce the concepts from Solid Mechanics and the Cosmic Fabric model [1] that will be used through the remainder of this paper. The Cosmic Fabric model identifies physical space with the mid-hypersurface of a thin four-dimensional fabric [1], which bends within an enclosing *hyperspace*. The prefix "hyper" refers to an additional spatial dimension, so *hyperspace* is a four-dimensional (not necessarily physical) space, while *hypersurface* is a three-dimensional surface-like object immersed within this hyperspace.

In the following subsections we describe the specific way we assign coordinates to the material points of the fabric's mid-hypersurface, the fundamental deformation equations that use these coordinates, and the relevant postulates of the Cosmic Fabric Model.

### 2.1 Coordinate Assignments

We adopt the coordinate conventions as in [1], which we summarize here. The cosmic fabric (physical space) is immersed in a four-dimensional hyperspace within which it can deform. The enclosing hyperspace is flat and has been assigned Cartesian coordinates $y^K,\ K=1\ldots 4$. Another set of coordinates $x^i,\ i=1\ldots 3$ is painted on the fabric in the following manner: prior to deformation the $x^i$ coordinates are painted such that they coincide with the $y^i$ coordinates. As the fabric deforms (see Fig. 2), the $x^i$ coordinates remain attached to each material point and displace along with it. We call $y^K$ *hyperspatial coordinates* since they pertain to the enclosing hyperspace. By contrast, we call $x^i$ *material coordinates*, because they label material points on the fabric. These hyperspatial and material coordinates are analogous, respectively, to the concepts of spatial and material coordinates from solid mechanics. Note that what we consider "material coordinates" from the viewpoint of Solid Mechanics are also the coordinates of physical three-dimensional space from the viewpoint of General Relativity.

![Material coordinates x^i versus hyperspatial coordinates y^I, before (a) and after (b) deformation of a body. The material coordinates are attached to each material point and are carried along with the material as it deforms, while hyperspatial coordinates remain fixed during deformation.](https://figures.tgtenev.com/tenev2019-spacetime-metric/fig-material-ref-coords.svg)

**Figure 2.** Material coordinates $x^i$ versus hyperspatial coordinates $y^I$, before (a) and after (b) deformation of a body $\mathcal{B}$. The material coordinates are attached to each material point and are carried along with the material as it deforms, while hyperspatial coordinates remain fixed during deformation. In the diagram, two of the spatial dimensions have been suppressed for clarity. The figure has been reproduced here from Tenev and Horstemeyer [1].

For the remainder of the paper we adopt the following index convention: Upper-case Latin indexes run over the four dimensions of hyperspace $(1\ldots 4)$, lower-case Latin indexes run over the three ordinary spatial dimensions $(1\ldots 3)$, and Greek indexes run over the four spacetime dimensions $(0\ldots 3)$, where the $0^\text{th}$ dimension is time scaled by the speed of light $c$, so it has units of space.

### 2.2 Deformation Basics

The metric tensor $g_{ij}$ of the fabric's mid-hypersurface defines how coordinate differences relate to distances. The three-dimensional (3D) distance $dl$ between two nearby material points is given by,

$$
\begin{split}
dl^2 = g_{ij}dx^i dx^j,
\end{split}
\tag{2.1}
$$

where per Einstein's convention, summation over repeated indexes is implied. Prior to deformation, the distance between the same two material points is the following,

$$
\begin{split}
d\overline{l}^2 = \overline{g}_{ij}dx^i dx^j.
\end{split}
\tag{2.2}
$$

In Eq. (2.2) and for the remainder of the paper, a bar over the variable name of a quantity indicates that the quantity pertains to the undeformed configuration. For Cartesian coordinates, as adopted here, $\overline{g}_{ij} = \delta_{ij}$, where,

$$
\begin{split}
\delta_{ij} = \delta^i_j = \delta^{ij} =\begin{cases}
1,& \quad i = j \\
0,& \quad i \neq j
\end{cases}
\end{split}
\tag{2.3}
$$

In principle, there are multiple ways to assign coordinates. The specific coordinate assignment defined here attributes physical meaning to the metric tensor $g_{ij}$ as the Cauchy-Green deformation tensor from solid mechanics.

The small strain tensor $\varepsilon_{ij}$ quantifies the amount of relative length change during deformation, and is given by the following equation,

$$
\begin{split}
2\varepsilon_{ij}dx^i dx^j & = dl^2 - d\overline{l}^2 = (g_{ij} - \delta_{ij})dx^i dx^j \\
\therefore \varepsilon_{ij} &= \frac{1}{2}(g_{ij} - \delta_{ij}).
\end{split}
\tag{2.4}
$$

The 3D volumetric strain $\varepsilon^\text{3D}$ is defined as follows:

$$
\begin{split}
\varepsilon^\text{3D} &\equiv \varepsilon_{ij} \overline{g}^{ij} = \varepsilon_{ij} \delta^{ij} \\
& \therefore \varepsilon^\text{3D} = \frac{1}{2}\left(g_{11} + g_{22} + g_{33} - 3\right).
\end{split}
\tag{2.5}
$$

The volumetric strain is a scalar field that represents the fractional increase of the fabric's volume (hypersurface area). In other words, $dV^\text{3D}/d\overline{V}^\text{3D} = (1+\varepsilon^\text{3D})$, where $dV^\text{3D}$ and $d\overline{V}^\text{3D}$ are, respectively, the deformed and undeformed volume elements. The definition of strain per Eq. (2.4) and Eq. (2.5) only applies when $\varepsilon_{ij} \ll 1$, which is why the term "small strain," and only when $\overline{g}_{ij} = \delta_{ij}$. The superscript $^\text{3D}$ indicates that the superscripted quantity pertains to the ordinary three spatial dimensions.

Hooke's Law relates the strain $\varepsilon_{ij}$ in a material to the stress $\sigma^{ik}$ according to the following general formula:

$$
\begin{split}
\sigma^{kl} = \frac{Y}{1+\nu} \left(\frac{\nu}{1-2\nu} \overline{g}^{ij}\overline{g}^{kl} + \overline{g}^{ik}\overline{g}^{jl}\right)\varepsilon_{ij}
\end{split}
\tag{2.6}
$$

where $Y$ and $\nu$ are the Young's elastic modulus and Poisson's ratio, respectively. According to the Cosmic Fabric model [1], the Poisson ratio is unity ($\nu = 1$), and since we assume flat unstrained geometry, $\overline{g}^{ij} = \delta^{ij}$, so Eq. (2.6) reduces to the following simpler form:

$$
\begin{split}
\sigma^{kl} = \frac{Y}{2}\left(\varepsilon^{kl} - \varepsilon^\text{3D} \delta^{kl}\right).
\end{split}
\tag{2.7}
$$

### 2.3 The Cosmic Fabric Model

The Cosmic Fabric model [1] is based on the following postulates: i) physical space is identified with the mid-hypersurface of a four-dimensional hyperplate, which is thin in a fourth spatial dimension; ii) matter induces volumetric strain $\varepsilon^\text{3D}$ per,

$$
\begin{split}
\nabla^2 \varepsilon^\text{3D} = -\frac{1}{2}c^2 \kappa \rho,\quad \kappa \equiv \frac{8\pi G}{c^4}
\end{split}
\tag{2.8}
$$

where $c$ and $G$ are the speed of light and gravitational constant, respectively, $\rho$ is the matter-energy density, and $\kappa$ is known as the Einstein constant (in [1] this postulate was stated more generally as $\nabla^2 \varepsilon^\text{3D} \propto \kappa\rho$, while here we specify the exact constant of proportionality); and iii) time lapse slows down in proportion to the volumetric expansion, so that the time-time component of the spacetime metric tensor becomes the following (see Equations (2.7) and (2.10) in [1]):

$$
\begin{split}
g_{00} = -(1+\varepsilon^\text{3D})^{-2} = -\left(\frac{dV^\text{3D}}{d\overline{V}^\text{3D}}\right)^{-2} = -\frac{1}{\det[g_{ij}]}
\end{split}
\tag{2.9}
$$

The last equality in Eq. (2.9) uses the fact that $g_{ij}$ is the fabric's Cauchy-Green deformation tensor, and therefore its determinant is the square of the volumetric expansion. Furthermore, since we assume a nearly static condition (velocities that are much less than $c$), then the time-space components of the spacetime metric tensor are negligible so that the determinant of the spacetime metric can be approximated as follows,

$$
\begin{split}
\det{[g_{\mu\nu}]} \approx g_{00} \det{[g_{ij}]} = -1.
\end{split}
\tag{2.10}
$$

The following are some key results of the Cosmic Fabric model [1], which are important to this study: 1) The Poisson ratio $\nu$ of the fabric and its Young's modulus of elasticity $Y$ are the following,

$$
\begin{split}
\nu = 1; \quad Y = \frac{24}{ \kappa L^2} =  \frac{3c^4}{\pi G L^2},
\end{split}
\tag{2.11}
$$

where $L$ and $\kappa$ represent the thickness of the fabric, and Einstein's constant, respectively.
2) The bending energy $U_\text{B}$ only depends on the intrinsic spatial curvature scalar $R^\text{3D}$ and is given by,

$$
\begin{split}
U_\text{B} = -\frac{1}{2\kappa}R^\text{3D}.
\end{split}
\tag{2.12}
$$

Although the cosmic fabric is a thin hyperplate, for the purposes of this paper, it can be approximated with its mid-hypersurface, which is a three-dimensional object. Such an approximation is admissible, because the thickness of the fabric, which resists bending, is already accounted for in the computation of the bending elastic energy density $U_\text{B}$ in terms of the fabric's intrinsic curvature $R^\text{3D}$ per Eq. (2.12).

## 3. Geometry of Spherically Symmetric Deformation

We consider a spherically symmetric inclusion, which allows us to describe the resulting deformation as a radial stretch $r = r(\overline{R})$ followed by a transverse displacement $w = w(r)$ into the fourth hyperspace dimension (see Fig. 3). Let $r = (1+e)\overline{R}$, where $e = e(\overline{R})$ is the stretch factor by which material points initially at distance $\overline{R}$ from the origin are displaced away from it. The overall deformation is fully specified by the functions $e = e(\overline{R})$ and $w = w(r)$. Note that $\overline{R}$ represents the undeformed 3D distance of a point that has been deformed to be at distance $r$. Table 1 summarizes the common variables pertaining to the geometry of the hypersurface that are used in the remainder of this paper.

![Profile of a spherically symmetric hypersurface that has been deformed by bending into a fourth spatial dimension.](https://figures.tgtenev.com/tenev2019-spacetime-metric/fig-profile.svg)

**Figure 3.** Profile of a spherically symmetric hypersurface that has been deformed by bending into a fourth spatial dimension. The deformation is specified by two radial functions $r= r(\overline{R})$, which represent, respectively, an in-plane stretching, and a transverse displacement $w = w(r)$, applied after the stretching, where $\overline{R}$ is the distance from the origin prior to deformation. The coordinates $x^i$ (material coordinates), displace along with the hypersurface as it deforms, while the coordinates $y^K$ (hyperspatial coordinates) remain fixed with respect to the enclosing hyperspace.

In the context of a spherically symmetric inclusion causing the fabric to deform, we derive the following pertinent quantities in terms of $e$ and $w$: metric tensor, strain tensor, extrinsic curvature tensor, and intrinsic curvature scalar. The following subsections detail the derivation for each of these quantities.

**Table 1.** Common kinematic variables used to describe a spherically symmetric deformation of a hypersurface within four-dimensional hyperspace.

| Variable(s) | Description |
|---|---|
| $y^K,\  K =1\ldots 4$ | Hyperspatial coordinates of the embedding hyperspace (Cartesian) |
| $x^i,\  i =1\ldots 3$ | Material rectilinear coordinates |
| $t, \overline{R}, \theta, \varphi$ | Material polar coordinates. Note that $t$ represents time and $ct = x^0$. |
| $\overline{R} = \sqrt{\sum_{i=1}^{3} (x^i)^2}$ | Undeformed distance from the origin |
| $e = y^i/x^i - 1$ | Common stretch factor for all $i = 1\ldots 3$ |
| $r = (e+1)\overline{R}$ | Stretched distance from the origin prior to transverse displacement. |
| $w = w(r)$ | Transverse displacement following the radial stretch. Note that $y^4 = w$. |
| $u \equiv \frac{(w')^2}{2(1+(w')^2)}$ | Convenient variable substitution that happens to represent the portion of volumetric strain due to transverse displacement. |
| $\varepsilon^\text{3D}, \varepsilon_r, \varepsilon_\Omega$ | Volumetric strain, radial strain, and hoop strain |

### 3.1 Material (Spatial) Metric Tensor

The spatial metric $g_{ij}$ can be computed from the inner product of the three surface tangent vectors $\partial_i y^L$:

$$
\begin{split}
g_{ij} = \partial_i y^L \partial_j y^L
\end{split}
\tag{3.1}
$$

So, we begin by computing the first derivatives of the hyperspatial coordinates $y^{L}$. The second derivatives of $y^L$ are also useful for the computation of other geometric quantities, such as extrinsic and intrinsic curvature, which is why we calculate both types of derivatives below. Our strategy is to first determine the general expressions, and next, evaluate these at conveniently chosen coordinates to take advantage of the spherical symmetry.

Let $y^K$, $K = 1\ldots 4$ be the hyperspatial coordinates of a material point after deformation, and let $x^i$, $i = 1\ldots 3$, be its material coordinates. Then,

$$
\begin{split}
y^4 &= w\quad \text{(by construction)}
\\
\partial_i y^4 & = \frac{x^i}{\overline{R}} w'r'
\\
\partial_{ij} y^4 &= \frac{x^i x^j}{\overline{R}^2}(w''(r')^2 + w'r'') \\
& + \frac{1}{\overline{R}}w'r'\left[\delta^i_j - \frac{x^i x^j}{\overline{R}^2}\right]
\\
y^k &= x^k (1+e) \quad \text{(by construction)}
\\
\partial_i y^k &= \delta^k_i (1+e) + \frac{x^i x^k}{\overline{R}}e'
\\
\partial_{ij} y^k &= \frac{x^i x^j x^k}{\overline{R}^2} e''\\
+ & \left[\delta^k_i\frac{x^j}{\overline{R}} + \delta^k_j \frac{x^i}{\overline{R}} + \delta^i_j\frac{x^k}{\overline{R}} - \frac{x^i x^j x^k}{\overline{R}^3}\right]e'
\end{split}
\tag{3.2}
$$

where $e' \equiv de/d\overline{R}$, $r' \equiv dr/d\overline{R}$, and $w' \equiv dw/dr$. Notice that in contrast to $e'$ and $r'$, the shorthand derivative notation $w'$ represents differentiation with respect to the stretched distance $r$ and not the undeformed distance $\overline{R}$. The reason is that $w = w(r)$ is specified as a function of $r$ and not $\overline{R}$.

Because of the spherical symmetry, without loss of generality, we only need to know the values of the above derivatives at a point with conveniently chosen coordinates. Thus, let us choose,

$$
\begin{split}
x^1 = \overline{R}, \quad x^2 = x^3 = 0
\end{split}
\tag{3.3}
$$

where the first derivatives of $y^K$ are as follows:

$$
\begin{split}
[\partial_i y^K] = \left(
\begin{array}{cccc}
r' & 0 & 0 & w'r' \\
0 & (1+e) & 0 & 0 \\
0 & 0 & (1+e) & 0
\end{array}
\right)
\end{split}
\tag{3.4}
$$

Likewise, the second derivatives of $y^K$ at the chosen coordinates are as follows:

$$
\begin{split}
[\partial_{ij} y^1] &= \left(
\begin{array}{ccc}
r'' & 0 & 0 \\
0 & e' & 0 \\
0 & 0 & e'
\end{array}
\right)
\\
[\partial_{ij} y^2] &= \left(
\begin{array}{ccc}
0 & e' & 0 \\
e' & 0 & 0 \\
0 & 0 & 0
\end{array}
\right)
\quad
[\partial_{ij} y^3] = \left(
\begin{array}{ccc}
0 & 0 & e' \\
0 & 0 & 0 \\
e'& 0 & 0
\end{array}
\right)
\\
[\partial_{ij} y^4] &= \left(
\begin{array}{ccc}
w''(r')^2 + w'r'' & 0 & 0 \\
0 &  w'r'\overline{R}^{-1} & 0 \\
0 & 0 & w'r'\overline{R}^{-1}
\end{array}
\right)
\end{split}
\tag{3.5}
$$

Substituting the values for $\partial_i y^K$ from Eq. (3.4) into Eq. (3.1) for the chosen coordinates given in Eq. (3.3) yields the following result:

$$
\begin{split}
[g_{ij}] = \left(
\begin{array}{ccc}
(r')^2(1+(w')^2) & 0 & 0 \\
0 & (1 + e)^2 & 0 \\
0 & 0 & (1 + e)^2
\end{array}
\right).
\end{split}
\tag{3.6}
$$

### 3.2 Intrinsic Curvature

The intrinsic curvature scalar $R^\text{3D}$ can be computed from the extrinsic curvature tensor $b_{ij}$ according to the following identity from differential geometry,

$$
\begin{split}
R^\text{3D} = (b^i_i)^2 - b^j_k b^k_j
\end{split}
\tag{3.7}
$$

Furthermore, the extrinsic curvature can be computed from the derivatives of the tangent vectors $\partial_i y^L$ as follows,

$$
\begin{split}
b_{ij} = -\partial_{ij} y^K \hat{n}^K
\end{split}
\tag{3.8}
$$

where $\hat{n}^K$ is the surface unit normal vector, and the indexes have been raised using the deformed spatial metric $g_{ij}$. Because of the spherical symmetry, we only need to work out the values of $b_{ij}$ and $\hat{n}^K$ for the chosen coordinates in Eq. (3.3).

The normal vector $\hat{n}$ is given by the following equation:

$$
\begin{split}
\hat{n}^I = \frac{1}{|n^I|} n^I, \quad n^I = \epsilon^I_{JKL}\partial_1 y^J \partial_2 y^K \partial_3 y^L.
\end{split}
\tag{3.9}
$$

where $\epsilon^I_{JKL}$ is the permutation operator. Substituting Eq. (3.4) into Eq. (3.9) produces the following result,

$$
\begin{split}
\left(
\begin{array}{c}
\hat{n}^1 \\ \hat{n}^2 \\ \hat{n}^3 \\ \hat{n}^4
\end{array}
\right)
= \frac{1}{\sqrt{1+(w')^2}}
\left(
\begin{array}{c}
w' \\ 0 \\ 0 \\ -1
\end{array}
\right).
\end{split}
\tag{3.10}
$$

Evaluating Eq. (3.8) for the chosen coordinates (Eq. (3.3)) yields the extrinsic curvature $b_{ij}$ as follows,

$$
\begin{split}
b_{11} &= \frac{w''(r')^2}{\sqrt{1+(w')^2}} \\
b_{22} &= b_{33} = \frac{(1 + e)^2 w'}{r\sqrt{1+(w')^2}} \\
b_{ij} &= 0\quad \text{for} \quad i \neq j.
\end{split}
\tag{3.11}
$$

Therefore, the components $b_i^k = b_{ij} g^{jk}$ are as follows:

$$
\begin{split}
b^1_1 &= \frac{b_{11}}{g_{11}} = \frac{w''}{(1+(w')^2)^{3/2}} \\
b^2_2 &= \frac{b_{22}}{g_{22}} = \frac{w'}{r (1+(w')^2)^{1/2}} \\
b^3_3 &= \frac{b_{33}}{g_{33}} = \frac{w'}{r (1+(w')^2)^{1/2}} \\
b^i_j &= 0,\quad i \neq j.
\end{split}
\tag{3.12}
$$

The following variable substitution helps simplify the algebra in the remaining equations. Let $u$ be defined as follows:

$$
\begin{split}
u \equiv \frac{(w')^2}{2\left(1 + (w')^2\right)}
\end{split}
\tag{3.13}
$$

As we shall see later in Eq. (3.16), $u$ also happens to represent the portion of the volumetric stretch that is due to transverse displacement into the fourth spatial dimension. In terms of $u$, the displacement $w$ and its derivatives are as follows:

$$
\begin{split}
(w')^2 &= 2u(1-2u)^{-1} \\
(w')^2 + 1 &= (1-2u)^{-1} \\
w' &= (2u)^{1/2}(1-2u)^{-1/2} \\
w'' &= (2u)^{-1/2}(1-2u)^{-3/2}
\end{split}
\tag{3.14}
$$

When the above identities are substituted into Eq. (3.12), we obtain the following result for the extrinsic curvature:

$$
\begin{split}
[b^i_j] = \left(
\begin{array}{ccc}
u'/\sqrt{2u} & 0 & 0 \\
0 & {\sqrt{2u}}/{r} & \\
0 & 0 & {\sqrt{2u}}/{r}
\end{array}
\right)
\end{split}
\tag{3.15}
$$

Substituting the result from Eq. (3.15) into Eq. (3.7) and taking into consideration the identity $ru' + u = (ru)'$, produces the following result for the intrinsic curvature scalar.

$$
\begin{split}
R^\text{3D} =  4 \frac{(ru)'}{r^2}, \quad u \equiv \frac{(w')^2}{2(1+(w')^2)}
\end{split}
\tag{3.16}
$$

Notice that $R^\text{3D}$ only depends on the transverse displacement $w$ and not on the horizontal stretch $e$. This is expected, because according to continuum mechanics theory, compatible deformations do not affect the intrinsic curvature. A "compatible" deformation is one that does not introduce overlaps or tears in the material. Therefore, any purely 3D deformation will not contribute to the 3D intrinsic curvature.

## 4. Spacetime Metric due to Spherically Symmetric Inclusion

In this section we formulate the equations that govern the interaction between a spherically symmetric inclusion and the fabric, and we calculate the resulting spacetime metric. We work in the limit of nearly static bodies and small strains to determine the fabric deformation caused by an inclusion. The result, expressed in terms of the metric tensor that characterizes the deformation, represents the spatial components of the fabric's spacetime metric. The temporal component can be determined from Eq. (2.9), which is based on the Time Lapse Postulate of the Cosmic Fabric Model [1]. The following paragraphs detail the derivation.

### 4.1 Formulation of the Governing Equations

The governing equations are formulated in terms of the radial stretch factor $e(r) = r/\overline{R} - 1$ and the transverse displacement $w(r)$ based on the following constraints: 1) the bending energy density must balance the relativistic energy density of the inclusion, 2) inclusions are a source of strain, and 3) the total membrane energy must vanish. As discussed in detail in [1], the term "bending energy" means the portion of the elastic energy due to bending whereby the mid-hypersurface of the fabric remains unstrained and the hypersurfaces on each side of it are being, respectively, stretched or compressed. By contrast, the term "membrane energy" is the elastic energy attributed to the stretching of the mid-hypersurface.

The above constraints are motivated as follows: Consider the Fabric's action $\mathcal{S} = \int \mathcal{L}_\text{F} \sqrt{|g|} dx^4$ where $\mathcal{L}_\text{F}$ is the Lagrangian of the fabric together with the inclusion; $g \equiv \det [g_{\mu\nu}]$ is the determinant of the spacetime metric; and the integral is taken over a sufficiently large volume of spacetime such that the integral converges. According to the Principle of Least Action, physical systems progress along a trajectory that extremizes the action (the action is either minimized or maximized). For a nearly static situation the kinetic components of $\mathcal{L}_\text{F}$ can be ignored, so only the contributions from the fabric's elastic energy and the body's relativistic energy need to be considered. Thus, $\mathcal{L}_\text{F} = -(U_\text{M} + U_\text{B} + c^2 \rho)$. Furthermore, per Eq. (2.10) the determinant $|g| \approx 1$. Therefore, since the total energy integrated over all of three-dimensional space should be non-negative, the action $\mathcal{S}$ would reach an extremum if the deformation functions $e$ and $w$ were such that the total elastic energy $W$, defined as follows, vanished:

$$
\begin{split}
W \equiv \int_\text{all space} (U_\text{M} + U_\text{B} + c^2 \rho) dx^3 = 0
\end{split}
\tag{4.1}
$$

As we show in detail in §5, the membrane energy component of the above integral is length scale dependent, because it depends on the fabric's thickness $L$, which is a length scale parameter, through the elastic modulus $Y$ per Eq. (2.11). Consequently, $U_\text{M}$ varies disproportionately with the mass of the gravitating body unlike the other two components which are length-scale independent. For example, for large bodies, $U_\text{M}$ becomes the dominant term in Eq. (4.1). Therefore, in order for $W$ from Eq. (4.1) to vanish for inclusion of any mass, it follows that the total membrane energy $W_\text{M}$, defined per Eq. (4.2), must vanish independently from the other two components, as follows:

$$
\begin{split}
W_\text{M} \equiv \int_\text{all space} U_\text{M} dx^3 = 0
\end{split}
\tag{4.2}
$$

From the remainder of the integral, $\int_\text{all space} (U_\text{B} + c^2\rho) dx^3 = 0$, we can deduce the following ostensibly stronger requirement:

$$
\begin{split}
U_\text{B} + c^2\rho = 0
\end{split}
\tag{4.3}
$$

To prove the above, we first observe that outside of inclusions, where $\rho = 0$, the bending energy $U_\text{B}$ vanishes, which follows from the results in [1], where we showed that the Cosmic Fabric Model produces the Einstein Field Equations for free space, which when contracted with the metric indicate that the Ricci scalar must vanish in free space: $R = 0$. We also showed [1] that in free space, $R^\text{3D} = R = 0$ per Eq. (2.23) and Eq. (2.12) of [1], which combined with Eq. (2.12) herein yields $U_\text{B} = 0$ outside of inclusions. Consequently, $\int_\text{all space} (U_\text{B} + c^2\rho) dx^3 = \int_\mathcal{B}  (U_\text{B} + c^2\rho) dx^3$ = 0, where $\mathcal{B}$ is the region of space occupied by the mass density $\rho$. In the weak field regime, as assumed herein, we expect that the effects of mass densities are linearly superimposable. Therefore, the contribution of any subregion $\mathcal{B}' \subset \mathcal{B}$ to the bending energy field must be the same as if $\mathcal{B}'$ were a free standing body apart from the rest of $\mathcal{B}$. In other words, the above integral must vanish for any arbitrary region $\mathcal{B}' \subset \mathcal{B}$, which can only be the case if the integrand vanished identically.

In addition, as Tenev and Horstemeyer [1] had previously postulated, the inclusion is a source of strain such that the Laplacian of the volumetric strain is proportional to the inclusion's relativistic energy density. Here, we narrow the postulate by specifying the constant of proportionality:

$$
\begin{split}
\nabla^2 \varepsilon^\text{3D} = -\frac{1}{2}c^2 \kappa \rho.
\end{split}
\tag{4.4}
$$

Equations (4.3) and (4.4) represent the first and second constraints respectively, while Eq. (4.2) represents the third constraint. The first two constraints are sufficient to produce a solution for the fabric's spacetime metric, which is the focus of this section. We address the third constraint in §5 where we examine the conditions under which the total membrane energy vanishes, and we show that it does indeed vanish for the case of matter made up of small particles, which is true for all known matter.

It is convenient to work with the geometric equivalents of the parameters describing the gravitating body. For example, rather than working with the mass of the body $M$, we use its Schwarzschild radius $r_s = 2GM/c^2$. Also, in the weak field regime, as assumed here, the relativistic energy density of the gravitating body is approximately $\rho = M/[(4/3)\pi r_g^3]$, where $r_g$ is the radius of the gravitating body. Consequently, we derive the following substitution,

$$
\begin{split}
\kappa c^2 \rho = \frac{3r_s}{r_g^3} \equiv \frac{3}{r_0^2}; \quad r_0 \equiv \sqrt{\frac{r_g^3}{r_s}}
\end{split}
\tag{4.5}
$$

where $r_0$, as defined above, is a geometric quantity characterizing the density of the inclusion. Finally, the result from the Cosmic Fabric model [1] expressed in Eq. (2.12) provides a geometric interpretation for the bending energy of the Fabric due to the gravitating body acting as an inclusion. Table 2 summarizes the geometric parameters used to describe a gravitating body.

**Table 2.** Geometric parameters used to describe a spherically symmetric gravitating body of mass $M$. In the following equations $G$ and $c$ are the gravitational constant and the speed of light, respectively.

| Parameter | Description |
|---|---|
| $r_g$ | Radius of the gravitating body after the initial stretch but before the transverse displacement. Note that this is not the actual geometric radius which is slightly larger due to the transverse displacement |
| $\overline{r}_g$ | Undeformed radius of the gravitating body. Since we work in the small strains (weak gravity) regime $\overline{r}_g \approx r_g$. |
| $r_s \equiv {2 G M}/{c^2}$ | Schwarzschild radius, which is the geometric equivalent of the body's mass. |
| $r_0 \equiv \sqrt{r_g^3/r_s}$ | Geometric equivalent of the body's density $\rho$. Specifically, $\kappa c^2\rho = 3/r_0^2$, where $\kappa \equiv 8 \pi G/c^4$ is the Einstein constant. |
| $R^\text{3D} = -2\kappa U_\text{B}$ | The intrinsic curvature scalar of the cosmic fabric is the geometric equivalent of the bending elastic energy caused by the matter inclusion. |

In terms of these geometric parameters Eq. (4.3) and Eq. (4.4) are expressed, respectively, as follows:

$$
\begin{split}
R^\text{3D} = \frac{6}{r_0^2}
\end{split}
\tag{4.6}
$$

$$
\begin{split}
\nabla^2 \varepsilon^\text{3D} = -\frac{3}{2 r_0^2}
\end{split}
\tag{4.7}
$$

The above two govern the bending of the fabric due to a spherically symmetric inclusion.

The following sections detail the solutions for these equations. We first solve for the transverse displacement $w = w(r)$ where $r \equiv (1+e)\overline{R}$ and the volumetric strain $\varepsilon^\text{3D} = \varepsilon^\text{3D}(\overline{R})$. The results are used to solve for the stretch factor $e = e(\overline{R})$. Finally, we derive the solution for the spacetime metric.

### 4.2 Transverse Displacement

We solve for the transverse displacement, $w$, by combining Eq. (4.6) with the result from Eq. (3.16), which yields the following equation,

$$
\begin{split}
(ru)' = \frac{3r^2}{2r_0^2}, \quad u \equiv {(w')^2}/{2(1+(w')^2)}
\end{split}
\tag{4.8}
$$

Let us consider separately the interior ($0 \le r < r_g$), versus the exterior region ($r_g \le r$) of the gravitating body. Within the interior, the mass density has a finite value $\rho$ and a finite geometric equivalent $r_0$, whereas in the exterior, $\rho = 0$ and $r_0 = \infty$. Let $u_\text{int}$ and $u_\text{ext}$ be the interior and exterior solutions, respectively. Eq. (4.8) implies that,

$$
\begin{split}
u_\text{int} = \frac{r^2}{2 r_0^2} + \frac{C_1}{r}; \quad u_\text{ext} = \frac{C_2}{r}
\end{split}
\tag{4.9}
$$

where $C_1$ and $C_2$ are constants of integration. The constant $C_1$ must vanish to avoid a singularity at $r = 0$. Furthermore, for $u(r)$ to be continuous we require that $u_\text{int}(r_g) = u_\text{ext}(r_g)$ from where we conclude that $C_2 = r_s/2$. Finally, we arrive at the following solutions for $u$ and $w$:

$$
\begin{split}
u_\text{int} = \frac{r^2}{2r_0^2}; \quad u_\text{ext} = \frac{r_s}{2r}
\end{split}
\tag{4.10}
$$

$$
\begin{split}
w_\text{int} &= (2r_s + r_g)\sqrt{r_g/r_s - 1} - \sqrt{r_0^2 - r^2} + C \\
w_\text{ext} &= 2\sqrt{r_s(r - r_s)} + C
\end{split}
\tag{4.11}
$$

where $C$ is a constant of integration that represents an arbitrary rigid translation of the fabric, and $r = (1+e)\overline{R}$ is the stretched distance from the center of the gravitating body.

### 4.3 Volumetric Strain

Below we solve for the volumetric strain $\varepsilon^\text{3D} = \varepsilon^\text{3D}(\overline{R})$, from which we can determine the radial stretch factor $e = e(\overline{R})$.

Let $f(\overline{R}) \equiv d\varepsilon^\text{3D}(\overline{R})/d\overline{R}$. By successive differentiation we determine the following,

$$
\begin{split}
\frac{\partial}{\partial x^i} \varepsilon^\text{3D} &= f \frac{x^i}{\overline{R}} \\
\frac{\partial^2}{(\partial x^i)^2} \varepsilon^\text{3D}  &= f'\frac{(x^i)^2}{\overline{R}^2} + f\frac{1}{\overline{R}} - f\frac{(x^i)^2}{\overline{R}^3} \\
\therefore \nabla^2 \varepsilon^\text{3D} & \equiv \sum_{i=0}^3 \frac{\partial^2}{(\partial x^i)^2} \varepsilon^\text{3D} \\
& = f' + 2f\frac{1}{\overline{R}} = \frac{(\overline{R}^2 f)'}{\overline{R}^2}.
\end{split}
\tag{4.12}
$$

When the above identity is substituted into Eq. (4.7) the result is as follows:

$$
\begin{split}
\frac{(\overline{R}^2 f)'}{\overline{R}^2} &= -\frac{3}{2}\frac{1}{r_0^2} \\
f &= -\frac{1}{2}\frac{\overline{R}}{r_0^2} - \frac{C_3}{\overline{R}^2} \\
\varepsilon^\text{3D} &= C_4 - \frac{1}{4}\frac{\overline{R}^2}{r_0^2} + \frac{C_3}{\overline{R}},
\end{split}
\tag{4.13}
$$

where $C_3$ and $C_4$ are constants of integration. Let $\varepsilon^\text{3D}_\text{int}$ and $\varepsilon^\text{3D}_\text{ext}$ represent the interior and exterior solutions, respectively. For the interior solution, $0\le \overline{R} \le \overline{r}_g$, we determine that $C_3 = 0$, or else $\varepsilon^\text{3D}_\text{int}$ diverges as $\overline{R} \rightarrow 0$. For the exterior case, $r_0 = \infty$, so $\varepsilon^\text{3D}_\text{ext} = C_4 + C_3/r$, but $C_4$ must vanish, for $\varepsilon^\text{3D}_\text{ext}$ to vanish at infinity. Thus, we conclude so far the following,

$$
\begin{split}
\varepsilon^\text{3D}_\text{int}  = C_4 - \frac{1}{4}\frac{r^2}{r_0^2}; \quad
\varepsilon^\text{3D}_\text{ext}  = \frac{C_3}{r}.
\end{split}
\tag{4.14}
$$

For it to be physically admissible, $\varepsilon^\text{3D}$ and its first derivative must be continuous throughout three-dimensional space. Therefore,

$$
\begin{split}
&\varepsilon^\text{3D}_\text{int}(r_g) = \varepsilon^\text{3D}_\text{ext}(r_g); \quad
\left.\frac{d }{d\overline{R}}\varepsilon^\text{3D}_\text{int}\right|_{r = r_g} = \left.\frac{d }{d\overline{R}}\varepsilon^\text{3D}_\text{ext}\right|_{r = r_g} \\
&\therefore C_3 = \frac{r_s}{2}; \quad C_4 =  \frac{3r_g^2}{4r_0^2},
\end{split}
\tag{4.15}
$$

which finally produces the following result:

$$
\begin{split}
\varepsilon^\text{3D}_\text{int} = \frac{3}{4}\frac{\overline{R}_g^2}{r_0^2} - \frac{1}{4}\frac{\overline{R}^2}{r_0^2}; \quad
\varepsilon^\text{3D}_\text{ext} = \frac{1}{2}\frac{r_s}{\overline{R}}
\end{split}
\tag{4.16}
$$

### 4.4 Radial Stretch

We solve for the radial stretch $e(\overline{R})$ by relating it to the volumetric stretch $\varepsilon^\text{3D}$ and the transverse displacement $w$. To simplify the math, we will use linearized approximations based on the fact that under the small strains regime adopted here the quantities $e$ and $u \equiv {(w')^2}/{(2(1+(w')^2))}$ are all much less than 1.

From the definition of volumetric strain in Eq. (2.5) and the result for the metric from Eq. (3.6) we derive the following:

$$
\begin{split}
2\varepsilon^\text{3D} &= (r')^2 (1+(w')^2) + 2(1+e)^2 - 3 \\
& = (e'\overline{R} + e + 1)^2 (1-2u)^{-1} + 2(1+e)^2 - 3 \\
& \approx (2e'\overline{R} + 2e + 1)(1 + 2u) + 2(1+ 2e) - 3 \\
\varepsilon^\text{3D} & = e'\overline{R} + 3e + u = \frac{(e\overline{R}^3)'}{\overline{R}^2} + u
\end{split}
\tag{4.17}
$$

Therefore,

$$
\begin{split}
(e\overline{R}^3)' = \overline{R}^2 \varepsilon^\text{3D} - \overline{R}^2 u.
\end{split}
\tag{4.18}
$$

After substituting the result for $\varepsilon^\text{3D}$ and $u$ from Eq. (4.16) and Eq. (4.10), respectively, into Eq. (4.18) and approximating $\overline{R}_g \approx r_g$, we obtain the following general solution:

$$
\begin{split}
\frac{(e_\text{int}\overline{R}^3)'}{\overline{R}^2} &= \frac{3r_g^2 - \overline{R}^2}{4r_0^2} - \frac{\overline{R}^2}{2r_0^2} = \frac{3(r_g^2 - \overline{R}^2)}{4r_0^2} \\
%
\therefore & e_\text{int} = \frac{1}{4}\frac{r_g^2}{r_0^2} - \frac{3}{20}\frac{\overline{R}^2}{r_0^2} + \frac{C_5}{\overline{R}^3} \\
%
\frac{(e_\text{ext}\overline{R}^3)'}{\overline{R}^2} &= \varepsilon^\text{3D}_\text{ext} - u
= \frac{1}{2}\frac{r_s}{\overline{R}} - \frac{1}{2}\frac{r_s}{\overline{R}} = 0 \\
&\therefore e_\text{ext} = \frac{C_6}{\overline{R}^3},
\end{split}
\tag{4.19}
$$

where $C_5$ and $C_6$ are constants of integration. The constant $C_5$ must vanish to avoid the singularity at $r = 0$. The constant $C_6$ can be determined by requiring that $e_\text{int}(r_g) = e_\text{ext}(r_g)$. Consequently, we arrive at the following solution for $e(\overline{R})$:

$$
\begin{split}
e_\text{int} = \frac{1}{4}\frac{r_g^2}{r_0^2}- \frac{3}{20}\frac{\overline{R}^2}{r_0^2},\quad
e_\text{ext} = \frac{1}{10}\frac{r_g^5}{r_0^2 \overline{R}^3} = \frac{1}{10}\frac{r_s r_g^2}{\overline{R}^3}
\end{split}
\tag{4.20}
$$

### 4.5 Metric

We are now ready to derive the spacetime metric of the deformed fabric in terms of the geometric characteristics of the inclusion that is the source of the deformation. These are: the inclusion's Schwarzschild radius $r_s$, its spatial radius $r_g$, and the geometric equivalent of its density $r_0$.

Because of the spherical symmetry, it is useful to derive the metric using the polar material coordinates $(t, \overline{R}, \theta, \varphi)$ corresponding, respectively, to time, undeformed radius, altitude angle, and azimuth angle. In terms of these coordinates, the spacetime line element $ds$ is given by,

$$
\begin{split}
ds = g_{tt} c^2 dt^2 + g_{\overline{R}\overline{R}} d\overline{R}^2 + g_{\Omega\Omega}\overline{R}^2 d\Omega^2
\end{split}
\tag{4.21}
$$

where $d\Omega^2 \equiv d\theta^2 + \cos^2 \theta d\varphi^2$, and where $g_{tt}$, $g_{\overline{R}\overline{R}}$, and $g_{\Omega\Omega}$ are the polar metric coefficients.

For the chosen rectilinear coordinates in Eq. (3.3), we can identify the spatial polar metric coefficients with the rectilinear coefficients $g_{ij}$ as follows,

$$
\begin{split}
g_{\overline{R}\overline{R}} &= g_{11} = (r')^2 (1+(w')^2) \\
& = (1 + e + e'\overline{R})^2(1-2u)^{-1} \\
& \approx 1 + 2(e + e'\overline{R} + u) \\
g_{\Omega\Omega}  &= g_{22} = g_{33} = (1+e)^2 \approx 1 + 2e
\end{split}
\tag{4.22}
$$

In the above derivation, we have used the result for $g_{ij}$ from Eq. (3.6) into which we have substituted $r = (1+e)\overline{R}$, and expressed $(1+(w')^2)$ in terms of $u$ per Eq. (3.14). Due to the spherical symmetry the above expressions only depend on the radial functions $e$ and $u$. Therefore, they apply for all points in space and not just for the specially chosen coordinates.

We also identify the time-time metric coefficient $g_{tt}$ with $g_{00}$. The latter can be determined from the Time Lapse Postulate of the Cosmic Fabric model [1] (see Eq. (2.9)) as follows,

$$
\begin{split}
g_{tt} = g_{00} = -(1+\varepsilon^\text{3D})^{-2} \approx -(1 - 2\varepsilon^\text{3D});
\end{split}
\tag{4.23}
$$

Finally, after substituting the results for $u$, $\varepsilon^\text{3D}$, and $e$ from Equations (4.10), (4.16), and (4.20) into Equations (4.22) and (4.23), we arrive at the following result for the spacetime element $ds$:

$$
\begin{split}
ds^2_\text{int} &= -\left(1 - \frac{3r_g^2}{2r_0^2} + \frac{\overline{R}^2}{2r_0^2}\right) c^2 dt^2 \\
& + \left(1 + \frac{r_g^2}{2r_0^2} + \frac{\overline{R}^2}{10r_0^2}\right) d\overline{R}^2 \\
& + \left(1 + \frac{r_g^2}{2r_0^2} - \frac{3\overline{R}^2}{10r_0^2}\right) \overline{R}^2 d\Omega^2,
\quad 0 \le \overline{R} < r_g
\\
%
ds^2_\text{ext} &= -\left(1-\frac{r_s}{\overline{R}}\right) c^2 dt^2 \\
& + \left(1+\frac{r_s}{\overline{R}} - \frac{2 r_s r_g^2}{5\overline{R}^3}\right) d\overline{R}^2 \\
& + \left(1+\frac{r_s r_g^2}{5\overline{R}^3}\right) \overline{R}^2 d\Omega^2, \quad r_g \le r
\end{split}
\tag{4.24}
$$

where $ds_\text{int}$ and $ds_\text{ext}$ represent, respectively, the interior and exterior solutions for the metric. In §6, we compare the result from Eq. (4.24) to the well known form of the Schwarzschild metric and show that they are equivalent up to a coordinate rescaling.

![Profile of the volumetric strain, radial strain, and hoop strain at distance from the center of a gravitating body.](https://figures.tgtenev.com/tenev2019-spacetime-metric/fig-strain.svg)

**Figure 4.** Profile of the volumetric strain $\varepsilon^\text{3D}$, radial strain $\varepsilon_r$, and hoop strain $\varepsilon_\Omega$ at distance $\overline{R}$ from the center of a gravitating body with Schwarzschild radius $r_s$ and geometric radius $r_g$. Note that $\varepsilon^\text{3D} = \varepsilon_r + 2\varepsilon_\Omega$.

From a solid mechanics perspective, the three metric coefficients in Eq. (4.24) can be expressed in terms of the volumetric strain $\varepsilon^\text{3D}$, radial strain $\varepsilon_r$, and hoop strain $\varepsilon_\Omega$ of the fabric as follows:

$$
\begin{split}
ds^2 =& -\left(1 - 2\varepsilon^\text{3D}\right)c^2dt^2
+ \left(1 + 2\varepsilon_r\right)d\overline{R}^2 \\
&+ \left(1 + 2\varepsilon_\Omega\right)d\overline{R}^2 d\Omega^2
\end{split}
\tag{4.25}
$$

Fig. 4 shows the profiles of these strains as a function of the undeformed radius $\overline{R}$. Note that $\varepsilon^\text{3D} = \varepsilon_r + 2\varepsilon_\Omega$, as one would expect, because a single radial and two hoop orientations form an orthogonal triad at any point along a spherical shell. Furthermore, the reason why the radial and hoop strains vanish at different rates ($\propto \overline{R}^{-1}$ versus $\propto \overline{R}^{-3}$, respectively) is because the radial strain depends on both the transverse displacement $w$ as well as the radial displacement ($\overline{R}$ displacing into $r$), whereas the hoop strain only depends on the radial displacement (see Fig. 3).

## 5. Membrane Energy and the Discrete Nature of Matter

The fabric's elastic energy density $U$ can be decomposed into membrane and bending terms, $U_\text{M}$ and $U_\text{B}$, respectively, such that $U = U_\text{M} + U_\text{B}$. §4 considered the bending term, while here we focus on the membrane term. In [1] we had shown that $U_\text{M}$ vanishes in the absence of in-plane stretching. However, the solution for the spacetime metric we derived in Eq. (4.24) includes in-plane stretch, which ostensibly leads to non-vanishing membrane energy density. Nevertheless, we can show that the fabric's membrane energy due to the inclusion of a gravitating body vanishes under the following conditions: 1) the body is made up of discrete particles, as opposed to being perfectly continuous, which is the case for all known matter, and 2) each individual particle induces a certain type of asymmetric deformation as discussed in §5.2. So, while the body may appear continuous and spherically symmetric at the continuum length scales, the spherical symmetry does not hold at substructure length scale. The fact that the Cosmic Fabric model requires for matter to be discrete is significant and is a consequence of the length-scale dependence built into the model via the fabric's thickness $L$.

We arrive at the above conclusion by reasoning progressively as follows: First, we consider the total membrane energy of the fabric due to the inclusion of a perfectly continuous spherically symmetric body. Next, we analyze how the membrane energy is different in a spherically symmetric body that has discontinuous substructure.

### 5.1 Total Membrane Energy of a Homogeneous Spherically Symmetric Body

The total membrane energy $W_\text{M} = W_\text{M}(\overline{R})$ within a ball of physical space of radius $\overline{R}$ concentric with the gravitating body is, by definition, the following:

$$
\begin{split}
W_\text{M}(\overline{R}) = 4\pi \int_{0}^{\overline{R}} U_\text{M}(\zeta) \zeta^2 d\zeta.
\end{split}
\tag{5.1}
$$

where $\zeta$ is the variable of integration representing undeformed distance from the origin. The membrane energy density $U_\text{M}$ is the elastic energy density of the fabric's mid-hypersurface given by $U_\text{M} = \sigma^{ij}\varepsilon_{ij}/2$, which by application of Hooke's Law from Eq. (2.7) is the following:

$$
\begin{split}
U_\text{M} = \frac{Y}{4}\left(\varepsilon^k_j\varepsilon^j_k - \varepsilon^i_i \varepsilon^k_k\right),
\end{split}
\tag{5.2}
$$

Due to the spherical symmetry, without loss of generality, we can evaluate the above result for the choice of coordinate values from Eq. (3.3). In the context of Hooke's Law, the strain tensor $\varepsilon_{ij}$ is defined with respect to the basis of the undeformed configuration, which is the ordinary Cartesian basis. Since the undeformed metric is $\overline{g}^{ij} = \delta^{ij}$, it follows that $\varepsilon^i_j = \varepsilon_{ij}$ and from the definition of small strain in Eq. (2.4) and the result in Eq. (3.6) we derive the following:

$$
\begin{split}
\varepsilon^1_1 &= (g_{11} - 1)/2 \\
& = \left[(1+e+e'\overline{R})^2 (1-2u)^{-1} - 1\right]/2 \\
& \approx e + e'\overline{R} + u \\
\varepsilon^2_2 &= (g_{22} - 1)/2 = [(1+e)^2-1]/2 \approx e \\
\varepsilon^3_3 &= (g_{33} - 1)/2 = [(1+e)^2-1]/2 \approx e
\end{split}
\tag{5.3}
$$

Substituting Eq. (5.3) into Eq. (5.2) leads to the following result for the membrane energy density:

$$
\begin{split}
U_\text{M}(\overline{R}) &= -\frac{Y}{2}\left(3e^2+2ee'\overline{R} + 2ue\right) \\
&= -\frac{Y}{2\overline{R}^2}\left[(e^2 \overline{R}^3)' + 2ue\overline{R}^2 \right]
\end{split}
\tag{5.4}
$$

We can now substitute the solutions for $u$ and $e$ from Eq. (4.10) and Eq. (4.20), respectively, into Eq. (5.4), and integrate the resulting expression for $U_\text{M}$ per Eq. (5.1) to produce the following result for $W_\text{M}$:

$$
\begin{split}
W_\text{M} &=  -\frac{3c^4 r_s^2 r_g}{50 G L^2} \times \\
&\begin{cases}
\left(\frac{5}{2} - \frac{3}{2}\xi^2\right)^2\xi^3 + 5\left(1 -\frac{3}{7}\xi^2\right)\xi^5,\ & 0 \le \xi < 1 \\
\xi^{-3} - 10\xi^{-1} + \frac{90}{7},\ & 1\le \xi
\end{cases},
\end{split}
\tag{5.5}
$$

where $\xi \equiv \overline{R}/r_g$. Also, we have used the result for $Y$ from Eq. (2.11) and we have taken the approximation $r \approx \overline{R}$, which holds under the small strain regime assumed here.

![The total membrane energy of the cosmic fabric due to a perfectly continuous gravitating body as a function of the undeformed distance from its center.](https://figures.tgtenev.com/tenev2019-spacetime-metric/fig-total-membrane-energy.svg)

**Figure 5.** The total membrane energy $W_\text{M}$ of the cosmic fabric due to a perfectly continuous (lacking substructure) gravitating body of radius $r_g$ and a Schwarzschild radius $r_s$ as a function of the undeformed distance $\overline{R}$.

Fig. 5 shows the changing membrane energy $W_\text{M}$ as a function of the undeformed distance $\overline{R}$ from the center of the gravitating body. The calculated total energy is negative and converges at infinity to the following value:

$$
\begin{split}
\max |W_\text{M}| = \lim_{\overline{R} \to \infty} |W_\text{M}| = \frac{27 c^4 r_s^2 r_g}{35 G L^2}
\end{split}
\tag{5.6}
$$

The fact that $W_\text{M}$ saturates at infinity was expected, because the effect of a gravitating body on the total energy of the fabric should become negligible at sufficiently large distances. However, the result in Eq. (5.6), which is illustrated in Fig. 5, also reveals two potential problems: 1) the total membrane energy $W_\text{M}$ is length-scale dependent and can become disproportionately large for more massive bodies relative to less massive ones, and 2) the total membrane energy is negative. As demonstrated below, both of these issues are resolved once we allow for the existence of substructure within the gravitating body instead of the body being perfectly continuous.

Eq. (5.6) shows that the amplitude of the fabric's membrane energy due to the inclusion of a body grows as the square of the body's Schwarzschild radius $r_s$, whereas the body's relativistic energy grows only linearly with $r_s$. Consequently, very massive bodies will result in membrane energies with disproportionately greater magnitudes compared to less massive bodies. This situation suggests that there must be a limit to the massiveness of a perfectly continuous body, or equivalently, to the size of its Schwarzschild radius. The fabric's thickness $L$, which figures into the equation for $\max|W_\text{M}|$ serves as a length-scale parameter that determines an upper bound for $r_s$, so that a spherically symmetric body with $r_s$ that is larger than said upper bound cannot be itself perfectly continuous but must be composed of smaller particles. To quantify this limit, we require that the effect of a gravitating body in terms of the total membrane energy $W_\text{M}$ should be comparable or less to the body's own relativistic energy, which in terms of the body's Schwarzschild radius $r_s$ is $r_s c^4 / (2 G)$. In other words, we assert that,

$$
\begin{split}
\frac{r_s c^4}{2G} &\gtrsim \max|W_\text{M}| = \frac{27 c^4 r_s^2 r_g}{35 G L^2} \\
&\therefore r_s r_g \lesssim \frac{35}{54}L^2
\end{split}
\tag{5.7}
$$

Since also $r_s \le r_g$, the maximum possible mass is achieved for a body such that $r_s = r_g$. In that case,

$$
\begin{split}
\max(r_s) \le \sqrt{\frac{35}{54}}L.
\end{split}
\tag{5.8}
$$

In [1], we concluded that the fabric's thickness, $L$, must be comparable to Planck's length $l_p = 1.616229\times 10^{-35}\text{m}$. The rationale is two fold: 1) the fabric must behave as an essentially three-dimensional object at ordinary length scales, so its thickness must be small, and 2) $L$ specifies an extremely small length scale parameter at which scale the behavior of the physical world differs significantly from our ordinary (macroscale) experience. Herein we propose a more precise value for $L$ founded on the notion that $L$ represents the intersection of two energy-based length scales: one derived from General Relativity and one from Quantum Mechanics. From General Relativity, one can assign a length value to the energy of a body using its Schwarzschild radius $r_s$, since the body's energy is given by $E = r_s c^4/(2G)$. Alternatively, one can also assign a length value to the body's energy from Quantum Mechanics using the body's De Broglie wavelength $\lambda$, in which case its energy is $E = hc/\lambda$, where $h$ is Planck's constant. Notice that $r_s$ is proportional to the energy of the body, but $\lambda$ is inversely proportional. We propose that $L$ corresponds to the energy scale at which these two length values coincide. Therefore,

$$
\begin{split}
\frac{h c}{L} &= \frac{r_s c^4} {2G} \\
& \therefore L = \sqrt{\frac{2 h G}{c^3}} = 5.729\times 10^{-35}\ \text{m}
\end{split}
\tag{5.9}
$$

which is still comparable to $l_p$ but slightly larger. From Eq. (5.9) and Eq. (5.8), it follows that the upper bound for the Schwarzschild radius $\max(r_s)$ of a perfectly continuous body and therefore the upper bound for its mass $\max(M)$ are given by:

$$
\begin{split}
\max(r_s) & \sim 3.713\times 10^{-35}\text{m} \\
\max(M)& = \max(r_s)\frac{c^2}{2G} \sim 2.500\times 10^{-8} \text{kg}
\end{split}
\tag{5.10}
$$

The maximum continuous mass derived above corresponds to the case when $r_g = r_s$. For ordinary matter, however, $r_g \gg r_s$.

How does the constraint expressed in Eq. (5.7) apply to the particles that comprise matter? Table 3 lists the values of $r_s$ and $r_g$ for the proton, neutron, and electron. Subatomic particles do not have definite radii, but the size of their radii can be modeled based on how they interact with other particles. For example, the root mean square charge radius of a proton is determined from electron scattering experiments; it has a well-accepted value [7] which is the one used in Table 3 for the proton radius. Modern particle theory considers the electron to be a point particle, but its classical radius $r_e$, which is what we use in Table 3, can be calculated as the combination of fundamental constants: $r_e = e^2/(4\pi \varepsilon_0 m_e c^2)$ where $e$, $m_e$, and $\varepsilon_0$ are the electron charge, electron mass, and the permittivity of free space, respectively. The radius of the neutron is relatively challenging to compute because of its overall neutral charge. Several researchers [8, 9, 10] have studied $^{208}$Pb to determine the difference between the neutron and proton radii with results in the range of $0.15 - 0.33$ fm. Based on this research, Table 3 uses an estimate for the neutron's radius that is $0.2$ fm larger than the proton's. One conclusion from the values of $r_s$ and $r_g$ for the listed particles is that since $r_g \gg r_s$, the weak field regime applies, at least for the case of the neutron, and so do the approximations used in our calculations herein. Accounting for the electron and proton's charge will affect the details, but we expect the conclusions below to be similar to those for the case of the neutron.

**Table 3.** Length scales and energy scales of common sub-atomic particles expressed in terms of their geometric and Schwarzschild radii in comparison to the fabric's thickness $L$.

| Particle | $M$ [kg] | $r_g$ [m] | $r_s = \frac{2GM}{c^2}$ [m] | ${54 r_s r_g}/{35 L^2}$ |
|---|---|---|---|---|
| proton [11, 7] | $1.673 \times 10^{-27}$ | $8.8 \times 10^{-16}$ | $2.5 \times 10^{-54}$ | $1.0 \times 10^{0}$ |
| neutron [12, 8, 9, 10] | $1.675 \times 10^{-27}$ | $1.1 \times 10^{-15}$ | $2.5 \times 10^{-54}$ | $1.3 \times 10^{0}$ |
| electron [13, 14] | $9.109 \times 10^{-31}$ | $2.8 \times 10^{-15}$ | $1.4 \times 10^{-57}$ | $1.8 \times 10^{-3}$ |

Table 3 also shows that the constraint expressed in Eq. (5.7) applies with some tolerance to the proton, neutron, and electron. While the electron fits well within the constraint, the proton and neutron exceed it slightly by about 2% and 30%, respectively. Unlike the electron, however, both the proton and the neutron have substructure, since they are made up of yet smaller particles known as quarks, so exceeding the constraint slightly in their case is not necessarily a problem. In reality, modeling subatomic particles as tiny spheres is an approximation anyway, since these particles also have wave nature and lack definite boundaries.

In fact, as the following subsection discusses, if we account for the possibility that these subatomic particles oscillate between various non-spherically symmetric configurations, then an arrangement is possible for which the total membrane energy vanishes completely.

In this section, we showed using a proof by contradiction that matter cannot be arbitrarily large and continuous at the same time, and that therefore it must be granular. Our approach was to assume the contrary, perform calculations with continuous matter, and reach a problematic conclusion. Had we considered discrete matter directly, we would have had to account for the motion of matter particles due to their interaction. Because the calculations were done in the context of continuous matter, they remained within the Cosmic Fabric Model's assumption of staticity.

### 5.2 Discrete Substructure

Next we show that a spherically symmetric inclusion can be arbitrarily massive as long as it is not perfectly continuous. In other words, continuity of matter is not admissible at any arbitrary length scale, but bodies must be composed of discrete particles. At the same time, a body could be treated as spherically symmetric and ostensibly continuous at sufficiently large length scales even while composed of discrete particles (see Fig. 6). We show herein that if individual particles prescribe asymmetric fabric strain, such as oblate or longitudinal expansion, then there would be no resulting membrane energy. Thus, it is possible for the gravitating body to cause in-plane fabric strain that appears symmetric at the continuum length scale, but without incurring any membrane energy.

![A spherically symmetric body that appears continuous and isotropic at the length scales comparable to its size, with its actual substructure progressively revealed.](https://figures.tgtenev.com/tenev2019-spacetime-metric/fig-substructure.svg)

**Figure 6.** A spherically symmetric body that appears continuous and isotropic at the length scales comparable to its size. The actual structure is progressively revealed in (a) through (c), where (a) shows the body idealized as perfectly continuous and spherically symmetric at all length scales. The dashed lines represent imaginary subdivisions of the body into cells. In (b) the mass in each cell is revealed to be concentrated into a small particle, while the mass density of the body remains unaffected at larger length scales. In (c) each particle is revealed to cause asymmetric strain from local anisotropies, while the body remains ostensibly isotropic at larger length scales.

Fig. 6 shows a spherically symmetric body whose substructure is revealed progressively from most idealized (no substructure) in Fig. 6a to least idealized (most detailed substructure) in Fig. 6c. At sufficiently large length scales the body appears continuous and isotropic, but at smaller length scales continuity and isotropy need not necessarily apply as Fig. 6c shows local anisotropies. In Fig. 6, the gravitating body is pictured as subdivided into cells whose total mass remains the same from one subfigure to another, but the distribution of that mass within the cell is revealed to be different from one subfigure to another. Eq. (5.6) shows that the membrane energy depends on the spatial radius $r_g$ of a gravitating body. Therefore, the membrane energy due to each cell within the body is reduced from Fig. 6a to Fig. 6b. To get an idea of the reduction, consider for example, that the mass of the Hydrogen atom with radius of about $5.3\times 10^{-11}\ \text{m}$ is concentrated in its nucleus, which is a single proton with radius of about $8.8\times 10^{-16}\ \text{m}$. So, simply by refining the picture we have for the hydrogen atom from a continuous solid sphere to a nearly hollow sphere with a nucleus, we would have to adjust our calculation for its resulting membrane energy by a factor of $\times 10^{-5}$. However, we can do even better than that and completely eliminate the membrane energy if we allow non-spherically symmetric strain at the substructure length scale as described below.

Consider the strain tensor $\varepsilon^i_j$ of the fabric due to a single sub-scale particle inclusion such as one of the anisotropic particles in Fig. 6c. Let us choose for convenience a coordinate system orientation in which this strain tensor is represented by a diagonal matrix, and let $\varepsilon_i \equiv \varepsilon^i_i\  i = 1\ldots 3$ (no summation) be the diagonal entries. From Eq. (5.2) we see that,

$$
\begin{split}
U_\text{M} & \propto \varepsilon_1^2 + \varepsilon_2^2 + \varepsilon_3^2 - (\varepsilon_1 + \varepsilon_2 + \varepsilon_3)^2 \\
& = -2\left[\varepsilon_1 \varepsilon_2 + \varepsilon_2 \varepsilon_3 + \varepsilon_3 \varepsilon_1 \right]
\end{split}
\tag{5.11}
$$

For any arbitrary value of the volumetric strain $\varepsilon^\text{3D} = \varepsilon_1 + \varepsilon_2 + \varepsilon_3 \neq 0$, the membrane energy $U_\text{M}$ can be made to vanish under a variety of conditions. For example, one such condition is purely a longitudinal strain: $\varepsilon^\text{3D} = \varepsilon_1;\  \varepsilon_2 = \varepsilon_3 = 0$, while another condition is an oblate strain: $\varepsilon_1 = \varepsilon_2;\  \varepsilon_3 = -\varepsilon_1/2;\  \varepsilon^\text{3D} = 3\varepsilon_1/2$. Therefore, if the substructure of all matter is closest to the one represented in Fig. 6c, then there would be no resulting membrane energy: $U_\text{M} = 0$.

Is the substructure depicted in Fig. 6c a reasonable description of matter? Indeed. Ordinary matter at different length scales exhibits anisotropies all the way down to subatomic particles that are themselves not solid spheres but waves and therefore not perfectly spherically symmetric. The lower length scale anisotropies average out to an overall isotropic and symmetric volumetric strain field in a homogenized manner.

## 6. Discussion

In the previous sections we developed a method for calculating the deformation metric of the cosmic fabric as it bends due to a spherically symmetric inclusion, and we derived a closed form solution (see Eq. (4.24)) for the metric in the regime of small strain (weak gravity). Below, we compare this result to the Schwarzschild solution [4] of the Field Equations of General Relativity and to Flamm's visualization of the same [6]. We also discuss future generalizations using numerical methods.

### 6.1 Comparison with the Schwarzschild Metric

The Schwarzschild Metric [4] is a solution of the Field Equations of General Relativity for a static spherically symmetric gravitating body. In the weak gravity regime, as assumed here, the Schwarzschild metric can be written in linearized form as follows:

$$
\begin{split}
ds^2_\text{int} &= -\left(1 - \frac{3r_g^2}{2r_0^2} + \frac{r^2}{2r_0^2}\right) c^2 dt^2 \\
&+ \left(1 + \frac{r^2}{r_0^2}\right) dr^2 + r^2 d\Omega^2 \\
ds^2_\text{ext} &= -\left(1-\frac{r_s}{r}\right) c^2 dt^2 \\
&+ \left(1+\frac{r_s}{r}\right) dr^2 + r^2 d\Omega
\end{split}
\tag{6.1}
$$

where, $d\Omega^2 \equiv d\theta^2 + \sin^2\theta d\varphi^2$, and $r_0^2 \equiv r_g^3/r_s$. Furthermore, $\overline{R}$, $\theta$ and $\varphi$ are the material polar coordinates in three-dimensional space, and $r = (1+e)\overline{R}$ is the stretched radius as indicated in Fig. 3.

Both the Schwarzschild metric in Eq. (6.1) and the one derived herein in Eq. (4.24) describe the same spacetime as it has been deformed due to a gravitating body of radius $r_g$ and Schwarzschild radius $r_s$. Notice that the time coefficients are the same in both metrics. Also, both metrics result in the same Ricci curvature of space, which is $R^\text{3D} = 6/r_0^2$ in the interior, and $R^\text{3D} = 0$ in the exterior of the gravitating body. The main difference between the two metrics are the spatial coefficients. The metric derived in Eq. (4.24), shows that the fractional amount by which space is stretched volumetrically equals the fractional amount by which time lapse has been retarded. While this is true for the exterior Schwarzschild metric, it is not the case for the interior according to Eq. (6.1). The reason for this difference is that the metric we derived in Eq. (4.24) accounts for the in-plane stretch of physical space that is specified by the radial function $e(\overline{R})$. Without attributing material properties to space, however, the radial stretch $e$ does not have physical meaning, since it does not produce a measurable intrinsic curvature. Therefore, in classical General Relativity, the stretch $e(\overline{R})$ would be viewed as mere coordinate relabeling.

If we expressed the metric we derived in Eq. (4.24) in terms of the stretched polar coordinates $(t, r, \theta, \varphi)$ instead of the material polar coordinates $(t, \overline{R}, \theta, \varphi)$, we would recover the linearized Schwarzschild metric per Eq. (6.1). Indeed, from $r = (1 + e)\overline{R}$ follows,

$$
\begin{split}
\overline{R} &\approx (1-e)r \\
d\overline{R} & \approx (1 - e - e'r)dr
\end{split}
\tag{6.2}
$$

Consequently,

$$
\begin{split}
\overline{R}_\text{int} &= \left(1 - \frac{r_g^2}{4r_0^2} + \frac{3r^2}{20r_0^2}\right)r \\
\quad \overline{R}_\text{ext} &= \left(1 - \frac{r_s r_0^2}{10r^3}\right)r \\
d\overline{R}_\text{int} &= \left(1 - \frac{r_g^2}{4r_0^2} + \frac{9r^2}{20r_0^2}\right)dr \\
d\overline{R}_\text{ext} &= \left(1 + \frac{r_s r_0^2}{5r^3}\right)dr
\end{split}
\tag{6.3}
$$

Substituting the above into Eq. (4.24) yields the linearized form of the Schwarzschild metric in Eq. (6.1). Therefore from the perspective of General Relativity, the two metrics are equivalent, because the above substitution constitutes mere coordinate rescaling. In General Relativity, the Schwarzschild solution has a slightly simpler form than the one derived here, which may be the reason why it is preferred, but the solution derived here is consistent with attributing material properties to spacetime.

Arriving at a metric that is equivalent to the weak field limit of the classical Schwarzschild metric is significant, because it validates the postulates underlying the Cosmic Fabric model. At the same time, the derived metric has the additional meaning of describing the deformation of a solid and as such it is equivalent to the fabric's Cauchy-Green deformation tensor (see §2.2). This equivalence is also significant, because: 1) it shows that the solid mechanics analogy of gravity is internally consistent, and 2) enables us to relate the rate of time lapse at a point in space to the volumetric expansion of the fabric at that point, which for the case of nearly static configuration allows us to construct the full spacetime metric from the deformation metric of physical space.

### 6.2 Flamm's Paraboloid

Shortly after Karl Schwarzschild published his solution to the Field Equations of General Relativity for the case of spherical symmetry [4], Ludwig Flamm [6] offered a geometric interpretation of it. Flamm considered the spatial geometry of the Schwarzschild metric at a fixed time coordinate. He recognized that the interior metric is equivalent to the metric of a spherical cap and the exterior to that of a paraboloid. The interior cap is generated by revolving a circular arc of radius $r_0$ around its perpendicular bisector within four-dimensional Euclidean space, where $r_0$ is as defined in Table 2. The paraboloid is generated by revolving a parabola around its directrix within the same four-dimensional space. In both cases the axes of revolution coincide with each other and are aligned along a fictitious fourth spatial dimension. The resulting shape is illustrated in Fig. 7, where the fictitious fourth spatial dimension is labeled $w$, while the three ordinary spatial dimensions are $x^i,\  i=1\ldots 3$. The shape is known today as "Flamm's Paraboloid," although only a portion of it is a paraboloid, and is used mainly as a pedagogic tool when teaching General Relativity.

![The bending of the cosmic fabric due to a spherically symmetric inclusion assumes the shape known as Flamm's Paraboloid, a paraboloid in the exterior with a spheroid cap in the interior.](https://figures.tgtenev.com/tenev2019-spacetime-metric/fig-flamms-paraboloid.svg)

**Figure 7.** The bending of the cosmic fabric due to a spherically symmetric inclusion of radius $r_g$ assumes the shape known as Flamm's Paraboloid, which consists of a paraboloid in the exterior of the inclusion, and a spheroid cap of radius $r_0 = 3/(\kappa c^2 \rho)$ within the interior, where $\rho$, $\kappa$, and $c$, are the density of the inclusion, the Einstein constant, and the speed of light, respectively. Only two of the ordinary spatial dimensions are depicted, but the third is implied.

Let $w = w(r)$ be the radial profile of Flamm's paraboloid, where $r$ is the distance from the axis of revolution, and $w$ represents the offset into the fictitious fourth spatial dimension. The closed form for $w$ which Flamm [6] computed is identical to the solution we derived in Eq. (4.11) for the transverse displacement $w$ of the cosmic fabric when bending as a result of an inclusion. In other words, the shape that the cosmic fabric attains when bending due to an inclusion is none other than Flamm's Paraboloid.

Until now Flamm's Paraboloid [6] has been mainly referenced for instructional purposes as a way to visualize the bending of space due to a spherical mass. For the first time in this paper, we show that Flamm's Paraboloid can be treated as a material body with constitutive properties, whose behavior is dictated by said properties according to solid mechanic's principles.

In addition to arriving at the shape of Flamm's Paraboloid, the solution of the fabric's governing equations also includes a radial stretch, which does not affect the curvature of the fabric. Such a radial stretch is not included in the description of Flamm's Paraboloid, because from a General Relativity perspective, it bears no physical significance and can be construed as mere coordinate rescaling. For the solid mechanics model, however, the radial stretch is significant, because it affects the time lapse rate and the membrane energy density of the fabric.

### 6.3 Generalization Using Numerical Methods

The method for calculating the cosmic fabric's metric can be readily generalized to non-flat initial geometry and asymmetric configuration. In such a case, the governing equations reasoned in §4.1 do not necessarily have closed form solutions but must be solved numerically. If the initial geometry of the fabric and its inclusion are spherically symmetric, then the method still reduces to a single first order ordinary differential equation, which is straightforward to solve using well known numerical techniques. If the configuration is not spherically symmetric, however, it may still be possible to approximate it with linear superposition of a finite number of spherically symmetric sub-configurations. These can be solved individually, and their solutions superimposed. Such a decomposition into spherically symmetric configurations and the subsequent linear superposition is valid in the regime of small strains (weak gravity).

Another potentially straightforward generalization of our method is for the spherically symmetric case of large strains (strong gravity). The majority of the steps used in earlier sections that derive the various kinematic and energy quantities of the fabric are admissible for large strains. The calculations for the metric tensor, extrinsic, and intrinsic curvature are such examples. The small strain assumption is mainly a convenience to avoid complicated radicals in the closed form solution, but that is not an issue when using numerical techniques.

### 6.4 Bridging between Length Scales

As we examine matter-fabric interaction at the continuum length scale, we are led to "peek" at the substructure (sub-continuum) length scale, and eventually conclude per §5.2 that matter must be made of discrete particles. The notion of "bridging between length scales" refers to the description of how phenomena at a lower length scale are aggregated to manifest at the length scale above, and conversely, what constraints are imposed by observations at a higher length scale onto the lower length scale models. Theories that bridge between length scales include a length parameter that controls the transition between scales. The fabric's thickness $L$ plays this role for the Cosmic Fabric Model.

One might ask whether using the fabric's thickness $L$ as a length scale parameter could lead to violating the Lorentz invariance. Ostensibly, there is a preferred reference frame wherein the fabric's thickness has the value of $L$ but in a boosted frame the thickness will be different due to the Lorentz contraction. Since a Lorentz contraction occurs in the direction of motion, which must be within the three ordinary spatial dimensions, the fabric's thickness will not be directly affected by it. Nevertheless, Lorentz contraction is still a factor since $L$ is used as a length scale against which the lengths of moving objects are compared. For example, consider a body in a boosted reference frame, whose length shortens from being much larger than $L$ at rest to being comparable or less than $L$; such a body would have transitioned from one length scale regime to another as it was boosted and will experience physical laws differently from one reference frame to the other. Such an outcome, which is indeed a consequence of the Cosmic Fabric Model, would constitute violation of the Lorentz invariance. However, achieving such a length scale transition requires boost speeds that are too close to the speed of light $c$ to be experimentally attainable. For example, the proton diameter is about $10^{20}$ times larger than Planck's length, and so it is about that much larger than $L$. For the proton to achieve length contraction of such order, requires a boost speed that approaches $c$ to within a fraction of $10^{-40}$. By comparison, CERN's Large Hadron Collider accelerates protons to only within $10^{-10}$ of the speed of light [15]. For larger bodies, the boost speed required to cross between length scale regimes will have to be even greater than what is required for the proton. So, while the Cosmic Fabric Model does suggest the theoretical possibility for violating the Lorentz invariance, doing so requires extreme conditions that are beyond practical observation.

The thickness of the cosmic fabric along a fourth spatial dimension is ostensibly reminiscent of models of large extra dimensions [16, 17] that have been proposed to explain why gravity is much weaker than the weak force, which is known as the "hierarchy problem" [17]. As with these models, the fabric's thickness $L$ only affects gravitational flux at length scales comparable to $L$, but for much larger length scales the fabric behaves as an essentially three-dimensional object. This, however, is the extent of the similarity. The models of large extradimensions must rely on a large number of additional dimensions to "hide" the gravitational flux at short range. By contrast, the Cosmic Fabric Model introduces only one extra dimension beyond the ordinary three and for a different reason: the fabric's thickness creates the needed resistance to bending, so that the Einstein Field Equations can be interpreted as the bending equations of a thin plate, as discussed in [1].

Other theories which have attempted to bridge the continuum and substructure length scales of physical space include: the theory of Causal Sets [18, 19, 20, 21, 22] (CS), Loop Quantum Gravity [23, 24, 25] (LQG), and Causal Dynamic Triangulation [26, 27] (CDT). CS treats spacetime as a collection of discrete events connected through causal relationships; in LQG space has extremely small substructure consisting of interwoven loops on the order of Planck's length; CDT is a complementary idea to LQG treating four-dimensional spacetime as arising from a two-dimensional spacetime near the Planck's scale. Unlike the Cosmic Fabric Model (CFM) discussed here, all three of the aforementioned theories are formulated at the substructure length scale, whereas the CFM's formulation is at the continuum length scale and offers, for now, limited perspective on the length scales below. In this context, CFM may be complementary with CS, CDT, and especially with LQG, because it is consistent with these theories in the following significant ways: they all seek to explain physical phenomena at multiple length scales, they all allow for space to have discontinuous substructure, and both CFM and LQG point to the notion that space and matter are fundamentally similar to each other.

## 7. Summary and Conclusion

In this paper, we advanced the Cosmic Fabric model beyond what Tenev and Horstemeyer [1, 2] accomplished, by investigating the details of how mass-energy inclusions interact with the fabric and cause it to bend. This investigation complemented the initial work reported in [1] which had focused on how the cosmic fabric bends outside of inclusions. In the process, we developed a method for calculating the spacetime metric of the cosmic fabric, which we applied for the case of initially flat fabric and a spherically symmetric inclusion. The derived metric was equivalent to Schwarzschild's [4] up to a rescaling factor that accounted for in-plane stretch. Furthermore, we showed that the fabric bends into the shape known as Flamm's Paraboloid [6].

We also demonstrated the scale-dependent nature of the Cosmic Fabric model [1], which is linked to its thickness. From an investigation of the total elastic energy due to an inclusion, we determined an upper limit for the mass of the largest possible continuous inclusion. We showed that the total membrane energy $W_\text{M}$ varies disproportionately with the size of the inclusion and is therefore length-scale dependent, where the fabric's thickness $L$ serves as the length-scale parameter. To avoid disproportionately large membrane energy, we reasoned that there must be a limit on the largest possible continuous material body, which we expressed in Eq. (5.7), Eq. (5.8), and Eq. (5.10). Consequently we concluded that matter must have discontinuous substructure as illustrated in Fig. 6. This result is consistent with the known constitution of matter at atomic and subatomic length scales.

In conclusion, the work presented herein further validates the Cosmic Fabric model of gravity [1] by showing that it leads to equivalent results as linearized General Relativity. Unlike General Relativity, however, the Cosmic Fabric model includes a built-in length-scale parameter, which leads to interesting predictions such as the discrete nature of matter. By contrast, General Relativity is strictly a continuum theory and therefore has no means of modeling substructure length scales. The length-scale dependence that is part of the Cosmic Fabric model but lacks in General Relativity is a necessary and useful aspect of the model that helps bridge between a theory of gravity and other physical theories, such as fundamental theories of matter.

## Acknowledgments

The authors would like to acknowledge the anonymous reviewers for the detailed scrutiny and thoughtful comments, which added value to the paper.

## References

1. T. G. Tenev and M. F. Horstemeyer, *International Journal of Modern Physics D* **27** (Jun 2018) 1850083, [arXiv:1603.07655](http://arxiv.org/abs/1603.07655).
2. T. G. Tenev and M. F. Horstemeyer, *Reports in Advances of Physical Sciences* **02** (Dec 2018) 1850011, [arXiv:1808.08804](http://arxiv.org/abs/1808.08804).
3. T. G. Tenev and M. F. Horstemeyer, *International Journal of Modern Physics D* (Jan 2019) S0218271819500822.
4. K. Schwarzschild, *Sitzungsber. Preuss. Akad. Wiss. Berlin (Math. Phys.)* **1916** (1916) 189, [arXiv:physics/9905030](http://arxiv.org/abs/physics/9905030).
5. A. Einstein, *Annalen der Physik* **354** (1916) 769.
6. L. Flamm, *General Relativity and Gravitation* **47** (Jun 2015) 72.
7. US National Institute of Standards and Technology, "Proton rms charge radius" (2014), https://physics.nist.gov/cgi-bin/cuu/Value?rp.
8. S. Abrahamyan et al., *Physical Review Letters* **108** (Mar 2012) 112502, [arXiv:1201.2568](http://arxiv.org/abs/arXiv:1201.2568v2).
9. A. W. Steiner, J. M. Lattimer and E. F. Brown, *The Astrophysical Journal* **722** (Oct 2010) 33, [arXiv:1005.0811](http://arxiv.org/abs/arXiv:1005.0811v2).
10. K. Hebeler, J. M. Lattimer, C. J. Pethick and A. Schwenk, *Physical Review Letters* **105** (Oct 2010) 161102, [arXiv:1007.1746](http://arxiv.org/abs/arXiv:1007.1746v2).
11. US National Institute of Standards and Technology, "Proton mass" (2014), https://physics.nist.gov/cgi-bin/cuu/Value?mp.
12. US National Institute of Standards and Technology, "Neutron mass" (2014), https://physics.nist.gov/cgi-bin/cuu/Value?mn.
13. US National Institute of Standards and Technology, "Electron mass" (2014), https://physics.nist.gov/cgi-bin/cuu/Value?me.
14. US National Institute of Standards and Technology, "Electron radius" (2014).
15. CERN, "LHC Guide" (2017).
16. M. Shifman, *International Journal of Modern Physics A* **25** (Jan 2010) 199, [arXiv:0907.3074](http://arxiv.org/abs/0907.3074v2).
17. N. Arkani-Hamed, S. Dimopoulos and G. Dvali, *Physics Letters B* **429** (Jun 1998) 263.
18. D. P. Rideout and R. D. Sorkin, *Physical Review D* **61** (Dec 1999) 024002.
19. R. D. Sorkin, "Does locality fail at intermediate length scales?," in *Approaches to Quantum Gravity*, ed. D. Oriti (Cambridge University Press, Cambridge, 2009) pp. 26–43.
20. D. D. Reid, *Physical Review D* **67** (Jan 2003) 024034.
21. G. Brightwell and R. Gregory, *Physical Review Letters* **66** (Jan 1991) 260.
22. D. B. Malament, *Journal of Mathematical Physics* **18** (Jul 1977) 1399.
23. R. Gambini and J. Pullin, *Classical and Quantum Gravity* **26** (Feb 2009) 035002.
24. C. Rovelli, *Quantum Gravity* (Cambridge University Press, 2004).
25. C. Rovelli, *Zakopane Lectures on Loop Gravity*, tech. rep., Centre de Physique Théorique de Luminy, Case 907, F-13288 Marseille, EU (Feb 2011).
26. R. Loll, *Nuclear Physics B (Proc. Suppl.)* **94** (2001) 96.
27. J. Ambjørn, J. Jurkiewicz and R. Loll, *Contemporary Physics* **47** (Mar 2006) 103.
