# 🔗 **Mesclando Células com `colspan` e `rowspan`**

## 🧠 **O que são?**

* **`colspan`** → Faz uma célula ocupar **várias colunas na horizontal**.
* **`rowspan`** → Faz uma célula ocupar **várias linhas na vertical**.

Eles são super úteis quando queremos criar cabeçalhos maiores, categorias agrupadas ou células que abrangem mais de uma linha ou coluna.

---

## 🎯 **Exemplos Práticos**

### ✅ **Exemplo de `colspan` (Horizontal)**

```html
<table border="1" style="border-collapse: collapse;">
  <tr>
    <th colspan="3">Informações do Produto</th>
  </tr>
  <tr>
    <th>Produto</th>
    <th>Quantidade</th>
    <th>Preço</th>
  </tr>
  <tr>
    <td>Notebook</td>
    <td>2</td>
    <td>4500</td>
  </tr>
</table>
```

🔸 **O que acontece?**
A primeira linha tem uma célula que ocupa **3 colunas**, funcionando como um título da tabela.

---

### ✅ **Exemplo de `rowspan` (Vertical)**

```html
<table border="1" style="border-collapse: collapse;">
  <tr>
    <th rowspan="2">Dia</th>
    <th colspan="2">Horário</th>
  </tr>
  <tr>
    <th>Início</th>
    <th>Fim</th>
  </tr>
  <tr>
    <td>Segunda</td>
    <td>08:00</td>
    <td>12:00</td>
  </tr>
  <tr>
    <td>Terça</td>
    <td>08:00</td>
    <td>12:00</td>
  </tr>
</table>
```

🔸 **O que acontece?**
A célula “Dia” fica ocupando **duas linhas na vertical**, enquanto a célula “Horário” se divide em **Início** e **Fim** na linha de baixo.

---

## 💡 **Exemplo mais elaborado combinando `colspan` e `rowspan`:**

```html
<table border="1" style="border-collapse: collapse;">
  <tr>
    <th rowspan="2">Produto</th>
    <th colspan="2">Detalhes</th>
    <th rowspan="2">Preço</th>
  </tr>
  <tr>
    <th>Cor</th>
    <th>Tamanho</th>
  </tr>
  <tr>
    <td>Camiseta</td>
    <td>Preta</td>
    <td>M</td>
    <td>50</td>
  </tr>
  <tr>
    <td>Calça</td>
    <td>Azul</td>
    <td>G</td>
    <td>100</td>
  </tr>
</table>
```

🔸 **O que rola aqui?**
O cabeçalho "Produto" e "Preço" ficam verticais (**2 linhas**) e "Detalhes" fica horizontal (**2 colunas**), que se dividem em "Cor" e "Tamanho".

---

## 🚀 **Resumo Visual:**

| Atributo  | Direção | Função                           |
| --------- | ------- | -------------------------------- |
| `colspan` | →       | Mescla células **na horizontal** |
| `rowspan` | ↓       | Mescla células **na vertical**   |

---

## ⚠️ **Dicas de Ouro:**

* Sempre verifique se a quantidade de colunas bate quando usar `colspan` e `rowspan`. Se não bater, a tabela quebra o layout.
* Dá pra misturar `colspan` e `rowspan` na mesma tabela sem problemas.
* Para tabelas mais bonitas, é melhor usar CSS ao invés de `border` diretamente no HTML. Mas pra ensino e rascunho tá valendo!
