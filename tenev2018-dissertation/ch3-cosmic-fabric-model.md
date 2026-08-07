[&#8592; Contents](../tenev2018-dissertation.md)

# III. Cosmic Fabric Model of Gravity

In this chapter, we develop a formal analogy between Solid Mechanics and General Relativity. Most of the content has been published in Tenev and Horstemeyer [160]. We identify physical space with the mid-hypersurface of a four-dimensional hyperplate, called the "cosmic fabric," which has a small thickness along a fourth spatial dimension and exhibits a constitutive stress–strain behavior. Matter–energy fields act as inclusions within the fabric causing it to expand longitudinally and consequently to bend. The effect, illustrated in Figure 3.1, is analogous to the result from General Relativity in which matter causes space to bend resulting in gravity. Unlike other theoretical paradigms that introduce additional spatial dimensions, such as string theory [61], or Brane world quantum models [45], our formulation is based on conventional Solid Mechanics theories that operate strictly within the three ordinary spatial dimensions.

![Plate bending from flat into a curved geometry.](https://figures.tgtenev.com/tenev2018-dissertation/fig-plate-bending.svg)

**Figure 3.1.** Plate bending from flat into a curved geometry. A plate bending from flat geometry (a) into a curved geometry (b) because of an inclusion that prescribes an uneven strain field, as indicated by the concentric dashed lines and the diverging arrows. The strain is larger near the center and tapers off with the distance from it. For the geometry of the plate to accommodate the prescribed strain, the plate must bend into the transverse dimension.

We conduct our study in the limit of weak and nearly static gravitational fields, and demonstrate that outside of inclusions, the fabric's action $\mathcal{S}\_\text{F}$ assumes the form of the Einstein–Hilbert action $\mathcal{S}\_\text{EH}$ as follows,

$$
\begin{split}
\mathcal{S}\_\text{F} = \frac{YL^2}{48} \int R\sqrt{|g|}\ \mathrm{d}x^4 \quad \text{versus}\quad \mathcal{S}\_\text{EH}= \frac{1}{2\kappa} \int R\sqrt{|g|}\ \mathrm{d}x^4
\end{split}
\tag{3.1}
$$

where $L$ is the reference thickness of the fabric, $g \equiv \det g_{\mu\nu}$, and the integral is taken over a large enough volume of spacetime that is sufficient to ensure convergence. The action integral of any physical system fully determines its dynamics, because the system's equations of motion can be derived from the variation of the action with respect to the metric. Therefore, once we recognize $\mathcal{S}\_\text{F}$ as analogous to $\mathcal{S}\_\text{EH}$, we can interpret various attributes of the cosmic fabric, such as its shape, strain, vibrations, and elastic moduli as analogous to properties of gravity and space, such as curvature, gravitational potential, gravitational waves, and the zero-point energy density of space.

Our approach ostensibly resembles the Arnowitt–Deser–Misner (ADM) [14] and DeWitt [40] formulations of gravity in the way time lapse is separated from spatial extent. For example, under the ADM approach, spacetime is foliated into space-like hypersurfaces related to each other via shift and lapse functions. Like ADM, DeWitt also considers the time evolution of the three-dimensional spatial metric. Nevertheless, the Cosmic Fabric model differs from these formulations in that it associates constitutive behavior with the geometric description of gravity and derives its governing equations from a material-like constitutive relation. Furthermore, unlike these formulations, the cosmic fabric specifies a hyperplane of absolute simultaneity.

The Cosmic Fabric model of gravity allows General Relativity problems to be formulated as Solid Mechanics problems, solved within the Solid Mechanics domain, and the solution interpreted back in General Relativity terms. The reverse is also true. Thus, ideas, methodologies and tools from each field become available to the other field. Over the past century, Solid Mechanics and General Relativity have advanced independently from each other with few researchers having expertise in both. Consequently, significant terminology and focus gaps exist between these two fields, which obscure their underlying physical similarities. Our research attempts to bridge these gaps.

The remainder of this chapter is organized as follows: In the section *Formulation of the Cosmic Fabric Model of Gravity* we develop the solid mechanics analogy of gravity by specifying a material body whose behavior, determined solely based on Hooke's Law (1.2), is demonstrably analogous to the behavior of spacetime. In the *Discussion* section we discuss the implications of the resulting model, and summarize and conclude in the *Summary and Conclusion* section.

### Formulation of the Cosmic Fabric Model of Gravity

Consider a four-dimensional hyperplate, called here the "cosmic fabric," which is thin in the fourth spatial dimension, $x^4$. We show that, for suitably chosen constitutive parameters, the fabric's Lagrangian density outside of inclusions is $\mathcal{L}\_\text{F} = (YL^2/48)R\sqrt{|g|}$, where $\mathcal{L}\_\text{F}$ is the integrand in Equation (3.1). This result enables us to subsequently analyze how the remaining kinematic properties of the cosmic fabric correspond to properties of gravity.

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

Next, we compute the total elastic energy density $U$ averaged across the fabric's thickness, and we separate it into a bending term $U_\text{B}$ and a membrane stretch term $U_\text{M}$. For this purpose, we split the strain at each surface, $\varepsilon_{ij}$, into a membrane strain $\varepsilon^\text{M}\_{ij}$ and a bending strain $\varepsilon^\text{B}\_{ij}$ as follows:

$$
\begin{split}
\varepsilon_{ij} & = \frac{1}{2}(g_{ij} - \delta_{ij}) = \varepsilon^\text{M}\_{ij} + \varepsilon^\text{B}\_{ij} \\
\varepsilon^\text{M}\_{ij} & = \frac{1}{2}(a_{ij} - \delta_{ij}) \\
\varepsilon^\text{B}\_{ij} & = -b_{ij}\xi + \mathcal{O}(b^2\xi^2)
\end{split}
\tag{3.14}
$$

$$
\begin{split}
U &= \frac{1}{L} \int_{-\frac{L}{2}}^{\frac{L}{2}} U_{\xi}\  \mathrm{d}\xi = \frac{1}{2L} \int_{-\frac{L}{2}}^{\frac{L}{2}} C^{ijkl}(\varepsilon^\text{M}\_{ij}\varepsilon^\text{M}\_{kl} + \varepsilon^\text{B}\_{ij}\varepsilon^\text{B}\_{kl} + [\varepsilon^\text{M}\_{ij}\varepsilon^\text{B}\_{kl} + \varepsilon^\text{B}\_{ij}\varepsilon^\text{M}\_{kl}])\  \mathrm{d}\xi \\
& = U_\text{M} + U_\text{B} \\
U_\text{M} &= \frac{1}{2L} \int_{-\frac{L}{2}}^{\frac{L}{2}} C^{ijkl}\varepsilon^\text{M}\_{ij}\varepsilon^\text{M}\_{kl}\  \mathrm{d}\xi \\
U_\text{B} &= \frac{1}{2L} \int_{-\frac{L}{2}}^{\frac{L}{2}} C^{ijkl}\varepsilon^\text{B}\_{ij}\varepsilon^\text{B}\_{kl}\  \mathrm{d}\xi
\end{split}
\tag{3.15}
$$

The term $\mathcal{O}(b^2\xi^2)$ stands for an expression whose order of magnitude is comparable to the square of the elements $b_{ij}$ multiplied by $\xi^2$. The mixed terms inside the square brackets in Equation (3.15) vanish under integration because the bending strain reverses sign across the mid-hypersurface; hence $\varepsilon^\text{B}\_{ij} = \varepsilon^\text{B}\_{ij}(\xi)$ is an odd function, while $\varepsilon^\text{M}\_{ij} = \varepsilon^\text{M}\_{ij}(\xi)$ is an even function.

For the remainder of this subsection, we focus on evaluating the term $U_\text{B}$. The term $U_\text{M}$ will be addressed in the following subsection where we show that it vanishes under appropriately chosen material properties and deformation kinematics. Also, Chapter V shows that this term vanishes in general once we account for the discrete substructure of matter.

Evaluating $U_\text{B}$ from Equation (3.15), we obtain the following:

$$
\begin{split}
U_\text{B} = L^2C^{ijkl}\left[b_{ij}b_{kl} + \mathcal{O}(b^3 L)\right]
\end{split}
\tag{3.16}
$$

The extrinsic curvature terms $b_{ij}$ have magnitudes comparable to the inverse of the curvature radius. The curvature radius is much greater than the thickness of the fabric, so $\mathcal{O}(b L) \ll 1$, which allows us to ignore the term $\mathcal{O}(b^3 L)$ in the above expression. Using the identity $R^\text{3D}\_{lijk} = b_{ik}b_{jl} - b_{ij}b_{kl}$, where $R^\text{3D}\_{lijk}$ is the Riemann curvature tensor of the mid-hypersurface, and setting $\mathcal{O}(b^3 L) = 0$, we can express $U_\text{B}$ in terms of the intrinsic three-dimensional spatial curvature $R^\text{3D}$ as follows,

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

Ignoring the kinetic energy component, under the simplifying assumption of nearly static fields, the Lagrangian density is $\mathcal{L}\_\text{F} = - U_\text{B} \sqrt{|g|} \propto R^\text{3D} \sqrt{|g|}$, where $g \equiv \det[g_{\mu\nu}]$. The factor $\sqrt{|g|}$, which converts from a coordinate volume to a proper volume, is needed for $\mathcal{L}\_\text{F}$ to be a tensor density, which requires invariance under coordinate transformations.

Next, we derive an expression for $\mathcal{L}\_\text{F}$ in terms of the Ricci curvature $R$ of the fabric's world volume. According to the gauge-invariant linearized expression for $R$ per Misner et al. [119],

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
\mathcal{L}\_\text{F} = -U_\text{B} \sqrt{|g|} = \frac{YL^2}{48} R \sqrt{|g|}
\end{split}
\tag{3.23}
$$

which has the same form as the Einstein–Hilbert Lagrangian density. The resulting action is simply the integral of the Lagrangian density over coordinate spacetime, namely,

$$
\begin{split}
\mathcal{S}\_\text{F} = \int \mathcal{L}\_\text{F}\  \mathrm{d}x^4 = \frac{YL^2}{48} \int R\sqrt{|g|}\ \mathrm{d}x^4
\end{split}
\tag{3.24}
$$

which is what we had set out to demonstrate as stated earlier per Equation (3.1).

### Discussion

In the previous sections, we postulated a material body, which we named the "cosmic fabric," whose constitutive behavior outside of inclusions is analogous to the behavior of gravity, and have shown the sequential mathematical development. For the analogy to be useful, it should allow us to map between notions in Solid Mechanics and General Relativity. Such a mapping is possible on the basis of identifying the fabric Lagrangian density $\mathcal{L}\_\text{F}$ with the Lagrangian density from the Einstein–Hilbert action, $\mathcal{L}\_\text{EH}$, as applying to free space. Specifically,

$$
\begin{split}
\mathcal{L}\_\text{F} = \frac{YL^2}{48}R\sqrt{|g|} = \mathcal{L}\_\text{EH} = \frac{1}{2\kappa}R\sqrt{|g|}
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
\rho_\text{F} = \frac{\mu}{c^2} = \frac{Y}{4c^2} \sim 1.3 \times 10^{96}\ \mathrm{kg}\ \mathrm{m}^{-3}
\end{split}
\tag{3.30}
$$

In accordance with the Cosmic Fabric analogy, the density of the fabric corresponds to the density of free space, which is also known as the zero-point energy density. The computed value for $\rho_\text{F}$ agrees to an order of magnitude with the predictions of Quantum Field Theory ($\sim 10^{96}\ \mathrm{kg}\ \mathrm{m}^{-3}$) for the energy density of free space [146]. Note that the predictions of Quantum Field Theory are also based on using Planck's length $l_p$ as a length-scale parameter.

#### Gravitational Waves

Let us consider whether shear waves in the fabric are analogous to gravitational waves. Such an analogy depends on demonstrating that the fabric's behavior parallels that of spacetime for fast changing fields as well. We leave the rigorous proof as future work, and for the rest of this subsection we assume that the fabric's behavior implied by the Lagrangian (3.23) also holds for fast changing fields. Based on this assumption, we proceed to investigate in-plane shear waves propagating through the fabric and their correspondence to gravitational waves.

First, we show that if static fields are negligible and in the absence of torsion, then the strain $\varepsilon_{\mu\nu}$ satisfies the harmonic gauge condition, $\partial_\alpha \varepsilon^{\mu\alpha} = (1/2)\partial^\mu \varepsilon^\alpha_\alpha$. For shear waves, $\varepsilon = 0$, and by Equation (3.10), $\varepsilon_{00} = 0$, implying that $\varepsilon^{\alpha}\_{\alpha} = 0$. Therefore, proving the harmonic gauge condition is reduced to demonstrating that $\partial_\alpha \varepsilon^{\mu\alpha} = 0$. Furthermore, the shear time–space components must vanish, $\varepsilon_{4j} = \varepsilon_{j4} = 0 = \varepsilon_{0j} = \varepsilon_{j0}$, because we are assuming negligible static fields and in-plane shear waves. Therefore, in order to prove that the harmonic gauge condition holds, we just need to show that $\partial_k \varepsilon_{ik} = 0$. Let $u_i$ be the material displacement field. In terms of the displacement field, the strain is $2\varepsilon_{ij} = \partial_j u_{i} + \partial_i u_{j}$, and so,

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
| Action integral in free space, $\mathcal{S} = \frac{1}{2\kappa} \int R\sqrt{\|g\|}\ d^4x$ | Action integral outside of inclusions, $\mathcal{S} = \frac{L^2 Y}{48} \int R\sqrt{\|g\|}\ d^4x$ |
| Constants of Nature: $G,\ \hbar,\ c$ | Elastic constants: $Y = 6c^7/2\pi\hbar G^2,\ \nu=1$ |

The research presented in this chapter suggests an equivalence between postulating the field equations of General Relativity and postulating a cosmic fabric having material-like properties as described here. We believe that these are two different approaches for studying the same underlying reality. The Cosmic Fabric model introduces a new paradigm for interpreting cosmological observations based on well-established ideas from Solid Mechanics.

---

---

[Contents](../tenev2018-dissertation.md)  &nbsp;•&nbsp;  [&#9664; Background](ch2-background.md)  &nbsp;•&nbsp;  [Recovering Relativity &#9654;](ch4-recovering-relativity.md)
