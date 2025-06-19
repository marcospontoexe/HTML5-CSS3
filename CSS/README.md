# CSS
**CSS** (Cascading Style Sheets), uma linguagem que descreve como os elementos HTML devem ser formatados para exibição.

- **Não é linguagem de programação**, pois não conseguimos realizar comandos condicionais (_if/else_), nem laços de repetição (_for/while_) ou nem funções, por exemplo.
- É uma linguagem descritiva para estilizar páginas web, visualizadas em navegadores.
- Folhas de estilo externas são armazenadas em arquivos com extensão `.css`, para serem aproveitadas em diversas páginas HTML, economizando o trabalho de formatação.

---

## Regra CSS

O CSS permite alterar completamente o visual de uma página web, apenas trocando o conjunto de formatação CSS.

Em resumo: **HTML + CSS**

- O HTML estrutura o layout de um documento web, ou seja, organiza os elementos visuais de um documento.
- O CSS formata a exibição dos elementos HTML.

Entendemos CSS por uma linguagem descritiva que permite a formatação visual de elementos de um documento HTML. Logo, não é uma linguagem de programação.

Basicamente, o CSS é composto por regras que indicam como formatar elementos HTML. É o navegador que interpreta as regras de associação entre um documento HTML e seu CSS, e as aplica ao documento, modificando sua aparência.

A composição de uma regra está exibida na Figura a seguir:

![Figura 1: Sintaxe da Regra CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/1.jpeg)

* [Veja como configurar cores](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/02-cores).
* [Vejam mais sobre tipografia (fontes)](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/03-tipografia(fontes)).
* [Veja como fazer alinhamento](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/04-alinhamento).
* [Resposividade](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/08-responsividade).
* [Imagens de fundo](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/09-imagens-fundo).
* [Mediaquery](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/10-mediaquery).

---

## Tipos de CSS

### Sintaxe da regra CSS

- **SELETOR**: indica o elemento HTML que recebe o estilo definido no bloco de declarações.
- **BLOCO DE DECLARAÇÃO**: delimitado por chaves `{ }`, mantém declarações separadas por `;`, onde temos: uma **PROPRIEDADE CSS** e seu **VALOR**, separados por `:`.

As regras de estilo CSS podem ser definidas de três formas:

1. **Inline**: as regras são definidas dentro de uma tag HTML.
2. **Interna**: as regras são definidas no cabeçalho do documento HTML.
3. **Externa**: as regras são definidas em um documento separado, externo a todas as páginas HTML.

Vamos praticar cada uma dessas formas de definir estilo para os elementos HTML.

---

#### 1. Sintaxe: Regra CSS inline

Utiliza o atributo `style` do elemento HTML.  
O código CSS é adicionado diretamente no elemento HTML por meio do atributo `style`: 

```html
<p style="text-align: right;">texto</p>
```

**Evite usar esta prática!** Ela mistura o código HTML com CSS e não permite o reuso do CSS, tornando a manutenção e evolução do código mais complexa.

Vamos criar um documento HTML formatado com folha de estilo CSS, para visualização em um navegador. Também vamos utilizar a ferramenta de inspeção de página do navegador Google Chrome.

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">    
    <title>Página HTML com CSS</title>
</head>
<body>
    <h1 style="color:rgb(17, 128, 35)">CSS inline</h1>
    <p  style="color:deepskyblue; font-family:Verdana; text-align:center">Texto 1.</p>
    <p  style="color:brown; font-family:'Courier New'; text-align:right">Texto 2. </p>
</body>
</html>
```

> **Dica:** Você pode utilizar um ambiente integrado de desenvolvimento, ou IDE – do inglês *Integrated Development Environment* –, como o Visual Studio Code da Microsoft ([https://code.visualstudio.com/download](https://code.visualstudio.com/download)).

![Figura 2: HTML com CSS inline](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/2.jpeg)

---

#### 2. Sintaxe: Regra CSS interna

O código CSS é inserido em um elemento `<style>`, que geralmente fica dentro da seção `<head>`:

```html
<head>    
   <title>Página HTML com CSS</title>
   <style>
      p {
         color: blue; 
         font-family: Verdana; 
      }
   </style>
</head>
```

Também evite usar esta prática! Ela deixa no mesmo arquivo o código HTML e o código CSS, o que não permite o reuso do CSS, podendo gerar duplicidade de código e tornar a manutenção e evolução do código mais complexa.

Vamos criar um documento HTML formatado com folha de estilo CSS, para visualização em um navegador.

Siga os passos indicados a seguir para ver o CSS interno funcionando:

```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">    
    <title>Página HTML com CSS</title>
    <style>
        p {
            color: deepskyblue; 
            font-family: Verdana; 
            text-align: center;
        }
        h1 {
            color: rgb(17, 128, 35);
        }
    </style>
</head>
<body>
    <h1>CSS interno</h1>
    <p>Texto 1.</p>
    <p>Texto 2.</p>
</body>
</html>
```

![Figura 3: HTML com CSS interna](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/3.jpeg)
---

#### 3. Sintaxe: Regra CSS externa

O código CSS é colocado em um arquivo `.css`, separadamente do arquivo `.html`.  

Neste caso, precisamos ligar o arquivo `.css` ao arquivo `.html`, o que é realizado por um link adicionado ao elemento `<head>`:

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

**Esta é uma boa prática!** Ela separa os arquivos de HTML e CSS, permitindo o reuso do CSS, evitando duplicidade de código, o que torna a manutenção e evolução do código menos complexa.

Vamos criar um documento HTML formatado com folha de estilo CSS, para visualização em um navegador.

Siga os passos indicados a seguir para ver o CSS externo funcionando:

Arquivo HTML:
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">    
    <title>Página HTML com CSS</title>
    <link href="css/style.css" rel="stylesheet" type="text/css"/>
</head>
<body>
    <h1>CSS externo</h1>
    <p>Texto 1.</p>
    <p>Texto 2.</p>
</body>
</html>
```

Arquivo CSS:
```css
p {
    color: deepskyblue; 
    font-family: Verdana; 
    text-align: center;
}

h1 {
    color: rgb(17, 128, 35);
}
```

![Figura 4: HTML com CSS externo](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/4.jpeg)

[Veja mais exemplos sobre regra de estilo](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/01-estilos).

---

## Seletores CSS

Os **seletores CSS** são usados para "encontrar" (ou selecionar) os elementos HTML que desejamos estilizar.

Podemos organizar os seletores CSS nas seguintes categorias:

1. **Seletor de elemento.**
2. **Seletor de id.**
3. **Seletor de classe.**
4. **Seletores de combinação** (agrupa elementos).
5. **Seletores de pseudo classe** (seleciona elementos com base em um determinado estado).
6. **Seletores de pseudo elemento** (Um pseudo-elemento permite estilizar partes específicas de um elemento que não podem ser acessadas diretamente no HTML.)

Vamos conhecer melhor cada um deles.

---

### Seletor de elemento CSS
Seleciona qual elemento HTML receberá o estilo, baseado no seu nome HTML, ou tag.

#### Exemplos de seletores:

- **`p`** serve para formatar um elemento HTML `<p>`.
- **`*`** serve para formatar elementos HTML de qualquer tipo.

```html
<!DOCTYPE html>
<html>
<head>
   <style>
      * { /* formatação para qualquer elemento HTML */
         font-family: Cambria, serif;
         color: darkolivegreen;
      }
      p { /* formatação para elemento HTML <p> */
         text-align: center;
         color: red;
      } 
   </style>
</head>
<body>
   <h2>H2 é afetado pelo seletor *</h2>
   <h3>H3 também é afetado pelo seletor *</h3>
   <p>Todo parágrafo é afetado por estilo próprio.</p>
   <p id="para1">Eu também!</p>
   <p>E eu idem!</p>
</body>
</html>
```

![Figura 5: Seletor de elemento CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/5.jpeg)

[Veja mais exemplos de uso com seletores](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/05-seletores).

---

### Seletor de id CSS

O seletor usa o atributo `id` (identificador) de um elemento HTML para selecionar um elemento específico.

O `id` de um elemento **é único dentro de uma página HTML**, logo o seletor de id é aplicado em um único elemento da página.

**USO CORRETO:** escreva um caractere hash (`#`), seguido do `id` do elemento.

```html
<!DOCTYPE html>
<html>
<head>
   <style>
      #para1 {
         text-align: center;
         color: red;
      }
   </style>
</head>
<body>
   <p id="para1">Olá mundo!</p>
   <p>Este parágrafo não é afetado pelo estilo.</p>
```

![Figura 6: Seletor de id CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/6.jpeg)

---

### Seletor de classe CSS

O seletor de classe seleciona elementos HTML com um atributo de `class` específico. Para selecionar elementos de uma classe, escrevemos um ponto (`.`), seguido do nome da classe.

```html
<!DOCTYPE html>
<html>
<head>
   <style>
      .center {
         text-align: center;
         color: red;
      }
   </style>
</head>
<body>
   <h1 class="center">Cabeçalho vermelho e centralizado</h1>
   <p class="center">Parágrafo vermelho e centralizado.</p>
</body>
</html>
```

![Figura 7: Seletor de classe CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/7.jpeg)

Elementos HTML também podem se referir a mais de uma classe.

```html
<!DOCTYPE html>
<html>
   <head>
      <style>
         p.center {
         text-align: center;
         color: red;
         }
         p.large {
         font-size: 300%;
         }
      </style>
   </head>
   <body>
      <h1 class="center">Este cabeçalho não será afetado</h1>
      <p class="center">Este parágrafo será vermelho e centralizado. </p>
      <p class="center large">Este parágrafo será vermelho, centralizado e na fonte grande (large). </p>
   </body>
</html>
```

![Figura 8: Seletor de classe CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/8.jpeg)

---

### Seletor de pseudoclasse CSS

Uma **pseudoclasse** é usada para definir um estado especial de um elemento. Pode ser usado para estilizar um elemento quando um usuário passa o mouse sobre ele, ou quando é um link visitado, ou quando o elemento estiver em foco, por exemplo.

**Sintaxe para pseudoclasse:**  
```
selector:pseudo-class { property: value; }
```

```html
<!DOCTYPE html>
<html>
   <head>
      <style>
         a:link {    /* pseudo-classe p/ link NÃO VISITADO */
         color: red;
         }
         a:visited { /* pseudo-classe p/ link VISITADO*/
         color: green;
         }
         a:hover {   /* pseudo-classe p/ MOUSE SOBRE o link */
         color: hotpink;
         }
         a:active {   /* pseudo-classe p/ link SELECIONADO*/
         color: blue;
         }
      </style>
   </head>
   <body>
      <h2>Estilo para link, dependendo do seu estado</h2>
      <p><b><a href="default.asp" target="_blank">Este é um link</a></b></p>
      <dl>
         <dt>
            <p><b>Importante 1:</b>
         </dt>
         <dd><b>a:hover</b> DEVE vir depois de <b>a:link</b> e <b>a:visited</b>, para ser efetivo no CSS.</dd>
         <dt>
            <p><b>Importante 2:</b> 
         </dt>
         <dd><b>a:active</b> DEVE vir depois de <b>a:hover</b>, para ser efetivo no CSS.</dd>
      </dl>
   </body>
</html>
```

---

### Seletor de pseudo elemento CSS
Um **pseudo-elemento** permite **estilizar partes específicas de um elemento** que não podem ser acessadas diretamente no HTML. Ele simula (ou "finge", daí o "pseudo") a existência de um elemento novo dentro de outro — **sem alterar o HTML**.

Ele é escrito com **dois-pontos duplos `::`** (embora os navegadores aceitem um só por compatibilidade antiga).

| Pseudo-elemento  | O que faz                                                 |
| ---------------- | --------------------------------------------------------- |
| `::before`       | Insere conteúdo antes do conteúdo real do elemento        |
| `::after`        | Insere conteúdo depois do conteúdo real do elemento       |
| `::first-letter` | Estiliza a **primeira letra** de um bloco de texto        |
| `::first-line`   | Estiliza a **primeira linha** visível de um parágrafo     |
| `::selection`    | Estiliza o texto selecionado pelo usuário                 |
| `::placeholder`  | Estiliza o texto de dica (placeholder) dentro de um input |

#### `::before` e `::after`

```css
p::before {
  content: "→ ";
  color: red;
}
```

Isso adiciona uma setinha antes do conteúdo de todos os `<p>` (parágrafos), sem alterar o HTML.

#### `::first-letter`

```css
p::first-letter {
  font-size: 2em;
  color: blue;
}
```

Deixa a **primeira letra** de cada parágrafo grande e azul (como em livros antigos).

#### `::selection`

```css
::selection {
  background: yellow;
  color: black;
}
```

### Seletor de agrupamento CSS

Para minimizar o código, podemos agrupar os seletores, separando cada seletor com uma vírgula.

```html
<!DOCTYPE html>
<html>
<head>
   <style>
      h1, h2, p {
         text-align: center;
         color: red;
      }
   </style>
</head>
<body>
   <h1>Olá mundo!</h1>
   <h2>Cabeçalho menor!</h2>
   <p>Este é um parágrafo.</p>
</body>
</html>
```

![Figura 9: Seletor de agrupamento CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/9.jpeg)

---

## CSS para a “box” (caixa) de elemento HTML

Quase todos os elementos HTML podem ser compreendidos como uma **box** (caixa), permitindo agrupamentos horizontal ou vertical, ou ainda inseridas uma dentro da outra.

As propriedades CSS evidenciam essa compreensão, pois você precisará indicar a dimensão dos elementos HTML, como largura e altura, ou sua cor, posição relativa aos demais elementos, ou ainda posição do seu conteúdo interno, e assim por diante.

A **box** que representa um elemento HTML tem algumas propriedades que definem o espaço que ocupam na página web, como relacionado abaixo:

- `height`: altura do elemento; é definida em pixel (ex: `50px`) ou em porcentagem (ex: `30%`).
- `width`: largura do elemento; é definida em pixel (ex: `80px`) ou em porcentagem (ex: `50%`).
- `border`: linha que envolve o elemento.
- `margin`: espaço externo ao elemento.
- `padding`: espaço interno ao elemento, entre a borda e o conteúdo.

Veja como é compreendida a box de um elemento HTML, exibida na Figura a seguir:

![Figura 10: Box do elemento HTML, formatada pelo CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/10.jpg)

Tudo começa a partir do conteúdo (content), que representamos acima com o bla 
bla bla… Por padrão, toda caixa é composta apenas pelo conteúdo e não possui 
padding, nem border, nem outline e nem margin. Uma exceção curiosa é o 
elemento <body> que já vem com uma margin de 8px. 

Todo conteúdo possui uma largura (**width**) e uma altura (**height**) e a esse conjunto 
de propriedades, damos o nome de box-size (tamanho da caixa). O tamanho da 
caixa não inclui as medidas de padding, border, outline e margin. 

Depois do conteúdo e de seu tamanho, vamos nos focar na **borda** que fica em volta 
dele. Ela pode ter uma espessura, uma cor e um formato. 

Entre a borda e o conteúdo - da borda para dentro - temos o preenchimento 
(**padding**) e da borda para fora, temos a margem (**margin**). 


Entre a margem e a borda, podemos determinar o contorno (**outline**) que é muito 
pouco utilizado, mas existe. Ele é um traçado visual que podemos criar fora da borda 
e o cálculo da sua espessura faz parte da margem estabelecida. 

### Tipos de Caixa 
Dependendo do comportamento da caixa, podemos classificar um elemento em uma de duas categorias: 
* Caixa do tipo **block-level**: Um elemento dito block-level sempre vai se iniciar em uma nova linha e vai ocupar a 
largura total do elemento onde ele está contido. Se não estiver contido em nenhuma 
outra caixa, ele vai **ocupar 100%** da largura do **```<body>```**. O elemento block-level mais conhecido é o **```<div>```** e suas variações semânticas 
modernas da HTML5, como **```<main>```**, **```<section>```**, **```<aside>```**, etc.

Na lista a seguir, coloquei alguns elementos HTML que são block-level: 
```html
<address> <article> <aside> <blockquote> <canvas> <dd>
<div> <dl> <dt> <fieldset> <figcaption> <figure>
<footer> <form> <h1> - <h6> <header> <hr> <li>
<main> <nav> <noscript> <ol> <p> <pre>
<section> <table> <tfoot> <ul> <video>
```

* Caixa do tipo **inline-level**: Um elemento do tipo inline-level não vai começar em uma nova linha, e sim no ponto 
exato onde foram definidos. E a largura dele vai ocupar apenas o tamanho relativo ao 
seu conteúdo. 

Abaixo, listei alguns elementos inline-level usados pela HTML: 
```html
<a> <abbr> <acronym> <b> <bdo> <br>
<button> <cite> <code> <dfn> <em> <i>
<img> <input> <kbd> <label> <map> <object>
<output> <q> <samp> <script> <select> <small>
<span> <strong> <sub> <textarea> <tt> <var>
```

[Veja mais exemplos sobre o uso de caixas HTML](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/06-caixas).

### Tag HTML `<div>` e Tag HTML `<span>`

As tags `<div>` e `<span>` definem uma divisão ou parte de um documento HTML. Qualquer tipo de conteúdo (elementos HTML) pode ser colocado dentro delas!

Ambas são usadas como um contêiner para elementos HTML, e podem ser:
- Estilizados com CSS usando o atributo `class` ou `id`; ou
- Manipulados com JavaScript.

A diferença entre elas é que:
- A tag `<div>` faz o agrupamento de elementos a nível de bloco.
- A tag `<span>` faz o agrupamento de elementos a nível de linha.

Ou seja, se você tem algum conteúdo em texto que precise ser agrupado e/ou destacado, você deve usar a tag `<span>`.

Veja no exemplo da Figura a seguir, em que a tag `<div>` é usada para estilizar elementos na página HTML:

![Figura 11: Box de elemento HTML, exemplificado com a tag <div>](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/11.jpeg)

As propriedades `padding`, `margin` e `border` são aplicadas aos quatro lados de um elemento HTML: superior, direita, inferior e esquerdo.

No exemplo da Figura anterior, essas propriedades receberam apenas um valor, que foi aplicado a todos os lados do elemento:


```html
<!DOCTYPE html>
<html>
<head>
   <style>
      .texto1 {
         font-family: Arial, Helvetica, sans-serif;
         background-color: LightSeaGreen;
         color: white;
         border: 2px solid black;
         margin: 20px;
         padding: 20px;
      }
      .texto2 {
         font-family: "Lucida Console", "Courier New", monospace;
         background-color: Chocolate;
         color: white;
         border: 4px solid black;
         margin: 40px;
         padding: 40px; /* um valor para toda a borda */
      }
   </style>
</head>
<body>
   <div class="texto1">
      <h2>Box 1</h2>
      <p>Verde marinho claro, borda 2px, margem 20px e padding 20px.</p>
   </div>
   <div class="texto2">
      <h2>Box 2</h2>
      <p>Chocolate, borda 4px, margem 40px e padding 40px.</p>
   </div>
</body>
</html>
```

Contudo, podemos especificar um valor para cada lado do elemento. Detalhamos esse tratamento para `padding` e `margin` a seguir.

---

### Posicionando elementos
A propriedade **position** no CSS define como um elemento HTML é posicionado na página. Ela determina o comportamento do elemento em relação ao seu contêiner ou à janela (viewport).

#### Valores principais de `position`:

| Valor      | O que faz                                                                                                                                      |
| ---------- | ---------------------------------------------------------------------------------------------------------------------------------------------- |
| `static`   | **Padrão**. O elemento é posicionado conforme o fluxo normal do HTML.** Não responde** ao top, right, bottom, left   |
| `relative` | Move o elemento **relativamente à sua posição original**.                                                                                      |
| `absolute` | Move o elemento **relativamente ao elemento pai com `position: relative`**, ou ao `<body>` se não houver pai posicionado. Sai do fluxo normal. |
| `fixed`    | Fixa o elemento **em relação à janela do navegador** (viewport).                                                                               |
| `sticky`   | O elemento fica entre `relative` e `fixed`: **rola com a página até um ponto e depois fixa**.                                                  |






1. **`static`**

   * Valor padrão.
   * O elemento segue o fluxo normal da página.
   * Propriedades como `top`, `left`, etc., não têm efeito. ([w3schools.com][1])

2. **`relative`**

   * Mantém-se no fluxo, mas pode ser deslocado em relação à sua posição original usando `top`, `left`, etc.
   * O espaço original do elemento é preservado.
   * Cria contexto para uso de `absolute` em elementos filhos e permite `z-index`. ([css-tricks.com][2])

3. **`absolute`**

   * Remove o elemento do fluxo; os demais agem como se ele não existisse.
   * Posiciona-se em relação ao ancestral posicionado mais próximo (`relative`, `absolute`, `fixed`) ou ao *initial containing block* (normalmente o `body`). ([en.wikipedia.org][3], [developer.mozilla.org][4])

4. **`fixed`**

   * Também desconecta o elemento do fluxo.
   * Posiciona-o em relação à viewport, mantendo-o visível mesmo durante o scroll. ([w3schools.com][1])

5. **`sticky`**

   * Híbrido entre `relative` e `fixed`.
   * Funciona como `relative` até que atinja um limite de rolagem (e.g. `top: 0`), momento em que “cola” à viewport enquanto estiver visível. ([youtube.com][5])

---

## 🔎 Um pouco de teoria

* **Elementos *posicionados*** são aqueles com `position` diferente de `static` – ou seja, `relative`, `absolute`, `fixed` ou `sticky`. ([developer.mozilla.org][4])
* O uso de `top`, `right`, `bottom` e `left` só tem efeito quando o elemento está *posicionado*. ([developer.mozilla.org][4])
* A posição `absolute` retira o elemento do fluxo, permitindo sobreposição sem alterar o layout dos outros elementos por estar “fora da estrutura”. ([css-tricks.com][2])
* Já o `relative` apenas move visualmente o elemento, mantendo seu espaço original reservado para evitar mudanças drásticas no layout.&#x20;
* `fixed` é posicionado em relação à janela, ideal para elementos que devem ficar sempre visíveis (como headers fixos). ([css-tricks.com][2])
* `sticky` combina o comportamento normal com o fixo após o scroll alcançar um certo ponto – perfeito para menus e cabeçalhos que “grudam” ao rolar. ([css-tricks.com][2])

---

## 📹 Vídeo recomendado

Para visualizar na prática, esse vídeo do canal W3Schools é excelente: uma comparação animada entre os cinco valores de `position` no CSS:

[CSS positions explained | static, relative, absolute, fixed and sticky](https://www.youtube.com/watch?v=Sb4oI8vU2FU&utm_source=chatgpt.com)

---

### 🧠 Dicas rápidas

* Use `relative` para criar contexto ou pequenos deslocamentos sem romper o fluxo.
* Use `absolute` para sobreposição precisa, respeitando um ancestral posicionado.
* Use `fixed` para elementos que ficam visíveis durante o scroll.
* Use `sticky` para “grudar” elementos no scroll sem sair do fluxo inicialmente.

---

Quer ver exemplos em código, casos de uso reais ou até exercícios? Posso criar também! É só dizer 😊

[1]: https://www.w3schools.com/css/css_positioning.asp?utm_source=chatgpt.com "CSS Layout - The position Property - W3Schools"
[2]: https://css-tricks.com/absolute-relative-fixed-positioining-how-do-they-differ/?utm_source=chatgpt.com "Absolute, Relative, Fixed Positioning: How Do They Differ?"
[3]: https://en.wikipedia.org/wiki/CSS?utm_source=chatgpt.com "CSS"
[4]: https://developer.mozilla.org/en-US/docs/Web/CSS/position?utm_source=chatgpt.com "position - CSS - MDN Web Docs - Mozilla"
[5]: https://www.youtube.com/watch?v=FNsn0pBmrKs&utm_source=chatgpt.com "Absolute, Relative, Fixed & Sticky Position | CSS Tutorial - YouTube"

---

### Grouping Tags e Semantic Tags 
A linguagem HTML padrão tinha apenas duas tags de agrupamento genérico: a ```<div>```(elemento agrupador do tipo **block-level**) e a ```<span>``` (elemento agrupador do tipo **inline-level**). No mais, eles agem exatamente da 
mesma maneira, servindo para juntar vários outros elementos HTML. 

Com o surgimento da HTML5, surgiram as **tags semânticas de agrupamento**. Isso não 
significa que as ```<div>``` e ```<span>``` (agora chamadas de não-semânticas) deixaram de 
existir ou ficaram **obsoletas**, mas seu uso agora faz menos sentido, pois temos tags 
para dividir as partes do nosso documento HTML. 

Vamos compreender a partir de agora os principais agregadores semânticos da HTML5. 

* **Header**: Cria áreas relativas a cabeçalhos. Pode ser o cabeçalho principal de um site ou até 
mesmo o cabeçalho de uma seção ou artigo. Normalmente inclui títulos `<h1>` - `<h6>`, busca, menu, apresentação, configuração, login
e subtítulos. **Podem também conter menus de navegação**. 

* **Nav**: Define uma área que possui os **links de navegação** pela 
estrutura de páginas que vão compor o website. Um 
```<nav>``` pode estar dentro de um ```<header>```. 

* **Main**: É um agrupador usado para delimitar o **conteúdo principal do nosso site**. Normalmente concentra as 
*seções*, *artigos* e *conteúdos periféricos*. 

* **Section**: **Cria seções para sua página**. Ela pode conter o conteúdo diretamente no seu corpo ou 
dividir os conteúdos em artigos com conteúdos específicos. Segundo a documentação 
oficial da W3C, “uma seção é um agrupamento temático de conteúdos, tipicamente 
com um cabeçalho”. 

* **Article**: Um artigo é um elemento que **vai conter um conteúdo** que pode ser lido de forma 
independente e dizem respeito a um mesmo assunto. Podemos usar um ```<article>```
para delimitar um post de blog ou fórum, uma notícia, etc. 

* **aside**: Delimita um conteúdo periférico e complementar ao conteúdo principal de um artigo ou seção. Normalmente um conteúdo `<aside>` está posicionado ao lado de um determinado texto ou até mesmo no meio dele.

* **footer**: Cria um rodapé para o site inteiro, seção ou artigo. É um conteúdo que não faz parte 
diretamente do conteúdo nem é um conteúdo periférico (o que caracterizaria um 
`<aside>`), mas possui informações sobre autoria do conteúdo, links adicionais, mapa 
do site, documentos relacionados. 

---

### Propriedade `padding`

Podemos atribuir valores diferentes para cada lado da **box** do elemento HTML, para o `padding`. Veja os exemplos na tabela e figura a seguir:
<h3>Propriedade padding</h3>
<table border="1" cellpadding="6" cellspacing="0">
  <thead>
    <tr>
      <th>Exemplo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <pre><code>div {
    padding: 25px 50px 75px 100px;
}</code></pre>
      </td>
      <td>
        <ul style="margin: 0; padding-left: 18px;">
          <li><strong>padding superior</strong> é de <strong>25px</strong></li>
          <li><strong>padding direito</strong> é de <strong>50px</strong></li>
          <li><strong>padding inferior</strong> é de <strong>75px</strong></li>
          <li><strong>padding esquerdo</strong> é de <strong>100px</strong></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>div {
    padding: 25px 50px 75px;
}</code></pre>
      </td>
      <td>
        <ul style="margin: 0; padding-left: 18px;">
          <li><strong>padding superior</strong> é de <strong>25px</strong></li>
          <li><strong>padding direito e esquerdo</strong> são de <strong>50px</strong></li>
          <li><strong>padding inferior</strong> é de <strong>75px</strong></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>div {
    padding: 25px 50px;
}</code></pre>
      </td>
      <td>
        <ul style="margin: 0; padding-left: 18px;">
          <li><strong>padding superior e inferior</strong> são de <strong>25px</strong></li>
          <li><strong>padding direito e esquerdo</strong> são de <strong>50px</strong></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>div {
    padding: 25px;
}</code></pre>
      </td>
      <td>
        <p><strong>padding de todos os lados</strong> são de <strong>25px</strong></p>
      </td>
    </tr>
  </tbody>
</table>

```html
<!DOCTYPE html>
<html>
   <head>
      <style>
         div {
         border: 1px solid black;
         padding: 25px 50px 75px 100px;
         background-color: lightgreen;
         }
      </style>
   </head>
   <body>
      <h2>Propriedade Padding</h2>
      <div>O elemento div tem padding superior = 25px, padding direito = 50px, padding inferior = 75px, padding esquerdo = 100px. </div>
   </body>
</html>
```

![ Figura 12: Exemplos de utilização da propriedade padding](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/12.jpeg)

Uma alternativa para configurar o `padding` é com suas propriedades específicas para cada lado, que podem ser utilizadas em conjunto ou individualmente:

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`


---

## Propriedade `margin`
Podemos atribuir valores diferentes para cada lado da **box** do elemento HTML, para a `margin`. Veja os exemplos nas figuras a seguir:

<h3>Propriedade margin</h3>
<table border="1" cellpadding="6" cellspacing="0">
  <thead>
    <tr>
      <th>Exemplo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <pre><code>div {
    margin: 25px 50px 75px 100px;
}</code></pre>
      </td>
      <td>
        <ul style="margin: 0; padding-left: 18px;">
          <li><strong>margin superior</strong> é de <strong>25px</strong></li>
          <li><strong>margin direito</strong> é de <strong>50px</strong></li>
          <li><strong>margin inferior</strong> é de <strong>75px</strong></li>
          <li><strong>margin esquerdo</strong> é de <strong>100px</strong></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>div {
    margin: 25px 50px 75px;
}</code></pre>
      </td>
      <td>
        <ul style="margin: 0; padding-left: 18px;">
          <li><strong>margin superior</strong> é de <strong>25px</strong></li>
          <li><strong>margin direito e esquerdo</strong> são de <strong>50px</strong></li>
          <li><strong>margin inferior</strong> é de <strong>75px</strong></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>div {
    margin: 25px 50px;
}</code></pre>
      </td>
      <td>
        <ul style="margin: 0; padding-left: 18px;">
          <li><strong>margin superior e inferior</strong> são de <strong>25px</strong></li>
          <li><strong>margin direito e esquerdo</strong> são de <strong>50px</strong></li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>div {
    margin: 25px;
}</code></pre>
      </td>
      <td>
        <p><strong>margin de todos os lados</strong> são de <strong>25px</strong></p>
      </td>
    </tr>
  </tbody>
</table>

```html
border: 1px solid black;
margin: 25px 50px 75px;
background-color: lightgreen;
}
</style>
</head>
<body>
   <h2>Propriedade Margin</h2>
   <div>O elemento div tem margin superior = 25px, margin direito e esquerdo = 50px, margin inferior = 75px. </div>
   <hr>
</body>
</html>
```

![Figura 13: Exemplos de utilização da propriedade margin](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/13.jpeg)


Uma alternativa para configurar a `margin` é com suas propriedades específicas para cada lado, que podem ser utilizadas em conjunto ou individualmente:

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

---

## variáveis no CSS

Também chamadas de **Custom Properties** (propriedades personalizadas), as variáveis no CSS permitem **armazenar valores reutilizáveis**, como cores, tamanhos, fontes etc., que podem ser usados em vários lugares do seu CSS. Se você precisar mudar algo depois, **basta alterar o valor da variável em um único lugar.**

[Veja alguns exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/CSS/material_didatico/Curso_em_V%C3%ADdeo/07-vari%C3%A1veis).

### Definindo uma variável:
As variáveis são sempre definidas com **dois hífens (`--`)** e geralmente dentro do seletor `:root` para que fiquem disponíveis globalmente:

```css
:root {
  --cor-principal: #3498db;
  --tamanho-fonte: 16px;
}
```

### Usando a variável:

Use a função `var()` para aplicar o valor da variável:

```css
body {
  background-color: var(--cor-principal);
  font-size: var(--tamanho-fonte);
}
```

#### Exemplo completo

```css
:root {
  --fundo: #f0f0f0;
  --texto: #333;
  --padding: 20px;
}

.container {
  background: var(--fundo);
  color: var(--texto);
  padding: var(--padding);
}
```

Se você quiser mudar o tema, basta mudar os valores no `:root`.

#### Valor padrão (fallback)

Você pode definir um **valor padrão** se a variável não estiver definida:

```css
color: var(--cor-secundaria, blue);
```

Se `--cor-secundaria` não existir, será usado o `blue`.

#### Compatibilidade

As variáveis CSS funcionam bem na maioria dos navegadores modernos (Chrome, Firefox, Edge, Safari). Não funcionam no **Internet Explorer**.

## CSS para texto

Existem várias propriedades CSS para formatar um texto. Veja alguns exemplos na imagem a seguir:

<h3>Formatando texto</h3>
<table border="1" cellpadding="6" cellspacing="0">
  <thead>
    <tr>
      <th>Exemplo</th>
      <th>Descrição</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>
        <pre><code>h1 {
  background-color: black;
  color: white;
}</code></pre>
      </td>
      <td>
        <ul style="margin: 0; padding-left: 18px;">
          <li><strong>background-color</strong>: cor de fundo do elemento</li>
          <li><strong>color</strong>: cor do texto</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>h2 {
  text-align: left;
}</code></pre>
      </td>
      <td>
        <p><strong>text-align</strong>: alinhamento horizontal de um texto. Pode assumir os valores: <em>center</em>, <em>right</em>, <em>left</em> ou <em>justify</em>.</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>h3 {
  text-decoration: underline;
}</code></pre>
      </td>
      <td>
        <p><strong>text-decoration</strong>: adiciona uma linha de decoração ao texto. Pode assumir os valores: <em>overline</em>, <em>line-through</em> ou <em>underline</em>.</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>p {
  text-transform: uppercase;
}</code></pre>
      </td>
      <td>
        <p><strong>text-transform</strong>: especifica letras maiúsculas e minúsculas em um texto. Pode assumir os valores: <em>uppercase</em>, <em>lowercase</em> ou <em>capitalize</em>.</p>
      </td>
    </tr>
    <tr>
      <td>
        <pre><code>p {
  font-family: Arial, Helvetica, sans-serif;
}</code></pre>
      </td>
      <td>
        <p><strong>font-family</strong>: especifica a fonte de um texto. Pode assumir os valores: <em>Arial</em>, <em>Helvetica</em>, <em>“Lucida Console”</em>, etc. Deve conter várias fontes para garantir compatibilidade entre diferentes navegadores.</p>
      </td>
    </tr>
  </tbody>
</table>


```html
<!DOCTYPE html>
<html>
<head>
   <style>
      body {
         background-color: lightgrey;
         color: blue;
      }
      .p1 {
         font-family: "Lucida Console", "Courier New", monospace;
         text-transform: uppercase;
         text-decoration: overline underline;
         background-color: lightgreen;
         color: black;
      }
   </style>
</head>
<body>
   <h1>CSS Formatação de Texto</h1>
   <p class="p1">Parágrafo formatado.</p>
   <p>Parágrafo sem formatação própria.</p>
</body>
</html>
```

![Figura 14: Exemplos de utilização da formatação para texto](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/14.jpeg)

---

## CSS para tabela

Existem várias propriedades CSS para formatar uma tabela. Veja alguns exemplos na imagem a seguir:

```html
<!DOCTYPE html>
<html>
<head>
<style>
#clientes {
  font-family: Arial, Helvetica;
  border-collapse: collapse;
  width: 100%;
}
#clientes td, #clientes th {
  border: 1px solid #ddd;
  padding: 8px;
}

#clientes tr:nth-child(even) {
  background-color: #e0ebeb;
}
#clientes tr:hover {
  background-color: #ddd;
}
#clientes th {
  padding-top: 12px;
  padding-bottom: 12px;
  text-align: center;
  background-color: #3d5c5c;
  color: white;
}
</style>
</head>
<body>
<h1>Tabela Personalizada</h1>
<table id="clientes">
  <tr>
    <th>Nome</th>
    <th>País</th>
  </tr>
  <tr>
    <td>Maria Flores</td>
    <td>Brasil</td>
  </tr>
  <tr>
    <td>Caroline Summers</td>
    <td>EUA</td>
  </tr>
  <tr>
    <td>Francisco Lopez</td>
    <td>Argentina</td>
  </tr>
  <tr>
    <td>Arthur Wood</td>
    <td>Inglaterra</td>
  </tr>
</table>
</body>
</html>
```

Observe alguns pontos importantes nesta formatação:
1. O identificador id="clientes" identifica a tabela que queremos formatar.
2. Os seletores do identificador (#clientes td, #clientes tr:hover, ...) podem
receber formatações exclusivas.
3. As linhas pares (#clientes tr:nth-child(even)) também recebem formatação
exclusiva.
4. As demais tags de tabela (<tr>, <td>, etc.) não têm propriedade interna formatada.
Assim, podemos mudar totalmente a personalização da tabela, apenas editando o CSS.

![Figura 15: Exemplos de formatação de tabela](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/15.jpeg)

---

## CSS para formulário

Existem várias propriedades CSS para formatar um formulário. Veja alguns exemplos na imagem a seguir:

```html
<!DOCTYPE html>
<html>
<style>
input[type=text], select {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}
input[type=submit] {
  width: 100%;
  background-color: #3d5c5c;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
input[type=submit]:hover {
  background-color: #73978C;
}
div {
  border-radius: 5px;
  background-color: #f2f2f2;
  font-family: Arial, Helvetica;
  padding: 20px;
}
</style>
<body>
<h3>Usando CSS em Formulário</h3>
<div>
  <form action="action_page.php">
    <label for="nome">Nome</label>
    <input type="text" id="nome" name="nome" placeholder="Seu nome..">

    <label for="snome">Sobrenome</label>
    <input type="text" id="snome" name="snome" placeholder="Seu sobrenome..">

    <label for="pais">País</label>
    <select id="pais" name="pais">
      <option value="brasil">Brasil</option>
      <option value="eua">EUA</option>
    </select>
    <br><br>
    <input type="submit" value="Enviar">
  </form>
</div>
</body>
</html>
```

 Observe que o CSS foi aplicado ao seletor input e seus tipos e pseudo-classes

![Figura 16: Exemplos de formatação de formulário](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/16.jpeg)

---

### Layout flexível: basta alterar o CSS

Observe que o CSS foi aplicado ao seletor `input` e seus tipos e pseudoclasses.

Vamos verificar na prática como facilitar a alteração de layout de uma página HTML. Para isso, basta alterar apenas o CSS, portanto, o HTML deve ser utilizado apenas para estruturar os elementos no documento. Toda formatação será feita com CSS externo – também para facilitar a manutenção e reutilização de código –, de modo a estilizar os elementos HTML ou as classes (atributo `class`) definidas no HTML.

Veja o exemplo na Figura a seguir:

![Figura 17: Mesmo formulário HTML com 2 formatações diferentes de CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/17.jpeg)

![Figura 17: Mesmo formulário HTML com 2 formatações diferentes de CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/18.jpeg)

Arquivo: form_action.html:
```html
<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/styleForm1.css">
    <title>Formulário com CSS</title>
</head>
<body>
    <div class="formulario">
        <h2>Formatação de Formulário</h2>
            <div class="campo">
                <h4>Parabéns, você preencheu o formulário!</h4>
            </div>
    </div>
</body>
</html>
```

Arquivo: form.html:
```html
<!DOCTYPE html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="css/styleForm1.css">
    <title>Formulário com CSS</title>
</head>

<body>
    <div class="formulario">
        <h2>Formatação de Formulário</h2>
        <form action="form_action.html">
            <div class="campo">
                <span class="tag"><label for="nome">Nome:</label></span>
                <input type="text" id="nome" name="nome" placeholder="Seu nome.." required>
            </div>
            <div class="campo">
                <span class="tag"><label for="s_name">Sobrenome:</label></span>
                <input type="text" id="s_nome" name="s_nome" placeholder="Seu sobrenome.." required>
            </div>
            <div class="campo">
                <span class="tag"><label for="pais">País:</label></span>
                <select id="pais" name="pais" required>
                    <option value="" disabled selected>Seu país.. </option>
                    <option value="brasil">Brasil</option>
                    <option value="eua">EUA</option>
                    <option value="argentina">Argentina</option>
                    <option value="outro">Outro</option>
                </select>
            </div>
            <div class="campo">
                <span class="tag"><label for="email">E-mail:</label></span>
                <input type="e-mail" id="email" name="email" placeholder="nome@email.com" required>
            </div>
            <div class="campo">
                <span class="tag"><label for="pwd">Senha:</label></span>
                <input type="password" id="senha" name="senha" placeholder="Sua senha..." required>
            </div>
            <div class="campo">
                <input type="submit" value="Enviar">
            </div>
        </form>
    </div>

</body>

</html>
```

Arquivo css:
```css
* {
    margin: 2px;
    padding: 2px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
}
body {
    background-color: #eeeeee;
    justify-content: center;
}
h2 {
    color: #697b98;
    text-align: center;
}
input[type=submit] {
    width: 100%;
    background-color: #697b98;
    color: white;
    padding: 14px 20px;
    margin: 8px 0;
    border: none;
    border-radius: 8px;
    text-transform: uppercase;
    text-align: center;
    font-weight: 700;
    letter-spacing: 1px;
    cursor: pointer;
}
.formulario {
    position: relative;
    width: 100%;
    max-width: 500px;
    min-height: 300px;
    margin: 50px;
    background: #fff;
    box-shadow: 0 35px 55px rgba(0, 0, 0, 0.3);
}
.campo {
    margin: 10px;
}
.campo .tag {
    width: 100px;
    display: inline-block;
    background: rgb(210, 230, 244);
    margin-left: 30px;
    font-weight: 500;
}
```

Arquivo 2 css:
```css
* {
    margin: 2px;
    padding: 2px;
    font-family: 'Courier New', Courier, monospace;
    font-size: medium;
}
body {
    background-color: #efd5d5;
    justify-content: center;
}
h2 {
    color: #753636;
    font-size: xx-large;
    text-align: center;
}
input {
    padding: 6px 6px;
    background-color: #f7eded;
    border: none;
    border-bottom: solid 2px #753636;
}
select {
    padding: 6px 6px;
    background-color: #f7eded;
    border: none;
    border-bottom: solid 2px #753636;
}
input[type=submit] {
    width: 60%;
    background-color: #753636;
    color: white;
    padding: 15px 15px;
    margin: 8px 0;
    border: none;
    border-radius: 30px;
    text-align: center;
    font-weight: 500;
    letter-spacing: 10px;
    margin-left: 70px;
}
.formulario {
    position: relative;
    width: 100%;
    max-width: 500px;
    min-height: 300px;
    margin: 50px;
    background: #fff;
    box-shadow: 0 35px 55px rgba(0, 0, 0, 0.3);
}
.campo {
    margin: 10px;
}
.campo .tag {
    width: 100px;
    padding: 6px 6px;
    display: inline-block;
    background: rgb(212, 141, 141);
    color: white;
    margin-left: 70px;
    font-weight: 700;
    border: none;
    border-radius: 20px;
}
```
---

