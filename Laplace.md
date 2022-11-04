# Laplace Transforms

Table of Contents

1. Definition

2. Tables


## 1. Definition

$\mathscr{L}\lbrace f \rbrace = \int$

## 2. Table
|$f(t)$|$\mathscr{L}\lbrace f \rbrace = F(s)$|$\mathscr{L}^{-1}  \lbrace f \rbrace$|
|-|-|-|
|$1$|$\frac{1}{s}$|$u(t)$|
|$e^{ax}$|$\frac{1}{s+a}$|$e^{-at}u(t)$|
|$\sin{ax}$|$\frac{a}{s^2+a^2}$|$u(t)\sin{at}$|
|$\cos{ax}$|$\frac{s}{s^2+a^2}$|$u(t)\cos{at}$|
|$x^n$|$\frac{n!}{s^{n+1}}$|$u(t)t^n$|
|$x^c$ (complex c)|$\frac{\Gamma(c+1)}{s^{c+1}}$|$u(t)t^c$|
|$\sinh{ax}$|$\frac{a}{s^2-a^2}$|$u(t)\sinh{at}$|
|$\cosh{ax}$|$\frac{s}{s^2-a^2}$|$u(t)\cosh{at}$|
|$\ln{x}$|$-\frac{1}{s}\lvert {\ln{s} + \gamma}\rvert$|$u(t)\ln{t}$|
