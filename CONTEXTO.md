# CONTEXTO DA SESSÃO

- **Última atualização:** 2026-09-29 21:40
- **Sessão nº:** 2
- **Status geral:** em andamento

## 1. Objetivo da tarefa
Transformar este repositório de estudos numa vitrine de portfólio: completar os projetos, deixar o [README.md](README.md) fiel ao conteúdo real e praticar um fluxo de branch/PR que recrutadores possam ver no GitHub.

## 2. Já feito ✅
- [CLAUDE.md](CLAUDE.md): guia do repositório + regra de handoff adaptada.
- [README.md](README.md): vitrine com demos ao vivo; as descrições foram auditadas contra o conteúdo real.
- Na `main`: Café Fontenebleu (7 páginas), Museu Nacional (7), Chalé Hotel (5 com conteúdo) e Notícias Cidade (home + 4 editorias; PR fundido em `eb54634`).
- [_config.yml](_config.yml) com `exclude:`: `/CLAUDE.html` e `/rascunho.html` respondem 404 no site.
- Curiosidades de Tecnologia (projeto 01-android): `noticias.html`, `curiosidades.html` e `fale-conosco.html` criadas, e o menu de `android.html` ligado a elas. Os erros antigos do `android.html` foram corrigidos, e a fonte Bebas Neue passou a ser carregada por `@import` no `style.css` (**tudo não commitado**).
- Estado e restrições de cada projeto: [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md).

## 3. Em andamento 🔧
- Branch `feature/new-pages-android-history` (criada da `main` em `eb54634`, ainda sem commits). Arquivos não commitados: os 3 HTML novos, `android.html` e `style/style.css` em [01-android](CSS/material_didatico/Curso_em_V%C3%ADdeo/desafios/01-android), mais [README.md](README.md), [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md) e este arquivo.
- Próximo passo imediato: commitar e abrir o PR.

## 4. Próximos passos (planejado) 📋
1. Commits e PR do projeto Android.
2. **Corrigir os formulários de contato do Museu e do Chalé**: usam `method="post"`, e o GitHub Pages responde 405 ao envio. Seguir o modelo do `fale-conosco.html` (`get` + `:target`). Fazer numa branch `fix/` própria.
3. Notícias: corrigir "Renato ROdrigues" nas 6 páginas; completar `brasil.html` e `fotos.html` (rodapé em `<p>` fica preto sobre azul).
4. Chalé: criar `reserva.html`, `rg.html`, `sc.html` e `pr.html`.
5. Blog e Projeto padrão: desenvolver ou deixar fora da vitrine.
6. Montar o portfólio usando as URLs do Pages.

## 5. Decisões e raciocínio 🧠
- O Pages publica a partir de `main` / (root), então **a `main` é o site no ar**: trabalho grande passa por branch + PR.
- O README só afirma o que foi verificado pela contagem de palavras visíveis.
- Os detalhes ficam em [.claude/docs/](.claude/docs/), não em `DOCS/`: o Jekyll ignora pastas que começam com ponto.
- Conteúdo fictício nos sites de empresas inventadas. No Android (site sobre tecnologia real), Notícias e Curiosidades trazem **só fatos reais e verificáveis**; inventar notícia sobre empresa real seria desinformação.
- Formulários usam `get`: o GitHub Pages responde 405 a `post`.
- PRs em inglês. Squash quando os commits da branch tiverem mensagens ruins.

## 6. Estado do projeto / ambiente
- Branch atual: `feature/new-pages-android-history` = `main` = `origin/main` = `eb54634`.
- Arquivos não commitados: ver seção 3.
- `git` **fora do PATH**: commits e PRs são feitos pela IDE e pelo GitHub web; o estado do git é lido direto em `.git`.
- Python 3.14 disponível; node/npx não.
- Site: <https://marcospontoexe.github.io/HTML5-CSS3/>.

## 7. Bloqueios e pendências ⚠️
- O projeto 13-iframe expõe links do Facebook e do Instagram pessoais na vitrine. A decisão é do usuário.
- Os itens 2 e 3 da seção 4 aguardam o usuário decidir quando fazer.

## 8. Comandos úteis
- Servir um projeto localmente (embeds do YouTube falham em `file://`):
  `python -m http.server 8000 --directory "<pasta do projeto>"`
- Ver o estado do git sem o `git`: `Get-Content .git\HEAD`, a pasta `.git\refs\heads\` e o arquivo `.git\logs\HEAD`.
- Comparar um arquivo entre branches ou commits: `https://raw.githubusercontent.com/marcospontoexe/HTML5-CSS3/<branch-ou-sha>/<caminho>`.
- Testar se uma página aceita `POST`: `Invoke-WebRequest -Uri "<url>" -Method Post -Body @{a='b'}` (o GitHub Pages responde 405).
- **Atenção:** trocar de branch na IDE troca os arquivos do disco. Confira `.git\HEAD` antes de concluir que algo "sumiu".

## 9. Como retomar
Leia este arquivo e [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md), confirme a branch atual em `.git\HEAD` e continue a partir da seção 3 (commits e PR do projeto Android).
