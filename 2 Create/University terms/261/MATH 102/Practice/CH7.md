# MATH 102 · Chapter 7 — Applications of Integration

## 7.1 Area of a Region Between Two Curves (24 problems)

**1)** Write (do not evaluate) a definite integral for the area between $y_1=x^2-6x$ and $y_2=0$.

> [!check]- Solution
> 
> $x^2-6x=0\Rightarrow x=0,6$, and on $(0,6)$ the parabola is below the axis, so top $=0$, bottom $=x^2-6x$. (Its value is $36$.) **Answer:** $\color{red}{\boxed{\displaystyle\int_0^6\big(6x-x^2\big) dx}}$

**2)** Write a definite integral for the area between $y_1=(x-1)^3$ and $y_2=x-1$.

> [!check]- Solution
> 
> $(x-1)^3=x-1\Rightarrow u^3=u$ with $u=x-1$ ⇒ $x=0,1,2$. On $(0,1)$ the cubic is on top; on $(1,2)$ the line is on top. $$A=\int_0^1\big[(x-1)^3-(x-1)\big]dx+\int_1^2\big[(x-1)-(x-1)^3\big]dx=\tfrac14+\tfrac14=\tfrac12$$
> 
> **Answer:** $\color{red}{\boxed{\displaystyle\int_0^1\big[(x-1)^3-(x-1)\big]dx+\int_1^2\big[(x-1)-(x-1)^3\big]dx=\tfrac12}}$

**3)** Sketch the region whose area is $\displaystyle\int_0^4\big(2\sqrt y-y\big) dy$ and find it.

> [!check]- Solution
> 
> Horizontal strips from the line $x=y$ (left) to the curve $x=2\sqrt y$ (right), for $0\le y\le4$; they meet at $(0,0)$ and $(4,4)$. $$\Big[\tfrac43y^{3/2}-\tfrac{y^2}{2}\Big]_0^4=\tfrac{32}{3}-8=\tfrac83$$ **Answer:** $\color{red}{\boxed{\text{region between }x=y\text{ and }x=2\sqrt y;\ A=\tfrac83}}$

**4)** Find the area bounded by $y=-x^2+3x+1$ and $y=-x+1$.

> [!check]- Solution
> 
> $-x^2+3x+1=-x+1\Rightarrow x(4-x)=0\Rightarrow x=0,4$; the parabola is on top. $$\int_0^4(4x-x^2) dx=32-\tfrac{64}{3}=\tfrac{32}{3}$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac{32}{3}}}$

**5)** Find the area bounded by $f(y)=y(2-y)$ and $g(y)=-y$.

> [!check]- Solution
> 
> $2y-y^2=-y\Rightarrow y(3-y)=0\Rightarrow y=0,3$; right curve $f$, left curve $g$. $$\int_0^3\big[(2y-y^2)-(-y)\big]dy=\int_0^3(3y-y^2) dy=\tfrac{27}{2}-9=\tfrac92$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac92}}$

**6)** Find the area bounded by $f(x)=\sin x$ and $g(x)=\cos2x$ for $-\frac\pi2\le x\le\frac\pi6$.

> [!check]- Solution
> 
> $\sin x=1-2\sin^2x\Rightarrow(2\sin x-1)(\sin x+1)=0$ ⇒ $x=\frac\pi6$ or $-\frac\pi2$ (the endpoints). At $x=0$: $\cos0=1>\sin0$, so $g$ is on top. $$\int_{-\pi/2}^{\pi/6}(\cos2x-\sin x) dx=\Big[\tfrac12\sin2x+\cos x\Big]_{-\pi/2}^{\pi/6}=\Big(\tfrac{\sqrt3}{4}+\tfrac{\sqrt3}{2}\Big)-0=\tfrac{3\sqrt3}{4}$$ **Answer:** $\color{red}{\boxed{\tfrac{3\sqrt3}{4}}}$

**7)** Find the area bounded by $f(x)=-2^x$ and $g(x)=1-3x$.

> [!check]- Solution
> 
> They meet at $x=1$ ($-2=-2$) and $x=3$ ($-8=-8$). At $x=2$: $f=-4>g=-5$, so $f$ is on top. $$\int_1^3\big(-2^x-1+3x\big)dx=\Big[-\frac{2^x}{\ln2}-x+\frac{3x^2}{2}\Big]_1^3=10-\frac{6}{\ln2}\approx1.344$$ **Answer:** $\color{red}{\boxed{10-\frac{6}{\ln2}\approx1.344}}$

**8)** Find the area of the region bounded by $y_1=\sin x,\ y_2=\cos x,\ y_3=\sin x+\cos x$ (figure: $0\le x\le\frac\pi2$).

> [!check]- Solution
> 
> Top is $y_3$. Bottom is $\cos x$ on $[0,\frac\pi4]$ and $\sin x$ on $[\frac\pi4,\frac\pi2]$: $$\int_0^{\pi/4}\sin x dx+\int_{\pi/4}^{\pi/2}\cos x dx=\Big(1-\tfrac{\sqrt2}{2}\Big)+\Big(1-\tfrac{\sqrt2}{2}\Big)=2-\sqrt2$$ **Answer:** $\color{red}{\boxed{2-\sqrt2}}$

**9)** Use integration to find the area of the triangle with vertices $(0,0),(6,0),(4,3)$.

> [!check]- Solution
> 
> In $y$: left edge $x=\frac43y$, right edge $x=6-\frac23y$, $0\le y\le3$: $$\int_0^3\Big(6-\tfrac23y-\tfrac43y\Big)dy=\int_0^3(6-2y) dy=18-9=9$$ **Answer:** $\color{red}{\boxed{9}}$

**10)** Find the area bounded by $f(x)=2x^3-1$ and its tangent line at $(1,1)$.

> [!check]- Solution
> 
> $f'(1)=6$, tangent $y=6x-5$. $2x^3-1=6x-5\Rightarrow x^3-3x+2=(x-1)^2(x+2)=0$. At $x=0$ the curve ($-1$) is above the line ($-5$). $$\int_{-2}^{1}(2x^3-6x+4) dx=\Big[\tfrac{x^4}{2}-3x^2+4x\Big]_{-2}^{1}=\tfrac32-(-12)=\tfrac{27}{2}$$ **Answer:** $\color{red}{\boxed{\tfrac{27}{2}}}$

**11)** Find $b$ such that the line $y=b$ divides the region bounded by $y=9-x^2$ and $y=0$ into two regions of equal area.

> [!check]- Solution
> 
> Total area $\int_{-3}^3(9-x^2) dx=36$. Above $y=b$: $\int_{-\sqrt{9-b}}^{\sqrt{9-b}}(9-b-x^2) dx=\frac43(9-b)^{3/2}$. $\frac43(9-b)^{3/2}=18\Rightarrow(9-b)^{3/2}=\frac{27}{2}\Rightarrow9-b=\frac{9}{\sqrt[3]4}$. **Answer:** $\color{red}{\boxed{b=9-\dfrac{9}{\sqrt[3]4}\approx3.330}}$

**12)** Show that the area of the ellipse $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ is $\pi ab$.

> [!check]- Solution
> 
> Upper half: $y=\frac ba\sqrt{a^2-x^2}$. By symmetry, $$A=4\int_0^a\frac ba\sqrt{a^2-x^2} dx=\frac{4b}{a}\cdot\frac{\pi a^2}{4}=\pi ab$$ (using $\int_0^a\sqrt{a^2-x^2} dx=$ area of a quarter circle). **Answer:** $\color{red}{\boxed{A=\pi ab}}$

**13)** The area enclosed by $x=2y^2$ and $x=4+y^2$ is

> [!check]- Solution
> 
> $2y^2=4+y^2\Rightarrow y=\pm2$; right curve $x=4+y^2$: $$\int_{-2}^2\big[(4+y^2)-2y^2\big]dy=2\int_0^2(4-y^2) dy=2\Big(8-\tfrac83\Big)=\tfrac{32}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{32}3}}$

**14)** The area of the region bounded by $y=\sin x,\ y=\cos x,\ x=0,\ x=\pi$ is

> [!check]- Solution
> 
> They cross at $x=\frac\pi4$. $$\int_0^{\pi/4}(\cos x-\sin x) dx+\int_{\pi/4}^{\pi}(\sin x-\cos x) dx=(\sqrt2-1)+(1+\sqrt2)=2\sqrt2$$
> 
> **Answer:** $\color{red}{\boxed{2\sqrt2}}$

**15)** The area enclosed by $y=12-x^2$ and $y=x^2-6$ is

> [!check]- Solution
> 
> $12-x^2=x^2-6\Rightarrow x=\pm3$: $$\int_{-3}^3(18-2x^2) dx=2\Big[18x-\tfrac{2x^3}{3}\Big]_0^3=2(54-18)=72$$ **Answer:** $\color{red}{\boxed{72}}$

**16)** The area of the region bounded by $y=x,\ y=x^2,\ x=0,\ x=2$ is

> [!check]- Solution
> 
> They cross at $x=1$: $x$ on top on $[0,1]$, $x^2$ on top on $[1,2]$. $$\int_0^1(x-x^2) dx+\int_1^2(x^2-x) dx=\tfrac16+\tfrac56=1$$ **Answer:** $\color{red}{\boxed{1}}$

**17)** The area bounded by $f(x)=\frac1{9x^2},\ y=1,\ x=1,\ x=2$ is

> [!check]- Solution
> 
> On $[1,2]$, $\frac1{9x^2}\le\frac19<1$, so $y=1$ is on top: $$\int_1^2\Big(1-\frac{1}{9x^2}\Big)dx=1+\Big[\frac{1}{9x}\Big]_1^2=1+\frac1{18}-\frac19=\frac{17}{18}$$ **Answer:** $\color{red}{\boxed{\tfrac{17}{18}}}$

**18)** The area bounded by $f(x)=\frac{-4}{x^3},\ y=0,\ x=-3,\ x=-1$ is

> [!check]- Solution
> 
> For $x<0$, $-\frac4{x^3}>0$: $$\int_{-3}^{-1}-4x^{-3} dx=\Big[\frac{2}{x^2}\Big]_{-3}^{-1}=2-\frac29=\frac{16}{9}$$ **Answer:** $\color{red}{\boxed{\tfrac{16}9}}$

**19)** The area bounded by $y=(x+1)^2$ and $y=1-|x|$ is

> [!check]- Solution
> 
> For $x\le0$, $1-|x|=1+x$; $(x+1)^2=1+x\Rightarrow x=-1,0$. (For $x>0$ the parabola is above $1-x$.) $$\int_{-1}^0\big[(1+x)-(x+1)^2\big]dx=\int_{-1}^0(-x-x^2) dx=\tfrac12-\tfrac13=\tfrac16$$ **Answer:** $\color{red}{\boxed{\tfrac16}}$

**20)** Find the area $A$ between $f(x)=\cos x$ and $g(x)=2-\cos x$ over $[0,2\pi]$.

> [!check]- Solution
> 
> $g-f=2-2\cos x\ge0$: $$A=\int_0^{2\pi}(2-2\cos x) dx=4\pi\approx12.57$$ **Answer:** $\color{red}{\boxed{A=4\pi\approx12.57}}$

**21)** The area bounded by $f(x)=2\sin x$ and $g(x)=\tan x$ over $\big[-\frac\pi3,\frac\pi3\big]$ is

> [!check]- Solution
> 
> $2\sin x=\tan x\Rightarrow x=0$ or $\cos x=\frac12$. Both functions are odd, so the two pieces have equal area; on $[0,\frac\pi3]$, $2\sin x\ge\tan x$. $$2\int_0^{\pi/3}(2\sin x-\tan x) dx=2\Big[-2\cos x+\ln|\cos x|\Big]_0^{\pi/3}=2\Big[(-1-\ln2)-(-2)\Big]=2(1-\ln2)$$ **Answer:** $\color{red}{\boxed{2(1-\ln2)}}$

**22)** The area bounded by $f(x)=\sin x$ and $g(x)=\frac2\pi x$ on $[0,\pi]$ is

> [!check]- Solution
> 
> They meet at $x=0,\frac\pi2$; $\sin x$ is on top on $[0,\frac\pi2]$ and the line on top on $[\frac\pi2,\pi]$. $$\Big[-\cos x-\frac{x^2}{\pi}\Big]_0^{\pi/2}+\Big[\frac{x^2}{\pi}+\cos x\Big]_{\pi/2}^{\pi}=\Big(1-\frac\pi4\Big)+\Big(\frac{3\pi}{4}-1\Big)=\frac\pi2$$ **Answer:** $\color{red}{\boxed{\tfrac\pi2}}$

**23)** The area of the region in the **first quadrant** bounded by $f(x)=x^2+2,\ g(x)=4-x^2,\ h(x)=2-x$ is

> [!check]- Solution
> 
> Intersections: $f=g$ at $x=1$; $f=h$ at $x=0$; $g=h$ at $x=2$. Bottom is $h$; top is $f$ on $[0,1]$ and $g$ on $[1,2]$. $$\int_0^1(x^2+x) dx+\int_1^2(2+x-x^2) dx=\tfrac56+\tfrac76=2$$
> 
> **Answer:** $\color{red}{\boxed{2}}$

**24)** $R$ is bounded by $y=2x-x^2$ and the $x$-axis. If $y=mx$ divides $R$ into two regions of equal area, then $m=$

> [!check]- Solution
> 
> Area of $R=\int_0^2(2x-x^2) dx=\frac43$. The line meets the parabola at $x=2-m$: $$\int_0^{2-m}\big[(2-m)x-x^2\big]dx=\frac{(2-m)^3}{6}=\frac12\cdot\frac43\Rightarrow(2-m)^3=4$$ **Answer:** $\color{red}{\boxed{m=2-\sqrt[3]4}}$

## 7.2 Volume — The Disk Method (24 problems)

**1)** Write and evaluate the integral for the volume when the region between $y=2$ and $y=4-\frac{x^2}{4}$ is revolved about the $x$-axis.

> [!check]- Solution
> 
> $4-\frac{x^2}4=2\Rightarrow x=\pm2\sqrt2$. Washer: $R=4-\frac{x^2}{4},\ r=2$. $$V=\pi\int_{-2\sqrt2}^{2\sqrt2}\Big[\Big(4-\frac{x^2}{4}\Big)^2-4\Big]dx=2\pi\int_0^{2\sqrt2}\Big(12-2x^2+\frac{x^4}{16}\Big)dx=2\pi\Big(24\sqrt2-\frac{32\sqrt2}{3}+\frac{8\sqrt2}{5}\Big)=\frac{448\sqrt2 \pi}{15}$$ **Answer:** $\color{red}{\boxed{\tfrac{448\sqrt2 \pi}{15}\approx132.7}}$

**2)** The region between $y=x^{2/3}$ and the $y$-axis for $0\le y\le1$ is revolved about the $y$-axis. Write and evaluate the integral.

> [!check]- Solution
> 
> $x=y^{3/2}$, horizontal disks of radius $x$: $$V=\pi\int_0^1\big(y^{3/2}\big)^2dy=\pi\int_0^1y^3dy=\frac\pi4$$ **Answer:** $\color{red}{\boxed{\tfrac\pi4}}$

**3)** Region bounded by $y=2x^2,\ y=0,\ x=2$. Find the volume about (a) the $y$-axis (b) the $x$-axis (c) $y=8$ (d) $x=2$.

> [!check]- Solution
> 
> (a) Washers in $y\in[0,8]$: $R=2,\ r=\sqrt{y/2}$: $\ \pi\int_0^8\big(4-\frac y2\big)dy=16\pi$. (b) Disks: $\pi\int_0^2(2x^2)^2dx=\pi\cdot\frac{4\cdot32}{5}=\frac{128\pi}{5}$. (c) $R=8,\ r=8-2x^2$: $\ \pi\int_0^2\big[64-(8-2x^2)^2\big]dx=\pi\int_0^2(32x^2-4x^4) dx=\frac{896\pi}{15}$. (d) Disks in $y$, radius $2-\sqrt{y/2}$: with $s=\sqrt{y/2}$ ($dy=4s ds$): $\ 4\pi\int_0^2(2-s)^2s ds=\frac{16\pi}{3}$. **Answer:** $\color{red}{\boxed{16\pi,\ \tfrac{128\pi}{5},\ \tfrac{896\pi}{15},\ \tfrac{16\pi}{3}}}$

**4)** Revolve the region bounded by $y=\frac{2}{1+x},\ y=0,\ x=0,\ x=4$ about the line $y=4$.

> [!check]- Solution
> 
> Washer: $R=4,\ r=4-\frac{2}{1+x}$: $$V=\pi\int_0^4\Big[\frac{16}{1+x}-\frac{4}{(1+x)^2}\Big]dx=\pi\Big[16\ln(1+x)+\frac{4}{1+x}\Big]_0^4=\pi\Big(16\ln5+\frac45-4\Big)=16\pi\Big(\ln5-\frac15\Big)$$
> 
> **Answer:** $\color{red}{\boxed{16\pi\big(\ln5-\tfrac15\big)\approx70.8}}$

**5)** Revolve the region bounded by $x=y^2$ and $x=4$ about the line $x=5$.

> [!check]- Solution
> 
> $y\in[-2,2]$. Washer: $R=5-y^2,\ r=5-4=1$: $$V=\pi\int_{-2}^{2}\big[(5-y^2)^2-1\big]dy=2\pi\int_0^2(24-10y^2+y^4) dy=2\pi\Big(48-\frac{80}{3}+\frac{32}{5}\Big)=\frac{832\pi}{15}$$ **Answer:** $\color{red}{\boxed{\tfrac{832\pi}{15}}}$

**6)** Revolve the region bounded by $y=\sqrt x,\ y=-\frac12x+4,\ x=0,\ x=8$ about the $x$-axis.

> [!check]- Solution
> 
> The curves cross at $x=4$ (both $=2$). The line is on top on $[0,4]$, $\sqrt x$ on top on $[4,8]$. $$\pi\int_0^4\Big[\Big(4-\frac x2\Big)^2-x\Big]dx+\pi\int_4^8\Big[x-\Big(4-\frac x2\Big)^2\Big]dx=\pi\Big(\frac{88}{3}+\frac{56}{3}\Big)=48\pi$$
> 
> **Answer:** $\color{red}{\boxed{48\pi}}$

**7)** Revolve the region bounded by $y=9-x^2,\ y=0,\ x=2,\ x=3$ about the $y$-axis.

> [!check]- Solution
> 
> Slices in $y\in[0,5]$: $x$ runs from $2$ to $\sqrt{9-y}$, so $R=\sqrt{9-y},\ r=2$: $$V=\pi\int_0^5\big[(9-y)-4\big]dy=\pi\Big[5y-\frac{y^2}{2}\Big]_0^5=\frac{25\pi}{2}$$ **Answer:** $\color{red}{\boxed{\tfrac{25\pi}{2}}}$

**8)** Revolve the region bounded by $y=\cos2x,\ y=0,\ x=0,\ x=\frac\pi4$ about the $x$-axis.

> [!check]- Solution
> 
> $$V=\pi\int_0^{\pi/4}\cos^22x dx=\pi\int_0^{\pi/4}\frac{1+\cos4x}{2}dx=\pi\Big[\frac x2+\frac{\sin4x}{8}\Big]_0^{\pi/4}=\frac{\pi^2}{8}$$ **Answer:** $\color{red}{\boxed{\tfrac{\pi^2}{8}}}$

**9)** The region bounded by $y=\sqrt x,\ y=0,\ x=1,\ x=3$ is revolved about the $x$-axis. Find the $x$ in $[1,3]$ that divides the solid into two parts of equal volume.

> [!check]- Solution
> 
> Total: $\pi\int_1^3x dx=4\pi$. Need $\pi\int_1^cx dx=\frac\pi2(c^2-1)=2\pi\Rightarrow c^2=5$.
> 
> **Answer:** $\color{red}{\boxed{x=\sqrt5}}$

**10)** The base of a solid is bounded by $y=x+1$ and $y=x^2-1$. Find the volume if the cross sections perpendicular to the $x$-axis are (a) squares (b) rectangles of height 1.

> [!check]- Solution
> 
> $x+1=x^2-1\Rightarrow x=-1,2$; side $s=(x+1)-(x^2-1)=2+x-x^2$. (a) $\int_{-1}^2(2+x-x^2)^2dx=\int_{-1}^2(x^4-2x^3-3x^2+4x+4) dx=\frac{81}{10}$ (b) $\int_{-1}^2(2+x-x^2) dx=\frac92$
> 
> **Answer:** $\color{red}{\boxed{\text{(a) }\tfrac{81}{10}\quad\text{(b) }\tfrac92}}$

**11)** The base is the disk $x^2+y^2\le4$. Find the volume if the cross sections perpendicular to the $x$-axis are (a) squares (b) equilateral triangles (c) semicircles (d) isosceles right triangles (hypotenuse in the base, as in the figure).

> [!check]- Solution
> 
> The chord at $x$ has length $s=2\sqrt{4-x^2}$, and $\int_{-2}^2(4-x^2) dx=\frac{32}3$. (a) $s^2=4(4-x^2)$: $\ 4\cdot\frac{32}{3}=\frac{128}{3}$ (b) $\frac{\sqrt3}{4}s^2=\sqrt3(4-x^2)$: $\ \frac{32\sqrt3}{3}$ (c) $\frac\pi8s^2=\frac\pi2(4-x^2)$: $\ \frac{16\pi}{3}$ (d) hypotenuse $s$ ⇒ area $\frac{s^2}{4}=4-x^2$: $\ \frac{32}{3}$ **Answer:** $\color{red}{\boxed{\tfrac{128}{3},\ \tfrac{32\sqrt3}{3},\ \tfrac{16\pi}{3},\ \tfrac{32}{3}}}$

**12)** The volume of the solid obtained by rotating the region bounded by $y=\ln x,\ y=0,\ y=2,\ x=0$ about $x=-1$ is

> [!check]- Solution
> 
> In $y$: $x$ from $0$ to $e^y$. Washer about $x=-1$: $R=e^y+1,\ r=1$. $$V=\pi\int_0^2\big[(e^y+1)^2-1\big]dy=\pi\Big[\frac{e^{2y}}{2}+2e^y\Big]_0^2=\frac\pi2\big(e^4+4e^2-5\big)$$ **Answer:** $\color{red}{\boxed{\tfrac\pi2(e^4+4e^2-5)}}$

**13)** The base of a solid is bounded by $y=\sqrt x,\ x=1,\ y=0$. Cross sections perpendicular to the $x$-axis are **equilateral triangles**. The volume is

> [!check]- Solution
> 
> $s=\sqrt x$: $\ V=\int_0^1\frac{\sqrt3}{4}x dx=\frac{\sqrt3}{8}$. **Answer:** $\color{red}{\boxed{\tfrac{\sqrt3}8}}$

**14)** Rotate the region bounded by $y=e^x,\ x=0,\ x=1,\ y=0$ about the line $y=4$. The volume is

> [!check]- Solution
> 
> Washer: $R=4-0=4,\ r=4-e^x$: $$V=\pi\int_0^1\big[16-(4-e^x)^2\big]dx=\pi\int_0^1(8e^x-e^{2x}) dx=\pi\Big[8e^x-\tfrac12e^{2x}\Big]_0^1=\frac\pi2(16e-e^2-15)$$ **Answer:** $\color{red}{\boxed{\tfrac\pi2(16e-e^2-15)}}$

**15)** The base is bounded by $x=y^3,\ y=1,\ x=0$. Cross sections perpendicular to the $y$-axis are **semicircles**. The volume is

> [!check]- Solution
> 
> Diameter $d=y^3$, radius $\frac{y^3}{2}$: $\ A(y)=\frac\pi2\Big(\frac{y^3}{2}\Big)^2=\frac\pi8y^6$. $$V=\int_0^1\frac\pi8y^6dy=\frac{\pi}{56}$$ **Answer:** $\color{red}{\boxed{\tfrac\pi{56}}}$

**16)** Revolve the region bounded by $y=\sqrt{1-x},\ x=0,\ y=0$ about the line $y=4$.

> [!check]- Solution
> 
> $R=4,\ r=4-\sqrt{1-x}$: $$\pi\int_0^1\big[16-(4-\sqrt{1-x})^2\big]dx=\pi\int_0^1\big[8\sqrt{1-x}-(1-x)\big]dx=\pi\Big(\frac{16}{3}-\frac12\Big)=\frac{29\pi}{6}$$ **Answer:** $\color{red}{\boxed{\tfrac{29\pi}6}}$

**17)** Revolve the region bounded by $y=x^2$ and $y=4x-x^2$ about the $x$-axis.

> [!check]- Solution
> 
> They meet at $x=0,2$; $R=4x-x^2,\ r=x^2$: $$\pi\int_0^2\big[(4x-x^2)^2-x^4\big]dx=\pi\int_0^2(16x^2-8x^3) dx=\pi\Big(\frac{128}{3}-32\Big)=\frac{32\pi}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{32\pi}3}}$

**18)** Revolve the region bounded by $y=x,\ y=3,\ x=0$ about the line $y=4$.

> [!check]- Solution
> 
> $R=4-x,\ r=4-3=1$: $$\pi\int_0^3\big[(4-x)^2-1\big]dx=\pi\Big[-\frac{(4-x)^3}{3}-x\Big]_0^3=\pi\Big(-\frac13-3+\frac{64}{3}\Big)=18\pi$$ **Answer:** $\color{red}{\boxed{18\pi}}$

**19)** Revolve the region bounded by $y=x^3,\ y=0,\ x=2$ about the line $x=4$.

> [!check]- Solution
> 
> Washers in $y\in[0,8]$: $x$ from $y^{1/3}$ to $2$, so $R=4-y^{1/3},\ r=4-2=2$: $$\pi\int_0^8\big[(4-y^{1/3})^2-4\big]dy=\pi\int_0^8\big(12-8y^{1/3}+y^{2/3}\big)dy=\pi\Big(96-96+\frac{96}{5}\Big)=\frac{96\pi}{5}$$ **Answer:** $\color{red}{\boxed{\tfrac{96\pi}5}}$

**20)** The base is bounded by $y=x^3,\ y=1,\ x=0$. Cross sections perpendicular to the $x$-axis are **squares**. The volume is

> [!check]- Solution
> 
> $s=1-x^3$: $$\int_0^1(1-x^3)^2dx=\int_0^1(1-2x^3+x^6) dx=1-\frac12+\frac17=\frac9{14}$$ **Answer:** $\color{red}{\boxed{\tfrac9{14}}}$

**21)** $S$ is formed by revolving the region bounded by $y=\sqrt x,\ y=0,\ x=1,\ x=3$ about the $x$-axis. If $c,d\in[1,3]$ divide $S$ into three parts of equal volume, then $c^2+d^2=$

> [!check]- Solution
> 
> Total $4\pi$, so each part is $\frac{4\pi}3$. $\frac\pi2(c^2-1)=\frac{4\pi}{3}\Rightarrow c^2=\frac{11}3$; $\ \frac\pi2(9-d^2)=\frac{4\pi}3\Rightarrow d^2=\frac{19}3$. **Answer:** $\color{red}{\boxed{c^2+d^2=10}}$

**22)** Revolve the region bounded by $y=x^5$ and $y=x^2$ about the $x$-axis.

> [!check]- Solution
> 
> On $[0,1]$, $x^2\ge x^5$: $$\pi\int_0^1(x^4-x^{10}) dx=\pi\Big(\frac15-\frac1{11}\Big)=\frac{6\pi}{55}$$ **Answer:** $\color{red}{\boxed{\tfrac{6\pi}{55}}}$

**23)** Revolve the region bounded by $y=\sqrt{25-x^2},\ y=0,\ x=0,\ x=3$ about the $x$-axis.

> [!check]- Solution
> 
> $$\pi\int_0^3(25-x^2) dx=\pi(75-9)=66\pi$$ **Answer:** $\color{red}{\boxed{66\pi}}$

**24)** Revolve the region bounded by $y^2=2x,\ y=4,\ x=0$ about the $x$-axis.

> [!check]- Solution
> 
> $y=\sqrt{2x}$ meets $y=4$ at $x=8$; region between $y=\sqrt{2x}$ (inner) and $y=4$ (outer): $$\pi\int_0^8\big(16-2x\big) dx=\pi(128-64)=64\pi$$ **Answer:** $\color{red}{\boxed{64\pi}}$

## 7.3 Volume — The Shell Method (22 problems)

**1)** Use shells to find the volume when the region bounded by $y=\sqrt{2x-5},\ y=0,\ x=4$ is revolved about the $y$-axis.

> [!check]- Solution
> 
> The region runs from $x=\frac52$ to $4$. With $u=2x-5$, $x=\frac{u+5}{2}$, $dx=\frac{du}2$: $$V=2\pi\int_{5/2}^4x\sqrt{2x-5} dx=\frac\pi2\int_0^3\big(u^{3/2}+5u^{1/2}\big)du=\frac\pi2\Big(\frac{18\sqrt3}{5}+10\sqrt3\Big)=\frac{34\sqrt3 \pi}{5}$$ **Answer:** $\color{red}{\boxed{\tfrac{34\sqrt3 \pi}{5}\approx37.0}}$

**2)** Use shells to revolve the region bounded by $y=1-\sqrt x,\ y=x+1,\ y=0$ about the $x$-axis.

> [!check]- Solution
> 
> In $y\in[0,1]$: left boundary $x=y-1$, right boundary $x=(1-y)^2$. Height $(1-y)^2-(y-1)=(1-y)(2-y)$. $$V=2\pi\int_0^1y(1-y)(2-y) dy=2\pi\int_0^1(2y-3y^2+y^3) dy=2\pi\Big(1-1+\frac14\Big)=\frac\pi2$$ **Answer:** $\color{red}{\boxed{\tfrac\pi2}}$

**3)** Use shells to revolve the region bounded by $y=3x-x^2$ and $y=x^2$ about the line $x=2$.

> [!check]- Solution
> 
> $3x-x^2=x^2\Rightarrow x=0,\frac32$. Radius $2-x$, height $3x-2x^2$: $$V=2\pi\int_0^{3/2}(2-x)(3x-2x^2) dx=2\pi\int_0^{3/2}(6x-7x^2+2x^3) dx=2\pi\cdot\frac{45}{32}=\frac{45\pi}{16}$$ **Answer:** $\color{red}{\boxed{\tfrac{45\pi}{16}}}$

**4)** Region bounded by $y=\frac{10}{x^2},\ y=0,\ x=1,\ x=5$. Find the volume about (a) the $x$-axis (b) the $y$-axis (c) $y=10$.

> [!check]- Solution
> 
> (a) Disks: $\pi\int_1^5\frac{100}{x^4}dx=\frac{100\pi}{3}\Big(1-\frac1{125}\Big)=\frac{496\pi}{15}$ (b) Shells: $2\pi\int_1^5x\cdot\frac{10}{x^2}dx=20\pi\ln5$ (c) Washers, $R=10,\ r=10-\frac{10}{x^2}$: $\ \pi\int_1^5\Big(\frac{200}{x^2}-\frac{100}{x^4}\Big)dx=\pi\Big(160-\frac{496}{15}\Big)=\frac{1904\pi}{15}$ **Answer:** $\color{red}{\boxed{\tfrac{496\pi}{15},\ 20\pi\ln5,\ \tfrac{1904\pi}{15}}}$

**5)** The integral $2\pi\displaystyle\int_0^6(y+2)\sqrt{6-y} dy$ is a volume. Identify (a) the plane region and (b) the axis of revolution.

> [!check]- Solution
> 
> Shells in $y$: radius $y+2$ means distance from the line $y=-2$; height $\sqrt{6-y}$ means horizontal strips from $x=0$ to $x=\sqrt{6-y}$ for $0\le y\le6$. **Answer:** $\color{red}{\boxed{\text{(a) region bounded by }y=6-x^2,\ x=0,\ y=0\text{ (1st quadrant)}\quad\text{(b) the line }y=-2}}$

**6)** A torus is formed by revolving the disk $x^2+y^2\le1$ about the line $x=2$. Find its volume.

> [!check]- Solution
> 
> Shells: radius $2-x$, height $2\sqrt{1-x^2}$: $$V=2\pi\int_{-1}^1(2-x) 2\sqrt{1-x^2} dx=8\pi\int_{-1}^1\sqrt{1-x^2} dx-4\pi\int_{-1}^1x\sqrt{1-x^2} dx=8\pi\cdot\frac\pi2-0=4\pi^2$$ (the first integral is a half disk; the second is odd). **Answer:** $\color{red}{\boxed{4\pi^2}}$

**7)** $V_1$ and $V_2$ are the volumes when the region bounded by $y=\frac1x,\ y=0,\ x=\frac14,\ x=c\ (c>\frac14)$ is revolved about the $x$-axis and the $y$-axis. Find $c$ with $V_1=V_2$.

> [!check]- Solution
> 
> $V_1=\pi\int_{1/4}^c\frac{dx}{x^2}=\pi\Big(4-\frac1c\Big)$, $\quad V_2=2\pi\int_{1/4}^cx\cdot\frac1x dx=2\pi\Big(c-\frac14\Big)$. $4-\frac1c=2c-\frac12\Rightarrow4c^2-9c+2=0\Rightarrow c=2$ or $\frac14$; we need $c>\frac14$. **Answer:** $\color{red}{\boxed{c=2}}$

**8)** Using shells, rotate the region bounded by $y=\frac2{x^2},\ x=1,\ x=3,\ y=0$ about the line $x=4$.

> [!check]- Solution
> 
> Radius $4-x$, height $\frac2{x^2}$: $$V=2\pi\int_1^3\Big(\frac8{x^2}-\frac2x\Big)dx=2\pi\Big[-\frac8x-2\ln x\Big]_1^3=2\pi\Big(\frac{16}{3}-2\ln3\Big)=\frac{4\pi}{3}(8-3\ln3)$$ **Answer:** $\color{red}{\boxed{\tfrac{4\pi}3(8-3\ln3)}}$

**9)** Using shells, rotate the region bounded by $y=5x-x^2$ and $y=3x$ about the line $x=3$.

> [!check]- Solution
> 
> $5x-x^2=3x\Rightarrow x=0,2$. Radius $3-x$, height $2x-x^2$: $$V=2\pi\int_0^2(3-x)(2x-x^2) dx=2\pi\int_0^2(6x-5x^2+x^3) dx=2\pi\Big(12-\frac{40}{3}+4\Big)=\frac{16\pi}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{16\pi}3}}$

**10)** Using shells, rotate the region bounded by $x=\sqrt y,\ y=2$ and the $y$-axis about the line $y=-1$.

> [!check]- Solution
> 
> Horizontal shells: radius $y+1$, height $\sqrt y$, $0\le y\le2$: $$V=2\pi\int_0^2\big(y^{3/2}+y^{1/2}\big)dy=2\pi\Big[\frac25y^{5/2}+\frac23y^{3/2}\Big]_0^2=2\pi\Big(\frac{8\sqrt2}{5}+\frac{4\sqrt2}{3}\Big)=\frac{88\sqrt2 \pi}{15}$$ **Answer:** $\color{red}{\boxed{\tfrac{88\pi}{15}\sqrt2}}$

**11)** Using shells, rotate the region bounded by $x=y-y^2$ and the $y$-axis about the line $y=2$.

> [!check]- Solution
> 
> $y-y^2=0\Rightarrow y=0,1$. Radius $2-y$, height $y-y^2$: $$V=2\pi\int_0^1(2-y)(y-y^2) dy=2\pi\int_0^1(2y-3y^2+y^3) dy=2\pi\Big(1-1+\frac14\Big)=\frac\pi2$$ **Answer:** $\color{red}{\boxed{\tfrac\pi2}}$

**12)** Using shells, rotate the region bounded by $y=e^x,\ x=0,\ x=2$ and the $x$-axis about the line $x=-2$.

> [!check]- Solution
> 
> Radius $x+2$, height $e^x$; by parts $\int(x+2)e^x dx=(x+1)e^x$: $$V=2\pi\Big[(x+1)e^x\Big]_0^2=2\pi(3e^2-1)$$ **Answer:** $\color{red}{\boxed{2\pi(3e^2-1)}}$

**13)** Using shells, rotate the region bounded by $y=x^3,\ y=1$ and the $y$-axis about the line $y=2$.

> [!check]- Solution
> 
> $x=y^{1/3}$, $0\le y\le1$. Radius $2-y$, height $y^{1/3}$: $$V=2\pi\int_0^1\big(2y^{1/3}-y^{4/3}\big)dy=2\pi\Big(\frac32-\frac37\Big)=\frac{15\pi}{7}$$ **Answer:** $\color{red}{\boxed{\tfrac{15\pi}7}}$

**14)** Revolve the region bounded by $y=x^2$ and $y=2-x^2$ about the line $x=1$.

> [!check]- Solution
> 
> They meet at $x=\pm1$. Radius $1-x$, height $2-2x^2$: $$V=2\pi\int_{-1}^1(1-x)(2-2x^2) dx=4\pi\int_{-1}^1(1-x-x^2+x^3) dx=4\pi\Big(2-\frac23\Big)=\frac{16\pi}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{16\pi}3}}$

**15)** Revolve the region bounded by $y=x^3,\ y=8,\ x=0$ about the $y$-axis.

> [!check]- Solution
> 
> $$V=2\pi\int_0^2x(8-x^3) dx=2\pi\Big(16-\frac{32}{5}\Big)=\frac{96\pi}{5}$$ **Answer:** $\color{red}{\boxed{\tfrac{96\pi}5}}$

**16)** Revolve the region bounded by $y=\sqrt{x-1},\ y=0,\ x=2$ about the $y$-axis.

> [!check]- Solution
> 
> $u=x-1$: $$V=2\pi\int_1^2x\sqrt{x-1} dx=2\pi\int_0^1(u+1)u^{1/2}du=2\pi\Big(\frac25+\frac23\Big)=\frac{32\pi}{15}$$ **Answer:** $\color{red}{\boxed{\tfrac{32\pi}{15}}}$

**17)** Revolve the region bounded by $y=\sqrt x,\ y=0,\ x=4$ about the $y$-axis.

> [!check]- Solution
> 
> $$V=2\pi\int_0^4x\cdot x^{1/2}dx=2\pi\cdot\frac25\cdot4^{5/2}=\frac{128\pi}{5}$$ **Answer:** $\color{red}{\boxed{\tfrac{128\pi}5}}$

**18)** Revolve the region bounded by $y=x^2+1,\ y=0,\ x=0,\ x=1$ about the $y$-axis.

> [!check]- Solution
> 
> $$V=2\pi\int_0^1x(x^2+1) dx=2\pi\Big(\frac14+\frac12\Big)=\frac{3\pi}{2}$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac{3\pi}2}}$

**19)** Revolve the region bounded by $y=x^{3/2},\ y=8,\ x=0$ about the $y$-axis.

> [!check]- Solution
> 
> $x^{3/2}=8\Rightarrow x=4$: $$V=2\pi\int_0^4x\big(8-x^{3/2}\big)dx=2\pi\Big[4x^2-\frac27x^{7/2}\Big]_0^4=2\pi\Big(64-\frac{256}{7}\Big)=\frac{384\pi}{7}$$ **Answer:** $\color{red}{\boxed{\tfrac{384}7\pi}}$

**20)** Revolve the first-quadrant region bounded by $y=3x-x^2,\ y=0$ about the line $x=4$.

> [!check]- Solution
> 
> $$V=2\pi\int_0^3(4-x)(3x-x^2) dx=2\pi\int_0^3(12x-7x^2+x^3) dx=2\pi\Big(54-63+\frac{81}{4}\Big)=\frac{45\pi}{2}$$ **Answer:** $\color{red}{\boxed{\tfrac{45\pi}2}}$

**21)** The region enclosed by $y^2-4y=-x$ and $x=0$ is revolved about the $x$-axis. Set up the volume integral (shell method).

> [!check]- Solution
> 
> $x=4y-y^2\ge0$ for $0\le y\le4$. Horizontal shells about the $x$-axis: radius $y$, height $4y-y^2$. **Answer:** $\color{red}{\boxed{2\pi\int_0^4y(4y-y^2) dy}}$

**22)** Using shells, set up the integral for the volume when the region bounded by $x=4-(y+1)^2,\ x=0$ is revolved about the line $y=2$.

> [!check]- Solution
> 
> $4-(y+1)^2=0\Rightarrow y=-3,1$. Radius $2-y$; height $4-(y+1)^2=(1-y)(3+y)$. **Answer:** $\color{red}{\boxed{2\pi\int_{-3}^1(1-y)(2-y)(3+y) dy}}$

## 7.4 Arc Length and Surfaces of Revolution (24 problems)

**1)** Find the arc length of $y=\frac23(x^2+1)^{3/2}$ on $[0,1]$.

> [!check]- Solution
> 
> $y'=2x\sqrt{x^2+1}$, so $1+y'^2=1+4x^4+4x^2=(2x^2+1)^2$: $$L=\int_0^1(2x^2+1) dx=\frac23+1=\frac53$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac53}}$

**2)** Find the arc length of $y=\frac{x^7}{14}+\frac{1}{10x^5}$ on $[1,2]$.

> [!check]- Solution
> 
> $y'=\frac{x^6}{2}-\frac{1}{2x^6}$, so $1+y'^2=\Big(\frac{x^6}{2}+\frac1{2x^6}\Big)^2$: $$L=\int_1^2\Big(\frac{x^6}{2}+\frac{x^{-6}}{2}\Big)dx=\Big[\frac{x^7}{14}-\frac{1}{10x^5}\Big]_1^2=\Big(\frac{128}{14}-\frac1{320}\Big)-\Big(\frac1{14}-\frac1{10}\Big)=\frac{20537}{2240}$$ **Answer:** $\color{red}{\boxed{\tfrac{20537}{2240}\approx9.168}}$

**3)** Find the arc length of $x=\frac13\sqrt y (y-3)$, $1\le y\le4$.

> [!check]- Solution
> 
> $x=\frac13\big(y^{3/2}-3y^{1/2}\big)$, $\ \frac{dx}{dy}=\frac12\big(y^{1/2}-y^{-1/2}\big)$, so $1+\big(\frac{dx}{dy}\big)^2=\frac14\big(y^{1/2}+y^{-1/2}\big)^2$: $$L=\frac12\int_1^4\big(y^{1/2}+y^{-1/2}\big)dy=\frac12\Big[\frac23y^{3/2}+2y^{1/2}\Big]_1^4=\frac12\Big(\frac{28}{3}-\frac83\Big)=\frac{10}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{10}3}}$

**4)** Find the arc length from $(0,3)$ clockwise to $(2,\sqrt5)$ along the circle $x^2+y^2=9$.

> [!check]- Solution
> 
> $y=\sqrt{9-x^2}$, $1+y'^2=\frac{9}{9-x^2}$: $$L=\int_0^2\frac{3}{\sqrt{9-x^2}}dx=3\arcsin\frac23\approx2.189$$ (Check: radius $\times$ angle $=3\cdot\arcsin\frac23$.) **Answer:** $\color{red}{\boxed{3\arcsin\tfrac23\approx2.189}}$

**5)** Find the area of the surface generated by revolving $y=\frac{x^3}{6}+\frac1{2x}$, $1\le x\le2$, about the $x$-axis.

> [!check]- Solution
> 
> $\sqrt{1+y'^2}=\frac{x^2}{2}+\frac{1}{2x^2}$: $$S=2\pi\int_1^2\Big(\frac{x^3}{6}+\frac1{2x}\Big)\Big(\frac{x^2}{2}+\frac1{2x^2}\Big)dx=2\pi\int_1^2\Big(\frac{x^5}{12}+\frac x3+\frac{1}{4x^3}\Big)dx=2\pi\cdot\frac{47}{32}=\frac{47\pi}{16}$$ **Answer:** $\color{red}{\boxed{\tfrac{47\pi}{16}}}$

**6)** Find the area of the surface generated by revolving $y=9-x^2$, $0\le x\le3$, about the $y$-axis.

> [!check]- Solution
> 
> $$S=2\pi\int_0^3x\sqrt{1+4x^2} dx=2\pi\cdot\frac1{12}\Big[(1+4x^2)^{3/2}\Big]_0^3=\frac\pi6\big(37\sqrt{37}-1\big)$$ **Answer:** $\color{red}{\boxed{\tfrac\pi6\big(37\sqrt{37}-1\big)\approx117.3}}$

**7)** A cone is generated by revolving the region bounded by $y=\frac{3x}4,\ y=3,\ x=0$ about the $y$-axis. Find its lateral surface area.

> [!check]- Solution
> 
> The slant edge is $y=\frac34x$, $0\le x\le4$, with $\sqrt{1+y'^2}=\frac54$: $$S=2\pi\int_0^4x\cdot\frac54 dx=2\pi\cdot\frac54\cdot8=20\pi$$ (Check: $\pi rL=\pi(4)(5)$.) **Answer:** $\color{red}{\boxed{20\pi}}$

**8)** Find the area of the sphere segment formed by revolving $y=\sqrt{r^2-x^2}$, $0\le x\le a$ ($a<r$), about the $y$-axis.

> [!check]- Solution
> 
> $\sqrt{1+y'^2}=\frac{r}{\sqrt{r^2-x^2}}$: $$S=2\pi\int_0^a\frac{rx}{\sqrt{r^2-x^2}}dx=2\pi r\Big[-\sqrt{r^2-x^2}\Big]_0^a=2\pi r\Big(r-\sqrt{r^2-a^2}\Big)$$
> 
> **Answer:** $\color{red}{\boxed{2\pi r\big(r-\sqrt{r^2-a^2}\big)}}$

**9)** $R$ is bounded by $y=\frac1x$, the $x$-axis, $x=1$ and $x=b\ (b>1)$; $D$ is $R$ revolved about the $x$-axis. (a) Find $V$. (b) Write the integral for the surface area $S$. (c) Show $V$ has a finite limit as $b\to\infty$. (d) Show $S\to\infty$.

> [!check]- Solution
> 
> (a) $V=\pi\int_1^b\frac{dx}{x^2}=\pi\Big(1-\frac1b\Big)$ (b) $S=2\pi\int_1^b\frac1x\sqrt{1+\frac1{x^4}} dx$ (c) $V\to\pi$ (d) $\sqrt{1+x^{-4}}>1$, so $S>2\pi\int_1^b\frac{dx}{x}=2\pi\ln b\to\infty$ (Gabriel's horn). **Answer:** $\color{red}{\boxed{V=\pi\big(1-\tfrac1b\big)\to\pi,\quad S\to\infty}}$

**10)** Let $C$ be $f(x)=\cosh x$, $0\le x\le t$. Show that the arc length of $C$ equals the area between $C$ and the $x$-axis, and name another curve with this property on $[0,t]$.

> [!check]- Solution
> 
> $\sqrt{1+\sinh^2x}=\cosh x$, so $L=\int_0^t\cosh x dx=\sinh t$, and Area $=\int_0^t\cosh x dx=\sinh t$ — equal. Another: $y=1$ ($L=t$ and Area $=t$). **Answer:** $\color{red}{\boxed{L=A=\sinh t;\ \text{e.g. }y=1}}$

**11)** The arc length of $y=x^2-\frac18\ln x$ on $[1,3]$ is

> [!check]- Solution
> 
> $y'=2x-\frac1{8x}$; $1+y'^2=4x^2+\frac12+\frac1{64x^2}=\Big(2x+\frac{1}{8x}\Big)^2$: $$L=\int_1^3\Big(2x+\frac1{8x}\Big)dx=\Big[x^2+\frac18\ln x\Big]_1^3=8+\frac18\ln3$$ **Answer:** $\color{red}{\boxed{8+\tfrac18\ln3}}$

**12)** The arc length of $y=\ln\big(\sqrt[3]{\sec3x}\big)$ on $\big[0,\frac\pi9\big]$ is

> [!check]- Solution
> 
> $y=\frac13\ln\sec3x\Rightarrow y'=\tan3x$, $\sqrt{1+\tan^23x}=\sec3x$: $$L=\int_0^{\pi/9}\sec3x dx=\frac13\Big[\ln|\sec3x+\tan3x|\Big]_0^{\pi/9}=\frac13\ln(2+\sqrt3)$$ **Answer:** $\color{red}{\boxed{\tfrac13\ln(2+\sqrt3)}}$

**13)** The surface area generated by revolving $y=x^3$, $0\le x\le1$, about the $x$-axis is

> [!check]- Solution
> 
> $$S=2\pi\int_0^1x^3\sqrt{1+9x^4} dx\overset{u=1+9x^4}{=}\frac{2\pi}{36}\int_1^{10}\sqrt u du=\frac\pi{18}\cdot\frac23\big(10\sqrt{10}-1\big)=\frac{\pi}{27}\big(10\sqrt{10}-1\big)$$ **Answer:** $\color{red}{\boxed{\tfrac\pi{27}(10\sqrt{10}-1)}}$

**14)** The surface area generated by revolving $y=\sqrt{1+4x}$, $0\le x\le1$, about the $x$-axis is

> [!check]- Solution
> 
> $y'=\frac{2}{\sqrt{1+4x}}$, so $y\sqrt{1+y'^2}=\sqrt{1+4x}\cdot\frac{\sqrt{4x+5}}{\sqrt{1+4x}}=\sqrt{4x+5}$: $$S=2\pi\int_0^1\sqrt{4x+5} dx=\frac{2\pi}{4}\cdot\frac23\Big[(4x+5)^{3/2}\Big]_0^1=\frac\pi3\big(27-5\sqrt5\big)$$ **Answer:** $\color{red}{\boxed{\tfrac\pi3(27-5\sqrt5)}}$

**15)** The surface area generated by revolving $y=2\sqrt{5-x}$, $1\le x\le5$, about the $x$-axis is

> [!check]- Solution
> 
> $y'=-\frac{1}{\sqrt{5-x}}$, so $y\sqrt{1+y'^2}=2\sqrt{5-x}\cdot\frac{\sqrt{6-x}}{\sqrt{5-x}}=2\sqrt{6-x}$: $$S=4\pi\int_1^5\sqrt{6-x} dx=4\pi\cdot\frac23\Big[-(6-x)^{3/2}\Big]_1^5=\frac{8\pi}{3}\big(5\sqrt5-1\big)$$ **Answer:** $\color{red}{\boxed{\tfrac{8\pi}3(5\sqrt5-1)}}$

**16)** The surface area generated by revolving $y=\frac1{12}x^3+\frac1x$, $1\le x\le2$, about the **$y$-axis** is

> [!check]- Solution
> 
> $y'=\frac{x^2}4-\frac1{x^2}$, $\sqrt{1+y'^2}=\frac{x^2}{4}+\frac1{x^2}$. About the $y$-axis the radius is $x$: $$S=2\pi\int_1^2x\Big(\frac{x^2}4+\frac1{x^2}\Big)dx=2\pi\Big[\frac{x^4}{16}+\ln x\Big]_1^2=2\pi\Big(\frac{15}{16}+\ln2\Big)$$ **Answer:** $\color{red}{\boxed{2\pi\big(\tfrac{15}{16}+\ln2\big)}}$

**17)** The arc length of $x=\frac13(y^2+2)^{3/2}$, $0\le y\le2$, is

> [!check]- Solution
> 
> $\frac{dx}{dy}=y\sqrt{y^2+2}$, $1+\big(\frac{dx}{dy}\big)^2=y^4+2y^2+1=(y^2+1)^2$: $$L=\int_0^2(y^2+1) dy=\frac83+2=\frac{14}{3}$$ **Answer:** $\color{red}{\boxed{\tfrac{14}3}}$

**18)** The arc length of $f(x)=\frac{x^4}8+\frac1{4x^2}$ on $[1,2]$ is

> [!check]- Solution
> 
> $f'=\frac{x^3}2-\frac1{2x^3}$, $\sqrt{1+f'^2}=\frac{x^3}2+\frac1{2x^3}$: $$L=\Big[\frac{x^4}{8}-\frac1{4x^2}\Big]_1^2=\Big(2-\frac1{16}\Big)-\Big(\frac18-\frac14\Big)=\frac{33}{16}$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac{33}{16}}}$

**19)** The arc length of $f(x)=\ln(\sin x)$ on $\big[\frac\pi4,\frac{3\pi}4\big]$ is

> [!check]- Solution
> 
> $f'=\cot x$, $\sqrt{1+\cot^2x}=\csc x$: $$L=\int_{\pi/4}^{3\pi/4}\csc x dx=\Big[\ln|\csc x-\cot x|\Big]_{\pi/4}^{3\pi/4}=\ln(\sqrt2+1)-\ln(\sqrt2-1)$$ **Answer:** $\color{red}{\boxed{\ln\tfrac{\sqrt2+1}{\sqrt2-1}}}$

**20)** The arc length of $f(x)=\ln\Big(\dfrac{e^x+1}{e^x-1}\Big)$ on $[\ln6,\ln8]$ is

> [!check]- Solution
> 
> $f'=\frac{e^x}{e^x+1}-\frac{e^x}{e^x-1}=\frac{-2e^x}{e^{2x}-1}$, so $1+f'^2=\Big(\frac{e^{2x}+1}{e^{2x}-1}\Big)^2=\coth^2x$: $$L=\int_{\ln6}^{\ln8}\coth x dx=\ln\frac{\sinh(\ln8)}{\sinh(\ln6)}=\ln\frac{63/16}{35/12}=\ln\frac{27}{20}$$ **Answer:** $\color{red}{\boxed{\ln\tfrac{27}{20}}}$

**21)** The area of the surface generated by revolving $y=2\sqrt x$ on $[4,9]$ about the $x$-axis is

> [!check]- Solution
> 
> $y'=\frac1{\sqrt x}$, $y\sqrt{1+y'^2}=2\sqrt x\cdot\frac{\sqrt{x+1}}{\sqrt x}=2\sqrt{x+1}$: $$S=4\pi\int_4^9\sqrt{x+1} dx=\frac{8\pi}{3}\Big[(x+1)^{3/2}\Big]_4^9=\frac{8\pi}{3}\big(10\sqrt{10}-5\sqrt5\big)$$ **Answer:** $\color{red}{\boxed{\tfrac{8\pi}3(10\sqrt{10}-5\sqrt5)}}$

**22)** The area of the surface generated by revolving $y=1-\frac{x^2}4$ on $[0,2]$ about the $y$-axis is

> [!check]- Solution
> 
> $y'=-\frac x2$: $$S=2\pi\int_0^2x\sqrt{1+\frac{x^2}{4}} dx\overset{u=1+x^2/4}{=}4\pi\int_1^2\sqrt u du=\frac{8\pi}{3}\big(2\sqrt2-1\big)$$ **Answer:** $\color{red}{\boxed{\tfrac{8\pi}3(2\sqrt2-1)}}$

**23)** The area of the surface generated by revolving $y=\sqrt{9-x^2}$ on $[-2,2]$ about the $x$-axis is

> [!check]- Solution
> 
> $y\sqrt{1+y'^2}=\sqrt{9-x^2}\cdot\frac{3}{\sqrt{9-x^2}}=3$: $$S=2\pi\int_{-2}^23 dx=24\pi$$
> 
> **Answer:** $\color{red}{\boxed{24\pi}}$

**24)** The area of the surface generated by revolving $y=\sqrt{25-x^2}$, $0\le x\le4$, about the $y$-axis is

> [!check]- Solution
> 
> Radius $x$, $\sqrt{1+y'^2}=\frac{5}{\sqrt{25-x^2}}$: $$S=2\pi\int_0^4\frac{5x}{\sqrt{25-x^2}}dx=10\pi\Big[-\sqrt{25-x^2}\Big]_0^4=10\pi(5-3)=20\pi$$ **Answer:** $\color{red}{\boxed{20\pi}}$