# 1.1 Vectors

## Course Route

Vectors & geometry → Matrices → Systems of linear equations → Column space, rank, projections → Least squares & linear regression

- Each module ends with 6 exercises → do them
- Module 1 goal: similarities, distances, simple predictions

## What Is a Vector

- **Vector** = ordered list of numbers → **entries / components**
- Written as a column $\begin{bmatrix} x_1 \ \vdots \ x_n \end{bmatrix}$ or a row $(x_1, \dots, x_n)$
- **Size = dimension** = number of entries → $\mathbf{x} \in \mathbb{R}^n$
- Data point = vector → house $\mathbf{x} = \begin{bmatrix} 120 \ 3 \end{bmatrix} \in \mathbb{R}^2$
    - $x_1$ = area (m²), $x_2$ = bedrooms

## Notation

- **Bold** letter = vector: $\mathbf{x}, \mathbf{a}, \mathbf{u}$
- $u_i$ = the $i$-th entry → indices $1 \dots n$ (Python: $0 \dots n-1$)
- $\mathbf{u}_i$ (bold) = the $i$-th vector in a list $\mathbf{u}_1, \dots, \mathbf{u}_k$

## Special Vectors

|Vector|Notation|Example in $\mathbb{R}^3$|
|---|---|---|
|Zero|$\mathbf{0}$ or $\mathbf{0}_n$|$(0, 0, 0)$|
|Ones|$\mathbf{1}$ or $\mathbf{1}_n$|$(1, 1, 1)$|
|Standard unit|$\mathbf{e}_i$ → 1 at position $i$, 0 elsewhere|$\mathbf{e}_1 = (1,0,0)$, $\mathbf{e}_2 = (0,1,0)$, $\mathbf{e}_3 = (0,0,1)$|

- $\mathbf{e}_1, \mathbf{e}_2, \mathbf{e}_3$ = the old $\hat{i}, \hat{j}, \hat{k}$ axes

## Addition

- Same size only → add entry by entry: $\mathbf{u} + \mathbf{v} = (u_1 + v_1, \dots, u_n + v_n)$
- Geometry → diagonal of the parallelogram formed by $\mathbf{u}$ and $\mathbf{v}$

## Scaling

- $c\mathbf{u} = (cu_1, \dots, cu_n)$, with $c \in \mathbb{R}$

|Scalar|Effect|
|---|---|
|$c > 1$|Longer, same direction|
|$0 < c < 1$|Shorter, same direction|
|$c < 0$|Flips direction ($-\mathbf{u}$: same length, opposite way)|
|$c = 0$|Zero vector|

- **Subtraction** = scale, then add → $\mathbf{u} - \mathbf{v} = \mathbf{u} + (-1)\mathbf{v}$

## Linear Combinations

- Scale vectors, then add them: $c_1\mathbf{u}_1 + c_2\mathbf{u}_2 + \dots + c_m\mathbf{u}_m$
- $c_i$ = **coefficients**
- Example: $2\mathbf{u} + 3\mathbf{v}$ → diagonal of the parallelogram of $2\mathbf{u}$ and $3\mathbf{v}$

## Span

- **Span** = set of all linear combinations → $\text{span}(\mathbf{u}, \mathbf{v}) = { c\mathbf{u} + d\mathbf{v} : c, d \in \mathbb{R} }$

|Nonzero vectors|All combinations give|
|---|---|
|One: $c\mathbf{u}$|A **line** through the origin|
|Two: $c\mathbf{u} + d\mathbf{v}$|A **plane** through the origin|

- Always through the origin → $c = d = 0$ gives $\mathbf{0}$

> [!warning] Two vectors → plane only if they're not parallel If $\mathbf{v}$ is a multiple of $\mathbf{u}$, the span is still just a line.

## Example: RGB Colors

- $\mathbf{r} = (1, 0, 0)$, $\mathbf{g} = (0, 1, 0)$, $\mathbf{b} = (0, 0, 1)$
- Yellow → $\mathbf{r} + \mathbf{g} = (1, 1, 0)$
- Gray → $0.5\mathbf{r} + 0.5\mathbf{g} + 0.5\mathbf{b} = (0.5, 0.5, 0.5)$
- Every color = a linear combination of $\mathbf{r}, \mathbf{g}, \mathbf{b}$

## Quick Recall

- Dimension of $(3, -1, 4, 0)$? → **4**
- $\mathbf{e}_2$ in $\mathbb{R}^3$? → $(0, 1, 0)$
- $2(1, 3) + 3(2, -1)$? → $(2, 6) + (6, -3) = (8, 3)$
- $\mathbf{u} - \mathbf{v}$ as a combination? → $\mathbf{u} + (-1)\mathbf{v}$
- What does $c < 0$ do? → **flips direction**
- Span of one nonzero vector? → **line** through the origin
- Span of two non-parallel vectors? → **plane** through the origin
- Why does a span always contain $\mathbf{0}$? → all coefficients $= 0$
- Yellow in RGB? → $(1, 1, 0)$

Source: [1.1 Vectors video](https://youtu.be/FeCxx5-q94Y)

# 1.2 Dot Product and Distance

## Dot Product

- Multiply matching entries, then add → **one number**
- $\mathbf{u} \cdot \mathbf{v} = \mathbf{u}^T\mathbf{v} = u_1v_1 + u_2v_2 + \dots + u_nv_n$
- $\mathbf{u}^T$ = **transpose** → column becomes row (and row becomes column)
- Example: $(1, 2) \cdot (3, -1) = 1 \cdot 3 + 2 \cdot (-1) = 1$
- Both vectors must have the **same size**

## Prediction as a Weighted Sum

- $\hat{y} = \mathbf{w}^T\mathbf{x} + b$
    - $\mathbf{x}$ = features, $\mathbf{w}$ = weights, $b$ = **bias**
    - Each feature × its weight, then add, then add the bias
- Example: $\mathbf{x} = (4, 3)$, $\mathbf{w} = (2, -1)$ → $\mathbf{w}^T\mathbf{x} = 8 - 3 = 5$ → $\hat{y} = 5 + b$

## Norm (Length)

- $\lVert \mathbf{u} \rVert = \sqrt{u_1^2 + \dots + u_n^2} = \sqrt{\mathbf{u} \cdot \mathbf{u}}$ → **Euclidean norm**
- **Unit vector** → norm $= 1$
- $\lVert c\mathbf{u} \rVert = \lvert c \rvert , \lVert \mathbf{u} \rVert$ → e.g. $\lVert -2\mathbf{u} \rVert = 2\lVert \mathbf{u} \rVert$
- $\lVert \mathbf{u} \rVert \ge 0$, and $= 0$ only if $\mathbf{u} = \mathbf{0}$
- **Triangle inequality**: $\lVert \mathbf{u} + \mathbf{v} \rVert \le \lVert \mathbf{u} \rVert + \lVert \mathbf{v} \rVert$ → going straight is never longer than a detour

## Distance

- $\text{dist}(\mathbf{u}, \mathbf{v}) = \lVert \mathbf{u} - \mathbf{v} \rVert$ (order doesn't matter)
- Example: $\mathbf{u} = (1, 2)$, $\mathbf{v} = (4, 6)$ → $\mathbf{v} - \mathbf{u} = (3, 4)$ → $\sqrt{9 + 16} = 5$

## Angle & Cosine Similarity

- $\cos\theta = \dfrac{\mathbf{u}^T\mathbf{v}}{\lVert \mathbf{u} \rVert , \lVert \mathbf{v} \rVert}$ → same as $\mathbf{u}^T\mathbf{v} = \lVert \mathbf{u} \rVert , \lVert \mathbf{v} \rVert \cos\theta$
- Range $-1$ to $1$:

|$\cos\theta$|Angle|Meaning|
|---|---|---|
|$1$|$0°$|Same direction (length can differ)|
|$0$|$90°$|**Orthogonal** (perpendicular)|
|$-1$|$180°$|Opposite directions|

- Undefined if either vector is $\mathbf{0}$

## Normalization

- $\hat{\mathbf{x}} = \dfrac{\mathbf{x}}{\lVert \mathbf{x} \rVert}$ ($\mathbf{x} \ne \mathbf{0}$) → keeps the direction, removes the length
- Example: $(3, 4)$ → norm $5$ → $(0.6, 0.8)$, norm $1$

## Example: Nearest Direction

- Query $\mathbf{q} = (1, 1)$; candidates $\mathbf{a} = (2, 0)$, $\mathbf{b} = (3, 3)$
- $\cos(\mathbf{q}, \mathbf{a}) = \dfrac{2}{\sqrt{2} \cdot 2} = \dfrac{1}{\sqrt{2}} \approx 0.71$
- $\cos(\mathbf{q}, \mathbf{b}) = \dfrac{6}{\sqrt{2} \cdot \sqrt{18}} = 1$ → $\mathbf{b}$ points the same way as $\mathbf{q}$

> The slide says 0.77; the correct value is $\frac{1}{\sqrt{2}} \approx 0.71$.

## Distance vs Similarity

- **Distance** → how close are the points? (location)
- **Cosine similarity** → how aligned are the directions? (direction)
- $(1, 1)$ and $(10, 10)$ → cosine $= 1$, but distance $= 9\sqrt{2} \approx 12.7$

## Quick Recall

- $(1, 2) \cdot (3, -1)$? → **1**
- What does $\mathbf{u}^T$ do? → turns a column into a row
- $\lVert (3, 4) \rVert$? → **5**
- $\lVert -3\mathbf{u} \rVert$? → $3\lVert \mathbf{u} \rVert$
- Distance formula? → $\lVert \mathbf{u} - \mathbf{v} \rVert$
- $\cos\theta = 0$ means? → **orthogonal**
- Normalize $(3, 4)$? → $(0.6, 0.8)$
- Same direction but far apart → which measure says "similar"? → **cosine similarity**

Source: [1.2 video](https://youtu.be/d8QfPSsedRY)

# 2.1 Matrices and Matrix Operations

## What Is a Matrix

- Rectangular array of numbers → **entries**
- **Size** $m \times n$ → $m$ rows, $n$ columns (rows first)
- $a_{ij}$ → row $i$, column $j$ (math starts at 1, Python at 0)

$$A = \begin{bmatrix} a_{11} & a_{12} & \cdots & a_{1n} \ \vdots & \vdots & \ddots & \vdots \ a_{m1} & a_{m2} & \cdots & a_{mn} \end{bmatrix}$$

## Shapes

|Shape|Condition|Example size|
|---|---|---|
|Tall|$m > n$ (more rows)|$4 \times 2$|
|Wide|$m < n$ (more columns)|$2 \times 3$|
|Square|$m = n$|$3 \times 3$|

## Matrices in Real Life

- Grayscale image → each pixel is a number from $0$ (black) to $1$ (white)
- Price table → $p_{ij}$ = price vendor $j$ charges for good $i$

## Special Matrices

|Matrix|Definition|
|---|---|
|Zero $0$|All entries $0$ (any size)|
|Identity $I$|Square, $1$ on the diagonal, $0$ elsewhere|
|Sparse|Most entries are $0$ → stored efficiently|
|Diagonal|Square, $a_{ij} = 0$ when $i \ne j$|
|Lower triangular|Square, $a_{ij} = 0$ when $i < j$ (zeros above the diagonal)|
|Upper triangular|Square, $a_{ij} = 0$ when $i > j$ (zeros below the diagonal)|

- **Main diagonal** → $a_{11}, a_{22}, \dots, a_{nn}$
- Lower + upper triangular at the same time → **diagonal**

## Transpose

- $A^T$ → rows become columns, columns become rows → $m \times n$ becomes $n \times m$
- Example: $A = \begin{bmatrix} 0 & 3 \ 6 & 1 \ 2 & -1 \end{bmatrix}$ ($3 \times 2$) → $A^T = \begin{bmatrix} 0 & 6 & 2 \ 3 & 1 & -1 \end{bmatrix}$ ($2 \times 3$)
- Row vector → transpose → column vector (and vice versa)
- **Symmetric** → $A^T = A$ → must be square, $a_{ij} = a_{ji}$ (mirror across the diagonal)

## Addition & Scalar Multiplication

- $A + B$ → **same size only**, add matching entries
- $kA$ → multiply every entry by $k$
- Properties: $A + B = B + A$ · $k(A + B) = kA + kB$ · $(A + B)^T = A^T + B^T$

## Example

- $A = \begin{bmatrix} -1 & 0 & 0 \ 2 & 3 & 0 \end{bmatrix}$, $B = \begin{bmatrix} 1 & -1 & 1 \ 3 & 1 & 0 \end{bmatrix}$, $C$ is $2 \times 2$
- $A + B = \begin{bmatrix} 0 & -1 & 1 \ 5 & 4 & 0 \end{bmatrix}$
- $-2A + B = \begin{bmatrix} 2 & 0 & 0 \ -4 & -6 & 0 \end{bmatrix} + B = \begin{bmatrix} 3 & -1 & 1 \ -1 & -5 & 0 \end{bmatrix}$
- $A + C$ → ❌ different sizes

## Quick Recall

- Size of a matrix with 3 rows, 4 columns? → $3 \times 4$
- $a_{23}$? → row 2, column 3
- Tall vs wide? → tall $m > n$, wide $m < n$
- Lower triangular → which entries are $0$? → above the diagonal ($i < j$)
- Transpose of a $3 \times 2$? → $2 \times 3$
- Symmetric means? → $A^T = A$
- Can you add $2 \times 3$ and $2 \times 2$? → **no**
￼￼2.2 Product of Matric
Source: [2.1 video](https://youtu.be/6HzOv2qICRo)

# 2.2 Product of Matrices

## From Equations to $A\mathbf{x} = \mathbf{b}$

- System: $x_1 + 3x_2 + x_3 = 1$ and $2x_1 - x_2 + x_3 = 1$

$$\underbrace{\begin{bmatrix} 1 & 3 & 1 \ 2 & -1 & 1 \end{bmatrix}}_{A} \underbrace{\begin{bmatrix} x_1 \ x_2 \ x_3 \end{bmatrix}}_{\mathbf{x}} = \underbrace{\begin{bmatrix} 1 \ 1 \end{bmatrix}}_{\mathbf{b}}$$

- Each row of $A$ = coefficients of one equation

## Two Ways to Read $A\mathbf{x}$

1. **Rows** → a batch of dot products: entry $i$ = $\mathbf{r}_i^T\mathbf{x}$ (row $i$ · $\mathbf{x}$)
2. **Columns** → a linear combination of the columns of $A$: $$A\mathbf{x} = x_1\mathbf{a}_1 + x_2\mathbf{a}_2 + \dots + x_n\mathbf{a}_n$$

- The column view comes back in modules 3, 4 and 5 → important
- $A\mathbf{e}_1$ = the **first column** of $A$ → e.g. $A\mathbf{e}_1 = (1, 2)$ above

## Matrix × Matrix

- **Rule**: columns of the left = rows of the right
- $(m \times n)(n \times l) \to (m \times l)$ → the middle $n$ must match and disappears
- Entry $(i, j)$ of $AB$ = row $i$ of $A$ · column $j$ of $B$

**Example**

$$\begin{bmatrix} 2 & -1 & 0 \ 1 & -1 & 1 \end{bmatrix} \begin{bmatrix} 0 & -2 \ 1 & 0 \ 1 & -1 \end{bmatrix} = \begin{bmatrix} -1 & -4 \ 0 & -3 \end{bmatrix}$$

- $(2 \times 3)(3 \times 2) \to 2 \times 2$
- Entry $(1,1)$: $2 \cdot 0 + (-1) \cdot 1 + 0 \cdot 1 = -1$

## Properties

- $AI = IA = A$
- **Not commutative** → in general $AB \ne BA$ (equal only in special cases, e.g. when one is $I$)

> [!warning] The lecture says $AB$ is _never_ equal to $BA$ The correct statement: it is _not always_ equal. Sometimes it is (e.g. $AI = IA$).

## Inverse

- Square $A$ is **invertible** (non-singular) if some $B$ gives $AB = BA = I$ → $B = A^{-1}$
- Like numbers: $2 \cdot \frac{1}{2} = 1$
- $A^{-1}$ **undoes** what $A$ does

**$2 \times 2$ formula**

$$A = \begin{bmatrix} a & b \ c & d \end{bmatrix}, \quad \det A = ad - bc \ne 0 \quad \Rightarrow \quad A^{-1} = \frac{1}{ad - bc} \begin{bmatrix} d & -b \ -c & a \end{bmatrix}$$

- Swap the diagonal, negate the other two, divide by the determinant
- If $ad - bc = 0$ → no inverse

**Example**

- $A = \begin{bmatrix} 2 & 1 \ 1 & 1 \end{bmatrix}$ → $\det A = 2 - 1 = 1$ → $A^{-1} = \begin{bmatrix} 1 & -1 \ -1 & 2 \end{bmatrix}$

## Quick Recall

- $A\mathbf{x}$ as rows? → dot products of each row with $\mathbf{x}$
- $A\mathbf{x}$ as columns? → $x_1\mathbf{a}_1 + \dots + x_n\mathbf{a}_n$
- $A\mathbf{e}_1$? → the first column of $A$
- $(2 \times 3)(3 \times 4)$? → $2 \times 4$
- $(2 \times 3)(2 \times 3)$? → ❌ not allowed
- Is $AB = BA$ always? → **no**
- When does a $2 \times 2$ have no inverse? → $ad - bc = 0$
- Inverse of $\begin{bmatrix} 2 & 1 \ 1 & 1 \end{bmatrix}$? → $\begin{bmatrix} 1 & -1 \ -1 & 2 \end{bmatrix}$

Source: [2.2 video](https://youtu.be/YLSydzA_PFk)