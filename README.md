# 🧠 Guia Interativo de Manipulação do DOM com JavaScript

Este repositório é um material de estudo pessoal criado por [Arthur do Couto](https://github.com/Arthur-Couto), com o objetivo de aprofundar e organizar os conhecimentos sobre **manipulação do DOM em JavaScript puro**.

Você pode visualizar o conteúdo como um site de documentação acessando:

🔗 **[guia-dom-javascript (GitHub Pages)](https://arthur-couto.github.io/guia-dom-javascript/)**

---

## 📚 O que você vai encontrar

- ✅ Explicação clara sobre `innerHTML`, `textContent` e `value`
- ✅ Uso da `classList` para manipular classes
- ✅ Conversão de valores do DOM em números
- ✅ Manipulação de eventos com `addEventListener`
- ✅ Criação, inserção, substituição e remoção de elementos
- ✅ Diferenças entre `innerHTML` e `createElement`
- ✅ Delegação de eventos
- ✅ Exemplo prático interativo

---

## 📂 Estrutura do Projeto

1. [innerHTML, textContent, value](#1-innerhtml-textcontent-e-value)
2. [classList](#2-classlist)
3. [Conversão de valores](#3-conversão-de-valores)
4. [Eventos com addEventListener](#4-eventos-com-addeventlistener)
5. [Criação de elementos com createElement](#5-criação-de-elementos-com-createelement)
6. [Remoção e substituição de elementos](#6-remoção-e-substituição-de-elementos)
7. [innerHTML vs createElement](#7-innerhtml-vs-createelement)
8. [Delegação de eventos](#8-delegação-de-eventos)

---

## 1. innerHTML, textContent e value

Use `innerHTML` para inserir HTML, `textContent` para texto puro, e `value` para campos de formulário.

```javascript
element.innerHTML = "<strong>Olá!</strong>";
element.textContent = "Olá!";
let valor = document.getElementById("campo").value;
```

## 2. classList

Adiciona, remove ou alterna classes CSS.

```javascript
element.classList.add("ativo");
element.classList.remove("inativo");
element.classList.toggle("oculto");
```

## 3. Conversão de valores

Sempre converta `input.value` para número, se necessário:

```javascript
let num = Number(input.value);
// ou
let num = +input.value;
```

## 4. Eventos com addEventListener

```javascript
botao.addEventListener("click", () => {
  alert("Clicado!");
});
```

## 5. Criação de elementos com createElement

```javascript
let novo = document.createElement("p");
novo.textContent = "Texto novo!";
document.body.appendChild(novo);
```

## 6. Remoção e substituição de elementos

```javascript
pai.removeChild(filho);
pai.replaceChild(novoElemento, antigoElemento);
```

## 7. innerHTML vs createElement

- `innerHTML` é mais rápido, mas menos seguro (XSS).
- `createElement` é mais seguro e recomendado em ambientes dinâmicos.

## 8. Delegação de eventos

```javascript
lista.addEventListener("click", (e) => {
  if (e.target.tagName === "LI") {
    alert("Item: " + e.target.textContent);
  }
});
```

---

## 📂 Exemplos

Veja exemplos práticos na pasta [`exemplos/`](./exemplos)

---

Feito com 💻 por Arthur do Couto
