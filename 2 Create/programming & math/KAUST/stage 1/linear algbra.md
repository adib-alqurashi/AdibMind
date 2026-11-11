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

# 1.2