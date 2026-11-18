# MATH 102 · Chapter 8 — Integration Techniques and Improper Integrals

## 8.1 Basic Integration Rules (22 problems)

**1)** Select the basic formula for $\displaystyle\int\frac{2}{(2t-1)^2+4} dt$ and identify $u$ and $a$ (then integrate).

> [!check]- Solution
> 
> Arctangent rule $\int\frac{du}{u^2+a^2}=\frac1a\arctan\frac ua+C$ with $u=2t-1$ ($du=2 dt$) and $a=2$: $$\int\frac{du}{u^2+4}=\frac12\arctan\frac{2t-1}{2}+C$$ **Answer:** $\color{red}{\boxed{u=2t-1,\ a=2;\ \tfrac12\arctan\tfrac{2t-1}{2}+C}}$

**2)** $\displaystyle\int\frac{x+1}{\sqrt{3x^2+6x}} dx$

> [!check]- Solution
> 
> $u=3x^2+6x,\ du=6(x+1) dx$: $\ \frac16\int u^{-1/2}du=\frac13u^{1/2}+C$. **Answer:** $\color{red}{\boxed{\tfrac13\sqrt{3x^2+6x}+C}}$

**3)** $\displaystyle\int\frac{2}{e^{-x}+1} dx$

> [!check]- Solution
> 
> Multiply top and bottom by $e^x$: $\int\frac{2e^x}{1+e^x}dx=2\ln(1+e^x)+C$.
> 
> **Answer:** $\color{red}{\boxed{2\ln(1+e^x)+C}}$

**4)** $\displaystyle\int\frac{1}{x^2-4x+9} dx$

> [!check]- Solution
> 
> $x^2-4x+9=(x-2)^2+5$: $$\int\frac{dx}{(x-2)^2+(\sqrt5)^2}=\frac{1}{\sqrt5}\arctan\frac{x-2}{\sqrt5}+C$$ **Answer:** $\color{red}{\boxed{\tfrac{1}{\sqrt5}\arctan\tfrac{x-2}{\sqrt5}+C}}$

**5)** $\displaystyle\int_2^3\frac{\ln(x+1)^3}{x+1} dx$ (read $\ln(x+1)^3=3\ln(x+1)$)

> [!check]- Solution
> 
> $u=\ln(x+1),\ du=\frac{dx}{x+1}$: $$\int_{\ln3}^{\ln4}3u du=\frac32\Big[(\ln4)^2-(\ln3)^2\Big]\approx1.072$$ (If it meant $[\ln(x+1)]^3$, the result would be $\frac14\big[(\ln4)^4-(\ln3)^4\big]\approx0.559$.) **Answer:** $\color{red}{\boxed{\tfrac32\big[(\ln4)^2-(\ln3)^2\big]\approx1.072}}$

**6)** $\displaystyle\int_0^1 7^{x^2+2x}(x+1) dx$

> [!check]- Solution
> 
> $u=x^2+2x,\ du=2(x+1) dx$; $x=0\to0,\ x=1\to3$: $$\frac12\int_0^37^u du=\frac12\cdot\frac{7^3-1}{\ln7}=\frac{171}{\ln7}\approx87.88$$ **Answer:** $\color{red}{\boxed{\tfrac{171}{\ln7}\approx87.88}}$

**7)** Find the area under $y=\frac{3x+2}{x^2+9}$ from $x=0$ to $x=5$ (the shaded region).

> [!check]- Solution
> 
> $$\int_0^5\Big(\frac{3x}{x^2+9}+\frac{2}{x^2+9}\Big)dx=\Big[\frac32\ln(x^2+9)+\frac23\arctan\frac x3\Big]_0^5=\frac32\ln\frac{34}{9}+\frac23\arctan\frac53\approx2.681$$ **Answer:** $\color{red}{\boxed{\tfrac32\ln\tfrac{34}{9}+\tfrac23\arctan\tfrac53\approx2.681}}$

**8)** $f(x)=x$ and $g(x)=ax^2$ meet at $(0,0)$ and $\big(\frac1a,\frac1a\big)$. Find $a>0$ such that the area between them is $\frac23$.

> [!check]- Solution
> 
> $$\int_0^{1/a}(x-ax^2) dx=\frac{1}{2a^2}-\frac{1}{3a^2}=\frac{1}{6a^2}=\frac23\Rightarrow a^2=\frac14$$ **Answer:** $\color{red}{\boxed{a=\tfrac12}}$

**9)** The region bounded by $y=e^{-x^2},\ y=0,\ x=0,\ x=b\ (b>0)$ is revolved about the $y$-axis. (a) Find the volume when $b=1$. (b) Find $b$ so that the volume is $\frac43$.

> [!check]- Solution
> 
> Shells: $V(b)=2\pi\int_0^bxe^{-x^2}dx=\pi\big(1-e^{-b^2}\big)$. (a) $\pi(1-e^{-1})\approx1.986$ (b) $1-e^{-b^2}=\frac{4}{3\pi}\Rightarrow b=\sqrt{\ln\frac{3\pi}{3\pi-4}}\approx0.743$ **Answer:** $\color{red}{\boxed{\text{(a) }\pi\big(1-\tfrac1e\big)\quad\text{(b) }b=\sqrt{\ln\tfrac{3\pi}{3\pi-4}}\approx0.743}}$

**10)** Find the arc length of $y=\ln(\cos x)$ from $x=0$ to $x=\frac\pi3$.

> [!check]- Solution
> 
> $y'=-\tan x$, $\sqrt{1+\tan^2x}=\sec x$: $$L=\int_0^{\pi/3}\sec x dx=\Big[\ln|\sec x+\tan x|\Big]_0^{\pi/3}=\ln(2+\sqrt3)\approx1.317$$ **Answer:** $\color{red}{\boxed{\ln(2+\sqrt3)}}$

**11)** Find the area of the surface formed by revolving $y=2\sqrt x$ on $[0,9]$ about the $x$-axis.

> [!check]- Solution
> 
> $y\sqrt{1+y'^2}=2\sqrt x\sqrt{1+\frac1x}=2\sqrt{x+1}$: $$S=4\pi\int_0^9\sqrt{x+1} dx=\frac{8\pi}{3}\big(10\sqrt{10}-1\big)\approx256.5$$ **Answer:** $\color{red}{\boxed{\tfrac{8\pi}3(10\sqrt{10}-1)}}$

**12)** Find the average value of $f(x)=\sin nx$ on $0\le x\le\frac\pi n$ ($n$ a positive integer).

> [!check]- Solution
> 
> $$\frac{1}{\pi/n}\int_0^{\pi/n}\sin nx dx=\frac n\pi\Big[-\frac{\cos nx}{n}\Big]_0^{\pi/n}=\frac n\pi\cdot\frac2n=\frac2\pi$$ **Answer:** $\color{red}{\boxed{\tfrac2\pi}}$ (independent of $n$)

**13)** $\displaystyle\int_{\pi/4}^{\pi/2}\frac{1+\sin^2x}{\sin^4x+\sin^2x\cos^2x} dx=$

> [!check]- Solution
> 
> Denominator $=\sin^2x(\sin^2x+\cos^2x)=\sin^2x$, so the integrand is $\csc^2x+1$: $$\Big[-\cot x+x\Big]_{\pi/4}^{\pi/2}=\frac\pi2-\Big(-1+\frac\pi4\Big)=1+\frac\pi4$$ **Answer:** $\color{red}{\boxed{\tfrac\pi4+1}}$

**14)** $\displaystyle\int_{2\pi/3}^{3\pi/4}\sqrt{\sec^2x (\sin^2x+\cos^2x+\tan^2x)} dx=$

> [!check]- Solution
> 
> $\sin^2+\cos^2+\tan^2=\sec^2x$, so $\sqrt{\sec^4x}=\sec^2x$: $$\Big[\tan x\Big]_{2\pi/3}^{3\pi/4}=-1-(-\sqrt3)=\sqrt3-1$$ **Answer:** $\color{red}{\boxed{\sqrt3-1}}$

**15)** $\displaystyle\int_0^{\pi/2}\sqrt{\sin^2x-8\sin x+16} dx=$

> [!check]- Solution
> 
> $\sqrt{(\sin x-4)^2}=|\sin x-4|=4-\sin x$: $$\Big[4x+\cos x\Big]_0^{\pi/2}=2\pi-1$$ **Answer:** $\color{red}{\boxed{2\pi-1}}$

**16)** $\displaystyle\int\frac{4-2t}{3t^2-12t-1} dt=$

> [!check]- Solution
> 
> $u=3t^2-12t-1,\ du=(6t-12) dt=-3(4-2t) dt$: $$-\frac13\int\frac{du}{u}=-\frac13\ln|u|+C=-\ln\big|\sqrt[3]{u}\big|+C$$ **Answer:** $\color{red}{\boxed{-\ln\big|\sqrt[3]{3t^2-12t-1}\big|+C}}$

**17)** $\displaystyle\int(\tan x)[\ln(\cos x)] dx=$

> [!check]- Solution
> 
> $u=\ln(\cos x),\ du=-\tan x dx$: $\ -\int u du=-\frac{u^2}{2}+C$. **Answer:** $\color{red}{\boxed{-\tfrac12[\ln(\cos x)]^2+C}}$

**18)** $\displaystyle\int(\cot x)\ln(\sin x) dx=$

> [!check]- Solution
> 
> $u=\ln(\sin x),\ du=\cot x dx$: $\ \int u du=\frac{u^2}{2}+C$. **Answer:** $\color{red}{\boxed{\tfrac12[\ln(\sin x)]^2+C}}$

**19)** $\displaystyle\int\frac{\tan(2/t)}{t^2} dt=$

> [!check]- Solution
> 
> $u=\frac2t,\ du=-\frac{2}{t^2}dt$: $\ -\frac12\int\tan u du=-\frac12\big(-\ln|\cos u|\big)+C=\frac12\ln\big|\cos\frac2t\big|+C$. **Answer:** $\color{red}{\boxed{\tfrac12\ln\big|\cos\tfrac2t\big|+C}}$

**20)** $\displaystyle\int_0^1\frac{x^2-x}{x^2+x+1} dx=$

> [!check]- Solution
> 
> $\frac{x^2-x}{x^2+x+1}=1-\frac{2x+1}{x^2+x+1}$: $$\Big[x-\ln(x^2+x+1)\Big]_0^1=1-\ln3$$ **Answer:** $\color{red}{\boxed{1-\ln3}}$

**21)** $\displaystyle\int\frac{d\theta}{\cos\theta-1}=$

> [!check]- Solution
> 
> Multiply by $\frac{\cos\theta+1}{\cos\theta+1}$: $\frac{\cos\theta+1}{\cos^2\theta-1}=-\frac{\cos\theta+1}{\sin^2\theta}=-\csc\theta\cot\theta-\csc^2\theta$. $$\int(-\csc\theta\cot\theta-\csc^2\theta) d\theta=\csc\theta+\cot\theta+C$$ **Answer:** $\color{red}{\boxed{\csc\theta+\cot\theta+C}}$

**22)** $\displaystyle\int\cot^2x dx=$

> [!check]- Solution
> 
> $\cot^2x=\csc^2x-1$: $\ \int(\csc^2x-1) dx=-\cot x-x+C$. **Answer:** $\color{red}{\boxed{-\cot x-x+C}}$

## 8.2 Integration by Parts (24 problems)

**1)** $\displaystyle\int\frac{5x}{e^{2x}} dx$

> [!check]- Solution
> 
> $u=5x,\ dv=e^{-2x}dx\Rightarrow v=-\frac12e^{-2x}$: $$-\frac52xe^{-2x}+\frac52\int e^{-2x}dx=-\frac52xe^{-2x}-\frac54e^{-2x}+C=-\frac54e^{-2x}(2x+1)+C$$
> 
> **Answer:** $\color{red}{\boxed{-\tfrac54e^{-2x}(2x+1)+C}}$

**2)** $\displaystyle\int\frac{\ln x}{x^3} dx$

> [!check]- Solution
> 
> $u=\ln x,\ dv=x^{-3}dx\Rightarrow v=-\frac1{2x^2}$: $$-\frac{\ln x}{2x^2}+\int\frac{1}{2x^3}dx=-\frac{\ln x}{2x^2}-\frac{1}{4x^2}+C$$
> 
> **Answer:** $\color{red}{\boxed{-\tfrac{\ln x}{2x^2}-\tfrac{1}{4x^2}+C}}$

**3)** $\displaystyle\int\frac{xe^{2x}}{(2x+1)^2} dx$

> [!check]- Solution
> 
> $u=xe^{2x}\Rightarrow du=e^{2x}(2x+1) dx$; $dv=(2x+1)^{-2}dx\Rightarrow v=-\frac{1}{2(2x+1)}$: $$-\frac{xe^{2x}}{2(2x+1)}+\int\frac{e^{2x}}{2}dx=-\frac{xe^{2x}}{2(2x+1)}+\frac{e^{2x}}{4}+C=\frac{e^{2x}}{4(2x+1)}+C$$
> 
> **Answer:** $\color{red}{\boxed{\dfrac{e^{2x}}{4(2x+1)}+C}}$

**4)** $\displaystyle\int t\csc t\cot t dt$

> [!check]- Solution
> 
> $u=t,\ dv=\csc t\cot t dt\Rightarrow v=-\csc t$: $$-t\csc t+\int\csc t dt=-t\csc t-\ln|\csc t+\cot t|+C$$
> 
> **Answer:** $\color{red}{\boxed{-t\csc t-\ln|\csc t+\cot t|+C}}$

**5)** $\displaystyle\int e^{-3x}\sin5x dx$

> [!check]- Solution
> 
> Two rounds of parts bring back the original integral $I$: $\ I=-\frac15e^{-3x}\cos5x-\frac{3}{25}e^{-3x}\sin5x-\frac{9}{25}I$, so $\frac{34}{25}I=-\frac{e^{-3x}}{25}(5\cos5x+3\sin5x)$. **Answer:** $\color{red}{\boxed{-\dfrac{e^{-3x}(3\sin5x+5\cos5x)}{34}+C}}$

**6)** $\displaystyle\int_0^1\ln(4+x^2) dx$

> [!check]- Solution
> 
> $u=\ln(4+x^2),\ dv=dx$: $\ x\ln(4+x^2)-\int\frac{2x^2}{4+x^2}dx=x\ln(4+x^2)-2x+4\arctan\frac x2$. $$\Big[x\ln(4+x^2)-2x+4\arctan\tfrac x2\Big]_0^1=\ln5-2+4\arctan\tfrac12\approx1.464$$ **Answer:** $\color{red}{\boxed{\ln5-2+4\arctan\tfrac12\approx1.464}}$

**7)** Use the tabular method: $\displaystyle\int(x+2)^2\sin x dx$

> [!check]- Solution
> 
> Differentiate $(x+2)^2\to2(x+2)\to2\to0$; integrate $\sin x\to-\cos x\to-\sin x\to\cos x$; signs $+,-,+$: **Answer:** $\color{red}{\boxed{-(x+2)^2\cos x+2(x+2)\sin x+2\cos x+C}}$

**8)** $\displaystyle\int\sin\sqrt x dx$ (substitution, then parts)

> [!check]- Solution
> 
> $w=\sqrt x,\ x=w^2,\ dx=2w dw$: $\ \int2w\sin w dw=-2w\cos w+2\sin w+C$.
> 
> **Answer:** $\color{red}{\boxed{-2\sqrt x\cos\sqrt x+2\sin\sqrt x+C}}$

**9)** Prove $\displaystyle\int x^n\cos x dx=x^n\sin x-n\int x^{n-1}\sin x dx$.

> [!check]- Solution
> 
> $u=x^n\Rightarrow du=nx^{n-1}dx$; $dv=\cos x dx\Rightarrow v=\sin x$. Then $\int u dv=uv-\int v du$ gives the formula directly. $\blacksquare$ **Answer:** $\color{red}{\boxed{u=x^n,\ dv=\cos x dx}}$ (proved)

**10)** Find the area of the region bounded by $y=x^3\ln x,\ y=0,\ x=1,\ x=3$.

> [!check]- Solution
> 
> $u=\ln x,\ dv=x^3dx$: $\int x^3\ln x dx=\frac{x^4}{4}\ln x-\frac{x^4}{16}$. $$\Big[\frac{x^4}{4}\ln x-\frac{x^4}{16}\Big]_1^3=\frac{81}{4}\ln3-\frac{81}{16}+\frac{1}{16}=\frac{81}{4}\ln3-5\approx17.25$$ **Answer:** $\color{red}{\boxed{\tfrac{81}{4}\ln3-5\approx17.25}}$

**11)** Region bounded by $y=x\sin x,\ y=0,\ x=0,\ x=\pi$: find (a) the area, (b) the volume about the $x$-axis, (c) the volume about the $y$-axis.

> [!check]- Solution
> 
> (a) $\int_0^\pi x\sin x dx=\big[-x\cos x+\sin x\big]_0^\pi=\pi$. (b) $\pi\int_0^\pi x^2\sin^2x dx=\frac\pi2\int_0^\pi x^2(1-\cos2x) dx=\frac\pi2\Big(\frac{\pi^3}{3}-\frac\pi2\Big)=\frac{\pi^4}{6}-\frac{\pi^2}{4}$ (tabular gives $\int_0^\pi x^2\cos2x dx=\frac\pi2$). (c) Shells: $2\pi\int_0^\pi x^2\sin x dx=2\pi\big[-x^2\cos x+2x\sin x+2\cos x\big]_0^\pi=2\pi(\pi^2-4)$. **Answer:** $\color{red}{\boxed{\pi,\quad\tfrac{\pi^4}{6}-\tfrac{\pi^2}{4},\quad2\pi(\pi^2-4)}}$

**12)** Find the fallacy: with $dv=dx\ (v=x)$ and $u=\frac1x\ (du=-\frac1{x^2}dx)$, $\displaystyle\int\frac{dx}{x}=\Big(\frac1x\Big)(x)-\int\Big(-\frac1{x^2}\Big)(x) dx=1+\int\frac{dx}{x}$, "so $0=1$".

> [!check]- Solution
> 
> An indefinite integral is a family of antiderivatives. $\int\frac{dx}x=1+\int\frac{dx}x$ only says the two families differ by a constant ($\ln|x|+C_1=1+\ln|x|+C_2$), which is true. You can't cancel $\int\frac{dx}{x}$ as if it were a single number. (With limits, $\big[\frac1x\cdot x\big]_a^b=0$ and no contradiction appears.) **Answer:** $\color{red}{\boxed{\text{the constant of integration was ignored}}}$

**13)** $\displaystyle\int_0^1x^{11}e^{-x^3} dx=$

> [!check]- Solution
> 
> $u=x^3,\ du=3x^2dx$: $\ \frac13\int_0^1u^3e^{-u}du$. Tabular: $\int u^3e^{-u}du=-e^{-u}(u^3+3u^2+6u+6)$. $$\frac13\Big[-e^{-u}(u^3+3u^2+6u+6)\Big]_0^1=\frac13\Big(-\frac{16}{e}+6\Big)=2-\frac{16}{3e}$$ **Answer:** $\color{red}{\boxed{2-\tfrac{16}{3e}}}$

**14)** $\displaystyle\int_{\pi/12}^{\pi/6}x\csc^2(3x) dx=$

> [!check]- Solution
> 
> $w=3x$: $\frac19\int_{\pi/4}^{\pi/2}w\csc^2w dw$; parts with $u=w,\ dv=\csc^2w dw$: $\int w\csc^2w dw=-w\cot w+\ln|\sin w|$. $$\frac19\Big[(0+0)-\Big(-\frac\pi4+\ln\frac{1}{\sqrt2}\Big)\Big]=\frac19\Big(\frac\pi4+\frac12\ln2\Big)=\frac\pi{36}+\frac1{18}\ln2$$ **Answer:** $\color{red}{\boxed{\tfrac\pi{36}+\tfrac1{18}\ln2}}$

**15)** $\displaystyle\int_0^1e^{\sqrt[4]{16x}} dx=$

> [!check]- Solution
> 
> $w=\sqrt[4]{16x}\Rightarrow w^4=16x,\ dx=\frac{w^3}{4}dw$; $x=0\to0,\ x=1\to2$: $$\frac14\int_0^2w^3e^w dw=\frac14\Big[e^w(w^3-3w^2+6w-6)\Big]_0^2=\frac14\big(2e^2+6\big)=\frac{e^2}{2}+\frac32$$ **Answer:** $\color{red}{\boxed{\tfrac32+\tfrac{e^2}2}}$

**16)** $\displaystyle\int_0^12e^{\arcsin x} dx=$

> [!check]- Solution
> 
> $w=\arcsin x,\ x=\sin w,\ dx=\cos w dw$; $0\to0,\ 1\to\frac\pi2$: $\ I=\int_0^{\pi/2}2e^w\cos w dw$. Parts twice (cycling): $\int2e^w\cos w dw=e^w(\cos w+\sin w)$. $$I=\Big[e^w(\cos w+\sin w)\Big]_0^{\pi/2}=e^{\pi/2}-1$$
> 
> **Answer:** $\color{red}{\boxed{e^{\pi/2}-1}}$

**17)** $\displaystyle\int\cosh(\sqrt x) dx=$

> [!check]- Solution
> 
> $u=\sqrt x,\ dx=2u du$: $\int2u\cosh u du=2u\sinh u-2\cosh u+C$. **Answer:** $\color{red}{\boxed{2\sqrt x\sinh\sqrt x-2\cosh\sqrt x+C}}$

**18)** $\displaystyle\int x\arctan\Big(\frac1x\Big)dx=$

> [!check]- Solution
> 
> $u=\arctan\frac1x\Rightarrow du=\frac{-1/x^2}{1+1/x^2}dx=-\frac{dx}{1+x^2}$; $dv=x dx\Rightarrow v=\frac{x^2}{2}$: $$\frac{x^2}{2}\arctan\frac1x+\frac12\int\frac{x^2}{1+x^2}dx=\frac{x^2}{2}\arctan\frac1x+\frac12\int\Big(1-\frac1{1+x^2}\Big)dx=\frac{x^2}{2}\arctan\frac1x+\frac x2-\frac12\arctan x+C$$ **Answer:** $\color{red}{\boxed{\tfrac12x^2\arctan\tfrac1x+\tfrac12x-\tfrac12\arctan x+C}}$

**19)** $\displaystyle\int_0^\pi x\sin(2x) dx=$

> [!check]- Solution
> 
> $$\Big[-\frac{x\cos2x}{2}+\frac{\sin2x}{4}\Big]_0^\pi=-\frac{\pi}{2}$$ **Answer:** $\color{red}{\boxed{-\tfrac\pi2}}$

**20)** $\displaystyle\int_0^{\pi/3}x\sec^2x dx=$

> [!check]- Solution
> 
> $u=x,\ dv=\sec^2x dx$: $\int x\sec^2x dx=x\tan x+\ln|\cos x|$. $$\frac\pi3\sqrt3+\ln\frac12=\frac{\sqrt3}{3}\pi-\ln2$$ **Answer:** $\color{red}{\boxed{\tfrac{\sqrt3}3\pi-\ln2}}$

**21)** $\displaystyle\int_1^2\frac{(\ln x)^2}{x^2} dx=$

> [!check]- Solution
> 
> $u=(\ln x)^2,\ dv=x^{-2}dx$: $\ -\frac{(\ln x)^2}{x}+2\int\frac{\ln x}{x^2}dx=-\frac{(\ln x)^2}{x}-\frac{2\ln x}{x}-\frac2x$. $$\Big(-\frac{(\ln2)^2}{2}-\ln2-1\Big)-(-2)=1-\ln2-\frac{(\ln2)^2}{2}$$ **Answer:** $\color{red}{\boxed{1-\ln2-\tfrac{(\ln2)^2}2}}$

**22)** $\displaystyle\int_2^4x\sec^{-1}x dx=$

> [!check]- Solution
> 
> $u=\sec^{-1}x\Rightarrow du=\frac{dx}{x\sqrt{x^2-1}}$, $v=\frac{x^2}2$: $$\frac{x^2}{2}\sec^{-1}x-\frac12\int\frac{x dx}{\sqrt{x^2-1}}=\frac{x^2}{2}\sec^{-1}x-\frac12\sqrt{x^2-1}$$ $$\Big[8\sec^{-1}4-\tfrac{\sqrt{15}}{2}\Big]-\Big[2\cdot\tfrac\pi3-\tfrac{\sqrt3}{2}\Big]=8\sec^{-1}4+\frac{3\sqrt3-3\sqrt{15}-4\pi}{6}$$ **Answer:** $\color{red}{\boxed{8\sec^{-1}4+\tfrac{3\sqrt3-3\sqrt{15}-4\pi}6}}$

**23)** $\displaystyle\int_0^1x\arcsin(x^2) dx=$

> [!check]- Solution
> 
> $u=x^2$: $\frac12\int_0^1\arcsin u du=\frac12\Big[u\arcsin u+\sqrt{1-u^2}\Big]_0^1=\frac12\Big(\frac\pi2-1\Big)$. **Answer:** $\color{red}{\boxed{\tfrac14(\pi-2)}}$

**24)** If $f(a)=f(b)=0$ and $f''$ exists on $[a,b]$, then $\displaystyle\int_a^b(x-a)(x-b)f''(x) dx=$

> [!check]- Solution
> 
> Parts with $u=(x-a)(x-b)$: the boundary term vanishes, leaving $-\int_a^b(2x-a-b)f'(x) dx$. Parts again: $-\Big\lbrace \big[(2x-a-b)f(x)\big]_a^b-2\int_a^bf\Big\rbrace =2\int_a^bf(x) dx$, since $f(a)=f(b)=0$. **Answer:** $\color{red}{\boxed{2\int_a^bf(x) dx}}$

## 8.3 Trigonometric Integrals (25 problems)

**1)** $\displaystyle\int\sin^33x dx$

> [!check]- Solution
> 
> $\sin^33x=(1-\cos^23x)\sin3x$; $u=\cos3x,\ du=-3\sin3x dx$: $$-\frac13\int(1-u^2) du=-\frac13\Big(u-\frac{u^3}{3}\Big)+C$$ **Answer:** $\color{red}{\boxed{-\tfrac13\cos3x+\tfrac19\cos^33x+C}}$

**2)** $\displaystyle\int\frac{\cos^5t}{\sqrt{\sin t}} dt$

> [!check]- Solution
> 
> $\cos^5t=(1-\sin^2t)^2\cos t$; $u=\sin t$: $$\int\frac{(1-u^2)^2}{u^{1/2}}du=\int\big(u^{-1/2}-2u^{3/2}+u^{7/2}\big)du=2u^{1/2}-\frac45u^{5/2}+\frac29u^{9/2}+C$$
> 
> **Answer:** $\color{red}{\boxed{2\sqrt{\sin t}-\tfrac45(\sin t)^{5/2}+\tfrac29(\sin t)^{9/2}+C}}$

**3)** $\displaystyle\int x^2\sin^2x dx$

> [!check]- Solution
> 
> $\int x^2\cdot\frac{1-\cos2x}{2}dx=\frac{x^3}{6}-\frac12\int x^2\cos2x dx$. Tabular: $\int x^2\cos2x dx=\frac{x^2}{2}\sin2x+\frac x2\cos2x-\frac14\sin2x$. **Answer:** $\color{red}{\boxed{\tfrac{x^3}6-\tfrac{x^2}4\sin2x-\tfrac x4\cos2x+\tfrac18\sin2x+C}}$

**4)** $\displaystyle\int\tan^5\frac x2 dx$

> [!check]- Solution
> 
> $u=\frac x2$: $2\int\tan^5u du$. Since $\tan^5=\tan^3(\sec^2-1)=\tan^3\sec^2-\tan\sec^2+\tan$: $$\int\tan^5u du=\frac{\tan^4u}{4}-\frac{\tan^2u}{2}-\ln|\cos u|$$ So the result is $\frac12\tan^4\frac x2-\tan^2\frac x2-2\ln\big|\cos\frac x2\big|+C$. **Answer:** $\color{red}{\boxed{\tfrac12\tan^4\tfrac x2-\tan^2\tfrac x2-2\ln\big|\cos\tfrac x2\big|+C}}$

**5)** $\displaystyle\int\sec^64x\tan4x dx$

> [!check]- Solution
> 
> $u=\sec4x,\ du=4\sec4x\tan4x dx$: $\ \frac14\int u^5du=\frac{u^6}{24}+C$. **Answer:** $\color{red}{\boxed{\tfrac{\sec^64x}{24}+C}}$

**6)** $\displaystyle\int\sin2t\cos9t dt$

> [!check]- Solution
> 
> $\sin2t\cos9t=\frac12\big[\sin(-7t)+\sin11t\big]=\frac12\big[\sin11t-\sin7t\big]$: **Answer:** $\color{red}{\boxed{\tfrac1{14}\cos7t-\tfrac1{22}\cos11t+C}}$

**7)** $\displaystyle\int\frac{\cot^2t}{\csc t} dt$

> [!check]- Solution
> 
> $\frac{\csc^2t-1}{\csc t}=\csc t-\sin t$: **Answer:** $\color{red}{\boxed{\ln|\csc t-\cot t|+\cos t+C}}$

**8)** $\displaystyle\int\frac{1-\sec t}{\cos t-1} dt$

> [!check]- Solution
> 
> $1-\sec t=\frac{\cos t-1}{\cos t}$, so the integrand is $\frac{1}{\cos t}=\sec t$. **Answer:** $\color{red}{\boxed{\ln|\sec t+\tan t|+C}}$

**9)** $\displaystyle\int_0^\pi\sin^5x dx$

> [!check]- Solution
> 
> $\sin^5x=(1-\cos^2x)^2\sin x$, $u=\cos x$ ($1\to-1$): $$\int_{-1}^{1}(1-u^2)^2du=2\Big(1-\frac23+\frac15\Big)=\frac{16}{15}$$ **Answer:** $\color{red}{\boxed{\tfrac{16}{15}}}$

**10)** Find the area under $y=\sin^2\pi x$ on $[0,1]$.

> [!check]- Solution
> 
> $$\int_0^1\frac{1-\cos2\pi x}{2}dx=\frac12-\Big[\frac{\sin2\pi x}{4\pi}\Big]_0^1=\frac12$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac12}}$

**11)** Revolve the region bounded by $y=\tan x,\ y=0,\ x=-\frac\pi4,\ x=\frac\pi4$ about the $x$-axis.

> [!check]- Solution
> 
> $$V=\pi\int_{-\pi/4}^{\pi/4}\tan^2x dx=2\pi\int_0^{\pi/4}(\sec^2x-1) dx=2\pi\Big(1-\frac\pi4\Big)=\pi\Big(2-\frac\pi2\Big)$$
> 
> **Answer:** $\color{red}{\boxed{\pi\big(2-\tfrac\pi2\big)}}$

**12)** $\displaystyle\int\cot^2(3x) dx=$

> [!check]- Solution
> 
> $u=3x$: $\frac13\int\cot^2u du=\frac13\int(\csc^2u-1) du=\frac13(-\cot u-u)+C$. **Answer:** $\color{red}{\boxed{-\tfrac13\cot3x-x+C}}$

**13)** $\displaystyle\int\frac{\tan^2\big(\frac{4}{x^2}\big)}{x^3} dx=$

> [!check]- Solution
> 
> $u=\frac4{x^2}=4x^{-2},\ du=-\frac8{x^3}dx$: $$-\frac18\int\tan^2u du=-\frac18\int(\sec^2u-1) du=-\frac18\tan u+\frac18u+C=-\frac18\tan\frac4{x^2}+\frac{1}{2x^2}+C$$ **Answer:** $\color{red}{\boxed{-\tfrac18\tan\tfrac4{x^2}+\tfrac1{2x^2}+C}}$

**14)** $\displaystyle\int\tan^3(2x)\sec^3(2x) dx=$

> [!check]- Solution
> 
> $v=2x$: $\frac12\int\tan^2v\sec^2v (\sec v\tan v dv)$. With $w=\sec v$: $\frac12\int(w^2-1)w^2dw=\frac12\Big(\frac{w^5}5-\frac{w^3}3\Big)+C$. **Answer:** $\color{red}{\boxed{\tfrac1{10}\sec^52x-\tfrac16\sec^32x+C}}$

**15)** $\displaystyle\int_{\pi/4}^{\pi/2}\cot^4x dx=$

> [!check]- Solution
> 
> $\cot^4x=\cot^2x(\csc^2x-1)=\cot^2x\csc^2x-\csc^2x+1$, so the antiderivative is $-\frac{\cot^3x}{3}+\cot x+x$: $$\Big(0+0+\frac\pi2\Big)-\Big(-\frac13+1+\frac\pi4\Big)=\frac\pi4-\frac23$$ **Answer:** $\color{red}{\boxed{\tfrac\pi4-\tfrac23}}$

**16)** $\displaystyle\int_0^{\pi/4}\tan^5x\sec^6x dx=$

> [!check]- Solution
> 
> Save $\sec^2x$; $u=\tan x$ ($0\to1$), $\sec^4x=(1+u^2)^2$: $$\int_0^1u^5(1+u^2)^2du=\int_0^1(u^5+2u^7+u^9) du=\frac16+\frac14+\frac1{10}=\frac{31}{60}$$ **Answer:** $\color{red}{\boxed{\tfrac{31}{60}}}$

**17)** $\displaystyle\int_0^{\pi/2}\frac{\cos^5x}{\sqrt{\sin x}} dx=$

> [!check]- Solution
> 
> $u=\sin x$ ($0\to1$; the integral is improper at $0$ but converges): $\cos^5x dx=(1-u^2)^2du$. $$\int_0^1\big(u^{-1/2}-2u^{3/2}+u^{7/2}\big)du=2-\frac45+\frac29=\frac{64}{45}$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac{64}{45}}}$

**18)** $\displaystyle\int\cos^3x\sin^4x dx=$

> [!check]- Solution
> 
> $u=\sin x$: $\int(1-u^2)u^4du=\frac{u^5}5-\frac{u^7}7+C$. **Answer:** $\color{red}{\boxed{\tfrac{\sin^5x}5-\tfrac{\sin^7x}7+C}}$

**19)** $\displaystyle\int\sin^32\theta\sqrt{\cos2\theta} d\theta=$

> [!check]- Solution
> 
> $u=\cos2\theta,\ du=-2\sin2\theta d\theta$: $$-\frac12\int(1-u^2)u^{1/2}du=-\frac12\Big(\frac23u^{3/2}-\frac27u^{7/2}\Big)+C=-\frac13u^{3/2}+\frac17u^{7/2}+C$$ **Answer:** $\color{red}{\boxed{-\tfrac13(\cos2\theta)^{3/2}+\tfrac17(\cos2\theta)^{7/2}+C}}$

**20)** If $\displaystyle\int\sec^43x\tan^33x dx=\frac{\tan^43x}{A}+\frac{\tan^63x}{B}+C$, then $A+B=$

> [!check]- Solution
> 
> Save $\sec^23x$; $u=\tan3x,\ du=3\sec^23x dx$: $\ \frac13\int(1+u^2)u^3du=\frac{u^4}{12}+\frac{u^6}{18}$. So $A=12,\ B=18$. **Answer:** $\color{red}{\boxed{30}}$

**21)** $\displaystyle\int\csc^4(3x) dx=$

> [!check]- Solution
> 
> $\csc^4=(1+\cot^2)\csc^2$; $u=\cot3x,\ du=-3\csc^23x dx$: $\ -\frac13\int(1+u^2) du=-\frac13u-\frac19u^3+C$. **Answer:** $\color{red}{\boxed{-\tfrac13\cot3x-\tfrac19\cot^33x+C}}$

**22)** $\displaystyle\int\tan^3(3t)\sec^3(3t) dt=$

> [!check]- Solution
> 
> Save $\sec3t\tan3t$; $u=\sec3t,\ du=3\sec3t\tan3t dt$: $\ \frac13\int(u^2-1)u^2du=\frac{u^5}{15}-\frac{u^3}{9}+C$. **Answer:** $\color{red}{\boxed{\tfrac{\sec^53t}{15}-\tfrac{\sec^33t}9+C}}$

**23)** $\displaystyle\int_0^{\pi/4}\tan^4x dx=$

> [!check]- Solution
> 
> $\tan^4=\tan^2\sec^2-\tan^2=\tan^2\sec^2-\sec^2+1$, so $\int\tan^4x dx=\frac13\tan^3x-\tan x+x$. $$\Big[\tfrac13\tan^3x-\tan x+x\Big]_0^{\pi/4}=\tfrac13-1+\tfrac\pi4=\tfrac\pi4-\tfrac23$$ **Answer:** $\color{red}{\boxed{\tfrac\pi4-\tfrac23}}$

**24)** $\displaystyle\int\frac{\tan^2x}{\sec^5x} dx=$

> [!check]- Solution
> 
> $\frac{\tan^2x}{\sec^5x}=\sin^2x\cos^3x=\sin^2x(1-\sin^2x)\cos x$; $u=\sin x$: $\frac{u^3}3-\frac{u^5}5+C$. **Answer:** $\color{red}{\boxed{\tfrac13\sin^3x-\tfrac15\sin^5x+C}}$

**25)** $\displaystyle\int_0^{\pi/2}\sin8x\cos7x dx=$

> [!check]- Solution
> 
> $\sin8x\cos7x=\frac12(\sin x+\sin15x)$: $$\frac12\Big[-\cos x-\frac{\cos15x}{15}\Big]_0^{\pi/2}=\frac12\Big[0-\Big(-1-\frac1{15}\Big)\Big]=\frac8{15}$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac8{15}}}$

## 8.4 Trigonometric Substitution (25 problems)

**1)** $\displaystyle\int\sqrt{16-4x^2} dx$

> [!check]- Solution
> 
> $\sqrt{16-4x^2}=2\sqrt{4-x^2}$. With $x=2\sin\theta$: $2\int\sqrt{4-x^2} dx=2\cdot\frac12\Big(x\sqrt{4-x^2}+4\arcsin\frac x2\Big)+C$. **Answer:** $\color{red}{\boxed{x\sqrt{4-x^2}+4\arcsin\tfrac x2+C}}$

**2)** $\displaystyle\int\frac{dx}{(x^2+5)^{3/2}}$

> [!check]- Solution
> 
> $x=\sqrt5\tan\theta,\ dx=\sqrt5\sec^2\theta d\theta$, $(x^2+5)^{3/2}=5\sqrt5\sec^3\theta$: $$\frac15\int\cos\theta d\theta=\frac15\sin\theta+C=\frac{x}{5\sqrt{x^2+5}}+C$$
> 
> **Answer:** $\color{red}{\boxed{\dfrac{x}{5\sqrt{x^2+5}}+C}}$

**3)** $\displaystyle\int\frac{\sqrt{1-x}}{\sqrt x} dx$

> [!check]- Solution
> 
> $x=\sin^2\theta,\ dx=2\sin\theta\cos\theta d\theta$: the integrand becomes $\frac{\cos\theta}{\sin\theta}\cdot2\sin\theta\cos\theta=2\cos^2\theta$. $$\int(1+\cos2\theta) d\theta=\theta+\sin\theta\cos\theta+C=\arcsin\sqrt x+\sqrt x\sqrt{1-x}+C$$ **Answer:** $\color{red}{\boxed{\arcsin\sqrt x+\sqrt{x-x^2}+C}}$

**4)** $\displaystyle\int\frac{x}{\sqrt{x^2-6x+5}} dx$ (complete the square)

> [!check]- Solution
> 
> $x^2-6x+5=(x-3)^2-4$; $u=x-3$: $$\int\frac{u+3}{\sqrt{u^2-4}}du=\sqrt{u^2-4}+3\ln\big|u+\sqrt{u^2-4}\big|+C$$ **Answer:** $\color{red}{\boxed{\sqrt{x^2-6x+5}+3\ln\big|x-3+\sqrt{x^2-6x+5}\big|+C}}$

**5)** $\displaystyle\int_4^6\frac{x^2}{\sqrt{x^2-9}} dx$

> [!check]- Solution
> 
> $x=3\sec\theta$ gives $9\int\sec^3\theta d\theta$, i.e. $\int\frac{x^2}{\sqrt{x^2-9}}dx=\frac x2\sqrt{x^2-9}+\frac92\ln\big|x+\sqrt{x^2-9}\big|$. $$\Big[\ \Big]_4^6=\big(9\sqrt3-2\sqrt7\big)+\frac92\ln\frac{6+3\sqrt3}{4+\sqrt7}\approx12.644$$ **Answer:** $\color{red}{\boxed{9\sqrt3-2\sqrt7+\tfrac92\ln\tfrac{6+3\sqrt3}{4+\sqrt7}\approx12.644}}$

**6)** Find the area of the region of the circle of radius $a$ above a chord that is $h$ units ($0<h<a$) from the center.

> [!check]- Solution
> 
> Circle $x^2+y^2=a^2$, chord $y=h$. Horizontal strips have width $2\sqrt{a^2-y^2}$: $$A=2\int_h^a\sqrt{a^2-y^2} dy=\Big[y\sqrt{a^2-y^2}+a^2\arcsin\frac ya\Big]_h^a=\frac{\pi a^2}{2}-h\sqrt{a^2-h^2}-a^2\arcsin\frac ha$$ **Answer:** $\color{red}{\boxed{\tfrac{\pi a^2}{2}-a^2\arcsin\tfrac ha-h\sqrt{a^2-h^2}}}$

**7)** Find the arc length of $y=\frac{x^2}4-2x$ on $[4,8]$.

> [!check]- Solution
> 
> $y'=\frac{x-4}{2}$. Let $u=\frac{x-4}2$ ($0\to2$), $dx=2 du$: $$L=2\int_0^2\sqrt{1+u^2} du=\Big[u\sqrt{1+u^2}+\ln\big(u+\sqrt{1+u^2}\big)\Big]_0^2=2\sqrt5+\ln(2+\sqrt5)\approx5.916$$ **Answer:** $\color{red}{\boxed{2\sqrt5+\ln(2+\sqrt5)}}$

**8)** Find the volume of the torus generated by revolving the disk $(x-3)^2+y^2\le1$ about the $y$-axis.

> [!check]- Solution
> 
> Shells: $V=2\pi\int_2^4x\cdot2\sqrt{1-(x-3)^2} dx$. With $u=x-3$: $4\pi\int_{-1}^1(u+3)\sqrt{1-u^2} du=4\pi\Big(0+3\cdot\frac\pi2\Big)=6\pi^2$. **Answer:** $\color{red}{\boxed{6\pi^2}}$

**9)** Show that the arc length of $y=\sin x$ on $[0,2\pi]$ equals the circumference of the ellipse $x^2+2y^2=2$.

> [!check]- Solution
> 
> Arc: $L=\int_0^{2\pi}\sqrt{1+\cos^2x} dx$. Ellipse: $x=\sqrt2\cos t,\ y=\sin t$, so $C=\int_0^{2\pi}\sqrt{2\sin^2t+\cos^2t} dt=\int_0^{2\pi}\sqrt{1+\sin^2t} dt$. Shifting $t=x+\frac\pi2$ turns $\sin^2t$ into $\cos^2x$ over a full period, so the integrals are equal (both $\approx7.640$). $\blacksquare$ **Answer:** $\color{red}{\boxed{L=C=\int_0^{2\pi}\sqrt{1+\cos^2x} dx\approx7.640}}$

**10)** Two circles of radius 3 with centers $(-2,0)$ and $(2,0)$ intersect. Find the area of the shaded (overlap) region.

> [!check]- Solution
> 
> They meet at $x=0$; the lens runs from $x=-1$ to $1$. By symmetry, $$A=4\int_0^1\sqrt{9-(x+2)^2} dx=4\int_2^3\sqrt{9-u^2} du=4\Big[\frac u2\sqrt{9-u^2}+\frac92\arcsin\frac u3\Big]_2^3=18\arccos\frac23-4\sqrt5\approx6.196$$ **Answer:** $\color{red}{\boxed{18\arccos\tfrac23-4\sqrt5\approx6.196}}$

**11)** $\displaystyle\int_1^2\sqrt{-x^2+2x+3} dx=$

> [!check]- Solution
> 
> $-x^2+2x+3=4-(x-1)^2$; $x-1=2\sin\theta$ ($0\to\frac\pi6$): $$4\int_0^{\pi/6}\cos^2\theta d\theta=2\Big[\theta+\tfrac12\sin2\theta\Big]_0^{\pi/6}=2\Big(\frac\pi6+\frac{\sqrt3}{4}\Big)=\frac\pi3+\frac{\sqrt3}{2}$$ **Answer:** $\color{red}{\boxed{\tfrac\pi3+\tfrac{\sqrt3}2}}$

**12)** $\displaystyle\int_1^{5/2}\sqrt{-x^2+2x+8} dx=$

> [!check]- Solution
> 
> $9-(x-1)^2$; $x-1=3\sin\theta$ ($0\to\frac\pi6$): $$9\int_0^{\pi/6}\cos^2\theta d\theta=\frac92\Big[\theta+\tfrac12\sin2\theta\Big]_0^{\pi/6}=\frac92\Big(\frac\pi6+\frac{\sqrt3}4\Big)=\frac34\pi+\frac98\sqrt3$$ **Answer:** $\color{red}{\boxed{\tfrac34\pi+\tfrac98\sqrt3}}$

**13)** $\displaystyle\int_{1/2}^1\sqrt{x-x^2} dx=$

> [!check]- Solution
> 
> $x-x^2=\frac14-\big(x-\frac12\big)^2$; $x-\frac12=\frac12\sin\theta$ ($0\to\frac\pi2$): $$\frac14\int_0^{\pi/2}\cos^2\theta d\theta=\frac14\cdot\frac\pi4=\frac{\pi}{16}$$ (A quarter of a disk of radius $\frac12$.) **Answer:** $\color{red}{\boxed{\tfrac\pi{16}}}$

**14)** $\displaystyle\int_0^2x^2\sqrt{4-x^2} dx=$

> [!check]- Solution
> 
> $x=2\sin\theta$ ($0\to\frac\pi2$): $$16\int_0^{\pi/2}\sin^2\theta\cos^2\theta d\theta=4\int_0^{\pi/2}\sin^22\theta d\theta=2\Big[\theta-\tfrac14\sin4\theta\Big]_0^{\pi/2}=\pi$$ **Answer:** $\color{red}{\boxed{\pi}}$

**15)** $\displaystyle\int\frac{\sqrt{x-9}}{x} dx=$

> [!check]- Solution
> 
> $u=\sqrt{x-9}$, $x=u^2+9$, $dx=2u du$: $$\int\frac{2u^2}{u^2+9}du=\int\Big(2-\frac{18}{u^2+9}\Big)du=2u-6\tan^{-1}\frac u3+C$$ **Answer:** $\color{red}{\boxed{2\sqrt{x-9}-6\tan^{-1}\tfrac{\sqrt{x-9}}3+C}}$

**16)** $\displaystyle\int\frac{4 dx}{x^2\sqrt{16-x^2}}=$

> [!check]- Solution
> 
> $x=4\sin\theta$: $\int\frac{4\cdot4\cos\theta d\theta}{16\sin^2\theta\cdot4\cos\theta}=\frac14\int\csc^2\theta d\theta=-\frac14\cot\theta+C$, and $\cot\theta=\frac{\sqrt{16-x^2}}{x}$. **Answer:** $\color{red}{\boxed{-\tfrac{\sqrt{16-x^2}}{4x}+C}}$

**17)** $\displaystyle\int\frac{x^2}{\sqrt{3-x^2}} dx=$

> [!check]- Solution
> 
> $x=\sqrt3\sin\theta$: $\int3\sin^2\theta d\theta=\frac32(\theta-\sin\theta\cos\theta)+C$, with $\sin\theta=\frac x{\sqrt3},\ \cos\theta=\frac{\sqrt{3-x^2}}{\sqrt3}$. **Answer:** $\color{red}{\boxed{\tfrac32\sin^{-1}\tfrac x{\sqrt3}-\tfrac12x\sqrt{3-x^2}+C}}$

**18)** $\displaystyle\int\frac{dx}{(16-x^2)^{3/2}}=$

> [!check]- Solution
> 
> $x=4\sin\theta$: $\int\frac{4\cos\theta d\theta}{64\cos^3\theta}=\frac1{16}\tan\theta+C=\frac{1}{16}\cdot\frac{x}{\sqrt{16-x^2}}+C$. **Answer:** $\color{red}{\boxed{\tfrac{x}{16\sqrt{16-x^2}}+C}}$

**19)** $\displaystyle\int_0^{\sqrt3/2}\frac{dx}{(1-x^2)^{5/2}}=$

> [!check]- Solution
> 
> $x=\sin\theta$ ($0\to\frac\pi3$): $\int_0^{\pi/3}\sec^4\theta d\theta=\Big[\tan\theta+\frac{\tan^3\theta}{3}\Big]_0^{\pi/3}=\sqrt3+\sqrt3=2\sqrt3$. **Answer:** $\color{red}{\boxed{2\sqrt3}}$

**20)** $\displaystyle\int_2^{7/2}\sqrt{5+4x-x^2} dx=$

> [!check]- Solution
> 
> $5+4x-x^2=9-(x-2)^2$; $u=x-2$ ($0\to\frac32$): $$\Big[\frac u2\sqrt{9-u^2}+\frac92\arcsin\frac u3\Big]_0^{3/2}=\frac34\cdot\frac{3\sqrt3}{2}+\frac92\cdot\frac\pi6=\frac{9\sqrt3}{8}+\frac{3\pi}{4}$$ **Answer:** $\color{red}{\boxed{\tfrac{3\pi}4+\tfrac{9\sqrt3}8}}$

**21)** $\displaystyle\int\frac{x}{\sqrt{4x-x^2}} dx=$

> [!check]- Solution
> 
> $4x-x^2=4-(x-2)^2$; $u=x-2$: $\int\frac{u+2}{\sqrt{4-u^2}}du=-\sqrt{4-u^2}+2\arcsin\frac u2+C$.
> 
> **Answer:** $\color{red}{\boxed{2\arcsin\tfrac{x-2}2-\sqrt{4x-x^2}+C}}$

**22)** $\displaystyle\int\frac{x^3}{4\sqrt{4+x^2}} dx=$

> [!check]- Solution
> 
> $u=4+x^2,\ x^2=u-4$: $\frac18\int(u-4)u^{-1/2}du=\frac1{12}u^{3/2}-u^{1/2}+C=\frac{\sqrt u (u-12)}{12}+C$, and $u-12=x^2-8$. **Answer:** $\color{red}{\boxed{(x^2-8)\tfrac{\sqrt{4+x^2}}{12}+C}}$

**23)** $\displaystyle\int_{1/(2\sqrt3)}^{1/2}\frac{dx}{x^2\sqrt{4x^2+1}}=$

> [!check]- Solution
> 
> $2x=\tan\theta$ ($\frac\pi6\to\frac\pi4$), $dx=\frac12\sec^2\theta d\theta$: $$\int\frac{\frac12\sec^2\theta}{\frac14\tan^2\theta\sec\theta}d\theta=2\int\csc\theta\cot\theta d\theta=\Big[-2\csc\theta\Big]_{\pi/6}^{\pi/4}=-2\sqrt2+4$$ **Answer:** $\color{red}{\boxed{4-2\sqrt2}}$

**24)** $\displaystyle\int\frac{2x^2}{(4+x^2)^2} dx=$

> [!check]- Solution
> 
> $x=2\tan\theta$: $\int\frac{2\cdot4\tan^2\theta\cdot2\sec^2\theta}{16\sec^4\theta}d\theta=\int\sin^2\theta d\theta=\frac\theta2-\frac{\sin\theta\cos\theta}{2}+C$. $\sin\theta\cos\theta=\frac{x}{\sqrt{x^2+4}}\cdot\frac{2}{\sqrt{x^2+4}}=\frac{2x}{x^2+4}$. **Answer:** $\color{red}{\boxed{\tfrac12\arctan\tfrac x2-\tfrac{x}{x^2+4}+C}}$

**25)** $\displaystyle\int_{\sqrt3}^2\frac{\sqrt{x^2-3}}{x} dx=$

> [!check]- Solution
> 
> $x=\sqrt3\sec\theta$ ($0\to\frac\pi6$): $\int\sqrt3\tan^2\theta d\theta=\sqrt3(\tan\theta-\theta)$. $$\sqrt3\Big(\frac1{\sqrt3}-\frac\pi6\Big)=1-\frac{\sqrt3}{6}\pi$$ **Answer:** $\color{red}{\boxed{1-\tfrac{\sqrt3}6\pi}}$

## 8.5 Partial Fractions (25 problems)

**1)** $\displaystyle\int\frac{1}{x^2-9} dx$

> [!check]- Solution
> 
> $\frac{1}{(x-3)(x+3)}=\frac{1/6}{x-3}-\frac{1/6}{x+3}$. **Answer:** $\color{red}{\boxed{\tfrac16\ln\big|\tfrac{x-3}{x+3}\big|+C}}$

**2)** $\displaystyle\int\frac{2x^3-4x^2-15x+5}{x^2-2x-8} dx$

> [!check]- Solution
> 
> Divide: $2x^3-4x^2-15x+5=(x^2-2x-8)(2x)+(x+5)$. Then $\frac{x+5}{(x-4)(x+2)}=\frac{3/2}{x-4}-\frac{1/2}{x+2}$. **Answer:** $\color{red}{\boxed{x^2+\tfrac32\ln|x-4|-\tfrac12\ln|x+2|+C}}$

**3)** $\displaystyle\int\frac{x^2-6x+2}{x^3+2x^2+x} dx$

> [!check]- Solution
> 
> $\frac{x^2-6x+2}{x(x+1)^2}=\frac Ax+\frac{B}{x+1}+\frac{C}{(x+1)^2}$: $x=0\Rightarrow A=2$; $x=-1\Rightarrow9=-C\Rightarrow C=-9$; $x^2$-coefficient: $1=A+B\Rightarrow B=-1$.
> 
> **Answer:** $\color{red}{\boxed{2\ln|x|-\ln|x+1|+\dfrac{9}{x+1}+C}}$

**4)** $\displaystyle\int\frac{6x}{x^3-8} dx$

> [!check]- Solution
> 
> $\frac{6x}{(x-2)(x^2+2x+4)}=\frac{A}{x-2}+\frac{Bx+C}{x^2+2x+4}$: $x=2\Rightarrow12=12A\Rightarrow A=1$; $x^2$: $B=-1$; constant: $0=4A-2C\Rightarrow C=2$. $$\int\frac{-x+2}{x^2+2x+4}dx=-\frac12\ln(x^2+2x+4)+\int\frac{3 dx}{(x+1)^2+3}$$ **Answer:** $\color{red}{\boxed{\ln|x-2|-\tfrac12\ln(x^2+2x+4)+\sqrt3\arctan\tfrac{x+1}{\sqrt3}+C}}$

**5)** $\displaystyle\int_0^1\frac{x^2-x}{x^2+x+1} dx$

> [!check]- Solution
> 
> $\frac{x^2-x}{x^2+x+1}=1-\frac{2x+1}{x^2+x+1}$: $\Big[x-\ln(x^2+x+1)\Big]_0^1=1-\ln3$. **Answer:** $\color{red}{\boxed{1-\ln3}}$

**6)** $\displaystyle\int\frac{5\cos x}{\sin^2x+3\sin x-4} dx$

> [!check]- Solution
> 
> $u=\sin x$: $\int\frac{5 du}{(u+4)(u-1)}=\int\Big(\frac1{u-1}-\frac1{u+4}\Big)du$. **Answer:** $\color{red}{\boxed{\ln\Big|\dfrac{\sin x-1}{\sin x+4}\Big|+C}}$

**7)** $\displaystyle\int\frac{\sqrt x}{x-4} dx$

> [!check]- Solution
> 
> $u=\sqrt x$, $dx=2u du$: $\int\frac{2u^2}{u^2-4}du=\int\Big(2+\frac{8}{u^2-4}\Big)du=2u+2\ln\Big|\frac{u-2}{u+2}\Big|+C$. **Answer:** $\color{red}{\boxed{2\sqrt x+2\ln\Big|\dfrac{\sqrt x-2}{\sqrt x+2}\Big|+C}}$

**8)** Find the average value of $f(x)=\frac{1}{4x^2-1}$ from $x=1$ to $x=4$.

> [!check]- Solution
> 
> $\frac{1}{(2x-1)(2x+1)}=\frac12\Big(\frac1{2x-1}-\frac1{2x+1}\Big)$, so $\int f=\frac14\ln\Big|\frac{2x-1}{2x+1}\Big|$. $$f_{\text{avg}}=\frac13\cdot\frac14\Big(\ln\frac79-\ln\frac13\Big)=\frac1{12}\ln\frac73\approx0.0706$$ **Answer:** $\color{red}{\boxed{\tfrac1{12}\ln\tfrac73\approx0.0706}}$

**9)** The region bounded by $y=\frac{2x}{x^2+1},\ y=0,\ x=0,\ x=3$ is revolved about the $x$-axis. Find the volume.

> [!check]- Solution
> 
> $\frac{4x^2}{(x^2+1)^2}=\frac{4}{x^2+1}-\frac{4}{(x^2+1)^2}$, and $\int\frac{dx}{(x^2+1)^2}=\frac12\Big(\arctan x+\frac{x}{x^2+1}\Big)$: $$V=\pi\int_0^3\frac{4x^2}{(x^2+1)^2}dx=\pi\Big[2\arctan x-\frac{2x}{x^2+1}\Big]_0^3=2\pi\Big(\arctan3-\frac3{10}\Big)\approx5.963$$ **Answer:** $\color{red}{\boxed{2\pi\big(\arctan3-\tfrac3{10}\big)\approx5.963}}$

**10)** Evaluate $\displaystyle\int_0^1\frac{x}{1+x^4} dx$ in two ways, one of which is partial fractions.

> [!check]- Solution
> 
> **Substitution** $u=x^2$: $\frac12\int_0^1\frac{du}{1+u^2}=\frac12\cdot\frac\pi4=\frac\pi8$.  
> **Partial fractions:** $1+x^4=(x^2+\sqrt2x+1)(x^2-\sqrt2x+1)$ and $\frac{x}{1+x^4}=\frac{1}{2\sqrt2}\Big(\frac{1}{x^2-\sqrt2x+1}-\frac1{x^2+\sqrt2x+1}\Big)$. Completing squares gives the antiderivative $\frac12\big[\arctan(\sqrt2x-1)-\arctan(\sqrt2x+1)\big]$; from $0$ to $1$ this is $\frac12\Big[\frac\pi8-\frac{3\pi}8+\frac\pi2\Big]=\frac\pi8$.  
> **Answer:** $\color{red}{\boxed{\tfrac\pi8}}$

**11)** $\displaystyle\int_0^1\frac{x-4}{x^2-5x+6} dx=$

> [!check]- Solution
> 
> $\frac{x-4}{(x-3)(x-2)}=\frac{-1}{x-3}+\frac{2}{x-2}$: $$\Big[-\ln|x-3|+2\ln|x-2|\Big]_0^1=(-\ln2+0)-(-\ln3+2\ln2)=-3\ln2+\ln3$$ **Answer:** $\color{red}{\boxed{-3\ln2+\ln3}}$

**12)** $\displaystyle\int\frac{10}{(x-1)(x^2+9)} dx=$

> [!check]- Solution
> 
> $\frac{10}{(x-1)(x^2+9)}=\frac{1}{x-1}+\frac{-x-1}{x^2+9}$ ($A=1$, $B=-1$, $C=-1$): $$\ln|x-1|-\frac12\ln(x^2+9)-\frac13\tan^{-1}\frac x3+C$$ **Answer:** $\color{red}{\boxed{\ln|x-1|-\tfrac12\ln(x^2+9)-\tfrac13\tan^{-1}\tfrac x3+C}}$

**13)** $\displaystyle\int\frac{e^x}{e^{2x}+3e^x+2} dx=$

> [!check]- Solution
> 
> $u=e^x$: $\int\frac{du}{(u+1)(u+2)}=\int\Big(\frac1{u+1}-\frac1{u+2}\Big)du=\ln\Big|\frac{u+1}{u+2}\Big|+C$. **Answer:** $\color{red}{\boxed{\ln\tfrac{e^x+1}{e^x+2}+C}}$

**14)** $\displaystyle\int\frac{\cos x}{\sin x-\sin^2x} dx=$

> [!check]- Solution
> 
> $u=\sin x$: $\int\frac{du}{u(1-u)}=\int\Big(\frac1u+\frac1{1-u}\Big)du=\ln|u|-\ln|1-u|+C$. **Answer:** $\color{red}{\boxed{\ln\Big|\tfrac{\sin x}{1-\sin x}\Big|+C}}$

**15)** If $\dfrac{1}{x(x+1)^2}=\dfrac Ax+\dfrac{B}{x+1}+\dfrac{C}{(x+1)^2}$, then $A+B+C=$

> [!check]- Solution
> 
> $1=A(x+1)^2+Bx(x+1)+Cx$. $x=0$: $A=1$. $x=-1$: $C=-1$. $x=1$: $1=4A+2B+C\Rightarrow B=-1$. **Answer:** $\color{red}{\boxed{-1}}$

**16)** If $\dfrac{-13+9x-x^2}{(x-2)(x-1)^2}=\dfrac{A}{x-2}+\dfrac{B}{x-1}+\dfrac{C}{(x-1)^2}$, then $A+B+C=$

> [!check]- Solution
> 
> $x=2$: $1=A$. $x=1$: $-5=-C\Rightarrow C=5$. $x^2$-coefficient: $-1=A+B\Rightarrow B=-2$. **Answer:** $\color{red}{\boxed{4}}$

**17)** If $\dfrac{9-x^2}{7x^3+x}=\dfrac Ax+\dfrac{Bx+C}{7x^2+1}$, then $A+B+C=$

> [!check]- Solution
> 
> $9-x^2=A(7x^2+1)+(Bx+C)x$. Constant: $A=9$. $x^2$: $-1=7A+B\Rightarrow B=-64$. $x$: $C=0$.
> 
> **Answer:** $\color{red}{\boxed{-55}}$

**18)** If $\dfrac{2x^3-4x-8}{x(x-1)(x^2+4)}=\dfrac2x-\dfrac2{x-1}+\dfrac{Cx+D}{x^2+4}$, then $C+D=$

> [!check]- Solution
> 
> $2x^3-4x-8=2(x-1)(x^2+4)-2x(x^2+4)+(Cx+D)x(x-1)$. $x^3$: $2=2-2+C\Rightarrow C=2$. $x$: $-4=8-8-D\Rightarrow D=4$. **Answer:** $\color{red}{\boxed{6}}$

**19)** If $\dfrac{x^2+6x+4}{x^4+8x^2+16}=\dfrac{Ax+B}{x^2+4}+\dfrac{Cx+D}{(x^2+4)^2}$, then $A+B+C+D=$

> [!check]- Solution
> 
> $x^2+6x+4=(Ax+B)(x^2+4)+Cx+D$: $A=0,\ B=1,\ 4A+C=6\Rightarrow C=6,\ 4B+D=4\Rightarrow D=0$. **Answer:** $\color{red}{\boxed{7}}$

**20)** $\displaystyle\int\frac{3-x}{3x^2-2x-1} dx=$

> [!check]- Solution
> 
> $\frac{3-x}{(3x+1)(x-1)}=\frac{A}{3x+1}+\frac{B}{x-1}$: $x=1\Rightarrow B=\frac12$; $x=-\frac13\Rightarrow\frac{10}3=-\frac43A\Rightarrow A=-\frac52$. $$-\frac52\cdot\frac13\ln|3x+1|+\frac12\ln|x-1|+C$$ **Answer:** $\color{red}{\boxed{-\tfrac56\ln|3x+1|+\tfrac12\ln|x-1|+C}}$

**21)** $\displaystyle\int\frac{8x}{x^3+x^2-x-1} dx=$

> [!check]- Solution
> 
> $x^3+x^2-x-1=(x-1)(x+1)^2$; $\frac{8x}{(x-1)(x+1)^2}=\frac{2}{x-1}-\frac{2}{x+1}+\frac{4}{(x+1)^2}$. $$2\ln|x-1|-2\ln|x+1|-\frac{4}{x+1}+C$$ **Answer:** $\color{red}{\boxed{2\ln\big|\tfrac{x-1}{x+1}\big|-\tfrac4{x+1}+C}}$

**22)** $\displaystyle\int\frac{4}{(x-1)(x^2+1)} dx=$

> [!check]- Solution
> 
> $\frac{4}{(x-1)(x^2+1)}=\frac{2}{x-1}+\frac{-2x-2}{x^2+1}$: $$2\ln|x-1|-\ln(x^2+1)-2\arctan x+C$$ **Answer:** $\color{red}{\boxed{\ln\tfrac{(x-1)^2}{x^2+1}-2\arctan x+C}}$

**23)** If $\displaystyle\int\frac{x^2}{x^4-2x^2-8} dx=\frac16\Big[\ln\Big|\frac{x-2}{x+2}\Big|+\alpha\tan^{-1}\frac{x}{\sqrt2}\Big]+C$, then $\alpha=$

> [!check]- Solution
> 
> $\frac{x^2}{(x^2-4)(x^2+2)}=\frac{2/3}{x^2-4}+\frac{1/3}{x^2+2}$. $\int\frac{2/3}{x^2-4}=\frac23\cdot\frac14\ln\Big|\frac{x-2}{x+2}\Big|=\frac16\ln|\cdot|$ and $\int\frac{1/3}{x^2+2}=\frac{1}{3\sqrt2}\tan^{-1}\frac x{\sqrt2}=\frac16\cdot\sqrt2\tan^{-1}\frac{x}{\sqrt2}$. **Answer:** $\color{red}{\boxed{\alpha=\sqrt2}}$

**24)** $\displaystyle\int\frac{\sin x}{\cos x+\cos^2x} dx=$

> [!check]- Solution
> 
> $u=\cos x$: $-\int\frac{du}{u(1+u)}=-\int\Big(\frac1u-\frac1{u+1}\Big)du=\ln\Big|\frac{u+1}{u}\Big|+C=\ln|1+\sec x|+C$.
> 
> **Answer:** $\color{red}{\boxed{\ln|1+\sec x|+C}}$

**25)** $\displaystyle\int\frac{e^x}{(e^x-1)(e^x+4)} dx=$

> [!check]- Solution
> 
> $u=e^x$: $\int\frac{du}{(u-1)(u+4)}=\frac15\int\Big(\frac1{u-1}-\frac1{u+4}\Big)du=\frac15\ln\Big|\frac{u-1}{u+4}\Big|+C$. **Answer:** $\color{red}{\boxed{\tfrac15\ln\big|\tfrac{e^x-1}{e^x+4}\big|+C}}$

## 8.7 Rational Functions of Sine and Cosine (10 problems)

**1)** $\displaystyle\int\frac{d\theta}{2-3\sin\theta}$

> [!check]- Solution
> 
> $u=\tan\frac\theta2$: $\ 2-3\sin\theta=\frac{2u^2-6u+2}{1+u^2}$, so the integral becomes $\int\frac{du}{u^2-3u+1}=\int\frac{du}{\big(u-\frac32\big)^2-\frac54}$. $$=\frac{1}{\sqrt5}\ln\Big|\frac{u-\frac32-\frac{\sqrt5}{2}}{u-\frac32+\frac{\sqrt5}2}\Big|+C=\frac1{\sqrt5}\ln\Big|\frac{2\tan\frac\theta2-3-\sqrt5}{2\tan\frac\theta2-3+\sqrt5}\Big|+C$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac1{\sqrt5}\ln\Big|\tfrac{2\tan(\theta/2)-3-\sqrt5}{2\tan(\theta/2)-3+\sqrt5}\Big|+C}}$

**2)** $\displaystyle\int_0^{\pi/2}\frac{d\theta}{1+\sin\theta+\cos\theta}$

> [!check]- Solution
> 
> $1+\sin\theta+\cos\theta=\frac{2+2u}{1+u^2}$, so the integrand becomes $\frac{du}{1+u}$; $\theta=0\to u=0,\ \theta=\frac\pi2\to u=1$: $$\int_0^1\frac{du}{1+u}=\ln2$$
> 
> **Answer:** $\color{red}{\boxed{\ln2}}$

**3)** $\displaystyle\int\frac{\cos\theta}{1+\cos\theta} d\theta$

> [!check]- Solution
> 
> $\frac{\cos\theta}{1+\cos\theta}=1-\frac{1}{1+\cos\theta}$. With $u=\tan\frac\theta2$: $1+\cos\theta=\frac{2}{1+u^2}$, so $\int\frac{d\theta}{1+\cos\theta}=\int du=\tan\frac\theta2$. **Answer:** $\color{red}{\boxed{\theta-\tan\tfrac\theta2+C}}$

**4)** $\displaystyle\int\frac{4}{\csc\theta-\cot\theta} d\theta$

> [!check]- Solution
> 
> $\frac{4}{\csc\theta-\cot\theta}=\frac{4\sin\theta}{1-\cos\theta}$; with $w=1-\cos\theta$, $dw=\sin\theta d\theta$: $\ 4\int\frac{dw}{w}=4\ln|1-\cos\theta|+C$. (With $u=\tan\frac\theta2$ you get $8\ln|u|-4\ln(1+u^2)=4\ln\sin^2\frac\theta2=4\ln\frac{1-\cos\theta}2$, the same up to a constant.) **Answer:** $\color{red}{\boxed{4\ln|1-\cos\theta|+C}}$

**5)** $\displaystyle\int\frac{4}{3-5\sin x} dx=$

> [!check]- Solution
> 
> $u=\tan\frac x2$: $3-5\sin x=\frac{3u^2-10u+3}{1+u^2}$, so the integral becomes $\int\frac{8 du}{(3u-1)(u-3)}=\int\Big(\frac{-3}{3u-1}+\frac{1}{u-3}\Big)du$. $$=-\ln|3u-1|+\ln|u-3|+C=\ln\Big|\frac{u-3}{3u-1}\Big|+C$$ **Answer:** $\color{red}{\boxed{\ln\Big|\tfrac{\tan(x/2)-3}{3\tan(x/2)-1}\Big|+C}}$

**6)** $\displaystyle\int_0^{\pi/2}\frac{\pi}{1+\sin\theta+\cos\theta} d\theta=$

> [!check]- Solution
> 
> Use $u=\tan\frac\theta2$: $\sin\theta=\frac{2u}{1+u^2},\ \cos\theta=\frac{1-u^2}{1+u^2},\ d\theta=\frac{2du}{1+u^2}$, so $1+\sin\theta+\cos\theta=\frac{2+2u}{1+u^2}$ and $$\int_0^{\pi/2}\frac{\pi d\theta}{1+\sin\theta+\cos\theta}=\pi\int_0^1\frac{du}{1+u}=\pi\ln2$$ **Answer:** $\color{red}{\boxed{\pi\ln2}}$

**7)** Using $t=\tan\frac x2$, $\displaystyle\int_{\pi/3}^{\pi/2}\frac{dx}{1+\sin x-\cos x}=$

> [!check]- Solution
> 
> $1+\sin x-\cos x=\frac{2t^2+2t}{1+t^2}$, so the integrand becomes $\frac{dt}{t(t+1)}$; $x=\frac\pi3\to t=\frac1{\sqrt3}$, $x=\frac\pi2\to t=1$: $$\Big[\ln\frac{t}{t+1}\Big]_{1/\sqrt3}^{1}=\ln\frac12-\ln\frac{1}{1+\sqrt3}=\ln\frac{\sqrt3+1}{2}$$ **Answer:** $\color{red}{\boxed{\ln\tfrac{\sqrt3+1}2}}$

**8)** $\displaystyle\int_0^{\pi/2}\frac{d\theta}{3-2\cos\theta}=$

> [!check]- Solution
> 
> $3-2\cos\theta=\frac{1+5u^2}{1+u^2}$, so the integrand becomes $\frac{2 du}{1+5u^2}$ ($0\to1$): $$\frac{2}{\sqrt5}\Big[\arctan(\sqrt5u)\Big]_0^1=\frac2{\sqrt5}\arctan\sqrt5$$
> 
> **Answer:** $\color{red}{\boxed{\tfrac2{\sqrt5}\arctan\sqrt5}}$

**9)** $\displaystyle\int_{\pi/3}^{\pi/2}\frac{dx}{\cos x-1}=$

> [!check]- Solution
> 
> $\cos x-1=\frac{-2u^2}{1+u^2}$, so the integrand becomes $-\frac{du}{u^2}$, with antiderivative $\frac1u=\cot\frac x2$ (equivalently $\csc x+\cot x$, see 8.1-E6). $$\Big[\cot\tfrac x2\Big]_{\pi/3}^{\pi/2}=1-\sqrt3$$ **Answer:** $\color{red}{\boxed{1-\sqrt3}}$

**10)** If $\alpha=2\tan^{-1}(-3)$, then $\displaystyle\int_\alpha^0\frac{dx}{\cos x-3\sin x+3}=$ (hint: $u=\tan\frac x2$)

> [!check]- Solution
> 
> $x=\alpha\Rightarrow u=-3$; $x=0\Rightarrow u=0$. $\ \cos x-3\sin x+3=\frac{2u^2-6u+4}{1+u^2}$, so the integrand becomes $\frac{du}{(u-1)(u-2)}=\Big(\frac{1}{u-2}-\frac1{u-1}\Big)du$: $$\Big[\ln\Big|\frac{u-2}{u-1}\Big|\Big]_{-3}^{0}=\ln2-\ln\frac54=\ln\frac85$$ **Answer:** $\color{red}{\boxed{\ln\tfrac85}}$

## 8.8 Improper Integrals (25 problems)

**1)** Decide whether $\displaystyle\int_0^1\frac{2x-5}{x^2-5x+6} dx$ is improper. Explain.

> [!check]- Solution
> 
> $x^2-5x+6=(x-2)(x-3)$ is zero only at $x=2,3$, outside $[0,1]$. The integrand is continuous on $[0,1]$ and the limits are finite. (Its value is $\big[\ln|x^2-5x+6|\big]_0^1=\ln\frac23$.) **Answer:** $\color{red}{\boxed{\text{Not improper}}}$

**2)** $\displaystyle\int_{-\infty}^0xe^{-4x} dx$

> [!check]- Solution
> 
> By parts, $\int xe^{-4x}dx=-\frac{x}{4}e^{-4x}-\frac1{16}e^{-4x}=-e^{-4x}\Big(\frac x4+\frac1{16}\Big)$. $$\lim_{t\to-\infty}\Big[-\frac1{16}+e^{-4t}\Big(\frac t4+\frac1{16}\Big)\Big]$$ As $t\to-\infty$, $e^{-4t}\to\infty$ while $\frac t4+\frac1{16}\to-\infty$, so the limit is $-\infty$. **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**3)** $\displaystyle\int_{-\infty}^{\infty}\frac{4}{16+x^2} dx$

> [!check]- Solution
> 
> $\int\frac{4}{16+x^2}dx=\arctan\frac x4$. Split at $0$: $\big(0-(-\frac\pi2)\big)+\big(\frac\pi2-0\big)$. **Answer:** $\color{red}{\boxed{\pi}}$

**4)** $\displaystyle\int_0^\infty\frac{x^3}{(x^2+1)^2} dx$

> [!check]- Solution
> 
> $u=x^2+1$: $\frac12\int\frac{u-1}{u^2}du=\frac12\Big(\ln u+\frac1u\Big)$. As $u\to\infty$, $\ln u\to\infty$. **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**5)** $\displaystyle\int_0^e\ln x^2 dx$

> [!check]- Solution
> 
> $\ln x^2=2\ln x$ (for $x>0$); $\int\ln x dx=x\ln x-x$: $$2\lim_{t\to0^+}\Big[x\ln x-x\Big]_t^e=2\Big[(e-e)-\lim_{t\to0^+}(t\ln t-t)\Big]=2[0-0]=0$$ (using $\lim_{t\to0^+}t\ln t=0$ by L'Hôpital). **Answer:** $\color{red}{\boxed{\text{Converges to }0}}$

**6)** $\displaystyle\int_0^5\frac{dx}{25-x^2}$

> [!check]- Solution
> 
> Discontinuous at $x=5$. $\int\frac{dx}{25-x^2}=\frac1{10}\ln\Big|\frac{5+x}{5-x}\Big|\to\infty$ as $x\to5^-$. **Answer:** $\color{red}{\boxed{\text{Diverges}}}$

**7)** $\displaystyle\int_0^\infty\frac{4}{\sqrt x (x+6)} dx$

> [!check]- Solution
> 
> $u=\sqrt x$, $dx=2u du$: $\int_0^\infty\frac{8 du}{u^2+6}=\frac{8}{\sqrt6}\Big[\arctan\frac{u}{\sqrt6}\Big]_0^\infty=\frac8{\sqrt6}\cdot\frac\pi2$.
> 
> **Answer:** $\color{red}{\boxed{\tfrac{4\pi}{\sqrt6}}}$

**8)** Find all $p$ for which $\displaystyle\int_1^\infty\frac{1}{x^p} dx$ converges.

> [!check]- Solution
> 
> $p=1$: $\ln x\to\infty$ (diverges). $p\ne1$: $\Big[\frac{x^{1-p}}{1-p}\Big]_1^\infty$ is finite only when $1-p<0$, and then it equals $\frac{1}{p-1}$. **Answer:** $\color{red}{\boxed{p>1\ \ \big(\text{value }\tfrac1{p-1}\big)}}$

**9)** Region $y\le e^{-x},\ y\ge0,\ x\ge0$: (a) the area (b) the volume about the $x$-axis (c) the volume about the $y$-axis.

> [!check]- Solution
> 
> (a) $\int_0^\infty e^{-x}dx=1$ (b) $\pi\int_0^\infty e^{-2x}dx=\frac\pi2$ (c) Shells: $2\pi\int_0^\infty xe^{-x}dx=2\pi\big[-(x+1)e^{-x}\big]_0^\infty=2\pi$ **Answer:** $\color{red}{\boxed{1,\ \tfrac\pi2,\ 2\pi}}$

**10)** Find the arc length of $y=\sqrt{16-x^2}$ on $[0,4]$.

> [!check]- Solution
> 
> $\sqrt{1+y'^2}=\frac{4}{\sqrt{16-x^2}}$ (improper at $x=4$): $$\lim_{t\to4^-}4\arcsin\frac x4\Big|_0^t=4\cdot\frac\pi2=2\pi$$ (A quarter of the circle of radius $4$.) **Answer:** $\color{red}{\boxed{2\pi}}$

**11)** Find the area of the surface formed by revolving $y=2e^{-x}$ on $[0,\infty)$ about the $x$-axis.

> [!check]- Solution
> 
> $S=2\pi\int_0^\infty2e^{-x}\sqrt{1+4e^{-2x}} dx$. Let $u=2e^{-x}$, $du=-2e^{-x}dx$ ($x=0\to u=2$, $x\to\infty\Rightarrow u\to0$): $$S=2\pi\int_0^2\sqrt{1+u^2} du=\pi\Big[u\sqrt{1+u^2}+\ln\big(u+\sqrt{1+u^2}\big)\Big]_0^2=\pi\big[2\sqrt5+\ln(2+\sqrt5)\big]\approx18.59$$ **Answer:** $\color{red}{\boxed{\pi\big[2\sqrt5+\ln(2+\sqrt5)\big]}}$

**12)** For what value of $c$ does $\displaystyle\int_1^\infty\Big(\frac{cx}{x^2+2}-\frac1{3x}\Big)dx$ converge? Evaluate it for that $c$.

> [!check]- Solution
> 
> For large $x$ the integrand $\approx\frac{c-\frac13}{x}$, so it can only converge when $c=\frac13$. Then $$\frac13\int_1^\infty\Big(\frac{x}{x^2+2}-\frac1x\Big)dx=\frac16\Big[\ln\frac{x^2+2}{x^2}\Big]_1^\infty=\frac16(\ln1-\ln3)=-\frac{\ln3}{6}$$ **Answer:** $\color{red}{\boxed{c=\tfrac13;\ \text{value }-\tfrac16\ln3}}$

**13)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_{-\infty}^0 6x^2e^{-x^3} dx$

> [!check]- Solution
> 
> $u=-x^3$: $\int6x^2e^{-x^3}dx=-2e^{-x^3}$. $$\lim_{t\to-\infty}\Big[-2e^{-x^3}\Big]_t^0=\lim_{t\to-\infty}\big(-2+2e^{-t^3}\big)=\infty\quad(-t^3\to+\infty)$$ **Answer:** $\color{red}{\boxed{\text{diverges}}}$

**14)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_{-1}^3\frac{1}{\sqrt{3-x}} dx$

> [!check]- Solution
> 
> Discontinuous at $x=3$: $$\lim_{t\to3^-}\Big[-2\sqrt{3-x}\Big]_{-1}^t=0+2\sqrt4=4$$ **Answer:** $\color{red}{\boxed{\text{converges to }4}}$

**15)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_1^\infty\frac{\ln x}{x} dx$

> [!check]- Solution
> 
> $\Big[\frac{(\ln x)^2}{2}\Big]_1^t\to\infty$. **Answer:** $\color{red}{\boxed{\text{diverges}}}$

**16)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_4^\infty\frac{dx}{x(\ln x)^3}$

> [!check]- Solution
> 
> $u=\ln x$: $\Big[-\frac{1}{2(\ln x)^2}\Big]_4^\infty=0+\frac{1}{2(\ln4)^2}$. **Answer:** $\color{red}{\boxed{\tfrac1{2(\ln4)^2}}}$

**17)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_{-\infty}^0e^{3x} dx$

> [!check]- Solution
> 
> $\lim_{t\to-\infty}\frac13\big(1-e^{3t}\big)=\frac13$. **Answer:** $\color{red}{\boxed{\tfrac13}}$

**18)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_1^\infty(1-x)e^{-x} dx=$

> [!check]- Solution
> 
> By parts, $\int(1-x)e^{-x}dx=xe^{-x}$ (check: $\frac{d}{dx}xe^{-x}=(1-x)e^{-x}$). $$\lim_{t\to\infty}te^{-t}-1\cdot e^{-1}=0-\frac1e$$ **Answer:** $\color{red}{\boxed{-\tfrac1e}}$

**19)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_{-\infty}^{\infty}\frac{e^x}{1+e^{2x}} dx=$

> [!check]- Solution
> 
> $u=e^x$: antiderivative $\arctan(e^x)$. As $x\to\infty$ it tends to $\frac\pi2$; as $x\to-\infty$, to $\arctan0=0$. **Answer:** $\color{red}{\boxed{\tfrac\pi2}}$

**20)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_3^6\frac{dx}{\sqrt{36-x^2}}$

> [!check]- Solution
> 
> $\lim_{t\to6^-}\Big[\arcsin\frac x6\Big]_3^t=\frac\pi2-\frac\pi6=\frac\pi3$. **Answer:** $\color{red}{\boxed{\tfrac\pi3}}$

**21)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_0^8\frac{3}{\sqrt{8-x}} dx$

> [!check]- Solution
> 
> $\lim_{t\to8^-}\Big[-6\sqrt{8-x}\Big]_0^t=6\sqrt8=12\sqrt2$. **Answer:** $\color{red}{\boxed{12\sqrt2}}$

**22)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_0^2\frac{dx}{\sqrt[3]{x-1}}$

> [!check]- Solution
> 
> Split at $x=1$; the antiderivative $\frac32(x-1)^{2/3}$ is continuous there: $$\Big[\tfrac32(x-1)^{2/3}\Big]_0^1+\Big[\tfrac32(x-1)^{2/3}\Big]_1^2=\Big(0-\tfrac32\Big)+\Big(\tfrac32-0\Big)=0$$ **Answer:** $\color{red}{\boxed{0}}$

**23)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_{-1}^2\frac{dx}{x^3}$

> [!check]- Solution
> 
> Discontinuous at $0$: $\int_{-1}^0x^{-3}dx=\lim_{t\to0^-}\Big[-\frac{1}{2x^2}\Big]_{-1}^t=-\infty$, so the whole integral diverges. **Answer:** $\color{red}{\boxed{\text{diverges}}}$

**24)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_3^\infty\frac{dx}{x\sqrt{x^2-9}}$

> [!check]- Solution
> 
> Improper at both ends; antiderivative $\frac13 \mathrm{arcsec}\frac x3$: $$\frac13\Big(\lim_{x\to\infty}\mathrm{arcsec}\frac x3-\mathrm{arcsec} 1\Big)=\frac13\Big(\frac\pi2-0\Big)=\frac\pi6$$ **Answer:** $\color{red}{\boxed{\tfrac\pi6}}$

**25)** Determine whether the integral converges or diverges; evaluate it if it converges: $\displaystyle\int_0^5\frac{10}{x} dx$

> [!check]- Solution
> 
> $\lim_{t\to0^+}10\big(\ln5-\ln t\big)=\infty$ ($p=1$ on $[0,5]$). **Answer:** $\color{red}{\boxed{\text{diverges}}}$