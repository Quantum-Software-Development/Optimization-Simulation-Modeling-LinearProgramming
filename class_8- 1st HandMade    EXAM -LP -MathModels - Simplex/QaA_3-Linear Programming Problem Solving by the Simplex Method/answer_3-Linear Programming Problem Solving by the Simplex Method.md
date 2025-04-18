
# Resolução de Problema de Programação Linear pelo Método Simplex

Este relatório apresenta a resolução completa do problema de programação linear usando o método Simplex, simulando uma resolução feita à mão, como seria realizada em um caderno.

## Problema de Programação Linear

O problema a ser resolvido é:

Max. Z = 5x₁ + 4x₂

Sujeito a:

- x₁ + 2x₂ ≤ 6
- -2x₁ + x₂ ≤ 4
- 5x₁ + 3x₂ ≤ 15
- x₁, x₂ ≥ 0


## Preparação do Problema para o Método Simplex

### Introdução de Variáveis de Folga

O primeiro passo é converter as restrições de desigualdade em equações, introduzindo variáveis de folga:

- x₁ + 2x₂ + s₁ = 6
- -2x₁ + x₂ + s₂ = 4
- 5x₁ + 3x₂ + s₃ = 15

A função objetivo na forma padrão:
Z - 5x₁ - 4x₂ = 0

### Construção do Tableau Inicial

O tableau inicial é formado pelos coeficientes das variáveis nas restrições, as variáveis de folga, e a função objetivo (com coeficientes negativos):


| Base | x₁ | x₂ | s₁ | s₂ | s₃ | b |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| s₁ | 1 | 2 | 1 | 0 | 0 | 6 |
| s₂ | -2 | 1 | 0 | 1 | 0 | 4 |
| s₃ | 5 | 3 | 0 | 0 | 1 | 15 |
| Z | -5 | -4 | 0 | 0 | 0 | 0 |

## Resolução Passo a Passo pelo Método Simplex

### Primeira Iteração

**Passo 1: Identificar a variável que entra na base**

Analisamos a linha Z e escolhemos a variável com coeficiente mais negativo. Neste caso, x₁ tem coeficiente -5, portanto x₁ entrará na base.

**Passo 2: Identificar a variável que sai da base**

Calculamos as razões para determinar qual variável sairá da base:

- Linha 1 (s₁): 6/1 = 6
- Linha 2 (s₂): não calculamos porque o coeficiente -2 não é positivo
- Linha 3 (s₃): 15/5 = 3

A menor razão positiva é 3, correspondente à linha 3, então s₃ sairá da base.

**Passo 3: Operações de pivoteamento**

O elemento pivô é 5 (linha 3, coluna x₁).

1. Dividimos a linha do pivô (linha 3) pelo valor do pivô (5):
-[^2][^1][^12] ÷ 5 = [1, 0.6, 0, 0, 0.2, 3]
2. Eliminamos os outros elementos da coluna pivô:
    - Linha 1:[^1][^1][^3] - 1×[1, 0.6, 0, 0, 0.2, 3] = [0, 1.4, 1, 0, -0.2, 3]
    - Linha 2: [-2, 1, 0, 1, 0, 4] - (-2)×[1, 0.6, 0, 0, 0.2, 3] = [0, 2.2, 0, 1, 0.4, 10]
    - Linha Z: [-5, -4, 0, 0, 0, 0] - (-5)×[1, 0.6, 0, 0, 0.2, 3] = [0, -1, 0, 0, 1, 15]

Obtemos o seguinte tableau:


| Base | x₁ | x₂ | s₁ | s₂ | s₃ | b |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| s₁ | 0 | 1.4 | 1 | 0 | -0.2 | 3 |
| s₂ | 0 | 2.2 | 0 | 1 | 0.4 | 10 |
| x₁ | 1 | 0.6 | 0 | 0 | 0.2 | 3 |
| Z | 0 | -1 | 0 | 0 | 1 | 15 |

### Segunda Iteração

**Passo 1: Identificar a variável que entra na base**

Na linha Z, o coeficiente de x₂ é -1, então x₂ entrará na base.

**Passo 2: Identificar a variável que sai da base**

Calculamos as razões:

- Linha 1 (s₁): 3/1.4 = 2.143
- Linha 2 (s₂): 10/2.2 = 4.545
- Linha 3 (x₁): 3/0.6 = 5

A menor razão positiva é 2.143, correspondente à linha 1, então s₁ sairá da base.

**Passo 3: Operações de pivoteamento**

O elemento pivô é 1.4 (linha 1, coluna x₂).

1. Dividimos a linha do pivô (linha 1) pelo valor do pivô (1.4):
    - [0, 1.4, 1, 0, -0.2, 3] ÷ 1.4 = [0, 1, 0.714, 0, -0.143, 2.143]
2. Eliminamos os outros elementos da coluna pivô:
    - Linha 2: [0, 2.2, 0, 1, 0.4, 10] - 2.2×[0, 1, 0.714, 0, -0.143, 2.143] = [0, 0, -1.571, 1, 0.714, 5.286]
    - Linha 3: [1, 0.6, 0, 0, 0.2, 3] - 0.6×[0, 1, 0.714, 0, -0.143, 2.143] = [1, 0, -0.429, 0, 0.286, 1.714]
    - Linha Z: [0, -1, 0, 0, 1, 15] - (-1)×[0, 1, 0.714, 0, -0.143, 2.143] = [0, 0, 0.714, 0, 0.857, 17.143]

Obtemos o seguinte tableau:


| Base | x₁ | x₂ | s₁ | s₂ | s₃ | b |
| :-- | :-- | :-- | :-- | :-- | :-- | :-- |
| x₂ | 0 | 1 | 0.714 | 0 | -0.143 | 2.143 |
| s₂ | 0 | 0 | -1.571 | 1 | 0.714 | 5.286 |
| x₁ | 1 | 0 | -0.429 | 0 | 0.286 | 1.714 |
| Z | 0 | 0 | 0.714 | 0 | 0.857 | 17.143 |

### Verificação de Otimalidade

Como todos os coeficientes na linha Z são não-negativos, atingimos a solução ótima.

## Solução Ótima

Expressando a solução em frações para maior precisão:

- x₁ = 12/7 ≈ 1.714
- x₂ = 15/7 ≈ 2.143
- Valor máximo de Z = 120/7 ≈ 17.143


## Conclusão

Aplicando o método Simplex, encontramos que a solução ótima para o problema de programação linear é produzir aproximadamente 1.714 unidades do produto 1 e 2.143 unidades do produto 2, resultando em um valor máximo da função objetivo Z = 17.143.

O método Simplex mostrou-se eficiente, convergindo para a solução ótima em apenas duas iterações. As variáveis de folga s₁ e s₃ são zero na solução ótima, indicando que as restrições correspondentes são ativas (estão no limite), enquanto s₂ = 5.286, indicando que a segunda restrição não é ativa.

