# ✨ Tags Especiais do HTML5
## Revolucionando o desenvolvimento web moderno

---

# 📜 Introdução

- HTML5 lançado oficialmente em 2014
- Revolucionou a criação de conteúdo na web
- Eliminou a necessidade de plugins externos (Flash, Silverlight)
- Trouxe tags especiais para mídia e interatividade
- Melhorou a experiência do usuário e a acessibilidade

---

# Objetivos da Aula

- Conhecer as principais tags especiais do HTML5
- Entender suas funcionalidades e atributos
- Aprender melhores práticas de uso
- Explorar exemplos práticos de implementação

---

# 🎧 Tag `<audio>`

**Definição**: Permite reproduzir áudio diretamente no navegador

**Estrutura básica**:
```html
<audio controls>
  <source src="arquivo.mp3" type="audio/mpeg">
  <source src="arquivo.ogg" type="audio/ogg">
  Seu navegador não suporta o elemento de áudio.
</audio>
```

---

# 🎧 Atributos da Tag `<audio>`

**Atributos essenciais**:
- `controls`: Exibe controles de reprodução
- `autoplay`: Inicia automaticamente
- `loop`: Reproduz em loop
- `muted`: Inicia sem som
- `preload`: Controla pré-carregamento

---

# Exemplo de `<audio>`

```html
<h2>🎵 Player de Podcast</h2>

<audio controls preload="metadata">
  <source src="podcast-episodio1.mp3" type="audio/mpeg">
  <source src="podcast-episodio1.ogg" type="audio/ogg">
  <p>Seu navegador não suporta o elemento de áudio. 
     <a href="podcast-episodio1.mp3">Clique aqui para baixar</a>.</p>
</audio>
```

---

# Compatibilidade de `<audio>`

**Formatos recomendados**:
- MP3: Suportado pela maioria dos navegadores
- OGG: Alternativa de código aberto
- WAV: Alta qualidade, arquivos maiores

**Acessibilidade**:
- Sempre forneça alternativa textual
- Inclua link para download
- Use descrições claras do conteúdo

---

# 🎥 Tag `<video>`

**Definição**: Permite incorporar vídeos diretamente nas páginas

**Estrutura básica**:
```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <source src="video.webm" type="video/webm">
  Seu navegador não suporta vídeos HTML5.
</video>
```

---

# 🎥 Atributos da Tag `<video>`

**Atributos importantes**:
- `controls`: Exibe controles de reprodução
- `width` e `height`: Dimensões do player
- `autoplay`: Inicia automaticamente
- `loop`: Reproduz em loop
- `poster`: Define imagem de miniatura
- `preload`: Controla pré-carregamento

---

# Exemplo de `<video>`

```html
<h2>📺 Tutorial de Programação</h2>

<video width="640" height="360" controls poster="thumbnail.jpg">
  <source src="tutorial.mp4" type="video/mp4">
  <source src="tutorial.webm" type="video/webm">
  <p>Seu navegador não suporta vídeos HTML5.
     <a href="tutorial.mp4">Baixe o vídeo</a> para assistir offline.</p>
</video>
```

---

# Legendas e Acessibilidade em `<video>`

**Adicionando legendas com a tag `<track>`**:

```html
<video controls>
  <source src="video.mp4" type="video/mp4">
  <track src="legendas-pt.vtt" kind="subtitles" 
         srclang="pt" label="Português">
  Seu navegador não suporta vídeo.
</video>
```

**Formatos para máxima compatibilidade**:
- MP4 (H.264): Amplamente suportado
- WebM: Formato aberto
- Ogg Theora: Alternativa de código aberto

---

# 🗂️ Tag `<input type="file">`

**Definição**: Permite que usuários selecionem arquivos do dispositivo

**Exemplo básico**:
```html
<label for="arquivo">Selecione uma imagem:</label>
<input type="file" id="arquivo" name="arquivo" accept="image/*">
```

---

# 🗂️ Atributos de `<input type="file">`

**Atributos importantes**:
- `accept`: Especifica tipos de arquivo aceitos
- `multiple`: Permite selecionar múltiplos arquivos
- `required`: Torna o campo obrigatório

**Exemplo**: `accept="image/png, image/jpeg, application/pdf"`

---

# Exemplo Completo de `<input type="file">`

```html
<h2>📤 Envie sua Foto de Perfil</h2>

<form action="/upload" method="post" enctype="multipart/form-data">
  <label for="arquivo">Selecione uma imagem:</label><br>
  <input type="file" id="arquivo" name="arquivo" accept="image/*">
  <p>Formatos aceitos: JPG, PNG ou GIF. Tamanho máximo: 5MB.</p>
  <button type="submit">Enviar</button>
</form>
```

---

# Acessibilidade em `<input type="file">`

**Boas práticas**:
- Associe um `<label>` ao input usando o atributo `for`
- Forneça instruções claras sobre tipos de arquivo aceitos
- Indique tamanhos máximos permitidos
- Use mensagens de erro informativas
- Ofereça feedback visual durante o upload

---

# 🌐 Tag `<iframe>`

**Definição**: Permite incorporar outro documento HTML dentro da página

**Exemplo básico**:
```html
<iframe src="pagina.html" width="600" height="400"></iframe>
```

---

# 🌐 Atributos da Tag `<iframe>`

**Atributos importantes**:
- `src`: URL do documento a ser incorporado
- `width` e `height`: Dimensões do iframe
- `loading`: Controla como o iframe é carregado
- `sandbox`: Restringe capacidades do conteúdo
- `allowfullscreen`: Permite tela cheia

---

# Exemplos de uso de `<iframe>`

**Incorporando mapas**:
```html
<iframe 
  src="https://www.google.com/maps/embed?pb=!1m18!1m12!..."
  width="600" height="450" allowfullscreen loading="lazy">
</iframe>
```

**Incorporando vídeos do YouTube**:
```html
<iframe width="560" height="315" 
  src="https://www.youtube.com/embed/dQw4w9WgXcQ"
  title="Tutorial de HTML5" allowfullscreen>
</iframe>
```

---

# Considerações de segurança com `<iframe>`

**Práticas recomendadas**:
- Use o atributo `sandbox` para conteúdo não confiável
- Use HTTPS para o conteúdo do iframe
- Defina uma política de referência adequada
- Evite incorporar conteúdo de fontes desconhecidas
- Considere alternativas quando possível

---

# 💡 Resumo das Tags Especiais

| Tag | Função | Exemplos de Uso |
|------|---------|------------------|
| `<audio>` | Reproduzir áudio | Podcasts, músicas |
| `<video>` | Incorporar vídeos | Tutoriais, demonstrações |
| `<input type="file">` | Upload de arquivos | Envio de fotos, documentos |
| `<iframe>` | Incorporar conteúdo externo | Mapas, vídeos do YouTube |

---

# 🧠 Exercícios Práticos

1️⃣ **Reprodutor de Podcast**
- Player de áudio com controles
- Descrição para cada episódio
- Opção de download

2️⃣ **Galeria de Vídeos**
- Dois vídeos com controles
- Legendas para um dos vídeos
- Descrição para cada vídeo

---

# 🧠 Exercícios Práticos (cont.)

3️⃣ **Formulário de Envio de Imagens**
- Validação de tipo de arquivo
- Limite de tamanho
- Instruções claras

4️⃣ **Página Incorporada**
- Iframe de conteúdo externo
- Título adequado para acessibilidade
- Atributos de segurança apropriados

---

<!-- _class: lead -->
# 🚀 Conclusão

- As tags especiais do HTML5 representam um avanço significativo
- Permitem criar experiências multimídia ricas
- Eliminam a necessidade de plugins externos
- São essenciais para o desenvolvimento web moderno
- Considere sempre acessibilidade, performance e segurança

---

# Referências e Recursos

- [MDN Web Docs - HTML5](https://developer.mozilla.org/pt-BR/docs/Web/HTML/HTML5)
- [W3Schools - HTML5 Tutorial](https://www.w3schools.com/html/)
- [HTML5 Doctor](http://html5doctor.com/)
- [Can I Use](https://caniuse.com/) - Compatibilidade de navegadores
