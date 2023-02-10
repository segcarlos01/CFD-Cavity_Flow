# Computational Fluid Dynamics
## Master's Project Abstract
The project examined the numerical approximation of the time-dependent, incompressible, viscous Navier-Stokes equations in a 2-dimensional periodic channel. A finite volume projection method is used on a staggered, rectangular grid arrangement. The computations are GPU-accelerated by using the CuPy open-source array library in Python. However, that project stayed with the university; to be continued as a 3-D model. 

Here, I will illustrate the mathematical and compuational workflows of the project by presenteting a 2-D cavity flow driven by a moving lid. 
## Navier Stokes Equations
Navier-Stokes equations, in fluid mechanics, are partial differential equations that describes the flow of incompressible fluids. For example, it describes the relationship between flow velocity (or momentum) and pressure. We will start with the simplified 2D model. The 2D Navier Stoke Equation are:
$$\vec{W}_{t} \nu\Delta\vec{W}+\left(\vec{W}\cdot\nabla\right)\vec{W}+\nabla P =0, \quad\mathbf{x}\in\Omega,\quad t>0$$
$$div \vec{W} = 0$$
Where $\mathbf{x}=\left(x,y\right)\in\Omega\subset\mathbb{R}^{2}$ is the spatial variable; and time variable is $t$. The viscosity is  $\nu>0$. 

There is velocity vector $\vec{W}=\vec{W}\left(x,y,t\right)=\left[u\left(x,y,t\right),v\left(x,y,t\right)\right]^{T}$.

With pressure, $P=p\left(x,y,t\right)$. In addition, we have divergence-free, incompressible flow; in other words, $div\vec{W} = \frac{\partial u}{\partial x} + \frac{\partial v}{\partial y}=0$. 

