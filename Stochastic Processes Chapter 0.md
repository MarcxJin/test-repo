# Stochastic Processes Chapter 0

<script type="text/javascript"
scr = "http://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>

## 0.4&emsp;Exercises

**0.1** &emsp;Find all functions $x(t),y(t)$ satisfying $$x'(t)=y(t)-x(t),$$ $$y'(t)=3x(t)-3y(t).$$  Find the particular pair of functions satisfying $x(0)=y(0)=1/2.$

**Solution: ** This is a first-order linear system of equation with 
$$
\textbf{A} = 
\left(
\begin{matrix}
-1 & 1 \\
3 & -3
\end{matrix}
\right)
$$
Let $\textbf{A} = \textbf{Q}^{-1}\textbf{DQ}$ where 
$$\textbf{Q}^{-1}=
\left(
\begin{matrix}
1 & 1 \\
1 & -3
\end{matrix} 
\right), 
\textbf{D} = 
\left(
\begin{matrix}
0 & 0 \\
0 & -4
\end{matrix}
\right).$$
Thus 
$$
\left(
\begin{matrix}
x(t)  \\
y(t)
\end{matrix}
\right)=e^{t\textbf{A}}v_0
=\textbf{Q}^{-1}e^{t\textbf{D}}\textbf{Q}v_0=\left(
\begin{matrix}
\frac{3}{4}+\frac{1}{4}e^{-4t} & \frac{1}{4}-\frac{1}{4}e^{-4t} \\
\frac{3}{4}-\frac{3}{4}e^{-4t} & \frac{1}{4}+\frac{3}{4}e^{-4t}
\end{matrix}
\right)
\left(
\begin{matrix}
x(0)  \\
y(0)
\end{matrix}
\right).
$$
This is the general form of all solutions. The one that satisfying $x(0)=y(0)=1/2$  is
$$
x(t)=y(t)=\frac{1}{2}.
$$

---
**0.2** &emsp; Find the function $f(n), n = 0,1,...,10 $ that satisfies
$$
f(n)=\frac{1}{4}f(n-1)+\frac{3}{4}f(n+1), n = 1,2,...,9,
$$
and $f(0)=0, f(1)=1.$

**Solutions:**&emsp; By fomulae $(0.5)$, 
$$
f(n)=c_1+c_2(\frac{1-p}{p})^n,
$$ where $p=\frac{3}{4}$. We know $f(0)=0, f(1)=1,$ so
$$
f(0)=c_1+c_2=0\\
f(1)=c_1+\frac{1}{3}c_2=1.
$$
We get $c_1 = \frac{3}{2}, c_2=-\frac{3}{2}$. Thus $f(n)=\frac{3}{2}-\frac{3}{2}(\frac{1}{3})^n$.

---

**0.3** &emsp; The Fibonacci numbers $F_n$ are defined by $F_1=1, F_2=1$ and for $n>2, F_n = F_{n-1}+F_{n-2}$. Find a formula for $F_n$ by solving the difference equation.

**Solutions:** &emsp; Assume $F_n = c_1\alpha_1^n+c_2\alpha_2^n,$ where $\alpha_1,\alpha_2$ satistisfy the equation $\alpha^n=\alpha^{n-1}+\alpha^{n-2}$. Thus $$\alpha_1 = \frac{1+\sqrt{5}}{2}, \alpha_2 = \frac{1-\sqrt{5}}{2}.$$
Plug $F_1, F_2$ into $F_n = c_1\alpha_1^n+c_2\alpha_2^n$, we get $c_1 = -c_2 = \frac{1}{\sqrt{5}}$.
Therefore, the formula is $$F_n = \frac{1}{\sqrt{5}}\left[\left(\frac{1+\sqrt{5}}{2}\right)^n+\left(\frac{1-\sqrt{5}}{2}\right)^n\right].$$

---
**0.4** &emsp; Find the function $f(n), n = 0,1,2,...$ that satisfies $$f(0)=0,$$ $$f(n)=\frac{1}{3}f(n-1)+\frac{1}{3}f(n+1)+\frac{1}{3}f(n+2), n \ge1,$$ $$\lim_{n\to\infty}f(n)=1.$$

**Solutions:** &emsp; Assume $f(n)=c_1\alpha_1^n+c_2\alpha_2^n+c_3\alpha_3^n$, where $\alpha_1, \alpha_2, \alpha_3$ satisfy the equation$\alpha^n=\frac{1}{3}\alpha^{n-1}+\frac{1}{3}\alpha^{n+1}+\frac{1}{3}\alpha^{n+2}$. Solve the equation we get
$$\alpha_1 = 1, \alpha_2=\sqrt{2}-1,\alpha_3=-\sqrt{2}-1$$