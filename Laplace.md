# Laplace Transforms

## Table of Contents

1. [Definitions](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/Laplace.md#1-definitions)

2. [Tables](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/Laplace.md#2-tables)

    2.1 [Why](https://github.com/pleituer/Calculus-Cheat-Sheet/blob/main/README.md#21-why)

## 1. Definitions

Laplace Transform: $\mathscr{L}\lbrace f(t) \rbrace = F(s) = \int_0^\infty f(t)e^{-st}dt$

Convolution: $f(t) * g(t) = \int_0^t f(t-v)g(v)dv$

## 2. Tables
|$f(t)$|$\mathscr{L}\lbrace f \rbrace = F(s)$|$\mathscr{L}^{-1}  \lbrace f \rbrace$|
|-|-|-|
|$1$|$\frac{1}{s}$|$u(t)$|
|$e^{at}$|$\frac{1}{s-a}$|$e^{-at}u(t)$|
|$\sin{at}$|$\frac{a}{s^2+a^2}$|$u(t)\sin{at}$|
|$\cos{at}$|$\frac{s}{s^2+a^2}$|$u(t)\cos{at}$|
|$t^n$|$\frac{n!}{s^{n+1}}$|$u(t)t^n$|
|$t^c$ (complex c)|$\frac{\Gamma(c+1)}{s^{c+1}}$|$u(t)t^c$|
|$\sinh{at}$|$\frac{a}{s^2-a^2}$|$u(t)\sinh{at}$|
|$\cosh{at}$|$\frac{s}{s^2-a^2}$|$u(t)\cosh{at}$|
|$\ln{t}$|$-\frac{1}{s}\lvert {\ln{s} + \gamma}\rvert$|$u(t)\ln{t}$|

### 2.1 Why

1. $\mathscr{L}\lbrace e^{at} \rbrace$

   $= \int_0^\infty e^{-(s-a)t}dt$
   
   $= \lbrack -\frac{e^{-(s-a)t}}{s-a} \rbrack |_ 0^\infty$
   
   $= \frac{1}{s-a}$
 
2. $\mathscr{L}\lbrace t^c \rbrace$

   $= \int_0^\infty t^ce^{-st}dt$ Note that $\Gamma(n+1)$ is defined as $\int_0^\infty t^ne^{-t}dt$
   
   $= \frac{1}{s^c}\int_0^\infty (st)^ce^{-st}dt$ Letting $u = st \to du = sdt$
   
   $= \frac{1}{s^{c+1}}\int_0^\infty u^ce^{-u}du$
   
   $= \frac{\Gamma(c+1)}{s^{c+1}}$ For natural $c$, it becomes $\frac{c!}{s^{c+1}}$

3. $\mathscr{L}\lbrace \sin{bt} \rbrace$

   $= \int_0^\infty e^{-st}\sin{bt}dt$ Note that $e^{i\theta} = \cos{\theta} + i\sin{\theta} \to \sin{\theta} = \frac{e^{i\theta} - e^{-i\theta}}{2i}$
   
   $= \frac{1}{2i}\int_0^\infty e^{(ib-s)t} - e^{(-ib-s)t}dt$
   
   $= \frac{1}{2i}\lbrack\frac{e^{(ib-s)t}}{ib-s} + \frac{e^{-(ib+s)t}}{ib+s}\rbrack |_ 0^\infty$
   
   $= -\frac{1}{2i}\lbrack\frac{e^{-st}((ib+s)(\cos{bt} + i\sin{bt}) + (ib-s)(\cos{bt} - i\sin{bt}))}{s^2 + b^2}\rbrack |_ 0^\infty$
   
   $= \frac{1}{2i(s^2 + b^2)}\lbrack e^{-st}(2ib\cos{bt} + 2si\sin{bt}) \rbrack |_ \infty^0$
   
   $= \frac{b}{s^2 + b^2}$

4. $\mathscr{L}\lbrace \cos{bt} \rbrace$

   $= \int_0^\infty e^{-st}\cos{bt}dt$ Note that $e^{i\theta} = \cos{\theta} + i\sin{\theta} \to \cos{\theta} = \frac{e^{i\theta} + e^{-i\theta}}{2}$
   
   $= \frac{1}{2}\int_0^\infty e^{(ib-s)t} + e^{(-ib-s)t}dt$
   
   $= \frac{1}{2}\lbrack\frac{e^{(ib-s)t}}{ib-s} - \frac{e^{-(ib+s)t}}{ib+s}\rbrack |_ 0^\infty$
   
   $= -\frac{1}{2}\lbrack\frac{e^{-st}((ib+s)(\cos{bt} + i\sin{bt}) - (ib-s)(\cos{bt} - i\sin{bt}))}{s^2 + b^2}\rbrack |_ 0^\infty$
   
   $= \frac{1}{2(s^2 + b^2)}\lbrack e^{-st}(2ib\sin{bt} + 2si\cos{bt}) \rbrack |_ \infty^0$
   
   $= \frac{s}{s^2 + b^2}$

5. $\mathscr{L}\lbrace \sinh{bt} \rbrace$

   $= \int_0^\infty e^{-st}\sinh{bt}dt$ Note that $\sinh{x} = \frac{e^{x} - e^{-x}}{2}$ and $e^x = \cosh{x} + \sinh{x}$
   
   $= \frac{1}{2}\int_0^\infty e^{(b-s)t} - e^{(-b-s)t}dt$
   
   $= \frac{1}{2i}\lbrack\frac{e^{(b-s)t}}{b-s} + \frac{e^{-(b+s)t}}{b+s}\rbrack |_ 0^\infty$
   
   $= -\frac{1}{2}\lbrack\frac{e^{-st}((b+s)(\cosh{bt} + \sinh{bt}) + (b-s)(\cosh{bt} - \sinh{bt}))}{s^2 - b^2}\rbrack |_ 0^\infty$
   
   $= \frac{1}{2(s^2 - b^2)}\lbrack e^{-st}(2b\cosh{bt} + 2s\sinh{bt}) \rbrack |_ \infty^0$
   
   $= \frac{b}{s^2 - b^2}$
 
6. $\mathscr{L}\lbrace \sinh{bt} \rbrace$

   $= \int_0^\infty e^{-st}\sinh{bt}dt$ Note that $\cosh{x} = \frac{e^{x} + e^{-x}}{2}$ and $e^x = \cosh{x} + \sinh{x}$
   
   $= \frac{1}{2}\int_0^\infty e^{(b-s)t} + e^{(-b-s)t}dt$
   
   $= \frac{1}{2i}\lbrack\frac{e^{(b-s)t}}{b-s} - \frac{e^{-(b+s)t}}{b+s}\rbrack |_ 0^\infty$
   
   $= -\frac{1}{2}\lbrack\frac{e^{-st}((b+s)(\cosh{bt} - \sinh{bt}) - (b-s)(\cosh{bt} - \sinh{bt}))}{s^2 - b^2}\rbrack |_ 0^\infty$
   
   $= \frac{1}{2(s^2 - b^2)}\lbrack e^{-st}(2b\sinh{bt} + 2s\cosh{bt}) \rbrack |_ \infty^0$
   
   $= \frac{s}{s^2 - b^2}$

7. $\mathscr{L} \lbrace C \rbrace$
   $= \int_0^\infty Ce^{-st}dt$
   $= \lbrack \frac{Ce^{-st}}{-s} \rbrack |_ 0^\infty$
   $= \frac{1}{s}$

8. $\mathscr{L} \lbrace u(t-a) \rbrace$ Where $u(x)$ is the unit-step function or the Heaviside function, and it is defined as $\lbrace \matrix{1 \text{ if } x > 0 \cr 0 \text{ if } x < 0}$
