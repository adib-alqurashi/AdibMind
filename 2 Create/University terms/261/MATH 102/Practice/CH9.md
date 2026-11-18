# MATH 102 · Chapter 9 — Infinite Series

## 9.1 Sequences (24 problems)

**1)** Write the first five terms of $a_n=(-1)^{n+1}\Big(\dfrac2n\Big)$.

> [!check]- Solution
>
> $n=1,\dots,5$: $\ 2,\ -\frac22,\ \frac23,\ -\frac24,\ \frac25$.
>
> **Answer:** $\color{red}{\boxed{2,\ -1,\ \tfrac23,\ -\tfrac12,\ \tfrac25}}$

**2)** Describe the graph of $a_n=\dfrac{10n}{n+1}$: is it increasing or decreasing, and what value does it approach?

> [!check]- Solution
>
> $a_1=5,\ a_2\approx6.67,\ a_3=7.5,\dots$ increasing, and $a_n\to10$.
>
> **Answer:** $\color{red}{\boxed{\text{increasing toward }10}}$

**3)** Simplify $\dfrac{(4n+1)!}{(4n+3)!}$.

> [!check]- Solution
>
> $(4n+3)!=(4n+3)(4n+2)(4n+1)!$.
>
> **Answer:** $\color{red}{\boxed{\dfrac{1}{(4n+2)(4n+3)}}}$

**4)** Find $\lim a_n$ for $a_n=\dfrac{2n}{\sqrt{n^2+1}}$.

> [!check]- Solution
>
> $\dfrac{2n}{n\sqrt{1+1/n^2}}=\dfrac{2}{\sqrt{1+1/n^2}}\to2$.
>
> **Answer:** $\color{red}{\boxed{2}}$

**5)** Converge or diverge? $a_n=(-1)^n\Big(\dfrac{n}{n+1}\Big)$

> [!check]- Solution
>
> $\frac{n}{n+1}\to1$, so the terms approach $+1$ (even $n$) and $-1$ (odd $n$). There is no single limit.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**6)** Converge or diverge? $a_n=\dfrac{(n-2)!}{n!}$

> [!check]- Solution
>
> $\frac{(n-2)!}{n!}=\frac{1}{n(n-1)}\to0$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges to }0}}$

**7)** Converge or diverge? $a_n=\dfrac{\cos2n}{3^n}$

> [!check]- Solution
>
> $-\frac1{3^n}\le\frac{\cos2n}{3^n}\le\frac1{3^n}$ and both bounds $\to0$, so by squeeze $a_n\to0$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges to }0}}$

**8)** Write an $n$th term for $\dfrac{1}{2\cdot3},\dfrac{2}{3\cdot4},\dfrac{3}{4\cdot5},\dfrac{4}{5\cdot6},\dots$ and decide convergence.

> [!check]- Solution
>
> The numerator is $n$; the denominator factors are $n+1$ and $n+2$. Since $\frac{n}{(n+1)(n+2)}\approx\frac1n\to0$:
>
> **Answer:** $\color{red}{\boxed{a_n=\dfrac{n}{(n+1)(n+2)}\ \to0\ \text{(converges)}}}$

**9)** Is $a_n=ne^{-n/2}$ monotonic? Is it bounded?

> [!check]- Solution
>
> $f(x)=xe^{-x/2}$, $f'(x)=e^{-x/2}\big(1-\frac x2\big)$: increasing for $x<2$, decreasing for $x>2$. Indeed $a_1\approx0.607<a_2=\frac2e\approx0.736>a_3\approx0.669$, so it is **not monotonic**.
>
> $0<a_n\le\frac2e$, so it is **bounded**.
>
> **Answer:** $\color{red}{\boxed{\text{Not monotonic; bounded }(0<a_n\le 2/e)}}$

**10)** Is $a_n=\Big(-\dfrac23\Big)^n$ monotonic? Is it bounded?

> [!check]- Solution
>
> Signs alternate ($-\frac23,\frac49,-\frac8{27},\dots$), so it is not monotonic. $|a_n|\le\frac23$, so it is bounded (and $\to0$).
>
> **Answer:** $\color{red}{\boxed{\text{Not monotonic; bounded}}}$

**11)** Use Theorem 9.5 (bounded + monotonic) to show $a_n=7+\dfrac1n$ converges, and find the limit.

> [!check]- Solution
>
> $a_{n+1}=7+\frac1{n+1}<7+\frac1n=a_n$, so it is decreasing. Also $7<a_n\le8$, so it is bounded. Theorem 9.5 gives convergence, and $\frac1n\to0$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges to }7}}$

**12)** Compute the first six terms of $a_n=\sqrt[n]{n}$ and find the limit.

> [!check]- Solution
>
> $1,\ \sqrt2\approx1.414,\ \sqrt[3]3\approx1.442,\ \sqrt[4]4\approx1.414,\ \sqrt[5]5\approx1.380,\ \sqrt[6]6\approx1.348$.
>
> $\ln a_n=\frac{\ln n}{n}\to0$, so $a_n\to e^0=1$.
>
> **Answer:** $\color{red}{\boxed{\text{Limit }=1}}$

**13)** Which of the following sequences are convergent?

I. $a_n=\dfrac{(2n+1)!}{n(2n-1)!}$ II. $b_n=\tan^{-1}(3n)$ III. $c_n=\dfrac{\ln(3n)}{\ln(5n)},\ n\ge2$

> [!check]- Solution
>
> I: $\frac{(2n+1)(2n)}{n}=2(2n+1)\to\infty$, so it diverges. II: $\tan^{-1}(3n)\to\frac\pi2$, so it converges. III: L'Hôpital gives $\frac{1/x}{1/x}=1$, so it converges to $1$.
>
> **Answer:** $\color{red}{\boxed{\text{II and III only}}}$

**14)** Does the sequence $a_n=n\ln\Big(1+\dfrac1n\Big)$ converge or diverge? If it converges, find the limit.

> [!check]- Solution
>
> $\infty\cdot0$ form: $\frac{\ln(1+1/x)}{1/x}$, then L'Hôpital: $\frac{\frac{-1/x^2}{1+1/x}}{-1/x^2}=\frac{1}{1+1/x}\to1$.
>
> **Answer:** $\color{red}{\boxed{\text{converges to }1}}$

**15)** $\displaystyle\lim_{n\to\infty}\big(ne^{1/n}-n\big)=$

> [!check]- Solution
>
> $\lim_{x\to\infty}\frac{e^{1/x}-1}{1/x}\overset{\text{H}}{=}\lim\frac{e^{1/x}(-1/x^2)}{-1/x^2}=e^0=1$.
>
> **Answer:** $\color{red}{\boxed{1}}$

**16)** $\displaystyle\lim_{n\to\infty}\frac{2^n+3^n}{4^n+5^n}=$

> [!check]- Solution
>
> Divide top and bottom by $5^n$: $\dfrac{(2/5)^n+(3/5)^n}{(4/5)^n+1}\to\dfrac{0+0}{0+1}=0$.
>
> **Answer:** $\color{red}{\boxed{0}}$

**17)** $\displaystyle\lim_{n\to\infty}\Big(1+\sin\frac1n\Big)^n=$

> [!check]- Solution
>
> $1^\infty$ form. $\ln y=\frac{\ln(1+\sin(1/x))}{1/x}\overset{\text H}{=}\frac{\cos(1/x)}{1+\sin(1/x)}\to1$, so $y\to e$.
>
> **Answer:** $\color{red}{\boxed{e}}$

**18)** Find the limit of the sequence $\big\lbrace (3n+2)\sin\frac5n\big\rbrace $.

> [!check]- Solution
>
> $\sin\frac5n\approx\frac5n$, so $(3n+2)\cdot\frac{\sin(5/n)}{5/n}\cdot\frac5n=\frac{5(3n+2)}{n}\cdot\frac{\sin(5/n)}{5/n}\to15\cdot1$.
>
> **Answer:** $\color{red}{\boxed{15}}$

**19)** $\displaystyle\lim_{n\to\infty}\Big(1+\frac3n+\frac5{n^2}\Big)^n=$

> [!check]- Solution
>
> $\ln y=n\ln\Big(1+\frac3n+\frac5{n^2}\Big)\approx n\Big(\frac3n+\frac{5}{n^2}\Big)\to3$ (L'Hôpital confirms), so $y\to e^3$.
>
> **Answer:** $\color{red}{\boxed{e^3}}$

**20)** Does the sequence $a_n=\dfrac{n^2}{2^n-1}$ converge or diverge? If it converges, find the limit.

> [!check]- Solution
>
> L'Hôpital twice on $\frac{x^2}{2^x-1}$: $\frac{2x}{2^x\ln2}\to\frac{2}{2^x(\ln2)^2}\to0$.
>
> **Answer:** $\color{red}{\boxed{\text{converges to }0}}$

**21)** Is the sequence $\Big\lbrace \dfrac{n^3+1}{n^2+1}\Big\rbrace $ monotonic? Is it bounded?

> [!check]- Solution
>
> $f(x)=\frac{x^3+1}{x^2+1}$, $f'(x)=\frac{x^4+3x^2-2x}{(x^2+1)^2}=\frac{x(x^3+3x-2)}{(x^2+1)^2}>0$ for $x\ge1$ (terms $1,\frac95,\frac{14}{5},\dots$ increase). And $a_n\approx n\to\infty$, so it is unbounded.
>
> **Answer:** $\color{red}{\boxed{\text{monotonic but not bounded}}}$

**22)** For $a_n=\dfrac{\sin\sqrt n}{\sqrt n}$, decide: does it converge (to what)? Is it bounded? Is it monotonic?

> [!check]- Solution
>
> $|a_n|\le\frac1{\sqrt n}\to0$, so it converges to $0$, is bounded, and changes sign (not monotonic).
>
> **Answer:** $\color{red}{\boxed{\text{converges to }0,\ \text{bounded},\ \text{not monotonic}}}$

**23)** Find the limit of $\lbrace a_n\rbrace $ with $a_1=\sqrt6$, $a_{n+1}=\sqrt{6+a_n}$ (given that it converges).

> [!check]- Solution
>
> If $a_n\to L$ then $L=\sqrt{6+L}\Rightarrow L^2-L-6=0\Rightarrow L=3$ or $-2$. All terms are positive, so $L=3$.
>
> **Answer:** $\color{red}{\boxed{3}}$

**24)** Given that $\sqrt2,\ \sqrt{2+\sqrt2},\ \sqrt{2+\sqrt{2+\sqrt2}},\dots$ converges, find its limit.

> [!check]- Solution
>
> $a_{n+1}=\sqrt{2+a_n}$; $L=\sqrt{2+L}\Rightarrow L^2-L-2=0\Rightarrow L=2$ (positive root).
>
> **Answer:** $\color{red}{\boxed{2}}$

## 9.2 Series and Convergence (25 problems)

**1)** Find $S_1,\dots,S_5$ for $1+\frac12+\frac14+\frac16+\frac18+\frac1{10}+\cdots$

> [!check]- Solution
>
> $S_1=1,\ S_2=\frac32,\ S_3=\frac74,\ S_4=\frac74+\frac16=\frac{23}{12},\ S_5=\frac{23}{12}+\frac18=\frac{49}{24}$.
>
> **Answer:** $\color{red}{\boxed{1,\ \tfrac32,\ \tfrac74,\ \tfrac{23}{12},\ \tfrac{49}{24}}}$

**2)** Verify that $\displaystyle\sum_{n=1}^\infty\frac{n}{2n+3}$ diverges.

> [!check]- Solution
>
> $\lim\frac{n}{2n+3}=\frac12\ne0$, so it diverges by the $n$th-term test.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges }(a_n\to\tfrac12)}}$

**3)** Verify that $\displaystyle\sum_{n=1}^\infty2\Big(-\frac12\Big)^n$ converges (and find its sum).

> [!check]- Solution
>
> Geometric with $|r|=\frac12<1$; first term $2\big(-\frac12\big)=-1$: sum $=\frac{-1}{1+1/2}=-\frac23$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges to }-\tfrac23}}$

**4)** Verify that $\displaystyle\sum_{n=1}^\infty\frac{1}{n(n+2)}$ converges (hint: partial fractions).

> [!check]- Solution
>
> $\frac{1}{n(n+2)}=\frac12\Big(\frac1n-\frac1{n+2}\Big)$. Telescoping: $S_n=\frac12\Big(1+\frac12-\frac1{n+1}-\frac1{n+2}\Big)\to\frac12\cdot\frac32$.
>
> **Answer:** $\color{red}{\boxed{\tfrac34}}$

**5)** $\displaystyle\sum_{n=0}^\infty\big[(0.3)^n+(0.8)^n\big]$

> [!check]- Solution
>
> $\frac{1}{1-0.3}+\frac1{1-0.8}=\frac{10}{7}+5$.
>
> **Answer:** $\color{red}{\boxed{\tfrac{45}{7}}}$

**6)** $\displaystyle\sum_{n=1}^\infty\frac{1}{9n^2+3n-2}$

> [!check]- Solution
>
> $9n^2+3n-2=(3n-1)(3n+2)$ and $\frac{1}{(3n-1)(3n+2)}=\frac13\Big(\frac1{3n-1}-\frac1{3n+2}\Big)$.
>
> Telescoping (shift 1 in $n$): $S_n=\frac13\Big(\frac12-\frac1{3n+2}\Big)\to\frac16$.
>
> **Answer:** $\color{red}{\boxed{\tfrac16}}$

**7)** Write $0.\overline{12}$ as a geometric series and as a ratio of integers.

> [!check]- Solution
>
> $0.121212\ldots=\sum_{n=0}^\infty\frac{12}{100}\Big(\frac1{100}\Big)^n=\frac{12/100}{1-1/100}=\frac{12}{99}$.
>
> **Answer:** $\color{red}{\boxed{\tfrac{4}{33}}}$

**8)** Converge or diverge? $\displaystyle\sum_{n=1}^\infty\frac{3^n}{n^3}$

> [!check]- Solution
>
> $\frac{3^x}{x^3}\to\infty$ (L'Hôpital 3 times), so $a_n\not\to0$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges ($n$th-term test)}}}$

**9)** Converge or diverge? $\displaystyle\sum_{n=1}^\infty\ln\Big(\frac{n+1}{n}\Big)$

> [!check]- Solution
>
> $\ln\frac{n+1}{n}=\ln(n+1)-\ln n$, so it telescopes: $S_n=\ln(n+1)\to\infty$. (Here $a_n\to0$, yet the series diverges.)
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**10)** Find all $x$ for which $\displaystyle\sum_{n=0}^\infty5\Big(\frac{x-2}{3}\Big)^n$ converges, and its sum.

> [!check]- Solution
>
> Geometric: $\big|\frac{x-2}3\big|<1\iff-1<x<5$. Sum $=\frac{5}{1-\frac{x-2}{3}}=\frac{15}{5-x}$.
>
> **Answer:** $\color{red}{\boxed{-1<x<5;\quad S=\dfrac{15}{5-x}}}$

**11)** A square has side 16 in. A new square is formed by joining the midpoints of the sides, and two of the corner triangles outside it are shaded; the process repeats. Find the shaded area (a) after five more repetitions, (b) when continued infinitely.

> [!check]- Solution
>
> The first two shaded corner triangles have legs $8$: area $2\cdot\frac12\cdot8\cdot8=64$. Each new square has half the area of the previous one, so each shaded pair is half the previous: $64,32,16,\dots$
>
> (a) Six shadings in total: $64\cdot\frac{1-(1/2)^6}{1/2}=126$ in² (b) $\frac{64}{1-1/2}=128$ in²
>
> **Answer:** $\color{red}{\boxed{\text{(a) }126\text{ in}^2\quad\text{(b) }128\text{ in}^2}}$

**12)** Find two divergent series $\sum a_n$ and $\sum b_n$ such that $\sum(a_n+b_n)$ converges.

> [!check]- Solution
>
> $a_n=1,\ b_n=-1$: both diverge ($n$th-term test) but $\sum(a_n+b_n)=\sum0=0$.
>
> **Answer:** $\color{red}{\boxed{\textstyle\sum1\text{ and }\sum(-1)}}$

**13)** Find the sum of $\displaystyle\sum_{n=0}^\infty\big[\tan^{-1}(2n+1)-\tan^{-1}(2n+3)\big]$.

> [!check]- Solution
>
> Telescoping: $S_n=\tan^{-1}1-\tan^{-1}(2n+3)\to\frac\pi4-\frac\pi2$.
>
> **Answer:** $\color{red}{\boxed{-\tfrac\pi4}}$

**14)** The series $\displaystyle\sum_{n=1}^\infty\frac{(27)^{\frac{2n+1}{3}}}{3(10)^{n-1}}$

> [!check]- Solution
>
> $27^{\frac{2n+1}3}=3^{2n+1}=3\cdot9^n$, so $a_n=\frac{9^n}{10^{n-1}}=10\Big(\frac9{10}\Big)^n$. Geometric: first term $9$, $r=\frac9{10}$: $\frac{9}{1/10}=90$.
>
> **Answer:** $\color{red}{\boxed{90}}$

**15)** Find the sum of $\displaystyle\sum_{n=1}^\infty\frac{2}{4n^2+16n+15}$.

> [!check]- Solution
>
> $\frac{2}{(2n+3)(2n+5)}=\frac{1}{2n+3}-\frac1{2n+5}$; $S_n=\frac15-\frac1{2n+5}\to\frac15$.
>
> **Answer:** $\color{red}{\boxed{\tfrac15}}$

**16)** Which series is (are) **divergent**? I. $\sum\big(\frac1e\big)^{1/n^2}$ II. $\sum2(\cos3)^n$ III. $\sum\dfrac{5(8)^{\frac{3-n}{3}}}{3^{2-n}}$

> [!check]- Solution
>
> I: terms $\to\big(\frac1e\big)^0=1\ne0$, so it diverges. II: $|r|=|\cos3|<1$, so it converges.
>
> III: $8^{\frac{3-n}{3}}=2^{3-n}$, so $a_n=\frac{5\cdot8\cdot2^{-n}}{9\cdot3^{-n}}=\frac{40}9\big(\frac32\big)^n$, with $r=\frac32>1$: it diverges.
>
> **Answer:** $\color{red}{\boxed{\text{I and III only}}}$

**17)** Find the sum of $\displaystyle\sum_{n=1}^\infty\frac{(-1)^n+2^{n+1}}{3^n}$.

> [!check]- Solution
>
> $\sum\big(-\frac13\big)^n=\frac{-1/3}{1+1/3}=-\frac14$ and $\sum2\big(\frac23\big)^n=\frac{4/3}{1/3}=4$.
>
> **Answer:** $\color{red}{\boxed{\tfrac{15}4}}$

**18)** The series $\displaystyle\sum_{n=1}^\infty\big[\tan^{-1}n-\tan^{-1}(n+2)\big]$

> [!check]- Solution
>
> Shift of 2, so two terms survive at each end: $S_n=\tan^{-1}1+\tan^{-1}2-\tan^{-1}(n+1)-\tan^{-1}(n+2)\to\frac\pi4+\tan^{-1}2-\pi$.
>
> **Answer:** $\color{red}{\boxed{-\tfrac{3\pi}4+\tan^{-1}2}}$

**19)** The series $\displaystyle\sum_{n=1}^\infty\big[e^{1/n}-e^{1/(n+2)}\big]$

> [!check]- Solution
>
> $S_n=e^1+e^{1/2}-e^{1/(n+1)}-e^{1/(n+2)}\to e+\sqrt e-1-1$.
>
> (Sec 5 Q2: $\sum[\cos\frac1n-\cos\frac1{n+2}]=-2+\cos1+\cos\frac12$.)
>
> **Answer:** $\color{red}{\boxed{e+\sqrt e-2}}$

**20)** $\displaystyle\sum_{n=0}^\infty\Big[\Big(\frac34\Big)^n-\frac{1}{(n+1)(n+2)}\Big]=$

> [!check]- Solution
>
> $\sum_{n=0}^\infty\big(\frac34\big)^n=4$ and $\sum_{n=0}^\infty\Big(\frac1{n+1}-\frac1{n+2}\Big)=1$, so $4-1=3$.
>
> **Answer:** $\color{red}{\boxed{3}}$

**21)** $\displaystyle\sum_{n=0}^\infty\frac{3}{2^n}+\sum_{n=1}^\infty\frac{2}{4n^2-1}=$

> [!check]- Solution
>
> $\frac{3}{1-1/2}=6$; $\ \frac{2}{(2n-1)(2n+1)}=\frac1{2n-1}-\frac1{2n+1}$ telescopes to $1$.
>
> **Answer:** $\color{red}{\boxed{7}}$

**22)** $\displaystyle\sum_{n=2}^\infty\ln\Big(1-\frac1{n^2}\Big)$

> [!check]- Solution
>
> $1-\frac1{n^2}=\frac{(n-1)(n+1)}{n^2}$, so $\sum_{n=2}^N\ln=\ln\prod_{n=2}^N\frac{n-1}{n}\cdot\frac{n+1}{n}=\ln\Big(\frac1N\cdot\frac{N+1}{2}\Big)\to\ln\frac12$.
>
> **Answer:** $\color{red}{\boxed{-\ln2}}$

**23)** Find the sum of the geometric series $6-3+\frac32-\frac34+\cdots$.

> [!check]- Solution
>
> $a=6,\ r=-\frac12$: $\frac{6}{3/2}=4$.
>
> **Answer:** $\color{red}{\boxed{4}}$

**24)** $\displaystyle\sum_{n=1}^\infty\big(e^{-n}+e^{-2n}\big)=$

> [!check]- Solution
>
> $\frac{e^{-1}}{1-e^{-1}}=\frac1{e-1}=\frac{e+1}{e^2-1}$ and $\frac{e^{-2}}{1-e^{-2}}=\frac1{e^2-1}$. Total $\frac{e+2}{e^2-1}$.
>
> **Answer:** $\color{red}{\boxed{\tfrac{e+2}{e^2-1}}}$

**25)** Which series is/are convergent? I. $\sum_{n=1}^\infty\dfrac{99^n}{n!}$ II. $\sum_{n=1}^\infty\Big(\dfrac1e-e^{-n}\Big)^n$ III. $\sum_{n=2}^\infty\dfrac{n}{\ln n}$

> [!check]- Solution
>
> I: ratio $\frac{99}{n+1}\to0<1$, so it converges. II: root $\frac1e-e^{-n}\to\frac1e<1$, so it converges. III: $\frac{n}{\ln n}\to\infty$, so it diverges by the $n$th-term test.
>
> **Answer:** $\color{red}{\boxed{\text{I and II only}}}$

## 9.3 The Integral Test and p-Series (24 problems)

**1)** Use the integral test on $\displaystyle\sum_{n=1}^\infty\frac{2}{3n+5}$.

> [!check]- Solution
>
> $f(x)=\frac2{3x+5}$ is positive, continuous and decreasing for $x\ge1$.
>
> $$\int_1^\infty\frac{2}{3x+5}dx=\lim_{t\to\infty}\frac23\Big[\ln(3x+5)\Big]_1^t=\infty$$
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**2)** Use the integral test on $\displaystyle\sum_{n=1}^\infty\frac{\ln n}{n^2}$.

> [!check]- Solution
>
> $f(x)=\frac{\ln x}{x^2}\ge0$ and $f'(x)=\frac{1-2\ln x}{x^3}<0$ for $x>\sqrt e$ (decreasing from $n=2$ on).
>
> By parts, $\int_1^\infty\frac{\ln x}{x^2}dx=\Big[-\frac{\ln x}{x}-\frac1x\Big]_1^\infty=0-(-1)=1$, which is finite.
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**3)** Use the integral test on $\displaystyle\sum_{n=1}^\infty n^ke^{-n}$, $k$ a positive integer.

> [!check]- Solution
>
> $f(x)=x^ke^{-x}$ is positive and decreasing for $x>k$. Using parts $k$ times (tabular), $\int_1^\infty x^ke^{-x}dx=\Big[-e^{-x}\big(x^k+kx^{k-1}+\cdots+k!\big)\Big]_1^\infty$, which is finite because $x^me^{-x}\to0$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges for every positive integer }k}}$

**4)** Explain why the integral test does not apply to $\displaystyle\sum_{n=1}^\infty\frac{(-1)^n}{n}$.

> [!check]- Solution
>
> The test needs a **positive** function $f$ with $f(n)=a_n$. Here the terms alternate in sign.
>
> **Answer:** $\color{red}{\boxed{\text{Terms are not positive}}}$

**5)** Use Theorem 9.11 ($p$-series): $\displaystyle\sum_{n=1}^\infty\frac1{\sqrt[5]n}$

> [!check]- Solution
>
> $p=\frac15\le1$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**6)** $\displaystyle\sum_{n=1}^\infty\frac{1}{n^\pi}$

> [!check]- Solution
>
> $p=\pi>1$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**7)** Find the positive $p$ for which $\displaystyle\sum_{n=2}^\infty\frac{1}{n(\ln n)^p}$ converges.

> [!check]- Solution
>
> $u=\ln x$: $\int_2^\infty\frac{dx}{x(\ln x)^p}=\int_{\ln2}^\infty\frac{du}{u^p}$, which converges iff $p>1$.
>
> So $p=1$ diverges, while $p=2,3$ converge.
>
> **Answer:** $\color{red}{\boxed{p>1}}$

**8)** Find the positive $p$ for which $\displaystyle\sum_{n=1}^\infty\Big(\frac3p\Big)^n$ converges.

> [!check]- Solution
>
> Geometric with $r=\frac3p$: converges iff $\frac3p<1$.
>
> **Answer:** $\color{red}{\boxed{p>3}}$

**9)** Find the sum of $\displaystyle\sum_{n=2}^\infty\ln\Big(1-\frac1{n^2}\Big)$.

> [!check]- Solution
>
> $\ln\frac{(n-1)(n+1)}{n^2}=[\ln(n-1)-\ln n]-[\ln n-\ln(n+1)]$ telescopes: $S_N=\ln\frac12+\ln\frac{N+1}{N}\to-\ln2$.
>
> **Answer:** $\color{red}{\boxed{-\ln2}}$

**10)** Converge or diverge? $\displaystyle\sum_{n=1}^\infty\Big(\frac1{n^2}-\frac1{n^3}\Big)$

> [!check]- Solution
>
> Both $\sum\frac1{n^2}$ and $\sum\frac1{n^3}$ are convergent $p$-series ($p=2,3>1$), so their difference converges.
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**11)** Converge or diverge? $\displaystyle\sum_{n=1}^\infty\Big(1+\frac1n\Big)^n$

> [!check]- Solution
>
> $a_n\to e\ne0$, so it diverges by the $n$th-term test.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**12)** Use the integral test to decide whether $\displaystyle\sum_{n=3}^\infty\frac{1}{n\ln n}$ converges or diverges.

> [!check]- Solution
>
> $f(x)=\frac{1}{x\ln x}$ is positive, continuous and decreasing on $[3,\infty)$, and $\int_3^\infty\frac{dx}{x\ln x}=\lim\big[\ln(\ln x)\big]_3^t=\infty$.
>
> **Answer:** $\color{red}{\boxed{\text{diverges by the integral test}}}$

**13)** Use the integral test to decide whether $\displaystyle\sum_{n=3}^\infty\frac{1}{n(\ln n)^2}$ converges or diverges.

> [!check]- Solution
>
> $\int_3^\infty\frac{dx}{x(\ln x)^2}=\Big[-\frac1{\ln x}\Big]_3^\infty=\frac1{\ln3}$, which is finite.
>
> **Answer:** $\color{red}{\boxed{\text{converges by the integral test}}}$

**14)** Use the integral test to decide whether $\displaystyle\sum_{n=3}^\infty\frac{1}{n[1+(\ln n)^2]}$ converges or diverges.

> [!check]- Solution
>
> $u=\ln x$: $\int_3^\infty\frac{dx}{x(1+(\ln x)^2)}=\Big[\tan^{-1}(\ln x)\Big]_3^\infty=\frac\pi2-\tan^{-1}(\ln3)$, which is finite.
>
> **Answer:** $\color{red}{\boxed{\text{converges by the integral test}}}$

**15)** Use the integral test to decide whether $\displaystyle\sum_{n=3}^\infty\frac{1}{n\sqrt{\ln n}}$ converges or diverges.

> [!check]- Solution
>
> $\int_3^\infty\frac{dx}{x\sqrt{\ln x}}=\Big[2\sqrt{\ln x}\Big]_3^\infty=\infty$.
>
> **Answer:** $\color{red}{\boxed{\text{diverges by the integral test}}}$

**16)** Which is/are convergent? I. $\sum_{n=2}^\infty\dfrac1{n(\ln n)^2}$ II. $\sum_{n=1}^\infty\dfrac1{n^{2025/2026}}$ III. $\sum_{n=1}^\infty\dfrac{1}{(n+1)(n+2)}$

> [!check]- Solution
>
> I converges ($p=2$ in B7). II: $p=\frac{2025}{2026}<1$, so it diverges. III telescopes to $\frac12$, so it converges.
>
> **Answer:** $\color{red}{\boxed{\text{I and III only}}}$

**17)** Use the integral test to decide whether $\displaystyle\sum_{n=2}^\infty\frac{n^2}{n^3+1}$ converges or diverges.

> [!check]- Solution
>
> $\int_2^\infty\frac{x^2}{x^3+1}dx=\frac13\big[\ln(x^3+1)\big]_2^\infty=\infty$. ($a_n\to0$, so the $n$th-term test says nothing.)
>
> **Answer:** $\color{red}{\boxed{\text{divergent by the Integral Test}}}$

**18)** Apply the integral test to $\displaystyle\sum_{n=1}^\infty\frac{\arctan n}{n^2+1}$: check that $f(x)=\frac{\arctan x}{x^2+1}$ is positive, continuous and decreasing for $x\ge1$, then decide convergence.

> [!check]- Solution
>
> $\int_1^\infty\frac{\arctan x}{1+x^2}dx=\Big[\frac{(\arctan x)^2}{2}\Big]_1^\infty=\frac{\pi^2}8-\frac{\pi^2}{32}=\frac{3\pi^2}{32}$, which is finite, so the series converges. $f$ is positive and continuous, and decreasing since $f'(x)=\frac{1-2x\arctan x}{(1+x^2)^2}<0$ for $x\ge1$.
>
> **Answer:** $\color{red}{\boxed{\text{converges}}}$

**19)** Which is/are convergent? I. $\sum\dfrac{\arctan n}{n^2+1}$ II. $\sum3^{-n}$ III. $\sum\dfrac{1}{n^{1.03}}$

> [!check]- Solution
>
> I converges (E3). II is geometric with $r=\frac13$, so it converges. III: $p=1.03>1$, so it converges.
>
> **Answer:** $\color{red}{\boxed{\text{I, II and III}}}$

**20)** Which is/are **divergent**? I. $\sum_{n=2}^\infty\dfrac1{n\sqrt{\ln n}}$ II. $\sum e^{-n}$ III. $\sum\dfrac1{n^\pi}$

> [!check]- Solution
>
> I diverges (Q4). II is geometric with $r=\frac1e$, so it converges. III: $p=\pi>1$, so it converges.
>
> **Answer:** $\color{red}{\boxed{\text{I only}}}$

**21)** Which is **divergent**? I. $\sum\dfrac1{n^{5/3}}$ II. $\sum\dfrac{1}{\sqrt[5]n}$ III. $\sum ne^{-n/2}$

> [!check]- Solution
>
> I: $p=\frac53>1$, converges. II: $p=\frac15$, diverges. III: $\int_1^\infty xe^{-x/2}dx$ is finite (integral test), so it converges.
>
> **Answer:** $\color{red}{\boxed{\text{II only}}}$

**22)** Which of these converge? $\sum\frac1{\sqrt{n^3}},\ \sum\frac1{\sqrt[3]{n^3}},\ \sum\frac1{\sqrt[4]{n^3}},\ \sum\frac1{\sqrt[5]{n^3}},\ \sum\frac1{\sqrt[6]{n^3}}$

> [!check]- Solution
>
> The exponents are $p=\frac32,1,\frac34,\frac35,\frac12$; only $\frac32>1$.
>
> **Answer:** $\color{red}{\boxed{\text{only }\textstyle\sum\frac1{\sqrt{n^3}}}}$

**23)** Which is/are convergent? I. $\sum\dfrac{n}{n^4+2n^2+1}$ II. $\sum\dfrac1{n^{1.001}}$ III. $\sum\dfrac1{n^{0.9}}$

> [!check]- Solution
>
> I: $\frac{n}{(n^2+1)^2}$, and $\int_1^\infty\frac{x dx}{(x^2+1)^2}=\frac14$, which is finite, so it converges. II: $p>1$, converges. III: $p<1$, diverges.
>
> **Answer:** $\color{red}{\boxed{\text{I and II only}}}$

**24)** Using the integral test, for positive $p$ the series $\displaystyle\sum_{n=1}^\infty\frac{n}{(1+n^2)^p}$ converges if

> [!check]- Solution
>
> $\int_1^\infty\frac{x}{(1+x^2)^p}dx=\frac12\int_2^\infty u^{-p}du$, which converges iff $p>1$ ($p=1$ gives $\ln$, which diverges).
>
> **Answer:** $\color{red}{\boxed{p>1}}$

## 9.4 Comparisons of Series (23 problems)

**1)** Use direct comparison: $\displaystyle\sum_{n=0}^\infty\frac{4^n}{5^n+3}$

> [!check]- Solution
>
> $0<\frac{4^n}{5^n+3}<\frac{4^n}{5^n}=\big(\frac45\big)^n$, a convergent geometric series.
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**2)** Use direct comparison: $\displaystyle\sum_{n=2}^\infty\frac{\ln n}{n+1}$

> [!check]- Solution
>
> For $n\ge3$, $\ln n>1$, so $\frac{\ln n}{n+1}>\frac{1}{n+1}$, and $\sum\frac1{n+1}$ diverges (harmonic).
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**3)** Use direct comparison: $\displaystyle\sum_{n=1}^\infty\frac{\sin^2n}{n^3}$

> [!check]- Solution
>
> $0\le\frac{\sin^2n}{n^3}\le\frac1{n^3}$, a convergent $p$-series ($p=3$).
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**4)** Use limit comparison: $\displaystyle\sum_{n=1}^\infty\frac{n^{k-1}}{n^k+1},\ k>2$

> [!check]- Solution
>
> $b_n=\frac1n$: $\lim\frac{n^{k-1}/(n^k+1)}{1/n}=\lim\frac{n^k}{n^k+1}=1>0$, and $\sum\frac1n$ diverges.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**5)** Use limit comparison: $\displaystyle\sum_{n=1}^\infty\sin\frac1n$

> [!check]- Solution
>
> $b_n=\frac1n$: $\lim\frac{\sin(1/n)}{1/n}=1$, and the harmonic series diverges.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**6)** Converge or diverge? $\displaystyle\sum_{n=3}^\infty\frac1{n^3-8}$

> [!check]- Solution
>
> Limit comparison with $\frac1{n^3}$: $\lim\frac{n^3}{n^3-8}=1$, and $\sum\frac1{n^3}$ converges ($p=3$).
>
> **Answer:** $\color{red}{\boxed{\text{Converges (limit comparison)}}}$

**7)** Converge or diverge? $\frac1{200}+\frac1{208}+\frac1{216}+\frac1{224}+\cdots$

> [!check]- Solution
>
> $a_n=\frac{1}{200+8n}$ ($n\ge0$). Limit comparison with $\frac1n$: $\lim\frac{n}{200+8n}=\frac18>0$, so it diverges like the harmonic series. (Small terms do not guarantee convergence.)
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**8)** Show that $\dfrac{x_1}{10}+\dfrac{x_2}{10^2}+\dfrac{x_3}{10^3}+\cdots$ converges, where each $x_i\in\lbrace 0,1,\dots,9\rbrace $.

> [!check]- Solution
>
> $0\le\frac{x_n}{10^n}\le\frac9{10^n}$ and $\sum\frac{9}{10^n}=9\cdot\frac{1/10}{1-1/10}=1$, so it converges by direct comparison. (Every decimal expansion is a convergent series.)
>
> **Answer:** $\color{red}{\boxed{\text{Converges (compare with }\textstyle\sum 9/10^n)}}$

**9)** Prove that $\displaystyle\sum_{n=1}^\infty\frac{1}{1+2+3+\cdots+n}$ converges.

> [!check]- Solution
>
> $1+2+\cdots+n=\frac{n(n+1)}2$, so $a_n=\frac{2}{n(n+1)}<\frac2{n^2}$, and $\sum\frac2{n^2}$ converges. (It even telescopes to $2$.)
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**10)** Does the every-other-term harmonic series $1+\frac13+\frac15+\frac17+\cdots$ converge?

> [!check]- Solution
>
> $a_n=\frac1{2n-1}$; limit comparison with $\frac1n$: $\lim\frac{n}{2n-1}=\frac12>0$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**11)** Which is convergent? I. $\sum_{n=3}^\infty\dfrac{2+\sin3n}{2^n}$ II. $\sum\tan^{-1}(-2n)$ III. $\sum_{n=3}^\infty\dfrac{\sqrt{n^2+1}}{n^3+5}$

> [!check]- Solution
>
> I: $\le\frac{3}{2^n}$ (geometric), so it converges by comparison. II: terms $\to-\frac\pi2\ne0$, so it diverges. III: limit comparison with $\frac{n}{n^3}=\frac1{n^2}$ gives limit $1$, so it converges.
>
> **Answer:** $\color{red}{\boxed{\text{I and III only}}}$

**12)** Which is convergent? I. $\sum\cos(2n)$ II. $\sum_{n=3}^\infty\Big(\dfrac{\cos n}{n}\Big)^2$ III. $\sum_{n=3}^\infty\dfrac{\ln n}{n^2}$

> [!check]- Solution
>
> I: $\cos2n$ has no limit, so it diverges by the $n$th-term test. II: $\le\frac{1}{n^2}$, converges. III: $\ln n<\sqrt n\Rightarrow\frac{\ln n}{n^2}<\frac1{n^{3/2}}$, converges.
>
> **Answer:** $\color{red}{\boxed{\text{II and III only}}}$

**13)** Which is convergent? I. $\sum_{n=3}^\infty\dfrac1{5^n+n^2}$ II. $\sum_{n=3}^\infty\dfrac{n+2^n}{n+3^n}$ III. $\sum_{n=3}^\infty\cos\Big(\dfrac1{2n^2+1}\Big)$

> [!check]- Solution
>
> I: $<\frac1{n^2}$, converges. II: limit comparison with $\big(\frac23\big)^n$ gives limit $1$, converges. III: terms $\to\cos0=1\ne0$, diverges.
>
> **Answer:** $\color{red}{\boxed{\text{I and II only}}}$

**14)** Which is convergent? I. $\sum_{n=3}^\infty\dfrac{e^n}{n^2}$ II. $\sum_{n=3}^\infty\dfrac{\cos^2n}{n\sqrt n}$ III. $\sum_{n=3}^\infty n\tan\dfrac1n$

> [!check]- Solution
>
> I: $\frac{e^n}{n^2}\to\infty$, diverges. II: $\le\frac1{n^{3/2}}$, converges. III: $n\tan\frac1n=\frac{\tan(1/n)}{1/n}\to1\ne0$, diverges.
>
> **Answer:** $\color{red}{\boxed{\text{II only}}}$

**15)** Which is/are **divergent**? I. $\sum\dfrac{2+\cos n}{\sqrt n}$ II. $\sum\dfrac1{n\sqrt{n^2+1}}$ III. $\sum\dfrac{n^k-1}{n^k+1},\ k>2$

> [!check]- Solution
>
> I: $\ge\frac1{\sqrt n}$ ($p=\frac12$), diverges. II: limit comparison with $\frac1{n^2}$, converges. III: terms $\to1$, diverges.
>
> **Answer:** $\color{red}{\boxed{\text{I and III only}}}$

**16)** Which is/are **convergent**? I. $\sum\dfrac{\sin^2n}{n^3}$ II. $\sum\dfrac{6^n+n}{5^n-1}$ III. $\sum\dfrac{n}{(n+1)2^{n-1}}$

> [!check]- Solution
>
> I converges (B3). II: terms $\to\infty$, diverges. III: $\frac{n}{n+1}\cdot\frac1{2^{n-1}}<\frac1{2^{n-1}}$, converges.
>
> **Answer:** $\color{red}{\boxed{\text{I and III only}}}$

**17)** Which is **convergent**? I. $\sum\dfrac{n}{n^2+1}$ II. $\sum\dfrac{2^n+1}{5^n+1}$ III. $\sum\sin\dfrac1n$

> [!check]- Solution
>
> I: limit comparison with $\frac1n$, diverges. II: limit comparison with $\big(\frac25\big)^n$, converges. III diverges (B5).
>
> **Answer:** $\color{red}{\boxed{\text{II only}}}$

**18)** Which is/are convergent? I. $\sum_{n=0}^\infty\dfrac{4^n}{5^n+3}$ II. $\sum_{n=2}^\infty\dfrac{\ln n}{n+1}$ III. $\sum\dfrac{n}{n^2+1}$

> [!check]- Solution
>
> I converges (B1); II diverges (B2); III diverges (E3).
>
> **Answer:** $\color{red}{\boxed{\text{I only}}}$

**19)** Which is convergent? I. $\sum_{n=0}^\infty\dfrac1{n!}$ II. $\sum\sin\dfrac1n$ III. $\sum_{n=0}^\infty\dfrac{n!}{2(n!)+1}$

> [!check]- Solution
>
> I: $\frac1{n!}\le\frac1{2^{n-1}}$ for $n\ge1$, converges (to $e$). II diverges. III: terms $\to\frac12\ne0$, diverges.
>
> **Answer:** $\color{red}{\boxed{\text{I only}}}$

**20)** Which is/are **divergent**? I. $\sum\sin\dfrac1n$ II. $\sum e^{-n^2}$ III. $\sum\dfrac5{4^n+1}$

> [!check]- Solution
>
> I diverges. II: $e^{-n^2}\le e^{-n}$, converges. III: $<\frac5{4^n}$, converges.
>
> **Answer:** $\color{red}{\boxed{\text{I only}}}$

**21)** Use the limit comparison test to decide whether $\displaystyle\sum_{n=1}^\infty\frac{4n^2+7}{n^{5/2}+5n+1}$ converges or diverges.

> [!check]- Solution
>
> Dominant terms: $\frac{4n^2}{n^{5/2}}=\frac4{\sqrt n}$. $\lim\frac{a_n}{1/\sqrt n}=\lim\frac{4n^{5/2}+7\sqrt n}{n^{5/2}+5n+1}=4>0$, and $\sum\frac1{\sqrt n}$ diverges.
>
> **Answer:** $\color{red}{\boxed{\text{diverges by LCT with }\textstyle\sum\frac1{\sqrt n}}}$

**22)** How many of (i) $\sum\dfrac{\ln n}{n+1}$ (ii) $\sum_{n=0}^\infty\dfrac1{n!}$ (iii) $\sum\dfrac{\sin^2n}{n^3}$ (iv) $\sum\dfrac{1}{4\sqrt[3]n-1}$ are divergent?

> [!check]- Solution
>
> (i) diverges, (ii) converges, (iii) converges, (iv) diverges (limit comparison with $\frac1{n^{1/3}}$).
>
> **Answer:** $\color{red}{\boxed{2}}$

**23)** True or false? (i) If $\sum a_n$ diverges, then $\sum\big(a_n+\frac1n\big)$ converges. (ii) If $a_n\ge2^n$, then $\sum a_n$ diverges. (iii) If $0\le a_n\le\frac1{n^2}$, then $\sum a_n$ converges. (iv) If $\sum a_n$ converges, then $\sum\big(a_n+\frac1n\big)$ diverges. (v) If $\sum a_n$ diverges, then $\sum2a_n$ diverges.

> [!check]- Solution
>
> Counterexample to (i): $a_n=\frac1n$ diverges, and $\sum\big(\frac1n+\frac1n\big)=2\sum\frac1n$ also diverges. (ii), (iii) are true by comparison; (iv) is true (convergent + divergent = divergent); (v) is true.
>
> **Answer:** $\color{red}{\boxed{\text{(i) false; (ii)–(v) true}}}$

## 9.5 Alternating Series (24 problems)

**1)** $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}n}{n^2+5}$

> [!check]- Solution
>
> $b_n=\frac{n}{n^2+5}\to0$; $f'(x)=\frac{5-x^2}{(x^2+5)^2}<0$ for $x>\sqrt5$, so it decreases for $n\ge3$. AST applies.
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**2)** $\displaystyle\sum_{n=1}^\infty\frac{(-1)^nn}{\ln(n+1)}$

> [!check]- Solution
>
> $\frac{n}{\ln(n+1)}\to\infty$, so the terms don't approach $0$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges ($n$th-term test)}}}$

**3)** $\displaystyle\sum_{n=1}^\infty\sin\frac{(2n-1)\pi}{2}$

> [!check]- Solution
>
> $\sin\frac\pi2,\sin\frac{3\pi}2,\dots=1,-1,1,-1,\dots$, so the terms don't approach $0$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**4)** $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}\sqrt n}{\sqrt[3]n}$

> [!check]- Solution
>
> $\frac{\sqrt n}{\sqrt[3]n}=n^{1/6}\to\infty$, so the terms don't approach $0$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**5)** Approximate $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}n}{3^n}$ using six terms, and bound the error.

> [!check]- Solution
>
> $S_6=\frac13-\frac29+\frac3{27}-\frac4{81}+\frac5{243}-\frac6{729}=\frac{243-162+81-36+15-6}{729}=\frac{135}{729}=\frac5{27}\approx0.1852$.
>
> $|S-S_6|\le b_7=\frac7{2187}\approx0.0032$. (Exact: $S=\frac3{16}=0.1875$.)
>
> **Answer:** $\color{red}{\boxed{S\approx0.1852,\ \text{error}\le0.0032}}$

**6)** Find the number of terms needed to approximate $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}}{2n^3-1}$ with error less than $0.001$.

> [!check]- Solution
>
> Need $b_{N+1}=\frac{1}{2(N+1)^3-1}<0.001\iff(N+1)^3>500.5\iff N+1\ge8$ ($7^3=343,\ 8^3=512$).
>
> **Answer:** $\color{red}{\boxed{7\text{ terms}}}$

**7)** Absolutely, conditionally, or divergent? $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}}{n\sqrt n}$

> [!check]- Solution
>
> $\sum\big|a_n\big|=\sum\frac1{n^{3/2}}$, a $p$-series with $p=\frac32>1$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges absolutely}}}$

**8)** $\displaystyle\sum_{n=2}^\infty\frac{(-1)^n}{n\ln n}$

> [!check]- Solution
>
> $\sum\frac1{n\ln n}$ diverges (integral test: $\ln\ln x\to\infty$), so it is not absolutely convergent. But $b_n=\frac1{n\ln n}$ decreases to $0$, so AST gives convergence.
>
> **Answer:** $\color{red}{\boxed{\text{Converges conditionally}}}$

**9)** $\displaystyle\sum_{n=1}^\infty(-1)^{n+1}\arctan n$

> [!check]- Solution
>
> $\arctan n\to\frac\pi2$, so the terms oscillate near $\pm\frac\pi2$ and don't approach $0$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**10)** Find the values of $p$ for which $\displaystyle\sum_{n=1}^\infty(-1)^n\frac1{n^p}$ converges.

> [!check]- Solution
>
> $p>0$: $\frac1{n^p}$ decreases to $0$, so AST gives convergence (absolute if $p>1$, conditional if $0<p\le1$). $p\le0$: terms don't approach $0$, so it diverges.
>
> **Answer:** $\color{red}{\boxed{p>0}}$

**11)** Converge or diverge (name the test)? $\displaystyle\sum_{n=2}^\infty\frac{\ln n}{n}$

> [!check]- Solution
>
> For $n\ge3$, $\frac{\ln n}{n}>\frac1n$, so it diverges by direct comparison with the harmonic series (or by the integral test: $\frac12(\ln x)^2\to\infty$).
>
> **Answer:** $\color{red}{\boxed{\text{Diverges (direct comparison)}}}$

**12)** Describe the error: $0=0+0+\cdots=(1-1)+(1-1)+\cdots=1+(-1+1)+(-1+1)+\cdots=1+0+0+\cdots=1$.

> [!check]- Solution
>
> The series $1-1+1-1+\cdots$ **diverges** (its terms don't approach $0$). Regrouping terms with parentheses is only valid for **convergent** series; for a divergent series different groupings can give different "sums".
>
> **Answer:** $\color{red}{\boxed{\text{Regrouping a divergent series is invalid}}}$

**13)** Does $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}n^2}{n^3+1}$ converge absolutely, converge conditionally, or diverge?

> [!check]- Solution
>
> $\sum\frac{n^2}{n^3+1}$ diverges (limit comparison with $\frac1n$). $b_n=\frac{n^2}{n^3+1}$ decreases for $n\ge2$ and $\to0$, so AST gives convergence.
>
> **Answer:** $\color{red}{\boxed{\text{converges conditionally}}}$

**14)** Does $\displaystyle\sum_{n=1}^\infty\frac{(-1)^n}{\sqrt n}$ converge absolutely, converge conditionally, or diverge?

> [!check]- Solution
>
> $\sum\frac1{\sqrt n}$: $p=\frac12$, diverges. AST: $\frac1{\sqrt n}\downarrow0$, converges.
>
> **Answer:** $\color{red}{\boxed{\text{converges conditionally}}}$

**15)** Does $\displaystyle\sum_{n=1}^\infty\frac{(-1)^n\sqrt[3]n}{n+1}$ converge absolutely, converge conditionally, or diverge?

> [!check]- Solution
>
> $|a_n|\approx\frac{1}{n^{2/3}}$ (limit comparison), $p=\frac23<1$, so it is not absolutely convergent. $b_n=\frac{n^{1/3}}{n+1}$ eventually decreases to $0$, so AST gives convergence.
>
> **Answer:** $\color{red}{\boxed{\text{converges conditionally}}}$

**16)** Does $\displaystyle\sum_{n=0}^\infty\frac{\cos n\pi}{n+1}$ converge absolutely, converge conditionally, or diverge?

> [!check]- Solution
>
> $\cos n\pi=(-1)^n$, so it is $\sum\frac{(-1)^n}{n+1}$, the alternating harmonic series.
>
> **Answer:** $\color{red}{\boxed{\text{converges conditionally}}}$

**17)** Which is/are **divergent**? I. $\sum\dfrac{(-1)^{n+1}}{n+1}$ II. $\sum\dfrac{(-1)^n\sqrt n}{\sqrt[3]n}$ III. $\sum\dfrac{(-1)^n}{e^n}$

> [!check]- Solution
>
> I converges (AST). II: terms $=\pm n^{1/6}$, don't approach $0$, diverges. III is geometric with $|r|=\frac1e$, converges.
>
> **Answer:** $\color{red}{\boxed{\text{II only}}}$

**18)** Which is convergent? I. $\sum\dfrac{(-1)^nn}{\ln(n+1)}$ II. $\sum\sin\dfrac{(2n-1)\pi}2$ III. $\sum\dfrac1n\cos n\pi$

> [!check]- Solution
>
> I diverges (B2); II diverges (B3); III $=\sum\frac{(-1)^n}{n}$ converges.
>
> **Answer:** $\color{red}{\boxed{\text{III only}}}$

**19)** Classify each as absolutely convergent, conditionally convergent, or divergent: I. $\sum\dfrac{(-1)^{n+1}}{n^{4/3}}$ II. $\sum_{n=0}^\infty\dfrac{(-1)^n}{\sqrt{n+4}}$

> [!check]- Solution
>
> I: $\sum\frac1{n^{4/3}}$ converges ($p>1$), so absolute. II: $\sum\frac1{\sqrt{n+4}}$ diverges, but AST holds, so conditional.
>
> **Answer:** $\color{red}{\boxed{\text{I absolutely, II conditionally}}}$

**20)** Which of these converge? $\sum(-1)^n\sin\frac1n,\ \sum(-1)^n\cos\frac1n,\ \sum(-1)^n,\ \sum(-1)^n\frac{n}{n+1},\ \sum(-1)^n\sqrt n$

> [!check]- Solution
>
> $\sin\frac1n$ decreases to $0$, so the AST gives convergence of the first. In the other four the terms don't approach $0$.
>
> **Answer:** $\color{red}{\boxed{\text{only }\textstyle\sum(-1)^n\sin\frac1n}}$

**21)** Using the remainder theorem, the least number of terms needed to approximate $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}}{n^2}$ with error less than $0.02$ is

> [!check]- Solution
>
> $\frac1{(N+1)^2}<0.02\iff(N+1)^2>50\iff N+1\ge8$.
>
> **Answer:** $\color{red}{\boxed{7}}$

**22)** The least number of terms needed to approximate $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}}{n^3}$ with error less than $0.001$ is

> [!check]- Solution
>
> $\frac{1}{(N+1)^3}<0.001\iff(N+1)^3>1000\iff N+1\ge11$.
>
> **Answer:** $\color{red}{\boxed{10}}$

**23)** The least number of terms needed to approximate $\displaystyle\sum_{n=0}^\infty\frac{(-1)^n}{2n^3-1}$ with error less than $0.01$ is

> [!check]- Solution
>
> $b_n=\frac{1}{2n^3-1}$ decreases to $0$ for $n\ge1$. Stopping at index $N$ leaves error $\le b_{N+1}$:
>
> $$\frac{1}{2(N+1)^3-1}<0.01\iff(N+1)^3>50.5\iff N+1\ge4\ (3^3=27,\ 4^3=64)$$
>
> So you sum up to $n=N=3$ ($b_4=\frac1{127}\approx0.008<0.01$, while $b_3=\frac1{53}\approx0.019$ is too big). Here $N$ is the index of the last term used. (The extra $n=0$ term is included in the sum but isn't counted.)
>
> **Answer:** $\color{red}{\boxed{3}}$

**24)** The least number of terms needed to approximate $\displaystyle\sum_{n=1}^\infty\frac{(-1)^n}{n!}$ with error less than $0.01$ is

> [!check]- Solution
>
> $\frac1{(N+1)!}<0.01\iff(N+1)!>100\iff N+1\ge5$ ($4!=24,\ 5!=120$).
>
> **Answer:** $\color{red}{\boxed{4}}$

## 9.6 The Ratio and Root Tests (20 problems)

**1)** $\displaystyle\sum_{n=0}^\infty(n+2)\Big(\frac97\Big)^{n+1}$

> [!check]- Solution
>
> $\Big|\frac{a_{n+1}}{a_n}\Big|=\frac{n+3}{n+2}\cdot\frac97\to\frac97>1$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**2)** $\displaystyle\sum_{n=1}^\infty\frac{(2n)!}{n^5}$

> [!check]- Solution
>
> $\frac{(2n+2)!}{(n+1)^5}\cdot\frac{n^5}{(2n)!}=(2n+2)(2n+1)\Big(\frac{n}{n+1}\Big)^5\to\infty$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**3)** $\displaystyle\sum_{n=0}^\infty\frac{(-1)^{n+1}n!}{1\cdot3\cdot5\cdots(2n+1)}$

> [!check]- Solution
>
> $\Big|\frac{a_{n+1}}{a_n}\Big|=\frac{(n+1)!}{n!}\cdot\frac{1\cdot3\cdots(2n+1)}{1\cdot3\cdots(2n+1)(2n+3)}=\frac{n+1}{2n+3}\to\frac12<1$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges (absolutely)}}}$

**4)** $\displaystyle\sum_{n=1}^\infty\Big(\frac{-3n}{2n+1}\Big)^{3n}$

> [!check]- Solution
>
> Root: $\sqrt[n]{|a_n|}=\Big(\frac{3n}{2n+1}\Big)^3\to\Big(\frac32\Big)^3=\frac{27}{8}>1$.
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**5)** $\displaystyle\sum_{n=2}^\infty\frac{n}{(\ln n)^n}$

> [!check]- Solution
>
> Root: $\frac{\sqrt[n]n}{\ln n}\to\frac{1}{\infty}=0<1$.
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**6)** $\displaystyle\sum_{n=1}^\infty\frac{10n+3}{n2^n}$ (any test)

> [!check]- Solution
>
> Ratio: $\frac{10n+13}{(n+1)2^{n+1}}\cdot\frac{n2^n}{10n+3}\to\frac12<1$. (Or: $\frac{10n+3}{n}\le13$, so $a_n\le\frac{13}{2^n}$.)
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**7)** $\displaystyle\sum_{n=1}^\infty\frac{(-1)^n3^n}{n2^n}$ (any test)

> [!check]- Solution
>
> $|a_n|=\frac{(3/2)^n}{n}\to\infty$, so the terms don't approach $0$ ($n$th-term test). (Ratio gives $\frac32>1$ too.)
>
> **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**8)** $a_1=2,\ a_{n+1}=\dfrac{2n+1}{5n-4} a_n$. Does $\sum a_n$ converge?

> [!check]- Solution
>
> The recursion gives the ratio directly: $\frac{a_{n+1}}{a_n}=\frac{2n+1}{5n-4}\to\frac25<1$ (all terms positive).
>
> **Answer:** $\color{red}{\boxed{\text{Converges (ratio test)}}}$

**9)** $1+\dfrac{1\cdot3}{1\cdot2\cdot3}+\dfrac{1\cdot3\cdot5}{1\cdot2\cdot3\cdot4\cdot5}+\dfrac{1\cdot3\cdot5\cdot7}{1\cdot2\cdots7}+\cdots$

> [!check]- Solution
>
> $a_n=\dfrac{1\cdot3\cdots(2n-1)}{(2n-1)!}$, so $\dfrac{a_{n+1}}{a_n}=\dfrac{2n+1}{(2n)(2n+1)}=\dfrac1{2n}\to0<1$: converges.
>
> (Since $(2n-1)!=[1\cdot3\cdots(2n-1)][2\cdot4\cdots(2n-2)]$, $a_n=\frac{1}{2^{n-1}(n-1)!}$ and the sum is $\sum\frac{(1/2)^k}{k!}=\sqrt e$.)
>
> **Answer:** $\color{red}{\boxed{\text{Converges}}}$

**10)** Which is/are **divergent**? I. $\sum\dfrac5{n!}$ II. $\sum\dfrac{9^n}{n^5}$ III. $\sum_{n=2}^\infty e^{-3n}$

> [!check]- Solution
>
> I: ratio $\frac{1}{n+1}\to0$, converges. II: ratio $9\big(\frac{n}{n+1}\big)^5\to9$, diverges. III: geometric, $r=e^{-3}$, converges.
>
> **Answer:** $\color{red}{\boxed{\text{II only}}}$

**11)** Apply the ratio test to $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n-1}(\pi/2)^n}{n^2}$: find $\lim\Big|\frac{a_{n+1}}{a_n}\Big|$ and conclude.

> [!check]- Solution
>
> $\frac\pi2\cdot\frac{n^2}{(n+1)^2}\to\frac\pi2\approx1.57>1$.
>
> **Answer:** $\color{red}{\boxed{>1,\ \text{diverges}}}$

**12)** If $a_1=1$ and $a_{n+1}=\dfrac{\sin n+1}{\sqrt n} a_n$, does $\sum a_n$ converge or diverge?

> [!check]- Solution
>
> $0\le\frac{a_{n+1}}{a_n}=\frac{\sin n+1}{\sqrt n}\le\frac{2}{\sqrt n}\to0$, so $L=0<1$.
>
> **Answer:** $\color{red}{\boxed{\text{converges by the ratio test}}}$

**13)** Does $\displaystyle\sum_{n=1}^\infty\frac{3\cdot5\cdot7\cdots(2n+1)}{18^n(2n-1) n!}$ converge or diverge?

> [!check]- Solution
>
> $\frac{a_{n+1}}{a_n}=\frac{(2n+3)(2n-1)}{18(2n+1)(n+1)}\to\frac{4}{36}=\frac19<1$.
>
> **Answer:** $\color{red}{\boxed{\text{converges by the ratio test}}}$

**14)** For $a_n=\dfrac{n}{3^n}$, $\lim\sqrt[n]{|a_n|}=$

> [!check]- Solution
>
> $\frac{\sqrt[n]n}{3}\to\frac13$.
>
> **Answer:** $\color{red}{\boxed{\tfrac13}}$

**15)** For $a_n=\dfrac{(n!)^n}{(n^n)^2}$, find $L=\lim\sqrt[n]{|a_n|}$ and decide whether $\sum a_n$ converges.

> [!check]- Solution
>
> $\sqrt[n]{a_n}=\frac{n!}{n^2}\to\infty$.
>
> **Answer:** $\color{red}{\boxed{\text{diverges},\ L=\infty}}$

**16)** For positive $p$, $\displaystyle\sum_{n=1}^\infty\Big(\frac3{2p}\Big)^n$ converges if

> [!check]- Solution
>
> Root (or geometric): need $\frac3{2p}<1\iff p>\frac32$.
>
> **Answer:** $\color{red}{\boxed{p>\tfrac32}}$

**17)** Which is/are **divergent**? I. $\sum_{n=0}^\infty\dfrac{6^n}{(n+1)^3}$ II. $\sum_{n=0}^\infty\dfrac{(n!)^2}{(3n)!}$ III. $\sum\Big(\dfrac{-3n}{2n+1}\Big)^{3n}$

> [!check]- Solution
>
> I: ratio $\to6$, diverges. II: ratio $\frac{(n+1)^2}{(3n+1)(3n+2)(3n+3)}\to0$, converges. III diverges (B4).
>
> **Answer:** $\color{red}{\boxed{\text{I and III only}}}$

**18)** Which is/are **divergent**? I. $\sum\dfrac{9^n}{n^5}$ II. $\sum\dfrac{(2n)!}{n^5}$ III. $\sum\Big(\dfrac{3n+2}{n+3}\Big)^n$

> [!check]- Solution
>
> I: ratio $\to9$. II: ratio $\to\infty$ (B2). III: root $\to3$. All $>1$.
>
> **Answer:** $\color{red}{\boxed{\text{I, II and III}}}$

**19)** Which is/are **convergent**? I. $\sum\dfrac{(n-1)!}{4^n}$ II. $\sum n^2\Big(\dfrac56\Big)^n$ III. $\sum\Big(\dfrac{n-2}{5n+1}\Big)^n$

> [!check]- Solution
>
> I: ratio $\frac n4\to\infty$, diverges. II: ratio $\to\frac56$, converges. III: root $\to\frac15$, converges.
>
> **Answer:** $\color{red}{\boxed{\text{II and III only}}}$

**20)** Decide whether each converges: (I) $\sum_{n=0}^\infty\dfrac{(n!)^3}{(3n)!}$ (II) $\sum\Big(\dfrac{\ln n}{n}\Big)^n$

> [!check]- Solution
>
> I: ratio $\frac{(n+1)^3}{(3n+1)(3n+2)(3n+3)}\to\frac1{27}<1$. II: root $\frac{\ln n}{n}\to0<1$.
>
> **Answer:** $\color{red}{\boxed{\text{Both series converge}}}$

## 9.7 Taylor Polynomials and Approximations (20 problems)

**1)** Find the first-degree polynomial $P_1$ whose value and slope agree with $f(x)=\sec x$ at $c=\frac\pi6$.

> [!check]- Solution
>
> $f\big(\frac\pi6\big)=\frac{2}{\sqrt3}$, $f'(x)=\sec x\tan x\Rightarrow f'\big(\frac\pi6\big)=\frac2{\sqrt3}\cdot\frac1{\sqrt3}=\frac23$.
>
> $$P_1(x)=f(c)+f'(c)(x-c)$$
>
> **Answer:** $\color{red}{\boxed{P_1(x)=\frac{2}{\sqrt3}+\frac23\Big(x-\frac\pi6\Big)}}$

**2)** Find the 4th Maclaurin polynomial for $f(x)=xe^x$.

> [!check]- Solution
>
> $e^x\approx1+x+\frac{x^2}{2}+\frac{x^3}{6}$, so multiply by $x$ and keep terms up to $x^4$.
>
> (Or with derivatives: $f^{(n)}(x)=(x+n)e^x$, so $f^{(n)}(0)=n$ and the coefficient of $x^n$ is $\frac{n}{n!}=\frac1{(n-1)!}$.)
>
> **Answer:** $\color{red}{\boxed{P_4(x)=x+x^2+\frac{x^3}{2}+\frac{x^4}{6}}}$

**3)** Find the 4th Maclaurin polynomial for $f(x)=x^2e^{-x}$.

> [!check]- Solution
>
> $e^{-x}\approx1-x+\frac{x^2}2-\cdots$, so $x^2e^{-x}\approx x^2-x^3+\frac{x^4}{2}$.
>
> **Answer:** $\color{red}{\boxed{P_4(x)=x^2-x^3+\frac12x^4}}$

**4)** Find the 4th Maclaurin polynomial for $f(x)=\dfrac{x}{x+1}$.

> [!check]- Solution
>
> $\frac1{1+x}=1-x+x^2-x^3+\cdots$, so $\frac{x}{1+x}=x-x^2+x^3-x^4+\cdots$
>
> (Check: $f^{(n)}(0)=(-1)^{n+1}n!$ for $n\ge1$.)
>
> **Answer:** $\color{red}{\boxed{P_4(x)=x-x^2+x^3-x^4}}$

**5)** Find the 3rd Taylor polynomial for $f(x)=\dfrac2x$ centered at $c=1$.

> [!check]- Solution
>
> $f=2x^{-1},\ f'=-2x^{-2},\ f''=4x^{-3},\ f'''=-12x^{-4}$. At $x=1$: $2,-2,4,-12$.
>
> $$P_3=2-2(x-1)+\frac{4}{2!}(x-1)^2-\frac{12}{3!}(x-1)^3$$
>
> **Answer:** $\color{red}{\boxed{P_3(x)=2-2(x-1)+2(x-1)^2-2(x-1)^3}}$

**6)** Find the 3rd Taylor polynomial for $f(x)=\sqrt[3]x$ centered at $c=8$.

> [!check]- Solution
>
> $f(8)=2$, $f'=\frac13x^{-2/3}\Rightarrow\frac1{12}$, $f''=-\frac29x^{-5/3}\Rightarrow-\frac{1}{144}$, $f'''=\frac{10}{27}x^{-8/3}\Rightarrow\frac{5}{3456}$.
>
> $$P_3=2+\frac{1}{12}(x-8)-\frac{1/144}{2}(x-8)^2+\frac{5/3456}{6}(x-8)^3$$
>
> **Answer:** $\color{red}{\boxed{P_3(x)=2+\frac{x-8}{12}-\frac{(x-8)^2}{288}+\frac{5(x-8)^3}{20736}}}$

**7)** Use the polynomial from the previous problem to approximate $\sqrt[3]{8.05}$.

> [!check]- Solution
>
> With $x-8=0.05$:
>
> $$P_3(8.05)=2+\frac{0.05}{12}-\frac{0.0025}{288}+\frac{5(0.000125)}{20736}\approx2+0.0041667-0.0000087+0.00000003$$
>
> **Answer:** $\color{red}{\boxed{\sqrt[3]{8.05}\approx2.00416}}$

**8)** Use Taylor's Theorem to bound the error of $\cos(0.3)\approx1-\dfrac{(0.3)^2}{2!}+\dfrac{(0.3)^4}{4!}$, then find the actual error.

> [!check]- Solution
>
> This is $P_4$ for $\cos x$. $R_4=\frac{f^{(5)}(z)}{5!}x^5$ with $f^{(5)}=-\sin z$, $|\sin z|\le1$:
>
> $$|R_4|\le\frac{(0.3)^5}{5!}=0.00002025$$
>
> Actual: $\cos0.3-0.9553375\approx-1.01\times10^{-6}$.
>
> **Answer:** $\color{red}{\boxed{|R_4|\le2.025\times10^{-5};\ \text{actual error}\approx1.01\times10^{-6}}}$

**9)** Find the degree of the Maclaurin polynomial needed so that the error in approximating $\sin(0.3)$ is less than $0.001$.

> [!check]- Solution
>
> $|R_n|\le\frac{(0.3)^{n+1}}{(n+1)!}$ since every derivative of $\sin$ is at most $1$.
>
> $n=2$: $\frac{0.027}{6}=0.0045$ (too big). $n=3$: $\frac{0.0081}{24}=0.0003375<0.001$.
>
> **Answer:** $\color{red}{\boxed{n=3}}$

**10)** Compare the Maclaurin polynomial of degree 4 for $f(x)=e^x$ with the one of degree 5 for $g(x)=xe^x$. What is the relationship between them?

> [!check]- Solution
>
> $P_4^{f}(x)=1+x+\frac{x^2}{2}+\frac{x^3}{6}+\frac{x^4}{24}$
>
> $P_5^{g}(x)=x+x^2+\frac{x^3}{2}+\frac{x^4}{6}+\frac{x^5}{24}$
>
> **Answer:** $\color{red}{\boxed{P_5^{g}(x)=x P_4^{f}(x)}}$

**11)** Find the second Taylor polynomial for $f(x)=\sqrt x$ centered at $c=4$.

> [!check]- Solution
>
> $f(4)=2$, $f'=\frac{1}{2\sqrt x}\Rightarrow\frac14$, $f''=-\frac14x^{-3/2}\Rightarrow-\frac14\cdot\frac18=-\frac1{32}$, so $\frac{f''(4)}{2!}=-\frac1{64}$.
>
> **Answer:** $\color{red}{\boxed{P_2(x)=2+\frac14(x-4)-\frac1{64}(x-4)^2}}$

**12)** If the 2nd Taylor polynomial for $f(x)=\sqrt x$ centered at $c=4$ is written as $p_2(x)=a_2x^2+a_1x+a_0$, find $64a_2+8a_1+4a_0$.

> [!check]- Solution
>
> Expand $P_2=2+\frac14(x-4)-\frac1{64}(x-4)^2$:
>
> $-\frac1{64}(x^2-8x+16)=-\frac{x^2}{64}+\frac x8-\frac14$ and $\frac14(x-4)=\frac x4-1$.
>
> So $a_2=-\frac1{64},\ a_1=\frac38,\ a_0=\frac34$, and $64a_2+8a_1+4a_0=-1+3+3$.
>
> **Answer:** $\color{red}{\boxed{5}}$

**13)** If the 3rd Taylor polynomial for $f(x)=\dfrac2x$ centered at $c=1$ is written as $p_3(x)=a_3x^3+a_2x^2+a_1x+a_0$, find $a_3+a_2+a_1+a_0$.

> [!check]- Solution
>
> $a_3+a_2+a_1+a_0=p_3(1)$, and a Taylor polynomial always matches $f$ at its center: $p_3(1)=f(1)=2$.
>
> **Answer:** $\color{red}{\boxed{2}}$

**14)** If $P_3(x)=2+b(x-1)+c(x-1)^2+d(x-1)^3$ is the 3rd Taylor polynomial for $f(x)=\dfrac2x$ at $x=1$, find $b+c+d$.

> [!check]- Solution
>
> From the 3rd Taylor polynomial above: $b=-2,\ c=2,\ d=-2$.
>
> **Answer:** $\color{red}{\boxed{-2}}$

**15)** Use the second-degree Maclaurin polynomial of $f(x)=\sec x$ to approximate $\sec1$.

> [!check]- Solution
>
> $f(0)=1$, $f'=\sec x\tan x\Rightarrow0$, $f''=\sec x\tan^2x+\sec^3x\Rightarrow1$. So $P_2=1+\frac{x^2}{2}$ and $P_2(1)=\frac32$.
>
> **Answer:** $\color{red}{\boxed{\frac32}}$

**16)** Use the third-degree Maclaurin polynomial of $f(x)=\tan x$ to approximate $\tan1$.

> [!check]- Solution
>
> $f(0)=0,\ f'(0)=\sec^20=1,\ f''(0)=2\sec^2x\tan x\big|_0=0,\ f'''(0)=2$. So $P_3=x+\frac{x^3}{3}$ and $P_3(1)=\frac43$.
>
> **Answer:** $\color{red}{\boxed{\frac43}}$

**17)** If $p_2(x)$ is the second Maclaurin polynomial for $f(x)=\cos\pi x$, find $p_2\Big(\dfrac1\pi\Big)$.

> [!check]- Solution
>
> $f(0)=1,\ f'(0)=0,\ f''(0)=-\pi^2$, so $p_2(x)=1-\frac{\pi^2x^2}{2}$ and $p_2\big(\frac1\pi\big)=1-\frac12$.
>
> **Answer:** $\color{red}{\boxed{\frac12}}$

**18)** Use the fourth Maclaurin polynomial of $f(x)=e^{4x}$ to approximate $e$.

> [!check]- Solution
>
> $P_4(x)=1+4x+\frac{(4x)^2}{2}+\frac{(4x)^3}{6}+\frac{(4x)^4}{24}$. Since $e=f\big(\frac14\big)$:
>
> $$P_4\Big(\frac14\Big)=1+1+\frac12+\frac16+\frac1{24}=\frac{65}{24}$$
>
> **Answer:** $\color{red}{\boxed{\frac{65}{24}}}$

**19)** If $P_3(x)$ is the third Maclaurin polynomial for $f(x)=x^2e^x$, find $P_3(1)$.

> [!check]- Solution
>
> $x^2e^x=x^2\big(1+x+\cdots\big)$, so $P_3(x)=x^2+x^3$ and $P_3(1)=2$.
>
> **Answer:** $\color{red}{\boxed{2}}$

**20)** Find the coefficient of $x^2$ in the Maclaurin polynomial of $f(x)=\dfrac{-x+\sin x}{x^3}$.

> [!check]- Solution
>
> $\sin x-x=-\frac{x^3}{3!}+\frac{x^5}{5!}-\cdots$, so
>
> $$f(x)=-\frac16+\frac{x^2}{120}-\cdots$$
>
> **Answer:** $\color{red}{\boxed{\frac1{120}}}$

## 9.8 Power Series (20 problems)

**1)** Find the radius of convergence of $\displaystyle\sum_{n=1}^\infty\frac{(4x)^n}{n^2}$.

> [!check]- Solution
>
> $$\lim\Big|\frac{a_{n+1}}{a_n}\Big|=\lim\frac{4|x| n^2}{(n+1)^2}=4|x|<1\iff|x|<\frac14$$
>
> **Answer:** $\color{red}{\boxed{R=\frac14}}$

**2)** Find the interval of convergence of $\displaystyle\sum_{n=0}^\infty\frac{(3x)^n}{(2n)!}$.

> [!check]- Solution
>
> $$\lim\Big|\frac{a_{n+1}}{a_n}\Big|=\lim\frac{3|x|}{(2n+2)(2n+1)}=0<1\quad\text{for every }x$$
>
> **Answer:** $\color{red}{\boxed{(-\infty,\infty)}}$

**3)** Find the interval of convergence of $\displaystyle\sum_{n=0}^\infty\frac{(-1)^nx^n}{(n+1)(n+2)}$.

> [!check]- Solution
>
> Ratio: $\lim\frac{(n+1)(n+2)}{(n+2)(n+3)}|x|=|x|<1$.
>
> Endpoints: $x=1$: $\sum\frac{(-1)^n}{(n+1)(n+2)}$ converges; $x=-1$: $\sum\frac{1}{(n+1)(n+2)}$ converges (compare with $\sum\frac1{n^2}$).
>
> **Answer:** $\color{red}{\boxed{[-1,1]}}$

**4)** Find where $\displaystyle\sum_{n=0}^\infty\frac{(-1)^nn!(x-5)^n}{3^n}$ converges.

> [!check]- Solution
>
> $$\lim\Big|\frac{a_{n+1}}{a_n}\Big|=\lim\frac{(n+1)|x-5|}{3}=\infty\quad\text{unless }x=5$$
>
> **Answer:** $\color{red}{\boxed{\text{only at }x=5}}$

**5)** Find the interval of convergence of $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}(x-4)^n}{n9^n}$.

> [!check]- Solution
>
> Ratio: $\frac{|x-4|}{9}<1\iff-5<x<13$.
>
> $x=13$: $\sum\frac{(-1)^{n+1}}{n}$ converges (AST). $x=-5$: $\sum\frac{(-1)^{n+1}(-1)^n}{n}=-\sum\frac1n$ diverges.
>
> **Answer:** $\color{red}{\boxed{(-5,13]}}$

**6)** Find the interval of convergence of $\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}\cdot3\cdot7\cdot11\cdots(4n-1)(x-3)^n}{4^n}$.

> [!check]- Solution
>
> $$\lim\Big|\frac{a_{n+1}}{a_n}\Big|=\lim\frac{(4n+3)|x-3|}{4}=\infty\quad\text{unless }x=3$$
>
> **Answer:** $\color{red}{\boxed{\lbrace 3\rbrace \ (R=0)}}$

**7)** Find the radius of convergence of $\displaystyle\sum_{n=0}^\infty\frac{(n!)^kx^n}{(kn)!}$, where $k$ is a positive integer.

> [!check]- Solution
>
> $$\Big|\frac{a_{n+1}}{a_n}\Big|=\frac{(n+1)^k|x|}{(kn+1)(kn+2)\cdots(kn+k)}\to\frac{|x|}{k^k}$$
>
> since the denominator has $k$ factors each $\approx kn$.
>
> **Answer:** $\color{red}{\boxed{R=k^k}}$

**8)** Write an equivalent series for $\displaystyle\sum_{n=0}^\infty\frac{x^n}{n!}$ with the index starting at $n=1$.

> [!check]- Solution
>
> Replace $n$ by $n-1$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=1}^\infty\frac{x^{n-1}}{(n-1)!}}}$

**9)** For $f(x)=\displaystyle\sum_{n=0}^\infty\Big(\frac x3\Big)^n$, find the intervals of convergence of (a) $f$, (b) $f'$, (c) $f''$, (d) $\int f(x) dx$.

> [!check]- Solution
>
> $R=3$ for all four. $f$: at $x=\pm3$ terms are $1$ or $(-1)^n$, diverges.
>
> $f'=\sum\frac{nx^{n-1}}{3^n}$ and $f''$: endpoints diverge (terms don't go to $0$).
>
> $\int f=\sum\frac{3}{n+1}\big(\frac x3\big)^{n+1}$: $x=3$ gives $\sum\frac{3}{n+1}$ (diverges); $x=-3$ gives an alternating harmonic-type series (converges).
>
> **Answer:** $\color{red}{\boxed{(-3,3),\ (-3,3),\ (-3,3),\ [-3,3)}}$

**10)** For $f(x)=\displaystyle\sum_{n=0}^\infty\frac{(-1)^{n+1}(x-1)^{n+1}}{n+1}$, find the intervals of convergence of (a) $f$, (b) $f'$, (c) $f''$, (d) $\int f(x) dx$.

> [!check]- Solution
>
> Center $1$, $R=1$.
>
> $f$: $x=2$: $\sum\frac{(-1)^{n+1}}{n+1}$ converges; $x=0$: $\sum\frac{1}{n+1}$ diverges.
>
> $f'=\sum(-1)^{n+1}(x-1)^n$ and $f''$: terms don't go to $0$ at $x=0,2$.
>
> $\int f=\sum\frac{(-1)^{n+1}(x-1)^{n+2}}{(n+1)(n+2)}$: converges at both ends.
>
> **Answer:** $\color{red}{\boxed{(0,2],\ (0,2),\ (0,2),\ [0,2]}}$

**11)** Where does $\displaystyle\sum_{n=0}^\infty\frac{x^{2n}}{(2n)!}$ converge?

> [!check]- Solution
>
> $$\lim\frac{x^2}{(2n+2)(2n+1)}=0<1\quad\text{for all }x$$
>
> **Answer:** $\color{red}{\boxed{\text{for all }x}}$

**12)** Find the interval of convergence of $\displaystyle\sum_{n=0}^\infty\frac{(-1)^nx^{2n+1}}{2n+1}$.

> [!check]- Solution
>
> Ratio: $\lim\frac{2n+1}{2n+3}x^2=x^2<1$.
>
> $x=1$: $\sum\frac{(-1)^n}{2n+1}$ converges; $x=-1$: $\sum\frac{(-1)^{n+1}}{2n+1}$ converges (AST).
>
> **Answer:** $\color{red}{\boxed{[-1,1]}}$

**13)** Find the interval of convergence of $\displaystyle\sum_{n=1}^\infty\frac{(-1)^nx^n}{n}$.

> [!check]- Solution
>
> $R=1$. $x=1$: $\sum\frac{(-1)^n}{n}$ converges (AST). $x=-1$: $\sum\frac1n$ diverges.
>
> **Answer:** $\color{red}{\boxed{(-1,1]}}$

**14)** Where does $\displaystyle\sum_{n=1}^\infty\frac{x^{2n}}{2n}$ converge?

> [!check]- Solution
>
> Ratio: $x^2<1$. At $x=\pm1$: $\sum\frac1{2n}$ diverges.
>
> **Answer:** $\color{red}{\boxed{-1<x<1}}$

**15)** If $f(x)=\displaystyle\sum_{n=1}^\infty\frac{(-1)^{n+1}(x-5)^n}{n5^n}$, find the interval of convergence of $f$.

> [!check]- Solution
>
> Ratio: $\frac{|x-5|}{5}<1\iff0<x<10$.
>
> $x=10$: $\sum\frac{(-1)^{n+1}}{n}$ converges. $x=0$: $\sum\frac{(-1)^{n+1}(-1)^n}{n}=-\sum\frac1n$ diverges.
>
> **Answer:** $\color{red}{\boxed{(0,10]}}$

**16)** Find the interval of convergence of $\displaystyle\sum_{n=1}^\infty\frac{(x-3)^{n+1}}{(n+1)4^{n+1}}$.

> [!check]- Solution
>
> Ratio: $\frac{|x-3|}{4}<1\iff-1<x<7$.
>
> $x=7$: $\sum\frac1{n+1}$ diverges. $x=-1$: $\sum\frac{(-1)^{n+1}}{n+1}$ converges.
>
> **Answer:** $\color{red}{\boxed{[-1,7)}}$

**17)** If $f(x)=\displaystyle\sum_{n=2}^\infty\Big(\frac x2\Big)^n$, find the interval of convergence of $\displaystyle\int f(x) dx$.

> [!check]- Solution
>
> $\int f=\sum\frac{2}{n+1}\big(\frac x2\big)^{n+1}+C$, $R=2$.
>
> $x=2$: $\sum\frac2{n+1}$ diverges. $x=-2$: $\sum\frac{2(-1)^{n+1}}{n+1}$ converges.
>
> **Answer:** $\color{red}{\boxed{[-2,2)}}$

**18)** Find the interval of convergence of $\displaystyle\sum_{n=2}^\infty\frac{(x-1)^n}{2^n\sqrt n}$.

> [!check]- Solution
>
> Ratio: $\frac{|x-1|}{2}<1\iff-1<x<3$.
>
> $x=3$: $\sum\frac1{\sqrt n}$ diverges ($p=\frac12$). $x=-1$: $\sum\frac{(-1)^n}{\sqrt n}$ converges (AST).
>
> **Answer:** $\color{red}{\boxed{[-1,3)}}$

**19)** Find the interval $I$ and radius $R$ of convergence of $\displaystyle\sum_{n=1}^\infty\frac{(-1)^n2^nx^n}{(n+1)(n+2)}$.

> [!check]- Solution
>
> $$\Big|\frac{a_{n+1}}{a_n}\Big|=\frac{2(n+1)}{n+3}|x|\to2|x|<1\iff|x|<\frac12$$
>
> $x=-\frac12$: $\sum\frac{1}{(n+1)(n+2)}$ converges (LCT with $\sum\frac1{n^2}$). $x=\frac12$: $\sum\frac{(-1)^n}{(n+1)(n+2)}$ converges (AST).
>
> **Answer:** $\color{red}{\boxed{I=\Big[-\frac12,\frac12\Big],\ R=\frac12}}$

**20)** True or false? (i) If $f(x)=\sum_{n=0}^\infty a_nx^n$ converges for $|x|<2$, then $\int_0^1f(x) dx=\sum_{n=0}^\infty\frac{a_n}{n+1}$. (ii) If $\sum a_nx^n$ converges at $x=2$, it also converges at $x=-2$. (iii) Some power series has interval of convergence $[0,\infty)$. (iv) If $\sum a_nx^n$ has interval $(-1,1)$, then $\sum a_n(x-1)^n$ has interval $(-2,0)$. (v) The radius of convergence of $\sum\frac1n$ is $1$.

> [!check]- Solution
>
> (i) True: $[0,1]$ lies inside $|x|<2$, so integrate term by term.
>
> (ii) False: $\sum\frac{(-1)^nx^n}{n2^n}$ converges at $x=2$ but not at $x=-2$.
>
> (iii) False: an interval of convergence is centered at $c$, so it is either a point, all of $\mathbb R$, or bounded.
>
> (iv) False: shifting the center to $1$ gives $(0,2)$.
>
> (v) False: $\sum\frac1n$ is not a power series in $x$ (and it diverges).
>
> **Answer:** $\color{red}{\boxed{\text{only (i) is true}}}$

## 9.9 Representation of Functions by Power Series (21 problems)

**1)** Find a geometric power series for $f(x)=\dfrac{1}{4-x}$ centered at $0$.

> [!check]- Solution
>
> $$\frac1{4-x}=\frac{1/4}{1-\frac x4}=\sum_{n=0}^\infty\frac14\Big(\frac x4\Big)^n,\qquad\Big|\frac x4\Big|<1$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{x^n}{4^{n+1}},\ (-4,4)}}$

**2)** Find a power series for $f(x)=\dfrac{1}{6-x}$ centered at $c=1$, and its interval of convergence.

> [!check]- Solution
>
> $$\frac1{6-x}=\frac1{5-(x-1)}=\frac{1/5}{1-\frac{x-1}5}=\sum_{n=0}^\infty\frac{(x-1)^n}{5^{n+1}},\qquad|x-1|<5$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(x-1)^n}{5^{n+1}},\ (-4,6)}}$

**3)** Find a power series for $g(x)=\dfrac{4x}{x^2+2x-3}$ centered at $0$, and its interval of convergence.

> [!check]- Solution
>
> Partial fractions: $\frac{4x}{(x-1)(x+3)}=\frac1{x-1}+\frac3{x+3}$.
>
> $\frac1{x-1}=-\sum x^n\ (|x|<1)$ and $\frac3{x+3}=\frac1{1+x/3}=\sum\big(-\frac13\big)^nx^n\ (|x|<3)$.
>
> Both hold on the smaller interval.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\Big[\Big(-\frac13\Big)^n-1\Big]x^n,\ (-1,1)}}$

**4)** Find a power series for $f(x)=\dfrac{5}{4-x^2}$ centered at $0$, and its interval of convergence.

> [!check]- Solution
>
> $$\frac5{4-x^2}=\frac{5/4}{1-\frac{x^2}4}=\sum_{n=0}^\infty\frac54\Big(\frac{x^2}{4}\Big)^n,\qquad x^2<4$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{5x^{2n}}{4^{n+1}},\ (-2,2)}}$

**5)** Use $\dfrac1{1+x}=\sum(-1)^nx^n$ to find a power series for $h(x)=\dfrac{-2}{x^2-1}=\dfrac1{1+x}+\dfrac1{1-x}$.

> [!check]- Solution
>
> $$\sum(-1)^nx^n+\sum x^n=\sum\big[(-1)^n+1\big]x^n$$
>
> Odd powers cancel, even powers double.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty2x^{2n},\ (-1,1)}}$

**6)** Find a power series for $f(x)=\dfrac{2}{(x+1)^3}=\dfrac{d^2}{dx^2}\Big[\dfrac1{x+1}\Big]$.

> [!check]- Solution
>
> Differentiate $\sum_{n=0}^\infty(-1)^nx^n$ twice: $\sum_{n=2}^\infty(-1)^nn(n-1)x^{n-2}$. Shift the index ($n\to n+2$).
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty(-1)^n(n+1)(n+2)x^n,\ (-1,1)}}$

**7)** Find a power series for $f(x)=\ln(x+1)=\displaystyle\int\frac{dx}{x+1}$ and its interval of convergence.

> [!check]- Solution
>
> $$\ln(x+1)=\int\sum(-1)^nx^n dx=\sum_{n=0}^\infty\frac{(-1)^nx^{n+1}}{n+1}\quad(C=0\text{ since }\ln1=0)$$
>
> $x=1$ converges (alternating harmonic); $x=-1$ diverges.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(-1)^nx^{n+1}}{n+1},\ (-1,1]}}$

**8)** Use $\dfrac1{1-x}=\sum x^n$ to find a power series for $f(x)=\dfrac{x}{(1-x)^2}$.

> [!check]- Solution
>
> $\frac1{(1-x)^2}=\frac{d}{dx}\frac1{1-x}=\sum_{n=1}^\infty nx^{n-1}$. Multiply by $x$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=1}^\infty nx^n,\ (-1,1)}}$

**9)** Find a power series for $f(x)=\dfrac{x(1+x)}{(1-x)^2}$ centered at $0$.

> [!check]- Solution
>
> $\frac{x}{(1-x)^2}=\sum_{n\ge1}nx^n$ and $\frac{x^2}{(1-x)^2}=\sum_{n\ge1}nx^{n+1}=\sum_{n\ge2}(n-1)x^n$.
>
> Adding: the coefficient of $x^n$ is $n+(n-1)=2n-1$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=1}^\infty(2n-1)x^n,\ (-1,1)}}$

**10)** Find the sum of $\displaystyle\sum_{n=1}^\infty(-1)^{n+1}\frac{1}{2^nn}$.

> [!check]- Solution
>
> $\ln(1+x)=\sum_{n=1}^\infty\frac{(-1)^{n+1}x^n}{n}$ for $-1<x\le1$. Put $x=\frac12$.
>
> **Answer:** $\color{red}{\boxed{\ln\frac32}}$

**11)** Find the sum of $\displaystyle\sum_{n=0}^\infty(-1)^n\frac{1}{2^{2n+1}(2n+1)}$.

> [!check]- Solution
>
> $\arctan x=\sum_{n=0}^\infty\frac{(-1)^nx^{2n+1}}{2n+1}$. With $x=\frac12$: $x^{2n+1}=\frac1{2^{2n+1}}$.
>
> **Answer:** $\color{red}{\boxed{\arctan\frac12}}$

**12)** Find the power series for $f(x)=\dfrac{5}{2x-3}$ centered at $c=-3$.

> [!check]- Solution
>
> $2x-3=2(x+3)-9=-9\Big[1-\frac{2(x+3)}{9}\Big]$, so
>
> $$\frac5{2x-3}=-\frac59\sum_{n=0}^\infty\Big(\frac{2(x+3)}{9}\Big)^n,\qquad\Big|\frac29(x+3)\Big|<1$$
>
> **Answer:** $\color{red}{\boxed{-5\sum_{n=0}^\infty\frac{2^n}{9^{n+1}}(x+3)^n,\ \Big|\frac29(x+3)\Big|<1}}$

**13)** Find a power series for $f(x)=\dfrac{4}{2+x^2}$ centered at $0$.

> [!check]- Solution
>
> $$\frac4{2+x^2}=\frac{2}{1+\frac{x^2}2}=2\sum_{n=0}^\infty(-1)^n\frac{x^{2n}}{2^n},\qquad x^2<2$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty(-1)^n\frac{x^{2n}}{2^{n-1}},\ |x|<\sqrt2}}$

**14)** Find a power series for $f(x)=\dfrac{3x-1}{x^2-1}$ centered at $0$.

> [!check]- Solution
>
> $\frac{3x-1}{x^2-1}=\frac1{x-1}+\frac2{x+1}=-\sum x^n+2\sum(-1)^nx^n$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\big[2(-1)^n-1\big]x^n,\ (-1,1)}}$

**15)** Find a power series centered at $0$ for $f(x)=\dfrac{2x+1}{x^2-1}$.

> [!check]- Solution
>
> $$f(x)=-(2x+1)\cdot\frac{1}{1-x^2}=-(2x+1)\sum_{n=0}^\infty x^{2n}$$
>
> **Answer:** $\color{red}{\boxed{-\sum_{n=0}^\infty\big(x^{2n}+2x^{2n+1}\big)}}$

**16)** Find a power series for $f(x)=\dfrac{1}{(5-x)^2}$ centered at $c=2$.

> [!check]- Solution
>
> $\frac1{5-x}=\frac1{3-(x-2)}=\sum_{n=0}^\infty\frac{(x-2)^n}{3^{n+1}}$. Differentiate (since $\frac{d}{dx}\frac1{5-x}=\frac1{(5-x)^2}$):
>
> $$\sum_{n=1}^\infty\frac{n(x-2)^{n-1}}{3^{n+1}}=\sum_{n=0}^\infty\frac{(n+1)(x-2)^n}{3^{n+2}}$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{n+1}{3^{n+2}}(x-2)^n,\ (-1,5)}}$

**17)** Find the power series for $f(x)=\dfrac{1+x}{(1-x)^2}$.

> [!check]- Solution
>
> $\frac1{(1-x)^2}=\sum(n+1)x^n$ and $\frac{x}{(1-x)^2}=\sum nx^n$. Adding: $\sum(2n+1)x^n$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty(2n+1)x^n,\ |x|<1}}$

**18)** Evaluate $\dfrac1{10}\displaystyle\sum_{n=1}^\infty n\Big(\frac9{10}\Big)^n$.

> [!check]- Solution
>
> $\sum_{n=1}^\infty nx^n=\frac{x}{(1-x)^2}$. At $x=\frac9{10}$: $\frac{0.9}{0.01}=90$. Then $\frac{90}{10}=9$.
>
> **Answer:** $\color{red}{\boxed{9}}$

**19)** Find a power series for $f(x)=\ln x$ centered at $x=1$.

> [!check]- Solution
>
> $\frac1x=\frac1{1+(x-1)}=\sum(-1)^n(x-1)^n$. Integrate from $1$ (and $\ln1=0$):
>
> $$\ln x=\sum_{n=0}^\infty(-1)^n\frac{(x-1)^{n+1}}{n+1}$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty(-1)^n\frac{(x-1)^{n+1}}{n+1}}}$

**20)** Find a power series for $f(x)=\arctan(2x)$ centered at $0$.

> [!check]- Solution
>
> $$\arctan(2x)=\sum_{n=0}^\infty\frac{(-1)^n(2x)^{2n+1}}{2n+1}=2\sum_{n=0}^\infty\frac{(-1)^n4^nx^{2n+1}}{2n+1}$$
>
> **Answer:** $\color{red}{\boxed{2\sum_{n=0}^\infty\frac{(-1)^n4^nx^{2n+1}}{2n+1}}}$

**21)** Find a power series for $f(x)=\ln(x^2+1)$ centered at $0$, with its interval of convergence.

> [!check]- Solution
>
> $\ln(1+u)=\sum_{n=0}^\infty\frac{(-1)^nu^{n+1}}{n+1}$ for $-1<u\le1$. Put $u=x^2$: valid for $x^2\le1$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(-1)^nx^{2n+2}}{n+1},\ [-1,1]}}$

## 9.10 Taylor and Maclaurin Series (25 problems)

**1)** Find the Maclaurin series for $f(x)=e^{-4x}$.

> [!check]- Solution
>
> $f^{(n)}(x)=(-4)^ne^{-4x}$, so $f^{(n)}(0)=(-4)^n$. (Or substitute $-4x$ into $e^x=\sum\frac{x^n}{n!}$.)
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(-1)^n4^nx^n}{n!}}}$

**2)** Use the definition to find the Taylor series for $f(x)=\ln x$ centered at $c=1$.

> [!check]- Solution
>
> $f^{(n)}(x)=\frac{(-1)^{n+1}(n-1)!}{x^n}$, so $f^{(n)}(1)=(-1)^{n+1}(n-1)!$ and $\frac{f^{(n)}(1)}{n!}=\frac{(-1)^{n+1}}{n}$ (with $f(1)=0$).
>
> **Answer:** $\color{red}{\boxed{\sum_{n=1}^\infty\frac{(-1)^{n+1}(x-1)^n}{n}}}$

**3)** Find the Maclaurin series for $f(x)=\ln(x^2+1)$.

> [!check]- Solution
>
> Put $x^2$ into $\ln(1+x)=\sum_{n=1}^\infty\frac{(-1)^{n+1}x^n}{n}$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=1}^\infty\frac{(-1)^{n+1}x^{2n}}{n}}}$

**4)** Find the first three nonzero terms of the Maclaurin series for $f(x)=\sec x$.

> [!check]- Solution
>
> Divide $1$ by $\cos x=1-\frac{x^2}2+\frac{x^4}{24}-\cdots$: write $\sec x=1+ax^2+bx^4$, then
>
> $(1-\frac{x^2}2+\frac{x^4}{24})(1+ax^2+bx^4)=1\Rightarrow a=\frac12,\ b-\frac a2+\frac1{24}=0\Rightarrow b=\frac5{24}$.
>
> **Answer:** $\color{red}{\boxed{1+\frac{x^2}{2}+\frac{5x^4}{24}+\cdots}}$

**5)** Use the binomial series to find the Maclaurin series for $f(x)=\sqrt[4]{1+x}$.

> [!check]- Solution
>
> $(1+x)^k=1+kx+\frac{k(k-1)}{2!}x^2+\cdots$ with $k=\frac14$:
>
> $$1+\frac x4-\frac{3x^2}{4^2 2!}+\frac{3\cdot7x^3}{4^33!}-\cdots$$
>
> **Answer:** $\color{red}{\boxed{1+\frac x4+\sum_{n=2}^\infty\frac{(-1)^{n+1}3\cdot7\cdot11\cdots(4n-5)}{4^nn!}x^n}}$

**6)** Use the binomial series to find the Maclaurin series for $f(x)=\sqrt{1+x^3}$.

> [!check]- Solution
>
> $\sqrt{1+u}=1+\frac u2-\frac{u^2}{2^22!}+\frac{1\cdot3u^3}{2^33!}-\cdots$. Put $u=x^3$.
>
> **Answer:** $\color{red}{\boxed{1+\frac{x^3}{2}+\sum_{n=2}^\infty\frac{(-1)^{n+1}1\cdot3\cdot5\cdots(2n-3)}{2^nn!}x^{3n}}}$

**7)** Find the Maclaurin series for $g(x)=\arctan5x$.

> [!check]- Solution
>
> Put $5x$ into $\arctan x=\sum\frac{(-1)^nx^{2n+1}}{2n+1}$ (valid for $|5x|\le1$).
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(-1)^n5^{2n+1}x^{2n+1}}{2n+1}}}$

**8)** Find the Maclaurin series for $f(x)=\cos x^{3/2}$.

> [!check]- Solution
>
> $\cos u=\sum\frac{(-1)^nu^{2n}}{(2n)!}$ with $u=x^{3/2}$, so $u^{2n}=x^{3n}$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(-1)^nx^{3n}}{(2n)!}}}$

**9)** Find the Maclaurin series for $f(x)=x\sin x$.

> [!check]- Solution
>
> $$x\sin x=x\sum_{n=0}^\infty\frac{(-1)^nx^{2n+1}}{(2n+1)!}$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(-1)^nx^{2n+2}}{(2n+1)!}}}$

**10)** Find the first four nonzero terms of the Maclaurin series for $g(x)=\dfrac{\sin x}{1+x}$.

> [!check]- Solution
>
> $\big(x-\frac{x^3}{6}+\cdots\big)\big(1-x+x^2-x^3+\cdots\big)$:
>
> $x$; $-x^2$; $x^3-\frac{x^3}6=\frac56x^3$; $-x^4+\frac{x^4}{6}=-\frac56x^4$.
>
> **Answer:** $\color{red}{\boxed{x-x^2+\frac56x^3-\frac56x^4+\cdots}}$

**11)** Find a Maclaurin series for $f(x)=\displaystyle\int_0^x\big(e^{-t^2}-1\big) dt$.

> [!check]- Solution
>
> $e^{-t^2}-1=\sum_{n=1}^\infty\frac{(-1)^nt^{2n}}{n!}$. Integrate from $0$ to $x$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=1}^\infty\frac{(-1)^nx^{2n+1}}{(2n+1)n!}}}$

**12)** Verify that $\displaystyle\sum_{n=0}^\infty(-1)^n\frac{1}{(2n+1)!}=\sin1$.

> [!check]- Solution
>
> $\sin x=\sum_{n=0}^\infty\frac{(-1)^nx^{2n+1}}{(2n+1)!}$ for all $x$. Put $x=1$.
>
> **Answer:** $\color{red}{\boxed{\sin1\approx0.8415}}$

**13)** Verify that $\displaystyle\sum_{n=1}^\infty(-1)^{n-1}\frac1{n!}=\frac{e-1}{e}$.

> [!check]- Solution
>
> $e^{-1}=\sum_{n=0}^\infty\frac{(-1)^n}{n!}=1-\sum_{n=1}^\infty\frac{(-1)^{n-1}}{n!}$, so the sum is $1-\frac1e$.
>
> **Answer:** $\color{red}{\boxed{\frac{e-1}{e}\approx0.6321}}$

**14)** Use a series to find $\displaystyle\lim_{x\to0}\frac{\sin x}{x}$.

> [!check]- Solution
>
> $$\frac{\sin x}{x}=1-\frac{x^2}{3!}+\frac{x^4}{5!}-\cdots\to1$$
>
> **Answer:** $\color{red}{\boxed{1}}$

**15)** Write $\displaystyle\int_0^{1/2}\arctan(x^2) dx$ as a series and evaluate it.

> [!check]- Solution
>
> $\arctan(x^2)=\sum\frac{(-1)^nx^{4n+2}}{2n+1}$. Integrate:
>
> $$\int_0^{1/2}\arctan(x^2) dx=\sum_{n=0}^\infty\frac{(-1)^n}{(4n+3)(2n+1)2^{4n+3}}=\frac1{24}-\frac1{2688}+\cdots$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{(-1)^n}{(4n+3)(2n+1)2^{4n+3}}\approx0.0413}}$

**16)** Find the coefficient of $x^{11}$ in the Maclaurin series for $f(x)=x\sin(x^2)$.

> [!check]- Solution
>
> $$x\sin(x^2)=\sum_{n=0}^\infty\frac{(-1)^nx^{4n+3}}{(2n+1)!}$$
>
> $4n+3=11\Rightarrow n=2$: $\frac{1}{5!}$.
>
> **Answer:** $\color{red}{\boxed{\frac1{5!}}}$

**17)** Find the coefficient of $x^9$ in the Maclaurin series for $f(x)=2\sin x^3$.

> [!check]- Solution
>
> $$2\sin x^3=2\sum_{n=0}^\infty\frac{(-1)^nx^{6n+3}}{(2n+1)!}$$
>
> $6n+3=9\Rightarrow n=1$: $\frac{-2}{3!}=-\frac13$.
>
> **Answer:** $\color{red}{\boxed{-\frac13}}$

**18)** Find the Maclaurin series for $f(x)=e^{x^2/2}$.

> [!check]- Solution
>
> $$e^{x^2/2}=\sum_{n=0}^\infty\frac{(x^2/2)^n}{n!}$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty\frac{x^{2n}}{2^nn!}}}$

**19)** Find the power series for $f(x)=\cos\sqrt x$.

> [!check]- Solution
>
> $\cos u=\sum\frac{(-1)^nu^{2n}}{(2n)!}$ with $u=\sqrt x$, so $u^{2n}=x^n$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty(-1)^n\frac{x^n}{(2n)!}}}$

**20)** Find the first three terms of the Taylor series for $f(x)=\dfrac{1}{4-x}$ centered at $c=2$.

> [!check]- Solution
>
> $$\frac1{4-x}=\frac1{2-(x-2)}=\frac12\cdot\frac1{1-\frac{x-2}2}=\sum_{n=0}^\infty\frac{(x-2)^n}{2^{n+1}}$$
>
> **Answer:** $\color{red}{\boxed{\frac12+\frac14(x-2)+\frac18(x-2)^2}}$

**21)** Find the Maclaurin series for $f(x)=\cos^2x$.

> [!check]- Solution
>
> $\cos^2x=\frac12\big(1+\cos2x\big)$ and $\cos2x=\sum\frac{(-1)^n(2x)^{2n}}{(2n)!}$.
>
> **Answer:** $\color{red}{\boxed{\frac12\Big[1+\sum_{n=0}^\infty\frac{(-1)^n(2x)^{2n}}{(2n)!}\Big]}}$

**22)** Find the coefficient of $x^5$ in the power series of $f(x)=(\cos x)\ln(1+x)$.

> [!check]- Solution
>
> $\cos x=1-\frac{x^2}2+\frac{x^4}{24}-\cdots$, $\ln(1+x)=x-\frac{x^2}2+\frac{x^3}3-\frac{x^4}4+\frac{x^5}5-\cdots$
>
> $x^5$: $1\cdot\frac15+\big(-\frac12\big)\frac13+\frac1{24}\cdot1=\frac{24-20+5}{120}=\frac{9}{120}$.
>
> **Answer:** $\color{red}{\boxed{\frac3{40}}}$

**23)** Write $\displaystyle\int_0^2xe^{-2x^3} dx$ as a series.

> [!check]- Solution
>
> $xe^{-2x^3}=\sum\frac{(-1)^n2^nx^{3n+1}}{n!}$, so
>
> $$\int_0^2xe^{-2x^3}dx=\sum_{n=0}^\infty\frac{(-1)^n2^n}{n!}\cdot\frac{2^{3n+2}}{3n+2}$$
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty(-1)^n\frac{2^{4n+2}}{(3n+2) n!}}}$

**24)** Find a Maclaurin series for $\displaystyle\int_0^x\cos(t^2) dt$.

> [!check]- Solution
>
> $\cos(t^2)=\sum\frac{(-1)^nt^{4n}}{(2n)!}$. Integrate from $0$ to $x$.
>
> **Answer:** $\color{red}{\boxed{\sum_{n=0}^\infty(-1)^n\frac{x^{4n+1}}{(4n+1)(2n)!}}}$

**25)** Evaluate $\displaystyle\sum_{n=2}^\infty\frac{(-1)^{n+1}\cdot6}{(2n+1)!}$.

> [!check]- Solution
>
> $$\sum_{n=2}^\infty\frac{(-1)^{n+1}6}{(2n+1)!}=-6\Big[\sum_{n=0}^\infty\frac{(-1)^n}{(2n+1)!}-\Big(1-\frac16\Big)\Big]=-6\Big[\sin1-\frac56\Big]$$
>
> **Answer:** $\color{red}{\boxed{5-6\sin1}}$
