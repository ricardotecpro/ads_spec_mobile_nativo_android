# Aula 11 - Java e Orientação a Objetos ☕

---

## Agenda 📅

1.  O Mundo dos Objetos <!-- .element: class="fragment" -->
2.  Classes vs Objetos <!-- .element: class="fragment" -->
3.  Java e a JVM <!-- .element: class="fragment" -->
4.  Os 3 Pilares da OO <!-- .element: class="fragment" -->
5.  Spring Boot (Java Moderno) <!-- .element: class="fragment" -->

---

## 1. O Mundo Orientado a Objetos 🌍

Até agora, programamos **Ações** (Funções).
Mas o mundo é feito de **Coisas** (Objetos).

- **Estruturada**: Verbo (Fazer algo). <!-- .element: class="fragment" -->
- **OO**: Substantivo (Algo que faz). <!-- .element: class="fragment" -->

---

## 2. Classe vs Objeto 🏗️

A distinção mais importante.

- **Classe**: O Molde. A Planta. A Ideia. (Abstrato). <!-- .element: class="fragment" -->
- **Objeto**: A Instância. A Casa. A Coisa Real. (Concreto). <!-- .element: class="fragment" -->

---

### Visualizando (Mermaid)

```mermaid
classDiagram
    class Carro {
        +String cor
        +acelerar()
    }
    Ferrari --|> Carro : É um
    Fusca --|> Carro : É um
```

---

## 3. Java e a JVM ♻️

"Write Once, Run Anywhere" (Escreva uma vez, rode em qualquer lugar).

- O Java não compila para Binário direto. <!-- .element: class="fragment" -->
- Ele compila para **Bytecode** (`.class`). <!-- .element: class="fragment" -->
- A **JVM** (Máquina Virtual Java) roda esse Bytecode em qualquer sistema (Windows, Linux, Android, Geladeira). <!-- .element: class="fragment" -->

---

## 4. Os 3 Pilares da OO 🏛️

1.  Encapsulamento <!-- .element: class="fragment" -->
2.  Herança <!-- .element: class="fragment" -->
3.  Polimorfismo <!-- .element: class="fragment" -->

---

### Encapsulamento 🛡️

Proteger os dados. Ninguém mexe no cofre do banco direto.

- **Private**: Só a classe vê. <!-- .element: class="fragment" -->
- **Public**: Todo mundo vê. <!-- .element: class="fragment" -->
- **Getters/Setters**: Porteiros que controlam o acesso. <!-- .element: class="fragment" -->

```java
private double saldo;

public void depositar(double valor) {
    if (valor > 0) saldo += valor;
}
```

---

### Herança 🧬

Reaproveitar código.

- `Cachorro` **é um** `Animal`. <!-- .element: class="fragment" -->
- `Gato` **é um** `Animal`. <!-- .element: class="fragment" -->
- Tudo que `Animal` tem, eles herdam (nome, idade). <!-- .element: class="fragment" -->

```java
public class Cachorro extends Animal { ... }
```

---

### Polimorfismo 🎭

Muitas formas.

- O método `fazerSom()` existe em Animal. <!-- .element: class="fragment" -->
- No Cachorro, ele faz "Au Au". <!-- .element: class="fragment" -->
- No Gato, ele faz "Miau". <!-- .element: class="fragment" -->
- O mesmo método se comporta diferente. <!-- .element: class="fragment" -->

---

## 5. Spring Boot 🍃

Java não é só "tela preta".
É a linguagem nº 1 em Bancos e Grandes Empresas.

- **Spring Boot**: Framework para criar APIs Web. <!-- .element: class="fragment" -->
- Tira toda a configuração chata. <!-- .element: class="fragment" -->

---

### Exemplo de API

```java
@RestController
public class OlaController {
    
    @GetMapping("/ola")
    public String dizerOla() {
        return "Olá, Mundo Java Web!";
    }
}
```

---

## Exercício Mental 🧠

Modele um sistema de **Venda**.

- Classes: `Produto`, `Cliente`, `Venda`. <!-- .element: class="fragment" -->
- Atributos: `Preco`, `Nome`. <!-- .element: class="fragment" -->
- Métodos: `CalcularTotal()`, `Pagar()`. <!-- .element: class="fragment" -->

---

## Resumo ✅

- **Classe** é molde, **Objeto** é real. <!-- .element: class="fragment" -->
- **JVM** garante portabilidade. <!-- .element: class="fragment" -->
- **Encapsulamento** protege. <!-- .element: class="fragment" -->
- **Herança** reutiliza. <!-- .element: class="fragment" -->
- **Polimorfismo** flexibiliza. <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- O concorrente direto do Java. <!-- .element: class="fragment" -->
- Criado pela Microsoft. <!-- .element: class="fragment" -->
- **C# e plataforma .NET**. <!-- .element: class="fragment" -->
- Foco em produtividade. <!-- .element: class="fragment" -->

👉 **Tarefa**: Instalar o JDK (Java Development Kit) e o VS Code Extension Pack for Java!