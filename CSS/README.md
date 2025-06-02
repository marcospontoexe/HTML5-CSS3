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

![Figura: Sintaxe da Regra CSS](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/CSS/imgens/1.jpeg)

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

#### PRÁTICA: visualizando o CSS inline em um documento web

Vamos criar um documento HTML formatado com folha de estilo CSS, para visualização em um navegador. Também vamos utilizar a ferramenta de inspeção de página do navegador Google Chrome.

Siga os passos indicados a seguir para ver o CSS inline funcionando:

1. Defina uma pasta de trabalho, como por exemplo `C:/Teste-CSS`.
2. Dentro da pasta, crie um documento `estiloInline.html`, com o código exemplificado a seguir:

<details>
<summary><strong>Arquivo C:/Teste-CSS/estiloInline.html</strong></summary>

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
</details>

> **Dica:** Você pode utilizar um ambiente integrado de desenvolvimento, ou IDE – do inglês *Integrated Development Environment* –, como o Visual Studio Code da Microsoft ([https://code.visualstudio.com/download](https://code.visualstudio.com/download)).

3. Abra o seu `estiloInline.html` no navegador (browser): copie o caminho completo do arquivo e cole na barra de endereços.

---

#### 2. Sintaxe: Regra CSS interna

O código CSS é inserido em um elemento `<style>`, que geralmente fica dentro da seção `<head>`:

<div align="center">
![Figura 2: HTML com CSS inline](sandbox:/mnt/data/image_page5_1.jpeg)
</div>

> **Fonte: A autora (2023).**  
> **#ParaTodosVerem**

Também evite usar esta prática! Ela deixa no mesmo arquivo o código HTML e o código CSS, o que não permite o reuso do CSS, podendo gerar duplicidade de código e tornar a manutenção e evolução do código mais complexa.

#### PRÁTICA: visualizando o CSS interno em um documento web

Vamos criar um documento HTML formatado com folha de estilo CSS, para visualização em um navegador.

Siga os passos indicados a seguir para ver o CSS interno funcionando:

1. Na pasta de trabalho (por exemplo, `C:/Teste-CSS`).
2. Dentro da pasta, crie um documento `estiloInterno.html`, com o código exemplificado a seguir:

<details>
<summary><strong>Arquivo C:/Teste-CSS/estiloInterno.html</strong></summary>

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
</details>

<div align="center">#ParaTodosVerem</div>

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

#### PRÁTICA: visualizando o CSS externo em um documento web

Vamos criar um documento HTML formatado com folha de estilo CSS, para visualização em um navegador.

Siga os passos indicados a seguir para ver o CSS externo funcionando:

1. Na pasta de trabalho, por exemplo `C:/Teste-CSS`.
2. Dentro da pasta, crie um documento `estiloExterno.html`, com o código exemplificado a seguir.
3. Crie uma subpasta `css`, por exemplo `C:/Teste-CSS/css`.

<div align="center">
![Figura 3: HTML com CSS interno](sandbox:/mnt/data/image_page7_1.jpeg)
</div>

> **Fonte: A autora (2023).**

#### Arquivo C:/Teste-CSS/estiloExterno.html

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

#### Arquivo C:/Teste-CSS/css/style.css

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

<div align="center">
![Figura 4: HTML com CSS externo](sandbox:/mnt/data/image_page10_1.jpeg)
</div>

> **Fonte: A autora (2023).**  
> **#ParaTodosVerem**

Seleciona qual elemento HTML receberá o estilo, baseado no seu nome HTML, ou tag.

#### Exemplos de seletores:

- **`p`** serve para formatar um elemento HTML `<p>`.
- **`*`** serve para formatar elementos HTML de qualquer tipo.

#### PRÁTICA: Seletor de elemento CSS no navegador

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

---

### Seletor de id CSS

O seletor usa o atributo `id` (identificador) de um elemento HTML para selecionar um elemento específico.

O `id` de um elemento é único dentro de uma página HTML, logo o seletor de id é aplicado em um único elemento da página.

**USO CORRETO:** escreva um caractere hash (`#`), seguido do `id` do elemento.

#### PRÁTICA: Seletor de id CSS no navegador

<div align="center">
![Figura 5: Seletor de elemento CSS](sandbox:/mnt/data/image_page12_1.jpeg)
</div>

> **Fonte: A autora (2023).**  
> **#ParaTodosVerem**

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

---

### Seletor de classe CSS

O seletor de classe seleciona elementos HTML com um atributo de `class` específico. Para selecionar elementos de uma classe, escrevemos um ponto (`.`), seguido do nome da classe.

#### PRÁTICA: Seletor de classe CSS no navegador

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

<div align="center">
![Figura 7: Seletor de classe CSS](sandbox:/mnt/data/image_page13_1.jpeg)
</div>

> **Fonte: A autora (2023).**  
> **#ParaTodosVerem**

Elementos HTML também podem se referir a mais de uma classe.