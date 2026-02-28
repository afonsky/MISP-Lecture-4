---
theme: seriph
addons:
  - "@twitwi/slidev-addon-ultracharger"
addonsConfig:
  ultracharger:
    inlineSvg:
      markersWorkaround: false
    disable:
      - metaFooter
      - tocFooter
background: /logo/mountain.jpg
highlighter: shiki
routerMode: hash
lineNumbers: false

css: unocss
title: AI in Particle Physics (Practical Course)
subtitle: Artificial Neural Networks
date: 28/02/2026
venue: HSE
author: Alexey Boldyrev
---

<br>
<br>

# <span style="font-size:28.0pt" v-html="$slidev.configs.title?.replaceAll(' ', '<br/>')"></span>
# <span style="font-size:32.0pt" v-html="$slidev.configs.subtitle?.replaceAll(' ', '<br/>')"></span>
# <span style="font-size:18.0pt" v-html="$slidev.configs.author?.replaceAll(' ', '<br/>')"></span>

<span style="font-size:18.0pt" v-html="$slidev.configs.date?.replaceAll(' ', '<br/>')"></span>


<style>
  :deep(footer) { padding-bottom: 3em !important; }
</style>


---
src: ./slides/0_introduction.md
---

---
src: ./slides/1_single_layer_NN.md
---

---
src: ./slides/2_multilayer_NN.md
---

---
src: ./slides/3_fitting_NN.md
---

---
src: ./slides/4_backpropagation.md
---

---
src: ./slides/5_loss_functions.md
---

---
src: ./slides/9_DL_tools.md
---

---
src: ./slides/0_end.md
---
