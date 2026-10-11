# Problem 1 — Houston Potholes

## (a)

Store the pothole locations as keys in an AVL tree.

Since an AVL tree supports insertion and deletion in

O(log⁡n)O(\log n)

time, this satisfies the required bounds.

## (b)

Use a modified in-order traversal that avoids subtrees that cannot contain a key in $[a,b]$.

```text
REPORT-RANGE(v, a, b)
    if v == NIL
        return

    if v.key > a
        REPORT-RANGE(v.left, a, b)

    if a <= v.key <= b
        output v.key

    if v.key < b
        REPORT-RANGE(v.right, a, b)
```

## (c)

Augment each node $v$ with a field `v.size`, equal to the number of nodes in the subtree rooted at $v$.

For each node,

v.size=1+size(v.left)+size(v.right),v.size = 1 + size(v.left) + size(v.right),

where

size(NIL)=0.size(NIL)=0.

Define `COUNT-LE(x)` to return the number of keys less than or equal to $x$.

```text
COUNT-LE(root, x)
    v = root
    count = 0

    while v != NIL
        if x < v.key
            v = v.left
        else
            count = count + size(v.left) + 1
            v = v.right

    return count
```

Define `COUNT-LT(x)` to return the number of keys strictly less than $x$.

```text
COUNT-LT(root, x)
    v = root
    count = 0

    while v != NIL
        if x <= v.key
            v = v.left
        else
            count = count + size(v.left) + 1
            v = v.right

    return count
```

Then the number of potholes in $[a,b]$ is

COUNT-LE(b)−COUNT-LT(a).

Each procedure follows one root-to-leaf path in the AVL tree, so the query takes

O(log⁡n).O(\log n).

# Problem 2 — Radix Trees

## (1)

A radix tree for a set $S$ of bit strings is a rooted binary tree whose edges are labeled $0$ or $1$, with at most one outgoing edge of each label from any node.

For a node $v$, let $s(v)$ be the string obtained by concatenating, in order, the edge labels on the unique path from the root to $v$. The root represents the empty string $\epsilon$.

A node $v$ is marked exactly when

s(v)∈S.s(v)\in S.
