# Math 331 — PSET 1 & 2 Solution Guide

Rudin Chapter 1, with Chapter 2 used only for countability.

## PSET 1

Use the decimal ending in zeros when there are two expansions, and use $+0$. Before the field axioms are proved, $-x$ means reversing the decimal's sign. Calculations with terminating decimals are rational calculations.

> The PDF has a typo: $x\le y$ means $x<y$ or $x=y$, equivalently, not $y<x$.

### 1. Show that $\mathbb{R}$ is ordered

**First, an inequality between truncations persists.** Suppose $t_{k}(x)<t_{k}(y)$ and $j>k$. The two $k$-digit truncations differ by at least $10^{-k}$.

For nonnegative $x,y$,

$$  
t_{j}(x)<t_{k}(x)+10^{-k}\le t_{k}(y)\le t_{j}(y).  
$$

For nonpositive $x,y$,

$$  
t_{j}(x)\le t_{k}(x)\le t_{k}(y)-10^{-k}<t_{j}(y).  
$$

For $x\le0\le y$,

$$  
t_{j}(x)\le t_{k}(x)<t_{k}(y)\le t_{j}(y).  
$$

The remaining sign case cannot have $t_{k}(x)<t_{k}(y)$.

**Trichotomy.** If $x\ne y$, their chosen decimal expansions differ, so some truncations differ. Thus $x<y$ or $y<x$. Both cannot hold: at a common later place, the first part would give opposite rational inequalities. Also $x<x$ is impossible.

**Transitivity.** If $x<y$ and $y<z$, choose a place $N$ at least as large as the two places witnessing these inequalities. Then

$$  
t_{N}(x)<t_{N}(y)<t_{N}(z),  
$$

so $x<z$.

It also follows that $x\le y$ implies $t_{k}(x)\le t_{k}(y)$ for every $k$.

### 2. If $x>0$, find $0<y<x$

Choose $k$ with $t_{k}(x)>0$. Since this truncation is a positive multiple of $10^{-k}$, it is at least $10^{-k}$.

Take $y=10^{-(k+1)}$. Then

$$  
0<t_{k+1}(y)=10^{-(k+1)}<10^{-k}\le t_{k+1}(x),  
$$

so $0<y<x$.

### 3. Well-ordering of $\mathbb{N}$

Suppose a nonempty $A\subseteq\mathbb{N}$ has no least element. We prove by strong induction that no natural number belongs to $A$.

- $1\notin A$, since otherwise it would be least.
    
- If $1,\ldots,n-1\notin A$, then $n\in A$ would make $n$ least. Thus $n\notin A$.
    

Hence $A=\varnothing$, a contradiction.

### Decimal facts needed below

The digits give

$$  
t_{k}(x)-10^{-k}<x<t_{k}(x)+10^{-k}.  
$$

**There is a terminating decimal between any two distinct reals.** For $0\le x<y$, choose $k$ with $t_{k}(x)<t_{k}(y)$. The chosen expansion of $x$ does not end in nines, so a later digit different from $9$ gives a place $j>k$ with

$$  
x<t_{j}(x)+10^{-j}<t_{k}(y)\le y.  
$$

Reverse signs if both numbers are nonpositive. If $x<0<y$, use $0$.

**Two numbers in arbitrarily short common rational intervals must be equal.** Otherwise, apply the preceding fact twice to put two terminating decimals strictly between them. Their positive rational difference is a lower bound for the length of every common interval.

In particular, if both numbers lie in a common interval of length at most $C10^{-k}$ for every $k$, with fixed rational $C>0$, they are equal. Such intervals eventually exclude any other fixed number.

### 4. Least-upper-bound property

Let $E\ne\varnothing$ have upper bound $u$, and fix $x_{0}\in E$.

**Choose the digits.** Let $s_{k}$ be the largest value of $t_{k}(x)$ for $x\in E$. This maximum exists: between $t_{k}(x_{0})$ and $t_{k}(u)$ there are only finitely many multiples of $10^{-k}$, and all other truncations are smaller.

The first $k$ digits of $s_{k+1}$ equal $s_{k}$. They cannot exceed $s_{k}$. They cannot be smaller either: an element of $E$ attaining $s_{k}$ would then have a larger $(k+1)$-digit truncation than $s_{k+1}$.

These consistent digits define a decimal $\alpha$. If they end in nines, carry to its terminating expansion. In either case,

$$  
s_{k}-10^{-k}\le\alpha\le s_{k}+10^{-k}.  
$$

For example, $E=\lbrace 0.9,0.99,\ldots\rbrace$ gives $\alpha=1$. Thus we cannot always claim $t_{k}(\alpha)=s_{k}$.

**Upper bound.** Every $x\in E$ satisfies $x\le s_{k}+10^{-k}$ for every $k$. If $x>\alpha$, then $x$ and $\alpha$ both lie in

$$  
[s_{k}-10^{-k},\ s_{k}+10^{-k}]  
$$

for every $k$. This forces $x=\alpha$, a contradiction.

**Least upper bound.** Suppose $\beta<\alpha$ were also an upper bound. For each $k$, choose $x\in E$ with $t_{k}(x)=s_{k}$. Then

$$  
s_{k}-10^{-k}\le x\le\beta<\alpha\le s_{k}+10^{-k}.  
$$

The same interval argument forces $\beta=\alpha$, a contradiction. Therefore $\alpha=\sup E$.

### 5. Approximation of $x+y$ and $xy$

If every $k$ satisfied

$$  
t_{k}(x)+t_{k}(y)\le x+y-\epsilon,  
$$

then $x+y-\epsilon$ would be an upper bound smaller than the defining supremum $x+y$. Therefore some $k$ satisfies

$$  
t_{k}(x)+t_{k}(y)>x+y-\epsilon.  
$$

The same argument applied to $\lbrace t_{k}(x)t_{k}(y)\in\mathbb{N}\rbrace$ gives the product inequality.

The subtraction and strict inequality used here are justified in #7. The underlying fact is simply that a number below a supremum is not an upper bound.

### 6. The addition definitions agree for $x,y>0$

Let

$$  
A=\sup_{k}\bigl(t_{k}(x)+t_{k}(y)\bigr),  
\qquad  
B=\sup_{k}\bigl(t_{k}(x)+t_{k}(y)-2\cdot10^{-k}\bigr).  
$$

Every term defining $B$ is at most the corresponding term defining $A$, so $B\le A$.

For $j\ge k$, each positive truncation gains less than $10^{-k}$. Earlier truncations are smaller. Consequently,

$$  
t_{k}(x)+t_{k}(y)-2\cdot10^{-k}  
\le B\le A\le  
t_{k}(x)+t_{k}(y)+2\cdot10^{-k}.  
$$

Both numbers lie in an interval of length $4\cdot10^{-k}$ for every $k$. Hence $A=B$.

### Bounds used in 7–9

The defining sets for sums and positive products are nonempty and bounded by integers, so their suprema exist. Define products involving zero to be zero; use the given sign rules for negative factors.

If terminating decimals satisfy

$$  
a\le x\le b,\qquad c\le y\le d,  
$$

then

$$  
a+c\le x+y\le b+d.  
$$

If $a,c\ge0$, we also have

$$  
ac\le xy\le bd.  
$$

For arbitrary signs, the product lies between the smallest and largest of $ac,ad,bc,bd$.

**Why these bounds hold.** The terms defining a sum are nondecreasing. In passing from $k$ to $k+1$, each truncation can decrease by at most $9\cdot10^{-(k+1)}$, while the correction $-2\cdot10^{-k}$ increases by $18\cdot10^{-(k+1)}$.

For large $k$, all four terminating endpoints truncate exactly. Thus

$$  
a+c-2\cdot10^{-k}  
\le t_{k}(x)+t_{k}(y)-2\cdot10^{-k}  
\le b+d-2\cdot10^{-k}.  
$$

Taking the supremum gives the upper bound $b+d$. If that supremum were below $a+c$, sufficiently large $k$ would make the left-hand bound exceed it, a contradiction.

For nonnegative products, the defining terms are nondecreasing and eventually lie between $ac$ and $bd$. Reversing signs gives the other product cases; for an interval crossing zero, apply the bounds to the side containing the factor.

Taking $a=b$ and $c=d$ shows that the new operations agree with rational arithmetic on terminating decimals.

### 7. Addition axioms

**Closure.** The defining supremum exists, as shown above.

**Commutativity.** Swapping $x,y$ leaves every term defining the sum unchanged.

**Associativity.** Apply the addition bounds twice. Both $(x+y)+z$ and $x+(y+z)$ lie between the two rational bounds

$$  
t_{k}(x)+t_{k}(y)+t_{k}(z)\pm3\cdot10^{-k}.  
$$

Their common interval has length $6\cdot10^{-k}$ for every $k$, so they are equal.

**Identity.** Both $x+0$ and $x$ lie between $t_{k}(x)-10^{-k}$ and $t_{k}(x)+10^{-k}$ for every $k$. Hence $x+0=x$.

**Inverse.** Sign reversal gives $t_{k}(-x)=-t_{k}(x)$. The addition bounds therefore give

$$  
-2\cdot10^{-k}\le x+(-x)\le2\cdot10^{-k}  
$$

for every $k$. Hence $x+(-x)=0$.

**Adding preserves order.** If $x<y$, choose terminating decimals $x<p<q<y$. For $k$ with $2\cdot10^{-k}<q-p$,

$$  
x+z  
\le p+t_{k}(z)+10^{-k}  
<q+t_{k}(z)-10^{-k}  
\le y+z.  
$$

In particular, $\epsilon>0$ implies $x-\epsilon<x$, as used in #5.

### 8. Multiplication axioms

**Closure and commutativity.** The defining supremum exists. Swapping the factors preserves the rational products and their signs.

**Associativity.** Apply the product bounds twice. Both $(xy)z$ and $x(yz)$ lie between the smallest and largest of the eight rational products

$$  
\bigl(t_{k}(x)\pm10^{-k}\bigr)  
\bigl(t_{k}(y)\pm10^{-k}\bigr)  
\bigl(t_{k}(z)\pm10^{-k}\bigr).  
$$

Choose a fixed integer $M$ larger than the magnitudes of $x,y,z$. Expanding these rational products shows that each differs from $t_{k}(x)t_{k}(y)t_{k}(z)$ by at most

$$  
(3M^{2}+3M+1)10^{-k}.  
$$

Thus the common interval can be made arbitrarily short, proving $(xy)z=x(yz)$.

**Identity.** Both $1x$ and $x$ lie between $t_{k}(x)-10^{-k}$ and $t_{k}(x)+10^{-k}$ for every $k$. Hence $1x=x$. The decimals $1$ and $0$ are distinct.

**Inverse.** Let $x>0$ and set

$$  
E=\lbrace y\ge0<1\rbrace.  
$$

First choose a positive terminating decimal $p<x$ and an integer $M>x$.

- For large $k$, we have $M10^{-k}<1$. Then $x10^{-k}\le M10^{-k}<1$, so $10^{-k}\in E$.
    
- Choose an integer $N$ with $pN>1$. If $y\ge N$, then $xy\ge pN>1$. Thus $N$ is an upper bound of $E$.
    

Therefore $r=\sup E$ exists and $r>0$.

Use truncation at place $k$ to choose positive terminating bounds $a<x<b$ and $c<r<d$, each of width $2\cdot10^{-k}$. The product bounds put $xr$ in $[ac,bd]$, whose length is

$$  
bd-ac=b(d-c)+c(b-a)=2(b+c)10^{-k}.  
$$

Since $b+c$ is bounded by a fixed integer, this interval can be made arbitrarily short.

- If $xr<1$, choose the bounds so that $bd<1$. Then $xd\le bd<1$, so $d\in E$ although $d>r$, a contradiction.
    
- If $xr>1$, choose the bounds so that $ac>1$. Every $y\ge c$ satisfies $xy\ge ac>1$, so $c<r$ is an upper bound of $E$, a contradiction.
    

Hence $xr=1$. For $x<0$, apply this result to $-x$ and reverse the inverse's sign.

Finally, positive terminating lower bounds give $x,y>0\Rightarrow xy>0$.

### 9. Distributive law

Choose an integer $M$ larger than the magnitudes of $x,y,z$.

By the addition bounds, $y+z$ lies between

$$  
t_{k}(y)+t_{k}(z)\pm2\cdot10^{-k}.  
$$

Apply the product bounds with $x$. Expanding the rational endpoints shows that $x(y+z)$ lies between

$$  
t_{k}(x)t_{k}(y)+t_{k}(x)t_{k}(z)  
\pm(4M+2)10^{-k}.  
$$

Similarly, $xy$ lies between $t_{k}(x)t_{k}(y)\pm(2M+1)10^{-k}$, and $xz$ lies between $t_{k}(x)t_{k}(z)\pm(2M+1)10^{-k}$. Adding these bounds puts $xy+xz$ in the same interval.

That interval has arbitrarily small length. Hence

$$  
x(y+z)=xy+xz.  
$$

The product bounds already cover all signs.

### 10. Awkwardness of decimal expansions

Choose $K>\max\lbrace n,m\rbrace$ and set

$$  
x_{1}=0,\qquad x_{2}=2\cdot10^{-K},\qquad  
y_{1}=y_{2}=10^{-m}-10^{-K}.  
$$

Since $2\cdot10^{-K}<10^{-n}$, the two $x$-truncations at place $n$ are zero. The two $y$-truncations agree because $y_{1}=y_{2}$.

But

$$  
t_{m}(x_{1}+y_{1})=0,\qquad  
t_{m}(x_{2}+y_{2})=10^{-m}.  
$$

## PSET 2

### 1. Embed $\mathbb{Q}$ into an ordered field $F$

**Show that $1_{F}>0_{F}$.** The field axioms give $1_{F}\ne0_{F}$. If $1_{F}<0_{F}$, adding $-1_{F}$ gives $-1_{F}>0_{F}$. The product of two positive elements is positive, so

$$  
1_{F}=(-1_{F})(-1_{F})>0_{F},  
$$

a contradiction. Thus $1_{F}>0_{F}$.

**Represent the integers in $F$.** For $n>0$, let $n\cdot1_{F}$ mean the sum of $n$ copies of $1_{F}$. Also define

$$  
0\cdot1_{F}=0_{F},\qquad  
(-n)\cdot1_{F}=-(n\cdot1_{F}).  
$$

Combining sums of ones gives

$$  
(m+n)\cdot1_{F}=m\cdot1_{F}+n\cdot1_{F}.  
$$

Distributing a product of two such sums gives

$$  
(mn)\cdot1_{F}=(m\cdot1_{F})(n\cdot1_{F}).  
$$

These hold first for nonnegative integers. Cancelling opposite copies of $1_{F}$ handles mixed sums; the field's sign rules handle negative products.

Since $1_{F}>0_{F}$, a sum of $n>0$ copies is positive. Negative integer multiples are negative. Therefore

$$  
n\cdot1_{F}=0_{F}\iff n=0,  
$$

and, by applying this sign comparison to $n-m$,

$$  
m<n\iff m\cdot1_{F}<n\cdot1_{F}.  
$$

**Define the map.** Write each rational with positive denominator and set

$$  
f\left(\frac{a}{b}\right)  
=\frac{a\cdot1_{F}}{b\cdot1_{F}},\qquad b>0.  
$$

The denominator is positive, hence nonzero, so division in $F$ is defined.

**Well-defined.** If $a/b=c/d$, where $b,d>0$, then $ad=bc$. Thus

$$  
(a\cdot1_{F})(d\cdot1_{F})  
=(c\cdot1_{F})(b\cdot1_{F}).  
$$

Multiplying by $(b\cdot1_{F})^{-1}(d\cdot1_{F})^{-1}$ gives

$$  
\frac{a\cdot1_{F}}{b\cdot1_{F}}  
=\frac{c\cdot1_{F}}{d\cdot1_{F}}.  
$$

So the value of $f$ does not depend on the fraction used.

**Addition.** Using the integer identities above,

$$  
\begin{aligned}  
f\left(\frac{a}{b}+\frac{c}{d}\right)  
&=f\left(\frac{ad+bc}{bd}\right)\  
&=\frac{(a\cdot1_{F})(d\cdot1_{F})+(b\cdot1_{F})(c\cdot1_{F})}  
{(b\cdot1_{F})(d\cdot1_{F})}\  
&=\frac{a\cdot1_{F}}{b\cdot1_{F}}+  
\frac{c\cdot1_{F}}{d\cdot1_{F}}\  
&=f\left(\frac{a}{b}\right)+f\left(\frac{c}{d}\right).  
\end{aligned}  
$$

**Multiplication.** Similarly,

$$  
\begin{aligned}  
f\left(\frac{a}{b}\frac{c}{d}\right)  
&=f\left(\frac{ac}{bd}\right)\  
&=\frac{(a\cdot1_{F})(c\cdot1_{F})}{(b\cdot1_{F})(d\cdot1_{F})}\  
&=f\left(\frac{a}{b}\right)f\left(\frac{c}{d}\right).  
\end{aligned}  
$$

**Injective.** If $f(a/b)=f(c/d)$, clearing the nonzero denominators gives

$$  
(ad-bc)\cdot1_{F}=0_{F}.  
$$

Hence $ad-bc=0$, so $a/b=c/d$.

**Order.** Because $b,d$ and their images are positive, multiplying inequalities by their denominators preserves the direction. Thus

$$  
\begin{aligned}  
\frac{a}{b}<\frac{c}{d}  
&\iff ad<bc\  
&\iff (ad)\cdot1_{F}<(bc)\cdot1_{F}\  
&\iff f\left(\frac{a}{b}\right)<f\left(\frac{c}{d}\right).  
\end{aligned}  
$$

**The image is a subfield.** Let $S=f(\mathbb{Q})$. It contains $f(0)=0_{F}$ and $f(1)=1_{F}$, and the formulas above show closure under addition and multiplication. Also,

$$  
f(-r)+f(r)=f(0)=0_{F},  
$$

so $-f(r)=f(-r)\in S$. For $r\ne0$,

$$  
f(r)f(1/r)=f(1)=1_{F},  
$$

so the inverse of $f(r)$ also belongs to $S$.

Thus $S$ is an ordered subfield of $F$. The map $f:\mathbb{Q}\to S$ is onto by the definition of $S$, injective as proved above, and preserves addition, multiplication, and order.

### 2. Isomorphisms preserve suprema

Let $\alpha=\sup A$.

**Upper bound.** For every $a\in A$, we have $a\le\alpha$, so $f(a)\le f(\alpha)$. Thus $f(\alpha)$ is an upper bound of $f(A)$.

**Least.** Let $\beta$ be another upper bound. Since $f$ is onto, write $\beta=f(\gamma)$. For every $a\in A$,

$$  
f(a)\le f(\gamma)\quad\Longrightarrow\quad a\le\gamma.  
$$

Therefore $\gamma$ is an upper bound of $A$, so $\alpha\le\gamma$. Applying $f$ gives $f(\alpha)\le\beta$. Hence $f(\alpha)=\sup f(A)$.

### 3. Every ordered field with LUB is isomorphic to $\mathbb{R}$

Use #1 to regard $\mathbb{Q}$ as a subfield of $F$. Regard $\mathbb{R}$ as Rudin's field of cuts of $\mathbb{Q}$. The PDF's phrase “cuts of the reals” is a typo.

**Positive integers are unbounded in $F$.** If they had supremum $s$, then $s-1$ would not be an upper bound. Some positive integer $n$ would satisfy $n>s-1$, giving $n+1>s$, a contradiction.

**There is a rational between any $x<y$ in $F$.** Choose a positive integer $n>(y-x)^{-1}$, so $1/n<y-x$. Let $m$ be the least integer greater than $nx$; it exists by well-ordering after an integer shift. Then $m-1\le nx<m$, so

$$  
x<\frac{m}{n}\le x+\frac{1}{n}<y.  
$$

**Define the map.** Set

$$  
f(x)=\lbrace q\in\mathbb{Q}<x\rbrace.  
$$

This is a cut: integer bounds make it nonempty and proper; it contains every rational below any of its elements; and rational density gives no greatest element.

**Order and injectivity.** If $x<y$, then $f(x)\subseteq f(y)$. A rational strictly between $x,y$ belongs to $f(y)$ but not $f(x)$, so the inclusion is strict. Trichotomy then gives order reflection and injectivity.

**Onto.** Given a cut $\alpha$, let $x=\sup_{F}\alpha$. This supremum exists because $\alpha$ is nonempty and any rational outside it is an upper bound.

- If $q\in\alpha$, choose $r\in\alpha$ with $q<r$. Then $q<r\le x$, so $q\in f(x)$.
    
- If $q\in f(x)$, then $q<x$, so $q$ is not an upper bound of $\alpha$. Some $r\in\alpha$ satisfies $q<r$; the cut property gives $q\in\alpha$.
    

Thus $f(x)=\alpha$.

**Addition.** A sum of a rational below $x$ and one below $y$ is below $x+y$. Hence $f(x)+f(y)\subseteq f(x+y)$.

Conversely, if rational $q<x+y$, choose rational $r$ with

$$  
q-y<r<x.  
$$

Then $q-r<y$, so $q=r+(q-r)\in f(x)+f(y)$. Therefore

$$  
f(x+y)=f(x)+f(y).  
$$

**Positive multiplication.** Suppose $x,y>0$. If $q<rs$ for positive rationals $r<x$, $s<y$, then $q<xy$. This gives $f(x)f(y)\subseteq f(xy)$.

Conversely, let rational $q<xy$.

- If $q>0$, choose positive rationals $r,s$ with
    
    $$  
    \frac{q}{y}<r<x,\qquad \frac{q}{r}<s<y.  
    $$
    
    Then $q<rs$, so $q\in f(x)f(y)$.
    
- If $q\le0$, choose any positive rationals $r<x$, $s<y$. Again $q<rs$.
    

Thus $f(xy)=f(x)f(y)$ for positive factors.

Finally, $f(0)$ and $f(1)$ are the zero and unit cuts. Additivity gives $f(-x)=-f(x)$, and the sign rules give the remaining product cases. Hence $f$ is an ordered-field isomorphism.

### 4. $I_{n}$ and $I_{m}$ are bijective iff $n=m$

First prove by induction that there is no injection $I_{n+1}\to I_{n}$.

- For $n=1$, two distinct elements cannot both map injectively into a one-element set.
    
- Suppose the statement holds for $n-1$. If an injection $I_{n+1}\to I_{n}$ existed, relabel the target so that $n+1$ maps to $n$. Its restriction to $I_{n}$ would then map injectively into $I_{n-1}$, contradicting the induction hypothesis.
    

If $m>n$, an injection $I_{m}\to I_{n}$ would restrict to the forbidden injection $I_{n+1}\to I_{n}$. A bijection with $m\ne n$, or its inverse, would give such an injection.

If $m=n$, the identity is a bijection.

### 5. Finite-alphabet languages are finite or countably infinite

Order the finite alphabet. List all words first by length, then in dictionary order within each length. Each length contributes finitely many words, so this gives a list of all finite words.

If the language is infinite, select its first word in the list, then its next, and so on. Every word is reached because it has only finitely many predecessors. This enumerates the language without repetitions.

Thus the language is either finite or countably infinite.

### 6. Reals with two decimal expansions are countably infinite

These are exactly the terminating decimals:

$$  
D=\left\lbrace\frac{k}{10^{n}}\mid k\in\mathbb{Z},\ n=0,1,2,\ldots\right\rbrace.  
$$

Every nonzero terminating decimal has a second expansion ending in nines. Under PSET 1's convention, $0$ has the two expansions $+0.000\ldots$ and $-0.000\ldots$. No other real has two expansions.

The set is countable because it is a subset of $\mathbb{Q}$. It is infinite because $10^{-1},10^{-2},\ldots$ are distinct. Hence it is countably infinite.

### 7. Bijection between $\mathbb{R}$ and all distinct decimal expansions

List the set from #6 as $D=\lbrace d_{0},d_{1},\ldots\rbrace$, without repetitions. Call the two expansions of $d_{n}$ $a_{n}$ and $b_{n}$.

Define

$$  
f(d_{2n})=a_{n},\qquad f(d_{2n+1})=b_{n}.  
$$

For $r\notin D$, let $f(r)$ be its unique decimal expansion.

Each $a_{n}$ has exactly the preimage $d_{2n}$, and each $b_{n}$ has exactly the preimage $d_{2n+1}$. Every remaining expansion has its represented real as its only preimage. Thus $f$ is bijective.

### 8. $\mathcal{P}(C)$ is uncountable when $C$ is countably infinite

Write $C=\lbrace c_{1},c_{2},\ldots\rbrace$ without repetitions. Its power set is infinite because it contains all singletons.

If it were countably infinite, list it as $A_{1},A_{2},\ldots$ and define

$$  
D=\lbrace c_{n}:c_{n}\notin A_{n}\rbrace.  
$$

For each $n$, the sets $D$ and $A_{n}$ disagree about whether they contain $c_{n}$. Thus $D$ is a subset of $C$ missing from the list, a contradiction.

### 9. No set is bijective with its power set

Suppose $f\to\mathcal{P}(S)$ were onto. Define

$$  
D=\lbrace s\in S\notin f(s)\rbrace.  
$$

Since $D\subseteq S$, there must be $s_{0}\in S$ with $f(s_{0})=D$. But then

$$  
s_{0}\in D\iff s_{0}\notin f(s_{0})\iff s_{0}\notin D,  
$$

a contradiction. Thus no surjection, and hence no bijection, exists. This also covers $S=\varnothing$.

### 10. Cantor–Schröder–Bernstein construction

Let $f\to B'\subseteq B$ and $g'\to B$ be the given bijections.

Start with the points where $g$ is unavailable, then repeatedly follow $f$ and $g^{-1}$. Define

$$  
C_{0}=A\setminus A',\qquad  
C_{n+1}=g^{-1}(f(C_{n})),\qquad  
C=\bigcup_{n\ge0}C_{n}.  
$$

Set

$$  
h(a)=\begin{cases}  
f(a),&a\in C,\  
g(a),&a\notin C.  
\end{cases}  
$$

This is well-defined: $a\notin C$ implies $a\notin C_{0}$, hence $a\in A'$.

**Injective.** Within either branch, use injectivity of $f$ or $g$. If $a\in C_{n}$ and $b\notin C$ had $f(a)=g(b)$, then

$$  
b=g^{-1}(f(a))\in C_{n+1}\subseteq C,  
$$

a contradiction.

**Onto.** Given $b\in B$, let $a=g^{-1}(b)\in A'$.

- If $a\notin C$, then $h(a)=g(a)=b$.
    
- If $a\in C$, it cannot lie in $C_{0}$ because $a\in A'$. Thus $a\in C_{n+1}$ for some $n$, so $a=g^{-1}(f(c))$ for some $c\in C_{n}$. Hence $h(c)=f(c)=b$.
    

Therefore $h$ is a bijection.

## Corrections to the accompanying notes

**Positive cut multiplication uses “there exist”:**

$$  
\alpha\beta=\lbrace q\in\mathbb{Q}:\exists r\in\alpha,\ \exists s\in\beta,\ r>0,\ s>0,\ q<rs\rbrace.  
$$

Using $q\le rs$ gives the same cut. Using “for all” in place of “there exist” is incorrect.

**Extended reals:** $\overline{\mathbb{R}}=\mathbb{R}\cup\lbrace-\infty,+\infty\rbrace$ is an ordered set, not a field. For example, $+\infty+(-\infty)$ is undefined.