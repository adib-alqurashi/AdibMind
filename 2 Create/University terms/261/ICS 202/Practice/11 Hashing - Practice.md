---
course: ICS 202
topic: Hashing
slides: "[[252 ICS202-11-Hashing.pdf]]"
type: final-practice
---
# 11 — Hashing · Final MCQ Practice

> [!info] Conventions (from the slides)
> Probe sequence: $h_i(k)=[h(k)+c(i)]\bmod n$, with linear $c(i)=i$, quadratic $c(i)=\pm i^2$ ($+i^2$ tried before $-i^2$), and double $c(i)=i\cdot h_p(k)$. Cell states: **E**mpty, **O**ccupied, **D**eleted (lazy deletion). A search continues past **D** and stops at **E**. Load factor $\lambda=\dfrac{\#\text{keys}}{\text{table size}}$.

---

**1.** The keys $15, 22, 8, 29, 4, 11, 36, 18, 25$ are inserted into a **separate chaining** table of size $7$ with $h(k)=k \bmod 7$. The load factor and the length of the longest chain are:

- (A) $\lambda=1$, longest chain $4$
- (B) $\lambda=\tfrac{9}{7}$, longest chain $4$
- (C) $\lambda=\tfrac{7}{9}$, longest chain $5$
- (D) $\lambda=\tfrac{9}{7}$, longest chain $5$
- (E) $\lambda=2$, longest chain $5$

> [!check]- Answer
> **(D)**. $15,22,8,29,36\to1$ (5 keys) and $4,11,18,25\to4$ (4 keys). $\lambda=9/7>1$, which is possible only with chaining.

**2.** Which collision resolution technique can produce a hash table with load factor **greater than 1**?

- (A) Linear probing
- (B) Quadratic probing
- (C) Double hashing
- (D) Separate chaining
- (E) None of them

> [!check]- Answer
> **(D)**. Open addressing stores all keys inside the table, so $\lambda\le1$ there.

**3.** In a table of size $13$ using **linear probing** with $h(k)=k\bmod 13$, the keys $27, 40, 14, 53, 66, 19, 32$ are inserted in order. Then $14$ is deleted. How many cells are inspected by `find(79)`?

- (A) $1$
- (B) $5$
- (C) $8$
- (D) $7$
- (E) $13$

> [!check]- Answer
> **(C)**. $27,40,14,53,66$ all hash to $1$ and fill cells $1..5$. $19\to6$, and $32\to6$ goes on to $7$. $79\to1$, so the search probes $1,2,3(\text{D, continue}),4,5,6,7,8(\text{E})$, which is 8 cells, and the search fails.

**4.** For the table in Q3 (after deleting $14$), how many cells does `find(66)` inspect?

- (A) $1$
- (B) $4$
- (C) $3$
- (D) $5$
- (E) $6$

> [!check]- Answer
> **(D)**. It probes cells $1,2,3(\text{D}),4,5$ and finds $66$ at cell $5$. This is why deleted cells are marked **D** and not **E**: an **E** at cell $3$ would stop the search early.

**5.** Consider this table of size $11$ with $h(k)=k\bmod 11$ and **quadratic probing** $c(i)=\pm i^2$:

| Index | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| State | E | E | O | O | O | E | O | O | E | E | O |
| Key |  |  | 13 | 25 | 37 |  | 6 | 18 |  |  | 32 |

Key $47$ is inserted. How many indexes are inspected, and where does $47$ go?

- (A) $3$ inspected, index $2$
- (B) $5$ inspected, index $5$
- (C) $6$ inspected, index $1$
- (D) $6$ inspected, index $5$
- (E) $7$ inspected, index $8$

> [!check]- Answer
> **(C)**. $h(47)=3$. The probes are $3$ (O), $3+1=4$ (O), $3-1=2$ (O), $3+4=7$ (O), $3-4\equiv10$ (O), $3+9\equiv1$ (E), so $47$ goes to index $1$.

**6.** The keys $24, 13, 35, 46, 57$ are inserted in order into an empty table of size $11$ using **quadratic probing** $c(i)=\pm i^2$ and $h(k)=k \bmod 11$. Where is $57$ placed?

- (A) $6$
- (B) $9$
- (C) $3$
- (D) $5$
- (E) $10$

> [!check]- Answer
> **(B)**. All five keys hash to $2$. They take $2$, then $2+1=3$, then $2-1=1$, then $2+4=6$. For $57$ the next probe is $2-4\equiv9$.

**7.** In Q6 all five keys follow **exactly the same** probe sequence. This phenomenon is called:

- (A) primary clustering, and double hashing does not fix it.
- (B) secondary clustering, and double hashing eliminates it.
- (C) primary clustering, and quadratic probing eliminates it.
- (D) secondary clustering, and linear probing eliminates it.
- (E) rehashing.

> [!check]- Answer
> **(B)**. Synonyms in quadratic probing share one probe sequence. Double hashing gives synonyms different step sizes $h_p(k)$.

**8.** Using **double hashing** on an empty table of size $13$ with $h(k)=k\bmod 13$ and $h_p(k)=1+(k\bmod 12)$, the keys $20, 33, 46, 59, 7$ are inserted in order. Where is $7$ placed?

- (A) $8$
- (B) $3$
- (C) $9$
- (D) $0$
- (E) $2$

> [!check]- Answer
> **(E)**. Every key has $h=7$. $20\to7$. $33$ has $h_p=10$, so it goes to $(7+10)\bmod13=4$. $46$ has $h_p=11$ and goes to $5$. $59$ has $h_p=12$ and goes to $6$. $7$ has $h_p=8$ and goes to $(7+8)\bmod 13=2$.

**9.** Which statement is **false**?

- (A) Linear probing suffers from primary clustering.
- (B) Quadratic probing eliminates primary clustering but may cause secondary clustering.
- (C) For quadratic probing, the table size should ideally be a prime of the form $4j+3$.
- (D) For double hashing, $h_p(k)$ and the table size must be relatively prime.
- (E) In open addressing, a deleted key's cell is set back to **Empty**.

> [!check]- Answer
> **(E)**. It must be marked **Deleted**. Otherwise later searches that should pass through that cell would stop early.

**10.** An open-addressing table of size $11$ holds $8$ keys. Following the slides' rehashing rule, the new table size should be:

- (A) $22$
- (B) $23$
- (C) $13$
- (D) $19$
- (E) $11$

> [!check]- Answer
> **(B)**. $\lambda=8/11\approx0.73>0.7$, which is undesirable. Double the size and take the next prime: $2\cdot11=22\to23$.

**11.** Consider a size-$17$ open-addressing table with states:

| 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | 16 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| D | O | D | D | E | D | O | D | D | D | E | D | D | O | D | D | E |

The most appropriate action to improve search efficiency is:

- (A) Rehash the keys without changing the table size.
- (B) Rehash the keys into a table of size $34$.
- (C) Rehash the keys into a table of size $37$.
- (D) Rehash the keys into a table of size $19$.
- (E) No action; the load factor is low.

> [!check]- Answer
> **(A)**. Only $3$ cells are occupied ($\lambda\approx0.18$), but the many **D** cells lengthen every search. Rehashing at the same size clears them.

**12.** Consider the two statements:
- $S_1$: With separate chaining and a hash function that spreads keys evenly, searching becomes very bad as soon as $\lambda$ approaches $1$.
- $S_2$: With open addressing, the load factor cannot exceed $1$.

Then:

- (A) $S_1$ is true and $S_2$ is false.
- (B) Both are true.
- (C) Both are false.
- (D) $S_1$ is false and $S_2$ is true.
- (E) $S_2$ is true only for linear probing.

> [!check]- Answer
> **(D)**. With $\lambda\approx1$ and an even spread, chains have about one key each, so search is still fast.

**13.** Which statement about **separate chaining** is **incorrect**?

- (A) The table size has to be a prime number.
- (B) Insertion at the head of a chain costs $\Theta(1)$.
- (C) Synonyms are stored in the same linked list.
- (D) Extra space is needed for the list references.
- (E) Deletion only touches the list at the key's hash address.

> [!check]- Answer
> **(A)**. A prime size helps the key distribution, but chaining works with any size. The "must be prime" rule matters for open addressing (quadratic probing and double hashing).

**14.** With $h(s)=\left(\sum \text{ASCII}(c)\right) \bmod 13$ and ASCII $a=97,\ b=98,\ d=100$, the value $h(\text{"dab"})$ is:

- (A) $8$
- (B) $9$
- (C) $0$
- (D) $11$
- (E) $4$

> [!check]- Answer
> **(B)**. $100+97+98=295$ and $295-286=9$. Note that "bad" and "dab" would collide, since anagrams always collide under a plain sum.

**15.** Using **folding** (split into 2-digit parts and add) followed by $\bmod 10$, the key $482917$ hashes to:

- (A) $2$
- (B) $7$
- (C) $4$
- (D) $9$
- (E) $1$

> [!check]- Answer
> **(C)**. $48+29+17=94$ and $94\bmod10=4$.

**16.** Which is a **disadvantage** of open addressing compared with separate chaining?

- (A) It needs an extra data structure outside the table.
- (B) Its performance degrades severely as the table fills, and it needs a three-state flag per cell.
- (C) It cannot use the division hash function.
- (D) It allows $\lambda>1$.
- (E) It uses more memory per key.

> [!check]- Answer
> **(B)**. The slides also list that keys must be distinct and that performance depends on choosing a proper table size.

**17.** For **open addressing**, the expected search time depends mainly on:

- (A) the table size only.
- (B) the number of keys only.
- (C) the load factor, not the table size itself.
- (D) the length of the keys.
- (E) whether the keys are integers.

> [!check]- Answer
> **(C)**. The slides recommend keeping $\lambda$ around $0.6$–$0.7$.
