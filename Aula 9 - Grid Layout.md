# 🖥️ Grid Layout em CSS 🚀

## O que é o `display: grid`? 🤔

A propriedade `display: grid` ativa o **CSS Grid Layout**, um sistema de layout bidimensional super poderoso que facilita a criação de layouts **complexos e responsivos** de forma simples e intuitiva. Ele permite organizar os elementos em linhas e colunas, oferecendo um controle incrível sobre o posicionamento dos itens na página. 🎨

---

## Como Funciona o Grid Layout? 💡

Quando você define `display: grid` em um container, ele se torna um **grid container** e os elementos dentro dele viram **grid items**. Diferente do Flexbox (que trabalha em apenas um eixo por vez), o Grid trabalha com:

* **Eixo de Linhas (Rows)** ⬇️
* **Eixo de Colunas (Columns)** ➡️

Ou seja: você pode posicionar os itens tanto na horizontal quanto na vertical **simultaneamente**! 🚀

---

## 🛠️ Propriedades Principais do Grid

### No **Grid Container** 🧑‍💻

#### 1️⃣ `display: grid`

Ativa o Grid no container:

```css
.container {
  display: grid;
}
```

#### 2️⃣ `grid-template-columns` 📏

Define quantas e quais serão as colunas no grid.

Exemplo:

```css
.container {
  display: grid;
  grid-template-columns: 200px 200px 200px;
}
```

Neste exemplo, o grid terá 3 colunas, cada uma com 200px de largura.

Você também pode usar `fr` (fractional unit), que divide o espaço restante proporcionalmente:

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}
```

Aqui a segunda coluna terá o dobro de largura das outras.

#### 3️⃣ `grid-template-rows` 📏

Define a altura das linhas:

```css
.container {
  display: grid;
  grid-template-rows: 100px 200px;
}
```

#### 4️⃣ `gap` (ou `grid-gap`) 🕳️

Define o espaçamento entre as linhas e colunas:

```css
.container {
  display: grid;
  gap: 20px;
}
```

Ou separadamente:

```css
.container {
  display: grid;
  row-gap: 10px;
  column-gap: 20px;
}
```

#### 5️⃣ `grid-template-areas` 🗺️

Permite nomear as áreas do grid para um posicionamento mais intuitivo:

```css
.container {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto auto;
  grid-template-areas: 
    "header header"
    "sidebar main";
}
```

E depois nos itens:

```css
.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;
}

.main {
  grid-area: main;
}
```

#### 6️⃣ `justify-items` e `align-items` 🎯

Controlam o alinhamento dos **itens dentro de suas células**.

* `justify-items`: alinha horizontalmente.
* `align-items`: alinha verticalmente.

Exemplo:

```css
.container {
  display: grid;
  justify-items: center;
  align-items: center;
}
```

#### 7️⃣ `justify-content` e `align-content` 📦

Controlam o alinhamento do **grid inteiro dentro do container** (quando o grid não ocupa todo o espaço disponível).

Exemplo:

```css
.container {
  display: grid;
  justify-content: center;
  align-content: center;
}
```

---

### Nos **Grid Items** ⚙️

#### 1️⃣ `grid-column` e `grid-row` 📊

Permitem posicionar um item em colunas e linhas específicas:

```css
.item {
  grid-column: 1 / 3; /* Vai ocupar da coluna 1 até antes da 3 (ou seja, 2 colunas) */
  grid-row: 1 / 2; /* Vai ocupar só a linha 1 */
}
```

#### 2️⃣ `grid-area` 🎯

Se você usou `grid-template-areas`, pode associar o item diretamente:

```css
.item {
  grid-area: header;
}
```

#### 3️⃣ `justify-self` e `align-self` 🙋‍♂️

Permitem alinhar individualmente cada item dentro de sua célula:

```css
.item {
  justify-self: end;
  align-self: start;
}
```

---

## 📝 Quando Usar o Grid Layout?

O **CSS Grid** é perfeito para:

* Layouts complexos de páginas.
* Galerias de imagens.
* Dashboards e cards.
* Layouts responsivos com várias seções.
* Quando você precisa de controle total sobre linhas e colunas.

---

## 🎮 Desafio Grid Garden

Agora é hora de praticar tudo isso de forma divertida com o **Grid Garden**, um joguinho onde você cultiva cenouras usando as propriedades do CSS Grid! 🥕🧑‍🌾

👉 [Acesse o Grid Garden aqui!](https://cssgridgarden.com/)

---

## Exemplo Prático de Grid Layout 🏗️

Aqui vai um exemplo de uma simples área de layout com header, sidebar e conteúdo principal:

```html
<!DOCTYPE html>
<html lang="pt">

<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .container {
      display: grid;
      grid-template-columns: 200px 1fr;
      grid-template-rows: 100px 1fr;
      grid-template-areas: 
        "header header"
        "sidebar main";
      height: 100vh;
      gap: 10px;
    }

    .header {
      grid-area: header;
      background-color: #6c5ce7;
      color: white;
      text-align: center;
      padding: 20px;
    }

    .sidebar {
      grid-area: sidebar;
      background-color: #00b894;
      color: white;
      padding: 20px;
    }

    .main {
      grid-area: main;
      background-color: #fdcb6e;
      padding: 20px;
    }
  </style>
  <title>Exemplo Grid Layout</title>
</head>

<body>
  <div class="container">
    <div class="header">Header</div>
    <div class="sidebar">Sidebar</div>
    <div class="main">Conteúdo Principal</div>
  </div>
</body>

</html>
```
