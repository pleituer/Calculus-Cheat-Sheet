# Calculus-Cheat-Sheet
## Table of contents

1. [Limits](https://github.com/pleituer/Calculus-Cheat-Sheet/edit/main/README.md#1-limits)

2. [Deritatives](https://github.com/pleituer/Calculus-Cheat-Sheet/edit/main/README.md#2-deritatives)

3. [Integration](https://github.com/pleituer/Calculus-Cheat-Sheet/edit/main/README.md#3-integration)

4. [Differential equations:](https://github.com/pleituer/Calculus-Cheat-Sheet/edit/main/README.md#4-differential-equations)

    4.1 [Seperable](https://github.com/pleituer/Calculus-Cheat-Sheet/edit/main/README.md#41-seperable)
    
    4.2 [First order ODE](https://github.com/pleituer/Calculus-Cheat-Sheet/edit/main/README.md#42-first-order-ode)
    
    4.3 [Bernoulli's Equation](https://github.com/pleituer/Calculus-Cheat-Sheet/edit/main/README.md#43-bernoullis-equation)





## 1. Limits

## 2. Deritatives

## 3. Integration

## 4. Differential Equations

### 4.1 Seperable
It looks as follows:

$\frac{dy}{dx} = p(x)q(y)$

As the name suggests, we can 'seperate' the equations and transform it into $\frac{1}{q(y)}dy = p(x)dx$

Which we can easily solve by intergrating both sides and rearraging $\int_{}{}\frac{1}{q(y)}dy = \int_{}{}p(x)dx$

This can alsp be extended to higher order.

### 4.2 First Order ODE
It looks as follows:

$\frac{dy}{dx} + p(x)y = q(x)$

The key to solving this type of equation is to use the product rule $(fg)' = f'g + fg'$

We can multiply both sides by an **Intergrating Factor**: $I = \int_{}{}p(x)dx$. This uses the fact that $\frac{d}{dx}e^{f(x)} = \frac{df}{dx}(x)e^x$ and $\frac{d}{dx}\int_{}{}f(x)dx = f(x)$, the fundamental theorem of calculus.

Using the Intergrating Factor, we can simplify both sides down to $\frac{d}{dx}(Iy) = Iq$

Now this question became a Seperable ODE, and we can get: $y = \frac{1}{I}\int_{}{}Iqdx$

### 4.3 Bernoulli's equation

It is a special case of the First Order ODE: $\frac{dy}{dx} + p(x)y = q(x)y^n$

Step 1: 

To solve it, we can just do u-sub, $u = y^{1-n} \to \frac{du}{dy} = (1-n)y^{-n}$, since $\frac{du}{dy} = \frac{\frac{du}{dx}}{\frac{dy}{dx}}$, $\frac{du}{dx} = (1-n)y^{-n}\frac{dy}{dx} \to \frac{dy}{dx} = \frac{y^n}{1-n}\frac{du}{dx}$.

Step 2:

If we subsitute it to the original equation, it will become $\frac{y^n}{1-n}\frac{du}{dx} + p(x)y = q(x)y^n \to \frac{du}{dx} + p(x) * (1-n)y^{1-n} = (1-n)q(x)$.

Step 3:

Note that $(1-n)y^{1-n}$ is equivalent to $u$, so the equation becomes $\frac{du}{dx} + p(x)u = (1-n)q(x)$.

Finally

Then we just need to treat it as a first order ODE, just don't forget to change it back to $y$ at last.







