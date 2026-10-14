==🟡**Report from Éloi:**==
-  Hexbugs in a confined flexible band can explore a 2D space.
-  When constrained from one or more ends, can exhibit **oscillatory behaviour** [1]
	- so-called **self-oscillation**
Occurs at given σ, *elastoactive parameter*

Model chain of hexbugs as series of pendulums connected by spiral springs with torsional stiffness. ∴ Restorative force applies torque [1]

$\sigma = \frac{F_Al}{C}$
Critical parameter for σ is $\sigma_C=0.16\pm0.005$ to observer self-oscillations

Oscillation can be driven by fixing both ends at some $L$ s.t. $L<l_{chain}$ given that $\sigma>\sigma_C$. 
Make $L\equiv L(T)$ by connecting the chain with LCE's.

==🔴**Buckling**==

Elastic beams under compressive axial load will buckle at $N_{Euler}=\dfrac{\pi^2EI}{L^2}$ , $E$ is YM and $I$ is area moment of inertia. [2]
\> Consider reading the euler (1744) or the Lagrange (1770) papers to get a full understanding. <

LCEs are polymer networks where the network consists of mesogens or mesogens are chemically-bonded to the network. 

→ Deform reversibly under ext. stimulus
i.e. at some T, nematic-isotropic transition causes formerly ordered orientation of polymer network to cluster which causes contraction along director axis.

Force of contraction >> F_weight

Dependent on:
	Elasticity is a function of cross-linking density (read: bond density)
	The bond itself
	mesogen itself

==🟢**Synthesis**==
See [1], Section 2.3

LCE stretched to provide temporary alignment and then UV induces polymerisation to fix orientation.
\> Deformation via heat will now restore to the polymerised state.

==🔵Random Walk==
Some gaussian perturbation to angle, from some $\mathcal{N}(0,\sigma^2)$. Given $n$ steps, we have some total angular displacement $\cal{N}(\mu,n\sigma^2)$ 
- Then one defines $D_a\equiv \dfrac{\sigma^2}{2\Delta l}$ , the diffusion coefficient, where $\Delta l = v\cdot \Delta t$, yielding 
		-  $\theta(t_0 + n\Delta t) - \theta(t_0) \sim \mathcal{N}(\mu,2D_aL)$   
- Then we can define $\vec{X_n}=(x_n,y_n,\theta_n)$, and your persistence length $\langle\cos\theta\rangle$ is                               $\langle\cos(\theta(t_0 + n\Delta t) - \theta(t_0))\rangle$ which is $\Re(\langle e^{i(\theta(t_0 + n\Delta t) - \theta(t_0))}\rangle)$ 
- $\langle e^{ikX}\rangle = e^{ik\mu -k^2\sigma^2/2}$ for $X\sim \mathcal{N}(\mu,\sigma^2)$
		$\therefore$ $\langle\cos\theta\rangle = \Re(e^{-2D_aL/2}) = \Re(e^{-D_aL})$
Hence $D_a$ is the persistence length

Then by camera tracking the hexbug one can *experimentally determine* $\sigma$.

Turns out that actually $\mu$ was non-zero and persistence length was about $l_p=2.3m$ for a hexbot which effectively means that for a boundary of $d<l_p$ we expect that there is not enough space to achieve random diffusive movement.

\> Makes sense then why the hexbugs would collide with the boundary, and especially if μ < 0 then they will stay stuck on average for counter-clockwise rotation and peel away for clockwise.

**==🟣Active Chain**==

Printing with TPU  (Thermoplastic Urethane) because PLA is too rigid and snaps instead of buckling

Joint width  = 3mm





References 

[1] E. Zheng, M. Brandenbourger, L. Robinet, P. Schall, E. Lerner, and C. Coulais, “Self-Oscillation and Synchronization Transitions in Elastoactive Structures,” _Phys. Rev. Lett._, vol. 130, no. 17, p. 178202, Apr. 2023, doi: [10.1103/PhysRevLett.130.178202](https://doi.org/10.1103/PhysRevLett.130.178202).
[2] A. Goriely, R. Vandiver, and M. Destrade, Nonlinear Euler buckling, Proc. R. Soc. A. **464**, 3003 (2008).

