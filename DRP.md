Linear programming - “planning with linear constraints”
A linear program is the problem of maximizing a given linear function over the set of all vectors that satisfy a given system of linear equations and inequalities.
Inequalities called constraints denoted by m.

![[Screenshot from 2026-02-20 09-30-09.png]]

objective function (minimized or maximized):
$$
c^Tx = c_1x_1 + ... + c_nx_n
$$
where c is a given vector.
Notice any equality can be represented by an inequality and minimizing $c^Tx$ is the same as maximizing $-c^Tx$. Feasible vs optimal solutions.

Specific example: m = 5, c = (1, 1), n = 2

![[Screenshot from 2026-02-20 10-29-54.png]]
infeasible.
![[Screenshot from 2026-02-20 10-30-39.png]]
Unbounded.

![[Screenshot from 2026-02-20 10-38-33.png]]

In theoretical computer science it has become one of the fundamental tools in algorithm design. For a number of computational problems the existence of an efficient (polynomial-time) algorithm was first established by general techniques based on linear programming.
Another surprising application of linear programming is theoretical: the duality theorem, which will be explained in Chapter 6, appears in proofs of numerous mathematical statements, most notably in combinatorics, and it provides a unifying abstract view of many seemingly unrelated results. The duality theorem is also significant algorithmically.


Example 1-

![[Screenshot from 2026-02-20 10-44-34.png]]

The linear program can be solved by standard methods. The optimal solution yields the price of e 0.07 with the following doses: carrot 9.5 g, cabbage 38 g, and pickled cucumber 290 g per dish (all rounded to two significant digits).