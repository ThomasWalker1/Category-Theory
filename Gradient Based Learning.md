The success of deep learning is in large part due to backpropagation, which utilises gradients as a way to optimize a model according to some loss function. In this section we generalise the idea of differentiation to a categorical setting.

We suppose that a machine learning model is given by a morphism $f:P\otimes A\to B$ in a monoidal category $(\mathcal{C},\otimes,I)$. Where
- $P$ represents the parameters parameters
- $A$ represents the observed data
- $B$ represents the prediction

A trained model involves finding $\theta:I\to P$ so that $f_{\theta}:A\to B$. To find $\theta$ we emply gradient based methods:
- $f:P\otimes A\to B$ is iteratively improved to minimize a loss function
- By making steps in the negative direction of the gradient (i.e. direction of descent) to reach a local minima of the loss function

## Cartesian Differential Categories
**Definition (Terminal Object):**
An object, $1$, such that for every object $x$ of a category $\mathcal{C}$ there exists a unique (up to isomorphism) a morphism $x\to 1$. This object (if it exists) is unique up to isomorphisms.

**Example**
Let $\mathcal{C}$ be the category $\text{Set}$. The objects of this category are sets and the morphisms are functions, with the usual notion of composition. Then the terminal objects are simply all the singleton sets (if they are present in the category), because for every set $x$ in $\text{Set}$ there is a unique function from that set to a singleton set, namely the function that maps all the elements of the set to the singleton element. 

**Definition:**
A Cartesian Differential Category is a monoidal category where the structure is given by the category-theoretic product. In this case the identity element is the terminal object.

**Definition:**
A category $\mathcal{C}$ that is a Cartesian monoidal category is Cartesian left-additive when it canonically bears the structure of a commutative monoide with addition, $+:A\times A\to A$ and $0_A:1\to A$

**Definition:**
A Cartesian Differential Category $\mathcal{C}$ is a Cartesian left-additive category equipped with a differential combinator $D$ which assigns each map $f:A\to B$ in $\mathcal{C}$ a map $D[f]:A\times A\to B$, with $D[f]$ satisfying the following:
- $D[f+g]=D[f]+D[g]$ and $D[0]=0$
- $(a\otimes(b+c))D[f]=(a\otimes b)D[f]+(a\otimes c)D[f]$ and $(a\otimes 0)D[f]$
- $D[1]=\pi_1, D[\pi_0]=\pi_1\pi_0$ and $D[\pi_1]=\pi_1\pi_1$
- $D[f\otimes g]=D[f]\otimes D[g]$
- $D[fg]=((\pi_0f)\otimes(D[f]))D[g]$
- $((a\otimes b)\otimes(0\otimes c))D[D[f]]=(a\otimes c)D[f]$
- $((a\otimes b)\otimes(c\otimes d))D[D[f]]=((a\otimes c)\otimes(b\otimes d))D[D[f]]$

Here we have that $f(x+x^{\prime})\approx f(x)+D[f](x,x^{\prime})$

## Reversed Derivative Categories

**Definition**
A Reverse Derivative Category $\mathcal{C}$ is a Cartesian left-additive category equipped with a reverse derivative combinator $R$ which assigns each map $f:A\to B$ in $\mathcal{C}$ a map $R[f]:A\times B\to A$.

Here we have that $f(x)+y^{\prime}\approx f(x+R[f](x,y^{\prime}))$
