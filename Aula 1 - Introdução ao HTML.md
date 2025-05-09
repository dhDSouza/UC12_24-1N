# Introdução ao HTML

## 1. O que é HTML?

`HTML` significa **_HyperText Markup Language_** **(Linguagem de Marcação de Hipertexto)**. É a linguagem usada para criar páginas da web. O `HTML` diz ao navegador como mostrar o conteúdo.

## 2. Estrutura básica de uma página HTML

**Exemplo:**

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Minha Primeira Página</title>
    </head>
    <body>
        <h1>Olá, Mundo!</h1>
        <p>Esta é a minha primeira página HTML.</p>
    </body>
</html>
```

- **Explicação:** Cada documento `HTML` começa com `<!DOCTYPE html>`, seguido pelas tags `<html>`, `<head>`, e `<body>`. O `<head>` contém informações sobre a página, como o título, que aparece na aba do navegador. O `<body>` é onde colocamos o conteúdo que aparece na página.

## 3. As principais tags do HTML

- **Tag `<h1> a <h6>`:** Usada para títulos, com `<h1>` sendo o maior e `<h6>` o menor.

- **Tag `<p>`:** Usada para parágrafos de texto.

- **Tag `<a>`:** Cria links.

  - **Exemplo:** `<a href="https://www.google.com">Clique aqui para ir ao Google</a>`

- **Tag `<img>`:** Exibe imagens.

  - **Exemplo:** `<img src="imagem.jpg" alt="Descrição da Imagem">`

- **Tag `<ul>` e `<li>`:** Criam listas não ordenadas (com marcadores).

  - **Exemplo:**

       ```html
       <ul>
           <li>Item 1</li>
           <li>Item 2</li>
           <li>Item 3</li>
       </ul>
       ```

- **Tag `<ol>` e `<li>`:** Criam listas ordenadas (com números).

  - **Exemplo:**

       ```html
       <ol>
           <li>Primeiro</li>
           <li>Segundo</li>
           <li>Terceiro</li>
       </ol>
       ```

## Exemplos Práticos

### 1. Criar um Documento HTML Simples

- Crie um arquivo chamado `index.html`.
- Adicione o seguinte código:

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Minha Página Simples</title>
    </head>
    <body>
        <h1>Bem-vindos à minha página</h1>
        <p>Este é o meu primeiro parágrafo.</p>
    </body>
</html>
```

### 2. Adicionar uma Imagem e um Link

- Adicione uma imagem e um link na página criada.

- **Exemplo:**

```html
<h2>Minha Foto Favorita</h2>
<img src="https://via.placeholder.com/150" alt="Imagem Exemplo">
       
<p>Visite o <a href="https://www.google.com">Google</a> para mais informações.</p>
```

### 3. Criar uma Lista

- Crie uma lista de seus hobbies ou coisas favoritas.

- **Exemplo:**

```html
<h2>Meus Hobbies</h2>
<ul>
    <li>Ler</li>
    <li>Jogar videogame</li>
    <li>Desenhar</li>
</ul>
```

## Exercícios Finais

1. **Crie um segundo título** (usando `<h2>`) com uma breve descrição sua.
2. **Adicione duas imagens diferentes** na página e certifique-se de incluir uma descrição em texto (usando o atributo `alt`).
3. **Crie uma lista ordenada** dos três lugares que você gostaria de visitar no futuro.
