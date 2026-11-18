# MATH 102 · Chapter 5 — Integration

## 5.2 Area (23 problems)

**1)** Find the sum: $\displaystyle\sum_{k=0}^{4}\frac{1}{k^2+1}$

> [!check]- Solution
> 
> $$\sum_{k=0}^{4}\frac{1}{k^2+1}=1+\frac12+\frac15+\frac1{10}+\frac1{17}=\frac{170+85+34+17+10}{170}=\frac{316}{170}=\frac{158}{85}$$ **Answer:** $\color{red}{\boxed{\frac{158}{85}\approx1.859}}$

**2)** Use sigma notation to write the sum $\Big[\big(\tfrac2n\big)^3-\tfrac2n\Big]\big(\tfrac2n\big)+\cdots+\Big[\big(\tfrac{2n}{n}\big)^3-\tfrac{2n}{n}\Big]\big(\tfrac2n\big)$.

> [!check]- Solution
> 
> The $i$-th term replaces $2$ by $2i$ inside the brackets; the factor $\frac2n$ stays. **Answer:** $\color{red}{\boxed{\displaystyle\sum_{i=1}^{n}\Big[\Big(\frac{2i}{n}\Big)^3-\frac{2i}{n}\Big]\Big(\frac2n\Big)}}$

**3)** Use the properties of summation to evaluate $\displaystyle\sum_{i=1}^{16}(5i-4)$.

> [!check]- Solution
> 
> $$\sum_{i=1}^{16}(5i-4)=5\cdot\frac{16(17)}{2}-4(16)=680-64=616$$ **Answer:** $\color{red}{\boxed{616}}$

**4)** Rewrite $\displaystyle\sum_{k=1}^{n}\frac{6k(k-1)}{n^3}$ without sigma notation, then find it for $n=10,100,1000,10 000$.

> [!check]- Solution
> 
> $$\sum_{k=1}^{n}\frac{6k(k-1)}{n^3}=\frac{6}{n^3}\Big[\frac{n(n+1)(2n+1)}{6}-\frac{n(n+1)}{2}\Big]=\frac{(n+1)(2n-2)}{n^2}=\frac{2(n^2-1)}{n^2}$$ $n=10:\ 1.98\quad n=100:\ 1.9998\quad n=1000:\ 1.999998\quad n=10^4:\ 1.99999998$ (it approaches $2$). **Answer:** $\color{red}{\boxed{\frac{2(n^2-1)}{n^2}}}$; $\ 1.98,\ 1.9998,\ 1.999998,\ 1.99999998$

**5)** Use left and right endpoints and **6 rectangles** to find two approximations of the area between $g(x)=2x^2-x-1$ and the $x$-axis on $[2,5]$.

> [!check]- Solution
> 
> $\Delta x=\frac12$. Values at $2,2.5,3,3.5,4,4.5,5$: $\ 5,\ 9,\ 14,\ 20,\ 27,\ 35,\ 44$. $$L_6=\tfrac12(5+9+14+20+27+35)=55,\qquad R_6=\tfrac12(9+14+20+27+35+44)=74.5$$ **Answer:** $\color{red}{\boxed{L_6=55,\ R_6=74.5}}$ (exact area $\frac{129}{2}=64.5$ is between them)

**6)** Bound the area under $y=\sqrt{x}$ on $[0,1]$ by finding the upper and lower sums with **4** subintervals.

> [!check]- Solution
> 
> Increasing $\Rightarrow$ lower uses left endpoints $0,\frac14,\frac12,\frac34$; upper uses right endpoints $\frac14,\frac12,\frac34,1$. $$s=\frac14\Big(0+\tfrac12+\tfrac{\sqrt2}{2}+\tfrac{\sqrt3}{2}\Big)=\frac{1+\sqrt2+\sqrt3}{8}\approx0.518,\qquad S=\frac14\Big(\tfrac12+\tfrac{\sqrt2}{2}+\tfrac{\sqrt3}{2}+1\Big)=\frac{3+\sqrt2+\sqrt3}{8}\approx0.768$$ **Answer:** $\color{red}{\boxed{0.518<\text{Area}<0.768}}$

**7)** Find the upper and lower sums (in terms of $n$) for $f(x)=9-x^2$ on $[0,2]$.

> [!check]- Solution
> 
> $f$ decreasing: **upper** uses left endpoints $\frac{2(i-1)}{n}$, **lower** uses right endpoints $\frac{2i}{n}$; $\Delta x=\frac2n$. $$s(n)=\sum_{i=1}^n\Big(9-\frac{4i^2}{n^2}\Big)\frac2n=18-\frac{4(n+1)(2n+1)}{3n^2}=\frac{46}{3}-\frac4n-\frac{4}{3n^2}$$ $$S(n)=\sum_{i=1}^n\Big(9-\frac{4(i-1)^2}{n^2}\Big)\frac2n=18-\frac{4(n-1)(2n-1)}{3n^2}=\frac{46}{3}+\frac4n-\frac{4}{3n^2}$$
> 
> **Answer:** $\color{red}{\boxed{S(n)=\frac{46}{3}+\frac4n-\frac4{3n^2},\quad s(n)=\frac{46}{3}-\frac4n-\frac4{3n^2}}}$

**8)** Use the limit process to find the area of the region bounded by $y=x^2-x^3$ and the $x$-axis on $[-1,1]$.

> [!check]- Solution
> 
> $\Delta x=\frac2n,\ x_i=-1+\frac{2i}{n}$. Expanding, $f(x_i)=x_i^2-x_i^3=2-\frac{10i}{n}+\frac{16i^2}{n^2}-\frac{8i^3}{n^3}$. $$S(n)=\frac2n\sum_{i=1}^n f(x_i)=4-\frac{10(n+1)}{n}+\frac{16(n+1)(2n+1)}{3n^2}-\frac{4(n+1)^2}{n^2}$$ $$\lim_{n\to\infty}S(n)=4-10+\frac{32}{3}-4=\frac23$$ **Answer:** $\color{red}{\boxed{\tfrac23}}$

**9)** Use the limit process to find the area between $f(y)=y^2$ and the $y$-axis for $0\le y\le5$.

> [!check]- Solution
> 
> $\Delta y=\frac5n,\ y_i=\frac{5i}{n}$: $$A=\lim_{n\to\infty}\sum_{i=1}^n\frac{25i^2}{n^2}\cdot\frac5n=\lim_{n\to\infty}\frac{125}{n^3}\cdot\frac{n(n+1)(2n+1)}{6}=\frac{125}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{125}{3}}}$

**10)** Use the Midpoint Rule with $n=4$ to approximate the area under $f(x)=\ln x$ on $[1,5]$.

> [!check]- Solution
> 
> $\Delta x=1$, midpoints $1.5,2.5,3.5,4.5$: $$M_4=\ln1.5+\ln2.5+\ln3.5+\ln4.5=\ln\frac{945}{16}\approx4.079$$ **Answer:** $\color{red}{\boxed{\ln\tfrac{945}{16}\approx4.079}}$

**11)** The upper sum (in terms of $n$) for the region bounded by $f(x)=2x^2$ and the $x$-axis on $[1,3]$ is

> [!check]- Solution
> 
> $f$ is increasing on $[1,3]$, so the upper sum uses right endpoints: $\Delta x=\frac2n,\ x_i=1+\frac{2i}{n}$. $$S(n)=\sum_{i=1}^n 2\Big(1+\frac{2i}{n}\Big)^2\frac2n=\frac4n\sum_{i=1}^n\Big(1+\frac{4i}{n}+\frac{4i^2}{n^2}\Big)=4+\frac{16}{n^2}\cdot\frac{n(n+1)}{2}+\frac{16}{n^3}\cdot\frac{n(n+1)(2n+1)}{6}$$ $$=4+8+\frac8n+\frac83\Big(2+\frac3n+\frac1{n^2}\Big)=\frac{52}{3}+\frac{16}{n}+\frac{8}{3n^2}$$ **Answer:** $\color{red}{\boxed{\frac{52}{3}+\frac{16}{n}+\frac{8}{3n^2}}}$

**12)** The upper sum for the region bounded by $f(x)=x^2$ and the $x$-axis on $[2,5]$ is

> [!check]- Solution
> 
> Increasing $\Rightarrow$ right endpoints: $\Delta x=\frac3n,\ x_i=2+\frac{3i}{n}$. $$S(n)=\frac3n\sum_{i=1}^n\Big(4+\frac{12i}{n}+\frac{9i^2}{n^2}\Big)=12+18\cdot\frac{n+1}{n}+\frac92\cdot\frac{(n+1)(2n+1)}{n^2}=39+\frac{63}{2n}+\frac{9}{2n^2}$$ **Answer:** $\color{red}{\boxed{39+\frac{63}{2n}+\frac{9}{2n^2}}}$

**13)** Using **four rectangles and left endpoints**, the approximate area under $f(x)=\sin(2x)+3x$ from $x=\frac{\pi}{3}$ to $x=\frac{5\pi}{3}$ is

> [!check]- Solution
> 
> $\Delta x=\frac{5\pi/3-\pi/3}{4}=\frac\pi3$; left endpoints $\frac\pi3,\frac{2\pi}3,\pi,\frac{4\pi}3$. $$L_4=\frac\pi3\Big[\big(\tfrac{\sqrt3}{2}+\pi\big)+\big(-\tfrac{\sqrt3}{2}+2\pi\big)+(0+3\pi)+\big(\tfrac{\sqrt3}{2}+4\pi\big)\Big]=\frac\pi3\Big(\frac{\sqrt3}{2}+10\pi\Big)=\frac{\sqrt3}{6}\pi+\frac{10}{3}\pi^2$$ **Answer:** $\color{red}{\boxed{\frac{\sqrt3}{6}\pi+\frac{10}{3}\pi^2}}$

**14)** Same function and interval as 5.2-Q3, but with **four rectangles and right endpoints**.

> [!check]- Solution
> 
> Right endpoints $\frac{2\pi}3,\pi,\frac{4\pi}3,\frac{5\pi}3$: $$R_4=\frac\pi3\Big[\big(-\tfrac{\sqrt3}{2}+2\pi\big)+3\pi+\big(\tfrac{\sqrt3}{2}+4\pi\big)+\big(-\tfrac{\sqrt3}{2}+5\pi\big)\Big]=\frac\pi3\Big(14\pi-\frac{\sqrt3}{2}\Big)=-\frac{\sqrt3}{6}\pi+\frac{14}{3}\pi^2$$ **Answer:** $\color{red}{\boxed{-\frac{\sqrt3}{6}\pi+\frac{14}{3}\pi^2}}$

**15)** If $R_n$ is the Riemann sum for $f(x)=x^2-2x$, $1\le x\le 4$, with $n$ subintervals and right endpoints, then $R_n=$

> [!check]- Solution
> 
> $\Delta x=\frac3n,\ x_i=1+\frac{3i}{n}$, and $f(x_i)=\Big(1+\frac{6i}{n}+\frac{9i^2}{n^2}\Big)-2-\frac{6i}{n}=-1+\frac{9i^2}{n^2}$. $$R_n=\sum_{i=1}^n\Big(-1+\frac{9i^2}{n^2}\Big)\frac3n=-3+\frac{27}{n^3}\cdot\frac{n(n+1)(2n+1)}{6}=-3+\frac{9(n+1)(2n+1)}{2n^2}$$ **Answer:** $\color{red}{\boxed{-3+\frac{9(n+1)(2n+1)}{2n^2}}}$

**16)** Using **three rectangles and midpoints**, the approximate area under $f(x)=\frac{x}{x-1}$ from $x=2$ to $x=8$ is

> [!check]- Solution
> 
> $\Delta x=2$, midpoints $3,5,7$: $$M_3=2\Big[\tfrac32+\tfrac54+\tfrac76\Big]=2\cdot\frac{18+15+14}{12}=\frac{47}{6}$$ **Answer:** $\color{red}{\boxed{\frac{47}{6}}}$

**17)** Using **three rectangles and left endpoints**, the approximate area under $f(x)=\frac{1}{x+1}$ from $x=1$ to $x=3$ is

> [!check]- Solution
> 
> $\Delta x=\frac23$, left endpoints $1,\frac53,\frac73$: $$L_3=\frac23\Big[\tfrac12+\tfrac38+\tfrac3{10}\Big]=\frac23\cdot\frac{20+15+12}{40}=\frac{47}{60}$$ **Answer:** $\color{red}{\boxed{\frac{47}{60}}}$

**18)** $\displaystyle\sum_{i=1}^{n}\frac{2i^3-3i}{n^4}-\frac1n+\frac1{n^2}+\frac{3}{2n^3}=$

> [!check]- Solution
> 
> $$\frac{2}{n^4}\cdot\frac{n^2(n+1)^2}{4}-\frac{3}{n^4}\cdot\frac{n(n+1)}{2}=\frac12+\frac1n+\frac1{2n^2}-\frac{3}{2n^2}-\frac{3}{2n^3}$$ Adding $-\frac1n+\frac1{n^2}+\frac{3}{2n^3}$ cancels every term except $\frac12$. **Answer:** $\color{red}{\boxed{\tfrac12}}$

**19)** The area of the region bounded by $f(x)=4-x^2$, the $x$-axis and $x=1,\ x=2$ (with $c_i$ the right endpoint) is given by

> [!check]- Solution
> 
> $\Delta x=\frac1n,\ c_i=1+\frac in$: $$f(c_i)\Delta x=\Big[4-\Big(1+\frac in\Big)^2\Big]\frac1n=\Big(3-\frac{2i}{n}-\frac{i^2}{n^2}\Big)\frac1n=\frac3n-\frac{2i}{n^2}-\frac{i^2}{n^3}$$ **Answer:** $\color{red}{\boxed{\lim_{n\to\infty}\Big(\frac3n\sum_{i=1}^n1-\frac2{n^2}\sum_{i=1}^n i-\frac1{n^3}\sum_{i=1}^n i^2\Big)}}$

**20)** Approximate the area between $f(x)=|\sin x|$, the $x$-axis, $x=-\frac{3\pi}{4}$ and $x=\frac\pi2$ using left endpoints and 5 rectangles of equal width.

> [!check]- Solution
> 
> $\Delta x=\frac{5\pi/4}{5}=\frac\pi4$; left endpoints $-\frac{3\pi}4,-\frac\pi2,-\frac\pi4,0,\frac\pi4$. $$L_5=\frac\pi4\Big[\tfrac{\sqrt2}{2}+1+\tfrac{\sqrt2}{2}+0+\tfrac{\sqrt2}{2}\Big]=\frac\pi4\cdot\frac{3\sqrt2+2}{2}=\frac\pi8(3\sqrt2+2)$$ **Answer:** $\color{red}{\boxed{\frac\pi8(3\sqrt2+2)}}$

**21)** Using the Midpoint Rule with $n=3$, the area under $f(x)=\sin^2x$ over $[0,\pi]$ is approximately

> [!check]- Solution
> 
> $\Delta x=\frac\pi3$, midpoints $\frac\pi6,\frac\pi2,\frac{5\pi}6$: $$M_3=\frac\pi3\Big[\big(\tfrac12\big)^2+1^2+\big(\tfrac12\big)^2\Big]=\frac\pi3\cdot\frac32=\frac\pi2$$ **Answer:** $\color{red}{\boxed{\tfrac\pi2}}$

**22)** The lower sum (in terms of $n$) for the region bounded by $f(x)=4-x^2$ and the $x$-axis on $[0,2]$ is

> [!check]- Solution
> 
> $f$ is **decreasing** on $[0,2]$, so the minimum on each piece is at the **right** endpoint $x_i=\frac{2i}{n}$. $$s(n)=\sum_{i=1}^n\Big(4-\frac{4i^2}{n^2}\Big)\frac2n=8-\frac{8}{n^3}\cdot\frac{n(n+1)(2n+1)}{6}=\frac{24n^2-4(2n^2+3n+1)}{3n^2}=\frac{4}{3n^2}(4n^2-3n-1)$$ **Answer:** $\color{red}{\boxed{\frac{4}{3n^2}(4n^2-3n-1)}}$

**23)** The upper sum for the region bounded by $f(x)=6-2x$ on $[1,2]$, in terms of $n$, is

> [!check]- Solution
> 
> Decreasing $\Rightarrow$ the maximum is at the **left** endpoint $x_{i-1}=1+\frac{i-1}{n}$, $\Delta x=\frac1n$. $$S(n)=\sum_{i=1}^n\Big(4-\frac{2(i-1)}{n}\Big)\frac1n=4-\frac{2}{n^2}\cdot\frac{(n-1)n}{2}=4-\frac{n-1}{n}=3+\frac1n$$ **Answer:** $\color{red}{\boxed{3+\frac1n}}$

## 5.3 Riemann Sums and Definite Integrals (24 problems)

**1)** Use the partition $c_i=\frac{3i^2}{n^2}$ to evaluate $\displaystyle\lim_{n\to\infty}\sum_{i=1}^n f(c_i)\Delta x_i$ over the region bounded by $f(x)=\sqrt x,\ y=0,\ x=0,\ x=3$.

> [!check]- Solution
> 
> $\Delta x_i=c_i-c_{i-1}=\frac{3i^2-3(i-1)^2}{n^2}=\frac{3(2i-1)}{n^2}$ and $f(c_i)=\frac{\sqrt3 i}{n}$. $$\lim_{n\to\infty}\sum_{i=1}^n\frac{\sqrt3 i}{n}\cdot\frac{3(2i-1)}{n^2}=\lim_{n\to\infty}\frac{3\sqrt3}{n^3}\Big[\frac{n(n+1)(2n+1)}{3}-\frac{n(n+1)}{2}\Big]=3\sqrt3\cdot\frac23=2\sqrt3$$ **Answer:** $\color{red}{\boxed{2\sqrt3}}$

**2)** Evaluate $\displaystyle\int_{-2}^{1}(2x^2+3) dx$ by the limit definition.

> [!check]- Solution
> 
> $\Delta x=\frac3n,\ x_i=-2+\frac{3i}{n}$, so $f(x_i)=2\Big(4-\frac{12i}{n}+\frac{9i^2}{n^2}\Big)+3=11-\frac{24i}{n}+\frac{18i^2}{n^2}$. $$\sum_{i=1}^n f(x_i)\frac3n=33-\frac{36(n+1)}{n}+\frac{9(n+1)(2n+1)}{n^2}\ \xrightarrow{n\to\infty}\ 33-36+18=15$$ **Answer:** $\color{red}{\boxed{15}}$

**3)** Write $\displaystyle\lim_{\Vert \Delta\Vert \to0}\sum_{i=1}^n\Big(1+\frac{3}{c_i}\Big)\Delta x_i$ on $[1,5]$ as a definite integral.

> [!check]- Solution
> 
> The integrand is what multiplies $\Delta x_i$, with $c_i\to x$:
> 
> **Answer:** $\color{red}{\boxed{\displaystyle\int_1^5\Big(1+\frac3x\Big)dx}}$

**4)** Write a definite integral for the area of the region under $f(x)=4-|x|$ (the triangle above the $x$-axis).

> [!check]- Solution
> 
> $4-|x|\ge0$ exactly when $-4\le x\le4$. (Its value is the triangle area $\frac12\cdot8\cdot4=16$.) **Answer:** $\color{red}{\boxed{\displaystyle\int_{-4}^{4}(4-|x|) dx}}$

**5)** Write a definite integral for the area between $x=g(y)=y^3$ and the $y$-axis for $0\le y\le2$ (the figure's region).

> [!check]- Solution
> 
> The region is measured horizontally, so integrate in $y$. (Its value is $\frac{y^4}{4}\big|_0^2=4$.) **Answer:** $\color{red}{\boxed{\displaystyle\int_0^2 y^3 dy}}$

**6)** Evaluate $\displaystyle\int_{-7}^{7}\sqrt{49-x^2} dx$ with a geometric formula.

> [!check]- Solution
> 
> $y=\sqrt{49-x^2}$ is the upper semicircle of radius $7$: area $=\frac12\pi(7)^2$. **Answer:** $\color{red}{\boxed{\frac{49\pi}{2}}}$

**7)** Given $\int_2^6x^3dx=320,\ \int_2^6x dx=16,\ \int_2^6dx=4$, evaluate $\displaystyle\int_2^6(2x^3-10x+7) dx$.

> [!check]- Solution
> 
> $$2(320)-10(16)+7(4)=640-160+28=508$$ **Answer:** $\color{red}{\boxed{508}}$

**8)** Given $\int_{-1}^1f(x) dx=0$ and $\int_0^1f(x) dx=5$, evaluate (a) $\int_{-1}^0f$ (b) $\int_0^1f-\int_{-1}^0f$ (c) $\int_{-1}^13f$ (d) $\int_0^13f$.

> [!check]- Solution
> 
> (a) $\int_{-1}^0f=\int_{-1}^1f-\int_0^1f=0-5=-5$ (b) $5-(-5)=10$ (c) $3(0)=0$ (d) $3(5)=15$ **Answer:** $\color{red}{\boxed{-5,\ 10,\ 0,\ 15}}$

**9)** $f$ is made of line segments through $(0,-1),(3,2),(4,2),(8,-2),(11,1)$. Evaluate (a) $\int_0^1-f$ (b) $\int_3^43f$ (c) $\int_0^7f$ (d) $\int_5^{11}f$ (e) $\int_0^{11}f$ (f) $\int_4^{10}f$.

> [!check]- Solution
> 
> $f$ crosses zero at $x=1,6,10$. Signed areas: $[0,1]:-\frac12$; $[1,3]:+2$; $[3,4]:+2$; $[4,6]:+2$; $[6,8]:-2$; $[8,10]:-2$; $[10,11]:+\frac12$. (a) $\frac12$ (b) $3\cdot2=6$ (c) $-\frac12+2+2+2-\frac12=5$ (d) $\frac12-2-2+\frac12=-3$ (e) $-\frac12+6-4+\frac12=2$ (f) $2-4=-2$ **Answer:** $\color{red}{\boxed{\tfrac12,\ 6,\ 5,\ -3,\ 2,\ -2}}$

**10)** Find $a$ and $b$ so that $\displaystyle\int_{-3}^{3}f dx+\int_3^6f dx-\int_a^bf dx=\int_{-1}^6f dx$.

> [!check]- Solution
> 
> The first two combine to $\int_{-3}^6f$. Then $\int_{-3}^6f-\int_a^bf=\int_{-1}^6f$ forces $\int_a^bf=\int_{-3}^{-1}f$.
> 
> **Answer:** $\color{red}{\boxed{a=-3,\ b=-1}}$

**11)** $\displaystyle L=\lim_{n\to\infty}\sum_{i=1}^n\frac2n e^{1+\frac{5i}{n}}=$

> [!check]- Solution
> 
> Write $\frac2n=\frac25\cdot\frac5n$. Take $\Delta x=\frac5n$ (so $b-a=5$) and $x_i=1+\frac{5i}{n}$ (so $a=1,\ b=6$); then $f(x_i)=e^{x_i}$. $$L=\frac25\lim_{n\to\infty}\sum_{i=1}^n e^{x_i}\Delta x=\frac25\int_1^6e^x dx$$ **Answer:** $\color{red}{\boxed{\int_1^6\tfrac25e^x dx}}$

**12)** $\displaystyle\lim_{n\to\infty}\sum_{i=1}^n\frac2n\Big(\frac{5i}{n}+3\Big)^6$ is the area under the curve

> [!check]- Solution
> 
> $\frac2n=\frac25\cdot\frac5n$, $\Delta x=\frac5n$, $x_i=3+\frac{5i}{n}$ ⇒ $a=3,\ b=8$, $f(x)=\frac25x^6$. **Answer:** $\color{red}{\boxed{y=\tfrac25x^6\text{ on }[3,8]}}$

**13)** $\displaystyle\lim_{n\to\infty}\sum_{i=1}^n\Big(\frac{4i^7}{n^8}+\frac{8n^2}{n^3+ni^2}\Big)=$

> [!check]- Solution
> 
> With $\Delta x=\frac1n,\ x_i=\frac in$ on $[0,1]$: $\ \frac{4i^7}{n^8}=4x_i^7\Delta x$ and $\frac{8n^2}{n^3+ni^2}=\frac{8}{1+(i/n)^2}\cdot\frac1n$. $$\int_0^1\Big(4x^7+\frac{8}{1+x^2}\Big)dx=\Big[\frac{x^8}{2}+8\tan^{-1}x\Big]_0^1=\frac12+8\cdot\frac\pi4=\frac12+2\pi$$ **Answer:** $\color{red}{\boxed{\tfrac12+2\pi}}$

**14)** $\displaystyle L=\lim_{n\to\infty}\sum_{i=1}^n\frac6n\ln\Big(2+\frac{3i}{n}\Big)=$

> [!check]- Solution
> 
> $\frac6n=2\cdot\frac3n$; $\Delta x=\frac3n$ and $x_i=2+\frac{3i}{n}$ ⇒ $[2,5]$ and $f(x)=2\ln x$. (Shifting $u=x-2$ gives $\int_0^32\ln(2+u) du$ — not listed.) **Answer:** $\color{red}{\boxed{\int_2^52\ln x dx}}$

**15)** $f$ is continuous with $\int_{-3}^1f=1,\ \int_1^4f=7,\ \int_4^3f=-10,\ \int_{-3}^0f=-4$. Then $\displaystyle\int_{-3}^3\big(f(x)+\sqrt{9-x^2}\big)dx=$

> [!check]- Solution
> 
> $\int_3^4f=10$, so $\int_{-3}^3f=\int_{-3}^1f+\int_1^4f-\int_3^4f=1+7-10=-2$. $\int_{-3}^3\sqrt{9-x^2} dx$ is a semicircle of radius 3: $\frac12\pi(9)=\frac92\pi$. **Answer:** $\color{red}{\boxed{-2+\tfrac92\pi}}$

**16)** $f$ is continuous with $\int_1^{-5}f=-8,\ \int_4^2f=1,\ \int_{-3}^23f=30,\ \int_1^4f=6$. Then $\displaystyle\int_{-5}^2[f(x)+2] dx=$

> [!check]- Solution
> 
> $\int_{-5}^1f=8,\ \int_2^4f=-1$, so $\int_1^2f=\int_1^4f-\int_2^4f=6+1=7$. $$\int_{-5}^2f=\int_{-5}^1f+\int_1^2f=8+7=15,\qquad \int_{-5}^22 dx=2(7)=14$$ **Answer:** $\color{red}{\boxed{29}}$

**17)** If $f(x)=\begin{cases}2x,&-1\le x\le0\cr \sqrt{16-25x^2},&0<x\le\frac45\end{cases}$, then $\displaystyle\int_{-1}^{4/5}f(x) dx=$

> [!check]- Solution
> 
> $\int_{-1}^02x dx=[x^2]_{-1}^0=-1$. $\int_0^{4/5}\sqrt{16-25x^2} dx=5\int_0^{4/5}\sqrt{\tfrac{16}{25}-x^2} dx=5\cdot\frac\pi4\Big(\frac45\Big)^2=\frac{4\pi}{5}$ (quarter circle, radius $\frac45$). **Answer:** $\color{red}{\boxed{-1+\tfrac{4\pi}{5}}}$

**18)** Using the comparison property to estimate $I=\int_1^e x^{-2}\ln x dx$, we get $A\le I\le B$. Then $A+B=$

> [!check]- Solution
> 
> $f(x)=x^{-2}\ln x$, $f'(x)=x^{-3}(1-2\ln x)=0\Rightarrow x=\sqrt e$. $f(1)=0,\ f(\sqrt e)=\frac{1/2}{e}=\frac1{2e}$ (max), $f(e)=\frac1{e^2}$. So $0\le f\le\frac1{2e}$ on $[1,e]$: $$0\le I\le\frac{e-1}{2e}\ \Rightarrow\ A+B=\frac{e-1}{2e}$$ **Answer:** $\color{red}{\boxed{\tfrac{e-1}{2e}}}$

**19)** $[0,8]$ is partitioned at $x_0=0,x_1=1,x_2=3,x_3=7,x_4=8$ with $c_1=1,c_2=2,c_3=5,c_4=8$. The Riemann sum of $f(x)=x^2+3x$ is

> [!check]- Solution
> 
> $\Delta x_i=1,2,4,1$ and $f(c_i)=4,10,40,88$: $$\sum f(c_i)\Delta x_i=4(1)+10(2)+40(4)+88(1)=272$$ **Answer:** $\color{red}{\boxed{272}}$

**20)** On $[0,\pi]$, $\displaystyle\lim_{\Vert \Delta\Vert \to0}\sum_{i=1}^n\big(2^{-c_i}\sin c_i\big)\Delta x_i$ can be written as

> [!check]- Solution
> 
> Replace $c_i$ by $x$, $\Delta x_i$ by $dx$, keep the interval $[0,\pi]$. **Answer:** $\color{red}{\boxed{\int_0^\pi2^{-x}\sin x dx}}$

**21)** $\displaystyle\lim_{\Vert \Delta\Vert \to0}\sum_{i=1}^n\sqrt{4-c_i^2} \Delta x_i$ on $[0,2]$ equals

> [!check]- Solution
> 
> It is $\int_0^2\sqrt{4-x^2} dx$, a quarter circle of radius 2: $\frac14\pi(2)^2=\pi$. **Answer:** $\color{red}{\boxed{\pi}}$

**22)** The graph of $f$: a segment from $(-4,-1)$ to $(-2,0)$, the lower semicircle of radius 2 on $[-2,2]$, then segments $(2,0)\to(4,2)\to(6,0)$. Find $\int_{-4}^6f(x) dx$.

> [!check]- Solution
> 
> $[-4,-2]$: triangle below, $-\frac12(2)(1)=-1$. $[-2,2]$: half disk below, $-\frac12\pi(2)^2=-2\pi$. $[2,6]$: triangle above, $\frac12(4)(2)=4$. $$-1-2\pi+4=3-2\pi$$
> 
> **Answer:** $\color{red}{\boxed{3-2\pi}}$

**23)** $\displaystyle\int_0^2\lfloor x\rfloor dx=$ (greatest integer function; hint: area under the curve)

> [!check]- Solution
> 
> $\lfloor x\rfloor=0$ on $[0,1)$ and $=1$ on $[1,2)$: area $=0+1\cdot1=1$. **Answer:** $\color{red}{\boxed{1}}$

**24)** For which pair is $\displaystyle\int_a^b\sin x dx<0$? (i) $a=\frac\pi2,\ b=2\pi$ (ii) $a=0,\ b=\frac\pi2$ (iii) $a=\frac\pi2,\ b=\frac{3\pi}2$ (iv) $a=0,\ b=\frac{3\pi}2$ (v) $a=\frac\pi2,\ b=\pi$

> [!check]- Solution
> 
> $\int_a^b\sin x dx=\cos a-\cos b$. (i) $0-1=-1<0$ ✓; (ii) $1$; (iii) $0$; (iv) $1$; (v) $1$. **Answer:** $\color{red}{\boxed{a=\tfrac\pi2,\ b=2\pi}}$

## 5.4 The Fundamental Theorem of Calculus (24 problems)

**1)** Evaluate $\displaystyle\int_1^8\sqrt{\frac2x} dx$.

> [!check]- Solution
> 
> $$\sqrt2\int_1^8x^{-1/2}dx=\sqrt2\Big[2\sqrt x\Big]_1^8=2\sqrt2 (2\sqrt2-1)=8-2\sqrt2$$ **Answer:** $\color{red}{\boxed{8-2\sqrt2}}$

**2)** Evaluate $\displaystyle\int_0^5|2x-5| dx$.

> [!check]- Solution
> 
> Split at $x=\frac52$: $$\int_0^{5/2}(5-2x) dx+\int_{5/2}^5(2x-5) dx=\Big[5x-x^2\Big]_0^{5/2}+\Big[x^2-5x\Big]_{5/2}^5=\frac{25}{4}+\frac{25}{4}=\frac{25}{2}$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac{25}{2}}}$

**3)** Evaluate $\displaystyle\int_0^{\pi/4}\frac{1-\sin^2\theta}{\cos^2\theta} d\theta$.

> [!check]- Solution
> 
> $1-\sin^2\theta=\cos^2\theta$, so the integrand is $1$: $\int_0^{\pi/4}d\theta=\frac\pi4$. **Answer:** $\color{red}{\boxed{\tfrac\pi4}}$

**4)** Find the area of the region bounded by $y=x^3+6x,\ x=2,\ y=0$.

> [!check]- Solution
> 
> $x^3+6x=x(x^2+6)=0$ only at $x=0$, and $y\ge0$ on $[0,2]$: $$\int_0^2(x^3+6x) dx=\Big[\frac{x^4}{4}+3x^2\Big]_0^2=4+12=16$$ **Answer:** $\color{red}{\boxed{16}}$

**5)** Find the value(s) of $c$ guaranteed by the Mean Value Theorem for Integrals for $f(x)=5-\frac1x$ on $[1,4]$.

> [!check]- Solution
> 
> $$\int_1^4\Big(5-\frac1x\Big)dx=\Big[5x-\ln x\Big]_1^4=15-\ln4\ \Rightarrow\ f(c)=\frac{15-\ln4}{3}=5-\frac{\ln4}{3}$$ $5-\frac1c=5-\frac{\ln4}{3}\Rightarrow c=\frac{3}{\ln4}\approx2.164\in[1,4]$. **Answer:** $\color{red}{\boxed{c=\frac{3}{\ln4}\approx2.164}}$

**6)** Find the average value of $f(x)=\sin x$ on $[0,\pi]$ and all $x$ where $f$ equals it.

> [!check]- Solution
> 
> $$f_{\text{avg}}=\frac1\pi\int_0^\pi\sin x dx=\frac1\pi\Big[-\cos x\Big]_0^\pi=\frac2\pi$$ $\sin x=\frac2\pi\Rightarrow x=\arcsin\frac2\pi\approx0.690$ or $x=\pi-\arcsin\frac2\pi\approx2.451$. **Answer:** $\color{red}{\boxed{\tfrac2\pi;\ x\approx0.690,\ 2.451}}$

**7)** Use the Second FTC to find $F'(x)$ for $F(x)=\displaystyle\int_1^x\sqrt t \csc t dt$.

> [!check]- Solution
> 
> The lower limit is a constant and the upper limit is $x$, so $F'(x)$ is the integrand at $x$. **Answer:** $\color{red}{\boxed{F'(x)=\sqrt x \csc x}}$

**8)** Find $F'(x)$ for $F(x)=\displaystyle\int_0^{2x}\cos t^4 dt$.

> [!check]- Solution
> 
> $F'(x)=\cos\big((2x)^4\big)\cdot2=2\cos(16x^4)$. **Answer:** $\color{red}{\boxed{2\cos(16x^4)}}$

**9)** $v(t)=t^2-t-12$ (ft/s), $1\le t\le5$. Find (a) the displacement and (b) the total distance traveled.

> [!check]- Solution
> 
> $v=(t-4)(t+3)$: negative on $[1,4)$, positive on $(4,5]$. Let $G(t)=\frac{t^3}{3}-\frac{t^2}{2}-12t$. $\int_1^4v dt=G(4)-G(1)=-\frac{45}{2},\qquad\int_4^5v dt=G(5)-G(4)=\frac{23}{6}$ (a) $-\frac{45}{2}+\frac{23}{6}=-\frac{56}{3}$ ft (b) $\frac{45}{2}+\frac{23}{6}=\frac{79}{3}$ ft **Answer:** $\color{red}{\boxed{\text{(a) }-\tfrac{56}{3}\text{ ft}\quad\text{(b) }\tfrac{79}{3}\text{ ft}}}$

**10)** Find $f(x)$ and all values of $c$ such that $\displaystyle\int_c^xf(t) dt=x^2+x-2$.

> [!check]- Solution
> 
> Differentiate: $f(x)=2x+1$. Put $x=c$: $0=c^2+c-2=(c+2)(c-1)$.
> 
> **Answer:** $\color{red}{\boxed{f(x)=2x+1,\quad c=1\text{ or }c=-2}}$

**11)** Prove that $\displaystyle\frac{d}{dx}\Big[\int_{u(x)}^{v(x)}f(t) dt\Big]=f(v(x)) v'(x)-f(u(x)) u'(x)$.

> [!check]- Solution
> 
> Let $F$ be an antiderivative of $f$ ($F'=f$). By the FTC, $\int_{u(x)}^{v(x)}f(t) dt=F(v(x))-F(u(x))$. By the chain rule, $$\frac{d}{dx}\big[F(v(x))-F(u(x))\big]=F'(v(x))v'(x)-F'(u(x))u'(x)=f(v(x))v'(x)-f(u(x))u'(x).\ \blacksquare$$ _Use it:_ $f(x)=\int_{\sqrt x}^xe^{t^2}dt\Rightarrow f'(x)=e^{x^2}-e^{x}\cdot\frac1{2\sqrt x}$, so $f'(4)=e^{16}-\frac{e^4}{4}$. **Answer:** $\color{red}{\boxed{f(v)v'-f(u)u'}}$ (proved)

**12)** $f$ is continuous and $\displaystyle\int_0^{\tan x}e^tf(t) dt=4x\cos x-\int_{\sin x}^{x^4}3f(t) dt$ for all $x$. Then $f(0)=$

> [!check]- Solution
> 
> Differentiate both sides: $$e^{\tan x}f(\tan x)\sec^2x=4\cos x-4x\sin x-\big[3f(x^4)\cdot4x^3-3f(\sin x)\cos x\big]$$ At $x=0$: $f(0)=4-[0-3f(0)]=4+3f(0)\Rightarrow-2f(0)=4$. **Answer:** $\color{red}{\boxed{f(0)=-2}}$

**13)** $g$ is continuous and $\displaystyle\int_1^{2x-1}g(t) dt=\pi^2+x\sin x+\int_{2x-1}^2(\cos t) g(t) dt$ for all $x$. Then $g(5)=$

> [!check]- Solution
> 
> Differentiate: $2g(2x-1)=x\cos x+\sin x-2\cos(2x-1) g(2x-1)$. $2x-1=5\Rightarrow x=3$: $\ 2g(5)=3\cos3+\sin3-2\cos5 g(5)\Rightarrow g(5)(2+2\cos5)=3\cos3+\sin3$. **Answer:** $\color{red}{\boxed{\dfrac{3\cos3+\sin3}{2+2\cos5}}}$

**14)** If $f(x)=\int_{x^3}^1t^5\tan\big(\frac\pi4t\big) dt$ and $g(y)=\int_2^yf(u) du$, then $g''(1)=$

> [!check]- Solution
> 
> $g'(y)=f(y)\Rightarrow g''(y)=f'(y)$, and $f'(x)=-(x^3)^5\tan\big(\frac\pi4x^3\big)\cdot3x^2$. $$g''(1)=f'(1)=-1\cdot\tan\tfrac\pi4\cdot3=-3$$ **Answer:** $\color{red}{\boxed{-3}}$

**15)** If $F(x)=\int_1^xf(t) dt$ and $f(t)=\int_1^{t^2}\sin(1+u^2) du$, then $F''(1)=$

> [!check]- Solution
> 
> $F'(x)=f(x)\Rightarrow F''(x)=f'(x)$, and $f'(t)=\sin(1+t^4)\cdot2t$. So $F''(1)=2\sin2$. **Answer:** $\color{red}{\boxed{2\sin2}}$

**16)** If $f(x)=\displaystyle\int_{\sin x}^{\cos3x}\frac{1}{\sqrt{1+4t^2}} dt$, then $f'\big(\frac\pi2\big)=$

> [!check]- Solution
> 
> $$f'(x)=\frac{-3\sin3x}{\sqrt{1+4\cos^23x}}-\frac{\cos x}{\sqrt{1+4\sin^2x}}$$ At $\frac\pi2$: $\cos\frac{3\pi}2=0,\ \sin\frac{3\pi}2=-1,\ \cos\frac\pi2=0$: $\ f'=\frac{3}{1}-0=3$. **Answer:** $\color{red}{\boxed{3}}$

**17)** A particle moves with $v(t)=3t^2-12$ m/s. The distance traveled during $[0,3]$ is

> [!check]- Solution
> 
> $v=3(t-2)(t+2)$: $v<0$ on $[0,2)$, $v>0$ on $(2,3]$. $$\int_0^2(12-3t^2) dt+\int_2^3(3t^2-12) dt=\big[12t-t^3\big]_0^2+\big[t^3-12t\big]_2^3=16+7=23$$ **Answer:** $\color{red}{\boxed{23\text{ m}}}$

**18)** The **sum** of the numbers $b$ for which the average value of $f(x)=-6x^2-6x+1$ on $[b,0]$ equals $1$ is

> [!check]- Solution
> 
> $$\frac{1}{0-b}\int_b^0(-6x^2-6x+1) dx=-\frac1b\Big[0-(-2b^3-3b^2+b)\Big]=-2b^2-3b+1=1$$ $b(2b+3)=0$; $b=0$ is rejected (no interval), so $b=-\frac32$. **Answer:** $\color{red}{\boxed{-\tfrac32}}$

**19)** The **sum** of the numbers $c$ such that $f(c)$ equals the average value of $f(x)=3x^2+x+1$ on $[0,2]$ is

> [!check]- Solution
> 
> $$f_{\text{avg}}=\frac12\int_0^2(3x^2+x+1) dx=\frac12\Big[x^3+\frac{x^2}{2}+x\Big]_0^2=\frac12(12)=6$$ $3c^2+c+1=6\Rightarrow3c^2+c-5=0\Rightarrow c=\frac{-1\pm\sqrt{61}}{6}$. Only $\frac{-1+\sqrt{61}}{6}\approx1.14$ lies in $[0,2]$. **Answer:** $\color{red}{\boxed{\frac{-1+\sqrt{61}}{6}}}$

**20)** $\displaystyle\lim_{n\to\infty}\sum_{i=1}^n\Big(\frac{i^4}{n^5}+\frac{i}{n^2}\Big)=$ (hint: a Riemann sum on $[0,1]$)

> [!check]- Solution
> 
> $\frac{i^4}{n^5}=\big(\frac in\big)^4\frac1n,\ \frac i{n^2}=\frac in\cdot\frac1n$: $$\int_0^1(x^4+x) dx=\frac15+\frac12=\frac7{10}$$ **Answer:** $\color{red}{\boxed{\tfrac{7}{10}}}$

**21)** The value of $c$ guaranteed by the MVT for integrals for $f(x)=\sqrt x$ on $[1,4]$ is

> [!check]- Solution
> 
> $$f(c)=\frac13\int_1^4\sqrt x dx=\frac13\cdot\frac23\big(8-1\big)=\frac{14}{9}\Rightarrow\sqrt c=\frac{14}{9}\Rightarrow c=\frac{196}{81}$$ **Answer:** $\color{red}{\boxed{\tfrac{196}{81}}}$

**22)** The average value of $f(x)=\dfrac{4(x^2+1)}{x^2}$ on $[1,4]$ is

> [!check]- Solution
> 
> $f(x)=4+4x^{-2}$: $$\frac13\int_1^4(4+4x^{-2}) dx=\frac13\Big[4x-\frac4x\Big]_1^4=\frac13\big[(16-1)-(4-4)\big]=5$$ **Answer:** $\color{red}{\boxed{5}}$

**23)** If $F(x)=\displaystyle\int_0^{x^3}\sin t^2 dt$, then $\sqrt[3]{\tfrac6\pi} F'\Big(\sqrt[6]{\tfrac\pi6}\Big)=$

> [!check]- Solution
> 
> $F'(x)=\sin(x^6)\cdot3x^2$. At $x=(\pi/6)^{1/6}$: $x^6=\frac\pi6$, $3x^2=3(\pi/6)^{1/3}$. $$\sqrt[3]{\tfrac6\pi}\cdot\sin\tfrac\pi6\cdot3\sqrt[3]{\tfrac\pi6}=\frac12\cdot3=\frac32$$ **Answer:** $\color{red}{\boxed{\tfrac32}}$

**24)** $g(x)=\int_0^xf(t) dt$ where the graph of $f$ is the broken line $(0,0)\to(2,-4)\to(4,0)\to(5,4)\to(7,4)\to(8,0)$. The largest open interval on which $g$ is decreasing is

> [!check]- Solution
> 
> $g'(x)=f(x)$, so $g$ decreases where $f<0$, which is $(0,4)$. **Answer:** $\color{red}{\boxed{(0,4)}}$

## 5.5 Integration by Substitution (24 problems)

**1)** $\displaystyle\int t\sqrt{t^2+2} dt$

> [!check]- Solution
> 
> $u=t^2+2,\ du=2t dt$: $\ \frac12\int u^{1/2}du=\frac13u^{3/2}+C$. **Answer:** $\color{red}{\boxed{\tfrac13(t^2+2)^{3/2}+C}}$

**2)** $\displaystyle\int\frac{6x^2}{(4x^3-9)^3} dx$

> [!check]- Solution
> 
> $u=4x^3-9,\ du=12x^2dx$: $\ \frac12\int u^{-3}du=-\frac{1}{4u^2}+C$. **Answer:** $\color{red}{\boxed{-\dfrac{1}{4(4x^3-9)^2}+C}}$

**3)** $\displaystyle\int\frac{\sin x}{\cos^3x} dx$

> [!check]- Solution
> 
> $u=\cos x,\ du=-\sin x dx$: $\ -\int u^{-3}du=\frac{1}{2u^2}+C=\frac12\sec^2x+C$. **Answer:** $\color{red}{\boxed{\tfrac12\sec^2x+C}}$

**4)** $\displaystyle\int\frac{2e^x-2e^{-x}}{(e^x+e^{-x})^2} dx$

> [!check]- Solution
> 
> $u=e^x+e^{-x},\ du=(e^x-e^{-x}) dx$: $\ 2\int u^{-2}du=-\frac2u+C$. **Answer:** $\color{red}{\boxed{-\dfrac{2}{e^x+e^{-x}}+C}}$

**5)** $\displaystyle\int\ln\big(e^{2x-1}\big) dx$

> [!check]- Solution
> 
> $\ln(e^{2x-1})=2x-1$, so $\int(2x-1) dx=x^2-x+C$. **Answer:** $\color{red}{\boxed{x^2-x+C}}$

**6)** Find $f$ with $f'(x)=\sec^2(2x)$ whose graph passes through $\big(\frac\pi2,2\big)$.

> [!check]- Solution
> 
> $f(x)=\frac12\tan(2x)+C$; $\ f\big(\frac\pi2\big)=\frac12\tan\pi+C=C=2$. **Answer:** $\color{red}{\boxed{f(x)=\tfrac12\tan(2x)+2}}$

**7)** $\displaystyle\int(x+1)\sqrt{2-x} dx$ (change of variables)

> [!check]- Solution
> 
> $u=2-x\Rightarrow x=2-u,\ x+1=3-u,\ dx=-du$: $$-\int(3-u)u^{1/2}du=-2u^{3/2}+\frac25u^{5/2}+C=\frac25u^{3/2}(u-5)+C=-\frac25(2-x)^{3/2}(x+3)+C$$
> 
> **Answer:** $\color{red}{\boxed{-\tfrac25(2-x)^{3/2}(x+3)+C}}$

**8)** $\displaystyle\int_1^9\frac{1}{\sqrt x (1+\sqrt x)^2} dx$

> [!check]- Solution
> 
> $u=1+\sqrt x,\ du=\frac{dx}{2\sqrt x}$; $x=1\to u=2,\ x=9\to u=4$: $$2\int_2^4u^{-2}du=2\Big[-\frac1u\Big]_2^4=2\Big(-\frac14+\frac12\Big)=\frac12$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac12}}$

**9)** Find the area bounded by $y=xe^{-x^2/4},\ y=0,\ x=0,\ x=\sqrt6$.

> [!check]- Solution
> 
> $u=-\frac{x^2}{4},\ du=-\frac x2dx$: $$\int_0^{\sqrt6}xe^{-x^2/4}dx=\Big[-2e^{-x^2/4}\Big]_0^{\sqrt6}=2-2e^{-3/2}\approx1.554$$ **Answer:** $\color{red}{\boxed{2-2e^{-3/2}\approx1.554}}$

**10)** Use even/odd properties: $\displaystyle\int_{-2}^{2}x(x^2+1)^3 dx$

> [!check]- Solution
> 
> $g(x)=x(x^2+1)^3$ satisfies $g(-x)=-g(x)$ (odd) and the interval is symmetric. **Answer:** $\color{red}{\boxed{0}}$

**11)** Write $\displaystyle\int_{-\pi/2}^{\pi/2}(\sin4x+\cos4x) dx$ as an odd part plus an even part and evaluate.

> [!check]- Solution
> 
> $\sin4x$ is odd ⇒ its integral is $0$. $\cos4x$ is even: $$2\int_0^{\pi/2}\cos4x dx=2\Big[\frac{\sin4x}{4}\Big]_0^{\pi/2}=\frac12(\sin2\pi-0)=0$$
> 
> **Answer:** $\color{red}{\boxed{0}}$

**12)** $\displaystyle\int\frac{9x^2}{\sqrt{3x+1}} dx=$

> [!check]- Solution
> 
> $u=3x+1\Rightarrow x=\frac{u-1}{3},\ dx=\frac{du}{3}$, and $9x^2=(u-1)^2$: $$\frac13\int\frac{u^2-2u+1}{u^{1/2}}du=\frac13\Big[\frac25u^{5/2}-\frac43u^{3/2}+2u^{1/2}\Big]+C=\frac2{15}u^{5/2}-\frac49u^{3/2}+\frac23u^{1/2}+C$$ **Answer:** $\color{red}{\boxed{\tfrac2{15}(3x+1)^{5/2}-\tfrac49(3x+1)^{3/2}+\tfrac23\sqrt{3x+1}+C}}$

**13)** $\displaystyle\int16x^5\sqrt{4x^2+1} dx=$

> [!check]- Solution
> 
> $u=4x^2+1,\ du=8x dx,\ x^2=\frac{u-1}{4}$: $\ 16x^5dx=16\big(\frac{u-1}{4}\big)^2\frac{du}{8}=\frac18(u-1)^2du$. $$\frac18\int(u^{5/2}-2u^{3/2}+u^{1/2}) du=\frac1{28}u^{7/2}-\frac1{10}u^{5/2}+\frac1{12}u^{3/2}+C$$ **Answer:** $\color{red}{\boxed{\tfrac1{28}(4x^2+1)^{7/2}-\tfrac1{10}(4x^2+1)^{5/2}+\tfrac1{12}(4x^2+1)^{3/2}+C}}$

**14)** $\displaystyle\int_1^2\sqrt{\frac{x^2-1}{x^8}} dx=$

> [!check]- Solution
> 
> $\sqrt{\frac{x^2-1}{x^8}}=\frac{1}{x^3}\sqrt{1-\frac1{x^2}}$. Let $u=1-x^{-2},\ du=2x^{-3}dx$; $x=1\to0,\ x=2\to\frac34$: $$\frac12\int_0^{3/4}u^{1/2}du=\frac13\Big(\frac34\Big)^{3/2}=\frac13\cdot\frac{3\sqrt3}{8}=\frac{\sqrt3}{8}$$ **Answer:** $\color{red}{\boxed{\tfrac18\sqrt3}}$

**15)** $\displaystyle\int_{\pi^2/16}^{\pi^2/9}\frac{\sec^2(\sqrt x)\tan^2(\sqrt x)}{\sqrt x} dx=$

> [!check]- Solution
> 
> $u=\tan\sqrt x,\ du=\frac{\sec^2\sqrt x}{2\sqrt x}dx$; $x=\frac{\pi^2}{16}\to u=1,\ x=\frac{\pi^2}{9}\to u=\sqrt3$: $$\int_1^{\sqrt3}2u^2du=\frac23\big(3\sqrt3-1\big)=2\sqrt3-\frac23$$ **Answer:** $\color{red}{\boxed{2\sqrt3-\tfrac23}}$

**16)** $\displaystyle\int_{3/\pi}^{12/\pi}\frac{6\sin(3/x)}{x^2} dx=$

> [!check]- Solution
> 
> $u=\frac3x,\ du=-\frac3{x^2}dx$; $x=\frac3\pi\to u=\pi,\ x=\frac{12}\pi\to u=\frac\pi4$: $$-2\int_\pi^{\pi/4}\sin u du=2\int_{\pi/4}^{\pi}\sin u du=2\Big[-\cos u\Big]_{\pi/4}^{\pi}=2\Big(1+\frac{\sqrt2}{2}\Big)=2+\sqrt2$$ **Answer:** $\color{red}{\boxed{\sqrt2+2}}$

**17)** $\displaystyle\int_1^2x\Big(e^{x^2}-\frac1{2x}\Big)dx=$

> [!check]- Solution
> 
> $\int_1^2xe^{x^2}dx=\frac12\big[e^{x^2}\big]_1^2=\frac12(e^4-e)$ and $\int_1^2\frac12 dx=\frac12$. **Answer:** $\color{red}{\boxed{\tfrac12(e^4-e-1)}}$

**18)** $\displaystyle\int_0^1x(1-x)^9 dx=$

> [!check]- Solution
> 
> $u=1-x,\ x=1-u,\ dx=-du$; $x=0\to1,\ x=1\to0$: $$\int_0^1(1-u)u^9du=\frac1{10}-\frac1{11}=\frac1{110}$$ **Answer:** $\color{red}{\boxed{\tfrac1{110}}}$

**19)** $\displaystyle\int\frac{\csc^2x}{\cot^3x} dx=$

> [!check]- Solution
> 
> $u=\cot x,\ du=-\csc^2x dx$: $\ -\int u^{-3}du=\frac{1}{2u^2}+C=\frac12\tan^2x+C$. Since $\tan^2x=\sec^2x-1$, this equals $\frac12\sec^2x+C'$. **Answer:** $\color{red}{\boxed{\tfrac12\sec^2x+C}}$

**20)** $\displaystyle\int\frac{2x-1}{\sqrt{x+3}} dx=$

> [!check]- Solution
> 
> $u=x+3,\ x=u-3$: $\int\frac{2u-7}{\sqrt u}du=\frac43u^{3/2}-14u^{1/2}+C=u^{1/2}\Big(\frac43u-14\Big)+C$. With $u=x+3$: $\sqrt{x+3}\big(\frac43x-10\big)=\frac23(2x-15)\sqrt{x+3}$. **Answer:** $\color{red}{\boxed{\tfrac23(2x-15)\sqrt{x+3}+C}}$

**21)** $\displaystyle\int15x\sqrt{1-x} dx=$

> [!check]- Solution
> 
> $u=1-x,\ x=1-u,\ dx=-du$: $$-15\int(1-u)u^{1/2}du=-15\Big[\frac23u^{3/2}-\frac25u^{5/2}\Big]+C=6u^{5/2}-10u^{3/2}+C$$ **Answer:** $\color{red}{\boxed{6(1-x)^{5/2}-10(1-x)^{3/2}+C}}$

**22)** If $f$ is even and $\int_0^1f(x) dx=5$, then $\displaystyle\int_{-1}^1(3x-4)f(x) dx=$

> [!check]- Solution
> 
> $xf(x)$ is odd ⇒ $\int_{-1}^1xf=0$; $f$ even ⇒ $\int_{-1}^1f=2(5)=10$. $$3(0)-4(10)=-40$$ **Answer:** $\color{red}{\boxed{-40}}$

**23)** $f$ is odd and continuous, $\int_0^1f=2$ and $\int_{-1}^3f=4$. Then $\displaystyle\int_{-3}^1f(x) dx=$

> [!check]- Solution
> 
> Odd ⇒ $\int_{-1}^1f=0$, so $\int_1^3f=\int_{-1}^3f-0=4$ and $\int_{-3}^{-1}f=-\int_1^3f=-4$. $$\int_{-3}^1f=\int_{-3}^{-1}f+\int_{-1}^1f=-4+0=-4$$ **Answer:** $\color{red}{\boxed{-4}}$

**24)** $f$ is odd and continuous with $\int_{-3}^6f=9$ and $\int_0^3f=-3$. Then $\displaystyle\int_0^6f(x) dx=$

> [!check]- Solution
> 
> $\int_{-3}^3f=0\Rightarrow\int_3^6f=9$. Then $\int_0^6f=\int_0^3f+\int_3^6f=-3+9=6$. **Answer:** $\color{red}{\boxed{6}}$

## 5.7 The Natural Logarithmic Function — Integration (24 problems)

**1)** $\displaystyle\int\frac{x^3-8x}{x^2} dx$

> [!check]- Solution
> 
> $\frac{x^3-8x}{x^2}=x-\frac8x$, so $\int\big(x-\frac8x\big)dx=\frac{x^2}{2}-8\ln|x|+C$. **Answer:** $\color{red}{\boxed{\tfrac{x^2}{2}-8\ln|x|+C}}$

**2)** $\displaystyle\int\frac{x^2+2x+3}{x^3+3x^2+9x} dx$

> [!check]- Solution
> 
> $u=x^3+3x^2+9x,\ du=3(x^2+2x+3) dx$: $\ \frac13\int\frac{du}{u}=\frac13\ln|u|+C$. **Answer:** $\color{red}{\boxed{\tfrac13\ln|x^3+3x^2+9x|+C}}$

**3)** $\displaystyle\int\frac{x(x-2)}{(x-1)^3} dx$

> [!check]- Solution
> 
> $u=x-1$: $x(x-2)=(u+1)(u-1)=u^2-1$. $$\int\frac{u^2-1}{u^3}du=\int\Big(\frac1u-u^{-3}\Big)du=\ln|u|+\frac{1}{2u^2}+C$$
> 
> **Answer:** $\color{red}{\boxed{\ln|x-1|+\dfrac{1}{2(x-1)^2}+C}}$

**4)** $\displaystyle\int\frac{\sqrt[3]x}{\sqrt[3]x-1} dx$ (hint: let $u$ be the denominator)

> [!check]- Solution
> 
> $u=x^{1/3}-1\Rightarrow x=(u+1)^3,\ dx=3(u+1)^2du$: $$\int\frac{u+1}{u}\cdot3(u+1)^2du=3\int\Big(u^2+3u+3+\frac1u\Big)du=u^3+\tfrac92u^2+9u+3\ln|u|+C$$ Back-substituting and absorbing constants: $x+\frac32x^{2/3}+3x^{1/3}+3\ln|x^{1/3}-1|+C$. Check: with $w=x^{1/3}$ the derivative is $1+\frac1w+\frac1{w^2}+\frac{1}{w^2(w-1)}=\frac{w}{w-1}$ ✓ **Answer:** $\color{red}{\boxed{x+\tfrac32x^{2/3}+3x^{1/3}+3\ln\big|\sqrt[3]x-1\big|+C}}$

**5)** $\displaystyle\int\cot\frac\theta3 d\theta$

> [!check]- Solution
> 
> $u=\frac\theta3,\ d\theta=3 du$: $\ 3\int\cot u du=3\ln|\sin u|+C$. **Answer:** $\color{red}{\boxed{3\ln\big|\sin\tfrac\theta3\big|+C}}$

**6)** $\displaystyle\int\frac{\sec x\tan x}{\sec x-1} dx$

> [!check]- Solution
> 
> $u=\sec x-1,\ du=\sec x\tan x dx$: $\ \int\frac{du}{u}=\ln|u|+C$. **Answer:** $\color{red}{\boxed{\ln|\sec x-1|+C}}$

**7)** Find the particular solution: $f''(x)=\frac{2}{x^2},\ f'(1)=1,\ f(1)=1,\ x>0$.

> [!check]- Solution
> 
> $f'(x)=-\frac2x+C_1$, $f'(1)=-2+C_1=1\Rightarrow C_1=3$. $f(x)=-2\ln x+3x+C_2$, $f(1)=3+C_2=1\Rightarrow C_2=-2$. **Answer:** $\color{red}{\boxed{f(x)=-2\ln x+3x-2}}$

**8)** $\displaystyle\int_0^2\frac{x^2-2}{x+1} dx$

> [!check]- Solution
> 
> Divide: $\frac{x^2-2}{x+1}=x-1-\frac{1}{x+1}$. $$\Big[\frac{x^2}{2}-x-\ln|x+1|\Big]_0^2=(2-2-\ln3)-0=-\ln3$$
> 
> **Answer:** $\color{red}{\boxed{-\ln3}}$

**9)** Find the area bounded by $y=\frac{5x}{x^2+2},\ x=1,\ x=5,\ y=0$.

> [!check]- Solution
> 
> $$\int_1^5\frac{5x}{x^2+2}dx=\frac52\Big[\ln(x^2+2)\Big]_1^5=\frac52\ln\frac{27}{3}=\frac52\ln9=5\ln3$$ **Answer:** $\color{red}{\boxed{5\ln3\approx5.493}}$

**10)** Find the average value of $f(x)=\sec\frac{\pi x}{6}$ on $[0,2]$.

> [!check]- Solution
> 
> $$\frac12\int_0^2\sec\frac{\pi x}{6}dx=\frac12\cdot\frac6\pi\Big[\ln\Big|\sec\frac{\pi x}{6}+\tan\frac{\pi x}{6}\Big|\Big]_0^2=\frac3\pi\ln(2+\sqrt3)$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac3\pi\ln(2+\sqrt3)\approx1.258}}$

**11)** Find $x$ such that $\displaystyle\int_1^x\frac3t dt=\int_{1/4}^x\frac1t dt$.

> [!check]- Solution
> 
> $3\ln x=\ln x-\ln\frac14=\ln x+\ln4\Rightarrow2\ln x=\ln4\Rightarrow x=2$.
> 
> **Answer:** $\color{red}{\boxed{x=2}}$

**12)** $\displaystyle\int_e^{e^e}\frac{[\ln(\ln x)]^3}{x\ln x} dx=$

> [!check]- Solution
> 
> $u=\ln(\ln x),\ du=\frac{dx}{x\ln x}$; $x=e\to u=0,\ x=e^e\to u=1$: $\ \int_0^1u^3du=\frac14$. **Answer:** $\color{red}{\boxed{\tfrac14}}$

**13)** $\displaystyle\int_1^{27}\frac{1}{x^{2/3}(2+\sqrt[3]x)} dx=$

> [!check]- Solution
> 
> $u=2+x^{1/3},\ du=\frac13x^{-2/3}dx$; $x=1\to3,\ x=27\to5$: $\ \int_3^5\frac{3 du}{u}=3\ln\frac53$. **Answer:** $\color{red}{\boxed{3\ln\tfrac53}}$

**14)** $\displaystyle\int\sec^2x \tan(\tan x) dx=$

> [!check]- Solution
> 
> $u=\tan x,\ du=\sec^2x dx$: $\ \int\tan u du=\ln|\sec u|+C$. **Answer:** $\color{red}{\boxed{\ln|\sec(\tan x)|+C}}$

**15)** $\displaystyle\int_1^e\frac{1}{x+x\ln x} dx=$

> [!check]- Solution
> 
> $\frac{1}{x(1+\ln x)}$; $u=1+\ln x,\ du=\frac{dx}x$; $x=1\to1,\ x=e\to2$: $\ \int_1^2\frac{du}{u}=\ln2$. **Answer:** $\color{red}{\boxed{\ln2}}$

**16)** $\displaystyle\int\sec^2x \cot(\tan x) dx=$

> [!check]- Solution
> 
> $u=\tan x$: $\int\cot u du=\ln|\sin u|+C$. **Answer:** $\color{red}{\boxed{\ln|\sin(\tan x)|+C}}$

**17)** $\displaystyle\int\frac{\cos x}{\sin x \ln(\sin x)} dx=$

> [!check]- Solution
> 
> $w=\ln(\sin x),\ dw=\frac{\cos x}{\sin x}dx$: $\ \int\frac{dw}{w}=\ln|w|+C$. **Answer:** $\color{red}{\boxed{\ln|\ln(\sin x)|+C}}$

**18)** $\displaystyle\int_0^3\frac{x^2+2}{x+1} dx=$

> [!check]- Solution
> 
> $\frac{x^2+2}{x+1}=x-1+\frac{3}{x+1}$: $$\Big[\frac{x^2}2-x+3\ln|x+1|\Big]_0^3=\frac92-3+3\ln4=\frac32+3\ln4$$ **Answer:** $\color{red}{\boxed{\tfrac32+3\ln4}}$

**19)** $\displaystyle\int\frac{x^3-4x^2-4x+20}{x^2-5} dx=$

> [!check]- Solution
> 
> $(x^2-5)(x-4)=x^3-4x^2-5x+20$, remainder $x$: integrand $=x-4+\frac{x}{x^2-5}$. $$\frac{x^2}{2}-4x+\frac12\ln|x^2-5|+C$$ **Answer:** $\color{red}{\boxed{\tfrac{x^2}2-4x+\tfrac12\ln|x^2-5|+C}}$

**20)** $\displaystyle\int_{\pi/8}^{\pi/4}(\csc2\theta-\cot2\theta) d\theta=$

> [!check]- Solution
> 
> $\int\csc2\theta=-\frac12\ln|\csc2\theta+\cot2\theta|$, $\int\cot2\theta=\frac12\ln|\sin2\theta|$. So the antiderivative is $-\frac12\ln\big|(\csc2\theta+\cot2\theta)\sin2\theta\big|=-\frac12\ln|1+\cos2\theta|$. $$\Big[-\tfrac12\ln(1+\cos2\theta)\Big]_{\pi/8}^{\pi/4}=-\tfrac12\ln1+\tfrac12\ln\Big(1+\tfrac{\sqrt2}{2}\Big)=\tfrac12\ln\Big(1+\tfrac{\sqrt2}{2}\Big)$$ **Answer:** $\color{red}{\boxed{\tfrac12\ln\big(1+\tfrac{\sqrt2}2\big)}}$

**21)** $\displaystyle\int_0^\pi\Big(1-\tan\frac\theta4\Big)d\theta=$

> [!check]- Solution
> 
> $\int\tan\frac\theta4 d\theta=-4\ln\big|\cos\frac\theta4\big|$: $$\Big[\theta+4\ln\cos\tfrac\theta4\Big]_0^\pi=\pi+4\ln\tfrac{\sqrt2}{2}=\pi-2\ln2$$ **Answer:** $\color{red}{\boxed{\pi-2\ln2}}$

**22)** $\displaystyle\int\frac{\sec(2\ln t)+\tan(2\ln t)}{t} dt=$

> [!check]- Solution
> 
> $u=2\ln t,\ du=\frac2t dt$: $\frac12\int(\sec u+\tan u) du=\frac12\big[\ln|\sec u+\tan u|-\ln|\cos u|\big]$. $\frac{\sec u+\tan u}{\cos u}=\frac{1+\sin u}{\cos^2u}=\frac{1+\sin u}{1-\sin^2u}=\frac1{1-\sin u}$, so the result is $-\frac12\ln|1-\sin u|+C$. **Answer:** $\color{red}{\boxed{-\tfrac12\ln|1-\sin(2\ln t)|+C}}$

**23)** If the average value of $f(x)=\frac{2\ln x}{x}$ on $[1,b]$ is $\frac{1}{e-1}$, then $b=$

> [!check]- Solution
> 
> $\int_1^b\frac{2\ln x}{x}dx=(\ln b)^2$, so $\frac{(\ln b)^2}{b-1}=\frac1{e-1}$, which $b=e$ satisfies. **Answer:** $\color{red}{\boxed{b=e}}$

**24)** $\displaystyle\int_e^{e^2}\frac{1}{x(\ln x^2)^3} dx=$

> [!check]- Solution
> 
> $u=\ln x^2=2\ln x,\ du=\frac2xdx$; $x=e\to2,\ x=e^2\to4$: $$\frac12\int_2^4u^{-3}du=\frac12\Big[-\frac1{2u^2}\Big]_2^4=\frac12\Big(\frac18-\frac1{32}\Big)=\frac3{64}$$ **Answer:** $\color{red}{\boxed{\tfrac3{64}}}$

## 5.8 Inverse Trigonometric Functions — Integration (24 problems)

**1)** $\displaystyle\int\frac{12}{1+9x^2} dx$

> [!check]- Solution
> 
> $u=3x,\ du=3 dx$: $\ 4\int\frac{du}{1+u^2}=4\arctan u+C$. **Answer:** $\color{red}{\boxed{4\arctan(3x)+C}}$

**2)** $\displaystyle\int\frac{5}{x\sqrt{9x^2-11}} dx$

> [!check]- Solution
> 
> $u=3x\Rightarrow\frac{dx}{x}=\frac{du}{u}$: $\ 5\int\frac{du}{u\sqrt{u^2-11}}=\frac{5}{\sqrt{11}} \mathrm{arcsec}\frac{|u|}{\sqrt{11}}+C$. **Answer:** $\color{red}{\boxed{\dfrac{5}{\sqrt{11}} \mathrm{arcsec}\dfrac{|3x|}{\sqrt{11}}+C}}$

**3)** $\displaystyle\int\frac{1}{\sqrt x \sqrt{1-x}} dx$

> [!check]- Solution
> 
> $u=\sqrt x,\ du=\frac{dx}{2\sqrt x}$, $1-x=1-u^2$: $\ 2\int\frac{du}{\sqrt{1-u^2}}=2\arcsin u+C$. **Answer:** $\color{red}{\boxed{2\arcsin\sqrt x+C}}$

**4)** $\displaystyle\int\frac{x-3}{x^2+1} dx$

> [!check]- Solution
> 
> $$\int\frac{x}{x^2+1}dx-3\int\frac{dx}{x^2+1}=\frac12\ln(x^2+1)-3\arctan x+C$$ **Answer:** $\color{red}{\boxed{\tfrac12\ln(x^2+1)-3\arctan x+C}}$

**5)** $\displaystyle\int_0^{1/6}\frac{3}{\sqrt{1-9x^2}} dx$

> [!check]- Solution
> 
> $\big[\arcsin3x\big]_0^{1/6}=\arcsin\frac12=\frac\pi6$. **Answer:** $\color{red}{\boxed{\tfrac\pi6}}$

**6)** $\displaystyle\int_0^{1/\sqrt2}\frac{\arcsin x}{\sqrt{1-x^2}} dx$

> [!check]- Solution
> 
> $u=\arcsin x,\ du=\frac{dx}{\sqrt{1-x^2}}$; $x=0\to0,\ x=\frac1{\sqrt2}\to\frac\pi4$: $\ \int_0^{\pi/4}u du=\frac12\Big(\frac\pi4\Big)^2$. **Answer:** $\color{red}{\boxed{\tfrac{\pi^2}{32}}}$

**7)** $\displaystyle\int\frac{dx}{\sqrt{-2x^2+8x+4}}$

> [!check]- Solution
> 
> $-2x^2+8x+4=-2(x^2-4x-2)=2\big[6-(x-2)^2\big]$: $$\frac{1}{\sqrt2}\int\frac{dx}{\sqrt{6-(x-2)^2}}=\frac{1}{\sqrt2}\arcsin\frac{x-2}{\sqrt6}+C=\frac{\sqrt2}{2}\arcsin\Big[\frac{\sqrt6}{6}(x-2)\Big]+C$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac{\sqrt2}2\arcsin\big[\tfrac{\sqrt6}6(x-2)\big]+C}}$

**8)** $\displaystyle\int\frac{\sqrt{x-2}}{x+1} dx$ with $u=\sqrt{x-2}$

> [!check]- Solution
> 
> $x=u^2+2,\ dx=2u du,\ x+1=u^2+3$: $$\int\frac{2u^2}{u^2+3}du=2\int\Big(1-\frac{3}{u^2+3}\Big)du=2u-2\sqrt3\arctan\frac{u}{\sqrt3}+C$$
> 
> **Answer:** $\color{red}{\boxed{2\sqrt{x-2}-2\sqrt3\arctan\sqrt{\tfrac{x-2}{3}}+C}}$

**9)** Find, if possible with the methods so far: (a) $\int\frac{dx}{1+x^4}$ (b) $\int\frac{x dx}{1+x^4}$ (c) $\int\frac{x^3 dx}{1+x^4}$

> [!check]- Solution
> 
> (a) No substitution fits — it needs partial fractions (Ch. 8). (b) $u=x^2$: $\frac12\int\frac{du}{1+u^2}=\frac12\arctan x^2+C$. (c) $u=1+x^4$: $\frac14\int\frac{du}{u}=\frac14\ln(1+x^4)+C$. **Answer:** $\color{red}{\boxed{\text{(a) not yet}\quad\text{(b) }\tfrac12\arctan x^2+C\quad\text{(c) }\tfrac14\ln(1+x^4)+C}}$

**10)** Find the area under $y=\frac{4e^x}{1+e^{2x}}$ from $x=0$ to $x=\ln\sqrt3$.

> [!check]- Solution
> 
> $u=e^x$: $\int\frac{4e^x}{1+e^{2x}}dx=4\arctan e^x$. $$4\Big[\arctan e^x\Big]_0^{\ln\sqrt3}=4\Big(\frac\pi3-\frac\pi4\Big)=\frac\pi3$$ **Answer:** $\color{red}{\boxed{\tfrac\pi3}}$

**11)** $\displaystyle\int_4^6\frac{2x-5}{\sqrt{8x-x^2}} dx=$

> [!check]- Solution
> 
> $8x-x^2=16-(x-4)^2$. Let $u=x-4$ ($0\to2$): $2x-5=2u+3$. $$\int_0^2\frac{2u}{\sqrt{16-u^2}}du+\int_0^2\frac{3}{\sqrt{16-u^2}}du=\Big[-2\sqrt{16-u^2}\Big]_0^2+3\Big[\arcsin\frac u4\Big]_0^2=(-4\sqrt3+8)+\frac\pi2$$ **Answer:** $\color{red}{\boxed{-4\sqrt3+8+\tfrac\pi2}}$

**12)** $\displaystyle\int\frac{3x^2+3x+16}{x^2+4} dx=$

> [!check]- Solution
> 
> Divide: $\frac{3x^2+3x+16}{x^2+4}=3+\frac{3x+4}{x^2+4}=3+\frac{3x}{x^2+4}+\frac{4}{x^2+4}$. $$3x+\frac32\ln(x^2+4)+4\cdot\frac12\tan^{-1}\frac x2+C$$ **Answer:** $\color{red}{\boxed{3x+\tfrac32\ln(4+x^2)+2\tan^{-1}\tfrac x2+C}}$

**13)** $\displaystyle\int_0^{\sqrt2}\frac{2x^5+9x}{x^4+4} dx=$

> [!check]- Solution
> 
> Divide: $\frac{2x^5+9x}{x^4+4}=2x+\frac{x}{x^4+4}$. For the second, $u=x^2$: $\frac12\int\frac{du}{u^2+4}=\frac14\tan^{-1}\frac{x^2}2$. $$\Big[x^2+\tfrac14\tan^{-1}\tfrac{x^2}{2}\Big]_0^{\sqrt2}=2+\tfrac14\cdot\tfrac\pi4=2+\tfrac\pi{16}$$ **Answer:** $\color{red}{\boxed{2+\tfrac\pi{16}}}$

**14)** $\displaystyle\int_0^{\ln\sqrt3}\frac{e^x}{\tan^{-1}(e^x) (1+e^{2x})} dx=$

> [!check]- Solution
> 
> $u=\tan^{-1}(e^x),\ du=\frac{e^x}{1+e^{2x}}dx$; $x=0\to\frac\pi4,\ x=\ln\sqrt3\to\frac\pi3$: $$\int_{\pi/4}^{\pi/3}\frac{du}{u}=\ln\frac{\pi/3}{\pi/4}=\ln\frac43$$ **Answer:** $\color{red}{\boxed{\ln\tfrac43}}$

**15)** $\displaystyle\int_{\ln(\pi/2)}^{\ln(2\pi)}\frac{\sin(e^x)}{[1+\cos^2(e^x)] e^{-x}} dx=$

> [!check]- Solution
> 
> The integrand is $\frac{e^x\sin(e^x)}{1+\cos^2(e^x)}$. Let $u=\cos(e^x),\ du=-e^x\sin(e^x) dx$; limits $\cos\frac\pi2=0\to\cos2\pi=1$: $$\int_0^1\frac{-du}{1+u^2}=-\Big[\tan^{-1}u\Big]_0^1=-\frac\pi4$$ **Answer:** $\color{red}{\boxed{-\tfrac\pi4}}$

**16)** $\displaystyle\int_0^{1/2}\frac{1+x}{\sqrt{1-x^2}} dx=$

> [!check]- Solution
> 
> $$\int_0^{1/2}\frac{dx}{\sqrt{1-x^2}}+\int_0^{1/2}\frac{x dx}{\sqrt{1-x^2}}=\Big[\sin^{-1}x\Big]_0^{1/2}+\Big[-\sqrt{1-x^2}\Big]_0^{1/2}=\frac\pi6-\frac{\sqrt3}{2}+1$$ **Answer:** $\color{red}{\boxed{\tfrac\pi6-\tfrac{\sqrt3}2+1}}$

**17)** $\displaystyle\int_0^{(\ln3)/4}\frac{e^{2x}}{e^{4x}+1} dx=$

> [!check]- Solution
> 
> $u=e^{2x},\ du=2e^{2x}dx$; $x=0\to1,\ x=\frac{\ln3}{4}\to e^{(\ln3)/2}=\sqrt3$: $$\frac12\int_1^{\sqrt3}\frac{du}{u^2+1}=\frac12\Big(\frac\pi3-\frac\pi4\Big)=\frac\pi{24}$$ **Answer:** $\color{red}{\boxed{\tfrac\pi{24}}}$

**18)** $\displaystyle\int_{-2}^{3}\frac{dx}{x^2+4x+8}=$

> [!check]- Solution
> 
> $x^2+4x+8=(x+2)^2+4$: $$\frac12\Big[\arctan\frac{x+2}{2}\Big]_{-2}^{3}=\frac12\Big(\arctan\frac52-0\Big)$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac12\arctan\tfrac52}}$

**19)** $\displaystyle\int_2^3\frac{2x-3}{\sqrt{4x-x^2}} dx=$

> [!check]- Solution
> 
> $4x-x^2=4-(x-2)^2$; $u=x-2$ ($0\to1$), $2x-3=2u+1$: $$\Big[-2\sqrt{4-u^2}+\arcsin\frac u2\Big]_0^1=(-2\sqrt3+\tfrac\pi6)-(-4)=4-2\sqrt3+\tfrac\pi6$$ **Answer:** $\color{red}{\boxed{4-2\sqrt3+\tfrac\pi6}}$

**20)** $\displaystyle\int\frac{1}{x\sqrt{x^4-4}} dx=$

> [!check]- Solution
> 
> $u=x^2,\ du=2x dx\Rightarrow\frac{dx}{x}=\frac{du}{2u}$: $$\frac12\int\frac{du}{u\sqrt{u^2-4}}=\frac12\cdot\frac12\sec^{-1}\frac{u}{2}+C=\frac14\sec^{-1}\frac{x^2}{2}+C$$ **Answer:** $\color{red}{\boxed{\tfrac14\sec^{-1}\tfrac{x^2}2+C}}$

**21)** $\displaystyle\int_3^{\sqrt3}\frac{dx}{x\sqrt{4x^2-9}}=$

> [!check]- Solution
> 
> $u=2x$, $\frac{dx}{x}=\frac{du}{u}$; $x=3\to6,\ x=\sqrt3\to2\sqrt3$: $$\frac13\Big[\mathrm{arcsec}\frac u3\Big]_6^{2\sqrt3}=\frac13\Big(\mathrm{arcsec}\tfrac{2}{\sqrt3}-\mathrm{arcsec} 2\Big)=\frac13\Big(\frac\pi6-\frac\pi3\Big)=-\frac\pi{18}$$ **Answer:** $\color{red}{\boxed{-\tfrac\pi{18}}}$

**22)** $\displaystyle\int_0^{1/\sqrt2}\frac{\cos^{-1}x}{\sqrt{1-x^2}} dx=$

> [!check]- Solution
> 
> $u=\cos^{-1}x,\ du=-\frac{dx}{\sqrt{1-x^2}}$; $x=0\to\frac\pi2,\ x=\frac1{\sqrt2}\to\frac\pi4$: $$-\int_{\pi/2}^{\pi/4}u du=\Big[\frac{u^2}{2}\Big]_{\pi/4}^{\pi/2}=\frac{\pi^2}{8}-\frac{\pi^2}{32}=\frac{3\pi^2}{32}$$ **Answer:** $\color{red}{\boxed{\tfrac{3\pi^2}{32}}}$

**23)** $\displaystyle\int\sqrt{e^t-3} dt=$

> [!check]- Solution
> 
> $u=\sqrt{e^t-3}\Rightarrow e^t=u^2+3,\ dt=\frac{2u du}{u^2+3}$: $$\int\frac{2u^2}{u^2+3}du=2u-\frac{6}{\sqrt3}\tan^{-1}\frac u{\sqrt3}+c=2u-2\sqrt3\tan^{-1}\frac{u}{\sqrt3}+c$$ **Answer:** $\color{red}{\boxed{2\sqrt{e^t-3}-2\sqrt3\tan^{-1}\sqrt{\tfrac{e^t-3}{3}}+c}}$

**24)** The area of the region enclosed by $y=\frac{2}{\sqrt{4-x^2}},\ y=\frac{-2}{\sqrt{4-x^2}},\ x=-1,\ x=1$ is

> [!check]- Solution
> 
> $$\int_{-1}^1\frac{4}{\sqrt{4-x^2}}dx=4\Big[\arcsin\frac x2\Big]_{-1}^{1}=4\Big(\frac\pi6+\frac\pi6\Big)=\frac{4\pi}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{4\pi}3}}$

## 5.9 Hyperbolic Functions — Integration (10 problems)

**1)** $\displaystyle\int\cosh^2(x-1)\sinh(x-1) dx$

> [!check]- Solution
> 
> $u=\cosh(x-1),\ du=\sinh(x-1) dx$: $\ \int u^2du=\frac{u^3}{3}+C$. **Answer:** $\color{red}{\boxed{\tfrac13\cosh^3(x-1)+C}}$

**2)** $\displaystyle\int\mathrm{sech}^3x\tanh x dx$

> [!check]- Solution
> 
> $u=\mathrm{sech} x,\ du=-\mathrm{sech} x\tanh x dx$: $\ \int\mathrm{sech}^2x (\mathrm{sech} x\tanh x dx)=-\int u^2du=-\frac{u^3}{3}+C$. **Answer:** $\color{red}{\boxed{-\tfrac13 \mathrm{sech}^3x+C}}$

**3)** $\displaystyle\int_0^{\ln2}\tanh x dx$

> [!check]- Solution
> 
> $\int\tanh x dx=\ln(\cosh x)$, and $\cosh(\ln2)=\frac{2+\frac12}{2}=\frac54$: $$\ln\tfrac54-\ln1=\ln\tfrac54$$
> 
> **Answer:** $\color{red}{\boxed{\ln\tfrac54}}$

**4)** $\displaystyle\int_0^{\ln2}2e^{-x}\cosh x dx$

> [!check]- Solution
> 
> $2e^{-x}\cosh x=e^{-x}(e^x+e^{-x})=1+e^{-2x}$: $$\Big[x-\tfrac12e^{-2x}\Big]_0^{\ln2}=\Big(\ln2-\tfrac18\Big)-\Big(0-\tfrac12\Big)=\ln2+\tfrac38$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac38+\ln2}}$

**5)** $\displaystyle\int_0^{\ln2}2e^{-x}\sinh x dx=$

> [!check]- Solution
> 
> $2e^{-x}\sinh x=e^{-x}(e^x-e^{-x})=1-e^{-2x}$: $$\Big[x+\tfrac12e^{-2x}\Big]_0^{\ln2}=\ln2+\tfrac18-\tfrac12=\ln2-\tfrac38$$ **Answer:** $\color{red}{\boxed{\ln2-\tfrac38}}$

**6)** $\displaystyle\int\frac{\sinh x}{1+\sinh^2x} dx=$

> [!check]- Solution
> 
> $1+\sinh^2x=\cosh^2x$. With $u=\cosh x$: $\int\frac{du}{u^2}=-\frac1u+C=-\mathrm{sech} x+C$. **Answer:** $\color{red}{\boxed{-\mathrm{sech} x+C}}$

**7)** $\displaystyle\int_0^{\sqrt[3]{\ln2}}x^2 \mathrm{sech}^2(x^3) dx=$

> [!check]- Solution
> 
> $u=x^3$: $\frac13\int_0^{\ln2}\mathrm{sech}^2u du=\frac13\tanh(\ln2)$, and $\tanh(\ln2)=\frac{2-\frac12}{2+\frac12}=\frac35$. **Answer:** $\color{red}{\boxed{\tfrac15}}$

**8)** $\displaystyle\int_{-1}^{1}\mathrm{sech}^3x\tanh x dx=$

> [!check]- Solution
> 
> $\mathrm{sech}$ is even and $\tanh$ is odd, so the integrand is **odd** on a symmetric interval. (Or use B2: $\big[-\frac13\mathrm{sech}^3x\big]_{-1}^1=0$.) **Answer:** $\color{red}{\boxed{0}}$

**9)** $\displaystyle\int_0^{\ln3}\tanh x dx=$

> [!check]- Solution
> 
> $\big[\ln\cosh x\big]_0^{\ln3}=\ln\frac{3+\frac13}{2}=\ln\frac53$. **Answer:** $\color{red}{\boxed{\ln\tfrac53}}$

**10)** $\displaystyle\int_{1/2}^{1}\mathrm{sech}^2(2x-1) dx=$

> [!check]- Solution
> 
> $$\Big[\tfrac12\tanh(2x-1)\Big]_{1/2}^{1}=\tfrac12\tanh1-\tfrac12\tanh0=\tfrac12\tanh1$$ **Answer:** $\color{red}{\boxed{\tfrac12\tanh1}}$