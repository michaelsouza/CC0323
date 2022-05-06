---
presentation:
    width: 800
    height: 600            
    center: true
    margin: 0.1
    progress: true
    theme: white.css
export_on_save:
  ebook: true
---

<style type="text/css">
  .reveal p {
    text-align: left;
    font-size: 25px;
  }
  .reveal ul {
    display: block;
  }
  .reveal ol {
    display: block;
  }
</style>

<!-- slide -->
@import "figures/03_07.png" {width="400px" title="my title" alt="my alt"}

#### Otimização Convexa
##### Capítulo 22

<!-- slide -->
**Def. gráfico de uma função**
O gráfico de $f:\Omega\to\mathbb{R}, \Omega\subset\mathbb{R}^n$, é o conjunto de pontos em $\Omega\times\mathbb{R}\subset\mathbb{R}^{n+1}$ dado por 

$$\left\{\binom{x}{f(x)}:x\in\Omega\right\}$$

**Def. epígrafe de uma função**
A epígrafe de uma função $f:\Omega\to\mathbb{R}, \Omega\subset\mathbb{R}^n$, representada por $epi(f)$, é o conjunto de pontos em $\Omega\times\mathbb{R}$ dado por
$$\left\{\binom{x}{\beta}:x\in\Omega, \beta\in\mathbb{R}, \beta\geq f(x)\right\}$$

<!-- slide -->
@import "figures/03_01.png" {width="800px" title="my title" alt="my alt"}

<!-- slide -->
**Def. função convexa**
Uma função $f:\Omega\to\mathbb{R}, \Omega\subset\mathbb{R}^n$, será *convexa em $\Omega$* se $epi(f)$ for um conjunto convexo.

@import "figures/03_02.png" {width="800px" title="my title" alt="my alt"}

<!-- slide -->
**Teorema**
Se uma função $f:\Omega\to\mathbb{R}, \Omega\subset\mathbb{R}^n$, for *convexa em $\Omega$, então $\Omega$ é um conjunto convexo*.

**Obs 1:** Toda projeção orthogonal de um conjunto convexo é um conjunto convexo.
**Obs 2:** O conjunto $\Omega$, domínio de $f$, é a projeção orthogonal de $epi(f)$ sobre $\mathbb{R}^n$.

@import "figures/03_06.png" {width="400px" title="my title" alt="my alt"}

<!-- slide -->
**Teorema**
Uma função $f:\Omega\to\mathbb{R}$, definida em um conjunto convexo $\Omega\subset\mathbb{R}^n$ será convexa se, e somente se, $\forall x,y\in\Omega$ e $\forall \alpha\in(0,1)$, tivermos
$$f(\alpha x + (1-\alpha)y)\leq \alpha f(x) + (1-\alpha)f(y).$$

@import "figures/03_03.png" {width="450px" title="my title" alt="my alt"}

<!-- slide -->
**Teorema**
Suponha que $f$ e $g$ sejam funções convexas, então, para qualquer $\kappa\geq 0$, as funções $\kappa f$ e $f + g$ também são convexas.

@import "figures/03_05.gif" {width="900px" title="my title" alt="my alt"}

<!-- slide -->
**Def. função estritamente convexa**
Uma função $f:\Omega\to\mathbb{R}$, definida em um conjunto convexo $\Omega\subset\mathbb{R}^n$, será estritamente convexa se $\forall x,y\in\Omega, x\neq y$ e $\alpha\in(0,1)$, tivermos
$$f(\alpha x + (1-\alpha)y)< \alpha f(x) + (1-\alpha)f(y).$$


**Def. função côncava**
Uma função $f:\Omega\to\mathbb{R}$, definida em um conjunto convexo $\Omega\subset\mathbb{R}^n$, será (estritamente) côncava se $-f$ for (estritamente) convexa.

<!-- slide -->
**Exercício:**
A função $f(x)=x_1x_2$ é convexa em $\Omega\equiv\{x:x_1\geq 0, x_2\geq 0\}$?

@import "figures/03_04.gif" {width="800px" title="my title" alt="my alt"}

<!-- slide -->
**Proposição.**
Uma forma quadrática $f:\Omega\to\mathbb{R}$, $\Omega\subset\mathbb{R}^n$, dada por $f(x)=x^tQx$ com $$Q\in\mathbb{R}^{n\times n} \;\;\text{ e }\;\; Q=Q^t\;\; \text{(matriz simétrica)},$$ será convexa em $\Omega$ se, e somente se, $\forall x,y \in \Omega$, tivermos $$(x-y)^tQ(x-y)\geq 0,$$
ou seja, $Q$ é uma matriz semidefinida positiva.

<!-- slide -->
**Exercício:**
Retornando à função $f(x)=x_1x_2$, mostre que $f$ pode ser escrita como $$f(x)=x^tQx\;\;\text{(forma quadrática)},$$ mas $Q$ não será uma matriz semidefinida positiva.

<!-- slide -->
**Teorema.**
 Seja $f:\Omega\to\mathbb{R}, f \in\mathcal{C}^1$, definida em um conjunto aberto e convexo $\Omega\subset\mathbb{R}^n$. Então, $f$ será convexa em $\Omega$ se, e somente se, $\forall x,y \in \Omega$, tivermos
$$f(y)\geq f(x)+\nabla f(x)(y-x).$$

@import "figures/03_04.png" {width="400px" title="my title" alt="my alt"}

<!-- slide -->
**Teorema.**
 Seja $f:\Omega\to\mathbb{R}, f \in\mathcal{C}^2$, definida em um conjunto aberto e convexo $\Omega\subset\mathbb{R}^n$. Então, $f$ será convexa em $\Omega$ se, e somente se, $\forall x \in \Omega$, a matriz hessiana $\nabla^2 f(x)$ for semidefinita positiva.

@import "figures/03_05.png" {width="500px" title="my title" alt="my alt"}

<!-- slide -->
**Exercício:**
Determine se as funções abaixo são convexas, côncavas ou nenhuma das duas.
 
**(1)** $f:\mathbb{R}\to\mathbb{R},$
$$f(x)=-8x^2.$$
**(2)** $f:\mathbb{R}^3\to\mathbb{R},$ 
$$f(x)=4x_1^2+3x_2^2+5x^2_3+6x_1x_2+x_1x_3-3x_1-2x_2+15.$$
**(3)** $f:\mathbb{R}^2\to\mathbb{R},$
$$f(x)=2x_1x_2-x_1^2-x_2^2.$$

<!-- slide -->
**Teorema.**
Se $f:\Omega\to\mathbb{R}$ é função convexa, então, em $\Omega$, todo minimizador local de $f$ também será um minimizador global.

**Lema.**
Se $g:\Omega\to\mathbb{R}$ for uma função convexa, então, para cada $c\in\mathbb{R}$, o conjunto $\Gamma_c = \{x\in\Omega:g(x)\leq c\}$ será convexo.

@import "figures/03_10.png" {width="500px" title="my title" alt="my alt"}

<!-- slide -->
**Corolário.**
Se $f:\Omega\to\mathbb{R}$ for uma função convexa, então o conjunto de minimizadores globais de $f$ em $\Omega$ será convexo.

@import "figures/03_01.jpg" {width="600px" title="my title" alt="my alt"}

<!-- slide -->
**Lema.**
Sejam $f:\Omega\to\mathbb{R}$ uma função convexa de classe $\mathcal{C}^1$ em um conjunto aberto contendo $\Omega\subset\mathbb{R}^n$. Suponha que $x^\ast\in\Omega$ é tal que, $\forall x\in\Omega$, $x\neq x^\ast$, temos
$$\nabla f(x^\ast)(x-x^\ast)\geq 0.$$
Então, $x^\ast$ é um minimizador global de $f$ em $\Omega$.

<!-- slide -->
**Teorema.**
Sejam $f:\Omega\to\mathbb{R}$ uma função convexa de classe $\mathcal{C}^1$ em um conjunto aberto contendo $\Omega\subset\mathbb{R}^n$. Suponha que $x^\ast\in\Omega$ é tal que, para qualquer direção viável $d$ em $x^\ast$, temos
$$d^t\nabla f(x^\ast)\geq 0.$$
Então, $x^\ast$ é um minimizador global de $f$ em $\Omega$.

<!-- slide -->
**Corolário.**
Seja $f:\Omega\to\mathbb{R}$ uma função convexa de classe $\mathcal{C}^1$. Suponha que $x^\ast\in\Omega$ é tal que
$$\nabla f(x^\ast) = 0.$$
Então, $x^\ast$ é um minimizador global de $f$ em $\Omega$.

<!-- slide -->
**Teorema.**
Sejam $f:\Omega\to\mathbb{R}$ uma função convexa de classe $\mathcal{C}^1$ em $$\Omega=\{x\in\mathbb{R}^n:h(x)=0\},$$
onde $h:\mathbb{R}^n\to\mathbb{R}^m$, $h\in\mathcal{C}^1$. Suponha que existam $x^\ast\in\Omega$ e $\lambda^\ast\in\mathbb{R}^m$ tais que 
$$\nabla f(x^\ast) + \nabla^t h(x^\ast)\lambda^* = 0.$$
Então, $x^\ast$ é um minimizador global de $f$ em $\Omega$.

<!-- slide -->
@import "figures/03_09.png" {width="800px" title="my title" alt="my alt"}

<!-- slide -->
**Teorema. Condições de Karush-Kuhn-Tucker (KKT)**
Sejam $f:\Omega\to\mathbb{R}$ uma função convexa de classe $\mathcal{C}^1$ em $$\Omega=\{x\in\mathbb{R}^n:h(x)=0, g(x)\leq 0\},$$
onde $h:\mathbb{R}^n\to\mathbb{R}^m$, $g:\mathbb{R}^n\to\mathbb{R}^p$, $h,g\in\mathcal{C}^1$. Suponha que existam $x^\ast\in\Omega$, $\lambda^\ast\in\mathbb{R}^m$ e $\mu^\ast\in\mathbb{R}^p$ tais que 

(1) $\mu^\ast\geq 0.$
(2) $\nabla f(x^\ast) + \nabla^t h(x^\ast) \lambda^*+ \nabla^t g(x^\ast)\mu= 0.$
(3) $g^t(x^\ast)\mu^\ast = 0.$

Então, $x^\ast$ é um minimizador global de $f$ em $\Omega$.

<!-- slide -->
@import "figures/03_08.png" {width="700px" title="my title" alt="my alt"}

<!-- slide vertical=false -->
#### FIM
