A monoidal category is a category that has a notion of "product", denoted $\otimes$. 

**Definition:**
A monoidal category $\mathcal{C}$ is a category equipped with
- A function 
$$\otimes:\mathcal{C}\times\mathcal{C}\to\mathcal{C}$$
- A unit object, $I$
- A natural isomorphism $a:(\cdot\otimes\cdot)\otimes\cdot\to\cdot\otimes(\cdot\otimes\cdot)$ which formalizes the notion of associativity
- A natural isomorphism $\lambda:(I\otimes\cdot)\to\cdot$
- A natural isomorphism $\rho:\cdot\otimes I\to\cdot$

If each of the above isomorphisms are the identity morphisms then the monoidal category is called strict.
