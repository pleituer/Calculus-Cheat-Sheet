# Calculus-Cheat-Sheet (Unfinished)
## Table of contents

1. [Limits](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#1-limits)

2. [Deritatives](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#2-deritatives)

3. [Integration](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#3-integration)

    3.1 [Basics](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#basics)
    
    3.2 [Techniques](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#32-techniques)

4. [Differential equations:](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#4-differential-equations)

    4.1 [Seperable](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#41-seperable)
    
    4.2 [First order ODE](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#42-first-order-ode)
    
    4.3 [Bernoulli's Equation](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#43-bernoullis-equation)

    4.4 [Homogeneous Equations](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#44-homogeneous-equations)





## 1. Limits

### 1.1.1 Limit of Function

### 1.1.2 Limit Laws

## 2. Deritatives

## 3. Integration

### 3.1 Basics

### 3.2 Techniques

### 3.2.1 Direct

Here are some of the ones that can be intergrated directly

|Function|Antideritative|
|-|-|
|$x^n$|$\frac{x^{n+1}}{n+1}$|
|$e^x$|$e^x$|
|$\sin{x}$|$-\cos{x}$|
|$\cos{x}$|$\sin{x}$|
|$\sec^2{x}$|$\tan{x}$|
|$\csc^2{x}$|$-\cot{x}$|
|$\sinh{x}$|$\cosh{x}$|
|$\cosh{x}$|$\sinh{x}$|
|$\text{sech}^2{x}$|$\tanh{x}$|
|$\text{csch}^2{x}$|$-\coth{x}$|
|$\frac{\sin{x}}{x}$|$\text{Si }{x}$|
|$\frac{1}{\log{x}}$|$\text{Li }{x}$|

#### 3.2.2 Reverse Chain Rule (u-sub)

#### 3.2.3 Integration by Parts (by parts)

### 3.3 Advanced Techniques

#### 3.3.1 Dummy Variables

#### 3.3.2 Partial Fractions

## 4. Differential Equations

### 4.1 Seperable
It looks as follows:

$\frac{dy}{dx} = p(x)q(y)$

As the name suggests, we can 'seperate' x and y and transform it into $\frac{1}{q(y)}dy = p(x)dx$

Which we can easily solve by intergrating both sides and rearraging $\int_{}{}\frac{1}{q(y)}dy = \int_{}{}p(x)dx$

This can also be extended to higher order.

E.g.

$\frac{dy}{dx} = y^2\sec^2{x}$

$y^{-2}dy = \sec^2{x}dx$

$\text{Integrate both sides: } \int_{}{}y^{-2}dy = \int_{}{}\sec^2{x}dx$

$-y^{-1} = \tan{x} + C$

|$y = -\frac{1}{\tan{x} + C}$|
|-|

### 4.2 First Order ODE
It looks as follows:

$\frac{dy}{dx} + p(x)y = q(x)$

The key to solving this type of equation is to use the product rule $(fg)' = f'g + fg'$

We can multiply both sides by an **Intergrating Factor**: $I = \int_{}{}p(x)dx$. This uses the fact that $\frac{d}{dx}e^{f(x)} = \frac{df}{dx}(x)e^x$ and $\frac{d}{dx}\int_{}{}f(x)dx = f(x)$, the fundamental theorem of calculus.

Using the Intergrating Factor, we can simplify both sides down to $\frac{d}{dx}(Iy) = Iq$

Now this question became a Seperable ODE, and we can get: $y = \frac{1}{I}\int_{}{}Iqdx$

E.g.

$\frac{1}{y}\frac{dy}{dx} + \frac{1}{x} = \frac{x}{y}$

$\frac{dy}{dx} + \frac{y}{x} = x$

$\text{The Integrating factor } I = e^{\int_{}{}\frac{dx}{x}} = x$

$\text{Multiply both sides by } I \text{, the original equation becomes } \frac{d}{dx}(xy) = x^2$

$d(xy) = x^2dx$

$\int_{}{}d(xy) = \int_{}{}x^2dx$

$xy = \frac{x^3}{3} + C$

|$\text{Thus, } y = \frac{x^2}{3} + \frac{C}{x}$|
|-|

### 4.3 Bernoulli's equation

It is a special case of the First Order ODE: $\frac{dy}{dx} + p(x)y = q(x)y^n$

Step 1: 

To solve it, we can just do u-sub, $u = y^{1-n} \to du = (1-n)y^{-n}dy \to dy = \frac{y^n}{1-n}du$.

Step 2:

If we subsitute it to the original equation, it will become $\frac{y^n}{1-n}\frac{du}{dx} + p(x)y = q(x)y^n \to \frac{du}{dx} + (1-n)p(x)*y^{1-n} = (1-n)q(x)$.

Step 3:

Note that $y^{1-n}$ is equivalent to $u$, so the equation becomes $\frac{du}{dx} + (1-n)p(x)u = (1-n)q(x)$.

Finally

Then we just need to treat it as a first order ODE, just don't forget to change it back to $y$ at last.

E.g.

$\sqrt{y}\cos{x}\frac{dy}{dx} + \sqrt{y^3}(\csc{x} - \sin{x}) = \tan{x}$

$\frac{dy}{dx} + y\cot{x} = \frac{1}{\sqrt{y}}\frac{\sin{x}}{\cos^2{x}}$

$\text{We let } u = \sqrt{y^3} \to du = \frac{3}{2}\sqrt{y}dy \to dy = \frac{2}{3\sqrt{y}}du$

$\text{Subsitute into the original equation } \frac{2}{3\sqrt{y}}\frac{du}{dx} + y\cot{x} = \frac{1}{\sqrt{y}}\frac{\sin{x}}{\cos^2{x}}$

$\frac{dy}{dx} + \frac{3}{2}\sqrt{y^3}\cot{x} = \frac{3\sin{x}}{2\cos^2{x}}$

$\frac{dy}{dx} + \frac{3}{2}u\cot{x} = \frac{3\sin{x}}{2\cos^2{x}}$

$\text{Let the Intergrating factor } I = e^{\frac{3}{2}\int_{}{}\cot{x}dx} = \sqrt{e^3}\sin{x}$

$\text{Multiply boths sides by } I \to \frac{d}{dx}(\sqrt{e^3}u\sin{x}) = \frac{3\sqrt{e^3}}{2}\tan^2{x} = \frac{3\sqrt{e^3}}{2}\sec^2{x} - \frac{3\sqrt{e^3}}{2}$

$\int_{}{}d(\sqrt{e^3}u\sin{x}) = \int_{}{}(\frac{3\sqrt{e^3}}{2}\sec^2{x} - \frac{3\sqrt{e^3}}{2})dx$

$\sqrt{e^3}u\sin{x} = \frac{3\sqrt{e^3}}{2}\tan{x} - \frac{3\sqrt{e^3}x}{2} + C$

$u = \frac{3}{2\cos{x}} - \frac{3x + C}{2\sin{x}}$

$y = \sqrt[3]{u^2}$

|$y = \sqrt[3]{(\frac{3}{2\cos{x}} - \frac{3x + C}{2\sin{x}})^2}$|
|-|

### 4.4 Homogeneous Equations

If a function $g(x,y)$ is homogeneous of degree $n$ $\to g(kx,ky) = k^ng(x,y)$

E.g.

$x^2+3xy+y^2$ is homogeneous of degree 2

Now, the Homogeneous equations look like $\frac{dy}{dx} = \frac{f(x,y)}{g(x,y)}$, where $f,g$ are homogeneous and have the same degree

It can be solved by the subsitution $u = \frac{y}{x}$

E.g.

$\frac{dy}{dx} = \frac{x^2+3xy+y^2}{x^2}$

$\text{Let } u = y/x \to y = ux \to dy = xdu + udx$

$\text{Also, } \frac{x^2+3xy+y^2}{x^2} = 1+\frac{3y}{x}+(\frac{y}{x})^2 = 1 + 3u + u^2$

$\text{Substitute it into the original equation: } x\frac{du}{dx} + u = u^2 + 3u + 1 \to \frac{du}{dx} = \frac{(u+1)^2}{x}$

$\text{Now this is just a seperable ODE } \frac{du}{(u+1)^2} = \frac{dx}{x}$

$\int_{}{}\frac{du}{(u+1)^2} = \int_{}{}\frac{dx}{x}$

$-\frac{1}{u+1} = \ln{|x|} + C$

$u = -\frac{1}{\ln{|x|} + C} - 1$

$\text{Change it back to } y$

|$y = -\frac{1}{x\ln{\|x\|} + Cx} - \frac{1}{x}$|
|-|

### 4.5 Exact Equations

It has the form of $M(x,y)dx + N(x,y)dy = 0$

If there exists a function $F(x,y)$ such that $\frac{\partial F}{\partial x} = M$ and $\frac{\partial F}{\partial y} = N$, then the equation simplifies to $\partial F = 0 \to F = C$, where $C$ is a constant.

Since $\frac{\partial F}{\partial x} = M$, which means $F = \int_{}{}Mdx + C_y$ Where $C_y$ is an arbitary function of $y$ only.

Similarly, $\frac{\partial F}{\partial y} = N \to F = \int_{}{}Ndy + C_x$ Where $C_x$ is an arbitary function of $x$ only.

This mean $\int_{}{}Mdx + C_y = \int_{}{}Ndy + C_x \to \frac{\partial^2}{\partial x \partial y}(\int_{}{}Mdx + C_y) = \frac{\partial^2}{\partial x\partial y}(\int_{}{}Ndy + C_x) \to \frac{\partial M}{\partial y} = \frac{\partial N}{\partial x}$ 

Now, if the solution exists, $F = \int_{}{}Mdx + C_y$, and we can subitute it into $\frac{\partial F}{\partial y} = N$ to find $C_y$ and thus $F$.

Lastly, the solution will then be $F(x,y) = C$

E.g.

$(x\sin{y} - y^2)\frac{dy}{dx} = \cos{y}$

$M = \cos{y} \text{  } (1)$

$N = y^2 - x\sin{y} \text{  } (2)$

$(1) \to \frac{\partial M}{\partial y} = -\sin{y}$

$(2) \to \frac{\partial N}{\partial x} = -\sin{x} = \frac{\partial M}{\partial y}$

$\text{Thus, a solution } F(x,y) \text{ exists}$

$\frac{\partial F}{\partial x} = M \to F = \int_{}{}Mdx + C_y = \int_{}{}\cos{y}dx + C_y = x\sin{y} + C_y \text{  } (3)$

$\text{Sub } (3) \text{ to } \frac{\partial F}{\partial y} = N \to \cos{y}x + \frac{\partial}{\partial y}C_y = y^2 - x\sin{y} \to C_y = \int_{}{}y^2 - x(\cos{y} + \sin{y})dy = \frac{y^3}{3} - x(\sin{x} - \cos{y})$

$\text{Thus, } F(x,y) = x\cos{y} + \frac{y^3}{3} = C$

$\text{The solution for this equation is: }$
|$x\cos{y} + \frac{y^3}{3} = C$|
|-|































