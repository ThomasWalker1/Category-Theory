**Definition:**

Given categories $\mathcal{C}$ and $\mathcal{D}$ and functors $F,G:\mathcal{C}\to\mathcal{D}$. A natural transformation $\alpha$ from $F$ to $G$ consists of morphisms $\alpha_c:Fc\to Gc$ for each object in $\mathcal{C}$ such that for any object $c^{\prime}$ in $\mathcal{C}$ and $f\in\mathcal{C}(c,c^{\prime})$
$$G(f)\circ\alpha_c=\alpha_{c^{\prime}}\circ F(f)$$

We can utilize this definition to define a category of functors, where functors are the objects and natural transformations form the morphisms. 

**Definition**

If for every object $c$ in $\mathcal{C}$, $\alpha_c$ is an isomorphism then we call $\alpha:F\to G$ a natural equivalence. 

**Definition**

We call $F:\mathcal{C}\to\mathcal{D}$ and $G:\mathcal{D}\to\mathcal{C}$ equivalences of categories if 
$$FG\sim\text{Id}_{\mathcal{C}}\text{ and }GF\sim\text{Id}_{\mathcal{C}}$$