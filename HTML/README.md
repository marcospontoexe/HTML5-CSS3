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

[Veja mais exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/1-sintaxe).
[Como usar emoji](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/3-emoji).
[Como usar iFrame](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/10-Iframe).

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

[Veja mais exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/4-T%C3%ADtulos).

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
      <img src="figuras/cavalos.jpg" alt="Passeio a cavalo." width="289" height="192">
      <h2>HTML Image</h2>
      <img src="figuras/praia.jpg" alt="Férias na praia." width="289" height="192">
   </body>
</html>
```

![Figura 5: HTML imagem: formato](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/5.jpeg)

> **Figura 5:** HTML imagem: formato.

[Veja mais exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/2-imagens).
[Veja como inserir **imagens dinâmicas**, **audio** e **vídeo**](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/8-m%C3%ADdias).

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
    <p></p>
    <a href="https://pucpr.br/"   target="_blank" title="PUCPR">Site PUCPR</a></p>
    <h2>URL relativas</h2>
    <p></p>
    <a href="images.html" title="Teste de imagens">Images</a></p>
    <p></p>
    <a href="headings.html" title="Teste de cabeçalhos">Headings</a></p>
    <h2>Link para e-mail</h2>
    <p></p>
    <a href="mailto:nome.sobrenome@site_examplo.com">Envie um e-mail</a></p>
  </body>
</html>
```

![Figura 7: HTML links](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/7.jpeg)

> **Figura 7:** HTML links.

[Veja mais exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/7-Links).

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

[Veja mais exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/6-listas).

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
<head>    <!-- Comentário HTML: Abre seção <head> --> 
  <style> /*   Comentário CSS: tags "table", "th" e "td" terão como formatação:  */ 
    table, th, td {                        
      border: 1px solid black; /* borda de 1 pixel, em linha cheia e na cor preta*/
    }
  </style> <!-- Fecha a seção </style> -->
</head> <!-- Fecha a seção </head> -->
```

### Exemplo de tabelas

```html
<!DOCTYPE html>
<html>
<head>    <!-- Comentário HTML: SPOILER de CSS: formatando o visual de uma tabela --> 
  <style> /*   Comentário CSS: Os elementos HTML: */ 
    table,                     /* "table" (tag para iniciar tabela),   */
    th,                        /* "th"    (tag para coluna cabeçalho) e */ 
    td {                       /* "td     (tag para coluna), terão como formatação: */
      border: 1px solid black; /* borda de 1 pixel, em linha cheia e na cor preta*/
    }
  </style> <!-- Fecha a seção </style>, dentro da seção de cabeçalho do HTM -->
</head>
</table>
<h2>Tabela Exemplo 1</h2>
<table width="60%"> <!-- Atributo width (largura) = % da tela do navegador. -->
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
    <th rowspan="3">Meses</th> <!-- Faz a união de 3 LINHAS (row)  --> 
    <th>Mês</th>
    <th>Economia</th>
  </tr>
  <tr>
    <td>Janeiro</td>
    <td>R$ 100,00</td>
  </tr>
  <tr>
    <td>Fevereiro</td>
    <td>R$ 80,0</td>
  </tr>
  <tr>
    <td>Total</td>
    <td colspan="2"> R$ 180,00</td> <!-- Faz a união de 2 COLUNAS (col) -->
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

[Veja mais exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/9-tabela).

---

## HTML formating (semantica)

O HTML define alguns elementos de formatação para exibir tipos especiais de textos:

* `<b>`: Texto em **negrito**.
* `<strong>`: Texto <em>importante</em>.
* `<i>`: Texto em *itálico*.
* `<em>`: Texto em *destaque*.
* `<small>`: Texto <small>menor</small>.
* `<sub>`: Texto <sub>subscrito</sub>.
* `<sup>`: Texto <sup>sobrescrito</sup>.
* `<address>`: Usando para endereço, no celular abre o maps.

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

![Figura 10: HTML tables](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/10.jpeg)

> **Figura 10:** HTML tables.

[Veja mais exemplos](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/5-sem%C3%A2ntica%20(formata%C3%A7%C3%A3o)).

---

## HTML forms

O elemento HTML `<form>` é utilizado para criar um formulário HTML para entrada do usuário. Ele é um contêiner para diferentes tipos de elementos de entrada, como: campos de texto, caixas de seleção, botões de opção, botões de envio etc.

```html
<!DOCTYPE html>
<html>
<body>
    <h2>Campos de entrada do tipo TEXT</h2>
    <form>
        <label for="pname">Primeiro nome:</label><br>
        <input type="text" id="pnome" name="pnome" value="João"><br>
        <label for="uname">Último nome:</label><br>
        <input type="text" id="lnome" name="unome" value="Silva">
    </form> <br>
    <b>Observe 1</b>: o formulário em si não é visível. <br>
    <b>Observe 2</b>: a largura padrão do campo de texto = <b>20</b> caracteres. <br>
    <br> <hr>
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
    <br> <hr>
    <h2>Campos de entrada do tipo CHECKBOX</h2>
    <form>
        <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike">
        <label for="vehicle1"> I have a bike</label><br>
        <input type="checkbox" id="vehicle2" name="vehicle2" value="Car">
        <label for="vehicle2"> I have a car</label><br>
        <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat">
        <label for="vehicle3"> I have a boat</label>
    </form>
    <br> <hr>
    <h2>Campos de entrada do tipo SUBMIT BUTTON</h2>
    <form action="https://www.w3schools.com/action_page.php" target="_self" >
        <label for="pname">Primeiro nome:</label><br>
        <input type="text" id="pnome" name="pnome" value="Maria"><br>
        <label for="uname">Último nome:</label><br>
        <input type="text" id="lnome" name="unome" value="Flores"><br><br>
        <input type="submit" value="Submit">
    </form>
    <p>Ao clicar no botão "Submit", os dados do formulário serão enviados para uma página do W3Schools: "action_page.php".</p>
</body>
</html>
```

![Figura 11: HTML tables](https://github.com/marcospontoexe/HTML5-CSS3/blob/main/HTML/imagens/11.jpeg)

> **Figura 11:** HTML tables.

<h3>Alguns atributos da tag &lt;form&gt;</h3>
<table>
  <tr><th>Atributo</th><th>Descrição</th></tr>
  <tr><td><code>action</code></td><td>Define a ação a ser executada quando o formulário for enviado</td></tr>
  <tr>
    <td><code>target</code></td>
    <td>
      Identifica onde abrir o documento vinculado. Pode ter os valores:<br>
      <strong>_self</strong> : Abre o documento na mesma janela/guia em que foi clicado.<br>
      <strong>_blank</strong> : Abre o documento em uma nova janela ou guia.
    </td>
  </tr>
  <tr>
    <td><code>method</code></td>
    <td>
      Especifica qual método do protocolo HTTP será usado ao enviar os dados do formulário:<br>
      <strong>GET</strong> Os dados do formulário são enviados como variáveis de URL.<br>
      <strong>POST</strong> Os dados do formulário são enviados como transação de postagem HTTP.
    </td>
  </tr>
  <tr>
    <td><code>autocomplete</code></td>
    <td>
      Indica se formulário deve ter o preenchimento automático.<br>
      <strong>on</strong> : Ativa o preenchimento automático.<br>
      <strong>off</strong> : Desativa o preenchimento automático.
    </td>
  </tr>
</table>

<h3>Alguns elementos subordinados à tag &lt;form&gt;</h3>
<table>
  <tr>
    <th>&lt;input&gt; - Elemento pode ser exibido de várias maneiras, dependendo do atributo type.</th>
    <th>Descrição</th>
  </tr>
  <tr><td>&lt;input type="checkbox"&gt;</td><td>Define um botão de escolha, do tipo caixa, para seleção de VÁRIOS valores.</td></tr>
  <tr><td>&lt;input type="color"&gt;</td><td>Define um campo de entrada para escolha de cor.</td></tr>
  <tr><td>&lt;input type="date"&gt;</td><td>Define um campo de entrada do tipo data.</td></tr>
  <tr><td>&lt;input type="datetime-local"&gt;</td><td>Define um campo de entrada do tipo data e hora.</td></tr>
  <tr><td>&lt;input type="email"&gt;</td><td>Define um campo de entrada do tipo endereço de e-mail.</td></tr>
  <tr><td>&lt;input type="file"&gt;</td><td>Define um campo de seleção de arquivo e um botão "Procurar" para uploads de arquivos.</td></tr>
  <tr><td>&lt;input type="hidden"&gt;</td><td>Define um campo de entrada não visível ao usuário.</td></tr>
  <tr><td>&lt;input type="image"&gt;</td><td>Define uma imagem como botão de envio.</td></tr>
  <tr><td>&lt;input type="month"&gt;</td><td>Permite que o usuário selecione um mês e ano.</td></tr>
  <tr><td>&lt;input type="number"&gt;</td><td>Define um campo de entrada de número.</td></tr>
  <tr><td>&lt;input type="password"&gt;</td><td>Define um campo de entrada de senha.</td></tr>
  <tr><td>&lt;input type="radio"&gt;</td><td>Define um botão de escolha, do tipo rádio, para seleção de ÚNICO valor.</td></tr>
  <tr><td>&lt;input type="range"&gt;</td><td>Define um campo de entrada do tipo deslizante.</td></tr>
  <tr><td>&lt;input type="reset"&gt;</td><td>Define um botão para limpar todos os campos do formulário.</td></tr>
  <tr><td>&lt;input type="submit"&gt;</td><td>Define um botão para enviar dados de formulário.</td></tr>
  <tr><td>&lt;input type="search"&gt;</td><td>Define um campo de entrada de texto com finalidade de busca.</td></tr>
  <tr><td>&lt;input type="tel"&gt;</td><td>Campo de entrada do tipo telefone.</td></tr>
  <tr><td>&lt;input type="text"&gt;</td><td>Campo de entrada de texto de linha única.</td></tr>
  <tr><td>&lt;input type="time"&gt;</td><td>Permite que o usuário selecione um horário.</td></tr>
  <tr><td>&lt;input type="url"&gt;</td><td>Campo de entrada que deve conter um endereço de URL.</td></tr>
</table>

[Veja mais exemplos para formulário](https://github.com/marcospontoexe/HTML5-CSS3/tree/main/HTML/Material%20did%C3%A1tico/Curso%20em%20v%C3%ADdeo/11-formulario).

### Métodos para envio de dados de formulário

Para entender o envio de dados via formulário HTML, precisamos saber o que é **HTTP** e o que são **métodos de envio**. Veja as descrições a seguir.

* **HTTP**, do inglês *Hypertext Transfer Protocol*, é um protocolo de comunicação da internet que controla a transferência de hipertextos, ou documentos web. Quando inserimos uma URL na barra de endereços do navegador, estamos solicitando um documento web, via protocolo HTTP, ao site web da URL.

* **HTTPS** acrescenta a palavra “*secure*” (“segurança”, em inglês) à sigla do HTTP. Isso significa que será utilizado um certificado **SSL** (*Secure Sockets Layer*, ou camada de segurança de socket) para **criptografar**, ou codificar, todas as trocas de mensagens que trafegam pela internet, garantindo a **confidencialidade** e **autenticidade** dessas mensagens. Ou seja, o SSL mantém a segurança das conexões via HTTP e impede que criminosos leiam ou modifiquem as informações transferidas entre dois sistemas, de um modelo de aplicação cliente-servidor.

> **Resumindo**: o HTTP funciona como um protocolo de **solicitação-resposta** entre um cliente e um servidor.

O lado **servidor** da aplicação recebe solicitações via HTTP quando acionamos o botão **submit** para “envio” de dados em um formulário HTML.

Esses dados podem ser enviados de duas formas, denominadas **métodos GET** e **POST**.

* O método **GET**: utilizado para enviar dados de **solicitação-resposta** de um *cliente* para um servidor. Os dados enviados na solicitação serão acrescentados no final do endereço da URL, no formato de pares *nome/valor*. 
Veja o exemplo a seguir:
`/test/demo_form.php?name1=value1&name2=value2`
  Algumas observações sobre solicitações **GET**:
  * Permanecem no histórico do navegador.
  * Nunca devem ser usadas ao lidar com dados confidenciais.
  * Têm restrições de comprimento, pois devem caber na URL.

* Método **POST**: utilizado para enviar dados de **solicitação-resposta** de
um *cliente* para um servidor. Os dados enviados na solicitação são
armazenados no corpo da mensagem HTTP, e não na URL!
Veja o exemplo a seguir:
`POST /teste/demo_form.php HTTP/1.1`
Host: 
www.acme.com
name1=value1&name2=value2
  Algumas observações sobre solicitações **POST**:
  * Não permanecem no histórico do navegador.
  * Indicadas para lidar com dados confidenciais.
  * Não têm restrições de comprimento, pois são enviadas no corpo da mensagem, e não na URL





