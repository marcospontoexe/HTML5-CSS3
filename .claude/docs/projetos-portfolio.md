# Projetos da vitrine: estado real e restrições de layout

Verificado em 2026-09-28 contando as palavras visíveis de cada página (script em PowerShell, removendo as tags do `<body>`). **O README só deve afirmar o que foi conferido assim.** Duas vezes o README descreveu projetos sem que ninguém abrisse os arquivos (Blog e Chalé), e as descrições estavam erradas.

## Estado por projeto

| Projeto | Pasta | Páginas com conteúdo | Pendências |
|---|---|---|---|
| Museu Nacional | [04-museu](../../CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/04-museu) | 7/7 | o formulário de `contato.html` usa `method="post"`, e o GitHub Pages responde **405** ao envio (ver Convenções) |
| Café Fontenebleu | [01-Restaurante](../../HTML/Material%20did%C3%A1tico/Udemy/Desenvolvedor%20web%20completo/PROJETOS/01-Restaurante) | 7/7 | nenhuma |
| Chalé Hotel | [03-Site_Chale](../../CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/03-Site_Chale) | 5/9 | `reserva.html`, `rg.html`, `sc.html`, `pr.html` são esqueletos (1 a 4 palavras). O botão RESERVAR do cabeçalho leva a uma página vazia. O formulário de `contato.html` usa `method="post"`: envio dá erro **405** no GitHub Pages |
| Notícias Cidade | [02-site_noticias](../../CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/02-site_noticias) | home + `internacional`, `economia`, `saude`, `ciencias` (cerca de 300 palavras cada, fora a lateral; feitas em 2026-09-29) | `brasil` e `fotos` repetem basicamente a lateral e têm o rodapé em `<p>`, que fica preto sobre a barra azul. Erro de digitação no conteúdo original: "Renato ROdrigues" (lateral, replicado nas 6 páginas). O "Nova legistação" da home já foi corrigido pelo usuário |
| Blog | [01-blog](../../CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/01-blog) | 0 | vazio; **fora da vitrine** |
| Projeto padrão (Bootstrap) | [01-projeto-padrao](../../CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/BOOTSTRAP-4/PROJETOS/01-projeto-padrao) | 0 | página em branco; **fora da vitrine** |
| Spotify, Finans | BOOTSTRAP-4/PROJETOS | com conteúdo (152 e 176 palavras) | nenhuma conhecida |
| Curiosidades de Tecnologia (Android) | [01-android](../../CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/01-android) | 4/4: `android.html` (artigo), `noticias.html`, `curiosidades.html`, `fale-conosco.html` (as três últimas feitas em 2026-09-29) | nenhuma conhecida. Os erros do `android.html` original (versão do Eclair, digitação, pontuação, `<en>`, `alt` errado, `type` da imagem, fonte Bebas Neue não carregada) foram corrigidos em 2026-09-29. O link do Dan Morrill aponta para a cópia no Internet Archive, porque o site original saiu do ar. O link do Inkscape responde 403 a scripts (bloqueio anti-robô), mas o site existe |
| Cordel | Curso_em_Vídeo/desafios | com conteúdo | nenhuma |
| Astronauta | Curso_em_Vídeo/desafios | 0 palavras **de propósito**: é só composição de imagens de fundo | nenhuma |
| Rede social (iframes) | HTML/.../Desafios/13-iframe | o `<iframe>` troca entre páginas locais de 1 palavra, cada uma com um link para as redes pessoais do usuário | links pessoais (Facebook e Instagram) ficam públicos na vitrine; a decisão é do usuário |

## Restrições de layout (para não quebrar ao criar páginas)

**Chalé Hotel**
- `article#anexo` é `position: absolute` dentro de um `main` com `overflow: hidden`. A altura da página vem **só** do `#principal`, então a coluna esquerda precisa ser mais alta que a direita, senão a direita é cortada.
- `#anexo li` tem `height: 6em` e `overflow: hidden`. Títulos curtos (uma ou duas palavras) e até cerca de 18 palavras de texto por cartão.
- O cabeçalho tem de ser copiado igual ao da `home.html`. O `section#conteudo` fica **dentro do `<nav>`** (nome estranho, mas o CSS depende dele).
- `#conteudo img { width: 266; height: 164; }` não tem unidade, então o navegador ignora a regra. É inofensivo, porque a imagem real tem 226×164. **Não acrescente `px`**, senão ela distorce.

**Museu Nacional**
- `imagem1` a `imagem6.jpg` têm 93×93. Mostre no tamanho real, dentro da moldura `fundo-foto.png`.
- `#conteudo img { width: 100% }` estica qualquer imagem. As regras novas começam com `#conteudo .classe` para ganhar em especificidade.
- A página de vídeos tem um único vídeo real (`Ab3MWzld_L8`). Não invente IDs.

**Notícias Cidade**
- São 3 colunas: `aside#janela1` e `section#janela2` flutuam; o `section#janela3` não flutua, fica ao lado por `margin-left: 65%`. O `footer` tem `clear: both`.
- A aba ativa é marcada com `style="background-color: rgb(255, 67, 67);"` e `href="#"` no `<li>` da própria página.
- Nos cartões pequenos, a miniatura só flutua se estiver dentro de um `<a>` (regra `main a img`). As editorias usam listas de `<h3>` + `<p>` sem link, para não criar links novos para `#`.
- A lateral (entrevistas + newsletter) é copiada igual à da home em todas as páginas, com erros de digitação e tudo. Uma correção precisa passar pelas 6 páginas.
- O rodapé usa `<h1>`: só o `footer h1` é branco. Um `<p>` fica preto sobre a barra azul.

**Café Fontenebleu**
- O rodapé usa `<address>` fora do `<p>` (é elemento de bloco). A regra `footer address { font-style: normal }` mantém a aparência.

**Curiosidades de Tecnologia (Android)**
- A `section` aplica `text-indent: 30px`, e isso é herdado por tudo que está dentro dela. Blocos que não são parágrafo de texto (formulário, data das notícias, aviso) precisam de `text-indent: 0px`.
- O menu marca a página atual com `aria-current="page"`, estilizado por `a[aria-current="page"]`. A especificidade é menor que a de `nav > a:hover` de propósito, para o hover continuar funcionando.
- `curiosidades.html` numera os títulos com contador CSS (`counter-reset` no `article.curiosidades`, `counter-increment` no `h2::before`).
- O formulário de `fale-conosco.html` envia por `get` para `fale-conosco.html#enviado`, e a confirmação aparece pela pseudoclasse `:target`, sem JavaScript.
- As notícias e as curiosidades são **fatos reais** e verificáveis, com data (`<time datetime>`). Não inventar notícias sobre empresas reais.

## Convenções combinadas com o usuário

- Branch: `tipo/descricao-curta`, só ASCII e minúsculas (`feat/`, `fix/`, `docs/`, `chore/`).
- Commits no padrão Conventional Commits, no imperativo. Título e descrição de PR **em inglês**.
- Trabalho grande vai por branch + PR (a `main` é o site no ar). Squash só quando os commits da branch tiverem mensagens ruins.
- Conteúdo das páginas é fictício: e-mails `@<projeto>.exemplo.br`, telefones `3000-000X` e nenhum veículo de imprensa real. A exceção são páginas sobre fatos reais (como as do Android), que só podem trazer fatos verificáveis.
- **Formulários:** o GitHub Pages responde `405 Method Not Allowed` a `POST` (testado em 2026-09-29). Use `method="get"`, de preferência com uma âncora de confirmação via `:target` (modelo: `fale-conosco.html` do Android).
