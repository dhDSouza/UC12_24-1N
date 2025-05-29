# 🧱 **Box Model e Layout com CSS**

### 🎯 **Objetivo da Aula**

Compreender como os elementos HTML se comportam visualmente em uma página e aprender a controlar seu **espaço, tamanho e posicionamento** usando o **Box Model** e técnicas modernas de **layout com CSS** como **Flexbox**.

---

## 🧩 **Conteúdo da Aula**

---

### 1. 📦 **Box Model (Modelo de Caixa)**

#### 🧠 O que é?

No CSS, **todos os elementos são caixas**. O **Box Model** descreve o espaço ocupado por cada elemento da seguinte forma:

* **Content**: o conteúdo em si (texto, imagem, etc).
* **Padding**: espaço interno entre o conteúdo e a borda.
* **Border**: contorno da caixa.
* **Margin**: espaço externo entre a caixa e outros elementos.

#### 🔍 Visualizando no Navegador

Abra o **DevTools (F12 ou botão direito > Inspecionar)** e veja a aba “Computed” para visualizar as partes do Box Model de qualquer elemento.

#### 🧪 Exemplo Prático:

```css
div {
  width: 200px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
}
```

#### 📏 Diferença entre `box-sizing`

```css
/* Padrão */
box-sizing: content-box; 

/* Recomendada */
box-sizing: border-box;
```

🔹 Com `border-box`, **padding** e **border** estão incluídos na largura total definida — facilita o controle de layout!

---

### 2. 📐 **Propriedades de Layout Importantes**

#### 🔄 `display`:

* `block`: ocupa toda a largura da linha (ex: `<div>`)
* `inline`: ocupa apenas o necessário (ex: `<span>`)
* `inline-block`: como inline, mas permite definir largura/altura
* `none`: oculta o elemento

#### 📐 Tamanho:

* `width`, `height`: definem dimensões
* `max-width`, `min-height`: limites para responsividade
* `overflow: hidden | scroll | auto | visible`

#### 🎯 `position`:

* `static`: posição padrão
* `relative`: ajusta posição **em relação a si mesmo**
* `absolute`: posição **relativa ao primeiro ancestral com `position` diferente de static**
* `fixed`: **fixo na tela** (ex: menu fixo)
* `sticky`: **mistura entre relative e fixed**, "gruda" quando atinge certo ponto

---

### 3. 🧭 **Introdução ao Flexbox**

#### 🧱 O que é?

Sistema moderno de layout 1D (linha ou coluna). Ideal para alinhamento e distribuição de elementos.

#### 💡 Propriedades principais:

```css
.container {
  display: flex;
  flex-direction: row; /* ou column */
  justify-content: center; /* alinha no eixo principal */
  align-items: center;     /* alinha no eixo cruzado */
  gap: 1rem;               /* espaçamento entre itens */
}
```

#### 🧪 Exemplo: Menu Horizontal

```html
<nav class="menu">
  <a href="#">Início</a>
  <a href="#">Sobre</a>
  <a href="#">Contato</a>
</nav>
```

```css
.menu {
  display: flex;
  justify-content: space-around;
  background-color: #f0f0f0;
  padding: 10px;
}
```

---

### 4. 🧱 **Criando um Layout Simples: Header, Main, Footer**

#### 🧪 Estrutura HTML:

```html
<header>Menu</header>
<main>Conteúdo principal</main>
<footer>Rodapé</footer>
```

#### 🎨 Estilização com Flexbox e Box Model:

```css
body {
  margin: 0;
  font-family: Arial, sans-serif;
}

header, footer {
  background: #333;
  color: white;
  text-align: center;
  padding: 1rem;
}

main {
  padding: 2rem;
  min-height: 60vh;
}
```

---

### 5. 📌 **Exercício: Landing Page Pessoal**

#### ✍️ Estrutura Esperada:

1. **Header** com título e links de navegação
2. **Main** com uma apresentação pessoal e imagem
3. **Footer** com contatos/redes sociais

#### 🎨 Estilos:

* Usar `box-sizing: border-box`
* Alinhar com `display: flex` (ex: colocar imagem e texto lado a lado)
* Usar um **Google Font** (ex: `Roboto`, `Poppins`)
* Criar um **arquivo CSS externo**

#### 💡 Dica:

```html
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
```

```css
body {
  font-family: 'Poppins', sans-serif;
}
```
