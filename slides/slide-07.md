# Aula 07 - Estruturas de Dados II: Matrizes 📈

---

## Agenda 📅

1.  O Mundo em 2D <!-- .element: class="fragment" -->
2.  O Que é uma Matriz? <!-- .element: class="fragment" -->
3.  Coordenadas (Linha x Coluna) <!-- .element: class="fragment" -->
4.  Percorrendo Matrizes <!-- .element: class="fragment" -->
5.  Aplicações Práticas <!-- .element: class="fragment" -->

---

## 1. O Mundo em 2D 🗺️

Nem tudo cabe numa lista (Vetor).

- Uma sala de cinema. <!-- .element: class="fragment" -->
- Um tabuleiro de xadrez. <!-- .element: class="fragment" -->
- Uma planilha do Excel. <!-- .element: class="fragment" -->
- Precisamos de **2 Dimensões**: Altura e Largura. <!-- .element: class="fragment" -->

---

## 2. O Que é uma Matriz? 🏗️

- É um **"Vetor de Vetores"**. <!-- .element: class="fragment" -->
- Tem Linhas (Horizontais) e Colunas (Verticais). <!-- .element: class="fragment" -->
- Cada "casinha" tem um endereço duplo. <!-- .element: class="fragment" -->

---

### Visualizando uma Matriz

```mermaid
graph TD;
    subgraph Matriz [3x3]
    direction TB
    L0[Linha 0] --- C00[0,0] --- C01[0,1] --- C02[0,2]
    L1[Linha 1] --- C10[1,0] --- C11[1,1] --- C12[1,2]
    L2[Linha 2] --- C20[2,0] --- C21[2,1] --- C22[2,2]
    end
```

---

## 3. Coordenadas (Linha, Coluna) 📍

Assim como na Batalha Naval: `B4`, `A1`.
Na programação, usamos índices numéricos.

- `matriz[LINHA][COLUNA]` <!-- .element: class="fragment" -->
- Sempre **LINHA primeiro**, depois COLUNA. <!-- .element: class="fragment" -->

---

### Sintaxe VisualG

```portugol
Var
   // 3 Linhas, 3 Colunas
   tabuleiro : vetor [0..2, 0..2] de inteiro
Inicio
   // Colocando valor no centro
   tabuleiro[1][1] <- 5
   
   // Canto superior esquerdo
   tabuleiro[0][0] <- 1
```

---

## 4. Percorrendo uma Matriz 🔄🔄

Se um vetor precisa de 1 loop, a matriz precisa de **2 Loops Aninhados**.

1.  O primeiro trava a **Linha**. <!-- .element: class="fragment" -->
2.  O segundo percorre todas as **Colunas** daquela linha. <!-- .element: class="fragment" -->

---

### O Código Padrão

```portugol
para i de 0 ate 2 faca  // Linhas
   para j de 0 ate 2 faca  // Colunas
      escreva("Posição [", i, ",", j, "]: ")
      leia(matriz[i][j])
   fimpara
fimpara
```

---

### Visualizando a Execução

1.  `i=0, j=0` -> [0,0] <!-- .element: class="fragment" -->
2.  `i=0, j=1` -> [0,1] <!-- .element: class="fragment" -->
3.  `i=0, j=2` -> [0,2] -> Fim das Colunas. <!-- .element: class="fragment" -->
4.  `i=1, j=0` -> [1,0] -> Nova Linha! <!-- .element: class="fragment" -->

---

## 5. Matriz Identidade 🆔

Um clássico da matemática.
Diagonal Principal = 1. Resto = 0.

- A Diagonal Principal acontece quando `i == j` (0,0; 1,1; 2,2). <!-- .element: class="fragment" -->

```portugol
se (i == j) entao
   matriz[i][j] <- 1
senao
   matriz[i][j] <- 0
fimse
```

---

## 6. Aplicações Reais 🌍

Onde usamos isso?

1.  **Imagens**: Cada pixel é uma célula com cor (RGB). <!-- .element: class="fragment" -->
2.  **Jogos**: O mapa do jogo (Tilemap). <!-- .element: class="fragment" -->
3.  **Gráficos 3D**: Matrizes de transformação. <!-- .element: class="fragment" -->

---

## Exercício Rápido ⚡

**Soma Total**

1.  Crie uma matriz 2x2. <!-- .element: class="fragment" -->
2.  Preencha com números. <!-- .element: class="fragment" -->
3.  Use dois loops para somar TUDO. <!-- .element: class="fragment" -->
4.  Mostre o total. <!-- .element: class="fragment" -->

---

## Resumo ✅

- Matriz = Linhas x Colunas. <!-- .element: class="fragment" -->
- Declaração: `vetor [L..L, C..C]`. <!-- .element: class="fragment" -->
- Acesso: `mat[linha][coluna]`. <!-- .element: class="fragment" -->
- Percorrer: 2 loops `Para`. <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- Nossos códigos estão ficando grandes... <!-- .element: class="fragment" -->
- Como organizar? <!-- .element: class="fragment" -->
- **Modularização**: Dividir para Conquistar. <!-- .element: class="fragment" -->
- Funções e Procedimentos. <!-- .element: class="fragment" -->

👉 **Tarefa**: Jogue Batalha Naval (no papel ou no código)!