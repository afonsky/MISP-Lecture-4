---
zoom: 0.9
---

# Biological NNs and Artificial NNs

<div class="grid grid-cols-[5fr_2fr]">
<div>
  <figure>
    <img src="/Neuron3.svg" style="width: 500px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 10px; position: absolute;"><br>Image source:
      <a href="https://commons.wikimedia.org/wiki/File:Neuron3.svg">https://commons.wikimedia.org/wiki/File:Neuron3.svg</a>
    </figcaption>
  </figure>
</div>
<div>
  <figure>
    <img src="/ISLRv2_figure_10.1.png" style="width: 250px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 10px; position: absolute;"><br>Feed-forward NN. Image source:
      <a href="https://hastie.su.domains/ISLR2/ISLRv2_website.pdf#page=412">ISLR Fig. 10.1</a>
    </figcaption>
  </figure>
</div>
</div>

<div class="grid grid-cols-[1fr_1fr]">
<div>
<br>
<br>
<v-clicks>

* <small>Both have *multiple* **inputs** from and **outputs** to other neurons</small>
* <small>Both use **activation** of the neurons</small>
* <small>Both are **designed to learn** an optimal behavior</small>

</v-clicks>
</div>
<div>
<v-clicks>
<small>In ANN:</small>

* <small>"**Dendrites**" are connections, which carry information<br> (learnt coefficients)</small>
* <small>"**Synapses**" are activation functions, which augment or filter information flow; and "**soma**" acts as the summation function</small>

</v-clicks>
</div>
</div>

---
zoom: 0.9
---

# Biological NNs and Artificial NNs

<div class="grid grid-cols-[5fr_2fr]">
<div>
  <figure>
    <img src="/Neuron3.svg" style="width: 500px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 10px; position: absolute;"><br>Image source:
      <a href="https://commons.wikimedia.org/wiki/File:Neuron3.svg">https://commons.wikimedia.org/wiki/File:Neuron3.svg</a>
    </figcaption>
  </figure>
</div>
<div>
  <figure>
    <img src="/ISLRv2_figure_10.1.png" style="width: 250px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 10px; position: absolute;"><br>Feed-forward NN. Image source:
      <a href="https://hastie.su.domains/ISLR2/ISLRv2_website.pdf#page=412">ISLR Fig. 10.1</a>
    </figcaption>
  </figure>
</div>
</div>

<div class="grid grid-cols-[3fr_2fr]">
<div>
<br>
<small>Further reading on biological NNs. <a href="https://christofkoch.com">Christof Koch:</a></small>

* <small><a href="https://christofkoch.com/biophysics-book/">Biophysics of Computation: Information Processing in Single Neurons
</a></small>
* <small><a href="https://www.cse.psu.edu/~rtc12/CSE597E/papers/Itti_etal98pami.pdf">A model of saliency-based visual attention for rapid scene analysis</a></small>
* <small><a href="https://www.youtube.com/watch?v=indbWawx3Hs">Consciousness & Reality Colloquium Series: Inaugural Lecture</a></small>
</div>
<div>

* <small>Neuroscience by Dale Purves et al. (6th ed., 2018)</small><br>
<small>Vyacheslav Dubynin (in russian):</small>
* <small>Мозг и его потребности: От питания до признания (2021)</small>
* <small><a href="https://www.youtube.com/@dubynin/playlists">Lectures on the YouTube</a></small>
</div>
</div>

---

# Biological NNs and Artificial NNs
<div>
</div>

Artificial neural networks (ANNs) are **inspired by** the biological neural networks (BNNs)<br> but most of them are only **loosely based on** the BNNs.<br>

<a href="https://en.wikipedia.org/wiki/Spiking_neural_network">Spiking neural networks</a> are ANNs that more closely mimic natural neural networks

<div class="grid grid-cols-[5fr_3fr]">
<div>
  <figure>
    <img src="/Unsupervised_learning_with_ferroelectric_synapses.png" style="width: 490px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 10px; position: absolute;"><br>Unsupervised learning with ferroelectric synapses. Image source:
      <a href="https://www.nature.com/articles/ncomms14736"><em>Nature Communications</em> 8, 14736 (2017)</a>
    </figcaption>
  </figure>
</div>
<div>

#### [Brain Score](http://www.brain-score.org)
<br>
  <figure>
    <img src="/gr3_lrg.jpg" style="width: 400px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 10px; position: absolute;"><br>Integrative Benchmarking to Advance Neurally Mechanistic Models of Human Intelligence. Image source:
      <a href="https://doi.org/10.1016/j.neuron.2020.07.040"><em>Neuron</em> 108.3 (2020)</a>
    </figcaption>
  </figure>
</div>
</div>

---
zoom: 0.85
---

# Why Deep Learning model?
<v-click at="1">

#### Because neural networks are universal approximators of **continuous univariate functions**
</v-click>
<br>

<div class="grid grid-cols-[3fr_4fr] gap-10">
<div>
<v-click at="2">

#### Arbitrary/bounded width

<figure>
    <img src="/2407.12895v1_uat_1.svg" style="width: 275px !important;">
</figure>
<br>

#### [Cybenko, G. (1989, Sigmoid)](https://link.springer.com/content/pdf/10.1007/BF02551274.pdf)
</v-click>
<br>
<v-click at="4">

See also:<br>
#### [arXiv:1710.11278 (2017, ReLU, minimal width)](https://arxiv.org/abs/1710.11278)
#### [Zhou (2020, CNN, bounded width and depth)](https://www.sciencedirect.com/science/article/pii/S1063520318302045)
</v-click>
</div>
<div>
<v-click at="3">

#### Arbitrary/bounded depth

<figure>
    <img src="/2407.12895v1_uat_2.svg" style="width: 435px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute"><br>Image source:
      <a href="https://arxiv.org/abs/2407.12895v1">arXiv:2407.12895</a>
    </figcaption>
</figure>
</v-click>
<br>
<v-click at="5">
<br>

#### Kolmogorov–Arnold representation theorem (1957):
$f(\mathbf x) = f(x_1,\ldots ,x_n) = \sum\limits_{q=0}^{2n} \Phi_{q}\!\left(\sum\limits_{p=1}^{n} \phi_{q,p}(x_{p})\right)$  
</v-click>
<br>

<v-click at="5">

#### Kolmogorov-Arnold Networks [Liu (2024)](https://arxiv.org/abs/2404.19756)

#### $w \to$ arbitrary univariate function
</v-click>
</div>
</div>

---
zoom: 0.9
---

# Artificial Neural Networks: Examples

<v-clicks>

1. [RNN](https://en.wikipedia.org/wiki/Recurrent_neural_network) for sequence data with short dependencies
1. [LSTM](https://en.wikipedia.org/wiki/Long_short-term_memory) for sequence data with short and long dependencies
1. [CNN](https://en.wikipedia.org/wiki/Convolutional_neural_network) for images with 2D and 3D (+[RGB](https://en.wikipedia.org/wiki/RGB_color_model)) spatial dependencies
1. [U-Net](https://en.wikipedia.org/wiki/U-Net) is an improved CNN
1. [VAE](https://en.wikipedia.org/wiki/Variational_autoencoder) to compress representation of images, audio, ...
1. [GAN](https://en.wikipedia.org/wiki/Generative_adversarial_network) to generate new observations (e.g. faces, voices) from the training distribution
1. [Transformers](https://en.wikipedia.org/wiki/Transformer_(machine_learning_model)) builds "*attention*" to the "*important*" input data
   * [LLMs](https://en.wikipedia.org/wiki/Large_language_model) utilize the transformer architecture
1. [Deep RL](https://en.wikipedia.org/wiki/Deep_reinforcement_learning) trains an agent to take max-reward actions based on current state and past history (e.g. gaming, robotics)
1. [GNN](https://en.wikipedia.org/wiki/Graph_neural_network) for graph-based data (e.g. social network, street maps, citation network)
1. [RBM](https://en.wikipedia.org/wiki/Restricted_Boltzmann_machine) to learn the distribution of input for generative tasks
1. [SOM](https://en.wikipedia.org/wiki/Self-organizing_map) for dimension reduction with maintaining the topological structure

</v-clicks>

---

# Essentials of Artificial Neural Networks

### Building blocks:
<div class="grid grid-cols-[3fr_2fr_2fr] gap-3">
<div>

* Neuron
* Loss function
* Activation function
* Optimizer
<!-- * <span style="color:#FA9370">Optimizer</span> -->
</div>

<div>

* Linear layer
* Convolution layer
* Pooling layer
* Recurrent layer
* Attention layer
</div>

<div>
  <figure>
    <img src="/lego_A.jpg" style="width: 190px !important;">
    <figcaption style="color:#b3b3b3ff; font-size: 11px; position: absolute;"><br>Image source:
      <a href="http://sgaguilarmjargueso.blogspot.com/2014/08/de-lego.html">http://sgaguilarmjargueso.blogspot.com</a>
    </figcaption>
  </figure>   
</div>
</div>
<br>

### Concepts:
<div class="grid grid-cols-[2fr_2fr_3fr] gap-2">
<div>

* Weights & Biases
* Backpropagation
* Gradient descent

</div>
<div>

* Learning rate
* MiniBatch
* Regularization
</div>

<div>

* Long Short-Term Memory (LSTM)
* Encoder - Decoder
</div>

</div>