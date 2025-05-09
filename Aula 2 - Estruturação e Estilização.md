# Estruturando e Estilizando Páginas com HTML

## 1. Introdução às Tags de Estrutura

1. **Tag `<div>`:** Usada para agrupar conteúdo e dividir a página em seções.

    - **Exemplo:**

    ```html
    <div>
        <h1>Seção Principal</h1>
        <p>Este é um parágrafo dentro de uma div.</p>
    </div>
    ```

    - **Explicação:** A `<div>` é como uma caixa que pode conter outros elementos. Ela ajuda a organizar a página.

2. **Tag `<span>`:** Usada para aplicar estilos a uma parte específica de um texto.

    - **Exemplo:**

    ```html
        <p>Esta palavra é <span style="color: red;">vermelha</span>.</p>
    ```

    - **Explicação:** Diferente da `<div>`, o `<span>` é usado dentro de linhas de texto.

## 2. Introdução ao Atributo `style`

- **Explicação:** O atributo `style` permite adicionar `CSS` **(folhas de estilo)** diretamente em elementos `HTML` para alterar a aparência.

- **Exemplo:**

     ```html
     <h1 style="color: blue; text-align: center;">Título Centralizado em Azul</h1>
     <p style="font-size: 18px; color: green;">Este parágrafo é verde e tem tamanho de fonte 18px.</p>
     ```

## 3. Trabalhando com Cores e Fontes

1. **Cores:**

    - **Explicação:** Podemos definir cores usando nomes (como `red`, `blue`) ou códigos hexadecimais (como `#ff0000` para vermelho).

    - **Exemplo:**

        ```html
        <p style="color: #00ff00;">Este texto é verde (usando hexadecimal).</p>
        ```

2. **Fontes:**

    - **Explicação:** Além de definir o tamanho da fonte, podemos alterar o tipo de fonte usando `font-family`.

    - **Exemplo:**

        ```html
        <p style="font-family: Arial, sans-serif;">Este texto usa a fonte Arial.</p>
        ```

## 4. Criando Links Internos e âncoras

- **Explicação:** Links internos permitem navegar dentro da mesma página.

- **Exemplo:**

    ```html
    <h2 id="seção1">Seção 1</h2>
    <p>Conteúdo da Seção 1.</p>
    
    <h2 id="seção2">Seção 2</h2>
    <p>Conteúdo da Seção 2.</p>
    
    <a href="#seção1">Voltar para a Seção 1</a>
    ```

- **Explicação:** Usamos `id` para marcar um ponto específico na página e `href="#id"` para criar um link que leva a esse ponto.

### Atividade Prática

1. Criar uma Página com Seções:**
  
    - Crie uma página com três seções, cada uma com um título (`<h2>`) e um parágrafo (`<p>`), usando `<div>` para agrupar cada seção.

    - **Exemplo:**

        ```html
        <div style="background-color: #f0f0f0;">
            <h2>Seção 1</h2>
            <p>Conteúdo da primeira seção.</p>
        </div>
        
        <div style="background-color: #e0e0e0;">
            <h2>Seção 2</h2>
            <p>Conteúdo da segunda seção.</p>
        </div>
        
        <div style="background-color: #d0d0d0;">
            <h2>Seção 3</h2>
            <p>Conteúdo da terceira seção.</p>
        </div>
        ```

2. Estilizar Textos

    - Aplique cores, tamanhos de fonte e estilos diferentes aos títulos e parágrafos.
    - **Exemplo:**

        ```html
        <h2 style="color: #333; text-align: left;">Título Esquerdo</h2>
        <p style="color: #666; font-size: 14px;">Este texto é cinza e pequeno.</p>
        ```

3. Criar Links Internos

    - Crie links internos que levem a diferentes seções da página.
    - **Exemplo:**

        ```html
        <a href="#seção1">Ir para a Seção 1</a>
         ```

## 5. Exercícios Finais

1. **Crie uma seção adicional** na página que inclua uma lista não ordenada de tópicos que você gostaria de aprender sobre HTML.
2. **Adicione estilos personalizados** à seção criada, mudando a cor de fundo e o tamanho do texto.
3. **Crie um link interno** que leva até essa nova seção a partir do topo da página.
