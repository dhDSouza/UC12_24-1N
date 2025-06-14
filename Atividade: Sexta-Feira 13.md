# 🕸️ **Atividade Prática de CSS Grid Layout: Mansão Assombrada** 🧟‍♂️

## 📅 Contexto especial: Sexta-feira 13 😱🔪

Hoje você vai montar o layout de uma **Mansão Assombrada** utilizando **CSS Grid Layout**.   
O objetivo é treinar o posicionamento de áreas em um layout bidimensional, controlando tanto linhas quanto colunas.

---

## 🎯 Objetivo

Criar um layout completo de uma mansão assombrada, utilizando as propriedades do **CSS Grid**.

---

## 🏰 Áreas do Layout

O seu layout deve conter as seguintes áreas:

* **Entrada Principal** `(header)`
* **Corredor Assombrado** `(sidebar)`
* **Sala Principal** `(main)`
* **Laboratório Secreto** `(lab)`
* **Porão** `(footer)`

---

## 🔧 Regras de Montagem do Grid

* O container principal deve utilizar `display: grid`.

* O grid deve ter:

  * **3 colunas**:

    * Primeira coluna: `200px`
    * Segunda coluna: `1fr` (fracionada)
    * Terceira coluna: `300px`
  * **3 linhas**:

    * Primeira linha: `100px` (header)
    * Segunda linha: ocupar o restante da altura (`1fr`)
    * Terceira linha: altura automática (`auto`) para o footer

* As áreas devem ser posicionadas da seguinte forma:

| Linha/Coluna | Coluna 1                                | Coluna 2       | Coluna 3            |
| ------------ | --------------------------------------- | -------------- | ------------------- |
| Linha 1      | Entrada Principal em todas as 3 colunas |                |                     |
| Linha 2      | Corredor                                | Sala Principal | Laboratório Secreto |
| Linha 3      | Footer ocupando todas as 3 colunas      |                |                     |

* Utilize `grid-template-areas` para organizar o posicionamento.

* Adicione uma distância entre os elementos com `gap`.

---

## 🎨 Personalização

* Escolha cores que remetam ao tema **terror**: vermelho-sangue, roxo-mistério, preto, cinza, etc.
* Utilize **ícones ou emojis** (ex.: 👻, 🕸️, 🔪, 🩸, ☠️) no conteúdo das áreas.
* Use uma fonte "assustadora" (ex.: Google Fonts `Creepster`).

---

## 🧪 Entrega

* Submeta o arquivo `.html` e o `.css` separadamente.
* Teste em navegadores diferentes para garantir o comportamento esperado.

---

<div align="center">
  <img src="https://i.gifer.com/ExcR.gif" alt="Jason aterroizante">
  <p>Fonte: <em><a href="https://i.gifer.com/ExcR.gif" target="_blank">https://i.gifer.com/ExcR.gif</a></em></p>
</div>
