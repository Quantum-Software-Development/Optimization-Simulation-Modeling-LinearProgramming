

## **Problema de Programação Linear**

**Objetivo**: Maximizar a função objetivo.

**Função objetivo**:

$$
\text{Max } Z = x_1 + 5x_2
$$

**Restrições**:

$$
\begin{cases}
x_1 + x_2 \leq 5 \\
x_1 + 2x_2 \leq 6 \\
2x_1 + x_2 \leq 7 \\
x_1 \geq 0, \quad x_2 \geq 0
\end{cases}
$$

---

## **Passo 1: Converter as Desigualdades em Igualdades para Traçar as Retas**

1. \$ x_1 + x_2 = 5 \$
    - Se \$ x_1 = 0 \$, então \$ x_2 = 5 \$
    - Se \$ x_2 = 0 \$, então \$ x_1 = 5 \$
2. \$ x_1 + 2x_2 = 6 \$
    - Se \$ x_1 = 0 \$, então \$ 2x_2 = 6 \Rightarrow x_2 = 3 \$
    - Se \$ x_2 = 0 \$, então \$ x_1 = 6 \$
3. \$ 2x_1 + x_2 = 7 \$
    - Se \$ x_1 = 0 \$, então \$ x_2 = 7 \$
    - Se \$ x_2 = 0 \$, então \$ 2x_1 = 7 \Rightarrow x_1 = 3,5 \$

---

## **Passo 2: Desenhar as Retas no Plano Cartesiano**

1. Trace as retas no plano \$ (x_1, x_2) \$.
2. Identifique a região viável, que é a área delimitada pelas retas e pelos eixos \$ x_1 \geq 0 \$ e \$ x_2 \geq 0 \$.

---

## **Passo 3: Determinar os Vértices da Região Viável**

Os vértices são os pontos de interseção das retas. Vamos calcular:

1. Interseção entre \$ x_1 + x_2 = 5 \$ e \$ x_1 + 2x_2 = 6 \$:
    - Subtraindo a primeira equação da segunda:
\$ (x_1 + 2x_2) - (x_1 + x_2) = 6 - 5 \$
\$ x_2 = 1 \$
    - Substituindo \$ x_2 = 1 \$ na primeira equação:
\$ x_1 + 1 = 5 \Rightarrow x_1 = 4 \$
    - Ponto: \$ (4, 1) \$
2. Interseção entre \$ x_1 + x_2 = 5 \$ e \$ 2x_1 + x_2 = 7 \$:
    - Subtraindo a primeira equação da segunda:
\$ (2x_1 + x_2) - (x_1 + x_2) = 7 - 5 \$
\$ x_1 = 2 \$
    - Substituindo \$ x_1 = 2 \$ na primeira equação:
\$ 2 + x_2 = 5 \Rightarrow x_2 = 3 \$
    - Ponto: \$ (2, 3) \$
3. Interseção entre \$ x_1 + 2x_2 = 6 \$ e \$ 2x_1 + x_2 = 7 \$:
    - Multiplicando a primeira equação por 2:
\$ 2x_1 + 4x_2 = 12 \$
    - Subtraindo a segunda equação da resultante:
\$ (2x_1 + 4x_2) - (2x_1 + x_2) = 12 - 7 \$
\$ 3x_2 = 5 \Rightarrow x_2 = \frac{5}{3} \$
    - Substituindo \$ x_2 = \frac{5}{3} \$ na primeira equação:
\$ x_1 + 2\left(\frac{5}{3}\right) = 6 \$
\$ x_1 = 6 - \frac{10}{3} = \frac{18 - 10}{3} = \frac{8}{3} \$
    - Ponto: \$ \left(\frac{8}{3}, \frac{5}{3}\right) \approx (2.67, 1.67) \$
4. Interseção com os eixos:
    - \$ (0, 0) \$
    - \$ (3.5, 0) \$
    - \$ (0, 3) \$

---

## **Passo 4: Avaliar a Função Objetivo nos Vértices**

1. \$ (0, 0) \Rightarrow Z = 0 + 5(0) = 0 \$
2. \$ (3.5, 0) \Rightarrow Z = 3.5 + 5(0) = 3.5 \$
3. \$ (0, 3) \Rightarrow Z = 0 + 5(3) = 15 \$
4. \$ (4, 1) \Rightarrow Z = 4 + 5(1) = 9 \$
5. \$ (2, 3) \Rightarrow Z = 2 + 5(3) = 17 \$
6. \$ \left(\frac{8}{3}, \frac{5}{3}\right) \Rightarrow Z = \frac{8}{3} + 5\left(\frac{5}{3}\right) = \frac{8}{3} + \frac{25}{3} = \frac{33}{3} = 11 \$

---

## **Passo 5: Identificar a Solução Ótima**

O maior valor de \$ Z \$ é 17, que ocorre no ponto \$ (2, 3) \$.

---

## **Resposta Final**

$$
\boxed{
x_1 = 2, \quad x_2 = 3, \quad Z_{\text{máximo}} = 17
}
$$

---

Portanto, a solução ótima é \$ x_1 = 2 \$, \$ x_2 = 3 \$, e o valor máximo da função objetivo é 17.

