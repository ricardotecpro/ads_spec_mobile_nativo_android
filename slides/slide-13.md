# Aula 13 - Python e Ciência de Dados 🐍

---

## Agenda 📅

1.  Por que Python? <!-- .element: class="fragment" -->
2.  Sintaxe Limpa <!-- .element: class="fragment" -->
3.  Estruturas de Dados Poderosas <!-- .element: class="fragment" -->
4.  Modo Interativo (REPL) vs Scripts <!-- .element: class="fragment" -->
5.  O Ecossistema de Data Science <!-- .element: class="fragment" -->

---

## 1. Por que Python? 🚀

- **Legibilidade**: Parece inglês. <!-- .element: class="fragment" -->
- **Produtividade**: Menos linhas, mais resultado. <!-- .element: class="fragment" -->
- **Ecossistema**: IA, Data Science, Web, Automação. <!-- .element: class="fragment" -->
- Não é o mais rápido (em CPU), mas é o mais rápido para **desenvolver**. <!-- .element: class="fragment" -->

---

## 2. Sintaxe Limpa ✨

Esqueça `{}` e `;`.

- **Indentação** (espaços) define os blocos. <!-- .element: class="fragment" -->
- Força o código a ser organizado. <!-- .element: class="fragment" -->

```python
if idade >= 18:
    print("Maior")
else:
    print("Menor")
```

---

## 3. Estruturas de Dados 🧱

Em vez de Arrays e Matrizes chatos de declarar, temos **Listas** e **Dicionários**.

---

### Listas (Arrays Turbinados)

```python
frutas = ["Maçã", "Banana", "Uva"]
print(frutas[0]) # Maçã
frutas.append("Pera") # Adiciona no fim
```

---

### Dicionários (Chave-Valor) 🔑

Como um JSON ou um Objeto.

```python
pessoa = {
    "nome": "Ana",
    "idade": 25,
    "tech": ["Python", "SQL"]
}
print(pessoa["nome"])
```

---

### Visualizando (Mermaid)

```mermaid
graph LR;
    subgraph Lista [Lista: Compras]
    L0[0: Maçã] --- L1[1: Banana] --- L2[2: Uva]
    end
    
    subgraph Dicionario [Dicionário: Pessoa]
    D1[Chave: 'Nome'\nValor: 'Ana'] --- D2[Chave: 'Idade'\nValor: 25]
    end
    
    style Lista fill:#bbf;
    style Dicionario fill:#f9f;
```

---

## 4. Modos de Execução ⚙️

1.  **REPL (Interativo)**: <!-- .element: class="fragment" -->
    - Digite `python` no terminal. <!-- .element: class="fragment" -->
    - Teste comandos na hora. `2 + 2`. <!-- .element: class="fragment" -->
    - Ótimo para aprender. <!-- .element: class="fragment" -->

2.  **Scripts (`.py`)**: <!-- .element: class="fragment" -->
    - Arquivos de texto com código. <!-- .element: class="fragment" -->
    - `python meu_script.py`. <!-- .element: class="fragment" -->
    - Para programas reais. <!-- .element: class="fragment" -->

---

## 5. O Ecossistema de Dados 📊

Por que Data Science ama Python? **Bibliotecas**.

1.  **Pandas**: O "Excel" do programador. Manipula milhões de linhas. <!-- .element: class="fragment" -->
2.  **Matplotlib**: Cria gráficos (Barras, Linhas, Pizza). <!-- .element: class="fragment" -->
3.  **TensorFlow/PyTorch**: Inteligência Artificial. <!-- .element: class="fragment" -->

---

### Exemplo Pandas 🐼

```python
import pandas as pd

# Ler uma planilha inteira
tabela = pd.read_csv("vendas.csv")

# Calcular totais
print(tabela["valor"].sum())
```

---

## Exercício Rápido ⚡

**Análise de Notas**

1.  Crie uma lista com 4 notas: `[6.0, 7.5, 9.0, 5.5]`. <!-- .element: class="fragment" -->
2.  Use `sum(lista)` e `len(lista)` para calcular a média. <!-- .element: class="fragment" -->
3.  Se média > 6, imprima "Aprovado". <!-- .element: class="fragment" -->

```python
notas = [6.0, 7.5, 9.0, 5.5]
media = sum(notas) / len(notas)
# Complete...
```

---

## Resumo ✅

- Python é a linguagem da prototipagem e dos dados. <!-- .element: class="fragment" -->
- **Indentação** é regra. <!-- .element: class="fragment" -->
- **Bibliotecas** fazem o trabalho pesado. <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- E quando performance é tudo? <!-- .element: class="fragment" -->
- Sistemas que não podem travar. <!-- .element: class="fragment" -->
- **Rust e Go**: As linguagens da Cloud e Sistemas. <!-- .element: class="fragment" -->

👉 **Tarefa**: Instalar Python e fazer o exercício da média!