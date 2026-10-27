
To develop the theory of mixed-order phase transitions, we require a good understanding of how we understand the physical system Hamiltonian, starting from the basis of the Transverse-Field Ising Model Hamiltonian. For closed-boundary TFIM, we have the Hamiltonian
$$\begin{align}
\hat{H}&=\sum_{\left<i,j\right>}j_{ij}\sigma_i^z\sigma_j^z+\sum_{i}h_{i}\sigma_i^x
\end{align}$$
where $j_{ij}$ is the $z$-$z$ dipole coupling between sites, and $h_i$ is the transverse field at each site. In order to determine a sense of strength of each of the coupling mechanisms, we can express the magnitudes under certain special conditions.

Suppose that the sign of $j_{ij}$ is the same (or zero) for all couplings. For systems of identical particles at each site, this is a valid assumption. We can then define a parameter for the total dipole coupling as the sum of the individual couplings
$$\begin{align}
|J|&=\sum_{\left<i,j\right>}|j_{ij}|=\sum_{i}|j_{i,i+1}|
\end{align}$$
In the extremes, a chosen value of $J$ can have a singular coupling interaction between two sites, while all other couplings are zero, and in the uniform limit the coupling becomes $j_{ij}=J/L$, where $L$ is the number of sites (chain length). This parameter $J$ gives an effect of how much energy is related to dipole coupling between sites, as well as the "strength" of this interaction.

Unfortunately, for transverse magnetic field, we can't necessarily impose that the magnetic field must be all the same sign or zero, but there are some alternative metrics. The magnetic field strength coupling can be bounded by each element, as well as its mean
$$\begin{align}
L\min|h_i|\le |H|&\le L\max|h_i| &\to&& \min|h_i|\le|h|&\le\max|h_i|
\end{align}$$
While the signs of the field might cause some difficulty, we will assume for the rest of the following sections that the magnetic fields will also always have identical signs.


## Elements of the Coupling Networks
Starting with the $z$-$z$ dipole coupling between sites, we can express these elements as an ordered list of "strength" elements, since these are all nearest-neighbor. As an example
$$\begin{align}
j\in\left\{j_{12},j_{23},\dots, j_{L-1,L}, j_{L,1}\right\}
\end{align}$$
With every element being of the same sign or zero. We also expect that if a site exists in a system, the will have interactions with their nearest neighbors through the whole chain, since if there exists a couplings of magnitude $0$ then it would effectively break the chain into two smaller chains. Realistically, we can impose that each element must be non-zero.
$$\begin{align}
|j_{ij}|\gt0 &&\forall j_{ij}\in j
\end{align}$$
It is expected that the dipole couplings are constant in time so long as the chain is restrained to existing at exact points in space. In the case that the particles in the chain are identical particles, the dipole coupling should be identical between each site so long as the displacement between sites is uniform. The transverse magnetic field coupling $h_i$ does not have any immediate restrictions, and can even be dynamic in time. In future sections, we will consider certain specific systems under certain symmetries.

## Identical and Uniformly Space Sites
Suppose we have a spin chain of length $L$ (having a total of $L$ sites), who are equally spaced and identical particles. Under translation invariance by our equal spacing constant, this imposes that
$$\begin{align}
j_{12}=j_{23}=\dots=j_{L-1,L}=j_{L,1}&=j
\end{align}$$
Every site interacts with their nearest neighbor identically, and contributes the same energy to the Hamiltonian, since any rearrangement of sites would produce the same physical system. Our total dipole coupling interaction is the sum of all individual contributions, with each contribution being identical leads to the per-site dipole interaction energy parameter
$$\begin{align}
J&=Nj &\implies&& j=J/N
\end{align}$$
Now we introduce the transverse magnetic field, which may or may not be uniform or dynamic in time. Since dipole interactions should be agnostic to this new field, we can use our previous statement about the uniform interactions. However, we cannot do a similar process to the magnetic field without further constraints. All together, the Hamiltonian for identical particle, uniformly spaced, spin chains are
$$\begin{align}
\hat{H}&=\frac{J}{N}\sum_{\left<i,j\right>}\sigma_i^z\sigma_j^z+\sum_{i}h_{i}\sigma_i^x
\end{align}$$
Lastly, we can non-dimensionalize the magnetic field coefficients by writing these in terms of the "total accumulated maximal field", defined as
$$\begin{align}
H&=N|\max h_i| &\implies&& \hat{H}&=\frac{J}{N}\sum_{\left<i,j\right>}\sigma_i^z\sigma_j^z+\dfrac{H}{N}\sum_{i}\frac{h_{i}}{|\max h_i|}\sigma_i^x
\end{align}$$
While not as simple in interpretation as $J$, the accumulated field $H$ gives a good understanding of the most extreme behavior that could occur. In the case of a uniform transverse field, the Hamiltonian reduces to the familiar form
$$\begin{align}
\hat{H}&=\frac{J}{N}\sum_{\left<i,j\right>}\sigma_i^z\sigma_j^z+\dfrac{H}{N}\sum_{i}\sigma_i^x
\end{align}$$
where $J$ is the total dipole-dipole interaction energy, and $H$ is the total accumulated field potential energy of the sites. This is exactly the Uniform Transverse Field Quantum Ising Model, and has been rigorously studied and is characteristics well determined.


## The Uniform Transverse Field Quantum Ising Model
The Hamiltonian for this system can be written as
$$\begin{align}
\hat{H}&=j\sum_{\left<i,j\right>}\sigma_i^z\sigma_j^z+h\sum_{i}\sigma_i^x
\end{align}$$
where $j$ is the individual dipole-dipole interaction parameter, and $h$ is the transverse magnetic field at each site. While the matrix representation expands to very large matrices pretty quickly, but it is apparent that each element is only determined from one of the interactions each, and does not overlap. For the $L=2$ case, we have the Hamiltonian:
$$\begin{align}
\hat{H}&=-j\begin{bmatrix}1&0&0&0\\0&-1&0&0\\0&0&-1&0\\0&0&0&1\end{bmatrix}-h\begin{bmatrix}0&1&1&0\\1&0&0&1\\1&0&0&1\\0&1&1&0\end{bmatrix}
\end{align}$$
Combining the matrices together, we get that
$$\begin{align}
\hat{H}&=-\begin{bmatrix}j&h&h&0\\h&-j&0&h\\h&0&-j&h\\0&h&h&j\end{bmatrix}
&\implies&&
\det\hat{H}&=j^2(j^2+4h^2)
\end{align}$$
Its eigenvalue and eigenvector are
$$\begin{align}
E_1&=-j & \vec\lambda_1&=\left[0,-1,1,0\right]^\text{T}\\
E_2&=+j & \vec\lambda_2&=\left[-1,0,0,1\right]^\text{T}\\
E_3&=-\sqrt{j^2+4h^2} & \vec\lambda_3&=\left[1,\frac{j+\sqrt{j^2+4h^2}}{2h},-\frac{j+\sqrt{j^2+4h^2}}{2h},1\right]^\text{T}\\
E_4&=+\sqrt{j^2+4h^2} & \vec\lambda_4&=\left[1,\frac{j-\sqrt{j^2+4h^2}}{2h},-\frac{j-\sqrt{j^2+4h^2}}{2h},1\right]^\text{T}
\end{align}$$
Some parameter derivatives are
$$\begin{align}
\dfrac{dE_1}{dj}&=-1 & \dfrac{dE_1}{dh}&=0\\
\dfrac{dE_2}{dj}&=+1 & \dfrac{dE_2}{dh}&=0\\
\dfrac{dE_3}{dj}&=-\dfrac{j}{\sqrt{j^2+4h^2}} & \dfrac{dE_3}{dh}&=-\dfrac{4h}{\sqrt{j^2+4h^2}}\\
\dfrac{dE_4}{dj}&=\dfrac{j}{\sqrt{j^2+4h^2}} & \dfrac{dE_4}{dh}&=\dfrac{4h}{\sqrt{j^2+4h^2}}\\
\dfrac{d|\hat{H}|}{dj}&=4j(j^2+2h^2) & \dfrac{d|\hat{H}|}{dh}&=8hj^2
\end{align}$$
For the two eigenvectors that have parameter dependence, we have that
$$\begin{align}
\dfrac{d\vec\lambda_3}{dj}&=\frac{j+\sqrt{j^2+4h^2}}{2h\sqrt{j^2+4h^2}}\left[0,1,-1,0\right]^\text{T}\\
\dfrac{d\vec\lambda_3}{d(h/j)}&=-\dfrac{1}{4j\left(h/j\right)^2\sqrt{1+4\left(h/j\right)^2}}\left[0,1,-1,0\right]^\text{T}\\
\end{align}$$










Suppose we now add a new term that is *non-local*, that we call interdependency. The new Hamiltonian takes the form
$$\begin{align}
\hat{H}&=j\sum_{\left<i,j\right>}\sigma_i^z\sigma_j^z+h\sum_{i}\sigma_i^x+f\sum_{i,j}\sigma_i^x\sigma_j^x
\end{align}$$
As a matrix, this changes the system to now be
$$\begin{align}
\hat{H}&=-\begin{bmatrix}j&h&h&f\\h&-j&f&h\\h&f&-j&h\\f&h&h&j\end{bmatrix}
&\implies&&
\det\hat{H}&=(j-f)(j+f)\left(j^2+4h^2-f^2\right)
\end{align}$$
For larger systems, we'll find that $f$ becomes smaller per site in the infinite limit, and so we're treating this as a perturbation. The new eigenvalues are
$$\begin{align}
\lambda_1&=-j-f &
\lambda_2&=+j-f &
\lambda_3&=-\sqrt{j^2+4h^2}+f &
\lambda_4&=+\sqrt{j^2+4h^2}+f
\end{align}$$
The first two eigenstates are unchanged, even if the energy has changed, but the other two eigenstates have a skew that appears in the superposition of spin states.

Some parameter derivatives are
$$\begin{align}
\dfrac{d\lambda_1}{dj}&=-1 & \dfrac{d\lambda_1}{dh}&=0 & \dfrac{d\lambda_1}{df}&=-1\\
\dfrac{d\lambda_2}{dj}&=+1 & \dfrac{d\lambda_1}{dh}&=0 & \dfrac{d\lambda_1}{df}&=-1\\
\dfrac{d\lambda_3}{dj}&=\frac{j}{\lambda_3-f} & \dfrac{d\lambda_3}{dh}&=\frac{4h}{\lambda_3-f} & \dfrac{d\lambda_3}{df}&=+1\\
\dfrac{d\lambda_4}{dj}&=\frac{j}{\lambda_4-f} & \dfrac{d\lambda_4}{dh}&=\frac{4h}{\lambda_4-f} & \dfrac{d\lambda_4}{df}&=+1
\end{align}$$
For the two varying eigenvectors, we have that


















## The Smallest (Ising) System
For $N=2$, the Hamiltonian of an Ising system is
$$\begin{align}
\hat{H}&=-J\sigma^z\otimes\sigma^z-h\sigma^x\otimes\mathbb{I}-h\mathbb{I}\otimes\sigma^x
\end{align}$$
Writing as a matrix, we have the following
$$\begin{align}
\hat{H}&=-\begin{bmatrix}J&h&h&0\\h&-J&0&h\\h&0&-J&h\\0&h&h&J\end{bmatrix}
\end{align}$$
The determinant of this Hamiltonian is
$$\begin{align}
\left|\hat{H}\right|&=4h^2J^2+J^4=J^2\left(J^2+4h^2\right)
\end{align}$$
The eigenvectors of this system are
$$\begin{align}
\lambda_1&=-J & \vec\lambda_1&=\begin{bmatrix}0\\-1\\1\\0\end{bmatrix}\\
\lambda_2&=J & \vec\lambda_2&=\begin{bmatrix}-1\\0\\0\\1\end{bmatrix}\\
\lambda_3&=-\sqrt{J^2+4h^2} & \vec\lambda_3&=\begin{bmatrix}-2hJ\\J^2+\sqrt{\left|\hat{H}\right|}\\J^2+\sqrt{\left|\hat{H}\right|}\\-2hJ\end{bmatrix}\\
\lambda_4&=\sqrt{J^2+4h^2} & \vec\lambda_4&=\begin{bmatrix}-2hJ\\J^2-\sqrt{\left|\hat{H}\right|}\\J^2-\sqrt{\left|\hat{H}\right|}\\-2hJ\end{bmatrix}\\
\end{align}$$
## The Smallest (QH) System
If we include an interdependency term, we get the Hamiltonian
$$\begin{align}
\hat{H}_\text{QH}&=-J\sigma^z\otimes\sigma^z-h\sigma^x\otimes\mathbb{I}-h\mathbb{I}\otimes\sigma^x-f\sigma^x\otimes\sigma^x
\end{align}$$
As a matrix, this adds terms on the off diagonal
$$\begin{align}
\hat{H}_\text{QH}&=-\begin{bmatrix}J&h&h&f\\h&-J&f&h\\h&f&-J&h\\f&h&h&J\end{bmatrix}
\end{align}$$
The determinant of this Hamiltonian is
$$\begin{align}
\left|\hat{H}\right|_\text{QH}&=f^4-4f^2h^2-2f^2J^2+4h^2J^2+J^4\\
&=\left(J^2-f^2\right)\left(4h^2+J^2-f^2\right)\\
&=\left(f-J\right)\left(f+J\right)\left(f-\sqrt{J^2+4h^2}\right)\left(f+\sqrt{J^2+4h^2}\right)
\end{align}$$
The zeros of this Hamiltonian are
$$\begin{align}
f&=\pm J & f&=\pm\sqrt{J^2+4h^2}
\end{align}$$
The eigenvectors of this system are
