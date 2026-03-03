# Aula 03 - Estrutura Sequencial ➡️

---

## Agenda 📅

1.  Variáveis (Revisão) <!-- .element: class="fragment" -->
2.  Tipos de Dados <!-- .element: class="fragment" -->
3.  Entrada e Saída <!-- .element: class="fragment" -->
4.  Operadores Aritméticos <!-- .element: class="fragment" -->
5.  Atribuição <!-- .element: class="fragment" -->

---

## 1. Variáveis: Caixas da Memória 📦

- Computador tem memória (RAM). <!-- .element: class="fragment" -->
- **Variável**: Um pedaço nomeado dessa memória. <!-- .element: class="fragment" -->
- Guardam **um valor** por vez. <!-- .element: class="fragment" -->

---

### Visualização 🧪

```mermaid
graph TD;
    Memoria[RAM] --> Var1[Gaveta 'IDADE'];
    Var1 --> Val1[Valor: 25];
    Memoria --> Var2[Gaveta 'NOME'];
    Var2 --> Val2["Valor: 'Maria'"];
```

---

## 2. Tipos de Dados 📐

Nem tudo cabe na mesma caixa.

1.  **Inteiro**: Números sem vírgula (10, -5). <!-- .element: class="fragment" -->
2.  **Real**: Números com vírgula (10.5, 3.14). <!-- .element: class="fragment" -->
3.  **Caractere**: Texto ("Olá", "A"). <!-- .element: class="fragment" -->
4.  **Lógico**: Verdadeiro ou Falso. <!-- .element: class="fragment" -->

---

### Erro Comum ❌

Tentar colocar texto numa caixa de número.

```visualg
Var
   idade : inteiro
Inicio
   idade <- "Vinte" // ERRO!
```

---

## 3. Entrada e Saída ⚙️

Como o programa fala com o usuário?

- **Entrada**: Dados que entram (Teclado). <!-- .element: class="fragment" -->
- **Saída**: Dados que saem (Tela). <!-- .element: class="fragment" -->

---

### Comando: ESCREVA (Saída) 📤

- Mostra texto na tela. <!-- .element: class="fragment" -->
- `escreva` (na mesma linha). <!-- .element: class="fragment" -->
- `escreval` (pula linha). <!-- .element: class="fragment" -->

```visualg
escreval("Olá Mundo")
escreva("Tudo bem?")
```

---

### Comando: LEIA (Entrada) 📥

- Pára o programa e espera o usuário digitar. <!-- .element: class="fragment" -->
- Guarda o que foi digitado numa variável. <!-- .element: class="fragment" -->

```visualg
escreva("Qual seu nome?")
leia(nome)
```

---

## 4. Atribuição (`<-`) ⬅️

- Colocar um valor dentro da variável. <!-- .element: class="fragment" -->
- Lê-se: "Recebe". <!-- .element: class="fragment" -->
- A seta sempre aponta para a esquerda (para a variável). <!-- .element: class="fragment" -->

```visualg
media <- (n1 + n2) / 2
nome <- "João"
```

---

## 5. Operadores Aritméticos 🧮

O computador é uma calculadora gigante.

| Operador | Nome | Exemplo |
| :---: | :--- | :--- |
| `+` | Soma | `5 + 3` |
| `-` | Subtração | `10 - 2` |
| `*` | Multiplicação | `4 * 3` |
| `/` | Divisão | `20 / 4` |

---

### Operadores Especiais ✨

- **Módulo (`%`)**: Resto da divisão. <!-- .element: class="fragment" -->
    - `5 % 2 = 1` (Sobrou 1). <!-- .element: class="fragment" -->
    - Útil para saber se é Par ou Ímpar. <!-- .element: class="fragment" -->
- **Potência (`^`)**: Elevar ao quadrado/cubo. <!-- .element: class="fragment" -->
    - `2 ^ 3 = 8`. <!-- .element: class="fragment" -->

---

## Ordem de Precedência 🥇

Matemática básica!

1.  Parênteses `( )` <!-- .element: class="fragment" -->
2.  Potência `^` <!-- .element: class="fragment" -->
3.  Multiplicação e Divisão `* /` <!-- .element: class="fragment" -->
4.  Soma e Subtração `+ -` <!-- .element: class="fragment" -->

> `2 + 3 * 4` = 14 (Não 20!)

---

## Exemplo Completo: Dobro do Número 🔢

Vamos criar um programa que lê um número e mostra o dobro.

---

### Passo 1: Definir Variáveis

```visualg
Algoritmo "Dobro"
Var
   numero : inteiro
   resultado : inteiro
```

---

### Passo 2: Entrada

```visualg
Inicio
   escreva("Digite um número: ")
   leia(numero)
```

---

### Passo 3: Processamento

```visualg
   resultado <- numero * 2
```

---

### Passo 4: Saída

```visualg
   escreval("O dobro é: ", resultado)
Fimalgoritmo
```

---

## Exercício Rápido ⚡

Faça no VisualG agora:
1.  Leia dois números. <!-- .element: class="fragment" -->
2.  Some os dois. <!-- .element: class="fragment" -->
3.  Mostre o resultado. <!-- .element: class="fragment" -->

---

## Resumo ✅

- **Variáveis**: Nome, Tipo e Valor. <!-- .element: class="fragment" -->
- **Tipos**: Inteiro, Real, Caractere, Lógico. <!-- .element: class="fragment" -->
- **Entrada**: `leia()`. <!-- .element: class="fragment" -->
- **Saída**: `escreva()`. <!-- .element: class="fragment" -->
- **Atribuição**: `<-`. <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- E se precisarmos tomar **decisões**? <!-- .element: class="fragment" -->
- O comando `SE`. <!-- .element: class="fragment" -->
- Estruturas Condicionais. <!-- .element: class="fragment" -->

👉 **Tarefa**: Terminar os exercícios da lista 03!