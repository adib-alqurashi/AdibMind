---
course: ICS 202
topic: AVL Trees
slides: "[[261 ICS202-08-AVL Trees.pdf]]"
type: final-practice
---
# 08 — AVL Trees · Final MCQ Practice

> [!info] Conventions (from the slides)
> $\text{BF}(x)=h(\text{right})-h(\text{left})$, and a node is balanced when $\text{BF}\in\{-1,0,+1\}$. Height of a single node $=0$, empty tree $=-1$. A **double rotation counts as 2 rotations**. Deletion is BST *deletion by copying* followed by rebalancing.

---

**1.** The keys $30, 20, 10, 25, 28, 40, 50$ are inserted, in this order, into an empty AVL tree. How many rotations are performed?

- (A) $3$
- (B) $4$
- (C) $5$
- (D) $6$
- (E) $2$

> [!check]- Answer
> **(C)**. $10$ causes a single right rotation at $30$ (1). $28$ causes an LR at $30$ (2 more, 3 total). $40$ causes an RR at root $20$ (4). $50$ causes an RR at $30$ (5).

**2.** After the insertions in Q1, the **preorder** traversal of the AVL tree is:

- (A) $20, 10, 28, 25, 40, 30, 50$
- (B) $28, 20, 10, 25, 40, 30, 50$
- (C) $25, 20, 10, 28, 40, 30, 50$
- (D) $28, 10, 20, 25, 30, 40, 50$
- (E) $30, 20, 10, 25, 28, 40, 50$

> [!check]- Answer
> **(B)**. The final tree is $28(20(10,25),\,40(30,50))$, which is perfect with height $2$.

**3.** Inserting $1, 2, 3, 4, 5, 6, 7$ in order into an empty AVL tree requires how many rotations, and what is the final root?

- (A) $3$ rotations, root $4$
- (B) $4$ rotations, root $3$
- (C) $5$ rotations, root $4$
- (D) $4$ rotations, root $4$
- (E) $6$ rotations, root $2$

> [!check]- Answer
> **(D)**. Every imbalance is RR, so each fix is one single left rotation. Rotations happen when inserting $3$, $5$, $6$ (the root $2$ rotates) and $7$. The result is a perfect tree rooted at $4$.

**4.** What is the **maximum** height of an AVL tree with $20$ nodes?

- (A) $4$
- (B) $6$
- (C) $19$
- (D) $5$
- (E) $3$

> [!check]- Answer
> **(D)**. $N(h)=N(h-1)+N(h-2)+1$ with $N(0)=1, N(1)=2$ gives $1,2,4,7,12,20,33$. Since $N(5)=20$, $20$ nodes can reach height $5$, and height $6$ would need $33$.

**5.** The **minimum** number of nodes in an AVL tree of height $6$ is:

- (A) $33$
- (B) $20$
- (C) $64$
- (D) $127$
- (E) $54$

> [!check]- Answer
> **(A)**. $N(6)=N(5)+N(4)+1=20+12+1=33$.

**6.** After deleting $70$ from the AVL tree below, the **root** will be:

```
        40
      /    \
    20      60
   /  \       \
  10   30      70
      /  \
     25   35
```

- (A) $40$
- (B) $20$
- (C) $30$
- (D) $60$
- (E) $25$

> [!check]- Answer
> **(C)**. With $70$ gone, $\text{BF}(40)=0-2=-2$ and $\text{BF}(20)=+1$. That is an LR case: a left rotation at $20$, then a right rotation at $40$, which makes $30$ the root.

**7.** Consider the AVL tree below. After deleting $10$, which node becomes the **left child** of $44$, and how many rotations were performed?

```
            44
         /      \
       17        62
      /  \      /   \
    10    32   50    78
         /    /  \     \
        25   48  54    88
```

- (A) $32$, 1 rotation
- (B) $25$, 2 rotations
- (C) $17$, 0 rotations
- (D) $25$, 1 rotation
- (E) $32$, 2 rotations

> [!check]- Answer
> **(B)**. Now $\text{BF}(17)=+2$ and $\text{BF}(32)=-1$, an RL case. A right rotation at $32$, then a left rotation at $17$, gives the subtree $25(17,32)$.

**8.** In the tree of Q7, what is the **balance factor of $44$** after deleting $10$ and rebalancing?

- (A) $0$
- (B) $-1$
- (C) $+2$
- (D) $-2$
- (E) $+1$

> [!check]- Answer
> **(E)**. The left subtree $25(17,32)$ has height $1$ and the right subtree rooted at $62$ has height $2$, so $\text{BF}=2-1=+1$.

**9.** Inserting which of the following keys into the AVL tree below causes a **double rotation**?

```
              50
          /        \
        40          70
       /  \        /  \
     30    45     60   80
    / \    /        \
   20 35  42        65
```

- (A) $36$
- (B) $85$
- (C) $10$
- (D) $44$
- (E) None of them

> [!check]- Answer
> **(D)**. $44$ goes to the right of $42$, making $\text{BF}(45)=-2$ with $\text{BF}(42)=+1$, an LR case. The keys $36, 85, 10$ cause no imbalance.

**10.** During AVL insertion, the deepest unbalanced node $x$ has $\text{BF}(x)=-2$ and its left child $y$ has $\text{BF}(y)=+1$. The fix is:

- (A) a single right rotation at $x$.
- (B) a single left rotation at $x$.
- (C) a left rotation at $y$, then a right rotation at $x$.
- (D) a right rotation at $y$, then a left rotation at $x$.
- (E) no rotation; only update heights.

> [!check]- Answer
> **(C)**. This is the LR case: the left subtree is taller, and the new key went into the right subtree of the left child.

**11.** A double rotation in an AVL tree with $n$ nodes takes:

- (A) $O(1)$
- (B) $O(\log n)$
- (C) $O(n)$
- (D) $O(n\log n)$
- (E) $O(\sqrt n)$

> [!check]- Answer
> **(A)**. It is two pointer-rearranging single rotations, independent of $n$. Finding the unbalanced node is part of the $O(\log n)$ insertion, not part of the rotation.

**12.** Which of the following is **always** an AVL tree?

- (A) A full binary search tree only
- (B) A perfect BST and a complete BST
- (C) A complete BST only
- (D) Any BST of height $\le n/2$
- (E) A full BST and a complete BST

> [!check]- Answer
> **(B)**. In perfect and complete trees, the subtree heights at every node differ by at most $1$. A full BST can be very lopsided (for example a "caterpillar").

**13.** Which statement is **true**?

- (A) After an AVL insertion, rotations may be needed at every ancestor up to the root.
- (B) After an AVL insertion, at most one single or one double rotation restores balance; after a deletion, rebalancing may propagate up to the root.
- (C) AVL deletion never needs a rotation.
- (D) The height of an AVL tree with $n$ nodes can be $n-1$.
- (E) Searching an AVL tree costs $O(n)$ in the worst case.

> [!check]- Answer
> **(B)**. A rotation after insertion restores the subtree's old height, so the ancestors stay balanced. Deletion can shrink heights, so the imbalance can repeat higher up.

**14.** The keys $50, 40, 30, 45, 47, 60, 55, 52$ are inserted in order into an empty AVL tree. How many rotations are performed (double $=2$)?

- (A) $4$
- (B) $5$
- (C) $6$
- (D) $7$
- (E) $3$

> [!check]- Answer
> **(C)**. $30$ causes a single rotation (1). $47$ causes an LR at $50$ (3). $60$ causes an RR at root $40$ (4). $55$ causes an RL at $50$ (6). $52$ causes no imbalance.

**15.** For the tree in Q9, the balance factors of $45$ and $70$ are, respectively:

- (A) $-1$ and $-1$
- (B) $+1$ and $-1$
- (C) $-1$ and $+1$
- (D) $0$ and $0$
- (E) $+1$ and $+1$

> [!check]- Answer
> **(A)**. $45$ has only a left child, so $\text{BF}=-1-0=-1$. For $70$, the left subtree $60(\cdot,65)$ has height $1$ and the right subtree $80$ has height $0$, so $\text{BF}=0-1=-1$.

**16.** Why is an AVL tree preferred over an ordinary BST for searching?

- (A) It uses less memory per node.
- (B) It guarantees $O(\log n)$ height, so search, insertion and deletion are $O(\log n)$ in the worst case.
- (C) Its insertion never changes the shape of the tree.
- (D) It stores keys in a complete-tree array.
- (E) It allows duplicate keys.

> [!check]- Answer
> **(B)**. Height balance prevents the $O(n)$ skewed case of a plain BST.
