# Chapter 12: Binary Search Trees

---

## Overview

> A concise introduction describing the chapter’s subject, scope, and primary objectives.

## 12.1 What Is A Binary Search Tree

---

### Definitions

- **Binary Search Tree**: Binary tree. Each node has a *key* and satellite data along with pointers *left*, *right*, and *p* pointing to the left child, right child, and parent respectively. The value of such pointers is $NIL$ if no such node exists. The tree itself has a pointer *root* which points to the root node. The keys must satisfy:
	- Let $x$ be a node in the tree. Then if $y$ is a node in the left subtree of x, $y.key \le x.key$. If $y$ is a node in the right subtree, then $x.key \le y.key$. 

### Algorithms

**In ORDER TREE WALK**
Prints nodes of a binary search tree in-order. Let $n$ denote the node count of the tree.
_Time Complexity: $\mathcal{O}(n)$_  (Consider all calls to nodes and the NIL)
	`INORDER-TREE-WALK(x : node)`
	1. if $x \ne NIL$
		1.1. `INORDER-TREE-WALK(x.left)`
		1.2. print x.key
		1.3. `INORDER-TREE-WALK(x.right)`

**Pre-Order Tree Walk**
Defined in a similar manner to In-Order, moving the print statement.

**Post-Order Tree Walk**
Defined in a similar manner to In-Order, moving the print statement.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 12.2 Querying A Binary Search Tree

---

### Algorithms

**Tree Search**
Searches a Binary Search Tree for some a node with a given value for *key*, returns $NIL$ if none is found. Let $h$ denote the height of the tree.
_Time Complexity: $\mathcal{O}(h)$_
	`TREE-SEARCH(x : root, key)`
	1. if $x == NIL$ or $x.key == k$:
		1.1. Return $x$
	2. if $k < x.key$:
		2.1. Return `TREE-SEARCH(x.left, k)`
	3. else Return `TREE-SEARCH(x.right, k)` 

**Tree Minimum**
Returns the node corresponding to the minimum *key* in a binary search tree, which is assumed to be non-empty. Let $h$ denote the height of the tree.
_Time Complexity: $\mathcal{O}(h)$_  
	`TREE-MINIMUM(x: node)`
	1. while $x.left \ne NIL$
		1.1. $x = x.left$
	2. Return $x$

**Tree Maximum**
Defined in a similar manner to minimum.

**Tree Successor**
Finds a successor node if it exists, else returns $NIL$. Let $h$ denote the height of the tree.
_Time Complexity: $\mathcal{O}(h)$_  
	`TREE-SUCCESSOR(x: node)`
	1. if $x.right \ne NIL$:
		1.1. return `TREE-MINIMUM(x.right)`
	2. else
		$y = x.p$.
		while $y \ne NIL$ and $x == y.right$:
			$x = y$
			$y = y.p$
		return $y$ 

**Tree Predecessor**
Defined in a similar manner to tree-successor.

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]


## 12.3 Insertion And Deletion

---

### Algorithms

**Tree Insert**
Inserts a new node into a binary search tree. Let $h$ denote the height of the tree.
_Time Complexity: $\mathcal{O}(h)$_
	`TREE-INSERT(T, z) =`
	1. $x = T.root$
	2. $y = NIL$
	3. while $x \ne NIL$:
		3.1. $y = x$
		3.2. If $z.key < x.key$:
			$x = x.left$
		else $x = x.right$
	4. $z.p = y$
	5. if $y == NIL$:
		5.1. $T.root = z$
	6. elseif $z.key < y.key$:
		6.1. $y.left = z$
	 7. else $y.right = z$

**Transplant**
Replaces a subtree with another.
	`TRANSPLANT(T, u, v) =`
	1. if $u.p == NIL$:
		1.1. $T.root = v$
	2. elseif $u = u.p.left$:
		 2.1. $u.p.left = v$
	3. else $u.p.right = v$:
	4. if $v \ne NIL$:
		4.1. $v.p = u.p$ 

**Tree Delete**
Deletes a node in a binary tree of height $h$.
_Time Complexity: $\mathcal{O}(h)$_
	`TREE-DELETE(T, z) =`
	1. if $z.left == NIL$
		1.1. `TRANSPLANT(T, z, z.right)`
	2. elseif $z.right == NIL$
		2.1. `TRANSPLANT(T, z, z.left)`
	3. else $y =$ `TREE-MINIMUM(z.right)`
		3.1. if $y \ne z.right$
			`TRANSPLANT(T, y, y.right)`
			$y.right = z.right$
			$y.right.p = y$
		3.2. `TRANSPLANT(T, z, y)`
		3.3. $y.left = z.left$
		3.4. $y.left.p = y$ 

### Related Links & References

- **Primary Text [Book]**: _Example Book Title_ — Chapter [Number], Pages [Range]
