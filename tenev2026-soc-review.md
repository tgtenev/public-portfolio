# Avalanches and Self-Organized Criticality: The Idea, the Theory, and the Evidence

**Document Metadata**

| | |
|---|---|
| **Store** | public-portfolio |
| **Publication** | Preprint, Zenodo, 2026 |
| **Published** | 2026-08-29 (Zenodo v1) |
| **DOI / URL** | https://doi.org/10.5281/zenodo.22151213 — concept DOI, cite this one for all versions; this version is 10.5281/zenodo.22151214 |
| **Licence** | CC BY 4.0 |
| **Cite as** | T. G. Tenev, "Avalanches and self-organized criticality: the idea, the theory, and the evidence," Zenodo, preprint, 2026, doi: 10.5281/zenodo.22151213. |

---

**Tichomir Tenev**
Independent Researcher
ticho@tenev.com

**Scope.** This document is a background reference, not a research contribution. It exists so that a companion research paper need not carry the avalanche and self-organized-criticality background itself: that paper states the background at a high level and cites this review for the detail. Nothing here is new. There are no new results, no proposed model, and no advocacy for or against any application of the framework; every quantitative statement is drawn from the published literature cited in place. The reader is assumed to know introductory probability and the vocabulary of equilibrium phase transitions (order parameter, control parameter, universality) at the level of a first statistical-mechanics course; everything more specialized is built in place.

**Abstract.** Many slowly driven systems respond to smooth loading not smoothly but in bursts: a sandpile fed one grain at a time relaxes through avalanches, a ferromagnet in a slowly rising field magnetizes through discrete domain-wall jumps, and a tectonic fault loaded over centuries slips in earthquakes. In each case the burst sizes span many decades and follow a power-law distribution with a cutoff at some largest scale, a pattern now collectively called crackling noise. Bak, Tang, and Wiesenfeld proposed in 1987 that such systems drive themselves to the critical point of a phase transition, with no one tuning anything, and named the idea self-organized criticality (SOC). This review develops the theory of that proposal from first exposure. It begins with the branching process that governs mean-field avalanches and fixes the size exponent $\tau = 3/2$, and with the resolution of the self-organization puzzle as a feedback loop that holds a conserved density at the critical point of an underlying absorbing-state phase transition. It then presents the exact mean-field result that bulk dissipation moves the self-organized state a calculable distance below criticality, with mean avalanche size $\langle s\rangle = 1/\epsilon$ set by the dissipation rate $\epsilon$, and the demonstration that non-conserving systems reach only a hovering, quasi-critical state whose observed statistics are a convolution over a fluctuating background. The abelian sandpile, the exactly solvable case, and the geometry connecting an avalanche's size to its spatial extent complete the theoretical core. One practical lesson organizes the whole subject, and the review returns to it repeatedly: the exponents of the power law are universal and computable, while the cutoff and the mean avalanche size are not universal and must be supplied by whatever mechanism limits the cascades, whether system size, dissipation, or distance from threshold. The closing sections examine the experimental record, from Barkhausen noise and rice piles to metallic glasses and neuronal avalanches, and state what any slowly driven dissipative system inherits from this framework.

## 1. The phenomenon: crackling noise

### 1.1 Bursts under smooth driving

Take a system with many interacting elements, each held in place by a local threshold, and load it slowly. Slowly means that the loading timescale is much longer than the internal relaxation timescale, so the system finishes responding to one increment before the next arrives. Most increments produce little: one element yields, or none does. Occasionally a single increment triggers a cascade, in which one yielding element pushes its neighbors past their thresholds, those push theirs, and the disturbance grows to involve thousands or millions of elementary events before it stops. The response to smooth input is then a train of discrete, intermittent releases whose sizes span many orders of magnitude. Sethna, Dahmen, and Myers [5] named this pattern crackling noise, after the sound of a crumpling candy wrapper, and their survey collects its instances: Barkhausen pulses in soft magnets, slip events in sheared granular packs, vortex avalanches in superconductors, acoustic emission in fracturing solids, and earthquakes.

The empirical regularities that motivated the theory predate it by decades. Gutenberg and Richter [2] established in 1944 that earthquake magnitudes follow a logarithmic frequency law with no characteristic size over the observed range; expressed in seismic moment, the fraction of events larger than $M$ falls off as a power law, with a cumulative exponent near $2/3$ [12]. Omori [3] found in 1894 that the rate of aftershocks decays as roughly the inverse of the time since the main shock, again with no characteristic timescale. Barkhausen [4] discovered in 1919 that a ferromagnet magnetizes audibly, in discrete jumps, and modern measurements resolve those jumps into avalanches whose size distribution is a power law over more than three decades [14]. Each of these laws says the same thing in its own domain: the system has no typical event size, and the large events are not a different phenomenon from the small ones but the same phenomenon continued.

### 1.2 The 1987 proposal

In equilibrium statistical mechanics, scale-free behavior of this kind is the signature of a critical point, and a critical point is ordinarily reached only by tuning: a ferromagnet shows power-law correlations at its Curie temperature and not elsewhere. The puzzle posed by the empirical laws above is that nobody tunes the Earth's crust or a magnet's disorder to a special value, yet the power laws are there. Bak, Tang, and Wiesenfeld [1] proposed a resolution: some driven, spatially extended, dissipative systems evolve on their own toward a critical state and then stay there, so that criticality is an attractor of the dynamics rather than a tuned point. They called the idea self-organized criticality, abbreviated SOC throughout this review, and illustrated it with a cellular-automaton model of a sandpile (Section 2) whose avalanche sizes indeed follow a power law in the steady state.

Two historical footnotes are worth recording, because both recur in the modern assessment of the field. First, the original paper's title promised an explanation of $1/f$ noise, the ubiquitous low-frequency spectrum of slowly fluctuating systems; later analyses showed that the sandpile model's own power spectrum is closer to $1/f^2$, so the original motivation detached from the model early [7]. Second, the phrase "self-organized" proved stronger than the mechanism: Sections 4 and 6 show that the criticality of sandpiles rests on a limit of infinitely slow driving and on a conservation law, so the tuning is hidden rather than absent. Neither footnote diminishes the subject. The models launched by the proposal turned out to be exactly analyzable to an unusual degree, and the theory that grew from them, assembled across the decade 1987 to 2000, is the subject of this review.

## 2. What scale-free means operationally

### 2.1 The size distribution and its two independent parts

The quantitative signature shared by all crackling systems is the avalanche size distribution. Let $s$ count the elementary events in one cascade: topplings in a sandpile, spin flips in one Barkhausen pulse, elementary slips in one earthquake. The observed distribution takes the form

$$P(s) \ \sim\ s^{-\tau}\ h(s/s_c)\ , \quad (1)$$

where $\tau$ is the size exponent and $h$ is a cutoff function, approximately constant for arguments well below one and falling off exponentially beyond the characteristic scale $s_c$ [11, 13]. A companion distribution governs avalanche durations $T$, with its own exponent and cutoff, and Section 4.4 gives the relation between the two.

Two logically independent questions hide inside equation (1), and keeping them separate is the single most useful discipline the field teaches. The exponent $\tau$ is set by the universality class of the dynamics, meaning the dimensionality, the symmetries, the range of the interactions, and the conservation laws; it is insensitive to microscopic detail, and it is computable in the solvable limits developed below. The cutoff $s_c$, and with it the mean avalanche size $\langle s\rangle$, is not universal: it is set by whatever limits the cascades, which may be the system size, the bulk dissipation rate, or the distance from a critical point, and no amount of universality reasoning will produce its value. The claim of Bak, Tang, and Wiesenfeld [1], restated in this vocabulary, is that some driven systems arrange for the cutoff to diverge by themselves. Sections 4 through 6 build the machinery to state exactly when that claim is true, and the answer will be that it is true for conserving systems in a slow-driving limit and instructively false otherwise.

### 2.2 Measuring a power law, and misidentifying one

Because the theory's central prediction is a power law, the practical question of how power laws are recognized deserves a paragraph before any theory. On doubly logarithmic axes a power law is a straight line, and the standard analysis bins event sizes logarithmically, plots the estimated density, and fits the slope over the region below the cutoff. Three failure modes recur across the literature. First, a straight-looking segment over one or two decades is weak evidence, since many non-power-law distributions, including lognormals and exponential mixtures, imitate straight lines over short ranges; the modern statistical treatment of this problem is the maximum-likelihood framework of Clauset, Shalizi, and Newman [6]. Second, the fitted exponent depends on where the cutoff region begins, and an unrecognized cutoff bends the fit systematically. Third, and most specific to this subject, Section 7 shows that a system fluctuating around a critical point produces a convolution of sub- and supercritical distributions that can imitate a power law over several decades without being one. The field's own history is a catalog of claims that dissolved under longer simulations and better statistics, and Section 10 collects the survey of what held up. The practical rule that emerges: an exponent claim needs several decades of data, an explicit statement of the cutoff model, and ideally a second observable (Section 4.4 supplies one) measured on the same events.

## 3. Sandpile models

### 3.1 The rules

The models that carry the theory are cellular automata of disarming simplicity. The original model of Bak, Tang, and Wiesenfeld [1], hereafter the BTW sandpile, lives on an $L \times L$ square lattice. Each site $i$ carries an integer $z_i$, pictured as a local count of sand grains. One grain is added to a randomly chosen site. If any site's count reaches the threshold value 4, that site topples: its count drops by 4, and each of its four neighbors gains one grain. Topplings may push neighbors past threshold, and those sites topple in turn, until no site is above threshold; the complete cascade set off by one grain addition is an avalanche, and its size $s$ is the number of topplings. Only then is the next grain added, which is the slow-driving condition in algorithmic form. At the lattice edges, toppling grains fall off and are gone: the boundaries are open, and they are the model's only loss mechanism.

Manna [8] introduced a stochastic variant that plays a central role in what follows. In the Manna model each site holds 0 or 1 grain stably; a site receiving a second grain topples, sending two grains to randomly chosen neighbors. The randomness of the target sites makes the model tractable by mean-field and field-theoretic methods that the deterministic BTW rules resist, and Section 10 returns to the once-surprising fact that the two models do not share a universality class.

Both models reach a statistical steady state in which grain input balances boundary outflow, and in that state the avalanche size distribution follows equation (1) with a cutoff set by the system size. The steady state is an attractor: whatever the initial condition, the dynamics finds it.

### 3.2 What conservation already implies

One exact statement can be made before any detailed theory, and it foreshadows the entire logic of Sections 5 and 6. In the steady state, every added grain must eventually leave through the boundary, and between addition and exit it moves only when a site topples. A grain's trajectory under the toppling rules is an unbiased random walk, and a random walk started at a random interior site of an $L \times L$ domain needs of order $L^2$ steps to reach the boundary. Each toppling moves a fixed number of grains, so the mean number of topplings per added grain, which is exactly the mean avalanche size, must grow as

$$\langle s\rangle \ \sim\ L^2\ . \quad (2)$$

The mean avalanche size diverges with system size, unconditionally, in any dimension, for any conserving toppling rule [13, 15]. This little bookkeeping argument carries two lessons. A divergent mean forces the size distribution to have a heavy tail, so conservation plus open boundaries already guarantees broad avalanche statistics before any criticality argument is made. And the mean is fixed by a conservation balance, input per drive event against loss per toppling, rather than by any universal exponent; this is the first appearance of the cutoff-versus-exponent division of Section 2.1, and it recurs as an exact identity in Section 6.

## 4. The branching process

### 4.1 From Galton and Watson to avalanches

The solvable limit that anchors all avalanche theory is older than the subject: it is the branching process introduced by Galton and Watson in the 1870s to compute the extinction probability of family surnames, and developed as a mathematical field in its own right (the standard treatise is Harris [9]). Strip an avalanche to its minimum. One active element either triggers new activity or does not; each newly activated element behaves the same way, independently. The one number that matters is the branching ratio $n_b$, defined as the mean number of new active elements created per active element. Three regimes follow immediately, and Figure 1 illustrates them:

- In the subcritical regime, $n_b < 1$, activity dies out exponentially fast and all avalanches are finite.
- In the critical regime, $n_b = 1$, activity is marginal and avalanches of all sizes occur with a power-law distribution.
- In the supercritical regime, $n_b > 1$, an avalanche never stops with finite probability.

![Figure 1: three branching trees illustrating subcritical, critical, and supercritical cascades](https://figures.tgtenev.com/tenev2026-soc-review/fig01-branching-regimes.svg)

**Figure 1.** The branching process. Each active site (filled) independently activates a number of offspring whose mean is the branching ratio $n_b$; the three panels show representative cascades in the subcritical, critical, and supercritical regimes. The mean avalanche size obeys the exact bookkeeping $\langle s\rangle = 1/(1-n_b)$, which diverges as $n_b \to 1^-$. Sitting near, but below, the critical point is how a system produces large-but-finite avalanches without any quantity being tuned to infinity.

The connection to sandpiles is the mean-field limit. When the lattice dimension is high, or the toppling targets are chosen at random as in a random-neighbor model, an avalanche almost never revisits a site, so its active front consists of independent elements and the cascade is exactly a branching process [10, 11]. The branching ratio then has a concrete meaning: it is the probability that a grain arriving at a site triggers a toppling, times the number of grains a toppling releases.

### 4.2 The mean size is exact bookkeeping

Generation $m$ of a cascade contains on average $n_b^m$ active elements, so the mean total size is a geometric series:

$$\langle s\rangle \ =\ \sum_{m=0}^{\infty} n_b^{\ m} \ =\ \frac{1}{1-n_b} \qquad (n_b < 1)\ . \quad (3)$$

No approximation enters. Any system whose cascades are branching-like, whatever its microphysics, has its mean avalanche size pinned to its branching deficit $1 - n_b$; a mean size of one thousand means the system sits a distance of exactly one part in a thousand below the critical point. This identity is the workhorse of everything that follows.

### 4.3 The size distribution and the exponent 3/2

The full distribution requires the generating-function machinery of Harris [9], and the two-offspring case shows it at tutorial level. Let each active site branch into two with probability $p$ and stop with probability $1-p$, so that $n_b = 2p$ and the critical point is $p_c = 1/2$. Define the generating function $f(x) = \sum_s P(s)\ x^s$. Because the two offspring found independent copies of the whole process, $f$ obeys the recursion

$$f_{n+1}(x) \ =\ x\left[(1-p) + p\ f_n^2(x)\right]\ , \quad (4)$$

whose fixed point is a quadratic equation with the closed solution $f(x) = \left(1 - \sqrt{1-4x^2 p(1-p)}\right)/(2xp)$ [10]. Expanding the square root in powers of $x$ and reading off coefficients gives, for $s \gg 1$,

$$P(s) \ =\ \sqrt{\frac{2(1-p)}{\pi p}}\ \ s^{-3/2}\ e^{-s/s_c}\ , \qquad s_c \ =\ \frac{-2}{\ln\left[4p(1-p)\right]}\ . \quad (5)$$

Two facts in equation (5) deserve to be internalized. First, the exponent $\tau = 3/2$ is not adjustable: it is the square-root branch point of the generating function, and it has a random-walk reading that explains its ubiquity. The number of active sites in a cascade performs a random walk (up steps when sites branch, down steps when they stop), and the avalanche ends at the walk's first return to zero; the first-return probability of an unbiased walk falls off with the $-3/2$ power, and that exponent is $\tau$. Second, expanding the cutoff near criticality with $n_b = 2p \to 1$ gives

$$s_c \ \approx\ \frac{2}{(1-n_b)^2}\ =\ 2\ \langle s\rangle^2\ . \quad (6)$$

The cutoff sits quadratically beyond the mean. A $\tau = 3/2$ power law is so heavy-tailed that its mean is dominated by its rare largest events: the probability that a given avalanche approaches the cutoff scale is only of order $1/\langle s\rangle$, yet those rare events carry most of the transported total [12]. Figure 2 shows the distribution (5) for three values of the branching deficit.

An exactly solvable check on these asymptotics exists. For the variant in which every branching event has a fixed yield, Fisher [12] notes that the size distribution is exactly the Borel distribution, $P(s) = e^{-\rho s}(\rho s)^{s-1}/s!$, whose Stirling-formula limit reproduces equation (5) term by term; the asymptotic form is therefore trustworthy all the way into its prefactor.

![Figure 2: log-log avalanche size distributions with the 3/2-slope power law and exponential cutoffs receding as the branching deficit shrinks](https://figures.tgtenev.com/tenev2026-soc-review/fig02-size-distribution.svg)

**Figure 2.** The near-critical size distribution of equation (5): a $\tau = 3/2$ power law (solid reference slope) with an exponential cutoff at $s_c \approx 2\langle s\rangle^2$ that recedes as the branching deficit $\varepsilon = 1 - n_b$ shrinks. The three curves are labeled by their deficit and the resulting mean size. The dashed reference line has the slope $\tau = 4/3$ of compact three-dimensional sandpile avalanches (Section 9). Over two decades the two slopes differ by less than the error bars of most data sets, which is why exponent measurements alone rarely settle a universality class.

### 4.4 Durations and the average shape

Time enters through the generation count: identify the number of generations a cascade spans with its duration $T$. At criticality the duration distribution is $P(T) \sim T^{-2}$, the mean-field lifetime exponent $y = 2$ [10, 11], and the typical duration of an avalanche of size $s$ obeys

$$T \ \sim\ \sqrt{s}\ , \quad (7)$$

which is the random-walk relation again: a walk that first returns to zero after covering total area $s$ does so in a time of order $\sqrt{s}$. Fisher [12] computes one further object that has become a standard diagnostic across the crackling-noise literature, the mean temporal profile of an avalanche of fixed size: the mean activity at time $t$ within avalanches of size $s$ is $\langle m_t \mid s\rangle \approx t\ e^{-t^2/2s}$. Activity ramps up linearly, rounds over, and dies, and the initial linear growth is independent of the avalanche's eventual size, so an avalanche that will be large is indistinguishable at birth from one that will be small. Figure 3 shows the profile for three sizes. Because the profile's shape is universal within a class while its scales are not, a collapse of measured profiles onto one curve tests the theory more stringently than an exponent fit, which is the second observable promised in Section 2.2.

![Figure 3: mean avalanche time profiles ramping linearly and dying at durations scaling as the square root of size](https://figures.tgtenev.com/tenev2026-soc-review/fig06-duration-profile.svg)

**Figure 3.** Mean-field avalanche time profiles for three sizes, from the result $\langle m_t \mid s\rangle = t\ e^{-t^2/2s}$ of Fisher [12]. Activity ramps linearly at a size-independent rate, rounds over, and dies at a duration $T \sim \sqrt{s}$, equation (7). The shape, replotted in rescaled variables, is a universality diagnostic: measured profiles that collapse onto this curve support a mean-field branching description of the underlying cascades.

## 5. Self-organization: a feedback loop around a phase transition

### 5.1 The paradox

A branching process at $n_b = 1$ is critical because someone set it there, and this is the founding puzzle of the field in its purest form: mean-field theories of sandpiles kept producing critical branching processes, but the criticality of a branching process requires tuning a parameter to a special value, which is precisely what SOC systems are defined not to need. The resolution came in two complementary forms, one explicit mechanism and one general picture, and this section presents both.

### 5.2 The self-organized branching process

Zapperi, Lauritsen, and Stanley [10] closed the loop explicitly in a model they named the self-organized branching process. Let the branching probability $p$ itself evolve under the system's grain bookkeeping. An avalanche propagates for at most $n$ generations, the model's stand-in for a finite system of $N = 2^{n+1}-1$ sites; a cascade that is still active at generation $n$ carries $\sigma_n$ grains out of the system, while a cascade that dies earlier leaves its added grain inside. Writing the grain balance per avalanche as a map for $p$ gives

$$p(t+1) \ =\ p(t) + \frac{1 - \sigma_n(p,t)}{N}\ . \quad (8)$$

When no grains exit, $p$ rises slightly, since the system retains matter; when a cascade reaches the boundary, $p$ falls in proportion to the outflow. The deterministic part of this flow has a single fixed point, and it sits exactly at $p_c = 1/2$, the critical value; linearizing shows the fixed point is attractive, and the fluctuations around it are Gaussian with variance shrinking as $1/N$ [10]. The control parameter is driven to its critical value by the dynamics, with no external tuning, and the paradox dissolves. The avalanche statistics of the self-organized state are then equation (5) evaluated at criticality: the power law $\tau = 3/2$ is realized as the stationary behavior of a feedback loop, confirmed both analytically and numerically in the same paper.

### 5.3 The absorbing-state picture

Dickman, Muñoz, Vespignani, and Zapperi [14] generalized the mechanism into a recipe, and their formulation is the modern understanding of what SOC is. The construction starts from a system with a continuous absorbing-state phase transition. An absorbing state is a configuration the dynamics can enter but never leave, and the transition of interest separates an active phase, with sustained activity, from an absorbing phase in which all activity eventually freezes. Their exemplar is a model of activated random walkers: particles on a lattice, immobile when alone at a site, active when two or more share a site, with active sites ejecting particle pairs to random neighbors. The particle density $\zeta$ is conserved by these rules, and simulations locate a continuous transition at a critical density $\zeta_c$ (approximately 0.9486 on the one-dimensional lattice), below which the system freezes and above which activity persists [14]. The model is exactly the sandpile of Manna [8] with the grain number frozen, and the authors accordingly call this closed-system counterpart a fixed-energy sandpile.

Now couple the density to the activity with two slow processes. Whenever the system is frozen, add one particle, raising $\zeta$ by an infinitesimal increment; while the system is active, allow loss at an infinitesimal rate, as boundary outflow supplies automatically. Above $\zeta_c$ there is activity, so the density falls; below $\zeta_c$ there is none, so the density rises. The only stationary point of this feedback is $\zeta_c$ itself, and the system therefore holds its own control parameter at the critical value of the underlying transition. Figure 4(a) draws the loop. This is the content of self-organized criticality in the absorbing-state picture: a conventional critical point, plus a feedback that follows from the drive and loss rules and holds the control parameter on it. Driven sandpiles and fixed-energy sandpiles are the same physics viewed through different ensembles, in close analogy with the equivalence of ensembles in equilibrium statistical mechanics.

Two qualifications from the same paper temper the recipe, and both matter later. The first concerns supervision: the rule "add a grain only when the system is quiet" presupposes an observer watching for quiescence, which is an odd ingredient for something called self-organized. The supervisor-free statement is that addition proceeds at a rate $h$, and SOC is the limit $h \to 0^+$; sandpiles are therefore scale-invariant at a point in parameter space, not generically, and the infinite separation of timescales is a form of tuning, albeit an unusually natural one that slow natural driving often realizes [13, 14]. The second concerns conservation: the recipe requires the transported quantity to be conserved by the bulk dynamics, with loss only through activity-contingent channels such as boundaries. The control parameter must be a conserved density precisely so that the feedback can move it without an external hand. What happens when conservation fails is the subject of the next two sections, and the answer reshapes the field's vocabulary.

## 6. Dissipation is relevant: self-organization to a subcritical state

### 6.1 The dissipative branching process

Lauritsen, Zapperi, and Stanley [11] asked the decisive question: what does the feedback of Section 5.2 do when a fraction of the transported quantity is destroyed in the bulk rather than at the boundary? Let each toppling dissipate its grains with probability $\epsilon$, so that the effective branching probability becomes $\tilde p = p(1-\epsilon)$, and repeat the grain bookkeeping with both boundary outflow and bulk dissipation in the balance. The critical point moves to $p_c = 1/[2(1-\epsilon)]$, since branching must now beat both stopping and dissipation. The flow equation acquires a dissipation term, and its unique attractive fixed point turns out to be

$$p^\ast \ =\ \tfrac{1}{2}\ \ \text{independent of } \epsilon\ , \qquad\text{hence}\qquad n_b \ =\ 2p^\ast(1-\epsilon)\ =\ 1 - \epsilon\ <\ 1\ . \quad (9)$$

The feedback still works: the state is still a robust attractor, reached from any initial condition with no tuning. But it no longer coincides with the critical point. The dynamics places the system a distance $\epsilon$ below criticality, and the two lines in the model's phase diagram, the fixed line $p^\ast = 1/2$ and the critical line $p_c = 1/[2(1-\epsilon)]$, intersect only at $\epsilon = 0$; Figure 4(b) draws them. In renormalization-group language, bulk dissipation is a relevant perturbation: any nonzero $\epsilon$ removes the criticality of the self-organized state [11].

The avalanche statistics of the dissipative attractor follow from Section 4 with $n_b = 1 - \epsilon$:

$$\langle s\rangle \ \approx\ \frac{1}{\epsilon}\ , \qquad s_c \ \approx\ \frac{2}{\epsilon^2}\ , \qquad T_c \ \sim\ \frac{1}{\epsilon}\ , \quad (10)$$

with the exponents $\tau = 3/2$ and $y = 2$ unchanged inside the scaling window [11]. Every clause of the Section 2.1 division is now explicit in one exact model. The exponents are universal and indifferent to $\epsilon$. The mean and the cutoff are set entirely by the dissipation rate, the cutoff standing quadratically beyond the mean exactly as equation (6) requires, and a system with sub-percent dissipation per event exhibits avalanches spanning many decades while being, strictly, subcritical.

![Figure 4: the conserving feedback loop pinning a density at its critical point, and the dissipative phase diagram whose attractor sits below the critical line](https://figures.tgtenev.com/tenev2026-soc-review/fig03-self-organization.svg)

**Figure 4.** Self-organization with and without conservation. (a) The conserving feedback loop of Section 5.3: activity above the critical density $\zeta_c$ burns the density down, quiescence below it lets the slow drive push the density up, and the only stationary point is the critical one. (b) The phase diagram of the dissipative self-organized branching process, after Lauritsen, Zapperi, and Stanley [11]: the dynamics flows to the fixed line $p^\ast = 1/2$ (dashed) for every dissipation rate $\epsilon$, while the critical line $p_c = 1/[2(1-\epsilon)]$ (solid) pulls away from it. The gap between the lines is the branching deficit $1 - n_b = \epsilon$; the feedback still self-organizes the system, but to a subcritical state with mean avalanche size $\langle s\rangle = 1/\epsilon$, a distance $\epsilon$ below criticality.

### 6.2 The unified mean-field picture

Vespignani and Zapperi [13] recast these results as ordinary nonequilibrium critical phenomena, treating the sandpile's site densities with a master-equation mean-field theory in which the driving rate $h$ and the effective dissipation $\epsilon$ appear as the control parameters and the density of active sites $\rho_a$ as the order parameter. Their stationary solution makes the structure transparent. The activity is $\rho_a = h/\epsilon$; the response of the activity to the drive defines a susceptibility, and it equals $\chi = 1/\epsilon$. Moreover the susceptibility and the mean avalanche size are the same object, because at slow driving all the activity that one added grain causes is causally connected into a single avalanche, giving the exact stationarity identity $\epsilon \langle s\rangle = 1$ [13]. In words:

$$\langle s\rangle \ =\ \frac{\text{injection per drive event}}{\text{dissipation per elementary event}}\ . \quad (11)$$

Equation (11) is conservation bookkeeping, not a mean-field approximation, and it is the finite-dissipation generalization of equation (2): with boundary-only loss, the effective dissipation per event scales as $L^{-2}$ and the mean size as $L^2$, a correspondence the same paper shows follows from conservation alone and therefore holds in every dimension. Criticality requires the double limit $h \to 0$ and $\epsilon \to 0$ with $h/\epsilon \to 0$: the drive infinitely slow, the dissipation infinitely weak, and the drive slower than the dissipation. Stated in this form, SOC is a conventional continuous phase transition whose control parameters are tuned to zero, with the single unusual feature that zero is a natural value that slow driving and near-conservation approximate without an experimenter, which is why the framework remains physically relevant despite the hidden tuning [13, 14].

## 7. Without conservation: self-organized quasi-criticality

### 7.1 Loading, and the fine-tuning theorem

Section 6 leaves a question open. Many of the systems SOC was invented for are not conserving: an earthquake dissipates elastic energy as heat and radiation, and a forest fire destroys its fuel. Such systems compensate with a loading mechanism, a background process that re-energizes the medium between avalanches, as tectonic motion reloads a fault and regrowth reloads a forest. Can loading restore the criticality that dissipation removes? Bonachela and Muñoz [16] made this question quantitative, and their analysis supplies the field's modern classification.

Add to the dissipative branching process of Section 6.1 a loading rate $\lambda$, the probability per avalanche that an inactive site is promoted to a state ready to topple. The flow equation acquires a loading term, and it does possess a fixed point at the critical value, but only if $\lambda$ equals a specific value $\lambda_c$ that depends on the dissipation and on the system size; for $\lambda > \lambda_c$ the stationary state is supercritical, and for $\lambda < \lambda_c$ subcritical [16]. Their verdict on models engineered to sit at the balance point is blunt: compensating dissipation by loading "requires an explicit parameter tuning" and "cannot be called bona fide self-organization." The size dependence makes the situation worse than ordinary tuning, since holding an ensemble of systems of different sizes at criticality would require a different loading rate for each. The conserving case needs no such balance because its feedback moves a conserved density that nothing else changes; the non-conserving case must balance two competing rates, and the balance point is a measure-zero target.

### 7.2 Hovering, and the convolution of backgrounds

The same paper's field-theoretic analysis explains what a non-conserving loaded system does instead of being critical. In the Langevin description, the conserving sandpile class couples the activity to a conserved background field; adding bulk dissipation converts the theory into the class of dynamical percolation, the theory of epidemics with immunity, in which regions already swept by an avalanche are less excitable and no sustained active phase exists at all [16]. A non-conserving system with loading then behaves as follows. Each avalanche starts from whatever background the loading has rebuilt, burns that background down as it propagates, and leaves a depleted medium behind; the loading then rebuilds it. The background state therefore executes large excursions around the critical point, a behavior Bonachela and Muñoz [16] call hovering, and the decisive result is that the excursions do not shrink as the system grows. In the conserving case the distribution of the background density narrows to a delta function at the critical value as $N \to \infty$; in the non-conserving case it stays broad at any size, with weight on both sides of the transition. Figure 5 contrasts the two.

The observed avalanche statistics of a hovering system are then a mixture. If $\mathcal{W}(E)$ is the broad stationary distribution of the background state $E$, and $P(s \mid E)$ the avalanche distribution the system would show at frozen background,

$$P_{\text{obs}}(s) \ =\ \int dE\ \ \mathcal{W}(E)\ \ P(s \mid E)\ , \quad (12)$$

a convolution of subcritical and supercritical pieces weighted by the background distribution. Such convolutions produce convincing-looking partial power laws over several decades, which the authors call pseudo-scaling, without strict criticality underneath [16]. In spatially extended systems the same logic runs locally: the medium develops patches of higher and lower excitability whose sizes are inherited from past avalanches, and the observed statistics convolve over the patch ensemble. Bonachela and Muñoz [16] name the whole phenomenon self-organized quasi-criticality, abbreviated SOqC, reserving genuine SOC for conserving dynamics.

![Figure 5: the conserving background distribution narrowing to a delta with system size versus the non-conserving background hovering with persistent width](https://figures.tgtenev.com/tenev2026-soc-review/fig04-soqc-hovering.svg)

**Figure 5.** SOC against SOqC, after Bonachela and Muñoz [16]. (a) Conserving dynamics: the distribution of the background state narrows with system size onto the critical value, and the limit of large $N$ is genuinely critical. (b) Non-conserving dynamics with loading: the background hovers, with excursions into both the propagating and absorbing phases that persist at every size. The observed avalanche statistics of the hovering state are the convolution of equation (12), the fixed-background distributions weighted over the broad background ensemble, which produces partial power laws without strict criticality.

### 7.3 The classified examples

The classification settles two long-contested model families. The earthquake model of Olami, Feder, and Christensen [18] redistributes only a fraction of a toppling site's stress to its neighbors, the fraction being the model's dissipation dial, and reloads continuously between events. Its random-neighbor version is solvable: the model is critical only at exact conservation, and its avalanche cutoff, while finite for any dissipation, grows so steeply as conservation is approached that simulations at weak dissipation display long apparent power laws [16]. The forest-fire model of Drossel and Schwabl [19] requires a double separation of timescales, tree growth much slower than burning and lightning much rarer than growth, and two decades of increasingly large simulations turned its apparent criticality into systematic violations of scaling [14, 16]. Both families are hovering systems in the sense of Section 7.2, and their partial power laws are the convolution at work. A separate construction, the extremal dynamics of Bak and Sneppen [20], reaches a critical stationary state by always advancing the globally weakest element; this achieves scale invariance at the cost of a global search, which is its own form of infinite timescale separation [14].

## 8. The exactly solvable case: the abelian sandpile

### 8.1 The abelian property

The BTW sandpile is not merely simulable; a large part of it is exactly solvable, and the solution, developed largely by Dhar and reviewed by Dhar [15], is one of the more beautiful exact structures in nonequilibrium statistical mechanics. This section presents it descriptively, at the level of statements rather than proofs.

Generalize the model slightly: heights $z_i$ on $N$ sites, an integer toppling matrix $\Delta$, a site unstable when its height exceeds the threshold set by the diagonal entry $\Delta_{ii}$, and toppling at site $i$ decreasing $z_j$ by $\Delta_{ij}$ for every $j$ (the off-diagonal entries are negative or zero, so neighbors gain). The square-lattice BTW model is the case where $\Delta$ is the lattice Laplacian. Define the operator $a_i$ as "add a grain at site $i$, then relax completely." The foundational result is the abelian property:

$$a_i\ a_j \ =\ a_j\ a_i\ , \quad (13)$$

the final stable configuration does not depend on the order in which unstable sites are toppled, nor on the order in which grains are added [15]. This is why the model is called the abelian sandpile. The property is special rather than generic; stochastic-redistribution models retain a version of it, but several well-known relatives, including the forest-fire model, do not, and with it they lose the exact solvability.

### 8.2 The steady state counted exactly

The abelian property reduces the steady state to algebra. Configurations divide into transient ones, visited at most finitely often, and recurrent ones, among which the long-run dynamics moves; on the recurrent set the operators $a_i$ are invertible and generate a finite abelian group. Three exact consequences follow [15]. The number of recurrent configurations equals $\det \Delta$. The stationary measure is uniform on the recurrent set, and it is independent of where grains are added. And membership of the recurrent set can be tested configuration by configuration with a local algorithm, the burning test: repeatedly delete (burn) any site whose height exceeds the number of its still-unburnt neighbors, and the configuration is recurrent precisely when every site burns. The unburnable residues are the forbidden subconfigurations, patterns such as two adjacent height-one sites that no history of legal topplings can produce. The burning test, run on a recurrent configuration, establishes a one-to-one correspondence between recurrent configurations and spanning trees of the lattice, which connects the sandpile to classical combinatorics and to the theory of loop-erased random walks, and makes quantities such as the exact height probabilities computable; on the infinite square lattice, the probability that a site has height one is $(2/\pi^2)(1 - 2/\pi) \approx 0.0736$ [15].

### 8.3 Directed sandpiles, and the dimensions where exponents are known

The avalanche exponents themselves are harder than the steady state, and the state of exact knowledge is worth recording dimension by dimension, because it calibrates how much confidence exponent claims deserve.

The directed sandpile of Dhar and Ramaswamy [17], in which toppled grains move only forward along a preferred direction, is solved completely in every dimension: in two dimensions the avalanche size distribution falls off with exponent $4/3$, the model's upper critical dimension is three, and mean-field exponents hold above it [15, 17]. For the undirected model the upper critical dimension is four, so the mean-field exponents of Section 4 apply for $d \geq 4$. In three dimensions the model simplifies enough for a near-exact argument, presented in Section 9. In two dimensions, the most simulated case in the field's history, the avalanche exponents remain unsettled after two decades of large-scale numerics: avalanches decompose into waves of toppling whose distribution is known exactly, but the avalanches assembled from the waves violate simple finite-size scaling, boundary-reaching and interior avalanches scale differently, and the surviving exact statements are bounds and conjectures (a conjectured size exponent of $6/5$, an exact bound of $11/8$) rather than results [15]. The most-studied model in the subject does not have established exponents in its most-studied dimension, a fact worth remembering whenever a two-decade experimental power law is assigned a class.

## 9. Geometry: what an avalanche of size $s$ looks like in space

### 9.1 The avalanche dimension

An avalanche has a size $s$, counting topplings, and a linear extent $\ell$, the diameter of the region it disturbs. The dictionary between them is a power law, $s \sim (\ell/a)^{D_{\text{av}}}$ with $a$ the lattice spacing, and the avalanche dimension $D_{\text{av}}$ is class-dependent in an instructive way. Fisher [12] computes it in a solvable model of driven elastic manifolds whose interaction kernel falls off with distance with a tunable range parameter $\alpha$ (short-range elasticity corresponds to $\alpha = 2$). The critical dimension is $d_c = 2\alpha$, and the geometry changes character there. Above $d_c$, and in mean field, an avalanche is a fractal of dimension $2\alpha$ embedded in $d$ dimensions: most sites inside its span never move, and for short-range elasticity $D_{\text{av}} = 4$. Below $d_c$ an avalanche is compact: every site in the span participates, each toppling repeatedly, roughly $s^{1-d/2\alpha}$ times [12]. The mean-field value $D_{\text{av}} = 4$ in three dimensions has a physical reading that dissolves its apparent paradox: it does not describe a four-dimensional object, but a compact region whose interior sites topple many times, so that size outruns volume through multiple topplings.

### 9.2 Three dimensions: the compact case solved

For the undirected sandpile in three dimensions, Dhar [15] shows that the geometry collapses to the simplest possible dictionary. Multiple topplings are negligible there, and avalanches are compact regions with size proportional to volume:

$$s \ \sim\ R^3\ , \quad (14)$$

with $R$ the avalanche radius. Combining this dictionary with the conservation identity $\langle s\rangle \sim L^2$ of equation (2) fixes the size exponent by pure bookkeeping: the mean of a power law with density exponent $\tau$ and cutoff $s_c \sim L^3$ grows as $L^{3(2-\tau)}$, and matching to $L^2$ forces

$$\tau_{d=3} \ =\ \tfrac{4}{3}\ . \quad (15)$$

The duration follows its own dictionary, $T \sim R^z$ with the dynamical exponent $z = 1.618 \pm 0.001$ measured through the model's equivalence to spanning-tree path lengths [15]. The pattern to hold onto spans the classes. Below the upper critical dimension, sandpile avalanches are compact with $D_{\text{av}} \approx d$ and a size exponent lighter than $3/2$, meaning a heavier tail. At and above it, or whenever the effective interaction is long-ranged, the mean-field $\tau = 3/2$ holds but the metric dictionary dissolves into multiple-toppling bookkeeping. Figure 6 draws both readings. As Figure 2 already showed, the difference between the slopes $3/2$ and $4/3$ over two decades of data is smaller than typical error bars, so the geometry, not the fitted slope, is often the more decisive class diagnostic.

![Figure 6: compact versus fractal avalanche clusters, and the size-extent dictionary lines for avalanche dimensions three and four](https://figures.tgtenev.com/tenev2026-soc-review/fig05-avalanche-geometry.svg)

**Figure 6.** The size-to-extent dictionary. (a) Below its critical dimension an avalanche is compact, with every site in the affected region participating, possibly repeatedly; above it, and at mean field, the cluster is a sparse fractal inside its span, and no metric dictionary is available. (b) The dictionary $s = (\ell/a)^{D_{\text{av}}}$ on logarithmic axes for the two readings developed in the text: compact three-dimensional avalanches with $D_{\text{av}} = 3$ and $\tau = 4/3$ (equations 14 and 15), and mean-field avalanches with $D_{\text{av}} = 4$ and $\tau = 3/2$, where the excess of size over volume is carried by multiple topplings of interior sites.

### 9.3 A geometrical aside: earthquakes at their critical dimension

One case deserves mention for how neatly it lands. A fault modeled as a planar surface has manifold dimension $d = 2$, and the elastic stress redistribution along it falls off as the inverse cube of distance, corresponding to $\alpha = 1$; the system therefore sits exactly at its critical dimension $d_c = 2\alpha = 2$, and slow tectonic drive holds it near threshold [12]. The solvable model then predicts a cumulative moment distribution falling off with exponent $1/2$, against the observed Gutenberg-Richter value near $2/3$ for regional catalogs, with individual faults often showing instead a characteristic-earthquake excess that the same model attributes to inertial stress overshoots [12]. The point of the aside is not the imperfect number but the mechanism: the marginal geometry, long-range interactions placing a two-dimensional system at its own critical dimension, is why earthquake statistics are as close to scale-free as they are.

## 10. What is robust and what is fragile

The field's own experience sorting universality claims is itself a result, and this section condenses it, because any reader intending to apply the framework needs the sorted list more than any single exponent.

The robust items, safe to build on, are the bookkeeping identities and the mean-field structure. The mean-size identity $\langle s\rangle = 1/(1-n_b)$, equation (3), and the drive-dissipation stationarity, equation (11), are exact. The exponential-with-power-law form of the size distribution, and the near-critical relation $s_c \approx 2\langle s\rangle^2$ of equation (6), hold across the class. The attractor character of the self-organized state is robust in both the conserving and the dissipative variants, and so is the dissipative scaling $\langle s\rangle \sim 1/\epsilon$ of equation (10). The mean-field exponents, $\tau = 3/2$, lifetime exponent 2, and $T \sim \sqrt{s}$, hold whenever the interaction is effectively long-ranged or the dimension is at least four.

The fragile items fall into three groups. First, exact exponent values below the upper critical dimension: the two-dimensional sandpile remains unsettled (Section 8.3), and numerical exponents in low dimensions have repeatedly shifted with better statistics. Second, universality-class assignments themselves. The BTW and Manna models were treated as one class for a decade before large-scale simulations separated them [13, 15]. More strikingly, Dhar [15] argues that an arbitrarily small probability of a grain sticking at a site without toppling, a perturbation that breaks conservation within the avalanche, drives the entire sandpile class to the exponents of directed percolation; microscopically minor-looking rule changes can move a system between classes. Third, any claim of strict criticality in a non-conserving system, which Section 7.1 showed requires a tuned loading rate. The field's recurring failure mode follows from the fragile list: a broad-but-cut-off distribution, or a convolution of non-critical pieces in the sense of equation (12), is easy to mistake for a critical power law, and a substantial fraction of the historical "SOC in X" claims dissolved under exactly that lesson [14, 16]. The durable practice that emerged is to report exponents together with the assumed class and the cutoff mechanism, and to treat the cutoff scale as a measured physical quantity in its own right rather than as a nuisance parameter.

## 11. The experimental record

### 11.1 Granular piles and the rice experiment

The namesake experiment came first and failed instructively. Laboratory sandpiles, studied within two years of the 1987 proposal, do not show scale-free avalanches: Jaeger, Liu, and Nagel [21] observed large, quasi-periodic discharge events separated by quiet intervals, the signature of a system oscillating between an angle of maximal stability and a smaller angle of repose rather than holding a critical slope. The identified culprit is grain inertia: once rolling, sand keeps rolling past the marginal state, which converts the marginal dynamics into a relaxation oscillation [14]. The repair followed the diagnosis. Frette, Christensen, Malthe-Sørenssen, Feder, Jøssang, and Meakin [22] built a pile of elongated rice grains, whose large surface-to-mass ratio suppresses inertia, fed it grain by grain at a very slow rate, and observed a convincing power-law avalanche distribution; the Oslo rice pile remains the canonical granular realization of SOC, and the model built on it (the Oslo model) is a standard member of the conserving universality class. The pair of experiments is the cleanest laboratory illustration in the field that slow driving and negligible inertia, the theory's actual preconditions, are physical conditions that a system may or may not meet, not rhetorical ones.

### 11.2 Barkhausen noise

Ferromagnetic domain walls are overdamped by eddy-current dissipation, so magnets meet the no-inertia condition automatically, and Barkhausen noise is accordingly the cleanest large-scale experimental crackling system. Measured pulse-size distributions follow power laws over more than three decades [14]. The system also displays the self-organization mechanism of Section 5 in an unusually transparent physical form. A domain wall driven by an external field through a disordered medium has a depinning transition at a critical field, an absorbing-state transition in the sense of Section 5.3; the demagnetizing field of the sample opposes the magnetization and grows with it, so as the external field rises slowly the internal field is automatically regulated back toward the depinning threshold. Urbach, Madison, and Markert [23] identified this feedback, and Zapperi, Cizeau, Durin, and Stanley [24] developed the quantitative domain-wall model; the loop is exactly the recipe of Section 5.3, with the ramp rate and the demagnetizing coupling as the two parameters whose slow limits realize criticality, and experiments can tune the coupling through the sample's aspect ratio [14, 24]. Vortex avalanches in type-II superconductors, measured by Field, Witt, Nori, and Ling [25] with pickup coils as flux enters a slowly ramped tube, form a closely related overdamped realization, with the marching density gradient of the Bean state playing the role of the pile slope.

### 11.3 Slip avalanches in deforming solids

A slowly compressed bulk metallic glass deforms in serrated bursts: the stress-strain curve descends in discrete stress drops, each corresponding to a collective slip event in the sample's shear bands. Antonaglia et al. [26] measured the stress-drop statistics in slowly compressed metallic-glass specimens and found power-law-distributed slip avalanches consistent with the mean-field exponent $\tau = 3/2$, the expected class since the elastic coupling that transmits slip through the sample is long-ranged, which places the system in the mean-field regime of Section 9.1. The same mean-field slip-avalanche framework, developed around the depinning theory of Section 5.3 and reviewed in the crackling-noise perspective of Sethna, Dahmen, and Myers [5], has been applied across sheared granular materials, crystals deforming by dislocation bursts, and laboratory earthquake analogs; acoustic-emission measurements in deforming and fracturing solids show related power laws, with the caveat that fracture proper is irreversible and lacks the stationary state the theory assumes [14].

### 11.4 Neuronal avalanches

Beggs and Plenz [27] recorded spontaneous activity in cortical slice cultures on multielectrode arrays and found that the activity arrives in avalanches: cascades of electrode activations whose size distribution follows a power law with exponent close to $3/2$, and whose measured branching parameter is close to one. The match to the critical branching process of Section 4 is striking, and it launched a large literature on criticality in neural systems. The classification of Section 7 supplies the necessary caution: neural tissue is neither conserving nor slowly driven in the sandpile sense, since synaptic transmission dissipates and external input arrives continuously, so the theoretically available state is the hovering quasi-criticality of Bonachela and Muñoz [16] rather than strict SOC, and partial power laws of the convolution type are exactly what such a system would show. Whether cortical dynamics is best described as critical, quasi-critical, or merely broad remains an active dispute, and this review takes no position beyond the classification.

## 12. The portable structure

The theory assembled above is not about sand. Its content is a set of statements about any medium with three properties: many elements held by local thresholds, a drive that loads the medium slowly compared with its internal relaxation, and a transport rule by which one element's release loads its neighbors. For any such system, the framework supplies the following, in descending order of generality.

First, bookkeeping that is exact regardless of class. The mean event size equals injection per drive event divided by dissipation per elementary event, equation (11), and equivalently pins the branching deficit through $\langle s\rangle = 1/(1-n_b)$, equation (3). These identities let a measured mean size be converted into a statement about how far below threshold the medium operates, with no model assumptions beyond the branching structure of cascades.

Second, a classification by conservation. If the transported quantity is conserved in the bulk, with loss only through activity-contingent channels, the slow-driving limit places the system at a genuine critical point, and the event statistics inherit the universal exponents of the corresponding class. If the bulk dissipates, the self-organized state sits a calculable distance below criticality, with the mean size set by the dissipation rate, equation (10), and the cutoff standing quadratically beyond the mean, equation (6). If the medium is dissipative and reloaded, the stationary state hovers, and observed statistics are convolutions over a fluctuating background, equation (12), producing partial power laws that must not be read as strict criticality.

Third, universal small-scale structure wherever a scaling window exists. Within the window, sizes follow a power law whose exponent is fixed by class rather than by microphysics, durations scale as a power of size, equation (7) in mean field, and the mean temporal profile of events collapses onto a universal shape, which furnishes a sharper diagnostic than exponent fits. The size-to-extent dictionary $s \sim (\ell/a)^{D_{\text{av}}}$ converts event statistics into spatial statistics, with $D_{\text{av}}$ known per class (Section 9).

Fourth, a discipline. The exponents are the universal content and the cutoff is the physical content; a measurement program should treat them as separate deliverables, extracting the class from the exponents and profiles, and the system's operating point from the mean size and cutoff through the exact identities. And a claim that any particular system is critical should specify which of the three conservation cases it falls under, because the framework itself supplies the reasons for skepticism about power laws read off two decades of data.

## 13. Summary

- Slowly driven threshold systems respond to smooth loading in scale-spanning bursts, a pattern called crackling noise, with power-law size distributions cut off at a largest scale, equation (1) [1, 5]. The exponent of the power law and the location of the cutoff are logically independent: the exponent is universal and computable, while the cutoff is set by whatever limits the cascades and carries no universal value.
- Near criticality, avalanches are branching processes. The mean size obeys the exact identity $\langle s\rangle = 1/(1-n_b)$, and the size distribution is a $\tau = 3/2$ power law with an exponential cutoff at $s_c \approx 2\langle s\rangle^2$. Durations scale as $T \sim \sqrt{s}$ with lifetime exponent 2, and the mean temporal profile is a universal ramp-and-die shape usable as a class diagnostic [9, 10, 12].
- Self-organization is a feedback loop around an absorbing-state phase transition: slow drive raises a conserved density when the system is frozen, activity-contingent loss lowers it when active, and the only stationary point is the critical density [10, 14]. The mechanism requires an infinite separation of timescales, so sandpiles are scale-invariant at a point in parameter space reached naturally by slow driving, not generically.
- Bulk dissipation is a relevant perturbation. A dissipative system self-organizes robustly, but to a subcritical state a distance $\epsilon$ below criticality, with $\langle s\rangle = 1/\epsilon$ and $s_c \approx 2/\epsilon^2$ set by the dissipation rate while the exponents stay mean-field [11, 13]. The mean size equals injection per drive event over dissipation per elementary event, an exact stationarity identity [13].
- Non-conserving systems with loading cannot be critical without a fine-tuned, size-dependent loading rate. They instead hover around the critical point with fluctuations that persist at every size, and their observed statistics are convolutions over the fluctuating background, a state named self-organized quasi-criticality; earthquake and forest-fire models, long claimed as SOC, belong to it [16].
- The abelian sandpile is the exactly solvable case: order-independent topplings, a recurrent set of exactly $\det \Delta$ configurations carrying the uniform stationary measure, the burning test, and the spanning-tree correspondence [15]. Exponents are exactly known for the directed model, near-exactly in three dimensions ($\tau = 4/3$, compact avalanches with $s \sim R^3$), and remain unsettled in two dimensions.
- Avalanche geometry is class-dependent. Below the critical dimension avalanches are compact with $D_{\text{av}} \approx d$ and a lighter size exponent; at mean field $\tau = 3/2$ holds but $D_{\text{av}} = 4$, with size outrunning volume through multiple topplings, and no metric dictionary [12, 15].
- The robust content is the bookkeeping identities, the cutoff relations, the attractor character of the self-organized state, and the mean-field exponents in their regime; the fragile content is low-dimensional exponent values, universality-class assignments (small rule changes, such as sticky grains, can move the class to directed percolation), and any claim of strict criticality without conservation [13, 15, 16].
- The experimental record matches the classification. Granular sand fails through inertia while the Oslo rice pile shows the predicted power laws [21, 22]. Barkhausen noise realizes the feedback loop physically through the demagnetizing field [23, 24]. Superconducting vortices, metallic-glass slip avalanches, and neuronal avalanches extend the record, the last with the quasi-criticality caveat attached [25, 26, 27].

## Acknowledgements

This review was prepared with the assistance of an AI assistant (Anthropic's Claude), used for drafting, for organizing the cited literature, and for generating the figures, under the author's direction. The author set the scope and framing, checked the claims and numerical values against the cited primary sources, and is responsible for the content, including any errors that remain.

## References

[1] P. Bak, C. Tang, and K. Wiesenfeld, "Self-organized criticality: An explanation of 1/f noise," Phys. Rev. Lett., vol. 59, pp. 381–384, 1987; and "Self-organized criticality," Phys. Rev. A, vol. 38, pp. 364–374, 1988.

[2] B. Gutenberg and C. F. Richter, "Frequency of earthquakes in California," Bull. Seismol. Soc. Am., vol. 34, pp. 185–188, 1944.

[3] F. Omori, "On the after-shocks of earthquakes," J. Coll. Sci. Imp. Univ. Tokyo, vol. 7, pp. 111–200, 1894.

[4] H. Barkhausen, "Zwei mit Hilfe der neuen Verstärker entdeckte Erscheinungen," Phys. Z., vol. 20, pp. 401–403, 1919.

[5] J. P. Sethna, K. A. Dahmen, and C. R. Myers, "Crackling noise," Nature, vol. 410, pp. 242–250, 2001.

[6] A. Clauset, C. R. Shalizi, and M. E. J. Newman, "Power-law distributions in empirical data," SIAM Rev., vol. 51, pp. 661–703, 2009.

[7] H. J. Jensen, K. Christensen, and H. C. Fogedby, "1/f noise, distribution of lifetimes, and a pile of sand," Phys. Rev. B, vol. 40, pp. 7425–7427, 1989.

[8] S. S. Manna, "Two-state model of self-organized criticality," J. Phys. A, vol. 24, pp. L363–L369, 1991.

[9] T. E. Harris, *The Theory of Branching Processes*. New York: Dover, 1989.

[10] S. Zapperi, K. B. Lauritsen, and H. E. Stanley, "Self-organized branching processes: Mean-field theory for avalanches," Phys. Rev. Lett., vol. 75, no. 22, pp. 4071–4074, 1995.

[11] K. B. Lauritsen, S. Zapperi, and H. E. Stanley, "Self-organized branching processes: Avalanche models with dissipation," Phys. Rev. E, vol. 54, pp. 2483–2488, 1996.

[12] D. S. Fisher, "Collective transport in random media: From superconductors to earthquakes," Phys. Rep., vol. 301, pp. 113–150, 1998 (also arXiv:cond-mat/9711179).

[13] A. Vespignani and S. Zapperi, "How self-organized criticality works: A unified mean-field picture," Phys. Rev. E, vol. 57, no. 6, pp. 6345–6362, 1998.

[14] R. Dickman, M. A. Muñoz, A. Vespignani, and S. Zapperi, "Paths to self-organized criticality," Braz. J. Phys., vol. 30, no. 1, pp. 27–41, 2000.

[15] D. Dhar, "Theoretical studies of self-organized criticality," Physica A, vol. 369, pp. 29–70, 2006.

[16] J. A. Bonachela and M. A. Muñoz, "Self-organization without conservation: true or just apparent scale-invariance?," J. Stat. Mech., 2009, P09009.

[17] D. Dhar and R. Ramaswamy, "Exactly solved model of self-organized critical phenomena," Phys. Rev. Lett., vol. 63, pp. 1659–1662, 1989.

[18] Z. Olami, H. J. S. Feder, and K. Christensen, "Self-organized criticality in a continuous, nonconservative cellular automaton modeling earthquakes," Phys. Rev. Lett., vol. 68, pp. 1244–1247, 1992.

[19] B. Drossel and F. Schwabl, "Self-organized critical forest-fire model," Phys. Rev. Lett., vol. 69, pp. 1629–1632, 1992.

[20] P. Bak and K. Sneppen, "Punctuated equilibrium and criticality in a simple model of evolution," Phys. Rev. Lett., vol. 71, pp. 4083–4086, 1993.

[21] H. M. Jaeger, C.-H. Liu, and S. R. Nagel, "Relaxation at the angle of repose," Phys. Rev. Lett., vol. 62, pp. 40–43, 1989.

[22] V. Frette, K. Christensen, A. Malthe-Sørenssen, J. Feder, T. Jøssang, and P. Meakin, "Avalanche dynamics in a pile of rice," Nature, vol. 379, pp. 49–52, 1996.

[23] J. S. Urbach, R. C. Madison, and J. T. Markert, "Interface depinning, self-organized criticality, and the Barkhausen effect," Phys. Rev. Lett., vol. 75, pp. 276–279, 1995.

[24] S. Zapperi, P. Cizeau, G. Durin, and H. E. Stanley, "Dynamics of a ferromagnetic domain wall: Avalanches, depinning transition, and the Barkhausen effect," Phys. Rev. B, vol. 58, pp. 6353–6366, 1998.

[25] S. Field, J. Witt, F. Nori, and X. Ling, "Superconducting vortex avalanches," Phys. Rev. Lett., vol. 74, pp. 1206–1209, 1995.

[26] J. Antonaglia, W. J. Wright, X. Gu, R. R. Byer, T. C. Hufnagel, M. LeBlanc, J. T. Uhl, and K. A. Dahmen, "Bulk metallic glasses deform via slip avalanches," Phys. Rev. Lett., vol. 112, 155501, 2014.

[27] J. M. Beggs and D. Plenz, "Neuronal avalanches in neocortical circuits," J. Neurosci., vol. 23, pp. 11167–11177, 2003.

---

*A note on the figures.* All six figures are original diagrams drawn for this review; none is reproduced from a published paper. Figures 4(b) and 5 are drawn after the corresponding figures of the cited sources but not copied from them. Where this review and a primary source disagree, the source is correct.
