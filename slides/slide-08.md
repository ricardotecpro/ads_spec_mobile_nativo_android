# Aula 08 - Modularização 🧩

---

## Agenda 📅

1.  Conceito de Módulos (Divide & Conquer) <!-- .element: class="fragment" -->
2.  Procedimentos vs Funções <!-- .element: class="fragment" -->
3.  Escopo de Variáveis (Locais x Globais) <!-- .element: class="fragment" -->
4.  Parâmetros (Valor x Referência) <!-- .element: class="fragment" -->
5.  Exemplos Práticos <!-- .element: class="fragment" -->

---

## 1. Dividir para Conquistar ⚔️

Imagine construir um carro inteiro num bloco só. Impossível!
Nós montamos:
- Motor 🔧 <!-- .element: class="fragment" -->
- Rodas 🚗 <!-- .element: class="fragment" -->
- Vidros 🪟 <!-- .element: class="fragment" -->
E depois **juntamos**.

---

### Na Programação

- Não escreva 1000 linhas no `Inicio`. <!-- .element: class="fragment" -->
- Quebre em pequenos blocos (**Módulos**). <!-- .element: class="fragment" -->
- Cada módulo resolve **um problema específico**. <!-- .element: class="fragment" -->

---

### Visualizando (Mermaid)

```mermaid
sequenceDiagram
    participant Principal
    participant Soma
    
    Principal->>Soma: Envia (5, 3)
    Note right of Soma: Calcula 5+3
    Soma-->>Principal: Retorna 8
    Principal->>Principal: Mostra 8
```

---

## 2. Tipos de Módulos 🛠️

Em Portugol, temos dois tipos principais.

1.  **Procedimentos**: Fazem uma ação, mas não devolvem valor matemático. <!-- .element: class="fragment" -->
2.  **Funções**: Calculam e **RETORNAM** um valor. <!-- .element: class="fragment" -->

---

### Procedimento (Ação)

Ex: `LimparTela()`, `MostrarMenu()`, `TocarSom()`.

```portugol
procedimento saudacao(nome : caractere)
inicio
   escreval("Olá, ", nome)
fimprocedimento
```
> Chamada: `saudacao("João")`

---

### Função (Cálculo)

Ex: `Raiz(x)`, `Soma(a,b)`, `Media(n1,n2)`.
Tem a palavra mágica **RETORNE**.

```portugol
funcao somar(a, b : inteiro) : inteiro
inicio
   retorne a + b
fimfuncao
```
> Chamada: `res <- somar(2, 3)`

---

## 3. Escopo de Variáveis 🏠

Onde minha variável vive?

- **Global**: Criada fora de tudo. Todo mundo vê. (Perigoso!). <!-- .element: class="fragment" -->
- **Local**: Criada dentro da função. Só a função vê. (Seguro!). <!-- .element: class="fragment" -->

---

### O Muro das Funções 🧱

Se eu crio `x` dentro de `somar`, o `Principal` **não sabe** quem é `x`.
Isso evita confusão!

---

## 4. Parâmetros 🚚

Como passar dados para a função?

1.  **Por Valor** (O padrão): Envia uma **CÓPIA**. Se a função mudar, o original não muda. <!-- .element: class="fragment" -->
2.  **Por Referência** (`var`): Envia o **ENDEREÇO**. Se a função mudar, o original MUDA! <!-- .element: class="fragment" -->

---

### Exemplo: Troca de Valores

Precisa ser por Referência!

```portugol
procedimento troca(var a, var b : inteiro)
inicio
   temp <- a
   a <- b
   b <- temp
fimprocedimento
```

---

## 5. Vantagens da Modularização ✅

1.  **Reutilização**: Escreve uma vez, usa 1000 vezes. <!-- .element: class="fragment" -->
2.  **Organização**: Código limpo. <!-- .element: class="fragment" -->
3.  **Facilidade de Manutenção**: Se o cálculo mudar, corrijo num lugar só. <!-- .element: class="fragment" -->

---

## Projeto Final Módulo 1 🏆

**Sistema de Notas Completo**

- Use Vetores. <!-- .element: class="fragment" -->
- Use Matrizes (se quiser). <!-- .element: class="fragment" -->
- Use Funções para calcular média. <!-- .element: class="fragment" -->
- Use Procedimentos para mostrar boletim. <!-- .element: class="fragment" -->

---

## Resumo ✅

- Modularizar = Organizar. <!-- .element: class="fragment" -->
- **Função** retorna valor. **Procedimento** faz ação. <!-- .element: class="fragment" -->
- Variáveis **Locais** são protegidas. <!-- .element: class="fragment" -->
- Use parâmetros para comunicar. <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- Fim da "Lógica Pura"! <!-- .element: class="fragment" -->
- Vamos conhecer linguagens reais. <!-- .element: class="fragment" -->
- **C e C++**: Os pais da programação moderna. <!-- .element: class="fragment" -->
- Gerenciamento de Memória na unha! <!-- .element: class="fragment" -->

👉 **Tarefa**: Refatore seus códigos antigos usando Funções!