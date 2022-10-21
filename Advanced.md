# Advanced

Table of contents

1. [Advanced Integration Techniques](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/Advanced.md#advanced-integration-techniques)

2. [Advanced Differential Equations](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/Advanced.md#advanced-differential-equations)

## Advanced Integration Techniques

## Advanced Differential Equations

### 2.1 Second order Linear ODE with constant coefficients (not just 2 degrees, even more!)

First, We need to understand about **Linear Independence**

Linear Independence means that 2 functions, $f(x)$ and $g(x)$ are **NOT** linearly related, that is you cannot find a value $k$ such that $f(x) = kg(x)$, so $\sin{x}$ and $4\sin{x}$ are linearly **Dependent**, while $\sin{x}$ and $\sin{4x}$ are linearly **Independent**

Now we introduce the concept of Wronskain, $W(f_1,f_2,...f_n)(x) = \left| \matrix{f_1 & f_2 & \cdots & f_n \cr f_1' & f_2' & \cdots & f_n' \cr \vdots & \vdots & \ddots & \vdots \cr f_1^{(n-1)} & f_2^{(n-1)} & \cdots & f_n^{(n-1)}}\right|$, if $W$ is **generally** nonzero then $f_1$, $f_2$ ,..., $f_n$ are linearly independent

Since if $f_1$, $f_2$,..., $f_n$ are linearly dependent, then $W = \left| \matrix{v & i_1v & \cdots & i_{n-1}v} \right|$ Where $v = \left( \matrix{ f_1 \cr f_1' \cr \vdots \cr f_1^{(n-1)}} \right)$ 

Using the [properties of the determinant](https://en.wikipedia.org/wiki/Determinant#Properties_of_the_determinant), we can get $W = \frac{1}{i_1} \left| \matrix{i_1v & i_1v & \cdots & i_{n-1}v} \right| \implies W = \frac{1}{i_1} \times 0 = 0$

So, $f_1$, $f_2$,..., $f_n$ are linearly dependent $\Longleftrightarrow W = 0$ 

Now, to solve the differential equation, we employ 2 facts:

1. $\frac{d}{dx}e^{ax} = ae^{ax}$

2. Given that $y_1$ and $y_2$ are solutions to $D(y) = 0$ and $D(y) = f(x)$ respectively, then $y = y_1 + y_2$ is also a solution to $D(y) = f(x)$. Since $D(y)$ is linear $\to D(y) = D(y_1 + y_2) = D(y_1) + D(y_2) = 0 + f(x) = f(x) \to D(y) = f(x)$

Thus, we can let $u = Ce^{\lambda x}$ (Complementary function) to be the solution to $D(y) = 0 \to (a\lambda^2 + b\lambda + c)u = 0$, where $C$ is a constant. Since $u$ cannot be $0$ at every point, we can divide $u$ on both sides and we get $a\lambda^2 + b\lambda + c = 0$. Solving $\lambda$ we can get two $\lambda$ s, $\lambda_1$ and $\lambda_2$, which we can seperate it into different cases

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

However it is not done yet!

We only found solutions to $D(y) = 0$, but we want to find $D(y) = f(x)$, to do that, we need to find the particular integral, and we will split it into different cases based of the deritative of $f(x)$

Case 1:
$f(x) = p(x)$ where $p(x)$ is a polynomial with degree $i$ (Fun fact: there will be multiple solutions if $i>n$ where n is the degree of the linear ode)

We let $p_i(x) = \Sigma_ia_ix^i$, now solve for each $a_i$ ( $p_i$ is the particular integral)

$\text{}$

Case 2:
$f(x) = t(x)$ where $t(x)$ is a sum of $\sin{}$ and $\cos{}$

We let $p_i(x) = \Sigma_i(a_i\cos{b_ix} + c_i\sin{b_ix})$ where $b_i$ is deduced through the equation ( $f(x) = \cos{3x} \to p_i(x) = A\cos{3x} + B\sin{3x}$ ). Now, solve for each $a_i$ and $c_i$

**ALERT:** If $A\cos{bx} + B\sin{bx}$ is a solution ( $e^{ax}$ not included ), you will need $Ax\cos{bx} + Bx\sin{bx}$ (Think why?)

$\text{}$

Case 3:
$f(x) = Ce^{ax}$

We let $p_i(x) = Ae^{ax}$, where $a$ is deduced through the equation ( $f(x) = 2e^{3x}\to p_i(x) = Ae^{3x}$ ). Now, solve for $A$

**ALERT:** If $Ae^{ax}$ is a solution, you will need $Axe^{ax}$, but if $Ae^{ax}$ is a repeated solution to the equation, you will need $Ax^2e^{ax}$ (Think why?)

$\text{}$

Case 4:
$f(x) = h_t(x)$ where $h_t(x)$ is a sum of $\sinh{}$ and $\cosh{}$

We let $p_i(x) = \Sigma_i(a_i\cosh{b_ix} + c_i\sinh{b_ix})$ where $b_i$ is deduced through the equation ( $f(x) = \cosh{3x} \to p_i(x) = A\cosh{3x} + B\sinh{3x}$ ). Now, solve for each $a_i$ and $c_i$

**ALERT:** If $A\cosh{bx} + B\sinh{bx}$ is a solution ( Since $\cosh{x} = \frac{e^x+e^{-x}}{2}$ and $\sinh{x} = \frac{e^x-e^{-x}}{2}$ ), you will need $Ax\cosh{bx} + Bx\sinh{bx}$ (Think why?)

$\text{}$

E.g.

$y'' + 2y' + y = \frac{1}{e^x} + \sin{4x}$

$\text{Let } y_c \text{ be the Complementary function, since the Charateristic equations is } m^2 + 2m + 1 = 0 \to m = -1 \to y_c = C_1e^{-x} + C_2xe^{-x}$

$\text{Now, let the particular integral be } y_p = Ax^2e^{-x} + B\sin{4x} + C\cos{4x}$

$\text{Substituting it into the orignial equation gives }$

$(2Ae^{-x} - 4Axe^{-x} + Ax^2e^{-x} - 16B\sin{4x} - 16C\cos{4x}) + 2(2Axe^{-x} - Ax^2e^{-x} + 4B\cos{4x} - 4C\sin{4x}) + (Ax^2e^{-x} + B\sin{4x} + C\cos{4x}) = e^{-x} + \sin{4x}$

$\text{Thus, } \left\lbrace \matrix{2A = 1 \text{  } (1) \cr -4A + 4A = 0 \text{  } (2) \cr A - 2A + A = 0 \text{  } (3) \cr -16B - 8C + B = 1 \text{  } (4) \cr -16C + 8B + C = 0 \text{  }(5)} \right.$

$\left\lbrace \matrix{(1) \to A = \frac{1}{2} \cr (5) \to C = \frac{8}{15}B \text{  } (6)} \right.$

$(6) \text{ sub into } (4) \to B = -\frac{15}{289} \to C = -\frac{8}{289}$

$\text{Thus, } y_p = \frac{1}{2}x^2e^{-x} - \frac{15}{289}\sin{4x} - \frac{8}{289}\cos{4x}$

$y = y_c + y_p$ = 
|$C_1e^{-x} + C_2xe^{-x} + \frac{1}{2}x^2e^{-x} - \frac{15}{289}\sin{4x} - \frac{8}{289}\cos{4x}$|
|-|


### Variation of Parameters

Consider the following equation: $y''+p(x)y'+q(x)y=f(x)$

We can solve it by solving for the homogeneous part then the non homogeneous part (We're not going to talk about how to solve it for now). Assuming the two **Linearly Independent** solutions $u_1$ and $u_2$ are solved, then we can solve for the non homogeneous part:

Step 1:
We let the general solution $u_g$ be $A(x)u_1 + B(x)u_2$, with 2 unknown functions, it is not possible to solve for $A$ and $B$, thus we impose $A'(x)u_1 + B'(x)u_2 = 0$

Step 2:
We can find $u_g'$ and $u_g''$, then plug it into the original equation: $Au_1''+Bu_2''+A'u_1'+B'u_2'+pAu_1'+pBu_2'+qAu_1+qBu_2=f \to A(u_1''+pu_1'+qu_1)+B(u_2''+pu_2'+qu_2)+A'u_1'+B'u_2'=f \to A'u_1'+B'u_2'=f$

Step 3:
Now put everything together: $\left\lbrace \matrix{A'u_1+B'u_2=0 \cr A'u_1'+B'u_2'=f} \right. \to \left\lbrack \matrix{u_1 & u_2 \cr u_1' & u_2'} \right\rbrack \left\lbrack \matrix{A'\cr B'} \right\rbrack = \left\lbrack \matrix{0\cr f} \right\rbrack$

Step 4:
Thus, $\left\lbrack \matrix{A\cr B} \right\rbrack = \int \left\lbrack \matrix{u_1 & u_2 \cr u_1' & u_2'} \right\rbrack ^{-1} \left\lbrack \matrix{0\cr f} \right\rbrack  dx$

Now, we can get $u_g$ and thus our final answer $y = u_g + C_1u_1 + C_2u_2$
