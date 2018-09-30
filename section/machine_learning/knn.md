---
layout: machine_learning
comments: true
mathjax: true
---

### [Nearest Neighbors](../machine_learning.html)

Nearest Neighbors is a non-parametric classifier.


$$ P(y = c|\mathbf{x}, \,\mathcal{D}, \,K) = \frac{1}{K}\sum_{i\in N_K (x,\,\mathcal{D})} \mathbb{I}(y_i= c) $$

$N_K(\mathbf{x}, \mathcal{D})$ are the indices of K nearest points to $\mathbf{x}$
 in $\mathcal{D}$ and $\mathbb{I}(e)$ is the $\mathbf{indicator}$
 $\mathbf{ function}$ defined as follows:

$$\mathbb{I}(e) =
\begin{cases}
1,  & \text{if $e$ is True} \\
0, & \text{if $e$ is False}
\end{cases}$$

### Curse of Dimensionality

The volume of an n-dimensional cube approach $\infty$ as $n \to \infty$, but the volume of an n-dimensional sphere approach 0 as $n \to \infty$.

More precisely,

$$ \frac{V_n(\text{Sphere})}{V_n (\text{Cube})} \to 0, \,\text{as}\; n \to \infty $$

Volume of an n-dim sphere (radius = R):

$$ V_n(R) = \frac{\pi^{n/2}}{\Gamma(n/2+1)} R^n $$

Volume of an n-dim cube (side length = a):

$$ V_n(a) = a^n $$

Thus the limit depends on whether $a\in(0,1)$, $a=1$ or $a>1.$

 The reason why $\frac{V_n(\text{Sphere})}{V_n (\text{Cube})}\to\infty$ as $n\to\infty$ is that, loosely speaking, much of the volume of the cube is near its corners which the ball doesn't reach, and this phenomenon becomes stronger and stronger as dimension grows. In other words, a ball of radius one cannot go very far in every direction at once, but the cube of side two can.

Suppose if we inscribe an n-ball in a n-cube, the n-ball comprises much small portion of input space. Most of the volume in higher dimensional spaces is very far from the center of the n-ball. So, even if we evenly distribute the points in n-cube most of the points are likely to be in the corners which would roughly equidistant from the n-ball.

As the dimensions increase, the Euclidean distances become less meaningful.

{% if page.comments %}
{% include disqus.html %}
{% endif %}
{% include mathjax.html %}
