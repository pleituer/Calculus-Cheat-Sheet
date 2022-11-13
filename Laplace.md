# Laplace Transforms

Table of Contents

1. Definition

2. Tables


## 1. Definition

Laplace Transform: $\mathscr{L}\lbrace f(t) \rbrace = F(s) = \int_0^\infty f(t)e^{-st}dt$

Convolution: $f(t) * g(t) = \int_0^t f(t-v)g(v)dv$

## 2. Table
|$f(t)$|$\mathscr{L}\lbrace f \rbrace = F(s)$|$\mathscr{L}^{-1}  \lbrace f \rbrace$|
|-|-|-|
|$1$|$\frac{1}{s}$|$u(t)$|
|$e^{at}$|$\frac{1}{s+a}$|$e^{-at}u(t)$|
|$\sin{at}$|$\frac{a}{s^2+a^2}$|$u(t)\sin{at}$|
|$\cos{at}$|$\frac{s}{s^2+a^2}$|$u(t)\cos{at}$|
|$t^n$|$\frac{n!}{s^{n+1}}$|$u(t)t^n$|
|$t^c$ (complex c)|$\frac{\Gamma(c+1)}{s^{c+1}}$|$u(t)t^c$|
|$\sinh{at}$|$\frac{a}{s^2-a^2}$|$u(t)\sinh{at}$|
|$\cosh{at}$|$\frac{s}{s^2-a^2}$|$u(t)\cosh{at}$|
|$\ln{t}$|$-\frac{1}{s}\lvert {\ln{s} + \gamma}\rvert$|$u(t)\ln{t}$|
