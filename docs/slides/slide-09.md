# Aula 09 - C e C++: Baixo Nível 🧱

---

## Agenda 📅

1.  História e Importância <!-- .element: class="fragment" -->
2.  Anatomia de um Programa C <!-- .element: class="fragment" -->
3.  Compilação <!-- .element: class="fragment" -->
4.  Gerenciamento de Memória (Stack vs Heap) <!-- .element: class="fragment" -->
5.  Ponteiros <!-- .element: class="fragment" -->
6.  Introdução ao C++ (OOP) <!-- .element: class="fragment" -->

---

## 1. O Pai das Linguagens 👴

- **C (1972)**: Dennis Ritchie (Bell Labs). <!-- .element: class="fragment" -->
- **Base de Tudo**: Windows, Linux, Mac, Android, iOS. <!-- .element: class="fragment" -->
- **Filosofia**: "Confie no programador" (mesmo se ele fizer besteira). <!-- .element: class="fragment" -->

---

### Por que aprender C hoje? 🧐

- Entender como a máquina funciona de verdade. <!-- .element: class="fragment" -->
- Gerenciar memória manualmente. <!-- .element: class="fragment" -->
- Performance extrema (Jogos, Sistemas Embarcados). <!-- .element: class="fragment" -->

---

## 2. Anatomia Básica 🦴

```c
#include <stdio.h>

int main() {
    printf("Olá, Mundo C!");
    return 0;
}
```

---

### Desmontando o Código 🔧

1.  `#include <stdio.h>`: Importa biblioteca de IO (Entrada/Saída). <!-- .element: class="fragment" -->
2.  `int main()`: A função principal. Todo programa começa aqui. <!-- .element: class="fragment" -->
3.  `printf(...)`: Imprime formatado. <!-- .element: class="fragment" -->
4.  `return 0;`: Retorna "Sucesso" para o Sistema Operacional. <!-- .element: class="fragment" -->

---

### O Ponto e Vírgula `;`

- Em C/C++, ele é **OBRIGATÓRIO**. <!-- .element: class="fragment" -->
- O compilador não adivinha onde a linha termina. <!-- .element: class="fragment" -->
- Esquecer `;` é o erro nº 1 de iniciantes. <!-- .element: class="fragment" -->

---

## 3. O Processo de Compilação ⚙️

C é uma linguagem **Compilada**.

1.  **Código Fonte** (`.c`): Texto legível. <!-- .element: class="fragment" -->
2.  **Compilador** (`gcc`): Traduz para Assembly/Machine Code. <!-- .element: class="fragment" -->
3.  **Linker**: Junta com bibliotecas. <!-- .element: class="fragment" -->
4.  **Executável** (`.exe`): Programa final. <!-- .element: class="fragment" -->

---

## 4. Memória: Stack vs Heap 🧠

Onde seus dados moram?

---

### Visualizando a Memória

```mermaid
graph TD;
    subgraph RAM
    Stack["Stack (Pilha)"] --- V["Locais\nAutomáticas\nRápidas"];
    Heap["Heap (Monte)"] --- D["Dinâmicas\nManuais\nLentas"];
    end
    style Stack fill:#f9f;
    style Heap fill:#bbf;
```

---

### Stack (Pilha) 🥞

- Variáveis normais: `int idade = 20;` <!-- .element: class="fragment" -->
- Criada e destruída automaticamente. <!-- .element: class="fragment" -->
- Tamanho fixo e pequeno. <!-- .element: class="fragment" -->

---

### Heap (Monte) 🏔️

- Memória dinâmica: `malloc()` ou `new`. <!-- .element: class="fragment" -->
- Você pede memória ao sistema. <!-- .element: class="fragment" -->
- **Cuidado**: Você precisa devolver (`free` ou `delete`), senão vaza memória (Memory Leak)! <!-- .element: class="fragment" -->

---

## 5. Ponteiros: O Superpoder ⚡

Um ponteiro não guarda o valor. Guarda o **ENDEREÇO**.

- `int x = 10;` (Valor 10) <!-- .element: class="fragment" -->
- `int *p = &x;` (Endereço onde o 10 mora, ex: `0x7ffee4`) <!-- .element: class="fragment" -->

---

### Para que serve? 🤷

1.  Modificar variáveis originais dentro de funções. <!-- .element: class="fragment" -->
2.  Alocar memória dinâmica. <!-- .element: class="fragment" -->
3.  Criar estruturas complexas (Listas, Árvores). <!-- .element: class="fragment" -->

> "Com grandes poderes vêm grandes responsabilidades." (E Segmentation Faults).

---

## 6. Introdução ao C++ 🚀

C++ = C + Classes (OOP).

- Mantém a performance do C. <!-- .element: class="fragment" -->
- Adiciona organização de objetos. <!-- .element: class="fragment" -->
- Base para Jogos (Unreal) e Softwares Pesados (Chrome, Photoshop). <!-- .element: class="fragment" -->

---

### Exemplo C++ 🚗

```cpp
#include <iostream>
using namespace std;

class Carro {
public:
    void buzinar() {
        cout << "Bi Bi!" << endl;
    }
};

int main() {
    Carro meuCarro;
    meuCarro.buzinar();
    return 0;
}
```

---

### Diferenças C vs C++

| Feature | C | C++ |
| :--- | :--- | :--- |
| **Paradigma** | Estruturado | Orientado a Objetos (Multi) |
| **Output** | `printf()` | `cout <<` |
| **Input** | `scanf()` | `cin >>` |
| **Extensão** | `.c` | `.cpp` |

---

## Termynal: Compilando 🖥️

<div data-termynal class="termy">
    <span data-ty="input">gcc programa.c -o programa</span>
    <span data-ty="progress">Compilando...</span>
    <span data-ty="input">./programa</span>
    <span data-ty>Olá Mundo C!</span>
</div>

---

## Resumo ✅

- C é a mãe de todas. <!-- .element: class="fragment" -->
- **Compilador** traduz para binário. <!-- .element: class="fragment" -->
- **Ponteiros** acessam memória direta. <!-- .element: class="fragment" -->
- **C++** adiciona Classes ao poder do C. <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- Sair do "Baixo Nível". <!-- .element: class="fragment" -->
- Ir para o mundo corporativo e robusto. <!-- .element: class="fragment" -->
- **Java**: "Escreva uma vez, rode em qualquer lugar". <!-- .element: class="fragment" -->

👉 **Tarefa**: Instalar o Code::Blocks ou configurar GCC no VS Code!