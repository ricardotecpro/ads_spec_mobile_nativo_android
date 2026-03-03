# Aula 15 - Publicação e Google Play Store 🚀

!!! tip "Objetivo"
    **Objetivo**: Conhecer o processo final de transformar seu código em um produto real, gerando o arquivo de produção (.aab), criando artes para a loja e entendendo os critérios de revisão.

---

## 1. APK vs AAB 📦

*   **APK (Android Package)**: Formato antigo. É um "zip" com tudo dentro.
*   **AAB (Android App Bundle)**: Formato moderno (obrigatório para novos apps). O Google Play usa o Bundle para gerar APKs otimizados para cada celular (só envia as imagens daquela densidade de tela, economizando espaço).

---

## 2. Preparando o App para Produção ⚙️

1.  **Remover Logs**: Limpe os `Log.d` ou use bibliotecas como o **Timber** para gerenciar isso.
2.  **Ofuscação (ProGuard/R8)**: Protege seu código contra pirataria e diminui o tamanho do app removendo código não usado.
3.  **Versão**: Atualize o `versionCode` (número inteiro) e `versionName` (ex: "1.0.0") no `build.gradle`.

---

## 3. Gerando a Chave de Assinatura (Keystore) 🔑

O Android exige que todo app seja assinado digitalmente.
**IMPORTANTE**: Se você perder o arquivo `.jks` (keystore), você nunca mais poderá atualizar seu app na loja. Guarde em 3 lugares diferentes! 💾

---

## 4. Google Play Console 🎮

É o portal do desenvolvedor Google.
*   **Custo**: Taxa única de **$25**.
*   **Revisão**: O app passa por uma análise automatizada e humana (pode levar de 1 a 7 dias).

---

## 5. Materiais para a Loja (Marketing) 🎨

Você vai precisar de:
1.  **Título e Descrição** (Curta e Longa).
2.  **Ícone do App** (512x512).
3.  **Feature Graphic** (1024x500 - Arte de destaque).
4.  **Screenshots** (Capturas de tela do app rodando).

---

## 6. Testes Rápidos (Canais de Teste) 🧪

Antes de lançar para o público geral, use os canais:
*   **Teste Interno**: Para sua equipe (instantâneo).
*   **Teste Fechado (Beta)**: Para convidados.
*   **Teste Aberto**: Qualquer um pode baixar e testar.

### 🆚 Comparação: App Store Connect e TestFlight (iOS)
No iOS, a taxa é anual ($99). O portal chama-se `App Store Connect` e o app de testes oficial é o `TestFlight`. A revisão da Apple é conhecida por ser muito mais rigorosa que a do Google.

---

## 7. Desafio: Checklist de Lançamento ✅

Imagine que você terminou seu app de Notas. Marque o que você faria ANTES de clicar em "Gerar AAB":
- [ ] Deixar a senha do banco de dados exposta no código? (Espero que não! 😱)
- [ ] Ativar o `minifyEnabled true` para encolher o código?
- [ ] Testar em um celular físico real?
- [ ] Verificar se as Strings estão traduzidas para PT-BR?

---

## 🔗 Materiais da Aula

<div class="grid cards" markdown>
- :material-presentation: **Slides**

    ---

    Material visual com diagramas e conceitos-chave.

    [:octicons-arrow-right-24: Slide 15](../slides/slide-15.html)

- :material-help-circle: **Quiz**

    ---

    Teste seu conhecimento com 10 questões interativas.

    [:octicons-arrow-right-24: Quiz 15](../quizzes/quiz-15.md)

- :fontawesome-solid-pencil: **Exercícios**

    ---

    5 exercícios progressivos (básico → desafio).

    [:octicons-arrow-right-24: Exercício 15](../exercicios/exercicio-15.md)

- :material-briefcase-outline: **Projeto**

    ---

    Aplicação prática dos conceitos da aula.

    [:octicons-arrow-right-24: Projeto 15](../projetos/projeto-15.md)

</div>

---

[➡️ Próxima Aula: Aula 16](./aula-16.md){ .md-button .md-button--primary }
