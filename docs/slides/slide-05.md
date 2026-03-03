# Aula 05 - Estruturas Repetitivas 🔁

---

## Agenda 📅

1.  O Poder da Repetição (Loops) <!-- .element: class="fragment" -->
2.  Estrutura Enquanto (While) <!-- .element: class="fragment" -->
3.  Estrutura Repita (Do-While) <!-- .element: class="fragment" -->
4.  Estrutura Para (For) <!-- .element: class="fragment" -->
5.  Controle de Fluxo (Interrompa) <!-- .element: class="fragment" -->
6.  Teste de Mesa <!-- .element: class="fragment" -->

---

## 1. O Poder da Repetição 🔄

Imagine escrever "Eu não vou jogar bolinha de papel" 100 vezes no quadro.

- **Humano**: Cansa, erra, demora. <!-- .element: class="fragment" -->
- **Computador**: Faz em 1 milissegundo. <!-- .element: class="fragment" -->

---

### O Loop (Laço) ♾️

- Executa um bloco de código **enquanto** uma condição for verdadeira. <!-- .element: class="fragment" -->
- Automatiza tarefas repetitivas. <!-- .element: class="fragment" -->
- Economiza linhas de código. <!-- .element: class="fragment" -->

---

### Visualizando um Loop

```mermaid
graph TD;
    Inicio([Início]) --> Cond{Contador < 5?};
    Cond -- Sim --> Acao["Escrever 'Olá'"];
    Acao --> Inc[Contador + 1];
    Inc --> Cond;
    Cond -- Não --> Fim([Fim]);
```

---

## 2. Enquanto (While) ⏳

- O mais comum. <!-- .element: class="fragment" -->
- Testa a condição **ANTES** de entrar. <!-- .element: class="fragment" -->
- Se a condição for falsa de cara, ele nunca executa. <!-- .element: class="fragment" -->

---

### Sintaxe

```visualg
enquanto (condicao) faca
   // Comandos
fimenquanto
```

---

### Exemplo: Contagem

```visualg
i <- 0
enquanto (i < 5) faca
   escreval("Número: ", i)
   i <- i + 1  // Importante!
fimenquanto
```

> Se esquecer o `i <- i + 1`, vira um **Loop Infinito**! 😱

---

## 3. Repita-Até (Do-While) 🛡️

- Testa a condição no **FINAL**. <!-- .element: class="fragment" -->
- Executa **pelo menos uma vez**. <!-- .element: class="fragment" -->
- Ótimo para menus ou validação. <!-- .element: class="fragment" -->

---

### Sintaxe

```visualg
repita
   // Comandos
ate (condicao)
```

**Atenção**: No VisualG/Portugol, ele repete *até* a condição ser verdadeira (ou seja, enquanto for falsa). Em outras linguagens (C, Java), é *enquanto* for verdadeira.

---

### Exemplo: Senha Correta 🔒

```visualg
repita
   escreva("Digite a senha: ")
   leia(senha)
ate (senha == "1234")
```

---

## 4. Para (For) 🎯

- Quando sabemos **exatamente** quantas vezes repetir. <!-- .element: class="fragment" -->
- Agrupa tudo numa linha só: <!-- .element: class="fragment" -->
    1.  **Início** (Onde começa) <!-- .element: class="fragment" -->
    2.  **Fim** (Onde termina) <!-- .element: class="fragment" -->
    3.  **Passo** (De quanto em quanto) <!-- .element: class="fragment" -->

---

### Sintaxe

```visualg
para i de 1 ate 10 passo 1 faca
   escreva(i)
fimpara
```

- **i**: Variável contadora. <!-- .element: class="fragment" -->
- **1**: Valor inicial. <!-- .element: class="fragment" -->
- **10**: Valor final. <!-- .element: class="fragment" -->
- **1**: Incremento. <!-- .element: class="fragment" -->

---

### Exemplo: Contagem Regressiva 🚀

```visualg
para i de 10 ate 0 passo -1 faca
   escreval(i)
fimpara
escreval("FOGO!")
```

---

## 5. Controle de Fluxo (Interrompa) 🛑

- Sai do loop imediatamente. <!-- .element: class="fragment" -->
- Útil para parar buscas ou sair de menus. <!-- .element: class="fragment" -->

```visualg
enquanto (verdadeiro) faca
   se (botao == "Sair") entao
      interrompa
   fimse
fimenquanto
```

---

## 6. O Teste de Mesa 🧠

Como debugar mentalmente?

1.  Crie uma tabela com as variáveis. <!-- .element: class="fragment" -->
2.  Simule linha por linha. <!-- .element: class="fragment" -->
3.  Anote as mudanças. <!-- .element: class="fragment" -->

| Passo | i | Saída |
| :--- | :--- | :--- |
| 1 | 0 | - |
| 2 | 0 | "0" |
| 3 | 1 | - |
| ... | ... | ... |

---

## Comparativo ⚖️

| Estrutura | Quando usar? |
| :--- | :--- |
| **Enquanto** | Não sei quantas vezes vai repetir. |
| **Repita** | Tenho que executar pelo menos 1 vez. |
| **Para** | Sei exatamente o número de repetições. |

---

## Exercício Rápido ⚡

**Tabuada do 7**

1.  Use um `para`. <!-- .element: class="fragment" -->
2.  De 1 até 10. <!-- .element: class="fragment" -->
3.  Mostre `7 x i = resultado`. <!-- .element: class="fragment" -->

---

## Resumo ✅

- **Loops** economizam tempo. <!-- .element: class="fragment" -->
- **Cuidado** com Loops Infinitos. <!-- .element: class="fragment" -->
- Escolha a estrutura certa para o problema. <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- E para guardar 50 notas de alunos? <!-- .element: class="fragment" -->
- Criar 50 variáveis? `n1, n2, n3...`? 😫 <!-- .element: class="fragment" -->
- **Vetores (Arrays)**: A solução elegante. <!-- .element: class="fragment" -->

👉 **Tarefa**: Fazer a Tabuada e o Primo!