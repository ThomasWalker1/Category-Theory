**Definition**
A function $F:\mathcal{C}\to\mathcal{D}$, between categories $\text{C}$ and $\mathcal{D}$, consit of the following data:
- An object $Fc\in\text{D}$ for each object $c\in\mathcal{C}$
- A morphism $Ff:Fc\to Fc^{\prime}\in\mathcal{D}$, for each $f:c\to c^{\prime}$
**Functoriality Axioms**
- For any composable pair $f,g\in\mathcal{C}$, $Fg\cdot Ff=F(g\cdot f)$
- For each object $c$ in $\mathcal{C}$, $F(1_c)=1_{F_c}$

**Definition**
A functor $F$ is called covariant if it preserves the directions of the arrows

**Definition**
A contravariant function $F$ from $\text{C}$ to $\mathcal{D}$ is a function $F:\mathcal{C}^{\text{op}}\to\mathcal{D}$

**Lemma**
Functors preserve isomorphisms.

**Example**

Suppose that $G=(X,\cdot)$ is a group, then the category $\text{B}G$ consist of the single object $X$, and morphisms given by the action of the elements on the set via the binary operation $\cdot$. The identity morphism for $X$ is simply given by the identity of the group, $e$. One can check that a group homomorphism $F:G\to H$, defines a a functor $\mathcal{F}:\text{B}G\to\text{B}H$. 

**Definition**
For any categories $\mathcal{C}$ and $\mathcal{D}$, there is a category $\mathcal{C}\times\mathcal{D}$, their product, whose
- Objects are ordered pairs $(c,d)$, $c$ an object in $\text{C}$ and $d$ an object in $\mathcal{D}$
- Morphisms are ordered pairs $(f,g):(c,d)\to(c^{\prime},d^{\prime})$ where $f:c\to c^{\prime}\in\mathcal{C}$ and $g:d\to d^{\prime}\in\mathcal{D}$
- Composition and identities are defined component wise

An isomorphism of categories is given by a pair of inverse functors $F:\mathcal{C}\to\mathcal{D}$ and $G:\mathcal{D}\to\mathcal{C}$ so that $GF$ and $FG$ are equal to the identity functors on $\text{C}$ and $\mathcal{D}$ respectively. 