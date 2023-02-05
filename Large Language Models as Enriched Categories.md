We now embed these ideas ([[Enriched Categories]] and [[Enriched Copresheaves]]) within the context of language models. A large language model aims to construct sequences of words in grammatically correct and meaningful ways. To formalise this process we are going to define a syntax category, this models the probability distribution on text continuations. The probability distribution will relate to how likely a particular word is to follow or be contained within another set of words. Therefore, the syntax category only really captures the distributional structure of language. To encode meaning and incorporate context, we can consider the category of enriched copresheaves on this category.

## The Syntax Category
**Definition**
The syntax category $\mathcal{L}$ is a category enriched over $[0,1]$ whose objects are expressions in language and where $[0,1]$-objects are defined by
$$\mathcal{L}(x,y):=\pi(y\vert x)$$
$\pi(y\vert x)$ denotes the probability that expression $y$ extends expression $x$. If $x$ is not a subtext of $y$ then $\pi(y\vert x)=0$
One can indeed check that this is well defined as
$$\begin{gather}\pi(x\vert x)=1\geq 1\\\pi(z\vert y)\pi(y\vert x)=\pi(z\vert x)\end{gather}$$
for all text $x,y,z$

This is inherently syntatical and neglets semantics.

## The Semantics Category
The motivation behind the definition of the semantics category comes from the fact that often a set of functions from a fixed set into a different set with nice structure has it self a nice structure. 
In our case the unit interval has nice structure and so we would like to consider the set of functors into this interval, if the category of consideration is $\mathcal{C}$ we will use $\hat{\mathcal{C}}=[0,1]^{\mathcal{C}}$ to denote precisely this set of functors.
As we saw from Enriched Copresheaves, $\hat{\mathcal{C}}$ is also a category. 

**Definition**
Let $\mathcal{L}$ be the syntax category. The semantic category $\hat{\mathcal{L}}:=[0,1]^{\mathcal{L}}$ is the $[0,1]$-category of $[0,1]$-enriched presheaves on the $[0,1]$-category $\mathcal{L}$
For each object $x$ in $\mathcal{L}$, $h^x:=\mathcal{L}(x,-)$ is given by
$$c\mapsto h^x(c):=\begin{cases}\pi(c\vert x)&\text{if }x\leq c\\0&\text{otherwise}\end{cases}$$
where $x\leq c\iff$ "$x$ is contained as a subtext of $c$". 
The proposition is that $h^x$ encodes the meaning of the expression $x$.  $h^x$ has a support that only contains texts including $x$. The varying intensities of $h^x$ in relation to the texts that contain it encodes the meaning of $x$. Intuitively, if you know that a piece of text $x$, is more greatly associated to words of a particular context, demonstrated by $h^x$ having a high intensity for texts within this context, then you can extract some meaning in regarding the piece of text $x$. 

Suppose $y$ extends the text $x$ and $\mathcal{L}(x,y)=\pi(y\vert x)=a\neq 0$. 
$$x\overset{a}{\longrightarrow}y\quad h^y\overset{a}{\longrightarrow} h^x$$
$h^x$ is the meaning of $x$ which represents the varying potential context in which $x$ might appear, and $h^y$ represents the varying potential context in which $y$ appears. The context $x$ appears in extends the contexts $y$ appears in. Therefore, continuing an expression restricts the potential context in which the expression can be used.