[&#8592; Contents](../tenev2018-dissertation.md)

# V. Spacetime Metric of a Spherically Symmetric Inclusion

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
[\partial_{ij} y^1] &= \begin{pmatrix} r'' & 0 & 0 \\
0 & e' & 0 \\
0 & 0 & e' \end{pmatrix}
\quad [\partial_{ij} y^2] = \begin{pmatrix} 0 & e' & 0 \\
e' & 0 & 0 \\
0 & 0 & 0 \end{pmatrix}
\quad [\partial_{ij} y^3] = \begin{pmatrix} 0 & 0 & e' \\
0 & 0 & 0 \\
e' & 0 & 0 \end{pmatrix} \\
[\partial_{ij} y^4] &= \begin{pmatrix} w''(r')^2 + w'r'' & 0 & 0 \\
0 & w'r'\overline{r}^{-1} & 0 \\
0 & 0 & w'r'\overline{r}^{-1} \end{pmatrix}
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
\begin{pmatrix} \hat{n}^1 \\
\hat{n}^2 \\
\hat{n}^3 \\
\hat{n}^4 \end{pmatrix} = \frac{1}{\sqrt{1+(w')^2}} \begin{pmatrix} w' \\
0 \\
0 \\
-1 \end{pmatrix}.
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

The above constraints are motivated as follows: Consider the Fabric's action $\mathcal{S} = \int \mathcal{L}\_\text{F} \sqrt{|g|}\  dx^4$ where $\mathcal{L}\_\text{F}$ is the Lagrangian of the fabric together with the inclusion; $g \equiv \det [g_{\mu\nu}]$ is the determinant of the spacetime metric; and the integral is taken over a sufficiently large volume of spacetime such that the integral converges. According to the Principle of Least Action, physical systems progress along a trajectory that extremizes the action (the action is either minimized or maximized). For a nearly static situation the kinetic components of $\mathcal{L}\_\text{F}$ can be ignored, so only the contributions from the fabric's elastic energy and the body's relativistic energy need to be considered. Thus, $\mathcal{L}\_\text{F} = -(U_\text{M} + U_\text{B} + c^2 \rho)$. Furthermore, per Equation (3.9) the determinant $|g| \approx 1$. Therefore, since the total energy integrated over all of three-dimensional space should be non-negative, the action $\mathcal{S}$ would reach an extremum if the deformation functions $e$ and $w$ were such that the total elastic energy $W$ vanished, where $W$ is defined as follows:

$$
\begin{split}
W \equiv \int_\text{all space} (U_\text{M} + U_\text{B} + c^2 \rho)\  dx^3 = 0
\end{split}
\tag{5.17}
$$

As the *Membrane Energy and the Discrete Nature of Matter* section demonstrates, the membrane energy component of the above integral is length scale dependent because it varies disproportionately with the mass of the gravitating body unlike the other two components which are length scale independent. Therefore, in order for $W$ from Equation (5.17) to vanish for inclusion of any mass, it follows that the total membrane energy $W_\text{M}$, defined per Equation (5.18), must vanish independently from the other two components. Consequently, Equation (5.17) yields these two independent equations:

$$
\begin{split}
W_\text{M} \equiv \int_\text{all space} U_\text{M}\  dx^3 = 0
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

where $C_3$ and $C_4$ are constants of integration. Let $\varepsilon_\text{int}$ and $\varepsilon_\text{ext}$ represent the interior and exterior solutions, respectively. For the interior solution, $0\le \overline{r} \le \overline{r}\_g$, we determine that $C_3 = 0$, or else $\varepsilon_\text{int}$ diverges as $\overline{r} \rightarrow 0$. For the exterior case, $r_0 = \infty$, so $\varepsilon_\text{ext} = C_4 + C_3/r$, but $C_4$ must vanish, for $\varepsilon_\text{ext}$ to vanish at infinity. Thus, we conclude so far the following,

$$
\begin{split}
\varepsilon_\text{int} = C_4 - \frac{1}{4}\frac{r^2}{r_0^2}; \quad \varepsilon_\text{ext} = \frac{C_3}{r}.
\end{split}
\tag{5.30}
$$

For it to be physically admissible, $\varepsilon$ and its first derivative must be continuous throughout three-dimensional space. Therefore,

$$
\begin{split}
&\varepsilon_\text{int}(r_g) = \varepsilon_\text{ext}(r_g); \quad \left.\frac{d}{d\overline{r}}\varepsilon_\text{int}\right|\_{r = r_g} = \left.\frac{d}{d\overline{r}}\varepsilon_\text{ext}\right|\_{r = r_g} \\
&\therefore\ C_3 = \frac{r_s}{2}; \quad C_4 = \frac{3r_g^2}{4r_0^2},
\end{split}
\tag{5.31}
$$

which finally produces the following result:

$$
\begin{split}
\varepsilon_\text{int} = \frac{3}{4}\frac{\overline{r}\_g^2}{r_0^2} - \frac{1}{4}\frac{\overline{r}^2}{r_0^2}; \quad \varepsilon_\text{ext} = \frac{1}{2}\frac{r_s}{\overline{r}}
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

where $d\Omega^2 \equiv d\theta^2 + \cos^2 \theta\  d\varphi^2$, and where $g_{tt}$, $g_{\overline{r}\overline{r}}$, and $g_{\Omega\Omega}$ are the polar metric coefficients.

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

Chapter III explains that the thickness of the fabric $L$ must be comparable to Planck's length $l_p = 1.616229\times 10^{-35}\ \text{m}$. Herein we propose a more precise value for $L$ founded on the notion that $L$ represents the intersection of two energy-based length scales: one derived from General Relativity and one from Quantum Mechanics. From General Relativity, one can assign a length value to the energy of a body using its Schwarzschild radius $r_s$, since the body's energy is given by $E = r_s c^4/(2G)$. Alternatively, one can also assign a length value to the body's energy from Quantum Mechanics using the body's De Broglie wavelength $\lambda$, in which case its energy is $E = hc/\lambda$, where $h$ is the Planck's constant. Notice that $r_s$ is proportional to the energy of the body, but $\lambda$ is inversely proportional. We propose that $L$ corresponds to the energy scale at which these two length values coincide. Therefore,

$$
\begin{split}
\frac{h c}{L} &= \frac{r_s c^4}{2G} \\
\therefore\ L &= \sqrt{\frac{2 h G}{c^3}} = 5.729\times 10^{-35}\ \text{m}
\end{split}
\tag{5.50}
$$

which is still comparable to $l_p$ but slightly larger. From Equation (5.50) and Equation (5.49), it follows that the upper bound for the Schwarzschild radius $\max(r_s)$ of a perfectly continuous body and therefore the upper bound for its mass $\max(M)$ are given by:

$$
\begin{split}
\max(r_s) & \sim 3.713\times 10^{-35}\ \text{m} \\
\max(M)& = \max(r_s)\frac{c^2}{2G} \sim 2.500\times 10^{-8}\ \text{kg}
\end{split}
\tag{5.51}
$$

The maximum continuous mass derived above represents the mass of a tiny black hole, because we had assumed that $r_g = r_s$. For ordinary matter, however, $r_g \gg r_s$. How does the constraint expressed in Equation (5.48) apply to the particles that comprise matter?

Table 5.3 lists the values of $r_s$ and $r_g$ for the proton, neutron, and electron. Subatomic particles do not have definite radii, but the size of their radii can be modeled based on how they interact with other particles. For example, the root mean square charge radius of a proton is determined from electron scattering experiments; it has a well-accepted value [168], which is the one used in Table 5.3 for the proton radius. Modern particle theory considers the electron to be a point particle, but its classical radius $r_e$, which is what we use in Table 5.3, can be calculated as the combination of fundamental constants: $r_e = e^2/(4\pi \varepsilon_0 m_e c^2)$ where $e$, $m_e$, and $\varepsilon_0$ are the electron charge, electron mass, and the permittivity of free space, respectively. The radius of the neutron is relatively challenging to compute because of its overall neutral charge. Several researchers [2, 63, 154] have studied $^{208}\text{Pb}$ to determine the difference between the neutron and proton radii with results in the range of $0.15 - 0.33$ fm. Based on this research, Table 5.3 uses an estimate for the neutron's radius that is $0.2$ fm larger than the proton's. One conclusion from the values of $r_s$ and $r_g$ for the listed particles is that because $r_g \gg r_s$, the regime of small strains (weak gravity) applies and so the approximations used in our calculations herein apply too.

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

Figure 5.4 shows a spherically symmetric body whose substructure is revealed progressively from most idealized (no substructure) in Figure 5.4a to least idealized (most detailed substructure) in Figure 5.4c. At a sufficiently large length scale, the body appears continuous and isotropic, but at smaller length scales continuity and isotropy need not necessarily apply as Figure 5.4c illustrates. In Figure 5.4, the gravitating body is pictured as subdivided into cells whose total mass remains the same from one subfigure to another, but the distribution of the mass within each cell is revealed to be different from one subfigure to another. Equation (5.47) shows that the membrane energy depends on the spatial radius $r_g$ of a gravitating body. Therefore, the membrane energy due to each cell within the body is reduced from Figure 5.4a to Figure 5.4b. To get an idea of the reduction, consider for example, that the mass of the Hydrogen atom with radius of about $5.3\times 10^{-11}\ \text{m}$ is concentrated in its nucleus, which is a single proton with radius of about $8.8\times 10^{-16}\ \text{m}$. So, simply by refining the picture we have for the hydrogen atom from a continuous solid sphere to a nearly hollow sphere with a nucleus, we would have to adjust our calculation for its resulting membrane energy by a factor of $\times 10^{-5}$. However, we can do even better than that and completely eliminate the membrane energy if we allowed non-spherically symmetric strain at the substructure length scale as described below.

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

where $d\Omega^2 \equiv d\theta^2 + \sin^2\theta\  d\varphi^2$, and $r_0^2 \equiv r_g^3/r_s$. Furthermore, $\overline{r}$, $\theta$ and $\varphi$ are the material polar coordinates in three-dimensional space, and $r = (1+e)\overline{r}$ is the stretched radius as Figure 5.1 indicates.

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
\overline{r}\_\text{int} &= \left(1 - \frac{r_g^2}{4r_0^2} + \frac{3r^2}{20r_0^2}\right)r; \quad \overline{r}\_\text{ext} = \left(1 - \frac{r_s r_0^2}{10r^3}\right)r \\
d\overline{r}\_\text{int} &= \left(1 - \frac{r_g^2}{4r_0^2} + \frac{9r^2}{20r_0^2}\right)dr; \quad d\overline{r}\_\text{ext} = \left(1 + \frac{r_s r_0^2}{5r^3}\right)dr
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

---

[Contents](../tenev2018-dissertation.md)  &nbsp;•&nbsp;  [&#9664; Recovering Relativity](ch4-recovering-relativity.md)  &nbsp;•&nbsp;  [Dark Matter Effect &#9654;](ch6-dark-matter-effect.md)
