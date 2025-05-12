# **Estruturando e Estilizando Páginas com HTML**

### 1. **Introdução às Tags de Estrutura**

#### 1.1. **Tag `<div>` e `<span>`**

* **Tag `<div>`**: Usada para agrupar conteúdo e dividir a página em seções.

  * **Exemplo:**

  ```html
  <div>
      <h1>Seção Principal</h1>
      <p>Este é um parágrafo dentro de uma div.</p>
  </div>
  ```

  * **Explicação**: A `<div>` é uma "caixa" para organizar o conteúdo. Ela ajuda a estruturar a página em blocos.

* **Tag `<span>`**: Usada para aplicar estilos a uma parte específica de um texto.

  * **Exemplo:**

  ```html
  <p>Esta palavra é <span style="color: red;">vermelha</span>.</p>
  ```

  * **Explicação**: Diferente da `<div>`, o `<span>` é uma tag de linha, usada dentro de textos. Ideal para estilizar partes específicas.

#### 1.2. **Tags Semânticas: `<header>`, `<footer>`, e `<section>`**

As tags semânticas ajudam a tornar o código mais intuitivo, tanto para os desenvolvedores quanto para os motores de busca.

* **Tag `<header>`**: Representa o cabeçalho de um documento ou seção.

* **Tag `<footer>`**: Representa o rodapé.

* **Tag `<section>`**: Divide o conteúdo em seções distintas.

* **Exemplo:**

  ```html
  <header>
      <h1>Bem-vindo ao Meu Site</h1>
      <nav>
          <a href="#home">Home</a> |
          <a href="#sobre">Sobre</a>
      </nav>
  </header>

  <section id="sobre">
      <h2>Sobre Mim</h2>
      <p>Texto sobre mim...</p>
  </section>

  <footer>
      <p>&copy; 2025 Meu Site</p>
  </footer>
  ```

* **Explicação**: O uso dessas tags ajuda a melhorar a estrutura do código, facilitando a leitura e manutenção.

---

### 2. **Introdução ao Atributo `style` (CSS Inline)**

* **Explicação**: O atributo `style` permite adicionar estilos CSS diretamente aos elementos HTML. Este método é simples, mas para projetos maiores é recomendado o uso de arquivos CSS externos.

#### 2.1. **Exemplo de Estilo Inline:**

* **Exemplo:**

  ```html
  <h1 style="color: blue; text-align: center;">Título Centralizado em Azul</h1>
  <p style="font-size: 18px; color: green;">Este parágrafo é verde e tem tamanho de fonte 18px.</p>
  ```

  * **Explicação**: O `style` é usado para personalizar a aparência do texto, controlando cores, fontes, alinhamento, etc.

#### 2.2. **Alinhamento e Espaçamento**

* **Exemplo de alinhamento e espaçamento:**

  ```html
  <h2 style="text-align: center;">Título Centralizado</h2>
  <p style="margin-bottom: 20px;">Este parágrafo tem um espaçamento inferior de 20px.</p>
  ```

* **Explicação**:

  * O atributo `text-align` alinha o texto horizontalmente.
  * `margin-bottom` cria um espaço abaixo do elemento.

#### 2.3. **Cor de Fundo e Imagens de Fundo**

Adicionar cor de fundo e imagens de fundo para uma personalização maior.

* **Exemplo:**

  ```html
  <div style="background-color: #f0f0f0; padding: 20px;">
      <h2>Seção Com Fundo</h2>
      <p>Esta seção tem um fundo cinza claro.</p>
  </div>

  <div style="background-image: url('https://via.placeholder.com/800x200'); background-size: cover; color: white; padding: 40px;">
      <h2>Seção Com Imagem de Fundo</h2>
      <p>O fundo está configurado com uma imagem.</p>
  </div>
  ```

* **Explicação**: A propriedade `background-image` permite adicionar uma imagem como fundo, e `background-size: cover` faz a imagem cobrir toda a área disponível.

---

### 3. **Criando Links Internos e Navegação**

* **Explicação**: Links internos ajudam a navegar dentro da mesma página.

#### 3.1. **Exemplo de Link Interno:**

* **Exemplo:**

  ```html
  <h2 id="seção1">Seção 1</h2>
  <p>Conteúdo da Seção 1.</p>

  <h2 id="seção2">Seção 2</h2>
  <p>Conteúdo da Seção 2.</p>

  <a href="#seção1">Voltar para a Seção 1</a>
  ```

* **Explicação**: Utilizamos o atributo `id` para marcar um ponto específico na página. O link então navega até esse ponto com `href="#id"`.

#### 3.2. **Navegação Fixa (Sticky Navigation)**

* **Explicação**: A navegação fixa fica visível enquanto o usuário rola a página.

* **Exemplo de navegação fixa:**

  ```html
  <div style="position: fixed; top: 0; left: 0; width: 100%; background-color: #333; color: white; padding: 10px;">
      <nav>
          <a href="#home" style="color: white;">Home</a> |
          <a href="#sobre" style="color: white;">Sobre</a> |
          <a href="#contato" style="color: white;">Contato</a>
      </nav>
  </div>

  <div style="margin-top: 60px;">
      <section id="home">
          <h2>Home</h2>
          <p>Bem-vindo à página inicial!</p>
      </section>
      <section id="sobre">
          <h2>Sobre</h2>
          <p>Texto sobre...</p>
      </section>
      <section id="contato">
          <h2>Contato</h2>
          <p>Informações de contato...</p>
      </section>
  </div>
  ```

* **Explicação**: A navegação fica "fixa" no topo da página enquanto o usuário rola, permitindo fácil acesso aos links.

---

### 4. **Formulários Simples**

Embora o foco seja HTML, os formulários são essenciais para coleta de dados dos usuários e são importantes para o próximo passo do aprendizado.

#### 4.1. **Exemplo de Formulário:**

* **Exemplo:**

  ```html
  <h2>Formulário de Contato</h2>
  <form action="#" method="post">
      <label for="nome">Nome:</label>
      <input type="text" id="nome" name="nome" required>
      <br>

      <label for="email">E-mail:</label>
      <input type="email" id="email" name="email" required>
      <br>

      <label for="mensagem">Mensagem:</label>
      <textarea id="mensagem" name="mensagem"></textarea>
      <br>

      <input type="submit" value="Enviar">
  </form>
  ```

* **Explicação**: O formulário coleta informações do usuário, como nome, e-mail e mensagem. O atributo `required` garante que os campos não sejam deixados em branco.

---

### 5. **Exercícios Finais**

1. **Crie uma Página de Portfólio:**

   * Crie uma página com três seções:

     * **Introdução**: Uma breve descrição sobre você.
     * **Habilidades**: Use listas não ordenadas (`<ul>`).
     * **Projetos**: Crie links para projetos fictícios ou reais.

2. **Adicionar Estilos Personalizados:**

   * Altere a cor de fundo das seções, e adicione margens e fontes diferentes para os títulos e parágrafos.

3. **Criar Links Internos:**

   * Adicione links internos para navegar entre as seções da página (por exemplo, de "Introdução" para "Habilidades").

4. **Formulário de Contato:**

   * Adicione um formulário básico para coleta de informações (nome, e-mail, mensagem).

5. **Desafio de Navegação Fixa:**

   * Crie uma navegação fixa no topo da página, permitindo que o usuário navegue facilmente entre as seções.

---

### **Resumo da Aula**

* **Tags de Estrutura**: Como usar `<div>`, `<span>`, `<header>`, `<footer>`, e `<section>` para organizar o conteúdo de forma semântica.

* **Estilos Inline**: Como estilizar páginas usando o atributo `style`, incluindo alinhamento de texto, cor de fundo, e imagens de fundo.
* **Links Internos**: Criando navegação dentro da mesma página usando links com o atributo `href`.
* **Formulários**: Introdução ao HTML de formulários, um dos elementos mais importantes para coletar dados do usuário.

