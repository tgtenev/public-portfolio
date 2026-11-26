# The Dark-Matter Effect in the Cosmic Fabric Model. II. The Field Theory and the Kinetics of the Law for Galaxies

**Document Metadata**

| | |
|---|---|
| **Store** | public-portfolio |
| **Publication** | Preprint, Zenodo, 2026 |
| **Published** | 2026-11-26 (Zenodo v1) |
| **DOI / URL** | https://doi.org/10.5281/zenodo.24533993 — concept DOI, cite this one for all versions; this version is 10.5281/zenodo.24533994 |
| **Licence** | CC BY 4.0 |
| **Cite as** | T. G. Tenev, "The dark-matter effect in the Cosmic Fabric Model. II. The field theory and the kinetics of the law for galaxies," Zenodo, preprint, 2026, doi: 10.5281/zenodo.24533993. |
| **Converted from** | research-workbench `cfm-dark-sector/cfm-dme-2.md`, commit `ad73e5a` (v27) — the Markdown from which the deposited PDF was built |

---

**T. G. Tenev**\*

\* Corresponding author: Tichomir G. Tenev, Ph.D., ticho@tenev.com

## Abstract

We complete the algebraic galaxy-scale law that Paper I derives from the renewal of a growing elastic space in the Cosmic Fabric Model, deriving its field theory and kinetics and computing its material constant for an example microstructure.
To explain the regularity that modified Newtonian dynamics (MOND) describes, such a law must hold beyond spherical symmetry and produce lensing from the same field.
Adding three identifications and no postulate, we homogenize the crimped microstructure into a strain-transmission tensor, derive a relaxation time and simulate avalanche kinetics on a lattice.
A new layer is taken as laid across the flux that the tensor transmits.
The tensor's axis then aligns with the field, a fixed point whose stability is shown for a uniform axis.
Once aligned, the field equation, well posed wherever the tensor is bounded and positive, is that of the aquadratic-Lagrangian theory.
Lensing equals the dynamics at linear order, in static fields by Paper I and in changing fields by the same law on each slice.
Below the catchment length, a renewal event's range of sensing, the Solar System and wide binaries keep their own fields Newtonian, while MOND predicts anomalies.
In disks the full solution departs from the algebraic relation by 0.06 dex rms and fits the rotation curves worse than it, by 1.7 to 2.0 standard deviations, as MOND's interpolation functions do when solved in full.
With both solved in full on the Newtonian field computed here, MOND's simple function fits better than the law by 2.7 standard deviations, and on SPARC's tabulated field by 0.7.
These preferences fall below one standard deviation if the stellar mass-to-light priors are centered 20 percent higher, at the edge of their normalization's uncertainty.
The equilibration time lies between an adopted $`10^3`$ yr, setting a floor of 58 pc on the catchment length, and a derived $`5.2\times10^4`$ yr.
Globular clusters with rich kinematics show no rise with the boost that an ambient-stretch coupling would give them, a slope of $`-0.20 \pm 0.08`$ against $`+1`$.
Ultra-faint dwarfs show dispersions an order of magnitude and more above the screened prediction, a surplus the law does not supply.
At a stand-in trigger scale, a simulated unit selected against the fitted divisor of the de Sitter acceleration gives a free volume of 0.188 and a divisor of 5.81, inside Paper I's 68 percent ranges, a consistency check only.
Composite mechanics and glass physics extend here to galaxy dynamics, whose acceleration scale rests on constants of the kinds measured in glasses.

## 1. Introduction

The rotation curves of disk galaxies follow a near-deterministic function of the visible baryons.
In the Spitzer Photometry and Accurate Rotation Curves (SPARC) database [1], thousands of measurements fall on one curve, the radial-acceleration relation (RAR) [2], with an intrinsic scatter below 0.057 dex and no second parameter [3], as in the central-density relation [4].
Its single acceleration scale, $`a_0 \approx 1.2\times10^{-10}\ \mathrm{m\ s^{-2}}`$, lies within a factor of order unity of $`cH_0`$, the acceleration set by the present expansion rate $`H_0`$ [5].
An explanation must derive both this curve and its scale within a law that holds beyond spherical symmetry and yields lensing from the same field.

Modified Newtonian dynamics (MOND), proposed by Milgrom [6], describes this regularity without explaining it.
In its field theories, the aquadratic-Lagrangian theory (AQUAL) of Bekenstein and Milgrom [7] and the quasi-linear formulation of Milgrom (QUMOND) [8], both the interpolation function and the scale enter as inputs.

The Cosmic Fabric Model treats space as a thin elastic solid, termed the fabric [9].
In its open-system form, the fabric grows from a precursor through a two-way exchange, the renewal, whose small net is cosmic expansion [10].
Paper I [11] derives an algebraic law for galaxies, the renewal growth boost law, from the steady state of that renewal.
A threshold drawn at each renewal event selects between the renewal's two modes, modeled on athermal transformations in solids.
Roughening folds excess length into the fabric's material as a crimp, which the inclusion postulate, taken as a local law of the material, turns into a reduced conductivity of the static field that circular orbits interpret as extra mass.
In spherical symmetry, the law recovers the deep-MOND exponent of $`-1/2`$ and an interpolation function equal to MOND's simple function with an exponential hardening.
Two identifications relate its scale to the de Sitter rate.
A system smaller than the catchment length, the range over which a renewal event senses the field, keeps its own field Newtonian.
In its constrained fit, Paper I imposes the scale relation, $`a_0 = cH_{\rm dS}\ln(1+\delta_{\text{fv}})`$, where $`\delta_{\text{fv}}`$ is the free volume per roughening event, and thus fits a single constant, the scale.
The divisor of the de Sitter acceleration, $`\mathcal{D} = cH_{\rm dS}/a_0`$, is then $`1/\ln(1+\delta_{\text{fv}})`$.

Our earlier review of MOND [12] asks that any explanation exhibit whatever suppresses the effect at high acceleration and state its prediction for wide binaries, where MOND with the external-field effect predicts an anomaly.
Paper I supplies both, through the hardening and through a null from its screen below the catchment length.
Because an algebraic law cannot hold exactly in a disk's midplane [13], the theory still requires a well-posed field equation off spherical symmetry.
Its lensing must also follow from the same field, because weak lensing of isolated galaxies extends the relation by roughly two decades in acceleration [14, 15].
Paper I obtains the equality of lensing and dynamical masses, the optical equality, for static fields from a single identification, and the law still needs this equality for time-dependent fields.
Its sole material constant, the free volume per roughening event, follows in Paper I from the fitted scale, whereas a material theory should compute it.

Here we address all three needs using three identifications of our own and no further postulate.
Homogenizing the crimped microstructure, we derive a transmission tensor whose axis, when a new layer is taken as laid across the transmitted flux, aligns with the field, a fixed point shown to be stable where the axis is uniform.
The resulting field equation is well posed and, on that aligned state, reduces to exact AQUAL.
Paper I's local law makes lensing equal to dynamics in static fields at linear order, and when applied on each time slice it maintains this equality in changing fields.
From the total renewal rate, we derive a relaxation time and a kinetic window whose adopted fast edge places a floor of 58 pc on the catchment length.
In small, fast systems, all of which already lie below the catchment length, the resulting residence screen partly suppresses the stretch.
For one candidate unit, a rod of four sites, a lattice simulation of the avalanche kinetics yields a free volume of 0.188 and a divisor of 5.81, close to the values of 0.19 and 5.75 used in Paper I.
Because that unit was selected against the fitted divisor, this agreement serves as a consistency check.

Papers I and II divide the law much as mechanics divides statics from kinetics, although this paper also extends the statics off spherical symmetry and computes the law's material constant for one candidate unit.
Paper I treats the balance through which renewal maintains a radial stretch of the material path around a body, whereas this paper treats how and how fast a disturbed stretch returns to that balance.
As in Paper I, the law's source is the baryons of bodies, while the gravitating content beyond the baryons, uniform on the scales tested here, enters only through its mean density, which raises the expansion rate above its floor.
The law applies to bodies below a host halo mass of about $`10^{13}`$ solar masses, the mass threshold of Paper I's §2.5.
Paper III [16] treats the outer limit of the law, the mass threshold and the content beyond bodies.

Section 2 summarizes the model of Paper I along with the postulates and identifications on which we build.
In Sections 3 to 5, we derive the field theory off spherical symmetry and the kinetics of renewal, and compute the free volume for an example microstructure.
Section 6 tests these results in disks, in the small systems of the Galaxy, and in disturbed galaxies, while Section 7 collects the results, open problems, and falsification criteria.

## 2. The model of Paper I in brief

We restate here the elements of Paper I on which we build.
Apart from the marginal identity in Eq. (4), which we derive below, Paper I provides their derivations.
The law follows from three statements about renewal around a body, covering guidance, the store of excess, and its readout:

1. A body's field guides the renewal.
Each renewal event is guided with probability $`1 - e^{-x_s}`$, where $`x_s = g/(cH_{\rm dS})`$ is the total field in units of the de Sitter acceleration.
This form holds at the counting factor of unity identified in Paper I.
2. A guided event smooths, re-laying a layer of the material in alignment and removing its excess, whereas an unguided event roughens, adding a free volume $`\delta_{\text{fv}}`$ to its layer.
Each layer therefore holds an excess equal to $`\delta_{\text{fv}}`$ times the number of roughening events since its last smoothing.
3. The excess lies along the field as folded material path that instruments do not measure.
It lowers the conductivity of the static field along the stack of layers, so a given mass supports a steeper gradient, and the boost equals one plus the mean excess.

Because the boosted field is the field that guides renewal, the loop closes on the total field and yields the law.
Paper I's Table 3 lists the law's four postulates and nine identifications, the latter paired with their counterparts in ordinary materials, and to these we add three identifications of our own.
The first, deferred to this paper by Paper I, interprets the free volume as a self-organized marginal value.
At that value the elastic energy that the renewal events release, the fabric's only agitation, just meets what the exchange with the precursor needs.
For a changing field, the second takes a new layer as laid across the transmitted flux of §3.1, which the inner rotation curves of strongly boosted galaxies select.
The third holds that a renewal domain, the region re-laid in a single renewal event, retains no lasting excess until a first smoothing has laid a layer in it.
Roughening still occurs in such a domain, but the excess it adds lasts only once a layer stands there.

We grade each result by the model in which it is shown.
A result at transport strength is exact for the field conducted through the fabric averaged over many layers, the transport whose tensor Appendix A derives, but is not shown for the discrete units themselves.
A result at simulation strength is shown in the lattice simulation of Appendix C, and one at toy strength in a simplified model of Appendix B or C.
We call a result estimated when it rests on an illustration or an order-of-magnitude estimate.
Table 1 lists our inputs along with the results on which later sections rest.

We retain the terms and symbols defined in Paper I, while Appendix D adds the symbols that recur across our sections to the notation of Paper I's Table 7.
Paper I's §2.1 defines the growth interface, the memory time $`\tau_c`$, the constitutive set point $`\varepsilon_e^\ast`$, and the trajectory clause of the Background Datum postulate.
The terms of statement 1 appear in Paper I's §3.2, including the threshold and its mean, the catchment length $`\ell_c`$, the contrast, the drive, the per-axis share, and the counting factor with its menu of four values.
Those of statement 2 appear in Paper I's §3.3, including sector selectivity, the layer, the material path, and the stretch.
Those of statement 3 appear in Paper I's §3.4, including the incoherence premise, the crimp, the local law of the material, and the readout.
Paper I's §3.5 defines the guidance law, its crossover at a boost of 2, the dilute slope $`s`$, and the hardening with its onset.
Paper I's §3.7 defines the screen below the catchment length, scale-selective coupling, and its alternative, the ambient-stretch coupling.
The characteristic size that the screen compares against the catchment length is a system's radius, taken for a stellar system as its half-light radius, circularized where elongated.
In the separate-lattice architecture, offered in Paper I's §3.1 as an example meeting the structural requirements on the fabric's parts, the fabric forms a single material comprising three sectors (Figure 1).
A discrete orientational sector holds the template, the aligned arrangement in which neighboring units share one orientation, together with its packing errors.

![A cross-section of one example arrangement of the fabric's three sectors](https://figures.tgtenev.com/tenev2026-dark-matter-effect-ii/architecture-example.svg)

**Figure 1.** An example arrangement of the separate-lattice architecture, showing how its three sectors relate: the shear continuum bearing the shear load, the orientational sector of discrete units, and the lattice of cells along whose links light travels.
Ticks mark the orientations of the template's units, uniform where aligned and mixed within a roughened patch bounded by walls, the surfaces across which neighboring units disagree in orientation.
Spanning several units, the links of the amorphous lattice of cells cross the patch without bending.
A charged fault of the lattice of cells represents a particle of ordinary matter, as in Paper I's §3.1.
The shapes are illustrative.

Balancing per event the excess added by roughening against that removed by smoothing gives the steady state, Paper I's Eq. (5):

$$\begin{aligned} (1 - \phi)\ \delta_{\text{fv}} &= \phi\ (\bar\ell' - 1) \\
\therefore\quad \bar\ell' - 1 &= \delta_{\text{fv}}\ \frac{\mathcal{U}}{\mathcal{G}(X)}, \qquad \frac{\mathcal{G}}{\mathcal{U}} = e^{\lambda X} - 1, \qquad \lambda = \ln(1+\delta_{\text{fv}}) \end{aligned} \quad (1)$$

where $`\phi = 1 - e^{-\lambda X}`$, with $`\lambda X = \kappa x_s`$, is the guided share, $`\bar\ell'`$ is the stretch, $`\mathcal{G}`$ and $`\mathcal{U}`$ are the smoothing and roughening rates per domain whose ratio defines the guidance law, and $`X = g/a_0`$ is the drive in MOND's units.
The steady state, $`\nu = \bar\ell' = 1 + \delta_{\text{fv}}\ \mathcal{U}/\mathcal{G}`$, yields the boost law and its scale, Paper I's Eqs. (8) and (10):

$$\nu(X) = 1 + \frac{\delta_{\text{fv}}}{e^{\lambda X} - 1}, \qquad a_0 = \frac{cH_{\rm dS}}{\mathcal{D}}, \qquad \mathcal{D} = \frac{\kappa}{\ln(1+\delta_{\text{fv}})} \quad (2)$$

with $`\nu`$ the boost, $`\mu = 1/\nu`$ the interpolation function, $`a_0`$ the scale, $`H_{\rm dS} = \sqrt{\Omega_\Lambda}\ H_0`$ the de Sitter rate, $`\kappa`$ the counting factor, and $`\mathcal{D}`$ the divisor.
The boost at a given baryonic field $`Y = g_N/a_0`$ follows from solving $`Y = X\mu(X)`$.
The steady-state field equation, Paper I's Eqs. (6) and (12), reads

$$\partial_i\big(C^{ij}\ \partial_j\Phi\big) = 4\pi G\hat\rho, \qquad C^{ij} = \bar\ell'^{-1}\ \hat n^i\hat n^j + \bar\ell'\ \big(\delta^{ij} - \hat n^i\hat n^j\big), \qquad \bar\ell' = \nu(\lvert\nabla\Phi\rvert/a_0) \quad (3)$$

with $`C^{ij}`$ the conductivity tensor, $`\Phi = -c^2\varepsilon`$ the lapse potential, $`\varepsilon`$ the actual strain, $`\hat n`$ the stretch axis, and $`\hat\rho`$ the mass density as measured by rulers.
The source equation underlying Eq. (3) has been derived only outside a single spherical body [10], a limitation addressed in §7.3.
Appendix A.1 verifies the agreement of this tensor with the covariant inclusion postulate of Tenev and Horstemeyer [17].

Because no thermal bath exists, the agitation driving roughening arises from the mechanism's own mechanical noise.
Self-noise closure requires that this agitation supply the energy that the two-way exchange with the precursor draws.
In §5.1, we derive the marginal identity from self-noise closure under the Background Datum postulate by evaluating each event's misfit energy as an Eshelby inclusion problem [18].
Paper I's identification of $`\kappa = 1`$ turns Eq. (2) into the scale relation of its Eq. (11), imposed in its constrained fit:

$$Z\ \delta_{\text{fv}}^2 = 2, \qquad Z = Z_1\ A, \qquad \mathcal{D}\ \ln(1+\delta_{\text{fv}}) = 1 \quad (4)$$

where $`Z_1 = (\varepsilon_u/\delta_{\text{fv}})^2`$ is the bare noise sum, equal to unity when a unit's expressed dilation $`\varepsilon_u`$ accommodates the full free volume, and $`A`$ is the avalanche amplification delivered by the interface [19].

Across 153 SPARC rotation curves, Paper I fits the algebraic relation $`g = \nu(g_N/a_0)\ g_N`$ with the free volume tied to the scale via Eq. (2) at $`\kappa = 1`$, leaving one fitted constant.
That fit places the scale at $`(0.97 \pm 0.07)\times10^{-10}\ \mathrm{m\ s^{-2}}`$, with galaxy-clustered errors.
Equation (2) converts that scale into a free volume of 0.20 at $`H_0 = 67.4`$ km/s/Mpc and 0.18 at 73 km/s/Mpc.
Following Paper I, we evaluate derived quantities at a fiducial free volume of 0.19, within 0.01 of the constrained best fits at both Hubble constants.
An unconstrained two-constant fit, with the free volume fitted beside the scale, yields a free volume of 0.30 while improving $`\chi^2`$ by only $`3.9 \pm 9.7`$, showing that rotation curves alone do not separate 0.30 from the inferred free volume.
At a free volume of 0.19 with $`Z_1 = 1`$, the marginal identity requires $`A \approx 55`$.
Throughout, divisors are quoted relative to $`H_{\rm dS}`$ adopting $`\Omega_\Lambda = 0.6847`$ [20].

**Table 1.** *The inputs of this paper and the results on which its later sections rest, with their status and their value or form, followed in brackets by the section that states each. The first row summarizes the model of Paper I.*

| Quantity | Status | Value or form<br>[Section] |
|---|---|---|
| the model of Paper I | derived and identified there, with one fitted constant, the scale, on the inputs that Paper I's Table 3 lists | Eqs. (1) to (3) and the scale relation of Eq. (4)<br>[§2] |
| size that the screen compares with the catchment length | adopted as a convention | a system's radius, for a stellar system its half-light radius, circularized where elongated<br>[§2] |
| direction of a new layer in a changing field | identified; selected by the inner residuals of 32 strongly boosted galaxies, against the gradient's central prediction at three to four standard deviations | across the flux<br>[§3.1, App. A] |
| variation of the field from the uneven excess of the layers | computed for the largest domains that the avalanches allow, an estimate; the size of a domain is open | at most 0.5 percent of the field at the Sun and 1.3 percent at a boost of 30, between volumes one catchment length across<br>[§3.1, App. A.2] |
| stability of the aligned state | shown for a uniform axis, given the interpretation of the layer; open for a displaced arrangement, an item of §7.3 | the layers' normal returns to the field<br>[§3.2, App. A] |
| equality of lensing and dynamical masses | derived in Paper I for static fields at linear order and extended in §3.3 to fields that change, given Paper I's local law adopted on each slice; the transverse part of the momentum constraint is open | both potentials take the conductivity, so the potential of the spatial curvature equals the lapse potential, $`\Psi = \Phi`$<br>[§3.3, App. A.4] |
| remaining tensorial part of the spatial metric, gravitational waves included | attributed, not derived; Paper I places the waves on the lattice of cells | elastic shear of the lattice of cells<br>[§3.3] |
| at least one renewal event per domain in each memory time | required by the self-noise closure, given the Background Datum postulate | $`n = \varepsilon_e^\ast/b \geq 1`$<br>[§4.1] |
| locality ceiling of the catchment length | estimated from the point-by-point locality of the radial-acceleration relation | 3 kpc or below, the estimate on which the slow edge of $`5.2\times10^4`$ yr rests<br>[§4.1] |
| ceiling of the catchment length | estimated in Paper I's §3.7 | 200 pc or below<br>[§4.1] |
| fast edge of the equilibration time | adopted; no datum sets it from below | $`10^3`$ yr, which gives the catchment length its floor of 58 pc<br>[§§4.1 and 4.2] |
| lasting excess only where a layer stands | identified | a domain holds no lasting excess until a smoothing has laid its layer<br>[§4.1, App. C] |
| scale-selective coupling of Paper I's §3.7 | selected by the planets against the anisotropic form of the alternative, in Paper I, and by the globular clusters against its isotropic form | a flat mass-to-light ratio below the catchment length<br>[§6.3] |
| marginal identity; the free volume as its self-organized value | derived from the self-noise closure, a requirement that is stated and not derived, given the Background Datum postulate; identified | $`Z\ \delta_{\text{fv}}^2 = 2`$; $`\sqrt{2/Z}`$<br>[§5.1] |
| bare noise sum | a premise of the example microstructure, whose unit pins its full free volume | $`Z_1 = 1`$<br>[§5.1, App. C] |
| unit's shape | selected against the divisor window of 5.70 to 6.19 | the rod of four sites<br>[§5.2] |
| trigger scale of the self-noise closure | open | stand-in 0.01 of a primary event's kick energy; the rod's divisor lies in the window for 0.0033 to 0.013<br>[§5.2, App. C] |
| delivery of a primary's or a repack's energy in the lattice simulation | adopted in place of the long-range Eshelby kicks | six equal kicks to the nearest neighbors<br>[§5.1, App. C] |
| laying rule of a roughening event | adopted for the example microstructure | random addition throughout the bulk<br>[§5.2, App. C] |
| stability check of the renewal's noise on layers | estimated, under two conventions | passes by a factor of 5.7 or more at the central threshold and 3.6 or more across its range, for layers in register or out of it<br>[§5.3] |

## 3. The field theory off spherical symmetry

Paper I solves Eq. (3) in spherical symmetry.
Off spherical symmetry, we derive the transmission tensor from the crimped microstructure, obtain the field equation on the aligned state where the tensor axis tracks the field, and establish gravitational lensing for time-dependent fields.

### 3.1 The transmission tensor of the crimped microstructure

At transport strength, homogenization makes the coarse-grained operator of the crimped microstructure, the transmission tensor, equal to the uniaxial conductivity tensor of Eq. (3), as derived in Appendix A by path counting.
Flux along the layer normal crosses $`\bar\ell'`$ of material path in series, whereas flux perpendicular to it passes through $`\bar\ell'`$ of cross-section in parallel.
A layered laminate achieves these exact two coefficients, the Wiener bounds of homogenization [21], providing the direct continuum analog for layers smoothed across the field.
A toy network of crimped elastic links in Appendix B recovers the same coefficients.
It also confirms that the wave-bearing lattice of cells must remain uncrimped, as required in Paper I, because crimp on that lattice would refract light through angles of order unity.
Thus, the conductivity tensor reweights only the static, configurational readout of a crimped region as the differential operator governing both metric potentials, to which slow orbits and light deflection respond.
Radiative waves, by contrast, cross the region at full speed $`c`$ along the straight lattice of cells, whose links span the template's folds rather than tracing them.

Because each layer accumulates its own roughening count, the stored excess is spatially uneven.
Under the scale-selective coupling of Paper I's §3.7, the stretch entering the tensor equals one plus the mean excess averaged across a volume one catchment length wide.
By the estimate in Appendix C, such a volume contains at least 6,050 domains, so any single layer contributes only a minute share.
Appendix A.2 evaluates the residual field fluctuations left by this uneven store, summarized in Table 1.

The local axis $`\hat n`$ of a domain is the normal to the layer established by its most recent smoothing.
In Paper I's static treatment, layers lie perpendicular to the field sensed across one catchment length.
In a time-varying geometry, where the stored axis and the potential gradient need not coincide, we adopt as an identification that each smoothing lays its new layer perpendicular to the transmitted flux, $`C^{ij}\partial_j\Phi`$.
The flux's divergence is set solely by local matter density.
Rafting in nickel superalloys provides the material counterpart, where precipitate plates orient perpendicular to an applied tensile stress [22]; external load sets stress there just as enclosed mass sets flux here.
Because stress and strain are coaxial in uniaxial loading, the laboratory counterpart does not distinguish between flux and gradient, leaving strongly boosted dwarf galaxies to decide between them empirically.
In any static aligned configuration, the axis, gradient, and flux are collinear, so both rules yield identical static fields, rotation curves, and disk departures.

Within the tightened kinetic window of §4.1, set by $`\ell_c \lesssim 200`$ pc, a domain retains its axis between smoothings for 1,200 to 4,100 yr at the crossover field and $`2.7\times10^4`$ to $`9.3\times10^4`$ yr at a boost of 28.
The law gives that boost about 200 kpc from a galaxy of baryonic mass $`10^{10.57}\ M_\odot`$.
Denoting the mean interval between smoothings by $`T`$, the axis pattern around a body translating at speed $`v`$ lags behind the body by roughly $`2vT`$ times a numerical factor of 0.85 to 0.92.
Appendix A.3 derives this lag at first order.
Here the factor of two reflects the crimp-weighted mean age of a domain, and the spatial lag remains local rather than growing with halo radius.
Around an isolated galaxy lens of baryonic mass $`10^{10.57}\ M_\odot`$ moving at 300 km/s, this lag is at most an estimated 0.03 percent of the radius between 100 kpc and 1 Mpc.
Among the 32 SPARC galaxies whose innermost measured point the law boosts by more than 5, moving at an estimated 515 to 694 km/s through the fabric, this lag stays below the radius at every innermost point.
It leaves 91 percent or more of the boost there at the central values of the kinetics and the speeds, and at least 69 percent at the most exposed values, at DDO 64.

Galaxy kinematics favor laying new layers across the flux rather than across the local interior gradient of a freshly smoothed domain.
That gradient points partway between the coarse-grained field and the flux.
Because the potential gradient tracks the stored axes strongly, orienting new layers by the interior gradient would rotate axes only fractionally toward a moving source at each smoothing.
At first order, the resulting spatial lag would scale as $`2vT\bar\ell'`$ multiplied by a logarithmic factor, $`\tfrac12\ln(R_{\text{out}}/r)`$, that grows with the halo's outer radius.
At the same points that lag would exceed a tenth of the radius at 22 to 32 of the galaxies and the radius itself at 3 to 20.
The innermost residuals would then fall with that lag, whereas their slope on the predicted fall is $`0.14 \pm 0.20`$, against the 1 that this rule requires and the 0 of the flux rule.
In its central prediction, laying across the interior gradient is therefore excluded at three to four standard deviations, and in its least prediction only by the nine galaxies boosted by more than 10.
The test rests most on UGCA 444, DDO 64 and NGC 3109, whose innermost fields have errors of 0.23 to 0.64 dex.
We classify this selection as a test of the predicted pattern rather than of the speeds, since no transverse velocity of these galaxies is measured and their flow speeds span a factor of 1.35 only.
Inner rotation curves also hold systematic errors that the test does not model, and where a trail nears the radius the first-order lag is taken beyond its range.

### 3.2 The aligned state and exact AQUAL

Where the layer axis is spatially uniform, alignment with the field forms a stable fixed point of renewal under our flux-orientation rule.
In a uniform-axis background, a single smoothing immediately aligns the layer normal with the flux pointing from the source, eliminating any small angular perturbation, as shown in Appendix A.3.
Around a localized mass, however, the unperturbed axis pattern is radial rather than uniform.
Proving stability against a rigid translation of the entire radial pattern relative to the mass remains an open problem of §7.3, because beyond roughly two source radii both the field and the flux bend to follow the displaced axes.
On the aligned state, the transmitted flux reduces identically to $`\bar\ell'^{-1}\nabla\Phi`$.
Equation (3) then simplifies directly to Paper I's Eq. (13), exact AQUAL governed by Paper I's interpolation function and coarse-grained at the catchment length:

$$\nabla\cdot\big[\mu(\lvert\nabla\Phi\rvert/a_0)\ \nabla\Phi\big] = 4\pi G\hat\rho \quad (5)$$

This equation governs the lapse potential, the time-time metric perturbation.
By Paper I's shared local law, the spatial curvature potential obeys the exact same equation.
Consequently, the integral momentum and angular-momentum conservation theorems of Bekenstein and Milgrom [7] apply directly, and because the total field sets the drive, the external-field effect operates literally.
Standard objections that algebraic MOND force laws violate curl-free conservative motion do not arise here, because the algebraic boost enters as a constitutive conductivity rather than a modified force vector.
Well-posedness of Eq. (3) is guaranteed by standard elliptic regularity wherever the stretch remains positive and bounded, as verified in Appendix A.
These mathematical properties are established for the local field equations, Eqs. (3) and (5).
Because the nonlocal field equation corresponding to the scale-selective coupling of Paper I's §3.7 is stated only verbally, its formal well-posedness and conservation laws remain to be written out.

A Newtonian observer interpreting the boosted potential through the standard flat-space Poisson equation infers an effective "phantom" dark-matter density given in closed form by

$$4\pi G\ \rho_{\text{phantom}} = \partial_i\big[(\delta^{ij} - C^{ij})\ \partial_j\Phi\big] \quad (6)$$

While the true divergence of the transmitted flux vanishes identically in vacuum, the unweighted Laplacian evaluated by a flat-space observer does not, revealing the apparent dark halo as the divergence of the conductivity deficit.

### 3.3 Lensing and the optical equality

Reproducing observed gravitational lensing requires that the full boost appear equally in both scalar potentials of the weak-field metric.
Because matter and light propagate on a single physical metric in the Cosmic Fabric Model, the theory belongs to the modified-gravity class.
Light deflection must emerge directly from the boosted metric potentials rather than from auxiliary vector or scalar fields added to the metric, as in the tensor-vector-scalar theory (TeVeS) and similar completions [23, 24].
Failure to boost light deflection ruled out early scalar-field formulations of relativistic AQUAL, where anomalous acceleration resided in a conformal scalar decoupled from null rays [5].

Written in areal radial coordinates, the linearized General Relativity metric with equal lapse and spatial curvature potentials reads

$$ds^2 = -(1 + 2\Phi_{\text{tot}}/c^2)\ c^2dt^2 + (1 + 2r\Phi_{\text{tot}}'/c^2)\ dr^2 + r^2 d\Omega^2 \quad (7)$$

where $`\Phi_{\text{tot}}`$ is the boosted potential, ensuring that photons deflect according to the full dynamical mass rather than the bare baryonic mass.
Paper I derives this optical equality for arbitrary static geometries at linear order by identifying a single local material transmission law governing both $`\Phi`$ and $`\Psi`$.
Because both potentials share the conductivity tensor of Eq. (3) and vanish at infinity, $`\Psi = \Phi`$ everywhere in static fields, equating lensing mass to orbital mass.
By contrast, attempting to map the lapse strain pointwise onto the spatial metric without solving the spatial constraint fails outside Keplerian fields.
Calibrated on a point mass, a local algebraic map puts $`1 - 2\Phi_{\text{tot}}/c^2`$ into $`g_{rr}`$ instead of $`1 + 2r\Phi_{\text{tot}}'/c^2`$, which for the logarithmic potential of a flat rotation curve makes light deflection depend unphysically on the arbitrary zero-point radius of $`\Phi_{\text{tot}}`$.

In realistic galaxies, baryons move continuously while the conductivity store trails behind within the relaxation time of §4.1.
Because the elliptic constraint equations of General Relativity hold instantaneously on each spatial hypersurface [10], we apply Paper I's shared local law slice by slice to the instantaneous conductivity tensor $`C^{ij}(t, \mathbf{x})`$, keeping $`\Psi(t, \mathbf{x}) = \Phi(t, \mathbf{x})`$ even as the store lags.
Combining the time derivative of the $`\Psi`$ constraint with matter continuity, $`\partial_t\hat\rho + \partial_i J^i = 0`$, determines the longitudinal part of the gravitational momentum constraint: the time rate of change of the transmitted flux, $`\partial_t(C^{ij}\partial_j\Psi)`$, balances $`-4\pi G`$ times the longitudinal matter momentum density.
The time-dependent conductivity tensor sits inside the time derivative, exactly as a time-varying dielectric permittivity sits inside Maxwell's displacement current in the Ampère-Maxwell law.
Consequently, the phantom dark-matter density of Eq. (6) carries an effective mass current analogous to a bound polarization current in electrodynamics.
This continuity argument determines only the longitudinal, curl-free sector of the momentum constraint.
In a steadily rotating axisymmetric disk, where $`\partial_t(C^{ij}\partial_j\Psi) = 0`$, gravitomagnetic frame dragging is governed by the transverse, divergence-free vector constraint, which remains open here alongside cosmological background terms and nonlinear corrections.

Geometrically, gravitating matter causes the three-dimensional fabric to bend into the fourth spatial dimension.
Transverse bending alone generates the spatial scalar curvature, which suffices to realize the spatial metric at linear order around a single spherical mass and around a spherically symmetric boosted halo.
We attribute the remaining tensorial degrees of freedom of the spatial metric, including radiative gravitational waves, to elastic shear deformations of the discrete lattice of cells.
Wherever a boosted spherical potential departs from the Keplerian $`1/r`$ form, matching the lapse potential requires an in-plane volumetric dilatation alongside transverse bending, whose microscopic derivation remains open, as §7.3 states.
In nonspherical geometries, the cellular lattice holds the trace-free spatial curvature that bending alone cannot supply, just as it does for nonspherical Newtonian sources.
At linear order, this framework directly accounts for the weak-lensing radial-acceleration relation observed out to hundreds of kiloparsecs [14].
Each modified constraint equation departs from standard General Relativity solely through the conductivity tensor $`C^{ij}`$ in its differential operator, with ordinary matter remaining the sole source term and no new propagating wave modes introduced.
One additional microstructural requirement is that crimped orientational layers transmit matter-prescribed strain into the macroscopic metric without attenuation.
Appendix B verifies this unattenuated transmission at toy strength by showing that uniform link strain scales folded paths and macroscopic chords identically.

### 3.4 The architecture's datum energy, isotropy and wave speeds

Our field theory places three structural demands on the separate-lattice architecture regarding its datum energy, optical isotropy, and wave speeds.
The shear modulus of the shear continuum saturates the relativistic causal bound, $`\mu_0 = u_0`$ [10, 25].
By an elasticity argument just short of a formal theorem, saturating $`\mu_0 = u_0`$ rules out any discrete network of bonds or struts in void as the bearer of the shear load, requiring the fabric to be a multiphase composite.
Reaching the causal ceiling demands that every joule of cohesive energy deform affinely under pure shear, which no bond lattice, isotropic self-stressed network or homogenized network of tension elements achieves.
A bond network falls below the affine bound through non-affine relaxation, and isotropic tension does no work against a shear that preserves volume.
Tension elements bear a tension equal to their energy density, yet a homogenized network of them reaches a shear modulus of one-tenth of that density when isotropic and roughly one-quarter when optimally oriented.
Only the rest energy density of the structureless shear continuum enters $`\mu_0 = u_0`$.

First, Paper I requires that all configurational energy stored in the orientational sector, including domain walls between misaligned units, belong to the non-gravitating datum energy of the open-system model.
By the open-system model's Datum Energy corollary, datum energy produces no curvature, enters no wave speed apart from the shear continuum's rest energy, and only the exchange with the reservoir supplies and returns it [10].
This condition is essential, since for a hyperplate thickness $`L`$ of a few Planck lengths, the continuum shear modulus $`\mu_0 = 3c^4/(4\pi G L^2)`$ [10] is roughly $`10^{112}\ \mathrm{J\ m^{-3}}`$.
Because each misaligned unit, of volume $`v_u`$, stores an Eshelby misfit energy of order $`\tfrac23\mu_0\delta_{\text{fv}}^2 v_u`$ by Eq. (11), the roughened orientational walls in a galactic halo hold roughly $`10^{110}\ \mathrm{J\ m^{-3}}`$.
Were that configurational energy gravitating, it would exceed the halo's apparent dark-matter density, $`\sim 10^{-4}\ \mathrm{J\ m^{-3}}`$, by 114 orders of magnitude and exceed the cosmic dark-energy density, $`\sim 5\times10^{-10}\ \mathrm{J\ m^{-3}}`$, by 119 orders of magnitude.
Treating wall energy as datum energy requires that the natural volume of template units have zero static coupling to macroscopic strain in the shear continuum.
A newly roughened unit strains the continuum only transiently, through the exterior strain whose energy §5.1 prices and whose subsequent relaxation at fixed unit volume remains to be modeled.
Under this condition, the standing stretch pattern around a galaxy exerts zero self-gravity, and any alternative microstructural realization must satisfy the same constraint.
By estimate, rotation-curve tightness bounds any self-gravity of the stretch pattern below a few percent of the total field in the live regime, a cap that remains to be computed.

Second, the composite architecture specifies the conditions required to preserve extreme isotropy for light and gravitational waves.
Modern rotating-resonator experiments constrain directional anisotropy in the speed of light to below $`10^{-18}`$ [26].
In our composite model, the shear continuum is a translationally uniform condensate possessing no lattice axes, while neither waves, rulers, nor clocks couple directly to the cubic grid of the orientational template.
Because electromagnetic and gravitational waves propagate along the cellular lattice, that lattice must form a statistically isotropic amorphous network rather than a periodic crystal so that macroscopic wave speeds remain direction-independent.
Renewal itself does not enforce amorphousness, leaving the realization of such a network an open problem.
The sole macroscopic anisotropy resides in the layer normal $`\hat n`$, which a smoothing lays across the transmitted flux, and it affects only the static conduction of the potentials near masses.

Finally, renewal alone does not automatically guarantee equal speeds for light and gravitational waves.
The GW170817 multimessenger bound restricts their fractional speed difference to between $`-3\times10^{-15}`$ and $`+7\times10^{-16}`$, as Paper I's §2.3 states.
Because both waves propagate on the cellular lattice, matching speed $`c`$ requires that the ratio of cell shear stiffness to cell inertia remain locked to the square of the continuum wave speed independently of roughening in the orientational sector.

## 4. The kinetics of renewal

Paper I derives the boost law from the static event balance of Eq. (1), from which time cancels out.
Here we formulate the time-dependent kinetics of renewal to find how rapidly a perturbed stretch relaxes back to steady state, establishing lower bounds on system size and residence duration.

### 4.1 The relaxation time and the kinetic window

Tracked in time at a fixed comoving patch of fabric, the excess stretch $`\bar\ell' - 1`$ evolves through competition between roughening and smoothing.
Uncorrelated roughening events add $`\delta_{\text{fv}}`$ at rate $`\mathcal{U}`$, whereas guided smoothing events wipe out a domain's accumulated excess completely at rate $`\mathcal{G}(X)`$.
Denoting the total renewal rate, the gross exchange rate per domain, by $`\Gamma = \mathcal{G} + \mathcal{U}`$, we define the equilibration time $`\tau_{\text{eq}}`$ as the interval for unguided roughening at full rate $`\Gamma`$ to accumulate an excess of unity on a layered domain:

$$\partial_t\ \bar\ell' = \delta_{\text{fv}}\ \mathcal{U} - \mathcal{G}(X)\ (\bar\ell' - 1), \qquad \tau_{\text{eq}} = \frac{1}{\Gamma\ \delta_{\text{fv}}} = \frac{b}{3H_{\rm dS}\ \delta_{\text{fv}}}, \qquad b = \frac{3H_{\rm dS}}{\Gamma} \quad (8)$$

Equation (8) applies wherever domains already possess established layer planes, which holds throughout any guided region.
At fixed drive $`X`$, the linear ordinary differential equation relaxes $`\bar\ell' - 1`$ exponentially toward $`\delta_{\text{fv}}\ \mathcal{U}/\mathcal{G}`$ at rate $`\mathcal{G}(X)`$, confirming that the steady state of Eq. (1) is a global attractor.
No relaxation term appears at the bulk volumetric memory rate $`1/\tau_c`$, because net reservoir accretion is insensitive to orientational crimp, and independent threshold draws at each event make the process Markovian.
In the final expression of Eq. (8), the dimensionless net-to-gross bias $`b`$ measures net cosmological floor expansion as a small fraction of the rapid gross exchange rate $`\Gamma`$.
Because $`\Gamma`$ cancels out of the static boost law in Eq. (1), equilibrium rotation curves cannot constrain $`b`$; only short-distance screening and time-domain phenomena probe it.

Because the steady state reflects a per-event ratio rather than a cumulative age, undisturbed regions maintain it indefinitely, while dynamically disturbed regions recover it on the smoothing timescale.

Under the Background Datum postulate, two consistency conditions bracket all kinetic parameters within a bounded window.
First, because athermal interface agitation relies entirely on the self-noise of discrete renewal events, maintaining continuous agitation without quiescent dead intervals requires at least one renewal event per domain within each configurational memory time $`\tau_c = \varepsilon_e^\ast/(3H_{\rm dS})`$ [10]; hence $`n = \Gamma\tau_c = \varepsilon_e^\ast/b \geq 1`$.
Second, the empirical point-by-point locality of the radial-acceleration relation requires that the catchment length, $`\ell_c = c\ \tau_c`$ by identification, remain smaller than galactic disk scales, $`\ell_c \lesssim 3`$ kpc, capping the memory time at $`\tau_c \lesssim 9{,}800`$ yr and the residual set-point strain at $`\varepsilon_e^\ast \lesssim 1.7\times10^{-6}`$.
Combining both bounds with Eq. (8) yields

$$\tau_{\text{eq}} = \frac{b}{3H_{\rm dS}\ \delta_{\text{fv}}} \leq \frac{\tau_c}{\delta_{\text{fv}}}, \qquad \varepsilon_e^\ast \geq b = 3H_{\rm dS}\ \delta_{\text{fv}}\ \tau_{\text{eq}} \quad (9)$$

Evaluating the upper bound places the slow edge of the equilibration window at $`\tau_{\text{eq}} \leq 5.2\times10^4`$ yr.
No current measurement bounds $`\tau_{\text{eq}}`$ from below.
We adopt a nominal fast edge of $`\tau_{\text{eq}} = 10^3`$ yr, chosen as a round figure exceeding the residence times, all below $`10^3`$ yr, of the Sun's $`a_0`$ shell and of the wide binaries in §4.2.
At $`\tau_{\text{eq}} = 10^3`$ yr, Eq. (9) places a lower bound on the set-point strain of $`\varepsilon_e^\ast \geq 3.3\times10^{-8}`$ and sets a floor on the catchment length of $`\ell_c \geq 58`$ pc, on which our screening analysis of Reticulum II in §6.4 relies.
Without this adopted fast edge, globular-cluster kinematics in Paper I set an estimated floor near 30 pc.

Together, these broad bounds restrict $`\tau_{\text{eq}}`$ to $`10^3\text{–}5.2\times10^4`$ yr and $`\varepsilon_e^\ast`$ to $`3.3\times10^{-8}\text{–}1.7\times10^{-6}`$ at $`H_0 = 67.4`$ km/s/Mpc; for $`\delta_{\text{fv}} = 0.19`$, they correspond to $`\tau_c \in [190,\ 9{,}800]`$ yr and $`\ell_c \in [58\ \text{pc},\ 3\ \text{kpc}]`$.
Because the fast edge is adopted, a nonempty window checks only that the derived slow edge lies above it.
Incorporating the stronger upper bound $`\ell_c \lesssim 200`$ pc that Paper I estimates from classical dwarf spheroidal galaxies, with half-light radii 0.2–1 kpc, narrows these intervals to our *tightened kinetic window*: $`\varepsilon_e^\ast \in [3.3\times10^{-8},\ 1.1\times10^{-7}]`$, $`\tau_c \in [190,\ 650]`$ yr, and $`\tau_{\text{eq}} \in [10^3,\ 3.4\times10^3]`$ yr.
Inside this tightened window, each domain experiences 1 to 3.4 renewal events per memory time, refreshing every $`10^2`$ to $`10^3`$ yr.

Relaxation within this window is astrophysically rapid.
Because increasing $`\bar\ell'`$ at fixed baryonic field $`Y`$ raises the drive $`X = Y\bar\ell'`$, linearizing Eq. (8) around steady state while accounting for self-consistent total-field feedback gives the perturbation relaxation rate $`1/\tau_{\text{rel}}`$:

$$\frac{1}{\tau_{\text{rel}}} = \mathcal{G}(X) + X\ \mathcal{G}'(X)\ \frac{\nu - 1 + \delta_{\text{fv}}}{\nu} \quad (10)$$

where $`\mathcal{G}' = d\mathcal{G}/dX`$, and the $`\delta_{\text{fv}}`$ term reflects conversion of roughening events into smoothing events at fixed gross rate $`\Gamma`$.
Deep in the weak-field regime, total-field feedback doubles the bare damping rate to $`\tau_{\text{rel}} \approx 1/(2\mathcal{G}) \propto 1/X`$.
At the $`X = 1`$ crossover, where $`\nu = 2`$, Eq. (10) gives $`\tau_{\text{rel}} = 0.77\ \tau_{\text{eq}}`$, and $`\tau_{\text{rel}} \to 1/\mathcal{G}`$ at high acceleration, $`X \gg 1`$.
Across the broad window, $`\tau_{\text{rel}}`$ is at most $`4.0\times10^4`$ yr at the crossover and $`3.0\times10^5`$ yr in the outer rotation-curve limbs, $`X \sim 0.1`$.
Within the tightened window, those upper bounds drop to $`2.6\times10^3`$ yr and $`2.0\times10^4`$ yr, with a crossover minimum near 770 yr at the fast edge.

Finally, we adopt as an identification that an unguided domain retains no cumulative crimp until an initial guided smoothing event establishes a coherent layer plane.
Layered intercalation hosts such as graphite [27] and swelling clays [28], which take up a guest between their layers and swell along the stacking axis alone, are its counterpart, though laboratory crystals do not directly test the absence of unlayered accumulation.
Under this rule, virgin unlayered fabric builds up its initial stretch more gradually.
The fraction $`p(t)`$ of domains possessing a layer grows as $`\partial_t\ p = \mathcal{G}\ (1 - p)`$ and multiplies the roughening source in Eq. (8), yielding a two-stage buildup $`1 - e^{-\mathcal{G}t}(1 + \mathcal{G}t)`$ at constant drive.
Around an isolated $`10^{10.57}\ M_\odot`$ galaxy lacking an external ambient field, initially unlayered fabric reaches 90 percent of its equilibrium boost in the tightened window within $`1.0\text{–}3.6\times10^4`$ yr at 20 kpc and within $`1.1\text{–}3.8\times10^6`$ yr at 1 Mpc.
Both are orders of magnitude shorter than the 0.1–1 Gyr orbital and residence timescales of galactic halos.

### 4.2 The residence screen

Finite relaxation times introduce a secondary, partial *residence screen* nested inside Paper I's spatial catchment-length screen (Figure 2).
The trajectory clause stipulates that solidifying fabric is laid down at rest in the cosmological frame, which Paper I's §5.2 places in the cosmic microwave background frame.
A compact gravitating body moving at peculiar speed $`v`$ therefore sweeps across background fabric elements, occupying its own characteristic radius $`R`$ for only a finite residence interval $`t_{\text{res}} \sim 2R/v`$.
Whenever $`t_{\text{res}} < \tau_{\text{rel}}`$, the local stretch pattern can build up only partially before the body moves on, an explicit kinetic departure from the frame independence of General Relativity.
Moving at the Solar System's 370 km/s speed relative to the microwave background, the Sun's $`a_0`$ crossover shell, ~7,800 astronomical units in radius at the law's scale, has a residence time of roughly 200 yr.
Wide binaries of $`\lesssim 0.15`$ pc reside for under $`10^3`$ yr, with pairs $`10^4`$ astronomical units apart crossing in ~130 yr, placing both below our adopted fast edge.
Because Solar neighborhood systems sit inside the Milky Way's guided disk field at $`X \approx 2`$, ambient domains already possess established layers and relax according to Eq. (10).
At the fast edge, $`\tau_{\text{rel}} \approx 470`$ yr, roughly 3.7 times the crossing time of a binary $`10^4`$ astronomical units across.
Consequently, residence lag alone caps any local pattern buildup around such a binary at $`1 - e^{-1/3.7} \approx 24`$ percent of steady state, and caps buildup at the solar crossover shell at 23 to 42 percent.

However, for systems moving at up to 600 km/s through drives above about 0.006, residence screening is nested inside the screen below the catchment length.
Residence suppression acts only when $`R < v\ \tau_{\text{rel}}`$, whereas self-noise continuity, $`n \geq 1`$, requires $`\ell_c \geq c\ \delta_{\text{fv}}\ \tau_{\text{eq}}`$.
Across moderate and strong drives, $`X \geq 0.1`$, where $`\tau_{\text{rel}} \leq 6\ \tau_{\text{eq}}`$, any residence-screened system spans a fraction of the catchment length bounded by $`R/\ell_c \leq 6v/(c\ \delta_{\text{fv}})`$.
For peculiar speeds of 370 to 600 km/s, the bound is 3.9 to 6.3 percent, or 7.8 to 12.6 pc in the tightened window.
For any translation speed below $`c\ \delta_{\text{fv}}/6 \approx 9{,}500`$ km/s, $`R/\ell_c < 1`$ holds, and at 600 km/s it holds down to $`X \approx 0.006`$.
Thus, within these bounds, residence kinetics carve out no new screened territory beyond Paper I's spatial screen: systems larger than $`\ell_c`$ obey AQUAL, while smaller systems remain Newtonian in a uniform ambient field.
Therefore, the predicted absence of MOND anomalies in the Solar System and wide binaries relies on averaging over a catchment length rather than on our adopted $`10^3`$ yr fast edge.

![The two screens as a map of residence time against system radius, with the catchment-length window from the adopted floor of 58 pc to 200 pc, the residence floor and the diagonal of the fastest motion through the fabric](https://figures.tgtenev.com/tenev2026-dark-matter-effect-ii/screening-map-nested.svg)

**Figure 2.** The screen below the catchment length and the kinetic residence screen, mapped as residence time in the fabric's frame, which the series identifies with the microwave background's, against system radius.
Residence times divide each system's extent, twice its radius, by the Solar System's 370 km/s frame speed, with vertical bars spanning 230 to 600 km/s.
Vertical dashed lines mark the catchment-length window between the adopted 58 pc kinetic floor, long-dashed, and the 200 pc dwarf-galaxy ceiling, short-dashed.
Systems to the left are *structural nulls* whose internal fields remain Newtonian via Paper I's spatial averaging, and the law acts on systems to the right.
Systems lying below the horizontal residence curve at the fast edge adopted in §4.1, $`\tau_{\text{eq}} = 10^3`$ yr, also experience partial kinetic suppression.
The dotted diagonal, shading faster motions below it, marks residence at 600 km/s, roughly the Local Group's peculiar speed; residence-screened systems occupy the lower-left wedge below ~0.3 pc.
Classical dwarf spheroidals lie beyond the catchment-length window and display boosted dynamics, whereas ultra-faint dwarfs sit inside the screened zone.
Galaxy clusters are plotted for spatial scale only, as the boost law is not applied above conventionally inferred host halo masses of $`\sim 10^{13}\ M_\odot`$ in Paper I's §2.5.

## 5. The free volume computed for the example microstructure

We next derive the marginal identity of Eq. (4) from self-noise closure under the Background Datum postulate, and evaluate the resulting self-organized free volume via lattice avalanche simulations for a candidate template unit.
Closure itself is stated as a microstructural requirement rather than derived.

### 5.1 The marginal identity and the free volume for the selected unit

Mechanically, each unguided roughening event introduces a local volumetric misfit of one template unit, acting as an Eshelby inclusion [18] embedded inside the elastic shear continuum.
Because the far-field elastic energy density around a point dilation in three dimensions decays as $`r^{-6}`$, its spatial sum over the surrounding lattice converges rapidly.
Within one configurational memory time $`\tau_c`$, a domain undergoes $`\varepsilon_e^\ast/b`$ primary events; summed across the lattice and over the triggered secondary avalanche, each primary delivers $`Z`$ times the characteristic unit misfit energy per unit mass, $`\lvert K_0\rvert\delta_{\text{fv}}^2/(2\rho_0)`$.
Self-noise closure requires the agitation that these $`\varepsilon_e^\ast/b`$ primaries deliver, $`Z\lvert K_0\rvert\delta_{\text{fv}}^2\varepsilon_e^\ast/(2\rho_0 b)`$, to match the specific energy $`\lvert K_0\rvert\varepsilon_e^\ast/(\rho_0 b)`$ needed to drive two-way interface exchange at density $`\rho_0`$ and bulk modulus $`K_0`$.
This demand follows from near-equilibrium exchange kinetics, under which the bias is the ratio of the potential drop that each unit of accreted mass descends, $`\lvert K_0\rvert\varepsilon_e^\ast/\rho_0`$ in the open-system model [10], to the agitation per unit mass.
Equating energy supply to demand cancels the unknown bias $`b`$, gross rate $`\Gamma`$, and interface constants identically, leaving the parameter-free marginal identity $`Z\ \delta_{\text{fv}}^2 = 2`$.

We evaluate the bare noise sum $`Z_1`$ from the exterior shear energy $`E_{\text{ext}}`$ that a uniform dilation $`\varepsilon_u`$ of a unit of volume $`v_u`$ stores in the continuum, an energy whose subsequent decay §3.4 leaves open.
Because the continuum bulk modulus satisfies the vanishing P-wave condition $`K_0 = -\tfrac43\mu_0`$, an Eshelby sphere stores negative interior bulk energy $`E_{\text{int}} = \tfrac12 K_0 \varepsilon_u^2 v_u`$ alongside positive exterior shear energy $`E_{\text{ext}} = \tfrac23\mu_0 \varepsilon_u^2 v_u`$:

$$E_{\text{int}} + E_{\text{ext}} = \tfrac16\ (3K_0 + 4\mu_0)\ \varepsilon_u^2 v_u = 0, \qquad Z_1 = \frac{2E_{\text{ext}}}{\lvert K_0\rvert\ \delta_{\text{fv}}^2\ v_u} = \Big(\frac{\varepsilon_u}{\delta_{\text{fv}}}\Big)^2 \quad (11)$$

Exact cancellation of total continuum elastic energy reflects the zero P-wave modulus, confirming that the shear continuum alone offers zero static restoring force against volumetric misfit.
Instead, internal stiffness of the discrete template unit pins its own natural volume while inter-unit packing remains compliant.
Full pinning, $`\varepsilon_u = \delta_{\text{fv}}`$, maximizes the energy partition at $`Z_1 = 1`$.
Consequently, unamplified single-event noise, $`A = 1`$ and $`Z \leq 1`$, would require $`\delta_{\text{fv}} \geq \sqrt{2} \approx 1.41`$, nearly an order of magnitude above empirical galaxy values, proving that interface agitation must operate via collective avalanches, $`A \gg 1`$ [19].

Via $`Z\ \delta_{\text{fv}}^2 = 2`$, we identify the material parameter $`\delta_{\text{fv}}`$ with the self-organized marginal free volume $`\sqrt{2/Z}`$ maintained dynamically by interface avalanches.
This identification constrains $`\delta_{\text{fv}}`$ only once avalanche amplification $`A`$ is computed.
Amorphous glasses provide the laboratory counterpart, trapping excess free volume as marginally stable solids [29], although no glass gives the marginal value itself.
Trapped free volumes reach about 0.018 in amorphous silicon [30] and about 0.20 in open-network vitreous silica.
The last is the glass's excess volume over quartz as a fraction of the volume of quartz, from densities of 2.20 and $`2.65\ \mathrm{g\ cm^{-3}}`$ [31, 32], as $`\delta_{\text{fv}}`$ is a fraction of a unit's natural volume.
Our galaxy-inferred value of $`0.197 \pm 0.016`$ lies within 0.5σ of the glass, and the fiducial 0.19 within 1σ.

In Appendix C, a mean-field toy model of the avalanche kinetics confirms dynamically that driven free-volume kinetics self-organize to marginality, disfavoring an unannealed free volume equal to the raw random-deposition error.
Placing that kinetic kernel onto a three-dimensional cubic template grid for a selected candidate unit, a $`1\times1\times4`$ *four-site rod*, yields a self-organized free volume of $`\delta_{\text{fv}} = 0.188`$ and avalanche amplification $`A = 57`$ at simulation strength.
Those outputs follow from the rod's intrinsic geometric constants, raw random-addition packing error $`\delta_0 = 0.282`$ and turning-hole activation constant $`c_a = 0.75`$, adopting a stand-in closure trigger scale equal to 0.01 of a primary kick distributed across six nearest neighbors.
The per-repack compaction efficiency, 1.0 percent for the rod, is set self-consistently where the stationary locus intersects $`A\ \delta_{\text{fv}}^2 = 2`$.
Like the inferred free volume, the computed $`\delta_{\text{fv}} = 0.188`$ lies near that of vitreous silica, although the simulation starts from the raw packing error of rods on the template's grid rather than from that of a glass.
It reproduces Paper I's fiducial dilute slope, $`s = 0.92`$, and hardening onset, $`X = 3.8`$, to two significant figures.

### 5.2 The comparison with the constrained fit

Across $`H_0 = 67.4`$ to $`73`$ km/s/Mpc, the four-site rod's simulated free volume of $`0.188`$ gives $`a_0 = cH_{\rm dS}\ln(1+\delta_{\text{fv}}) = (0.93\text{–}1.01)\times10^{-10}\ \mathrm{m\ s^{-2}}`$, bracketed by Paper I's constrained SPARC fit of $`(0.97 \pm 0.07)\times10^{-10}\ \mathrm{m\ s^{-2}}`$.
Global stellar mass-to-light normalization adds a ~20 percent systematic scale uncertainty [2], and Eq. (2) applies to the guidance-law crossover rather than to empirical RAR fits.

Viewed in terms of free volume and dimensionless divisor $`\mathcal{D} = 1/\ln(1+\delta_{\text{fv}})`$, the rod's $`\delta_{\text{fv}} = 0.188`$ sits inside both 68 percent galaxy-clustered intervals, $`0.180\text{–}0.213`$ at 67.4 km/s/Mpc and $`0.167\text{–}0.197`$ at 73 km/s/Mpc.
Its divisor of 5.81 lies within 1 percent of the fiducial 5.75 and between the best-fit divisors 5.57 and 5.98 at the two Hubble constants.
However, we selected the four-site rod by screening 59 polycube shapes of up to 36 sites, those of a catalog of 62 whose avalanche loci cross the marginal identity, against a target divisor window of 5.70 to 6.19.
Its lower edge gives a scale of $`0.951\times10^{-10}\ \mathrm{m\ s^{-2}}`$ at 67.4 km/s/Mpc, and its upper edge gives $`0.948\times10^{-10}\ \mathrm{m\ s^{-2}}`$ at 73 km/s/Mpc.
Because the unit geometry was chosen to match the fitted divisor range, this agreement demonstrates internal microstructural consistency rather than constituting an ab initio prediction of $`a_0`$.
It shows that a simple discrete unit consistent with the fitted scale exists.
Moreover, because the simulated divisor shifts by ~7 percent per factor of three in the unknown trigger scale $`E_{\text{trig}}`$, remaining inside the target window requires $`E_{\text{trig}} \in [0.0033,\ 0.013]`$, full-hole activation weighting from Appendix C, and bulk random-addition deposition.

Compared secondarily against fits using the empirical RAR function, whose scale in Paper I's §5.3, $`1.05\times10^{-10}\ \mathrm{m\ s^{-2}}`$, gives divisors of 5.2 to 5.6, the rod's divisor sits ~4 percent high.
Translated into the mass-to-light-independent baryonic Tully-Fisher normalization for gas-rich dwarfs, the rod gives $`a_0/s = (1.02\text{–}1.10)\times10^{-10}\ \mathrm{m\ s^{-2}}`$, restating the scale relation without providing an independent test of unit shape.

### 5.3 The stability of the renewal's noise

Order-of-magnitude energetic estimates confirm that self-noise inside our tightened kinetic window is strong enough to prevent spontaneous orientational ordering across neighboring renewal domains, preserving the incoherence premise of Paper I.
Modeling domains in the conservative limit of aspect ratio unity, each layer shares four lateral edges plus either two faces, stacked in register, or eight partial faces, staggered out of register.
It has 6 or 12 neighbors total, coupled across boundaries by an alignment interaction bounded above by one unit misfit energy.
In three-dimensional Ising statistics of the folds, 12-neighbor staggered stacks order below an effective noise temperature of ~9.75 misfit energies, confirmed by fcc Monte Carlo runs, while 6-neighbor registered stacks order below ~4.5.
The ordering point of staggered stacks spans 4.4 to 15.5 across the fold's symmetry, the number of neighbors and the fluctuation corrections.
Within our tightened kinetic window, with $`n \in [1,\ 3.4]`$ events per memory time, each amplified by $`Z \approx 55`$, standing interface agitation maintains 55 to 190 misfit energies per domain.
This exceeds the 9.75 ordering threshold by safety factors of 5.7 at the slow edge and 19.5 at the fast edge with the largest set point, and at least 3.6 across the widest threshold range.
Scaling coupling with shared face area instead of per-pair would push the ordering point lower, to about 1.6.
The margin rests on two conventions, a noise temperature that counts each renewal event once and a bound on the alignment energy taken per pair.
Determining the exact order-unity prefactors belongs to the microstructure theory.

## 6. The observational tests

We now compare the field equation off spherical symmetry, kinetic bounds, and screening predictions with observations of galactic disks, Milky Way compact stellar systems, and dynamically disturbed galaxies.

### 6.1 The disk departure

In a flattened axisymmetric disk, exact AQUAL, Eq. (5), departs systematically from the spherical algebraic relation because the nonlinear conductivity responds to the vertical gravitational pull of the stellar and gas layers alongside the radial pull.
As Brada and Milgrom [13] showed with exact fields for thin disks, the algebraic MOND relation does not hold exactly in the midplane, although standard fits of rotation curves, those to SPARC included, apply it.
Solving Eq. (5) numerically across all 153 finite-thickness SPARC galaxies places the midplane radial acceleration a median of ~3 percent below the algebraic formula, with 0.06 dex rms scatter across points.
The deficit grows to a median of 18 percent at low-field points where vertical disk gravity exceeds radial gravity just outside the gas layer, mostly in gas-rich dwarfs.
QUMOND [8] reproduces this geometric behavior.

Refitting the 153 rotation curves using full axisymmetric field-equation solutions under the constrained scale relation reveals a mild empirical preference for the simpler algebraic approximation: $`\Delta\chi^2 = 246 \pm 143`$, or 1.7σ, using SPARC's tabulated Newtonian disk fields.
Self-consistent finite-thickness Newtonian potentials, "the model's own field," give $`286 \pm 142`$, or 2.0σ.
Unconstrained two-constant fits and fits of the empirical function on the full field equation show comparable 1.6σ to 2.0σ preferences, or 1.5σ to 1.8σ when coarse-grained at catchment lengths of 100 to 200 pc.
MOND's simple and standard functions, solved likewise, lose 1.5σ to 1.8σ and 2.5σ.
In unconstrained fits, however, the penalty disappears when distances and inclinations are locked to catalog values and weakens under wider mass-to-light priors.
A regression of the residuals on the part of the offset between the full field equation and the algebraic relation that no refit absorbs is evaluated once, outside the constrained fit.
It disfavors the full offset at 2.4σ to 2.7σ globally and ~3σ in inner disks relative to vertically gas-averaged accelerations.
There the observed $`\Delta\chi^2`$ sits ~5σ from its value for noiseless rotation curves made by the full solution.

Furthermore, solving the full field equation in disks alters unconstrained hardening inferences substantially.
In two-constant fits on the full solution, coarse-grained or local, the best-fit free volume falls to $`\delta_{\text{fv}} \leq 0.005`$, erasing high-acceleration hardening and reducing Eq. (2) to MOND's simple function.
With the algebraic relation evaluated on self-consistent finite-thickness Newtonian fields, the free volume likewise falls to the lowest value of its fitted grid, showing that $`\delta_{\text{fv}} \approx 0.30`$ in two-constant fits belongs to the algebraic relation on SPARC's tabulated potentials.
Under our one-parameter constrained fit at $`H_0 = 67.4`$ km/s/Mpc, $`\delta_{\text{fv}}`$ shifts much less, settling to 0.179 and 0.167 on SPARC Newtonian and self-consistent fields, compared with 0.197 and 0.184 for the algebraic approximation.
With the full field equation on self-consistent disk fields, however, MOND's unhardened simple function, solved alike with one fitted scale, outperforms our constrained law by $`\Delta\chi^2 = 39.3 \pm 14.7`$, or 2.7σ.
On SPARC's Newtonian fields, the simple and empirical functions lead by only $`10.8 \pm 16.2`$ and $`9.7 \pm 5.4`$, or 0.7σ and 1.8σ.
Paper I's baseline parameters and our §5.2 rod comparison rest specifically on the algebraic relation evaluated on SPARC's fields.

Testing the theoretical scale relation $`\mathcal{D}\ln(1+\delta_{\text{fv}}) = 1`$ on full field-equation solutions mirrors this split.
Because unconstrained fits on the full solution push $`\delta_{\text{fv}}`$ toward zero, where $`\mathcal{D}\ln(1+\delta_{\text{fv}}) \approx 0.02`$, enforcing Eq. (4) incurs at least $`\Delta\chi^2 = 9.3 \pm 9.9`$, or 0.9σ, on SPARC's fields, poorly constrained across a 0.003–0.15 bootstrap span.
The cost rises to $`32.7 \pm 12.0`$, a 2.7σ tension, on self-consistent disk fields.
Similarly, discrete menu fits on the full field equation favor $`\kappa = 1/3`$ over $`\kappa = 1`$ by 0.8σ and 2.8σ because smaller $`\kappa`$ suppresses hardening.

In these comparisons, as in Paper I's fits, the stellar mass-to-light priors are centered on the conventional values of 0.5 for disks and 0.7 for bulges, whereas the normalization of these ratios is uncertain by 20 percent [2].
Because the full solution lowers the midplane field by a few percent, which slightly larger stellar masses offset, its fits depend on that normalization.
We therefore repeat the fits with both centers raised by 10 and 20 percent.
On the model's own field, the law's full solution then trails the algebraic relation by 1.4σ and 0.9σ, and MOND's simple function leads the constrained law by 1.5σ and 0.4σ.
The cost of imposing the scale relation there falls to 1.7σ and 0.6σ, and the full solution's constrained fit improves at the higher centers, its $`\chi^2`$ falling by 94 and 154 on this field.
On SPARC's field the full solution then trails the relation by 1.2σ and 0.7σ, while the law leads MOND's simple function by 0.4σ and 1.4σ.

At the higher centers the two-constant fit on SPARC's field no longer pushes the free volume toward zero, reaching 0.15 and 0.23 on the full solution, and the menu fits there favor $`\kappa = 1`$ by 0.3σ and 1.2σ.
On the model's own field the menu's preference for $`\kappa = 1/3`$ falls to 1.6σ and 0.5σ, and the algebraic relation's two-constant free volume rises to 0.17 and 0.37.
The two-constant value of 0.30 therefore no longer belongs to SPARC's tabulated potentials alone.

At centers raised by 10 and 20 percent, the empirical function's residual-slope tests disfavor the full offset at 2.0σ to 2.2σ and 1.9σ globally, and at 2.6σ to 2.7σ and 2.2σ to 2.3σ against the gas-averaged accelerations.
The reverse tests, which regress the full solution's residuals on the reversed offset, disfavor the algebraic relation at 1.5σ to 2.4σ and 1.7σ to 2.5σ, against 1.3σ to 2.3σ at the conventional centers.
With noiseless rotation curves made at the same centers, the observed $`\Delta\chi^2`$ then lies 3.8σ to 4.4σ and 3.3σ to 3.8σ from the full solution's value, against 1.1σ to 1.6σ and 1.5σ to 2.1σ from the relation's.
Against the gas-averaged accelerations alone, that distance falls from 4.8σ to 5.0σ at the conventional centers to 4.2σ to 4.4σ and 3.7σ to 3.8σ.
Paper I's fit of record, the algebraic relation on SPARC's field, instead worsens at the higher centers, its $`\chi^2`$ rising by 5 and 34, and there the scale relation costs it 1.0σ and 1.5σ.
The vertical velocity dispersions of the DiskMass Survey's disks disfavor higher stellar ratios, since modified-gravity MOND already needs disks about half as thick as edge-on ones of equal scale length, and higher ratios strengthen the vertical field [33].

While modified-inertia frameworks avoid disk departures because they give the algebraic relation exactly for circular orbits [3, 13], a modified-gravity field theory required to bend starlight via Eq. (7) cannot evade its own Poisson operator.
Consequently, the departure of the full field equation in disks stands as an empirical tension, weaker but not removed at higher stellar normalizations; §7.3 outlines physical mechanisms within flattened disks that may resolve it.

### 6.2 The Solar System and the wide binaries

Lying orders of magnitude below the 58–200 pc catchment-length window, and further suppressed by rapid frame motion, the Solar System is a structural null whose internal planetary dynamics remain Newtonian.
Precision planetary ephemerides tightly exclude standard unscreened MOND tails [5, 34].
Exponential hardening in Eq. (2) would also suppress planetary anomalies on its own.
The screen below the catchment length, however, keeps the Sun's own field from setting the stretch inside the Solar System, rendering ephemerides insensitive to the high-acceleration tail unless screening itself failed, which falsifier F-II.2 of §7.4 tests.

Wide binary stars in the Solar neighborhood, ~0.01–0.15 pc apart with internal accelerations crossing $`a_0`$, provide the cleanest observational discriminant between our screened theory and standard MOND.
Because wide binaries sit far below $`\ell_c`$, our model predicts Newtonian relative velocities, whereas unscreened AQUAL/QUMOND with the Milky Way's external-field effect predicts an ~20 percent orbital speed boost, equivalent to an effective gravitational constant $`G_{\text{eff}} \approx 1.4\text{–}1.5\ G`$.
Current analyses of wide binaries in Gaia's third data release (DR3) clash: Chae [35] reports a MOND-consistent boost, while Banik et al. [36] and Cookson et al. [37] find consistency with Newtonian gravity under strict quality cuts.
Chae and Yoon [38] argue that quality-selected subsamples still show the low-acceleration anomaly, at more than three standard deviations, in the form that realistic QUMOND orbits predict.
Because this observational debate hinges on unresolved triple-star contamination and error modeling, our wide-binary null stands as a sharp, pre-settlement falsifiable prediction, criterion F-II.1.

### 6.3 The globular clusters

Milky Way globular clusters test Paper I's *scale-selective coupling* against the alternative *ambient-stretch coupling* across system sizes below $`\ell_c`$ (Figure 3).
As Paper I's §3.7 states, planetary ephemerides already rule out the anisotropic form of the ambient-stretch coupling, aligned with the Galactic center.
The Sun's field along that axis would then be 0.69 of its field across it.
Globular clusters test the remaining isotropic form of the ambient-stretch coupling.
Under it, the ambient Galactic stretch $`\bar\ell'`$ uniformly rescales the effective gravitational constant of a cluster smaller than the catchment length, inflating its Newtonian-inferred dynamical mass-to-light ratio $`\Upsilon_{\text{dyn}}`$ by $`P = \nu(\bar X(\ell_c))/\nu_\odot`$ relative to a cluster at the Solar circle.
We call this effect ambient rescaling, with $`P`$ its factor.
Here $`\bar X(\ell_c)`$ sums the cluster's boundary field at $`\ell_c`$ and the Milky Way's point-mass field, evaluated on MOND's simple function at $`1.2\times10^{-10}\ \mathrm{m\ s^{-2}}`$; switching to Eq. (2) shifts $`P`$ by under 10 percent.
In outer-halo clusters, $`P`$ climbs to factors of 4 to 11 across the catchment-length window, detectable only in velocity dispersions.
Star-count mass estimates in catalogs such as that of Baumgardt and Hilker [39, 40] instead reflect assumed stellar-population mass-to-light ratios unaffected by gravity boosts.

The 133 globular clusters with rich internal kinematics have proper motions or $`\geq 50`$ radial velocities, with a median of about 700 measurements per cluster.
Analyzing them provides a high-weight radial test, which incorporates our per-star Jeans fit of remote NGC 2419 on the stellar velocities that the database of [39] compiles and the photometry of [41].
Although predicted rescaling $`P`$ varies by factors of 3.2 to 6.2 across Galactocentric radius, dynamical mass-to-light ratios show zero upward trend.
At $`\ell_c = 58`$ pc, regressing $`\log\Upsilon_{\text{dyn}}`$ against $`\log P`$ yields a slightly negative slope of $`-0.20 \pm 0.08`$, decisively rejecting the $`+1`$ slope predicted by ambient rescaling.
Profiling over intrinsic stellar $`\Upsilon_\star`$ and scatter, scale-selective coupling, with flat slope 0 fitted at $`\Upsilon_\star = 1.90`$, is favored over ambient rescaling by $`\Delta\ln\mathcal{L} = 60`$ to $`72`$ across $`\ell_c \in [58,\ 200]`$ pc.
Beyond 8 kpc, the 35 outer clusters favor it by 11 to 18.

Because $`P`$ correlates tightly with Galactocentric radius, only a fivefold outward drop in true stellar $`\Upsilon_\star`$ could mask a $`+1`$ boost slope.
Leaving a radial power-law trend free reduces $`\Delta\ln\mathcal{L}`$ to 13–15, but observed cluster metallicities in the Harris catalog [42] permit at most a factor of 1.4 to 1.75 decline from 0.7 to 96 kpc.
Mass-function depletion via dynamical evaporation works in the opposite direction.
Capping radial population gradients at that metallicity limit preserves a decisive preference of $`\Delta\ln\mathcal{L} = 32.5`$ to $`62.6`$, or 6.3 to 14.5 beyond 8 kpc.
A metallicity trend of that size may supply the mild $`-0.20 \pm 0.08`$ downward drift, 2.5σ below flat.

Among 21 faint, sparse outer-halo clusters with small-sample velocity dispersions (Figure 3a), data remain inconclusive.
Pal 4 and Pal 14 match bare Newtonian expectations, whereas five diffuse systems display dispersions 2.0 to 3.7 times above star-count predictions [40]: Crater, Pal 3, Pal 5, Pal 13, and Sagittarius II.
With one stellar value fitted, the data show a mild $`\Delta\ln\mathcal{L} = 1.2\text{–}3.6`$ lean toward rescaling that reverses if unresolved binary stars contribute up to 1 km/s of velocity jitter, while the method of [40] assigns such excess to binaries.
NGC 2419 adds a test of normalization, since its radial dispersion profile has the Newtonian shape [41].
If rescaling acts on the whole cluster, it would need a stellar ratio of 0.5 to 1.4 within 58–200 pc, against the $`\Upsilon_{\text{dyn}} = 2.15`$ of our Newtonian Jeans fit.
Globular-cluster kinematics thus strongly favor scale-selective coupling over the isotropic form, without triggering falsifier F-II.4.

![The globular-cluster test on dynamical mass-to-light ratios at the adopted floor of 58 pc](https://figures.tgtenev.com/tenev2026-dark-matter-effect-ii/gc-test-58pc.svg)

**Figure 3.** Dynamical mass-to-light ratios of Milky Way globular clusters plotted against the ambient rescaling factor $`P`$ predicted by the isotropic form of the ambient-stretch coupling at $`\ell_c = 58`$ pc, compared with the flat locus of scale-selective coupling.
(a) Remote outer-halo clusters: filled circles mark measured velocity-dispersion ratios, the filled triangle marks our per-star Jeans fit of NGC 2419, and gray diamonds show star-count stellar-population ratios.
Small diamonds connected by dotted vertical segments indicate the five sparse clusters whose raw dispersion ratios sit higher, and large diamonds mark clusters with no measured dispersion.
The horizontal dashed line shows scale-selective coupling, flat at 2.16, the stellar ratio of 25 high-acceleration inner clusters.
Anchored on the same 25 clusters, whose median $`P`$ is 0.69, the rising solid line, $`3.15\ P`$, shows the ambient-stretch coupling, and the dotted line, $`1.8\ P`$, shows it at a stellar value of 1.8.
(b) Rich-kinematics sample of 133 clusters: open circles inside 15 kpc, filled circles beyond 15 kpc, and open squares showing binned medians.
The fitted logarithmic slope of $`-0.20 \pm 0.08`$ strongly favors the flat scale-selective fit at 1.90, dashed, over the rising ambient-stretch coupling, $`2.26\ P`$, solid.

### 6.4 The ultra-faint dwarfs

Ultra-faint dwarf spheroidal galaxies present an empirical puzzle.
With circularized half-light radii near 21 pc [43] and 32 pc [44], Segue 1 and Reticulum II sit well below our 58 pc floor on the catchment length, where spatial screening predicts Newtonian internal dynamics.
Yet their observed stellar velocity dispersions, $`3.7^{+1.4}_{-1.1}`$ km/s [45] and $`3.3 \pm 0.7`$ km/s [46], exceed Newtonian baryonic predictions by over an order of magnitude, implying dynamical mass-to-light ratios near 3,400 [45] and 470 [46].

Adjusting $`\ell_c`$ cannot cleanly rescue both systems: lowering $`\ell_c`$ below Segue 1's 21 pc circularized radius would unscreen Newtonian outer globular clusters such as Pal 14, at 23.6–27.6 pc [39].
Placing $`\ell_c`$ between Pal 14 and Reticulum II, at 32 pc, would violate the 58 pc floor set by our adopted $`10^3`$ yr kinetic fast edge, though observation alone does not forbid a shorter fast edge.

Whether ultra-faint dwarf dispersions reflect true virial equilibrium remains debated, with Milky Way tidal stripping and binary-star inflation cited as caveats, though tides would need to inflate dispersions ten- to thirtyfold.
Unscreened MOND faces a similar shortfall in Segue 1 under the Galactic external field, attributing the excess to non-equilibrium tidal heating as ultra-faint dwarfs nearly fill their MOND tidal radii [5, 47].
Because our screened boost law generates no potential well at 30 pc, this kinematic excess remains unexplained and constitutes the primary challenge to spatial screening, leaving the large-amplitude clause of falsifier F-II.4 open pending confirmation of their equilibrium.

### 6.5 Disturbed galaxies

Because stretch perturbations re-equilibrate within $`\tau_{\text{rel}} \lesssim 3.0\times10^5`$ yr, three orders of magnitude faster than $`10^8\text{–}10^9`$ yr galactic dynamical and lopsidedness timescales, our kinetic model predicts no excess low-acceleration RAR scatter in mildly disturbed disks.
SPARC quality flag $`Q = 2`$ galaxies have minor asymmetries and/or H I data of lower quality [1], whereas $`Q = 1`$ galaxies have high-quality H I data or hybrid Hα/H I rotation curves [1].
Comparing them confirms that the median per-galaxy ratio of scatter below $`a_0`$ to scatter above $`a_0`$ shifts insignificantly, from 0.452 for $`Q = 1`$ to 0.648 for $`Q = 2`$, a rise that 12 percent of bootstrap resamplings erase or reverse.
Merging galaxy clusters cannot test relaxation here because conventionally inferred host halo masses above $`\sim 10^{13}\ M_\odot`$ lie outside the single-body boost regime of Paper I.
The time-domain clause of self-noise falsifier F-II.3 thus rests on disturbed disk galaxies.

### 6.6 The three accounts of the small systems

Across compact stellar systems, our nested spatial and residence screens predict Newtonian behavior in the Solar System, wide binaries, and rich globular clusters without fine-tuning the interpolation tail.
They leave the large velocity dispersions of ultra-faint dwarfs, and of five sparse outer clusters, unassigned.

Standard MOND, moderated by the external-field effect, predicts ubiquitous small-scale boosts: an ~20 percent velocity boost in wide binaries, currently contested in Gaia DR3, and dynamical mass-to-light boosts in the 133 rich globular clusters.
With the Galaxy's field for a flat rotation curve and the QUMOND monopole, the boosts run from 1.02 to 2.13, and their positive log-slope against $`\log P`$ is disfavored by $`\Delta\ln\mathcal{L} = 14`$ relative to flat Newtonian behavior.
Over five treatments of the external field, the slope runs from $`+0.09`$ to $`+0.27`$ and $`\Delta\ln\mathcal{L}`$ from 4.8 to 29.0, alongside tension in NGC 2419 [41].

The standard model of cosmology predicts Newtonian behavior in the Solar System, wide binaries, and baryon-only globular clusters, while assigning dense primordial cold dark matter subhalos to explain the extreme mass-to-light ratios of ultra-faint dwarfs.

## 7. Discussion

### 7.1 The results against the data

Table 2 sets our derivations and simulation outputs beside their empirical tests.
It marks the unassigned dispersions of the ultra-faint dwarfs and two tensions of the full field equation in disks, the midplane departure and the scale relation's cost on the model's own field, both at the conventional stellar normalization.

**Table 2.** *The derived or predicted quantities of this paper against their measurements.*

| Derived or predicted quantity | Measured | Verdict |
|---|---|---|
| *Divisor* $`\mathcal{D}`$<br>$`1/\ln(1+\delta_{\text{fv}})`$: 5.81 at the computed free volume | 5.57 and 5.98 at the constrained best fits for 67.4 and 73 km/s/Mpc, 5.75 at a free volume of 0.19, and the selection window of 5.70 to 6.19; 5.2 to 5.6 from the empirical function's scale | inside, for a unit selected against the fitted divisor; 4 percent above the empirical function's range |
| *Free volume* $`\delta_{\text{fv}}`$<br>the marginal value $`\sqrt{2/Z}`$; 0.188 for the rod | $`0.197 \pm 0.016`$ and $`0.182 \pm 0.015`$ inferred from the fitted scale at 67.4 and 73 km/s/Mpc, and 0.17 to 0.18 in the constrained fit on the full field equation; 0.30 in the two-constant fit at the conventional stellar normalization, within $`\Delta\chi^2 = 3.9 \pm 9.7`$ of the constrained best fit | inside both inferred 68 percent ranges, for a selected unit |
| *Scale relation on the full field equation*<br>$`\mathcal{D}\ln(1+\delta_{\text{fv}}) = 1`$ | about 0.02 where the two-constant fit pushes the free volume toward zero, at the conventional stellar normalization; imposing the scale relation costs at least 0.9σ on SPARC's mass models and 2.7σ on the model's own field | undetermined on SPARC's mass models; on the model's own field disfavored at the conventional stellar normalization, and not at one 20 percent higher, 0.6σ |
| *Disk departure*<br>exact AQUAL, 0.06 dex rms from the algebraic relation | in the constrained fit, the algebraic relation preferred at 1.7 to 2.0σ and MOND's simple function at 2.7σ on the model's own field; in the two-constant fit and the empirical function's, 1.6 to 2.0σ, 1.5 to 1.8σ coarse-grained and none with catalog distances | tension at the conventional stellar normalization; at one 20 percent higher, local fit preferences below 1σ and residual-slope tests at 1.9 to 2.3σ |
| *Kinetic window*<br>$`\tau_{\text{eq}}`$ from an adopted $`10^{3}`$ to a derived $`5.2\times10^{4}`$ yr | window nonempty; no re-equilibration signature in SPARC's quality split | consistent |
| *Globular clusters*<br>flat ratio below the catchment length | slope $`-0.20 \pm 0.08`$; flat preferred by 60 to 72 in log-likelihood over the rising relation that the isotropic form of the ambient-stretch coupling predicts | consistent, 2.5σ below flat, a fall that the metallicity trend of §6.3 may supply |
| *Ultra-faint dwarfs*<br>Newtonian internal dynamics below the catchment length | dispersions an order of magnitude and more above the screened prediction | unexplained surplus |

### 7.2 The position among the completions

On the aligned state our static field equation reduces to exact AQUAL on scales above $`\ell_c`$, so the framework inherits AQUAL's galactic phenomenology [5], subject to completing the multi-source derivation of Eq. (3).
This phenomenology includes Faber-Jackson scaling in elliptical galaxies, strong lensing by galaxies via $`\Psi = \Phi`$, and thin-disk midplane departures.
Within the MOND family, the screen below the catchment length renders the Solar System a structural null by size rather than through a high-acceleration tail of the interpolation function.

Among the relativistic field completions of MOND, TeVeS, which Bekenstein proposed [23], introduces dynamical vector and scalar fields whose distinct metric couplings were ruled out by GW170817 [48].
The aether-scalar-tensor theory of Skordis and Złośnik [24] instead satisfies wave-speed bounds and fits cosmic microwave background peaks via dust-like auxiliary fields.
Our material framework introduces zero new propagating fields, secures linear-order optical equality via a single identified local law of the material, and offers no account of the microwave background of its own.
Verlinde's emergent gravity scale $`cH_0/6`$ [49], divisor 4.96 relative to $`H_{\rm dS}`$, sits 17 percent above our four-site rod's scale, within the ~20 percent stellar mass-to-light systematic uncertainty of §5.2.

### 7.3 The open problems

Table 3 organizes the three foundational microstructural tasks alongside four specific field-equation problems.

Under Open Problem 1, the microstructure theory, verifying unattenuated transmission of matter strain into the macroscopic metric is critical, as a suppressed transmission would leave lensing at about half the strength of the dynamics.
Under Open Problem 2, the microscopic model of a renewal event, a smoothing event in galactic outskirts must align its layer normal with the local flux to within $`0.2^\circ\text{–}0.7^\circ`$.
A tilt $`\beta`$ raises the conductivity along the field to $`\cos^2\beta/\bar\ell' + \bar\ell'\sin^2\beta`$, enough to trim boosts of 90 and 28 by 10 percent.
These boosts are the law's values about 600 kpc and 200 kpc from an isolated galaxy of baryonic mass $`10^{10.57}\ M_\odot`$.
The model must explain how a single planar domain stores multiple cumulative roughening increments, which the lattice simulation of Appendix C does not represent, since a site holds at most $`\delta_0 = 0.282`$.

Four targeted issues remain in the continuum field equation:
1. *Multi-source superposition and non-Keplerian dilatation:* Because the membrane strain of the hyperplate's transverse bend is quadratic in deflection slope, bare bending strains do not superpose across distributed disk baryons.
Nor does spherical bending strain, $`r\Phi'/c^2`$, match the lapse strain, $`-\Phi/c^2`$, wherever boost flattens a rotation curve.
Supplying the missing in-plane volumetric dilatation via microstructure gradient stiffness, or restating the readout via constraint equations, remains open.
2. *Accretion strain deposit in conductivity:* Stress relaxation via bulk exchange deposits a neutral strain of order $`10^{-6}`$ around galaxies within time $`\tau_c`$ [10, Sec. 6.1].
This strain equals 1 or 3 times the field's volumetric strain depending on interface coupling, and how much that datum deposit perturbs $`C^{ij}`$ awaits calculation.
3. *Flattened-disk tension of the field equation:* Offsetting the departure without ad hoc fitting needs a physical rise of the scale, 17 to 29 percent across the disks and more where the vertical field exceeds the radial one.
Because the field in the deep regime scales as $`\sqrt{a_0}`$, that increase is, in dex, twice the part of the 0.06 dex departure that the rotation curves do not show, about 55 to 90 percent of it.
These figures hold at the conventional stellar normalization.
With priors centered 20 percent higher, the fit preferences fall below one standard deviation, while the residual-slope tests still disfavor the full offset at about 2σ, as §6.1 states.
The rise could proceed via counting-factor geometry in oblate drives, local agitation shifts in trigger scale, or orbital crossing times across $`\ell_c`$, after an independent calibration of the stellar normalization, wider-prior gas-layer slope checks and distance-free global metrics [50].
4. *Layer orientation mechanics and global translation stability:* It remains to derive why a new layer lies across the mean flux while the threshold comparison takes the field, and to prove that a rigidly offset pattern returns to its body.

**Table 3.** *The open items of this paper, with their deliverables and what decides them.*

| Item | Deliverable | Decided by |
|---|---|---|
| Open problem 1, the microstructure theory | The theory must derive sector selectivity, the transmission tensor, the local law of the material for both potentials and the full transmission of the strain from an explicit network. It must give the loose sign of roughening's packing error in general, with the deficit of natural density pinned in the shear continuum outweighing the orientational sector's own differences of compaction, and the negative bulk modulus. It must also give a template without stiffness against strain, the free volume pinned in an orientational sector with no propagating wave of its own, and a unit's exterior field and transient strain. It shares with the microscopic model of a renewal event the premises on what smoothing and roughening lay. Its other items are an amorphous lattice of cells whose waves track those of the shear continuum, the cells' inertia following their stiffness and the transverse part of the momentum constraint. The order-one factors of the stability check of §5.3 and the proof of the aligned state's stability complete it. | derivation |
| Open problem 2, the microscopic model of a renewal event | The model must give the mediator of the signal and, from the event's sensing, the catchment length and the threshold law with its mean. It must derive the per-axis share as a theorem, with the calibration of the mean threshold. It must also give the renewal of a domain as a whole with its size, the store that holds the excess of many roughenings on one layer, the independence of the thresholds of neighboring layers, and the scale selectivity. | derivation |
| Open problem 3, the avalanche and annealing kinetics | the amplification and the trigger scale computed forward, with the efficiency, the bias and the total renewal rate, and the amplification for other microstructures | a microscopic model of the units |
| The field equation beyond a single spherical body | the Poisson form of the strain outside combined and nonspherical sources, with the in-plane dilatation that the lapse needs where the potential is not Keplerian | the microstructure's gradient stiffness, checked outside a disk |
| The exchange's deposit in the conductivity | its share of the conductivity, of order $`\Phi/c^2`$ by estimate | that computation in a galaxy and a cluster, under both interpretations of the exchange |
| The disk departure | a correction of the field equation for flattened systems that the mechanism derives, against a preference for the algebraic relation of 1.7 to 2.0σ in the constrained fit at the conventional stellar normalization | an independent calibration of the stellar normalization, an independent gas-layer baseline, the global measure free of distances and inclinations, and fits that take the distances and mass-to-light ratios from external sources |
| The direction of a new layer | a physical reason for laying a layer across the mean flux while the threshold comparison takes the field, the stability of an arrangement displaced rigidly from its body, and a test of the interpretation against the speeds themselves | derivation for the first two, and for the test the transverse velocities of strongly boosted galaxies in the microwave background's frame |

### 7.4 The falsification criteria

None of the four falsification criteria in Table 4, numbered F-II.1 through F-II.4 to continue F-I.1 through F-I.5 of Paper I, is triggered; ongoing Gaia wide-binary analyses will test F-II.1 in the near term.

**Table 4.** *The falsification criteria of this paper, with what each would rule out and its status.*

| # | Criterion | Rules out | Status |
|---|---|---|---|
| F-II.1 | a confirmed wide-binary anomaly of MOND's sign | the screen below the catchment length of Paper I's §3.7, to which the residence screen adds only a partial suppression | Open and contested [35–38], in a dispute over contamination and the modeling of multiple stars; the model predicts a null. |
| F-II.2 | an ephemeris anomaly softer than quadratic, an excess planetary acceleration whose fractional size falls more slowly than $`X^{-2}`$, as the $`1/X`$ tail of MOND's simple function does | the screening of the Sun's crossover shell together with the law's hardening | Not triggered. |
| F-II.3 | A free volume from the lattice simulation, at a trigger scale computed forward, outside the inferred ranges of 0.17 to 0.21, or a trigger scale outside 0.0033 to 0.013. A calibration of the free volume independent of the mass-to-light ratios outside 0.17 to 0.21 also meets the criterion. So does a persistence of the pattern that forces $`\tau_{\text{eq}}`$ above the window, such as a residual excess in dated disturbed galaxies that decays with an e-folding time far above $`3\times10^5`$ yr. | the self-noise closure | Untested until the trigger scale is computed forward, since the rod was selected at the stand-in value of 0.01. The time-domain clause rests on the disturbed galaxies of §6.5. |
| F-II.4 | globular-cluster ratios rising with the ambient stretch; at large amplitude, a systematic boost of a factor of two or more in the internal dynamics of compact systems below the catchment length, globular clusters or ultra-faint dwarfs | the scale-selective coupling; at large amplitude, the screen below the catchment length | Not triggered, at a slope of $`-0.20 \pm 0.08`$ against +1. Five faint remote clusters whose dispersions exceed their star-count masses remain open until velocities over several epochs separate binaries from a boost. The ultra-faint dwarfs keep the large-amplitude clause open. |

## 8. Conclusion

In this second paper, we have extended Paper I's algebraic galaxy boost law into a well-posed non-spherical field theory, derived its relaxation kinetics, and demonstrated microstructural self-organization of its material parameter on a discrete lattice.
Homogenizing crimped orientational layers produces a uniaxial strain-transmission tensor; when newly smoothed layers orient perpendicular to the transmitted flux, alignment with the field forms a fixed point on which the static field equation reduces to exact AQUAL.
Its stability is shown for a uniform axis.
Applying Paper I's shared conductivity law slice by slice maintains linear-order equality between gravitational lensing and dynamical masses even in time-varying fields.
Laying new layers across the flux keeps the trail of the stored axes local, and the inner rotation curves of strongly boosted galaxies select that rule over the alternative at three to four standard deviations.
Solved numerically across 153 finite-thickness SPARC disks, exact AQUAL departs from the spherical algebraic approximation by 0.06 dex rms, introducing a 1.7σ to 2.0σ tension alongside a 2.7σ preference for MOND's unhardened simple function on the model's own field.
Both fall below one standard deviation with the stellar mass-to-light priors centered 20 percent higher, at the edge of their normalization's uncertainty, while the residual-slope tests still disfavor the full offset at about 2σ.

Renewal competition establishes an equilibration window between an adopted $`10^3`$ yr fast edge and a derived $`5.2\times10^4`$ yr slow edge, placing a 58 pc kinetic floor on the catchment length beneath the 200 pc ceiling that Paper I estimates.
While rapid motion through the microwave background frame partially suppresses stretch buildup in systems far smaller than the catchment length, residence screening nests entirely inside the screen below the catchment length.
The spatial screen thus predicts Newtonian internal dynamics for the Solar System, the Solar neighborhood's wide binaries and the 133 kinematically rich globular clusters, which sets our wide-binary null and flat cluster ratios apart from unscreened MOND.
The large velocity dispersions of ultra-faint dwarfs, however, remain an unexplained surplus.

Lattice avalanche simulations for a selected four-site rod self-organize to a marginal free volume of 0.188 and divisor of 5.81.
They confirm that an elementary discrete geometry can sustain the parameter inferred from galaxy rotation curves without predicting the scale ab initio.
Deriving sector selectivity, shared potential conduction, domain size, and the trigger scale from first principles, alongside resolving the offset of the field equation in flattened disks and ultra-faint dwarf kinematics, defines the next stage of this work.

## Data and code availability

Every test reported here is fully scripted.
The modeling and analysis code and its data are archived on Zenodo [51], with an index that maps each result to its code.
The deposit holds the simulations, the solutions of the field equation, and the fit and reduction outputs.
The deposit redistributes the public SPARC dataset [52] under its CC BY 4.0 license.
The globular-cluster database [53], the database pages that the cluster tests read and the 2010 Harris catalog [42] are not redistributed, and the deposit records their sources, retrieval dates and checksums.
The data plotted in Figure 3 copy values from that database, so the deposit holds the code that computes them rather than the data.
The galaxies' velocities for the test of §3.1, read from SIMBAD and VizieR, are likewise recorded by their queries rather than redistributed.

## Appendix A. The field theory's derivations

Circular-orbit geodesics and the empirical exclusion of macroscopic ruler stretching are derived in Paper I, §3.4.

### A.1 The conductivity form and its checks

Given three principal stretches $`\bar\ell'_1`$, $`\bar\ell'_2`$, and $`\bar\ell'_3`$ of the folded material path, applying the series/parallel path count of §A.2 along each principal axis yields principal conductivity eigenvalues $`\bar\ell'_2\bar\ell'_3/\bar\ell'_1`$ and cyclic permutations.
While arbitrary positive stretches could generate any symmetric positive-definite tensor, uniaxial laminate deposition along the layer normal $`\hat n`$ equates the two transverse eigenvalues, determining the tensor $`C^{ij}`$ from a single scalar stretch $`\bar\ell'`$ and unit vector $`\hat n`$.
Spherical symmetry specializes $`\hat n`$ to $`\hat r`$; on the aligned state, transverse conductivity drops out of the flux.

Expressed on an effective material metric $`\bar g_{ij}`$ having principal eigenvalues $`(\bar\ell'_a)^2`$, the covariant inclusion postulate of Tenev and Horstemeyer [17] transforms identically into Eq. (3) via the Voss-Weyl divergence identity, $`\bar\nabla_i V^i = \bar g^{-1/2}\ \partial_i(\sqrt{\bar g}\ V^i)`$, applied to $`V^i = \bar g^{ij}\partial_j\varepsilon`$.
Multiplying through by $`\sqrt{\bar g}`$ yields ruler mass density $`\hat\rho = \rho\sqrt{\bar g}`$ and $`C^{ij} = \sqrt{\bar g}\ \bar g^{ij}`$, matching our path-count tensor; because total enclosed mass $`M = \int\hat\rho\ d^3x = \int\rho\ dV`$ is preserved, both formulations represent the same differential equation.

Three limiting checks verify consistency:
1. *Newtonian limit:* As $`\bar\ell' \to 1`$, $`C^{ij} \to \delta^{ij}`$ and $`\hat\rho \to \rho`$, recovering the standard Poisson equation.
2. *Vacuum neutrality:* Because $`\bar\ell'`$ enters only through the homogeneous operator $`C^{ij}`$ and the bookkeeping of $`\hat\rho`$, setting $`\hat\rho = 0`$ admits the exact vacuum solution $`\varepsilon \equiv 0`$ under any crimp, so stretch never produces gravity on its own [17].
3. *Spherical Gauss law:* Integrating Eq. (3) over a sphere gives $`\Phi' = \bar\ell'\ g_N`$, recovering Paper I's orbital boost.

### A.2 The transmission tensor from the crimped microstructure

Under Paper I's incoherence premise, roughening brings the material path to $`\bar\ell'`$ per unit ruler distance along $`\hat n`$, storing the excess as microscopic crimp within the orientational sector without macroscopic displacement or elastic stress, leaving the ruler metric flat.

Coarse-grained across many domains, unfolded template material conducts static strain with unit specific conductivity.
Consider a macroscopic slab of unit ruler area and thickness $`d`$ normal to $`\hat n`$, enclosing material volume $`\bar\ell' d`$.
Flux normal to the slab traverses path length $`\bar\ell' d`$ in series across unit area, raising resistance proportionally and yielding axial conductivity $`1/\bar\ell'`$, the harmonic mean and lower Wiener bound [21].
Flux parallel to the slab traverses unit ruler length across an enlarged material cross-section $`\bar\ell'`$ in parallel, yielding transverse conductivity $`\bar\ell'`$, the arithmetic mean and upper Wiener bound.
Thus, exact homogenization at transport strength produces $`C^{ij}`$ in Eq. (3), while ruler mass density $`\hat\rho`$ matches photometric baryon density and local clock lapse transfers directly, up to negligible $`\mathcal{O}(10^{-6})`$ metric strain corrections.
Reduced axial conductivity stems from series path length rather than mechanical unbending of folds, as tested in Appendix B against Paper I's agreement of the law with the empirical function.

To bound field fluctuations caused by geometric roughening variance across layers, recall that scale-selective coupling averages $`C^{ij}`$ over regions one catchment length across, each containing at least $`N = 2A^2 \approx 6{,}050`$ independent domains, as Appendix C estimates.
Layer excess around mean $`\nu - 1`$ has variance $`(\nu - 1)(\nu - 1 + \delta_{\text{fv}})`$ via Paper I's Eq. (5).
Adding independent domain fluctuations in quadrature produces a fractional volume-to-volume field rms of $`\sqrt{(\nu - 1)(\nu - 1 + \delta_{\text{fv}})}/(\nu\sqrt{N})`$, amounting for $`\delta_{\text{fv}} = 0.19`$ to at most 0.47 percent at the Solar circle and 1.25 percent at a boost of 30, approaching $`1/\sqrt{N} \approx 1.3`$ percent.
Because finer scales are screened and larger shells average over several regions, 1.3 percent is the peak fluctuation at any scale, contributing under 0.006 dex to RAR scatter.
Reaching the 0.057 dex bound on intrinsic scatter would require $`N \lesssim 50`$.
Unaveraged layer-scale conduction would allow flux to detour around high-excess blocks, cutting a nominal boost of 29.5 to $`0.57 \times 29.5`$.
Averaging over a region one catchment length across instead suppresses flux detours to the square of the variation, $`\lesssim 2\times10^{-4}`$.

This homogenization relies on Paper I's incoherence premise, sector selectivity, and scale-selective coupling, closed dynamically by $`\bar\ell' = \nu(X)`$ and axis relaxation in §A.3.

### A.3 Well-posedness and the stability of the alignment

Because static acceleration $`-\nabla\Phi`$ is an exact gradient, orbital dynamics are automatically conservative.
Treating $`\bar\ell'`$ and $`\hat n`$ as internal state variables evolved on finite renewal timescales renders Eq. (3) at each instant a linear second-order elliptic equation for $`\Phi`$ with eigenvalues $`1/\bar\ell'`$ and $`\bar\ell'`$, positive and bounded wherever the stretch is bounded.
Standard uniform elliptic regularity secures existence and uniqueness there.
Even in the instantaneous static aligned limit, exact AQUAL of Eq. (5), linearization yields positive transverse and longitudinal eigenvalues $`\mu > 0`$ and $`d(X\mu)/dX > 0`$ for all $`X > 0`$, preserving ellipticity everywhere outside isolated field nulls.

Away from alignment, stored domain axes strongly channel the potential gradient.
If transmitted flux crosses stored axis $`\hat n`$ at angle $`\chi`$, anisotropic conductivity bends the potential gradient to angle $`\arctan(\tan\chi/\bar\ell'^2)`$ from $`\hat n`$, just $`0.6^\circ`$ away from $`\hat n`$ when $`\chi = 45^\circ`$ at $`\bar\ell' = 10`$.
In a spatially uniform axis background around a point source, however, transmitted flux points radially from the mass.
Under our §3.1 identification that smoothing lays new planes perpendicular to the flux $`C^{ij}\partial_j\Phi`$, a single smoothing immediately aligns $`\hat n`$ radially, making $`\hat n \parallel \nabla\Phi`$ an exponentially stable fixed point analogous to conjugate-force alignment in continuum damage mechanics [54].
Stability against a rigid translation of a spherical halo pattern remains open, as linear perturbation theory shows both field and flux tracking displaced axes beyond ~2 body radii, removing under 1 percent of the offset per smoothing.

For a spherical mass translating steadily at speed $`v`$, first-order perturbation theory under flux alignment yields a compact, radius-independent axis lag of $`(0.85\text{–}0.92) \times 2vT`$, confirmed to within 10 percent by full nonlinear numerical relaxations.
By contrast, alternative orientation rules suffer cumulative lag.
Across a freshly smoothed, uncrimped lamina, where $`C = 1`$, interface continuity of normal flux and tangential gradient tilts the interior gradient to $`\arctan(\tan\chi/\bar\ell')`$, correcting only a fraction $`1/\bar\ell'`$ of misalignment per smoothing and producing a logarithmically growing trail $`\propto 2vT\bar\ell'\ln(R_{\text{out}}/r)`$.
Orienting directly across the coarse-grained exterior gradient corrects only $`1/\bar\ell'^2`$ per smoothing, causing the trail to diverge linearly with halo size.

### A.4 The spatial potential and fields that change

Subtracting the conductivity equations of Eq. (3) that Paper I's local law makes both $`\Psi`$ and $`\Phi`$ obey, multiplying by $`\Psi - \Phi`$, which vanishes at spatial infinity, and integrating by parts gives $`\int \partial_i(\Psi - \Phi)\ C^{ij}\ \partial_j(\Psi - \Phi)\ dV = 0`$.
Positive definiteness of $`C^{ij}`$ forces $`\Psi = \Phi`$ identically, establishing, in spherical symmetry, the areal-radius metric of Eq. (7) for any baryon and stretch profile.

When baryons move and $`C^{ij}(t, \mathbf{x})`$ evolves, applying Eq. (3) instantaneously on each spatial slice preserves $`\Psi(t, \mathbf{x}) = \Phi(t, \mathbf{x})`$ at all times.
Taking the time derivative of $`\partial_i(C^{ij}\partial_j\Psi) = 4\pi G\hat\rho`$ and substituting matter continuity $`\partial_t\hat\rho + \partial_i J^i = 0`$, where $`J^i`$ is the momentum density of matter, yields $`\partial_i[\partial_t(C^{ij}\partial_j\Psi) + 4\pi G J^i] = 0`$, determining the longitudinal momentum constraint, $`\partial_t(C^{ij}\partial_j\Psi)_L = -4\pi G J^i_L`$, which reduces to linearized General Relativity when $`C^{ij} = \delta^{ij}`$.
In flat-space phantom-halo variables, Eq. (6), anomalous mass conservation is maintained by an effective polarization current $`-\partial_t P^i`$ with $`P^i = (\delta^{ij} - C^{ij})\partial_j\Phi/(4\pi G)`$, leaving only the divergence-free transverse vector sector open.
The equality is thus derived at linear order, given Paper I's local law applied on each slice.

## Appendix B. The crimp-stiffness toy model

At toy strength, an explicit discrete elastic network illustrates three parts of Open Problem 1: uniaxial conductivity $`C^{ij}`$, unattenuated metric strain accommodation, and straight cellular wave propagation.
Model the orientational sector as a network of identical Hookean links of natural length $`\ell_0`$ and spring stiffness $`k`$ transmitting static template displacements, folded randomly at micro-scales so macroscopic ruler geometry stays flat.
Here $`\bar\ell' = 1`$ represents taut, unfolded material.

Along layer normal $`\hat n`$, a ruler span $`\Delta x`$ encloses $`N_\ell = \bar\ell'\ \Delta x/\ell_0`$ links connected in series; adding series compliances linearly gives

$$\begin{aligned} \frac{N_\ell}{k} &= \frac{\bar\ell'\ \Delta x}{\ell_0\ k}, \qquad k_{\text{eff}}(\Delta x) = \frac{\ell_0\ k}{\bar\ell'\ \Delta x} \\
\therefore\quad C_\parallel &= \frac{1}{\bar\ell'} \end{aligned} \quad (12)$$

where $`k_{\text{eff}}`$ is the span's effective stiffness and $`C_\parallel`$, the axial coefficient of $`C^{ij}`$, is the stiffness per unit length relative to taut material, setting the exact $`-1`$ axial exponent.
Perpendicular to $`\hat n`$, the folded material packs $`\bar\ell'`$ parallel links per unit cross-sectional area; adding parallel stiffnesses directly gives $`C_\perp = \bar\ell'`$, recovering Eq. (3).

To check the metric strain accommodation of §3.3, impose a locally uniform axial strain $`\varepsilon_\ell`$ stretching every link to $`\ell_0(1 + \varepsilon_\ell)`$ at fixed fold angles, with unit tangents $`\hat t_i`$; summing segment vectors gives the macroscopic chord

$$\Delta\mathbf{x} = \sum_i \ell_0\ \hat t_i \ \longrightarrow\ \sum_i \ell_0(1+\varepsilon_\ell)\ \hat t_i = (1+\varepsilon_\ell)\ \Delta\mathbf{x} \quad (13)$$

Because uniform scaling acts as a geometric homothety, microscopic link strain transfers into macroscopic chord strain at 100 percent amplitude independently of $`\bar\ell'`$, with gradient corrections suppressed by $`\ell_c/r`$.

Finally, the toy highlights two potential failure modes:
1. *Mechanical unbending compliance:* Literal elastic fibers, as in textiles or collagen, unbend under tension, multiplying series compliance by $`f(\bar\ell') \geq 1`$ so $`C_\parallel = 1/[f(\bar\ell')\bar\ell']`$.
This distorts the RAR shape in ways that Paper I's 0.009 dex rms agreement of the law with the empirical function disfavors for large $`f`$, consistent with pure configurational transmission, $`f \equiv 1`$.
2. *Wave refraction:* Were light and gravitational waves forced to trace crimped paths, the effective refractive index $`n_{\text{eff}} = \bar\ell'`$ would bend starlight by radians rather than arcseconds, a deflection excluded by a factor of about $`10^5`$.
Wave-bearing cellular links must therefore span folds straight across, with $`n_{\text{eff}} = 1`$.

## Appendix C. The avalanche toy model and the lattice simulation

In material coordinates of the orientational sector, discrete template units occupy sites of a cubic grid distinct from the amorphous wave-bearing cell lattice.
Each unit is a rigid, uncharged connected polycube with no wave of its own, possessing discrete cubic orientation labels; uniform aligned tiling maximizes density, while label mismatches form domain walls.

A candidate polycube shape determines its number of orientation labels and two geometric inputs.
Its *activation constant* $`c_a`$ is the turning hole: fresh vacant sites needed to reorient divided by unit site count.
Its *raw packing error* $`\delta_0`$ is the free volume, empty sites per occupied site, left after random-site, random-orientation sequential jamming in the bulk.
Like that rule, a roughening event lays the units of its domain at random, throughout the bulk of the fabric.
Among 59 candidate shapes up to 36 sites whose avalanche loci intersect the marginal identity, only the $`1\times1\times4`$ *four-site rod* lands inside the target divisor window $`5.70\text{–}6.19`$ across all turning-hole definitions.
It has 3 orientation labels, leaves 22 percent vacant sites so $`\delta_0 = 0.282`$, and requires 3 fresh sites for every rotation so $`c_a = 3/4`$ unambiguously.
Four other shapes enter under minimum-cost reorientation, and still others under the largest change or a plain mean of the changes.

The toy model rests on two premises, that roughening lays material loose and that avalanches are the route of annealing.
To compute avalanche amplification $`A`$ at toy strength for Open Problem 3, we first formulate a mean-field kinetic model across $`N_{\text{s}}`$ sites holding local unit free volumes $`\delta_i`$, distinct from cumulative layer crimp.
These evolve via three sequential rules, primary roughening, Cohen-Turnbull [55] free-volume-activated triggering, and partial compaction:

$$\delta_i \to \delta_0, \qquad p_{\text{trig}} = \min\lbrace 1,\ (E/E_{\text{trig}})\ e^{-c_a/\delta_j}\rbrace, \qquad \delta_j \to (1 - \eta_a)\ \delta_j \quad (14)$$

Each primary resets a random site to $`\delta_0`$ and radiates total energy $`Z_1\delta_0^2`$, in units of $`\tfrac12\lvert K_0\rvert v_u`$, equally to random receivers.
A kick $`E`$ arriving at site $`j`$ triggers a secondary repack with probability $`p_{\text{trig}}`$, radiating $`Z_1\delta_j^2`$ onward and compacting $`\delta_j`$ by efficiency $`\eta_a`$.
Here $`E_{\text{trig}}`$ is the trigger scale, and $`Z_1`$ cancels out of $`E/E_{\text{trig}}`$.
Where no layer stands, a re-laying adds nothing lasting to the crimp, by the identification of §4.1.
Summing primary plus secondary repacks until quiescence defines mean amplification $`A`$, with no hand-tuning of branching ratios.

Three exact or emergent laws govern this stationary state:
1. *Self-organized marginality:* Free-volume feedback tunes the stationary branching ratio to $`1 - 1/A < 1`$, setting mean avalanche size to the inverse dissipation fraction as an exact mean-field attractor [19, 56, 57].
2. *Free-volume conservation, or flux balance:* Equating primary free-volume injection $`\langle\delta_w\rangle - \bar\delta`$ against removal $`(A - 1)\eta_a\delta_{\text{emit}}`$ across secondary repacks gives

$$A = 1 + \frac{\langle\delta_w\rangle - \bar\delta}{\eta_a\ \delta_{\text{emit}}} \quad (15)$$

with $`\langle\delta_w\rangle`$ the mean deposited free volume, $`\bar\delta`$ the standing mean and $`\delta_{\text{emit}}`$ the mean free volume of the sites that repacks compact.

3. *Heterogeneous marginality:* A small self-organized subpopulation of freshly loose sites produces several times its share of the triggering, making stationary free volume only logarithmically sensitive to $`c_a`$.
Across $`5\times10^4`$-site mean-field scans, $`\eta_a A \delta_{\text{emit}}^2`$ remains nearly constant over a decade in $`\eta_a`$, with $`A \propto 1/\eta_a`$.

Next, 398 three-dimensional lattice runs place this kernel onto a periodic $`16^3`$ cubic grid, checked from $`12^3`$ to $`32^3`$, with six nearest-neighbor kicks, stand-in trigger scale $`E_{\text{trig}} = 0.01\ Z_1\delta_0^2/6`$, and 2 to 12 orientation labels.
Matching neighbor plurality sets $`\delta_w = 0`$, otherwise $`\delta_0`$.
Canonical sphere-packing inputs are $`\delta_0 = 0.163`$, $`0.283`$, and $`0.334`$ [58–60], and separate runs take the four-site rod.
Lattice runs self-organize cleanly from every cold start, with the branching ratio held below one by the dissipation [19, 56, 57, 61].
They obey Eq. (15), with a drift term for the slowly changing standing mean, to $`8\times10^{-6}`$ and match random-neighbor controls within 1.3 percent in $`A`$ and 0.001 in $`\delta_{\text{emit}}`$.

With $`\delta_{\text{fv}} = \delta_{\text{emit}}`$ at $`Z_1 = 1`$, a premise of the example microstructure, intersecting the stationary locus with the marginal identity $`A\ \delta_{\text{emit}}^2 = 2`$ maps $`(\delta_0, c_a)`$ to $`(\delta_{\text{fv}}, A, \eta_a)`$.
For the four-site rod, the crossing yields $`\delta_{\text{fv}} = 0.188`$, $`A = 57`$, $`\eta_a = 1.0`$ percent, and divisor $`\mathcal{D} = 5.81`$, staying inside $`5.70\text{–}6.19`$ for $`E_{\text{trig}} \in [0.0033,\ 0.013]`$ under full turning-hole activation.
For comparison, random-loose spheres at $`c_a = 1.0`$ yield $`\mathcal{D} = 4.68\text{–}4.82`$, inside the empirical function's divisors of 4.52 to 5.60, which span its published scale of $`1.20\times10^{-10}\ \mathrm{m\ s^{-2}}`$ and the scale that Paper I fits to it.
Simulated compaction efficiencies, $`0.13\text{–}2.0`$ percent, mirror the small fraction of flow dilatation that metallic glasses retain [62, 63] and the sub-percent compaction per event of tapped granular packs [59].
One-signed annealing, $`\delta_{\text{emit}}/\delta_0 \in [0.60,\ 0.97]`$, disfavors a free volume equal to the raw $`\delta_0`$, selecting the self-organized interpretation.

By estimate, requiring the mean-field avalanche dissipation cutoff of $`2A^2`$ domains [56] to fit within a region one catchment length across bounds domain volume below $`\ell_c^3/(2A^2)`$, ensuring at least $`2A^2 \approx 6{,}050\text{–}6{,}500`$ domains in such a region.
Each, if as thick as it is wide, is $`\lesssim 0.055\ \ell_c`$, or 3.2–11 pc wide in the tightened window.
Testing whether long-range $`r^{-6}`$ Eshelby kicks reproduce mean-field cutoffs on the lattice remains open.

## Appendix D. Notation

Table 5 supplements the notation of Paper I's Table 7 with the symbols of this paper that recur across its sections.

**Table 5.** *Notation.*

| Symbol | Meaning |
|---|---|
| $`\bar g_{ij}`$, $`\sqrt{\bar g}`$, $`\bar\nabla_i`$ | the metric of the covariant form in §A.1, with the squares of the principal stretches as its principal values, the root of its determinant and its covariant derivative |
| $`b`$, $`n`$ | the exchange's net-to-gross bias, $`3H_{\rm dS}/\Gamma`$, with $`\Gamma`$ the total renewal rate of Paper I's Table 7; the renewal events per domain within one memory time |
| $`\tau_{\text{eq}}`$, $`\tau_{\text{rel}}`$ | the equilibration time, Eq. (8); the pattern's relaxation time, Eq. (10)|
| $`Z_1 = (\varepsilon_u/\delta_{\text{fv}})^2`$, $`Z = Z_1 A`$ | the bare noise sum, with $`\varepsilon_u`$ the unit's expressed dilation; the delivered noise sum, with $`A`$ the amplification, the mean size of an avalanche of the interface |
| $`v_u`$ | a unit's volume |
| $`T`$ | the mean interval between smoothings, §3.1 |
| $`\delta_0`$, $`c_a`$ | a unit's raw packing error and its activation constant, Appendix C |
| $`\eta_a`$, $`E_{\text{trig}}`$ | the compaction efficiency of a repack; the trigger scale of a repack, Eq. (14) |

## Acknowledgments

The author declares that no external funding was received for this study.
This work has made use of the SIMBAD database and of the VizieR catalogue access tool, both operated at CDS, Strasbourg, France.
In accordance with research-integrity guidelines on the use of artificial-intelligence tools, the author discloses the following use, which does not meet the criteria for authorship.
Claude, an artificial-intelligence model made by Anthropic, was used under the direction of the author to assist in the development and internal review of this work.
This assistance included working derivations and analyses under iterative direction, and implementing and running the lattice simulation of the avalanche kinetics and the tests against the SPARC and globular-cluster data.
It also included generating the figures and drafting and revising portions of the manuscript text.
The core physical thesis, the Cosmic Fabric Model, the postulates on which the series rests, and all research directions and decisions are the author's own or those of the author's coauthors of [9, 10, 17].
The author critically evaluated, tested and verified all AI-assisted derivations, analyses and text, made all research and editorial decisions, and maintains full ethical and legal accountability for the accuracy, originality and integrity of the presented work.

## References

[1] F. Lelli, S. S. McGaugh, and J. M. Schombert, "SPARC: Mass models for 175 disk galaxies with Spitzer photometry and accurate rotation curves," Astron. J., vol. 152, 157, 2016.

[2] S. S. McGaugh, F. Lelli, and J. M. Schombert, "Radial acceleration relation in rotationally supported galaxies," Phys. Rev. Lett., vol. 117, 201101, 2016.

[3] P. Li, F. Lelli, S. McGaugh, and J. Schombert, "Fitting the radial acceleration relation to individual SPARC galaxies," Astron. Astrophys., vol. 615, A3, 2018.

[4] F. Lelli, S. S. McGaugh, J. M. Schombert, and M. S. Pawlowski, "The relation between stellar and dynamical surface densities in the central regions of disk galaxies," Astrophys. J. Lett., vol. 827, L19, 2016.

[5] B. Famaey and S. S. McGaugh, "Modified Newtonian Dynamics (MOND): Observational phenomenology and relativistic extensions," Living Rev. Relativ., vol. 15, no. 10, 2012.

[6] M. Milgrom, "A modification of the Newtonian dynamics as a possible alternative to the hidden mass hypothesis," Astrophys. J., vol. 270, pp. 365–370, 1983.

[7] J. Bekenstein and M. Milgrom, "Does the missing mass problem signal the breakdown of Newtonian gravity?," Astrophys. J., vol. 286, pp. 7–14, 1984.

[8] M. Milgrom, "Quasi-linear formulation of MOND," Mon. Not. R. Astron. Soc., vol. 403, pp. 886–895, 2010.

[9] T. G. Tenev and M. F. Horstemeyer, "Mechanics of spacetime — A solid mechanics perspective on the theory of general relativity," Int. J. Mod. Phys. D, vol. 27, no. 8, 1850083, 2018.

[10] T. G. Tenev, C. B. Ward, T. F. Tenev, and M. F. Horstemeyer, "Stability of an elastic space with negative bulk modulus: Open-system growth, Friedmann expansion and a de Sitter floor," Zenodo preprint, version 4, 2026, doi: 10.5281/zenodo.21652255. Versions 1 and 2 have the earlier title "Emergent de Sitter expansion and closed topology from the Cosmic Fabric Model as an open thermodynamic system: Resolving the negative bulk modulus paradox."

[11] T. G. Tenev, "The dark-matter effect in the Cosmic Fabric Model. I. A derived law for galaxies with one fitted constant," Zenodo preprint, 2026, doi: 10.5281/zenodo.24533985.

[12] T. G. Tenev, "Modified Newtonian dynamics after four decades: The idea, the evidence, and the open questions," Zenodo preprint, 2026, doi: 10.5281/zenodo.21693735.

[13] R. Brada and M. Milgrom, "Exact solutions and approximations of MOND fields of disc galaxies," Mon. Not. R. Astron. Soc., vol. 276, no. 2, pp. 453–459, 1995.

[14] M. M. Brouwer et al., "The weak lensing radial acceleration relation: Constraining modified gravity and cold dark matter theories with KiDS-1000," Astron. Astrophys., vol. 650, A113, 2021.

[15] T. Mistele, S. McGaugh, F. Lelli, J. Schombert, and P. Li, "Indefinitely flat circular velocities and the baryonic Tully–Fisher relation from weak lensing," Astrophys. J. Lett., vol. 969, L3, 2024.

[16] T. G. Tenev, "The dark-matter effect in the Cosmic Fabric Model. III. The reach of the law for galaxies and the content beyond it," in preparation.

[17] T. G. Tenev and M. F. Horstemeyer, "Dark matter effect attributed to the inherent structure of cosmic space," Int. J. Mod. Phys. D, vol. 28, no. 8, art. 1950082, 2019.

[18] J. D. Eshelby, "The determination of the elastic field of an ellipsoidal inclusion, and related problems," Proc. R. Soc. London A, vol. 241, pp. 376–396, 1957.

[19] S. Zapperi, K. B. Lauritsen, and H. E. Stanley, "Self-organized branching processes: Mean-field theory for avalanches," Phys. Rev. Lett., vol. 75, pp. 4071–4074, 1995.

[20] Planck Collaboration, N. Aghanim et al., "Planck 2018 results. VI. Cosmological parameters," Astron. Astrophys., vol. 641, A6, 2020.

[21] G. W. Milton, *The Theory of Composites*. Cambridge Univ. Press, 2002.

[22] J. K. Tien and S. M. Copley, "The effect of uniaxial stress on the periodic morphology of coherent gamma prime precipitates in nickel-base superalloy crystals," Metall. Trans., vol. 2, pp. 215–219, 1971.

[23] J. D. Bekenstein, "Relativistic gravitation theory for the modified Newtonian dynamics paradigm," Phys. Rev. D, vol. 70, 083509, 2004.

[24] C. Skordis and T. Złośnik, "New relativistic theory for modified Newtonian dynamics," Phys. Rev. Lett., vol. 127, 161302, 2021.

[25] Ya. B. Zel'dovich, "The equation of state at ultrahigh densities and its relativistic limitations," Sov. Phys. JETP, vol. 14, pp. 1143–1147, 1962.

[26] M. Nagel, S. R. Parker, E. V. Kovalchuk, P. L. Stanwix, J. G. Hartnett, E. N. Ivanov, A. Peters, and M. E. Tobar, "Direct terrestrial test of Lorentz symmetry in electrodynamics to 10⁻¹⁸," Nat. Commun., vol. 6, 8174, 2015, doi: 10.1038/ncomms9174.

[27] M. S. Dresselhaus and G. Dresselhaus, "Intercalation compounds of graphite," Adv. Phys., vol. 30, p. 139, 1981.

[28] K. Norrish, "The swelling of montmorillonite," Discuss. Faraday Soc., vol. 18, pp. 120–134, 1954.

[29] M. Müller and M. Wyart, "Marginal stability in structural, spin, and electron glasses," Annu. Rev. Condens. Matter Phys., vol. 6, pp. 177–200, 2015.

[30] J. S. Custer, M. O. Thompson, D. C. Jacobson, J. M. Poate, S. Roorda, W. C. Sinke, and F. Spaepen, "Density of amorphous Si," Appl. Phys. Lett., vol. 64, no. 4, pp. 437–439, 1994, doi: 10.1063/1.111121.

[31] R. Brückner, "Properties and structure of vitreous silica. I," J. Non-Cryst. Solids, vol. 5, no. 2, pp. 123–175, 1970, doi: 10.1016/0022-3093(70)90190-0.

[32] J. W. Anthony, R. A. Bideaux, K. W. Bladh, and M. C. Nichols, Eds., "Quartz," in Handbook of Mineralogy, version 1.2, Mineral Data Publishing, 2001.

[33] G. W. Angus, G. Gentile, R. Swaters, B. Famaey, A. Diaferio, S. S. McGaugh, and K. J. van der Heyden, "Mass models of disc galaxies from the DiskMass Survey in modified Newtonian dynamics," Mon. Not. R. Astron. Soc., vol. 451, no. 4, pp. 3551–3580, 2015.

[34] E. V. Pitjeva and N. P. Pitjev, "Relativistic effects and dark matter in the Solar System from observations of planets and spacecraft," Mon. Not. R. Astron. Soc., vol. 432, pp. 3431–3437, 2013.

[35] K.-H. Chae, "Breakdown of the Newton–Einstein standard gravity at low acceleration in internal dynamics of wide binary stars," Astrophys. J., vol. 952, no. 2, art. 128, 2023.

[36] I. Banik, C. Pittordis, W. Sutherland, B. Famaey, R. Ibata, S. Mieske, and H. Zhao, "Strong constraints on the gravitational law from Gaia DR3 wide binaries," Mon. Not. R. Astron. Soc., vol. 527, no. 3, pp. 4573–4615, 2024.

[37] S. A. Cookson, I. Banik, K. El-Badry, W. Sutherland, Z. Penoyre, C. Pittordis, and C. J. Clarke, "A quality framework for testing gravity with wide binaries: no evidence for MOND," Mon. Not. R. Astron. Soc., vol. 547, no. 2, art. stag342, 2026 (arXiv:2602.24035).

[38] K.-H. Chae and Y. Yoon, "Revisiting data quality control and multiple-star modeling in wide binary gravity tests: confirmation of MOND-type gravitational anomaly at low acceleration," arXiv:2607.14450, 2026 (preprint).

[39] H. Baumgardt and M. Hilker, "A catalogue of masses, structural parameters, and velocity dispersion profiles of 112 Milky Way globular clusters," Mon. Not. R. Astron. Soc., vol. 478, pp. 1520–1557, 2018, with the maintained database at https://people.smp.uq.edu.au/HolgerBaumgardt/globular/, whose parameter table was retrieved on 17 July 2026.

[40] H. Baumgardt, M. Hilker, A. Sollima, and A. Bellini, "Mean proper motions, space orbits, and velocity dispersion profiles of Galactic globular clusters derived from Gaia DR2 data," Mon. Not. R. Astron. Soc., vol. 482, no. 4, pp. 5138–5155, 2019.

[41] R. Ibata et al., "The globular cluster NGC 2419: a crucible for theories of gravity," Astrophys. J., vol. 738, no. 2, art. 186, 2011.

[42] W. E. Harris, "A catalog of parameters for globular clusters in the Milky Way," Astron. J., vol. 112, p. 1487, 1996, 2010 edition (arXiv:1012.3224).

[43] N. F. Martin, J. T. A. de Jong, and H.-W. Rix, "A comprehensive maximum likelihood analysis of the structural properties of faint Milky Way satellites," Astrophys. J., vol. 684, no. 2, pp. 1075–1092, 2008, doi: 10.1086/590336.

[44] S. E. Koposov, V. Belokurov, G. Torrealba, and N. W. Evans, "Beasts of the Southern Wild: Discovery of nine ultra faint satellites in the vicinity of the Magellanic Clouds," Astrophys. J., vol. 805, no. 2, 130, 2015, doi: 10.1088/0004-637X/805/2/130.

[45] J. D. Simon et al., "A complete spectroscopic survey of the Milky Way satellite Segue 1: the darkest galaxy," Astrophys. J., vol. 733, 46, 2011.

[46] J. D. Simon et al., "Stellar kinematics and metallicities in the ultra-faint dwarf galaxy Reticulum II," Astrophys. J., vol. 808, 95, 2015.

[47] S. S. McGaugh and J. Wolf, "Local Group dwarf spheroidals: Correlated deviations from the baryonic Tully–Fisher relation," Astrophys. J., vol. 722, no. 1, pp. 248–261, 2010, doi: 10.1088/0004-637X/722/1/248.

[48] S. Boran, S. Desai, E. O. Kahya, and R. P. Woodard, "GW170817 falsifies dark matter emulators," Phys. Rev. D, vol. 97, no. 4, 041501, 2018, doi: 10.1103/PhysRevD.97.041501.

[49] E. Verlinde, "Emergent gravity and the dark universe," SciPost Phys., vol. 2, 016, 2017.

[50] J. Petersen and F. Lelli, "A first attempt to differentiate between modified gravity and modified inertia with galaxy rotation curves," Astron. Astrophys., vol. 636, A56, 2020.

[51] T. G. Tenev, "Code and data for the dark-matter effect in the Cosmic Fabric Model, Papers I and II," Zenodo, software, version 1.0.1, 2026, doi: 10.5281/zenodo.24544860.

[52] F. Lelli, S. S. McGaugh, and J. M. Schombert, "SPARC Galaxy Rotation Curve," Zenodo, dataset, Nov. 2016, doi: 10.5281/zenodo.16284118, license CC BY 4.0. Accessed: Jul. 13, 2026.

[53] Baumgardt globular-cluster database, "combined fundamental-parameter table (combined_table.txt)," with the velocity-dispersion and parameter pages. [Online]. Available: https://people.smp.uq.edu.au/HolgerBaumgardt/globular/. Accessed: Jul. 17, 2026 (table) and Oct. 10, 2026 (pages).

[54] J. Lemaitre, *A Course on Damage Mechanics*, 2nd ed. Springer, 1996.

[55] M. H. Cohen and D. Turnbull, "Molecular transport in liquids and glasses," J. Chem. Phys., vol. 31, pp. 1164–1169, 1959.

[56] K. B. Lauritsen, S. Zapperi, and H. E. Stanley, "Self-organized branching processes: Avalanche models with dissipation," Phys. Rev. E, vol. 54, pp. 2483–2488, 1996.

[57] A. Vespignani and S. Zapperi, "How self-organized criticality works: A unified mean-field picture," Phys. Rev. E, vol. 57, pp. 6345–6362, 1998.

[58] G. D. Scott and D. M. Kilgour, "The density of random close packing of spheres," J. Phys. D: Appl. Phys., vol. 2, no. 6, pp. 863–866, 1969.

[59] J. B. Knight, C. G. Fandrich, C. N. Lau, H. M. Jaeger, and S. R. Nagel, "Density relaxation in a vibrated granular material," Phys. Rev. E, vol. 51, pp. 3957–3963, 1995.

[60] G. Y. Onoda and E. G. Liniger, "Random loose packings of uniform spheres and the dilatancy onset," Phys. Rev. Lett., vol. 64, no. 22, pp. 2727–2730, 1990.

[61] T. G. Tenev, "Avalanches and self-organized criticality: The idea, the theory, and the evidence," Zenodo preprint, 2026, doi: 10.5281/zenodo.22151213.

[62] F. Spaepen, "A microscopic mechanism for steady state inhomogeneous flow in metallic glasses," Acta Metall., vol. 25, pp. 407–415, 1977.

[63] M. Heggen, F. Spaepen, and M. Feuerbacher, "Creation and annihilation of free volume during homogeneous flow of a metallic glass," J. Appl. Phys., vol. 97, no. 3, 033506, 2005, doi: 10.1063/1.1827344.
