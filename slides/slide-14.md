# Aula 14 - Sistemas Modernos: Rust e Go 🦀🐹

---

## Agenda 📅

1.  O Problema do C/C++ <!-- .element: class="fragment" -->
2.  Rust: Segurança de Memória <!-- .element: class="fragment" -->
3.  Go: Concorrência Simples <!-- .element: class="fragment" -->
4.  Comparativo <!-- .element: class="fragment" -->
5.  Quando usar? <!-- .element: class="fragment" -->

---

## 1. O Problema do C/C++ 💥

- C/C++ são rápidos, mas perigosos. <!-- .element: class="fragment" -->
- **70% das vulnerabilidades** de segurança são erros de memória (Microsoft). <!-- .element: class="fragment" -->
- Buffer Overflow, Use-After-Free. <!-- .element: class="fragment" -->

---

## 2. Rust 🦀

- Criada pela Mozilla. <!-- .element: class="fragment" -->
- Promessa: **Performance de C++ com Segurança de Memória**. <!-- .element: class="fragment" -->
- Sem Garbage Collector (GC). <!-- .element: class="fragment" -->
- Sem Tela Azul. <!-- .element: class="fragment" -->

---

### O Segredo: Ownership (Posse) 🔑

- Cada dado tem **um único dono**. <!-- .element: class="fragment" -->
- Quando o dono muda, o antigo perde o acesso. <!-- .element: class="fragment" -->
- O compilador verifica isso **antes** de rodar. <!-- .element: class="fragment" -->

---

### Visualizando Ownership

```mermaid
graph LR;
    A["Variável A\n(Dona do Dado)"] -- "Move" --> B["Variável B\n(Nova Dona)"];
    style A fill:#f9f;
    style B fill:#bbf;
    
    NoteA["A morre.\nNão pode mais acessar!"] --- A
```

---

### Código Rust

```rust
fn main() {
    let a = String::from("Olá");
    let b = a; // MOVEU para b
    
    // println!("{}", a); // ERRO DE COMPILAÇÃO!
    // O compilador te salva de usar memória inválida.
}
```

---

## 3. Go (Golang) 🐹

- Criada pelo Google (Rob Pike, Ken Thompson). <!-- .element: class="fragment" -->
- Foco: **Simplicidade** e **Google Scale**. <!-- .element: class="fragment" -->
- Compila ultra-rápido. <!-- .element: class="fragment" -->

---

### Concorrência Fácil (Goroutines) 🧵

- Threads são pesadas. <!-- .element: class="fragment" -->
- Goroutines são leves (milhares em poucos MBs). <!-- .element: class="fragment" -->
- **Channels**: Forma segura de conversar entre processos. <!-- .element: class="fragment" -->

---

### Visualizando Channels

```mermaid
graph LR;
    T1[Goroutine A] -->|Envia 'Ping'| Canal((Channel));
    Canal -->|Recebe 'Ping'| T2[Goroutine B];
    
    style Canal fill:#ff9;
```

---

### Código Go

```go
package main
import "fmt"

func main() {
    mensagens := make(chan string)

    go func() { mensagens <- "Ping" }()

    msg := <-mensagens
    fmt.Println(msg)
}
```

---

## 4. Comparativo ⚖️

| Feature | Rust 🦀 | Go 🐹 |
| :--- | :--- | :--- |
| **Foco** | Controle, Segurança Absoluta | Simplicidade, Web Services |
| **Aprendizado** | Curva Íngreme (Dificil) | Muito Fácil |
| **Performance** | Extrema (Zero-Cost) | Muito Boa (Com GC) |
| **Uso** | Drivers, Engines, Crypto | Microservices, Cloud, APIs |

---

## Termynal: Execução 🖥️

<div data-termynal class="termy">
    <span data-ty="input">cargo run</span>
    <span data-ty="progress">Compiling...</span>
    <span data-ty>Hello Rust! (Safe)</span>
    <span data-ty="input">go run main.go</span>
    <span data-ty>Hello Go! (Fast Build)</span>
</div>

---

## Resumo ✅

- **Rust**: Substitui C++ onde segurança é crítica. <!-- .element: class="fragment" -->
- **Go**: Substitui Java/Node onde concorrência é crítica. <!-- .element: class="fragment" -->
- Ambas são o futuro da Infraestrutura (Docker, Kubernetes). <!-- .element: class="fragment" -->

---

## Próxima Aula 🚀

- Sair do Servidor. <!-- .element: class="fragment" -->
- Ir para o dispositivo que está na sua mão. <!-- .element: class="fragment" -->
- **Desenvolvimento Mobile**: Flutter (Dart) e Nativo. <!-- .element: class="fragment" -->

👉 **Tarefa**: Instalar o Go e rodar um "Olá Mundo"!