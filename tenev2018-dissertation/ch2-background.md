[&#8592; Contents](../tenev2018-dissertation.md)

# II. Background

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
\Delta x^i = b^i - a^i, \quad i = \lbrace 1,2\rbrace
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

where the coefficients $g_{ij}, i,j=\lbrace 1,2\rbrace$ are called the *metric*. It is possible to show that these coefficients obey tensor transformation rules under change of basis and thus show that they are the components of a tensor $\mathbf{g}$ known as the *metric tensor*. Being a tensor means that $\mathbf{g}$ represents a quantity that is independent of the choice of basis so that only the specific representation of $\mathbf{g}$ in terms of its components $g_{ij}$ depends on the basis.

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
(ds)^2 = d\mathbf{x}^T\mathbf{g}\ d\mathbf{x}
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
g_{ij} = \mathbf{e_i}\cdot\mathbf{e_j}, \quad i,j = \lbrace 1,2\rbrace
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
= d\mathbf{x}^T \mathbf{g}\  d\mathbf{y}
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
\eta_{00}=-1, \  \eta_{0i}=\eta_{i0}=0, \  \eta_{ij} =\delta_{ij} \quad (i,j=1\ldots 3)
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

**Figure 2.1.** A line segment $ds$ in skewed Cartesian (a) and spherical (b) coordinates. The metric for case (a), when the basis are unit vectors subtending some angle $\theta$ with each other, is $ds^2 = (dx^1)^2 + (dx^2)^2 + 2dx^1 dx^2 \cos \theta$. For case (b) of the coordinates $(\theta, \varphi)$ for the surface of a sphere with radius $R$, the metric is $ds^2 = R^2 d\theta^2 + R^2 \sin^2 \theta\  d\varphi^2$.

Just as with the previous example of Cartesian coordinates, the current one also involves a flat (Euclidean) space and yet the metric tensor's representation is no longer one and the same as the identity tensor. That is because the metric tensor's representation depends on the choice of basis vectors. At the same time, in both of the above cases the metric is constant throughout space.

In spherical coordinates, the great circles serve as coordinate axes and, as illustrated in Figure 2.1b, the square length $ds^2$ of an infinitesimal line segment can be computed as follows:

$$
\begin{split}
ds^2 = R^2 d\theta^2 + R^2 \sin^2 \theta\  d\varphi^2
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
& a_P = \sqrt{g_{rr}}\ \ddot{r} = c^2\frac{\partial_r g_{00}}{2 \sqrt{g_{rr}}}
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

---

[Contents](../tenev2018-dissertation.md)  &nbsp;•&nbsp;  [&#9664; Introduction](ch1-introduction.md)  &nbsp;•&nbsp;  [Cosmic Fabric Model of Gravity &#9654;](ch3-cosmic-fabric-model.md)
