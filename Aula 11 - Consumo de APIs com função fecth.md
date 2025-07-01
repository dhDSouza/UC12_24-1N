# 🌐 Aula: Trabalhando com `fetch` e Consumindo APIs no JavaScript

## 🧠 O que é o `fetch`?

O `fetch` é uma função nativa do *JavaScript* usada para enviar e receber mensagens entre seu código e servidores, utilizando o protocolo **HTTP**.

* Ele é **assíncrono** e baseado em **Promises**, ou seja:

  * Não trava o código enquanto espera a resposta,
  * E permite trabalhar com **requisições encadeadas** e **tratamento de erros**.

> [!TIP]
> O `fetch` é o **caminho moderno** pra interagir com **APIs** — interfaces que os servidores oferecem pra você **buscar ou enviar dados**!

---

## 📚 A Importância de Ler a Documentação da API

Antes de usar qualquer API, é essencial entender como ela funciona:

🔍 **Por que ler a documentação da API?**

* 📎 Descobre os **endpoints disponíveis** (URLs que você pode acessar).
* 📮 Entende os **métodos HTTP** que ela aceita (`GET`, `POST`, etc).
* 🧾 Sabe **quais dados enviar e receber**, e em qual formato (geralmente JSON).
* ❌ Aprende como a API **retorna erros** (pra tratar corretamente no seu código).
* 🔐 E se for protegida, aprende como usar **tokens de acesso** (API Keys, Bearer Tokens...).

> [!NOTE] 
> A última [sessão](#-documentação-das-apis-vistas) desta aula contém links para as documentações de cada API utilizada nos exemplos. Leia com carinho ❤️

---

## ⚙️ Como funciona o `fetch`?

### 🧪 Sintaxe básica:

```javascript
fetch(url, options)
  .then(response => response.json()) // Converte a resposta para JSON
  .then(data => console.log(data))   // Usa os dados recebidos
  .catch(error => console.error('Erro:', error)); // Trata erros
```

* `url`: endereço do recurso (API).
* `options`: configurações como método, cabeçalhos, corpo da requisição.
* `.then()`: manipula a resposta (com `.json()` para transformar).
* `.catch()`: captura erros de rede ou falhas na API.

---

## 🔁 Métodos HTTP e o CRUD

| Ação do CRUD | Método HTTP |         Significado        |
| :----------: | :---------: | :------------------------: |
|    Create    |     POST    |     Criar um novo dado     |
|     Read     |     GET     |      Buscar/ler dados      |
|    Update    | PUT / PATCH | Atualizar dados existentes |
|    Delete    |    DELETE   |        Remover dados       |

---

## 🧪 Exemplos Práticos

### ✅ Exemplo 1: Requisição GET – Listando Usuários

```html
<h1>Usuários</h1>
<ul id="listaUsuarios"></ul>

<script>
  fetch('https://jsonplaceholder.typicode.com/users')
    .then(res => res.json())
    .then(data => {
      const ul = document.getElementById('listaUsuarios');
      data.forEach(user => {
        const li = document.createElement('li');
        li.textContent = `${user.name} - ${user.email}`;
        ul.appendChild(li);
      });
    })
    .catch(erro => console.error('Erro:', erro));
</script>
```

---

### 📝 Exemplo 2: Requisição POST – Criando um Post

```html
<form id="formPost">
  <input id="titulo" placeholder="Título" required />
  <textarea id="conteudo" placeholder="Conteúdo" required></textarea>
  <button type="submit">Enviar</button>
</form>

<script>
  document.getElementById('formPost').addEventListener('submit', (e) => {
    e.preventDefault();

    const titulo = document.getElementById('titulo').value;
    const conteudo = document.getElementById('conteudo').value;

    fetch('https://jsonplaceholder.typicode.com/posts', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({
        title: titulo,
        body: conteudo,
        userId: 1
      })
    })
    .then(res => res.json())
    .then(data => console.log('Post criado:', data))
    .catch(err => console.error('Erro:', err));
  });
</script>
```

---

### 🎬 Exemplo 3: Consumindo API de Filmes (OMDb)

```javascript
fetch(`http://www.omdbapi.com/?t=Inception&apikey=SUA_API_KEY`)
  .then(res => res.json())
  .then(data => {
    console.log(data.Title, data.Year, data.Poster);
  });
```

> [!IMPORTANT]
> Substitua `SUA_API_KEY` por uma chave válida da OMDb (gratuita com cadastro no site deles).

---

### 🔎 Exemplo 4: Busca Dinâmica com Formulário (OMDb)

```html
<form id="formBusca">
  <input id="filme" placeholder="Nome do filme" required />
  <button type="submit">Buscar</button>
</form>
<div id="resultado"></div>

<script>
  const API_KEY = 'SUA_API_KEY';

  document.getElementById('formBusca').addEventListener('submit', function (e) {
    e.preventDefault();

    const titulo = document.getElementById('filme').value;
    fetch(`http://www.omdbapi.com/?t=${titulo}&apikey=${API_KEY}`)
      .then(res => res.json())
      .then(data => {
        const resultado = document.getElementById('resultado');
        if (data.Response === "True") {
          resultado.innerHTML = `
            <p><strong>Título:</strong> ${data.Title}</p>
            <p><strong>Ano:</strong> ${data.Year}</p>
            <img src="${data.Poster}" alt="Pôster do filme" />
          `;
        } else {
          resultado.innerHTML = '<p>Filme não encontrado 😢</p>';
        }
      });
  });
</script>
```

---

## 🧩 Exercícios

### 1. ✅ Listar Tarefas com `GET`

-  Use a URL: `https://jsonplaceholder.typicode.com/todos`
- Mostre os **10 primeiros** títulos e se estão **completos ou não**.

---

### 2. 📝 Criar um Formulário de Comentários com `POST`

- Envie nome e comentário para: `https://jsonplaceholder.typicode.com/comments`
- Mostre no console a resposta da API.

---

### 3. 🧠 Desafio: Busca de Personagens de Rick and Morty

- Use a URL:
  `https://rickandmortyapi.com/api/character/?name=<nome_do_personagem>`
- Mostre na tela:

  * Nome
  * Imagem
  * Status (vivo ou morto)

## 📖 Documentação das APIs vistas 

- {JSON} Placeholder: [https://jsonplaceholder.typicode.com/guide](https://jsonplaceholder.typicode.com/guide)
- OMDb API: [http://www.omdbapi.com/](http://www.omdbapi.com/)
- The Rick and Morty API: [https://rickandmortyapi.com/documentation](https://rickandmortyapi.com/documentation)
