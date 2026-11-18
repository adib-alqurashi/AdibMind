---
course: ICS 202
topic: Binary Heaps & Priority Queues
slides: "[[261 ICS202-09-Heaps.pdf]]"
type: final-practice
---
# 09 — Binary Heaps · Final MCQ Practice

> [!info] Conventions (from the slides)
> Arrays are **1-indexed**: the root is at $1$, the children of $i$ are at $2i$ and $2i+1$, and the parent is at $\lfloor i/2\rfloor$. The breadth-first order equals the array order. Root height $=0$.

---

**1.** The keys $35, 22, 40, 10, 18, 5, 30$ are inserted, in this order, into an empty **min-heap**. The resulting array is:

- (A) $5, 10, 18, 22, 35, 40, 30$
- (B) $5, 18, 10, 35, 22, 40, 30$
- (C) $5, 18, 10, 22, 35, 40, 30$
- (D) $10, 18, 5, 35, 22, 40, 30$
- (E) $5, 10, 22, 35, 18, 40, 30$

> [!check]- Answer
> **(B)**. $10$ percolates up past $35$ and then $22$. $18$ swaps with $22$. $5$ swaps with $40$ and then with $10$. $30$ stays under $10$.

**2.** The array $35, 22, 40, 10, 18, 5, 30, 12$ is converted into a **min-heap** using the **bottom-up** algorithm. The result is:

- (A) $5, 10, 30, 12, 18, 40, 35, 22$
- (B) $5, 12, 10, 18, 22, 40, 30, 35$
- (C) $5, 10, 12, 22, 18, 40, 30, 35$
- (D) $5, 10, 30, 22, 18, 40, 35, 12$
- (E) $10, 5, 30, 12, 18, 40, 35, 22$

> [!check]- Answer
> **(A)**. Percolate down at $i=4,3,2,1$. $40\leftrightarrow5$, then $22\leftrightarrow10$, then $22\leftrightarrow12$, then $35\leftrightarrow5$ and $35\leftrightarrow30$. (B) is what you get by inserting top-down.

**3.** In Q2, how many **swaps** does the bottom-up algorithm perform?

- (A) $3$
- (B) $4$
- (C) $6$
- (D) $5$
- (E) $7$

> [!check]- Answer
> **(D)**. One swap at $i=3$, two at $i=2$, and two at $i=1$.

**4.** A **deleteMin** is performed on the min-heap $3, 8, 5, 12, 9, 7, 15, 20$. The resulting array is:

- (A) $5, 8, 7, 12, 9, 20, 15$
- (B) $5, 8, 20, 12, 9, 7, 15$
- (C) $5, 7, 8, 12, 9, 20, 15$
- (D) $8, 5, 7, 12, 9, 20, 15$
- (E) $5, 8, 7, 12, 9, 15, 20$

> [!check]- Answer
> **(A)**. Move the last key $20$ to the root, then percolate it down through the smaller child each time: $20\leftrightarrow5$, then $20\leftrightarrow7$.

**5.** A priority queue is implemented as a **max-heap** whose breadth-first order is $12, 9, 7, 4, 6$. The keys $3$ and then $10$ are inserted. The new breadth-first order is:

- (A) $12, 10, 9, 4, 6, 3, 7$
- (B) $12, 9, 10, 4, 6, 7, 3$
- (C) $12, 9, 10, 4, 6, 3, 7$
- (D) $12, 9, 7, 4, 6, 3, 10$
- (E) $12, 10, 7, 4, 6, 3, 9$

> [!check]- Answer
> **(C)**. $3$ goes to position $6$ under $7$ and stays. $10$ goes to position $7$ under $7$, swaps with it, and stops below $12$.

**6.** A **deleteMax** is performed on the max-heap $50, 30, 45, 10, 25, 40, 20$. The result is:

- (A) $45, 30, 20, 10, 25, 40$
- (B) $45, 40, 30, 10, 25, 20$
- (C) $45, 30, 40, 10, 25, 20$
- (D) $40, 30, 45, 10, 25, 20$
- (E) $45, 25, 40, 10, 30, 20$

> [!check]- Answer
> **(C)**. $20$ moves to the root, swaps with the larger child $45$, then swaps with $40$.

**7.** The **minimum** and **maximum** number of elements in a heap of height $h$ are, respectively:

- (A) $2^h$ and $2^{h+1}-1$
- (B) $h$ and $2^h$
- (C) $2^{h-1}$ and $2^h-1$
- (D) $2^h+1$ and $2^{h+1}$
- (E) $1$ and $2^h$

> [!check]- Answer
> **(A)**. Levels $0..h-1$ are full ($2^h-1$ nodes) plus at least $1$ node on level $h$, giving $2^h$. With level $h$ full the total is $2^{h+1}-1$.

**8.** In the 1-indexed array of a heap with $40$ elements, the node at index $13$ has its parent at index $p$ and its children at indices $c_1, c_2$. Then:

- (A) $p=6,\ c_1=26,\ c_2=27$
- (B) $p=7,\ c_1=26,\ c_2=27$
- (C) $p=6,\ c_1=27,\ c_2=28$
- (D) $p=6,\ c_1=25,\ c_2=26$
- (E) $p=12,\ c_1=14,\ c_2=15$

> [!check]- Answer
> **(A)**. $\lfloor 13/2\rfloor = 6$, $2\cdot13=26$ and $2\cdot13+1=27$. Both children exist because $27 \le 40$.

**9.** When deleting an **arbitrary** key (not the root) from a min-heap by copying the last key into its place, you may need to:

- (A) percolate down only
- (B) percolate up only
- (C) percolate down, or percolate up, or do nothing
- (D) always percolate both up and down
- (E) rebuild the heap from scratch

> [!check]- Answer
> **(C)**. The copied last key may be smaller than the new parent (so it goes up), larger than a child (so it goes down), or fit exactly (nothing to do). The slides' algorithm shows the "down" case, but all three are possible.

**10.** Converting an array of $n$ keys into a binary heap takes $\Theta(n)$ time using:

- (A) the top-down algorithm only
- (B) the bottom-up algorithm only
- (C) both the top-down and bottom-up algorithms
- (D) neither; both are $\Theta(n\log n)$
- (E) heap sort

> [!check]- Answer
> **(B)**. Top-down is repeated insertion, which is $O(n\log n)$. Bottom-up percolates down from $\lfloor n/2\rfloor$ to $1$, which is $O(n)$.

**11.** In a **min-heap** of distinct keys, the **maximum** key is:

- (A) always at the root
- (B) always the last element of the array
- (C) always in one of the leaves
- (D) always a child of the root
- (E) anywhere in the heap

> [!check]- Answer
> **(C)**. A node with a child is smaller than that child, so the maximum cannot have children. It must be a leaf, though not necessarily the last one.

**12.** A **3-ary max-heap** is stored in a 0-indexed array: the root is at $a[0]$ and the children of $a[i]$ are at $a[3i+1], a[3i+2], a[3i+3]$. Which array is a valid 3-ary max-heap?

- (A) $30, 25, 28, 22, 20, 18, 26$
- (B) $30, 22, 28, 25, 20, 18, 21$
- (C) $30, 18, 28, 25, 26, 20, 22$
- (D) $18, 20, 22, 25, 26, 28, 30$
- (E) More than one of the above

> [!check]- Answer
> **(B)**. The root $30$ is at least $22, 28, 25$, and the children of $22$ ($a[4..6]=20,18,21$) are all $\le 22$. In (A), $26 > 25$. In (C), $26 > 18$. (D) is a min-heap.

**13.** The array $16, 4, 21, 9, 30, 12$ is first converted to a **max-heap** (bottom-up), giving $30, 16, 21, 9, 4, 12$. After **one** iteration of in-place heap sort (swap the root with the last element of the heap, shrink the heap by $1$, percolate down), the array is:

- (A) $21, 16, 12, 9, 4, 30$
- (B) $12, 16, 21, 9, 4, 30$
- (C) $21, 12, 16, 9, 4, 30$
- (D) $16, 21, 12, 9, 4, 30$
- (E) $21, 16, 9, 12, 4, 30$

> [!check]- Answer
> **(A)**. After the swap the array is $12,16,21,9,4\mid30$. Then $12$ swaps with the larger child $21$ and stops, since position $6$ is outside the heap.

**14.** To sort an array in **increasing** order *in place* using heap sort, you should use:

- (A) a min-heap, giving $O(n\log n)$
- (B) a max-heap, giving $O(n\log n)$
- (C) a max-heap, giving $O(n)$
- (D) a min-heap, giving $O(n^2)$
- (E) either heap, giving $O(\log n)$

> [!check]- Answer
> **(B)**. Each deleteMax places the largest remaining key in the freed last cell, so the array ends up increasing. There are $n$ deletions at $O(\log n)$ each.

**15.** In a min-heap, the priority of key $15$ is changed to $40$. In general this:

- (A) never requires percolation.
- (B) may require percolating $40$ down.
- (C) requires percolating $40$ up.
- (D) requires rebuilding the heap.
- (E) may require percolating $40$ up or down.

> [!check]- Answer
> **(B)**. The key increased, so the parent is still smaller, but a child may now be smaller than $40$. Decreasing a key would mean percolating up.

**16.** Which implementation of a minimum priority queue has the **worst** cost for *dequeue-min*?

- (A) Min-heap
- (B) AVL tree
- (C) Sorted list
- (D) Unsorted list
- (E) They are all $O(\log n)$

> [!check]- Answer
> **(D)**. An unsorted list needs an $O(n)$ scan to find the minimum. The min-heap and AVL tree are $O(\log n)$, and the sorted list is $O(1)$.
