











## Operators
We can have any product that is in units of $\hbar$ as an operator on a wavefunction:
$$\begin{align}
U(G;a)&=e^{-iGa/\hbar} & &\text{(General Operator)}\\
U(\hat{p}\cdot\hat{r};r)&=e^{-i(\hat{p}\cdot\hat{r})r/\hbar} & &\text{(Spatial Translation)}\\
U(\hat{J}\cdot\hat{n};\phi)&=e^{-i(\hat{J}\cdot\hat{n})\phi/\hbar} & &\text{(Rotation Translation)}\\
U(\hat{H};t)&=e^{-i\hat{H}t/\hbar} & &\text{(Time Translation)}\\
\end{align}$$
Where $G$ is the generator of the translation of the conjugate variable.
## Chapter 3 - Angular Momentum
Angular Momentum Commutator:
$$\begin{align}
[J_i,J_j]&=i\hbar\epsilon_{ijk} J_k
\end{align}$$
Spin-$1/2$ operators:
$$\begin{align}
S_x&=\dfrac{\hbar}{2}\left(\ket{\chi_{-}^Z}\bra{\chi_{+}^Z}+\ket{\chi_{+}^Z}\bra{\chi_{-}^Z}\right)\\
S_y&=\dfrac{\hbar}{2}i\left(\ket{\chi_{-}^Z}\bra{\chi_{+}^Z}-\ket{\chi_{+}^Z}\bra{\chi_{-}^Z}\right)\\
S_z&=\dfrac{\hbar}{2}\left(\ket{\chi_{+}^Z}\bra{\chi_{+}^Z}-\ket{\chi_{-}^Z}\bra{\chi_{-}^Z}\right)
\end{align}$$
With expected values:
$$\begin{align}
\braket{S_x}&\rightarrow\braket{S_x}\cos\phi-\braket{S_y}\sin\phi\\
\braket{S_y}&\rightarrow\braket{S_y}\cos\phi+\braket{S_x}\sin\phi\\
\braket{S_z}&\rightarrow\braket{S_z}
\end{align}$$









## Chapter 3 - Angular Momentum
$$\begin{align}
\vec{J}^2&=J_xJ_x+J_yJ_y+J_zJ_z\\
[\vec{J}^2,J_k]&=0\\
\vec{J}^2\ket{j,m}&=j(j+1)\hbar^2\\
J_z\ket{j,m}&=m\hbar
\end{align}$$
Ladder operators:
$$\begin{align}
J_\pm&\equiv J_x\pm iJ_y\\
[J_+,J_-]&=2\hbar J_z\\
[J_z,J_\pm]&=\pm\hbar J_\pm
\end{align}$$





### Tensors
Suppose we have a 2-tensor of the form:
$$\begin{align}
T_{ij}&=U_iV_j
\end{align}$$
We can decompose this into 3 different types of tensors:
$$\begin{align}
T_{ij}&=\dfrac{\vec U\cdot\vec V}{3}\delta_{ij}+\dfrac{(U_iV_j-U_jV_i)}{2}+\left(\dfrac{U_iV_j+U_jV_i}{2}-\dfrac{\vec U\cdot\vec V}{3}\delta_{ij}\right)
\end{align}$$
Upon rotating this tensor $T_{ij}$, these 3 parts transform differently:
 - The first part is a scalar product is invariant under rotation
 - The second part is an antisymmetric tensor
 - The third part is a symmetric traceless tensor


### Proof of Usage
A Cartesian vector transforms as:
$$\begin{align}
V_{i}&=\sum_{i'} R_{ii'}V_{i'}\\
\end{align}$$
Define the following relations:
$$\begin{align}
\begin{bmatrix}V_{+1}^{(1)}\\V_{0}^{(1)}\\V_{-1}^{(1)}\end{bmatrix}&=\begin{bmatrix}-\tfrac{1}{\sqrt2}&-\tfrac{i}{\sqrt2}&0\\
0&0&1\\
+\tfrac{1}{\sqrt2}&-\tfrac{i}{\sqrt2}&0
\end{bmatrix}\begin{bmatrix}V_x\\V_y\\V_z\end{bmatrix}
\end{align}$$
Inverting the transform, we get:
$$\begin{align}
\begin{bmatrix}V_x\\V_y\\V_z\end{bmatrix}&=\begin{bmatrix}-\tfrac{1}{\sqrt2}&0&+\tfrac{1}{\sqrt2}\\
\tfrac{i}{\sqrt2}&0&\tfrac{i}{\sqrt2}\\
0&1&0
\end{bmatrix}\begin{bmatrix}V_{+1}^{(1)}\\V_{0}^{(1)}\\V_{-1}^{(1)}\end{bmatrix}
\end{align}$$








A rank-2 tensor transforms as:
$$\begin{align}
T_{ij}&=\sum_{i',j'} R_{ii'}R_{jj'}T_{i'j'}\\
\end{align}$$
Each part can be seen:

$k=1$:
$$\begin{align}
T^{(0)}_0&=\dfrac{1}{\sqrt3}\delta_{ij}T_{ij}
\end{align}$$
$k=2$:
$$\begin{align}
A_{ij}&=\dfrac{1}{2}\left(T_{ij}-T_{ji}\right)\\
T^{(1)}_k&=\dfrac{1}{\sqrt2}\epsilon_{ijk}T_{ij}\\
\end{align}$$









We can decompose $T_{i'j'}$ into 3 parts:
$$\begin{align}
T_{i'j'}&=\dfrac{\vec U\cdot\vec V}{3}\delta_{i'j'}+\dfrac{U_{i'}V_{j'}-U_{j'}V_{i'}}{2}+\left(\dfrac{U_{i'}V_{j'}+U_{j'}V_{i'}}{2}-\dfrac{\vec U\cdot\vec V}{3}\delta_{i'j'}\right)\\
\end{align}$$



