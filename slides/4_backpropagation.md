---
zoom: 0.9
---

# Backpropagation

#### How do we find the directions to move $\theta$ so as to decrease the objective $R(\theta)$?

One need to calculate **gradient** of $R(\theta)$ evaluated at some current value $\theta = \theta^m$:

$\nabla R(\theta^m) = \frac{\partial R(\theta)}{\partial\theta} \biggr\rvert_{\theta = \theta^m}$

The idea of gradient descent is to move $\theta$ a little in the opposite direction:

$\theta^{m+1} \leftarrow \theta^m - \rho \nabla R(\theta^m)$,

where $\rho$ is the **learning rate**.

If the gradient vector is zero, then we may have arrived at a minimum of the objective.

#### Backpropagation:
* Allows us to compute gradients algorithmically
* Used by deep learning frameworks (PyTorch, etc.) 

---
zoom: 0.9
---

# Backpropagation: Example

<v-click at="1">
<div class="grid grid-cols-[2fr_2fr]">
<div>
  <figure>
    <img src="/Backpropagation_Ex2.png" style="width: 350px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute;"><br>Ex. credits:
      <a href="https://web.stanford.edu/class/archive/cs/cs224n/cs224n.1184/syllabus.html">https://web.stanford.edu/class/archive/cs/cs224n/cs224n.1184</a>
    </figcaption>
  </figure>
</div>
<div>

$$
\boxed{
  \begin{array}{rcl}
f(x, y, z) = (x + y) ~\mathrm{max}(y, z)\\
x = 1, ~y = 2, ~z = 0\\
\\
\mathrm{Find~}\frac{\partial{f}}{\partial{y}}
\end{array}
}
$$
</div>
</div>
</v-click>

<div class="grid grid-cols-[2fr_2fr]">
<div>
<v-click at="2">

Forward propagation steps:<br>
$a = x + y$

$b = \mathrm{max}(y, z)$

$f = a \cdot b$
</v-click>
</div>
<div>
<v-click at="3">

Local gradients:<br>
$\frac{\partial{a}}{\partial{x}} = 1$ $~~~\frac{\partial{a}}{\partial{x}} = 1$

$\frac{\partial{b}}{\partial{y}} = \boldsymbol{1} (y > z) = 1$ $~~~\frac{\partial{b}}{\partial{z}} = \boldsymbol{1} (y < z) = 0$
</v-click>

<v-click at="4">

$$
\frac{\partial{f}}{\partial{a}} = b = 2~~~~~~~ \frac{\partial{f}}{\partial{b}} = a = 3
$$
</v-click>
</div>
</div>
<v-click at="5">

$\frac{\partial{f}}{\partial{x}} = 2~~~~~~ \boxed{\frac{\partial{f}}{\partial{y}} = 3 + 2 = 5}~~~~~ \frac{\partial{f}}{\partial{z}} = 0$
</v-click>