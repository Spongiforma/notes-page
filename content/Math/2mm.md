+++
title = "Mathematical methods pt. 2"
author = ["root"]
draft = false
+++

## Fourier series {#fourier-series}

\\[
f(x) = \frac{a\_0}{2} + \sum\_{r=1}^\infty \left[a\_r \cos\left(\frac{2\pi r x}{L}\right) + b\_r \sin\left(\frac{2\pi r x}{L}\right)\right]
\\]


### Dirichlet conditions {#dirichlet-conditions}

The conditions a function must fulfil in order that it may be expanded as a fourier series.

-   The function must be periodic\*
-   It must be single-valued and continuous, except at a finite number of finite discontinuties
-   It must have only have a finite number of maxima and minima within one period
-   The integral over one period of |f(x)| must converge

    Then the fourier series will converge to f(x) at all points where f(x) is continuous.


### Properties of fourier series {#properties-of-fourier-series}

-   Completeness
-   All terms are mutually orthogonal

    i.e.

\\[
\int\_{x\_0}^{x\_0+L}\sin(2\pi r x / L)\cos(2 \pi p x/L)\dd{x} = 0
\\]

for all r and p
\\[
\int\_{x\_0}^{x\_0+L}\cos(2\pi r x / L)\cos(2 \pi p x/L)\dd{x} =\begin{cases}
L & r = p = 0 \\\\
\frac12 L & r = p > 0 \\\\
0 & r \neq p
\end{cases}
\\]

\\[
\int\_{x\_0}^{x\_0+L}\sin(2\pi r x / L)\sin(2 \pi p x/L)\dd{x} =\begin{cases}
0 & r = p = 0 \\\\
\frac12 L & r = p > 0 \\\\
0 & r \neq p
\end{cases}
\\]

where r and p are integers greater than or equal to zero.


### Fourier coefficients {#fourier-coefficients}

\\[
a\_r = \frac{2}{L} \int\_{x\_0}^{x\_0+L}f(x)\cos(2\pi r x / L) \dd{x}
\\]
\\[
b\_r = \frac{2}{L} \int\_{x\_0}^{x\_0+L}f(x)\sin(2\pi r x / L) \dd{x}
\\]


#### Symmetry about quarter period {#symmetry-about-quarter-period}

if f(x) is even about L/4 then a_odd = 0 and b_even = 0
if f(x) is odd about L/4 then a_2r = 0 and b_odd = 0


### Discontinuous functions {#discontinuous-functions}

At a discontinuity the value of the fourier series at that point is halfway between the upper and lower values. There is also an overshoot which does not disappear in the limit of an infinite number of terms. This is the **Gibbs' phenomenon**


### Non-periodic functions {#non-periodic-functions}

Can be extended to non-periodic functions by extending them (in numerous ways), usually to odd or even functions. Care must be taken that it converges properly at possible discontinuities at the ends.


### Integration and differentiation {#integration-and-differentiation}

Try it out!


### Complex fourier series {#complex-fourier-series}

\\[
f(x) = \sum\_{r=-\infty}^\infty c\_r \exp(2 \pi i r x / L)
\\]

\\[
c\_r = \frac{1}{L}\int\_{x\_0}^{x\_0+L}f(x)\exp(-\frac{2 \pi i r x}{L})\dd{x}
\\]

in relation to real fourier coefficients:

\begin{align\*}
c\_r & = \frac12 (a\_r - i b\_r) \\\\
c\_{-r} & = \frac12 (a\_r + i b\_r) \\\\
\end{align\*}

if f(x) is real then \\(c\_{-r} = c\_r^\*\\)


### Parseval's theorem {#parseval-s-theorem}

\begin{align\*}
\frac{1}{L} \int\_{x\_0}^{x\_0+L}|f(x)|^2 \dd{x} & = \sum\_{-\infty}^\infty |c\_r|^2 \\\\
& =(\frac12 a\_0)^2 + \frac12 \sum\_{r=1}^\infty (a\_r^2 + b\_r^2)
\end{align\*}


## Integral transforms {#integral-transforms}


### Fourier transform {#fourier-transform}

Recall that a periodid function f can be expressed as:

\\[
f(t) = \sum\_{r=-\infty}^\infty c\_r e^{2\pi i r t/ T} = \sum\_{r=-\infty}^\infty c\_r e^{i\omega\_r t}
\\]

where \\(\omega\_r = 2\pi r / T\\)

The fourier transform of f(t):

\\[
\tilde{f}(\omega) = \frac{1}{\sqrt{2\pi}} \int\_{-\infty}^\infty f(t) e^{-i\omega t} \dd{t}
\\]

\\[
f(t) = \frac{1}{\sqrt{2\pi}} \int\_{-\infty}^\infty \tilde{f}(\omega) e^{i\omega t} \dd{\omega}
\\]


#### Dirac delta function {#dirac-delta-function}

\\[
\delta(t-u) = \frac{1}{2\pi} \int\_{-\infty}^\infty e^{i\omega (t-u)}\dd{\omega}
\\]

\\[
\delta(t) = \lim\_{\Omega \to \infty} \left(\frac{\sin\Omega t}{\pi t}\right)
\\]

\\[
\tilde{\delta}(\omega) = \frac{1}{\sqrt{2\pi}}
\\]

\\[
H'(t) = \delta(t)
\\]


#### Properties {#properties}

-   Differentiation

\\[
\mathcal{F}[f'(t)] = i\omega \tilde{f}(\omega)
\\]

and so on for higher derivatives

-   Integration

\\[
\mathcal{F}\left[\int^t f(s) \dd{s}\right] = \frac{1}{i\omega}\tilde{f}(\omega) + 2\pi c \delta(\omega)
\\]

where c is a constant.

-   Scaling

\\[
\mathcal{F}[f(at)] = \frac{1}{a}\tilde{f}\left(\frac{\omega}{a}\right)
\\]

-   Translation

\\[
\mathcal{F}[f(t + a)] = e^{ia\omega}\tilde{f}(\omega)
\\]

-   Exponential multiplication

\\[
\mathcal{F}[e^{\alpha t}f(t)] = \tilde{f}(\omega + i\alpha)
\\]

where \\(\alpha \in \mathbb{C}\\)


#### Odd and even functions {#odd-and-even-functions}

<!--list-separator-->

-  Odd

    \\[
    \tilde{f}(\omega) = \sqrt{\frac{2}{\pi}} \int\_0^\infty f(t) \sin\omega t \dd{t}
    \\]

    \\[
    f(t) = \sqrt{\frac{2}{\pi}} \int\_0^\infty \tilde{f}(\omega) \sin\omega t \dd{\omega}
    \\]

    For even functions, we can replace sin with cos.


#### Convolution and Deconvolution {#convolution-and-deconvolution}

\\[
h(z) = \int\_{-\infty}^\infty f(x)g(z-x) \dd{x}
\\]

where f(x) is the 'true' function and g(z-x) is the resolution function.


#### Parseval's theorem {#parseval-s-theorem}

\\[
\int\_{-\infty}^\infty \vert f(t) \vert^2 \dd{t} = \int\_{-\infty}^\infty \vert \tilde{f}(\omega) \vert^2 \dd{\omega}
\\]


### Laplace transform {#laplace-transform}

When a function does not satisfy the dirichlet conditions as it may not converge at infinity or if it is only defined for t &gt; 0. we may want to use the Laplace transform.

\\[
\bar{f}(s) = \int\_0^\infty f(t)e^{-st}\dd{t}
\\]

where we assume s is real. Usually, for a given f(t), there will be some real number \\(s\_0\\) such that the integral exists for \\(s > s\_0\\) but diverges otherwise.


#### Standard Lapalace transforms {#standard-lapalace-transforms}

look up a table


#### Laplace transforms of derivatives and integrals {#laplace-transforms-of-derivatives-and-integrals}

\\[
\mathcal{L}\left[\dv[n]{f}{t}\right] = s^n\bar{f} - s^{n-1}f(0) - s^{n-2}f'(0) - \ldots - \dv[n-1]{f}{t}(0), \text{ for s > 0}
\\]

\\[
\mathcal{L}\left[\int\_0^t f(u)\dv{u}\right] = \frac{1}{s}\mathcal{L}[f]
\\]


## Ordinary Differential equations {#ordinary-differential-equations}

**Order** is the order of the highest derivative it contains
**Degree** is the power to which the highest order derivative is raised (after rationalisation)


### 1st-degree, 1st-order {#1st-degree-1st-order}


#### Seperable-variable equations {#seperable-variable-equations}

**Form**:

\\[
\dv{y}{x} = f(x)g(y)
\\]

**Solution method**:

Factorise when necessary.

\\[
\int \frac{\dd{y}}{g(y)} = \int f(x) \dd{x}
\\]


#### Exact equations {#exact-equations}

**Form**:

\\[
A(x,y) \dd{x} + B(x,y) \dd{y} = 0
\\]

where the expression is an exact differential.

Since \\(\pdv{A}{y} = \pdv{B}{x}\\), we may equate the expression to dU and thus dU = 0, U = c.

**Solution method**:

Make sure to check that its exact.
\\[
U(x,y) = \int A(x,y) \dd{x} + F(y)
\\]

F(y) can be found by differentiating U wrt y and equating the expression to B(x,y). Then sub back in.


#### Inexact equations: integrating factors {#inexact-equations-integrating-factors}

**Form**:

Above but inexact.

The differential can be made exact by multiplying by an **integrating factor** \\(\mu(x,y)\\) which obeys:

\\[
\pdv{(\mu A)}{y} = \pdv{(\mu B)}{x}
\\]

If the integrating factor is a function of either x or y alone then the eq can be explicitly solved. Assuming \\(\mu = \mu(x)\\):

\begin{align\*}
&\mu\pdv{A}{y} =\mu \pdv{B}{x} + B\pdv{\mu}{x} \\\\
\implies & \frac{\dd{\mu}}{\mu} = \frac{1}{B}\left(\pdv{A}{y}-\pdv{B}{x}\right)\dd{x} = f(x) \dd{x}
\end{align\*}

where we require f(x) be a function of x only.

**Solution method**:

In which case,

\\[
\mu(x) = \exp\left\\{\int f(x) \dd{x}\right\\} \text{   where   } f(x) = \frac{1}{B}\left(\pdv{A}{y}-\pdv{B}{x}\right)
\\]

\\[
\mu(y) = \exp\left\\{\int f(y) \dd{y}\right\\} \text{   where   } f(y) = \frac{1}{A}\left(\pdv{B}{x}-\pdv{A}{y}\right)
\\]


#### Linear equations {#linear-equations}

Special case of inexact ODEs

**Form**:

\\[
\dv{y}{x} + P(x)y = Q(x)
\\]

**Solution method**:

\\[
\mu(x) = \exp\left\\{\int P(x) \dd{x}\right\\}
\\]

Multiply throughout and then integrate left and right hand sides.


#### Homogenous equations {#homogenous-equations}

**Form**:

\\[
\dv{y}{x} = \frac{A(x,y)}{B(x,y)} = F\left(\frac{y}{x}\right)
\\]

where A(x,y) and B(x,y) are homogenous functions of the same degree. A function is homogenous of degree n if it obeys:

\\[
f(\lambda x,\lambda y) = \lambda^n f(x,y)
\\]

in general, the sum of the powers of x and y in each term of A and B should be the same.

**Solution method**:

The equation may solved by making the substitution y = vx, so that:

\\[
\dv{y}{x} = v + x\dv{v}{x} = F(v)
\\].

This is now seperable and can be integrated directly to give:

\\[
\int \frac{\dd{v}}{F(v) - v} = \int \frac{\dd{x}}{x}
\\]


#### Isobaric {#isobaric}

**Form**:

A generalisation of the homogeneous ODE.

\\[
\dv{y}{x} = \frac{A(x,y)}{B(x,y)}
\\]

where the equation is dimensionally consistent if y and dy are each given a weight m relative to x and dx. i.e. if the substitution y=vx^m makes it seperable

**Solution method**:
Write the equation in the form Adx + Bdy = 0. Given y and dy weight m and x and dx each weight 1. then find an m which makes all the sums equal


#### Bernoulli's equation {#bernoulli-s-equation}

**Form**:

\\[
\dv{y}{x} + P(x)y = Q(x)y^n \text{ where $n\neq 0$ or $1$}
\\]

**Solution method**:

The equation can be made linear by substituting \\(v = y^{1-n}\\) and correspondingly

\\[
\dv{y}{x} = \left(\frac{y^n}{1-n}\right) \dv{v}{x}
\\]

This can be substituted into the first equation and we find:

\\[
\dv{v}{x} + (1-n)P(x)v = (1-n)Q(x)
\\]

which is linear and can then be solved.


#### Miscellaneous {#miscellaneous}

<!--list-separator-->

-  ax + by + c

    **Form**:

    \\[\dv{y}{x} = F(ax + by + c)\\]

    **Solution method**:

    Letting v = ax + by + c,

    \\[
      \dv{v}{x} = a + b\dv{y}{x} = a + bF(v)
    \\]

    which can be solved.

<!--list-separator-->

-  y' = ax+by+c/ex+fy+g

    **Form**:

    \\[
    \dv{y}{x} = \frac{ax + by + c}{ex + fy + g}
    \\]

    unless a/e = b/f where it reduces to the form above.

    **Solution method**:

    By letting \\(x = X + \alpha\\) and \\(y = Y + \beta\\), where \\(\alpha\\) and \\(\beta\\) are found from:

    \\[
    a\alpha + b\beta + c = 0
    \\]

    \\[
    e\alpha + f\beta + g = 0
    \\]

    \\[
    \dv{Y}{X} = \frac{aX + bY}{eX + fY}
    \\]


### Higher-degree 1st-order equations {#higher-degree-1st-order-equations}

Can expressed as:

\\[
p^n + a\_{n-1}(x,y)p^{n-1} + \ldots + a\_1(x,y)p + a\_0(x,y) = 0
\\]

where \\(p = \dd{y}/\dd{x}\\)

Singular solutions are sometimes given which contain no arbitrary constants.


#### Equations soluble for p {#equations-soluble-for-p}

If the LHS can be factorised into the form:

\\[
(p-F\_1)(p-F\_2)\ldots(p-F\_2)=0
\\]

then we are left with solving the n first-degree equations \\(p = F\_i\\)


#### Equations soluble for x {#equations-soluble-for-x}

If the equation can be expressed as:

\\[
x = F(y,p)
\\]

then it can be reduced to:

\\[
\dv{x}{y} = \frac{1}{p} = \pdv{F}{y} + \pdv{F}{p}\dv{p}{y}
\\]

which can be factorized


#### Equations soluble for y {#equations-soluble-for-y}

If the equation can be expressed as:

\\[
x = F(y,p)
\\]

then it can be reduced to:

\\[
\dv{y}{x} = p = \pdv{F}{x} + \pdv{F}{p}\dv{p}{x}
\\]

which can be factorized.


#### Clairaut's equation {#clairaut-s-equation}

Special case of equations soluble for y.

**Form:**

\\[
y = px + F(p)
\\]

The general solution is given by \\(y = c\_1 x + F(c\_1)\\), the singular solution can often be found from the relation:

\\[
\dv{F}{p} + x = 0
\\]


### Higher-order linear equations {#higher-order-linear-equations}

Linear ODE of general order:

\\[
a\_n(x)\dv[n]{y}{x} + a\_{n-1}(x)\dv[n-1]{y}{x} + \ldots +a\_1(x)\dv{y}{x} + a\_0(x)y = f(x)
\\]

An nth order linear ODE must have n linearly independent solutions for the complementary equation. Their linear independence can be confirmed by forming n simultaneous equations for the n constants by repeatedly differentiating them and noticing that RHS is always zero for the complementary solution. This can be constructed as a determinant or the **Wronkskian** of the set of functions. If it does not vanish then the n functions are linearly independent though the converse does not necessarily apply.


#### Linear equations with constant coefficients {#linear-equations-with-constant-coefficients}

(The coefficients \\(a\_m\\) are constants)

To find the complementary solution try a solution of the form Ae^kx, and we are left with an auxillary equation in k. If all roots are distinct then the solutions are linearly independent and can be superposed. If some roots are complex and all coefficients are real, then it for every complex root its complex conjugate is also a root. If some roots are repeated, then we must try solutions of the form \\(x^ne^{kx}\\) are also solutions.

for particular solutions, use method of undetermined coefficients.

-   if f(x) = ae^rx, try be^rx
-   if f(x) = a sin(rx) + b cos(rx) (a or b may be zero), then try c sin(rx) + d cos(rx)
-   if f(x) = polynomial of degree N, where some coefficients may be zero, then try another polynomial of degree N.


#### Linear recurrence relations {#linear-recurrence-relations}

Form:

\\[
u\_{n+1} = \sum\_{r=0}^{N-1}a\_r u\_{n-r} + k
\\]

where k may be a simple function of n.

Equations involving terms whose indices differ by up to N are called Nth-order recurrence relations. If k=0, then the relation is called homogenous.

<!--list-separator-->

-  First-order recurrence relations

    For the equation:

    \\[
    u\_{n+1} = au\_n + k
    \\]

    the general solution is:

    when \\(a \neq 1\\):
    \\[
    u\_n = u\_0 a^n + k \frac{1-a^n}{1-a}
    \\]
    when a = 1:

    \\[
    u\_n = u\_0 + nk
    \\]

<!--list-separator-->

-  Second-order recurrence relations

    Similar to differential equations, Try a solution of the form \\(A\lambda^n\\) for the homogenous solution and solve the characteristic equation in lambda. If there are repeated roots, then try the general solution \\((A + Bn)\lambda\_1^n\\).


#### Laplace transform {#laplace-transform}

The laplace transform is defined as:

\\[
\bar{f}(s) = \int\_0^\infty e^{-sx}f(x)\dd{x}
\\]

Recall that the Laplace transform of the nth derivative of \\(f(x)\\) is:

\\[
\mathcal{L}\left[f^{(n)}(s)\right] = s^n\bar{f}(s) - s^{n-1}f(0) - s^{n-2}f'(0) - \ldots - sf^{(n-2)}(0) - f^{(n-1)}(0)
\\]

After getting \\(\bar{f}(s)\\), we may apply the inverse Laplace transform.


### Linear equations with variable coefficients {#linear-equations-with-variable-coefficients}

Although there is no generally applicable method, in certain cases a solution is possible.


#### Legendre and Euler linear equations {#legendre-and-euler-linear-equations}

Legendre's linear equation has the form

\\[
a\_n(\alpha x+ \beta)^n \dv[n]{y}{x} + \ldots + a\_1(\alpha x + \beta)\dv{y}{x} + a\_0 y = f(x)
\\]

By making the substitution \\(\alpha x + \beta = e^t\\), we have:

\\[
\dv{y}{x} = \dv{t}{x} \dv{y}{t} = \frac{\alpha}{\alpha x + \beta} \dv{y}{t}
\\]

\\[
\dv[2]{y}{x} = \frac{\alpha^2}{(\alpha x + \beta)^2}\left(\dv[2]{y}{t} - \dv{y}{t})
\\]

and so on.

\\[
(\alpha x + \beta)^n \dv[n]{y}{x} = \alpha^n \dv{}{t}\left(\dv{}{t} - 1 \right)\ldots\left(\dv{}{t} -n + 1\right)y
\\]

Legendre's linear equation thus becomes:

\\[
a\_n \alpha^n \dv{}{t}\left(\dv{}{t} - 1\right) \ldots \left(\dv{}{t} - n + 1\right)y + \ldots + a\_1 \alpha \dv{y}{t} + a\_0y = f\left(\frac{e^t - \beta}{\alpha}\right)
\\]

which can be solved with previously discussed methods.

<!--list-separator-->

-  Euler's equation

    Euler's equation is a special case where \\(\alpha = 1\\) and \\(\beta = 0\\).

    If \\(f(x) = 0\\), then substituting \\(y = x^\lambda\\) leads to a simple algebraic equation in \\(\lambda\\). If \\(\lambda\_1\\) is a k-fold root, then \\(x^\lambda\_1, x^\lambda\_1\ln x, \ldots, x^\lambda\_1(\ln x)^{k-1}\\) are k LI solutions corresponding to the root.


#### Exact equations {#exact-equations}

Sometimes, an ODE is merely the derivative of another ODE of an order lower, in which case it is called exact. It can be shown the nth-order linear ODE:

\\[
a\_n(x)\dv[n]{y}{x} + \ldots + a\_1(x)\dv{y}{x}  + a\_0(x)y = f(x)
\\]

is exact when \\(a\_0(x) - a\_1'(x) + a\_2''(x) - \ldots + (-1)^na\_n^{(n)}(x) = 0\\). The lower order ODE with coefficients to be determined can be solved for by differentiating, comparing coefficents and then be integrated directly.

In some cases, an integrating factor is required to turn an ODE exact.


#### Partially known complementary function {#partially-known-complementary-function}

If we wish to solve an nth-order linear ODE and we already know one part of the complementary solution \\(u(x)\\), we can make the substitution \\(y = uv\\) to transform the ODE into one of order \\(n-1\\) in \\(dv/dx\\). The simpler equation may be soluble. The solution will contain both the full complementary function.


#### Variation of parameters {#variation-of-parameters}

If the whole complementary solution of a linear ODE is known, then assume a particular integral of the same form with constants replaced by functions of x, and impose a system of LI equations for the unknowns including the ODE itself.


#### Green's functions {#green-s-functions}


#### Canonical form for second order equations {#canonical-form-for-second-order-equations}

For nth-order linear ODEs with variable coefficients to those of order 2, rearrange the equation till the coefficient of the second derivative is unity.

\\[
\dv[2]{y}{x} + a\_1(x)\dv{y}{x} + a\_0(x)y = f(x)
\\]

By making the substitution \\(y = uv\\), where

\\[
u(x) = \exp\left\\{-\frac12 \int a\_1(z) \dd{z}\right\\}
\\]
we obtain an equation of the form:

\\[
\dv[2]{v}{x} + g(x)v = h(x)
\\]

where:
\\[
g(x) = a\_0(x) - \frac14[a\_1(x)]^2 - \frac12 a\_1'(x)
\\]

\\[
h(x) = f(x)\exp\left\\{\frac12 \int a\_1(z) \dd{z}\right\\}
\\]

Which may be easier to solve.


### General ordinary differential equations {#general-ordinary-differential-equations}


#### Dependent variable absent {#dependent-variable-absent}

Substitute \\(p = \dv{y}{x}\\).

Can be extended to absence of lower derivatives.


## Series solutions of ODEs {#series-solutions-of-odes}


### Second-order linear ODE {#second-order-linear-ode}

A homogenous 2nd order linear ODE can be written

\\[
y'' + p(x)y' + q(x) = 0
\\]

The general form of the solution is:

\\[
y\_h(x) = c\_1y\_1(x) + c\_2y\_2(x)
\\]

If the wronskian W(x) does not vanish in a given interval, then the two solutions are linearly independent.

\\[
W(x) = \mqty| y\_1 && y\_2 \\\ y'\_1 && y\_2' \\\| = C\exp\left\\{-\int^x p(u) \dd{u} \right\\}
\\]

If p and q can be expressed as a complex power series at a certain point, then they are **analytic** at that point. If they diverge at a point, then that is a **singular point** of the ODE.

Even if an ODE is singular at a point, it may have a non-singular finite solution iff \\((z-z\_0)p(z)\\) and \\((z-z\_0)^2q(z)\\) are both analytic at \\(z=z\_0\\). These are called **regular singular points**. A point which does not satisfy both criteria is called an **irregular** or **essential singularity**.

To test for singularity at infinity, sub \\(w = 1/z\\) and set \\(w = 0\\).


### Solution about regular singular points {#solution-about-regular-singular-points}

**Fuch's Theorem**

For an equation of the above form, there exists at least one solution of the form:

\\[
y = z^\sigma \sum\_{n=0}^\infty a\_nz^n
\\]

where \\(\sigma\\) may be complex and where \\(a\_0 \neq 0\\). The series is called a **Frobenius series**.

By subbing and obtaining a indical equation in \\(\sigma\\), if the two roots of \\(\sigma\\) don't differ by a real integer, then two independent solutions are expected. If they do, then only the larger root is expected to give a solution.


### Finding a second solution {#finding-a-second-solution}


#### Wronskian method {#wronskian-method}

\\[
y\_2(z) = y\_1(z) \int^z \frac{1}{y\_1^2(u)} \exp\left\\{ -\int^u p(v)\dd{v} \right\\} \dd{u}
\\]


#### Derivative method {#derivative-method}

Who cares


## Eigenfunction methods for differential equations {#eigenfunction-methods-for-differential-equations}

\\[
\mathcal{L} y(x) = f(x)
\\]


### Sturm-Liouville equations {#sturm-liouville-equations}

\\[
p(x) \dv[2]{y}{x} + r(x) \dv{y}{x} + q(x) y + \lambda \rho(x) y = 0
\\]

where \\(r(x) = \dv{p(x)}{x}\\), and the weightfunction \\(\rho\\) must be finite and not change sign in the natural interval.

SL equations can be written in the forms,

\\[
\mathcal{L}y=\lambda\rho(x)y
\\]

\\[
(py')' + qy + \lambda\rho y=0
\\]

The SL operator is thus,

\\[
\mathcal{L}\equiv -\left[\dv{}{x}\left(p(x)\dv{}{x}\right)+q(x)\right]
\\]

The operator is self-adjoint and hermitian given that any two eigenfunctions \\(y\_i,y\_j\\) satisfy,

\\[
[y\_i^\* p y\_j']\_{x=a}^{x=b} = 0
\\]

Even when \\(p'\neq r\\), a 2nd-order DE can be converted into SL-form by multiplying through by,

\\[
F(x) = \exp\left\\{\int^x \frac{r(u)-p'(u)}{p(u)}\right\\}
\\]

To solve equations of the form,

\\[
\mathcal{L} y(x) = f(x)
\\]

we may expand out y in terms of eigenfunctions and eventually get,

\\[
y(x) = \int\_a^b \left\\{ \sum\_{n=0}^\infty \frac{1}{\lambda\_n}\hat{y}\_n(x)\hat{y}^\*\_n(z)\right\\} f(z)\dd{z}
\\]

Where the quantity in braces is **Green's function**, \\(G(x,z)\\).

In general to solve a DE \\(\mathcal{L}y = f(x)\\),

1.  Find the solution to \\(\mathcal{L}y = \lambda y\\) to find the eigenfunctions.
2.  Sub in boundary conditions
3.  Normalize the eigenfunctions
4.  Find the Green's function
5.  Integrate with f and get solution