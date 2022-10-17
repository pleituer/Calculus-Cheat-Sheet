# Calculus-Cheat-Sheet
## Table of contents

1. [Limits](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#1-limits)

2. [Deritatives](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#2-deritatives)

3. [Integration](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#3-integration)

    3.1 [Types](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#types)
    
    3.2 [Techniques](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#32-techniques)

4. [Differential equations:](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#4-differential-equations)

    4.1 [Seperable](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#41-seperable)
    
    4.2 [First order ODE](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#42-first-order-ode)
    
    4.3 [Bernoulli's Equation](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#43-bernoullis-equation)





## 1. Limits

## 2. Deritatives

## 3. Integration

### 3.1 Types

Indefinite: $\int_{}{}f(x)dx$

Definite: $\int_{a}^{b}f(x)dx$

### 3.2 Techniques

### 3.2.1 Direct

Here are some of the ones that can be intergrated directly

|Function|Antideritative|
|-|-|
|$x^n$|$\frac{x^{n+1}}{n+1}$|
|$e^x$|$e^x$|
|$\sin{x}$|$-\cos{x}$|
|$\cos{x}$|$\sin{x}$|
|$$|$$|

#### 3.2.2 Reverse Chain Rule (u-sub)

#### 3.2.3 Technique 3: Integration by Parts (by parts)

### 3.3 Advanced Techniques

#### 3.3.1 Dummy Variables

## 4. Differential Equations

### 4.1 Seperable
It looks as follows:

$\frac{dy}{dx} = p(x)q(y)$

As the name suggests, we can 'seperate' the equations and transform it into $\frac{1}{q(y)}dy = p(x)dx$

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











