---
course: ICS 202
topic: Binary Trees & Binary Search Trees
slides: "[[261 ICS202-07-Binary Trees.pdf]]"
type: final-practice
---
# 07 — Binary Trees & BST · Final MCQ Practice

> [!info] Conventions (from the slides)
> Level/depth of the root $=0$. Height of a node $=$ number of edges on the longest path down to a leaf. Height of an empty tree $=-1$. Choose **one** answer; open the folded box only after you commit.

---

**1.** A BST is built by inserting $45, 28, 63, 15, 33, 50, 71, 30, 40, 55$ in this order into an empty tree. Its **preorder** traversal is:

- (A) $45, 28, 63, 15, 33, 50, 71, 30, 40, 55$
- (B) $15, 30, 40, 33, 28, 55, 50, 71, 63, 45$
- (C) $45, 28, 15, 33, 30, 40, 63, 50, 55, 71$
- (D) $45, 28, 15, 33, 40, 30, 63, 50, 71, 55$
- (E) $15, 28, 30, 33, 40, 45, 50, 55, 63, 71$

> [!check]- Answer
> **(C)**. N-L-R. (A) is breadth-first, (B) is postorder, (E) is inorder.

**2.** For the same BST as Q1, which traversal produces $15, 30, 40, 33, 28, 55, 50, 71, 63, 45$?

- (A) Preorder
- (B) Inorder
- (C) Breadth-first
- (D) Postorder
- (E) None of the given traversals

> [!check]- Answer
> **(D)**. Every node comes after both its subtrees, and the root $45$ is last.

**3.** For the same BST as Q1, the height of the tree and the number of leaves are, respectively:

- (A) $3$ and $5$
- (B) $4$ and $5$
- (C) $3$ and $4$
- (D) $4$ and $4$
- (E) $2$ and $6$

> [!check]- Answer
> **(A)**. The longest path is $45\to28\to33\to30$, which has 3 edges. The leaves are $15, 30, 40, 55, 71$.

**4.** In the BST of Q1, how many nodes are visited (compared) during an **unsuccessful** search for $38$?

- (A) $3$
- (B) $5$
- (C) $2$
- (D) $10$
- (E) $4$

> [!check]- Answer
> **(E)**. $45 \to 28 \to 33 \to 40$. The left child of $40$ is null, so the search stops.

**5.** In the BST of Q1, key $45$ is deleted using **deletion by copying with the inorder successor**. The preorder traversal of the resulting tree is:

- (A) $40, 28, 15, 33, 30, 63, 50, 55, 71$
- (B) $50, 28, 15, 33, 30, 40, 63, 55, 71$
- (C) $28, 15, 33, 30, 40, 63, 50, 55, 71$
- (D) $50, 28, 15, 33, 30, 40, 55, 63, 71$
- (E) $55, 28, 15, 33, 30, 40, 63, 50, 71$

> [!check]- Answer
> **(B)**. The successor is the minimum of the right subtree, $50$. It is copied into the root, and its old node (which has right child $55$) is replaced by $55$. (A) is what you get with the predecessor $40$.

**6.** In the BST of Q1, key $45$ is deleted using **deletion by merging** (the right subtree is attached as the right child of the **rightmost node of the left subtree**). What are the new root and the new height?

- (A) Root $28$, height $5$
- (B) Root $40$, height $3$
- (C) Root $50$, height $3$
- (D) Root $28$, height $4$
- (E) Root $63$, height $5$

> [!check]- Answer
> **(A)**. The left child $28$ becomes the root. Subtree $63$ hangs under $40$, which is the rightmost node of the left subtree. The path $28\to33\to40\to63\to50\to55$ has 5 edges, so merging made the tree **taller**.

**7.** The keys $1, 2, 3, \dots, 60$ are inserted, in this order, into an empty BST. Then:

- (A) all depth-first traversals produce the same output.
- (B) each depth-first traversal produces a different output.
- (C) only preorder and inorder traversals produce the same output.
- (D) only preorder and postorder traversals produce the same output.
- (E) only inorder and postorder traversals produce the same output.

> [!check]- Answer
> **(C)**. The tree is a right-skewed chain. Preorder $=1,2,\dots,60$ and inorder $=1,2,\dots,60$, while postorder $=60,59,\dots,1$.

**8.** The **maximum** number of nodes in a binary tree of height $5$ is:

- (A) $32$
- (B) $31$
- (C) $63$
- (D) $64$
- (E) $6$

> [!check]- Answer
> **(C)**. $\sum_{i=0}^{h}2^i = 2^{h+1}-1 = 2^6-1 = 63$.

**9.** In a **complete** binary tree of height $4$, the number of nodes is:

- (A) exactly $31$
- (B) between $16$ and $31$, inclusive
- (C) between $5$ and $31$, inclusive
- (D) exactly $16$
- (E) between $15$ and $31$, inclusive

> [!check]- Answer
> **(B)**. Levels $0..3$ are full, giving $15$ nodes. Level $4$ has between $1$ and $16$ nodes, so the total is $16$ to $31$.

**10.** The **minimum** height of a binary tree with $100$ nodes is:

- (A) $7$
- (B) $99$
- (C) $5$
- (D) $6$
- (E) $50$

> [!check]- Answer
> **(D)**. $h_{\min}=\lceil \lg(n+1)\rceil-1=\lceil \lg 101\rceil-1=7-1=6$. A tree of height $5$ holds at most $63$ nodes.

**11.** A **full** binary tree (every node has $0$ or $2$ children) has $20$ internal nodes. The number of leaves is:

- (A) $19$
- (B) $20$
- (C) $40$
- (D) $41$
- (E) $21$

> [!check]- Answer
> **(E)**. In a full (decision) tree, leaves $=$ internal nodes $+1$.

**12.** Which of the following statements is **incorrect**?

- (A) Every perfect binary tree is a complete binary tree.
- (B) Every perfect binary tree is a full binary tree.
- (C) Every complete binary tree is a full binary tree.
- (D) In a perfect binary tree, level $k$ contains $2^k$ nodes.
- (E) A skewed binary tree with $n$ nodes has height $n-1$.

> [!check]- Answer
> **(C)**. A complete tree can have a node with exactly one (left) child in the second-to-last level, so it is not necessarily full.

**13.** The **preorder** traversal of a BST is $40, 25, 10, 30, 60, 50, 70, 65$. Its **postorder** traversal is:

- (A) $10, 30, 25, 50, 65, 70, 60, 40$
- (B) $10, 25, 30, 40, 50, 60, 65, 70$
- (C) $10, 30, 25, 65, 70, 50, 60, 40$
- (D) $30, 10, 25, 50, 65, 70, 60, 40$
- (E) $40, 25, 60, 10, 30, 50, 70, 65$

> [!check]- Answer
> **(A)**. Rebuild the tree by inserting the preorder keys: $40(25(10,30),\,60(50,70(65,\cdot)))$. Then read it L-R-N.

**14.** For the expression tree of $(a-b)*(c+d/e)$, which traversal produces the **postfix** expression, and what is it?

- (A) Inorder: $a-b*c+d/e$
- (B) Postorder: $a\,b-c\,d\,e\,/+*$
- (C) Preorder: $*-a\,b+c\,/\,d\,e$
- (D) Postorder: $a\,b\,c\,d\,e-+/*$
- (E) Breadth-first: $*-+a\,b\,c\,/\,d\,e$

> [!check]- Answer
> **(B)**. Postorder produces postfix (preorder produces prefix). Option (C) is a correct prefix expression, but the question asks for postfix.

**15.** In which scenario does searching a BST with $n$ keys cost $O(n)$?

- (A) When the tree is perfectly balanced.
- (B) When the tree is a complete binary tree.
- (C) When the keys were inserted in sorted (increasing or decreasing) order.
- (D) When the tree has an odd number of nodes.
- (E) When the root holds the median key.

> [!check]- Answer
> **(C)**. Sorted insertions create a skewed (linear) tree of height $n-1$.

**16.** In a BST, the inorder successor of a node $x$ that has **two** children is:

- (A) the right child of $x$.
- (B) the minimum key in the right subtree of $x$.
- (C) the maximum key in the left subtree of $x$.
- (D) the parent of $x$.
- (E) always a node with two children.

> [!check]- Answer
> **(B)**. Go one step right, then all the way left. The node you reach has no left child.

**17.** Compared with an array of child pointers, the **left-child right-sibling** representation of a general tree:

- (A) uses more memory and gives faster access.
- (B) uses less memory but may require more node-access time.
- (C) only works when every node has at most two children.
- (D) cannot represent the leaves.
- (E) uses the same memory and the same access time.

> [!check]- Answer
> **(B)**. Each node stores only two references. Reaching the $k$-th child, however, means walking the sibling list.

**18.** Which statement about BST insertion is **true**?

- (A) A new key may be inserted as an internal node if it is smaller than the root.
- (B) A new key is always inserted as a leaf.
- (C) Insertion always keeps the BST height at $\lfloor \lg n\rfloor$.
- (D) Duplicate keys are inserted in the left subtree.
- (E) Insertion takes $O(1)$ in the worst case.

> [!check]- Answer
> **(B)**. The search for the key ends at a null reference, and the new node is placed there. The slides' insert throws on duplicates.
