# HTML

O HTML é a linguagem fundamental para construção de um site. Ela está presente em qualquer site ou sistema baseado na web. Vamos conhecer um pouquinho mais sobre ele? Veja a seguir os seus pontos de destaque.

A internet, criada pelo cientista britânico Tim Berners-Lee, é uma grande rede que conecta computadores do mundo inteiro. A conexão global entre computadores permitiu o compartilhamento de documentos que ganharam uma nova forma de organização, conhecida como hipertexto. A principal característica de um hipertexto é que ele tem uma leitura não linear, pois possui ligações, ou links, com outros textos, imagens, vídeos e áudios.

A conexão global possibilita o desenvolvimento de sistemas distribuídos, em uma estrutura conhecida como modelo cliente-servidor.

* Não é linguagem de programação, pois não conseguimos realizar comandos condicionais (if/else), laços de repetição (for/while) ou funções, por exemplo.
* É uma linguagem de marcação (Hypertext Markup Language = HTML) para documentos do tipo hipertexto, como são as páginas web que visualizamos em navegadores, ou browsers.
* Um hipertexto, por sua vez, é um texto de leitura não linear, pois podemos acessar diferentes partes do documento por meio de links para outros textos ou documentos, além de incluir imagens, gráficos, vídeos, animações e áudios nesse tipo de documento.
* No contexto do hipertexto, o HTML foi desenvolvido para estruturar o layout de um documento, ou seja, estruturar os elementos visuais de um documento, organizando como textos, imagens, áudios, vídeos etc. serão apresentados ao usuário de um site ou sistema web.
* Por fim, é o navegador que interpreta o HTML e renderiza seus elementos (ou exibe conteúdos visuais) na tela do usuário. Em resumo, o navegador transforma o código HTML em uma exibição visual estruturada, para interagir com o usuário do site ou aplicação web.

Neste documento falará sobre a linguagem HTML, apresentando suas marcações, ou tags, e como utilizá-las para criar diferentes tipos de estruturação de documentos web, com formatação de textos e imagens, criação de links, tabelas, listas e formulários.

**Em resumo: HTML**

* Pesquise mais sobre os temas a seguir.
* Não é linguagem de programação.
* É linguagem de marcação (tag) para estruturar hipertexto.
* É interpretada e renderizada em um navegador web.

---

## COMENTÁRIOS NOS CÓDIGO HTML, CSS E JAVASCRIPT

Comentários servem para explicar um código, sem interferir na codificação propriamente dita, pois não são interpretados como comandos ou palavras reservadas da linguagem.

* No HTML, comentários ficam delimitados pelos caracteres: `<!--` e `-->`.
* No CSS e no JavaScript, os comentários são delimitados pelos caracteres: `/*` e `*/`.

## Estrutura do documento HTML

Um documento HTML é basicamente um arquivo texto, com elementos que são marcados utilizando tags (tag = etiquetas).

**Tags**

As tags são delimitadas com os sinais `<` e `>`. Entre esses sinais, está o nome da tag, que é uma palavra reservada, para indicar um elemento HTML.

Logo, um elemento HTML é apresentado com uma tag de abertura e uma tag de fechamento, como exibido na Figura a seguir.

![1](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/1.jpeg)

> **Figura 1:** Elemento HTML.

A Figura a seguir, apresenta a estrutura fundamental de um documento HTML, que nada mais é do que um arquivo texto com extensão `.html`, em que encontramos tags de organização.

![2](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/2.jpeg)

> **Figura 2:** Estrutura fundamental de um documento HTML.

Vamos comentar as tags iniciais da Figura apresentada:

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Minha primeira página HTML</title>
  </head>
  <body>
    <h1>Primeiro cabeçalho da página</h1>
    <p>Primeiro parágrafo.</p>
    <p>Segundo parágrafo.</p>
  </body>
</html>
```

* `<!DOCTYPE html>`: o Document Type Definition (DTD, ou simplesmente Doctype) é uma tag que informa ao navegador qual é o tipo do documento em questão, e deve ser declarado antes da tag `<html>`.
* `<html>` e `</html>`: respectivamente, abertura e fechamento do documento HTML; são tags que abrangem todas as demais tags do documento.
* `<head>` e `</head>`: respectivamente, abertura e fechamento da seção de cabeçalho do documento HTML. A seção cabeçalho deve ser declarada após a tag `<html>`.
* `<meta charset="utf-8">`: a tag de metadados indica informações a respeito da página e do conteúdo nela publicado no navegador, sendo invisíveis para os usuários. Todos os metadados ficam contidos dentro da seção de cabeçalho, delimitada pelas tags `<head>` e `</head>`. A metatag `charset` é usada para indicar o conjunto de caracteres que nossa página está utilizando. No caso, indicamos uma codificação de caracteres do tipo `utf-8`: ou UCS Transformation Format 8, a mais comum da web.
* `<title>` e `</title>`: define o título da página, que é exibido na barra de título dos navegadores. Também é usada pelas ferramentas de busca da internet, para indexar e encontrar páginas web. São tags de metadados, logo ficam contidos nas tags `<head>` e `</head>`.
* `<body>` e `</body>`: respectivamente, abertura e fechamento do corpo do documento HTML; a tag `</body>` deve ser declarada imediatamente antes da tag de fechamento de documento `</html>`.
* `<p>` e `</p>`: respectivamente, abertura e fechamento de um parágrafo no documento HTML.

---

# HTML básico

Utilizando o ambiente de desenvolvimento VS Code para criar páginas HTML

Como acabamos de mencionar, um documento HTML é um arquivo-texto, que pode ser criado em qualquer editor básico de texto, como Microsoft Notepad. Contudo, para desenvolver uma aplicação web, precisamos trabalhar várias linguagens, como JavaScript, PHP e SQL, além do HTML e CSS. Com um ambiente de desenvolvimento (IDE, do inglês Integrated Development Environment), temos ajuda para escrever, atualizar e depurar códigos, dentre outras facilidades. Então, fica a dica: vamos trabalhar desde já com um ambiente de desenvolvimento para codificar nossas primeiras páginas HTML! O indicado é VS Code, da Microsoft.

---

## HTML headings

Headings são elementos HTML para cabeçalhos. Eles são definidos com as tags `<h1>` ao `<h6>`. Sendo que o `<h1>` define o cabeçalho de maior nível, ou mais importante, e o `<h6>` define o cabeçalho de menor nível, ou o menos importante.


```html
<!DOCTYPE html>
<html>
   <body>
      <h1>Este é o heading 1</h1>
      <h2>Este é o heading 2</h2>
      <h3>Este é o heading 3</h3>
      <h4>Este é o heading 4</h4>
      <h5>Este é o heading 5</h5>
      <h6>Este é o heading 6</h6>
   </body>
</html>
```

![Figura 3: HTML headings](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/3.jpeg)

> **Figura 3:** HTML headings.

---

## HTML imagens

As imagens podem melhorar o design e a aparência de uma página da web. Elas são apresentadas em um documento web com a tag `<img>` e possuem alguns atributos, como exemplificado a seguir.

![Figura 4: HTML imagem: formato](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/4.jpeg)

> **Figura 4:** HTML imagem: formato.

```html
<!DOCTYPE html>
<html>
   <body>
      <h2>HTML Image</h2>
      <img src="figuras/cavalos.jpg" alt="Passeio a cavalo." width="289" height="">
      <h2>HTML Image</h2>
      <img src="figuras/praia.jpg" alt="Férias na praia." width="289" height="">
   </body>
</html>
```

![Figura 5: HTML imagem: formato](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/5.jpeg)

> **Figura 5:** HTML imagem: formato.

---

## HTML Links

Links são elementos HTML que permitem a ligação com outros documentos web. Eles são definidos com a tag `<a>` de âncora, ou anchor, em inglês. Ao serem acionados ou clicados, os links redirecionam a página atual para outro documento referenciado na tag.

A tag `<a>` também possui alguns atributos, como exemplificado a seguir.

![Figura 6: HTML links](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/6.jpeg)

> **Figura 6:** HTML links.

<table border="1" cellspacing="0" cellpadding="8" style="border-collapse: collapse; width: 100%;">
  <thead>
    <tr>
      <th colspan="2" style="text-align: left;">Alguns atributos da <em>tag</em> <code>&lt;a&gt;</code></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>href</code></td>
      <td>O mais importante da <em>tag</em> <code>&lt;a&gt;</code>, pois identifica o destino do <em>link</em>.</td>
    </tr>
    <tr>
      <td><code>title</code></td>
      <td>Texto “dica” que aparece quando o <em>mouse</em> se move sobre o elemento.</td>
    </tr>
    <tr>
      <td rowspan="2"><code>target</code></td>
      <td><code>_self</code> : Abre o documento na mesma janela/guia em que foi clicado.</td>
    </tr>
    <tr>
      <td><code>_blank</code> : Abre o documento em uma nova janela ou guia.</td>
    </tr>
  </tbody>
</table>


```html
<!DOCTYPE html>
<html>
  <body>
    <h2>URLs absolutas</h2>
    <p><a href="https://google.com/" target="_blank" title="Google">Site Google</a></p>
    <p><a href="https://pucpr.br/" target="_blank" title="PUCPR">Site <u>PUCPR</u></a></p>
    <h2>URL relativas</h2>
    <p><a href="images.html" title="Teste de imagens">Images</a></p>
    <p><a href="headings.html" title="Teste de cabeçalhos">Headings</a></p>
    <h2>Link para e-mail</h2>
    <p><a href="mailto:nome.sobrenome@site_exemplo.com">Envie um e-mail</a></p>
  </body>
</html>
```

![Figura 7: HTML links](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/7.jpeg)

> **Figura 7:** HTML links.

---

## HTML lists

Podemos agrupar um conjunto de itens relacionados em uma estrutura de lista, que possui três tipos possíveis:

* **Unordered HTML list**, ou lista não ordenada, definida com as tags `<ul>` e `</ul>`, sendo cada item identificado com as tags `<li>` e `</li>`.
* **Ordered HTML list**, ou lista ordenada, definida com as tags `<ol>` e `</ol>`, sendo cada item identificado com as tags `<li>` e `</li>`.
* **HTML description lists**, ou lista de descrição, definida com as tags `<dl>` e `</dl>`, sendo cada item identificado com as tags `<dt>` e `</dt>`, com sua descrição delimitada pelas tags `<dd>` e `</dd>`.

```html
<!DOCTYPE html>
<html>
<body>
    <h2>Lista Não Ordenadas</h2>
    <ul>
        <li>Café</li>
        <li>Chá</li>
        <li>Leite</li>
    </ul>
    <h2>Lista Ordenadas</h2>
    <ol>
        <li>Café</li>
        <li>Chá</li>
        <li>Leite</li>
    </ol>
    <h2>Lista de Definição</h2>
    <dl>
        <dt>Café</dt>
        <dd>- Bebida quente, produzida a partir dos grãos torrados do café.</dd>
        <dt>Chá</dt>
        <dd>- Bebida quente, preparada pela infusão de folhas.</dd>
        <dt>Leite</dt>
        <dd>- Bebida gelada branca.</dd>
    </dl>
</body>
</html>
```

![Figura 8: HTML listas](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/8.jpeg)

> **Figura 8:** HTML listas. 

---

## HTML tables

Podemos organizar um conjunto de dados em uma estrutura de tabela, com linhas e colunas. Para tanto, usamos as seguintes tags:

* `<table>` e `</table>`: Tags de início e fim de tabela.
* `<tr>` e `</tr>`: Tags de início e fim de linha.
* `<th>` e `</th>`: Tags de início e fim de coluna do tipo cabeçalho.
* `<td>` e `</td>`: Tags de início e fim de coluna simples.


A formatação de tabelas HTML é feita com CSS. A formatação visual de tabelas no HTML (cores, bordas, textos etc.) é feita com estilos CSS, de Cascading Style Sheets, ou folha de estilos em cascata.

Para formatar as bordas das nossas tabelas-exemplo, usamos um pequeno trecho de CSS para desenhar bordas na cor preta e em linha cheia de 1 pixel de largura:

```html
<head>
  <!-- Comentário HTML: Abre seção <head> -->
  <style>
    /* Comentário CSS: tags "table", "th" e "td" */
    table, th, td {
      border: 1px solid black; /* borda de 1 pixel, em linha cheia e na cor preta */
    }
  </style>
  <!-- Fecha a seção </style> -->
</head>
```

### Exemplo de tabelas

```html
<!DOCTYPE html>
<html>
<head>
  <!-- Comentário HTML: Abre seção <head> -->
  <style>
    /* Comentário CSS: Formatação visual de uma tabela */
    table, th, td {
      border: 1px solid black; /* borda de 1 pixel, em linha cheia e na cor preta */
    }
  </style>
  <!-- Fecha a seção </style>, dentro da seção de cabeçalho do HTML -->
</head>
<body>
  <h2>Tabela Exemplo 1</h2>
  <table width="60%">
    <tr>
      <th>Itens/Mês</th>
      <th>Janeiro</th>
      <th>Fevereiro</th>
    </tr>
    <tr>
      <th>Usuarios</th>
      <td>80</td>
      <td>93</td>
    </tr>
    <tr>
      <th>Linhas</th>
      <td>3</td>
      <td>9</td>
    </tr>
  </table>
  <h2>Tabela Exemplo 2: atributos colspan e rowspan</h2>
  <table>
    <tr>
      <th rowspan="3">Meses</th> <!-- Faz a união de 3 LINHAS (row) -->
      <th>Mês</th>
      <th>Economia</th>
    </tr>
    <tr>
      <td>Janeiro</td>
      <td>R$ 100,00</td>
    </tr>
    <tr>
      <td>Fevereiro</td>
      <td>R$ 80,00</td>
    </tr>
    <tr>
      <td>Total</td>
      <td colspan="2">R$ 180,00</td> <!-- Faz a união de 2 COLUNAS (col) -->
    </tr>
  </table>
</body>
</html>
```

![Figura 9: HTML tables](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/9.jpeg)

> **Figura 9:** HTML tables.

**Alguns atributos para as _tags_: `<td>` e `<td>`**

| Atributo        | Descrição                                                         |
|-----------------|-------------------------------------------------------------------|
| `colspan="valor"` | Define quantas células uma **coluna** poderá ter.                |
| `rowspan="valor"` | Define quantas células uma **linha** poderá ter.                 |

---

## HTML formating

O HTML define alguns elementos de formatação para exibir tipos especiais de textos:

* `<b>`: Texto em **negrito**.
* `<strong>`: Texto <em>importante</em>.
* `<i>`: Texto em *itálico*.
* `<em>`: Texto em *destaque*.
* `<small>`: Texto <small>menor</small>.
* `<sub>`: Texto <sub>subscrito</sub>.
* `<sup>`: Texto <sup>sobrescrito</sup>.

### PRÁTICA: formating

1. Copie o texto a seguir para o seu arquivo `formating.html`. Após, abra o arquivo no navegador.

```html
<!DOCTYPE html>
<html>
<body>
    <h2>Formatação básica de texto</h2>
    <p>Este é um texto normal.</p>
    <p><b>Este é um texto negrito.</b></p>
    <p><strong>Este é um texto importante!</strong></p>
    <p><i>Este é um texto em itálico.</i></p>
    <p><em>Este é um texto enfatizado.</em></p>
    <p><small>Este é um texto em uma fonte menor.</small></p>
    <p>Este é um texto <sub>subscrito</sub>.</p>
    <p>Este é um texto <sup>sobrescrito</sup>.</p>
</body>
</html>
```

---

## HTML forms

O elemento HTML `<form>` é utilizado para criar um formulário HTML para entrada do usuário. Ele é um contêiner para diferentes tipos de elementos de entrada, como: campos de texto, caixas de seleção, botões de opção, botões de envio etc.

### PRÁTICA: forms

1. Copie o texto a seguir para o seu arquivo `forms.html`. Após, abra o arquivo no navegador.

```html
<!DOCTYPE html>
<html>
<body>
    <h2>Campos de entrada do tipo TEXT</h2>
    <form>
        <label for="pnome">Primeiro nome:</label><br>
        <input type="text" id="pnome" name="pnome" value="João"><br>
        <label for="unome">Último nome:</label><br>
        <input type="text" id="lnome" name="unome" value="Silva">
    </form><br>
    <b>Observe 1</b>: o formulário em si não é visível.<br>
    <b>Observe 2</b>: a largura padrão do campo de texto = **20** caracteres.
    <br><hr>
    <h2>Campos de entrada do tipo RADIO BUTTON</h2>
    <p>Escolha sua linguagem web favorita:</p>
    <form>
        <input type="radio" id="html" name="fav_linguagem" value="HTML">
        <label for="html">HTML</label><br>
        <input type="radio" id="css" name="fav_linguagem" value="CSS">
        <label for="css">CSS</label><br>
        <input type="radio" id="javascript" name="fav_linguagem" value="JavaScript">
        <label for="javascript">JavaScript</label>
    </form>
    <br><hr>
    <h2>Campos de entrada do tipo CHECKBOX</h2>
    <form>
        <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
        <label for="vehicle1"> I have a bike</label><br>
        <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
        <label for="vehicle2"> I have a car</label><br>
        <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
        <label for="vehicle3"> I have a boat</label>
    </form>
    <br><hr>
    <h2>Campos de entrada do tipo SUBMIT BUTTON</h2>
    <form action="https://www.w3schools.com/action_page.php" target="_self">
        <label for="pnome">Primeiro nome:</label><br>
        <input type="text" id="pnome" name="pnome" value="Maria"><br>
        <label for="lnome">Último nome:</label><br>
        <input type="text" id="lnome" name="lnome" value="Flores"><br><br>
        <input type="submit" value="Submit">
    </form>
    <p>Ao clicar no botão "Submit", os dados do formulário serão enviados.</p>
</body>
</html>
```

---

### Alguns atributos da tag `<form>`

* **action**: Define a ação a ser executada quando o formulário for enviado.
* **target**: Identifica onde abrir o documento vinculado. Pode ter os valores:

  * `_self`: Abre o documento na mesma janela/guia em que foi clicado.
  * `_blank`: Abre o documento em uma nova janela ou guia.
* **method**: Especifica qual método do protocolo HTTP será usado ao enviar os dados do formulário:

  * `GET`: Os dados do formulário são enviados como variáveis de URL.
  * `POST`: Os dados do formulário são enviados como transação de postagem HTTP.
* **autocomplete**: Indica se formulário deve ter o preenchimento automático:

  * `on`: Ativa o preenchimento automático.
  * `off`: Desativa o preenchimento automático.

#### Alguns elementos subordinados à tag `<form>`

* `<input>`: Elemento pode ser exibido de várias maneiras, dependendo do atributo `type`.
* `<input type="checkbox">`: Define um botão de escolha, do tipo caixa, para seleção de vários valores.
* `<input type="color">`: Define um campo de entrada para escolha de cor.
* `<input type="date">`: Define um campo de entrada do tipo data.
* `<input type="datetime-local">`: Define um campo de entrada do tipo data e hora.
* `<input type="email">`: Define um campo de entrada do tipo endereço de e-mail.
* `<input type="file">`: Define um campo de seleção de arquivo e um botão "Procurar" para uploads de arquivos.
* `<input type="hidden">`: Define um campo de entrada não visível ao usuário.
* `<input type="image">`: Define uma imagem como botão de envio.
* `<input type="month">`: Permite que o usuário selecione um mês e ano.
* `<input type="number">`: Define um campo de entrada numérico.
* `<input type="password">`: Define um campo de entrada de senha.
* `<input type="radio">`: Define um botão de escolha, do tipo rádio, para seleção de único valor.
* `<input type="range">`: Define um campo de entrada do tipo controle deslizante.
* `<input type="reset">`: Define um botão para limpar todos os campos do formulário.
* `<input type="submit">`: Define um botão para enviar dados de formulário.
* `<input type="text">`: Define um campo de entrada de texto de linha única.
* `<input type="time">`: Permite que o usuário selecione um horário.
* `<input type="url">`: Campo de entrada que deve conter um endereço de URL.

A tabela a seguir traz um resumo de atributos da tag `<form>` e uma relação de elementos HTML subordinados à tag `<form>`, que são campos de entrada.

> **Figura 13:** HTML forms. Fonte: Autora (2023).

---

# Conclusão

Olá!

Acabamos de ter o primeiro contato com o desenvolvimento web. Vimos que teremos duas frentes de trabalho:

1. Desenvolvimento web front-end, em que trabalharemos com HTML, CSS e JavaScript.
2. Desenvolvimento web back-end, em que, dentre as várias tecnologias alternativas, trabalharemos com PHP e SQL.

Assim, nesta unidade, começamos com HTML, que não é linguagem de programação, mas, sim, linguagem de marcação.

Na próxima unidade, continuaremos no front-end, mas trabalhando para estilizar HTML com CSS.

Realize as práticas indicadas aqui para HTML, pois assim você aproveitará melhor nossa próxima unidade!

Até!

# Referências Bibliográficas

* ALVES, W. P. *Desenvolvimento e design de sites.* São Paulo: Erica, 2014.
* MILETTO, E. M.; BERTAGNOLLI, S. C. *Desenvolvimento de software II: Introdução ao desenvolvimento web com HTML, CSS, JavaScript e PHP.* Porto Alegre: Bookman, 2014.
* TERUEL, E. C. *HTML 5: Guia prático.* 2. ed. Porto Alegre: Bookman, 2014.

© PUCPR - Todos os direitos reservados.
