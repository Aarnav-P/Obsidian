So given some object of dimension $L$ with velocity $U$ in a fluid of density $\rho$ and viscosity $\eta$ , it has a ratio of inertial to viscous forces of the Reynolds number $\textrm{Re} = LU\rho/\eta$

An easy trick is to consider $\eta^2/\rho$ which gives a force which one can use to estimate the force to tow objects with small Re.

Ex. for water $\eta^2/\rho\sim10^{-4}$ dyn or $10^{-9}$N, and $F\sim\text{Re}\dfrac{\eta^2}{\rho}$, so one estimates that with a force of 1 nN one can move with a Reynolds number of 1 in water.

Re=1 means quick movement for small things and slow movement for big things, but it also tells us that in a given fluid, if we are interested in small things, and thereby small Re, then necessarily we are interested in very small Re.

Scallop thm tells us that motion is reversible because the equation admits a linear solution at low Re. If you only have a reciprocal motion then you will simply move back and forth. In order to swim you need at least 2 d.o.f.

Why does making a loop in configuration space allow swimming, but the line (scallop motion) does not? 

Consider that there is some transformation $T$ such that $TT^{-1}=\mathbb{I}$ , but that $[T_1,T_2]\neq 0$.
Take for example driving a car where you may define $T_1$="Turn the steering wheel left" and $T_2$ = "Drive Forward".

Then it is clear that $T_1T_2T_1^{-1}T_2^{-1}$ will not return you to the original state. A low reynolds number swimmer can only swim by combining two transformations that do not commute repeatedly, which requires a (net) unidirectional loop in configuration space.

One might consider how a given rotating body can then provide propulsion at low Re. Given that everything is linear, let's just say that for some body with linear velocity $v$ and angular velocity $\Omega$ that Force (F) and Torque (N) are given by some matrix 
$\begin{align} F &= Av + B\Omega \\ N &= Cv + D\Omega \end{align}$

