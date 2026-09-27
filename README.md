## LaTeX Lecture 1

### New, empty document

```plaintext
\documentclass{article}
\usepackage{amsmath}
\usepackage{amsthm}
\usepackage{amssymb}
\title{My First Mathematics Paper}
\author{Your Name}
\date{\today}
\begin{document}
\maketitle
\section{Introduction}
This is my first mathematical document.
\end{document}
```

### Writing math

- inline math:

```plaintext
Let $f(x) = x^2 + 1$. Then $f(x) > 0$ for every $x \in \mathbb{R}$.
```

- display math:

```plaintext
\[
f(x) = x^2 + 1.
\]
```

- equations:

```plaintext
\begin{equation}
a^2 + b^2 = c^2.
\end{equation}
```

- common syntax:

```plaintext
$x^2$ is a power of 2.

$x_i$ is a variable with a numeric index.

$\frac{a}{b}$ is a fraction.

$\sqrt{x}$ is the square root of x.

$\sum_{i=1}^n i$ is a summation.

$\int_0^1 x^2\,dx$ is an integral; the lower limit is followed by the upper limit.

$\alpha$ and $\epsilon$ are examples of greek letters.

$\infty$ is infinity.

$\mathbb{R}$ is all real numbers.
```

### Multi-line calculations with amsmath and unnumbered equations

- Example 1:

```plaintext
\begin{align}
(x+1)^2
    &= (x+1)(x+1) \\
    &= x^2 + 2x + 1.
\end{align}
```

- Example 2:

```plaintext
\begin{align*}
(x+1)^2
    &= (x+1)(x+1) \\
    &= x^2 + 2x + 1.
\end{align*}
```

### Definitions, theorems, and proofs

- Add to preamble:

```plaintext
\newtheorem{theorem}{Theorem}
\newtheorem{lemma}{Lemma}
\newtheorem{definition}{Definition}
```

- Examples:

```plaintext
\begin{definition}
An integer $n$ is even if there exists an integer $k$ such that
\[
n = 2k.
\]
\end{definition}

\begin{theorem}
The sum of two even integers is even.
\end{theorem}

\begin{proof}
Let $a$ and $b$ be even integers. Then there exist integers $m$ and $n$ such that
\[
a = 2m
\qquad\text{and}\qquad
b = 2n.
\]
Therefore,
\[
a+b = 2m+2n = 2(m+n).
\]
Since $m+n$ is an integer, $a+b$ is even.
\end{proof}
```

- To use a reference, add a label to a theorem

```plaintext
\begin{theorem}\label{thm:even-sum}
The sum of two even integers is even.
\end{theorem}
```

- Then, use the label

```plaintext
By Theorem~\ref{thm:even-sum}, the sum is even.
```

- You can use labels with equations as well

```plaintext
\begin{equation}\label{eq:pythagorean}
a^2+b^2=c^2.
\end{equation}

Equation~\eqref{eq:pythagorean} is the Pythagorean equation.
```
