

## Como desenhar o gráfico manualmente

1. **Eixos**: Desenhe os eixos $x_1$ (horizontal) e $x_2$ (vertical), ambos a partir de zero (pois $x_1, x_2 \geq 0$).
2. **Desenhe as retas das restrições (igualdades):**

- $x_1 + 3x_2 = 7$
Pontos:
    - $x_1=0 \Rightarrow x_2 = \frac{7}{3} \approx 2,33$
    - $x_2=0 \Rightarrow x_1=7$
- $2x_1 + 2x_2 = 8$
Pontos:
    - $x_1=0 \Rightarrow x_2=4$
    - $x_2=0 \Rightarrow x_1=4$
- $x_1 + x_2 = 3$
Pontos:
    - $x_1=0 \Rightarrow x_2=3$
    - $x_2=0 \Rightarrow x_1=3$
- $x_2 = 2$ (reta horizontal)

3. **Sombreie a região que satisfaz as desigualdades (área abaixo ou à esquerda das retas, e acima dos eixos).**
4. **Marque os vértices da região viável e identifique o ponto ótimo (3,0).**

---

## Código Python para gerar o gráfico

```python
import numpy as np
import matplotlib.pyplot as plt

# Definir os valores de x1 para plotar as retas
x1 = np.linspace(0, 8, 400)

# Restrições
# 1) x1 + 3x2 &lt;= 7  =&gt; x2 &lt;= (7 - x1)/3
x2_1 = (7 - x1) / 3

# 2) 2x1 + 2x2 &lt;= 8 =&gt; x2 &lt;= (8 - 2x1)/2 = 4 - x1
x2_2 = 4 - x1

# 3) x1 + x2 &lt;= 3 =&gt; x2 &lt;= 3 - x1
x2_3 = 3 - x1

# 4) x2 &lt;= 2
x2_4 = 2 * np.ones_like(x1)

# Limites para x2 (não negativas)
x2_min = np.zeros_like(x1)

# Plotar as restrições
plt.figure(figsize=(8,8))
plt.plot(x1, x2_1, label=r'$x_1 + 3x_2 \leq 7$')
plt.plot(x1, x2_2, label=r'$2x_1 + 2x_2 \leq 8$')
plt.plot(x1, x2_3, label=r'$x_1 + x_2 \leq 3$')
plt.plot(x1, x2_4, label=r'$x_2 \leq 2$')

# Preencher a região viável
# Criar uma grade de pontos
X1, X2 = np.meshgrid(np.linspace(0,8,400), np.linspace(0,5,400))

# Condições das restrições
cond1 = X1 + 3*X2 &lt;= 7 + 1e-5
cond2 = 2*X1 + 2*X2 &lt;= 8 + 1e-5
cond3 = X1 + X2 &lt;= 3 + 1e-5
cond4 = X2 &lt;= 2 + 1e-5
cond5 = X1 &gt;= 0
cond6 = X2 &gt;= 0

# Região viável
region = cond1 &amp; cond2 &amp; cond3 &amp; cond4 &amp; cond5 &amp; cond6

plt.imshow(region.astype(int), extent=(0,8,0,5), origin='lower', cmap='Greys', alpha=0.3)

# Pontos vértices (calculados anteriormente)
vertices = np.array([
    [0,0],
    [0,2],
    [1,2],
    [2,0],
    [3,0]
])

plt.scatter(vertices[:,0], vertices[:,1], color='red')
for i, (x, y) in enumerate(vertices):
    plt.text(x + 0.1, y, f'({x},{y})', fontsize=9)

# Ponto ótimo
plt.scatter(3,0, color='green', s=100, label='Ótimo (3,0)')

plt.xlim(0,8)
plt.ylim(0,5)
plt.xlabel(r'$x_1$')
plt.ylabel(r'$x_2$')
plt.title('Região Viável e Restrições do Problema')
plt.legend()
plt.grid(True)
plt.show()
```

---

### Como usar o código

- Copie e cole o código em um ambiente Python com as bibliotecas **numpy** e **matplotlib** instaladas (ex: Jupyter Notebook, Google Colab, Anaconda).
- Execute para visualizar o gráfico com as restrições, região viável sombreada, vértices e ponto ótimo destacado.

