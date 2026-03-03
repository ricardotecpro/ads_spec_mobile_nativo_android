# Aula 16 - PHP e o Lado do Servidor 🐘

---

## Agenda 📅

1.  Como a Web Funciona? <!-- .element: class="fragment" -->
2.  PHP: O Motor da Internet <!-- .element: class="fragment" -->
3.  Arquitetura MVC <!-- .element: class="fragment" -->
4.  Laravel (Framework) <!-- .element: class="fragment" -->
5.  Projeto Final <!-- .element: class="fragment" -->

---

## 1. O Ciclo da Web 🌍

Client vs Server.

- **Cliente (Browser)**: Pede coisas (Request). <!-- .element: class="fragment" -->
- **Servidor**: Processa e Devolve (Response). <!-- .element: class="fragment" -->
- **Banco de Dados**: Guarda as informações. <!-- .element: class="fragment" -->

---

### Requisição e Resposta (Sequence)

```mermaid
sequenceDiagram
    participant Browser
    participant Servidor
    participant Banco
    
    Browser->>Servidor: 1. GET /perfil
    Servidor->>Banco: 2. SELECT * FROM users
    Banco-->>Servidor: 3. Dados (João, 25)
    Servidor-->>Browser: 4. HTML Pronto
```

---

## 2. O Que é PHP? 🐘

**P**HP: **H**ypertext **P**reprocessor.

- Roda no Servidor (Back-end). <!-- .element: class="fragment" -->
- Gera HTML dinâmico. <!-- .element: class="fragment" -->
- Fácil de hospedar (qualquer servidor barato tem). <!-- .element: class="fragment" -->
- Poderoso (Facebook, Wikipedia, WordPress). <!-- .element: class="fragment" -->

---

### Código PHP

```php
<?php
    $nome = "Maria";
    $saldo = 100.50;
    
    echo "<h1>Olá, $nome!</h1>";
    echo "<p>Saldo: $saldo</p>";
?>
```

---

## 3. Arquitetura MVC 🏗️

Para organizar sites grandes, não misturamos código.

- **M**odel (Modelo): Dados e Banco. <!-- .element: class="fragment" -->
- **V**iew (Visão): HTML e Telas. <!-- .element: class="fragment" -->
- **C**ontroller (Controlador): A Lógica. <!-- .element: class="fragment" -->

---

### Fluxo MVC

```mermaid
graph LR;
    User -->|Rota| Controller;
    Controller -->|Pede| Model;
    Model -->|Devolve| Controller;
    Controller -->|Envia| View;
    View -->|HTML| User;
```

---

## 4. Laravel 🚀

O Framework PHP mais popular.

- Sintaxe elegante. <!-- .element: class="fragment" -->
- Ferramentas prontas (Login, Email, Banco). <!-- .element: class="fragment" -->
- "O PHP Moderno". <!-- .element: class="fragment" -->

```php
// Rota simples em Laravel
Route::get('/', function () {
    return view('welcome');
});
```

---

## Projeto Final do Curso 🏆

**Mural de Recados Fullstack**

- **Banco**: MySQL (`recados`: id, mensagem). <!-- .element: class="fragment" -->
- **Back**: PHP (Busca recados). <!-- .element: class="fragment" -->
- **Front**: HTML/CSS (Mostra recados). <!-- .element: class="fragment" -->
- Use tudo que aprendeu: Lógica, Loops, Vetores (Dados do banco), HTML. <!-- .element: class="fragment" -->

---

## Termynal: Servidor PHP 🖥️

<div data-termynal class="termy">
    <span data-ty="input">php -S localhost:8000</span>
    <span data-ty="progress">Listening on localhost:8000...</span>
    <span data-ty>Requisição recebida: /index.php</span>
    <span data-ty>200 OK</span>
</div>

---

## Resumo do Módulo ✅

1.  **Lógica**: Algoritmos, Fluxogramas. <!-- .element: class="fragment" -->
2.  **Dados**: Variáveis, Vetores, Matrizes. <!-- .element: class="fragment" -->
3.  **Tecnologias**: <!-- .element: class="fragment" -->
    - Baixo nível (C/C++). <!-- .element: class="fragment" -->
    - Web (JS, PHP). <!-- .element: class="fragment" -->
    - Mobile (Flutter). <!-- .element: class="fragment" -->
    - Corporativo (Java, C#). <!-- .element: class="fragment" -->

---

## Parabéns! 🎓

Você completou a jornada de Lógica e Algoritmos.
Você agora tem a **base** para aprender qualquer linguagem.

**Próximos Passos?**
- Escolha uma área (Front, Back, Mobile, Dados). <!-- .element: class="fragment" -->
- Aprofunde-se na linguagem escolhida. <!-- .element: class="fragment" -->
- **PRATIQUE!** <!-- .element: class="fragment" -->

👉 **Projeto Final**: Entregar o Mural de Recados!