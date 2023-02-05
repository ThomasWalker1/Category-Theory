**Definition**
A morphism $f:x\to y$ in a category is
1. A monomorphism if for any parallel morphisms $h,k:w\rightrightarrows x$, $fh=fk$ implies that $h=k$
2. An epimorphism if for any parallel morphisms $h,k:y\rightrightarrows z$, $hf=kf$ implies that $h=k$.
A monomorphism in $\mathcal{C}$ becomes an epimorphism in $\mathcal{C}^{\text{op}}$ and vice-versa

$\rightarrowtail$ denotes monomorphism and $\twoheadrightarrow$ defines an epimorphism.

Equivalently, we have that
1. $f:x\to y$ is a monomorphism in $\mathcal{C}$ if and only if for all objects $c\in\mathcal{C}$, post-composition with $f$ defines an injection.
2. $f:x\to y$ defines an epimorphism in $\mathcal{C}$ if and only if for all objects $c\in\mathcal{C}$, pre-composition with $f$ defines an injection.