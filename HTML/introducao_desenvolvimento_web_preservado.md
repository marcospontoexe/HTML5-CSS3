Fundamentos de Programação Web

**UNIDADE 01**
Introdução ao desenvolvimento web

O HTML é a linguagem fundamental para construção de um *site*.  Ela está presente em qualquer

*site* ou sistema baseado na *web*. Vamos conhecer um pouquinho mais sobre ele? Veja a seguir os

seus pontos de destaque.

Não é linguagem de programação, pois não conseguimos realizar comandos condicionais
(***if***/***else***), laços de repetição (***for***/***while***) ou funções, por exemplo.

É uma linguagem de marcação (***Hypertext Markup Language*** = **HTML**) para documentos do
tipo **hipertexto**, como são as **páginas *****web*** que visualizamos em **navegadores**, ou *browsers*.
Um **hipertexto**, por sua vez, é um texto de leitura não linear, pois podemos acessar diferentes
partes do documento por meio de *links* para outros textos ou documentos, além de incluir

imagens, gráficos, vídeos, animações e áudios nesse tipo de documento.
No contexto do hipertexto, o HTML, foi desenvolvido para **estruturar o *****layout*** de um
documento, ou seja, **estruturar dos elementos visuais** de um documento, organizando como


---

textos, imagens, áudios, vídeos etc. serão apresentados ao usuário de um *site* ou sistema
*web*.

Por fim, é o **navegador** que **interpreta **o** HTML** e **renderiza** seus elementos (ou exibe
conteúdos visuais) na tela do usuário. Em resumo, o **navegador transforma o código HTML**
**em uma exibição visual estruturada, para interagir com o usuário do *****site***** ou aplicação *****web***.

Nesta unidade, iniciaremos os trabalhos com a linguagem HTML, apresentando suas marcações,

ou *tags*, e como utilizá-las para criar diferentes tipos de estruturação de documentos *web*, com

**formatação** de **textos** e **imagens**, criação de ***links***, **tabelas**, **listas **e** formulários**.

**Em resumo: HTML**

Pesquise mais sobre os temas a seguir.

**Não **é linguagem de programação.

É linguagem de **marcação** (*tag*) para estruturar **hipertexto**.
É **interpretada** e **renderizada** em um navegador *web*.

Antes de ler o material, vamos conhecer melhor a proposta da disciplina e como iniciaremos

nossos trabalhos com HTML!

Apresentação geral da disciplina e trabalhando com HTML
Apresentação geral da disciplina e trabalhando com HTML


---

![Imagem extraída da página 3](extracted_images_preservado/page_3_img_1.jpeg)

A **internet**, criada pelo cientista britânico **Tim Berners-Lee**, é uma grande rede que conecta

computadores do mundo inteiro. A conexão global entre computadores permitiu o

compartilhamento de documentos que ganharam uma nova forma de organização, conhecida

como **hipertexto**. A principal característica de um **hipertexto** é que ele tem uma** leitura não linear**,

pois possui ligações, ou ***links***, com outros **textos**, **imagens**, **vídeos** e **áudios**.

A conexão global possibilita o desenvolvimento de **sistemas distribuídos**, em uma estrutura

conhecida como modelo **cliente-servidor **(Figura 2). Nele, uma máquina **remota** atua como

**servidor de documentos do tipo hipertexto** e uma outra máquina atua **local** como **cliente**, que

**solicita hipertextos**, fornecendo sua localização por meio do seu **endereço de rede**, também

conhecido como **URL**, do inglês *Uniform Resource Locator*, ou “localização uniforme de recurso”.

De forma geral, a **URL** é passada na **barra de endereços** de um programa do tipo **navegador *****web***,

ou *browser*, para obter documentos do tipo hipertexto. O **navegador** é conhecido, portanto, como

o lado **cliente **de uma requisição de documentos, sendo que o **computador remoto**, em que estão

as informações desejadas, é o **lado servidor** de um **sistema **ou **aplicação *****web***.

Para desenvolver uma **aplicação *****web***, construiremos um sistema distribuído que possui:

Figura 1: Modelo cliente-servidor. Fonte:©sergeyvasutin/Adobe Stock.

#ParaTodosVerem


---

![Imagem extraída da página 4](extracted_images_preservado/page_4_img_1.jpeg)

**Estrutura do documento HTML**

1. Uma **interface de usuário**, executada a partir de um **navegador** em um **computador local**,

que representa o lado **cliente** da aplicação, também conhecido como ***front-end***.

2. Uma aplicação executada no **computador remoto**, que representa o lado servidor da

aplicação, também conhecido como ***back-end***, que se encarrega de enviar ao cliente as
informações solicitadas, baseadas nos dados de um banco de dados.

**Para começar a desenvolver para a web**

Nesta unidade, iniciaremos o ***desenvolvimento web*** pelo lado **cliente**, ou ***front-end***, em que a

principal preocupação é criar uma **interface visual** que oriente a navegação do usuário na

aplicação, para permitir que ele encontre e obtenha o que precisa.

Portanto, o ponto de partida para o desenvolvimento ***front-end*** é saber realizar a formatação da

estrutura de **hipertextos**, ou **páginas *****web***, feita com a linguagem **HTML**, a ser trabalhada a seguir.

Um documento **HTML** é basicamente um arquivo **texto**, com **elementos** que são **marcados**

utilizando ***tags ***(*tag = *etiquetas).

**Tags**

As ***tags**** *são delimitadas com os sinais **<** e **/>**. Entre esses sinais, está o **nome da *****tag***, que é uma

palavra reservada, para indicar um **elemento HTML**.

Logo, um **elemento HTML** é apresentado com uma ***tag***** de abertura** e uma ***tag***** de fechamento**,

como exibido na Figura 3 a seguir.

**Documento HTML, com suas tags iniciais**

Figura 2: Elemento HTML. Fonte: Autora (2023).

#ParaTodosVerem


---

![Imagem extraída da página 5](extracted_images_preservado/page_5_img_1.jpeg)

A Figura 3, a seguir, apresenta a estrutura fundamental de um documento HTML, que nada mais é

do que um arquivo texto com extensão **.html**, em que encontramos *tags* de organização.

Vamos comentar as *tags* iniciais da Figura apresentada:

**<!DOCTYPE html>**: o *Document Type Defination* (DTD, ou simplesmente *Doctype*) é uma *tag*
que informa ao navegador qual é o tipo do documento em questão, e deve ser declarado

antes da *tag* **<html>**.
**<html>** e **</html>**: respectivamente, abertura e fechamento do documento HTML; são *tags*
que abrangem todas as demais *tags* do documento.
**<head>** e **</head>:** respectivamente, abertura e fechamento da seção de cabeçalho do

documento HTML. A seção cabeçalho deve ser declarada após a *tag* **<html>**.* *
**<meta charset="utf-8">**: a *tag *de* *metadados indica informações a respeito da página e do
conteúdo nela publicado no navegador, sendo invisíveis para os usuários. Todos os
metadados ficam contidos dentro da seção de cabeçalho, delimitada pelas *tag* **<head>** e

**</head>**. A *metatag* **charset** é usada para indicar o conjunto de caracteres que nossa página
está utilizando. No caso, indicamos uma codificação de caracteres do tipo **utf-8**: ou *UCS*
*Transformation Format 8*, a mais comum da *web*.
**<title>** e **</title>**:  define o título da página, que é exibido na barra de título dos navegadores.

Também é usada pelas ferramentas de busca da internet, para indexar e encontrar páginas
web. São *tags* de metadados, logo ficam contidos nas *tags* **<head> **e **</head>**.
**<body>** e **</body>:** respectivamente, abertura e fechamento do corpo do documento HTML;
a *tag* **</body>** deve ser declarada imediatamente antes da *tag* de fechamento de documento

Figura 3: Estrutura fundamental de um documento HTML. Fonte: Autora (2023).

#ParaTodosVerem


---

**</html>**.* *
**<p>** e **</p>:** respectivamente, abertura e fechamento de um parágrafo no documento HTML.

**PRÁTICA: visualizando um documento web no navegador**

Vamos criar um documento HTML e visualizar sua interpretação (renderização) em um navegador.

Além disso, vamos encontrar a **ferramenta de inspeção** de página do **navegador Google**

**Chrome .**

Siga os passos indicados a seguir.

1. Crie uma pasta de trabalho, como, por exemplo: **C:/Teste-HTML.**

2. Dentro da pasta, crie um documento** texto** com o nome **index.html** – atenção para a extensão

do arquivo: precisa ser **.html!**

3. Copie o texto a seguir para o seu arquivo **index.html .**

Primeiro documento HTML. Fonte: Autora (2023).

**EXPERIMENTE**

**1**

**2**

**Arquivo C:/Teste-HTML/index.html**

<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Minha primeira página HTML</title>
</head>
<body>
    <h1>Primeiro cabeçalho da página</h1>
    <p>Primeiro parágrafo. </p>
    <p>Segundo parágrafo. </p>
</body>
</html>

1
2
3
4
5
6
7
8
9
10
11
12
13
14


---

![Imagem extraída da página 7](extracted_images_preservado/page_7_img_1.jpeg)

Google Chrome: http://google.com/chrome

 Você pode utilizar um ambiente integrado de desenvolvimento, ou **IDE** – do inglês

*Integrated Development Environment* –, como o **Visual Studio Code** da Microsoft

(https://code.visualstudio.com).

4. Abra o seu **index.html** no navegador (*browser*): copie o caminho completo do arquivo e cole da

barra de endereços, ou barra de navegação.

5. Verifique como o navegador interpretou o seu **index.html:** ache o **título** da página, ou

documento web, e verifique como o navegador pode inspecionar o HTML de todos os elementos

da sua página na** janela de inspeção.**

1

2

Figura 4: Visualização do documento HTML no navegador, com janela de inspeção. Fonte: Autora (2023).

#ParaTodosVerem


---

**HTML básico**


**VS Code para criar páginas HTML**

Como acabamos de mencionar, um documento HTML é

um arquivo-texto, que pode ser criado em qualquer editor

básico de texto, como Microsoft Notepad. Contudo, para

desenvolver uma aplicação *web*, precisamos trabalhar

várias linguagens, como JavaScript, PHP e SQL, além do

HTML e CSS. Com um ambiente de desenvolvimento (IDE,

do inglês *Integrated Development Environment*), temos

ajuda para escrever, atualizar e depurar códigos, dentre

outras facilidades. Então, fica a dica: vamos trabalhar

desde já com um ambiente de desenvolvimento para

codificar nossas primeiras páginas HTML! O indicado é VS

Code, da Microsoft.

Usando um ambient
Usando um ambient

…

**HTML *****headings***

*Headings* são elementos HTML para **cabeçalhos**. Eles são definidos com as *tags* **<h1>** ao **<h6>**.

Sendo que o **<h1>** define o cabeçalho de maior nível, ou mais importante, e o **<h6>** define o

cabeçalho de menor nível, ou o menos importante.

**PRÁTICA: cabeçalhos**

1. Copie o texto a seguir para o seu arquivo **headings.html.** Após, abra o arquivo no navegador.

**EXPERIMENTE**

**Arquivo C:/Teste-HTML/headings.html**


---

![Imagem extraída da página 9](extracted_images_preservado/page_9_img_1.jpeg)

**HTML imagens**

As **imagens** podem melhorar o *design* e a aparência de uma página da *web*. Elas são apresentadas

em um documento *web* com a *tag* **<img>** e possui alguns **atributos**, como exemplificado a seguir.

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

1
2
3
4
5
6
7
8
9
10
11
12
13

Figura 5: HTML headings. Fonte: Autora (2023).

#ParaTodosVerem


---

![Imagem extraída da página 10](extracted_images_preservado/page_10_img_1.jpeg)

**PRÁTICA: imagens**

1. Crie uma pasta com o nome **Figuras**, subordinada à sua pasta de trabalho, como no exemplo:

**C:/Teste-HTML/Figuras.**

2. Na pasta **Figuras**, recém-criada, salve duas imagens, do tipo **.jpg** com os nomes **“cavalos.jpg”** e

**“praia.jpg”.**

3. Copie o texto a seguir para o seu arquivo **images.html.** Após, abra o arquivo no navegador.

Figura 6: HTML imagem: formato. Fonte: Autora (2023).

#ParaTodosVerem

**EXPERIMENTE**

**Arquivo C:/Teste-HTML/images.html**

<!DOCTYPE html>
<html>
   <body>
      <h2>HTML Image</h2>
      <img src="figuras/cavalos.jpg" alt="Passeio a cavalo." width="289" h
      <h2>HTML Image</h2>
      <img src="figuras/praia.jpg" alt="Férias na praia." width="289" heig
   </body>
</html>

1
2
3
4
5
6
7
8
9
10
11


---

![Imagem extraída da página 11](extracted_images_preservado/page_11_img_1.jpeg)

![Imagem extraída da página 11](extracted_images_preservado/page_11_img_2.jpeg)

**HTML *****Links***

*Links* são elementos HTML que permitem a **ligação** com outros documentos *web*. Eles são

definidos com a *tag* **<a> **de **âncora**, ou *anchor*, em inglês. Ao serem acionados ou clicados, os ***links***

redirecionam a página atual para outro documento referenciado na *tag*.

A *tag ***<a>** também possui alguns **atributos**, como exemplificado a seguir.

Figura 7: HTML images. Fonte: Autora (2023).

#ParaTodosVerem

**Alguns atributos da *****tag *****<**a**>**

**href**
O mais importante da *tag* **<a>**, pois identifica o destino do *link*.

**title**
Texto “dica” que aparece quando o *mouse* se move sobre o elemento.

#ParaTodosVerem


---

**PRÁTICA: links**

1. Copie o texto a seguir para o seu arquivo **links.html.** Após, abra o arquivo no navegador,

garantindo que as páginas **images.html** e **headings.html**, da prática anterior, já existam em

**C:/Teste-HTML.**

**target**

Identifica onde abrir o documento vinculado. Pode ter os valores:

_self
: Abre o documento na mesma janela/guia em que foi clicado.

_blank
: Abre o documento em uma nova janela ou guia.

Figura 8: HTML links: formato. Fonte: Autora (2023).

**EXPERIMENTE**

**Arquivo C:/Teste-HTML/links.html**

<!DOCTYPE html>
<html>
  <body>
    <h2>URLs absolutas</h2>
    <p><a href="https://google.com/" target="_blank" title="Google">Site G
    <p></p>
    <a href="https://pucpr.br/"   target="_blank" title="PUCPR">Site PUCPR
    <h2>URL relativas</h2>
    <p></p>
    <a href="images.html" title="Teste de imagens">Images</a></p>
    <p></p>
    <a href="headings.html" title="Teste de cabeçalhos">Headings</a></p>
    <h2>Link para e-mail</h2>
    <p></p>
    <a href="mailto:nome.sobrenome@site_examplo.com">Envie um e-mail</a></
  </body>
</html>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19


---

![Imagem extraída da página 13](extracted_images_preservado/page_13_img_1.jpeg)

**HTML *****lists***

Podemos agrupar um conjunto de **itens relacionados** em uma estrutura de **lista**, que possui três

tipos possíveis:

***Unordered HTML list***, ou lista não ordenada, definida com as *tags* **<ul> **e  **</ul>**, sendo cada
item identificado com as *tags* **<li> **e  **</li>**.
***Ordered HTML list***, ou lista ordenada, definida com as *tags* **<ol> **e **</ol>**, sendo cada item
identificado com as *tags* **<li> **e **</li>**.

***HTML description lists***, ou lista de descrição, definida com as *tags* **<dl> **e **</dl>**, sendo cada
item identificado com as *tags* **<dt> **e **</dt>**, com sua a descrição delimitada pelas *tags* **<dd> **e
**</dd>**.

**PRÁTICA: listas **

1. Copie o texto a seguir para o seu arquivo **lists.html**. Após, abra o arquivo no navegador.

Figura 9: HTML links. Fonte: Autora (2023).

#ParaTodosVerem

**EXPERIMENTE**


---

**Arquivo C:/Teste-HTML/lists.html**

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
        <dd>- Bebida quente, produzida a partir dos grãos torrados do cafe
        <dt>Chá</dt>
        <dd>- Bebida quente, preparada pela infusão de folhas. </dd>
        <dt>Leite</dt>
        <dd>- Bebida gelada branca. </dd>
    </dl>
</body>
</html>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28


---

![Imagem extraída da página 15](extracted_images_preservado/page_15_img_1.jpeg)

**IMPORTANTE**

**HTML *****tables***

Podemos organizar um conjunto de dados em uma estrutura de **tabela**, com **linhas** e **colunas**.

Para tanto, usamos as seguintes *tags*:

**<table> **e  **</table>**         - *Tags* de início e fim de tabela.
**<tr> **e  **</tr>**                      - *Tags* de início e fim de linha.

**<th> **e  **</th>**                    - *Tags* de início e fim de coluna do tipo cabeçalho.
**<td> **e  **</td>**                    - *Tags* de início e fim de coluna simples.

**COMENTÁRIOS NOS CÓDIGO HTML, CSS E JAVASCRIPT**

Comentários servem para explicar um código, sem interferir na codificação

propriamente dita, pois não são interpretados como comandos ou palavras

reservadas da linguagem.

Para isso, precisam estar sinalizados com caracteres especiais:

Figura 10: HTML lists. Fonte: Autora (2023).

#ParaTodosVerem


---

No HTML, comentários ficam delimitados pelos caracteres:  <!-- e -->.
No CSS e no JavaScript, os comentários são delimitados pelos

caracteres:  /* e */.

**A FORMATAÇÃO DE TABELAS HTML É FEITA COM CSS**

A formatação visual de tabelas no HTML (cores, bordas, textos etc.) é feita

com estilos CSS, de Cascate Style Sheet, ou folha de estilos em cascata. 

O CSS é uma linguagem de formatação de conteúdo, que será vista na

próxima unidade. 

Por enquanto, usaremos um pequeno trecho de CSS para formatar as

bordas das nossas tabelas-exemplo, para que sejam desenhas na cor preta e

em linha cheia de 1 pixel de largura:

**PRÁTICA: tabelas**

1. Copie o texto a seguir para o seu arquivo **tables.html.** Após, abra o arquivo no navegador.

<head>    <!-- Comentário HTML: Abre seção <head> --> 
  <style> /*   Comentário CSS: tags "table", "th" e "td"
    table, th, td {                        
      border: 1px solid black; /* borda de 1 pixel, em l
    }
  </style> <!-- Fecha a seção </style> -->
</head> <!-- Fecha a seção </head> -->

1
2
3
4
5
6
7
8
9

**EXPERIMENTE**

**Arquivo C:/Teste-HTML/tables.html**


---

<!DOCTYPE html>
<html>
<head>    <!-- Comentário HTML: SPOILER de CSS: formatando o visual de uma
  <style> /*   Comentário CSS: Os elementos HTML: */ 
    table,                     /* "table" (tag para iniciar tabela),   */
    th,                        /* "th"    (tag para coluna cabeçalho) e */
    td {                       /* "td     (tag para coluna), terão como fo
      border: 1px solid black; /* borda de 1 pixel, em linha cheia e na co
    }
  </style> <!-- Fecha a seção </style>, dentro da seção de cabeçalho do HT
</head>
</table>
<h2>Tabela Exemplo 1</h2>
<table width="60%"> <!-- Atributo width (largura) = % da tela do navegador
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

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46


---

![Imagem extraída da página 18](extracted_images_preservado/page_18_img_1.jpeg)

**HTML *****formating***

O HTML define alguns elementos de formatação para exibir tipos especiais de textos:

**<b>**                       - Texto em negrito.
**<strong>**             - Texto importante.
**<i>**                         - Texto em itálico.
**<em>**                   - Texto em destaque.

    <td>Total</td>
    <td colspan="2"> R$ 180,00</td> <!-- Faz a união de 2 COLUNAS (col) --
  </tr>
</table>
</body>
</html>

47
48
49
50
51
52
53
54

**Alguns atributos para as *****tags: *****<td> e <td>**

colspan ="valor"
Define quantas células uma **coluna** poderá ter.

rowspan ="valor"
Define quantas células uma **linha** poderá ter.

Figura 11: HTML tables. Fonte: Autora (2023).

#ParaTodosVerem


---

**<small>**               - Texto menor.
**<sub>**                   - Texto subscrito.

**<sup>**                   - Texto sobrescrito.

**PRÁTICA: formating **

1. Copie o texto a seguir para o seu arquivo **formating.html.** Após, abra o arquivo no navegador.

**EXPERIMENTE**

**Arquivo C:/Teste-HTML/formating.html**

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

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16


---

![Imagem extraída da página 20](extracted_images_preservado/page_20_img_1.jpeg)

**HTML *****forms***

O elemento HTML **<form>** é utilizado para criar um formulário HTML para entrada do usuário.

Ele é um contêiner para diferentes tipos de elementos de entrada, como: **campos de** **texto**, **caixas**

**de seleção**, **botões de opção**, **botões de envio** etc.

**PRÁTICA: *****forms***

1. Copie o texto a seguir para o seu arquivo **forms.html.** Após, abra o arquivo no navegador.

Figura 12: HTML formating. Fonte: Autora (2023).

#ParaTodosVerem

**EXPERIMENTE**


---

**Arquivo C:/Teste-HTML/forms.html**


---

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
    <b>Observe 2</b>: a largura padrão do campo de texto = <b>20</b> carac
    <br> <hr>
    <h2>Campos de entrada do tipo RADIO BUTTON</h2>
    <p>Escolha sua linguagem web favorita:</p>
    <form>
        <input type="radio" id="html" name="fav_linguagem" value="HTML">
        <label for="html">HTML</label><br>
        <input type="radio" id="css" name="fav_linguagem" value="CSS">
        <label for="css">CSS</label><br>
        <input type="radio" id="javascript" name="fav_linguagem" value="Ja
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
    <form action="https://www.w3schools.com/action_page.php" target="_self
        <label for="pname">Primeiro nome:</label><br>
        <input type="text" id="pnome" name="pnome" value="Maria"><br>
        <label for="uname">Último nome:</label><br>
        <input type="text" id="lnome" name="unome" value="Flores"><br><br>
        <input type="submit" value="Submit">
    </form>
    <p>Ao clicar no botão "Submit", os dados do formulário serão enviados 
</body>
</html>

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46


---

![Imagem extraída da página 23](extracted_images_preservado/page_23_img_1.jpeg)

47

#ParaTodosVerem


---

**Alguns atributos da *****tag***** form>**

**action**
Define a ação a ser executada quando o formulário for enviado

**target**

Identifica onde abrir o documento vinculado. Pode ter os valores:

_self
: Abre o documento na mesma janela/guia em que foi clicado.

_blank
: Abre o documento em uma nova janela ou guia.

**method**

Especifica qual método do protocolo HTTP será usado ao enviar os dados do formulário:

GET
Os dados do formulário são enviados como variáveis de URL.

POST
Os dados do formulário são enviados como transação de postagem HTTP.

**autocomplete**

Indica se formulário deve ter o preenchimento automático.

on
Ativa o preenchimento automático.

off
Desativa o preenchimento automático.

**Alguns elementos subordinados à *****tag ***** <form>**

**<input>** - **Elemento pode ser exibido de várias maneiras, dependendo do atributo type.**

**<input type="checkbox">**
Define um botão de escolha, do tipo caixa, para seleção de VÁRIOS valores.

**<input type="color">**
Define um campo de entrada para escolha de cor.

**<input type="date">**
Define um campo de entrada do tipo data.

**<input type="datetime-**

**local">**

Define um campo de entrada do tipo data e hora.

**<input type="email">**
Define um campo de entrada do tipo endereço de e-mail.

**<input type="file">**
Define um campo de seleção de arquivo e um botão "Procurar" para uploads
de arquivos.

**<input type="hidden">**
Define um campo de entrada não visível ao usuário.




---

**SAIBA MAIS**

**IMPORTANTE**

**<input type="image">**
Define uma imagem como botão de envio.

**<input type="month">  **
Permite que o usuário selecione um mês e ano.

**<input type="number">**
Define um campo de entrada numérico.

**<input type="password">**
Define um campo de entrada de senha.

**<input type="radio">**
Define um botão de escolha, do tipo rádio, para seleção de ÚNICO valor.

**<input type="range">**
Define um campo de entrada do tipo controle deslizante.

**<input type="reset">**
Define um botão para limpar todos os campos do formulário.

**<input type="submit">**
Define um botão para enviar dados de formulário

**<input type="text">**
Define um campo de entrada de texto de linha única.

**<input type="time">**
Permite que o usuário selecione um horário.

**<input type="url">**
Campo de entrada que devem conter um endereço de URL.

A tabela traz um resumo de textual para exemplificar a sintaxe de utilização do HTML para criação de formulários. Ela apresenta um
conjunto de atributos para a tag form e uma relação de elementos HTML subordinados à tag <form>, que são campos de entrada.
Fonte: Autora (2023).

**Para você praticar mais – HTML *****forms***

Acesse: https://www.w3schools.com/html/html_forms.asp

**Métodos para envio de dados de formulário**

Para entender o **envio de dados via formulário HTML,** precisamos saber o

que é **HTTP** e o que são **métodos** **de envio**. Veja as descrições a seguir.

**HTTP**, do inglês *Hypertext Transfer Protocol,* é um **protocolo de**
**comunicação da internet** que controla a **transferência de hipertextos**,
ou **documentos *****web***. Quando inserimos uma **URL** na barra de
endereços do **navegador**, estamos **solicitando um documento *****web***, via

protocolo **HTTP**, ao site *web* da URL.


---

**HTTPS**, acrescenta a palavra “*secure*” (“segurança”, em inglês) à sigla
do **HTTP**. Isso significa que será utilizado um certificado SSL (*Secure*

*Sockets Layer*, ou camada de segurança de socket) para **criptografar**, ou
codificar, todas as **trocas de mensagens** que trafegam pela internet,
garantindo a confidenciabilidade e autenticidade dessas mensagens.
Ou seja, o **SSL** mantém a segurança das conexões via HTTTP e impede

que criminosos leiam ou modifiquem as informações transferidas entre
dois sistemas, de um modelo de aplicação **cliente-servidor**.

Resumindo: o **HTTP **funciona como um **protocolo de solicitação-resposta**

entre um **cliente** e um **servidor.**

O lado **servidor** da aplicação, recebe **solicitações via HTTP** quando

acionamos o botão ***submit*** para “envio” de dados em um **formulário HTML.**

Esses dados podem ser enviados de duas formas, denominadas métodos

*GET e POST.*

**O método *****GET***: utilizado para enviar dados de **solicitação-resposta** de
um **cliente** para um servidor. Os dados enviados na solicitação serão

acrescentados no final do endereço da URL, no formato de
pares **nome/valor.** 
Veja o exemplo a seguir:
/test/demo_form.php?name1=value1&name2=value2

                Algumas observações sobre solicitações **GET:**

Permanecem no histórico do navegador.
Nunca devem ser usadas ao lidar com dados confidenciais.
Têm restrições de comprimento, pois devem caber na URL.

**Método *****POST:*** utilizado para enviar dados de** solicitação-resposta** de

um **cliente** para um servidor. Os dados enviados na solicitação são
armazenados no corpo da mensagem HTTP, e não na URL!
Veja o exemplo a seguir:
POST /teste/demo_form.php HTTP/1.1

Host: www.acme.com
name1=value1&name2=value2
Algumas observações sobre solicitações ***POST:***

Não permanecem no histórico do navegador.

Indicadas para lidar com dados confidenciais.
Não têm restrições de comprimento, pois são enviadas no corpo
da mensagem, e não na URL.


---

**SAIBA MAIS**

**Conclusão**

**PARA PRATICAR MAIS:** https://www.w3schools.com/html/html_forms.asp

**HTML no W3School**

O https://www.w3schools.com/ é um site educacional voltado ao

aprendizado de tecnologias web. Seu conteúdo inclui tutoriais e referências

relacionados a HTML, CSS, Javascript, dentre outras tecnologias.

Pesquise mais sobre os temas indicados a seguir.

Tutorial HTML: https://www.w3schools.com/html
HTML Forms (formulários):
https://www.w3schools.com/html/html_forms.asp
HTML Vídeo: https://www.w3schools.com/html/html5_video.asp

HTML Áudio: https://www.w3schools.com/html/html5_audio.asp
HTML YouTube: https://www.w3schools.com/html/html_youtube.asp

Olá!

Acabamos de ter o primeiro contato com o desenvolvimento *web*. Vimos que teremos duas frentes

de trabalho:

Desenvolvimento *web ****front-end***, em que trabalharemos com **HTML**, **CSS** e **Javascript**.
Desenvolvimento *web ****back-end***, em que, dentre as várias tecnologias alternativas,
trabalharemos com **PHP** e **SQL**.

Assim, nesta unidade, começamos com HTML, que não é linguagem de programação, mas, sim,

linguagem de marcação.

Na próxima unidade, continuaremos no *front-end*, mas trabalhando para estilizar HTML com CSS.

Realize as práticas indicadas aqui para HTML, pois assim você aproveitará melhor nossa próxima

unidade!

Até!


---

**Referências Bibliográficas**

ALVES, W. P. **Desenvolvimento e *****design***** de sites**. São Paulo: Erica, 2014.

MILETTO, E. M.; BERTAGNOLLI, S. C. **Desenvolvimento de software II**: Introdução ao

desenvolvimento web com HTML, CSS, Java Script e PHP. Porto Alegre: Bookman, 2014.

TERUEL, E. C. **HTML 5**: Guia prático. 2. ed. Porto Alegre: Bookman, 2014.

© PUCPR - Todos os direitos reservados.


---
