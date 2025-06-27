# 🚀 Introdução ao JavaScript para Front-End


**Então pessoal, finalmente chegou a hora do JavaScript! 🚀**   

Depois de construir o **esqueleto do nosso site** com **HTML** e dar aquele visual estiloso com **CSS**, chegou o momento de **dar vida a tudo isso**.   

O que veremos hoje:

1. **📚 Revisão dos conceitos básicos**
2. **🎯 Eventos em JavaScript**
3. **🌳 Manipulação do DOM**

<div align="center">
  <img src="https://i.gifer.com/Af6V.gif" alt="esqueleto dançando"/>
  <p>Fonte: <a href="https://i.gifer.com/Af6V.gif" target="_blank">https://i.gifer.com/Af6V.gif</a></p>
</div>

## 📚 Parte 1: Revisão dos Conceitos Básicos

### O que é JavaScript? 🤔

JavaScript é uma linguagem de programação que permite adicionar interatividade às páginas web. Enquanto HTML estrutura o conteúdo e CSS estiliza, JS faz a mágica acontecer!

```html
<script>
  // Código em JavaScript
</script>
```

### Variáveis: `let` vs `const` 📦
- `let`: Variável que pode ser reatribuída
- `const`: Constante, não pode ser reatribuída (mas objetos/arrays podem ser modificados)

```javascript
let nome = "João";
nome = "Maria"; // ✅ Permitido

const PI = 3.14;
PI = 3.1415; // ❌ Erro! Constante não pode ser reatribuída
```

### Funções 🛠️
Blocos de código reutilizáveis que realizam uma tarefa específica.

```javascript
// Declaração de função
function saudacao(nome) {
  return `Olá, ${nome}!`;
}

// Arrow function
const soma = (a, b) => a + b;

console.log(saudacao("Rodolfo")); // "Olá, Rodolfo!"
console.log(soma(2, 3)); // 5
```

### Estruturas de Repetição 🔁
#### `for` - Quando sabemos quantas vezes repetir
```javascript
for (let i = 0; i < 5; i++) {
  console.log(`Iteração ${i}`);
}
```

#### `while` - Quando não sabemos quantas vezes repetir
```javascript
let contador = 0;
while (contador < 5) {
  console.log(`Contador: ${contador}`);
  contador++;
}
```

#### `forEach` - Para arrays
```javascript
const frutas = ["maçã", "banana", "laranja"];
frutas.forEach((fruta, index) => {
  console.log(`${index + 1}: ${fruta}`);
});
```

## 🎯 Parte 2: Eventos em JavaScript

### O que são Eventos? 🎪
Eventos são ações ou ocorrências que acontecem no navegador, como cliques, teclas pressionadas, movimentos do mouse, etc.

### Tabela de Eventos Comuns 📋

| Evento         | Descrição                          | Exemplo de Uso                     |
|:--------------:|:----------------------------------:|:----------------------------------:|
| `click`        | Quando um elemento é clicado       | Botões, links                      |
| `dblclick`     | Duplo clique no elemento           | Edição rápida                      |
| `mouseover`    | Mouse sobre o elemento             | Efeitos hover                      |
| `mouseout`     | Mouse sai do elemento              | Reverter efeitos hover             |
| `mousemove`    | Mouse se move sobre o elemento     | Animações com mouse                |
| `keydown`      | Tecla pressionada                  | Controles de jogo, atalhos         |
| `keyup`        | Tecla liberada                     | Validação de formulário            |
| `submit`       | Formulário submetido               | Validação antes de enviar          |
| `change`       | Valor de input/select alterado     | Atualizações dinâmicas             |
| `focus`        | Elemento recebe foco               | Destacar campo ativo               |
| `blur`         | Elemento perde foco                | Validação ao sair do campo         |
| `load`         | Página/elemento carregado          | Inicializar após carregamento      |
| `scroll`       | Rolagem da página/elemento         | Efeitos parallax, lazy loading     |
| `resize`       | Janela redimensionada              | Layouts responsivos                |

### Como Usar Eventos? 🛠️

#### Método 1: Atributo HTML (não recomendado)
```html
<button onclick="alert('Clicado!')">Clique-me</button>
```

#### Método 2: Propriedade do elemento (pouco usado)
```javascript
const btn = document.querySelector('button');
btn.onclick = function() {
  console.log('Clicado!');
};
```

#### Método 3: `addEventListener` (recomendado)
```javascript
const btn = document.querySelector('button');
btn.addEventListener('click', function() {
  console.log('Clicado com addEventListener!');
});
```

### Exemplo Completo com Evento ✨
```html
<button id="meuBotao">Clique-me</button>
<p id="contador">0 cliques</p>

<script>
  const botao = document.getElementById('meuBotao');
  const contadorElemento = document.getElementById('contador');
  let contador = 0;

  botao.addEventListener('click', () => {
    contador++;
    contadorElemento.textContent = `${contador} cliques`;
    
    if (contador > 5) {
      botao.style.backgroundColor = 'red';
    }
  });
</script>
```

## 🌳 Parte 3: Manipulação do DOM

### O que é o DOM? 🌐
DOM (Document Object Model) é uma representação em árvore do documento HTML, onde cada elemento é um nó (node). O JavaScript pode manipular esses nós para alterar a página dinamicamente.

### Como Acessar Elementos? 🔍

| Método                         | Retorno                           | Exemplo                     |
|:------------------------------:|:---------------------------------:|:---------------------------:|
| `document.getElementById()`    | Elemento com ID específico        | `document.getElementById('header')` |
| `document.querySelector()`     | Primeiro elemento que casa com o seletor | `document.querySelector('.btn')` |
| `document.querySelectorAll()`  | NodeList de todos elementos que casam | `document.querySelectorAll('p')` |
| `document.getElementsByTagName()` | HTMLCollection de elementos pela tag | `document.getElementsByTagName('div')` |
| `document.getElementsByClassName()` | HTMLCollection de elementos pela classe | `document.getElementsByClassName('active')` |

### Manipulando Elementos ✂️

#### Alterando conteúdo
```javascript
// textContent (apenas texto)
elemento.textContent = 'Novo texto';

// innerHTML (permite HTML)
elemento.innerHTML = '<strong>Texto</strong> em negrito';
```

#### Alterando estilos
```javascript
elemento.style.backgroundColor = 'blue';
elemento.style.fontSize = '20px';
```

#### Adicionando/Removendo classes
```javascript
elemento.classList.add('ativo');
elemento.classList.remove('inativo');
elemento.classList.toggle('destaque'); // adiciona se não tem, remove se tem
```

#### Criando/Removendo elementos
```javascript
// Criar novo elemento
const novoParagrafo = document.createElement('p');
novoParagrafo.textContent = 'Sou novo aqui!';

// Adicionar ao DOM
document.body.appendChild(novoParagrafo);

// Remover elemento
const elementoParaRemover = document.getElementById('remover');
elementoParaRemover.remove();
```

### Exemplo Completo de Manipulação DOM 🏗️
```html
<div id="container">
  <button id="adicionar">Adicionar Item</button>
  <button id="remover">Remover Último</button>
  <ul id="lista"></ul>
</div>

<script>
  const adicionarBtn = document.getElementById('adicionar');
  const removerBtn = document.getElementById('remover');
  const lista = document.getElementById('lista');
  let contador = 1;

  adicionarBtn.addEventListener('click', () => {
    const novoItem = document.createElement('li');
    novoItem.textContent = `Item ${contador++}`;
    novoItem.classList.add('item-lista');
    lista.appendChild(novoItem);
  });

  removerBtn.addEventListener('click', () => {
    const ultimoItem = lista.lastElementChild;
    if (ultimoItem) {
      ultimoItem.remove();
      contador--;
    }
  });
</script>
```

### Event Delegation (Delegação de Eventos) 🎯
Ótimo para elementos dinâmicos ou muitos elementos similares:

```html
<ul id="lista-tarefas">
  <!-- Itens serão adicionados dinamicamente -->
</ul>

<script>
  const listaTarefas = document.getElementById('lista-tarefas');
  
  // Adiciona evento na lista (pai) em vez de cada item (filho)
  listaTarefas.addEventListener('click', (event) => {
    if (event.target.tagName === 'LI') {
      event.target.classList.toggle('completa');
    }
  });
  
  // Adicionando itens dinamicamente
  for (let i = 1; i <= 5; i++) {
    const item = document.createElement('li');
    item.textContent = `Tarefa ${i}`;
    listaTarefas.appendChild(item);
  }
</script>
```

## 🧠 **Exercícios - Parte 1: Revisão dos Conceitos Básicos**

### 📝 **Ex. 1 – Criação de Variáveis e Funções**

Crie um arquivo HTML com um `<script>` interno contendo o seguinte:

1. Declare uma variável `nome` com `let` e atribua seu nome.
2. Declare uma constante `curso` com o valor `"Front-End"` usando `const`.
3. Crie uma função chamada `boasVindas` que retorne a frase:
   `"Bem-vindo, [nome]! Você está no curso de [curso]."`
4. Exiba o resultado da função no console.

### 📝 **Ex. 2 – Soma com Função**

Crie uma função `somaNumeros(a, b)` que receba dois números e retorne a soma. Chame a função passando 5 e 7 e exiba o resultado no console.

---

## 🧠 **Exercícios - Parte 2: Eventos em JavaScript**

### 🔁 **Ex. 3 – Alternar Visibilidade de um Elemento**

Crie:

* Um botão com o texto "Mostrar/Esconder"
* Um parágrafo com um texto qualquer

**Objetivo:**

* Ao clicar no botão, o parágrafo deve ser escondido se estiver visível e mostrado se estiver escondido.

### 🎨 **Ex. 4 – Mudança de Cor com Mouse**

Crie um `<div>` com 200x200px de largura/altura e cor de fundo cinza.

Adicione eventos:

* Ao passar o mouse por cima (`mouseover`), mude a cor para azul
* Ao tirar o mouse (`mouseout`), volte para cinza

### 🔡 **Ex. 5 – Mostrar Texto ao Pressionar Tecla**

Adicione um `<input>` e um `<p>` vazio abaixo dele.

Ao digitar algo no input:

* Mostre em tempo real no parágrafo o que está sendo digitado (usando `keyup`).

---

## 🧠 **Exercícios - Parte 3: Manipulação do DOM**

### 🧾 **Ex. 6 – Lista de Tarefas Simples**

Crie:

* Um campo de texto
* Um botão "Adicionar"
* Uma `<ul>` vazia

Ao clicar no botão:

* Pegue o valor do campo de texto
* Crie um novo `<li>` com esse texto
* Adicione o `<li>` à lista

### 🌟 **Ex. 7 – Botão com Estilo Dinâmico**

Crie um botão com o texto "Mudar tema".

Ao clicar:

* Troque a cor de fundo da página entre branco e preto (modo claro/escuro)
* Troque a cor do texto também (para ficar visível)
* Use `classList.toggle()` para aplicar/remover uma classe CSS

---

## 🎉 Conclusão

Agora você já tem as bases para:
1. Trabalhar com variáveis e funções em JS
2. Lidar com os eventos mais comuns no navegador
3. Manipular o DOM para criar páginas dinâmicas e interativas
