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

### 🎯 **Position (Posicionamento)**

A propriedade `position` no CSS define o tipo de posicionamento de um elemento na página. Existem cinco valores principais para a propriedade `position`, e cada um deles altera a forma como o elemento é posicionado em relação ao seu contexto.

#### 1. **`static`** (Padrão)

* **O que faz**: Este é o valor **padrão** para todos os elementos HTML. Quando um elemento tem `position: static`, ele é posicionado no fluxo normal do documento, ou seja, de acordo com a ordem em que aparece no código.
* **Exemplo**: Um parágrafo com `position: static` ocupará sua posição natural, abaixo do elemento anterior.

```css
div {
  position: static;
  width: 200px;
  height: 100px;
  background-color: lightblue;
}
```

**Exemplo visual**: O elemento aparecerá na página no local padrão, de acordo com a ordem no HTML.

---

#### 2. **`relative`** (Relativo)

* **O que faz**: Com `position: relative`, o elemento é posicionado de acordo com o fluxo normal da página, mas você pode **ajustar sua posição** em relação à sua posição original. Ou seja, ele se move para cima, para baixo, para a esquerda ou para a direita, mas ainda mantém o espaço que ocuparia normalmente na página.
* **Exemplo**: Se você mover um elemento com `position: relative` 50px para a direita, ele **desloca-se**, mas o espaço onde ele estava ainda será mantido.

```css
div {
  position: relative;
  top: 20px;  /* Move o elemento 20px para baixo */
  left: 50px; /* Move o elemento 50px para a direita */
  width: 200px;
  height: 100px;
  background-color: lightcoral;
}
```

**Exemplo visual**: O div se move, mas o espaço que ele ocuparia na página (antes de ser deslocado) continua sendo "reservado".

---

#### 3. **`absolute`** (Absoluto)

* **O que faz**: Com `position: absolute`, o elemento é posicionado em relação ao seu **primeiro ancestral com `position` diferente de `static`** (geralmente, um elemento com `position: relative`). Ele sai do fluxo normal da página e não afeta o layout dos outros elementos.
* **Exemplo**: Um elemento com `position: absolute` será posicionado em relação ao contêiner pai que tiver `position: relative`, ou ao elemento `body` se nenhum contêiner pai tiver esse estilo.

```css
.container {
  position: relative;
  width: 500px;
  height: 500px;
  background-color: lightgray;
}

div {
  position: absolute;
  top: 50px;
  left: 100px;
  width: 200px;
  height: 100px;
  background-color: lightgreen;
}
```

**Exemplo visual**: O `div` com `position: absolute` se posiciona 50px para baixo e 100px para a direita dentro da `.container`, que tem `position: relative`.

---

#### 4. **`fixed`** (Fixo)

* **O que faz**: Com `position: fixed`, o elemento é posicionado em relação à **tela** (ou janela do navegador), não importa onde ele esteja no fluxo do documento. O elemento permanece fixo na tela, mesmo quando a página é rolada.
* **Exemplo**: Um cabeçalho fixo no topo da página ou um menu de navegação que fica visível quando você rola a página.

```css
div {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 50px;
  background-color: darkblue;
  color: white;
  text-align: center;
}
```

**Exemplo visual**: O `div` ficará fixado no topo da página, mesmo quando o usuário rolar a página para baixo.

---

#### 5. **`sticky`** (Adesivo)

* **O que faz**: O `position: sticky` é uma mistura entre `relative` e `fixed`. O elemento fica **relativo até um certo ponto** e depois se torna **fixo** quando o usuário rola a página. Ele "gruda" quando atinge um ponto específico da rolagem.
* **Exemplo**: Um cabeçalho que se comporta como um `relative` até que você role para uma certa posição da página, onde ele se fixa no topo.

```css
header {
  position: sticky;
  top: 0; /* Fica fixo no topo da página quando atinge a posição */
  background-color: #333;
  color: white;
  padding: 10px 0;
  text-align: center;
}
```

**Exemplo visual**: O `header` se move com a rolagem até o topo da página, onde ele "gruda" e permanece visível enquanto a página continua sendo rolada.

---

### Resumo

* **`static`**: Posição normal no fluxo do documento (não é possível alterar).
* **`relative`**: Posição ajustada em relação à sua posição original.
* **`absolute`**: Posição em relação ao primeiro ancestral com `position` diferente de `static`.
* **`fixed`**: Fixo na tela, independentemente da rolagem da página.
* **`sticky`**: Combinação de `relative` e `fixed`, "gruda" na tela após atingir um ponto específico.

Essas propriedades são fundamentais para o controle do layout em CSS e podem ser usadas para criar designs responsivos, menus fixos, ou até mesmo efeitos de rolagem interessantes.

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
