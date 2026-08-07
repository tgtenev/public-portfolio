[&#8592; Contents](../tenev2018-dissertation.md)

# VII. Numerical Framework for Weak Gravity Dynamics

Earlier chapters detailed the theoretical basis that enables one to use the numerical tools of solid mechanics for solving problems within General Relativity and cosmology. Herein, we apply these ideas as we contribute with a numerical framework that is suited for a category of problems in cosmology, namely those concerning weak gravitational dynamics at galactic length scales.

The *Computational Methods* section of Chapter I discussed a number of mainstream computational techniques, such as the Finite Element Method (FEM), Finite Difference Method (FDM), and the N-Body Method, which find a variety of applications in solid mechanics, General Relativity and Cosmology. To this list, we add the Particle Mesh Method, which is a combination of the FDM and the N-Body Method, where the bodies do not interact with each other directly but through the gravitational potential. In turn, the latter is computed using FDM to solve a Boundary Value Problem based on the Poisson Equation of gravity.

Nearly all numerical methods consist of the following stages: preprocessing, solving, and post-processing. Also, most computational methods include a discretization strategy for reducing the solution domain from infinite to finite number of parameters. The Preprocessing Stage maps the physical problem onto a mathematical model, which usually involves configuring the geometry of the simulated bodies and their initial and boundary conditions. Typically, such a mathematical model is an idealization of the original problem. For example, when modeling the deformation of a body, not all surface details of the body are represented in the model but only what is considered relevant. Likewise, when modeling the large structure formation of the cosmos, stars and even galaxies may be treated as point particles. A divide-and-conquer strategy is often applied during the preprocessing stage, such as defining an element mesh in the case of FEM and FDM, or using a nested set of cells for the N-Body Method. The Solving Stage computes the result of the numerical simulation. Iterative solvers, such as used in FDM and the N-Body Method, compute the result incrementally so that a growing portion of the result becomes available before the computation terminates. By contrast, direct solvers, such as used with FEM, compute the result in one big step by, for example, solving a system of linear equations, so that any part of the result only becomes available upon the completion of the computation. Finally, the Post-Processing stage is when the computation result is analyzed and visualized.

This chapter introduces a MATLAB®-based framework that we have developed for performing numerical experiments in the category of weak gravity dynamics under the conditions of non-flat inherent geometry of space. The chapter also includes several such experiments that illustrate the use of the framework and whose results support the Inherent Structure Hypothesis introduced in Chapter VI. Our framework is based on the Particle Mesh method that has been modified to account for the presence of inherent intrinsic curvature of space. The numerical method described here assumes weak gravity (small strain) and nearly static gravitational fields (low strain rates). As stated in Chapter I, these assumptions are valid for our common experience of gravity. They are also consistent with the conditions under which the Dark Matter effect (see Chapter VI) has been observed, such as the conditions in the peripheries of galaxies and in galactic clusters.

The weak gravity (small strain) assumption allows us to reduce what is generally a four-dimensional (4D) problem to a three-dimensional (3D) one and solve it with conventional 3D numerical tools. That is because under the small strain assumption, the displacement of grid nodes is not a significant factor in the calculations and can be ignored. Geometric quantities, such as the hyperspatial displacement, $w$, the undeformed metric, $\overline{g}\_{ij}$, and Christoffel symbols, $\overline{\Gamma}^k\_{ij}$, are treated as generic field quantities whose discrete values have been assigned to the nodes of a fixed grid. The metric and Christoffel symbols pertaining to spacetime and to deformed space are also treated in the same way. Although grid nodes are not displaced during deformation, by accounting for these geometric quantities at each node, we are still taking into consideration the undeformed curvature.

The terms "mesh" and "grid" are used interchangeably in this chapter. Typically the former refers to any general subdivision of a body into smaller elements whose vertexes are the nodes of the mesh, while the latter implies a rectangular organization of the nodes. The framework described here is based on a rectangular grid of nodes, in which context both terms have essentially the same meaning.

The broad contributions of the work presented in this chapter include: 1) the modifications to the Particle Mesh method that generalize it for the case of non-flat space, and 2) the specific numerical experiments that showcase the framework and demonstrate that the Inherent Structure Hypothesis is a plausible explanation for the Dark Matter effect.

In the following sections, we describe the mathematical underpinnings of the numerical framework (the *Mathematical Model and Discretization* section) and what it does (the *Numerical Framework* section), and in the *Numerical Experiments* section we apply it to specific numerical experiments. In the *Discussion* section we comment on the important factors for the design of the framework and the experiments that are based on it. Finally, we summarize and conclude in the *Summary and Conclusion* section.

### Mathematical Model and Discretization

Our setup consists of a three-dimensional (3D) rectangular grid of nodes and a set of particles within the grid (see Figure 7.1). Various field quantities, such as density and curvature, can be assigned to each node of the grid and subsequently deduced for an arbitrary point in space by spline interpolation from the nearby node quantities. The inherent intrinsic curvature of space is specified via a displacement function, $\overline{w} = \overline{w}(x^i)$, like the one discussed in Chapter VI and visualized in Figure 6.1, except that here the displacement function is not necessarily spherically symmetric, but can vary independently in each coordinate direction.

![Particle-Mesh grid.](https://figures.tgtenev.com/tenev2018-dissertation/fig-grid.svg)

**Figure 7.1.** The grid nodes, indexed as $(a, b, c)$, are represented with round dots, while particles, indexed with subscript $p$, are represented as larger hollow disks. The indexes $i,j,k = 1\ldots 3$ run over the three spatial dimensions. Some of the quantities associated with the grid nodes and particles are also represented such as: $x^k\_{abc}$ (node position), $g\_{ij}(x^k\_{abc})$ (the metric tensor at location $x^k\_{abc}$), $x^i_p$ (the position of the $p^\text{th}$ particle) and $m_p$ (the mass of the $p^\text{th}$ particle). The spacing $h^1_a$ between the grid nodes in dimension 1 varies along that dimension, but remains constant along the remaining dimensions, and likewise for the spacings $h^2_b$ and $h^3_c$.

We will use the following notation:

- $\rho\_{abc}$: Latin subscripts in the alphabet range of $a, b, c$ are used to denote the grid indexes of the node to which the subscripted quantity applies, where $a = 1\ldots a\_\text{max}$, $b = 1\ldots b\_\text{max}$, and $c = 1\ldots c\_\text{max}$ on a grid of size $a\_\text{max} \times b\_\text{max} \times c\_\text{max}$ (see Figure 7.1). For example, $\rho\_{abc}$ means the mass density at grid node $(a, b, c)$.
- $m_p$: Latin subscript $p$ specifies the particle index. For example, $m_p$ is the mass of the $p^\text{th}$ particle, where $p = 1\ldots p\_\text{tot}$ and $p\_\text{tot}$ is the total number of particles.
- $x^i$: Latin indexes in the alphabet range of $i, j, k, l = 1\ldots 3$ correspond to the spatial components of vectors and tensors. For example, $x^i\_{abc}$ refers to the three spatial coordinates for the grid node $(a, b, c)$. Similarly, $x^i_p$ are the three spatial coordinates of the $p^\text{th}$ particle. Note that $\rho\_{abc} \equiv \rho(x^i\_{abc})$, because being a field quantity, $\rho$ is a function of the position $x^i$. This alternative way of denoting a field quantity helps with tensor notation where writing the node indexes as subscripts to the tensor quantity could be awkward. For example, $g\_{ij}(x^k\_{abc})$ denotes the value of the metric tensor $g\_{ij}$ at the node $(a,b,c)$.
- $x^\mu, \Gamma^{\mu}\_{\ \alpha\beta}$: As usual, Greek indexes $\mu,\nu, \alpha,\beta = 0\ldots 3$ run over the four spacetime dimensions with the $0^\text{th}$ dimension corresponding to time.

We consider a grid of dimensions $a\_\text{max} \times b\_\text{max} \times c\_\text{max}$, for which the spacing between the grid nodes is not necessarily uniform but is specified by the differences $h^1_a$, $h^2_b$, and $h^3_c$, where $a = 1\ldots (a\_\text{max}-1)$, and likewise for $b$ and $c$. In other words, $x^1\_{abc} = x^1\_{(a-1)bc} + h^1\_{(a-1)}$, and likewise for $x^2\_{abc}$ and $x^3\_{abc}$ (see Figure 7.1). The non-uniform spacing of the grid is useful when higher fidelity is needed at some locations but not others, such as the center of a gravitational system compared to its outskirts.

The following are the two governing differential equations, which are based on the Cosmic Fabric analogy of General Relativity under the conditions of weak gravity (small strain) and slow changing fields:

$$
\begin{split}
\ddot{x}^\alpha + \Gamma^{\alpha}\_{\mu\nu} \dot{x}^\mu \dot{x}^\nu = 0
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
g\_{\alpha\beta}\Gamma^{\alpha}\_{\mu\nu} = \frac{1}{2} \left( \partial\_\nu g\_{\mu\beta} + \partial\_{\mu} g\_{\beta\nu} - \partial\_\beta g\_{\mu\nu} \right),
\end{split}
\tag{7.3}
$$

and through the Time Lapse postulate of the Cosmic Fabric, which for weak gravity can be stated as follows (see Equation (3.7)):

$$
\begin{split}
g\_{00} \approx -1 + 2\varepsilon
\end{split}
\tag{7.4}
$$

where $\varepsilon$ is the volumetric strain of the fabric.

In the following subsections, we convert the above equations to a discretized form suitable for use in a numerical simulation. The goal is to be able to compute particle accelerations, so that we can evolve the system starting from a set of initial particle positions and velocities. We begin by developing the technique for discretizing first and second derivatives. Next we use this technique to discretize the metric and Christoffel symbols, the geodesic Equation (7.1), and the covariant Poisson Equation (7.2). Finally, we discuss how the density field quantity $\rho$ is computed for each grid node from the particle masses.

#### Discretization of First and Second Derivatives

We will use a three point stencil along each dimension to discretize the first and second partial derivatives. Following the approach outlined by Sundqvist and Veronis [156], let $f(x^i)$ be a field quantity and let $f\_{abc} = f(x^i\_{abc})$ be the specific values of this quantity assigned to each grid node. We seek to compute the values $\partial_i f\_{abc}$, and $\partial\_{ij} f\_{abc}$. Below, we do so using concrete values for $i$ and $j$ from which the generalization to any values of $i,j=1\ldots 3$ should be clear.

First, we compute the single and double derivatives, $\partial_i$ and $\partial\_{ii}$, respectively, for $i = 1$. Using the Taylor series expansions for $f\_{(a-1)bc}$ and $f\_{(a+1)bc}$ around the point $x\_{abc}$ we obtain the following two equations:

$$
\begin{split}
f\_{(a-1)bc} = f\_{abc} - h^1\_{(a-1)} \partial_1 f\_{abc} + \frac{\left(h^1\_{(a-1)}\right)^2}{2}\partial\_{11} f\_{abc} - \frac{\left(h^1\_{(a-1)}\right)^3}{6}\partial\_{111} f\_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.5}
$$

$$
\begin{split}
f\_{(a+1)bc} = f\_{abc} + h^1\_{a} \partial_1 f\_{abc} + \frac{\left(h^1\_{a}\right)^2}{2}\partial\_{11} f\_{abc} + \frac{\left(h^1\_{a}\right)^3}{6}\partial\_{111} f\_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.6}
$$

The third power term in the expansion is included to convey the error due to the approximation. By first solving the above two equations for $\partial_1 f\_{abc}$ and then for $\partial\_{11} f\_{abc}$ we obtain the following results:

$$
\begin{split}
\partial_1 f\_{abc} = d^1_a {f\_{(a+1)bc}}- e^1_a {f\_{(a-1)bc}} + (e^1_a - d^1_a){f\_{abc}} - \frac{h^1\_{(a-1)}h^1\_{a}}{6}\partial\_{111} f\_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.7}
$$

$$
\begin{split}
\partial\_{11} f\_{abc} &= 2 \left[\frac{d^1_a}{h^1\_{(a-1)}}f\_{(a+1)bc} + \frac{e^1_a}{h^1_a}f\_{(a-1)} - \left(\frac{d^1_a }{h^1\_{(a-1)}} + \frac{e^1_a}{h^1\_{a}}\right)f\_{abc}\right] \\
& - \frac{h^1\_{a} - h^1\_{(a-1)}}{3}\partial\_{111} f\_{abc} + \mathcal{O}(h^4)
\end{split}
\tag{7.8}
$$

where we have made the following substitutions:

$$
\begin{split}
d^1_a & \equiv \frac{h^1\_{(a-1)}}{(h^1\_{(a-1)} + h^1_a) h^1_a}, \  a = 2\ldots (a\_\text{max}-1); \quad d^1_1 \equiv \frac{1}{h^1_1}; \quad d^1\_{a\_\text{max}} \equiv 0 \\
e^1_a & \equiv \frac{h^1_a}{(h^1\_{(a-1)} + h^1_a) h^1\_{(a-1)}}, \  a = 2\ldots (a\_\text{max}-1); \quad e^1_1 \equiv 0 \quad e^1\_{a\_\text{max}} \equiv \frac{1}{h^1\_{(a\_\text{max}-1)}}
\end{split}
\tag{7.9}
$$

After dropping the high-order terms, we can write the finite difference approximations of the first and second derivative in terms of the operators $\Delta\_{1}$ and $\Delta\_{11}$ defined as follows:

$$
\begin{split}
\partial_1 f\_{abc} \approx \Delta_1 f\_{abc} \equiv d^1_a {f\_{(a+1)bc}}- e^1_a {f\_{(a-1)bc}} + (e^1_a - d^1_a){f\_{abc}}
\end{split}
\tag{7.10}
$$

$$
\begin{split}
\partial\_{11} f\_{abc} \approx \Delta\_{11} f\_{abc} \equiv 2 \left[\frac{d^1_a}{h^1\_{(a-1)}}f\_{(a+1)bc} + \frac{e^1_a}{h^1_a}f\_{(a-1)} - \left(\frac{d^1_a }{h^1\_{(a-1)}} + \frac{e^1_a}{h^1\_{a}}\right)f\_{abc}\right]
\end{split}
\tag{7.11}
$$

The discretization of $\partial_i$ and $\partial\_{ii}$ for $i = 2, 3$ can be computed analogously. The approximation of the second derivative in Equation (7.11) is known as the central differencing scheme.

Equations (7.10) and (7.11) show that the discretized derivative for a value at a node is some linear combination of the values at adjacent nodes. Based on this observation, we can replace the finite difference operators $\Delta_i$ and $\Delta\_{ii}$ with linear ones. Let us define:

$$
\begin{split}
n\_{abc} &\equiv 1 + a\_\text{max} b\_\text{max}(c-1) + a\_\text{max}(b-1) + (a-1) \\
n\_\text{max} & \equiv a\_\text{max} b\_\text{max} c\_\text{max} \\
F\_{n\_{abc}} &\equiv f\_{abc} \\
D^{(1)}\_{n\_{abc}n\_{(a+1)bc}} & \equiv d^1_a; \quad D^{(1)}\_{n\_{abc}n\_{(a-1)bc}} \equiv -e^1_a; \quad D^{(1)}\_{n\_{abc}n\_{abc}} \equiv e^1_a - d^1_a \\
D^{(11)}\_{n\_{abc}n\_{(a+1)bc}} & \equiv \frac{2d^1_a}{h^1\_{(a-1)}}; \quad D^{(11)}\_{n\_{abc}n\_{(a-1)bc}} \equiv \frac{2e^1_a}{h^1_a}; \quad D^{(11)}\_{n\_{abc}n\_{abc}} \equiv -\frac{2d^1_a }{h^1\_{(a-1)}} - \frac{2e^1_a}{h^1\_{a}}
\end{split}
\tag{7.12}
$$

and likewise for $D^{(i)}\_{nm}$ and $D^{(ii)}\_{nm}$ where $i = 2,3$ and $n, m = 1\ldots n\_\text{max}$. Note that the above definitions only apply when the indexes $(a,b,c)$ are within their respective bounds. So, for example, $D^{(1)}\_{n\_{abc}n\_{(a-1)bc}}$ is only defined for $a = 2\ldots a\_\text{max}$. The discretization of the mixed derivative $\partial\_{ij}$ for $i \neq j$, is simply the combination of the respective first derivatives:

$$
\begin{split}
D^{(ij)}\_{nm} = D^{i}\_{nt} D^{j}\_{tm}, i \neq j
\end{split}
\tag{7.13}
$$

where summation of repeated indexes is implied. Given the above definitions, Equations (7.10) and (7.11) can be formulated as follows:

$$
\begin{split}
F^{(i)}\_n &= D^{(i)}\_{nm} F_m \\
F^{(ij)}\_n &= D^{(ij)}\_{nm} F_m
\end{split}
\tag{7.14}
$$

where we have let $F^{(i)}\_{n\_{abc}} \equiv \Delta_i f\_{abc}$ and $F^{(ij)}\_{n\_{abc}} \equiv \Delta\_{ij} f\_{abc}$. Notice that the $D$ matrices only depend on the grid spacing and can therefore be precomputed during the preprocessing stage.

The method described above applies to computing field derivatives at the location of each grid node. In order to compute a field derivative of some field quantity at an arbitrary location, we would first compute the field derivative at the grid nodes and use spline interpolation to determine the value of the derivative at the given location.

#### Discretization of the Undeformed Metric and Christoffel Symbols

The undeformed metric and Christoffel symbols can be computed during the preprocessing stage from the following analytical formula:

$$
\begin{split}
\overline{g}\_{ij} &= \delta\_{ij} + \partial_i \overline{w} \partial_j \overline{w} \\
\overline{\Gamma}^{k}\_{\ ij} &= \frac{1}{2}\overline{g}^{kl}\left(\partial_j \overline{g}\_{il} + \partial_i \overline{g}\_{lj} - \partial_l \overline{g}\_{ij} \right).
\end{split}
\tag{7.15}
$$

where $\overline{w} = \overline{w}(x^i)$ is the displacement of the cosmic fabric into the fourth hyperspatial dimension, by which the user specifies inherent curvature (see Chapter VI). In discretized form, the above formula becomes the following:

$$
\begin{split}
G^{(ij)}\_n &= \delta\_{ij} + \left(D^{(i)}\_{nm}W_m\right)\circ(D^{(j)}\_{nm}W_m) \\
J^{(kij)}\_n &= \frac{1}{2}\mathrm{inv}\left[G^{(kl)}\_n\right]\circ \left( D^{(j)}\_{nm}G^{(il)}\_m + D^{(i)}\_{nm}G^{(lj)}\_m - D^{(l)}\_{nm}G^{(ij)}\_m \right)
\end{split}
\tag{7.16}
$$

where $G^{(ij)}\_{n\_{abc}}\equiv \overline{g}\_{ij}(x^k\_{abc})$, $W \equiv \overline{w}\_{abc}$, and $J^{(kij)}\_n \equiv \overline{\Gamma}^{k}\_{\ ij}(x^k\_{abc})$. Furthermore, the operator $\mathrm{inv}$ applies to $G$'s parenthesized indexes and represents a $3 \times 3$ matrix inversion, the binary operator $\circ$ represents element-wise multiplication *with respect to the unparenthesized indexes*, summation over repeated indexes is implied, and the $D$ matrices are defined per Equations (7.12) and (7.13). Note that the element-wise multiplication of vector elements that is represented by the binary operator $\circ$ can be substituted with regular matrix multiplication provided that the vectors are treated as diagonal matrices with the diagonal elements being the vector elements.

#### Discretization of the Geodesic Equation

The geodesic equation is used to compute particle acceleration for a given gravitational field. Using the chain rule, we can rewrite Equation (7.1) to be in terms of coordinate time instead of proper time:

$$
\begin{split}
\partial\_{00} x^{\mu} = -\Gamma^{\mu}\_{\ \alpha\beta}\partial_0 x^\alpha \partial_0 x^\beta + \Gamma^0\_{\ \alpha\beta}\partial_0 x^\alpha \partial_0 x^\beta \partial_0 x^\mu
\end{split}
\tag{7.17}
$$

For simulation purposes, we need to use a notion of time that is common to all particles, but proper time is by definition particle-specific. This is why we work in terms of coordinate time. Thus, $\partial\_{00} x^{\mu}$ is the $\mu^\text{th}$ component of the particle's coordinate acceleration, while $\partial_0 x^\mu$ is the $\mu^\text{th}$ component of the particle's coordinate velocity. Notice that for $\mu = 0$ (acceleration in the time direction), both sides of Equation (7.17) vanish identically since $\partial_0 x^0 = 1$, because the speed of coordinate time is always one second per second. In fact, we are only interested in the spatial components of the particle acceleration, $\partial\_{00}x^k$.

In the case of slow changing fields, the time derivatives, $\partial_0$, of field quantities and the time-space components of the metric, $g\_{i0}$ and $g\_{0i}$, are all negligible. Consequently, some of the Christoffel symbols vanish and the remaining ones are as follows:

$$
\begin{split}
\Gamma^0\_{\ i0} &= \Gamma^0\_{\ 0i} = \frac{\partial_i g\_{00}}{2g\_{00}};\quad \Gamma^0\_{00} = \Gamma^0\_{ij} = 0 \\
\Gamma^k\_{00} &= -\frac{1}{2}g^{kl}\partial_l g\_{00}; \quad \Gamma^{k}\_{\ i0} = \Gamma^{k}\_{\ 0i} = 0 \\
\Gamma^{k}\_{\ ij} &= \frac{1}{2}g^{kl}\left(\partial_j g\_{il} + \partial_i g\_{lj} - \partial_l g\_{ij} \right),
\end{split}
\tag{7.18}
$$

which when substituted into Equation (7.17) and evaluated for the spatial components of the particle acceleration, produce the following:

$$
\begin{split}
\partial\_{00} x^k &= -\Gamma^k\_{\ 00}(\partial_0 x^0)^2 + 2 \Gamma^0\_{\ 0i}\partial_0 x^k \partial_0 x^i - \Gamma^k\_{\ ij} \partial_0 x^i\partial_0 x^j \\
& = \frac{1}{2}g^{kl}\partial_l g\_{00} + \frac{\partial_i g\_{00}}{g\_{00}}\partial_0 x^i \partial_0 x^k - \Gamma^k\_{\ ij} \partial_0 x^i\partial_0 x^j
\end{split}
\tag{7.19}
$$

Notice that although we have assumed that the fields are slow changing, we do not assume that particle velocities are slow, but that individual particles could achieve speeds comparable to $c$. Therefore, while we can approximate the time derivatives of field quantities as vanishing, we do not make the same approximation for the time derivatives of particle quantities. In a typical configuration, such as a galaxy, the total gravitational field is the combined effect of a large number of particles (billions of stars), so as long as the collection of particles as a whole moves slowly through space, then the motion of individual particles (stars) will not cause the gravitational field to change rapidly except in its immediate vicinity.

Next, we invoke the weak gravity (small strain) assumption to approximate the spatial curvature of the deformed fabric with that of the undeformed one: $g\_{ij} \approx \overline{g}\_{ij}$ and $\Gamma^k\_{\ ij} \approx \overline{\Gamma}^k\_{\ ij}$. Furthermore, from Equation (7.4) follows that $\partial_l g\_{00} \approx 2\partial_l \varepsilon$. Finally, we recognize that since $x^0 = ct$, where $t$ is coordinate time, then $a^k = c^2 \partial\_{00} x^k$ and $v^k = c \partial_0 x^k$, where $a^k$ and $v^k$ are, respectively, the particle's coordinate acceleration and velocity. When these substitutions are made into Equation (7.19), we arrive at the following formula for the acceleration $a^k$:

$$
\begin{split}
a^k = c^2\overline{g}^{kl} \partial_l \varepsilon - \frac{2 \partial_i \varepsilon}{1 - 2\varepsilon} v^i v^k - \overline{\Gamma}^k\_{\ ij}(x^k) v^i v^j
\end{split}
\tag{7.20}
$$

Note that in the absence of intrinsic curvature ($\overline{g}^{ij} = \delta^{ij}$) and for the case of slow particle velocities ($v^i \ll c$) the last two terms vanish. Moreover, per Equation (3.27), $\varepsilon = -\Phi/c^2$, so Equation (7.20) becomes the classical equation for gravitational acceleration: $a^k = -\partial^k \Phi(x^k)$. Notice also that in the case when a particle's velocity is a non-negligible fraction of the speed of light, then the second term in Equation (7.20) reduces the coordinate acceleration, which prevents the particle from achieving superluminal speed. This is why accounting for this term is important for the numerical simulation. Finally, the last term represents the influence of the inherent (undeformed) curvature on the acceleration computation for the case of fast particles.

The discretized version of the particle acceleration Equation (7.20) can now be derived and is as follows:

$$
\begin{split}
A^{(k)}\_p = \left. c^2 \mathrm{inv}\left[G^{(kl)}\_n\right]\circ D^{(l)}\_{nm}E_m \right|\_p - \left. \frac{2 D^{(i)}\_{nm} E_m}{1 - 2 E_n}\right|\_p \circ V^{(i)}\_p \circ V^{(k)}\_p - \left. J^{(kij)}\_n \right|\_p \circ V^{(i)}\_p \circ V^{(j)}\_p
\end{split}
\tag{7.21}
$$

where $E_n$ is an $n$-component vector, such that $E\_{n\_{abc}} \equiv \varepsilon\_{abc}$. Furthermore, $V^{(k)}\_p$ and $A^{(k)}\_p$ are, respectively, the velocity and acceleration components of the $p^\text{th}$ particle. The notation $\left.X\right|\_p$ means that the quantity $X$ should be interpolated from its grid node values for the location of the $p^\text{th}$ particle. The division operation in the second term of the above expression should be understood as element-wise.

#### Discretization of the Poisson Equation

Given the following expansion of the covariant Laplace operator in terms of the metric and Christoffel symbols,

$$
\begin{split}
\nabla_i (\nabla^i \varepsilon) = \overline{g}^{ij}\left( \partial\_{ij} - \overline{\Gamma}^k\_{\ ij} \partial_k \right)\varepsilon
\end{split}
\tag{7.22}
$$

the Covariant Laplacian $\nabla_i (\nabla^i \varepsilon)$ is discretized as follows:

$$
\begin{split}
L\_{nm} \equiv \mathrm{inv}\left[G^{(ij)}\_n\right]\circ \left(D^{(ij)}\_{nm} - J^{(kij)}\_n \circ D^{(k)}\_{nm} \right)
\end{split}
\tag{7.23}
$$

where the matrix inversion is with respect to the upper indexes $(ij)$.

Discretizing the Poisson Equation (7.2) requires that we take into account the following boundary conditions,

$$
\begin{split}
\varepsilon\_{abc} = \varepsilon^{\*}\_{abc}, \quad \text{for boundary nodes } (a,b,c)
\end{split}
\tag{7.24}
$$

where a "boundary node" $(a, b, c)$, as opposed to an "interior node" is one for which at least one of the following is the case: $a \in \lbrace 0, a\_\text{max}\rbrace \text{ or } b \in \lbrace 0, b\_\text{max}\rbrace, \text{ or } c \in \lbrace 0, c\_\text{max}\rbrace$. Furthermore, the strains $\varepsilon^{\*}\_{abc}$ stand for user-specified boundary quantities. Consequently, we arrive at the following discretization for the Poisson Equation:

$$
\begin{split}
&Q\_{nm} E_m = S_n \\
&\quad \text{where} \\
& \quad Q\_{n\_{abc}m} \equiv \begin{cases}
L\_{n\_{abc}m}, & \text{when } (a,b,c) \text{ is an interior node} \\
1, & \text{when } (a, b, c) \text{ is a boundary node}
\end{cases} \\
& \quad S\_{n\_{abc}} = \begin{cases}
-\frac{1}{2}c^2\kappa \rho\_{abc}, & \text{when } (a,b,c) \text{ is an interior node} \\
\varepsilon^{\*}\_{abc}, & \text{when } (a,b,c) \text{ is a boundary node}
\end{cases} \\
& \quad E\_{m\_{abc}} = \varepsilon\_{abc}
\end{split}
\tag{7.25}
$$

Solving Equation (7.25) amounts to solving a linear system of $n$ equations where the matrix $Q\_{nm}$ is sparse and banded. A banded matrix consists of a main diagonal and $m$ pairs of secondary diagonals that are parallel to the main one within a narrow band. An optimal solver for such type of matrices can compute the solution within $\mathcal{O}(m^2 n\_\text{max})$ time. For the case of flat geometry, $m = 3$, but could be as large as $m = 13$ for non-flat geometry. Numerical platforms, such as MATLAB®, have built-in routines to perform just this type of calculation. Notice also that the matrix $Q\_{nm}$ in Equation (7.25) can be computed during the preprocessing stage.

#### Density Computation

The matter density, which figures as the source in the Poisson Equation (7.2) and in its discretized version in Equation (7.25), is computed from the following two sources: 1) predefined fixed matter density associated with each node, and 2) density due to the particle distributions, which may vary from one time step to another. The former is specified directly by the user as part of setting up a numerical experiment; the computation of the latter is described below. These two are added together to produce the total density and its value is assigned to each grid node.

Each particle contributes to the matter density value associated with the grid nodes in its immediate neighborhood. Let $\Omega\_{abc}$ represent the rectangular space bounded by eight adjacent grid nodes such that two of them are $(a, b, c)$ and $(a+1, b+1, c+1)$, and let $p \in \Omega\_{abc}$ denote the fact that the $p^\text{th}$ particle is located somewhere within $\Omega\_{abc}$. Define $\xi^1_a \equiv x^1_p - x^1\_{abc}$ to denote the coordinate differences between the coordinates of the particle and the node $(a, b, c)$, and likewise for $\xi^2_b$ and $\xi^3_c$. Therefore, the following expression $(1 - \xi^1_a/h^1_a)(1-\xi^2_b/h^2_b)(1-\xi^3_c/h^3_c)$ represents the fraction of the particle's mass that will be ascribed to node $(a, b, c)$, while $(\xi^1_a/h^1_a)(\xi^2_b/h^2_b)(\xi^3_c/h^3_c)$ is the fraction of mass ascribed to node $(a+1, b+1, c+1)$, and so on for the other six nodes that are the vertexes of $\Omega\_{abc}$. Note that the sum of all such fractional contributions is unity.

To compute the mass density $\rho\_{abc}$ at a given node $(a,b,c)$, we will consider all of the particles' contributions from the eight adjacent spaces, $\Omega\_{(a-1)(b-1)(c-1)}, \Omega\_{a(b-1)(c-1)}\ldots \Omega\_{abc}$. Therefore,

$$
\begin{split}
\rho\_{abc} &= \rho^{\*}\_{abc} + \frac{8}{\mathcal{V}\_{abc}} \left\lbrace  \sum\_{p\in \Omega\_{(a-1)(b-1)(c-1)}} m_p \frac{\xi^1\_{(a-1)}}{h^1\_{(a-1)}}\frac{\xi^2\_{(b-1)}}{h^2\_{(b-1)}}\frac{\xi^3\_{(c-1)}}{h^3\_{(c-1)}} \right. \\
& +\sum\_{p\in \Omega\_{a(b-1)(c-1)}} m_p \left(1 - \frac{\xi^1\_{a}}{h^1\_{a}}\right)\frac{\xi^2\_{(b-1)}}{h^2\_{(b-1)}}\frac{\xi^3\_{(c-1)}}{h^3\_{(c-1)}} + \ldots \\
& \left. +\sum\_{p\in \Omega\_{abc}} m_p \left(1 - \frac{\xi^1\_{a}}{h^1\_{a}}\right) \left(1 - \frac{\xi^2\_{b}}{h^2\_{b}}\right) \left(1 - \frac{\xi^3\_{c}}{h^3\_{c}}\right) \right\rbrace \\
& \text{where} \quad \mathcal{V}\_{abc} \equiv \sqrt{\overline{g}\_{abc}}\ (h^1\_{(a-1)} + h^1_a)(h^1\_{(b-1)} + h^1_b)(h^1\_{(c-1)} + h^1_c)
\end{split}
\tag{7.26}
$$

where $\mathcal{V}\_{abc}$ represents the proper volume of the rectangular space bounded by the nodes $(a-1, b-1, c-1)$ and $(a+1, b+1, c+1)$ that is made up of the eight smaller rectangular spaces each of which corresponds to a summation expression in Equation (7.26). Furthermore, $\overline{g}\_{abc} \equiv \det \overline{g}\_{ij}(x^k\_{abc})$, and $\rho^{\*}\_{abc}$ is the fixed density at node $(a,b,c)$ that has been pre-assigned by the user. Note that $\mathcal{V}\_{abc}$ can be computed during the preprocessing stage.

We have found out that the precision of the particle density calculation worsens with larger variations of the grid spacing. For such situations, we use an auxiliary grid of uniform spacing at whose nodes we calculate the particle densities by the above scheme. Then, we interpolate the resulting values onto the nodes of the main grid. The number of nodes in this auxiliary grid can be much larger than those of the main grid, because it does not affect the solving of the Poisson Equation, which is typically the most time consuming step of the simulation.

### Numerical Framework

Using MATLAB®, we implemented a numerical framework based on the mathematical model discussed in the *Mathematical Model and Discretization* section. Its features allow the user to define and run numerical experiments in weak gravity under conditions of various kinds of intrinsic curvature (or none) that may involve point particles or gravitating mass densities or both. The difference between point particles and mass densities is that the former are modeled as having no spatial extent but can move, while the latter occupy finite volume but are fixed. Point particles and mass densities interact indirectly with each other through the gravitational field in whose creation they participate. The framework does not model direct interaction such as collision or friction between particles and densities.

There are two broad categories of numerical experiments that can be performed with the framework: 1) static evaluation of gravitational fields, and 2) time evolution of point particles. For experiments in the first category, the Poisson equation of gravity, Equation (7.25), is solved once and the resulting gravitational field is analyzed. The experiments presented in the *Numerical Experiments* section fall into this category. For the second category of experiments, the Poisson Equation is solved once for each time step. At each iteration, the volumetric strain, which is the solution of the Poisson Equation, is used to compute the accelerations of the point particles and update their positions and velocities.

#### Input Parameters

The following are the input parameters that specify a numerical experiment within the framework:

1. Configuration of a three-dimensional rectangular mesh that has $a\_\text{max} \times b\_\text{max} \times c\_\text{max}$ nodes and represents a volume of space that is $|x^1\_\text{max} - x^1\_\text{min}| \times |x^2\_\text{max} -x^2\_\text{min}| \times |x^3\_\text{max} - x^3\_\text{min}|$ large. The nodes along each edge need not be evenly spaced, so some parts of the mesh can be finer than others. The framework allows edge nodes to be distributed linearly, quadratically, or cubicly within user-specified ranges. In the latter cases, the points are denser in the middle of a range and less so near its two ends according to a quadratic or cubic function, respectively.
2. Intrinsic curvature defined in terms of the function $w = w(x^1, x^2, x^3)$, which is the displacement into the fourth (hyperspatial) dimension.
3. A set of fixed mass density distributions, such as those representing large gravitating bodies or dust clouds.
4. A set of point particles specified in terms of their masses $m_p$ where $p = 1\ldots p\_\text{tot}$ and $p\_\text{tot}$ is the total number of particles, their initial positions $x^i_p$ and velocities $v^i_p$.
5. Boundary conditions specifying the volumetric fabric strain at the edge nodes and face nodes of the mesh. (In the current implementation, the boundary values of the volumetric strain are assumed to approximately vanish, which is generally true if the mesh is made large enough such that gravitating masses are near the center of the mesh.)

#### Preprocessing Stage

During the preprocessing stage, the framework builds the grid illustrated in Figure 7.1, computes the derivative matrices $D^{(i)}\_{nm}$ and $D^{(ij)}\_{nm}$ (see the *Discretization of First and Second Derivatives* section), which are then used to compute the metric $G^{(ij)}\_{n}$ and the Christoffel symbols. Finally, the $Q\_{nm}$ matrix is computed (see the *Discretization of the Poisson Equation* section) that is used in the solution of the Poisson equation. At this stage, the framework also pre-computes the velocity-independent coefficients in the geodesic Equation (7.21), which is used during the Solving Stage to evaluate particle accelerations. Some of these preprocessing operations are computationally expensive and being able to perform them ahead of time and not at each iteration during the solving stage is important for the efficiency of the algorithm.

#### Solving Stage

The Solving Stage begins by computing the aggregate density distribution of matter within the mesh, which consists of accounting for particle density and user-inputted fixed densities as described in the *Density Computation* section. This aggregate density (from point particles and fixed density) figures in the right-hand side of the Poisson Equation (7.25). Solving Equation (7.25) is at the heart of the solving stage and is the most computationally intensive step. MATLAB®, which is the engine running our framework, uses a set of heuristics to decide the best way to solve the linear system of equations [101]. In our case, since the $Q\_{mn}$ matrix is banded, a banded solver is used. In the current implementation of the framework, we assume that the grid is always constructed large enough so that the strain at the boundary is nearly vanishing. In other words, we assume that in Equation (7.25) the quantities $\varepsilon^{\*}\_{abc} = 0$.

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

where `obj` refers to the simulation object instance, while `px`, `pv`, and `pa` are MATLAB®'s representation of the $x^i_p$, $v^i_p$ and $a^i_p$ vectors corresponding, respectively, to the particles' positions, velocities, and acceleration. For example, `px{1}` is represented numerically as a vector of $p\_\text{tot}$ elements where the $p^\text{th}$ element corresponds to the $x^1$ coordinate of the $p^\text{th}$ particle and so on.

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
-\frac{4}{3}\pi G \rho\_\odot r, & r \le r\_\odot \\
-G M\_\odot r^{-2}, & r > r\_\odot
\end{cases}
\end{split}
\tag{7.27}
$$

where $r$ represents the distance from the Sun's center, and $M\_\odot$, $\rho\_\odot$, and $r\_\odot$ are its mass, mass density, and radius, respectively. Figure 7.3 (right) shows a comparison between the theoretical acceleration and that which has been simulated. The discrepancy between theory and simulation is very small both in the vicinity of the Sun as well as at distances comparable to the Sun-Earth distance.

![Fabric strain and acceleration due to the Sun.](https://figures.tgtenev.com/tenev2018-dissertation/fig-sun.svg)

**Figure 7.3.** Panel (a) shows the variation of density $\rho$ and the fabric's volumetric strain in the vicinity of the Sun. Panels (b) and (c) compare the theoretical value for the gravitational acceleration due to the Sun with the simulated value that was output from simulating the Sun's gravity. The comparison is shown within two radial ranges: in the vicinity of the Sun (b), and in the vicinity of the Earth (c). The mesh used in this experiment had $58\times 58\times 58 = 195,112$ nodes.

#### Modeling the Effect of Inherent Curvature on the Gravity of Messier 33

We now apply the framework to investigating the Inherent Structure Hypothesis (see Chapter VI) as a possible explanation for the Dark Matter Effect. We do so by considering the rotational velocity curve (or "rotation curve" for short) of a given galaxy for the cases of with- and without inherent curvature. For the following experiment, we chose the Triangulum galaxy, also known as Messier 33 (M33), because it is a relatively well studied subject for the Dark Matter effect [35, 36, 37, 147], which effect is inferred from the rotation curve of the galaxy. For example, Figure 5 in Corbelli [35] shows the rotation curve of M33 decomposed into contributions due to the stellar disk, galactic gases, and the hypothetical dark matter. It is clear from this and similar other figures in the literature that based on the contributions from ordinary matter alone (stars and gases), rotational velocities are expected to begin to decline after some distance from the center. By contrast, measurements show that rotational velocities tend to increase monotonically with their distance from the galactic center. Such a discrepancy is commonly attributed to the presence of dark matter.

About two thirds of the ordinary (visible) matter of M33 resides in the stellar disk, while the remaining third is in the form of molecular and atomic Hydrogen. For the experiment herein, we used the total surface density data reported in Figure 10 of Corbelli et al. [37], which we have plotted at the bottom panels of Figure 7.4. Because most galaxies are thin disks, as is the case with M33, it is customary to report their matter density as surface density in units of solar masses per square parsecs ($M\_\odot/\text{pc}^{2}$). For the purposes of the numerical simulation, however, we need volume density. Therefore, following Ciardullo et al. [32] we have assumed a constant galactic half-thickness of $z\_{\*} = 175\ \text{pc}$. As Saburova and Zasov [147] point out, such constant thickness is an idealization, but for the purposes of our comparison we assume that the effects of varying transverse thickness are insignificant.

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

where `@mesh.spaceCube` and `@mesh.spaceLinear` specify the manner of distributing the points along each edge. A linear distribution spaces the nodes evenly, but a cubic distribution concentrates more nodes near the center and less near the ends of the specified range. The M33 object was introduced into the mesh as a cylindrical density of uniform half-thickness $z\_{\*} = 175\ \text{pc}$.

Figure 7.4 and Figure 7.5 show the results of the computation in terms of the cosmic fabric strain and the galaxy rotation curve, respectively. The rotational velocities $v$ plotted in Figure 7.5 were calculated using the formula,

$$
\begin{split}
\frac{v^2}{r} = a^1\_\text{proper} = \frac{a^1}{\sqrt{g\_{11}}}, \quad a^1 = c^2\overline{g}^{1i}\partial_i \varepsilon
\end{split}
\tag{7.28}
$$

where $a^1\_\text{proper}$ is the proper radial acceleration and $a^1$ is the coordinate radial acceleration that were measured in the $x^1$ direction. The last equality is an approximation of Equation (7.20), in which the velocity terms are treated as insignificant on the assumption that rotation velocities are much less than the speed of light, which is the case here.

![Fabric strain due to the M33 galaxy.](https://figures.tgtenev.com/tenev2018-dissertation/fig-m33-strain.svg)

**Figure 7.4.** Fabric strain due to the M33 galaxy without (a) and with (b) inherent curvature. The top panels visualize a quadrant of the strain field, while the bottom panels show the density and strain profiles. The density profile used here is from Figure 10 of Corbelli et al. [37].

![Rotation curve of the M33 galaxy.](https://figures.tgtenev.com/tenev2018-dissertation/fig-rot-v.svg)

**Figure 7.5.** The top panel shows M33's observed rotation curve [35] along those computed with and without inherent curvature. The inherent curvature was specified by a radially symmetric hyperspatial displacement $w = w(x^i)$ (bottom panel) that produces MOND-equivalent effect per Equation (6.33). The displayed fit was achieved with a scale mass of $M = 10^{11} M\_\odot$, which is about $10\times$ the mass of M33. The bottom panel also shows $\sqrt{g\_{11}}$ which represents the ratio between the proper distance element $dl$ and the coordinate element $dx^1$.

These results illustrate that for an appropriately chosen inherent curvature, the simulated velocity curve fits well with the data. The fit is quite good although there was only one parameter to adjust for choosing the inherent curvature (the scale mass $M$). In principle, the inherent curvature is free to have any shape provided it is geometrically consistent (no kinks, intersects or tears), so an even better fit could be achieved when a more detailed relief is chosen for the inherent spatial structure.

### Discussion

The following factors are important in the design of the numerical framework and experiments: trade-off between reducing numerical errors versus reducing computational costs; avoiding numerical instability, and ensuring convergence. Below we discuss how each of these factors has been addressed.

Achieving optimal trade-off between reduction of numerical errors and computational cost relies on understanding the sources of errors. For example, one such source is imprecision of the input data. It would be computationally wasteful to try to achieve numerical precision that is higher than the input precision. Another source of error is the defeaturing (idealization) of modeled entities. Reducing this error involves using more grid nodes at the location of the entity whose feature we want to express. For example, the accurate modeling of the Sun as part of the validation experiment in the *Numerical Experiments* section required that more mesh nodes were introduced in its vicinity compared to the rest of the grid. The discretization of derivatives per Equations (7.7) and (7.8) introduces numerical errors by omitting higher order terms that depend on the grid spacing. Notably, for the discretization of the second derivative, the error is linear in terms of the difference between adjacent grid spacing values. So, one must be careful not to vary the grid spacing too suddenly. Finally, numerical errors are also introduced during the post processing stage when the output from the solver is often interpolated to extract meaningful outcome.

Numerical instability is a unique source of errors, which is manifested when a small perturbation in the input leads to dramatic changes in the output. We have found such instability to arise, for example, when the $Q$ matrix that is constructed in the solution of the Poisson Equation is poorly scaled. This can happen if the numerical values of the boundary coefficients, which are set to unity per Equation (7.25), differ by many orders of magnitude from the coefficients in the $L$ matrix. To avoid this problem, we first scale all interior node coefficients $Q\_{mn}$ by some fixed scale factor before setting the boundary node coefficients to unity, and then apply this scale factor to the outcome from solving the Poisson equation. Pathological choice for the location of grid nodes can be another cause of numerical instability, such as placing them close to a location at which the node values would be singular or nearly so.

Ensuring convergence means achieving grid fidelity beyond which adding more nodes does not qualitatively change the result of the computation, but only incrementally increases its precision. Without ensuring convergence, the meaningfulness of the numerical results is questionable. To check convergence for a given number of mesh nodes, we rerun the same calculation with fewer number of nodes and note whether the result changes qualitatively. If the precision of the result is only incrementally decreased, then we assume to have achieved convergence.

Understanding the physics of the modeled variables also helps achieve optimal trade-off between reducing error and computational cost. For example, the error in Equations (7.7) and (7.8) depends on the third derivative of the differentiated quantity, which happens to be the volumetric strain $\varepsilon$ in the case of solving the Poisson Equation. Since $\varepsilon$ diminishes approximately as the inverse distance to the center of the gravitating system, therefore the error will be diminishing as the inverse cube of the distance from the center of the system. This enabled us to use cubic distribution for the edge nodes, whereby node spacing increases proportional to the square of the distance to the center.

For the category of numerical experiments where time is involved, the choice of the time step must also be considered. We use an explicit method for computing the time evolution of the system, which means that the future configuration is computed from the current one. For this type of computation, the Courant–Friedrichs–Lewy (CFL) condition [136] limits the size of the time step $\Delta t$, such that $\Delta t \le h/c$, where $h$ is the characteristic grid spacing and $c$ is the speed of signal propagation, which in our case is the speed of light. An implication of the CFL condition is that whenever the grid is refined by reducing $h$, the time step $\Delta t$ must also be reduced to ensure that the simulation remains convergent. Such coupling between the spatial spacing and the time step results in higher computational cost.

### Summary and Conclusion

We presented a working numerical framework for investigating the dynamics of gravitational systems in the regime of weak gravity. The framework is suited to studying the Dark Matter effect in the context of the Inherent Structure Hypothesis discussed in Chapter VI. It uses the Finite Differences Method to solve the Covariant Poisson equation, which lets it account for the effects of inherent spatial curvature.

The proper functioning of the framework was validated by modeling the gravity of the Sun and comparing the result to the prediction of Newtonian gravity. The result was within 16% of the theoretical prediction for a relatively coarse mesh of $60\times 60\times 60$ nodes. More accurate results can be achieved in the future at the expense of more computational power (both CPU and memory).

The framework was applied to studying the effect of inherent curvature on the gravity of stellar object Messier 33 (M33), which is also known as the Triangulum Galaxy. The results, which are visualized in Figure 7.4 and Figure 7.5, demonstrated that the presence of inherent curvature does in fact cause the galaxy rotation velocities to monotonically increase with distance from the center in a manner similar to the effect of a hypothetical dark matter halo. Furthermore, for an appropriately chosen inherent curvature, the simulated rotation curve fitted well the observational data. This result validates the ideas presented in Chapter VI.

The primary goal of the work presented in this chapter was the development of the numerical framework, while conducting numerical experiments based on it was a secondary goal. Although the experimental results were promising, future work is needed for a thorough assessment of their significance and for better quantification of the error by accounting for uncertainties in the input data. The framework should be extended to allow for more flexible specification of the boundary conditions, and a greater variety of galactic shapes and inherent curvatures should be investigated.

---

---

[Contents](../tenev2018-dissertation.md)  &nbsp;•&nbsp;  [&#9664; Dark Matter Effect](ch6-dark-matter-effect.md)  &nbsp;•&nbsp;  [Conclusions &#9654;](ch8-conclusions.md)
