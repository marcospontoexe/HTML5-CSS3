# Fundamentos de Programação Web [cite: 186]

## UNIDADE 01: Introdução ao desenvolvimento web [cite: 186]

O HTML é a linguagem fundamental para a construção de um site, estando presente em qualquer site ou sistema baseado na web[cite: 187].

### Pontos de destaque do HTML:

* Não é uma linguagem de programação, pois não permite a realização de comandos condicionais (if/else), laços de repetição (for/while) ou funções[cite: 188].
* É uma linguagem de marcação (Hypertext Markup Language = HTML) para documentos do tipo hipertexto, como as páginas web visualizadas em navegadores[cite: 189].
* Um hipertexto é um texto de leitura não linear, possibilitando o acesso a diferentes partes do documento por meio de links para outros textos ou documentos, além de incluir imagens, gráficos, vídeos, animações e áudios[cite: 190].
* No contexto do hipertexto, o HTML foi desenvolvido para estruturar o layout de um documento, organizando como textos, imagens, áudios, vídeos, etc., serão apresentados ao usuário de um site ou sistema web[cite: 191, 192].
* O navegador interpreta o HTML e renderiza seus elementos, exibindo conteúdos visuais na tela do usuário[cite: 193]. Ou seja, o navegador transforma o código HTML em uma exibição visual estruturada para interação com o usuário do site ou aplicação web[cite: 194].

Nesta unidade, iniciaremos o trabalho com a linguagem HTML, apresentando suas marcações (tags) e como utilizá-las para criar diferentes tipos de estruturação de documentos web, incluindo formatação de textos e imagens, criação de links, tabelas, listas e formulários[cite: 195].

### Em resumo: HTML [cite: 196]

* Não é linguagem de programação[cite: 197].
* É linguagem de marcação (tag) para estruturar hipertexto[cite: 197].
* É interpretada e renderizada em um navegador web[cite: 197].

Antes de ler o material, vamos conhecer melhor a proposta da disciplina e como iniciaremos nossos trabalhos com HTML[cite: 198, 199]!

## Modelo Cliente-Servidor [cite: 207]

A internet, criada por Tim Berners-Lee, é uma grande rede que conecta computadores globalmente[cite: 200]. Essa conexão permitiu o compartilhamento de documentos organizados como hipertexto[cite: 201]. A principal característica de um hipertexto é sua leitura não linear, com links para outros textos, imagens, vídeos e áudios[cite: 202].

A conexão global possibilita o desenvolvimento de sistemas distribuídos, como o modelo cliente-servidor (Figura 1)[cite: 203]. Neste modelo, uma máquina remota atua como servidor de documentos hipertexto, e uma máquina local atua como cliente, solicitando hipertextos por meio de seu endereço de rede, a URL (Uniform Resource Locator)[cite: 204]. Geralmente, a URL é inserida na barra de endereços de um navegador web para obter documentos hipertexto[cite: 205]. O navegador é o lado cliente da requisição de documentos, enquanto o computador remoto com as informações é o lado servidor de um sistema ou aplicação web[cite: 206].

Para desenvolver uma aplicação web, constrói-se um sistema distribuído com:

1.  Uma interface de usuário executada em um navegador local, que é o lado cliente (front-end) da aplicação[cite: 208].
2.  Uma aplicação executada no computador remoto, que é o lado servidor (back-end), responsável por enviar as informações solicitadas ao cliente, com base em dados de um banco de dados[cite: 209].

### Para começar a desenvolver para a web [cite: 210]

Nesta unidade, começaremos com o desenvolvimento web do lado cliente (front-end), focando na criação de uma interface visual que oriente a navegação do usuário para que ele encontre e obtenha o que precisa[cite: 210]. O ponto de partida para o desenvolvimento front-end é a formatação da estrutura de hipertextos (páginas web) usando HTML[cite: 211].

## Estrutura do documento HTML [cite: 212]

Um documento HTML é um arquivo de texto com elementos marcados usando tags[cite: 212].

### Tags [cite: 213]

As tags são delimitadas por `<` e `/>`[cite: 213]. Entre esses sinais, há o nome da tag, uma palavra reservada que indica um elemento HTML[cite: 214]. Um elemento HTML é composto por uma tag de abertura e uma tag de fechamento (Figura 2)[cite: 215].

```html
<nome elemento>Conteúdo</nome do elemento>
```

### Documento HTML, com suas tags iniciais [cite: 217]

A Figura 3 mostra a estrutura fundamental de um documento HTML, que é um arquivo de texto com extensão `.html` contendo tags de organização[cite: 218].

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8" />
    <title>Minha Página HTML</title>
  </head>
  <body>
    <p>Meu 1º. parágrafo</p>
    <p>Meu 2º. parágrafo</p>
  </body>
</html>
```

Vamos comentar as tags iniciais da Figura 3[cite: 222]:

* `<!DOCTYPE html>`: O Document Type Definition (DTD, ou Doctype) é uma tag que informa ao navegador o tipo do documento e deve ser declarada antes da tag `<html>`[cite: 222].
* `<html>` e `</html>`: Tags de abertura e fechamento do documento HTML, abrangendo todas as outras tags[cite: 223, 224].
* `<head>` e `</head>`: Tags de abertura e fechamento da seção de cabeçalho do documento HTML, declarada após a tag `<html>`[cite: 225, 226].
* `<meta charset="utf-8">`: A tag de metadados fornece informações sobre a página e seu conteúdo para o navegador, sendo invisível para os usuários[cite: 227]. Todos os metadados ficam dentro da seção de cabeçalho, delimitada pelas tags `<head>` e `</head>`[cite: 228]. A metatag `charset` é usada para indicar o conjunto de caracteres da página[cite: 229]. `utf-8` (UCS Transformation Format 8) é a codificação de caracteres mais comum na web[cite: 230].
* `<title>` e `</title>`: Definem o título da página, que é exibido na barra de título dos navegadores[cite: 231]. Também são usadas por ferramentas de busca para indexar e encontrar páginas web[cite: 232]. São tags de metadados, contidas dentro das tags `<head>` e `</head>`[cite: 233].
* `<body>` e `</body>`: Tags de abertura e fechamento do corpo do documento HTML[cite: 234]. A tag `</body>` deve ser declarada imediatamente antes da tag de fechamento do documento `</html>`[cite: 235, 236].
* `<p>` e `</p>`: Tags de abertura e fechamento de um parágrafo no documento HTML[cite: 236].

## EXPERIMENTE

### PRÁTICA: visualizando um documento web no navegador [cite: 237]

Vamos criar um documento HTML e visualizar sua interpretação (renderização) em um navegador. Além disso, vamos encontrar a ferramenta de inspeção de página do navegador Google Chrome.

Siga os passos indicados a seguir[cite: 238].

1.  Crie uma pasta de trabalho, por exemplo: `C:/Teste-HTML`[cite: 239].
2.  Dentro da pasta, crie um documento de texto com o nome `index.html`. Atenção para a extensão do arquivo: precisa ser `.html`[cite: 240]!
3.  Copie o texto a seguir para o seu arquivo `index.html`[cite: 241]:

    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <meta charset="UTF-8" />
        <title>Minha primeira página HTML</title>
      </head>
      <body>
        <h1>Primeiro cabeçalho da página</h1>
        <p>Primeiro parágrafo.</p>
        <p>Segundo parágrafo.</p>
      </body>
    </html>
    ```

4.  Abra o seu `index.html` no navegador (browser): copie o caminho completo do arquivo e cole na barra de endereços, ou barra de navegação[cite: 245].
5.  Verifique como o navegador interpretou o seu `index.html`: encontre o título da página (documento web) e verifique como o navegador pode inspecionar o HTML de todos os elementos da sua página na janela de inspeção[cite: 251].

## Utilizando o ambiente de desenvolvimento VS Code para criar páginas HTML [cite: 252]

Como mencionado, um documento HTML é um arquivo de texto que pode ser criado em qualquer editor básico de texto, como o Microsoft Notepad[cite: 252]. No entanto, para desenvolver uma aplicação web, é necessário trabalhar com várias linguagens, como JavaScript, PHP e SQL, além de HTML e CSS[cite: 253]. Com um ambiente de desenvolvimento integrado (IDE - Integrated Development Environment), há ferramentas para escrever, atualizar e depurar códigos, entre outras facilidades[cite: 254]. É recomendado trabalhar com um ambiente de desenvolvimento para codificar as primeiras páginas HTML[cite: 255]. O indicado é o VS Code, da Microsoft[cite: 256].

## HTML headings [cite: 257]

Headings são elementos HTML para cabeçalhos[cite: 257]. Eles são definidos com as tags `<h1>` a `<h6>`[cite: 257]. O `<h1>` define o cabeçalho de maior nível (mais importante), e o `<h6>` define o cabeçalho de menor nível (menos importante)[cite: 257].

### EXPERIMENTE

### PRÁTICA: cabeçalhos [cite: 258]

1.  Copie o texto a seguir para o seu arquivo `headings.html`. Depois, abra o arquivo no navegador[cite: 258].

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

## HTML imagens [cite: 261]

As imagens podem melhorar o design e a aparência de uma página da web[cite: 261]. Elas são apresentadas em um documento web com a tag `<img>` e possuem alguns atributos, como exemplificado na Figura 6[cite: 262]:

```html
<img src="figura.jpg" alt="Exemplo de figura." width="200" height="100" />
```

* **Atributo src**: especifica o caminho para a imagem[cite: 263].
* **Atributo alt**: especifica um texto alternativo para a imagem[cite: 264].
* **Atributos width e height**: especificam, respectivamente, largura e altura de uma imagem, em pixels[cite: 264].

### EXPERIMENTE

### PRÁTICA: imagens [cite: 265]

1.  Crie uma pasta com o nome `Figuras`, subordinada à sua pasta de trabalho, como no exemplo: `C:/Teste-HTML/Figuras`[cite: 265].
2.  Na pasta `Figuras`, recém-criada, salve duas imagens do tipo `.jpg` com os nomes "cavalos.jpg" e "praia.jpg"[cite: 266].
3.  Copie o texto a seguir para o seu arquivo `images.html`. Depois, abra o arquivo no navegador[cite: 267].

    ```html
    <!DOCTYPE html>
    <html>
      <body>
        <h2>HTML Image</h2>
        <img src="figuras/cavalos.jpg" alt="Passeio a cavalo." width="289" />
        <h2>HTML Image</h2>
        <img src="figuras/praia.jpg" alt="Férias na praia." width="289" />
      </body>
    </html>
    ```

## HTML Links [cite: 269]

Links são elementos HTML que permitem a ligação com outros documentos web[cite: 269]. Eles são definidos com a tag `<a>` de âncora, ou *anchor*[cite: 270]. Ao serem acionados ou clicados, os links redirecionam a página atual para outro documento referenciado na tag[cite: 271]. A tag `<a>` também possui alguns atributos, como exemplificado na Figura 8[cite: 272]:

```html
<a href="https://google.com/" title="Google" target="_blank">Site do Google</a>
```

* **href**: O atributo mais importante da tag `<a>`, pois identifica o destino do link[cite: 273].
* **title**: Texto "dica" que aparece quando o mouse se move sobre o elemento[cite: 274].
* **target**: Identifica onde abrir o documento vinculado. Pode ter os valores:
    * `_self`: Abre o documento na mesma janela/guia em que foi clicado[cite: 277].
    * `_blank`: Abre o documento em uma nova janela ou guia[cite: 278].

### EXPERIMENTE

### PRÁTICA: links [cite: 275]

1.  Copie o texto a seguir para o seu arquivo `links.html`. Depois, abra o arquivo no navegador, garantindo que as páginas `images.html` e `headings.html` da prática anterior já existam em `C:/Teste-HTML`[cite: 276].

    ```html
    <!DOCTYPE html>
    <html>
      <body>
        <h2>URLs absolutas</h2>
        <p><a href="https://google.com/" target="_blank" title="Google">Site Google</a></p>
        <p></p>
        <a href="https://pucpr.br/" target="_blank" title="PUCPR">Site PUCPR</a>
        <h2>URL relativas</h2>
        <p></p>
        <a href="images.html" title="Teste de imagens">Images</a>
        <p></p>
        <a href="headings.html" title="Teste de cabeçalhos">Headings</a>
        <h2>Link para e-mail</h2>
        <p></p>
        <a href="mailto:nome.sobrenome@site_examplo.com">Envie um e-mail</a>
      </body>
    </html>
    ```

## HTML lists [cite: 280]

É possível agrupar um conjunto de itens relacionados em uma estrutura de lista, que possui três tipos possíveis[cite: 280]:

* **Unordered HTML list (Lista não ordenada)**: Definida com as tags `<ul>` e `</ul>`, com cada item identificado pelas tags `<li>` e `</li>`[cite: 280].
* **Ordered HTML list (Lista ordenada)**: Definida com as tags `<ol>` e `</ol>`, com cada item identificado pelas tags `<li>` e `</li>`[cite: 281].
* **HTML description lists (Lista de descrição)**: Definida com as tags `<dl>` e `</dl>`, com cada item identificado pelas tags `<dt>` e `</dt>`, e sua descrição delimitada pelas tags `<dd>` e `</dd>`[cite: 282].

### EXPERIMENTE

### PRÁTICA: listas [cite: 283]

1.  Copie o texto a seguir para o seu arquivo `lists.html`. Após, abra o arquivo no navegador[cite: 283].

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
          <dd>- Bebida quente, produzida a partir dos grãos torrados do cafe</dd>
          <dt>Chá</dt>
          <dd>- Bebida quente, preparada pela infusão de folhas.</dd>
          <dt>Leite</dt>
          <dd>- Bebida gelada branca.</dd>
        </dl>
      </body>
    </html>
    ```

## IMPORTANTE

### HTML tables [cite: 287]

É possível organizar um conjunto de dados em uma estrutura de tabela, com linhas e colunas[cite: 287]. Para isso, são usadas as seguintes tags:

* `<table>` e `</table>`: Tags de início e fim de tabela[cite: 288].
* `<tr>` e `</tr>`: Tags de início e fim de linha[cite: 289].
* `<th>` e `</th>`: Tags de início e fim de coluna do tipo cabeçalho[cite: 290].
* `<td>` e `</td>`: Tags de início e fim de coluna simples[cite: 291].

### COMENTÁRIOS NOS CÓDIGOS HTML, CSS E JAVASCRIPT [cite: 292]

Comentários servem para explicar um código sem interferir na codificação, pois não são interpretados como comandos ou palavras reservadas da linguagem[cite: 292]. Para isso, precisam estar sinalizados com caracteres especiais:

* No HTML, comentários são delimitados pelos caracteres: ``[cite: 294].
* No CSS e no JavaScript, os comentários são delimitados pelos caracteres: `/*` e `*/`[cite: 295].

### A FORMATAÇÃO DE TABELAS HTML É FEITA COM CSS [cite: 296]

A formatação visual de tabelas no HTML (cores, bordas, textos, etc.) é feita com estilos CSS (Cascading Style Sheets, ou folha de estilos em cascata)[cite: 296]. O CSS é uma linguagem de formatação de conteúdo que será abordada na próxima unidade[cite: 297]. Por enquanto, será usado um pequeno trecho de CSS para formatar as bordas das tabelas de exemplo, para que sejam desenhadas na cor preta e em linha cheia de 1 pixel de largura[cite: 298]:

```html
<head>
  <style>
    /* Comentário CSS: tags "table", "th" e "td" */
    table,
    th,
    td {
      border: 1px solid black; /* borda de 1 pixel, em l */
    }
  </style>
  </head>
```

### EXPERIMENTE

### PRÁTICA: tabelas [cite: 298]

1.  Copie o texto a seguir para o seu arquivo `tables.html`. Após, abra o arquivo no navegador[cite: 299].

    ```html
    <!DOCTYPE html>
    <html>
      <head>
        <style>
          /* Comentário CSS: Os elementos HTML: */
          table,
          /* "table" (tag para iniciar tabela), */
          th,
          /* "th" (tag para coluna cabeçalho) e */
          td {
            /* "td (tag para coluna), terão como fo */
            border: 1px solid black; /* borda de 1 pixel, em linha cheia e na co */
          }
        </style>
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
            <th rowspan="3">Meses</th>
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
            <td colspan="2">R$ 180,00</td>
            </tr>
        </table>
      </body>
    </html>
    ```

Alguns atributos para as tags `<td>` e `<th>`:

* `colspan="valor"`: Define quantas células uma coluna poderá ter[cite: 305].
* `rowspan="valor"`: Define quantas células uma linha poderá ter[cite: 306].

## HTML formating [cite: 303]

O HTML define alguns elementos de formatação para exibir tipos especiais de textos:

* `<b>`: Texto em negrito[cite: 303].
* `<strong>`: Texto importante[cite: 304].
* `<i>`: Texto em itálico.
* `<em>`: Texto em destaque[cite: 304].
* `<small>`: Texto menor[cite: 307].
* `<sub>`: Texto subscrito[cite: 307].
* `<sup>`: Texto sobrescrito[cite: 307].

### EXPERIMENTE

### PRÁTICA: formating [cite: 308]

1.  Copie o texto a seguir para o seu arquivo `formating.html`. Após, abra o arquivo no navegador[cite: 308].

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

## HTML forms [cite: 310]

O elemento HTML `<form>` é utilizado para criar um formulário HTML para entrada do usuário[cite: 310]. Ele é um contêiner para diferentes tipos de elementos de entrada, como: campos de texto, caixas de seleção, botões de opção, botões de envio, etc. [cite: 311]

### EXPERIMENTE

### PRÁTICA: forms [cite: 311]

1.  Copie o texto a seguir para o seu arquivo `forms.html`. Após, abra o arquivo no navegador[cite: 312].

    ```html
    <!DOCTYPE html>
    <html>
      <body>
        <h2>Campos de entrada do tipo TEXT</h2>
        <form>
          <label for="pname">Primeiro nome:</label><br />
          <input type="text" id="pnome" name="pnome" value="João" /><br />
          <label for="uname">Último nome:</label><br />
          <input type="text" id="lnome" name="unome" value="Silva" />
        </form>
        <br />
        <b>Observe 1</b>: o formulário em si não é visível. <br />
        <b>Observe 2</b>: a largura padrão do campo de texto = <b>20</b> carac <br />
        <br />
        <hr />
        <h2>Campos de entrada do tipo RADIO BUTTON</h2>
        <p>Escolha sua linguagem web favorita:</p>
        <form>
          <input type="radio" id="html" name="fav_linguagem" value="HTML" />
          <label for="html">HTML</label><br />
          <input type="radio" id="css" name="fav_linguagem" value="CSS" />
          <label for="css">CSS</label><br />
          <input type="radio" id="javascript" name="fav_linguagem" value="Ja" />
          <label for="javascript">JavaScript</label>
        </form>
        <br />
        <hr />
        <h2>Campos de entrada do tipo CHECKBOX</h2>
        <form>
          <input type="checkbox" id="vehicle1" name="vehicle1" value="Bike" />
          <label for="vehicle1">I have a bike</label><br />
          <input type="checkbox" id="vehicle2" name="vehicle2" value="Car" />
          <label for="vehicle2">I have a car</label><br />
          <input type="checkbox" id="vehicle3" name="vehicle3" value="Boat" />
          <label for="vehicle3">I have a boat</label>
        </form>
        <br />
        <hr />
        <h2>Campos de entrada do tipo SUBMIT BUTTON</h2>
        <form action="https://www.w3schools.com/action_page.php" target="_self">
          <label for="pname">Primeiro nome:</label><br />
          <input type="text" id="pnome" name="pnome" value="Maria" /><br />
          <label for="uname">Último nome:</label><br />
          <input type="text" id="lnome" name="unome" value="Flores" /><br /><br />
          <input type="submit" value="Submit" />
        </form>
        <p>Ao clicar no botão "Submit", os dados do formulário serão enviados</p>
      </body>
    </html>
    ```

### Alguns atributos da tag `<form>` [cite: 318]

* **action**: Define a ação a ser executada quando o formulário for enviado[cite: 318].
* **target**: Identifica onde abrir o documento vinculado[cite: 319]. Pode ter os valores:
    * `_self`: Abre o documento na mesma janela/guia em que foi clicado[cite: 319].
    * `_blank`: Abre o documento em uma nova janela ou guia[cite: 320].
* **method**: Especifica qual método do protocolo HTTP será usado ao enviar os dados do formulário[cite: 321]:
    * `GET`: Os dados do formulário são enviados como variáveis de URL[cite: 321].
    * `POST`: Os dados do formulário são enviados como transação de postagem HTTP[cite: 322].
* **autocomplete**: Indica se o formulário deve ter o preenchimento automático[cite: 323].
    * `on`: Ativa o preenchimento automático[cite: 323].
    * `off`: Desativa o preenchimento automático[cite: 324].

### Alguns elementos subordinados à tag `<form>` [cite: 324]

* `<input>`: Elemento que pode ser exibido de várias maneiras, dependendo do atributo `type`[cite: 325].
    * `<input type="checkbox">`: Define um botão de escolha, do tipo caixa, para seleção de VÁRIOS valores[cite: 325].
    * `<input type="color">`: Define um campo de entrada para escolha de cor[cite: 326].
    * `<input type="date">`: Define um campo de entrada do tipo data[cite: 327].
    * `<input type="datetime-local">`: Define um campo de entrada do tipo data e hora[cite: 328].
    * `<input type="email">`: Define um campo de entrada do tipo endereço de e-mail[cite: 329].
    * `<input type="file">`: Define um campo de seleção de arquivo e um botão "Procurar" para uploads de arquivos[cite: 330].
    * `<input type="hidden">`: Define um campo de entrada não visível ao usuário[cite: 331].

## SAIBA MAIS

* `<input type="image">`: Define uma imagem como botão de envio[cite: 332].
* `<input type="month">`: Permite que o usuário selecione um mês e ano[cite: 333].
* `<input type="number">`: Define um campo de entrada numérico[cite: 334].
* `<input type="password">`: Define um campo de entrada de senha[cite: 334].
* `<input type="radio">`: Define um botão de escolha, do tipo rádio, para seleção de ÚNICO valor[cite: 335].
* `<input type="range">`: Define um campo de entrada do tipo controle deslizante[cite: 336].
* `<input type="reset">`: Define um botão para limpar todos os campos do formulário[cite: 337].
* `<input type="submit">`: Define um botão para enviar dados de formulário[cite: 337].
* `<input type="text">`: Define um campo de entrada de texto de linha única[cite: 338].
* `<input type="time">`: Permite que o usuário selecione um horário[cite: 338].
* `<input type="url">`: Campo de entrada que deve conter um endereço de URL[cite: 339].

A tabela apresenta um resumo textual para exemplificar a sintaxe de utilização do HTML para criação de formulários[cite: 339]. Ela apresenta um conjunto de atributos para a tag `<form>` e uma relação de elementos HTML subordinados à tag `<form>`, que são campos de entrada[cite: 340].

### Para você praticar mais – HTML forms [cite: 341]

Acesse: `https://www.w3schools.com/html/html_forms.asp`

### Métodos para envio de dados de formulário [cite: 341]

Para entender o envio de dados via formulário HTML, é preciso saber o que é HTTP e o que são métodos de envio[cite: 341].

* **HTTP (Hypertext Transfer Protocol)**: É um protocolo de comunicação da internet que controla a transferência de hipertextos, ou documentos web[cite: 342]. Ao inserir uma URL na barra de endereços do navegador, está-se solicitando um documento web, via protocolo HTTP, ao site web da URL[cite: 343].
* **HTTPS**: Adiciona a palavra "secure" (segurança) à sigla do HTTP[cite: 344]. Isso significa que um certificado SSL (Secure Sockets Layer) será usado para criptografar (codificar) todas as trocas de mensagens que trafegam pela internet, garantindo a confidencialidade e autenticidade dessas mensagens[cite: 345]. Ou seja, o SSL mantém a segurança das conexões via HTTP e impede que criminosos leiam ou modifiquem as informações transferidas entre dois sistemas, em um modelo de aplicação cliente-servidor[cite: 346].

Em resumo, o HTTP funciona como um protocolo de solicitação-resposta entre um cliente e um servidor[cite: 347]. O lado servidor da aplicação recebe solicitações via HTTP quando o botão "submit" é acionado para o "envio" de dados em um formulário HTML[cite: 348]. Esses dados podem ser enviados de duas formas, denominadas métodos GET e POST[cite: 349].

* **Método GET**: Utilizado para enviar dados de solicitação-resposta de um cliente para um servidor[cite: 350]. Os dados enviados na solicitação são adicionados ao final do endereço da URL, no formato de pares nome/valor[cite: 351]. Exemplo: `/test/demo_form.php?name1=value1&name2=value2`[cite: 352].
    * **Observações sobre solicitações GET**:
        * Permanecem no histórico do navegador[cite: 353].
        * Nunca devem ser usadas ao lidar com dados confidenciais[cite: 353].
        * Têm restrições de comprimento, pois devem caber na URL[cite: 354].
* **Método POST**: Utilizado para enviar dados de solicitação-resposta de um cliente para um servidor[cite: 354]. Os dados enviados na solicitação são armazenados no corpo da mensagem HTTP, e não na URL[cite: 355]! Exemplo:
    ```
    POST /teste/demo_form.php HTTP/1.1
    Host: www.acme.com
    name1=value1&name2=value2
    ```
    * **Observações sobre solicitações POST**:
        * Não permanecem no histórico do navegador[cite: 357].
        * Indicadas para lidar com dados confidenciais[cite: 357].
        * Não têm restrições de comprimento, pois são enviadas no corpo da mensagem, e não na URL[cite: 357].

## SAIBA MAIS

### PARA PRATICAR MAIS: `https://www.w3schools.com/html/html_forms.asp` [cite: 358]

### HTML no W3School [cite: 358]

O `https://www.w3schools.com/` é um site educacional voltado ao aprendizado de tecnologias web[cite: 359]. Seu conteúdo inclui tutoriais e referências relacionados a HTML, CSS, Javascript, dentre outras tecnologias[cite: 359].

Pesquise mais sobre os temas indicados a seguir:

* Tutorial HTML: `https://www.w3schools.com/html`
* HTML Forms (formulários): `https://www.w3schools.com/html/html_forms.asp`
* HTML Vídeo: `https://www.w3schools.com/html/html5_video.asp`
* HTML Áudio: `https://www.w3schools.com/html/html5_audio.asp`
* HTML YouTube: `https://www.w3schools.com/html/html_youtube.asp`

## Conclusão [cite: 361]

Acabamos de ter o primeiro contato com o desenvolvimento web[cite: 361]. Vimos que teremos duas frentes de trabalho:

* Desenvolvimento web front-end, em que trabalharemos com HTML, CSS e Javascript[cite: 362].
* Desenvolvimento web back-end, em que, dentre as várias tecnologias alternativas, trabalharemos com PHP e SQL[cite: 363].

Assim, nesta unidade, começamos com HTML, que não é linguagem de programação, mas, sim, linguagem de marcação[cite: 364]. Na próxima unidade, continuaremos no front-end, mas trabalhando para estilizar HTML com CSS[cite: 365]. Realize as práticas indicadas aqui para HTML, pois assim você aproveitará melhor nossa próxima unidade[cite: 366]!

Até!

## Referências Bibliográficas [cite: 367]

ALVES, W. P. Desenvolvimento e design de sites. São Paulo: Erica, 2014[cite: 367].

MILETTO, E. M.; BERTAGNOLLI, S. C. Desenvolvimento de software II: Introdução ao desenvolvimento web com HTML, CSS, Java Script e PHP. Porto Alegre: Bookman, 2014[cite: 368].

TERUEL, E. C. HTML 5: Guia prático. 2. ed. Porto Alegre: Bookman, 2014[cite: 369].

© PUCPR - Todos os direitos reservados.