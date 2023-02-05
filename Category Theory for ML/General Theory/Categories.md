**Definition (Category)**:
- The data of a category includes:
	- a collection of objects $(X,Y,Z,\dots)$
  - a collection of morphisms $(f,g,h,\dots)$
- Morphisms have domains and codomains consisting of objects, $f:X\to Y$
- Each object has an identity morphism, $1_X:X\to X$
- There is a notion of composition of morphisms, $f:X\to Y,g:Y\to Z\longrightarrow gf:X\to Z$

The axioms underpinning a category are the following:
1. For $f: X\to Y$, $1_Yf=f=f1_X$
2. For $f,g,h$ morphism, $h(gf)=(hg)f$

There are some issues we need to consider regarding the semantics used to describe a category. One could say that the category consists of a *set* of objects, however, as the objects themselves be sets we introduce Russell-like paradoxes. Therefore, for refer to the objects of a category as a *collection*.

**Definition**
An isomorphism in a category is a morphism $f:X\to Y$ for which there is a $g:Y\to X$ such that $gf=1_X$ and $fg=1_Y$. In this case $X$ and $Y$ are said to be isomorphic, written $X\cong Y$.

**Definition**
An endomorphism is a morphism whose codomain equals its domain

**Definition**
An automorphism is an endomorphism that is an isomorphism

**Definition**
A subcategory $\text{D}$ of a category $\text{C}$ is the restriction of $\text{C}$ to a subcollection of objects and morphisms, with all the necessary axioms still holding. 

**Definition**
A groupoid is a category in which every morphism is an isomorphism

**Examples (Categories):**
1. The category $\text{Set}$ is a category whose objects are sets and whose morphisms are functions between those sets, with compositionality being the usual composition of functions.
2. The category $\text{Vect}_k$ is the category of vector spaces over a field $k$, with the morphisms being linear transformations.