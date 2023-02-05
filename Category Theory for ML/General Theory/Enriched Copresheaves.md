A presheaf is a functor $F:\mathcal{C}^{\text{op}}\to\text{Set}$. The dual of this notion is the copresheaf, that is a functor $G:\mathcal{C}\to\text{Set}$. Where throughout $\text{Set}$ denotes the category of sets.

**Definition**
Let $\mathcal{C}$ and $\mathcal{D}$ be categories enriched over a commutative monoidal preorder $(\mathcal{V},\otimes,\leq, 1)$. An enriched functor $\mathcal{C}\to\mathcal{D}$ is a function $f:\mathcal{C}\to\mathcal{D}$ satisfying
$$\mathcal{C}(x,y)\leq\mathcal{D}(fx,fy)\quad\forall\;x,y\in\mathcal{C}$$

**Definition**
Let $\mathcal{C}$ be a category enriched over a closed commutative monoidal preorder $\mathcal{V}$. An enriched copresheaf is a function $f:\mathcal{C}\to\mathcal{V}$ satisfying $\mathcal{C}(x,y)\leq\mathcal{V}(fx,fy)$ for all objects $x,y\in\mathcal{C}$.

**Lemma**
If $\mathcal{C}$ is a category enriched over $[0,1]$ then the category $\hat{\mathcal{C}}:=[0,1]^{\mathcal{C}}$ of copresheaves (where $\mathcal{V}$ is replaced by $[0,1]$ in the above definition) is also enriched over $[0,1]$. The $[0,1]$-object between any pair of copresheaves $f,g:\mathcal{C}\to[0,1]$ is given by
$$\hat{\mathcal{C}}(f,g)=\inf_{c\in\mathcal{C}}\left\{1, \frac{gc}{fc}\right\}$$
This says that enriched copresheaves form an enriched category.

**Lemma**
Let $\mathcal{C}$ be a $[0,1]$-category. For every object $x$, the function
$$h^x:=\mathcal{C}(x,-)$$
is a $[0,1]$-functor
This says that objects define a representable copresheaf.

**Definition**
For any object $x$ in a $[0,1]$-category $\mathcal{C}$, we call the functor $h^x:=\mathcal{C}(x,-)$ the copresheaf represented by $x$. We say a copresheaf $f:\mathcal{C}\to[0,1]$ is representable if $f=h^x$ for some $x\in\mathcal{C}$. 

**Theorem (The Enriched Yoneda Lemma)**
For any object $x$ in a $[0,1]$ category $\mathcal{C}$ and any $[0,1]$-copresheaf $f:\mathcal{C}\to[0,1]$, we have $\hat{\mathcal{C}}(h^x, f)=f(x)$
**Corrolary**
$\mathcal{C}(y,x)=\hat{\mathcal{C}}(h^x,h^y)$ for all objects $x,y$ in $[0,1]$-category $\mathcal{C}$
Therefore, $x\mapsto h^x$ embedds (the opposite of) a $[0,1]$-category within its category of copresheaves.
That is, for any $[0,1]$-category $\mathcal{C}$, the assignment $x\mapsto h^x$ defines an enriched functor $\mathcal{C}^{\text{op}}\to\hat{\mathcal{C}}$, embedding $\mathcal{C}^{\text{op}}$ as an enriched subcategory of $\hat{\mathcal{C}}$.
