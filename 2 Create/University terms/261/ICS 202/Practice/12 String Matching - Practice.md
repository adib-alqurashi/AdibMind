---
course: ICS 202
topic: String Matching (Brute Force & KMP)
slides: "[[252 ICS202-12-String Matching.pdf]]"
type: final-practice
---
# 12 — String Matching · Final MCQ Practice

> [!info] Conventions (from the slides)
> $\text{next}[0]=-1$, and $\text{next}[j]$ is the length of the **border** (longest proper prefix that is also a proper suffix) of $P[0..j-1]$. On a mismatch at $j>0$, shift the pattern $j-\text{next}[j]$ and resume at $\text{next}[j]$; at $j=0$, shift by $1$. **Every character comparison counts, including mismatches.** For non-overlapping brute force, jump by $m$ after a match.

---

**1.** The KMP next array of the pattern $CCCCADCC$ is:

- (A) $\langle 0,1,2,3,4,0,0,1\rangle$
- (B) $\langle -1,0,1,2,3,0,1,2\rangle$
- (C) $\langle -1,0,1,2,3,0,0,1\rangle$
- (D) $\langle -1,0,1,2,3,4,0,1\rangle$
- (E) None of the given answers

> [!check]- Answer
> **(C)**. $CCCC$ has border length $3$, giving $\text{next}[4]=3$. The prefixes ending in $A$ and $D$ have no border, so $\text{next}[5]=\text{next}[6]=0$. $CCCCADC$ has border $C$, so $\text{next}[7]=1$.

**2.** The KMP next array of the pattern $BBBABBBB$ is:

- (A) $\langle -1,0,1,2,0,1,2,3\rangle$
- (B) $\langle -1,0,1,2,3,0,1,2\rangle$
- (C) $\langle -1,0,1,2,0,3,2,1\rangle$
- (D) $\langle -1,0,1,2,3,3,3,4\rangle$
- (E) $\langle 0,1,2,0,1,2,3,3\rangle$

> [!check]- Answer
> **(A)**. $\text{next}[7]$ is the border of $BBBABBB$, which is $BBB$, so $3$.

**3.** The **border** of the pattern $BBBABBBB$ (the whole pattern) is:

- (A) $B$
- (B) $BB$
- (C) $BBB$
- (D) $BBBB$
- (E) All of the given answers

> [!check]- Answer
> **(C)**. $B$, $BB$ and $BBB$ are all prefixes that are also suffixes, but the **border** is the longest one. $BBBB$ is a suffix but not a prefix (the prefix of length 4 is $BBBA$).

**4.** The KMP next array of $ABCABDABC$ is:

- (A) $\langle -1,0,0,0,1,2,0,1,2\rangle$
- (B) $\langle -1,0,0,1,2,0,1,2,3\rangle$
- (C) $\langle -1,0,0,0,1,2,3,1,2\rangle$
- (D) $\langle 0,0,0,1,2,0,1,2,3\rangle$
- (E) $\langle -1,0,0,0,1,0,0,1,2\rangle$

> [!check]- Answer
> **(A)**. $ABCAB$ has border $AB$, so $\text{next}[5]=2$. $ABCABD$ has none, so $\text{next}[6]=0$. Then $A$ and $AB$ start matching again, giving $1,2$.

**5.** Using the **brute-force** algorithm, how many character comparisons are needed to find **all non-overlapping** occurrences of $abab$ in the text $abaababaab$?

- (A) $9$
- (B) $10$
- (C) $11$
- (D) $12$
- (E) $28$

> [!check]- Answer
> **(C)**. Shift 0 compares $a,b,a$ and mismatches on the 4th character (4). Shift 1 mismatches immediately (1). Shift 2 compares $a$ and mismatches on the 2nd (2). Shift 3 matches all 4 (4). After the match, jump to shift $7$; only $3$ characters remain, so stop. Total $11$.

**6.** Searching for $aba$ in $ababababa$ with brute force, the number of comparisons for **overlapping** and for **non-overlapping** matching are, respectively:

- (A) $15$ and $7$
- (B) $15$ and $15$
- (C) $21$ and $7$
- (D) $12$ and $6$
- (E) $15$ and $9$

> [!check]- Answer
> **(A)**. Overlapping: 7 shifts costing $3,1,3,1,3,1,3$, which is $15$ (matches at $0,2,4,6$). Non-overlapping: match at 0 (3), shift to 3 and mismatch (1), match at 4 (3), then only 2 characters remain. Total $7$.

**7.** The pattern $XYXYXYZ$ has next array $\langle -1,0,0,1,2,3,4\rangle$. Using **KMP**, how many character comparisons are needed to find the **first** match in the text $XYXYXYXYZQ$?

- (A) $7$
- (B) $9$
- (C) $10$
- (D) $15$
- (E) $13$

> [!check]- Answer
> **(C)**. $6$ matches, then a mismatch at $j=6$ ($7$ comparisons). Resume at $j=\text{next}[6]=4$ without moving back in the text. Then $X,Y,Z$ match ($3$ more). Total $10$, with the match at index $2$.

**8.** For the same text and pattern as Q7, **brute force** needs how many comparisons to find the first match?

- (A) $10$
- (B) $13$
- (C) $14$
- (D) $15$
- (E) $21$

> [!check]- Answer
> **(D)**. Shift 0 costs $7$ (mismatch at $Z$), shift 1 costs $1$, and shift 2 matches all $7$. Total $15$. Compare this with KMP's $10$.

**9.** The pattern $ABABCAB$ has next array $\langle -1,0,0,1,2,0,1\rangle$. Using KMP on the text $ABABABCABABD$, how many comparisons until the first match is found?

- (A) $10$
- (B) $11$
- (C) $12$
- (D) $9$
- (E) $14$

> [!check]- Answer
> **(A)**. $ABAB$ matches ($4$), then $A\ne C$ at $j=4$ ($5$). Resume at $j=\text{next}[4]=2$ with the same text index. Then $A,B,C,A,B$ match ($5$ more), for a total of $10$ (match at index $2$).

**10.** In KMP, a mismatch occurs at pattern index $j=6$ where $\text{next}[6]=2$. The pattern is shifted to the right by:

- (A) $2$ positions, and the search resumes at pattern index $0$.
- (B) $4$ positions, and the search resumes at pattern index $2$.
- (C) $6$ positions, and the search resumes at pattern index $0$.
- (D) $1$ position, and the search resumes at pattern index $2$.
- (E) $4$ positions, and the search resumes at pattern index $0$.

> [!check]- Answer
> **(B)**. The shift is $j-\text{next}[j]=6-2=4$, and the search resumes at $\max\{0,\text{next}[j]\}=2$.

**11.** For a text of length $n$ and a pattern of length $m<n$, the **worst-case** costs of brute force and of KMP's search phase are, respectively:

- (A) $\Theta(n\log m)$ and $\Theta(n)$
- (B) $\Theta(nm)$ and $\Theta(n)$
- (C) $\Theta(n^2)$ and $\Theta(m)$
- (D) $\Theta(nm)$ and $\Theta(m\log n)$
- (E) $\Theta(n+m)$ and $\Theta(n)$

> [!check]- Answer
> **(B)**. Brute force does $(n-m+1)\cdot m$ comparisons in the worst case. KMP never moves backward in the text, so its search is $\Theta(n)$, and building the next array adds $\Theta(m)$.

**12.** Brute force searches for $AAAB$ in the text $AAAAAAAAAA$ (10 A's). The number of comparisons is:

- (A) $10$
- (B) $28$
- (C) $40$
- (D) $7$
- (E) $24$

> [!check]- Answer
> **(B)**. This is the worst case: $(n-m+1)\cdot m=7\cdot4=28$, since each shift fails on the 4th character.

**13.** The **best-case** number of comparisons for brute force (text length $n$, pattern length $m$) is:

- (A) $m$
- (B) $n$
- (C) $n-m+1$
- (D) $nm$
- (E) $\log n$

> [!check]- Answer
> **(C)**. Every shift fails on its first character.

**14.** Which statement about KMP is **true**?

- (A) KMP resets the text index $i$ back after every mismatch.
- (B) The next array depends on both the text and the pattern.
- (C) The text index $i$ never moves backward, and the next array depends only on the pattern.
- (D) KMP cannot find overlapping occurrences.
- (E) KMP is always slower than brute force on short patterns.

> [!check]- Answer
> **(C)**. Preprocessing uses only $P$. KMP can find both overlapping and non-overlapping occurrences.

**15.** How many **proper** prefixes, including the empty string $\lambda$, does the string $STATES$ have?

- (A) $5$
- (B) $6$
- (C) $7$
- (D) $4$
- (E) $12$

> [!check]- Answer
> **(B)**. They are $\lambda, S, ST, STA, STAT, STATE$. A proper prefix excludes the whole string.

**16.** The KMP next array of $AABAACAAB$ is:

- (A) $\langle -1,0,1,0,1,2,0,1,2\rangle$
- (B) $\langle -1,0,1,0,1,2,3,1,2\rangle$
- (C) $\langle -1,0,1,0,1,2,0,1,3\rangle$
- (D) $\langle -1,0,1,1,2,3,0,1,2\rangle$
- (E) $\langle 0,1,0,1,2,0,1,2,3\rangle$

> [!check]- Answer
> **(A)**. $AABAA$ has border $AA$, so $\text{next}[5]=2$. After the $C$ the value resets to $0$, then $A$ gives $1$ and $AA$ gives $2$.
