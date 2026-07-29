# Modified Newtonian Dynamics after Four Decades: The Idea, the Evidence, and the Open Questions

**Document Metadata**

| | |
|---|---|
| **Store** | public-portfolio |
| **Publication** | Preprint, Zenodo, 2026 |
| **Published** | 2026-07-30 (Zenodo v1) |
| **DOI / URL** | https://doi.org/10.5281/zenodo.21693735 — concept DOI, cite this one for all versions; this version is 10.5281/zenodo.21693736 |
| **Licence** | CC BY 4.0 |
| **Cite as** | T. G. Tenev, "Modified Newtonian dynamics after four decades: the idea, the evidence, and the open questions," Zenodo, preprint, 2026, doi: 10.5281/zenodo.21693735. |
| **Converted from** | research-workbench `cfm-dark-sector-program/mond-review.md`, commit `0b0eed0` (v2); figures served from the R2/CDN bucket rather than committed |

---

**Tichomir Tenev**
Independent Researcher
ticho@tenev.com

**Scope.** This document is a background reference, not a research contribution. It exists so that a companion research paper need not carry the MOND phenomenology itself: that paper states the background at a high level and cites this review for the detail. Nothing here is new. There are no new results, no proposed model, and no advocacy for or against modified gravity; the review's one interpretive move, distinguishing MOND as a theory from the regularity it summarizes, is drawn from the literature it cites.

**Abstract.** In the outer parts of galaxies, stars and gas orbit faster than the gravity of the visible matter can explain. The standard resolution adds unseen mass: dark matter. Modified Newtonian Dynamics (MOND) is the competing hypothesis, proposed by Milgrom [1, 2] in 1983, that no mass is missing and that the laws of dynamics instead change character below a universal acceleration $a_0 \approx 1.2\times10^{-10}\ \mathrm{m\ s^{-2}}$. This review introduces the idea and follows its development across four decades: the short algebra that turns one constant into a family of confirmed predictions, the field theories built to make the rule self-consistent, the modern data that made its central regularities precise, the numerical coincidence tying $a_0$ to the expansion of the universe, and the places where the hypothesis is contested or fails outright. One distinction organizes everything: MOND *as a candidate fundamental theory*, which is under real strain in galaxy clusters and cosmology, versus MOND *as a compact description of an empirical regularity in galaxy data*, which is now established at a precision that any theory of galaxies, dark matter included, must account for. Two features of that regularity motivate the attention given it here. The first is economy: one constant and one shared function shape cover five decades of galaxy mass, where halo modeling of the same galaxies uses several hundred adjustable numbers and must still explain why the results collapse onto a single curve. The second is recency: the database and the relation that carry the modern argument both appeared in 2016, long after the terms of the original debate were set. The reader is assumed to know first-year mechanics (circular motion, Newton's law of gravitation) and logarithms; everything else is built in place. The canonical technical review of the subject is Famaey and McGaugh [3]; this document is a gentler path into the same material.

## Preface: why this deserves consideration

Much of the standing skepticism about MOND is well grounded, and none of it is disputed here: it fails in galaxy clusters by a factor of about two, the Bullet Cluster is real, simple relativistic versions were ruled out by the equality of gravitational-wave and light speeds, and no MOND-based cosmology approaches the standard model's maturity (Table 1 records all of it). But a skeptic's picture often dates from the era when the idea was new, while the evidence now carrying the argument is recent: the database that made the tests precise, and the relation built on it, both appeared in 2016.

**What is measured rather than fitted.** The Radial Acceleration Relation (Section 3.2) uses one universal mass-to-light ratio and no per-galaxy adjustments, and puts 2693 points across 153 galaxies on a single curve whose scatter is nearly all observational [7, 8]. The Baryonic Tullyâ€“Fisher Relation holds at slope 4, anchored by gas-rich galaxies almost independent of stellar calibration [9], and weak lensing traces the same relation to megaparsec scales [12]. The old objection that such fits were manufactured by tuning mass-to-light ratios was removed by near-infrared photometry: the relation grew tighter when that freedom was taken away (Section 3.4). Each new dataset could have dissolved it into scatter; each has confirmed it more precisely.

**The economy conventional accounts must still explain.** One constant and one shared function shape cover five decades of galaxy mass. Halo modeling of the same sample gives each galaxy its own profile with at least two free parameters, several hundred numbers in all, and must still explain why the results collapse onto one curve. Within the standard cosmology the same facts become demanding requirements on galaxy formation: scatter below the floor halo variation alone would produce [10], unseen-baryon fractions tracking rotation velocity in lockstep, and an acceleration scale coinciding with $cH_0$ for no internal reason (Sections 5 and 8).

**The theory and the regularity are separable.** Nothing here argues that MOND has the ontology right. The claim is narrower: the fit and its economy are not accounted for by conventional theory, and that alone earns them attention. Hold the two apart, as this review does throughout, treat the empirical core as a benchmark any account of galaxies must meet, and let the tests in progress (wide binaries, Section 6.4; the scale's redshift behavior, Section 5) decide. Parts of MOND have already been refuted; what survived is the part that was measured.

## 1. The problem: galaxies rotate too fast

### 1.1 What Newton predicts

Start with the one calculation everything else rests on. A body on a circular orbit of radius $R$ needs a centripetal acceleration $v^2/R$ pointing at the center, and gravity supplies it. If the mass enclosed within the orbit is $M(R)$ and $G$ is Newton's gravitational constant,

$$\frac{v^2}{R} = \frac{G\ M(R)}{R^2} \qquad \Longrightarrow \qquad v(R) = \sqrt{\frac{G\ M(R)}{R}}. \quad (1)$$

The Solar System is the textbook check. Nearly all the mass sits in the Sun, so $M(R)$ is constant and equation (1) gives $v \propto 1/\sqrt{R}$: orbital speed falls with distance. Mercury orbits at 47.9 km/s; Neptune, seventy-seven times farther out, at 5.4 km/s. The ratio is $\sqrt{77} \approx 8.8$, exactly as predicted. This falling pattern is called a **Keplerian decline**, and it is what equation (1) predicts for *any* system once the orbit encloses essentially all the mass.

### 1.2 How a galaxy's rotation is measured

A spiral galaxy is a rotating disk of stars and gas, typically tens of kiloparsecs across (a parsec is the astronomers' distance unit, about 3.26 light-years; a kiloparsec, kpc, is a thousand parsecs). Its rotation is measured with the Doppler effect. Orbiting gas emits spectral lines, most usefully a radio line of atomic hydrogen with a wavelength of 21 cm, and the side of the disk rotating toward us has its line shifted to shorter wavelengths while the receding side is shifted to longer ones. After correcting for the disk's inclination (its tilt relative to the line of sight), the shifts give the orbital speed $v$ at each radius $R$. The resulting function $v(R)$ is the galaxy's **rotation curve**.

The other side of equation (1) requires the enclosed mass, and here the visible matter is counted. Astronomers call ordinary matter (atoms, in stars and gas) **baryonic** matter. Photometry gives the profile of starlight, and a **stellar mass-to-light ratio** $\Upsilon_\star$, the number of solar masses of stars per solar luminosity emitted, converts light to stellar mass. The 21 cm line brightness gives the atomic-gas mass directly. Together these yield the baryonic $M(R)$, and equation (1) then predicts the rotation curve the visible matter can support.

### 1.3 What is observed instead

The two sides of equation (1) disagree, badly and systematically. Measured rotation curves rise and then stay **flat**, sometimes to many times the radius of the visible disk, where the visible mass predicts Keplerian decline. Rubin and Ford [4] established this in the optical for Andromeda; Bosma [5] showed with 21 cm data that the flatness continues far beyond the starlight. Figure 1 shows a classic case, the spiral NGC 3198: the baryons predict a curve that peaks near 100 km/s and falls, while the measured curve locks onto about 150 km/s and holds it. The gap grows with radius. Expressed as mass, the discrepancy reaches a factor of several to ten in the outer parts.

![Figure 1: the observed flat rotation curve of NGC 3198 against the declining curve predicted from its visible stars and gas](https://figures.tgtenev.com/tenev2026-mond-review/fig01-rotation-curve.svg)

**Figure 1.** The mass discrepancy in one galaxy. Points: the observed rotation curve of the spiral NGC 3198, from the public SPARC database (Section 3.1). Red: the rotation that the visible baryons produce, with stars converted to mass at the universal near-infrared mass-to-light ratio and the gas measured directly. The gap that opens beyond about 10 kpc, and stays open, is the phenomenon this entire subject is about.

Only two kinds of repair are possible, because equation (1) has only two sides. Either the right-hand side is missing mass, or the left-hand relation between acceleration and gravity is wrong at galactic scales. The first option is **dark matter**: each galaxy sits inside a roughly spherical envelope (a "halo") of unseen particles that supply the missing gravity. Folded into the standard cosmological model, called $\Lambda\text{CDM}$ ($\Lambda$ for the cosmological constant driving the universe's accelerating expansion, CDM for cold dark matter), this option also accounts for observations on far larger scales, which is why it is the standard resolution. The second option is **modified dynamics**, and taking it seriously is the subject of this review.

## 2. Milgrom's proposal

### 2.1 A new constant of nature

In 1983 Milgrom [1, 2] noticed that the discrepancy does not switch on at a particular radius, or size, or mass. It switches on at a particular *acceleration*. Wherever the measured acceleration $g = v^2/R$ falls below roughly $10^{-10}\ \mathrm{m\ s^{-2}}$, the discrepancy appears; above that value it does not. He therefore proposed that the discrepancy is not missing mass but a change of law: below a critical acceleration, the true gravitational acceleration $g$ departs from the Newtonian value $g_N = G M_\mathrm{bar}/R^2$ computed from the baryons alone,

$$\mu\left(\frac{g}{a_0}\right) g = g_N, \qquad \mu(x) \to 1 \ \ (x \gg 1), \qquad \mu(x) \to x \ \ (x \ll 1), \quad (2)$$

where $a_0$ is a proposed new constant of nature with the dimensions of acceleration and $\mu$ is an **interpolation function** bridging the two limits (its role is examined in Section 4.4). At high accelerations $\mu \to 1$ and Newton is recovered; at low accelerations the law changes. Empirically,

$$a_0 \approx 1.2\times10^{-10}\ \mathrm{m\ s^{-2}}.$$

It is hard to overstate how small this is: about $10^{11}$ times weaker than Earth's surface gravity, and roughly the acceleration that would take an object from rest to the speed of light over the age of the universe. Every laboratory experiment and every planetary orbit sits enormously above it. For example, Earth's acceleration toward the Sun is $6\times10^{-3}\ \mathrm{m\ s^{-2}}$, about fifty million times $a_0$. The low-acceleration regime, called the **deep-MOND regime**, is reached only in the outskirts of galaxies, in small and dim galaxies throughout, and in the outer reaches of galaxy groups and clusters. One instructive case: the Sun's own orbit in the Milky Way (about 230 km/s at a radius of 8 kpc) has $g \approx 2\times10^{-10}\ \mathrm{m\ s^{-2}}$, within a factor of two of $a_0$. Our own neighborhood in the Galaxy sits near the transition.

### 2.2 Two predictions from one line of algebra

The reason MOND was taken seriously, rather than filed as a curve-fitting exercise, is what the low-acceleration limit predicts with no further input. In the deep-MOND regime equation (2) becomes $(g/a_0)\ g = g_N$, so

$$g = \sqrt{a_0\  g_N} = \sqrt{a_0\ \frac{G M_\mathrm{bar}}{R^2}} = \frac{\sqrt{a_0\  G M_\mathrm{bar}}}{R}. \quad (3)$$

Now impose a circular orbit, $g = v^2/R$, and the radius cancels:

$$\frac{v^2}{R} = \frac{\sqrt{a_0\  G M_\mathrm{bar}}}{R} \qquad \Longrightarrow \qquad v^4 = a_0\  G\  M_\mathrm{bar}. \quad (4)$$

Equation (4) is two famous predictions in one line.

**Flat rotation curves.** The radius has disappeared: once the orbit encloses essentially all of a galaxy's baryons, $v$ is the same at every larger radius. Flatness is not an accident to be arranged galaxy by galaxy; it is forced.

**The Baryonic Tullyâ€“Fisher Relation (BTFR).** The flat velocity's fourth power is proportional to the galaxy's *baryonic* mass, stars plus gas, with a proportionality constant fixed by $a_0 G$ and by nothing else. On a log-log plot (both axes logarithmic, so a power law $M_\mathrm{bar} \propto v_f^{\ n}$ appears as a straight line of slope $n$), equation (4) predicts a single line of slope exactly 4, the same line for every galaxy, with no allowance for a galaxy's size or how concentrated its light is. That the relation involves total baryonic mass rather than starlight matters most in gas-rich dwarf galaxies, where stars are a minority of the baryons: there, the older luminosity-based Tullyâ€“Fisher relation falls apart while the baryonic version holds (Section 3.3).

A one-parameter rule that delivers both the qualitative shape of rotation curves and a quantitative scaling law is the reason this subject has survived four decades of scrutiny.

### 2.3 Ten regularities, one constant

The harvest extends beyond those two. Famaey and McGaugh [3] collect ten distinct "Kepler-like laws of galactic dynamics" that the single constant $a_0$ organizes at once. Among them: the asymptotic flatness and the BTFR above; the analogous velocityâ€“mass relation for elliptical galaxies, which are supported by random stellar motions rather than rotation (the Faberâ€“Jackson relation); a systematic relation between the size of a galaxy's mass discrepancy and its acceleration; a maximum characteristic surface density of galaxy disks, set by $a_0/G$; a split in rotation-curve shapes (rising versus flat-from-the-start) at that same surface-density scale; and the rule, named for the astronomer Renzo Sancisi, that every feature in a galaxy's baryonic profile (a bump in the light, a ring of gas) has a counterpart feature in its rotation curve, even far out where dark matter would supposedly dominate completely. Their summary of that list states the situation plainly: ten otherwise-independent regularities "have been elegantly unified by the single law proposed by Milgrom." Whatever one concludes about MOND as a theory, that unification is a fact about galaxies.

## 3. The modern evidence

### 3.1 SPARC: the database

Modern work on these questions rests on **SPARC** (Spitzer Photometry and Accurate Rotation Curves; Lelli, McGaugh and Schombert [6]): a sample of 175 disk galaxies with high-quality rotation curves and uniform photometry from the Spitzer Space Telescope in the near-infrared, at a wavelength of 3.6 Î¼m. The sample spans five decades of mass, every disk-galaxy type, gas fractions from 0.01 to 0.97, and the full observed range of surface brightness (how spread out or concentrated a galaxy's light is).

The near-infrared choice is the methodological centerpiece. Starlight at 3.6 Î¼m is dominated by the old stars that carry most of the stellar mass, and models of stellar populations predict that in this band the mass-to-light ratio $\Upsilon_\star$ is nearly the *same* for every disk galaxy, about 0.5 in solar units. Converting light to mass therefore needs **one universal number**, not a per-galaxy adjustment. That removes, at the source, the single largest freedom that plagued earlier work (Section 3.4).

### 3.2 The Radial Acceleration Relation

Now put every galaxy on a common footing. At each measured radius in each galaxy, compute two numbers that come from independent observations: the acceleration actually felt there, $g_\mathrm{obs} = v^2/R$ from the rotation curve, and the acceleration the baryons alone would produce, $g_\mathrm{bar}$, from the photometry and the gas via Newtonian gravity. Plot one against the other for every point in every galaxy.

McGaugh, Lelli and Schombert [7] did this for 2693 points across 153 SPARC galaxies and found not a scattered cloud but a single narrow curve, reproduced from the same public data in Figure 2. At high acceleration the curve is the line of equality, $g_\mathrm{obs} = g_\mathrm{bar}$: no discrepancy. Below about $10^{-10}\ \mathrm{m\ s^{-2}}$ it bends onto the square-root branch $g_\mathrm{obs} = \sqrt{g_\dagger\  g_\mathrm{bar}}$, exactly the deep-MOND form of equation (3). The whole curve is fit by one function with one parameter,

$$g_\mathrm{obs} = \frac{g_\mathrm{bar}}{1 - e^{-\sqrt{g_\mathrm{bar}/g_\dagger}}}, \quad (5)$$

with the fitted transition scale

$$g_\dagger = (1.20 \pm 0.02\ \mathrm{rand} \pm 0.24\ \mathrm{sys})\times10^{-10}\ \mathrm{m\ s^{-2}}, \quad (6)$$

numerically indistinguishable from Milgrom's $a_0$ (the systematic term reflects the absolute calibration of $\Upsilon_\star$). This is the **Radial Acceleration Relation** (RAR).

![Figure 2: the Radial Acceleration Relation â€” thousands of points from about 150 galaxies collapsing onto one one-parameter curve](https://figures.tgtenev.com/tenev2026-mond-review/fig02-rar.svg)

**Figure 2.** The Radial Acceleration Relation, rebuilt from the public SPARC database with the quality cuts of the source analysis (disk inclination at least 30Â°, the two best quality classes, velocities measured to 10% or better; 2696 points appear here, against the published 2693 across 153 galaxies, the small difference coming from an approximated sample cut). Every point is one radius in one galaxy. The red curve is equation (5) with the published $g_\dagger$, not refit to this rendering. Dotted: the deep-limit square-root branch. Dashed: the line of equality.

How narrow is "narrow"? Astronomers quote scatter in **dex**, meaning powers of ten: a scatter of 0.13 dex means the points typically spread over a factor of $10^{0.13} \approx 1.35$, about 30%. The RAR's total scatter is 0.13 dex, and the paper's own error budget (velocity errors, inclination, distance, mass-to-light variation, flux calibration) already accounts for 0.12 dex of it, "leaving little room for intrinsic scatter" in the authors' words [7]. A follow-up fitting each galaxy individually bounds the relation's intrinsic width below 0.057 dex [8]. Two further facts deserve emphasis. Individual galaxies are indistinguishable in this plane: the outer points of giant galaxies land on top of the inner points of dwarfs. And the relation was built with the single universal $\Upsilon_\star$ of Section 3.1, so there were no per-galaxy adjustments anywhere in the construction. The source paper's closing assessment is that the relation is "tantamount to a natural law for rotating galaxies" [7].

### 3.3 The Baryonic Tullyâ€“Fisher Relation

The RAR's square-root branch, integrated over a whole galaxy, is equation (4), and that prediction has its own precise modern test. Lelli, McGaugh and Schombert [9] assembled the 118 SPARC galaxies with well-measured flat velocities and found: a slope statistically consistent with 4; an intrinsic scatter of $0.10 \pm 0.02$ dex; the observed scatter minimized exactly at the population-model value $\Upsilon_\star \approx 0.5$; and no residual dependence on galaxy size or surface brightness. Figure 3 shows the relation. The anchoring role of gas-rich dwarfs is visible there: for them the baryonic mass is mostly gas, measured directly at 21 cm, so the low-mass end of the relation is nearly free of the mass-to-light calibration, and it lands on the same slope-4 line. For contrast, surveys that use unresolved line widths instead of true flat velocities recover shallower slopes near 3; the slope-4, low-scatter result belongs to properly resolved rotation curves.

![Figure 3: the Baryonic Tully-Fisher relation â€” five decades of baryonic mass on a single slope-4 line](https://figures.tgtenev.com/tenev2026-mond-review/fig03-btfr.svg)

**Figure 3.** The Baryonic Tullyâ€“Fisher Relation from the public SPARC galaxy table (baryonic mass $M_b = 0.5\ L_{[3.6]} + 1.33\ M_\mathrm{HI}$, i.e. stars at the universal mass-to-light ratio plus measured atomic gas; galaxies with measured flat velocities and reliable inclinations). The red line is not a fit: it is equation (4) with the RAR's $g_\dagger$. Aqua points are gas-dominated galaxies, whose masses barely depend on the stellar calibration; they anchor the low-mass end on the same line. A slope-3 line (dashed) is shown for contrast.

One comparison shows why this precision matters. In a representative semi-analytic $\Lambda\text{CDM}$ treatment, the halo-to-halo variation in dark-matter structure alone predicts a *minimum* intrinsic BTFR scatter of about 0.15 dex (Dutton [10]), before any scatter from gas physics is added. The measured intrinsic scatter, $0.10 \pm 0.02$ dex, sits below that floor. Within $\Lambda\text{CDM}$, something must regulate galaxies more tightly than halo statistics alone would.

### 3.4 Was the tightness manufactured?

The classic objection to MOND's rotation-curve fits was that the mass-to-light ratio, the one genuinely free astrophysical conversion, was tuned galaxy by galaxy until the fits worked. Against the optical-photometry work of the 1980s and 90s, where $\Upsilon_\star$ genuinely varies between galaxies and was often left free, this was a fair complaint. Against the modern result it is not, for a specific reason: the headline RAR uses a **single, fixed, universal** $\Upsilon_\star$ (0.5 at 3.6 Î¼m for every disk, 0.7 for every bulge, values predicted in advance by stellar-population models), with "no adjustable parameters" in the authors' words, and the 0.13 dex tightness is what emerges anyway [7].

Per-galaxy fitting does exist in the literature, and its role is worth stating carefully. Li et al. [8] refit each SPARC galaxy allowing $\Upsilon_\star$, distance, and inclination to vary, but only within the ranges that stellar-population models and the measurement errors permit. The fitted values cluster near their expected values rather than running to extremes, and the leftover scatter shrinks toward pure measurement noise. The allowed freedom is absorbed by known uncertainties, not used to hide a mismatch. So the objection did not merely fail: its removal converted the relation from a suspicious fit into the strongest single piece of evidence in the subject.

Three caveats belong in the record [3, 7, 8]. About 10% of SPARC galaxies fit poorly even with the allowed freedom, mostly those with the worst distance or inclination data. The relation's *normalization*, and with it the absolute value of $g_\dagger$, rides on the near-infrared calibration (the tightness does not). And universality is a strong but actively tested claim, with occasional counterexamples proposed in dwarf-galaxy samples that have so far not survived scrutiny.

### 3.5 A second parameter, and how far the relation reaches

"One curve" is only as strong as the search for a second dimension. Lelli et al. [11] regressed the RAR's residuals against radius, luminosity, size, surface brightness, gas fraction, disk stability, and environment, and found no statistically significant second dependence; anything hidden contributes at or below the 0.1 dex level. The relation also extends far beyond where rotation curves can be measured. Mass bends passing light, so the images of distant background galaxies are slightly distorted by any foreground mass they shine past; averaging these distortions over many background galaxies measures the foreground gravity (this is **weak gravitational lensing**). Brouwer et al. [12] applied this entirely independent probe and traced the same relation, along the same curve, out to of order a megaparsec from galaxy centers, two decades deeper in $g_\mathrm{bar}$ than any rotation curve.

## 4. From a rule to a theory

### 4.1 What must be repaired, and the two ways to do it

Equation (2), applied bluntly to each body, violates the conservation laws: a pair of bodies obeying it can accelerate its own center of mass. Making the rule respectable requires deriving it from a Lagrangian (the standard machinery that guarantees energy and momentum conservation), and doing so forces a choice that the bare rule leaves open. **Modified gravity**: the field generated by mass strengthens at low acceleration, while $F = ma$ is untouched. **Modified inertia**: the response to force departs from $F = ma$ at low acceleration, while the gravitational field stays Newtonian. The two agree for circular orbits and differ elsewhere. Modified inertia is harder to formulate consistently (it generically requires equations of motion that depend on a body's entire history, not just its present state), and nearly all practical MOND work uses modified gravity.

### 4.2 AQUAL and QUMOND

Newtonian gravity can be written as a field equation: the potential $\Phi$ (whose spatial rate of change gives the acceleration, $\mathbf{g} = -\nabla\Phi$) obeys $\nabla^2\Phi = 4\pi G\rho$, with $\rho$ the mass density. Bekenstein and Milgrom [13] replaced it with the nonlinear equation

$$\nabla\cdot\left[\mu\left(\frac{|\nabla\Phi|}{a_0}\right)\nabla\Phi\right] = 4\pi G\rho, \quad (7)$$

a theory known as **AQUAL** (for "a quadratic Lagrangian"). Because it descends from a Lagrangian, it conserves energy and momentum; it reproduces the rule (2) exactly for spherical systems and differs by small computable corrections otherwise. A later reformulation, **QUMOND** (Milgrom [14]), reaches the same phenomenology using only linear equations of the familiar type and is the workhorse of MOND computer codes. One technical caution from the review literature: the function appearing in the field equation is not identical to the algebraic $\mu$ of equation (2), and conflating the two has produced published errors [3].

### 4.3 The External Field Effect

Equation (7) has a consequence with no analogue in Newtonian gravity or general relativity. In those theories a *uniform* external gravitational field is undetectable from inside a system: everything falls together, so internal dynamics proceed as if the field were absent (this is one statement of the equivalence principle, and it is why astronauts float). Because equation (7) is nonlinear in the *total* field, MOND breaks this. A small galaxy whose internal accelerations are below $a_0$ behaves differently depending on the external field it is immersed in: if a massive neighbor's field pushes the total acceleration above $a_0$, the deep-MOND boost is suppressed and the little galaxy turns quasi-Newtonian inside, even though the external field exerts no tide. This is the **External Field Effect** (EFE), illustrated in Figure 4.

![Figure 4: the External Field Effect â€” an isolated dwarf keeps its deep-MOND boost; the same dwarf embedded in a host's field becomes quasi-Newtonian](https://figures.tgtenev.com/tenev2026-mond-review/fig04-efe.svg)

**Figure 4.** The External Field Effect. Left: an isolated dwarf galaxy with internal accelerations below $a_0$ carries the full deep-MOND boost. Center: the same dwarf inside a host's field has total acceleration above $a_0$, and the boost is suppressed; the environment changes the internal dynamics. Right: why the effect is simultaneously MOND's cleanest structural signature and, because the external field is often poorly known, open to being invoked after the fact (the critics' complaint).

Three properties of the EFE matter. It is a genuine prediction that no dark-matter model makes, so it is a place where the frameworks can be told apart. It supplies MOND's explanation for otherwise awkward systems, including galaxies that appear to lack dark matter (Section 6.3). And its flexibility is a standing methodological complaint: the external field on a given system is often poorly known, so the effect can be invoked after the fact to explain either outcome. Chae et al. [15] reported statistical evidence for the EFE in the declining outer rotation curves of galaxies sitting in stronger environmental fields; the claim remains debated.

### 4.4 The interpolation function is a choice, and the choice has consequences

Between its two fixed limits, the function $\mu$ of equation (2) is chosen, not derived. Two classical choices recur in the literature, the "standard" function $\mu(x) = x/\sqrt{1+x^2}$ and the "simple" function $\mu(x) = x/(1+x)$ (Famaey and Binney [16]), and the modern RAR analyses fit the exponential form of equation (5). Through the transition region the families barely differ, and rotation-curve data scarcely discriminate among them (Figure 5a). In the **high-acceleration tail** they differ by orders of magnitude (Figure 5b), and there the choice is not academic. The "simple" function approaches Newton so slowly that a residual fraction $a_0/g_N$ of anomalous gravity survives in the Solar System. Planetary **ephemerides** (the precision tables of planetary positions, maintained by fitting centuries of observations and decades of spacecraft ranging) constrain any anomalous residual at Saturn to parts in $10^9$ or better (Pitjeva and Pitjev [17]), which excludes that slow tail outright. The "standard" function survives marginally; the exponential form dies away fast enough to be safe by a wide margin.

![Figure 5: interpolation-function families agree through the transition but differ by orders of magnitude in the high-acceleration tail, where planetary ephemerides exclude the slow ones](https://figures.tgtenev.com/tenev2026-mond-review/fig05-interpolation-functions.svg)

**Figure 5.** The free choice and its consequences. (a) Through the transition decade the classical families and the RAR's exponential fit are nearly indistinguishable. (b) The same functions' residual anomaly at high acceleration: the "simple" function's slow $1/y$ tail runs into the region excluded by planetary ephemerides; the "standard" function's $1/(2y^2)$ tail survives marginally; the exponential is safe by a wide margin. The tail is unconstrained by the galaxy data that motivated the law; it must be *chosen* safe.

The lesson generalizes beyond MOND. Solar-System safety is a property of the chosen function, not of the modified-dynamics idea as such, and any theory in this territory must exhibit, not assume, whatever suppresses its effects at high acceleration.

## 5. The strange value of the constant

One number in MOND has attracted more theoretical attention than everything else combined: the value of $a_0$ itself, because of what it numerically equals. The universe's expansion is quantified by the Hubble constant $H_0 \approx 70$ km/s per megaparsec: each megaparsec of distance adds about 70 km/s of recession speed. Dividing by a megaparsec ($3.09\times10^{22}$ m) puts it in pure units, $H_0 \approx 2.3\times10^{-18}\ \mathrm{s^{-1}}$, and its inverse, $1/H_0 \approx 14$ billion years, is roughly the age of the universe. Multiplying by the speed of light gives an acceleration:

$$c H_0 \approx 6.8\times10^{-10}\ \mathrm{m\ s^{-2}}, \qquad \frac{c H_0}{2\pi} \approx 1.1\times10^{-10}\ \mathrm{m\ s^{-2}} \approx a_0. \quad (8)$$

The acceleration at which galaxy dynamics changes character agrees, to within tens of percent, with the acceleration scale set by the expansion rate of the universe (this is the precise version of the informal statement in Section 2.1 about reaching the speed of light over the age of the universe). Equivalently, because the present-day expansion is dominated by the cosmological constant $\Lambda$ (so that $H_0^2 \approx \Lambda c^2/3$), one may write $a_0 \sim c^2\sqrt{\Lambda/3}/2\pi$: the scale can be read as tied to the vacuum energy instead. Figure 6 places $a_0$ on the acceleration number line and shows the coincidence.

![Figure 6: the acceleration number line â€” all Solar-System accelerations sit far above the MOND scale, which lands within an order-one factor of cH0](https://figures.tgtenev.com/tenev2026-mond-review/fig06-a0-coincidence.svg)

**Figure 6.** The scale and the coincidence. Every laboratory and Solar-System acceleration sits ten or more decades above the MOND scale; the anomaly begins where gravity is about as weak as the acceleration that takes an object from rest to the speed of light over the age of the universe. The ratio $c H_0/a_0 \approx 6$ is an order-one number: the galactic acceleration scale appears to know about cosmology.

Famaey and McGaugh [3] treat this as the deepest fact in the subject. Their closing figure is captioned, in their words, "the characteristic acceleration scale $a_0 \sim \sqrt{\Lambda}$ is in the data, *irrespective of the interpretation*," and their summary calls it "an empirically established fact" that is "mandatory for *any* successful model of galaxy formation and evolution to explain." Note the wording: whatever explains galaxies, dark matter included, must explain why this scale, with this value, organizes the data.

The two readings of the coincidence pull apart in the past, and that makes them testable. The expansion rate $H(z)$ was larger at earlier cosmic times (astronomers label epochs by redshift $z$, with larger $z$ meaning earlier), while $\Lambda$ is constant. If $a_0$ tracks the expansion rate, the acceleration scale was different in young galaxies and the relations of Section 3 should drift with redshift; if it is tied to $\Lambda$, they are frozen. Rotation curves of massive galaxies ten billion years in the past are just becoming measurable (Genzel et al. [18]) and hint at smaller discrepancies at early times, but severe selection effects (only the densest, highest-acceleration galaxies can be measured there) keep this frontier inconclusive for now.

## 6. The scorecard: where MOND succeeds, is contested, and fails

MOND's observational record is sharply scale-dependent, and the pattern of the record is itself informative. Famaey and McGaugh [3] score MOND against roughly 35 distinct observational tests; Table 1 condenses that scorecard and adds the major post-2012 developments.

**Table 1.** The observational ledger, condensed from the scorecard of Famaey and McGaugh [3] with post-2012 additions. "Successful" means the observation matches MOND's expectation without adjustment; "contested" means the data or their interpretation are in active dispute; "problematic" means the observation is not accounted for without additions the theory does not itself supply.

| Test | Standing | Note |
|---|---|---|
| Spiral rotation-curve shapes | successful | one-parameter fits; features track the baryons |
| Low-surface-brightness galaxies | successful | shapes predicted before measurement |
| Baryonic Tullyâ€“Fisher relation | successful | slope 4, low scatter, gas-rich anchor (Section 3.3) |
| Radial Acceleration Relation | successful | one curve, one parameter (Section 3.2) |
| Dwarf-spheroidal velocity dispersions | successful | with EFE caveats for the deepest-embedded cases |
| Weak-lensing extension of the RAR | successful | same curve to ~1 Mpc (Section 3.5) |
| Wide binary stars | contested | live dispute (Section 6.4) |
| Galaxies apparently lacking dark matter | contested | EFE explanation debated (Section 6.3) |
| Galaxy clusters | problematic | factor ~2 of mass still missing (Section 6.2) |
| Colliding clusters (Bullet Cluster) | problematic | lensing peaks track galaxies, not gas (Section 6.2) |
| Cosmic microwave background, cosmology | problematic | requires engineered relativistic completions (Section 7) |

### 6.1 The successes

Beyond the rotation-curve, RAR, and BTFR results of Sections 2 and 3, two entries deserve comment. The low-surface-brightness prediction is the clearest case of MOND predicting *in advance*: Milgrom stated in 1983, before such galaxies were well measured, that dim, spread-out disks would show large discrepancies everywhere, and when they were measured a decade later they did. Velocity dispersions of the Milky Way's dwarf-spheroidal satellites, tiny pressure-supported galaxies deep in the low-acceleration regime, likewise land near the MOND expectation, though the cases most deeply embedded in the Milky Way's field require the EFE and are individually arguable [3].

### 6.2 The durable failure: galaxy clusters

A galaxy cluster is the largest bound structure in the universe: hundreds to thousands of galaxies plus, dominating the visible mass several-fold, a diffuse atmosphere of hot X-ray-emitting gas. Applying Newtonian gravity to a rich cluster's visible baryons understates its measured dynamical mass by a factor near 100 at the naive level; counting the hot gas closes most of that, to a factor near 8; applying MOND closes most of the rest. But a stubborn residual factor of about 2 remains, concentrated toward cluster centers, and no choice of interpolation function removes it [3, 19]. The **Bullet Cluster** (Clowe et al. [20]) displays the same shortfall in a collision: two clusters passed through each other, the hot gas of each (most of the visible mass) slowed and pooled between them, the galaxies flew ahead, and the weak-lensing map shows the total mass peaked on the galaxies, not on the gas. That geometry is natural if most mass is collisionless and unseen, and awkward for any theory in which gravity traces the visible matter alone.

MOND proponents respond by positing additional unseen matter in clusters: undetected ordinary baryons, or a hot component such as sterile neutrinos (a hypothetical neutrino variant interacting only by gravity). Critics reply that a modified-gravity theory requiring extra unseen mass has conceded the principle. Either way the plain statement stands: **MOND reduces the unseen-mass problem in clusters; it does not eliminate it.**

### 6.3 Hard cases among the dwarfs

Ultra-diffuse galaxies (galaxies as large as giants but exceedingly dim) cut both ways. The satellites NGC 1052-DF2 and DF4 show internal motions consistent with *no* dark matter at all (van Dokkum et al. [21]). A halo can plausibly be stripped away by tides; a law of nature cannot be switched off, so MOND must attribute these systems' Newtonian behavior to the EFE of the nearby giant NGC 1052, an explanation whose adequacy is debated. In the opposite direction, the isolated gas-rich dwarf AGC 114905 shows a nearly Newtonian rotation curve where MOND predicts a large boost and no external field can be blamed (Mancera PiÃ±a et al. [22]); here the contested quantity is the galaxy's inclination, which the discrepancy claim depends on sensitively. Both cases illustrate the same methodological point: the EFE gives MOND real explanatory reach and real vulnerability to the charge of unfalsifiability, at the same time.

### 6.4 A test in progress: wide binary stars

Pairs of stars orbiting each other at separations wider than a few thousand astronomical units (AU, the Earthâ€“Sun distance) have mutual gravitational accelerations that approach and fall below $a_0$. They are a clean discriminating test, because nobody proposes that dark matter clumps inside a stellar binary: Newtonian gravity predicts ordinary Keplerian motion there, while MOND (with the Milky Way's external field properly included via the EFE) predicts relative velocities enhanced by roughly 15â€“20%. The European Space Agency's *Gaia* satellite, which measures positions and motions for about two billion stars, supplies exactly the needed data.

The field is in open conflict. Chae [23] and, independently, Hernandez and collaborators report a velocity enhancement consistent with the MOND expectation, across several analyses. Banik et al. [24] analyze a differently selected sample and report a strong null result, quoted near 19Ïƒ against the MOND prediction. Each camp disputes the other's sample selection, treatment of unseen third companions (a hidden close companion inflates the apparent relative velocity), and statistical modeling, rather than the underlying *Gaia* measurements. The dispute is genuinely unresolved: treat wide binaries as a test in progress, not as a verdict for either side.

## 7. Making MOND relativistic: TeVeS, GW170817, AeST

Everything above is non-relativistic. To address gravitational lensing, cosmology, and the cosmic microwave background (the **CMB**: the relic radiation released when the universe became transparent about 380,000 years after the beginning, whose pattern of small ripples encodes the early universe's contents), MOND must be embedded in a relativistic theory, one that, like general relativity, treats light and gravity together. The history compresses to three steps.

The first serious construction, **TeVeS** (Bekenstein [25]), added new tensor, vector, and scalar fields to gravity and achieved the milestone of bending light by the right amount: in TeVeS, lensing traces the same enhanced gravity the stars feel. It was widely regarded as the proof that relativistic MOND was possible. It then failed against a single event. **GW170817**, a merger of two neutron stars observed in 2017, delivered its gravitational waves and its burst of gamma rays within seconds of each other after both had traveled about 130 million light-years (Abbott et al. [26]); the two propagation speeds therefore agree to about one part in $10^{15}$. TeVeS-class theories generically predict gravitational waves traveling at a different effective speed than light, and this single measurement ruled out the whole family.

The surviving construction is **AeST** (Aether-Scalar-Tensor theory; Skordis and ZÅ‚oÅ›nik [27]). It is built so that gravitational waves propagate at exactly the speed of light, and its fields are arranged to behave, in the early universe, like a pressureless medium ("dust") that plays the gravitational role cold dark matter plays at the epoch the CMB was released; with that arrangement it fits the CMB's acoustic structure (the characteristic pattern of ripple sizes, set by sound waves in the hot early universe) at a level competitive with $\Lambda\text{CDM}$ on linear scales. The construction is engineering rather than explanation: the fields are arranged to produce the required early-universe behavior, not derived from a deeper principle. It nonetheless changes the state of the debate. The statement "MOND is ruled out by the CMB or by gravitational waves" is out of date. The accurate statement is that *simple* relativistic MOND is ruled out, and that the surviving completions are elaborate.

Two lessons from this history transfer to any alternative theory of the discrepancy. Light must fall in the same effective potential the stars feel, or lensing observations rule the theory out at once. And the CMB's acoustic structure must be preserved, which is the single hardest cosmological demand on any theory without particle dark matter.

## 8. MOND and the standard cosmology: what actually hangs on this

Loose statements in both directions ("MOND disproves dark matter"; "the Bullet Cluster disproved MOND") are common and wrong. The precise situation is asymmetric in an instructive way.

Where $\Lambda\text{CDM}$'s support is strongest (the CMB's acoustic structure, primordial element abundances, the growth of large-scale structure, cluster masses), MOND is weakest. Where MOND is strongest (the one-parameter precision of galaxy scaling relations), $\Lambda\text{CDM}$ faces its most demanding tests. And the two kinds of success differ in *kind*, not just location. MOND's galaxy-scale results are theorems of one law: equation (4) *is* the BTFR, derived in four lines. The corresponding $\Lambda\text{CDM}$ account is emergent: halo assembly plus gas physics plus star-formation feedback must together produce a relation whose intrinsic scatter is measured below the floor set by halo-to-halo variation alone [10], and whose acceleration scale coincides with $cH_0$ for no reason internal to the model. Famaey and McGaugh [3] quantify what the regulation must accomplish: to keep the BTFR tight, the fraction of baryons a halo fails to turn into visible stars and gas must track its rotation velocity in lockstep ("we know not only how many baryons we see, but also how many we do not see â€” a remarkable feat of non-observation," as they put it). Simulation groups have reported RAR-like relations emerging from feedback (Ludlow et al. [28]); whether the emergent relation achieves the observed tightness and the zero-parameter normalization, and survives in the gas-rich dwarfs where feedback has little to regulate against, remains actively contested.

The stakes run in both directions. If the galaxy-scale regularity is fundamental physics, the case for particle dark matter at galaxy scales dissolves, and the cosmological successes of $\Lambda\text{CDM}$ become constraints that any completed alternative must re-derive (AeST's engineered early-universe sector is the current existence proof of how demanding that is). If instead the regularity is emergent regulation within $\Lambda\text{CDM}$, then its measured tightness is a permanent, quantitative obligation on galaxy-formation theory, growing stricter with every improvement in the data. On either reading, the regularity itself, one curve, one parameter, one cosmologically coincident scale, is the thing that must be explained.

## 9. What any explanation must accomplish

The record above can be distilled into a requirements list, stated so that it applies to any candidate account of the mass discrepancy: a dark-matter model, a modified law, or anything else. The items are ordered roughly by how strongly they discriminate.

1. **The scale.** Produce a transition at $g \approx a_0 \approx cH_0/2\pi$, and ideally explain the cosmological coincidence rather than inserting the number.
2. **The low-acceleration exponent.** Recover $g \to \sqrt{a_0\ g_\mathrm{bar}}$, equivalently the slope-4 BTFR. This is the most restrictive single constraint: mechanisms whose extra gravity is a simple power of the source mass produce the wrong exponent and are excluded at once.
3. **Tightness and universality.** The effect must follow from the baryon distribution almost deterministically: intrinsic scatter below a few hundredths of a dex, and no second parameter. Figure 7 shows why this filters whole classes of explanation: any account in which the extra gravity also depends on a galaxy's individual history, environment, or motion must keep that dependence below the observed scatter, which is a demanding requirement.
4. **Small-scale safety.** Whatever suppresses the effect at high accelerations must be exhibited and tested (Section 4.4 showed that even within MOND, safety is a property of a choice), and the account should also state its prediction for wide binary stars.
5. **Clusters, stated plainly.** Say what the mechanism does in clusters. The observed shape of the record is that galaxies obey the one-parameter law while clusters retain a factor-2 shortfall concentrated at their centers, at acceleration values where galaxies show no anomaly; an account that matches the galaxy data and adds nothing in clusters is matching the record as it stands, and an account claiming to repair clusters through the same law that fits galaxies must explain why the change does not spoil the galaxy fits [3].
6. **A point of divergence.** Make at least one prediction that differs from both MOND's and $\Lambda\text{CDM}$'s (the redshift behavior of the scale, the wide-binary regime, an environmental signature), so that the account is falsifiable on its own terms.

![Figure 7: two synthetic acceleration-relation panels â€” the scattered cloud produced if each galaxy's halo depended on its own history, versus the observed tight relation](https://figures.tgtenev.com/tenev2026-mond-review/fig07-tightness.svg)

**Figure 7.** The tightness as a filter on explanations. (a) A synthetic radial-acceleration plane for the case where each galaxy's extra gravity depends on its own assembly history, environment, or motion: a spread of factors of several at fixed baryons. (b) A synthetic plane at the observed scatter. The data are panel (b): the extra gravity is determined by the baryon distribution and almost nothing else, and any proposed explanation must reproduce that near-determinism.

## 10. Summary

- In galaxy outskirts, measured rotation exceeds what visible matter's gravity supports. Either unseen mass exists (dark matter) or the dynamical law changes at galactic scales (modified dynamics). The discrepancy correlates with acceleration, not with size or mass.
- Milgrom [1, 2] proposed in 1983 that dynamics changes below a universal acceleration $a_0 \approx 1.2\times10^{-10}\ \mathrm{m\ s^{-2}}$. In the low-acceleration limit, four lines of algebra yield flat rotation curves and the slope-4 Baryonic Tullyâ€“Fisher Relation, and one constant organizes some ten otherwise-independent galactic regularities [3].
- The modern evidence is precise. Across 153 galaxies and 2693 points, observed acceleration is a single one-parameter function of the baryonic acceleration (the Radial Acceleration Relation), with transition scale $g_\dagger = 1.20\times10^{-10}\ \mathrm{m\ s^{-2}}$, total scatter 0.13 dex, intrinsic scatter below 0.057 dex, and no credible second parameter [7, 8, 11]. The relation was built with a single universal mass-to-light ratio, so it is not a product of per-galaxy tuning, and weak lensing extends it to megaparsec scales [12].
- The bare rule was embedded in field theories that conserve energy and momentum and support computation (AQUAL, QUMOND [13, 14]). The formulation predicts the External Field Effect, a violation of the strong equivalence principle that is simultaneously MOND's most distinctive signature and its most criticized flexibility. The interpolation function connecting the two regimes is a free choice, and Solar-System data already exclude the slow-tailed choices [16, 17].
- The scale itself is the deepest clue: $a_0 \approx cH_0/2\pi$ within tens of percent, tying galaxy dynamics to cosmology for no known reason. Whether the scale is frozen (a $\Lambda$-like reading) or tracks cosmic history (an $H$-like reading) is testable against high-redshift galaxies [18].
- The record is scale-dependent: MOND is repeatedly successful in disk galaxies, contested in wide binaries and ultra-diffuse dwarfs, and fails by a factor of about 2 in galaxy clusters, where unseen mass is reduced but not eliminated [3, 19, 20]. Relativistic completions exist; the simple ones are ruled out by the equality of gravitational-wave and light speeds, and the surviving one (AeST [27]) fits the CMB by construction rather than by explanation.
- Whatever MOND's fate as a theory, the empirical regularity it summarizes, one curve with one cosmologically coincident parameter governing the gravity of galaxies, is established. Explaining it, rather than explaining it away, is a requirement on every theory of galactic dynamics, and Section 9's list states what an explanation must deliver.

## Acknowledgements

This review was prepared with the assistance of an AI assistant (Anthropic's Claude), used for drafting, for organizing the cited literature, and for generating the figures, under the author's direction. The author set the scope and framing, checked the claims and numerical values against the cited primary sources, and is responsible for the content, including any errors that remain.

## References

[1] M. Milgrom, "A modification of the Newtonian dynamics as a possible alternative to the hidden mass hypothesis," Astrophys. J., vol. 270, pp. 365â€“370, 1983.

[2] M. Milgrom, "A modification of the Newtonian dynamics â€” Implications for galaxies," Astrophys. J., vol. 270, pp. 371â€“383, 1983; and companion, pp. 384â€“389, 1983.

[3] B. Famaey and S. S. McGaugh, "Modified Newtonian Dynamics (MOND): Observational phenomenology and relativistic extensions," Living Rev. Relativ., vol. 15, 10, 2012.

[4] V. C. Rubin and W. K. Ford, Jr., "Rotation of the Andromeda nebula from a spectroscopic survey of emission regions," Astrophys. J., vol. 159, 379, 1970.

[5] A. Bosma, "21-cm line studies of spiral galaxies. II," Astron. J., vol. 86, pp. 1825â€“1846, 1981.

[6] F. Lelli, S. S. McGaugh, and J. M. Schombert, "SPARC: Mass models for 175 disk galaxies with Spitzer photometry and accurate rotation curves," Astron. J., vol. 152, 157, 2016.

[7] S. S. McGaugh, F. Lelli, and J. M. Schombert, "The radial acceleration relation in rotationally supported galaxies," Phys. Rev. Lett., vol. 117, 201101, 2016.

[8] P. Li, F. Lelli, S. McGaugh, and J. Schombert, "Fitting the radial acceleration relation to individual SPARC galaxies," Astron. Astrophys., vol. 615, A3, 2018.

[9] F. Lelli, S. S. McGaugh, and J. M. Schombert, "The small scatter of the baryonic Tullyâ€“Fisher relation," Astrophys. J. Lett., vol. 816, L14, 2016.

[10] A. A. Dutton, "The baryonic Tullyâ€“Fisher relation and galactic outflows," Mon. Not. R. Astron. Soc., vol. 424, pp. 3123â€“3128, 2012.

[11] F. Lelli, S. S. McGaugh, J. M. Schombert, and M. S. Pawlowski, "One law to rule them all: The radial acceleration relation of galaxies," Astrophys. J., vol. 836, 152, 2017.

[12] M. M. Brouwer et al., "The weak lensing radial acceleration relation: Constraining modified gravity and cold dark matter theories with KiDS-1000," Astron. Astrophys., vol. 650, A113, 2021.

[13] J. Bekenstein and M. Milgrom, "Does the missing mass problem signal the breakdown of Newtonian gravity?" Astrophys. J., vol. 286, pp. 7â€“14, 1984.

[14] M. Milgrom, "Quasi-linear formulation of MOND," Mon. Not. R. Astron. Soc., vol. 403, pp. 886â€“895, 2010.

[15] K.-H. Chae, F. Lelli, H. Desmond, S. S. McGaugh, P. Li, and J. M. Schombert, "Testing the strong equivalence principle: Detection of the external field effect in rotationally supported galaxies," Astrophys. J., vol. 904, 51, 2020.

[16] B. Famaey and J. Binney, "Modified Newtonian dynamics in the Milky Way," Mon. Not. R. Astron. Soc., vol. 363, pp. 603â€“608, 2005.

[17] E. V. Pitjeva and N. P. Pitjev, "Relativistic effects and dark matter in the Solar system from observations of planets and spacecraft," Mon. Not. R. Astron. Soc., vol. 432, pp. 3431â€“3437, 2013.

[18] R. Genzel et al., "Strongly baryon-dominated disk galaxies at the peak of galaxy formation ten billion years ago," Nature, vol. 543, pp. 397â€“401, 2017.

[19] R. H. Sanders and S. S. McGaugh, "Modified Newtonian dynamics as an alternative to dark matter," Annu. Rev. Astron. Astrophys., vol. 40, pp. 263â€“317, 2002.

[20] D. Clowe et al., "A direct empirical proof of the existence of dark matter," Astrophys. J. Lett., vol. 648, L109, 2006.

[21] P. van Dokkum et al., "A galaxy lacking dark matter," Nature, vol. 555, pp. 629â€“632, 2018; and Astrophys. J. Lett., vol. 874, L5, 2019.

[22] P. E. Mancera PiÃ±a et al., "No need for dark matter: resolved kinematics of the ultra-diffuse galaxy AGC 114905," Mon. Not. R. Astron. Soc., vol. 512, pp. 3230â€“3242, 2022.

[23] K.-H. Chae, "Breakdown of the Newtonâ€“Einstein standard gravity at low acceleration in internal dynamics of wide binary stars," Astrophys. J., vol. 952, 128, 2023.

[24] I. Banik et al., "Strong constraints on the gravitational law from Gaia DR3 wide binaries," Mon. Not. R. Astron. Soc., vol. 527, pp. 4573â€“4615, 2024.

[25] J. D. Bekenstein, "Relativistic gravitation theory for the modified Newtonian dynamics paradigm," Phys. Rev. D, vol. 70, 083509, 2004.

[26] B. P. Abbott et al., "Gravitational waves and gamma-rays from a binary neutron star merger: GW170817 and GRB 170817A," Astrophys. J. Lett., vol. 848, L13, 2017.

[27] C. Skordis and T. ZÅ‚oÅ›nik, "New relativistic theory for modified Newtonian dynamics," Phys. Rev. Lett., vol. 127, 161302, 2021.

[28] A. D. Ludlow et al., "Mass-discrepancy acceleration relation: A natural outcome of galaxy formation in cold dark matter halos," Phys. Rev. Lett., vol. 118, 161103, 2017; see also A. Di Cintio and F. Lelli, Mon. Not. R. Astron. Soc., vol. 456, L127, 2016.

---

*A note on the figures.* Figures 1â€“3 are built from the public SPARC database [6] with the sample cuts stated in their captions; Figures 4â€“7 are original diagrams. No figure is reproduced from a published paper. Where this review and a primary source disagree, the source is correct.
