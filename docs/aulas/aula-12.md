# Aula 12 - UX/UI e Material Design 3 🎨

!!! tip "Objetivo"
    **Objetivo**: Elevar a qualidade visual do app seguindo os padrões do Google (Material Design 3), entendendo temas, cores dinâmicas e componentes modernos.

---

## 1. O que é Material Design? 💄

É o sistema de design do Google (criado em 2014, agora na versão 3 - "Material You").
Ele imita "papel e tinta" (sombras, elevação) mas com cores vibrantes e adaptáveis.

*   **Princípio**: O design deve se adaptar ao usuário, não o contrário.
*   **Foco**: Legibilidade, Acessibilidade e consistência.

### 🆚 Comparação: HIG (Human Interface Guidelines)
A Apple tem o **HIG**.
*   **Material (Android)**: Mais colorido, elevação (sombras), Botões FAB (flutuantes), interação mais "brincalhona".
*   **HIG (iOS)**: Mais plano (flat), minimalista, foco no conteúdo, desfoque (blur).

---

## 2. Material 3 (Material You) 🌸

A grande novidade é o **Dynamic Color**. O App pega as cores do papel de parede do usuário e aplica no tema dele.
Se meu wallpaper é verde, todos os botões do seu app ficam verdes (se configurado).

### Componentes Chave

1.  **FAB (Floating Action Button)**: Botão flutuante para ação principal.
2.  **Bottom Navigation**: Barra inferior para navegação principal.
3.  **Cards**: Conteúdo agrupado com bordas arredondadas.
4.  **TopAppBar**: Barra superior (antiga Toolbar).

---

## 3. Implementando Material no Android 🛠️

Certifique-se de usar a biblioteca correta no `build.gradle`:
`implementation 'com.google.android.material:material:1.x.x'`

### XML - Botão Material
```xml
<com.google.android.material.button.MaterialButton
    style="@style/Widget.Material3.Button.Tonal"
    android:text="Botão Moderno" ... />
```

### XML - Card
```xml
<com.google.android.material.card.MaterialCardView
    app:cardCornerRadius="16dp"
    app:strokeWidth="1dp"
    app:strokeColor="@color/material_dynamic_primary" ... >
    
    <!-- Conteúdo do card aqui -->
    
</com.google.android.material.card.MaterialCardView>
```

---

## 4. Ícones e Tipografia 🔡

*   **Ícones**: Use **Vector Assets** (SVG). O Android Studio tem uma biblioteca gigante de ícones embutida. (File > New > Vector Asset).
*   **Fontes**: Use fontes legíveis. Material 3 usa muito a **Roboto** e variações de peso (Bold, Medium).

---

## 5. Dark Mode (Modo Escuro) 🌑

Hoje em dia é **obrigatório**.
O Android gerencia isso com pastas de recursos:
*   `values/colors.xml` (Cores Dia)
*   `values-night/colors.xml` (Cores Noite)

Defina nomes semânticos, não literais:
*   ❌ `background_white` (Ruim: e se no escuro for preto?)
*   ✅ `background_color` (Bom: no dia é branco, na noite é preto)

---

## 6. Feedback Tátil e Visual (Ripples) 🌊

O usuário precisa saber que tocou.
O Android tem o efeito **Ripple** (onda) nativo em botões. Se criar um componente customizado, adicione:
`android:background="?attr/selectableItemBackground"`

Se a ação for perigosa (deletar), use cores de erro (vermelho). Se for sucesso, cores de confirmação.

---

## 7. Desafio: Redesign do App 💅

Pegue o exercício da Lista de Filmes (Aula 09) ou Tarefas (Aula 08) e aplique Material Design:
1.  Use `MaterialCardView` para os itens da lista.
2.  Adicione um `FloatingActionButton` (+) para incluir novos itens.
3.  Crie uma versão de cores para **Modo Escuro** (teste trocando o tema do celular).
4.  Certifique-se que os textos têm contraste suficiente.

---

## 🔗 Materiais da Aula

<div class="grid cards" markdown>
- :material-presentation: **Slides**

    ---

    Material visual com diagramas e conceitos-chave.

    [:octicons-arrow-right-24: Slide 12](../slides/slide-12.html)

- :material-help-circle: **Quiz**

    ---

    Teste seu conhecimento com 10 questões interativas.

    [:octicons-arrow-right-24: Quiz 12](../quizzes/quiz-12.md)

- :fontawesome-solid-pencil: **Exercícios**

    ---

    5 exercícios progressivos (básico → desafio).

    [:octicons-arrow-right-24: Exercício 12](../exercicios/exercicio-12.md)

- :material-briefcase-outline: **Projeto**

    ---

    Aplicação prática dos conceitos da aula.

    [:octicons-arrow-right-24: Projeto 12](../projetos/projeto-12.md)

</div>

---

[➡️ Próxima Aula: Aula 13](./aula-13.md){ .md-button .md-button--primary }
