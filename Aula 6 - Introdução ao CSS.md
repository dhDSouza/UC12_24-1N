# 🎨 **Introdução ao CSS**

## 📌 **O que é CSS?**

CSS significa **Cascading Style Sheets** (Folhas de Estilo em Cascata). É uma linguagem usada para **estilizar páginas web**, ou seja, definir cores, tamanhos, fontes, espaçamentos, bordas, layouts, etc.

Enquanto o **HTML** cria a estrutura da página (como se fossem os tijolos de uma casa), o **CSS** é responsável pela aparência, o design, a decoração dessa casa!

---

## 🎯 **Formas de aplicar CSS**

### ✅ **1. Inline (CSS na linha)**

O CSS é aplicado diretamente no elemento HTML, usando o atributo `style`.

### **Exemplo:**

```html
<p style="color: blue; font-size: 20px;">
  Este parágrafo está azul e com fonte de 20px.
</p>
```

> [!WARNING]
> Essa forma não é recomendada para projetos grandes, pois dificulta a manutenção.

---

### ✅ **2. Internal (CSS interno)**

O CSS fica dentro do próprio arquivo HTML, usando a tag `<style>` no `<head>`.

### **Exemplo:**

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Exemplo CSS Interno</title>
  <style>
    p {
      color: green;
      font-size: 18px;
    }
  </style>
</head>
<body>
  <p>Este parágrafo está verde!</p>
</body>
</html>
```

---

### ✅ **3. External (CSS externo)**

O CSS fica em um arquivo separado (ex.: `estilo.css`) e é importado no HTML através da tag `<link>`.

### **Exemplo (HTML):**

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Exemplo CSS Externo</title>
  <link rel="stylesheet" href="estilo.css">
</head>
<body>
  <p>Este parágrafo foi estilizado por um arquivo externo!</p>
</body>
</html>
```

### **Exemplo (estilo.css):**

```css
p {
  color: red;
  font-size: 22px;
}
```

---

## 🏹 **Seletores CSS**

Seletores são usados para selecionar quais elementos HTML você quer estilizar.

### ✅ **Principais seletores:**

* **Por tag:** aplica a todos os elementos dessa tag.

  ```css
  p {
    color: blue;
  }
  ```

* **Por classe:** usa `.` antes do nome. Permite estilizar vários elementos com a mesma classe.

  ```css
  .destaque {
    color: orange;
  }
  ```

  ```html
  <p class="destaque">Texto destacado</p>
  ```

* **Por ID:** usa `#`. É único, aplicado a um elemento específico.

  ```css
  #titulo {
    color: purple;
  }
  ```

  ```html
  <h1 id="titulo">Título da Página</h1>
  ```

---

## ✍️ **Propriedades Básicas de Estilização**

### ✅ **Cor (color)**

```css
p {
  color: blue;
}
```

### ✅ **Fundo (background-color)**

```css
body {
  background-color: lightgray;
}
```

### ✅ **Fonte (font-family, font-size, font-weight)**

```css
h1 {
  font-family: Arial, sans-serif;
  font-size: 32px;
  font-weight: bold;
}
```

### ✅ **Alinhamento de texto (text-align)**

```css
p {
  text-align: center;
}
```

### ✅ **Margens e espaçamentos (margin, padding)**

```css
div {
  margin: 20px;
  padding: 10px;
}
```

### ✅ **Borda (border)**

```css
div {
  border: 2px solid black;
}
```

---

## 🔤 **Fontes no CSS**

Você pode usar fontes padrões do sistema ou importar fontes do Google Fonts.

### ✅ **Fontes padrão:**

```css
body {
  font-family: Arial, Verdana, sans-serif;
}
```

### ✅ **Importando do Google Fonts:**

1. Acesse [https://fonts.google.com/](https://fonts.google.com/)
2. Escolha uma fonte (ex.: Poppins)
3. Copie o link:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins&display=swap" rel="stylesheet">
```

4. Use no CSS:

```css
body {
  font-family: 'Poppins', sans-serif;
}
```

---

## 🚀 **Exemplo Completo**

### **HTML + CSS interno:**

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="UTF-8">
  <title>Minha Página CSS</title>
  <style>
    body {
      background-color: #f0f0f0;
      font-family: Arial, sans-serif;
    }

    h1 {
      color: #333333;
      text-align: center;
    }

    p {
      color: #555555;
      font-size: 18px;
    }

    .destaque {
      color: red;
      font-weight: bold;
    }
  </style>
</head>
<body>
  <h1>Bem-vindo ao mundo do CSS!</h1>
  <p>Este é um parágrafo comum.</p>
  <p class="destaque">Este é um parágrafo destacado!</p>
</body>
</html>
```

---

## ✍️ **Exercício Prático!**

### 🎶 **Crie uma tabela com seu Top 5 músicas favoritas!**

* A tabela deve conter:

  * **Capa do álbum** (use imagens via `<img>`)
  * **Nome da música**
  * **Artista**
  * **Player de áudio** (use a tag `<audio>` com um arquivo de áudio ou link externo)

### ✅ **Além disso:**

* Aplique CSS usando **arquivo externo (External)**.
* Estilize:

  * **Borda da tabela**
  * **Cores alternadas nas linhas**
  * **Texto centralizado**
  * **Fonte personalizada (pode usar Google Fonts)**
