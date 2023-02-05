For objects $A,B,C$ in a category $\mathcal{C}$, we say that $C$ is the product of $A$ and $B$ if there are mpas 
$$\pi_1:C\to A\text{ and }\pi_2:C\to B\text{ (the projections)}$$
such that given any other pair of maps
$$f_1:X\to A\text{ and }f_2:X\to B$$
there is a unique map 
$$f:X\to C$$
such that
$$\pi_1\circ f = f_1\text{ and }\pi_2\circ f=f_2$$
That is we can first map $X\to C$, take the projections in $C$ and still retrieve the projections of $A,B$ in $X$. 

We say that $C$ has the universal property there exists morphisms $\pi_1:C\to A$ and $\pi_2:C\to B$

Of courses these ideas can be extrapolated to products of an arbitrary collection of objects.

**Example**
In the category $\text{Set}$ the product of two objects $X_1$ and $X_2$ is the usual cartesian product of sets
$$X_1\times X_2=\{(x_1,x_2)\vert x_1\in X_1, x_2\in X_2\}$$
where
$$\pi_1:X_1\times X_2\to X_i\\ (x_1,x_2)\mapsto x_i$$

