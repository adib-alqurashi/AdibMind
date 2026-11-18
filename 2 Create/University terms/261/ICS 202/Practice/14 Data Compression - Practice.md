---
course: ICS 202
topic: Data Compression (Static Huffman, LZ78)
slides: "[[252 ICS202-14-DataCompression.pdf]]"
type: final-practice
---
# 14 — Data Compression · Final MCQ Practice

> [!info] Conventions (from the slides)
> **Huffman:** dequeue the two smallest trees $t_1,t_2$ and make $t_1$ the left child and $t_2$ the right child; left $=0$, right $=1$. **Tree transmission:** postorder, where a leaf is written as `1` followed by the 8-bit character, an internal node as `0`, plus one final `0`. On recovery, the **first popped node becomes the right child**. **Compression ratio** $=\dfrac{\text{bits before}}{\text{bits after}}$, with 8-bit ASCII before. **LZ78 bits:** the $k$-th codeword's index uses as many bits as $k-1$ needs (minimum 1), plus $8$ bits for the character (none if the character is empty).

---

**1.** A message contains only these characters, with the given frequencies:

| char | a | b | c | d | e | f |
|---|---|---|---|---|---|---|
| freq | 20 | 6 | 9 | 15 | 30 | 4 |

The number of bits in the **static Huffman** encoding of the message (excluding the tree) is:

- (A) $168$
- (B) $197$
- (C) $210$
- (D) $252$
- (E) $672$

> [!check]- Answer
> **(B)**. The merges are $4+6=10$, $9+10=19$, $15+19=34$, $20+30=50$, $34+50=84$. Codeword lengths: $e,a,d\to2$, $c\to3$, $b,f\to4$. Total $30\cdot2+20\cdot2+15\cdot2+9\cdot3+6\cdot4+4\cdot4=197$.

**2.** For Q1, the compression ratio (with 8-bit ASCII before compression, tree excluded) is approximately:

- (A) $2.13$
- (B) $2.67$
- (C) $3.41$
- (D) $4.00$
- (E) $0.29$

> [!check]- Answer
> **(C)**. $84\cdot8=672$ bits before, and $672/197\approx3.41$.

**3.** In Q1, the codeword **length** of character $b$ is:

- (A) $2$
- (B) $3$
- (C) $5$
- (D) $4$
- (E) $1$

> [!check]- Answer
> **(D)**. $b$ ($6$) and $f$ ($4$) are merged first, and that subtree ends up $4$ levels deep.

**4.** Using static Huffman coding on the message $mississippi$, the total number of encoded bits (tree excluded) is:

- (A) $21$
- (B) $22$
- (C) $24$
- (D) $11$
- (E) $33$

> [!check]- Answer
> **(A)**. The frequencies are $i{:}4,\ s{:}4,\ p{:}2,\ m{:}1$. The merges are $1+2=3$, $3+4=7$, $4+7=11$, giving lengths $1,2,3,3$. Total $4\cdot1+4\cdot2+2\cdot3+1\cdot3=21$, whichever of $i/s$ gets the short code.

**5.** Which set of codewords **cannot** be the result of the static Huffman algorithm?

- (A) $a{:}00,\ b{:}01,\ c{:}100,\ d{:}101,\ e{:}11$
- (B) $a{:}0,\ b{:}10,\ c{:}110,\ d{:}1110,\ e{:}1111$
- (C) $a{:}00,\ b{:}01,\ c{:}10,\ d{:}110$
- (D) $a{:}11,\ b{:}10,\ c{:}01,\ d{:}001,\ e{:}000$
- (E) All of them can

> [!check]- Answer
> **(C)**. Node $11$ would have only one child ($110$). A Huffman tree is always **full** (every internal node has 2 children), and $d$ could simply be $11$.

**6.** The transmitted Huffman tree is `1p1q01r1s1t0000` (characters shown instead of their ASCII codes). Which characters have the **longest** codewords?

- (A) $p$ and $q$
- (B) $r$ only
- (C) $s$ and $t$
- (D) $t$ only
- (E) All codewords have the same length

> [!check]- Answer
> **(C)**. Rebuilding with a stack gives $(p,q)$, then $(s,t)$, then $(r,(s,t))$, then the root $((p,q),(r,(s,t)))$. The codes are $p{=}00,\ q{=}01,\ r{=}10,\ s{=}110,\ t{=}111$.

**7.** How many bits are needed to transmit the tree in Q6 (8-bit ASCII per character)?

- (A) $40$
- (B) $45$
- (C) $49$
- (D) $50$
- (E) $55$

> [!check]- Answer
> **(D)**. $5$ characters $\times 8=40$, plus five `1`s, four internal `0`s and the end `0`, which is $10$ bits. Total $50$. (Check with the slides: $7$ chars gives $7\cdot8+14=70$.)

**8.** In static Huffman coding, the **prefix property**:

- (A) ensures that decoding is unambiguous.
- (B) means that no two codewords share a common prefix.
- (C) guarantees the minimum total number of bits.
- (D) gives frequent characters longer codewords.
- (E) More than one of the given answers is correct.

> [!check]- Answer
> **(A)**. It means no codeword is a prefix of **another** codeword. Codewords may still share prefixes: $110$ and $111$ share $11$.

**9.** A Huffman coding tree built for a message with $9$ **distinct** characters has how many internal nodes and how many total nodes?

- (A) $9$ and $18$
- (B) $8$ and $17$
- (C) $8$ and $16$
- (D) $10$ and $19$
- (E) It depends on the frequencies.

> [!check]- Answer
> **(B)**. The tree is full, so $n$ leaves give $n-1$ internal nodes and $2n-1$ nodes in total. Each merge creates one internal node, and there are $n-1$ merges.

**10.** The LZ78 encoding of $ABBABBBAABAB$ is:

- (A) $(0,A)(0,B)(2,A)(2,B)(3,A)(3,B)$
- (B) $(0,A)(0,B)(2,B)(1,B)(3,A)(3,B)$
- (C) $(0,A)(0,B)(1,B)(2,B)(3,A)(1,B)$
- (D) $(0,A)(0,B)(2,A)(2,B)(3,A)(4,)$
- (E) $(0,A)(0,B)(2,A)(2,B)(4,A)(3,B)$

> [!check]- Answer
> **(A)**. The dictionary builds as $1{=}A$, $2{=}B$, $3{=}BA$, $4{=}BB$, $5{=}BAA$, $6{=}BAB$.

**11.** Using the slides' bit-count rule, the compression ratio for Q10 is:

- (A) $\dfrac{12\times8}{6\times8+9}$
- (B) $\dfrac{12\times8}{6\times8+12}$
- (C) $\dfrac{12\times8}{6\times8+6}$
- (D) $\dfrac{6\times8}{12\times8}$
- (E) $\dfrac{12\times8}{6\times8+18}$

> [!check]- Answer
> **(B)**. The index bits for codewords $k=1..6$ are $1,1,2,2,3,3$, which sum to $12$, and there are $6$ characters $\times8$. The result is $96/60=1.6$.

**12.** The LZ78 codes $(0,K)(0,L)(1,L)(3,K)(2,K)(4,)$ decode to a message of length:

- (A) $10$
- (B) $11$
- (C) $13$
- (D) $12$
- (E) There is a mistake in the encoding.

> [!check]- Answer
> **(D)**. They decode to $K, L, KL, KLK, LK, KLK$, which is $1+1+2+3+2+3=12$ characters. A final pair $(i,)$ with an empty character is valid when the message ends on an existing dictionary entry.

**13.** In Q12, the number of bits after compression (slides' rule) is:

- (A) $52$
- (B) $53$
- (C) $60$
- (D) $48$
- (E) $57$

> [!check]- Answer
> **(A)**. $(1+8)+(1+8)+(2+8)+(2+8)+(3+8)+3=52$. The last pair has no character.

**14.** The LZ78 encoding of $AAABABBBBAB$ ends with which codeword, and how many codewords are there?

- (A) $(3,B)$; $6$ codewords
- (B) $(3,)$; $7$ codewords
- (C) $(4,)$; $7$ codewords
- (D) $(3,A)$; $6$ codewords
- (E) $(1,)$; $8$ codewords

> [!check]- Answer
> **(B)**. The codes are $(0,A)(1,A)(0,B)(1,B)(3,B)(3,A)(3,)$. The final $B$ is already entry $3$.

**15.** The dictionary used in LZ78 is most suitably implemented as:

- (A) an AVL tree
- (B) a min-heap
- (C) a B-tree
- (D) a stack
- (E) a hash table

> [!check]- Answer
> **(E)**. The slides note this explicitly. It gives fast "is this pattern in the dictionary?" checks.

**16.** Which statement is **correct**?

- (A) In LZ78, the dictionary does not need to be transmitted to the receiver.
- (B) LZ78 is a 2-pass compression algorithm.
- (C) LZ78 is a string-matching algorithm.
- (D) In LZ78 each character always maps to a fixed-length binary code.
- (E) Static Huffman coding needs only one pass over the message.

> [!check]- Answer
> **(A)**. LZ78 is adaptive: the receiver rebuilds the dictionary while decoding. Static Huffman is the **two-pass** method (count frequencies, then encode), and its tree must be sent.

**17.** Which pairing is **correct**?

- (A) Lossless compression: JPEG; lossy compression: ZIP
- (B) Lossless compression: Huffman and LZ78; lossy compression: JPEG and MP3
- (C) Lossless compression always gives a higher compression ratio than lossy compression
- (D) Lossy compression recovers the original data exactly
- (E) Huffman coding is lossy

> [!check]- Answer
> **(B)**. Lossy methods remove less-important data and reach **higher** ratios. Lossless methods recover the data exactly.

**18.** Static Huffman coding is an example of a:

- (A) dynamic-programming algorithm, and its tree is unique.
- (B) greedy algorithm, and its tree is not necessarily unique.
- (C) divide-and-conquer algorithm.
- (D) greedy algorithm whose tree is always unique.
- (E) backtracking algorithm.

> [!check]- Answer
> **(B)**. It always merges the two smallest trees. Ties and the choice of 0/1 per edge can give different trees with the same total cost.
