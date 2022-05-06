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

#### Busca Unidimensional
##### Capítulo 07

<!-- slide -->
Esquema geral dos algoritmos de direções de descida.

@import "figures/05_01.png" {width="600px" title="my title" alt="my alt"}

<!-- slide -->
Esquema geral dos algoritmos de direções de descida.

```python {}
def opt_method(f, x, maxit, ftol, xtol):
  fx = f(x)
  for i in range(maxit):
    xOld = x                     # save current point
    fxOld = fx                   # save current value
    d = descent_direction(f, x)  # descent direction
    s = line_search(f, x, d)     # step size
    x = xOld + s * d             # point update
    fx = f(x)                    # function update
    done = converged(x, xold, fx, fxOld, ftol, xtol)
    if done:
      break
  raise Exception('Max number of iterations exceeded')

```


<!-- slide vertical=false -->
#### FIM
