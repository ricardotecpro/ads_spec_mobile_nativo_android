# Aula 14 - Testes, Qualidade e Debugging 🐞

!!! tip "Objetivo"
    **Objetivo**: Aprender a encontrar e corrigir erros de forma profissional, utilizar o Logcat e escrever testes automatizados (Unitários e de UI) para garantir a estabilidade do app.

---

## 1. O Logcat: Seu melhor amigo 📝

Esqueça o `println`. No Android, usamos a classe `Log` para monitorar o que acontece.

```kotlin
Log.v("TAG", "Verbose - Detalhes irrelevantes")
Log.d("TAG", "Debug - Informação para o dev")
Log.i("TAG", "Info - Evento importante (Login, etc)")
Log.w("TAG", "Warning - Algo estranho, mas não quebrou")
Log.e("TAG", "Error - QUEBROU! 💥")
```

No Android Studio, você pode filtrar logs pela TAG ou pelo nível de erro.

---

## 2. Debugging Passo a Passo 🛠️

Quando o app trava ou tem um comportamento estranho:
1.  Coloque um **Breakpoint** (clique na lateral da linha).
2.  Rode o app em modo **Debug** (Ícone do besouro).
3.  O app vai "congelar" naquela linha e você poderá ver o valor de todas as variáveis.

---

## 3. Pirâmide de Testes 🏔️

1.  **Testes Unitários (70%)**: Testam pequenas partes (funções) isoladas. São ultra-rápidos. Rodam no computador (JVM).
2.  **Testes de Integração (20%)**: Testam a conversa entre componentes (ex: ViewModel + Repositório).
3.  **Testes de UI / Instrumentados (10%)**: Testam o app rodando no emulador. Clicam em botões, abrem telas. (Ex: **Espresso**).

---

## 4. Escrevendo um Teste Unitário 🧪

Pasta: `src/test/java`

```kotlin
class CalculadoraTest {
    @Test
    fun soma_estaCorreta() {
        val result = Calculadora().somar(2, 2)
        assertEquals(4, result)
    }
}
```

### 🆚 Comparação: XCTest (iOS)
No iOS, usamos o framework `XCTest`. A lógica é a mesma: Criar uma classe de teste e usar métodos `assert` para verificar se o resultado bate com o esperado.

---

## 5. Testes de UI com Espresso ☕

O Espresso é a biblioteca padrão para testar a interface.

```kotlin
@Test
fun clicarNoBotao_deveMudarTexto() {
    onView(withId(R.id.btnEnviar)).perform(click())
    onView(withId(R.id.txtResultado)).check(matches(withText("Enviado!")))
}
```

---

## 6. Gerenciamento de Erros (Try/Catch) 🛡️

Nunca deixe o app fechar sozinho na mão do usuário.

```kotlin
try {
    val resultado = 10 / 0
} catch (e: ArithmeticException) {
    Log.e("AVISO", "Divisão por zero!", e)
    exibirMensagemAmigavel("Ops, algo deu errado.")
}
```

---

## 7. Desafio: O Caçador de Bugs 🕵️‍♂️

Vou te dar um código com 3 erros. Tente identificar quais são (mentalmente ou no AS):

```kotlin
var lista: List<String>? = null

fun main() {
    // Erro 1:
    println(lista.size) 
    
    // Erro 2:
    val num = "123a".toInt()
    
    // Erro 3 (UI):
    txtView.text = "Olá" // Tentando atualizar UI dentro de uma Thread comum?
}
```

??? success "Respostas"
    1.  **NullPointerException**: A lista é nula. Deveria usar `lista?.size`.
    2.  **NumberFormatException**: A string tem um 'a'. Deveria usar `toIntOrNull()`.
    3.  **CalledFromWrongThreadException**: UI só pode ser alterada na Main Thread.

---

## 🔗 Materiais da Aula

<div class="grid cards" markdown>
- :material-presentation: **Slides**

    ---

    Material visual com diagramas e conceitos-chave.

    [:octicons-arrow-right-24: Slide 14](../slides/slide-14.html)

- :material-help-circle: **Quiz**

    ---

    Teste seu conhecimento com 10 questões interativas.

    [:octicons-arrow-right-24: Quiz 14](../quizzes/quiz-14.md)

- :fontawesome-solid-pencil: **Exercícios**

    ---

    5 exercícios progressivos (básico → desafio).

    [:octicons-arrow-right-24: Exercício 14](../exercicios/exercicio-14.md)

- :material-briefcase-outline: **Projeto**

    ---

    Aplicação prática dos conceitos da aula.

    [:octicons-arrow-right-24: Projeto 14](../projetos/projeto-14.md)

</div>

---

[➡️ Próxima Aula: Aula 15](./aula-15.md){ .md-button .md-button--primary }
