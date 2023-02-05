In normal categories each object has a set of morphisms mapping it from itself to another element of the set. In an enriched category the set of morphisms acts as objects and form a category.

For objects $x,y$ in our category $\mathcal{C}$ we use $\mathcal{C}(x,y)$ to denote the set of all morphisms from $x\to y$, sometimes refered to as the hom-set.
In the setting of enriched categories, $\mathcal{C}(x,y)$ are now objects of some category $K$. If our category $K$ is monoidal the notion of composition is given by the product, 
$$\circ:\mathcal{C}(y,z)\otimes\mathcal{C}(x,y)\to\mathcal{C}(x,z)$$

A preorder is a set ($\mathcal{V}$) together with a reflexive, transitive relation ($\leq$). A $\text{Preorder}$ is a category whose:
 - Objects are elements of the set
 - A morphism exists from $a$ to $b$ if and only if $a$ is related to $b$, i.e. $a\leq b$

A commutative monoid is simply a binary operation that has an identity element, is associative and commutative.

**Definition**
A commutative monoidal preorder $(\mathcal{V}, \leq, \otimes, 1)$ is a preorder $(\mathcal{V},\leq)$ and a commutative monoid $(\mathcal{V},\otimes, 1)$ satisfying $x\otimes y\leq x^{\prime}\otimes y^{\prime}$ whenever $x\leq x^{\prime}$ and $y\leq y^{\prime}$
**Definition**
Let $(\mathcal{V},\leq,\otimes,1)$ be a commutative monoidal preorder. Then a $\mathcal{V}$-enriched category consists of a set of objects $\mathcal{C}$, and for every pair of objects $x$ and $y$, there is an element $\mathcal{C}(x,y)\in\mathcal{V}$ called a $\mathcal{V}$-hom object. We have that
$$1\leq\mathcal{C}(x,x)\\\mathcal{C}(y,x)\otimes\mathcal{C}(x,y)\leq\mathcal{C}(x,z)$$
for all objects **$x,y,z\in\mathcal{C}$**

**Example**
The interval $[0,1]$ equipped with multiplication and the usual $\leq$ relation is a commutative monoidal preorder. A $[0,1]$-enriched category consists of a set of objects $\mathcal{C}$ and a $[0,1]$-valued function $(x,y)\mapsto\mathcal{C}(x,y)$ defined for every $x,y\in\mathcal{C}$. 