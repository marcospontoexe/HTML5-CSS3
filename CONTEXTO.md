# CONTEXTO DA SESSÃO

- **Última atualização:** 2026-09-28 22:40
- **Sessão nº:** 1
- **Status geral:** em andamento

## 1. Objetivo da tarefa
Transformar este repositório de estudos numa vitrine de portfólio: completar os projetos, deixar o [README.md](README.md) fiel ao conteúdo real e praticar um fluxo de branch/PR que recrutadores possam ver no GitHub.

## 2. Já feito ✅
- [CLAUDE.md](CLAUDE.md) criado: guia do repositório + regra de handoff adaptada.
- [README.md](README.md) reescrito como vitrine com demos ao vivo; descrições auditadas contra o conteúdo real (Blog e Projeto padrão saíram; Notícias, Chalé e iframes corrigidos).
- Café Fontenebleu: 4 páginas criadas, `review.html` padronizado, rodapé com `<address>`, dimensões de imagem corrigidas (já na `main`).
- Museu Nacional: 6 páginas internas + CSS (branch `museu-project`, PR fundido na `main`).
- Chalé Hotel: `hist`, `imprensa`, `gast` e `contato` reescritas + bloco CSS "páginas internas" (**ainda não commitado**).
- Usuário apagou a branch `gh-pages` e a pasta `docs/`.
- [_config.yml](_config.yml) ganhou `exclude:` para [CLAUDE.md](CLAUDE.md), este arquivo e [rascunho.md](rascunho.md), que deixam de virar páginas do site (**ainda não commitado**; só vale depois do push). A seção "GitHub Pages" do [CLAUDE.md](CLAUDE.md) foi atualizada.
- Estado e restrições de cada projeto: [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md).

## 3. Em andamento 🔧
- Branch `feat-chale_Hotel-new-pages-` (criada da `main` em `7c86de6`), com alterações **não commitadas**: 4 HTML e `estilo/style.css` do [Chalé](CSS/material_didatico/Udemy/Desenvolvimento%20Web%20Completo%202022/PROJETOS/03-Site_Chale), e o [README.md](README.md).
- Próximo passo imediato: (opcional) renomear a branch para `feat/chale-hotel-paginas-internas`; depois fazer 2 commits: `feat: add inner pages to the Chalé Hotel site` (HTML + CSS) e `docs: correct project descriptions in README`.

## 4. Próximos passos (planejado) 📋
1. Abrir o PR da branch do Chalé e fundir com **Rebase and merge** (preserva os 2 commits, que desta vez têm boas mensagens).
2. Depois do push, confirmar que `https://marcospontoexe.github.io/HTML5-CSS3/CLAUDE.html` passou a responder 404.
3. Chalé: criar `reserva.html`, `rg.html`, `sc.html`, `pr.html` (numa branch própria).
4. Notícias Cidade: criar as editorias `internacional`, `economia`, `ciencias` e `saude` (numa branch própria).
5. Blog e Projeto padrão: desenvolver ou deixar fora da vitrine.
6. Montar o portfólio usando as URLs do Pages.

## 5. Decisões e raciocínio 🧠
- O Pages publica a partir de `main` / (root), então **a `main` é o site no ar**: trabalho grande passa por branch + PR.
- O README só afirma o que foi verificado pela contagem de palavras visíveis. Mais detalhes em [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md).
- Os detalhes ficam em [.claude/docs/](.claude/docs/), e não em `DOCS/`: tudo o que está na raiz é publicado pelo Pages, e o Jekyll ignora pastas que começam com ponto.
- Conteúdo fictício: não inventar IDs de YouTube nem citar veículos de imprensa reais.

## 6. Estado do projeto / ambiente
- Branch atual: `feat-chale_Hotel-new-pages-`. `main` = `origin/main` = `7c86de6`.
- Arquivos não commitados: os 4 HTML e o CSS do Chalé, [README.md](README.md), [_config.yml](_config.yml), [CLAUDE.md](CLAUDE.md), este arquivo e [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md).
- `git` **fora do PATH**: commits e PRs são feitos pela IDE e pelo GitHub web; o estado do git é lido direto em `.git`.
- Python 3.14 disponível; node/npx não.
- Site: <https://marcospontoexe.github.io/HTML5-CSS3/>. Os `.md` da raiz viram páginas públicas (`/CLAUDE.html` e `/rascunho.html` respondem 200).

## 7. Bloqueios e pendências ⚠️
- O nome da branch atual está fora do padrão. Renomear antes do primeiro commit é mais simples.
- O projeto 13-iframe expõe links do Facebook e do Instagram pessoais na vitrine. A decisão é do usuário.

## 8. Comandos úteis
- Servir um projeto localmente (embeds do YouTube falham em `file://`):
  `python -m http.server 8000 --directory "<pasta do projeto>"`
- Ver o estado do git sem o `git`: `Get-Content .git\HEAD`, a pasta `.git\refs\heads\` e o arquivo `.git\logs\HEAD`.
- Comparar um arquivo entre branches: `https://raw.githubusercontent.com/marcospontoexe/HTML5-CSS3/<branch>/<caminho>`.

## 9. Como retomar
Leia este arquivo e [.claude/docs/projetos-portfolio.md](.claude/docs/projetos-portfolio.md), confirme a branch atual em `.git\HEAD` e continue a partir da seção 3 (commits e PR do Chalé).
