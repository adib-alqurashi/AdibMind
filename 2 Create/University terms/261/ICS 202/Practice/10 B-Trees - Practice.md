---
course: ICS 202
topic: B-Trees
slides: "[[261 ICS202-10-BTrees.pdf]]"
type: final-practice
---
# 10 — B-Trees · Final MCQ Practice

> [!info] Conventions (from the slides)
> In a B-tree of order $m$: max keys $=m-1$, and a node **overflows** when it reaches $m$ keys. A non-root node has min keys $=\lceil m/2\rceil-1$ and **underflows** at $\lceil m/2\rceil-2$. The root has $\ge 1$ key. For odd $m$ the middle key is promoted. For even $m$: **right-bias** means the right node gets more keys, **left-bias** means the left node does. A key rotation is always tried before a merge. Root height $=0$.

---

**1.** The keys $50, 30, 70, 20, 40, 60, 80, 10, 25$ are inserted, in this order, into an empty B-tree of **order 3**. The final tree is:

- (A) `[30 | 50]` with leaves `[10 20] [25 40] [60 70 80]`
- (B) `[50]` → `[20 | 30]`, `[70]` → leaves `[10] [25] [40] [60] [80]`
- (C) `[40]` → `[20 | 30]`, `[60 | 70]` → leaves `[10] [25] [30] [50] [80]`
- (D) `[30]` → `[20]`, `[50 | 70]` → leaves `[10] [25] [40] [60] [80]`
- (E) `[50]` → `[25]`, `[70]` → leaves `[10 20] [30 40] [60] [80]`

> [!check]- Answer
> **(B)**. The splits are: $70$ (promote $50$), $40$ (promote $30$), $80$ (promote $70$, which then splits the root and promotes $50$), and $25$ (promote $20$).

**2.** In Q1, how many **node splits** occurred in total, and how many nodes does the final tree have?

- (A) $4$ splits, $8$ nodes
- (B) $5$ splits, $7$ nodes
- (C) $5$ splits, $8$ nodes
- (D) $6$ splits, $8$ nodes
- (E) $4$ splits, $7$ nodes

> [!check]- Answer
> **(C)**. There are 3 leaf splits for $70$, $40$, $80$, 1 root split caused by $80$'s promotion, and 1 leaf split for $25$, so $5$ splits. The final tree has a root, $2$ internal nodes and $5$ leaves, so $8$ nodes.

**3.** The keys $15, 40, 25, 10, 30, 50, 5, 20, 35, 45, 55$ are inserted in order into an empty B-tree of **order 5**. The root of the final tree is:

- (A) `[25]`
- (B) `[30]`
- (C) `[25 | 40]`
- (D) `[20 | 40]`
- (E) `[25 | 35 | 45]`

> [!check]- Answer
> **(C)**. $30$ fills `[10 15 25 30 40]`, which splits and promotes $25$. Later $45$ overflows `[30 35 40 45 50]` and promotes $40$. The leaves are `[5 10 15 20] [30 35] [45 50 55]`.

**4.** In a B-tree of **order 4**, the leaf `[14 | 26 | 33]` receives key $41$ and overflows. Which key is promoted under **right-bias** and under **left-bias**, respectively?

- (A) $26$ and $33$
- (B) $33$ and $26$
- (C) $26$ and $26$
- (D) $33$ and $33$
- (E) $14$ and $41$

> [!check]- Answer
> **(A)**. The node holds $14,26,33,41$. Right-bias gives the right node 2 keys, so the split is `[14]` ↑$26$ `[33 41]`. Left-bias gives the left node 2 keys, so the split is `[14 26]` ↑$33$ `[41]`.

**5.** The **maximum** number of keys in a B-tree of **order 4** and **height 2** (3 levels) is:

- (A) $21$
- (B) $48$
- (C) $63$
- (D) $64$
- (E) $84$

> [!check]- Answer
> **(C)**. There are at most $1+4+16=21$ nodes, each with $m-1=3$ keys, so $21\cdot 3=63=4^{3}-1$.

**6.** The **minimum** number of keys in a B-tree of **order 5** and **height 2** is:

- (A) $7$
- (B) $11$
- (C) $13$
- (D) $17$
- (E) $26$

> [!check]- Answer
> **(D)**. The root has $1$ key and $2$ children. Each of those has $2$ keys and $\lceil 5/2\rceil=3$ children, giving $6$ leaves with $2$ keys each. Total $1+4+12=17$.

**7.** In a B-tree of **order 7**, a non-root node must contain between ___ keys, and it underflows when it has ___ keys.

- (A) $3$ and $6$; $2$
- (B) $3$ and $7$; $2$
- (C) $4$ and $6$; $3$
- (D) $2$ and $6$; $1$
- (E) $3$ and $6$; $3$

> [!check]- Answer
> **(A)**. Min $=\lceil 7/2\rceil-1=3$, max $=m-1=6$, and underflow happens at $\lceil 7/2\rceil-2=2$.

**8.** A new key is inserted into a B-tree that has **four** levels. What is the **maximum** number of extra nodes that can be created?

- (A) $3$
- (B) $4$
- (C) $5$
- (D) $8$
- (E) $1$

> [!check]- Answer
> **(C)**. In the worst case each of the 4 levels splits, adding one new sibling each ($4$ nodes), and the root split also creates a new root ($+1$).

**9.** B-trees are considered **balanced** because:

- (A) every node has exactly $m-1$ keys.
- (B) the lengths of the paths from the root to all leaves are equal.
- (C) the paths from the root to the leaves differ in length by at most $1$.
- (D) sibling nodes always have the same number of keys.
- (E) the root always has exactly $2$ children.

> [!check]- Answer
> **(B)**. All leaves are at the same level, because the tree grows only at the root (by splitting).

**10.** Consider this B-tree of **order 4**:

```
                      [50]
           [20 | 35]          [65 | 80]
 [5 10 15] [22 28] [38 41 47]  [55 60] [70 75] [85 90 95]
```

Inserting which sequence (in the given order) causes **at least one node split**?

- (A) $25, 72, 58$
- (B) $61, 77, 30$
- (C) $24, 72, 26$
- (D) $52, 78$
- (E) More than one of the given answers

> [!check]- Answer
> **(C)**. $24$ makes `[22 24 28]`, and $26$ then makes 4 keys, which is an overflow. In the other options every leaf reaches at most 3 keys.

**11.** Deleting a key from a **non-root leaf** that has the **minimum** number of keys always results in:

- (A) a merge with an adjacent sibling only.
- (B) a key rotation (borrowing) from an adjacent sibling only.
- (C) either a key rotation from an adjacent sibling or a merge with an adjacent sibling.
- (D) both a key rotation and a merge.
- (E) the tree height decreasing by $1$.

> [!check]- Answer
> **(C)**. The leaf underflows. A rotation is tried first if a sibling has $\ge\lceil m/2\rceil$ keys; otherwise the leaf merges.

**12.** Consider this B-tree of **order 5**:

```
          [30 | 60]
 [10 20]  [40 45 50]  [70 80]
```

After deleting $20$, the root is:

- (A) `[30 | 60]`
- (B) `[40 | 60]`
- (C) `[60]`
- (D) `[45 | 60]`
- (E) `[30 | 50]`

> [!check]- Answer
> **(B)**. `[10]` underflows (min is 2). The right sibling `[40 45 50]` has $3\ge\lceil5/2\rceil$ keys, so a left key-rotation moves $30$ down (giving `[10 30]`) and $40$ up.

**13.** In the original tree of Q12, deleting $80$ instead makes the root:

- (A) `[30 | 50]`
- (B) `[30 | 45]`
- (C) `[30]`
- (D) `[30 | 60]`
- (E) `[40 | 60]`

> [!check]- Answer
> **(A)**. `[70]` underflows. Its left sibling `[40 45 50]` can lend, so a right key-rotation moves $60$ down (giving `[60 70]`) and $50$ up.

**14.** Consider this B-tree of **order 3**. Deleting which key reduces the **number of levels**?

```
               [40]
       [20]              [60 | 80]
   [10]   [30]      [50]   [70]   [90]
```

- (A) $10$
- (B) $50$
- (C) $90$
- (D) $40$
- (E) None of the given keys

> [!check]- Answer
> **(E)**. Deleting $10$ merges `[20 30]`, and the empty parent then borrows through the sibling `[60 80]` (rotation: $40$ down, $60$ up). Deleting $50$ or $90$ merges inside the right subtree, whose parent still keeps one key. Deleting $40$ swaps it with $30$ or $50$ (in a leaf), and either way the fix-up keeps 3 levels. The height never shrinks.

**15.** To delete a key that is in an **internal** node of a B-tree, the algorithm first:

- (A) merges the node's two children.
- (B) swaps it with its inorder predecessor or successor, which is always in a leaf.
- (C) moves it to the root.
- (D) deletes the whole subtree under it.
- (E) splits the node.

> [!check]- Answer
> **(B)**. The deletion is then done at the leaf, where the underflow cases are handled.

**16.** Why are B-trees preferred over AVL trees for data stored on **disk**?

- (A) B-tree nodes hold a single key, which reduces comparisons.
- (B) A large branching factor makes the tree shallow, so a search needs far fewer disk accesses.
- (C) B-trees do not need to be balanced.
- (D) AVL trees cannot store more than $2^{16}$ keys.
- (E) B-tree search is $O(1)$.

> [!check]- Answer
> **(B)**. In the slides' example, $16{,}000{,}000$ keys with $m=300$ take about $4$ disk accesses, while an AVL tree needs about $24$ comparisons/levels.

**17.** You need the data structure (among those covered) that is **most efficient for range queries** on huge, disk-resident data, such as database indices. The slides name:

- (A) an AVL tree
- (B) a hash table
- (C) a min-heap
- (D) a B$^+$-tree (a B-tree variant)
- (E) a doubly linked list

> [!check]- Answer
> **(D)**. The slides note that the B$^+$-tree is the most common structure for database indices. Its keys are kept in linked, sorted leaves, which suits range scans.
