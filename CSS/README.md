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
    <p style="color:deepskyblue; font-family:Verdana; text-align:center">Texto 1.</p>
    <p style="color:brown; font-family:'Courier New'; text-align:right">Texto 2.</p>
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
---

## Seletores CSS

Os **seletores CSS** são usados para "encontrar" (ou selecionar) os elementos HTML que desejamos estilizar.

Podemos organizar os seletores CSS nas seguintes categorias:

1. **Seletor de elemento.**
2. **Seletor de id.**
3. **Seletor de classe.**
4. **Seletores de combinação** (agrupa elementos).
5. **Seletores de pseudoclasse** (seleciona elementos com base em um determinado estado).

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

---

### Seletor de id CSS

O seletor usa o atributo `id` (identificador) de um elemento HTML para selecionar um elemento específico.

O `id` de um elemento é único dentro de uma página HTML, logo o seletor de id é aplicado em um único elemento da página.

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
   <p class="center">Este parágrafo será vermelho e centralizado</p>
   <p class="center large">Este parágrafo será vermelho e grande</p>
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
      a:link {    /* pseudo-classe para link NÃO VISITADO */
         color: red;
      }
      a:visited { /* pseudo-classe para link VISITADO */
         color: green;
      }
      a:hover {   /* pseudo-classe para MOUSE SOBRE o link */
         color: hotpink;
      }
      a:active {  /* pseudo-classe para link SELECIONADO */
         color: blue;
      }
   </style>
</head>
<body>
   <h2>Estilo para link, dependendo do seu estado</h2>
   <p><b><a href="default.asp" target="_blank">Este é um link</a></b></p>
   <dl>
      <dt><p><b>Importante 1:</b></p></dt>
      <dd><b>a:hover</b> DEVE vir depois de <b>a:link</b></dd>
      <dt><p><b>Importante 2:</b></p></dt>
      <dd><b>a:active</b> DEVE vir depois de <b>a:hover</b></dd>
   </dl>
</body>
</html>
```

---

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

<div align="center">
![Figura 9: Seletor de agrupamento CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/9.jpeg)
</div>

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
- `background-color`: cor de fundo do elemento; é definida pelo nome em inglês da cor, ou no padrão hexadecimal RGB (Red-Green-Blue), como por exemplo `#3040AF`.

Veja como é compreendida a box de um elemento HTML, exibida na Figura a seguir:

![Figura 10: Box do elemento HTML, formatada pelo CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/10.jpeg)

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


<div align="center">
![Propriedade Padding](sandbox:/mnt/data/image_page18_3.jpeg)
</div>

Uma alternativa para configurar o `padding` é com suas propriedades específicas para cada lado, que podem ser utilizadas em conjunto ou individualmente:

- `padding-top`
- `padding-right`
- `padding-bottom`
- `padding-left`

---

<div align="center">
![Figura 12: Exemplos de utilização da propriedade padding](sandbox:/mnt/data/image_page19_1.jpeg)
</div>

---

## Propriedade `margin`

Podemos atribuir valores diferentes para cada lado da **box** do elemento HTML, para a `margin`. Veja os exemplos nas figuras a seguir:

**Exemplo 1:**

```css
div {
    margin: 25px 50px 75px 100px;
}
```
- `margin` superior é de 25px
- `margin` direito é de 50px
- `margin` inferior é de 75px
- `margin` esquerdo é de 100px

**Exemplo 2:**

```css
div {
    margin: 25px 50px 75px;
}
```
- `margin` superior é de 25px
- `margin` direito e esquerdo são de 50px
- `margin` inferior é de 75px

**Exemplo 3:**

```css
div {
    margin: 25px 50px;
}
```
- `margin` superior e inferior são de 25px
- `margin` direito e esquerdo são de 50px

**Exemplo 4:**

```css
div {
    margin: 25px;
}
```
- `margin` de todos os lados são de 25px

<div align="center">
![Propriedade Margin](sandbox:/mnt/data/image_page20_1.jpeg)
</div>

Uma alternativa para configurar a `margin` é com suas propriedades específicas para cada lado, que podem ser utilizadas em conjunto ou individualmente:

- `margin-top`
- `margin-right`
- `margin-bottom`
- `margin-left`

---

<div align="center">
![Figura 13: Exemplos de utilização da propriedade margin](sandbox:/mnt/data/image_page23_1.jpeg)
</div>

---

## CSS para texto

Existem várias propriedades CSS para formatar um texto. Veja alguns exemplos na imagem a seguir:

| Exemplo                                                   | Descrição                                                                                                                                              |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| ```css                                                    | `background-color`: cor de fundo do elemento<br>`color`: cor do texto                                                                                  |
| h1 {<br>  background-color: black;<br>  color: white;<br>} |                                                                                                                                                        |
|                                                           |                                                                                                                                                        |
| ```css                                                    | `text-align`: alinhamento horizontal de um texto.<br>Pode assumir os valores: _center_, _right_, _left_ ou _justify_.                                                                        |
| h2 {<br>  text-align: left;<br>}                           |                                                                                                                                                        |
|                                                           |                                                                                                                                                        |
| ```css                                                    | `text-decoration`: adiciona uma linha de decoração ao texto. Pode assumir os valores: _overline_, _line-through_ ou _underline_.                                                              |
| h3 {<br>  text-decoration: underline;<br>}                |                                                                                                                                                        |
|                                                           |                                                                                                                                                        |
| ```css                                                    | `text-transform`: especifica letras maiúsculas e minúsculas em um texto. Pode assumir os valores: _uppercase_, _lowercase_ ou _capitalize_.                                                      |
| p {<br>  text-transform: uppercase;<br>}                   |                                                                                                                                                        |
|                                                           |                                                                                                                                                        |
| ```css                                                    | `font-family`: especificar a fonte de um texto. Pode assumir os valores: _Arial_, _Helvetica_, _“Lucida Console”_, etc. Deve conter várias fontes para garantir compatibilidade entre diferentes navegadores. |
| p {<br>  font-family: Arial, Helvetica, sans-serif;<br>}  |                                                                                                                                                        |

<div align="center">
![Formatando texto](sandbox:/mnt/data/image_page25_1.jpeg)
</div>

#### PRÁTICA: Formatando texto no navegador

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

---

## CSS para tabela

Existem várias propriedades CSS para formatar uma tabela. Veja alguns exemplos na imagem a seguir:

<div align="center">
![Figura 14: Exemplos de utilização da formatação para texto](sandbox:/mnt/data/image_page27_1.jpeg)
</div>

> **Fonte: A autora (2023).**  
> **#ParaTodosVerem**

#### PRÁTICA: Formatando tabela

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

<div align="center">
![Figura 15: Exemplos de formatação de tabela](sandbox:/mnt/data/image_page29_1.jpeg)
</div>

---

## CSS para formulário

Existem várias propriedades CSS para formatar um formulário. Veja alguns exemplos na imagem a seguir:

<div align="center">
![Figura 16: Exemplos de formatação de formulário](sandbox:/mnt/data/image_page31_1.jpeg)
</div>

#### PRÁTICA: Formatando formulário

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
      <option value="argentina">Argentina</option>
      <option value="outro">Outro</option>
    </select>
    <br><br>
    <input type="submit" value="Enviar">
  </form>
</div>
</body>
</html>
```

---

### Layout flexível: basta alterar o CSS

Observe que o CSS foi aplicado ao seletor `input` e seus tipos e pseudoclasses.

Vamos verificar na prática como facilitar a alteração de layout de uma página HTML. Para isso, basta alterar apenas o CSS, portanto, o HTML deve ser utilizado apenas para estruturar os elementos no documento. Toda formatação será feita com CSS externo – também para facilitar a manutenção e reutilização de código –, de modo a estilizar os elementos HTML ou as classes (atributo `class`) definidas no HTML.

Veja o exemplo na Figura a seguir:

<div align="center">
![Figura 17: Mesmo formulário HTML com 2 formatações diferentes de CSS](sandbox:/mnt/data/image_page41_1.jpeg)
</div>

> **Fonte: A autora (2023).**  
> **#ParaTodosVerem**

---

#### Arquivos de exemplo para Formulário

##### Arquivo: form_action.html

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

##### Arquivo: form.html

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
        <form action="form_action.html">
            <div class="campo">
                <span class="tag"><label for="nome">Nome:</label></span>
                <input type="text" id="nome" name="nome" placeholder="Seu nome..">
            </div>
            <div class="campo">
                <span class="tag"><label for="s_name">Sobrenome:</label></span>
                <input type="text" id="s_nome" name="s_nome" placeholder="Seu sobrenome..">
            </div>
            <div class="campo">
                <span class="tag"><label for="pais">País:</label></span>
                <select id="pais" name="pais" required>
                    <option value="" disabled selected>Seu país..</option>
                    <option value="brasil">Brasil</option>
                    <option value="eua">EUA</option>
                    <option value="argentina">Argentina</option>
                    <option value="outro">Outro</option>
                </select>
            </div>
            <div class="campo">
                <span class="tag"><label for="email">E-mail:</label></span>
                <input type="email" id="email" name="email" placeholder="Seu e-mail..">
            </div>
            <div class="campo">
                <span class="tag"><label for="pwd">Senha:</label></span>
                <input type="password" id="senha" name="senha" placeholder="Digite sua senha..">
            </div>
            <div class="campo">
                <input type="submit" value="Enviar">
            </div>
        </form>
    </div>
</body>
</html>
```

##### Arquivo: css/styleForm1.css

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

##### Arquivo: css/styleForm2.css

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

## ATIVIDADE FORMATIVA

Execute o exercício proposto na videoaula-tutorial a seguir, para criar um curriculum vitae em HTML, estilizado com CSS. Nesta prática, além de exercitar diferentes maneiras de formatar elementos HTML, você poderá verificar como um ambiente de desenvolvimento adequado, como o VS Code ([https://code.visualstudio.com/download](https://code.visualstudio.com/download)), auxilia bastante na escrita dos códigos. Além disso, um navegador com janela de inspeção vai permitir até testes de layout para visualizar qual é o mais interessante para a sua página.

<div align="center">
![Figura: Atividade Formativa](sandbox:/mnt/data/image_page42_1.jpeg)
</div>

> **Fonte: A autora (2023).**  
> **#ParaTodosVerem**

---

## SAIBA MAIS

### Conclusão

Criando páginas HTML com CSS para definição de estilo.

Vamos criar um curriculum vitae com um layout bem diferenciado, para treinar diferentes tipos de formatação possíveis. Observe que o HTML não tem formatação, que é feita totalmente em um arquivo `.css` em separado. Vamos também preparar nossa página para outros dispositivos, utilizando a responsividade do CSS, que é a capacidade de adaptar o tamanho das páginas web de acordo com o tamanho das telas em que elas são exibidas. Mãos à obra!

- **Criando páginas HTML com CSS**
- [Tutorial CSS (W3Schools)](https://www.w3schools.com/css)
- [CSS Formulários (W3Schools)](https://www.w3schools.com/css/css_form.asp)
- [CSS Fontes (W3Schools)](https://www.w3schools.com/css/css_font.asp)
- [CSS Cores (W3Schools)](https://www.w3schools.com/css/css_colors.asp)
- [CSS Avançado (W3Schools)](https://www.w3schools.com/css/css3_borders.asp)
- [CSS Responsivo (W3Schools)](https://www.w3schools.com/css/css_rwd_intro.asp)
- [Vídeo sobre Responsividade](https://www.youtube.com/watch?v=9TWmkfQeCX4)

Até a próxima unidade, em que continuaremos no front-end, contudo com programação em JavaScript. Realize as práticas indicadas aqui para o HTML juntamente com CSS, pois assim você aproveitará melhor nossa próxima unidade!

---

## Referências Bibliográficas

- **ALVES, W. P.** _Desenvolvimento e design de sites_. São Paulo: Érica, 2014.
- **MILETTO, E. M.; BERTAGNOLLI, S. C.** _Desenvolvimento de software II: Introdução ao desenvolvimento web com HTML, CSS, JavaScript e PHP_. Porto Alegre: Bookman, 2014.
- **TERUEL, E. C.** _HTML 5: Guia prático_. 2. ed. Porto Alegre: Bookman, 2014.

© PUCPR – Todos os direitos reservados.
