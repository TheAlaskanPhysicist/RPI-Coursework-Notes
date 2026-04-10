**Author:** Stanley Goodwin
**Date:** April 9th, 2026

---
## Question 11.1
> Two, equivalent, inertial frames $K$ and $K'$ are such that $K'$ moves in the positive $x$ direction with speed $v$ as seen from $K$. The spatial coordinate axes in $K'$ are parallel to those in $K$ and the two origins are coincident at times $t=t'=0$.
---
### Question 11.1.A
> Show that the isotropy and homogeneity of space-time and equivalence of different inertial frames (first postulate of relativity) require that the most general transformation between space-time coordinates $(t,x,y,z)$ and $(t',x',y',z')$ is a linear transformation,
> $$\begin{align}t'&=g(v^2)t-vh(v^2)x & x'&=f(v^2)x-vf(v^2)t & y'&=y & z'&=z\end{align}$$
> and its inverse
> $$\begin{align}t&=g(v^2)t'+vh(v^2)x' & x&=f(v^2)x'+vf(v^2)t' & y'&=y & z'&=z\end{align}$$
> where $f,g,h$ are functions of $v^2$, the structures of the $x'$ and $x$ equations are determined by the definition of the inertial frames in relative motion, and the signs in the inverse equation are a reflection of the reversal of roles of the two frames.

By the definition of inertial reference frames, we know that the relative motion between these two frames is dependent on velocity and position only. In order to model a change in reference frame, suppose a general transformation between their coordinates takes the form
$$\begin{align}
x_i'=\Lambda(\vec{x},t)&=A_{i}^{(0)}+A_{i\mu}^{(1)}x_\mu+A_{i\mu\nu}^{(2)}x_\mu x_\nu+A^{(3)}_{i\mu\nu\gamma}x_\mu x_\nu x_\gamma+\dots
\end{align}$$
where each index can range from 0 to 3. If we impose the condition that space-time is isotropic, then rotations of our spatial coordinate basis does not change the effect of the transformation. Therefore, without loss of generality, make a change of basis in both coordinates systems to align each axis parallel to the velocity to be $x_1=x$ and $x_1'=x'$, and the remaining perpendicular spatial bases not involve themselves in the transform.
<div style="page-break-before: always;"></div>



The effect of isotropy is that we only need to iterate over indices $0,1$, instead of all 4, resulting in
$$\begin{align}
x_i'=\Lambda(\vec{x},t)&=A_{i}^{(0)}+A_{i\mu}^{(1)}x_\mu+A_{i\mu\nu}^{(2)}x_\mu x_\nu+A^{(3)}_{i\mu\nu\gamma}x_\mu x_\nu x_\gamma+\dots
\end{align}$$
where the space is now reduced significantly. To write it more explicitly, we have:
$$\begin{align}
x_i'=\Lambda(\vec{x},t)=&A_{i}^{(0)}+A_{i0}^{(1)}t+A_{i1}^{(1)}x+A_{i00}^{(2)}t^2+(A_{i01}^{(2)}+A_{i10}^{(2)})tx+A_{i11}^{(2)}x^2+\dots
\end{align}$$
This continues for higher order products of the coordinates as the $\dots$ imply.

Now, if we impose the condition of space-time having homogeneity, then our transform between frames should not depend on a particular choice of origin we base our coordinates off of. Mathematically, we can write this condition as:
$$\begin{align}
\Lambda(\vec{x}+\delta\vec{x},t+\delta t)
=\Lambda(\vec{x},t)+\Lambda(\delta\vec{x},\delta t)
\end{align}$$
If we were to substitute our displacements $\vec{x}\to\vec{x}+\delta\vec{x}$, $t\to t+\delta t$, we would find that our general transformation becomes
$$\begin{align}
\Lambda^\text{new}(\vec{x},t)&=A_{i}^{(0)}+A_{i\mu}^{(1)}(x_\mu+\delta x_\mu)+A_{i\mu\nu}^{(2)}(x_\mu+\delta x_\mu)(x_\nu+\delta x_\nu)+\dots
\end{align}$$
If we were to expand each coefficient, all terms that contain the product of at least two coordinates have mixed couplings between $(t,\vec{x})$ and arbitrary displacement $(\delta t,\delta \vec{x})$, and therefore such entries must be $0$ in order to enforce homogeneity for *any* choice of displacement.
$$\begin{align}
x_i'^\text{new}=\Lambda^\text{new}(\vec{x},t)&=A_{i}^{(0)}+A_{i\mu}^{(1)}(x_\mu+\delta x_\mu)+0+0+\dots
\end{align}$$
This 0th term is independent of the other frame coordinate axes, and actually corresponds to an arbitrary choice in the coordinates of this frame. Therefore, our transform simplifies to:
$$\begin{align}
x_i'=\Lambda(\vec{x},t)&=A_{i\mu}^{(1)}x_\mu
\end{align}$$
From our choice of basis due to isotropy in space-time, we only need $4$ choices:
$$\begin{align}
x_0'&=A_{00}^{(1)}x_0+A_{01}^{(1)}x_1 & x_1'&=A_{10}^{(1)}x_0+A_{11}^{(1)}x_1
\end{align}$$
In terms of position $x,x'$ and $t,t'$, as well as the perpendicular directions, we have
$$\begin{align}
t'&=A_{00}^{(1)}t+A_{01}^{(1)}x & x'&=A_{10}^{(1)}t+A_{11}^{(1)}x & y'&=y & z'&=z
\end{align}$$
where the coefficients out the front absorb any extra physical constants. 
<div style="page-break-before: always;"></div>



In order to write the velocity dependence in our system, we define the origin in space-time for $K'$ to be $x'=0$ for all time $t'$. Writing in terms of the $K$ frame coordinates, we have:
$$\begin{align}
0&=A_{10}^{(1)}t+A_{11}^{(1)}x &\implies&& 
v&=-\tfrac{A_{10}^{(1)}}{A_{11}^{(1)}} &\implies&& 
A_{10}^{(1)}&=-A_{11}^{(1)}v
\end{align}$$
The matrix representation of this coordinate transform is
$$\begin{align}
\Lambda(v)&=\begin{bmatrix}A_{00}^{(1)}&-vA_{01}^{(1)}\\ -vA_{11}^{(1)}&A_{11}^{(1)}
\end{bmatrix}
\end{align}$$
I choose to rewrite $A_{01}^{(1)}\to -vA_{01}^{(1)}$ for symmetry sake, and will become apparent later. Define the following functions for the coefficients be the same as the problem suggests:
$$\begin{align}
A_{00}^{(1)}&=g(v^2) & A_{01}^{(1)}&=h(v^2) & A_{11}^{(1)}&=f(v^2)
\end{align}$$
Reapplying our transformation to the original system, we get exactly as expected:
$$\begin{align}
\Aboxed{t'&=g(v^2)t-vh(v^2)x} & \Aboxed{x'&=f(v^2)x-vf(v^2)t} & \Aboxed{y'&=y} & \Aboxed{z'&=z}
\end{align}$$
---
### Question 11.1.B
> Show that consistency of the initial transformation and its inverse require
> $$\begin{align}f(v^2)&=g(v^2) &\text{and}&& f(v^2)\cdot\left[f(v^2)-v^2h(v^2)\right]&=1\end{align}$$

This transformation in itself is independent of the coordinates it applies to, and so the inverse transformation is effectively the negative velocity transform. I will also choose to rewrite $A_{11}^{(1)}\to -vA_{11}^{(1)}$ for symmetry sake. Thus we have the transformations:
$$\begin{align}
\Lambda(v)&=\begin{bmatrix}A_{00}^{(1)}&-vA_{01}^{(1)}\\ -vA_{11}^{(1)}&A_{11}^{(1)}
\end{bmatrix} &
\Lambda(-v)&=\begin{bmatrix}A_{00}^{(1)}&vA_{01}^{(1)}\\ vA_{11}^{(1)}&A_{11}^{(1)}
\end{bmatrix}
\end{align}$$
Since we have the inverse transformation relation
$$\begin{align}
\Lambda^{-1}(v)&=\Lambda(-v) &\implies&& \Lambda^{-1}(v)\Lambda(v)&=\Lambda(-v)\Lambda^{}(v)=\mathbb{I}
\end{align}$$
We can write the product of these transforms as
$$\begin{align}
\Lambda(-v)\Lambda(v)&=\begin{bmatrix}
A_{00}^2-v^2A_{01}A_{11} & vA_{00}A_{01}-vA_{01}A_{11} \\
-vA_{11}A_{00}+vA_{11}^2 & -v^2A_{11}A_{01}+A_{11}^2
\end{bmatrix}=\mathbb{I}
\end{align}$$
Thus, we have the relationship between the coefficients:
$$\begin{align}
A_{11}&=A_{00} &  A_{00}(A_{00}-v^2A_{01})&=1
\end{align}$$
Using our substitutions from earlier, we have:
$$\begin{align}
\Aboxed{f(v^2)&=g(v^2)} & \Aboxed{f(v^2)\left[f(v^2)-v^2h(v^2)\right]&=1}
\end{align}$$
This is precisely what the question asks for.

---
### Question 11.1.C
> If a physical entity has speed $u'$ parallel to the $x'$ axis in $K'$, show that its speed $u$ parallel to the $x$ axis in $K$ is
> $$\begin{align}
u=\dfrac{u'+v}{1+vu'(h/f)}
\end{align}$$
> Using the second postulate $2'$ (universal limiting speed $C$), show that $h=f/C^2$ is required and that the Lorentz transformation of the coordinates results. The universal limiting speed $C$ is to be determined from experiment.

Start with our Lorentz transform
$$\begin{align}t'&=f(v^2)t-vh(v^2)x & x'&=f(v^2)x-vf(v^2)t\end{align}$$
and differentiate with respect to the parameters, keeping $v$ constant to find
$$\begin{align}dt'&=f(v^2)dt-vh(v^2)dx & dx'&=f(v^2)dx-vf(v^2)dt\end{align}$$
then form the ratio between the $dx'$ and $dt'$ to achieve:
$$\begin{align}
\dfrac{dx'}{dt'}&=\dfrac{f(v^2)dx-vf(v^2)dt}{f(v^2)dt-vh(v^2)dx}
\end{align}$$
We know that the $x'$ derivative is $u'$, and the $x$ derivative is $u$, and so we write this as:
$$\begin{align}
u'&=\dfrac{f(v^2)u-vf(v^2)}{f(v^2)-vh(v^2)u}
\end{align}$$
Rearrange for $u$, as well as dividing out a $f(v^2)$, and we get that:
$$\begin{align}
\Aboxed{u&=\dfrac{u'+v}{1+vu'(h/f)}}
\end{align}$$
As for the relationship between these two functions, start with its definition:
$$\begin{align}
f(v^2)\left[f(v^2)-v^2h(v^2)\right]&=1
\end{align}$$
<div style="page-break-before: always;"></div>



Let $h(v^2)=f(v^2)/C^2$, then we get that:
$$\begin{align}
f(v^2)^2\left[1-v^2/C^2\right]&=1 &\implies&& f(v^2)&=\dfrac{1}{\sqrt{1-v^2/C^2}}
\end{align}$$
This is the only solution who is symmetric in $v$ that satisfies this constraint, and thus this really is the required answer:
$$\begin{align}
\Aboxed{f(v^2)&=\dfrac{1}{\sqrt{1-v^2/C^2}}} & \Aboxed{h(v^2)&=\dfrac{1}{C^2}\dfrac{1}{\sqrt{1-v^2/C^2}}}
\end{align}$$
---
## Question 11.3
> Show, explicitly, that two successive Lorentz transformations in the same direction are equivalent to a single Lorentz transformation with velocity:
> $$\begin{align}
v=\dfrac{v_1+v_2}{1+\tfrac{v_1v_2}{c^2}}
\end{align}$$
> This is an alternative way to derive the parallel-velocity addition law.

The Lorentz Transform matrix for this system is
$$\begin{align}
\Lambda(v)&=\gamma(v)\begin{bmatrix}1&-v/c^2\\-v&1\end{bmatrix}
\end{align}$$
We can solve this with consecutive application:
$$\begin{align}
\Lambda(v_1)\Lambda(v_2)&=\gamma(v_1)\begin{bmatrix}1&-v_1/c^2\\-v_1&1\end{bmatrix}\gamma(v_2)\begin{bmatrix}1&-v_2/c^2\\-v_2&1\end{bmatrix}\\
&=\gamma(v_1)\gamma(v_2)\begin{bmatrix}1+\tfrac{v_1v_2}{c^2} & -\tfrac{v_2}{c^2}-\tfrac{v_1}{c^2}\\ -v_1-v_2 & 1+\tfrac{v_1v_2}{c^2}\end{bmatrix}\\
\Lambda(v_1)\Lambda(v_2)&=\gamma(v_1)\gamma(v_2)\begin{bmatrix}1+\tfrac{v_1v_2}{c^2} & -(v_1+v_2)/c^2\\ -(v_1+v_2) & 1+\tfrac{v_1v_2}{c^2}\end{bmatrix}
\end{align}$$
Or we can substitute in our summed velocity value above:
$$\begin{align}
\Lambda(v)&=\dfrac{\gamma\left(\dfrac{v_1+v_2}{1+\tfrac{v_1v_2}{c^2}}\right)}{1+\tfrac{v_1v_2}{c^2}}\begin{bmatrix}1+\tfrac{v_1v_2}{c^2}&-(v_1+v_2)/c^2\\-(v_1+v_2)&1+\tfrac{v_1v_2}{c^2}\end{bmatrix}
\end{align}$$
The matrices are identical, so we only need to consider the factor out the front.
<div style="page-break-before: always;"></div>



The product of the two gamma factors is:
$$\begin{align}
\dfrac{1}{\sqrt{1-\beta_1^2}}\dfrac{1}{\sqrt{1-\beta_2^2}}&=\dfrac{1}{\sqrt{1+\beta_1^2\beta_2^2-\beta_1^2-\beta_2^2}}
\end{align}$$
The combined gamma factor then is:
$$\begin{align}
\gamma(v)&=\dfrac{1}{\sqrt{1-\left(\dfrac{\beta_1+\beta_2}{1+\beta_1\beta_2}\right)^2}}\\
&=\dfrac{1+\beta_1\beta_2}{\sqrt{(1+\beta_1\beta_2)^2-\left(\beta_1+\beta_2\right)^2}}\\
&=\dfrac{1+\beta_1\beta_2}{\sqrt{\beta_1^2\beta_2^2+2\beta_1\beta_2+1-\beta_1^2-\beta_2^2-2\beta_1\beta_2}}\\
&=\dfrac{1+\beta_1\beta_2}{\sqrt{1+\beta_1^2\beta_2^2-\beta_1^2-\beta_2^2}}\\
\gamma(v)&=(1+\beta_1\beta_2)\gamma(v_1)\gamma(v_2)
\end{align}$$
When used for the Lorentz matrix of the velocity sum, the coefficient cancels the denominator, giving us exactly the right relationship:
$$\begin{align}
\Aboxed{\gamma(v)&=\left(1+\dfrac{v_1v_2}{c^2}\right)\gamma(v_1)\gamma(v_2)}
\end{align}$$
---
## Question 11.14
### Question 11.14.A
> Express the Lorentz scalars $F^{\alpha\beta}F_{\alpha\beta}$, $\mathfrak{F}^{\alpha\beta}F_{\alpha\beta}$, and $\mathfrak{F}^{\alpha\beta}\mathfrak{F}_{\alpha\beta}$, in terms of $\vec{E}$ and $\vec{B}$. Are there any other invariants quadratic in the field strengths $\vec{E}$ and $\vec{B}$?

Our matrix forms for the field tensor are [given](https://en.wikipedia.org/wiki/Electromagnetic_tensor) as
$$\begin{align}
F^{\mu\nu}&=\begin{bmatrix}
0&-E_x/c&-E_y/c&-E_z/c\\
E_x/c&0&-B_z&B_y\\
E_y/c&B_z&0&-B_x\\
E_z/c&-B_y&B_x&0
\end{bmatrix} &
F_{\mu\nu}&=\begin{bmatrix}
0&E_x/c&E_y/c&E_z/c\\
-E_x/c&0&-B_z&B_y\\
-E_y/c&B_z&0&-B_x\\
-E_z/c&-B_y&B_x&0
\end{bmatrix}
\end{align}$$
<div style="page-break-before: always;"></div>


while the tensor duals from the same table, using the notation of the question, are
$$\begin{align}
\mathfrak{F}^{\mu\nu}&=\begin{bmatrix}
0&-B_x&-B_y&-B_z\\
B_x&0&E_z/c&-E_y/c\\
B_y&-E_z/c&0&E_x/c\\
B_z&E_y/c&-E_x/c&0
\end{bmatrix} & 
\mathfrak{F}_{\mu\nu}&=\begin{bmatrix}
0&B_x&B_y&B_z\\
-B_x&0&E_z/c&-E_y/c\\
-B_y&-E_z/c&0&E_x/c\\
-B_z&E_y/c&-E_x/c&0
\end{bmatrix}
\end{align}$$
The first Lorentz scalar $F^{\alpha\beta}F_{\alpha\beta}$ is the sum of the product of individual entries
$$\begin{align}
F^{\mu\nu}F_{\mu\nu}=&\ 0\cdot0-E_x^2/c^2-E_y^2/c^2-E_z^2/c^2\\
-&\ E_x^2/c^2+0\cdot0+(-B_z)^2+B_y^2\\
-&\ E_y^2/c^2+B_z^2+0\cdot0+(-B_x)^2 \\
-&\ E_z^2/c^2+(-B_y)^2+B_x^2+0\cdot0\\
\Aboxed{F^{\mu\nu}F_{\mu\nu}=&2\left(|\vec{B}|^2-\dfrac{|\vec{E}|^2}{c^2}\right)}
\end{align}$$
Similarly, the third Lorentz scalar $\mathfrak{F}^{\alpha\beta}\mathfrak{F}_{\alpha\beta}$ is the Hodge dual, and takes the similar form
$$\begin{align}
\Aboxed{\mathfrak{F}^{\mu\nu}\mathfrak{F}_{\mu\nu}&=2\left(\dfrac{|\vec{E}|^2}{c^2}-|\vec{B}|^2\right)=-F^{\mu\nu}F_{\mu\nu}}
\end{align}$$
The second Lorentz scalar $\mathfrak{F}^{\alpha\beta}F_{\alpha\beta}$ is also the sum of the product of entries
$$\begin{align}
c\cdot\mathfrak{F}^{\mu\nu}F_{\mu\nu}=
&\ 0\cdot0-B_xE_x-B_yE_y-B_zE_z \\
-&\ B_xE_x+0\cdot0-B_zE_z-B_yE_y \\
-&\ B_yE_y-B_zE_z+0\cdot0-B_xE_x \\
-&\ B_zE_z-B_yE_y-B_xE_x+0\cdot0\\
\Aboxed{\mathfrak{F}^{\mu\nu}F_{\mu\nu}=&-4\ \vec{B}\cdot\dfrac{\vec{E}}{c}}
\end{align}$$
All together, using $c=1$ for convenience, we have:
$$\begin{align}
\Aboxed{F^{\mu\nu}F_{\mu\nu}&=-2\left(|\vec{E}|^2-|\vec{B}|^2\right)} &
\Aboxed{\mathfrak{F}^{\mu\nu}F_{\mu\nu}&=-4\ \vec{E}\cdot\vec{B}} &
\Aboxed{\mathfrak{F}^{\mu\nu}\mathfrak{F}_{\mu\nu}&=+2\left(|\vec{E}|^2-|\vec{B}|^2\right)}
\end{align}$$
As for other <u>quadratic scalar invariants</u>, there is only one other scalar:
$$\begin{align}
\Aboxed{F^{\mu\nu}\mathfrak{F}_{\mu\nu}&=-4\ \vec{E}\cdot\vec{B}}
\end{align}$$
Given the structure of Hodge duals, this is identical to taking the Hodge dual of both sides of our mixed-contraction scalar and rearranging appropriately
$$\begin{align}
(\mathfrak{F}^{\mu\nu}F_{\mu\nu})^\star&=(-4\ \vec{E}\cdot\vec{B})^\star 
&\implies&& 
-F^{\mu\nu}\mathfrak{F}_{\mu\nu}&=+4\ \vec{B}\cdot\vec{E}
&\implies&& 
\Aboxed{F^{\mu\nu}\mathfrak{F}_{\mu\nu}&=\mathfrak{F}^{\mu\nu}F_{\mu\nu}}
\end{align}$$
In a sense, this is a different scalar. It just happens to be symmetric in the Hodge dual, unlike the inner product of the dual fields together, or in another way
$$\begin{align}
\Aboxed{\mathfrak{F}^{\mu\nu}\mathfrak{F}_{\mu\nu}&=-F^{\mu\nu}F_{\mu\nu}} & 
\Aboxed{F^{\mu\nu}\mathfrak{F}_{\mu\nu}&=\mathfrak{F}^{\mu\nu}F_{\mu\nu}}
\end{align}$$
---
### Question 11.14.B
> Is it possible to have an electromagnetic field that appears as a purely electric field in one inertial frame and as a purely magnetic field in some other inertial frame? What are the criteria imposed on $\vec{E}$ and $\vec{B}$ such that there is an initial frame where there is no electric field?

Start with the Lorentz-invariant scalars from [[#Question 11.14.A (595)|part a]], specifically the first scalar
$$\begin{align}
\dfrac{1}{2}F^{\mu\nu}F_{\mu\nu}=&|\vec{B}|^2-|\vec{E}|^2
\end{align}$$
Between any two inertial frames, this scalar must remain unchanged. If in frame $1$ we have a pure electric field, and in frame $2$ we have a pure electric field, we see that
$$\begin{align}
|\vec{B}_1|^2-|\vec{E}_1|^2&=|\vec{B}_2|^2-|\vec{E}_2|^2 &\rightarrow&& |\vec{B}_2|^2&=-|\vec{E}_1|^2
\end{align}$$
Given that the square magnitude of both fields must be non-negative, then the only fields that would produce this system are
$$\begin{align}
\Aboxed{\vec{B}_2=0\text{ and }\vec{E}_1=0}
\end{align}$$
So, for two inertial frames to have pure fields opposite to each other, the field cannot exist!

---
### Question 11.14.C
> For macroscopic media, $\vec{E},\vec{B}$ form the field tensor $F^{\alpha\beta}$ and $\vec{D},\vec{H}$ the tensor $G^{\alpha\beta}$. What further invariants can be formed? What are there explicit expressions in terms of the $3$-vector fields?

As a foreword, I was not able to find the tensor for $G$ in the textbook, so I did a simple exchange between $E\leftrightarrow D$ and $B\leftrightarrow H$. If there are differing sign conventions, it will show up either as a complete negation of value, or by one of the dot products swapping signs, or both.
<div style="page-break-before: always;"></div>


Inspired by [[#Question 11.14.A (595)|part a]], we can form a few Lorentz scalars such as
$$\begin{align}
(\text{Mixed}) && 
F^{\mu\nu}G_{\mu\nu}&=G^{\mu\nu}F_{\mu\nu}=-\mathfrak{G}^{\mu\nu}\mathfrak{F}_{\mu\nu}=-\mathfrak{F}^{\mu\nu}\mathfrak{G}_{\mu\nu}\\
&&
F^{\mu\nu}\mathfrak{G}_{\mu\nu}&=\mathfrak{G}^{\mu\nu}F_{\mu\nu}=G^{\mu\nu}\mathfrak{F}_{\mu\nu}=\mathfrak{F}^{\mu\nu}G_{\mu\nu}\\
(\text{Self}) && 
G^{\mu\nu}G_{\mu\nu}&=-\mathfrak{G}^{\mu\nu}\mathfrak{G}_{\mu\nu}\\
&& 
G^{\mu\nu}\mathfrak{G}_{\mu\nu}&=\mathfrak{G}^{\mu\nu}G_{\mu\nu}
\end{align}$$
For linear media, the $G$ tensor takes the same form as $F$, just with the macroscopic fields, so
$$\begin{align}
\Aboxed{G^{\mu\nu}G_{\mu\nu}&=-2\left(|\vec{D}|^2-|\vec{H}|^2\right)} &
\Aboxed{G^{\mu\nu}\mathfrak{G}_{\mu\nu}&=-4\ \vec{D}\cdot\vec{H}} &
\Aboxed{\mathfrak{G}^{\mu\nu}\mathfrak{G}_{\mu\nu}&=+2\left(|\vec{D}|^2-|\vec{H}|^2\right)}
\end{align}$$
The first mixed Lorentz scalar $F^{\mu\nu}G_{\mu\nu}$ is the sum of the product of their elements
$$\begin{align}
F^{\mu\nu}G_{\mu\nu}=&\ 0\cdot0-E_xD_x-E_yD_y-E_zD_z\\
-&\ E_xD_x+0\cdot0+(-B_z)(-H_z)+B_yH_y\\
-&\ E_yD_y+B_zH_z+0\cdot0+(-B_x)(-H_x) \\
-&\ E_zD_z+(-B_y)(-H_y)+B_xH_x+0\cdot0\\
\Aboxed{F^{\mu\nu}G_{\mu\nu}=&-2\left(\vec{E}\cdot\vec{D}-\vec{B}\cdot\vec{H}\right)}\\
\Aboxed{\mathfrak{F}^{\mu\nu}\mathfrak{G}_{\mu\nu}=&+2\left(\vec{E}\cdot\vec{D}-\vec{B}\cdot\vec{H}\right)}
\end{align}$$
The second mixed Lorentz scalar is calculated similarly
$$\begin{align}
F^{\mu\nu}\mathfrak{G}_{\mu\nu}=
&\ 0\cdot0-E_xH_x-E_yH_y-E_zH_z \\
-&\ E_xH_x+0\cdot0-B_zD_z-B_yD_y \\
-&\ E_yH_y-B_zD_z+0\cdot0-B_xD_x \\
-&\ E_zH_z-B_yD_y-B_xD_x+0\cdot0\\
\Aboxed{F^{\mu\nu}\mathfrak{G}_{\mu\nu}=&-2\left(\vec{E}\cdot\vec{H}+\vec{B}\cdot\vec{D}\right)=G^{\mu\nu}\mathfrak{F}_{\mu\nu}}
\end{align}$$
Lastly, I had assumed this was a linear media and that the question only was talking about Lorentz Scalars, otherwise this problem would take a lot longer, and we'd need a new tensor:
$$\begin{align}
G^{\mu\nu}&=\chi^{\mu\nu\alpha\beta}F_{\alpha\beta} && \text{Pain...}
\end{align}$$
The important part is that the sign difference between the dot products is based on having 0 or 2 duals in the product and having 1 of each, and that the double dual product is the negative of the typical field tensor product.
