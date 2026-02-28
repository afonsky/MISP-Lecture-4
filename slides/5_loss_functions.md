# Loss Function
<div></div>

A loss function is a function $L:(z,y)\in \R \times Y \rightarrow L(z,y) \in R$ that takes as inputs the predicted value $z$ corresponding to the real data value $y$ and outputs how different they are.

<br>
<div>
<center>
  <figure>
    <img src="/Loss_functions_cs-229.png" style="width: 750px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: relative;"><br>Image source:
      <a href="https://stanford.edu/~shervine/teaching/cs-229/cheatsheet-supervised-learning">by Shervine Amidi</a>
    </figcaption>
  </figure>
  </center>
</div>

---
zoom: 0.9
---

# Loss Functions: Quick Reference

| Loss | Task | Formula | Key Property |
|------|------|---------|--------------|
| MSE | Regression | $(x-y)^2$ | Smooth, sensitive to outliers |
| MAE | Regression | $\|x-y\|$ | Robust to outliers |
| Cross-Entropy | Multi-class | $-\sum y_j \log \hat{y}_j$ | Works with softmax |
| NLL | Multi-class | $-\log \hat{y}_{\text{true}}$ | Expects log-probabilities |
| BCE | Binary | $-[y\log x + (1-y)\log(1-x)]$ | Special case of CE |
| Hinge | Binary (SVM) | $\max(0, 1-y\cdot x)$ | Margin-based |
| KL Divergence | Distribution matching | $\sum y(\log y - \log x)$ | Asymmetric |

**For classification**: Cross-Entropy is standard choice

---

# Cross Entropy on Iris Flower Data Set

* Let’s explore famous [Iris data set](https://en.wikipedia.org/wiki/Iris_flower_data_set)
* Goal: classify iris species based on petal and sepal widths and lengths (total 4 features)
* 3 classes (species)
* 50 observations per class

<br>
<center>
<div class="grid grid-cols-[2fr_2fr_2fr] gap-10">
<div>
  <figure>
    <img src="/iris_setosa.png" style="width: 200px">
  </figure>
</div>
<div>
  <figure>
    <img src="/iris_versicolor.png" style="width: 200px">
  </figure>
</div>
<div>
  <figure>
    <img src="/iris_virginica.png" style="width: 200px">
  </figure>
</div>
</div>
</center>
<br>

<span style="color:grey"><small> Images source: [https://en.wikipedia.org/wiki/Iris_flower_data_set](https://en.wikipedia.org/wiki/Iris_flower_data_set)</small></span>

---

# Cross Entropy
<div></div>

<small>
  <small>

| Petal Width | Sepal Width | Species    | $"p"$  | Cross Entropy      |
|-------------|-------------|------------|--------|--------------------|
| **0.04**        | **0.42**        | **Setosa**     |  **0.57**  | $\bm{-\mathrm{log}("p")}$ **= 0.56** |
| 1.0         | 0.54        | Virginica  |  0.58  | $-\mathrm{log}("p")$ = 0.54 |
| 0.50        | 0.37        | Versicolor |  0.52  | $-\mathrm{log}("p")$ = 0.65 |

</small>
</small>
<div>
<center>
  <figure>
    <img src="/Cross_entropy_1.svg" style="width: 680px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute; right: 60px; top: 60px"><br>Example inspired by:
      <a href="https://www.youtube.com/watch?v=6ArSys5qHAU">Josh Starmer's video</a>
    </figcaption>
  </figure>
</center>
</div>

---

# Cross Entropy
<div></div>

<small>
  <small>

| Petal Width | Sepal Width | Species    | $"p"$  | Cross Entropy      |
|-------------|-------------|------------|--------|--------------------|
| 0.04        | 0.42        | Setosa     |  0.57  | $-\mathrm{log}("p")$ = 0.56 |
| **1.0**         | **0.54**        | **Virginica**  |  **0.58**  | $\bm{-\mathrm{log}("p")}$ **= 0.54** |
| 0.50        | 0.37        | Versicolor |  0.52  | $-\mathrm{log}("p")$ = 0.65 |

</small>
</small>

<div>
<center>
  <figure>
    <img src="/Cross_entropy_2.svg" style="width: 680px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute; right: 60px; top: 60px"><br>Example inspired by:
      <a href="https://www.youtube.com/watch?v=6ArSys5qHAU">Josh Starmer's video</a>
    </figcaption>
  </figure>
</center>
</div>

---

# Cross Entropy
<div></div>

<small>
  <small>

| Petal Width | Sepal Width | Species    | $"p"$  | Cross Entropy      |
|-------------|-------------|------------|--------|--------------------|
| 0.04        | 0.42        | Setosa     |  0.57  | $-\mathrm{log}("p")$ = 0.56 |
| 1.0         | 0.54        | Virginica  |  0.58  | $-\mathrm{log}("p")$ = 0.54 |
| **0.50**        | **0.37**        | **Versicolor** |  **0.52**  | $\bm{-\mathrm{log}("p")}$ **= 0.65** |

</small>
</small>

<div>
<center>
  <figure>
    <img src="/Cross_entropy_3.svg" style="width: 680px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute; right: 60px; top: 60px"><br>Example inspired by:
      <a href="https://www.youtube.com/watch?v=6ArSys5qHAU">Josh Starmer's video</a>
    </figcaption>
  </figure>
</center>
</div>

---

# Cross Entropy
<div></div>

<small>
  <small>

| Petal Width | Sepal Width | Species    | $"p"$  | Cross Entropy      |
|-------------|-------------|------------|--------|--------------------|
| 0.04        | 0.42        | Setosa     |  0.57  | $\bm{-\mathrm{log}("p")}$ **= 0.56** |
| 1.0         | 0.54        | Virginica  |  0.58  | $\bm{-\mathrm{log}("p")}$ **= 0.54** |
| 0.50        | 0.37        | Versicolor |  0.52  | $\bm{-\mathrm{log}("p")}$ **= 0.65** |

</small>
</small>

<br>

<div class="grid grid-cols-[2fr_3fr] gap-40">
<div>
  <figure>
    <img src="/Log_loss.png" style="width: 350px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute;"><br>Image source:
      <a href="https://ml-cheatsheet.readthedocs.io/en/latest/loss_functions.html">ml-cheatsheet.readthedocs.io</a>
    </figcaption>
  </figure>
</div>
<div>

##### Total Cross Entropy = 0.56 + 0.54 + 0.65 = 1.75
</div>
</div>