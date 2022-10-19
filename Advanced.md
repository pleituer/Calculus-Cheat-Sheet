# Advanced

Table of contents

1. [Advanced Integration Techniques](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/Advanced.md#advanced-integration-techniques)

2. [Advanced Differential Equations](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/Advanced.md#advanced-differential-equations)

## Advanced Integration Techniques

## Advanced Differential Equations

### 2.1 Second order Linear ODE with constant coefficients

First, We need to understand about **Linear Independence**

Linear Independence means that 2 functions, $f(x)$ and $g(x)$ are **NOT** linearly related, that is you cannot find a value $k$ such that $f(x) = kg(x)$, so $\sin{x}$ and $4\sin{x}$ are linearly **Dependent**, while $\sin{x}$ and $\sin{4x}$ are linearly **Independent**

Now we introduce the concept of Wronskain, $W(f_1,f_2,...f_n)(x) = \left| \matrix{f_1 & f_2 & \cdots & f_n \cr f_1' & f_2' & \cdots & f_n' \cr \vdots & \vdots & \ddots & \vdots \cr f_1^{(n-1)} & f_2^{(n-1)} & \cdots & f_n^{(n-1)}}\right|$, if $W$ is **generally** nonzero then $f_1$, $f_2$ ,..., $f_n$ are linearly independent

Since if $f_1$, $f_2$,..., $f_n$ are linearly dependent, then $W = f \left| \matrix{i_1 & i_2 & \cdots &i_n \cr i_1\alpha & i_2\alpha & \cdots & i_n\alpha \cr \vdots & \vdots & \ddots & \vdots \cr i_1\alpha ^{n-1} & i_2\alpha ^{n-1} & \cdots & i_n\alpha ^{n-1}}\right|$ Where $f = \frac{f_1}{i_1} = \frac{f_2}{i_2} = \cdots = \frac{f_n}{i_n}$ for some number $i$ and $f' = \alpha f$ for some function $\alpha$

To solve this, we employ 2 facts:

1. $\frac{d}{dx}e^{ax} = ae^{ax}$

2. Given that $y_1$ and $y_2$ are solutions to $D(y) = 0$ and $D(y) = f(x)$ respectively, then $y = y_1 + y_2$ is also a solution to $D(y) = f(x)$. Since $D(y)$ is linear $\to D(y) = D(y_1 + y_2) = D(y_1) + D(y_2) = 0 + f(x) = f(x) \to D(y) = f(x)$

Thus, we can let $u = Ce^{\lambda x}$ to be the solution to $D(y) = 0 \to (a\lambda^2 + b\lambda + c)u = 0$, where $C$ is a constant. Since $u$ cannot be $0$ at every point, we can divide $u$ on both sides and we get $a\lambda^2 + b\lambda + c = 0$. Solving $\lambda$ we can get two $\lambda$ s, $\lambda_1$ and $\lambda_2$, which we can seperate it into different cases

Case 1:
$\lambda_1$ and $\lambda_2$ are real and different:

We can do $u = C_1e^{\lambda_1 x} + C_2e^{\lambda_2 x}$

Case 2:
$\lambda_1$ and $\lambda_2$ are complex and different:

Same thing, we can do $u = C_1e^{\lambda_1 x} + C_2e^{\lambda_2 x}$. But since both $\lambda$ are complex, we can let $\lambda_1 = a + bi \to \lambda_2 = a - bi$. Thus, using $e^{ix} = \cos{x} + i\sin{x}$, we get $u = C_1e^{ax}(\cos{bx}+i\sin{bx}) + C_2e^{ax}(\cos{bx}-i\sin{bx}) = e^{ax}((C_1+C_2)\cos{bx}+(C_1-C_2)i\sin{bx}) = e^{ax}(A\cos{bx} + B\sin{bx})$, where $A = C_1+C_2$ and $B = (C_1-C_2)i$ 

Note that both of these contants are complex, since we introducted the concept of complex numbers, $A, B, C_1, C_2$ are complex numbers

Case 3:
$\lambda_1$ and $\lambda_2$ are the same

Since $\lambda_1 = \lambda_2$, we can easily derive that they are $-\frac{b}{2}$we can use the method of reduction, just like in polynomials. If $y = y_1 = C_1e^{-\frac{bx}{2a}}$ is a solution to the equation $D(y) = 0$, then we can find the other solution like so:

$\text{Let } u \text{ be the other solution, since } y_1 \text{ is a solution, then by the method of reduction, } y_2 = y_1u \to y_2' = y_1'u + y_1u' \to y_2'' = y_1''u + 2y_1'u' + y_1u''$ So, $(y_1''u + 2y_1'u' +y_1u'') + \frac{b}{a}(y_1'u + u'y_1) + \frac{c}{a}(y_1u)$ Meaning, $y_1u'' + u'(2y_1'+\frac{b}{a}y_1) + u(y_1''+\frac{b}{a}y_1'+\frac{c}{a}y_1)$ Thus, $u''= 0 \to u = C_2x \to y_2 = C_2xe^{-\frac{bx}{2a}} \to y = C_1e^{-\frac{bx}{2a}} + C_2xe^{-\frac{bx}{2a}}$ 
